---
title: "开始生产订单"
description: "该过程显示如何在作业车间启动生产订单。"
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 3b5657e5eb2719702eae3a3c5178b3a04f7545e3
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---
# <a name="start-a-production-order"></a><span data-ttu-id="84efb-103">开始生产订单</span><span class="sxs-lookup"><span data-stu-id="84efb-103">Start a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84efb-104">该过程显示如何在作业车间启动生产订单。</span><span class="sxs-lookup"><span data-stu-id="84efb-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="84efb-105">此流程会报告时间和物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="84efb-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="84efb-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="84efb-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="84efb-107">这是解释生产订单周期的七个步骤中的第五步。</span><span class="sxs-lookup"><span data-stu-id="84efb-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="84efb-108">开始生产订单</span><span class="sxs-lookup"><span data-stu-id="84efb-108">Start a production order</span></span>
1. <span data-ttu-id="84efb-109">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="84efb-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="84efb-110">选择一个状态为“已发布”的生产订单。</span><span class="sxs-lookup"><span data-stu-id="84efb-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="84efb-111">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="84efb-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="84efb-112">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="84efb-112">Click Start.</span></span>
    * <span data-ttu-id="84efb-113">在此页，可以确认生产订单的开始时间。</span><span class="sxs-lookup"><span data-stu-id="84efb-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="84efb-114">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="84efb-114">Click the General tab.</span></span>
5. <span data-ttu-id="84efb-115">在“开始工序</span><span class="sxs-lookup"><span data-stu-id="84efb-115">In the From Oper.</span></span> <span data-ttu-id="84efb-116">编号</span><span class="sxs-lookup"><span data-stu-id="84efb-116">No.</span></span> <span data-ttu-id="84efb-117">字段中，输入“10”。</span><span class="sxs-lookup"><span data-stu-id="84efb-117">field, enter '10'.</span></span>
6. <span data-ttu-id="84efb-118">在“自动工艺路线消耗量”字段中，选择“始终”。</span><span class="sxs-lookup"><span data-stu-id="84efb-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="84efb-119">单击“现在过帐工艺卡”复选框。</span><span class="sxs-lookup"><span data-stu-id="84efb-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="84efb-120">在“自动 BOM 消耗量”字段中，选择“始终”。</span><span class="sxs-lookup"><span data-stu-id="84efb-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="84efb-121">单击“过帐领料单”复选框。</span><span class="sxs-lookup"><span data-stu-id="84efb-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="84efb-122">单击“打印过帐领料单”复选框。</span><span class="sxs-lookup"><span data-stu-id="84efb-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="84efb-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84efb-123">Click OK.</span></span>
    * <span data-ttu-id="84efb-124">这是一个已打印的显示生产订单所使用的物料的领料单。</span><span class="sxs-lookup"><span data-stu-id="84efb-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="84efb-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84efb-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="84efb-126">验证领料单</span><span class="sxs-lookup"><span data-stu-id="84efb-126">Validate the picking list</span></span>
1. <span data-ttu-id="84efb-127">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="84efb-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="84efb-128">单击“领料单”。</span><span class="sxs-lookup"><span data-stu-id="84efb-128">Click Picking list.</span></span>
3. <span data-ttu-id="84efb-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="84efb-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="84efb-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="84efb-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="84efb-131">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="84efb-131">Click Edit.</span></span>
6. <span data-ttu-id="84efb-132">在“消耗”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84efb-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="84efb-133">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="84efb-133">Click Post.</span></span>
8. <span data-ttu-id="84efb-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84efb-134">Click OK.</span></span>
    * <span data-ttu-id="84efb-135">在领料单日记帐中，过帐生产订单的物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="84efb-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="84efb-136">在过帐日记帐之前，如果在估计数量和实际消耗的数量之间存在差异，可以进行调整。</span><span class="sxs-lookup"><span data-stu-id="84efb-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="84efb-137">单击“网格面板”选项卡。</span><span class="sxs-lookup"><span data-stu-id="84efb-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="84efb-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84efb-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="84efb-139">核实工艺卡日记帐</span><span class="sxs-lookup"><span data-stu-id="84efb-139">Verify the route card journal</span></span>
1. <span data-ttu-id="84efb-140">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="84efb-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="84efb-141">单击“工艺卡”。</span><span class="sxs-lookup"><span data-stu-id="84efb-141">Click Route card.</span></span>
3. <span data-ttu-id="84efb-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="84efb-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="84efb-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="84efb-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="84efb-144">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="84efb-144">Click Edit.</span></span>
6. <span data-ttu-id="84efb-145">在“小时”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="84efb-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="84efb-146">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="84efb-146">Click Post.</span></span>
8. <span data-ttu-id="84efb-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84efb-147">Click OK.</span></span>
    * <span data-ttu-id="84efb-148">在“工艺卡日记帐”，记录各工序所用的时间。</span><span class="sxs-lookup"><span data-stu-id="84efb-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="84efb-149">还可以报告完好和残次数量。</span><span class="sxs-lookup"><span data-stu-id="84efb-149">Good and error quantity can also be reported.</span></span>  

