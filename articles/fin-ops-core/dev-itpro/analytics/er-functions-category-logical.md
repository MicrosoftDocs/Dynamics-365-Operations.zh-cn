---
title: 逻辑类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的逻辑函数的信息。
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2361fa0df3fe60813e75c772134299ad948f3582
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888182"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>逻辑类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 逻辑函数可用于与逻辑值一起使用，来在单个表达式中执行多个比较或测试多个条件。 本文提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能 | 说明 |
|----------|-------------|
| [并](er-functions-logical-and.md)                       | 此函数返回一个 *布尔* 值 **TRUE**（如果所有指定条件都为 true）。 否则，返回 *布尔* 值 **FALSE**。 |
| [包装箱](er-functions-logical-case.md)                     | 此函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。 否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。 返回的值可以是任何受支持的数据类型的值。 |
| [包含](er-functions-logical-contains.md)             | 此函数确定指定的输入是否包含指定文本。 如果指定的输入包含指定的文本，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。 |
| [EndsWith](er-functions-logical-endswith.md)             | 此函数确定指定的输入是否以指定文本结尾。 如果指定的输入以指定文本结尾，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。 |
| [如果](er-functions-logical-if.md)                         | 如果满足指定条件，此函数返回第一个指定值。 否则，返回第二个指定值。 返回的值可以是任何受支持的数据类型的值。 |
| [不](er-functions-logical-not.md)                       | 此函数作为 *布尔* 值返回指定条件的冲销逻辑值。 |
| [Or](er-functions-logical-or.md)                         | 此函数返回一个 *布尔* 值 **FALSE**（如果所有指定条件都为 false）。 如果所有指定条件都为 true，此函数返回一个 *布尔* 值 **TRUE**。 |
| [StartsWith](er-functions-logical-startswith.md)         | 此函数确定指定的输入是否以指定文本开头。 如果指定的输入以指定文本开头，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。 |
| [ValueIn](er-functions-logical-valuein.md)               | 此函数确定指定的输入是否匹配指定列表中任何指定项目的值。 如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。 否则，返回 *布尔* 值 **FALSE**。 |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | 此函数确定指定的 *Int64* 或 *整数* 类型的输入是否匹配指定列表中任何指定项目的值。 如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。 否则，返回 *布尔* 值 **FALSE**。 |


## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]