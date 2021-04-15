---
title: 补货策略
description: 此主题提供有关补货策略的信息，并说明如何使用波次需求补货模板行上的“补货策略”字段选择补货方式。
author: mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 84c97bdbe00285d7992a25edbf5d42ffe9b58903
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814504"
---
# <a name="replenishment-strategies"></a><span data-ttu-id="a7a9f-103">补货策略</span><span class="sxs-lookup"><span data-stu-id="a7a9f-103">Replenishment strategies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7a9f-104">在 **补货模板** 页上定义的模板包括波次需求补货模板行，可用于选择补货的方式。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-104">The templates that are defined on the **Replenishment templates** page include wave demand replenishment template lines that let you select how replenishment is done.</span></span> <span data-ttu-id="a7a9f-105">每一行现在包含一个 **补货策略** 字段。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-105">Each line now includes a **Replenishment strategy** field.</span></span>

<span data-ttu-id="a7a9f-106">*波次需求数量* 策略是默认策略。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-106">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="a7a9f-107">它是在引入 **补货策略** 字段之前使用的补货策略。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-107">It's the replenishment strategy that was used before the introduction of the **Replenishment strategy** field.</span></span> <span data-ttu-id="a7a9f-108">它使用补货位置指令查找可以补货的位置。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-108">It uses the replenishment location directives to find locations that can be replenished.</span></span> <span data-ttu-id="a7a9f-109">然后，为这些位置补货，直到达到需求量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-109">It then replenishes those locations until the demand is covered.</span></span>

<span data-ttu-id="a7a9f-110">*最大位置容量* 策略引入了一些新功能。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-110">The *Maximum location capacity* strategy introduces some new functionality.</span></span> <span data-ttu-id="a7a9f-111">像 *波次需求数量* 策略一样，此策略使用补货位置指令来查找可以补货的位置，然后为这些位置补货，直到达到需求量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-111">Like the *Wave demand quantity* strategy, this strategy uses the replenishment location directives to find locations that can be replenished, and then it replenishes those locations until the demand is covered.</span></span> <span data-ttu-id="a7a9f-112">它不同于 *波次需求数量* 策略，因为所有补货位置将补货到位置库存限制定义的最大容量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-112">It differs from the *Wave demand quantity* strategy in that all the replenished locations are replenished to their maximum capacity, as defined by the location stocking limits.</span></span> <span data-ttu-id="a7a9f-113">*最大位置容量* 策略尝试创建工作来引入请求的数量以及一些额外数量，以填充要补货的位置。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-113">The *Maximum location capacity* strategy tries to create work to bring in the requested quantity, plus some extra quantity, to fill the locations that are being replenished.</span></span> <span data-ttu-id="a7a9f-114">但是，在有些情况下，该尝试可能失败。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-114">However, in some cases, that attempt might fail.</span></span> <span data-ttu-id="a7a9f-115">例如，堆放位置可能没有足够的库存来覆盖额外的数量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-115">For example, the bulk locations might not have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="a7a9f-116">在这些情况下，系统会检测到失败，然后尝试恢复。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-116">In these cases, the system detects the failure and tries to recover.</span></span>

<span data-ttu-id="a7a9f-117">旺季是 *最大位置容量* 策略优于 *波次需求数量* 策略情况的一个例子。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-117">Peak season is one example of a situation where the *Maximum location capacity* strategy is preferable to the *Wave demand quantity* strategy.</span></span> <span data-ttu-id="a7a9f-118">在旺季，一些物料可能会大量出售。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-118">During peak season, some items might be selling at high volume.</span></span> <span data-ttu-id="a7a9f-119">因此，您可能希望尽可能多地为相关领料位置主动补货，以减少为补货而创建的工作 ID 的数量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-119">Therefore, you might want to proactively replenish the relevant picking locations as much as possible, to reduce the number of work IDs that are created for replenishment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7a9f-120">要充分利用 *最大位置容量* 策略，您必须重新定义相关位置的库存限制。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-120">To take full advantage of the *Maximum location capacity* strategy, you must redefine the stocking limits for the relevant locations.</span></span> <span data-ttu-id="a7a9f-121">否则，此策略就与 *波次需求数量* 策略一样了。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-121">Otherwise, this strategy works just like the *Wave demand quantity* strategy.</span></span>

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a><span data-ttu-id="a7a9f-122">开启“根据库存限制进行最大补货”功能</span><span class="sxs-lookup"><span data-stu-id="a7a9f-122">Turn on the Replenish to max based on stocking limits feature</span></span>

<span data-ttu-id="a7a9f-123">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-123">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a7a9f-124">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查此功能的状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-124">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of this feature and turn it on if it's required.</span></span> <span data-ttu-id="a7a9f-125">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-125">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a7a9f-126">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="a7a9f-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a7a9f-127">**功能名称**：*根据库存限制进行最大补货*</span><span class="sxs-lookup"><span data-stu-id="a7a9f-127">**Feature name:** *Replenish to max based on stocking limits*</span></span>

## <a name="set-up-replenishment-strategies"></a><span data-ttu-id="a7a9f-128">设置补货策略</span><span class="sxs-lookup"><span data-stu-id="a7a9f-128">Set up replenishment strategies</span></span>

<span data-ttu-id="a7a9f-129">要访问模板，转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-129">To access the templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span> <span data-ttu-id="a7a9f-130">在 **概览** 部分，选择或创建波次需求补货模板，其中的 **补货类型** 字段设置为 *波次需求*。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-130">In the **Overview** section, select or create a wave demand replenishment template where the **Replenishment type** field is set to *Wave demand*.</span></span> <span data-ttu-id="a7a9f-131">然后在 **补货模板详细信息** 部分设置补货模板行。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-131">Then set up the replenishment template lines in the **Replenishment template details** section.</span></span> <span data-ttu-id="a7a9f-132">对于每一行，在 **补货策略** 字段中，选择要使用的补货策略。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-132">For each line, in the **Replenishment strategy** field, select the replenishment strategy that you want to use.</span></span>

<span data-ttu-id="a7a9f-133">![补货模板页](media/ReplenTempWaveDmdMaxLocCap.png "补货模板页")</span><span class="sxs-lookup"><span data-stu-id="a7a9f-133">![Replenishment templates page](media/ReplenTempWaveDmdMaxLocCap.png "Replenishment templates page")</span></span>

<span data-ttu-id="a7a9f-134">如果 **补货策略** 列未出现在 **补货模板详细信息** 部分的网格中，请确保此功能已开启，并且所选补货模板的补货类型为 *波次需求*。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-134">If the **Replenishment strategy** column doesn't appear in the grid in the **Replenishment template details** section, make sure that the feature has been turned on, and that the selected replenishment template has a replenishment type of *Wave demand*.</span></span>

> [!NOTE]
> <span data-ttu-id="a7a9f-135">*波次需求数量* 策略是默认策略。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-135">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="a7a9f-136">因此，您只需要更新要使用 *最大位置容量* 策略的补货模板行。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-136">Therefore, you just have to update the replenishment template lines where you want to use the *Maximum location capacity* strategy instead.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="a7a9f-137">示例方案</span><span class="sxs-lookup"><span data-stu-id="a7a9f-137">Example scenarios</span></span>

### <a name="example-1"></a><span data-ttu-id="a7a9f-138">示例 1</span><span class="sxs-lookup"><span data-stu-id="a7a9f-138">Example 1</span></span>

<span data-ttu-id="a7a9f-139">在此示例中，只有一个补货模板，它只有一个补货模板行。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-139">For this example, there is only one replenishment template that has only one replenishment template line.</span></span>

<span data-ttu-id="a7a9f-140">您为 130 件 (pcs) 物料 A0001 创建了一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-140">You create a sales order for 130 pieces (pcs) of item A0001.</span></span> <span data-ttu-id="a7a9f-141">在您将订单下达到仓库之前，仓库按以下方式设置：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-141">Before you release the order to the warehouse, the warehouse is set up in the following way:</span></span>

- <span data-ttu-id="a7a9f-142">只有一个堆放位置，该位置可用的现有库存量为 500 件。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-142">There is only one bulk location, and it has 500 pcs of available on-hand inventory.</span></span>
- <span data-ttu-id="a7a9f-143">有三个领料位置，每个领料位置的库存限制为 100 件。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-143">There are three pick locations, each of which has a stocking limit of 100 pcs.</span></span> <span data-ttu-id="a7a9f-144">（请记住，*最大位置容量* 策略需要有库存限制。）</span><span class="sxs-lookup"><span data-stu-id="a7a9f-144">(Remember that stocking limits are required for the *Maximum location capacity* strategy.)</span></span>
- <span data-ttu-id="a7a9f-145">补货放置位置与销售领料位置相同。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-145">The replenishment put locations are the same as the sales pick locations.</span></span>
- <span data-ttu-id="a7a9f-146">补货单位是箱（1 箱 = 20 件）。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-146">The replenishment unit is a box (1 box = 20 pcs).</span></span>

<span data-ttu-id="a7a9f-147">订购时，以下库存在销售领料位置有现有库存：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-147">At the time of the order, the following inventory is on hand at the sales pick locations:</span></span>

- <span data-ttu-id="a7a9f-148">**领料-001：** 20 件（1 箱）</span><span class="sxs-lookup"><span data-stu-id="a7a9f-148">**Pick-001:** 20 pcs (1 box)</span></span>
- <span data-ttu-id="a7a9f-149">**领料-002：** 0 件</span><span class="sxs-lookup"><span data-stu-id="a7a9f-149">**Pick-002:** 0 pcs</span></span>
- <span data-ttu-id="a7a9f-150">**领料-003：** 0 件</span><span class="sxs-lookup"><span data-stu-id="a7a9f-150">**Pick-003:** 0 pcs</span></span>

<span data-ttu-id="a7a9f-151">最初，补货策略设置为 *波次需求数量*。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-151">Initially, the replenishment strategy is set to *Wave demand quantity*.</span></span>

<span data-ttu-id="a7a9f-152">将销售订单下达到仓库，波次运行波次处理后，您获得以下补货工作：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-152">After you release the sales order to the warehouse, and wave processing runs for the wave, you get the following replenishment work:</span></span>

- <span data-ttu-id="a7a9f-153">**补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-153">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="a7a9f-154">**补货工作 2：** 从堆放位置领取 2 箱，将它们放到位置“领料-002”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-154">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="a7a9f-155">您将获得两个补货工作 ID，因为您必须为两个位置补货，但不支持多个放置。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-155">You get two replenishment work IDs because you must replenish two locations, and multi-puts aren't supported.</span></span>

<span data-ttu-id="a7a9f-156">如果您将补货策略设置为 *最大位置容量*，您将获得以下补货工作：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-156">If you set the replenishment strategy to *Maximum location capacity* instead, you get the following replenishment work:</span></span>

- <span data-ttu-id="a7a9f-157">**补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-157">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="a7a9f-158">**补货工作 2：** 从堆放位置领取 5 箱，将它们放到位置“领料-002”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-158">**Replenishment work 2:** Pick 5 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="a7a9f-159">[![示例 1](media/ReplenTemp_example_1.png "示例 1")](media/ReplenTemp_example_1_large.png)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-159">[![Example 1](media/ReplenTemp_example_1.png "Example 1")](media/ReplenTemp_example_1_large.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="a7a9f-160">示例 2</span><span class="sxs-lookup"><span data-stu-id="a7a9f-160">Example 2</span></span>

<span data-ttu-id="a7a9f-161">此示例显示了当堆放位置的库存不足以覆盖额外数量时发生的情况。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-161">This example shows what happens when the bulk location doesn't have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="a7a9f-162">它使用与示例 1 相同的场景，只是堆放位置有 160 件（8 箱）。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-162">It uses the same scenario as example 1, but the bulk location has 160 pcs (8 boxes).</span></span>

<span data-ttu-id="a7a9f-163">*波次需求数量* 策略创建与示例 1 相同的工作。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-163">The *Wave demand quantity* strategy creates the same work that it did in example 1.</span></span>

<span data-ttu-id="a7a9f-164">但是，由于 *最大位置容量* 策略尝试像示例 1 一样创建工作 ID，这可能会失败。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-164">However, because the *Maximum location capacity* strategy tries to create the work IDs as it did in example 1, it might fail.</span></span> <span data-ttu-id="a7a9f-165">这时，系统会尝试恢复。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-165">At that point, the system tries to recover.</span></span>

<span data-ttu-id="a7a9f-166">根据补货领料的位置指令上的 **允许拆分** 选项的设置，可能有两种结果：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-166">Depending on the setting of the **Allow split** option on the location directives for replenishment picking, two outcomes are possible:</span></span>

- <span data-ttu-id="a7a9f-167">如果 **允许拆分** 选项设置为 *是*，将创建以下补货工作：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-167">If the **Allow split** option is set to *Yes*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="a7a9f-168">**补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-168">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="a7a9f-169">**补货工作 2：** 从堆放位置领取 4 箱，将它们放到位置“领料-002”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-169">**Replenishment work 2:** Pick 4 boxes from the bulk location, and put them in location pick-002.</span></span>

- <span data-ttu-id="a7a9f-170">如果 **允许拆分** 选项设置为 *否*，将创建以下补货工作：</span><span class="sxs-lookup"><span data-stu-id="a7a9f-170">If the **Allow split** option is set to *No*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="a7a9f-171">**补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-171">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="a7a9f-172">**补货工作 2：** 从堆放位置领取 2 箱，将它们放到位置“领料-002”。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-172">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="a7a9f-173">结果会因创建工作时可用的信息不同而不同。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-173">The outcomes differ because of the information that is available when you create the work.</span></span> <span data-ttu-id="a7a9f-174">当在补货领料的位置指令上将 **允许拆分** 设置为 *是* 时，您知道您最终找到了 160 件。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-174">When the **Allow split** is set to *Yes* on the location directives for replenishment picking, you know that you managed to find 160 pcs.</span></span> <span data-ttu-id="a7a9f-175">因此，您可以为该数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-175">Therefore, you can create work for that quantity.</span></span> <span data-ttu-id="a7a9f-176">但是，当 **允许拆分** 选项设置为 *否* 时，您不知道这 160 件的存在。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-176">However, when the **Allow split** option is set to *No*, you don't know about the existence of the 160 pcs.</span></span> <span data-ttu-id="a7a9f-177">因为您决定补货的额外数量是 3 箱，所以您放弃了这个额外数量，再次尝试原始数量。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-177">Because the extra quantity that you decided to replenish was 3 boxes, you drop that extra quantity and try the original quantity again.</span></span>

<span data-ttu-id="a7a9f-178">[![示例 2](media/ReplenTemp_example_2.png "示例 2")](media/ReplenTemp_example_2_large.png)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-178">[![Example 2](media/ReplenTemp_example_2.png "Example 2")](media/ReplenTemp_example_2_large.png)</span></span>

<span data-ttu-id="a7a9f-179">因此，要为补货位置获得最大数量，应在补货领料的位置指令上将 **允许拆分** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="a7a9f-179">Therefore, to get the maximum quantity to the replenished locations, you should set the **Allow split** option to *Yes* on the location directives for replenishment picking.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]