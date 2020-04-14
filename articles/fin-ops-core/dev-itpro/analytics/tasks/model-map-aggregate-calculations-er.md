---
title: 使用模型映射配置在数据库级别执行聚合计算
description: 此过程提供有关如何设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0912b620fc70f8ed33e336da9ecefacd1f4e376e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143169"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>使用模型映射配置在数据库级别执行聚合计算

[!include [banner](../../includes/banner.md)]

此过程提供有关如何设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。 在此过程中，您将创建示例公司“Litware 公司”的配置。 

此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 可使用任何数据集完成这些步骤。

 为了完成这些步骤，您必须首先完成“ER 通过在数据库级别执行聚合计算改进这些计算的效率（第 1 部分：准备配置）”这一过程中的步骤。

1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“内部统计模型”。
3. 在树中，选择“内部统计模型\内部统计示例映射”。
4. 单击“设计器”。
5. 单击“设计器”。
6. 在树中，选择“Dynamics 365 for Operations\表记录”'。
7. 单击“添加根”。
    * 添加表示您要分组的记录的新数据源。  
8. 在“名称”字段中，键入“交易记录”。
    * 交易  
9. 在“表”字段中，键入“内部统计”。
    * 内部统计  
10. 单击“确定”。
11. 在树结构中，选择“功能\分组依据”。
    * 此数据源类型用于在运行时引入新数据源以分组记录、计算所需的合并。  
12. 单击“添加根”。
13. 在“名称”字段中，键入“TransactionsGroups”。
    * TransactionsGroups  
14. 单击“编辑分组依据”。
15. 在树结构中，选择“交易记录”。
    * 选择表示您要分组的记录的“记录列表”类型的已添加数据源。  
16. 单击“将字段添加到”。
17. 单击“什么要分组”。
18. 在树结构中，展开“交易记录”。
19. 在树结构中，选择“交易记录\指令”。
20. 单击“将字段添加到”。
21. 单击“分组字段”。
    * 选择字段以指定分组级别。 基于此选择，数据源将在运行时返回与将在内部统计表中达到的指令代码数量同样多的交易记录组。  
22. 在树中，选择“Transactions\Invoice amount(AmountMST)”。
    * 选择字段以指定合并计算的源。  
23. 单击“将字段添加到”。
24. 单击“合并字段”。
25. 在列表中，标记所选的行。
26. 在“方法”字段中选择“求和”。
    * 选择合并类型。  
27. 在“名称”字段中键入“SumOfAmountMST”。
    * 在配置的数据源中指定此合并的名称。  
28. 单击“保存”。
    * 请注意，“执行位置”字段指示此分组将在运行时在 SQL 数据库中执行。  
29. 关闭该页面。
30. 单击“确定”。
31. 在树中，展开“合计”。
32. 在树中，展开“TransactionsGroups”。
33. 在树结构中，展开“TransactionsGroups\aggregated”。
34. 在树中，选择“TransactionsGroups\aggregated\SumOfAmountMST”。
35. 在树中，选择“Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')”。
36. 单击“绑定”。
    * 基于此设置，此数据源将计算每个交易记录组的“AmountMST”字段值的总和。 此合并计算可作为 TransactionsGroups.aggregated.TotalAmount 项目提供。  
37. 在树中，展开“TransactionsGroups”。
38. 在树中，选择“TransactionsGroups”。
39. 单击“编辑”。
40. 单击“编辑分组依据”。
41. 在树结构中，展开“交易记录”。
42. 在树中，选择“Transactions\Invoice amount(AmountMST)”。
43. 单击“将字段添加到”。
44. 单击“合并字段”。
45. 在列表中，标记所选的行。
46. 在“方法”字段中选择“最大值”。
47. 在“名称”字段中键入“MaxOfAmountMST”。
48. 单击“保存”。
    * 目前，GROUPBY 数据源的执行可以转换到具有某些限制的 SQL 数据库级别。 转换可用于“记录列表”类型的数据源或表示为使用 FILTER 函数的表达式的数据源。 当为单个分组记录字段只配置了一个合并时，也可以执行。  
    * 请注意，即使为 AmountMST 字段配置了多个合并，“执行位置”字段仍然指示此分组在运行时在 SQL 数据库中执行。 这是因为只有一个合并绑定到数据模型项目，并用于在运行时从此数据源拉取数据。  
49. 关闭该页面。
50. 单击“确定”。
51. 在树中，展开“TransactionsGroups”。
52. 在树结构中，展开“TransactionsGroups\aggregated”。
53. 在树中，选择“TransactionsGroups\aggregated\MaxOfAmountMST”。
54. 在树中，选择“Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')”。
55. 单击“绑定”。
56. 在树中，展开“TransactionsGroups”。
57. 在树中，选择“TransactionsGroups”。
58. 单击“编辑”。
59. 单击“编辑分组依据”。
    * 请注意，“执行位置”字段指示此分组将在运行时在内存中执行，因为同一个字段的两个合并均绑定到数据模型项目。   
60. 在列表中，标记或取消标记所有行。
61. 单击“删除”。
62. 单击“是”。
63. 单击“删除”。
64. 单击“是”。
65. 单击“将字段添加到”。
66. 单击“什么要分组”。
67. 在树中，展开“Commodity record(Intrastat)”。
68. 单击“保存”。
    * 请注意，“执行位置”字段指示此分组将在运行时在内存中执行，即使未定义合并，且所选的“表记录”类型的数据源引用同一个“内部统计”表。 原因在于数据源包含一些不能转换为 SQL 数据库级别的已计算字段。  

