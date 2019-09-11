---
title: 设置物料到达概览配置文件
description: 此主题侧重于到货概览配置文件的设置。
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867214"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="b4891-103">设置物料到达概览配置文件</span><span class="sxs-lookup"><span data-stu-id="b4891-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4891-104">此主题侧重于到货概览配置文件的设置。</span><span class="sxs-lookup"><span data-stu-id="b4891-104">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="b4891-105">到货概览配置文件是用户打开到货概览页面时将应用的规则的集合。</span><span class="sxs-lookup"><span data-stu-id="b4891-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="b4891-106">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="b4891-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b4891-107">此过程通常由验收员完成。</span><span class="sxs-lookup"><span data-stu-id="b4891-107">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="b4891-108">在导航窗格中，转到**模块 > 库存管理 > 设置 > 配送 > 到货概览配置文件**。</span><span class="sxs-lookup"><span data-stu-id="b4891-108">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="b4891-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b4891-109">Select **New**.</span></span> <span data-ttu-id="b4891-110">由于您几乎总是操作相同仓库的整车卸货，您应创建到货概览资料，以简化收到物料的登记流程。</span><span class="sxs-lookup"><span data-stu-id="b4891-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="b4891-111">在**到货概览配置文件名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b4891-111">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="b4891-112">在**显示行**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b4891-112">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="b4891-113">选择要针对收货显示的行：</span><span class="sxs-lookup"><span data-stu-id="b4891-113">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="b4891-114">**全部** - 显示所有行，而不考虑状态。</span><span class="sxs-lookup"><span data-stu-id="b4891-114">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="b4891-115">**在进行中** – 显示进度为“完成”或“部分”的收货的行。</span><span class="sxs-lookup"><span data-stu-id="b4891-115">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="b4891-116">这意味着，对于每个行，已在到达日记帐中登记全部数量或部分数量。</span><span class="sxs-lookup"><span data-stu-id="b4891-116">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="b4891-117">**未完成** – 显示进度为“无”或“部分”的收货的行。</span><span class="sxs-lookup"><span data-stu-id="b4891-117">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="b4891-118">这意味着，对于每个行，没有在到达日记帐中登记数量或仅登记部分数量。</span><span class="sxs-lookup"><span data-stu-id="b4891-118">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="b4891-119">展开或收起**到货选项**部分。</span><span class="sxs-lookup"><span data-stu-id="b4891-119">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="b4891-120">在**提前天数**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b4891-120">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="b4891-121">这设置了筛选器，以显示预期在接下来几天内（取决于您设置的数字）收到的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-121">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="b4891-122">在**延迟天数**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b4891-122">In the **Days back** field, type a value.</span></span> <span data-ttu-id="b4891-123">这设置了筛选器，以显示在今天之前的几天内收到的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-123">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="b4891-124">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b4891-124">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="b4891-125">一个或多个仓库筛选器。</span><span class="sxs-lookup"><span data-stu-id="b4891-125">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="b4891-126">在**交货方式**字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b4891-126">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="b4891-127">它可设置一个筛选器以仅显示带此“交货方式”的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-127">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="b4891-128">在**名称**字段中选择 WHS。</span><span class="sxs-lookup"><span data-stu-id="b4891-128">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="b4891-129">在**仓库**字段中，选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="b4891-129">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="b4891-130">这是默认仓库，将用于使用此模板的已登记的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-130">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="b4891-131">在**库位**字段中，选择 **Baydoor**。</span><span class="sxs-lookup"><span data-stu-id="b4891-131">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="b4891-132">这是默认位置，将用于使用此模板的已登记的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-132">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="b4891-133">展开或折叠**到货查询详细信息**部分。</span><span class="sxs-lookup"><span data-stu-id="b4891-133">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="b4891-134">在**限制到站点**字段中，选择站点 2。</span><span class="sxs-lookup"><span data-stu-id="b4891-134">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="b4891-135">它可设置一个筛选器以仅显示带此站点的收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-135">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="b4891-136">将**采购订单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b4891-136">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="b4891-137">从采购订单选择收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-137">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="b4891-138">将**转移单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b4891-138">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="b4891-139">从转移订单选择收据行。</span><span class="sxs-lookup"><span data-stu-id="b4891-139">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="b4891-140">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b4891-140">Select **Save**.</span></span>
18. <span data-ttu-id="b4891-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b4891-141">Close the page.</span></span>

