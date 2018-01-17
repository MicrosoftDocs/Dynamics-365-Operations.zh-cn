---
title: "定义库存盘点流程"
description: "此过程向您介绍，通过创建一个盘点组和盘点日记帐，配置基本存货盘点过程。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: f3610b52fd690b698d50a608c41adfb918930266
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---
# <a name="define-inventory-counting-processes"></a><span data-ttu-id="bfb23-103">定义库存盘点流程</span><span class="sxs-lookup"><span data-stu-id="bfb23-103">Define inventory counting processes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfb23-104">此过程向您介绍，通过创建一个盘点组和盘点日记帐，配置基本存货盘点过程。</span><span class="sxs-lookup"><span data-stu-id="bfb23-104">This procedure walks you through the configuration of basic inventory counting processes by creating a counting group and a counting journal.</span></span> <span data-ttu-id="bfb23-105">它也将向您展示如何在仓库和物料级别启用盘点策略。</span><span class="sxs-lookup"><span data-stu-id="bfb23-105">It also shows you how to enable counting policies on a warehouse and item level.</span></span> <span data-ttu-id="bfb23-106">这些任务通常由仓库主管执行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-106">These tasks would typically be carried out by a warehouse supervisor.</span></span> <span data-ttu-id="bfb23-107">它是某些现有发布产品和仓库的先决条件。</span><span class="sxs-lookup"><span data-stu-id="bfb23-107">It is a prerequisite to have some existing released products and warehouses.</span></span> <span data-ttu-id="bfb23-108">如果您使用演示数据公司，您可以在 USMF 公司中对任何库存物料执行此过程。</span><span class="sxs-lookup"><span data-stu-id="bfb23-108">If you're using a demo data company, you can run this procedure in the USMF company with any stocked item.</span></span>


## <a name="create-a-counting-group"></a><span data-ttu-id="bfb23-109">创建一个盘点组</span><span class="sxs-lookup"><span data-stu-id="bfb23-109">Create a counting group</span></span>
1. <span data-ttu-id="bfb23-110">转到“库存管理”>“设置”>“库存”>“盘点组”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-110">Go to Inventory management > Setup > Inventory > Counting groups.</span></span>
2. <span data-ttu-id="bfb23-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-111">Click New.</span></span>
3. <span data-ttu-id="bfb23-112">在“盘点组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bfb23-112">In the Counting group field, type a value.</span></span>
4. <span data-ttu-id="bfb23-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bfb23-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bfb23-114">在“盘点代码”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="bfb23-114">In the Counting code field, select an option.</span></span>
    * <span data-ttu-id="bfb23-115">手动 – 每次运行作业时包括行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-115">Manual – Includes lines every time you run the job.</span></span> <span data-ttu-id="bfb23-116">换言之，由您决定盘点组的计数间隔。</span><span class="sxs-lookup"><span data-stu-id="bfb23-116">In other words, you decide the counting interval for the counting group.</span></span>  <span data-ttu-id="bfb23-117">期间 – 期间间隔过期时在盘点日志中包括此期间的行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-117">Period – Includes lines for the period in the counting journal when the period interval has expired.</span></span>   <span data-ttu-id="bfb23-118">零库存 – 如果现有库存量变为零 (0)，则在运行作业时在盘点日志中生成行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-118">Zero in stock – If on-hand inventory reaches zero (0), lines are generated in the counting journal when the job is run.</span></span> <span data-ttu-id="bfb23-119">如果一次计数后现有库存量变为 0，则下次开始计数时生成行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-119">If the on-hand inventory reaches 0 after a count, lines are generated the next time that you start the count.</span></span>   <span data-ttu-id="bfb23-120">最小值 – 如果现有库存量等于或低于指定的最小值，则在盘点日志中插入行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-120">Minimum – Inserts lines in the counting journal if the on-hand inventory is equal to or less than the minimum that is specified.</span></span>  
    * <span data-ttu-id="bfb23-121">可选：如果您在“盘点代码”字段中指定了“期间”，则您必须在“盘点期间”字段中键入期间间隔。</span><span class="sxs-lookup"><span data-stu-id="bfb23-121">Optional: If you have specified Period in the Counting code field, you must type the interval for the period in the Counting period field.</span></span> <span data-ttu-id="bfb23-122">间隔单位是天。</span><span class="sxs-lookup"><span data-stu-id="bfb23-122">The unit for intervals is days.</span></span>  
    * <span data-ttu-id="bfb23-123">当您在盘点日记帐创建新行时运行作业，无论您运行同一作业的频率是多少，新行将在“特定的间隔”字段中得到创建。</span><span class="sxs-lookup"><span data-stu-id="bfb23-123">When you run the job for creating new lines in the counting journal, new lines are created at the interval specified in this field, regardless of how often you run the same job.</span></span> <span data-ttu-id="bfb23-124">例如，若盘点期间设置为 7，且盘点日记帐行在 1 月 1 日最终生成，而另一作业在 1 月 5 日开始，并未经过 7 日，因而在该期间间隔内日记帐中不会生成行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-124">For example, if Counting period is set to 7, and journal lines were last generated for a count on January 1, if another job is started on January 5, seven days have not passed and so no lines are generated in the journal for that period interval.</span></span> <span data-ttu-id="bfb23-125">如果您在 1 月 8 日再次开始作业，因为已过 7 天，则在盘点日记帐中能够生成此期间的行。</span><span class="sxs-lookup"><span data-stu-id="bfb23-125">If you start the job again on January 8, lines are generated for the period in the counting journal, because 7 days have passed.</span></span>  
6. <span data-ttu-id="bfb23-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-126">Click Save.</span></span>

## <a name="create-a-counting-journal-name"></a><span data-ttu-id="bfb23-127">创建一个盘点日记帐名称</span><span class="sxs-lookup"><span data-stu-id="bfb23-127">Create a counting journal name</span></span>
1. <span data-ttu-id="bfb23-128">单击“库存管理”>“设置”>“日记帐名称”>“库存”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-128">Go to Inventory management > Setup > Journal names > Inventory.</span></span>
2. <span data-ttu-id="bfb23-129">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-129">Click New.</span></span>
3. <span data-ttu-id="bfb23-130">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bfb23-130">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bfb23-131">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bfb23-131">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bfb23-132">在“日记帐类型”字段中，选择“盘点”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-132">In the Journal type field, select 'Counting'.</span></span>
    * <span data-ttu-id="bfb23-133">可选：当在创建盘点日记帐时，如果您想要为凭证 ID 生成特定的编号规则，您可以选择不同的凭证系列 ID。</span><span class="sxs-lookup"><span data-stu-id="bfb23-133">Optional: you can select a different voucher series ID if you want a specific number sequence for the voucher IDs generated when creating counting journals.</span></span> <span data-ttu-id="bfb23-134">在“编号规则”页设置凭证系列。</span><span class="sxs-lookup"><span data-stu-id="bfb23-134">Voucher series are created in the Number sequences page.</span></span>  
6. <span data-ttu-id="bfb23-135">在“细节级别”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="bfb23-135">In the Detail level field, select an option.</span></span>
    * <span data-ttu-id="bfb23-136">在日记帐过帐时，应用的合计级别。</span><span class="sxs-lookup"><span data-stu-id="bfb23-136">This is the level of detail that is applied when the journal is posted.</span></span>  
    * <span data-ttu-id="bfb23-137">可选：您可以更改“预留”字段中的值。</span><span class="sxs-lookup"><span data-stu-id="bfb23-137">Optional: you can change the value in the Reservation field.</span></span> <span data-ttu-id="bfb23-138">这就是在盘点期间，预留物料的方法。</span><span class="sxs-lookup"><span data-stu-id="bfb23-138">This is the method used to reserve items during counting.</span></span>   
    * <span data-ttu-id="bfb23-139">手动 - 物料应在“预留”窗体中手动预留。</span><span class="sxs-lookup"><span data-stu-id="bfb23-139">Manual – The items are reserved manually in the Reservation form.</span></span>   <span data-ttu-id="bfb23-140">自动 - 订单数量将从物料的可用、现有库存量中保留。</span><span class="sxs-lookup"><span data-stu-id="bfb23-140">Automatic – The order quantity is reserved from the available, on-hand inventory for the item.</span></span>   <span data-ttu-id="bfb23-141"> 分解 - 预留为交易主计划的一部分。</span><span class="sxs-lookup"><span data-stu-id="bfb23-141">Explosion – The reservation is part of the master planning of the transaction.</span></span>  
7. <span data-ttu-id="bfb23-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-142">Click Save.</span></span>

## <a name="set-standard-counting-journal-name"></a><span data-ttu-id="bfb23-143">设置标准盘点日记帐名称</span><span class="sxs-lookup"><span data-stu-id="bfb23-143">Set standard counting journal name</span></span>
1. <span data-ttu-id="bfb23-144">转到“库存管理”>“设置”>“库存和仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-144">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="bfb23-145">单击“日记帐”选项卡。</span><span class="sxs-lookup"><span data-stu-id="bfb23-145">Click the Journals tab.</span></span>
3. <span data-ttu-id="bfb23-146">在“盘点”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="bfb23-146">In the Counting field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bfb23-147">选择您之前创建的日记帐。</span><span class="sxs-lookup"><span data-stu-id="bfb23-147">Select the journal you previously created.</span></span>
    * <span data-ttu-id="bfb23-148">该日记帐将为“盘点类型”的库存日记帐的默认日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="bfb23-148">This journal will then be the default journal name for inventory journals of the Counting type.</span></span>  
5. <span data-ttu-id="bfb23-149">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="bfb23-149">Click the General tab.</span></span>
    * <span data-ttu-id="bfb23-150">可选：选择此选项以在盘点过程中锁定某物料，以避免更新装箱单、领料单或进行领料单登记等。</span><span class="sxs-lookup"><span data-stu-id="bfb23-150">Optional: Select this option to lock an item during the counting process to prevent updates for packing slips, picking lists, or picking list registrations.</span></span>  

## <a name="set-the-counting-policy-for-an-item"></a><span data-ttu-id="bfb23-151">设置物料的盘点策略</span><span class="sxs-lookup"><span data-stu-id="bfb23-151">Set the counting policy for an item</span></span>
1. <span data-ttu-id="bfb23-152">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-152">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="bfb23-153">在该列表中，单击您想为其设置盘点策略产品的物料编号的链接。</span><span class="sxs-lookup"><span data-stu-id="bfb23-153">In the list, click on the link for the Item number of the product that you want to set counting policies on.</span></span>
    * <span data-ttu-id="bfb23-154">请注意：您需要选择进行库存跟踪的物料。</span><span class="sxs-lookup"><span data-stu-id="bfb23-154">Note that you need to select an item that is inventory tracked.</span></span> <span data-ttu-id="bfb23-155">不能盘点非库存产品。</span><span class="sxs-lookup"><span data-stu-id="bfb23-155">A non-stocked product can't be counted.</span></span> <span data-ttu-id="bfb23-156">如果您正使用 USMF 演示数据，您可以选择物料 A0001。</span><span class="sxs-lookup"><span data-stu-id="bfb23-156">If you are using USMF demo data you can select item A0001.</span></span>  
3. <span data-ttu-id="bfb23-157">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-157">Click Edit.</span></span>
4. <span data-ttu-id="bfb23-158">切换“库存管理”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="bfb23-158">Toggle the expansion of the Manage inventory section.</span></span>
5. <span data-ttu-id="bfb23-159">在“盘点组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="bfb23-159">In the Counting group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bfb23-160">在该列表中，单击您之前创建的盘点组。</span><span class="sxs-lookup"><span data-stu-id="bfb23-160">In the list, click on the counting group you previously created.</span></span>
    * <span data-ttu-id="bfb23-161">此产品将包含在使用此盘点组创建库存盘点日记帐行之中。</span><span class="sxs-lookup"><span data-stu-id="bfb23-161">This product will now be included when inventory counting journal lines are created using this counting group.</span></span>  
7. <span data-ttu-id="bfb23-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-162">Click Save.</span></span>

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a><span data-ttu-id="bfb23-163">为特定仓库中的物料设置盘点策略</span><span class="sxs-lookup"><span data-stu-id="bfb23-163">Set the counting policy for an item in a specific warehouse</span></span>
1. <span data-ttu-id="bfb23-164">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-164">On the Action Pane, click Manage inventory.</span></span>
2. <span data-ttu-id="bfb23-165">单击“仓库物料”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-165">Click Warehouse items.</span></span>
3. <span data-ttu-id="bfb23-166">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-166">Click New.</span></span>
4. <span data-ttu-id="bfb23-167">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="bfb23-167">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bfb23-168">在该列表中，选择您想设置特定盘点的策略的仓库。</span><span class="sxs-lookup"><span data-stu-id="bfb23-168">In the list, select the warehouse you want set up specific counting policies for.</span></span>
6. <span data-ttu-id="bfb23-169">在“盘点组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="bfb23-169">In the Counting group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bfb23-170">在列表中，选择一个盘点组。</span><span class="sxs-lookup"><span data-stu-id="bfb23-170">In the list, select a counting group</span></span>
    * <span data-ttu-id="bfb23-171">您可以选择一个应用于您所选择的特定仓库的物料的特定盘点组。</span><span class="sxs-lookup"><span data-stu-id="bfb23-171">Here you can select a specific counting group that should apply to the item in the specific warehouse you have selected.</span></span> <span data-ttu-id="bfb23-172">在该仓库执行盘点时，此盘点策略将覆盖物料的常规盘点策略。</span><span class="sxs-lookup"><span data-stu-id="bfb23-172">When counting is performed in that warehouse, this counting policy will override the general counting policy for the item.</span></span>  
8. <span data-ttu-id="bfb23-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bfb23-173">Click Save.</span></span>

