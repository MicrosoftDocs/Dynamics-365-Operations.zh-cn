---
title: ISEMPTY ER 函数
description: 本主题提供有关 ISEMPTY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916123"
---
# <a name="ISEMPTY">ISEMPTY ER 函数</a>

[!include [banner](../includes/banner.md)]

`ISEMPTY` 函数返回一个*布尔*值 **TRUE**（如果指定列表未包含记录）。 否则，返回*布尔*值 **FALSE**。

## <a name="syntax"></a>语法

```
ISEMPTY (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*布尔值*

生成的*布尔*值。

## <a name="example-1"></a>示例 1

如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `ISEMPTY(DS)` 将返回 **FALSE**。

## <a name="example-2"></a>示例 2

表达式 `ISEMPTY (SPLIT ("",1))` 返回 **TRUE**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)
