---
title: ISOCREDREF ER 函数
description: 本主题提供有关 ISOCREDREF 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748309"
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