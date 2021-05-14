---
title: 创建和处理不符合项
description: 此主题介绍如何执行不符合项管理，基于现有的质检订单。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956198"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="d6783-103">创建和处理不符合项</span><span class="sxs-lookup"><span data-stu-id="d6783-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6783-104">此主题介绍如何执行不符合项管理，基于现有的质检订单。</span><span class="sxs-lookup"><span data-stu-id="d6783-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="d6783-105">通常，不符合项管理由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="d6783-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="d6783-106">先决条件是，您必须有可用的质检订单。</span><span class="sxs-lookup"><span data-stu-id="d6783-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="d6783-107">（有关如何创建质检订单的信息，请参阅[检查货物质量](inspect-quality-goods.md)。）</span><span class="sxs-lookup"><span data-stu-id="d6783-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="d6783-108">必须先在 **用户** 页的 **人员** 字段中为用户分配工作人员，然后用户才能够处理不符合项的审核。</span><span class="sxs-lookup"><span data-stu-id="d6783-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="d6783-109">而且，必须在用户的用户选项中将 **启用文档处理** 选项设置为 *是*，用户才能够使用文档注释。</span><span class="sxs-lookup"><span data-stu-id="d6783-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="d6783-110">创建一个不符合项</span><span class="sxs-lookup"><span data-stu-id="d6783-110">Create a nonconformance</span></span>

<span data-ttu-id="d6783-111">要创建不符合项，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d6783-112">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-113">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d6783-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="d6783-114">在 **创建不符合项** 对话框的 **问题类型** 字段中，选择在检查流程中发现的问题的类型。</span><span class="sxs-lookup"><span data-stu-id="d6783-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="d6783-115">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6783-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="d6783-116">批准或拒绝不符合项</span><span class="sxs-lookup"><span data-stu-id="d6783-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="d6783-117">要批准或拒绝不符合项，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d6783-118">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-119">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-120">您只能向已批准的不符合项添加更正。</span><span class="sxs-lookup"><span data-stu-id="d6783-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-121">在操作窗格上，选择 **功能 \> 批准不符合项** 来批准不符合项，或选择 **功能 \> 拒绝不符合项** 来拒绝不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="d6783-122">您可以将批准的不符合项与[相关操作](../quality-operations.md)关联。</span><span class="sxs-lookup"><span data-stu-id="d6783-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="d6783-123">这样，您可以记录作为不符合项处理和更正处理的一部分完成的工作。</span><span class="sxs-lookup"><span data-stu-id="d6783-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="d6783-124">系统将提示您确认选择。</span><span class="sxs-lookup"><span data-stu-id="d6783-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d6783-125">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="d6783-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="d6783-126">向不符合项添加操作和其他详细信息</span><span class="sxs-lookup"><span data-stu-id="d6783-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="d6783-127">创建不符合项后，您可以开始添加相关操作并指定有关这些操作的其他信息。</span><span class="sxs-lookup"><span data-stu-id="d6783-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="d6783-128">您只能向已批准的不符合项添加相关操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="d6783-129">除了基本信息，您还可以向操作添加以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="d6783-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="d6783-130">**物料** – 您可以创建执行更正所消耗的物料的列表。</span><span class="sxs-lookup"><span data-stu-id="d6783-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="d6783-131">例如，物料可能是维修设备所需的产品或成品返工所需的成分。</span><span class="sxs-lookup"><span data-stu-id="d6783-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="d6783-132">**质量费用** – 您可以创建产生或记入外部来源的费用列表。</span><span class="sxs-lookup"><span data-stu-id="d6783-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="d6783-133">**工时单** – 您可以创建每个工作人员花在操作上的时间日志。</span><span class="sxs-lookup"><span data-stu-id="d6783-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="d6783-134">其余设置是可选的。</span><span class="sxs-lookup"><span data-stu-id="d6783-134">The remaining settings are optional.</span></span> <span data-ttu-id="d6783-135">每个物料的成本、质量费用和工时单将汇总并显示在操作中。</span><span class="sxs-lookup"><span data-stu-id="d6783-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="d6783-136">您无法直接在操作上编辑 **成本** 字段。</span><span class="sxs-lookup"><span data-stu-id="d6783-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="d6783-137">为不符合项创建操作</span><span class="sxs-lookup"><span data-stu-id="d6783-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="d6783-138">要为不符合项创建操作，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d6783-139">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-140">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-141">您只能为已批准的不符合项添加或更新操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-142">在操作窗格上，选择 **相关操作**。</span><span class="sxs-lookup"><span data-stu-id="d6783-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d6783-143">在 **相关操作** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6783-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d6783-144">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d6783-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d6783-145">**操作** – 选择要为不符合项执行的操作的代码。</span><span class="sxs-lookup"><span data-stu-id="d6783-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="d6783-146">**原因** – 输入解释为何需要执行此操作的详细说明。</span><span class="sxs-lookup"><span data-stu-id="d6783-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="d6783-147">**销售订单** – 如果所选的操作代码与销售订单类型相关，选择操作要链接到的销售订单。</span><span class="sxs-lookup"><span data-stu-id="d6783-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="d6783-148">**采购订单** – 如果所选的操作代码与采购订单类型相关，选择操作要链接到的采购订单。</span><span class="sxs-lookup"><span data-stu-id="d6783-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="d6783-149">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="d6783-150">向操作添加物料</span><span class="sxs-lookup"><span data-stu-id="d6783-150">Add items to an operation</span></span>

<span data-ttu-id="d6783-151">要向操作添加物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d6783-152">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-153">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-154">您只能为已批准的不符合项添加或更新操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-155">在操作窗格上，选择 **相关操作**。</span><span class="sxs-lookup"><span data-stu-id="d6783-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d6783-156">在 **相关操作** 页上，选择要添加物料的操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="d6783-157">在操作窗格上，选择 **物料**。</span><span class="sxs-lookup"><span data-stu-id="d6783-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="d6783-158">在 **相关操作** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6783-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d6783-159">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d6783-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="d6783-160">**物料编号** – 选择将在选定操作中使用的产品。</span><span class="sxs-lookup"><span data-stu-id="d6783-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="d6783-161">**数量** – 输入将要消耗的物品数量。</span><span class="sxs-lookup"><span data-stu-id="d6783-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-162">您可以在 **常规** 选项卡上的 **成本** 字段中查看物料的成本。此处显示的成本来自在 **已发布产品** 页上设置的成本。</span><span class="sxs-lookup"><span data-stu-id="d6783-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="d6783-163">无法在 **相关操作物料** 页上直接更新此成本。</span><span class="sxs-lookup"><span data-stu-id="d6783-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="d6783-164">**相关操作物料** 页上添加的所有物料的成本会自动添加到 **相关操作** 页上的 **成本** 字段中。</span><span class="sxs-lookup"><span data-stu-id="d6783-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="d6783-165">对必须添加的其他每个物料重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="d6783-166">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="d6783-167">向操作添加质量费用</span><span class="sxs-lookup"><span data-stu-id="d6783-167">Add quality charges to an operation</span></span>

<span data-ttu-id="d6783-168">要向操作添加质量费用，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d6783-169">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-170">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-171">您只能为已批准的不符合项添加或更新操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-172">在操作窗格上，选择 **相关操作**。</span><span class="sxs-lookup"><span data-stu-id="d6783-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d6783-173">在 **相关操作** 页上，选择要添加质量费用的操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="d6783-174">在操作窗格上，选择 **质量费用**。</span><span class="sxs-lookup"><span data-stu-id="d6783-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="d6783-175">在 **相关操作费用** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6783-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d6783-176">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d6783-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d6783-177">**费用代码** – 选择要添加的质量费用。</span><span class="sxs-lookup"><span data-stu-id="d6783-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="d6783-178">**描述** – 输入费用的详细描述。</span><span class="sxs-lookup"><span data-stu-id="d6783-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="d6783-179">**费用值** – 输入费用的金额。</span><span class="sxs-lookup"><span data-stu-id="d6783-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="d6783-180">对必须添加的其他每个费用重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="d6783-181">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d6783-182">所有质量费用的 **费用值** 字段中的金额会自动汇总，然后加到 **相关操作** 页上 **成本** 字段中的任何其他金额中。</span><span class="sxs-lookup"><span data-stu-id="d6783-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="d6783-183">在操作上创建工时单</span><span class="sxs-lookup"><span data-stu-id="d6783-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="d6783-184">要向操作添加工时单，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="d6783-185">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-186">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-187">您只能为已批准的不符合项添加或更新操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-188">在操作窗格上，选择 **相关操作**。</span><span class="sxs-lookup"><span data-stu-id="d6783-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="d6783-189">在 **相关操作** 页上，选择要添加工时单的操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="d6783-190">在操作窗格上，选择 **工时单**。</span><span class="sxs-lookup"><span data-stu-id="d6783-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="d6783-191">在 **相关操作工时单** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6783-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d6783-192">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d6783-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d6783-193">**日期** – 指定完成工作的日期。</span><span class="sxs-lookup"><span data-stu-id="d6783-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="d6783-194">默认情况下，此字段设置为当天。</span><span class="sxs-lookup"><span data-stu-id="d6783-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="d6783-195">**工作人员** – 选择完成工作的工作人员。</span><span class="sxs-lookup"><span data-stu-id="d6783-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="d6783-196">默认情况下，此字段设置为分配给当前用户的工作人员。</span><span class="sxs-lookup"><span data-stu-id="d6783-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="d6783-197">**操作时间** – 输入在所选操作上工作的小时数。</span><span class="sxs-lookup"><span data-stu-id="d6783-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="d6783-198">**已开票** – 如果已在发票上将时间计入客户或供应商费用，选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="d6783-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-199">您可以在 **常规** 选项卡上的 **成本** 字段中查看成本。此成本使用您在 **库存管理参数** 页定义的费率计算。</span><span class="sxs-lookup"><span data-stu-id="d6783-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="d6783-200">对必须添加的其他每个工时单行重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="d6783-201">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d6783-202">所有工时单行的 **成本** 字段中的金额将汇总，然后加到 **相关操作** 页上 **成本** 字段中的任何其他金额中。</span><span class="sxs-lookup"><span data-stu-id="d6783-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="d6783-203">向不符合项添加更正</span><span class="sxs-lookup"><span data-stu-id="d6783-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="d6783-204">要向不符合项添加更正，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d6783-205">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-206">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-207">您只能向已批准的不符合项添加更正。</span><span class="sxs-lookup"><span data-stu-id="d6783-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-208">在操作窗格上，选择 **更正**。</span><span class="sxs-lookup"><span data-stu-id="d6783-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d6783-209">在 **更正** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="d6783-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="d6783-210">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d6783-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="d6783-211">**诊断** – 选择用于标识您要创建的更正类型的诊断类型。</span><span class="sxs-lookup"><span data-stu-id="d6783-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="d6783-212">**工作人员** – 选择负责更正的人员。</span><span class="sxs-lookup"><span data-stu-id="d6783-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="d6783-213">**更正优先级** – 选择指示如何设定更正优先级（*低*、*一般* 或 *高*）的选项。</span><span class="sxs-lookup"><span data-stu-id="d6783-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="d6783-214">**请求日期** – 输入请求执行更正操作的日期。</span><span class="sxs-lookup"><span data-stu-id="d6783-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="d6783-215">**计划日期** – 输入预期完成更正的日期。</span><span class="sxs-lookup"><span data-stu-id="d6783-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="d6783-216">**短期解决方案** – 如果更正操作在短时间内即可更正不符合项，则选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="d6783-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="d6783-217">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="d6783-218">将更正标记为完成</span><span class="sxs-lookup"><span data-stu-id="d6783-218">Mark a correction as completed</span></span>

<span data-ttu-id="d6783-219">要将不符合项更正标记为完成，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="d6783-220">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-221">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6783-222">您只能向已批准的不符合项添加更正。</span><span class="sxs-lookup"><span data-stu-id="d6783-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="d6783-223">在操作窗格上，选择 **更正**。</span><span class="sxs-lookup"><span data-stu-id="d6783-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d6783-224">在 **更正** 页上的网格中，选择要标记为完成的更正。</span><span class="sxs-lookup"><span data-stu-id="d6783-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="d6783-225">在操作窗格上，选择 **标记完成**。</span><span class="sxs-lookup"><span data-stu-id="d6783-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="d6783-226">系统将提示您确认选择。</span><span class="sxs-lookup"><span data-stu-id="d6783-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d6783-227">选择 **确定** 继续。</span><span class="sxs-lookup"><span data-stu-id="d6783-227">Select **OK** to continue.</span></span> <span data-ttu-id="d6783-228">**完成日期和时间** 字段将设置为当前日期和时间，并选中 **已完成** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d6783-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="d6783-229">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="d6783-230">重新打开完成的更正</span><span class="sxs-lookup"><span data-stu-id="d6783-230">Reopen a completed correction</span></span>

<span data-ttu-id="d6783-231">要重新打开完成的更正，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d6783-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="d6783-232">转到 **库存管理 \> 定期任务 \> 质量管理 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-233">在列表中，选择要更新的不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="d6783-234">在操作窗格上，选择 **更正**。</span><span class="sxs-lookup"><span data-stu-id="d6783-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="d6783-235">在 **更正** 页上的网格中，选择要重新打开的更正。</span><span class="sxs-lookup"><span data-stu-id="d6783-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="d6783-236">在操作窗格上，选择 **重新打开**。</span><span class="sxs-lookup"><span data-stu-id="d6783-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="d6783-237">系统将提示您确认选择。</span><span class="sxs-lookup"><span data-stu-id="d6783-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d6783-238">选择 **确定** 继续。</span><span class="sxs-lookup"><span data-stu-id="d6783-238">Select **OK** to continue.</span></span> <span data-ttu-id="d6783-239">此值将从 **完成日期和时间** 字段中清除，**已完成** 复选框也将清除。</span><span class="sxs-lookup"><span data-stu-id="d6783-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="d6783-240">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-240">Close the page.</span></span>

<span data-ttu-id="d6783-241">现在，您可以对更正进行其他编辑或更新了。</span><span class="sxs-lookup"><span data-stu-id="d6783-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="d6783-242">完成后，可以再次将更正标记为完成。</span><span class="sxs-lookup"><span data-stu-id="d6783-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="d6783-243">关闭不符合项</span><span class="sxs-lookup"><span data-stu-id="d6783-243">Close a nonconformance</span></span>

<span data-ttu-id="d6783-244">要关闭不符合项，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d6783-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="d6783-245">转到 **库存管理 \> 定期任务 \> 质量管理 \> 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="d6783-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="d6783-246">在网格中选择一个质检订单。</span><span class="sxs-lookup"><span data-stu-id="d6783-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="d6783-247">在操作窗格上，选择 **查询 \> 不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="d6783-248">在 **不符合项** 页上，在网格中选择目标不符合项。</span><span class="sxs-lookup"><span data-stu-id="d6783-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="d6783-249">在操作窗格上，选择 **功能 \> 关闭不符合项**。</span><span class="sxs-lookup"><span data-stu-id="d6783-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="d6783-250">系统将提示您确认选择。</span><span class="sxs-lookup"><span data-stu-id="d6783-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="d6783-251">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="d6783-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="d6783-252">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d6783-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6783-253">其他资源</span><span class="sxs-lookup"><span data-stu-id="d6783-253">Additional resources</span></span>

- [<span data-ttu-id="d6783-254">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="d6783-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="d6783-255">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="d6783-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="d6783-256">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="d6783-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="d6783-257">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="d6783-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="d6783-258">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="d6783-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="d6783-259">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="d6783-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="d6783-260">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="d6783-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="d6783-261">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="d6783-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
