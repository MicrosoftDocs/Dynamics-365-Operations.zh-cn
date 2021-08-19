---
title: NOT ER 函数
description: 本主题提供有关 NOT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 094c60157d3ac4091fb02b24dcc00dddba2397abe87510952371a779eb3a2f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725276"
---
# <a name="not-er-function"></a>NOT ER 函数

[!include [banner](../includes/banner.md)]

`NOT` 函数作为 *布尔* 值返回指定条件的冲销逻辑值。

## <a name="syntax"></a>语法

```vb
NOT (condition)
```

## <a name="arguments"></a>参数

`condition`：*布尔值*

必须冲销的有效条件表达式。

## <a name="return-values"></a>返回值

*布尔值*

生成的 *布尔* 值。

## <a name="example"></a>示例

`NOT (TRUE)` 返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]