---
title: LOWER ER 函数
description: 本主题提供有关 LOWER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041093"
---
# <a name="LOWER">LOWER ER 函数</a>

[!include [banner](../includes/banner.md)]

在将指定的文本字符串转换为小写字母后，`LOWER` 函数作为*字符串*值返回该字符串。

## <a name="syntax"></a>语法

```vb
LOWER (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

指定文本的*字符串*值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`LOWER ("Sample")` 返回 **"sample"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
