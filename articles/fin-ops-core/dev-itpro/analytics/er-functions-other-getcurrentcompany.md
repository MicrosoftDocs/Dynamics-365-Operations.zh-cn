---
title: GETCURRENTCOMPANY ER 函数
description: 本主题提供有关 GETCURRENTCOMPANY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744111"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER 函数

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY` 函数返回表示用户目前已登录到的法人（公司）的代码的*字符串*值。

## <a name="syntax"></a>语法

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`GETCURRENTCOMPANY ()` 为已登录 **Contoso Entertainment System USA** 公司的用户返回 **USMF**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)
