---
title: NULLDATETIME ER 函数
description: 本文提供有关 NULLDATETIME 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287269"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER 函数

[!include [banner](../includes/banner.md)]

`NULLDATETIME` 函数返回一个 *日期时间* 值，此值表示协调世界时（格林威治标准时间 \[GMT\]）的 **空** 日期/时间值（1900 年 1 月 1 日）。

## <a name="syntax"></a>语法

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>返回值

*DateTime*

生成的日期/时间值。

## <a name="example"></a>示例

当由在 **语言和国家/地区首选项** 部分具有时区值 **(GMT) 协调世界时** 的应用程序用户启动的流程中调用时，`DATETIMEFORMAT( NULLDATETIME(), "O")` 返回字符串值 **1900-01-01T00:00:00.0000000+00:00**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
