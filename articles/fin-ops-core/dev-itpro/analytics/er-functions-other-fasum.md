---
title: FA_SUM ER 函数
description: 本主题提供有关 FA_SUM 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: fccd318a8ab67528f0ce048fc770a2037f625d7a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744122"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER 函数

[!include [banner](../includes/banner.md)]

`FA_SUM` 函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产金额、价值模型代码和日期期限组成。

## <a name="syntax"></a>语法

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>参数

`fixed asset code`：*字符串*

一个*字符串*值，表示要为其计算余额的固定资产项目的代码。

`value model code`：*字符串*

一个*字符串*值，表示要为其计算余额的价值模型的代码。

`start date`：*日期*

表示固定资产金额计算期间的开始日期的*日期*值。

`end date`：*日期*

表示固定资产金额计算期间的结束日期的*日期*值。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example"></a>示例

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` 返回已为 **Current** 价值模型准备的期间为 **Date1** 到 **Date2** 的固定资产 **COMP-000001** 的数据容器。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)
