---
title: 商店库存管理
description: 本主题描述可用于管理库存的文档类型。
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "339226"
---
# <a name="store-inventory-management"></a><span data-ttu-id="d65ee-103">商店库存管理</span><span class="sxs-lookup"><span data-stu-id="d65ee-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d65ee-104">本主题描述可用于管理库存的文档类型。</span><span class="sxs-lookup"><span data-stu-id="d65ee-104">This topic describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="d65ee-105">您可以使用以下文档的类型管理您的组织的库存。</span><span class="sxs-lookup"><span data-stu-id="d65ee-105">You can use the following types of documents to manage your organization's inventory.</span></span>

<span data-ttu-id="d65ee-106">在 Dynamics 365 for Retail 中处理库存和使用 POS 应用程序时，请务必记住 POS 为库存维度和某些库存物料类型提供有限支持。</span><span class="sxs-lookup"><span data-stu-id="d65ee-106">When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</span></span>  

<span data-ttu-id="d65ee-107">POS 解决方案不支持以下物料配置：</span><span class="sxs-lookup"><span data-stu-id="d65ee-107">The POS solution does not support the following item configurations:</span></span>
- <span data-ttu-id="d65ee-108">物料清单物料（除套件产品外，其使用物料清单框架的某些组件）</span><span class="sxs-lookup"><span data-stu-id="d65ee-108">BOM items (except kit products, which utilize some components of the BOM framework)</span></span>
- <span data-ttu-id="d65ee-109">实际称重物料</span><span class="sxs-lookup"><span data-stu-id="d65ee-109">Catch weight items</span></span>
- <span data-ttu-id="d65ee-110">批次控制物料</span><span class="sxs-lookup"><span data-stu-id="d65ee-110">Batch-controlled items</span></span>

<span data-ttu-id="d65ee-111">POS 应用程序当前在 POS 中不支持以下跟踪维度：</span><span class="sxs-lookup"><span data-stu-id="d65ee-111">The POS application currently does not support the following tracking dimensions in the POS:</span></span>
- <span data-ttu-id="d65ee-112">批次跟踪维度</span><span class="sxs-lookup"><span data-stu-id="d65ee-112">Batch tracking dimension</span></span>
- <span data-ttu-id="d65ee-113">所有者维度</span><span class="sxs-lookup"><span data-stu-id="d65ee-113">Owner dimension</span></span>

<span data-ttu-id="d65ee-114">POS 解决方案为以下维度提供有限支持。</span><span class="sxs-lookup"><span data-stu-id="d65ee-114">The POS solution provides limited support for the following dimensions.</span></span> <span data-ttu-id="d65ee-115">有限支持指示 POS 可以根据仓库/商店设置配置将其中的一些维度自动默认为库存交易记录中的维度。</span><span class="sxs-lookup"><span data-stu-id="d65ee-115">Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</span></span> <span data-ttu-id="d65ee-116">如果销售交易记录手动输入到 ERP，POS 将不以维度支持方式完全支持这些维度。</span><span class="sxs-lookup"><span data-stu-id="d65ee-116">POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</span></span> 

- <span data-ttu-id="d65ee-117">库位</span><span class="sxs-lookup"><span data-stu-id="d65ee-117">Location</span></span>
- <span data-ttu-id="d65ee-118">牌照（仅当在物料和商店仓库上启用了 **Uuse 仓库管理流程**时适用）</span><span class="sxs-lookup"><span data-stu-id="d65ee-118">License plate (only applicable when **Uuse warehouse management process** has been enabled on the item and the store warehouse)</span></span>
- <span data-ttu-id="d65ee-119">序列号</span><span class="sxs-lookup"><span data-stu-id="d65ee-119">Serial number</span></span>
- <span data-ttu-id="d65ee-120">库存状态</span><span class="sxs-lookup"><span data-stu-id="d65ee-120">Inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="d65ee-121">所有组织均必须在将配置部署到生产前在开发或测试环境中通过 POS 测试物料配置。</span><span class="sxs-lookup"><span data-stu-id="d65ee-121">All organizations must test item configurations through POS in development or test environments before deploying them to production.</span></span> <span data-ttu-id="d65ee-122">通过您的物料的 POS 通过执行常规的付现自运的销售交易并创建客户订单来测试您的物料（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d65ee-122">Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</span></span> <span data-ttu-id="d65ee-123">测试必须包括在测试环境中运行完整的对帐单过帐流程并确认没有问题。</span><span class="sxs-lookup"><span data-stu-id="d65ee-123">Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</span></span>
> <span data-ttu-id="d65ee-124">按 POS 应用程序不支持的方式配置物料，且不进行适当的测试，可能导致对帐单过帐流程在生产中失败，且没有更正问题的简便方法。</span><span class="sxs-lookup"><span data-stu-id="d65ee-124">Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</span></span> <span data-ttu-id="d65ee-125">可以有选择地考虑对应用程序进行合作伙伴或客户自定义以允许这些过帐流程成功完成。</span><span class="sxs-lookup"><span data-stu-id="d65ee-125">Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</span></span> <span data-ttu-id="d65ee-126">如果不需要自定义，组织必须确保您的产品的产品配置已经以标准 POS 应用程序/订单创建/对帐单过帐流程支持的方式完成。</span><span class="sxs-lookup"><span data-stu-id="d65ee-126">If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="d65ee-127">采购订单</span><span class="sxs-lookup"><span data-stu-id="d65ee-127">Purchase orders</span></span>

<span data-ttu-id="d65ee-128">采购订单在总部创建。</span><span class="sxs-lookup"><span data-stu-id="d65ee-128">Purchase orders are created at the head office.</span></span> <span data-ttu-id="d65ee-129">如果零售仓库包括在采购订单头中，通过使用 Microsoft Dynamics 365 for Retail 中的 Modern POS (MPOS) 或 Cloud POS 订货可以在商店接收。</span><span class="sxs-lookup"><span data-stu-id="d65ee-129">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d65ee-130">在商店输入已接收数量后，可以保存本地以供附加修改。</span><span class="sxs-lookup"><span data-stu-id="d65ee-130">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="d65ee-131">或者，数量可承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="d65ee-131">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="d65ee-132">在总部，在商店接收的数量将在 Dynamics 365 for Retail 中在采购订单的**当前接收量**字段中显示。</span><span class="sxs-lookup"><span data-stu-id="d65ee-132">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="d65ee-133">转移单</span><span class="sxs-lookup"><span data-stu-id="d65ee-133">Transfer orders</span></span>

<span data-ttu-id="d65ee-134">转移单可指定特定商店为可用于装运物料的位置。</span><span class="sxs-lookup"><span data-stu-id="d65ee-134">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="d65ee-135">在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 内的拣货请求。</span><span class="sxs-lookup"><span data-stu-id="d65ee-135">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="d65ee-136">在请求的领料数量后，它们承诺和发送总部。</span><span class="sxs-lookup"><span data-stu-id="d65ee-136">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="d65ee-137">在总部，在商店已领料的数量将在 Dynamics 365 for Retail 中在转移单上的**当前装运量**字段中显示。</span><span class="sxs-lookup"><span data-stu-id="d65ee-137">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="d65ee-138">转移单可以指定该物料可以装运到的位置的特定商店。</span><span class="sxs-lookup"><span data-stu-id="d65ee-138">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="d65ee-139">在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 中的接收请求。</span><span class="sxs-lookup"><span data-stu-id="d65ee-139">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="d65ee-140">在商店输入已接收数量后，可以保存本地以供附加修改。</span><span class="sxs-lookup"><span data-stu-id="d65ee-140">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="d65ee-141">或者，数量可承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="d65ee-141">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="d65ee-142">在总部，在商店接收的数量将在 Dynamics 365 for Retail 中在转移单的**当前接收量**字段中显示。</span><span class="sxs-lookup"><span data-stu-id="d65ee-142">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="d65ee-143">存货盘点</span><span class="sxs-lookup"><span data-stu-id="d65ee-143">Stock counts</span></span>

<span data-ttu-id="d65ee-144">存货盘点可以是计划或不定期的。</span><span class="sxs-lookup"><span data-stu-id="d65ee-144">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="d65ee-145">存货盘点在总部启动，总部指定必须盘点的物料。</span><span class="sxs-lookup"><span data-stu-id="d65ee-145">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="d65ee-146">总部会创建盘点文档，并将商店接收，将实际的现有存货数量输入 MPOS 或 Cloud POS.。</span><span class="sxs-lookup"><span data-stu-id="d65ee-146">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="d65ee-147">计划外存货盘点在商店启动，在 MPOS 或 Cloud POS. 中更新实际的现有存货数量。</span><span class="sxs-lookup"><span data-stu-id="d65ee-147">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="d65ee-148">与周期盘点不同，计划外存货盘点没有物料的预定义列表。</span><span class="sxs-lookup"><span data-stu-id="d65ee-148">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="d65ee-149">在存货盘点类型为已完工入库时，它承诺和发送给总部。</span><span class="sxs-lookup"><span data-stu-id="d65ee-149">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="d65ee-150">在总部，将验证和过帐盘点。</span><span class="sxs-lookup"><span data-stu-id="d65ee-150">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="d65ee-151">库存查找</span><span class="sxs-lookup"><span data-stu-id="d65ee-151">Inventory lookup</span></span>

<span data-ttu-id="d65ee-152">在库存查找页可以查看多个商店和仓库的当前现有产品数量。</span><span class="sxs-lookup"><span data-stu-id="d65ee-152">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="d65ee-153">除了当前现有数量以外，还可以查看各个商店的未来可承诺 (ATP) 数量。</span><span class="sxs-lookup"><span data-stu-id="d65ee-153">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="d65ee-154">为此，选择你要查看 ATP 的商店，然后单击**查看商店可用性**。</span><span class="sxs-lookup"><span data-stu-id="d65ee-154">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>
