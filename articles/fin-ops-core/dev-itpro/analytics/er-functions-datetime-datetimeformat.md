---
title: DATETIMEFORMAT ER 函数
description: 本文提供有关 DATETIMEFORMAT 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 09/08/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e21b676046b6279826a728657fcc0d2a00a38b76
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287359"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER 函数

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` 函数返回一个 *[字符串](er-formula-supported-data-types-primitive.md#string)* 值，此值以指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）将给定日期/时间值显示为文本。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

## <a name="syntax-1"></a>语法 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>语法 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>参数

`datetime`：*[日期/时间](er-formula-supported-data-types-primitive.md#datetime)*

表示要设定格式的日期和时间的日期/时间值。

`format`：*字符串*

输出字符串的格式。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

> [!NOTE]
> 当您使用标准格式或自定义格式时，格式字符串区分大小写。 例如，[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)“d”格式说明符使用短日期模式返回日期，而标准“D”格式说明符使用长日期模式返回日期。 而且，[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)“M”格式说明符返回月份 1 到 12，而自定义“m”格式说明符返回分钟 0 到 59。

`culture`：*字符串*

用于设定格式的区域性。 有关受支持的区域性的信息，请参阅[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)。

## <a name="return-values"></a>返回值

*字符串*

生成的字符串值。

## <a name="usage-notes"></a>使用说明

如果区域性未被定义为被调用函数的参数，`culture` 由调用上下文定义。 例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATETIMEFORMAT` 函数，则将使用德国区域性完成转换。 默认 `culture` 值为 **EN-US**。

当 `DATETIMEFORMAT` 函数转换给定的日期/时间值时，它将考虑正在运行 ER 格式（调用该函数的上下文的 ER 格式）的应用程序用户的时区设置。

## <a name="example-1"></a>示例 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期/时间值 2015 年 12 月 24 日为 **"24-12-2015"**。

## <a name="example-2"></a>示例 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。

## <a name="example-3"></a>示例 3

当此函数在 **语言和国家/地区首选项** 部分具有时区值 **(GMT-08:00)太平洋时间(美国和加拿大)** 的应用程序用户启动的流程中调用时，`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` 返回字符串值 **2019-11-12T08:00:00.0000000-08:00**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
