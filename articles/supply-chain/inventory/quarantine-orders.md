---
title: 检验单
description: 本主题介绍如何使用隔离订单锁定库存。
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956174"
---
# <a name="quarantine-orders"></a><span data-ttu-id="6b9fc-103">检验单</span><span class="sxs-lookup"><span data-stu-id="6b9fc-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b9fc-104">本主题介绍如何使用隔离订单锁定库存。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="6b9fc-105">隔离订单可让您锁定库存。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="6b9fc-106">例如，您可能要检验质量控制原因的物料。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="6b9fc-107">将把已检验的库存转移到检验仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="6b9fc-108">如果您使用高级仓库管理流程（在仓库管理中），隔离订单处理仅用于退货销售订单。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="6b9fc-109">检验现有库存物料</span><span class="sxs-lookup"><span data-stu-id="6b9fc-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="6b9fc-110">隔离物料时，可以手动创建隔离订单，也可以将系统设置为在入站处理期间自动创建订单。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="6b9fc-111">要将系统设置为自动生成隔离订单，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="6b9fc-112">转到 **库存管理 \> 设置 \> 库存 \> 物料模型组**。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="6b9fc-113">在列表窗格中选择一个相关模型组，或创建一个新模型组。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="6b9fc-114">在 **库存策略** 快速选项卡上，选中 **隔离管理** 复选框。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="6b9fc-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-115">Close the page.</span></span>
1. <span data-ttu-id="6b9fc-116">在接收仓库的 **隔离仓库** 字段中，指定默认隔离仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="6b9fc-117">当在仓库登记为已接收的物料属于已选中 **隔离管理** 复选框的模型组时，系统将为其生成隔离订单。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="6b9fc-118">隔离订单指示工作人员将物料移至隔离仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="6b9fc-119">当您在 **隔离订单** 页上手动创建隔离订单时，不必在关联的物料模型组中对物料进行隔离管理设置。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="6b9fc-120">对于此流程，必须指定应检验的现有库存量和应使用的检验仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="6b9fc-121">您可以使用检验单状态来帮助计划流程。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="6b9fc-122">检验单状态</span><span class="sxs-lookup"><span data-stu-id="6b9fc-122">Quarantine order statuses</span></span>

<span data-ttu-id="6b9fc-123">检验单可以有下列状态：</span><span class="sxs-lookup"><span data-stu-id="6b9fc-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="6b9fc-124">已创建</span><span class="sxs-lookup"><span data-stu-id="6b9fc-124">Created</span></span>
- <span data-ttu-id="6b9fc-125">已开始</span><span class="sxs-lookup"><span data-stu-id="6b9fc-125">Started</span></span>
- <span data-ttu-id="6b9fc-126">完工入库</span><span class="sxs-lookup"><span data-stu-id="6b9fc-126">Reported as finished</span></span>
- <span data-ttu-id="6b9fc-127">已结束</span><span class="sxs-lookup"><span data-stu-id="6b9fc-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="6b9fc-128">创建时间</span><span class="sxs-lookup"><span data-stu-id="6b9fc-128">Created</span></span>

<span data-ttu-id="6b9fc-129">如果检验单已手动创建，但物料不在检验仓库中，则检验单具有 **已创建** 状态。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="6b9fc-130">生成两个库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="6b9fc-131">一个交易记录是可具有 **在单**、**实际预留** 或 **已领料** 状态的发货交易记录。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="6b9fc-132">另一个交易记录是可在检验仓库中具有 **已订购** 或 **已登记** 状态的收货交易记录。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="6b9fc-133">可使用一般流程预留、领取和登记库存更新。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="6b9fc-134">已开始</span><span class="sxs-lookup"><span data-stu-id="6b9fc-134">Started</span></span>

<span data-ttu-id="6b9fc-135">当检验单已具有 **已开始** 状态时，库存将从常规仓库转移到检验仓库，并且会生成两个库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="6b9fc-136">一个交易记录具有 **已扣除** 状态，另一个交易记录具有 **已接收** 状态。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="6b9fc-137">同时，创建两个库存交易记录以处理退货转移。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="6b9fc-138">这些交易记录未到期。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-138">These transactions aren't dated.</span></span> <span data-ttu-id="6b9fc-139">一个交易记录具有 **实际预留** 状态，另一个交易记录具有 **已订购** 状态。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="6b9fc-140">完工入库</span><span class="sxs-lookup"><span data-stu-id="6b9fc-140">Reported as finished</span></span>

<span data-ttu-id="6b9fc-141">要将开始的隔离订单报告为完工入库，打开该订单，然后在操作窗格上选择 **完工入库**。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="6b9fc-142">物料将从隔离区释放，但尚未移回常规仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="6b9fc-143">移回常规仓库可以通过可在完工入库流程中初始化的物料到达日记帐进行处理。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="6b9fc-144">已结束</span><span class="sxs-lookup"><span data-stu-id="6b9fc-144">Ended</span></span>

<span data-ttu-id="6b9fc-145">当检验单结束后，物料将从检验仓库移回常规仓库。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="6b9fc-146">物料交易记录的状态在检验仓库中设置为 *已售出*，在常规仓库中设置为 *已采购*。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="6b9fc-147">检验单报废</span><span class="sxs-lookup"><span data-stu-id="6b9fc-147">Quarantine order scrap</span></span>

<span data-ttu-id="6b9fc-148">作为检验单流程的一部分，可以报废库存。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="6b9fc-149">当处理报废时，库存状态将按隔离仓库中的发货交易设置为 *已售出*。</span><span class="sxs-lookup"><span data-stu-id="6b9fc-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b9fc-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="6b9fc-150">Additional resources</span></span>

- [<span data-ttu-id="6b9fc-151">库存锁定</span><span class="sxs-lookup"><span data-stu-id="6b9fc-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
