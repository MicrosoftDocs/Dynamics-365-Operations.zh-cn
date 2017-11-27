--- 
title: "创建基于维度的基础产品的物料清单"
description: "对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8b5432addd1dd79a64dcbb751a59cf3084a63ab1
ms.openlocfilehash: 05837c2b21957133729074f614a6d3d7b7c08dad
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="f1eea-103">创建基于维度的基础产品的物料清单</span><span class="sxs-lookup"><span data-stu-id="f1eea-103">Create a bill of materials for a dimension-based product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1eea-104">对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。</span><span class="sxs-lookup"><span data-stu-id="f1eea-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="f1eea-105">前 4 个记录设置完成此过程需要的数据。</span><span class="sxs-lookup"><span data-stu-id="f1eea-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="f1eea-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f1eea-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f1eea-107">此任务通常由产品设计器处理。</span><span class="sxs-lookup"><span data-stu-id="f1eea-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="f1eea-108">选择产品</span><span class="sxs-lookup"><span data-stu-id="f1eea-108">Select the product</span></span>
1. <span data-ttu-id="f1eea-109">单击“已发布产品的维护”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="f1eea-110">单击“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-110">Click Released products.</span></span>
3. <span data-ttu-id="f1eea-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f1eea-112">使用您以此顺序在第一个任务指南中创建的基于维度的配置技术查找发布的基础产品。</span><span class="sxs-lookup"><span data-stu-id="f1eea-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="f1eea-113">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="f1eea-114">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="f1eea-115">创建新的物料清单和物料清单版本</span><span class="sxs-lookup"><span data-stu-id="f1eea-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="f1eea-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-116">Click New.</span></span>
2. <span data-ttu-id="f1eea-117">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="f1eea-118">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f1eea-119">设置站点</span><span class="sxs-lookup"><span data-stu-id="f1eea-119">Setting a site</span></span>  
    * <span data-ttu-id="f1eea-120">在此过程中，我们不设置物料清单的特定站点。</span><span class="sxs-lookup"><span data-stu-id="f1eea-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="f1eea-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-121">Click OK.</span></span>
5. <span data-ttu-id="f1eea-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-122">Click New.</span></span>
    * <span data-ttu-id="f1eea-123">在此过程中，我们将添加四行到物料清单。</span><span class="sxs-lookup"><span data-stu-id="f1eea-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="f1eea-124">两行表示电缆选项，两行表示机柜选项。</span><span class="sxs-lookup"><span data-stu-id="f1eea-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="f1eea-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f1eea-126">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-127">选择物料编号 A0001，HDMI 6' 电缆。</span><span class="sxs-lookup"><span data-stu-id="f1eea-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="f1eea-128">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-129">选择以此顺序在指南 4 中创建的电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="f1eea-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="f1eea-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-130">Click New.</span></span>
    * <span data-ttu-id="f1eea-131">选择物料编号 A0002，HDMI 12' 电缆。</span><span class="sxs-lookup"><span data-stu-id="f1eea-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="f1eea-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f1eea-133">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f1eea-134">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-135">再次选择电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="f1eea-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="f1eea-136">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-136">Click New.</span></span>
14. <span data-ttu-id="f1eea-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="f1eea-138">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-139">选择物料编号 D0002 机柜。</span><span class="sxs-lookup"><span data-stu-id="f1eea-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="f1eea-140">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-141">选择此物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="f1eea-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="f1eea-142">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-142">Click New.</span></span>
18. <span data-ttu-id="f1eea-143">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f1eea-144">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-145">选择物料编号 M0007 StandardCabinet 作为最后的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="f1eea-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="f1eea-146">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1eea-147">选择最后物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="f1eea-147">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="f1eea-148">审核并启用</span><span class="sxs-lookup"><span data-stu-id="f1eea-148">Approve and activate</span></span>
1. <span data-ttu-id="f1eea-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f1eea-149">Close the page.</span></span>
2. <span data-ttu-id="f1eea-150">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-150">Click Approve.</span></span>
3. <span data-ttu-id="f1eea-151">在“已审核”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1eea-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="f1eea-152">在“是否还要审核该物料清单？”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="f1eea-153">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-153">Click OK.</span></span>
6. <span data-ttu-id="f1eea-154">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="f1eea-154">Click Activate.</span></span>


