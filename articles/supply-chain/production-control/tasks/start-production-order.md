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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 933bf83613f30b544a9cc8e55ad4e32305522b3d
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="start-a-production-order"></a><span data-ttu-id="98bb3-103">开始生产订单</span><span class="sxs-lookup"><span data-stu-id="98bb3-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98bb3-104">该过程显示如何在作业车间启动生产订单。</span><span class="sxs-lookup"><span data-stu-id="98bb3-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="98bb3-105">此流程会报告时间和物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="98bb3-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="98bb3-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="98bb3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="98bb3-107">这是解释生产订单周期的七个步骤中的第五步。</span><span class="sxs-lookup"><span data-stu-id="98bb3-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="98bb3-108">开始生产订单</span><span class="sxs-lookup"><span data-stu-id="98bb3-108">Start a production order</span></span>
1. <span data-ttu-id="98bb3-109">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="98bb3-110">选择一个状态为“已发布”的生产订单。</span><span class="sxs-lookup"><span data-stu-id="98bb3-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="98bb3-111">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="98bb3-112">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-112">Click Start.</span></span>
    * <span data-ttu-id="98bb3-113">在此页，可以确认生产订单的开始时间。</span><span class="sxs-lookup"><span data-stu-id="98bb3-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="98bb3-114">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="98bb3-114">Click the General tab.</span></span>
5. <span data-ttu-id="98bb3-115">在“开始工序</span><span class="sxs-lookup"><span data-stu-id="98bb3-115">In the From Oper.</span></span> <span data-ttu-id="98bb3-116">编号</span><span class="sxs-lookup"><span data-stu-id="98bb3-116">No.</span></span> <span data-ttu-id="98bb3-117">字段中，输入“10”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-117">field, enter '10'.</span></span>
6. <span data-ttu-id="98bb3-118">在“自动工艺路线消耗量”字段中，选择“始终”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="98bb3-119">单击“现在过帐工艺卡”复选框。</span><span class="sxs-lookup"><span data-stu-id="98bb3-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="98bb3-120">在“自动 BOM 消耗量”字段中，选择“始终”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="98bb3-121">单击“过帐领料单”复选框。</span><span class="sxs-lookup"><span data-stu-id="98bb3-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="98bb3-122">单击“打印过帐领料单”复选框。</span><span class="sxs-lookup"><span data-stu-id="98bb3-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="98bb3-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-123">Click OK.</span></span>
    * <span data-ttu-id="98bb3-124">这是一个已打印的显示生产订单所使用的物料的领料单。</span><span class="sxs-lookup"><span data-stu-id="98bb3-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="98bb3-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="98bb3-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="98bb3-126">验证领料单</span><span class="sxs-lookup"><span data-stu-id="98bb3-126">Validate the picking list</span></span>
1. <span data-ttu-id="98bb3-127">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="98bb3-128">单击“领料单”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-128">Click Picking list.</span></span>
3. <span data-ttu-id="98bb3-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="98bb3-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="98bb3-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="98bb3-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98bb3-131">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-131">Click Edit.</span></span>
6. <span data-ttu-id="98bb3-132">在“消耗”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="98bb3-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="98bb3-133">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-133">Click Post.</span></span>
8. <span data-ttu-id="98bb3-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-134">Click OK.</span></span>
    * <span data-ttu-id="98bb3-135">在领料单日记帐中，过帐生产订单的物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="98bb3-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="98bb3-136">在过帐日记帐之前，如果在估计数量和实际消耗的数量之间存在差异，可以进行调整。</span><span class="sxs-lookup"><span data-stu-id="98bb3-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="98bb3-137">单击“网格面板”选项卡。</span><span class="sxs-lookup"><span data-stu-id="98bb3-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="98bb3-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="98bb3-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="98bb3-139">核实工艺卡日记帐</span><span class="sxs-lookup"><span data-stu-id="98bb3-139">Verify the route card journal</span></span>
1. <span data-ttu-id="98bb3-140">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="98bb3-141">单击“工艺卡”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-141">Click Route card.</span></span>
3. <span data-ttu-id="98bb3-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="98bb3-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="98bb3-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="98bb3-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98bb3-144">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-144">Click Edit.</span></span>
6. <span data-ttu-id="98bb3-145">在“小时”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="98bb3-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="98bb3-146">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-146">Click Post.</span></span>
8. <span data-ttu-id="98bb3-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="98bb3-147">Click OK.</span></span>
    * <span data-ttu-id="98bb3-148">在“工艺卡日记帐”，记录各工序所用的时间。</span><span class="sxs-lookup"><span data-stu-id="98bb3-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="98bb3-149">还可以报告完好和残次数量。</span><span class="sxs-lookup"><span data-stu-id="98bb3-149">Good and error quantity can also be reported.</span></span>  

