---
title: SESSIONTODAY ER 函数
description: 本文提供有关 SESSIONTODAY 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274880"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER 函数

[!include [banner](../includes/banner.md)]

`SESSIONTODAY` 函数返回一个 *日期* 值，此值表示当前应用程序会话的日期。

## <a name="syntax"></a>语法

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>返回值

*日期*

生成的日期值。

## <a name="example"></a>示例

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为字符串 **"24-12-2015"**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
