---
title: 定义库存盘点流程
description: 此主题介绍如何通过创建一个盘点组和盘点日记帐来配置基本存货盘点过程。
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df5db0e71f550e82820e15b1597d9e287071f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423261"
---
# <a name="define-inventory-counting-processes"></a><span data-ttu-id="a0cdc-103">定义库存盘点流程</span><span class="sxs-lookup"><span data-stu-id="a0cdc-103">Define inventory counting processes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0cdc-104">此主题介绍如何通过创建一个盘点组和盘点日记帐来配置基本存货盘点过程。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-104">This topic describes the configuration of basic inventory counting processes by creating a counting group and a counting journal.</span></span> <span data-ttu-id="a0cdc-105">它也将向您展示如何在仓库和物料级别启用盘点策略。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-105">It also shows you how to enable counting policies on a warehouse and item level.</span></span> <span data-ttu-id="a0cdc-106">这些任务通常由仓库主管执行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-106">These tasks would typically be carried out by a warehouse supervisor.</span></span> <span data-ttu-id="a0cdc-107">它是某些现有发布产品和仓库的先决条件。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-107">It is a prerequisite to have some existing released products and warehouses.</span></span> <span data-ttu-id="a0cdc-108">如果您使用演示数据公司，您可以在 USMF 公司中对任何库存物料执行此过程。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-108">If you're using a demo data company, you can run this procedure in the USMF company with any stocked item.</span></span>


## <a name="create-a-counting-group"></a><span data-ttu-id="a0cdc-109">创建一个盘点组</span><span class="sxs-lookup"><span data-stu-id="a0cdc-109">Create a counting group</span></span>
1. <span data-ttu-id="a0cdc-110">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 库存 > 盘点组**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-110">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory > Counting groups**.</span></span>
2. <span data-ttu-id="a0cdc-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-111">Select **New**.</span></span>
3. <span data-ttu-id="a0cdc-112">在新行的 **盘点组** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-112">In the **Counting group** field of the new row, type a value.</span></span>
4. <span data-ttu-id="a0cdc-113">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-113">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a0cdc-114">在 **盘点代码** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-114">In the **Counting code** field, select an option.</span></span>

    - <span data-ttu-id="a0cdc-115">**手动** – 每次运行作业时包括行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-115">**Manual** – Includes lines every time you run the job.</span></span> <span data-ttu-id="a0cdc-116">换言之，由您决定盘点组的计数间隔。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-116">In other words, you decide the counting interval for the counting group.</span></span>  
    - <span data-ttu-id="a0cdc-117">**期间** – 期间间隔过期时在盘点日志中包括此期间的行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-117">**Period** – Includes lines for the period in the counting journal when the period interval has expired.</span></span>  
    - <span data-ttu-id="a0cdc-118">**零库存** – 如果现有库存量变为零 (0)，则在运行作业时在盘点日志中生成行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-118">**Zero in stock** – If on-hand inventory reaches zero (0), lines are generated in the counting journal when the job is run.</span></span> <span data-ttu-id="a0cdc-119">如果一次计数后现有库存量变为 0，则下次开始计数时生成行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-119">If the on-hand inventory reaches 0 after a count, lines are generated the next time that you start the count.</span></span>  
    - <span data-ttu-id="a0cdc-120">**最小值** – 如果现有库存量等于或低于指定的最小值，则在盘点日志中插入行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-120">**Minimum** – Inserts lines in the counting journal if the on-hand inventory is equal to or less than the minimum that is specified.</span></span>  
    - <span data-ttu-id="a0cdc-121">可选：如果您在 **盘点代码** 字段中指定了 **期间**，则您必须在 **盘点期间** 字段中键入期间间隔。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-121">Optional: If you have specified **Period** in the **Counting code** field, you must type the interval for the period in the **Counting period** field.</span></span> <span data-ttu-id="a0cdc-122">间隔单位是天。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-122">The unit for intervals is days.</span></span>  
    - <span data-ttu-id="a0cdc-123">当您在盘点日记帐创建新行时运行作业，无论您运行同一作业的频率是多少，新行将在“特定的间隔”字段中得到创建。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-123">When you run the job for creating new lines in the counting journal, new lines are created at the interval specified in this field, regardless of how often you run the same job.</span></span> <span data-ttu-id="a0cdc-124">例如，若 **盘点期间** 设置为 7，且盘点日记帐行在 1 月 1 日最终生成，而另一作业在 1 月 5 日开始，并未经过 7 日，因而在该期间间隔内日记帐中不会生成行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-124">For example, if **Counting period** is set to 7, and journal lines were last generated for a count on January 1, if another job is started on January 5, seven days have not passed and so no lines are generated in the journal for that period interval.</span></span> <span data-ttu-id="a0cdc-125">如果您在 1 月 8 日再次开始作业，因为已过 7 天，则在盘点日记帐中能够生成此期间的行。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-125">If you start the job again on January 8, lines are generated for the period in the counting journal, because 7 days have passed.</span></span>  

6. <span data-ttu-id="a0cdc-126">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-126">Select **Save**.</span></span>

## <a name="create-a-counting-journal-name"></a><span data-ttu-id="a0cdc-127">创建一个盘点日记帐名称</span><span class="sxs-lookup"><span data-stu-id="a0cdc-127">Create a counting journal name</span></span>
1. <span data-ttu-id="a0cdc-128">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 日记帐名称 > 库存**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-128">In the navigation pane, go to **Modules > Inventory management > Setup > Journal names > Inventory**.</span></span>
2. <span data-ttu-id="a0cdc-129">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-129">Select **New**.</span></span>
3. <span data-ttu-id="a0cdc-130">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-130">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a0cdc-131">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a0cdc-132">在 **日记帐类型** 字段中，选择 **盘点**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-132">In the **Journal type** field, select **Counting**.</span></span> <span data-ttu-id="a0cdc-133">可选：当在创建盘点日记帐时，如果您想要为凭证 ID 生成特定的编号规则，您可以选择不同的凭证系列 ID。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-133">Optional: you can select a different voucher series ID if you want a specific number sequence for the voucher IDs generated when creating counting journals.</span></span> <span data-ttu-id="a0cdc-134">在 **编号规则** 页设置凭证系列。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-134">Voucher series are created in the **Number sequences** page.</span></span>  
6. <span data-ttu-id="a0cdc-135">在 **详细程度** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-135">In the **Detail level** field, select an option.</span></span>  

    - <span data-ttu-id="a0cdc-136">在日记帐过帐时，应用的合计级别。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-136">This is the level of detail that is applied when the journal is posted.</span></span>  
    - <span data-ttu-id="a0cdc-137">可选：您可以更改“预留”字段中的值。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-137">Optional: you can change the value in the Reservation field.</span></span> <span data-ttu-id="a0cdc-138">这就是在盘点期间，预留物料的方法。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-138">This is the method used to reserve items during counting.</span></span>   
    - <span data-ttu-id="a0cdc-139">**手动** - 物料应在“预留”窗体中手动预留。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-139">**Manual** – The items are reserved manually in the Reservation form.</span></span>  
    - <span data-ttu-id="a0cdc-140">**自动** - 订单数量将从物料的可用、现有库存量中保留。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-140">**Automatic** – The order quantity is reserved from the available, on-hand inventory for the item.</span></span>   
    - <span data-ttu-id="a0cdc-141">**分解** - 预留为交易主计划的一部分。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-141">**Explosion** – The reservation is part of the master planning of the transaction.</span></span>  

7. <span data-ttu-id="a0cdc-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-142">Select **Save**.</span></span>

## <a name="set-standard-counting-journal-name"></a><span data-ttu-id="a0cdc-143">设置标准盘点日记帐名称</span><span class="sxs-lookup"><span data-stu-id="a0cdc-143">Set standard counting journal name</span></span>
1. <span data-ttu-id="a0cdc-144">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-144">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="a0cdc-145">选择 **日记帐** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-145">Select the **Journals** tab.</span></span>
3. <span data-ttu-id="a0cdc-146">在 **盘点** 字段的下拉菜单中，选择之前创建的日记帐。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-146">In the drop down menu of the **Counting** field, select the journal you previously created.</span></span> <span data-ttu-id="a0cdc-147">该日记帐将为 **盘点** 类型的库存日记帐的默认日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-147">This journal will then be the default journal name for inventory journals of the **Counting** type.</span></span>  
4. <span data-ttu-id="a0cdc-148">选择 **常规** 选项卡。可选：选择此选项以在盘点过程中锁定某物料，以避免更新装箱单、领料单或进行领料单登记等。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-148">Select the **General** tab. Optional: Select this option to lock an item during the counting process to prevent updates for packing slips, picking lists, or picking list registrations.</span></span>  

## <a name="set-the-counting-policy-for-an-item"></a><span data-ttu-id="a0cdc-149">设置物料的盘点策略</span><span class="sxs-lookup"><span data-stu-id="a0cdc-149">Set the counting policy for an item</span></span>
1. <span data-ttu-id="a0cdc-150">在导航窗格中，转到 **模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-150">In the navigation pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="a0cdc-151">在该列表中，选择您想为其设置盘点策略产品的物料编号的链接。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-151">In the list, select the link for the Item number of the product that you want to set counting policies on.</span></span> <span data-ttu-id="a0cdc-152">必须选择要对其进行库存跟踪的物料。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-152">You must select an item that is inventory tracked.</span></span> <span data-ttu-id="a0cdc-153">不能盘点非库存产品。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-153">A non-stocked product can't be counted.</span></span> <span data-ttu-id="a0cdc-154">如果您正使用 USMF 演示数据，您可以选择物料 A0001。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-154">If you are using USMF demo data you can select item A0001.</span></span>  
3. <span data-ttu-id="a0cdc-155">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-155">Select **Edit**.</span></span>
4. <span data-ttu-id="a0cdc-156">切换 **库存管理** 部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-156">Toggle the expansion of the **Manage inventory** section.</span></span>
5. <span data-ttu-id="a0cdc-157">在 **盘点组** 字段的下拉菜单中，选择之前创建的盘点组。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-157">In the drop-down menu of the **Counting group** field, select the counting group you previously created.</span></span> <span data-ttu-id="a0cdc-158">此产品将包含在使用此盘点组创建库存盘点日记帐行之中。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-158">This product will now be included when inventory counting journal lines are created using this counting group.</span></span>  
6. <span data-ttu-id="a0cdc-159">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-159">Select **Save**.</span></span>

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a><span data-ttu-id="a0cdc-160">为特定仓库中的物料设置盘点策略</span><span class="sxs-lookup"><span data-stu-id="a0cdc-160">Set the counting policy for an item in a specific warehouse</span></span>
1. <span data-ttu-id="a0cdc-161">在操作窗格上，选择 **库存管理**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-161">On the Action Pane, select **Manage inventory**.</span></span>
2. <span data-ttu-id="a0cdc-162">选择 **仓库物料**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-162">Select **Warehouse items**.</span></span>
3. <span data-ttu-id="a0cdc-163">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-163">Select **New**.</span></span>
4. <span data-ttu-id="a0cdc-164">在 **仓库** 字段的下拉菜单中，选择要为其设置特定盘点策略的仓库。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-164">In the drop-down menu of the **Warehouse** field, select the warehouse you want to set up specific counting policies for.</span></span>
5. <span data-ttu-id="a0cdc-165">在 **盘点组** 字段的下拉菜单中，选择盘点组。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-165">In the drop-down menu of the **Counting group** field, select a counting group.</span></span> <span data-ttu-id="a0cdc-166">您可以选择一个应用于您所选择的特定仓库的物料的特定盘点组。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-166">You can select a specific counting group that should apply to the item in the specific warehouse you have selected.</span></span> <span data-ttu-id="a0cdc-167">在该仓库执行盘点时，此盘点策略将覆盖物料的常规盘点策略。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-167">When counting is performed in that warehouse, this counting policy will override the general counting policy for the item.</span></span>  
6. <span data-ttu-id="a0cdc-168">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a0cdc-168">Select **Save**.</span></span>

