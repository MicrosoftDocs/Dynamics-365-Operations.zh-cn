---
title: ABS ER 函数
description: 本主题提供有关 ABS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917089"
---
# <a name="ABS">ABS ER 函数</a>

[!include [banner](../includes/banner.md)]

`ABS` 函数作为*实数*值返回指定数字的绝对值（模数）。 即，返回不带符号的数字。

## <a name="syntax"></a>语法

```
ABS (number)
```

## <a name="arguments"></a>参数

`number`：*实数*

您想要的模数的数值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="example"></a>示例

`ABS (-1)` 将返回 **1**。

## <a name="additional-resources"></a>其他资源

[数学函数](er-functions-category-mathematical.md)
