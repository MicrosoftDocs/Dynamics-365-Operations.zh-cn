---
title: ISOCREDREF ER 函数
description: 本文提供有关 ISOCREDREF 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 189843d608cc00ac51a284b163553da6d821150e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277577"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER 函数

[!include [banner](../includes/banner.md)]

`ISOCREDREF` 函数基于指定发票编号的数字和字母符号返回一个 *字符串* 值，该值表示国际标准化组织 (ISO) 贷方引用。

## <a name="syntax"></a>语法

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>参数

`invoice number digits`：*字符串*

代表发票编号数字的文本值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

> [!NOTE] 
> 若要从不是 ISO 兼容的字母表中清除符号，`invoice number digits` 参数必须在传递给此函数前转换。

## <a name="example"></a>示例

`ISOCredRef ("VEND-200002")` 将返回 **"RF23VEND-200002"**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
