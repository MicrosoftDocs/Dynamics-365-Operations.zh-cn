---
title: IF ER 函数
description: 本文提供有关 IF 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b674a6f3e86af3763a251cbdc7c30fb8c5ed0f55
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275540"
---
# <a name="if-er-function"></a>IF ER 函数

[!include [banner](../includes/banner.md)]

如果满足指定条件，`IF` 函数返回第一个指定值。 否则，返回第二个指定值。 返回的值可以是任何受支持的数据类型的值。

## <a name="syntax"></a>语法

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>参数

`condition`：*布尔值*

必须测试的有效条件表达式。

`first value`：*任何受支持的数据类型*

满足条件时返回的结果。

`second value`：*任何受支持的数据类型*

不满足条件时返回的结果。

## <a name="return-values"></a>返回值

*任何受支持的数据类型*

生成的任何受支持数据类型的值。

## <a name="usage-notes"></a>使用说明

必须使用相同的数据类型指定 `first value` 和 `second value` 参数。 如果配置值的数据类型不匹配，则会在设计时引发异常。

如果第一个值与第二个值是 *容器（记录）* 或 *记录列表* 数据类型的值，结果只包含两个值中都存在的字段。

## <a name="example"></a>示例

`IF (1=2, "condition is met", "condition is not met")` 返回字符串 **"condition is not met"**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
