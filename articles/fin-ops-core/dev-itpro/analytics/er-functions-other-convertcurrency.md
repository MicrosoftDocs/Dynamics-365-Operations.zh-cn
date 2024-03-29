---
title: CONVERTCURRENCY ER 函数
description: 本文提供有关 CONVERTCURRENCY 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: ac9a1cbb1c0a4b381a4e268f563c6ab0dd9c8053
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275503"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER 函数

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY` 函数返回一个 *实数* 值，该值表示通过使用指定日期的指定公司的设置，将指定的货币金额从指定源币种转换为指定目标币种的结果。

## <a name="syntax"></a>语法

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>参数

`amount`：*整数* 或 *实数*

表示必须转换的货币金额的数字值。

`source currency`：*字符串*

源币种的代码。

`target currency`：*字符串*

目标币种的代码。

`date`：*日期*

代表用于确定转换汇率的日期的 *日期* 值。

`company`：*字符串*

表示提供转换所用设置的公司的代码的 *字符串* 值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="example"></a>示例

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` 基于 **DEMF** 公司的设置返回当前会话日期一欧元的等额美元。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
