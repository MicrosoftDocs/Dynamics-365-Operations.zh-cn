---
title: 创建新仓库布局
description: 此主题描述如何在仓库中设置有关库位的信息。
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145655"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="66907-103">创建新仓库布局</span><span class="sxs-lookup"><span data-stu-id="66907-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66907-104">此主题描述如何在仓库中设置有关库位的信息。</span><span class="sxs-lookup"><span data-stu-id="66907-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="66907-105">此程序仅适用于仓库中“库存管理模块”的“基本仓储”，不适用于“仓库管理模块”。</span><span class="sxs-lookup"><span data-stu-id="66907-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="66907-106">您可以使用演示数据公司 USMF 或您自己的数据使用该程序。</span><span class="sxs-lookup"><span data-stu-id="66907-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="66907-107">设置默认库位容量</span><span class="sxs-lookup"><span data-stu-id="66907-107">Set the default location capacity</span></span>
1. <span data-ttu-id="66907-108">在导航窗格中，转到**模块 > 库存管理 > 设置 > 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="66907-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="66907-109">选择**库位**选项卡。</span><span class="sxs-lookup"><span data-stu-id="66907-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="66907-110">在**标准宽度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="66907-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="66907-111">在**标准深度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="66907-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="66907-112">在**标准高度**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="66907-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="66907-113">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="66907-113">Select **Save**.</span></span>
7. <span data-ttu-id="66907-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="66907-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="66907-115">定义库位名称格式</span><span class="sxs-lookup"><span data-stu-id="66907-115">Define the location name format</span></span>
1. <span data-ttu-id="66907-116">在导航窗格中，转到**模块 > 库存管理 > 设置 > 库存细分 > 仓库**。</span><span class="sxs-lookup"><span data-stu-id="66907-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="66907-117">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="66907-117">Select **New**.</span></span>
3. <span data-ttu-id="66907-118">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="66907-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="66907-119">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="66907-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="66907-120">在**站点**字段中，在查找中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="66907-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="66907-121">切换到**库位名称**部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="66907-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="66907-122">此部分中的选项定义库位名称的默认格式。</span><span class="sxs-lookup"><span data-stu-id="66907-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="66907-123">在我们的示例中，我们增加了通道编号、货架编号和货位编号。</span><span class="sxs-lookup"><span data-stu-id="66907-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="66907-124">将**包括通道**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="66907-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="66907-125">将**包括货架**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="66907-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="66907-126">在货架的**格式**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="66907-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="66907-127">将**包括货位**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="66907-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="66907-128">在货架的**格式**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="66907-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="66907-129">定义仓库库位</span><span class="sxs-lookup"><span data-stu-id="66907-129">Define warehouse locations</span></span>
1. <span data-ttu-id="66907-130">在操作窗格上，选择**仓库**。</span><span class="sxs-lookup"><span data-stu-id="66907-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="66907-131">选择**库位向导**。</span><span class="sxs-lookup"><span data-stu-id="66907-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="66907-132">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="66907-132">Select **Next**.</span></span>
4. <span data-ttu-id="66907-133">取消选择**出货台**选项</span><span class="sxs-lookup"><span data-stu-id="66907-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="66907-134">取消选择**堆放库位**选项</span><span class="sxs-lookup"><span data-stu-id="66907-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="66907-135">选择**下一步**，直到用于选择**完成**的选项。</span><span class="sxs-lookup"><span data-stu-id="66907-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="66907-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="66907-136">Close the page.</span></span>
8. <span data-ttu-id="66907-137">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="66907-137">Refresh the page.</span></span>

