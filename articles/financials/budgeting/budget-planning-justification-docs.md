---
title: 预算计划理由文档
description: 理由文档让请求预算的人员可以说明为何必须获得特定预算。
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cae6334cd39a91eaf3a2a79f30edc705f484bc8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "333568"
---
# <a name="budget-planning-justification-documents"></a>预算计划理由文档

[!include [banner](../includes/banner.md)]

理由文档让请求预算的人员可以说明为何必须获得特定预算。 

预算计划模板由预算经理在 Microsoft Word 中创建，并分配给当前预算计划流程。 然后，预算所有者可以打开该模板，并根据预算请求在 Word 中自动填充数据。 保存个性化理由文档并附加到预算计划之前，可以添加更多文本或数据。

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>设置 Microsoft Word 的 Microsoft Dynamics Office 加载项

1.  打开新 Microsoft Word 文档。
2.  单击功能区中的**插入**，然后单击**应用商店**。
3.  搜索 Microsoft Dynamics Office 加载项，然后单击**添加**。
4.  在 Word 的右窗格中，单击**添加服务器信息**。
5.  输入或粘贴服务器 URL，然后单击**确定**。

##### <a name="define-the-justification-template-in-microsoft-word"></a>在 Microsoft Word 中定义理由模板

1.  登录后，单击 Microsoft Dynamics Office 加载项中的**设计**。
2.  对于标题信息，请使用**添加字段**按钮。
3.  选择实体数据源 BudgetPlanJustification，然后单击**下一步**。 **注释：** 所有理由文档都需要此实体。 可以使用其他实体，但是如果不包含此实体，上传回 Microsoft Dynamics 365 for Finance and Operations 将失败。
4.  在 Word 文档中添加 BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenter 和 DocumentNumber 标签和值。 **注释：** 如果需要，您可以使用之间的自定义标签，而不是标准标签。
5.  单击**完成**完成标题部分。
6.  对于预算计划金额的行级别详细信息，请单击**添加表**。
7.  再次选择实体数据源 BudgetPlanJustification，然后单击**下一步**。
8.  为 EffectiveDate、ScenarioName、AccountDisplayValue 和 AccountingCurrencyExpenseAmount 添加标签。 **注释：** 如果可以在单个预算计划行内添加注释，可以在此处将其添加到表。
9.  添加任何附加说明以提供给最终用户，并对文档执行任何必要的格式或样式设置。
10. 将该文档保持到您的本地计算机，然后在继续操作之前关闭该文件。

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>设置预算计划流程以使用理由模板

1.  在 Finance and Operations 中，转至**预算编制** &gt; **设置** &gt; **预算计划** &gt; **理由文档模板**。
2.  单击**新建**并浏览至新创建的 Microsoft Word 文档。
3.  输入模板显示名称和描述。 单击**确定**。
4.  转至**预算编制** &gt; **设置** &gt; **预算** **计划** &gt; **预算计划流程**。
5.  选择应使用理由模板的流程，然后单击**编辑**。
6.  在**理由文档模板**字段中，选择相应模板并保存。

##### <a name="edit-and-save-personalized-justification-documents"></a>编辑并保存个性化的理由文档

1.  在 Finance and Operations 中，新建预算计划或打开现有预算计划。
2.  在**理由**下拉菜单中，选择**创建新理由**。
3.  填写详细信息之后，选择从**理由**下拉菜单上传个性化的文档。




