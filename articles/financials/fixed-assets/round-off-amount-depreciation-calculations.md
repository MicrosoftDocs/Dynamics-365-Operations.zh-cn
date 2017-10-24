---
title: "计算化整折旧金额"
description: "本文讨论在“帐簿设置”页找到的“化整折旧”字段。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ae5c24633a9ce4ce43e213581eb64c8548eecf5d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="5e009-103">计算化整折旧金额</span><span class="sxs-lookup"><span data-stu-id="5e009-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e009-104">本文讨论在“帐簿设置”页找到的“化整折旧”字段。</span><span class="sxs-lookup"><span data-stu-id="5e009-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="5e009-105">将为每个帐簿设置化差折扣金额。</span><span class="sxs-lookup"><span data-stu-id="5e009-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="5e009-106">化整折旧金额用于固定资产折旧图（显示固定资产的未来折旧和价值），也用于折旧方案。</span><span class="sxs-lookup"><span data-stu-id="5e009-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="5e009-107">输入此帐簿允许的最低折旧金额。</span><span class="sxs-lookup"><span data-stu-id="5e009-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="5e009-108">不管使用的是什么化整设置，系统都不会化整最近折旧期间的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="5e009-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="5e009-109">在最近折旧期间结束时，如果使用残值，则固定资产的值必须为 0（零）或残值。</span><span class="sxs-lookup"><span data-stu-id="5e009-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="5e009-110">示例</span><span class="sxs-lookup"><span data-stu-id="5e009-110">Example</span></span>

<span data-ttu-id="5e009-111">没有化整的折旧计算为 2,444.44。</span><span class="sxs-lookup"><span data-stu-id="5e009-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="5e009-112">如下表中所示，根据设置的化整方式，建议的金额将不同。</span><span class="sxs-lookup"><span data-stu-id="5e009-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="5e009-113">舍入方法</span><span class="sxs-lookup"><span data-stu-id="5e009-113">Rounding method</span></span> | <span data-ttu-id="5e009-114">折旧金额</span><span class="sxs-lookup"><span data-stu-id="5e009-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="5e009-115">化整 0.1</span><span class="sxs-lookup"><span data-stu-id="5e009-115">Rounding 0.1</span></span>    | <span data-ttu-id="5e009-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="5e009-116">2,444.40</span></span>            |
| <span data-ttu-id="5e009-117">化整 1.00</span><span class="sxs-lookup"><span data-stu-id="5e009-117">Rounding 1.00</span></span>   | <span data-ttu-id="5e009-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="5e009-118">2,444.00</span></span>            |
| <span data-ttu-id="5e009-119">化整 10.00</span><span class="sxs-lookup"><span data-stu-id="5e009-119">Rounding 10.00</span></span>  | <span data-ttu-id="5e009-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="5e009-120">2,440.00</span></span>            |
| <span data-ttu-id="5e009-121">化整 100.00</span><span class="sxs-lookup"><span data-stu-id="5e009-121">Rounding 100.00</span></span> | <span data-ttu-id="5e009-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="5e009-122">2,400.00</span></span>            |





