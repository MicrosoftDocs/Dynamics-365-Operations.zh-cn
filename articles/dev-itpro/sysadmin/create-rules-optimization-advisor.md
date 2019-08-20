---
title: 为优化顾问创建规则
description: 本主题讨论如何为优化顾问添加新规则。
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851413"
---
# <a name="create-rules-for-optimization-advisor"></a>为优化顾问创建规则

[!include [banner](../includes/banner.md)]

本主题介绍如何为**优化顾问**创建新规则。 例如，可创建一个新规则来识别哪些询价单 (RFQ) 案例的标题为空。 可通过案例的标题轻松识别和搜索案例。 此示例非常简单，介绍了通过优化规则可达到哪些目的。 

*规则*是对应用程序数据的检查。 如果满足规则评估的条件，将产生优化流程或改进数据的机会。 可抓住这些机会，也可以选择衡量措施的影响。 

若要为**优化顾问**创建新规则，请添加一个新类，该类用于扩展 **SelfHealingRule** 抽象类和实施 **IDiagnosticsRule** 接口，并由 **DiagnosticRule** 属性装饰。 该类还必须有一个使用 **DiagnosticsRuleSubscription** 属性装饰的方法。 按照惯例，这通过 **opportunityTitle** 方法执行，后者将在下文探讨。 这个新类将添加到依赖于 **SelfHealingRules** 方法的一个自定义模型。 在以下示例中，实施的规则称为 **RFQTitleSelfHealingRule**。

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule** 抽象类具有必须在继承类中实施的抽象方法。 核心是 **evaluate** 方法，该方法返回由规则标识的商机的列表。 商机可以按法人，也可以适用于整个系统。

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

上面显示的方法在公司间循环，并选择 **findRFQCasesWithEmptyTitle** 方法中带空标题的 RFQ 案例。 如果找到了至少一个这样的类，将使用 **getOpportunityForCompany** 方法创建公司特定的商机。 请注意，**SelfHealingOpportunity** 表中字段**数据**的类型为**容器**，因此可以包含与特定于该规则的逻辑有关的任何数据。 使用当前时间戳设置 **OpportunityDate** 将注册商机的最近评估时间。  

商机也可以跨公司。 在此情况下，不必执行公司间循环，并且必须使用 **getOpportunityAcrossCompanies** 方法创建商机。 

以下代码显示 **findRFQCasesWithEmptyTitle** 方法，用于返回具有空标题的 RFQ 案例的 ID。

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

还必须实施的两个方法是 **opportunityTitle** 和 **opportunityDetails**。 前者返回商机的短标题，后者返回商机的详细说明（其中也可以包含数据）。

**opportunityTitle** 返回的标题在**优化顾问**工作区中的**优化商机**列下显示。 还显示为侧窗格的标题，用于显示有关商机的详细信息。 按照惯例，此方法使用 **DiagnosticRuleSubscription** 属性装饰，后者采用以下自变量： 

* **诊断区域** – 类型为 **DiagnosticArea** 的枚举，用于描述规则所属的应用程序范围，如 **DiagnosticArea::SCM**。 

* **规则名称** – 包含规则名称的字符串。 这将在**诊断验证规则**窗体中的**规则名称**列下显示 (**DiagnosticsValidationRuleMaintain**)。 

* **运行频率** – 类型为 **DiagnosticRunFrequency** 的枚举，用于描述应运行规则的频率，如 **DiagnosticRunFrequency::Daily**。 

* **规则说明** – 包含规则更详细的说明的字符串。 这将在**诊断验证规则**窗体中的**规则说明**列下显示 (**DiagnosticsValidationRuleMaintain**)。 

> [!NOTE]
> 规则需要 **DiagnosticRuleSubscription** 属性才能工作。 该属性通常在 **opportunityTitle** 中使用，但是可以装饰类的任何方法。

下面是一个示例实施。 使用原始字符串是为了简单方便，但是正确的实施需要标签。 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

**opportunityDetails** 返回的说明在侧窗格中显示，用于显示有关商机的详细信息。 它采用 **SelfHealingOpportunity** 自变量，后者是可用于提供有关商机的更多详细信息的**数据**字段。 在该示例中，方法返回具有空标题的 RFQ 案例的 ID。 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

其余两个要实施的抽象方法是 **provideHealingAction** 和 **securityMenuItem**。 

如果提供了治愈操作，**provideHealingAction** 将返回 true。否则返回 false。 如果返回 true，则必须实施方法 **performAction**，否则将引发错误。 **performAction** 方法采用 **SelfHealingOpportunity** 自变量，可在其中将数据用于操作。 在该示例中，操作将打开 **PurchRFQCaseTableListPage** 以执行手动更正。 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

规则可能可以采用商机数据执行自动操作，具体取决于规则的具体内容。 在该示例中，系统可以为 RFQ 案例自动生成标题。 

**securityMenuItem** 返回操作的名称，以便只有可访问操作菜单项的用户可查看规则。 安全设置可能要求只有授权用户可访问特定规则和商机。 在该示例中，只有可访问 **PurchRFQCaseTitleAction** 的用户可查看商机。 请注意，此操作菜单项是为本示例创建，并作为 **PurchRFQCaseTableMaintain** 安全权限的进入点添加的。 

> [!NOTE]
> 此菜单项必须是操作菜单项，才能确保安全。 **显示菜单项**之类其他菜单项类型无法正确工作。

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

编译规则后，请执行以下作业，以便使其在用户界面 (UI) 中显示。

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

此规则将在**诊断验证规则**窗体（可从**系统管理** > **定期任务** > **维护诊断验证规则**访问）中显示。 若要评估该规则，请转到**系统管理** > **定期任务** > **计划诊断验证规则**，然后选择规则的频率，如**每日**。 单击**确定**。 转到**系统管理** > **优化顾问**以查看新商机。 

以下示例是带规则摘要的代码段，其中包括所有必需的方法和属性。 可帮助您熟悉如何撰写新规则。此示例中使用的标签和操作菜单项仅用于演示目的。

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

有关详细信息，请观看以下 YouTube 视频短片：[Dynamics 365 for Finance and Operations 中的优化顾问](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
