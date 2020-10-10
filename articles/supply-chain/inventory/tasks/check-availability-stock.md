---
title: 检查存货可用性
description: 此过程显示如何检查特定物料编号的现有和实际现有库存量。
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3f6f601d2d48ede2c4db198ac5438aa32e056d
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829769"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="a7da4-103">检查库存可用性</span><span class="sxs-lookup"><span data-stu-id="a7da4-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7da4-104">此过程显示如何检查特定物料编号的现有和实际现有库存量。</span><span class="sxs-lookup"><span data-stu-id="a7da4-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="a7da4-105">它还向您显示如何获取有关物料的供应信息。</span><span class="sxs-lookup"><span data-stu-id="a7da4-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="a7da4-106">实际现有库存量为可用现有库存量，即购买、接收和登记的库存量。</span><span class="sxs-lookup"><span data-stu-id="a7da4-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="a7da4-107">现有库存量不仅包括可用的现有库存量，而且还包括已经订购但尚未收到或登记的库存量。</span><span class="sxs-lookup"><span data-stu-id="a7da4-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="a7da4-108">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="a7da4-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="a7da4-109">如果您正在使用 USMF，则可以使用显示的示例值。</span><span class="sxs-lookup"><span data-stu-id="a7da4-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="a7da4-110">这些任务通常由仓库工作人员完成。</span><span class="sxs-lookup"><span data-stu-id="a7da4-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="a7da4-111">检查物料的现有库存量</span><span class="sxs-lookup"><span data-stu-id="a7da4-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="a7da4-112">转到**导航窗格 > 模块 > 库存管理 > 查询和报表 > 现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="a7da4-113">选择**物料编号**行。</span><span class="sxs-lookup"><span data-stu-id="a7da4-113">Select the **Item number** row.</span></span> <span data-ttu-id="a7da4-114">要按物料编号查询现有库存量，请选择“表”设置为**现有库存量**和“字段”设置为**物料**编号的行。</span><span class="sxs-lookup"><span data-stu-id="a7da4-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="a7da4-115">在**标准**字段中，选择要查询的物料。</span><span class="sxs-lookup"><span data-stu-id="a7da4-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="a7da4-116">如果您正在使用 USMF 演示数据公司，则可以选择“M9201”。</span><span class="sxs-lookup"><span data-stu-id="a7da4-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="a7da4-117">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-117">Click **OK**.</span></span>
5. <span data-ttu-id="a7da4-118">在**操作窗格**上，单击**维度**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="a7da4-119">**维度**选项卡允许您选择您要查看的现有库存信息的详细程度。</span><span class="sxs-lookup"><span data-stu-id="a7da4-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="a7da4-120">如果您需要有关预留的数据，则必须显示使用高级仓库程序 (WMS) 物料的所有库存维度。</span><span class="sxs-lookup"><span data-stu-id="a7da4-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="a7da4-121">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-121">Click **OK**.</span></span>
7. <span data-ttu-id="a7da4-122">在**操作窗格**上，单击**相关信息**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="a7da4-123">如果未看到此选项，则需要单击省略号按钮 (…) 以查看其他的操作窗格选项。</span><span class="sxs-lookup"><span data-stu-id="a7da4-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="a7da4-124">单击**供给概览**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-124">Click **Supply overview**.</span></span> <span data-ttu-id="a7da4-125">**供给概览**选项卡提供了特定物料的供应信息，例如现有数量、提前期和供应商信息。</span><span class="sxs-lookup"><span data-stu-id="a7da4-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="a7da4-126">展开**现有量**部分。</span><span class="sxs-lookup"><span data-stu-id="a7da4-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="a7da4-127">展开**供应商**部分。</span><span class="sxs-lookup"><span data-stu-id="a7da4-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="a7da4-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-128">Close the page.</span></span>
12. <span data-ttu-id="a7da4-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="a7da4-130">检查实际现有库存</span><span class="sxs-lookup"><span data-stu-id="a7da4-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="a7da4-131">转到**导航窗格 > 模块 > 仓库管理 > 查询和报表 > 实际现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="a7da4-132">在**项目编号**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a7da4-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="a7da4-133">您可以使用“站点和仓库”字段筛选物料列表。</span><span class="sxs-lookup"><span data-stu-id="a7da4-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="a7da4-134">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-134">Refresh the page.</span></span>
4. <span data-ttu-id="a7da4-135">在**操作窗格**上单击**显示维度**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="a7da4-136">“维度显示”选项卡允许您选择您要查看的现有库存信息的详细程度。</span><span class="sxs-lookup"><span data-stu-id="a7da4-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="a7da4-137">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-137">Click **OK**.</span></span>
6. <span data-ttu-id="a7da4-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="a7da4-139">按库位查看现有库存量</span><span class="sxs-lookup"><span data-stu-id="a7da4-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="a7da4-140">转到**导航窗格 > 模块 > 仓库管理 > 查询和报表 > 按库位显示的现有量**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="a7da4-141">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a7da4-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="a7da4-142">如果您正在使用 USMF 演示数据公司，则可以使用“51”。</span><span class="sxs-lookup"><span data-stu-id="a7da4-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="a7da4-143">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-143">Refresh the page.</span></span>
4. <span data-ttu-id="a7da4-144">单击**显示维度**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="a7da4-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7da4-145">Click **OK**.</span></span>
6. <span data-ttu-id="a7da4-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a7da4-146">Close the page.</span></span>

