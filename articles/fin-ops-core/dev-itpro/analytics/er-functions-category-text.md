---
title: 文本类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的文本函数的信息。
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 502a68d51705114adc096a1cd2217210f4e925bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885534"
---
# <a name="list-of-er-functions-of-the-text-category"></a>文本类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 文本函数可用于对 *字符串* 数据类型的数据源执行操作。 本文提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能 | 说明 |
|----------|-------------|
| [Char](er-functions-text-char.md) | 此函数返一个 *字符串* 值，该值表示指定 Unicode 数值引用的单个字符。 |
| [连接](er-functions-text-concatenate.md) | 在将所有指定的文本字符串合并为一个字符串之后，此函数将这些字符串作为 *字符串* 值返回。 |
| [格式](er-functions-text-format.md) | 通过使用第 *N* 个参数替换出现的所有 **%N** 设定指定字符串的格式后，此函数作为 *字符串* 值返回该字符串。 |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | 此函数通过使用指定为 *字符串* 值的枚举名称在指定的枚举数据源中搜索特定的 *枚举* 值。 如果找到 *枚举* 值，函数将返回此值。 |
| [GetLabelText](er-functions-text-getlabeltext.md) | 此函数搜索特定标签以返回一个 *[字符串](er-formula-supported-data-types-primitive.md#string)* 值，该值表示使用指定语言对指定标签的翻译。 |
| [GuidValue](er-functions-text-guidvalue.md) | 此函数将 *字符串* 类型的指定输入转换为 *GUID* 类型的数据项。 |
| [JsonValue](er-functions-text-jsonvalue.md) | 此函数分析在指定路径访问且格式为 JavaScript Object Notation (JSON) 的数据，并提取基于指定 ID 的标量值。 然后将提取的标量值返回为 *字符串* 值。 |
| [左对齐](er-functions-text-left.md) | 此函数返回 *字符串* 值，该值在指定字符串的开头显示指定的字符数量。 |
| [Len](er-functions-text-len.md) | 此函数返回 *整数* 值，该值在指定的字符串中显示字符数量。 |
| [Lower](er-functions-text-lower.md) | 在将指定的文本字符串转换为小写字母后，此函数作为 *字符串* 值返回该字符串。 |
| [Mid](er-functions-text-mid.md) | 此函数返回一个 *[字符串](er-formula-supported-data-types-primitive.md#string)* 值，此值在指定位置的开始处，在指定的字符串中显示指定的字符数量。 |
| [NewGUID](er-functions-text-newguid.md) | 此函数返回新生成的 *[GUID](er-formula-supported-data-types-primitive.md#guid)* 值。 |
| [NumberFormat](er-functions-text-numberformat.md) | 此函数返回一个 *字符串* 值，此值以指定格式和指定的区域性（可选）显示指定数字。 |
| [NumeralsToText](er-functions-text-numeralstotext.md) | 在使用指定语言拼出（即转换为文本字符串）指定数字后，此函数作为 *字符串* 返回指定数字。 |
| [PadLeft](er-functions-text-padleft.md) | 此函数返回指定长度的 *字符串* 值，其中指定字符串的开头是使用一个或多个指定字符的实例填充的。 |
| [QrCode](er-functions-text-qrcode.md) | 此函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。 |
| [替换](er-functions-text-replace.md) | 在将全部或部分指定文本字符串替换为另一个字符串之后，此函数作为 *字符串* 值返回指定的文本字符串。 |
| [右对齐](er-functions-text-right.md) | 此函数返回 *字符串* 值，该值在指定字符串的末尾显示指定的字符数量。 |
| [文本](er-functions-text-text.md) | 在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，此函数将该数字作为 *字符串* 值返回。 |
| [翻译](er-functions-text-translate.md) | 此函数返回一个 *字符串* 值，该值中包含使用指定文本字符替换提供的另一组字符的结果。 |
| [Trim](er-functions-text-trim.md) | 此函数在制表符、回车符、换行符和换页符被单个空格字符替换后，在前导和尾随空格被截断后，以及字词之间的多个空格被删除后，将指定的文本字符串作为 *字符串* 值返回。 |
| [Upper](er-functions-text-upper.md) | 在将指定的文本字符串转换为大写字母后，此函数作为 *字符串* 值返回该字符串。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
