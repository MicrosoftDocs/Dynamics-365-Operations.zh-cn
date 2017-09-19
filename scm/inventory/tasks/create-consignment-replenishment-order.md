---
title: "创建托运补货订单"
description: "此过程显示如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。"
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 6286e8f52b8131a8e4779f1e11d84233b8e0760e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="c7d39-103">创建托运补货订单</span><span class="sxs-lookup"><span data-stu-id="c7d39-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7d39-104">此过程显示如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。</span><span class="sxs-lookup"><span data-stu-id="c7d39-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="c7d39-105">还显示如何记录物料收据，以便将托运库存登记为供应商拥有的现有库存。</span><span class="sxs-lookup"><span data-stu-id="c7d39-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="c7d39-106">此过程通常由采购专员完成。</span><span class="sxs-lookup"><span data-stu-id="c7d39-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="c7d39-107">您可以使用演示数据公司 USMF 运行此指南。</span><span class="sxs-lookup"><span data-stu-id="c7d39-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="c7d39-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="c7d39-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="c7d39-109">创建托运补货订单</span><span class="sxs-lookup"><span data-stu-id="c7d39-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="c7d39-110">转到“采购和购置”>“托运|>托运补货订单“。</span><span class="sxs-lookup"><span data-stu-id="c7d39-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="c7d39-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-111">Click New.</span></span>
3. <span data-ttu-id="c7d39-112">在“供应商帐户”字段中选择供应商 US-104。</span><span class="sxs-lookup"><span data-stu-id="c7d39-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="c7d39-113">必须在“库存所有者”页面中选择已登记为所有者的供应商。</span><span class="sxs-lookup"><span data-stu-id="c7d39-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="c7d39-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-114">Click OK.</span></span>
5. <span data-ttu-id="c7d39-115">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-115">Click Add line.</span></span>
6. <span data-ttu-id="c7d39-116">在“物料编号”字段中，键入“M9211CI”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="c7d39-117">必须选择为托运库存设置的物料。</span><span class="sxs-lookup"><span data-stu-id="c7d39-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="c7d39-118">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c7d39-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="c7d39-119">在“请求交付日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="c7d39-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="c7d39-120">请求日期和确认日期由 MRP 引擎用于货物的预期到达。</span><span class="sxs-lookup"><span data-stu-id="c7d39-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="c7d39-121">在“确认交货日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="c7d39-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="c7d39-122">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="c7d39-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="c7d39-123">单击“库存维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="c7d39-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="c7d39-124">若要在”库存维度所有者“字段中显示所有者，请刷新页面。</span><span class="sxs-lookup"><span data-stu-id="c7d39-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="c7d39-125">供应商 US-104 现在作为所有者列出。</span><span class="sxs-lookup"><span data-stu-id="c7d39-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="c7d39-126">检查库存交易记录状态。</span><span class="sxs-lookup"><span data-stu-id="c7d39-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="c7d39-127">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-127">Click Inventory.</span></span>
2. <span data-ttu-id="c7d39-128">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-128">Click Transactions.</span></span>
3. <span data-ttu-id="c7d39-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c7d39-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c7d39-130">请注意，“收货”字段设置为“已订购”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="c7d39-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c7d39-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="c7d39-132">接收多个物料</span><span class="sxs-lookup"><span data-stu-id="c7d39-132">Receive items</span></span>
1. <span data-ttu-id="c7d39-133">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-133">Click Product receipt.</span></span>
2. <span data-ttu-id="c7d39-134">在“外部物料收据”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c7d39-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="c7d39-135">在”数量“字段中，输入一个比此处显示的数字更小的数字。</span><span class="sxs-lookup"><span data-stu-id="c7d39-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="c7d39-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="c7d39-137">检查现有库存量</span><span class="sxs-lookup"><span data-stu-id="c7d39-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="c7d39-138">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-138">Click Inventory.</span></span>
2. <span data-ttu-id="c7d39-139">单击”现有量“。</span><span class="sxs-lookup"><span data-stu-id="c7d39-139">Click On-hand.</span></span>
3. <span data-ttu-id="c7d39-140">单击“概览”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-140">Click Overview.</span></span>
    * <span data-ttu-id="c7d39-141">已作为供应商拥有的托运库存接收的物料现有可用。</span><span class="sxs-lookup"><span data-stu-id="c7d39-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="c7d39-142">托运补货订单的剩余数量在“订购总数”字段中显示。</span><span class="sxs-lookup"><span data-stu-id="c7d39-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="c7d39-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c7d39-143">Close the page.</span></span>
5. <span data-ttu-id="c7d39-144">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="c7d39-144">Click Close.</span></span>
