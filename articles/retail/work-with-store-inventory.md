---
title: "管理商店库存"
description: "本文描述可用于管理库存的文档类型。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 031a2f9c27bb6223dc65c3ae6b3d4e3ce775ae21
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="manage-store-inventory"></a><span data-ttu-id="9d9f8-103">管理商店库存</span><span class="sxs-lookup"><span data-stu-id="9d9f8-103">Manage store inventory</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d9f8-104">本文描述可用于管理库存的文档类型。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="9d9f8-105">您可以使用以下文档的类型管理您的组织的库存。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="9d9f8-106">采购订单</span><span class="sxs-lookup"><span data-stu-id="9d9f8-106">Purchase orders</span></span>
<span data-ttu-id="9d9f8-107">采购订单在总部创建。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="9d9f8-108">如果零售仓库包括在采购订单头中，通过使用 Microsoft Dynamics 365 for Retail 中的 Modern POS (MPOS) 或 Cloud POS 订货可以在商店接收。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9d9f8-109">在商店输入已接收数量后，可以保存本地以供附加修改。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9d9f8-110">或者，数量可承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9d9f8-111">在总部，在商店接收的数量将显示在 Dynamics 365 for Retail 中的采购订单的**当前接收量**字段中。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="9d9f8-112">转移单</span><span class="sxs-lookup"><span data-stu-id="9d9f8-112">Transfer orders</span></span>
<span data-ttu-id="9d9f8-113">转移单可指定特定商店为可用于装运物料的位置。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="9d9f8-114">在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 内的拣货请求。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9d9f8-115">在请求的领料数量后，它们承诺和发送总部。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="9d9f8-116">在总部，在商店领取的数量将显示在 Dynamics 365 for Retail 中的转移单的**当前装运量**字段中。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="9d9f8-117">转移单可以指定该物料可以装运到的位置的特定商店。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="9d9f8-118">在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 中的接收请求。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9d9f8-119">在商店输入已接收数量后，可以保存本地以供附加修改。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9d9f8-120">或者，数量可承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9d9f8-121">在总部，在商店接收的数量将显示在 Dynamics 365 for Retail 中的转移单的**当前接收量**字段中。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="9d9f8-122">存货盘点</span><span class="sxs-lookup"><span data-stu-id="9d9f8-122">Stock counts</span></span>
<span data-ttu-id="9d9f8-123">存货盘点可以是计划或不定期的。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="9d9f8-124">存货盘点在总部启动，总部指定必须盘点的物料。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="9d9f8-125">总部会创建盘点文档，并将商店接收，将实际的现有存货数量输入 MPOS 或 Cloud POS.。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="9d9f8-126">计划外存货盘点在商店启动，在 MPOS 或 Cloud POS. 中更新实际的现有存货数量。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="9d9f8-127">与周期盘点不同，计划外存货盘点没有物料的预定义列表。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="9d9f8-128">在存货盘点类型为已完工入库时，它承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="9d9f8-129">在总部，将验证和过帐盘点。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="9d9f8-130">库存查找</span><span class="sxs-lookup"><span data-stu-id="9d9f8-130">Inventory lookup</span></span>
<span data-ttu-id="9d9f8-131">在库存查找页可以查看多个商店和仓库的当前现有产品数量。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="9d9f8-132">除了当前现有数量以外，还可以查看各个商店的未来可承诺 (ATP) 数量。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="9d9f8-133">为此，选择你要查看 ATP 的商店，然后单击**查看商店可用性**。</span><span class="sxs-lookup"><span data-stu-id="9d9f8-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





