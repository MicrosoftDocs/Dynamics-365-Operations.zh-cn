---
title: NOW ER 函数
description: 本主题提供有关 NOW 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: e8c411e1ce9656ffa35986f1ceef712c9def1e6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743511"
---
# <a name="now-er-function"></a><span data-ttu-id="82f52-103">NOW ER 函数</span><span class="sxs-lookup"><span data-stu-id="82f52-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82f52-104">`NOW` 函数返回一个*日期时间*值，此值表示当前应用程序服务器的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="82f52-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f52-105">语法</span><span class="sxs-lookup"><span data-stu-id="82f52-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="82f52-106">返回值</span><span class="sxs-lookup"><span data-stu-id="82f52-106">Return values</span></span>

<span data-ttu-id="82f52-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="82f52-107">*DateTime*</span></span>

<span data-ttu-id="82f52-108">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="82f52-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="82f52-109">示例</span><span class="sxs-lookup"><span data-stu-id="82f52-109">Example</span></span>

<span data-ttu-id="82f52-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期/时间值 2015 年 12 月 24 日为 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="82f52-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82f52-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="82f52-111">Additional resources</span></span>

[<span data-ttu-id="82f52-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="82f52-112">Date and time functions</span></span>](er-functions-category-datetime.md)
