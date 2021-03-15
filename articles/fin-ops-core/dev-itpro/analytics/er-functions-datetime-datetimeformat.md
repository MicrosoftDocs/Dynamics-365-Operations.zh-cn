---
title: DATETIMEFORMAT ER 函数
description: 本主题提供有关 DATETIMEFORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825365"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER 函数

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` 函数返回一个 *字符串* 值，此值以指定格式和指定的[区域性](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）将给定日期/时间值显示为文本。 有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)。

## <a name="syntax-1"></a>语法 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>语法 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>参数

`datetime`：*日期时间*

表示要设定格式的日期和时间的日期/时间值。

`format`：*字符串*

输出字符串的格式。

> [!NOTE]
> 当您使用标准格式或自定义格式时，格式字符串区分大小写。 例如，[标准](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx)“d”格式说明符使用短日期模式返回日期，而标准“D”格式说明符使用长日期模式返回日期。 而且，[自定义](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)“M”格式说明符返回月份 1 到 12，而自定义“m”格式说明符返回分钟 0 到 59。

`culture`：*字符串*

用于设定格式的区域性。

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