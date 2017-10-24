---
title: "库存锁定"
description: "本文提供库存锁定的概览，这是 Microsoft Dynamics 365 for Finance and Operations Enterprise版本中质量检查流程的一部分。 您可以使用库存锁定来阻止处理或消耗物料。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: eed2f3e203808f378ce954b6cc308859fea89e60
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---

# <a name="inventory-blocking"></a><span data-ttu-id="48d78-104">库存锁定</span><span class="sxs-lookup"><span data-stu-id="48d78-104">Inventory blocking</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="48d78-105">本文提供库存锁定的概览，这是 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本中质量检查流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="48d78-105">This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="48d78-106">您可以使用库存锁定来阻止处理或消耗物料。</span><span class="sxs-lookup"><span data-stu-id="48d78-106">You can use inventory blocking to prevent items from being processed or consumed.</span></span>

<span data-ttu-id="48d78-107">您可以按照以下方法锁定库存物料：</span><span class="sxs-lookup"><span data-stu-id="48d78-107">You can block inventory items in the following ways:</span></span>
-   <span data-ttu-id="48d78-108">手动</span><span class="sxs-lookup"><span data-stu-id="48d78-108">Manually</span></span>
-   <span data-ttu-id="48d78-109">通过创建质量订单</span><span class="sxs-lookup"><span data-stu-id="48d78-109">By creating a quality order</span></span>
-   <span data-ttu-id="48d78-110">通过使用生成质量订单的流程</span><span class="sxs-lookup"><span data-stu-id="48d78-110">By using a process that generates a quality order</span></span>
-   <span data-ttu-id="48d78-111">使用库存状态锁定</span><span class="sxs-lookup"><span data-stu-id="48d78-111">By using inventory status blocking</span></span>

## <a name="blocking-items-manually"></a><span data-ttu-id="48d78-112">手动锁定物料</span><span class="sxs-lookup"><span data-stu-id="48d78-112">Blocking items manually</span></span>
<span data-ttu-id="48d78-113">您可以通过在**库存锁定**页中创建交易记录来锁定物料的数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-113">You can block a quantity of an item by creating a transaction on the **Inventory blocking** page.</span></span> <span data-ttu-id="48d78-114">只有作为现有库存可用的物料可以被手动锁定。</span><span class="sxs-lookup"><span data-stu-id="48d78-114">Only items that are available as on-hand inventory can be blocked manually.</span></span> <span data-ttu-id="48d78-115">对于手动锁定的数量，您必须决定计划活动是否作为预期的现有数量包括预期收货。</span><span class="sxs-lookup"><span data-stu-id="48d78-115">For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity.</span></span> <span data-ttu-id="48d78-116">预期收货锁定您希望在检查完成后作为现有库存可用的物料。</span><span class="sxs-lookup"><span data-stu-id="48d78-116">Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed.</span></span> <span data-ttu-id="48d78-117">您可以维护预期日期。</span><span class="sxs-lookup"><span data-stu-id="48d78-117">You can maintain the expected date.</span></span> <span data-ttu-id="48d78-118">默认情况下，**预期收货**选项为通过质检订单锁定的物料选中。</span><span class="sxs-lookup"><span data-stu-id="48d78-118">By default, the **Expected receipts** option is selected for items that are blocked through a quality order.</span></span> <span data-ttu-id="48d78-119">您可以通过删除**库存锁定**页中的交易记录取消数量的手动锁定。</span><span class="sxs-lookup"><span data-stu-id="48d78-119">You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.</span></span>

## <a name="blocking-items-by-creating-a-quality-order"></a><span data-ttu-id="48d78-120">通过创建质检订单锁定物料</span><span class="sxs-lookup"><span data-stu-id="48d78-120">Blocking items by creating a quality order</span></span>
<span data-ttu-id="48d78-121">您可以通过在**质检订单**页上创建质检订单来指定必须检查的物料。</span><span class="sxs-lookup"><span data-stu-id="48d78-121">You can specify items that must be inspected by creating a quality order on the **Quality orders** page.</span></span> <span data-ttu-id="48d78-122">当您创建一个质量订单时，将锁定您为物料指定的数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-122">When you create a quality order, the quantity that you specify for an item is blocked.</span></span> <span data-ttu-id="48d78-123">与质检订单控制关联的抽样计划只控制必须检查的物料的数量，而不控制被锁定的数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-123">The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked.</span></span> <span data-ttu-id="48d78-124">在质检订单上输入的数量是已锁定的数量，不管抽样计划指定的数量是否应发送供检查。</span><span class="sxs-lookup"><span data-stu-id="48d78-124">The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.</span></span>

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a><span data-ttu-id="48d78-125">通过使用生成质检订单流程锁定物料</span><span class="sxs-lookup"><span data-stu-id="48d78-125">Blocking items by using a process that generates a quality order</span></span>
<span data-ttu-id="48d78-126">如果质量流程指定必须检查物料，则物料数量将被自动锁定。</span><span class="sxs-lookup"><span data-stu-id="48d78-126">If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically.</span></span> <span data-ttu-id="48d78-127">因此，当自动生成质检订单时，与该质检订单相关联的物料抽样计划同时控制锁定的物料的数量和必须检查的数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-127">Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected.</span></span> <span data-ttu-id="48d78-128">如果选择了**物料抽样**页中的**完全锁定**选项，则不管物料抽样数量，在检查期间锁定采购订单行等的整个数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-128">If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.</span></span>
### <a name="example"></a><span data-ttu-id="48d78-129">示例</span><span class="sxs-lookup"><span data-stu-id="48d78-129">Example</span></span>

<span data-ttu-id="48d78-130">在以下的示例中，过账采购订单的装箱单时生成了一个质量订单。</span><span class="sxs-lookup"><span data-stu-id="48d78-130">In the following example, a quality order is generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="48d78-131">在**质量关联**页中，您指定了采购订单装箱单的过帐为激活质量订单的流程。</span><span class="sxs-lookup"><span data-stu-id="48d78-131">On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.</span></span>

|<span data-ttu-id="48d78-132">设置</span><span class="sxs-lookup"><span data-stu-id="48d78-132">Setup</span></span>                                                                     |<span data-ttu-id="48d78-133">用户操作</span><span class="sxs-lookup"><span data-stu-id="48d78-133">User action</span></span>                 |<span data-ttu-id="48d78-134">结果</span><span class="sxs-lookup"><span data-stu-id="48d78-134">Result</span></span>             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| <span data-ttu-id="48d78-135">质量关联指定在采购订单装箱单过帐时必须生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="48d78-135">A quality association specifies that a quality order must be generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="48d78-136">质检订单的物料抽样设置指定必须检查 10% 的采购订单行数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-136">The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected.</span></span> <span data-ttu-id="48d78-137">此外，由于在物料抽样设置中选择了**完全锁定**选项，因此不管发送以供检查的数量，在检查期间必须锁定采购订单行的整个数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-137">Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection.</span></span> | <span data-ttu-id="48d78-138">过账装箱单。</span><span class="sxs-lookup"><span data-stu-id="48d78-138">The packing slip is posted.</span></span> | <span data-ttu-id="48d78-139">生成质量订单。</span><span class="sxs-lookup"><span data-stu-id="48d78-139">A quality order is generated.</span></span> <span data-ttu-id="48d78-140">将物料的 10% 的采购订单数量送检。</span><span class="sxs-lookup"><span data-stu-id="48d78-140">Ten percent of the purchase order quantity for the item is sent to inspection.</span></span> <span data-ttu-id="48d78-141">锁定该采购订单行的整个数量。</span><span class="sxs-lookup"><span data-stu-id="48d78-141">The full quantity of the purchase order line is blocked.</span></span> |

## <a name="blocking-items-by-using-inventory-status-blocking"></a><span data-ttu-id="48d78-142">通过使用库存状态锁定锁定物料</span><span class="sxs-lookup"><span data-stu-id="48d78-142">Blocking items by using inventory status blocking</span></span>
<span data-ttu-id="48d78-143">您可以使用**库存状态**页上的**锁定库存**参数指定哪些库存状态是锁定状态。</span><span class="sxs-lookup"><span data-stu-id="48d78-143">You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page.</span></span> <span data-ttu-id="48d78-144">您不能使用库存状态作为生产订单、销售订单、转移单、传出交易记录或项目集成的锁定状态。</span><span class="sxs-lookup"><span data-stu-id="48d78-144">You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations.</span></span> <span data-ttu-id="48d78-145">对于出货工作，使用具有个可用库存状态的物料。</span><span class="sxs-lookup"><span data-stu-id="48d78-145">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="48d78-146">如果物料具有**中断**状态，并且主计划在这些物料上运行，则将物料视为缺失，库存会自动补货。</span><span class="sxs-lookup"><span data-stu-id="48d78-146">If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.</span></span>



<a name="see-also"></a><span data-ttu-id="48d78-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="48d78-147">See also</span></span>
--------

[<span data-ttu-id="48d78-148">创建和维护库存锁定（任务指南）</span><span class="sxs-lookup"><span data-stu-id="48d78-148">Create and maintain an inventory blocking (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-maintain-inventory-blocking)

[<span data-ttu-id="48d78-149">质量管理流程</span><span class="sxs-lookup"><span data-stu-id="48d78-149">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="48d78-150">检查货物的质量（任务指南）</span><span class="sxs-lookup"><span data-stu-id="48d78-150">Inspect the quality of goods (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/inspect-quality-goods)
