---
title: "Dynamics 365 for Talent Core HR（2018 年 12 月 6 日）中的新增功能或更改的功能"
description: "此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新功能和更改的功能。"
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 09936c7161a7e303a0ada2f48ef3281b81a67295
ms.openlocfilehash: 6fae56d2feeec8e5c26fc86bdf89b8ab4c282144
ms.contentlocale: zh-cn
ms.lasthandoff: 12/10/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-6-2018"></a>Dynamics 365 for Talent Core HR（2018 年 12 月 6 日）中的新增功能或更改的功能

[!include [banner](includes/banner.md)]

**内部版本 8.1.2071**

此主题介绍了 Core HR 中的新增功能和更改的功能。


## <a name="platform-update-22"></a>平台 update 22

### <a name="export-up-to-1-million-rows-to-excel"></a>最多将 100 万行导出到 Excel

“导出到 Excel”功能现在可以配置为允许用户从 Talent 中的网格最多导出 100 万行，比之前的 10,000 行限制大幅增加。 

### <a name="restyled-personalization-toolbar"></a>改变样式的个性化工具栏

个性化工具栏已在平台更新 22 中改变样式以帮助用户更轻松地在 Talent 中定制其自己的体验。 进行了下列更改： 

-  每个个性化工具的名称现在显示有图标，可帮助用户快速识别他们有兴趣使用的工具。
-  如何使用当前工具的描述现在也会显示，将帮助用户了解如何执行需要的个性化。  
-  整个个性化工具栏可以跨屏幕移动，方法是拖放到工具栏最左侧的特定区域。 这允许用户个性化工具栏以前隐藏的元素。   

### <a name="optimized-is-one-of-filtering-experience"></a>经过优化的“之一”筛选体验

“之一”筛选运算符在使用筛选器窗格和网格标题下拉列表时对于大多数字段可用。 此运算符允许用户基于多个值筛选字段。 “之一”运算符的新的和改进的体验在平台更新 22 中提供。 若要了解更多信息，请参阅[优化的“之一”筛选体验](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering)。

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>使用“之一”运算符将列表从 Excel 粘贴到筛选器字段中

对于某些任务，用户可能有想要用于在 Talent 中筛选数据的 Excel 中的值列表。 例如，人力资源用户可能发现报表中有一组员工需要在系统中进一步研究，对于此用户，最理想的是将此列表直接从 Excel 复制到 Talent 中的筛选器字段。

从平台更新 22 开始，筛选器窗格和网格列筛选中的“之一”运算符现在识别从 Excel 复制的列表，以便可以将其直接粘贴到筛选器字段中。 这包括一组从 Excel 中的不同行和列复制的值。 若要了解有关此功能的更多信息，请参阅[使用“之一”运算符将列表从 Excel 粘贴到筛选器字段中](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel)。

## <a name="in-preview"></a>预览模式

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>配置 Talent 和 Dayforce 之间的 UK 工资单集成

Microsoft Dynamics 365 for Talent 和 Ceridian Dayforce 之间的集成在 UK 的预览中提供。 请参阅以下主题了解更多信息：[配置 Talent 和 Dayforce 之间的工资单集成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/configure-payroll-integration)。

## <a name="coming-soon"></a>即将到期

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>休假和缺勤：将来的休假和预测的休假余额

随着对允许员工预测休假和申请将来休假请求，而不会影响其当前休假余额的更改，显示休假余额的方式也在更改。 

当前显示的可用余额是包括截至今天的应计在内的可以请求的时间量，以及时间结束前的所有批准的休假请求。 

在预测功能发布时，显示的余额将更改为包括截至今天的应计和请求在内的当前休假余额。 员工和经理将在**休假**卡和**休假余额**窗口中的员工和经理自助服务中看到这些更新的余额。 HR 经理将在**人员**工作区和员工的**指定休假计划**窗口中看到这些更新的余额。

## <a name="other-changes"></a>其他更改 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>终止雇用代码不填充到工作人员职位分配记录

已经实施了更改，将在解除雇用流程期间在职位分配记录中填充原因代码。

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>对正在使用的人员编号的验证需要其他详细信息

当编号规则在使用时显示其他信息，以更好地了解不能生成新编号的问题。
 
### <a name="attachments-buttons-not-available-for-workers"></a>附件按钮对工作人员不可用

已进行更改来更正附件。 在向工作人员添加新附件时，**新建**和**编辑**按钮现在会在 FactBox 在工作人员窗口中打开时可用。 

## <a name="known-issues"></a>已知问题

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Finance and Operations 集成中的映射错误

以下问题已在用于将 Talent 与 Finance and Operations 集成的当前模板中发现。 新模板将很快发布并应用到创建的所有新集成项目中。 对于现有的集成项目，可以更新任务映射。 请参阅下表了解更新的映射。 

>[!NOTE]
> “职位到职位父作业分配”任务不集成数据。 这是当前正在研究的问题。 当前映射没有解决方法。 

“部门到运营单位”任务需要更新以下映射。

| 现有源字段          | 新源字段 |
| -------------------------------|------------------|
| cdm_description（描述）  | cdm_name（名称）  |

还需要添加其他映射。 选择上一个**无**字段添加以下映射。

| 源字段                   | 目标字段    |
| -------------------------------|----------------------|
| cdm_description（描述）  | NAMEALIAS (NAMEALIAS)|

更新的映射应如此处所示。

![“部门到运营单位”任务](./media/DepartmentMapping.png)


“作业到作业详细信息”任务需要更新以下映射。

| 现有源字段          | 新源字段                   |
| -------------------------------|------------------------------------|
| cdm_name（名称）                | cdm_description（描述）      |
| cdm_name（描述）         | cdm_jobdescription（作业描述）|


更新的映射应如此处所示。

![“作业到作业详细信息”任务](./media/JobMapping.png)

“工作人员到工作”任务需要更新以下映射。

| 现有源字段                 | 新源字段                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1（电子邮件地址 1）   | cdm_primaryemailaddress（主要电子邮件地址 |
| cdm_telephone1（电话 1）          | cdm_primarytelephone（主电话）       |

“性别”字段转换也需要更新。 为“性别”选择 **fn**（功能）映射类型并更新以下值映射。

| CDS 值   | Finance and Operations 值 | | ------------|------------------ -----------| | 75440000    | 男                         | | 75440001    | 女                       | | 75440002    | 无                         | | 75440003    | 非特定                  |

更新的映射应如此处所示。

![“工作人员到工作人员”任务](./media/WorkerMapping.png)

![“性别”字段转换](./media/WorkerTransform.png)


