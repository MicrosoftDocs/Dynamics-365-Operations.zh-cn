---
title: SESSIONTODAY ER 函数
description: 本主题提供有关 SESSIONTODAY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: caadfbe9d82c967b84abd362211a2ecec1bdd0481c7f3907816b7aec23883175
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756469"
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