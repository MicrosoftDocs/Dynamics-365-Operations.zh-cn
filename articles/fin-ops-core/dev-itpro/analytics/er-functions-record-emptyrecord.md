---
title: EMPTYRECORD ER 函数
description: 本主题提供有关 EMPTYRECORD 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684803"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER 函数

[!include [banner](../includes/banner.md)]

`EMPTYRECORD` 函数返回与指定记录列表或记录具有相同结构的空 *容器（记录）* 值。

## <a name="syntax"></a>语法

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表* 或 *容器（记录）*

*记录列表* 或 *容器（记录）* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="usage-notes"></a>使用说明

> [!NOTE] 
> null 记录为其中的所有字符串都有空值的记录。 空值对于数字来说为 **0**（零），对于字符串来说为空字符串，依此类推。

## <a name="example"></a>示例

`EMPTYRECORD (SPLIT ("abc", 1))` 返回具有与 `SPLIT` 函数返回的列表相同结构的新空记录。 有关详细信息，请参阅 [SPLIT](er-functions-list-split.md)。

## <a name="additional-resources"></a>其他资源

[记录函数](er-functions-category-record.md)
