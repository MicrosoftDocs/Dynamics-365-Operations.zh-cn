---
title: 使用装载计划工作台计划负荷和装运
description: 本主题显示如何使用装载计划工作台创建销售订单的装载量。
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5e20eef8aa748bb64c6c14dd7e1d92ccf6592e0
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/10/2019
ms.locfileid: "1739057"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="75aaa-103">使用装载计划工作台计划负荷和装运</span><span class="sxs-lookup"><span data-stu-id="75aaa-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75aaa-104">本主题显示如何使用装载计划工作台创建销售订单的装载量。</span><span class="sxs-lookup"><span data-stu-id="75aaa-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="75aaa-105">作为先决条件，我们将首先创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="75aaa-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="75aaa-106">此过程为运输协调员日常工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="75aaa-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="75aaa-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="75aaa-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="75aaa-108">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="75aaa-108">Create a sales order</span></span>
1. <span data-ttu-id="75aaa-109">转到**导航窗格 > 模块 > 应收帐款 > 订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="75aaa-110">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-110">Select **New**.</span></span>
3. <span data-ttu-id="75aaa-111">在**客户帐户**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="75aaa-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="75aaa-112">选择帐户 **US-004**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="75aaa-113">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-113">Select **OK**.</span></span>
6. <span data-ttu-id="75aaa-114">在**物料编号**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="75aaa-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="75aaa-115">选择物料 **A0001**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-115">Select item **A0001**.</span></span> <span data-ttu-id="75aaa-116">**A0001** 可供运输管理流程使用。</span><span class="sxs-lookup"><span data-stu-id="75aaa-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="75aaa-117">在**站点**字段中，选择下拉按钮以打开查找，然后选择物料。</span><span class="sxs-lookup"><span data-stu-id="75aaa-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="75aaa-118">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="75aaa-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="75aaa-119">在**仓库**字段中，为此示例键入“24”。</span><span class="sxs-lookup"><span data-stu-id="75aaa-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="75aaa-120">此仓库可供运输管理和高级仓库管理使用。</span><span class="sxs-lookup"><span data-stu-id="75aaa-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="75aaa-121">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-121">Select **Save**.</span></span>
12. <span data-ttu-id="75aaa-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="75aaa-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="75aaa-123">创建“新装载”。</span><span class="sxs-lookup"><span data-stu-id="75aaa-123">Create a new load</span></span>
1. <span data-ttu-id="75aaa-124">找到**导航窗格 > 模块 > 运输管理 > 计划 > 装载计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="75aaa-125">选择**销售行**选项卡。现在将构建您刚创建的销售订单的装载量。</span><span class="sxs-lookup"><span data-stu-id="75aaa-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="75aaa-126">装载量的构建基于采购订单、转移订单和销售订单的供应和需求。</span><span class="sxs-lookup"><span data-stu-id="75aaa-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="75aaa-127">在操作窗格上，选择**供应与需求**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="75aaa-128">选择**至新负荷**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-128">Select **To new load**.</span></span>
5. <span data-ttu-id="75aaa-129">在**装载模板 ID** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="75aaa-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="75aaa-130">装载量模板定义整个装载量的重量和体积的最大度量值。</span><span class="sxs-lookup"><span data-stu-id="75aaa-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="75aaa-131">例如，装载量模板可能表示卡车或集装箱的大小。</span><span class="sxs-lookup"><span data-stu-id="75aaa-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="75aaa-132">选择某一物料。</span><span class="sxs-lookup"><span data-stu-id="75aaa-132">Select an item.</span></span>
6. <span data-ttu-id="75aaa-133">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="75aaa-134">为装载量评级和路线选择</span><span class="sxs-lookup"><span data-stu-id="75aaa-134">Rate and route the load</span></span>
1. <span data-ttu-id="75aaa-135">选择**评级和路线选择**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="75aaa-136">选择**费率路线工作台**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="75aaa-137">选择**费率工场**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="75aaa-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="75aaa-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="75aaa-139">选择**分配**。</span><span class="sxs-lookup"><span data-stu-id="75aaa-139">Select **Assign**.</span></span>
6. <span data-ttu-id="75aaa-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="75aaa-140">Close the page.</span></span>

