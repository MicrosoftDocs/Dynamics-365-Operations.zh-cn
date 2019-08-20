---
title: 检查存货可用性
description: 此过程显示如何检查特定物料编号的现有和实际现有库存量。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b78b2e4ec3179450d635857353846c9bcb23eed
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795164"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="fe7f0-103">检查库存可用性</span><span class="sxs-lookup"><span data-stu-id="fe7f0-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe7f0-104">此过程显示如何检查特定物料编号的现有和实际现有库存量。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="fe7f0-105">它还向您显示如何获取有关物料的供应信息。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="fe7f0-106">实际现有库存量为可用现有库存量，即购买、接收和登记的库存量。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="fe7f0-107">现有库存量不仅包括可用的现有库存量，而且还包括已经订购但尚未收到或登记的库存量。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="fe7f0-108">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="fe7f0-109">如果您正在使用 USMF，则可以使用显示的示例值。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="fe7f0-110">这些任务通常由仓库工作人员完成。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="fe7f0-111">检查物料的现有库存量</span><span class="sxs-lookup"><span data-stu-id="fe7f0-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="fe7f0-112">转到“库存管理”>“查询和报表”>“现有库存量”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="fe7f0-113">选择物料编号行。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-113">Select the Item number row.</span></span>
    * <span data-ttu-id="fe7f0-114">要按物料编号查询现有库存量，请选择“表”设置为现有库存量和“字段”设置为物料编号的行。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="fe7f0-115">在“标准”字段中，选择要查询的物料。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="fe7f0-116">如果您正在使用 USMF 演示数据公司，则可以选择“M9201”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="fe7f0-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-117">Click OK.</span></span>
5. <span data-ttu-id="fe7f0-118">单击“维度”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-118">Click Dimensions.</span></span>
    * <span data-ttu-id="fe7f0-119">“维度”选项卡允许您选择您要查看的现有库存信息的详细程度。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="fe7f0-120">如果您需要有关预留的数据，则必须显示使用高级仓库程序 (WHS) 物料的所有库存维度。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="fe7f0-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-121">Click OK.</span></span>
7. <span data-ttu-id="fe7f0-122">在“操作”窗格上，单击“相关信息”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="fe7f0-123">如果未看到它，则需要单击省略号按钮 (…) 以查看其他的操作窗格选项。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="fe7f0-124">单击“供给概览”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-124">Click Supply overview.</span></span>
    * <span data-ttu-id="fe7f0-125">“供应概览”选项卡提供了特定物料的供应信息，例如现有数量、提前期和供应商信息。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="fe7f0-126">展开“现有量”部分。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="fe7f0-127">展开“供应商”部分。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="fe7f0-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-128">Close the page.</span></span>
12. <span data-ttu-id="fe7f0-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="fe7f0-130">检查实际现有库存</span><span class="sxs-lookup"><span data-stu-id="fe7f0-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="fe7f0-131">转到“库存管理”>“查询和报表”>“实际现有库存量”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="fe7f0-132">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fe7f0-133">您可以使用“站点和仓库”字段筛选物料列表。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="fe7f0-134">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-134">Refresh the page.</span></span>
4. <span data-ttu-id="fe7f0-135">单击“显示维度”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="fe7f0-136">“维度显示”选项卡允许您选择您要查看的现有库存信息的详细程度。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="fe7f0-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-137">Click OK.</span></span>
6. <span data-ttu-id="fe7f0-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="fe7f0-139">按库位查看现有库存量</span><span class="sxs-lookup"><span data-stu-id="fe7f0-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="fe7f0-140">转到“仓库管理”>“查询和报表”>“现有库位”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="fe7f0-141">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="fe7f0-142">如果您正在使用 USMF 演示数据公司，则可以使用“51”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="fe7f0-143">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-143">Refresh the page.</span></span>
4. <span data-ttu-id="fe7f0-144">单击“显示维度”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="fe7f0-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-145">Click OK.</span></span>
6. <span data-ttu-id="fe7f0-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fe7f0-146">Close the page.</span></span>

