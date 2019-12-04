---
title: 折旧方法和惯例
description: 本文提供 Microsoft Dynamics 365 Finance 支持的折旧惯例和折旧方法的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3370db28f551b5ce4a9b49342cb0c0b2f3945c0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769492"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="a58a2-103">折旧方法和惯例</span><span class="sxs-lookup"><span data-stu-id="a58a2-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a58a2-104">本文提供支持的折旧惯例和折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="a58a2-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="a58a2-105">您可以选择不同的折旧法和惯例。</span><span class="sxs-lookup"><span data-stu-id="a58a2-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="a58a2-106">这些方法的目的是将固定资产的可折旧价值分摊到各会计期间中。</span><span class="sxs-lookup"><span data-stu-id="a58a2-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="a58a2-107">固定资产的可折旧价值是购置价格减去残值（如果有）。</span><span class="sxs-lookup"><span data-stu-id="a58a2-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="a58a2-108">如果您在使用折旧惯例并且修改某一资产的最后折旧开始日期（将跳过某些折旧），则最后一年的折旧可能高于或低于预期。</span><span class="sxs-lookup"><span data-stu-id="a58a2-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="a58a2-109">按最后折旧开始日期的修改影响的折旧期间的数目，调整折旧。</span><span class="sxs-lookup"><span data-stu-id="a58a2-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="a58a2-110">例如，如果您在超过三年后使用半年折旧惯例，则折旧通常在 3 1/2 年发生。</span><span class="sxs-lookup"><span data-stu-id="a58a2-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="a58a2-111">如果您在这一 3 1/2 年的期间中更改最后折旧开始日期，则折旧的最后一年会移出影响的期间外。</span><span class="sxs-lookup"><span data-stu-id="a58a2-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="a58a2-112">如果您按三个月移动日期，则最后一年将有九个月值得折旧，而正常情况下是有六个月值得折旧。</span><span class="sxs-lookup"><span data-stu-id="a58a2-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="a58a2-113">您可以从以下折旧惯例中进行选择。</span><span class="sxs-lookup"><span data-stu-id="a58a2-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="a58a2-114">半年</span><span class="sxs-lookup"><span data-stu-id="a58a2-114">Half year</span></span>
-   <span data-ttu-id="a58a2-115">全月</span><span class="sxs-lookup"><span data-stu-id="a58a2-115">Full month</span></span>
-   <span data-ttu-id="a58a2-116">季度中间</span><span class="sxs-lookup"><span data-stu-id="a58a2-116">Mid quarter</span></span>
-   <span data-ttu-id="a58a2-117">月中间(月的第 1 天)</span><span class="sxs-lookup"><span data-stu-id="a58a2-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="a58a2-118">月中间(月的第 15 天)</span><span class="sxs-lookup"><span data-stu-id="a58a2-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="a58a2-119">半年(年度开始)</span><span class="sxs-lookup"><span data-stu-id="a58a2-119">Half year (start of year)</span></span>
-   <span data-ttu-id="a58a2-120">半年(下一年)</span><span class="sxs-lookup"><span data-stu-id="a58a2-120">Half year (next year)</span></span>

<span data-ttu-id="a58a2-121">可以从以下计算方法中进行选择。</span><span class="sxs-lookup"><span data-stu-id="a58a2-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="a58a2-122">直线法</span><span class="sxs-lookup"><span data-stu-id="a58a2-122">Straight line service life</span></span>
-   <span data-ttu-id="a58a2-123">余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-123">Reducing balance</span></span>
-   <span data-ttu-id="a58a2-124">手动</span><span class="sxs-lookup"><span data-stu-id="a58a2-124">Manual</span></span>
-   <span data-ttu-id="a58a2-125">系数</span><span class="sxs-lookup"><span data-stu-id="a58a2-125">Factor</span></span>
-   <span data-ttu-id="a58a2-126">消耗量法</span><span class="sxs-lookup"><span data-stu-id="a58a2-126">Consumption</span></span>
-   <span data-ttu-id="a58a2-127">直线法(剩余年限)</span><span class="sxs-lookup"><span data-stu-id="a58a2-127">Straight line life remaining</span></span>
-   <span data-ttu-id="a58a2-128">200% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-128">200% reducing balance</span></span>
-   <span data-ttu-id="a58a2-129">175% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-129">175% reducing balance</span></span>
-   <span data-ttu-id="a58a2-130">150% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-130">150% reducing balance</span></span>
-   <span data-ttu-id="a58a2-131">125% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="a58a2-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="a58a2-132">Additional resources</span></span>
--------

[<span data-ttu-id="a58a2-133">固定资产折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="a58a2-134">直线法使用年限折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="a58a2-135">余额递减法折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="a58a2-136">手动折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="a58a2-137">因素/系数折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="a58a2-138">工作量法折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="a58a2-139">剩余年限法折旧</span><span class="sxs-lookup"><span data-stu-id="a58a2-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="a58a2-140">125% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a58a2-141">150% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a58a2-142">175% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="a58a2-143">200% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="a58a2-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



