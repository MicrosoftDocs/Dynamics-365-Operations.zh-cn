---
title: 仓库库存调整
description: 本主题提供有关使用缩放单元时仓库库存调整日记帐和处理的信息。
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938218"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="25e02-103">仓库库存调整</span><span class="sxs-lookup"><span data-stu-id="25e02-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="25e02-104">当为[制造工作负荷](cloud-edge-workload-manufacturing.md)和[仓库管理工作负荷](cloud-edge-workload-warehousing.md)运行云和边缘缩放单元时，将使用“仓库库存调整”功能。</span><span class="sxs-lookup"><span data-stu-id="25e02-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="25e02-105">当工作人员使用仓库应用针对缩放单元仓库管理工作负荷进行库存调整时，必须由 **仓库库存调整日记帐** 批处理作业处理实际现有量更新，您可以转到 **仓库管理 > 定期任务 > 仓库库存调整日记** 来运行和计划此作业。</span><span class="sxs-lookup"><span data-stu-id="25e02-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="25e02-106">以下仓库应用工作流程当前对缩放单元工作负荷使用 **仓库库存调整日记帐**：</span><span class="sxs-lookup"><span data-stu-id="25e02-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="25e02-107">调入/调出</span><span class="sxs-lookup"><span data-stu-id="25e02-107">Adjustment in/out</span></span>
- <span data-ttu-id="25e02-108">周期盘点</span><span class="sxs-lookup"><span data-stu-id="25e02-108">Cycle counting</span></span>
- <span data-ttu-id="25e02-109">牌照加载</span><span class="sxs-lookup"><span data-stu-id="25e02-109">License plate loading</span></span>

<span data-ttu-id="25e02-110">由于中心和缩放单元部署共享库存记录，因此在库存调整流程中将多个库存交易创建为云和边缘的一部分。</span><span class="sxs-lookup"><span data-stu-id="25e02-110">Several inventory transactions are created as part of cloud and edge an inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="25e02-111">库存调整示例</span><span class="sxs-lookup"><span data-stu-id="25e02-111">Inventory adjustment example</span></span>

<span data-ttu-id="25e02-112">在此示例中，仓库工作人员已使用仓库应用登记了现有库存量的增加。</span><span class="sxs-lookup"><span data-stu-id="25e02-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="25e02-113">首先，缩放单元工作负荷为正实际调整创建仓库库存调整交易，然后交易将被同步到中心，致使中心现有库存量增加。</span><span class="sxs-lookup"><span data-stu-id="25e02-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="25e02-114">类型</span><span class="sxs-lookup"><span data-stu-id="25e02-114">Type</span></span>                                    | <span data-ttu-id="25e02-115">缩放单元</span><span class="sxs-lookup"><span data-stu-id="25e02-115">Scale unit</span></span> | <span data-ttu-id="25e02-116">方向</span><span class="sxs-lookup"><span data-stu-id="25e02-116">Direction</span></span> | <span data-ttu-id="25e02-117">中心</span><span class="sxs-lookup"><span data-stu-id="25e02-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="25e02-118">仓库库存调整</span><span class="sxs-lookup"><span data-stu-id="25e02-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="25e02-119">+1</span><span class="sxs-lookup"><span data-stu-id="25e02-119">+1</span></span>         | ->        | <span data-ttu-id="25e02-120">+1</span><span class="sxs-lookup"><span data-stu-id="25e02-120">+1</span></span>  |

<span data-ttu-id="25e02-121">然后，中心处理盘点日记帐过帐，这通过[消息处理器消息](cloud-edge-message-processor-messages.md)接收。</span><span class="sxs-lookup"><span data-stu-id="25e02-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="25e02-122">这将更新其他现有库存。</span><span class="sxs-lookup"><span data-stu-id="25e02-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="25e02-123">为了防止重叠的现有库存，中心将在此流程中创建抵销交易，并删除与仓库库存调整有关的先前记录的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="25e02-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="25e02-124">类型</span><span class="sxs-lookup"><span data-stu-id="25e02-124">Type</span></span>                                    | <span data-ttu-id="25e02-125">缩放单元</span><span class="sxs-lookup"><span data-stu-id="25e02-125">Scale unit</span></span> | <span data-ttu-id="25e02-126">方向</span><span class="sxs-lookup"><span data-stu-id="25e02-126">Direction</span></span> | <span data-ttu-id="25e02-127">中心</span><span class="sxs-lookup"><span data-stu-id="25e02-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="25e02-128">盘点</span><span class="sxs-lookup"><span data-stu-id="25e02-128">Counting</span></span>                                | <span data-ttu-id="25e02-129">+1</span><span class="sxs-lookup"><span data-stu-id="25e02-129">+1</span></span>         | <-        | <span data-ttu-id="25e02-130">+1</span><span class="sxs-lookup"><span data-stu-id="25e02-130">+1</span></span>  |
| <span data-ttu-id="25e02-131">仓库库存调整（抵销）</span><span class="sxs-lookup"><span data-stu-id="25e02-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="25e02-132">-1</span><span class="sxs-lookup"><span data-stu-id="25e02-132">-1</span></span>         | <-        | <span data-ttu-id="25e02-133">-1</span><span class="sxs-lookup"><span data-stu-id="25e02-133">-1</span></span>  |

<span data-ttu-id="25e02-134">缩放单元在中心创建了 **仓库库存调整日记帐** 之后，您可以查看中心作为调整流程一部分创建的 **盘点日记帐** 和 **抵销日记帐**。</span><span class="sxs-lookup"><span data-stu-id="25e02-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="25e02-135">您可以通过执行以下步骤在 Supply Chain Management 中查看这些日记帐条目和交易的每一个：</span><span class="sxs-lookup"><span data-stu-id="25e02-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="25e02-136">登录到缩放单元。</span><span class="sxs-lookup"><span data-stu-id="25e02-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="25e02-137">转到 **仓库管理 \> 定期任务 \> 仓库库存调整日记帐**。</span><span class="sxs-lookup"><span data-stu-id="25e02-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="25e02-138">在 **仓库库存调整日记帐** 页上，找到并打开记录库存现有量更改的日记帐。</span><span class="sxs-lookup"><span data-stu-id="25e02-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="25e02-139">**日记帐行** 部分显示此日记帐记录的每个调整。</span><span class="sxs-lookup"><span data-stu-id="25e02-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="25e02-140">登录到中心。</span><span class="sxs-lookup"><span data-stu-id="25e02-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="25e02-141">转到 **仓库管理 \> 定期任务 \> 仓库库存调整日记帐**。</span><span class="sxs-lookup"><span data-stu-id="25e02-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="25e02-142">在 **仓库库存调整日记帐** 页上，如果中心和缩放单元已同步，您应该会看到列出的相同日记帐。</span><span class="sxs-lookup"><span data-stu-id="25e02-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="25e02-143">打开日记帐。</span><span class="sxs-lookup"><span data-stu-id="25e02-143">Open the journal.</span></span> <span data-ttu-id="25e02-144">如果 [消息处理器消息](cloud-edge-message-processor-messages.md)已处理，您将在标头中看到指向 **盘点日记帐** 和 **抵销日记帐** 的链接。</span><span class="sxs-lookup"><span data-stu-id="25e02-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="25e02-145">**盘点日记帐** 应显示与日记帐行相同的维度值。</span><span class="sxs-lookup"><span data-stu-id="25e02-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="25e02-146">**抵销日记帐** 应显示将消除重叠的库存调整的抵销量。</span><span class="sxs-lookup"><span data-stu-id="25e02-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="25e02-147">完成所有同步和处理后，**盘点日记帐** 和 **抵销日记帐** 将被同步回缩放单元。</span><span class="sxs-lookup"><span data-stu-id="25e02-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="25e02-148">这些内容也可以从相关的 **仓库库存调整日记帐** 页查看。</span><span class="sxs-lookup"><span data-stu-id="25e02-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
