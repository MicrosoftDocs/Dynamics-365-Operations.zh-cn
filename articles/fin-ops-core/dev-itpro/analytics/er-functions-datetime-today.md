---
title: TODAY ER 函数
description: 本主题提供有关 TODAY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683787"
---
# <a name="today-er-function"></a><span data-ttu-id="e6f7c-103">TODAY ER 函数</span><span class="sxs-lookup"><span data-stu-id="e6f7c-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6f7c-104">`TODAY` 函数返回一个 *日期* 值，此值表示当前应用程序服务器的日期。</span><span class="sxs-lookup"><span data-stu-id="e6f7c-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="e6f7c-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e6f7c-106">返回值</span><span class="sxs-lookup"><span data-stu-id="e6f7c-106">Return values</span></span>

<span data-ttu-id="e6f7c-107">*日期*</span><span class="sxs-lookup"><span data-stu-id="e6f7c-107">*Date*</span></span>

<span data-ttu-id="e6f7c-108">生成的日期值。</span><span class="sxs-lookup"><span data-stu-id="e6f7c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e6f7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6f7c-109">Example</span></span>

<span data-ttu-id="e6f7c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期 2015 年 12 月 24 日为字符串 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="e6f7c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6f7c-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="e6f7c-111">Additional resources</span></span>

[<span data-ttu-id="e6f7c-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="e6f7c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
