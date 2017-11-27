---
title: "库存状态"
description: "本文介绍如何使用库存状态来分类和跟踪库存。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5caa5620db428f18d451fdfe2aeae9e2a76a24f8
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-statuses"></a><span data-ttu-id="24ddf-103">库存状态</span><span class="sxs-lookup"><span data-stu-id="24ddf-103">Inventory statuses</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="24ddf-104">本文介绍如何使用库存状态来分类和跟踪库存。</span><span class="sxs-lookup"><span data-stu-id="24ddf-104">This article describes how you can use inventory statuses to categorize and keep track of inventory.</span></span>

<span data-ttu-id="24ddf-105">您可以使用库存状态对库存分类。</span><span class="sxs-lookup"><span data-stu-id="24ddf-105">You can use inventory statuses to categorize inventory.</span></span> <span data-ttu-id="24ddf-106">您然后可以开始相应的操作，例如补货或入库工作。</span><span class="sxs-lookup"><span data-stu-id="24ddf-106">You can then initiate appropriate actions, such as replenishment or put-away work.</span></span>

<span data-ttu-id="24ddf-107">这是您可以使用库存状态的方式的一些示例：</span><span class="sxs-lookup"><span data-stu-id="24ddf-107">Here are some examples of ways that you can use inventory statuses:</span></span>

-   <span data-ttu-id="24ddf-108">创建现有库存量、进货交易记录和出货交易记录的库存状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-108">Create inventory statuses for on-hand inventory, inbound transactions, and outbound transactions.</span></span>
-   <span data-ttu-id="24ddf-109">为仓库交易记录指定默认库存状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-109">Specify a default inventory status for warehouse transactions.</span></span>
-   <span data-ttu-id="24ddf-110">在物料到达前、到达时或在库存移动期间储存物料时，更改物料的库存状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-110">Change an inventory status for items before arrival, during arrival, or when the items are put away during inventory movement.</span></span>
-   <span data-ttu-id="24ddf-111">使用库存状态为退回的物料定价，并在主计划期间计划物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="24ddf-111">Use an inventory status to price items that are returned and to plan item coverage during master planning.</span></span>

<span data-ttu-id="24ddf-112">库存状态是存储维度组中的一个维度。</span><span class="sxs-lookup"><span data-stu-id="24ddf-112">An inventory status is one of the dimensions in the storage dimension group.</span></span> <span data-ttu-id="24ddf-113">库存状态可归类为可用或不可用，您可以使用**库存锁定**参数锁定具有不可用库存状态的物料。</span><span class="sxs-lookup"><span data-stu-id="24ddf-113">Inventory statuses can be categorized as available or unavailable, and you can use the **Inventory blocking** parameter to block items that have an unavailable inventory status.</span></span> <span data-ttu-id="24ddf-114">具有锁定状态的物料被视为实际库存，并且不能在生产订单、销售订单、转移定单或出货交易记录中使用。</span><span class="sxs-lookup"><span data-stu-id="24ddf-114">Items that have a blocked status are considered physical inventory, and they can't be used on a production order, sales order, transfer order, or outbound transaction.</span></span>

<span data-ttu-id="24ddf-115">您可以为进货工作使用具有可用或不可用库存状态的仓库物料。</span><span class="sxs-lookup"><span data-stu-id="24ddf-115">You can use warehouse items that have either available or unavailable inventory statuses for inbound work.</span></span> <span data-ttu-id="24ddf-116">例如，您创建名为**就绪**的可用状态，名为**已损坏**的不可用状态，和名为**已锁定**的锁定状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-116">For example, you create an available status that is named **Ready**, an unavailable status that is named **Damaged**, and a blocked status that is named **Blocked**.</span></span> <span data-ttu-id="24ddf-117">在您创建已接收或退回物料的采购订单时，如果任何物料已损坏或已中断，您可以在采购订单行上更改这些物料的库存状态为**已损坏**。</span><span class="sxs-lookup"><span data-stu-id="24ddf-117">When you create a purchase order for received or returned items, if any items are damaged or broken, you can change the inventory status of those items to **Damaged** on the purchase order line.</span></span> <span data-ttu-id="24ddf-118">在这些物料接收后，状态自动设置为**已锁定**。</span><span class="sxs-lookup"><span data-stu-id="24ddf-118">After these items are received, the status is automatically set to **Blocked**.</span></span> <span data-ttu-id="24ddf-119">如果您通过使用移动设备扫描已损坏的物料，Microsoft Dynamics 365 for Finance and Operations 可以使用库位指令和工作模板来显示有关您可以将这些物料入库的适当库位或库位范围的信息。</span><span class="sxs-lookup"><span data-stu-id="24ddf-119">If you scan the damaged items by using a mobile device, Microsoft Dynamics 365 for Finance and Operations can use location directives and work templates to show information about an appropriate location or range of locations where you can put away those items.</span></span> <span data-ttu-id="24ddf-120">对于退回的物料，在**库存交易记录**页中创建**预留**的发货类型。</span><span class="sxs-lookup"><span data-stu-id="24ddf-120">For returned items, an issue type of **Reservation** is created on the **Inventory transactions** page.</span></span>

<span data-ttu-id="24ddf-121">对于出货工作，使用具有个可用库存状态的物料。</span><span class="sxs-lookup"><span data-stu-id="24ddf-121">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="24ddf-122">如果您有处于**已中断**状态的物料，并且主计划运行这些物料，则将物料视为缺失，库存会自动补货。</span><span class="sxs-lookup"><span data-stu-id="24ddf-122">If you have items that have a status of **Broken**, and master planning is run on these items, the items are considered missing, and inventory is automatically replenished.</span></span>

<span data-ttu-id="24ddf-123">在设置库存状态后，您可以为站点、物料和仓库设置默认库存状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-123">After you set up inventory statuses, you can set the default inventory status for a site, item, and warehouse.</span></span> <span data-ttu-id="24ddf-124">您还可以设置销售、转移和采购订单的默认状态。</span><span class="sxs-lookup"><span data-stu-id="24ddf-124">You can also set a default status for sales, transfer, and purchase orders.</span></span> <span data-ttu-id="24ddf-125">销售订单和出货转移单的默认状态不能将**库存锁定**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="24ddf-125">The default status for sales orders and outbound transfer order can't have the **Inventory blocking** option set to **Yes**.</span></span> <span data-ttu-id="24ddf-126">从站点、仓库、物料、采购订单、转移单或销售订单的默认设置继承的库存状态可通过使用移动设备，或者在采购订单、销售订单或转移单行上更改。</span><span class="sxs-lookup"><span data-stu-id="24ddf-126">The inventory status that is inherited from the default settings on a site, warehouse, item, purchase order, transfer order or sales order can be changed by using the mobile device, or on the purchase order, sales order, or transfer order line.</span></span>

<span data-ttu-id="24ddf-127">若要计划具有可用库存状态的物料的覆盖范围，则在**存储维度组**页为存储维度选择**按维度的覆盖范围计划**选项。</span><span class="sxs-lookup"><span data-stu-id="24ddf-127">To plan coverage for items that have an available inventory status, select the **Coverage plan by dimension** option for a storage dimension on the **Storage dimension groups** page.</span></span> <span data-ttu-id="24ddf-128">当您打开**物料覆盖范围**向导时，具有可用状态的物料显示在**状态**页。</span><span class="sxs-lookup"><span data-stu-id="24ddf-128">When you open the **Item Coverage** wizard, items that have an available status appear on the **Status** page.</span></span> <span data-ttu-id="24ddf-129">若要创建这些物料的覆盖范围设置，请为可用库存状态选择库存状态 ID。</span><span class="sxs-lookup"><span data-stu-id="24ddf-129">To create coverage settings for these items, select the inventory status ID for the available inventory statuses.</span></span> <span data-ttu-id="24ddf-130">基于覆盖范围设置，在主计划期间您可以计算物料需求并预测可用物料的供应和需求。</span><span class="sxs-lookup"><span data-stu-id="24ddf-130">Based on the coverage settings, you can calculate the item requirements and forecast the supply and demand of available items during master planning.</span></span> <span data-ttu-id="24ddf-131">您无法创建具有锁定库存状态的物料覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="24ddf-131">You can't create an item coverage setup that has a blocked inventory status.</span></span> <span data-ttu-id="24ddf-132">或者，使用**物料覆盖范围**页来创建或修改物料覆盖范围参数。</span><span class="sxs-lookup"><span data-stu-id="24ddf-132">Alternatively, use the **Item coverage** page to create or modify the item coverage parameters.</span></span>

