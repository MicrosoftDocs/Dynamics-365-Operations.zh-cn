---
title: "仓库管理中关联工作的库存变动"
description: "此主题描述如何从移动设备设置和应用单件领料确认。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 463e438418c4bc1b38fd1bde8251d1383cb44a13
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="20aac-103">仓库管理中关联工作的库存变动</span><span class="sxs-lookup"><span data-stu-id="20aac-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20aac-104">使用库存变动可以决定允许哪些仓库工作人员移动预留的库存。</span><span class="sxs-lookup"><span data-stu-id="20aac-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="20aac-105">您可以灵活地在受管制的仓库中决定不允许工作人员为已经创建的领料工作选择新的领料库位。</span><span class="sxs-lookup"><span data-stu-id="20aac-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="20aac-106">它还允许仓库经理控制一些缺乏经验的工作人员应具有哪些功能。</span><span class="sxs-lookup"><span data-stu-id="20aac-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="20aac-107">灵活地管理仓库工作人员的日常操作在有些场景中很有用，例如：</span><span class="sxs-lookup"><span data-stu-id="20aac-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="20aac-108">方案 1</span><span class="sxs-lookup"><span data-stu-id="20aac-108">Scenario 1</span></span>
<span data-ttu-id="20aac-109">一家公司拥有一个相对较小的收货区，那里塞满了等待入库的托盘和箱子。</span><span class="sxs-lookup"><span data-stu-id="20aac-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="20aac-110">当天计划要装运大批货物，因此收货职员决定将部分托盘移到辅助入库暂存区，以便将收货区清理出来。</span><span class="sxs-lookup"><span data-stu-id="20aac-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="20aac-111">方案 2</span><span class="sxs-lookup"><span data-stu-id="20aac-111">Scenario 2</span></span>
<span data-ttu-id="20aac-112">一位经验丰富的仓库工作人员注意到仓库中可以将物料合并到一个库位，而不是分成很少的数量存入 3 个彼此相邻的库位。</span><span class="sxs-lookup"><span data-stu-id="20aac-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="20aac-113">该工作人员要合并这些数量，将每个库位的物料移动到同一个库位和牌照上。</span><span class="sxs-lookup"><span data-stu-id="20aac-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="20aac-114">方案 3</span><span class="sxs-lookup"><span data-stu-id="20aac-114">Scenario 3</span></span>
<span data-ttu-id="20aac-115">托盘正在暂存库位（例如 BAYDOOR01 附近的 STAGE01）等待装运。</span><span class="sxs-lookup"><span data-stu-id="20aac-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="20aac-116">但是，由于计划更改，卡车预计将抵达 BAYDOOR04。</span><span class="sxs-lookup"><span data-stu-id="20aac-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="20aac-117">装运职员了解这一情况，因此需要确保卡车不必等待从 STAGE01 装货。</span><span class="sxs-lookup"><span data-stu-id="20aac-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="20aac-118">装运职员决定将要装运的物料从 STAGE01 移动到离新的目的地更近的 STAGE04。</span><span class="sxs-lookup"><span data-stu-id="20aac-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="20aac-119">当前限制</span><span class="sxs-lookup"><span data-stu-id="20aac-119">Current limitations</span></span>

<span data-ttu-id="20aac-120">您可以移动的工作预留限于销售订单、转移单发货、转移单收货、采购订单和补货工作。</span><span class="sxs-lookup"><span data-stu-id="20aac-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="20aac-121">移动物料受到限制，以防止拆分工作行。</span><span class="sxs-lookup"><span data-stu-id="20aac-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="20aac-122">这意味着，如果一个工作行中有来自库位 Loc1 的 100 件物料 A，则您无法仅将其中的 30 件物料 A 移动到另一个库位。</span><span class="sxs-lookup"><span data-stu-id="20aac-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="20aac-123">这将导致现有工作行被拆分为 30 和 70，因为现在的库位不相同。</span><span class="sxs-lookup"><span data-stu-id="20aac-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="20aac-124">对于暂存方案，您要将货物移出来的牌照或您要将货物移进去的牌照设置为工作订单的目标 LP，仅允许移动整个 LP，以免分解目标 LP。</span><span class="sxs-lookup"><span data-stu-id="20aac-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="20aac-125">目前仅支持临时变动。</span><span class="sxs-lookup"><span data-stu-id="20aac-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="20aac-126">这意味着您无法通过模板移动设备菜单项的移动来移动预留的库存。</span><span class="sxs-lookup"><span data-stu-id="20aac-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="20aac-127">为单个工作人员设置移动预留库存的权限</span><span class="sxs-lookup"><span data-stu-id="20aac-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="20aac-128">对于应允许其移动预留库存的工作人员，选择**仓库管理** > **设置** > **工作人员**下的**允许包含关联工作的库存移动**复选框。</span><span class="sxs-lookup"><span data-stu-id="20aac-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="20aac-129">往回移植</span><span class="sxs-lookup"><span data-stu-id="20aac-129">Backported</span></span>

<span data-ttu-id="20aac-130">此功能也已往回移植到 Microsoft Dynamics AX 2012 R3，并将作为 CU12 的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="20aac-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="20aac-131">也可以通过 KB 编号 3192548 单独下载。</span><span class="sxs-lookup"><span data-stu-id="20aac-131">It can also be downloaded individually through KB number 3192548.</span></span> 


