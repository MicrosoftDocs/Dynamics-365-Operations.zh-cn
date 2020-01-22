---
title: NOT ER 函数
description: 本主题提供有关 NOT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916031"
---
# <a name="NOT">NOT ER 函数</a>

[!include [banner](../includes/banner.md)]

`NOT` 函数作为*布尔*值返回指定条件的冲销逻辑值。

## <a name="syntax"></a>语法

```
NOT (condition)
```

## <a name="arguments"></a>参数

`condition`：*布尔值*

必须冲销的有效条件表达式。

## <a name="return-values"></a>返回值

*布尔值*

生成的*布尔*值。

## <a name="example"></a>示例

`NOT (TRUE)` 返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)
