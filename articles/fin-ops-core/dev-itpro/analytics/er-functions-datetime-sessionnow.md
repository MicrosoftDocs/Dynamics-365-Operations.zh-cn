---
title: SESSIONNOW ER 函数
description: 本主题提供有关 SESSIONNOW 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 47b88a1ca0ea9fd09c2a82963901d9ace78891bb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746785"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="652f8-103">SESSIONNOW ER 函数</span><span class="sxs-lookup"><span data-stu-id="652f8-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="652f8-104">`SESSIONNOW` 函数返回一个 *日期时间* 值，此值表示当前应用程序会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="652f8-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="652f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="652f8-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="652f8-106">返回值</span><span class="sxs-lookup"><span data-stu-id="652f8-106">Return values</span></span>

<span data-ttu-id="652f8-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="652f8-107">*DateTime*</span></span>

<span data-ttu-id="652f8-108">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="652f8-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="652f8-109">示例</span><span class="sxs-lookup"><span data-stu-id="652f8-109">Example</span></span>

<span data-ttu-id="652f8-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。</span><span class="sxs-lookup"><span data-stu-id="652f8-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="652f8-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="652f8-111">Additional resources</span></span>

[<span data-ttu-id="652f8-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="652f8-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]