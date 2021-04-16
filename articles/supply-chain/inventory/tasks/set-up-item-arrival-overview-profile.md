---
title: 设置物料到达概览配置文件
description: 此主题侧重于到货概览配置文件的设置。
author: ShylaThompson
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0394d1b4288dac0ff913b125017571a8c0bc95a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829828"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="1a855-103">设置物料到达概览配置文件</span><span class="sxs-lookup"><span data-stu-id="1a855-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="1a855-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="1a855-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="1a855-105">此主题侧重于到货概览配置文件的设置。</span><span class="sxs-lookup"><span data-stu-id="1a855-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="1a855-106">到货概览配置文件是用户打开到货概览页面时将应用的规则的集合。</span><span class="sxs-lookup"><span data-stu-id="1a855-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="1a855-107">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="1a855-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="1a855-108">此过程通常由验收员完成。</span><span class="sxs-lookup"><span data-stu-id="1a855-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="1a855-109">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 配送 > 到货概览配置文件**。</span><span class="sxs-lookup"><span data-stu-id="1a855-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="1a855-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1a855-110">Select **New**.</span></span> <span data-ttu-id="1a855-111">由于您几乎总是操作相同仓库的整车卸货，您应创建到货概览资料，以简化收到物料的登记流程。</span><span class="sxs-lookup"><span data-stu-id="1a855-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="1a855-112">在 **到货概览配置文件名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1a855-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="1a855-113">在 **显示行** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="1a855-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="1a855-114">选择要针对收货显示的行：</span><span class="sxs-lookup"><span data-stu-id="1a855-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="1a855-115">**全部** - 显示所有行，而不考虑状态。</span><span class="sxs-lookup"><span data-stu-id="1a855-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="1a855-116">**在进行中** – 显示进度为“完成”或“部分”的收货的行。</span><span class="sxs-lookup"><span data-stu-id="1a855-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="1a855-117">这意味着，对于每个行，已在到达日记帐中登记全部数量或部分数量。</span><span class="sxs-lookup"><span data-stu-id="1a855-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="1a855-118">**未完成** – 显示进度为“无”或“部分”的收货的行。</span><span class="sxs-lookup"><span data-stu-id="1a855-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="1a855-119">这意味着，对于每个行，没有在到达日记帐中登记数量或仅登记部分数量。</span><span class="sxs-lookup"><span data-stu-id="1a855-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="1a855-120">展开或收起 **到货选项** 部分。</span><span class="sxs-lookup"><span data-stu-id="1a855-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="1a855-121">在 **提前天数** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1a855-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="1a855-122">这设置了筛选器，以显示预期在接下来几天内（取决于您设置的数字）收到的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="1a855-123">在 **延迟天数** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1a855-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="1a855-124">这设置了筛选器，以显示在今天之前的几天内收到的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="1a855-125">在 **仓库** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1a855-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="1a855-126">一个或多个仓库筛选器。</span><span class="sxs-lookup"><span data-stu-id="1a855-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="1a855-127">在 **交货方式** 字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1a855-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="1a855-128">它可设置一个筛选器以仅显示带此“交货方式”的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="1a855-129">在 **名称** 字段中选择 WHS。</span><span class="sxs-lookup"><span data-stu-id="1a855-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="1a855-130">在 **仓库** 字段中，选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="1a855-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="1a855-131">这是默认仓库，将用于使用此模板的已登记的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="1a855-132">在 **库位** 字段中，选择 **Baydoor**。</span><span class="sxs-lookup"><span data-stu-id="1a855-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="1a855-133">这是默认位置，将用于使用此模板的已登记的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="1a855-134">展开或折叠 **到货查询详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="1a855-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="1a855-135">在 **限制到站点** 字段中，选择站点 2。</span><span class="sxs-lookup"><span data-stu-id="1a855-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="1a855-136">它可设置一个筛选器以仅显示带此站点的收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="1a855-137">将 **采购订单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="1a855-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="1a855-138">从采购订单选择收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="1a855-139">将 **转移单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="1a855-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="1a855-140">从转移订单选择收据行。</span><span class="sxs-lookup"><span data-stu-id="1a855-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="1a855-141">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a855-141">Select **Save**.</span></span>
18. <span data-ttu-id="1a855-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a855-142">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]