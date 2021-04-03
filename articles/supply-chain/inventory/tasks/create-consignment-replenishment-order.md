---
title: 创建托运补货订单
description: 此主题介绍如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。
author: RichardLuan
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09b6b69d72d0a5f429dbd8cba6faefd4b1a057e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264866"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="48c73-103">创建托运补货订单</span><span class="sxs-lookup"><span data-stu-id="48c73-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48c73-104">此主题介绍如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。</span><span class="sxs-lookup"><span data-stu-id="48c73-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="48c73-105">还显示如何记录物料收据，以便将托运库存登记为供应商拥有的现有库存。</span><span class="sxs-lookup"><span data-stu-id="48c73-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="48c73-106">此过程通常由采购专员完成。</span><span class="sxs-lookup"><span data-stu-id="48c73-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="48c73-107">您可以使用演示数据公司 USMF 运行此指南。</span><span class="sxs-lookup"><span data-stu-id="48c73-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="48c73-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="48c73-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="48c73-109">创建托运补货订单</span><span class="sxs-lookup"><span data-stu-id="48c73-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="48c73-110">在导航窗格中，转到 **模块 > 采购 > 托运 > 托运补货订单**。</span><span class="sxs-lookup"><span data-stu-id="48c73-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="48c73-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48c73-111">Select **New**.</span></span>
3. <span data-ttu-id="48c73-112">在 **供应商帐户** 字段中，选择供应商 **US-104**（必须选择在 **库存所有者** 页中注册为所有者的供应商）。</span><span class="sxs-lookup"><span data-stu-id="48c73-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="48c73-113">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="48c73-113">Select **OK**.</span></span>
5. <span data-ttu-id="48c73-114">选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="48c73-114">Select **Add line**.</span></span>
6. <span data-ttu-id="48c73-115">在 **物料编号** 字段中，键入 `M9211CI`（必须选择为托运库存设置的物料）。</span><span class="sxs-lookup"><span data-stu-id="48c73-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="48c73-116">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="48c73-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="48c73-117">在 **请求交付日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="48c73-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="48c73-118">请求日期和确认日期由 MRP 引擎用于货物的预期到达。</span><span class="sxs-lookup"><span data-stu-id="48c73-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="48c73-119">在 **确认交货日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="48c73-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="48c73-120">展开 **行详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="48c73-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="48c73-121">选择 **库存维度** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="48c73-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="48c73-122">若要在 **库存维度负责人** 字段中显示负责人，请刷新页面。</span><span class="sxs-lookup"><span data-stu-id="48c73-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="48c73-123">供应商 US-104 现在作为所有者列出。</span><span class="sxs-lookup"><span data-stu-id="48c73-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="48c73-124">检查库存交易记录状态。</span><span class="sxs-lookup"><span data-stu-id="48c73-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="48c73-125">选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="48c73-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="48c73-126">选择 **交易记录**。</span><span class="sxs-lookup"><span data-stu-id="48c73-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="48c73-127">请注意，**收货** 字段设置为 **已订购**。</span><span class="sxs-lookup"><span data-stu-id="48c73-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="48c73-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="48c73-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="48c73-129">接收多个物料</span><span class="sxs-lookup"><span data-stu-id="48c73-129">Receive items</span></span>
1. <span data-ttu-id="48c73-130">选择 **物料收货**。</span><span class="sxs-lookup"><span data-stu-id="48c73-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="48c73-131">在 **外部物料收据** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="48c73-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="48c73-132">在 **数量** 字段中，输入一个比此处显示的数字更小的数字。</span><span class="sxs-lookup"><span data-stu-id="48c73-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="48c73-133">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="48c73-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="48c73-134">检查现有库存量</span><span class="sxs-lookup"><span data-stu-id="48c73-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="48c73-135">选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="48c73-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="48c73-136">选择 **现有**。</span><span class="sxs-lookup"><span data-stu-id="48c73-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="48c73-137">选择 **概览**。</span><span class="sxs-lookup"><span data-stu-id="48c73-137">Select **Overview**.</span></span> <span data-ttu-id="48c73-138">已作为供应商拥有的托运库存接收的物料现有可用。</span><span class="sxs-lookup"><span data-stu-id="48c73-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="48c73-139">托运补货订单的剩余数量在 **订购总数** 字段中显示。</span><span class="sxs-lookup"><span data-stu-id="48c73-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="48c73-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="48c73-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]