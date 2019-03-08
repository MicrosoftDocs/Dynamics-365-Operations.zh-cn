---
title: 检验单
description: 本主题介绍检验单如何用于锁定库存。
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "362571"
---
# <a name="quarantine-orders"></a><span data-ttu-id="43d5a-103">检验单</span><span class="sxs-lookup"><span data-stu-id="43d5a-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43d5a-104">本主题介绍检验单如何用于锁定库存。</span><span class="sxs-lookup"><span data-stu-id="43d5a-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="43d5a-105">检验单可用于锁定库存。</span><span class="sxs-lookup"><span data-stu-id="43d5a-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="43d5a-106">例如，您可能要检验质量控制原因的物料。</span><span class="sxs-lookup"><span data-stu-id="43d5a-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="43d5a-107">将把已检验的库存转移到检验仓库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="43d5a-108">**注意：** 如果您使用高级仓库管理流程（在仓库管理中），仅为退货销售订单使用检验单。</span><span class="sxs-lookup"><span data-stu-id="43d5a-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="43d5a-109">检验现有库存物料</span><span class="sxs-lookup"><span data-stu-id="43d5a-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="43d5a-110">在检验物料时，您可以手动创建检验单或设置该系统以在收货处理期间自动创建检验单。</span><span class="sxs-lookup"><span data-stu-id="43d5a-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="43d5a-111">若要自动创建检验单，请在**物料模型组**页的**库存策略**选项卡上选择**检验管理**选项。</span><span class="sxs-lookup"><span data-stu-id="43d5a-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="43d5a-112">您还必须在**检验仓库**字段中为接收仓库指定默认检验仓库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="43d5a-113">当实际现有库存量在采购订单或生产订单中记录时，检验物料会自动移至 Microsoft Dynamics 365 for Finance and Operations 中的检验仓库中。</span><span class="sxs-lookup"><span data-stu-id="43d5a-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="43d5a-114">因为检验单的状态改为**已开始**，所以发生此移动。</span><span class="sxs-lookup"><span data-stu-id="43d5a-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="43d5a-115">当您手动创建检验单时，则不必需在相关的物料模型组中为检验管理设置物料。</span><span class="sxs-lookup"><span data-stu-id="43d5a-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="43d5a-116">对于此流程，必须指定应检验的现有库存量和应使用的检验仓库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="43d5a-117">您可以使用检验单状态来帮助计划流程。</span><span class="sxs-lookup"><span data-stu-id="43d5a-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="43d5a-118">检验单状态</span><span class="sxs-lookup"><span data-stu-id="43d5a-118">Quarantine order statuses</span></span>
<span data-ttu-id="43d5a-119">检验单可以有下列状态：</span><span class="sxs-lookup"><span data-stu-id="43d5a-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="43d5a-120">已创建</span><span class="sxs-lookup"><span data-stu-id="43d5a-120">Created</span></span>
-   <span data-ttu-id="43d5a-121">已开始</span><span class="sxs-lookup"><span data-stu-id="43d5a-121">Started</span></span>
-   <span data-ttu-id="43d5a-122">完工入库</span><span class="sxs-lookup"><span data-stu-id="43d5a-122">Reported as finished</span></span>
-   <span data-ttu-id="43d5a-123">已结束</span><span class="sxs-lookup"><span data-stu-id="43d5a-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="43d5a-124">创建时间</span><span class="sxs-lookup"><span data-stu-id="43d5a-124">Created</span></span>

<span data-ttu-id="43d5a-125">如果检验单已手动创建，但物料不在检验仓库中，则检验单具有**已创建**状态。</span><span class="sxs-lookup"><span data-stu-id="43d5a-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="43d5a-126">生成两个库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="43d5a-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="43d5a-127">一个交易记录是可具有**在单**、**实际预留**或**已领料**状态的发货交易记录。</span><span class="sxs-lookup"><span data-stu-id="43d5a-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="43d5a-128">另一个交易记录是可在检验仓库中具有**已订购**或**已登记**状态的收货交易记录。</span><span class="sxs-lookup"><span data-stu-id="43d5a-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="43d5a-129">可使用一般流程预留、领取和登记库存更新。</span><span class="sxs-lookup"><span data-stu-id="43d5a-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="43d5a-130">已开始</span><span class="sxs-lookup"><span data-stu-id="43d5a-130">Started</span></span>

<span data-ttu-id="43d5a-131">当检验单已具有**已开始**状态时，库存将从常规仓库转移到检验仓库，并且会生成两个库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="43d5a-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="43d5a-132">一个交易记录具有**已扣除**状态，另一个交易记录具有**已接收**状态。</span><span class="sxs-lookup"><span data-stu-id="43d5a-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="43d5a-133">同时，创建两个库存交易记录以处理退货转移。</span><span class="sxs-lookup"><span data-stu-id="43d5a-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="43d5a-134">这些交易记录未到期。</span><span class="sxs-lookup"><span data-stu-id="43d5a-134">These transactions aren't dated.</span></span> <span data-ttu-id="43d5a-135">一个交易记录具有**实际预留**状态，另一个交易记录具有**已订购**状态。</span><span class="sxs-lookup"><span data-stu-id="43d5a-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="43d5a-136">完工入库</span><span class="sxs-lookup"><span data-stu-id="43d5a-136">Reported as finished</span></span>

<span data-ttu-id="43d5a-137">通过单击**完工入库**，您可以将已开始的检验单报告为完工入库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="43d5a-138">物料从检验仓库中取出，但尚未移回常规仓库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="43d5a-139">移回常规仓库可以通过可在完工入库流程中初始化的物料到达日记帐进行处理。</span><span class="sxs-lookup"><span data-stu-id="43d5a-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="43d5a-140">已结束</span><span class="sxs-lookup"><span data-stu-id="43d5a-140">Ended</span></span>

<span data-ttu-id="43d5a-141">当检验单结束后，物料将从检验仓库移回常规仓库。</span><span class="sxs-lookup"><span data-stu-id="43d5a-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="43d5a-142">物料交易记录的状态在检验仓库中设置为**已售出**，在常规仓库中设置为**已采购**。</span><span class="sxs-lookup"><span data-stu-id="43d5a-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="43d5a-143">检验单报废</span><span class="sxs-lookup"><span data-stu-id="43d5a-143">Quarantine order scrap</span></span>
<span data-ttu-id="43d5a-144">作为检验单流程的一部分，可以报废库存。</span><span class="sxs-lookup"><span data-stu-id="43d5a-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="43d5a-145">当处理报废时，库存状态将按检验仓库中的发货交易记录设置为**售出**。</span><span class="sxs-lookup"><span data-stu-id="43d5a-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="43d5a-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="43d5a-146">Additional resources</span></span>
--------

[<span data-ttu-id="43d5a-147">库存锁定</span><span class="sxs-lookup"><span data-stu-id="43d5a-147">Inventory blocking</span></span>](inventory-blocking.md)
