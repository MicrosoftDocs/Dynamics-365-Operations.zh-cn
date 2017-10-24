--- 
title: "创建生产订单"
description: "此程序说明如何创建一个生产订单。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 730adcea0ac59f683ecae8cbb62025bd7db75c55
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-order"></a><span data-ttu-id="a5c44-103">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="a5c44-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5c44-104">此程序说明如何创建一个生产订单。</span><span class="sxs-lookup"><span data-stu-id="a5c44-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="a5c44-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="a5c44-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5c44-106">这七个程序中的第一个诠释了生产订单的生命周期。</span><span class="sxs-lookup"><span data-stu-id="a5c44-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="a5c44-107">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="a5c44-107">Create a production order</span></span>
1. <span data-ttu-id="a5c44-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="a5c44-109">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-109">Click New production order.</span></span>
3. <span data-ttu-id="a5c44-110">在“物料编号”字段中，键入“D0001”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="a5c44-111">在“交货”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="a5c44-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="a5c44-112">交货日期说明生产订单应已完成以便按时交货。</span><span class="sxs-lookup"><span data-stu-id="a5c44-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="a5c44-113">此日期可以在计划流程中使用。</span><span class="sxs-lookup"><span data-stu-id="a5c44-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="a5c44-114">例如，您可以根据交货日期制定之后的订单。</span><span class="sxs-lookup"><span data-stu-id="a5c44-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="a5c44-115">将“数量”设置为“20”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="a5c44-116">注意：物料清单编号字段自动显示当前物料的所有有效物料清单的编号，但是，您可以通过从审核的物料清单版本列表中选择有效物料清单来更改生产订单的物料清单。</span><span class="sxs-lookup"><span data-stu-id="a5c44-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="a5c44-117">工艺路线编号字段自动显示当前物料的所有有效工艺路线的编号，但是，您可以通过从审核的工艺路线版本列表中选择有效工艺路线来更改生产订单的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="a5c44-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="a5c44-118">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="a5c44-119">确认生产订单</span><span class="sxs-lookup"><span data-stu-id="a5c44-119">Validate the production order</span></span>
1. <span data-ttu-id="a5c44-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a5c44-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a5c44-121">单击您所创建的生产订单编号的链接。</span><span class="sxs-lookup"><span data-stu-id="a5c44-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="a5c44-122">可以打开订单的详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="a5c44-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="a5c44-123">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-123">Click Edit.</span></span>
3. <span data-ttu-id="a5c44-124">在“交货”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="a5c44-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="a5c44-125">例如，可以更改生产订单的交货日期。</span><span class="sxs-lookup"><span data-stu-id="a5c44-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="a5c44-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-126">Click Save.</span></span>
5. <span data-ttu-id="a5c44-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a5c44-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="a5c44-128">更新物料清单</span><span class="sxs-lookup"><span data-stu-id="a5c44-128">Update the BOM</span></span>
1. <span data-ttu-id="a5c44-129">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a5c44-130">单击“物料清单”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-130">Click BOM.</span></span>
    * <span data-ttu-id="a5c44-131">打开“物料清单”页面并确认物料清单数据是订单创建时所复制的默认数据。</span><span class="sxs-lookup"><span data-stu-id="a5c44-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="a5c44-132">在此程序中，需要更新物料清单的数量。</span><span class="sxs-lookup"><span data-stu-id="a5c44-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="a5c44-133">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-133">Click Edit.</span></span>
4. <span data-ttu-id="a5c44-134">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a5c44-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a5c44-135">更改该物料清单行的数量将会影响生产订单物料消耗的成本预估。</span><span class="sxs-lookup"><span data-stu-id="a5c44-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="a5c44-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-136">Click Save.</span></span>
6. <span data-ttu-id="a5c44-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a5c44-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="a5c44-138">更新生产路径</span><span class="sxs-lookup"><span data-stu-id="a5c44-138">Update the production route</span></span>
1. <span data-ttu-id="a5c44-139">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a5c44-140">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-140">Click Route.</span></span>
    * <span data-ttu-id="a5c44-141">打开“路径”页面并确认生产流程的数据是创建订单之时所复制的默认数据。</span><span class="sxs-lookup"><span data-stu-id="a5c44-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="a5c44-142">在此程序中，需要更新生产流程中的操作步骤数量。</span><span class="sxs-lookup"><span data-stu-id="a5c44-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="a5c44-143">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a5c44-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a5c44-144">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-144">Click Edit.</span></span>
5. <span data-ttu-id="a5c44-145">在“进程数量“ 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a5c44-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="a5c44-146">更改生产时间将会影响生产订单的路线消耗预估和成本预估。</span><span class="sxs-lookup"><span data-stu-id="a5c44-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="a5c44-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a5c44-147">Click Save.</span></span>
7. <span data-ttu-id="a5c44-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a5c44-148">Close the page.</span></span>

