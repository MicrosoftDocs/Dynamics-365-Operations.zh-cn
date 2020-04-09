---
title: 创建 lean manufacturing 的转包工作单元
description: 若要为 lean manufacturing 的转包工作建模，必须创建与提供该工作的供应商关联的工作单元。
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03fcc62236b14a8721a4cb611978e8672ae77ea3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146920"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="21d35-103">创建 lean manufacturing 的转包工作单元</span><span class="sxs-lookup"><span data-stu-id="21d35-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21d35-104">若要为 lean manufacturing 的转包工作建模，必须创建与提供该工作的供应商关联的工作单元。</span><span class="sxs-lookup"><span data-stu-id="21d35-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="21d35-105">转包工作单元通过关联供应商类型的资源链接到供应商。</span><span class="sxs-lookup"><span data-stu-id="21d35-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="21d35-106">如果在 USMF 演示公司播放此录制，可以选择供应商帐户 ID 1002 和站点 1。</span><span class="sxs-lookup"><span data-stu-id="21d35-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="21d35-107">创建供应商资源</span><span class="sxs-lookup"><span data-stu-id="21d35-107">Create a vendor resource</span></span>
1. <span data-ttu-id="21d35-108">转到“资源”。</span><span class="sxs-lookup"><span data-stu-id="21d35-108">Go to Resources.</span></span>
2. <span data-ttu-id="21d35-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="21d35-109">Click New.</span></span>
3. <span data-ttu-id="21d35-110">在“资源”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="21d35-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="21d35-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="21d35-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21d35-112">在“类型”字段中选择“供应商”。</span><span class="sxs-lookup"><span data-stu-id="21d35-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="21d35-113">在“供应商”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="21d35-114">创建资源组</span><span class="sxs-lookup"><span data-stu-id="21d35-114">Create the resource group</span></span>
1. <span data-ttu-id="21d35-115">转到“资源组”。</span><span class="sxs-lookup"><span data-stu-id="21d35-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="21d35-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="21d35-116">Click New.</span></span>
3. <span data-ttu-id="21d35-117">在“资源组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="21d35-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="21d35-118">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="21d35-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21d35-119">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="21d35-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21d35-120">选择应将工作单元分配给的站点。</span><span class="sxs-lookup"><span data-stu-id="21d35-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="21d35-121">理论上，站点可以表示由供应商运营的一个站点。</span><span class="sxs-lookup"><span data-stu-id="21d35-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="21d35-122">但是在大多数情况下，转包资源仅分配给订购转包工作的站点。</span><span class="sxs-lookup"><span data-stu-id="21d35-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="21d35-123">请注意，转包工作单元的输入和输出仓库必须在同一个站点。</span><span class="sxs-lookup"><span data-stu-id="21d35-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="21d35-124">在“站点”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="21d35-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="21d35-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="21d35-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="21d35-126">选中或清除“工作单元”复选框。</span><span class="sxs-lookup"><span data-stu-id="21d35-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="21d35-127">在“输入仓库”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21d35-128">选择用于为供应商管理的工作单元暂存材料的仓库和库位。</span><span class="sxs-lookup"><span data-stu-id="21d35-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="21d35-129">许多情况下，通过为每个供应商使用一个单独的仓库和每个工作单元使用一个库位，为仓库和库位建模。</span><span class="sxs-lookup"><span data-stu-id="21d35-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="21d35-130">在“输入位置”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="21d35-131">在“输出仓库”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21d35-132">定义过帐工作单元的转包活动时过帐材料的仓库和库位。</span><span class="sxs-lookup"><span data-stu-id="21d35-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="21d35-133">如果供应商报告看板作业，仓库和库位可以在供应商站点。</span><span class="sxs-lookup"><span data-stu-id="21d35-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="21d35-134">仓库和库位也可以在与生产流下一步关联的收货库位。</span><span class="sxs-lookup"><span data-stu-id="21d35-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="21d35-135">在“输出位置”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="21d35-136">展开或折叠“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="21d35-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="21d35-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="21d35-137">Click Add.</span></span>
15. <span data-ttu-id="21d35-138">在“日历”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21d35-139">将工作单元的工作时间日历与资源组关联。</span><span class="sxs-lookup"><span data-stu-id="21d35-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="21d35-140">对于关键资源，我们建议您定义用于表示工作单元或供应商站点的确切工作时间和相关产能的特定日历。</span><span class="sxs-lookup"><span data-stu-id="21d35-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="21d35-141">展开或折叠“资源”部分。</span><span class="sxs-lookup"><span data-stu-id="21d35-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="21d35-142">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="21d35-142">Click Add.</span></span>
    * <span data-ttu-id="21d35-143">转包资源组必须有供应商类型的关联资源，用于将资源组链接到供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="21d35-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="21d35-144">在“资源”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21d35-145">选择或收入您在先前的子任务中创建的供应商资源。</span><span class="sxs-lookup"><span data-stu-id="21d35-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="21d35-146">展开或折叠“工作单元产能”部分。</span><span class="sxs-lookup"><span data-stu-id="21d35-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="21d35-147">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="21d35-147">Click Add.</span></span>
    * <span data-ttu-id="21d35-148">必须为工作单元定义产能。</span><span class="sxs-lookup"><span data-stu-id="21d35-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="21d35-149">在此示例中，我们创建的吞吐量产能为每个标准工作日 100 件。</span><span class="sxs-lookup"><span data-stu-id="21d35-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="21d35-150">在“生产流模型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="21d35-151">在“产能期间”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="21d35-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="21d35-152">在“平均吞吐量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="21d35-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="21d35-153">在“单位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="21d35-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="21d35-154">ResolveChanges 单位。</span><span class="sxs-lookup"><span data-stu-id="21d35-154">ResolveChanges the Unit.</span></span>

