---
title: ROUNDAMOUNT ER 函数
description: 本主题提供有关 ROUNDAMOUNT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: cce35a33ca179ad85bbde879122d3afbeefe5ee7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745655"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER 函数

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT` 函数根据指定的舍入规则，作为将指定数字舍入为另一个数字的最接近倍数的结果返回 *实数* 值。

## <a name="syntax"></a>语法

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>参数

`number`：*Int* 或 *实数*

必须舍入的数值。

`decimals`：*Int* 或 *实数*

`number` 参数的值必须舍入到其倍数的数字。

`round rule`：*枚举值*

定义舍入规则的 **RoundOffType** 枚举的枚举值。 此枚举提供以下值：

- 一般（常规）
- 向下 (RoundDown)
- 向上舍入 (RoundUp)

## <a name="return-values"></a>返回值

*实数*

产生的数值是 `decimals` 参数指定的值的倍数，并且最接近 `number` 参数指定的值。

## <a name="usage-notes"></a>使用说明

当 `number` 参数为零时，此函数始终返回零。

当 `decimals` 参数为零时，此函数将舍入为默认舍入值。 当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，默认舍入值为 **0.01**。 否则，默认舍入值为 **1.0**。

当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，此函数舍入到最接近的舍入金额。

当 `round rule` 参数设置为 **RoundOffType.RoundDown** 时，此函数朝零舍入到最接近的舍入金额。

当 `round rule` 参数设置为 **RoundOffType.RoundUp** 时，此函数离零舍入到最接近的舍入金额。

当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，此函数的行为类似于 [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel 函数和 [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ 函数。

## <a name="remarks"></a>注解

要将数值舍入到指定的小数位数，请使用 [ROUND](er-functions-mathematical-round.md) 函数。

## <a name="example"></a>示例

如果 **model.RoundOff** 参数设置为 **RoundOffType.Ordinary**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 7.35。 

如果 **model.RoundOff** 参数设置为 **RoundOffType.RoundDown**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 7.35。 

如果 **model.RoundOff** 参数设置为 **RoundOffType.RoundUp**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 8.4。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)

[数学函数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]