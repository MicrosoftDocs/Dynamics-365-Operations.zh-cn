---
title: NUMBERFORMAT ER 函数
description: 本文提供有关 NUMBERFORMAT 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274756"
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
