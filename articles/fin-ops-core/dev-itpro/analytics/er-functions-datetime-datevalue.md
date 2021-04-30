---
title: DATEVALUE ER 函数
description: 本主题提供有关 DATEVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891225"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER 函数

[!include [banner](../includes/banner.md)]

`DATEVALUE` 函数返回一个 *日期* 值，此值从指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）的给定文本值转换为日期值。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

## <a name="syntax-1"></a>语法 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>语法 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表要设定格式的值的文本。

`format`：*字符串*

给定文本的格式。

`culture`：*字符串*

用于设定给定文本的格式的区域性。

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