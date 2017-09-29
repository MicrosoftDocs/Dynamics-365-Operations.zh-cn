---
title: "实际和财务更新"
description: "本主题提供哪些类型的交易记录将增减库存数量的概要。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 07ed503b7c441cb594e8e96ddcd9a81c0745a963
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="54cda-103">实际和财务更新</span><span class="sxs-lookup"><span data-stu-id="54cda-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="54cda-104">本主题提供哪些类型的交易记录将增减库存数量的概要。</span><span class="sxs-lookup"><span data-stu-id="54cda-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="54cda-105">库存交易记录可以在 Microsoft Dynamics 365 for Finance and Operations 中完成实际更新和财务更新。</span><span class="sxs-lookup"><span data-stu-id="54cda-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="54cda-106">某些实际交易记录和财务交易记录类型会增加库存数量，而其他则会减少数量。</span><span class="sxs-lookup"><span data-stu-id="54cda-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="54cda-107">实际增加</span><span class="sxs-lookup"><span data-stu-id="54cda-107">Physical increases</span></span>
<span data-ttu-id="54cda-108">在过帐某一实际交易记录时，该交易记录的状态为**已接收**。</span><span class="sxs-lookup"><span data-stu-id="54cda-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="54cda-109">以下交易记录被视为实际增加：</span><span class="sxs-lookup"><span data-stu-id="54cda-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="54cda-110">采购订单收货</span><span class="sxs-lookup"><span data-stu-id="54cda-110">Purchase order receipt</span></span>
-   <span data-ttu-id="54cda-111">销售订单装箱单返回</span><span class="sxs-lookup"><span data-stu-id="54cda-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="54cda-112">将生产订单报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="54cda-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="54cda-113">生产订单领料单上的副产品</span><span class="sxs-lookup"><span data-stu-id="54cda-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="54cda-114">财务增加</span><span class="sxs-lookup"><span data-stu-id="54cda-114">Financial increases</span></span>
<span data-ttu-id="54cda-115">在过帐某一财务收货交易记录时，增加数量的交易记录的状态为**已采购**。</span><span class="sxs-lookup"><span data-stu-id="54cda-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="54cda-116">以下交易记录被视为财务增加：</span><span class="sxs-lookup"><span data-stu-id="54cda-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="54cda-117">供应商发票</span><span class="sxs-lookup"><span data-stu-id="54cda-117">Vendor invoice</span></span>
-   <span data-ttu-id="54cda-118">用于退货的销售订单发票</span><span class="sxs-lookup"><span data-stu-id="54cda-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="54cda-119">生产订单成本计算</span><span class="sxs-lookup"><span data-stu-id="54cda-119">Production order costing</span></span>
-   <span data-ttu-id="54cda-120">正数量库存日记帐，例如移动、损益、盘点、物料清单和转移</span><span class="sxs-lookup"><span data-stu-id="54cda-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="54cda-121">增加数量的交易记录</span><span class="sxs-lookup"><span data-stu-id="54cda-121">Transactions that increase quantity</span></span>
<span data-ttu-id="54cda-122">以移动平均成本价过帐增加数量的交易记录。</span><span class="sxs-lookup"><span data-stu-id="54cda-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="54cda-123">Finance and Operations 计算移动平均成本价（基于每个财务跟踪的库存维度的上述各交易记录的成本）。</span><span class="sxs-lookup"><span data-stu-id="54cda-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="54cda-124">有关移动平均成本价的信息，请参阅[移动平均成本价](running-average-cost-price.md)。</span><span class="sxs-lookup"><span data-stu-id="54cda-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="54cda-125">减少数量的交易记录</span><span class="sxs-lookup"><span data-stu-id="54cda-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="54cda-126">过帐减少数量的交易记录时，Finance and Operations 使用计算出的移动平均成本价，而不考虑与该库存关联的库存模型。</span><span class="sxs-lookup"><span data-stu-id="54cda-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="54cda-127">减少数量的交易记录不得在另一个交易记录过帐前标记为该交易记录。</span><span class="sxs-lookup"><span data-stu-id="54cda-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="54cda-128">如果实际现有库存量变为负值，Finance and Operations 使用为**物料**页上的物料定义的库存成本。</span><span class="sxs-lookup"><span data-stu-id="54cda-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="54cda-129">**注意：**如果启用多站点功能，则该成本将改为在**默认订单设置**页上定义的库存成本。</span><span class="sxs-lookup"><span data-stu-id="54cda-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="54cda-130">实际发货与财务发货</span><span class="sxs-lookup"><span data-stu-id="54cda-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="54cda-131">在过帐某一实际发货交易记录时，该交易记录的状态为**已减少**。</span><span class="sxs-lookup"><span data-stu-id="54cda-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="54cda-132">以下交易记录被视为实际发货：</span><span class="sxs-lookup"><span data-stu-id="54cda-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="54cda-133">生产订单领料单日志</span><span class="sxs-lookup"><span data-stu-id="54cda-133">Production order picking list journal</span></span>
-   <span data-ttu-id="54cda-134">销售订单装箱单</span><span class="sxs-lookup"><span data-stu-id="54cda-134">Sales order packing slip</span></span>
-   <span data-ttu-id="54cda-135">采购订单装箱单退货</span><span class="sxs-lookup"><span data-stu-id="54cda-135">Purchase order packing slip return</span></span>

<span data-ttu-id="54cda-136">在过帐某一财务交易记录时，该交易记录的状态为**已销售**。</span><span class="sxs-lookup"><span data-stu-id="54cda-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="54cda-137">以下交易记录被视为财务发货：</span><span class="sxs-lookup"><span data-stu-id="54cda-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="54cda-138">结束生产订单</span><span class="sxs-lookup"><span data-stu-id="54cda-138">Ending a production order</span></span>
-   <span data-ttu-id="54cda-139">销售订单发票</span><span class="sxs-lookup"><span data-stu-id="54cda-139">Sales order invoice</span></span>
-   <span data-ttu-id="54cda-140">供应商发票退货</span><span class="sxs-lookup"><span data-stu-id="54cda-140">Vendor invoice return</span></span>
-   <span data-ttu-id="54cda-141">负数量库存日记帐，例如移动、损益、盘点、物料清单和转移</span><span class="sxs-lookup"><span data-stu-id="54cda-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="54cda-142">以移动平均成本价过帐减少数量的交易记录。</span><span class="sxs-lookup"><span data-stu-id="54cda-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="54cda-143">因此，需要库存结转过程以将发货交易记录结算到基于分配给每个物料的库存模型的收货交易记录。</span><span class="sxs-lookup"><span data-stu-id="54cda-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




