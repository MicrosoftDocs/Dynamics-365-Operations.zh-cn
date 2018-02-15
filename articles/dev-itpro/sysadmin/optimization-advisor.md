---
title: "为优化顾问创建规则"
description: "本主题讨论如何为优化顾问添加新规则。"
author: roxanadiaconu
manager: AnnBe
ms.date: 01/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 9cb9343028acacc387370e1cdd2202b84919185e
ms.openlocfilehash: 88739298405343a36ae5bc11f51c666c414e7157
ms.contentlocale: zh-cn
ms.lasthandoff: 01/23/2018

---

# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="ccf99-103">为优化顾问创建规则</span><span class="sxs-lookup"><span data-stu-id="ccf99-103">Create rules for Optimization advisor</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ccf99-104">本主题介绍如何为**优化顾问**创建新规则。</span><span class="sxs-lookup"><span data-stu-id="ccf99-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="ccf99-105">例如，可创建一个新规则来识别哪些询价单 (RFQ) 案例的标题为空。</span><span class="sxs-lookup"><span data-stu-id="ccf99-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="ccf99-106">可通过案例的标题轻松识别和搜索案例。</span><span class="sxs-lookup"><span data-stu-id="ccf99-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="ccf99-107">此示例非常简单，介绍了通过优化规则可达到哪些目的。</span><span class="sxs-lookup"><span data-stu-id="ccf99-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="ccf99-108">*规则*是对应用程序数据的检查。</span><span class="sxs-lookup"><span data-stu-id="ccf99-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="ccf99-109">如果满足规则评估的条件，将产生优化流程或改进数据的机会。</span><span class="sxs-lookup"><span data-stu-id="ccf99-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="ccf99-110">可抓住这些机会，也可以选择衡量措施的影响。</span><span class="sxs-lookup"><span data-stu-id="ccf99-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="ccf99-111">若要为**优化顾问**创建新规则，请添加一个新类，该类用于扩展 **SelfHealingRule** 抽象类和实施 **IDiagnosticsRule** 接口，并由 **DiagnosticRule** 属性装饰。</span><span class="sxs-lookup"><span data-stu-id="ccf99-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="ccf99-112">该类还必须有一个使用 **DiagnosticsRuleSubscription** 属性装饰的方法。</span><span class="sxs-lookup"><span data-stu-id="ccf99-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="ccf99-113">按照惯例，这通过 **opportunityTitle** 方法执行，后者将在下文探讨。</span><span class="sxs-lookup"><span data-stu-id="ccf99-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="ccf99-114">这个新类将添加到依赖于 **SelfHealingRules** 方法的一个自定义模型。</span><span class="sxs-lookup"><span data-stu-id="ccf99-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="ccf99-115">在以下示例中，实施的规则称为 **RFQTitleSelfHealingRule**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="ccf99-116">**SelfHealingRule** 抽象类具有必须在继承类中实施的抽象方法。</span><span class="sxs-lookup"><span data-stu-id="ccf99-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="ccf99-117">核心是 **evaluate** 方法，该方法返回由规则标识的商机的列表。</span><span class="sxs-lookup"><span data-stu-id="ccf99-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="ccf99-118">商机可以按法人，也可以适用于整个系统。</span><span class="sxs-lookup"><span data-stu-id="ccf99-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

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

<span data-ttu-id="ccf99-119">上面显示的方法在公司间循环，并选择 **findRFQCasesWithEmptyTitle** 方法中带空标题的 RFQ 案例。</span><span class="sxs-lookup"><span data-stu-id="ccf99-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="ccf99-120">如果找到了至少一个这样的类，将使用 **getOpportunityForCompany** 方法创建公司特定的商机。</span><span class="sxs-lookup"><span data-stu-id="ccf99-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="ccf99-121">请注意，**SelfHealingOpportunity** 表中字段**数据**的类型为**容器**，因此可以包含与特定于该规则的逻辑有关的任何数据。</span><span class="sxs-lookup"><span data-stu-id="ccf99-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="ccf99-122">使用当前时间戳设置 **OpportunityDate** 将注册商机的最近评估时间。</span><span class="sxs-lookup"><span data-stu-id="ccf99-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="ccf99-123">商机也可以跨公司。</span><span class="sxs-lookup"><span data-stu-id="ccf99-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="ccf99-124">在此情况下，不必执行公司间循环，并且必须使用 **getOpportunityAcrossCompanies** 方法创建商机。</span><span class="sxs-lookup"><span data-stu-id="ccf99-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="ccf99-125">以下代码显示 **findRFQCasesWithEmptyTitle** 方法，用于返回具有空标题的 RFQ 案例的 ID。</span><span class="sxs-lookup"><span data-stu-id="ccf99-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

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

<span data-ttu-id="ccf99-126">还必须实施的两个方法是 **opportunityTitle** 和 **opportunityDetails**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="ccf99-127">前者返回商机的短标题，后者返回商机的详细说明（其中也可以包含数据）。</span><span class="sxs-lookup"><span data-stu-id="ccf99-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="ccf99-128">**opportunityTitle** 返回的标题在**优化顾问**工作区中的**优化商机**列下显示。</span><span class="sxs-lookup"><span data-stu-id="ccf99-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="ccf99-129">还显示为侧窗格的标题，用于显示有关商机的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ccf99-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="ccf99-130">按照惯例，此方法使用 **DiagnosticRuleSubscription** 属性装饰，后者采用以下自变量：</span><span class="sxs-lookup"><span data-stu-id="ccf99-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="ccf99-131">**诊断区域** – 类型为 **DiagnosticArea** 的枚举，用于描述规则所属的应用程序范围，如 **DiagnosticArea::SCM**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="ccf99-132">**规则名称** – 包含规则名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccf99-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="ccf99-133">这将在**诊断验证规则**窗体中的**规则名称**列下显示 (**DiagnosticsValidationRuleMaintain**)。</span><span class="sxs-lookup"><span data-stu-id="ccf99-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="ccf99-134">**运行频率** – 类型为 **DiagnosticRunFrequency** 的枚举，用于描述应运行规则的频率，如 **DiagnosticRunFrequency::Daily**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="ccf99-135">**规则说明** – 包含规则更详细的说明的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccf99-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="ccf99-136">这将在**诊断验证规则**窗体中的**规则说明**列下显示 (**DiagnosticsValidationRuleMaintain**)。</span><span class="sxs-lookup"><span data-stu-id="ccf99-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="ccf99-137">规则需要 **DiagnosticRuleSubscription** 属性才能工作。</span><span class="sxs-lookup"><span data-stu-id="ccf99-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="ccf99-138">该属性通常在 **opportunityTitle** 中使用，但是可以装饰类的任何方法。</span><span class="sxs-lookup"><span data-stu-id="ccf99-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="ccf99-139">下面是一个示例实施。</span><span class="sxs-lookup"><span data-stu-id="ccf99-139">The following is an example implementation.</span></span> <span data-ttu-id="ccf99-140">使用原始字符串是为了简单方便，但是正确的实施需要标签。</span><span class="sxs-lookup"><span data-stu-id="ccf99-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

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

<span data-ttu-id="ccf99-141">**opportunityDetails** 返回的说明在侧窗格中显示，用于显示有关商机的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ccf99-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="ccf99-142">它采用 **SelfHealingOpportunity** 自变量，后者是可用于提供有关商机的更多详细信息的**数据**字段。</span><span class="sxs-lookup"><span data-stu-id="ccf99-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="ccf99-143">在该示例中，方法返回具有空标题的 RFQ 案例的 ID。</span><span class="sxs-lookup"><span data-stu-id="ccf99-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

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

<span data-ttu-id="ccf99-144">其余两个要实施的抽象方法是 **provideHealingAction** 和 **securityMenuItem**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="ccf99-145">如果提供了治愈操作，**provideHealingAction** 将返回 true。否则返回 false。</span><span class="sxs-lookup"><span data-stu-id="ccf99-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="ccf99-146">如果返回 true，则必须实施方法 **performAction**，否则将引发错误。</span><span class="sxs-lookup"><span data-stu-id="ccf99-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="ccf99-147">**performAction** 方法采用 **SelfHealingOpportunity** 自变量，可在其中将数据用于操作。</span><span class="sxs-lookup"><span data-stu-id="ccf99-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="ccf99-148">在该示例中，操作将打开 **PurchRFQCaseTableListPage** 以执行手动更正。</span><span class="sxs-lookup"><span data-stu-id="ccf99-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

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

<span data-ttu-id="ccf99-149">规则可能可以采用商机数据执行自动操作，具体取决于规则的具体内容。</span><span class="sxs-lookup"><span data-stu-id="ccf99-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="ccf99-150">在该示例中，系统可以为 RFQ 案例自动生成标题。</span><span class="sxs-lookup"><span data-stu-id="ccf99-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="ccf99-151">**securityMenuItem** 返回操作的名称，以便只有可访问操作菜单项的用户可查看规则。</span><span class="sxs-lookup"><span data-stu-id="ccf99-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="ccf99-152">安全设置可能要求只有授权用户可访问特定规则和商机。</span><span class="sxs-lookup"><span data-stu-id="ccf99-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="ccf99-153">在该示例中，只有可访问 **PurchRFQCaseTitleAction** 的用户可查看商机。</span><span class="sxs-lookup"><span data-stu-id="ccf99-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="ccf99-154">请注意，此操作菜单项是为本示例创建，并作为 **PurchRFQCaseTableMaintain** 安全权限的进入点添加的。</span><span class="sxs-lookup"><span data-stu-id="ccf99-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="ccf99-155">编译规则后，请执行以下作业，以便使其在用户界面 (UI) 中显示。</span><span class="sxs-lookup"><span data-stu-id="ccf99-155">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

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

<span data-ttu-id="ccf99-156">此规则将在**诊断验证规则**窗体（可从**系统管理** > **定期任务** > **维护诊断验证规则**访问）中显示。</span><span class="sxs-lookup"><span data-stu-id="ccf99-156">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="ccf99-157">若要评估该规则，请转到**系统管理** > **定期任务** > **计划诊断验证规则**，然后选择规则的频率，如**每日**。</span><span class="sxs-lookup"><span data-stu-id="ccf99-157">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="ccf99-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccf99-158">Click **OK**.</span></span> <span data-ttu-id="ccf99-159">转到**系统管理** > **优化顾问**以查看新商机。</span><span class="sxs-lookup"><span data-stu-id="ccf99-159">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="ccf99-160">有关详细信息，请观看 YouTube 短视频：</span><span class="sxs-lookup"><span data-stu-id="ccf99-160">For more information, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

