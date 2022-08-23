---
title: GETCURRENTCOMPANY ER 函数
description: 本文提供有关 GETCURRENTCOMPANY 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b5f5f7d7c884000f59b93e10875f78289a879779
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280176"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER 函数

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY` 函数返回表示用户目前已登录到的法人（公司）的代码的 *字符串* 值。

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
