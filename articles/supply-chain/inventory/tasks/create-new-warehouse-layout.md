---
title: "创建新仓库布局"
description: "该程序将向您说明如何设置有关仓库库位的信息。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="672a5-103">创建新仓库布局</span><span class="sxs-lookup"><span data-stu-id="672a5-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="672a5-104">该程序将向您说明如何设置有关仓库库位的信息。</span><span class="sxs-lookup"><span data-stu-id="672a5-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="672a5-105">此程序仅适用于仓库中“库存管理模块”的“基本仓储”，不适用于“仓库管理模块”。</span><span class="sxs-lookup"><span data-stu-id="672a5-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="672a5-106">您可以使用演示数据公司 USMF 或您自己的数据使用该程序。</span><span class="sxs-lookup"><span data-stu-id="672a5-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="672a5-107">设置默认库位容量</span><span class="sxs-lookup"><span data-stu-id="672a5-107">Set the default location capacity</span></span>
1. <span data-ttu-id="672a5-108">转到“库存管理”>“设置”>“库存和仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="672a5-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="672a5-109">单击“库位”选项卡。</span><span class="sxs-lookup"><span data-stu-id="672a5-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="672a5-110">在“标准宽度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="672a5-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="672a5-111">在“标准深度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="672a5-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="672a5-112">在“标准高度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="672a5-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="672a5-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="672a5-113">Click Save.</span></span>
7. <span data-ttu-id="672a5-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="672a5-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="672a5-115">定义库位名称格式</span><span class="sxs-lookup"><span data-stu-id="672a5-115">Define the location name format</span></span>
1. <span data-ttu-id="672a5-116">转到库存管理 > 设置 > 库存细分 > 仓库。</span><span class="sxs-lookup"><span data-stu-id="672a5-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="672a5-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="672a5-117">Click New.</span></span>
3. <span data-ttu-id="672a5-118">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="672a5-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="672a5-119">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="672a5-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="672a5-120">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="672a5-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="672a5-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="672a5-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="672a5-122">切换到“库位名称”部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="672a5-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="672a5-123">此部分中的选项定义库位名称的默认格式。</span><span class="sxs-lookup"><span data-stu-id="672a5-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="672a5-124">在我们的示例中，我们增加了通道编号、货架编号和货位编号。</span><span class="sxs-lookup"><span data-stu-id="672a5-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="672a5-125">将“包括通道”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="672a5-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="672a5-126">将“包括货架”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="672a5-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="672a5-127">在货架的“格式”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="672a5-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="672a5-128">例如：-##</span><span class="sxs-lookup"><span data-stu-id="672a5-128">For example: -##</span></span>  
11. <span data-ttu-id="672a5-129">将“包括货位”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="672a5-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="672a5-130">在货架的“格式”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="672a5-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="672a5-131">例如：-##</span><span class="sxs-lookup"><span data-stu-id="672a5-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="672a5-132">定义仓库库位</span><span class="sxs-lookup"><span data-stu-id="672a5-132">Define warehouse locations</span></span>
1. <span data-ttu-id="672a5-133">在“操作窗格”中，单击“仓库”。</span><span class="sxs-lookup"><span data-stu-id="672a5-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="672a5-134">单击“库位向导”。</span><span class="sxs-lookup"><span data-stu-id="672a5-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="672a5-135">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-135">Click Next.</span></span>
4. <span data-ttu-id="672a5-136">取消选择“出货台”选项</span><span class="sxs-lookup"><span data-stu-id="672a5-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="672a5-137">取消选择“堆放库位”选项</span><span class="sxs-lookup"><span data-stu-id="672a5-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="672a5-138">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-138">Click Next.</span></span>
7. <span data-ttu-id="672a5-139">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-139">Click Next.</span></span>
8. <span data-ttu-id="672a5-140">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-140">Click Next.</span></span>
9. <span data-ttu-id="672a5-141">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-141">Click Next.</span></span>
10. <span data-ttu-id="672a5-142">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-142">Click Next.</span></span>
11. <span data-ttu-id="672a5-143">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-143">Click Next.</span></span>
12. <span data-ttu-id="672a5-144">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-144">Click Next.</span></span>
    * <span data-ttu-id="672a5-145">请注意在此页上显示的物理维度是您在启动该程序时所设置的。</span><span class="sxs-lookup"><span data-stu-id="672a5-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="672a5-146">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="672a5-146">Click Next.</span></span>
14. <span data-ttu-id="672a5-147">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="672a5-147">Click Finish.</span></span>
15. <span data-ttu-id="672a5-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="672a5-148">Close the page.</span></span>
16. <span data-ttu-id="672a5-149">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="672a5-149">Refresh the page.</span></span>

