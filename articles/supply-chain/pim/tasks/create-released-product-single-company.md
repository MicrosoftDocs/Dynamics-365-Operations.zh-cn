---
title: 创建单个公司的已发布产品
description: 此过程介绍如何在单个法定单位背景下创建单个已发布产品。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9265ee4311ac89ae88ff7dd089519251828b1e3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "315950"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="6269a-103">创建单个公司的已发布产品</span><span class="sxs-lookup"><span data-stu-id="6269a-103">Create a released product for a single company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6269a-104">此过程介绍如何在单个法定单位背景下创建单个已发布产品。</span><span class="sxs-lookup"><span data-stu-id="6269a-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="6269a-105">在创建已发布产品后，其仅立即在该单位中可用。</span><span class="sxs-lookup"><span data-stu-id="6269a-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="6269a-106">您可以使用 USMF 公司演示数据浏览此过程。</span><span class="sxs-lookup"><span data-stu-id="6269a-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="6269a-107">此任务通常由产品设计者执行。</span><span class="sxs-lookup"><span data-stu-id="6269a-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="6269a-108">创建已发布产品</span><span class="sxs-lookup"><span data-stu-id="6269a-108">Create a released product</span></span>
1. <span data-ttu-id="6269a-109">转至“产品发布”。</span><span class="sxs-lookup"><span data-stu-id="6269a-109">Go to Released products.</span></span>
2. <span data-ttu-id="6269a-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6269a-110">Click New.</span></span>
3. <span data-ttu-id="6269a-111">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6269a-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6269a-112">如果没有在“产品编号”字段中自动输入产品编号，则键入唯一的产品编号。</span><span class="sxs-lookup"><span data-stu-id="6269a-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="6269a-113">该步骤只有在还未设置产品编号的编号顺序时才需要。</span><span class="sxs-lookup"><span data-stu-id="6269a-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="6269a-114">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6269a-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="6269a-115">产品名称默认为搜索名称。</span><span class="sxs-lookup"><span data-stu-id="6269a-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="6269a-116">如果需要，您可以选择更改搜索名称。</span><span class="sxs-lookup"><span data-stu-id="6269a-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="6269a-117">在“物料模型组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-118">此物料模型组包含确定在进行物料收货和发货时如何控制和处理物料的设置。</span><span class="sxs-lookup"><span data-stu-id="6269a-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="6269a-119">该设置还确定如何计算物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="6269a-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="6269a-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6269a-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6269a-122">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-123">物料组基于物料特征将库存物料分成不同的组，可用于管理库存。</span><span class="sxs-lookup"><span data-stu-id="6269a-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="6269a-124">例如，若要管理信息如何过帐到主科目，您可以创建与特定的主科目关联的一系列不同物料组。</span><span class="sxs-lookup"><span data-stu-id="6269a-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="6269a-125">这让您能够在不同阶段跟踪物料的库存价值。</span><span class="sxs-lookup"><span data-stu-id="6269a-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="6269a-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6269a-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="6269a-128">在“存储维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-129">存储维度帮助您控制物料存储方式和库存提取方式。</span><span class="sxs-lookup"><span data-stu-id="6269a-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="6269a-130">例如，存储维度可以是站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="6269a-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="6269a-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="6269a-132">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6269a-133">在“跟踪维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-134">跟踪维度组确定可以添加到产品中的跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="6269a-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="6269a-135">例如，批号和序列号用于跟踪库存物料。</span><span class="sxs-lookup"><span data-stu-id="6269a-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="6269a-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="6269a-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="6269a-138">在“库存单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-139">库存单位确定产品在存于库存时如何量化产品。</span><span class="sxs-lookup"><span data-stu-id="6269a-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="6269a-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="6269a-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="6269a-142">在“采购单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-143">采购单位确定从供应商购买产品时如何量化产品。</span><span class="sxs-lookup"><span data-stu-id="6269a-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="6269a-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="6269a-145">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="6269a-146">在“销售单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-147">销售单位确定向客户销售产品时如何量化产品。</span><span class="sxs-lookup"><span data-stu-id="6269a-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="6269a-148">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="6269a-149">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="6269a-150">在“物料清单单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-151">物料清单单位确定在添加产品到物料清单时如何量化产品。</span><span class="sxs-lookup"><span data-stu-id="6269a-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="6269a-152">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="6269a-153">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="6269a-154">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-155">销售税务组中的物料销售税组确定如何计算每个物料的销售税。</span><span class="sxs-lookup"><span data-stu-id="6269a-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="6269a-156">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="6269a-157">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="6269a-158">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6269a-159">采购税务组中的物料销售税组确定如何计算每个物料的采购税。</span><span class="sxs-lookup"><span data-stu-id="6269a-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="6269a-160">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="6269a-161">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="6269a-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6269a-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="6269a-163">添加产品特征。</span><span class="sxs-lookup"><span data-stu-id="6269a-163">Add product characteristics</span></span>
1. <span data-ttu-id="6269a-164">展开或折叠“管理库存”部分。</span><span class="sxs-lookup"><span data-stu-id="6269a-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="6269a-165">在“净重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="6269a-166">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="6269a-167">在“总深度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="6269a-168">在“总宽度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="6269a-169">在“总高度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="6269a-170">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6269a-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="6269a-171">添加财务维度</span><span class="sxs-lookup"><span data-stu-id="6269a-171">Add financial dimensions</span></span>
1. <span data-ttu-id="6269a-172">展开或折叠“财务维度”部分。</span><span class="sxs-lookup"><span data-stu-id="6269a-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="6269a-173">在“业务单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6269a-174">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6269a-175">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6269a-176">在“成本中心”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6269a-177">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6269a-178">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6269a-179">在“部门”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6269a-180">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6269a-181">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="6269a-182">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6269a-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6269a-183">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6269a-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="6269a-184">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6269a-184">In the list, click the link in the selected row.</span></span>

