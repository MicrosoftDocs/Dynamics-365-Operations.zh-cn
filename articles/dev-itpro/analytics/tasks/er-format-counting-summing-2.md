--- 
title: "配置计算以执行盘点和合计"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d41ce101c0b038627e2baf6b5eac2410095af7ce
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="configure-computations-to-do-counting-and-summing"></a>配置计算以执行盘点和合计

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。 这些步骤可以在任何公司执行。

必须首先完成“ER 配置格式以执行盘点和合计（第 1 部分：创建格式）”过程中的步骤，才能完成这些步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>创建格式配置以添加盘点和合计详细信息
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树中，展开“内部统计模型”。
4. 在树中，选择“内部统计模型\内部统计 (DE)”。
    * 假设您需要通过在内部统计报表结尾添加包含摘要详细信息的行，自定义 Microsoft 提供的格式。 方法是从 Microsoft 实例派生自己的内部统计配置实例来进行修改。  
5. 单击“创建配置”，以打开下拉对话框。
6. 在“新建”字段中，输入“从以下名称派生: 内部统计 (DE)、Microsoft”。
7. 在“名称”字段中，键入“带盘点和合计的内部统计 (DE)”。
8. 单击“创建配置”。

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>配置此报表以基于输出详细信息执行盘点和合计。
1. 单击“设计器”。
2. 在“收集输出详细信息”字段中，选择“是”。
    * 此标记将在运行时激活收集输出详细信息的过程，以便生成内部统计文件。  
    * 您需要对不同内部统计放心执行盘点，以便向数据源的此格式配置列表添加专门的模型枚举。  
3. 单击“映射”选项卡。
4. 单击“添加根”以打开下拉对话框。
5. 在树结构中，选择“数据模型\枚举”。
6. 在“名称”字段中，键入“Direction”。
7. 在“模型枚举”字段中，输入或选择一个值。
    * 选择值“方向”。  
8. 单击“确定”。
9. 单击“添加根”以打开下拉对话框。
10. 在树结构中，选择“功能\计算字段”。
11. 在“名称”字段中，键入“$BlockName”。
12. 单击“编辑公式”。
13. 在“公式”字段中，输入“block”。
14. 单击“保存”。
15. 关闭该页面。
16. 单击“确定”。
17. 单击“添加根”以打开下拉对话框。
18. 在树结构中，选择“功能\计算字段”。
19. 在“名称”字段中，键入“$RecName”。
20. 单击“编辑公式”。
21. 在“公式”字段中，输入“record”。
22. 单击“保存”。
23. 关闭该页面。
24. 单击“确定”。
25. 单击“添加根”以打开下拉对话框。
26. 在树结构中，选择“功能\计算字段”。
27. 在“名称”字段中，键入“$InvName”。
28. 单击“编辑公式”。
29. 在“公式”字段中，输入“InvoicedAmountEUR”。
30. 单击“保存”。
31. 关闭该页面。
32. 单击“确定”。
33. 在树结构中，选择“内部统计\数据”。
34. 单击“已收集的数据键名”字段中的“编辑”按钮
35. 单击“添加数据源”。
    * $BlockName  
36. 单击“保存”。
37. 关闭该页面。
38. 单击“已收集的数据键值”字段中的“编辑”按钮。
39. 在“公式”字段中，输入“IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”。
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. 单击“保存”。
41. 关闭该页面。
    * 统计此序列的行数。 结果将与名称“block”一起单独用于不同方向。 值“Import”将用于任何到货内部统计交易。 值“Export”将用于任何内部统计发货交易。 请将其视为虚拟 Excel 电子表格。 对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。  
42. 在树中，展开“内部统计\数据: 序列”。
43. 在树中，选择“内部统计\数据: 序列\到货?”。
44. 单击“已收集的数据键名”字段中的“编辑”按钮。
    * 统计此序列的行数。 将使用名称“记录”记忆结果。  
45. 在树中，选择“$RecName”。
46. 单击“添加数据源”。
47. 单击“保存”。
48. 关闭该页面。
49. 单击“已收集的数据键值”字段中的“编辑”按钮
50. 在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。
51. 单击“保存”。
52. 关闭该页面。
    * 统计此序列的行数。 结果将与名称“record”一起单独用于不同商品代码。 请将其视为虚拟 Excel 电子表格。 对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”且第二个块“record”填充了商品代码值的行。  
53. 在树中，选择“内部统计\数据: 序列\发货?”。
54. 单击“已收集的数据键名”字段中的“编辑”按钮
55. 在树中，选择“$RecName”。
56. 单击“添加数据源”。
57. 单击“保存”。
58. 关闭该页面。
59. 单击“已收集的数据键值”字段中的“编辑”按钮。
60. 在公式"字段中，输入“Intrastat.CommodityRecord.CommodityCode”。
61. 单击“保存”。
62. 关闭该页面。
63. 在树中，展开“内部统计\数据: 序列\发货: 序列?”。
64. 在树中，展开“内部统计\数据: 序列\发货: 序列?\Record = Intrastat.CommodityRecord”。
65. 单击“公式”选项卡。
66. 在树中，选择“内部统计\数据\发货\记录\发票金额 EUR”。
67. 单击“映射”选项卡。
68. 单击“已收集的数据键名”字段中的“编辑”按钮。
69. 在树中，选择“$InvName”。
70. 单击“添加数据源”。
71. 单击“保存”。
72. 关闭该页面。
    * 汇总此序列的行的开票金额值。 结果将与名称“InvoicedAmountEUR”一起单独用于不同内部统计方向和商品代码。 请将其视为 Excel 电子表格中的虚拟创建。 对于每笔交易，为第一个列“block”相应填充了值“Import”和“Export”的行。 第二个块“record”填充了商品代码值，第三个列“InvoicedAmountEUR”则填充了发票金额值。  
73. 在树中，展开“内部统计\数据\到货?”。
74. 在树中，展开“内部统计\数据: 序列\到货?\Record = Intrastat.CommodityRecord”。
75. 单击“公式”选项卡。
76. 在树中，选择“内部统计\数据\到货\记录\发票金额 EUR”。
77. 单击“映射”选项卡。
78. 单击“已收集的数据键名”字段中的“编辑”按钮。
79. 在树中，选择“$InvName”。
80. 单击“添加数据源”。
81. 单击“保存”。
82. 关闭该页面。
83. 单击“保存”。
84. 关闭该页面。


