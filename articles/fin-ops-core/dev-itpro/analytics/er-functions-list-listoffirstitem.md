---
title: LISTOFFIRSTITEM ER 函数
description: 本文提供有关 LISTOFFIRSTITEM 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881150"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM ER 函数

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` 函数返回一个 *记录列表* 值，此值仅包含指定列表的第一条记录。

## <a name="syntax"></a>语法

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="example"></a>示例

表达式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` 返回文本值 **"A"**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]