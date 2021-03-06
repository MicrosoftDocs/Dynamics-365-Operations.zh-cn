---
title: NUMBERFORMAT ER 函数
description: 本主题提供有关 NUMBERFORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890375"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER 函数

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT` 函数返回一个 *字符串* 值，此值以指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）显示指定数字。 有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-numeric-format-strings)和[自定义](/dotnet/standard/base-types/custom-numeric-format-strings)。

## <a name="syntax-1"></a>语法 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>语法 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>参数

`number`：*整数* 或 *实数*

指定必须设定格式的数字的数字值。

`format`：*字符串*

代表格式的 *字符串* 值。

`culture`：*字符串*

代表用于设定格式的区域性的 *字符串* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

如果未将区域性定义为所调用函数的参数，运行此函数的上下文将确定用于设定数字格式的区域性。

## <a name="example-1"></a>示例 1

对于 **EN-US** 区域性，`NUMBERFORMAT (0.45, "p")` 将返回 **"45.00 %"**，`NUMBERFORMAT (10.45, "#")` 将返回 **"10"**。

## <a name="example-2"></a>示例 2

`NUMBERFORMAT (10/3, "F2", "de")` 将返回 **3,33**，而 `NUMBERFORMAT (10/3, "F2", "en-us")` 将返回 **3.33**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]