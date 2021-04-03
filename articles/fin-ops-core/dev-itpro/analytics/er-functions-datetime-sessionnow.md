---
title: SESSIONNOW ER 函数
description: 本主题提供有关 SESSIONNOW 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: a79e8055a4b5025e1b1c4ab91875cf165fa8b354
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563382"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="9bb72-103">SESSIONNOW ER 函数</span><span class="sxs-lookup"><span data-stu-id="9bb72-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bb72-104">`SESSIONNOW` 函数返回一个 *日期时间* 值，此值表示当前应用程序会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="9bb72-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb72-105">语法</span><span class="sxs-lookup"><span data-stu-id="9bb72-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="9bb72-106">返回值</span><span class="sxs-lookup"><span data-stu-id="9bb72-106">Return values</span></span>

<span data-ttu-id="9bb72-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="9bb72-107">*DateTime*</span></span>

<span data-ttu-id="9bb72-108">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="9bb72-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="9bb72-109">示例</span><span class="sxs-lookup"><span data-stu-id="9bb72-109">Example</span></span>

<span data-ttu-id="9bb72-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。</span><span class="sxs-lookup"><span data-stu-id="9bb72-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bb72-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="9bb72-111">Additional resources</span></span>

[<span data-ttu-id="9bb72-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="9bb72-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]