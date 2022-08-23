---
title: SESSIONNOW ER 函数
description: 本文提供有关 SESSIONNOW 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1cf092d55728f23cb10070324abc4458004946c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272613"
---
# <a name="sessionnow-er-function"></a>SESSIONNOW ER 函数

[!include [banner](../includes/banner.md)]

`SESSIONNOW` 函数返回一个 *日期时间* 值，此值表示当前应用程序会话的日期和时间。

## <a name="syntax"></a>语法

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>返回值

*DateTime*

生成的日期/时间值。

## <a name="example"></a>示例

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
