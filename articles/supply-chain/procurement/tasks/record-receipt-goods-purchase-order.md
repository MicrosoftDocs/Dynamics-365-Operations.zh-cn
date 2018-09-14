--- 
title: "记录采购订单上的收货"
description: "此过程演示如何直接在采购订单中记录收货。"
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="50f46-103">记录采购订单上的收货</span><span class="sxs-lookup"><span data-stu-id="50f46-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50f46-104">此过程演示如何直接在采购订单中记录收货。</span><span class="sxs-lookup"><span data-stu-id="50f46-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="50f46-105">还可以在仓库中登记产品收货，以后再记录到采购订单中。</span><span class="sxs-lookup"><span data-stu-id="50f46-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="50f46-106">此任务通常由代购代理或应付账款协调员执行。</span><span class="sxs-lookup"><span data-stu-id="50f46-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="50f46-107">可以在 USMF 演示数据公司中使用本指南中的示例。</span><span class="sxs-lookup"><span data-stu-id="50f46-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="50f46-108">此示例包括简单采购订单的创建步骤，以便您将此过程用作任务指南。</span><span class="sxs-lookup"><span data-stu-id="50f46-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="50f46-109">如果您使用此过程和您自己的数据，则可以从“记录收货”子任务着手。</span><span class="sxs-lookup"><span data-stu-id="50f46-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="50f46-110">为收货准备新采购订单</span><span class="sxs-lookup"><span data-stu-id="50f46-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="50f46-111">转到“采购”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="50f46-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="50f46-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="50f46-112">Click New.</span></span>
3. <span data-ttu-id="50f46-113">在“供应商帐户”字段中输入 US-101。</span><span class="sxs-lookup"><span data-stu-id="50f46-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="50f46-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="50f46-114">Click OK.</span></span>
5. <span data-ttu-id="50f46-115">在“物料编号”字段中输入 M0001。</span><span class="sxs-lookup"><span data-stu-id="50f46-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="50f46-116">在“数量”字段中，输入 5。</span><span class="sxs-lookup"><span data-stu-id="50f46-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="50f46-117">在操作窗格上，单击“采购”。</span><span class="sxs-lookup"><span data-stu-id="50f46-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="50f46-118">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="50f46-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="50f46-119">记录收货</span><span class="sxs-lookup"><span data-stu-id="50f46-119">Record receipt of goods</span></span>
1. <span data-ttu-id="50f46-120">在操作窗格上，单击“接收”。</span><span class="sxs-lookup"><span data-stu-id="50f46-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="50f46-121">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="50f46-121">Click Product receipt.</span></span>
    * <span data-ttu-id="50f46-122">“数量”字段用于为要接收的数量选择不同选项。</span><span class="sxs-lookup"><span data-stu-id="50f46-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="50f46-123">例如，如果某个数量以前在仓库中已登记，可以选择“登记数量”。</span><span class="sxs-lookup"><span data-stu-id="50f46-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="50f46-124">对于此示例，请使用“订购数量”的值。</span><span class="sxs-lookup"><span data-stu-id="50f46-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="50f46-125">在“物料收货”字段中键入任何值。</span><span class="sxs-lookup"><span data-stu-id="50f46-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="50f46-126">此字段用于输入将用作产品收货日记帐的凭证的参考。</span><span class="sxs-lookup"><span data-stu-id="50f46-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="50f46-127">展开“行”部分。</span><span class="sxs-lookup"><span data-stu-id="50f46-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="50f46-128">将“数量”设置为“4”。</span><span class="sxs-lookup"><span data-stu-id="50f46-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="50f46-129">您可以在此处手动指定订单中各行将收到的数量。</span><span class="sxs-lookup"><span data-stu-id="50f46-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="50f46-130">折叠“行”部分。</span><span class="sxs-lookup"><span data-stu-id="50f46-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="50f46-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="50f46-131">Click OK.</span></span>
    * <span data-ttu-id="50f46-132">此货物现已在采购订单中记录为已接收，并已创建了单据格式的产品收货日记帐以体现此信息。</span><span class="sxs-lookup"><span data-stu-id="50f46-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="50f46-133">可使用“产品收货”操作审查随采购订单创建的日记帐，以了解产品的收货内容和收货时间。</span><span class="sxs-lookup"><span data-stu-id="50f46-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


