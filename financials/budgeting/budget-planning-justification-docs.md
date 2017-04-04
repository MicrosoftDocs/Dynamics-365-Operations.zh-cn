---
title: Budget planning justification documents
description: "对齐方式为请求这些文档的提供一个报告预算说明某一特定预算的原因是必需的。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budget planning justification documents

对齐方式为请求这些文档的提供一个报告预算说明某一特定预算的原因是必需的。 

预算计划模板由 Microsoft Word 中的预算经理用于创建和分配给当前预算计划流程。 预算所有者可以然后打开模板和具有在 Word 自动填充该字段：时，会基于的预算数据的请求。 他们可以在保存和将它们附加的个性化的理由文档之前然后添加附加文本或其数据到预算计划。

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Office Word 的安装 Microsoft Dynamics 外接程序

1.  打开新的 Microsoft Word 文档。
2.  **单击插入** "功能区和单击** **商店。
3.  Office 和 Microsoft Dynamics 外接程序单击"搜索** **添加。
4.  在 Word 中，在右窗格，请单击** **服务器添加信息。
5.  输入或粘贴服务器 URL 然后单击** **好。

##### <a name="define-the-justification-template-in-microsoft-word"></a>定义 Microsoft Word 中的理由模板

1.  **单击 Design ** Dynamics 在 Microsoft Office 外接程序，则登录后。
2.  对于订单头信息，请使用** **字段添加按钮。
3.  选择 BudgetPlanJustification 实体数据源，然后单击"下一步** **。 **注释：**此实体所有。理由文档所需的。 可以使用其他实体，但回 Microsoft Dynamics 365 的上载的工序将失败，则此未包括的实体。
4.  添加 BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenter 和 DocumentNumber 标签和值在 Word 文档。 **注释：**如果需要您可以使用您自定义了标记，而不是标准，标签。
5.  **单击"完成**完成部分标题。
6.  对于预算计划金额行级别详细信息，然后单击** **添加表。
7.  而且，请选择 BudgetPlanJustification 实体数据源，然后单击"下一步** **。
8.  添加 EffectiveDate、ScenarioName、AccountDisplayValue 和 AccountingCurrencyExpenseAmount 的字段。 **注释：**注释，则可用在单个预算计划内添加行，则可以在此添加到表。
9.  添加所有附加说明提供给最终用户，并执行任何所需的格式或称呼到该单据。
10. 将该文档保持到您的本地计算机然后再继续。关闭该文件。

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>设置预算计划流程使用模板对齐方式

1.  在工序的 Microsoft Dynamics 365 中，为预算** &gt; ** **设置** &gt; ** ** &gt; **预算计划文档模板**对齐方式。
2.  **单击新**和浏览到新创建您的 Microsoft Word 文档。
3.  输入模板显示名称和描述。 Click **OK**.
4.  **到预算** ** &gt; 设置的现** &gt; **预算** **计划** &gt; ** **预算计划流程。
5.  选择对齐方式模板应使用的流程和单击** **编辑。
6.  **在文档模板**对齐方式"字段中，选择相应的配置文件并保存。

##### <a name="edit-and-save-personalized-justification-documents"></a>编辑和保存个性化的理由文档

1.  在工序的 Dynamics 365，请创建一个新的预算计划或打开现有预算计划。
2.  ** **在"对齐方式"下拉菜单中，选择创建新**的理由**。
3.  在中详细信息后，从选择上载**理由**下拉菜单的个性化的填充。



