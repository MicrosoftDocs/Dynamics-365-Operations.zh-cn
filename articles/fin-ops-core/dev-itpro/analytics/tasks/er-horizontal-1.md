---
title: ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分 - 设计格式）
description: 本主题介绍如何配置电子报告 (ER) 格式以将报表生成为 OPENXML 工作表 (Excel) 文件。 （第 1 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3281f3059562fd34f9ccb71a6a11f64bf664008
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093493"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分 - 设计格式）

[!include [banner](../../includes/banner.md)]

下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。 这些步骤可以在任何公司执行。

若要完成这些步骤，首先必须完成下面的三个任务指南： 

ER 创建一个配置提供程序，并标记其为当前运行的

“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”

“ER 将财务维度用作数据源（第 2 部分：模型映射）”

您还必须下载和保存模板的本地副本，示例报表可以在这里找到：[Financial Dimensions Web 服务示例报表](https://go.microsoft.com/fwlink/?linkid=862266)。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="create-a-new-report-configuration"></a>创建新报表配置
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，选择“财务维度示例模型”。
3. 单击“创建配置”，以打开下拉对话框。
4. 在“新建”字段中，输入“格式基于数据模型财务维度示例模型”。
    * 将提前创建的模型用作新报表的数据源。  
5. 在”名称“字段中，键入”包含可水平扩展范围的示例报表“。
    * 包含可水平扩展范围的示例报表  
6. 在”描述“字段中，键入”通过动态添加列创建 Excel 输出“。
    * 通过动态添加列创建 Excel 输出  
7. 在“数据模型定义”字段中，选择“条目”。
8. 单击“创建配置”。

## <a name="design-the-report-format"></a>设计报表格式
1. 单击“设计器”。
2. 开启”显示详细信息“切换按钮。
3. 在“操作”窗格上，单击“导入”。
4. 单击“从 Excel 导入”。
5. 单击“附加”。
    * 导入报表的模板。 使用为其下载的 Excel 文件。  
6. 单击“新建”。
7. 单击“文件”。
8. 关闭该页面。
9. 在“模板”字段中，输入或选择一个值。
    * 选择下载的模板。  
10. 单击“确定”。
    * 添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。 每个列的每个单元格表示一个财务维度的名称。  
11. 单击“添加”以打开下拉对话框。
12. 在树中，选择“Excel\范围”。
13. 在“Excel 范围”字段中，键入“DimNames”。
    * DimNames  
14. 在“复制方向”字段中，选择“水平”。
15. 单击“确定”。
16. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。
17. 单击“上移”。
18. 在树中，选择“Excel = "SampleFinDimWsReport"\Cell<DimNames>”。
19. 单击“剪切”。
20. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。
21. 单击“粘贴”。
22. 在树中，展开“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。
23. 在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。
24. 在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。
25. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。
    * 添加新范围，以便使用（在用户对话框窗体中）为财务维度选择的列数量动态创建 Excel 输出。 每个列的每个单元格表示报告的每个交易的一个财务维度的值。  
26. 单击“添加范围”。
27. 在“Excel 范围”字段中，键入“DimValues”。
    * DimValues  
28. 在“复制方向”字段中，选择“水平”。
29. 单击“确定”。
30. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>”。
31. 单击“剪切”。
32. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。
33. 单击“粘贴”。
34. 在树中，展开“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。

## <a name="map-format-elements-to-data-sources"></a>将格式元素映射到数据源
1. 单击“映射”选项卡。
2. 在树中，展开“模型: 数据模型财务维度示例模型”。
3. 在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。
4. 在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。
5. 在树中，展开“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。
6. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>”。
7. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表\代码: 字符串”。
8. 单击“绑定”。
9. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal”。
10. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\维度数据: 记录列表”。
11. 单击“绑定”。
12. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>”。
13. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数”。
14. 单击“绑定”。
15. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>”。
16. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\借方: 实数”。
17. 单击“绑定”。
18. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>”。
19. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\币种: 字符串”。
20. 单击“绑定”。
21. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>”。
22. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\日期: 日期”。
23. 单击“绑定”。
24. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>”。
25. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表\贷方: 实数\凭证: 字符串”。
26. 单击“绑定”。
27. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>”。
28. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。
29. 单击“绑定”。
30. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical”。
31. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\交易: 记录列表”。
32. 单击“绑定”。
33. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>”。
34. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表\批次: 字符串”。
35. 单击“绑定”。
36. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical”。
37. 在树中，选择“模型: 数据模型财务维度示例模型\日记帐: 记录列表”。
38. 单击“绑定”。
39. 在树中，展开“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。
40. 在树中，选择“模型: 数据模型财务维度示例模型\代码: 字符串”。
41. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>”。
42. 单击“绑定”。
43. 在树中，选择“模型: 数据模型财务维度示例模型\维度设置: 记录列表”。
44. 在树中，选择“Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal”。
45. 单击“绑定”。
46. 在树中，选择“Excel = "SampleFinDimWsReport"\Cell<CompanyName>”。
47. 在树中，选择“模型: 数据模型财务维度示例模型\公司: 字符串”。
48. 单击“绑定”。
49. 单击“保存”。
50. 关闭该页面。

