---
title: "工作量法折旧"
description: "本文提供消耗量折旧方法的概览。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c0f64fee275f63a3e6b31a196df872e41c84dde6
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="consumption-depreciation"></a><span data-ttu-id="2e6bb-103">工作量法折旧</span><span class="sxs-lookup"><span data-stu-id="2e6bb-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e6bb-104">本文提供消耗量折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="2e6bb-105">如果您为固定资产设置折旧模板，并在 **“折旧模板”** 页上的 **“方法”** 字段中选择 **“消耗量”**，则会根据使用率将固定资产分配给折旧模板。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="2e6bb-106">您不必在 **“折旧模板”** 页上设置百分比和时间间隔。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="2e6bb-107">在您创建使用“消耗量”方法的折旧模板后，可以通过多种方式设置折旧方法。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="2e6bb-108">设置和使用工作量法折旧</span><span class="sxs-lookup"><span data-stu-id="2e6bb-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="2e6bb-109">在 **“折旧模板”** 页上，创建折旧模板。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="2e6bb-110">对于工作量法计算，折旧模板必须有 ID 和名称，以及必须在 **“方法”** 字段中选择 **“消耗量”**。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="2e6bb-111">在 **“消耗系数”** 页上，设置消耗系数。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="2e6bb-112">每个消耗系数都必须具有 ID 和名称，以及指定为数量或百分比的消耗系数。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="2e6bb-113">在 **“工作量单位”** 页上，设置工作量单位。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="2e6bb-114">每个消耗单位都必须具有 ID 和名称。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="2e6bb-115">折旧单位用于计算 **“工作量法折旧”** 页上的工作量法折旧。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="2e6bb-116">单位的示例为千米 (km)、千克 (kg) 和小时。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="2e6bb-117">在 **“固定资产”** 页上，设置各个固定资产。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="2e6bb-118">对于每个固定资产，选择具有折旧模板的价值模型和折旧帐簿。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="2e6bb-119">如果您有使用基于“消耗量”方法折旧模版的固定资产，则必须为工作量法折旧设置值模型或折旧帐簿。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="2e6bb-120">此设置是在 **“价值模型”** 页的 **“折旧”** 选项卡或 **“折旧模板”** 的 **“常规”** 快速选项卡上完成的。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="2e6bb-121">您可以将同一价值模型用于多个固定资产。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="2e6bb-122">对于每个固定资产，选择具有折旧模板的价值模型和折旧帐簿。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="2e6bb-123">您不能直接在 **“固定资产”** 页上添加或修改折旧模板。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="2e6bb-124">您只能在 **“折旧帐簿”** 上修改折旧模板。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="2e6bb-125">在 **“价值模型”** 页或 **“折旧帐簿”** 页上，在 **“工作量法折旧”** 字段组中，在以下字段中输入信息：</span><span class="sxs-lookup"><span data-stu-id="2e6bb-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="2e6bb-126">消耗系数</span><span class="sxs-lookup"><span data-stu-id="2e6bb-126">Consumption factor</span></span>
    -   <span data-ttu-id="2e6bb-127">单位</span><span class="sxs-lookup"><span data-stu-id="2e6bb-127">Unit</span></span>
    -   <span data-ttu-id="2e6bb-128">单位折旧额</span><span class="sxs-lookup"><span data-stu-id="2e6bb-128">Unit depreciation</span></span>
    -   <span data-ttu-id="2e6bb-129">估计消耗量</span><span class="sxs-lookup"><span data-stu-id="2e6bb-129">Estimated consumption</span></span>

    <span data-ttu-id="2e6bb-130">**“已过帐的消耗量”** 字段按单位显示已为固定资产和价值模型组合或固定资产折旧帐簿过帐的工作量法折旧。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="2e6bb-131">不能在此字段中手动更新值。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="2e6bb-132">示例</span><span class="sxs-lookup"><span data-stu-id="2e6bb-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="2e6bb-133">示例 1</span><span class="sxs-lookup"><span data-stu-id="2e6bb-133">Example 1</span></span>

<span data-ttu-id="2e6bb-134">为 1 月 31 日设置以下消耗系数：</span><span class="sxs-lookup"><span data-stu-id="2e6bb-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="2e6bb-135">数量为 1,000。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="2e6bb-136">为固定资产指定的单位折旧价格为 1.5。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="2e6bb-137">1 月 31 日的折旧方案如下：数量 × 单位折旧 1,000 × 1.5 = 1,500。如果为固定资产指定的系数是百分比系数，则在 **“估计消耗量”** 字段中为固定资产的价值模型估计的数量会乘以为所选结束日期设置的百分比。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="2e6bb-138">然后，生成的数量建议作为期间的折旧数量。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="2e6bb-139">示例 2</span><span class="sxs-lookup"><span data-stu-id="2e6bb-139">Example 2</span></span>

<span data-ttu-id="2e6bb-140">为 1 月 31 日设置以下工作量法折旧系数：</span><span class="sxs-lookup"><span data-stu-id="2e6bb-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="2e6bb-141">百分比为 10%。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="2e6bb-142">为固定资产指定的单位折旧价格为 1.5。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="2e6bb-143">固定资产的估计数量为 2,000。</span><span class="sxs-lookup"><span data-stu-id="2e6bb-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="2e6bb-144">1 月 31 日的折旧方案如下：估计数量 × 百分比 × 单位折旧 2,000 × .10 × 1.5 = 300</span><span class="sxs-lookup"><span data-stu-id="2e6bb-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




