---
title: ISEMPTY ER 函数
description: 本文提供有关 ISEMPTY 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1d8c9a2195afbc76bc00f31778d087268b98279f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845509"
---
# <a name="isempty-er-function"></a>ISEMPTY ER 函数

[!include [banner](../includes/banner.md)]

`ISEMPTY` 函数返回一个 *布尔* 值 **TRUE**（如果指定列表未包含记录）。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*布尔值*

生成的 *布尔* 值。

## <a name="example-1"></a>示例 1

如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `ISEMPTY(DS)` 将返回 **FALSE**。

## <a name="example-2"></a>示例 2

表达式 `ISEMPTY (SPLIT ("",1))` 返回 **TRUE**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]