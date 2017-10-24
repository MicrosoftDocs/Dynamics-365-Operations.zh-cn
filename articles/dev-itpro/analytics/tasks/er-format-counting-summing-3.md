--- 
title: "针对电子申报 (ER) 使用计算以生成用于盘点和合计的输出"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 143856f65eaf1d6d667f4f7dfb229807da6f4ad8
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a>针对电子申报 (ER) 使用计算以生成用于盘点和合计的输出

[!include[task guide banner](../../includes/task-guide-banner.md)]

以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。 这些步骤可以在任何公司执行。

必须首先完成“ER 配置格式以执行盘点和合计（第 2 部分：配置计算）”过程中的步骤，才能完成这些步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>配置此报表以使用盘点和合计信息
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树中，展开“内部统计模型”。
4. 在树中，展开“内部统计模型\内部统计 (DE)”。
5. 在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。
6. 单击“设计器”。
7. 单击“映射”选项卡。
8. 单击“添加根”以打开下拉对话框。
    * 添加新数据源以获取记忆的块列表。  
9. 在树结构中，选择“功能\计算字段”。
10. 在“名称”字段中，键入“$BlocksList”。
    * $BlocksList  
11. 单击“编辑公式”。
12. 在此该树中，选择“数据收集函数\COLLECTEDLIST”。
13. 单击“添加”功能。
14. 单击“添加数据源”。
15. 在“公式”字段中，输入“COLLECTEDLIST('$BlockName',”。
    * COLLECTEDLIST('$BlockName',  
16. 在“公式”字段中，输入“COLLECTEDLIST('$BlockName', "*")”。
    * COLLECTEDLIST('$BlockName', "*")  
17. 单击“保存”。
    * 模式“*”表示所有块都包含在此记录的列表中。  
18. 关闭该页面。
19. 单击“确定”。
20. 单击“公式”选项卡。
21. 在树结构中，选择“内部统计\数据”。
22. 单击“添加”以打开下拉对话框。
23. 在树中，选择“文本\序列”。
24. 在“名称”字段中，键入“按块的合计”。
    * 按块的总计  
25. 在"特殊字符"字段中，选择“换行 - Windows (CR LF)”。
26. 单击“确定”。
27. 在树中，选择“内部统计\数据\按块的合计”。
28. 单击“添加”以打开下拉对话框。
29. 在树结构中，选择“文本\字符串”。
30. 在“名称”字段中，键入“块代码”。
    * 块代码  
31. 单击“确定”。
32. 单击“添加字符串”。
33. 在“名称”字段中，键入“行合计”。
    * 行合计  
34. 单击“确定”。
35. 单击“添加字符串”。
36. 在“名称”字段中，键入“总金额”。
    * 总数  
37. 单击“确定”。
38. 单击“映射”选项卡。
39. 在树中，选择“$BlocksList”。
40. 单击“绑定”。
    * 为记忆的每个块创建汇总行。  
41. 单击“公式”选项卡。
42. 在树中，选择“内部统计\数据\按块的合计\块代码”。
43. 单击“映射”选项卡。
44. 单击“编辑公式”。
45. 在“公式”字段中，输如""块 id: " & '"。
    * "块 id: " &  
46. 在树中，展开“$BlocksList”。
47. 在树中，选择“$BlocksList\值”。
48. 单击“添加数据源”。
49. 单击“保存”。
50. 关闭该页面。
51. 单击“公式”选项卡。
52. 在树中，选择“内部统计\数据\按块的合计\行合计”。
53. 单击“映射”选项卡。
54. 单击“编辑公式”。
    * 为此报表中的每个块的行数创建输出。  
55. 在“公式”字段中，输入“"此块中的行数: " & ”。
    * "此块中的行数: " &  
56. 在“公式”字段中，输入“"此块中的行数: & TEXT(”。
    * "此块中的行数: " & TEXT(  
57. 在此该树中，选择“数据收集函数\COUNTIFS”。
58. 单击“添加”功能。
59. 单击“添加数据源”。
60. 在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', ”。
    * "此块中的行数: " & TEXT(COUNTIFS('$BlockName',  
61. 在树中，展开“$BlocksList”。
62. 在树中，选择“$BlocksList\值”。
63. 单击“添加数据源”。
64. 在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,”。
    * "此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. 在树中，选择“$RecName”。
66. 单击“添加数据源”。
67. 在“公式”字段中，输入“"此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))”。
    * "此块中的行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. 单击“保存”。
69. 关闭该页面。
70. 单击“公式”选项卡。
71. 在树中，选择“内部统计\数据\按块的合计\总金额”。
72. 单击“映射”选项卡。
73. 单击“编辑公式”。
    * 创建将为此报表中的每个块的开票金额总和的输出。  
74. 在“公式”字段中，输入“"开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))”。
    * "开票金额总和: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. 单击“保存”。
76. 关闭该页面。
77. 单击“保存”。
78. 关闭该页面。


