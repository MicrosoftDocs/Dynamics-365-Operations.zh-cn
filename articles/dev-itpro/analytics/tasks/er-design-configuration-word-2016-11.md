---
title: 设计 ER 配置以生成 Word 格式的报表
description: 以下步骤说明属于系统管理员或电子申报开发人员的用户如何配置电子申报格式，以便生成 Microsoft Word 文件格式的报表。
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916014"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>设计 ER 配置以生成 Word 格式的报表

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明属于系统管理员或电子申报开发人员的用户如何配置电子申报 (ER) 格式，以便生成 Microsoft Word 文件格式的报表。 这些步骤可以在 GBSI 公司执行。

为了完成这些步骤，您首先必须完成任务指南“创建用于以 OPENXML 格式生成报表的 ER 配置”中的步骤。 您还必须提前为同一个报表下载以下模板并保存到本地：

- [付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)
- [绑定付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)


此过程针对 Microsoft Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="select-the-existing-er-report-configuration"></a>选择现有 ER 报表配置
1. 在导航窗格中，转到**模块 > 组织管理 > 工作区 > 电子申报**。 确保配置提供商“Litware 公司” 已选中为有效。  
2. 单击**申报配置**。 我们将重复使用最初为生成 OPENXML 格式的报表输出而设计的现有 ER 配置。  
3. 在树结构中，展开“付款模型”。
4. 在树结构中，选择“付款模型\示例工作表报表”。
5. 单击“设计器”。

## <a name="replace-the-excel-template-with-the-word-template"></a>将 Excel 模板替换为 Word 模板

目前使用 Excel 文档作为模板生成 OPENXML 格式的输出。 我们将导入 Word 格式的报表模板。

1. 单击**附加**。 将现有 Excel 模板替换为前面下载的 Word 模板 SampleVendPaymDocReport.docx。 请注意，此模板中仅包含要作为 ER 输出生成的文档的布局。  
2. 单击**删除**。
3. 单击**是**。
4. 单击**新建**。
5. 单击**文件**。
6. 单击**浏览**。 导航到前面下载的 SampleVendPaymDocReport.docx 并选中。 单击 **确定**。 选择上一步中下载的模板。  
7. 在**模板**字段中，输入或选择一个值。

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>通过添加自定义 XML 部件扩展 Work 模板
1. 单击**保存**。 除了存储配置更改之外，“保存”操作还会更新附加的 Word 模板。 所设计格式的结构采用名称“报表”并作为新的自定义 XML 的一部分移植到附加的 Word 文档。 请注意，附加的 Word 模板中不仅包含要作为 ER 输出生成的文档的布局，还包含 ER 将在运行时填充到此模板中的数据的结构。  
2. 单击**附加**。
    + 现在需要将自定义 XML 部件“报表”的元素绑定到 Word 文档部件。  
    + 如果您熟悉可设计为包含与自定义 XML 部件的元素绑定的内容控件的窗体的 Word 文档，请执行下一个子任务的所有步骤以创建此类文档。 有关更多详细信息，请参阅[在 Words 中创建用户填写或打印的表单](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US)。 否则，请跳过下一子任务的所有步骤。  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>让包含自定义 XML 部件的 Word 执行数据绑定

在 Word 中打开此文档并执行以下操作：  
1. 打开“Word 开发人员”选项卡（如果尚未启用此选项卡，请自定义功能区）。
2. 选择“XML 映射”窗格。
3. 在查找中选择自定义 XML 部件“报表”。
4. 执行所选自定义 XML 部件的元素与 Word 文档的内容控件之间的映射。  5 将更新后的 Word 文档保存到本地驱动器。  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>上传包含绑定到内容控件的自定义 XML 部件的 Word 模板
1. 单击**删除**。
2. 单击**是**。 添加新模板。 如果完成了前面的子任务中的步骤，请选择已准备并保存到本地的 Word 文档。 否则，选择之前下载的 SampleVendPaymDocReportBounded.docx MS Word 模板。  
3. 单击**新建**。
4. 单击**文件**。
5. 单击**浏览**。 导航到前面下载的 SampleVendPaymDocReportBounded.docx 并选中。 单击 **确定**。
6. 在**模板**字段中，选择上一步中下载的文档。
7. 单击**保存**。
8. 关闭该页面。

## <a name="execute-the-format-to-create-word-output"></a>执行格式以创建 Word 输出
1. 在**操作窗格**上，单击**配置**。
2. 单击**用户参数**。
3. 在**运行设置**字段中选择“是”。
4. 单击 **确定**。
5. 单击**编辑**。
6. 在**运行草稿**字段中选择“是”。
7. 单击**保存**。
8. 关闭该页面。
9. 关闭该页面。
10. 在**导航窗格**中，转到**模块 > 应付帐款 > 付款 > 付款日记帐**。
11. 单击**行**。
12. 在列表中，标记或取消标记所有行。
13. 单击**付款状态**。
14. 单击**无**。
15. 单击**生成付款**。
16. 单击 **确定**。
17. 单击 **确定**。 分析生成的输出。 请注意，创建的输出以 Word 格式表示，并且其中包含处理的付款的详细信息。  

