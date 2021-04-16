---
title: 采购申请
description: 本主题介绍计划优化中如何支持采购申请。
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808032"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="5c174-103">采购申请</span><span class="sxs-lookup"><span data-stu-id="5c174-103">Purchase requisitions</span></span>

<span data-ttu-id="5c174-104">主计划可以补充已审核的采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="5c174-105">因此，要覆盖采购申请，用户不必使用工作流来创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="5c174-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="5c174-106">而可以通过主计划覆盖采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="5c174-107">由于此功能，采购申请可以生成采购订单、转移单或生产订单，具体取决于为相关产品设置的 **计划订单类型** 值。</span><span class="sxs-lookup"><span data-stu-id="5c174-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="5c174-108">让主计划包括申请</span><span class="sxs-lookup"><span data-stu-id="5c174-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="5c174-109">要在主计划的覆盖范围计算期间包括申请，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5c174-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="5c174-110">转到 **主计划** \> **设置** \> **计划** \> **主计划**。</span><span class="sxs-lookup"><span data-stu-id="5c174-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="5c174-111">创建或选择主计划。</span><span class="sxs-lookup"><span data-stu-id="5c174-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="5c174-112">在 **常规** 快速选项卡上，将 **包括申请** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="5c174-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="5c174-113">对要包括申请的其他每个主计划重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="5c174-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="5c174-114">已审核的申请时限</span><span class="sxs-lookup"><span data-stu-id="5c174-114">Approved requisitions time fence</span></span>

<span data-ttu-id="5c174-115">*已审核的申请时限* 确定主计划包括已审核的补货申请的需求要追溯多长时间（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="5c174-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="5c174-116">您可以在覆盖范围组级别和主计划级别设置已审核的申请时限。</span><span class="sxs-lookup"><span data-stu-id="5c174-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="5c174-117">为覆盖范围组设置已审核的申请时限</span><span class="sxs-lookup"><span data-stu-id="5c174-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="5c174-118">转到 **主计划** \> **设置** \> **覆盖范围** \> **覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="5c174-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="5c174-119">创建或选择一个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="5c174-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="5c174-120">在 **其他** 快速选项卡上，将 **已审核的申请时限(天)** 字段设置为时限要包括的天数。</span><span class="sxs-lookup"><span data-stu-id="5c174-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="5c174-121">对要设置已审核的申请时限的其他每个覆盖范围组重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="5c174-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="5c174-122">为各个主计划设置已审核的申请时限</span><span class="sxs-lookup"><span data-stu-id="5c174-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="5c174-123">当您为单个主计划设置已审核的申请时限时，设置将替代任何适用覆盖范围组的时限设置。</span><span class="sxs-lookup"><span data-stu-id="5c174-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="5c174-124">转到 **主计划** \> **设置** \> **计划** \> **主计划**。</span><span class="sxs-lookup"><span data-stu-id="5c174-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="5c174-125">创建或选择主计划。</span><span class="sxs-lookup"><span data-stu-id="5c174-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="5c174-126">在 **时限(天)** 快速选项卡上，将 **已审核的申请时限(天)** 字段设置为时限要包括的天数。</span><span class="sxs-lookup"><span data-stu-id="5c174-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="5c174-127">对要设置已审核的申请时限的其他每个主计划重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="5c174-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c174-128">**即将推出：** 计划优化尚不支持已审核的申请时限。</span><span class="sxs-lookup"><span data-stu-id="5c174-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="5c174-129">在支持之前，您在 **已审核的申请时限(天)** 字段中输入的所有值都将被忽略。</span><span class="sxs-lookup"><span data-stu-id="5c174-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="5c174-130">独立供应，不考虑覆盖范围代码</span><span class="sxs-lookup"><span data-stu-id="5c174-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="5c174-131">采购申请始终由独立的计划订单覆盖，而不考虑覆盖范围代码。</span><span class="sxs-lookup"><span data-stu-id="5c174-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="5c174-132">此行为将确保采购申请和补货订单之间具有清晰的可追溯性和工作流。</span><span class="sxs-lookup"><span data-stu-id="5c174-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="5c174-133">示例 1</span><span class="sxs-lookup"><span data-stu-id="5c174-133">Example 1</span></span>

<span data-ttu-id="5c174-134">设置产品时，其 **覆盖范围代码** 值为 *最小值/最大值*。它具有以下库存和申请状态：</span><span class="sxs-lookup"><span data-stu-id="5c174-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="5c174-135">现有库存数量 = 10。</span><span class="sxs-lookup"><span data-stu-id="5c174-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="5c174-136">最小库存数量 = 15。</span><span class="sxs-lookup"><span data-stu-id="5c174-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="5c174-137">最大库存数量 = 20。</span><span class="sxs-lookup"><span data-stu-id="5c174-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="5c174-138">存在针对一件产品的采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="5c174-139">请求日期是今天。</span><span class="sxs-lookup"><span data-stu-id="5c174-139">It has a requested date of today.</span></span>

<span data-ttu-id="5c174-140">当主计划运行时，创建了两个计划订单：一个是将库存补充到最大数量的 10 件产品的计划订单，另一个是补充采购申请的 1 件产品的计划订单。</span><span class="sxs-lookup"><span data-stu-id="5c174-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="5c174-141">示例 2</span><span class="sxs-lookup"><span data-stu-id="5c174-141">Example 2</span></span>

<span data-ttu-id="5c174-142">设置产品时，其 **覆盖范围代码** 值为 *最小值/最大值*。它具有以下库存和申请状态：</span><span class="sxs-lookup"><span data-stu-id="5c174-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="5c174-143">现有库存数量 = 17。</span><span class="sxs-lookup"><span data-stu-id="5c174-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="5c174-144">最小库存数量 = 15。</span><span class="sxs-lookup"><span data-stu-id="5c174-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="5c174-145">最大库存数量 = 20。</span><span class="sxs-lookup"><span data-stu-id="5c174-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="5c174-146">存在针对一件产品的采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="5c174-147">请求日期是今天。</span><span class="sxs-lookup"><span data-stu-id="5c174-147">It has a requested date of today.</span></span>

<span data-ttu-id="5c174-148">主计划运行时，创建了一个针对一件产品的计划订单来补充采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="5c174-149">示例 3</span><span class="sxs-lookup"><span data-stu-id="5c174-149">Example 3</span></span>

<span data-ttu-id="5c174-150">设置产品时，其 **覆盖范围代码** 值为 *期间*，期间长度为 7 天。</span><span class="sxs-lookup"><span data-stu-id="5c174-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="5c174-151">它具有以下库存、销售订单和请购状态：</span><span class="sxs-lookup"><span data-stu-id="5c174-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="5c174-152">现有库存数量 = 0。</span><span class="sxs-lookup"><span data-stu-id="5c174-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="5c174-153">存在采购五件产品的采购订单。</span><span class="sxs-lookup"><span data-stu-id="5c174-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="5c174-154">预期装运日期是今天加上一天。</span><span class="sxs-lookup"><span data-stu-id="5c174-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="5c174-155">存在针对三件产品的采购申请。</span><span class="sxs-lookup"><span data-stu-id="5c174-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="5c174-156">请求日期是今天加上三天。</span><span class="sxs-lookup"><span data-stu-id="5c174-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="5c174-157">当主计划运行时，创建了两个计划订单：一个是补充采购申请的 3 件产品的计划订单，另一个是补充销售订单需求的 5 件产品的计划订单。</span><span class="sxs-lookup"><span data-stu-id="5c174-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="5c174-158">限定到采购申请的计划订单确认后，计划引擎保留采购申请限定。</span><span class="sxs-lookup"><span data-stu-id="5c174-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="5c174-159">如果后来发现确认订单缺少一些满足采购申请所需的数量，系统将为相差数量创建一个新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="5c174-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="5c174-160">有关采购申请的详细信息，请参阅[采购申请概述](../../procurement/purchase-requisitions-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5c174-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]