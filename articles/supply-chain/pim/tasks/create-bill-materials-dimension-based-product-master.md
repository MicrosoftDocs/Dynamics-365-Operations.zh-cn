---
title: 创建基于维度的基础产品的物料清单
description: 对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: acac36a1078e3f45f59989e62accbc63d596cc26
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209275"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="44220-103">创建基于维度的基础产品的物料清单</span><span class="sxs-lookup"><span data-stu-id="44220-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44220-104">对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。</span><span class="sxs-lookup"><span data-stu-id="44220-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="44220-105">前 4 个记录设置完成此过程需要的数据。</span><span class="sxs-lookup"><span data-stu-id="44220-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="44220-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="44220-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="44220-107">此任务通常由产品设计器处理。</span><span class="sxs-lookup"><span data-stu-id="44220-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="44220-108">选择产品</span><span class="sxs-lookup"><span data-stu-id="44220-108">Select the product</span></span>
1. <span data-ttu-id="44220-109">单击“已发布产品的维护”。</span><span class="sxs-lookup"><span data-stu-id="44220-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="44220-110">单击“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="44220-110">Click Released products.</span></span>
3. <span data-ttu-id="44220-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="44220-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="44220-112">使用您以此顺序在第一个任务指南中创建的基于维度的配置技术查找发布的基础产品。</span><span class="sxs-lookup"><span data-stu-id="44220-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="44220-113">在“操作”窗格上，单击“设计”。</span><span class="sxs-lookup"><span data-stu-id="44220-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="44220-114">单击“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="44220-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="44220-115">创建新的物料清单和物料清单版本</span><span class="sxs-lookup"><span data-stu-id="44220-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="44220-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44220-116">Click New.</span></span>
2. <span data-ttu-id="44220-117">单击“物料清单”和“物料清单版本”。</span><span class="sxs-lookup"><span data-stu-id="44220-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="44220-118">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="44220-119">设置站点</span><span class="sxs-lookup"><span data-stu-id="44220-119">Setting a site</span></span>  
    * <span data-ttu-id="44220-120">在此过程中，我们不设置物料清单的特定站点。</span><span class="sxs-lookup"><span data-stu-id="44220-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="44220-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="44220-121">Click OK.</span></span>
5. <span data-ttu-id="44220-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44220-122">Click New.</span></span>
    * <span data-ttu-id="44220-123">在此过程中，我们将添加四行到物料清单。</span><span class="sxs-lookup"><span data-stu-id="44220-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="44220-124">两行表示电缆选项，两行表示机柜选项。</span><span class="sxs-lookup"><span data-stu-id="44220-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="44220-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="44220-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="44220-126">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-127">选择物料编号 A0001，HDMI 6' 电缆。</span><span class="sxs-lookup"><span data-stu-id="44220-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="44220-128">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-129">选择以此顺序在指南 4 中创建的电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="44220-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="44220-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44220-130">Click New.</span></span>
    * <span data-ttu-id="44220-131">选择物料编号 A0002，HDMI 12' 电缆。</span><span class="sxs-lookup"><span data-stu-id="44220-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="44220-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="44220-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="44220-133">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="44220-134">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-135">再次选择电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="44220-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="44220-136">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44220-136">Click New.</span></span>
14. <span data-ttu-id="44220-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="44220-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="44220-138">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-139">选择物料编号 D0002 机柜。</span><span class="sxs-lookup"><span data-stu-id="44220-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="44220-140">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-141">选择此物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="44220-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="44220-142">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="44220-142">Click New.</span></span>
18. <span data-ttu-id="44220-143">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="44220-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="44220-144">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-145">选择物料编号 M0007 StandardCabinet 作为最后的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="44220-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="44220-146">在“配置组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="44220-147">选择最后物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="44220-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="44220-148">审核并启用</span><span class="sxs-lookup"><span data-stu-id="44220-148">Approve and activate</span></span>
1. <span data-ttu-id="44220-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="44220-149">Close the page.</span></span>
2. <span data-ttu-id="44220-150">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="44220-150">Click Approve.</span></span>
3. <span data-ttu-id="44220-151">在“已审核”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="44220-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="44220-152">在“是否还要审核该物料清单？”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="44220-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="44220-153">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="44220-153">Click OK.</span></span>
6. <span data-ttu-id="44220-154">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="44220-154">Click Activate.</span></span>

