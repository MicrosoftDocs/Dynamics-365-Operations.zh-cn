---
title: DATEVALUE ER 函数
description: 本文提供有关 DATEVALUE 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268689"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER 函数

[!include [banner](../includes/banner.md)]

`DATEVALUE` 函数返回一个 *[日期](er-formula-supported-data-types-primitive.md#date)* 值，此值从指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）的给定文本值转换为日期值。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

## <a name="syntax-1"></a>语法 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>语法 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>参数

`text`：*[字符串](er-formula-supported-data-types-primitive.md#string)*

代表要设定格式的值的文本。

`format`：*字符串*

给定文本的格式。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

`culture`：*字符串*

用于设定给定文本的格式的区域性。 有关受支持的区域性的信息，请参阅[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)。

## <a name="return-values"></a>返回值

*日期*

生成的日期值。

## <a name="usage-notes"></a>使用说明

当区域性未被定义为被调用函数的参数时，`culture` 由调用上下文定义。 例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATEVALUE` 函数，则将使用德国区域性完成转换。 默认 `culture` 值为 **EN-US**。

## <a name="example-1"></a>示例 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` 基于指定的自定义格式和默认的应用程序的 **EN-US** 区域性返回日期值 **December 21, 2016**。

## <a name="example-2"></a>示例 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` 基于指定的自定义格式和区域性返回日期值 **January 21, 2016**。

但是，`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` 将引发异常，以通知用户指定字符串无法识别为指定区域性的有效日期。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
