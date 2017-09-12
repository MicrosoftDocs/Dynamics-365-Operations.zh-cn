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
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ac2ee418082aa6579424fc9480478587b7c22c6d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-production-order"></a><span data-ttu-id="34d7c-103">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="34d7c-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34d7c-104">此程序说明如何创建一个生产订单。</span><span class="sxs-lookup"><span data-stu-id="34d7c-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="34d7c-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="34d7c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="34d7c-106">这七个程序中的第一个诠释了生产订单的生命周期。</span><span class="sxs-lookup"><span data-stu-id="34d7c-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="34d7c-107">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="34d7c-107">Create a production order</span></span>
1. <span data-ttu-id="34d7c-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="34d7c-109">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-109">Click New production order.</span></span>
3. <span data-ttu-id="34d7c-110">在“物料编号”字段中，键入“D0001”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="34d7c-111">在“交货”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="34d7c-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="34d7c-112">交货日期说明生产订单应已完成以便按时交货。</span><span class="sxs-lookup"><span data-stu-id="34d7c-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="34d7c-113">此日期可以在计划流程中使用。</span><span class="sxs-lookup"><span data-stu-id="34d7c-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="34d7c-114">例如，您可以根据交货日期制定之后的订单。</span><span class="sxs-lookup"><span data-stu-id="34d7c-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="34d7c-115">将“数量”设置为“20”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="34d7c-116">注意：物料清单编号字段自动显示当前物料的所有有效物料清单的编号，但是，您可以通过从审核的物料清单版本列表中选择有效物料清单来更改生产订单的物料清单。</span><span class="sxs-lookup"><span data-stu-id="34d7c-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="34d7c-117">工艺路线编号字段自动显示当前物料的所有有效工艺路线的编号，但是，您可以通过从审核的工艺路线版本列表中选择有效工艺路线来更改生产订单的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="34d7c-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="34d7c-118">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="34d7c-119">确认生产订单</span><span class="sxs-lookup"><span data-stu-id="34d7c-119">Validate the production order</span></span>
1. <span data-ttu-id="34d7c-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="34d7c-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="34d7c-121">单击您所创建的生产订单编号的链接。</span><span class="sxs-lookup"><span data-stu-id="34d7c-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="34d7c-122">可以打开订单的详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="34d7c-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="34d7c-123">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-123">Click Edit.</span></span>
3. <span data-ttu-id="34d7c-124">在“交货”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="34d7c-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="34d7c-125">例如，可以更改生产订单的交货日期。</span><span class="sxs-lookup"><span data-stu-id="34d7c-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="34d7c-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-126">Click Save.</span></span>
5. <span data-ttu-id="34d7c-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34d7c-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="34d7c-128">更新物料清单</span><span class="sxs-lookup"><span data-stu-id="34d7c-128">Update the BOM</span></span>
1. <span data-ttu-id="34d7c-129">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="34d7c-130">单击“物料清单”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-130">Click BOM.</span></span>
    * <span data-ttu-id="34d7c-131">打开“物料清单”页面并确认物料清单数据是订单创建时所复制的默认数据。</span><span class="sxs-lookup"><span data-stu-id="34d7c-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="34d7c-132">在此程序中，需要更新物料清单的数量。</span><span class="sxs-lookup"><span data-stu-id="34d7c-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="34d7c-133">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-133">Click Edit.</span></span>
4. <span data-ttu-id="34d7c-134">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="34d7c-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="34d7c-135">更改该物料清单行的数量将会影响生产订单物料消耗的成本预估。</span><span class="sxs-lookup"><span data-stu-id="34d7c-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="34d7c-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-136">Click Save.</span></span>
6. <span data-ttu-id="34d7c-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34d7c-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="34d7c-138">更新生产路径</span><span class="sxs-lookup"><span data-stu-id="34d7c-138">Update the production route</span></span>
1. <span data-ttu-id="34d7c-139">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="34d7c-140">单击“路径”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-140">Click Route.</span></span>
    * <span data-ttu-id="34d7c-141">打开“路径”页面并确认生产流程的数据是创建订单之时所复制的默认数据。</span><span class="sxs-lookup"><span data-stu-id="34d7c-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="34d7c-142">在此程序中，需要更新生产流程中的操作步骤数量。</span><span class="sxs-lookup"><span data-stu-id="34d7c-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="34d7c-143">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34d7c-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="34d7c-144">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-144">Click Edit.</span></span>
5. <span data-ttu-id="34d7c-145">在“处理数量”</span><span class="sxs-lookup"><span data-stu-id="34d7c-145">In the Process qty.</span></span> <span data-ttu-id="34d7c-146">字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="34d7c-146">field, enter a number.</span></span>
    * <span data-ttu-id="34d7c-147">更改生产时间将会影响生产订单的路线消耗预估和成本预估。</span><span class="sxs-lookup"><span data-stu-id="34d7c-147">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="34d7c-148">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34d7c-148">Click Save.</span></span>
7. <span data-ttu-id="34d7c-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="34d7c-149">Close the page.</span></span>


