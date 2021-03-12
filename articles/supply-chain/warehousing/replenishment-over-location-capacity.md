---
title: 库位容量范围内的补货
description: 本主题提供有关“按位置容量补货”功能的信息。 此功能使创建当天所需的所有补货工作成为可能，并管理该补货工作的可用性，以确保领料位置既不会用完库存，也不会超出容量。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3f94053920b475ef9190b5ac65a5f9ca01dcd4a1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996115"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="bdc5b-104">库位容量范围内的补货</span><span class="sxs-lookup"><span data-stu-id="bdc5b-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdc5b-105">有些大容量或空间受限的仓库每天必须装运比领料位置将容纳的更多数量的物料。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="bdc5b-106">*按位置容量补货* 功能使创建当天所需的所有补货工作成为可能，并管理该补货工作的可用性，以确保领料位置既不会用完库存，也不会超出容量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="bdc5b-107">此功能使创建的补货工作多于某个位置所能容纳的数量，当该位置已满时，它将阻止完成补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="bdc5b-108">随着领料位置的库存下降到可配置阈值以下，可以进行更多的补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="bdc5b-109">启用“按位置容量补货”功能</span><span class="sxs-lookup"><span data-stu-id="bdc5b-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="bdc5b-110">要使此功能可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="bdc5b-111">组织范围内的工作阻止</span><span class="sxs-lookup"><span data-stu-id="bdc5b-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="bdc5b-112">库位容量范围内的补货</span><span class="sxs-lookup"><span data-stu-id="bdc5b-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="bdc5b-113">为示例方案设置此功能</span><span class="sxs-lookup"><span data-stu-id="bdc5b-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="bdc5b-114">本节提供指南和示例，演示如何设置此功能，以及如何为本主题后面提供的示例方案准备示例数据。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="bdc5b-115">启用示例数据</span><span class="sxs-lookup"><span data-stu-id="bdc5b-115">Enable sample data</span></span>

<span data-ttu-id="bdc5b-116">若要使用此处指定的示例记录和值演练[示例方案](#example-scenario)，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bdc5b-117">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="bdc5b-118">位置模板</span><span class="sxs-lookup"><span data-stu-id="bdc5b-118">Location profile</span></span>

<span data-ttu-id="bdc5b-119">在位置模板上启用按容量补货功能。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="bdc5b-120">转到 **仓库管理 \> 设置 \> 仓库 \> 位置模板**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="bdc5b-121">在左窗格中，选择 **PICK-06**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="bdc5b-122">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bdc5b-123">在 **补货** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-124">**超出位置容量**：*是*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="bdc5b-125">在启用时，补货工作将允许超过库位的最大产能。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="bdc5b-126">这也会启用 **补货** 快速选项卡上的其他字段。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="bdc5b-127">**工作可用性阈值类型**：*数量*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="bdc5b-128">此字段定义用于确定何时应释放更多工作的方法。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="bdc5b-129">您可以按数量或百分比释放：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="bdc5b-130">*百分比* – 选择此选项可以使用基于库存限制或容量的百分比容量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="bdc5b-131">选择此选项将启用 **溢出百分比** 字段，并禁用两个数量相关字段 **溢出数量** 和 **溢流单位**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="bdc5b-132">如果领料位置使用容量，可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="bdc5b-133">如果选择此选项，请将 **溢出百分比** 字段设置为可以进行更多补货工作的百分比。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="bdc5b-134">*数量* – 选择此选项可以使用特定的数量值。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="bdc5b-135">选择此选项将禁用 **溢出百分比** 字段，并启用 **溢出数量** 和 **溢流单位** 字段。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="bdc5b-136">当您没有对要补货的位置使用容量时，或者您希望在将更多库存放入该位置时数量保持一致时，使用此选项。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="bdc5b-137">如果选择此选项，请将 **溢出数量** 和 **溢流单位** 字段设置为可进行更多补货工作的数量和单位。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="bdc5b-138">**溢出数量**：*0.65*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="bdc5b-139">此字段定义位置溢出的数量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="bdc5b-140">只要位置的现有数量与工作数量的总和低于此值，工作就可以进行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="bdc5b-141">超过此值的任何补货工作将被锁定，并且必须手动解锁。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="bdc5b-142">计算工作数量时将考虑位置库存限制。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="bdc5b-143">**溢出单位**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="bdc5b-144">此字段定义与溢出量关联的单位。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="bdc5b-145">在此例中，当位置降至 0.65 托盘 (PL) 时，可以进行更多补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="bdc5b-146">**超额百分比**</span><span class="sxs-lookup"><span data-stu-id="bdc5b-146">**Overflow percentage**</span></span>

        <span data-ttu-id="bdc5b-147">此字段定义位置溢出的百分比。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="bdc5b-148">只要位置的现有数量与工作数量的总和低于此百分比，工作就可以进行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="bdc5b-149">超过此值的任何补货工作数量百分比将被锁定，并且必须手动解锁。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="bdc5b-150">计算工作数量百分比时将考虑位置库存限制。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="bdc5b-151">如果未定义库位库存限制，则在位置模板中定义了体积约束后，将按体积计算工作数量百分比。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bdc5b-152">如果您使用的是 **USMF** 法人的演示数据，并且先前已打开 *位置牌照定位* 功能，则必须关闭 **BULK-06** 位置模板的 **启用牌照定位** 设置，才能完成示例方案中的移动步骤。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="bdc5b-153">波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="bdc5b-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="bdc5b-154">要按照此处所述设置波次步骤代码，您可能首先必须使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)打开名为 *组织范围内的波次步骤代码* 的功能。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="bdc5b-155">转到 **仓库管理 \> 设置 \> 波次 \> 波次步骤代码**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="bdc5b-156">选择 **新建**，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="bdc5b-157">**波次步骤代码**：*Replen*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="bdc5b-158">**波次步骤描述**：*补货*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="bdc5b-159">**波次步骤类型**：*补货*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="bdc5b-160">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="bdc5b-161">补货模板</span><span class="sxs-lookup"><span data-stu-id="bdc5b-161">Replenishment template</span></span>

<span data-ttu-id="bdc5b-162">补货模板是控制何时和如何为货位补货的一系列规则。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="bdc5b-163">转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="bdc5b-164">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bdc5b-165">在 **概览** 部分，选择 **补货模板** 字段设置为 *需求补货* 的行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="bdc5b-166">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-166">Set the following values:</span></span>

    - <span data-ttu-id="bdc5b-167">**波次步骤代码**：*Replen*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="bdc5b-168">\**允许波次需求使用未预留数量：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="bdc5b-169">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="bdc5b-170">波次模板</span><span class="sxs-lookup"><span data-stu-id="bdc5b-170">Wave template</span></span>

1. <span data-ttu-id="bdc5b-171">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="bdc5b-172">在左窗格中，将 **波次模板类型** 设置为 *装运*。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="bdc5b-173">在列表中选择模板 **61 装运**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="bdc5b-174">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bdc5b-175">在 **常规** 快速选项卡上，将 **自动化补货工作释放** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="bdc5b-176">将此选项设置为 *是* 来创建基于需求的补货工作并将其自动释放。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="bdc5b-177">您必须将补货波次方法添加到波次模板，然后创建 **波次需求** 类型的补货模板。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="bdc5b-178">在 **补货模板** 页设置一个补货模板。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="bdc5b-179">要设置补货模板，必须将补货方法添加到波次模板。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="bdc5b-180">在 **方法** 快速选项卡上，在 **选定方法** 列中，找到以下行：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="bdc5b-181">**方法名称**：*补货*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="bdc5b-182">**名称**：*补货*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="bdc5b-183">将此行的 **波次步骤代码** 字段设置为 *Replen*。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="bdc5b-184">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bdc5b-185">示例场景</span><span class="sxs-lookup"><span data-stu-id="bdc5b-185">Example scenario</span></span>

<span data-ttu-id="bdc5b-186">在使所有前面描述的示例数据可用并进行设置之后，您可以演练此方案来试用 *按位置容量补货* 功能了。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="bdc5b-187">此方案中显示的值假设您使用的是标准演示数据，选择了 **USMF** 法人，并且您准备了本主题前面介绍的示例记录。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="bdc5b-188">此方案还可以用作说明如何在生产设置中使用此功能的示例。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="bdc5b-189">创建补货工作</span><span class="sxs-lookup"><span data-stu-id="bdc5b-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="bdc5b-190">创建销售订单 1</span><span class="sxs-lookup"><span data-stu-id="bdc5b-190">Create sales order 1</span></span>

1. <span data-ttu-id="bdc5b-191">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bdc5b-192">在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bdc5b-193">在对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-194">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="bdc5b-195">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bdc5b-196">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bdc5b-197">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-197">The new sales order is opened.</span></span> <span data-ttu-id="bdc5b-198">将在 **销售订单行** 快速选项卡中添加一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bdc5b-199">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-200">\**物料编号：\*\*\*T0100*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bdc5b-201">**数量：** *40*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="bdc5b-202">在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bdc5b-203">在 **预留** 页上，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bdc5b-204">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-204">Close the page.</span></span>
1. <span data-ttu-id="bdc5b-205">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bdc5b-206">您将收到显示创建的波次 ID 和装运 ID 的信息性消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bdc5b-207">补货波次也将创建。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bdc5b-208">您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”</span><span class="sxs-lookup"><span data-stu-id="bdc5b-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="bdc5b-209">创建销售订单 2</span><span class="sxs-lookup"><span data-stu-id="bdc5b-209">Create sales order 2</span></span>

1. <span data-ttu-id="bdc5b-210">在 **所有销售订单** 页面上，在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bdc5b-211">在对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="bdc5b-212">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="bdc5b-213">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bdc5b-214">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bdc5b-215">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-215">The new sales order is opened.</span></span> <span data-ttu-id="bdc5b-216">将在 **销售订单行** 快速选项卡中添加一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bdc5b-217">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-218">\**物料编号：\*\*\*T0100*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bdc5b-219">**数量：** *60*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="bdc5b-220">在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bdc5b-221">在 **预留** 页上，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bdc5b-222">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-222">Close the page.</span></span>
1. <span data-ttu-id="bdc5b-223">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bdc5b-224">您将收到显示创建的波次 ID 和装运 ID 的信息性消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bdc5b-225">补货波次也将创建。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bdc5b-226">您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”</span><span class="sxs-lookup"><span data-stu-id="bdc5b-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="bdc5b-227">创建销售订单 3</span><span class="sxs-lookup"><span data-stu-id="bdc5b-227">Create sales order 3</span></span>

1. <span data-ttu-id="bdc5b-228">在 **所有销售订单** 页面上，在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="bdc5b-229">在对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-230">**客户帐户**：*US-004*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="bdc5b-231">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bdc5b-232">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bdc5b-233">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-233">The new sales order is opened.</span></span> <span data-ttu-id="bdc5b-234">将在 **销售订单行** 快速选项卡中添加一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bdc5b-235">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="bdc5b-236">\**物料编号：\*\*\*T0100*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bdc5b-237">**数量：** *30*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="bdc5b-238">在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="bdc5b-239">在 **预留** 页上，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="bdc5b-240">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-240">Close the page.</span></span>
1. <span data-ttu-id="bdc5b-241">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bdc5b-242">您将收到显示创建的波次 ID 和装运 ID 的信息性消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="bdc5b-243">补货波次也将创建。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="bdc5b-244">您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”</span><span class="sxs-lookup"><span data-stu-id="bdc5b-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="bdc5b-245">查看工作详细信息</span><span class="sxs-lookup"><span data-stu-id="bdc5b-245">View work details</span></span>

1. <span data-ttu-id="bdc5b-246">转到 **仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="bdc5b-247">在 **概览** 部分，筛选仓库 *61* 的 **仓库** 列。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="bdc5b-248">您应该看到为三个需求销售订单创建了七个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="bdc5b-249">七个工作 ID 中有三个的 **工作订单类型** 值为 *补货*，四个的 **工作订单类型** 值为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="bdc5b-250">**工作订单类型** 值为 *补货* 的所有三个工作 ID 在 **行** 部分有相同的 *领料* 和 *放置* 位置：</span><span class="sxs-lookup"><span data-stu-id="bdc5b-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="bdc5b-251">**领料**：*02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="bdc5b-252">**放置**：*06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="bdc5b-253">为销售订单 1 创建了两个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="bdc5b-254">记下销售订单的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="bdc5b-255">根据您的现有数量，创建的工作数量可能会略有不同。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="bdc5b-256">但是，总体上，创建的工作标题应与此方案示例匹配。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="bdc5b-257">现有库存量牌照 ID</span><span class="sxs-lookup"><span data-stu-id="bdc5b-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="bdc5b-258">在此方案的后面，您将使用仓库应用（或模拟器），这时，您必须确定牌照才能完成领料和补货方案。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="bdc5b-259">要查找以后需要的牌照 ID，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="bdc5b-260">转到 **库存管理 \> 查询和报表 \> 现有量列表**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="bdc5b-261">选择 **显示筛选器** 按钮打开筛选器窗格。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="bdc5b-262">输入以下筛选条件以获取方案的车牌。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="bdc5b-263">使用 *开头为* 筛选器。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="bdc5b-264">\**物料编号：\*\*\*T0100*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="bdc5b-265">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="bdc5b-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="bdc5b-266">选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-266">Select **Apply**.</span></span>
1. <span data-ttu-id="bdc5b-267">在操作窗格上，选择 **维度**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="bdc5b-268">在 **维度显示** 对话框的 **存储维度** 部分，选择所有值。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="bdc5b-269">在 **事务** 部分，选择 **物料编号** 和 **数量 \<\> 0**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="bdc5b-270">完成后，选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="bdc5b-271">**现有** 网格显示每个位置物料 *T0100* 的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="bdc5b-272">记下每个位置的牌照，稍后您将需要此信息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="bdc5b-273">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="bdc5b-274">流程步骤</span><span class="sxs-lookup"><span data-stu-id="bdc5b-274">Process steps</span></span>

<span data-ttu-id="bdc5b-275">您将为前两个工作 ID 执行仓库位置补货。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="bdc5b-276">第三项补货工作的工作将被阻止，直到领料位置的库存级别降至阈值以下。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="bdc5b-277">补货</span><span class="sxs-lookup"><span data-stu-id="bdc5b-277">Replenishment</span></span>

1. <span data-ttu-id="bdc5b-278">以仓库 *61* 用户身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="bdc5b-279">（用户 ID 输入 *61*，密码输入 *1*。）</span><span class="sxs-lookup"><span data-stu-id="bdc5b-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bdc5b-280">转到 **库存 \> 补货**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="bdc5b-281">系统将提示您完成第一项补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="bdc5b-282">物料编号、数量和要领料的位置将显示。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="bdc5b-283">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bdc5b-284">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bdc5b-285">系统将为所领取物料的新牌照生成目标牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="bdc5b-286">选择 **确定** 确认值。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="bdc5b-287">放置工作将显示，指示用户将目标牌照放到补货位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="bdc5b-288">*放置* 位置应该是 **06A01R2S1B**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="bdc5b-289">确认放置详细信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="bdc5b-290">您将收到“工作已完成”消息，同时显示下一个补货领料任务的详细信息：物料编号、数量、要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="bdc5b-291">领料位置将与第一个补货位置相同。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="bdc5b-292">因此，牌照将具有与第一项补货工作任务使用的相同的牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="bdc5b-293">重复上述步骤完成第二项工作任务的补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="bdc5b-294">数量和目标牌照将不同于第一项工作任务的数量和目标牌照。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="bdc5b-295">在第二项补货工作完成后，您会收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bdc5b-296">移动设备也会通知您没有可进行的工作，即使剩余了一些补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="bdc5b-297">发生此行为的原因是补货工作的可用性状态为 *暂停*，因此被标记为 **已锁定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="bdc5b-298">*暂停* 状态被触发，是因为分配了工作的领料位置的位置模板的 **溢流数量** 值为 *0.65 PL*。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="bdc5b-299">之前的两项补货工作任务几乎已将位置填充到物料 *T0100* 的溢出限制。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="bdc5b-300">（物料的单位转换为 *1 托盘 = 100 个*。）因此，剩余的补货工作将导致该位置超出其溢出限制。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="bdc5b-301">直到从该位置领取了足够库存才能降低到移动设备菜单项上的工作释放阈值以下，此补货工作仍将处于锁定状态。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="bdc5b-302">销售订单领料</span><span class="sxs-lookup"><span data-stu-id="bdc5b-302">Sales order pick</span></span>

<span data-ttu-id="bdc5b-303">领料位置的库存必须消耗到可以解锁其余补货工作的级别，才能够完成剩余补货工作任务。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="bdc5b-304">换言之，该位置的现有库存数量与补货数量之和不能超过 **溢出数量** 值。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="bdc5b-305">当此和低于溢出数量时，剩余补货工作将被解锁。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="bdc5b-306">以仓库 *61* 用户身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="bdc5b-307">（用户 ID 输入 *61*，密码输入 *1*。）</span><span class="sxs-lookup"><span data-stu-id="bdc5b-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bdc5b-308">转到 **出站 \> 销售领料**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="bdc5b-309">输入销售订单 1 的第一个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="bdc5b-310">请参考您先前记下的 **工作详细信息** 页面上的销售订单的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="bdc5b-311">您在此处输入的工作 ID 将分别在两个位置生成数量为 10 个的领料工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="bdc5b-312">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-312">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-313">**销售订单：领料** 任务页面将显示第一个位置的物料编号、数量和要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="bdc5b-314">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bdc5b-315">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bdc5b-316">**销售订单：领料** 任务页面将显示下一个位置的物料编号、数量和要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="bdc5b-317">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bdc5b-318">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bdc5b-319">**销售订单：放置** 页面将指示您将完成的两项领料工作放到出站暂存位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="bdc5b-320">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-320">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-321">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="bdc5b-322">输入销售订单 1 的第二个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="bdc5b-323">此工作 ID 只有一个领料任务。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bdc5b-324">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-324">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-325">**销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bdc5b-326">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bdc5b-327">您指定的牌照将是补货工作任务中系统生成的牌照之一。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="bdc5b-328">为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bdc5b-329">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bdc5b-330">确认将任务放置到出站暂存位置的指示。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bdc5b-331">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-331">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-332">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="bdc5b-333">由于与其关联的补货任务未完成，销售订单 2 被锁定，无法领料。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="bdc5b-334">当前，领料位置的数量仍然为 30 个，销售订单 2 的补货数量为 60 个。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="bdc5b-335">现有库存量和补货库存量的总和（90 个）超出溢出数量 0.65 托盘（或 65 个）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="bdc5b-336">销售订单 3 必须先领料，然后才能够完成补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="bdc5b-337">输入销售订单 3 的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="bdc5b-338">此工作 ID 只有一个领料任务。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bdc5b-339">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-339">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-340">**销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bdc5b-341">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bdc5b-342">您指定的牌照将是补货工作任务中系统生成的牌照之一。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="bdc5b-343">为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bdc5b-344">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bdc5b-345">确认将任务放置到出站暂存位置的指示。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bdc5b-346">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-346">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-347">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="bdc5b-348">一旦领料位置的现有数量与补货数量之和低于阈值，您便可以处理剩余的补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="bdc5b-349">返回 **工作详细信息** 页面，注意补货最后一项工作（销售订单 2）的补货工作可用性为 *开放*，因为现在该位置有足够的空间来接受补货。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="bdc5b-350">您现在可以通过移动设备处理此补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="bdc5b-351">转到 **库存 \> 补货**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="bdc5b-352">系统将提示您完成剩余补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="bdc5b-353">物料编号、数量和要领料的位置将显示。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="bdc5b-354">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="bdc5b-355">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="bdc5b-356">系统将为所领取物料的新牌照生成目标牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="bdc5b-357">选择 **确定** 确认值。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="bdc5b-358">放置工作将显示，指示用户将目标牌照放到补货位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="bdc5b-359">*放置* 位置应该是 **06A01R2S1B**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="bdc5b-360">确认放置详细信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="bdc5b-361">您将收到“工作已完成”和“没有可进行的工作”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="bdc5b-362">现在，您可以为销售订单 2 领料。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-362">You can now pick sales order 2.</span></span> <span data-ttu-id="bdc5b-363">当与此销售订单关联的补货工作完成时，它将变为解锁状态。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="bdc5b-364">输入销售订单 2 的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="bdc5b-365">此工作 ID 只有一个领料任务。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="bdc5b-366">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-366">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-367">**销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="bdc5b-368">在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="bdc5b-369">您指定的牌照将是补货工作任务中系统生成的牌照。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="bdc5b-370">为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="bdc5b-371">选择 **确定** 按钮（复选标记符号）。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="bdc5b-372">确认将任务放置到出站暂存位置的指示。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="bdc5b-373">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-373">Select **OK**.</span></span>

    <span data-ttu-id="bdc5b-374">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="bdc5b-375">说明和提示</span><span class="sxs-lookup"><span data-stu-id="bdc5b-375">Notes and tips</span></span>

- <span data-ttu-id="bdc5b-376">此功能适用于所有类型的补货：波次需求、最小/最大、负荷需求和时隙。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="bdc5b-377">如果需要，您可以从 **工作详细信息** 页面手动覆盖每个工作标题的补货工作可用性。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="bdc5b-378">当系统设置补货工作可用性时，将考虑在完成任何工作之前该位置已经存在的任何库存</span><span class="sxs-lookup"><span data-stu-id="bdc5b-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="bdc5b-379">销售订单工作的每项工作都将关联到特定的补货工作。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="bdc5b-380">没有相应的销售工作可用性功能。</span><span class="sxs-lookup"><span data-stu-id="bdc5b-380">There is no corresponding sales work availability functionality.</span></span>
