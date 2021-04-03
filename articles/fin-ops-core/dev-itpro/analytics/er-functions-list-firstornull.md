---
title: FIRSTORNULL ER 函数
description: 本主题说明 FIRSTORNULL 电子申报 (ER) 函数如何使用
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564617"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER 函数

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` 函数返回指定列表的第一条记录为 *容器（记录）* 值（如果该记录不为空）。 如果记录为空，此函数将返回空 *容器（记录）* 值。

## <a name="syntax"></a>语法

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example"></a>示例

表达式 `FIRSTORNULL(SPLIT("",1)).Value` 返回一个空字符串 (**""**)。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]