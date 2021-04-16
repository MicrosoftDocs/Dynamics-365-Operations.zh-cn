---
title: 减少拆分后的余额折旧
description: 本主题描述固定资产中使用减少余额方法拆分资产后用于计算折旧的方法。
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 056808b7d4d490bc4d60aa058108d159c1d4867c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826243"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="0f0d1-103">减少拆分后的余额折旧</span><span class="sxs-lookup"><span data-stu-id="0f0d1-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f0d1-104">本主题描述固定资产中使用减少余额方法将资产拆分为另一资产后用于计算折旧的方法。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="0f0d1-105">在资产帐簿中配置的折旧年份是会计年度。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="0f0d1-106">有关详细信息，请参阅[减少余额折旧](reduce-balance-depreciation.md)和[拆分固定资产](tasks/split-fixed-asset.md)。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="0f0d1-107">如果在晚于资产的购置期间的会计期间拆分固定资产，减少的余额折旧将考虑前一年的资产帐面净值 (NBV)。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="0f0d1-108">还将考虑从拆分资产的交易中产生的购置和折旧调整交易。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="0f0d1-109">此行为假定资产在一个会计年度中购置，在下一会计年度中拆分。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="0f0d1-110">拆分后必须为原始资产折旧的金额反映资产拆分之前资产的资产 NBV，以及为拆分过帐的购置和折旧调整交易。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="0f0d1-111">例如，以下条件有效：</span><span class="sxs-lookup"><span data-stu-id="0f0d1-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="0f0d1-112">会计期间为 6 月 30 日至 7 月 1 日。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="0f0d1-113">减少的余额百分比为 18％，并于 2019 年 6 月以 10,000 美元的购置价购置了一项资产。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="0f0d1-114">第一个会计年度的折旧等于 18,000 美元，每月的折旧等于 150 美元，然后资产折旧到 2019 年 11 月，金额为 738.75 美元。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="0f0d1-115">在 2019 年 11 月，此资产的 80％ 被拆分为另一项固定资产。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="0f0d1-116">[![减少拆分后的余额折旧](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="0f0d1-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="0f0d1-117">原始资产的折旧额为 1,822.25 美元。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="0f0d1-118">该金额等于拆分交易过帐之前的 NBV（9,111.25 美元）加上拆分交易过帐期间产生的购置调整（-8,000 美元），再加上拆分交易期间产生的折旧调整（711 美元）。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="0f0d1-119">因此，第二年的折旧为 (1,822.25×18％) ÷12 = 27.33 美元。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="0f0d1-120">第一年新固定资产的折旧额为 (8,000×18％) ÷12 = 120 美元。</span><span class="sxs-lookup"><span data-stu-id="0f0d1-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]