---
title: ABS ER 函数
description: 本主题提供有关 ABS 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753136"
---
# <a name="abs-er-function"></a>ABS ER 函数

[!include [banner](../includes/banner.md)]

`ABS` 函数作为 *实数* 值返回指定数字的绝对值（模数）。 即，返回不带符号的数字。

## <a name="syntax"></a>语法

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]