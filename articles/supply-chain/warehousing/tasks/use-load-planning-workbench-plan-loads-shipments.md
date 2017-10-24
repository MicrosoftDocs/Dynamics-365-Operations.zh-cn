--- 
title: "使用装载计划工作台计划负荷和装运"
description: "此过程显示如何使用装载计划工作台创建销售订单的装载量。"
author: BibiSp
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
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="5e012-103">使用装载计划工作台计划负荷和装运</span><span class="sxs-lookup"><span data-stu-id="5e012-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e012-104">此过程显示如何使用装载计划工作台创建销售订单的装载量。</span><span class="sxs-lookup"><span data-stu-id="5e012-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="5e012-105">作为先决条件，我们将首先创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="5e012-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="5e012-106">此过程为运输协调员日常工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="5e012-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="5e012-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="5e012-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="5e012-108">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="5e012-108">Create a sales order</span></span>
1. <span data-ttu-id="5e012-109">转到应收帐项目>订单>所有销售订单。</span><span class="sxs-lookup"><span data-stu-id="5e012-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5e012-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5e012-110">Click New.</span></span>
3. <span data-ttu-id="5e012-111">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5e012-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5e012-112">选择帐户 US-004。</span><span class="sxs-lookup"><span data-stu-id="5e012-112">Select account US-004.</span></span>
5. <span data-ttu-id="5e012-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5e012-113">Click OK.</span></span>
6. <span data-ttu-id="5e012-114">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5e012-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5e012-115">选择物料 A0001。</span><span class="sxs-lookup"><span data-stu-id="5e012-115">Select item A0001.</span></span>
    * <span data-ttu-id="5e012-116">A0001 可供运输管理流程使用。</span><span class="sxs-lookup"><span data-stu-id="5e012-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="5e012-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="5e012-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5e012-118">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="5e012-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="5e012-119">在“仓库”字段中，键入“24”。</span><span class="sxs-lookup"><span data-stu-id="5e012-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="5e012-120">在此示例中，选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="5e012-120">In this example select warehouse 24.</span></span> <span data-ttu-id="5e012-121">此仓库可供运输管理和高级仓库管理使用。</span><span class="sxs-lookup"><span data-stu-id="5e012-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="5e012-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5e012-122">Click Save.</span></span>
12. <span data-ttu-id="5e012-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5e012-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="5e012-124">创建“新装载”。</span><span class="sxs-lookup"><span data-stu-id="5e012-124">Create a new load</span></span>
1. <span data-ttu-id="5e012-125">转到“运输管理”>“计划”>“装载计划工作台”。</span><span class="sxs-lookup"><span data-stu-id="5e012-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="5e012-126">单击“销售行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="5e012-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="5e012-127">现在将构建您刚创建的销售订单的装载量。</span><span class="sxs-lookup"><span data-stu-id="5e012-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="5e012-128">装载量的构建基于采购订单、转移订单和销售订单的供应和需求。</span><span class="sxs-lookup"><span data-stu-id="5e012-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="5e012-129">在操作窗格上，单击“供应与需求”。</span><span class="sxs-lookup"><span data-stu-id="5e012-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="5e012-130">单击“至新装载量”。</span><span class="sxs-lookup"><span data-stu-id="5e012-130">Click To new load.</span></span>
5. <span data-ttu-id="5e012-131">在“装载模板 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5e012-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5e012-132">装载量模板定义整个装载量的重量和体积的最大度量值。</span><span class="sxs-lookup"><span data-stu-id="5e012-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="5e012-133">例如，装载量模板可能表示卡车或集装箱的大小。</span><span class="sxs-lookup"><span data-stu-id="5e012-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="5e012-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="5e012-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5e012-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5e012-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="5e012-136">为装载量评级和路线选择</span><span class="sxs-lookup"><span data-stu-id="5e012-136">Rate and route the load</span></span>
1. <span data-ttu-id="5e012-137">单击“评级和路线选择”。</span><span class="sxs-lookup"><span data-stu-id="5e012-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="5e012-138">单击“费率路线工作台”。</span><span class="sxs-lookup"><span data-stu-id="5e012-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="5e012-139">单击“费率工场”。</span><span class="sxs-lookup"><span data-stu-id="5e012-139">Click Rate shop.</span></span>
4. <span data-ttu-id="5e012-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="5e012-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5e012-141">单击“分配”。</span><span class="sxs-lookup"><span data-stu-id="5e012-141">Click Assign.</span></span>
6. <span data-ttu-id="5e012-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5e012-142">Close the page.</span></span>
7. <span data-ttu-id="5e012-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5e012-143">Close the page.</span></span>


