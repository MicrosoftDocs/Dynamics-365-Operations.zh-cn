---
title: 数据收集类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的数据收集函数的信息。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: a8d4f5068bedcf1f15ae5257e29004a4773ef84c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908552"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>数据收集类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 数据收集函数用于根据已经以 **文本** 或 **Xml** 格式生成的输出数据，以正在运行的 ER 格式进行计数和求和。 此方法用于帮助提高运行的 ER 格式的性能，以在生成的文档中输入运行总计值，以及其他目的。 本文提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能 | 说明 |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | 此函数返回一个 *记录列表* 值，此值包含格式元素的 **已收集的数据键值** 属性返回的以及在格式运行期间使用格式元素生成传出文档时收集的值，并且满足指定条件。 每个条件包含一个键范围和一个键值。 |
| [CountIF](er-functions-datacollection-countif.md) | 此函数返回一个 *整数* 值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。 条件包含一个键范围和一个键值。 |
| [CountIF](er-functions-datacollection-countifs.md) | 此函数返回一个 *整数* 值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。 每个条件包含一个键范围和一个键值。 |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | 此函数返回一个 *字符串* 值，此值代表当前 (ER) 格式元素的名称。 |
| [SumIF](er-functions-datacollection-sumif.md) | 此函数返回一个 *实数* 值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。 条件包含一个键范围和一个键值。 |
| [SumIF](er-functions-datacollection-sumifs.md) | 此函数返回一个 *实数* 值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。 每个条件包含一个键范围和一个键值。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]