---
title: LEN ER 函数
description: 本主题提供有关 LEN 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744255"
---
# <a name="len-er-function"></a>LEN ER 函数

[!include [banner](../includes/banner.md)]

`LEN` 函数作为*整数*值在指定的字符串中返回字符数量。

## <a name="syntax"></a>语法

```vb
LEN (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

指定文本的*字符串*值。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="example"></a>示例

`LEN ("Sample")` 将返回 **6**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
