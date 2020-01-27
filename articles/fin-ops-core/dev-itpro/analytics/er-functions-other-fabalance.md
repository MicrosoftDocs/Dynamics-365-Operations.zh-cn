---
title: FA_BALANCE ER 函数
description: 本主题提供有关 FA_BALANCE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916008"
---
# <a name="FA_BALANCE">FA_BALANCE ER 函数</a>

[!include [banner](../includes/banner.md)]

`FA_BALANCE` 函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产余额、价值模型代码、报告年度和报告日期数据组成。

## <a name="syntax"></a>语法

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>参数

`fixed asset code`：*字符串*

一个*字符串*值，表示要为其计算余额的固定资产项目的代码。

`value model code`：*字符串*

一个*字符串*值，表示要为其计算余额的价值模型的代码。

`reporting year`：*枚举值*

定义余额计算期间的 **AssetYear** 应用程序枚举的枚举值。

`reporting date`：*日期*

定义余额计算日期的*日期*值。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example"></a>示例

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` 返回已在当前应用程序会话日期为价值模型 **Current** 准备的固定资产 **COMP-000001** 的余额的数据容器。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)
