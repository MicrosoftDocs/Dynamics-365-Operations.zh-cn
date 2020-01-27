---
title: NULLDATETIME ER 函数
description: 本主题提供有关 NULLDATETIME 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917480"
---
# <a name="NULLDATETIME">NULLDATETIME ER 函数</a>

[!include [banner](../includes/banner.md)]

`NULLDATETIME` 函数返回一个*日期时间*值，此值表示协调世界时（格林威治标准时间 \[GMT\]）的**空**日期/时间值（1900 年 1 月 1 日）。

## <a name="syntax"></a>语法

```
NULLDATETIME ()
```

## <a name="return-values"></a>返回值

*DateTime*

生成的日期/时间值。

## <a name="example"></a>示例

当由在**语言和国家/地区首选项**部分具有时区值 **(GMT) 协调世界时**的应用程序用户启动的流程中调用时，`DATETIMEFORMAT( NULLDATETIME(), "O")` 返回字符串值 **1900-01-01T00:00:00.0000000+00:00**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)
