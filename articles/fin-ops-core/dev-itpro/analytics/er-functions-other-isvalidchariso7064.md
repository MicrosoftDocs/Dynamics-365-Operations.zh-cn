---
title: ISVALIDCHARACTERISO7064 ER 函数
description: 本文提供有关 ISVALIDCHARACTERISO7064 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 26ee54d1c3cd5673ec573e2df688780d3902b69d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275366"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER 函数

[!include [banner](../includes/banner.md)]

如果指定字符串表示有效的国际银行帐号 (IBAN)，`ISVALIDCHARACTERISO7064` 函数返回 *布尔* 值 **TRUE**。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表 IBAN 的文本值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` 返回 **TRUE**。 

`ISVALIDCHARACTERISO7064 ("AT61")` 返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
