---
title: TODAY ER 函数
description: 本主题提供有关 TODAY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746739"
---
# <a name="today-er-function"></a><span data-ttu-id="e1cc2-103">TODAY ER 函数</span><span class="sxs-lookup"><span data-stu-id="e1cc2-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1cc2-104">`TODAY` 函数返回一个 *日期* 值，此值表示当前应用程序服务器的日期。</span><span class="sxs-lookup"><span data-stu-id="e1cc2-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cc2-105">语法</span><span class="sxs-lookup"><span data-stu-id="e1cc2-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e1cc2-106">返回值</span><span class="sxs-lookup"><span data-stu-id="e1cc2-106">Return values</span></span>

<span data-ttu-id="e1cc2-107">*日期*</span><span class="sxs-lookup"><span data-stu-id="e1cc2-107">*Date*</span></span>

<span data-ttu-id="e1cc2-108">生成的日期值。</span><span class="sxs-lookup"><span data-stu-id="e1cc2-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e1cc2-109">示例</span><span class="sxs-lookup"><span data-stu-id="e1cc2-109">Example</span></span>

<span data-ttu-id="e1cc2-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期 2015 年 12 月 24 日为字符串 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="e1cc2-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1cc2-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="e1cc2-111">Additional resources</span></span>

[<span data-ttu-id="e1cc2-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="e1cc2-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]