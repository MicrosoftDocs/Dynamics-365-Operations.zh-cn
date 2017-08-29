--- 
title: "针对电子申报 (ER) 通过重新应用 Microsoft Excel 模板修改格式"
description: "为了完成此过程中的步骤，您首先必须完成“ER - 设计用于以 OPENXML 格式生成报表的配置”这一过程中的步骤。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c6077b8a34ba4a11df014912d8b4c2b3749bc04d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a>针对电子申报 (ER) 通过重新应用 Microsoft Excel 模板修改格式

[!include[task guide banner](../../includes/task-guide-banner.md)]

为了完成此过程中的步骤，您首先必须完成“ER - 设计用于以 OPENXML 格式生成报表的配置”这一过程中的步骤。

此过程介绍如何通过重新应用已修改的 Microsoft Excel 模板，修改电子申报 (ER) 格式配置。 在此过程中，将把一个修改后的 Excel 模板导入已为示例公司 Litware 公司创建的 ER 格式配置，然后生成电子单据。 此过程针对具有系统管理员角色或电子申报开发人员角色的用户。 可通过使用 GBSI 数据集完成这些步骤。 首先请下载并保存“通过重新应用 Excel 模板修改电子申报格式”(https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template/) 这一帮助主题中列出的文件 SampleVendPaymWsReport2.xlsx。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。 如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。  

## <a name="select-the-er-format"></a>选择 ER 格式。
1. 单击“申报配置”。
2. 在树结构中，展开“付款模型”。
3. 在树结构中，选择“付款模型\示例工作表报表”。
4. 单击“附加”。
    * 请注意，SampleVendPaymWsReport.xlsx Excel 文件当前用作处理付款日记帐的模板。   
5. 单击“打开”。
    * 单击“打开”以浏览 Excel 模板的布局。  
    * 查看模板。 请注意，其中现在包含各付款行的以下详细信息：供应商帐号、供应商名称、银行、银行代号、帐号、借方、贷方和币种。 在此示例中，我们将通过添加有关付款日期的详细信息扩展此列表。   
6. 关闭该页面。

## <a name="reapply-a-new-excel-template-to-er-format"></a>对 ER 格式重新应用新 Excel 模板。
1. 单击“设计器”。
    * 打开所选 ER 格式的草稿版本以进行编辑。  
2. 在“操作”窗格上，单击“导入”。
3. 单击“Excel 的更新”。
    * 单击“更新模板”，然后选择文件 SampleVendPaymWsReport2.xlsx。  
    * 单击“更新模板”并浏览以获取前面下载的 SampleVendPaymWsReport2.xlsx 文件。  
4. 单击“确定”。
    * 将应用模板 SampleVendPaymWsReport2.xlsx。 将把 ER 格式的结构与模板内容同步，并将后者的元素添加到该 ER 格式。 将从格式定义中删除模板中不包含，但在 ER 格式中存在的所有现有元素。  
5. 在树中，选择“Excel”。
    * 请注意，“模板”字段中现在包含对新模板的引用。   
6. 单击“附加”。
7. 单击“打开”。
    * 单击“打开”以浏览修改后的 Excel 模板的布局。  
    * 查看模板。 请注意，其中现在包含付款日期行。   
8. 关闭该页面。
9. 在树中，展开“Excel”。
10. 在树结构中，展开或折叠“Excel\付款方式行”。
11. 在树中，选择从“Excel\付款方式行\付款日期”。
    * 请注意，ER 格式中现在包含多项。 已向 Excel 添加了单元格 PaymDate。  
12. 单击“映射”选项卡。
13. 在树结构中，展开“模型”。
14. 在树结构中，展开“模型\付款”。
15. 在树结构中，选择“模型\付款\交易日期”。
16. 单击“绑定”。
    * 指定在运行时向新单元格添加哪些数据。  
17. 单击“保存”。
18. 关闭该页面。

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>启用修改后的 ER 格式草稿版本，以便在付款日记帐处理中使用。
1. 在操作窗格上，单击“配置”。
2. 单击“用户参数”。
3. 在“运行设置”字段中选择“是”。
4. 单击“确定”。
5. 单击“编辑”。
6. 在“运行草稿”字段中选择“是”。

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>将修改后的 ER 格式草稿版本用于付款日记帐处理。
    * 查看创建的工作表，包括付款日期这一付款行的新详细信息。  


