---
title: 记录采购订单上的收货
description: 本主题介绍如何直接在采购订单中记录收货。
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cdf2b8624bf0319cd421ec11417695cfd4c78db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244079"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="bf35e-103">记录采购订单上的收货</span><span class="sxs-lookup"><span data-stu-id="bf35e-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf35e-104">本主题介绍如何直接在采购订单中记录收货。</span><span class="sxs-lookup"><span data-stu-id="bf35e-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="bf35e-105">还可以在仓库中登记产品收货，以后再记录到采购订单中。</span><span class="sxs-lookup"><span data-stu-id="bf35e-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="bf35e-106">此任务通常由代购代理或应付账款协调员执行。</span><span class="sxs-lookup"><span data-stu-id="bf35e-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="bf35e-107">可以在 USMF 演示数据公司中使用本指南中的示例。</span><span class="sxs-lookup"><span data-stu-id="bf35e-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="bf35e-108">此示例包括简单采购订单的创建步骤，以便您将此过程用作任务指南。</span><span class="sxs-lookup"><span data-stu-id="bf35e-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="bf35e-109">如果您使用此过程和您自己的数据，则可以从 **记录收货** 子任务着手。</span><span class="sxs-lookup"><span data-stu-id="bf35e-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="bf35e-110">为收货准备新采购订单</span><span class="sxs-lookup"><span data-stu-id="bf35e-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="bf35e-111">转到 **导航窗格 > 模块 > 采购 > 采购订单 > 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="bf35e-112">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-112">Select **New**.</span></span>
3. <span data-ttu-id="bf35e-113">在 **供应商帐户** 字段中输入 `US-101`。</span><span class="sxs-lookup"><span data-stu-id="bf35e-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="bf35e-114">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-114">Select **OK**.</span></span>
5. <span data-ttu-id="bf35e-115">在 **物料编号** 字段中输入 `M0001`。</span><span class="sxs-lookup"><span data-stu-id="bf35e-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="bf35e-116">在 **数量** 字段中，输入 `5`。</span><span class="sxs-lookup"><span data-stu-id="bf35e-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="bf35e-117">在操作窗格上，选择 **采购**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="bf35e-118">选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="bf35e-119">记录收货</span><span class="sxs-lookup"><span data-stu-id="bf35e-119">Record receipt of goods</span></span>
1. <span data-ttu-id="bf35e-120">在操作窗格上，选择 **接收**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="bf35e-121">选择 **物料收货**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-121">Select **Product receipt**.</span></span> <span data-ttu-id="bf35e-122">**数量** 字段用于为要接收的数量选择不同选项。</span><span class="sxs-lookup"><span data-stu-id="bf35e-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="bf35e-123">例如，如果某个数量以前在仓库中已登记，可以选择 **登记数量**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="bf35e-124">对于此示例，请使用 **订购数量** 的值。</span><span class="sxs-lookup"><span data-stu-id="bf35e-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="bf35e-125">展开 **概览** 部分。</span><span class="sxs-lookup"><span data-stu-id="bf35e-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="bf35e-126">在 **物料收货** 字段中键入任何值。</span><span class="sxs-lookup"><span data-stu-id="bf35e-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="bf35e-127">此字段用于输入将用作产品收货日记帐的凭证的参考。</span><span class="sxs-lookup"><span data-stu-id="bf35e-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="bf35e-128">展开 **行** 部分。</span><span class="sxs-lookup"><span data-stu-id="bf35e-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="bf35e-129">将 **数量** 设置为“4”。</span><span class="sxs-lookup"><span data-stu-id="bf35e-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="bf35e-130">您可以在此处手动指定订单中各行将收到的数量。</span><span class="sxs-lookup"><span data-stu-id="bf35e-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="bf35e-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bf35e-131">Select **OK**.</span></span> <span data-ttu-id="bf35e-132">此货物现已在采购订单中记录为已接收，并已创建了单据格式的产品收货日记帐以体现此信息。</span><span class="sxs-lookup"><span data-stu-id="bf35e-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="bf35e-133">可使用“产品收货”操作审查随采购订单创建的日记帐，以了解产品的收货内容和收货时间。</span><span class="sxs-lookup"><span data-stu-id="bf35e-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]