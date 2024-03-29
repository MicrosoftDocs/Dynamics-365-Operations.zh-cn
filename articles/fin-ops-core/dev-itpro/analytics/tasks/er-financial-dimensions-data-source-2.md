---
title: ER 将财务维度用作数据源（第 2 部分 - 模型映射）
description: 本文介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 2 部分）
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 0d2daedd38c93ff17ef39780140c9c28ece82736
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290805"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER 将财务维度用作数据源（第 2 部分 - 模型映射）

[!include [banner](../../includes/banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。 这些步骤可以在任何公司执行。

为了完成这些步骤，您必须首先完成“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”这一过程中的步骤。


## <a name="add-required-data-sources-to-model-mapping"></a>向模型映射添加所需数据源
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，选择“财务维度示例模型”。
3. 单击“设计器”。
4. 单击“映射模型到数据源”。
5. 单击“新建”。
6. 在“定义”字段中，选择“条目”。
7. 在“名称”字段中，键入“维度数据映射”。
8. 在“描述”字段中，键入“维度数据映射”。
9. 单击“保存”。
10. 单击“设计器”。
11. 在树中，选择“Dynamics 365 for Operations\表”'。
12. 单击“添加根”。
13. 在“名称”字段中，键入“公司”。
14. 在“表格”字段中，键入“公司信息”。
15. 单击“确定”。
16. 在树中，选择“功能\财务维度细节”。
17. 单击“添加根”。
    * 此数据源指定如何为将把该模型用作数据源的任何报表定义财务维度的范围。  
18. 在“名称”字段中，键入一个值。
19. 在“要求维度”字段中选择“是”。
    * 选择“是”将允许用户在“用户”对话框窗体中运行时选择维度。 如果设置为“否”，默认将使用当前实例的所有财务维度。  
20. 在“财务维度选择”字段中，选择“法人”。
    * 选择“所有”将允许用户在“查询”字段中选择当前实例的所需维度。  选择“法人”将允许用户在“查询”字段中选择公司的维度。  选择“维度”将允许用户选择使用单个纬度集的维度。  
21. 在“要求主科目”字段中选择“是”。
    * 将“请求主科目”设置为“是”将允许用户把主科目作为维度列表的一部分选择。   如果设置为“否”，将不会在维度列表中包含主科目，并且启用“主科目是否必填”选项。 如果“主科目是否必填”设置为“是”，无论用户如何选择，都应该在维度列表中包含主科目。  
22. 单击“确定”。
![财务维度的详细信息数据源属性滑出。](../media/er-financial-dimensions-guides-model-mapping1.png)
23. 在树中，选择“Dynamics 365 for Operations\表记录”'。
24. 单击“添加根”。
25. 在“名称”字段中，键入“分类日记帐”。
26. 在“要求查询”字段中选择“是”。
27. 在“表格”字段中，键入“分类日记帐表”。
28. 单击“确定”。
![<odel 映射设计器页面，表记录数据源类型。](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>将数据模型元素映射到添加的数据源
1. 在树中，展开“日记帐”。
2. 在树中，展开“日记帐\交易”。
3. 在树中，展开“日记帐\交易\维度数据”。
4. 在树中，展开“维度设置”。
5. 在树中，展开“分类日记帐”。
6. 在树中，展开“分类日记帐\<关系”。
7. 在树中，展开“分类日记帐\<关系\分类日记帐交易”。
8. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\凭证”。
9. 在树中，选择“日记帐\交易\凭证”。
10. 单击“绑定”。
11. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。
    * 请注意，对于对财务维度设置为的任何引用（如 LedgerDimension），都有一个相应数据源项 (LedgerDimension.Dimension) 可用。 此数据源项提供设置为记录的列表的维度的财务维度。  
12. 在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。
13. 在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。
14. 在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值”。
15. 在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义”。
16. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义\名称”。
17. 在树中，选择“日记帐\交易\维度数据\名称”。
18. 单击“绑定”。
19. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\描述”。
20. 在树中，选择“日记帐\交易\维度数据\描述”。
21. 单击“绑定”。
22. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\代码”。
23. 在树中，选择“日记帐\交易\维度数据\代码”。
24. 单击“绑定”。
25. 在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。
26. 在树中，选择“日记帐\交易\维度数据”。
27. 单击“绑定”。
!模型映射设计器页面、映射选项卡、数据源树。](../media/er-financial-dimensions-guides-model-mapping3.png)
28. 在树中，选择“分类日记帐\<关系\分类日记帐交易\Debit(AmountCurDebit)”。
29. 在树中，选择“日记帐\交易\借方”。
30. 单击“绑定”。
31. 在树中，选择“分类日记帐\<关系\分类日记帐交易\Date(TransDate)”。
32. 在树中，选择“日记帐\交易\日期”。
33. 单击“绑定”。
34. 在树中，选择“分类日记帐\<关系\分类日记帐交易\Currency(CurrencyCode)”。
35. 在树中，选择“日记帐\交易\币种”。
36. 单击“绑定”。
37. 在树中，选择“分类日记帐\<关系\分类日记帐交易\Credit(AmountCurCredit)”。
38. 在树中，选择“日记帐\交易\贷方”。
39. 单击“绑定”。
40. 在树中，选择“分类日记帐\<关系\分类日记帐交易”。
41. 在树中，选择“日记帐\交易”。
42. 单击“绑定”。
43. 在树中，选择“分类日记帐\日记帐批号（日记帐编号）”。
44. 在树中，选择“日记帐\批次”。
45. 单击“绑定”。
46. 在树中，选择“分类日记帐”。
47. 在树中，选择“日记帐”。
48. 单击“绑定”。
49. 在树中，展开“维度”。
50. 在树中，展开“维度\主科目和维度”。
51. 在树中，展开“维度\主科目和维度\定义”。
52. 在树中，选择“维度\主科目和维度\定义\名称”。
53. 在树中，选择“维度设置\代码”。
54. 单击“绑定”。
55. 在树中，选择“维度\主科目和维度\定义\报表列名”。
56. 在树中，选择“维度设置\名称”。
57. 单击“绑定”。
58. 在树中，选择“维度\主科目和维度”。
59. 在树中，选择“维度设置”。
60. 单击“绑定”。
61. 在树中，选择“公司”。
62. 单击“编辑”。
63. 在“expressionAsStringText”字段中，输入“Company.'find()'.'name()'”。
    * Company.'find()'.'name()'  
64. 单击保存。
![ER 模型映射设计器页面。](../media/er-financial-dimensions-guides-model-mapping4.png)
65. 关闭该页面。
66. 单击保存。
67. 关闭该页面。

## <a name="complete-this-draft-models-version"></a>完成此草稿模型的版本
1. 关闭该页面。
2. 关闭该页面。
3. 单击“更改状态”。
4. 单击“完成”。
5. 单击“确定”。
![“电子报告配置”页面。](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
