---
title: 设置固定资产过帐模板
description: 此过程演示如何设置固定资产过帐模板。
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8001428cf2df111458fddd0ecbcdae0daf9b25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863063"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>设置固定资产过帐模板

[!include [banner](../../includes/banner.md)]

此过程演示如何设置固定资产过帐模板。 本文中给出的示例是一个基础过帐模板，但是必须针对您的特定会计科目表和财务报表要求创建过帐模板。

1. 在导航窗格中，转到 **模块 > 固定资产 > 设置 > 固定资产过帐模板**。
2. 单击 **新建**。
3. 在 **过帐模板** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。 您将需要在处理固定资产时使用的每个固定资产交易类型创建过帐模板。 此任务指南将从购置交易类型开始。  
5. 单击工具栏中的 **添加**。
6. 在 **帐簿** 字段中，输入或选择一个值。 **分组** 字段可让您按表（为每个固定资产设置一个科目）或“组”（为每个固定资产组设置一个科目）定义过帐模板。 对于此任务指南，将此该值设置为“全部”以适用于有指定帐簿的所有固定资产。  
7. 在 **主科目** 字段中，指定所需值。 对于购置，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。    
8. 在 **会计科目** 快速选项卡下的下拉菜单中，选择“购置调整”。 对于购置调整交易记录，我们将使用与用于购置交易记录的相同科目。  
9. 单击 **添加**。
10. 在 **帐簿** 字段中，输入或选择一个值。
11. 在 **主科目** 字段中，指定所需值。 对于购置调整，您可以输入抵消科目或将其留为空白以针对特定交易填写此字段。    
12. 在 **会计科目** 快速选项卡下的下拉菜单中，选择“折旧”。
13. 单击 **添加**。
14. 在 **帐簿** 字段中，输入或选择一个值。
15. 在 **主科目** 字段中，指定所需值。
16. 在 **抵销帐户** 字段中，指定所需值。
17. 在 **会计科目** 快速选项卡下的下拉菜单中，选择“折旧调整”。 对于折旧调整交易记录，我们将使用与用于折旧交易记录的相同科目。  
18. 单击 **添加**。
19. 在 **帐簿** 字段中，输入或选择一个值。
20. 在 **主科目** 字段中，指定所需值。
21. 在 **抵销帐户** 字段中，指定所需值。
22. 在 **会计科目** 快速选项卡下的下拉菜单中，选择“处置 - 出售”。
23. 单击 **添加**。
24. 在 **帐簿** 字段中，输入或选择一个值。
25. 在 **主科目** 字段中，指定所需值。 对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。  
26. 在 **会计科目** 快速选项卡下的下拉菜单中，选择“处置 - 报废”。 对“处置出售”和“处置报废”使用相同的科目。  
27. 单击 **添加**。
28. 在 **帐簿** 字段中，输入或选择一个值。
29. 在 **主科目** 字段中，指定所需值。 对于处置，您可以输入对方科目或将其留为空白以针对特定交易自动填写此字段。  
30. 展开 **处置** 快速选项卡。 您必须对销售及报废设置处置过帐模板。  我们从处置销售交易开始。  
31. 单击 **添加**。
32. 在 **帐簿** 字段中，输入或选择一个值。
33. 在 **过帐值** 字段中，选择“购置值”。
    * 购置价值将用于所有年度的购置和购置调整价值。 您还可以为这些交易类型分别定义科目。  
    * 根据处置是否造成收益或损失，您可以设置处置流程以使用不同科目。 我将“销售价值类型”设置为“全部”以对所有处置类型使用相同的科目。  
34. 在 **主科目** 字段中，指定所需值。
35. 在 **抵销帐户** 字段中，指定所需值。
36. 单击 **添加**。
37. 在 **帐簿** 字段中，输入或选择一个值。
38. 在 **过帐值** 字段中，选择“折旧（往年）”。  
38. 在 **主科目** 字段中，指定所需值。
39. 在 **抵销帐户** 字段中，指定所需值。
40. 单击 **添加**。
41. 在 **帐簿** 字段中，输入或选择一个值。
42. 在 **过帐值** 字段中，选择“折旧（今年）”。
43. 在 **主科目** 字段中，指定所需值。
44. 在 **抵销帐户** 字段中，指定所需值。
45. 单击 **添加**。
46. 在 **帐簿** 字段中，输入或选择一个值。
47. 在 **过帐值** 字段中，选择“折旧调整（往年）”。
48. 在 **主科目** 字段中，指定所需值。
49. 在 **抵销帐户** 字段中，指定所需值。
50. 单击 **添加**。
51. 在 **帐簿** 字段中，输入或选择一个值。
52. 在 **过帐值** 字段中，选择“折旧调整（今年）”。
53. 在 **主科目** 字段中，指定所需值。
54. 在 **抵销帐户** 字段中，指定所需值。
55. 单击 **添加**。
56. 在 **帐簿** 字段中，输入或选择一个值。
57. 在 **过帐值** 字段中，选择“帐面净值”。
58. 在 **主科目** 字段中，指定所需值。
59. 在 **抵销帐户** 字段中，指定所需值。
60. 在 **出售还是报废** 字段中，选择“报废”
61. 单击 **添加**。
62. 在 **帐簿** 字段中，输入或选择一个值。
63. 在 **过帐值** 字段中，选择“购置值”。
64. 在 **主科目** 字段中，指定所需值。
65. 在 **抵销帐户** 字段中，指定所需值。
66. 单击 **添加**。
67. 在 **帐簿** 字段中，输入或选择一个值。
67. 在 **过帐值** 字段中，选择“折旧（往年）”。  
68. 在 **主科目** 字段中，指定所需值。
69. 在 **抵销帐户** 字段中，指定所需值。
70. 单击 **添加**。
71. 在 **帐簿** 字段中，输入或选择一个值。
72. 在 **过帐值** 字段中，选择“折旧（今年）”。
73. 在 **主科目** 字段中，指定所需值。
74. 在 **抵销帐户** 字段中，指定所需值。
75. 单击 **添加**。
76. 在 **帐簿** 字段中，输入或选择一个值。
77. 在 **过帐值** 字段中，选择“折旧调整（往年）”。
78. 在 **主科目** 字段中，指定所需值。
79. 在 **抵销帐户** 字段中，指定所需值。
80. 单击 **添加**。
81. 在 **帐簿** 字段中，输入或选择一个值。
82. 在 **过帐值** 字段中，选择“折旧调整（今年）”。
83. 在 **主科目** 字段中，指定所需值。
84. 在 **抵销帐户** 字段中，指定所需值。
85. 单击 **添加**。
86. 在 **帐簿** 字段中，输入或选择一个值。
87. 在 **过帐值** 字段中，选择“帐面净值”。
88. 在 **主科目** 字段中，指定所需值。
89. 在 **抵销帐户** 字段中，指定所需值。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
