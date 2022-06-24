---
title: CH_BANK_MOD_10 ER 函数
description: 本文提供有关 CH_BANK_MOD_10 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 494aa335ef170db0cd2f61a1d33391de474cd4bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885018"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER 函数

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10` 函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD10 表达式表示贷方引用。

## <a name="syntax"></a>语法

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>参数

`invoice number digits`：*字符串*

代表发票编号数字的文本值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`CH_BANK_MOD_10 ("VEND-200002")` 将返回 **3**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]