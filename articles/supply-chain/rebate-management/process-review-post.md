---
title: 处理、审核和过帐返点
description: 本主题介绍如何处理返点管理交易、计算其折扣、审核生成的交易记录、过帐交易记录和审核过帐。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 53a24866786f209a1d0f6932bb4f782bf936bd21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819248"
---
# <a name="process-review-and-post-rebates"></a><span data-ttu-id="d0416-103">处理、审核和过帐返点</span><span class="sxs-lookup"><span data-stu-id="d0416-103">Process, review, and post rebates</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d0416-104">本主题介绍如何处理返点管理交易、计算其折扣、审核生成的交易记录、过帐交易记录和审核过帐。</span><span class="sxs-lookup"><span data-stu-id="d0416-104">This topic describes how to process your Rebate management deals, calculate their discounts, review the transactions that are generated, post transactions, and review the postings.</span></span>

## <a name="change-the-status-of-a-deal"></a><span data-ttu-id="d0416-105">更改交易的状态</span><span class="sxs-lookup"><span data-stu-id="d0416-105">Change the status of a deal</span></span>

<span data-ttu-id="d0416-106">您可以将状态分配到每个交易以帮助跟踪它。</span><span class="sxs-lookup"><span data-stu-id="d0416-106">You can assign a status to each deal to help track it.</span></span> <span data-ttu-id="d0416-107">此状态仅供参考。</span><span class="sxs-lookup"><span data-stu-id="d0416-107">The status is for informational purposes only.</span></span>

1. <span data-ttu-id="d0416-108">选择交易（例如，在 [**所有返点管理交易** 页面](rebate-management-deals.md)上）。</span><span class="sxs-lookup"><span data-stu-id="d0416-108">Select a deal (for example, on the [**All rebate management deals** page](rebate-management-deals.md)).</span></span>
1. <span data-ttu-id="d0416-109">在操作窗格的 **返点管理交易** 选项卡上，在 **维护** 组中，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="d0416-109">On the Action Pane, on the **Rebate management deals** tab, in the **Maintain** group, select **Change status**.</span></span>
1. <span data-ttu-id="d0416-110">在 **更改状态** 对话框中，将 **返点状态** 字段设置为新状态。</span><span class="sxs-lookup"><span data-stu-id="d0416-110">In the **Change status** dialog box, set the **Rebate status** field to a new status.</span></span>
1. <span data-ttu-id="d0416-111">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0416-111">Select **OK**.</span></span>

## <a name="calculate-fifo-purchase-prices"></a><span data-ttu-id="d0416-112">计算 FIFO 采购价格</span><span class="sxs-lookup"><span data-stu-id="d0416-112">Calculate FIFO purchase prices</span></span>

<span data-ttu-id="d0416-113">必须运行 **计算 FIFO 采购价格** 定期任务以计算 **价格基准** 字段设置为 *FIFO* 的[交易](rebate-management-deals.md)的返点。</span><span class="sxs-lookup"><span data-stu-id="d0416-113">The **Calculate FIFO purchase price** periodic task must be run to calculate the rebates for [deals](rebate-management-deals.md) where the **Price basis** field is set to *FIFO*.</span></span> <span data-ttu-id="d0416-114">系统将使用先进先出 (FIFO) 规则计算已出售存货的价值。</span><span class="sxs-lookup"><span data-stu-id="d0416-114">The system will use a first in, first out (FIFO) rule to calculate the value of the stock that was sold.</span></span> <span data-ttu-id="d0416-115">然后，该价值将用于计算供应商返点。</span><span class="sxs-lookup"><span data-stu-id="d0416-115">This value will then be used to calculate the vendor rebates.</span></span>

<span data-ttu-id="d0416-116">转到 **返点管理 \> 定期任务 \> 计算 FIFO 采购价格**。</span><span class="sxs-lookup"><span data-stu-id="d0416-116">Go to **Rebates management \> Periodic tasks \> Calculate FIFO purchase price**.</span></span> <span data-ttu-id="d0416-117">在显示的对话框中，选择 **确定** 以运行计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-117">In the dialog box that appears, select **OK** to run the calculation.</span></span>

## <a name="process-rebate-management-deals"></a><span data-ttu-id="d0416-118">处理返点管理交易</span><span class="sxs-lookup"><span data-stu-id="d0416-118">Process Rebate management deals</span></span>

<span data-ttu-id="d0416-119">处理交易时，系统将计算所有已设置的相关返点和特许使用费。</span><span class="sxs-lookup"><span data-stu-id="d0416-119">When you process a deal, the system calculates all relevant rebates and royalties that are set up.</span></span> <span data-ttu-id="d0416-120">仅处理具有已准备好计算的计算期间和状态为 *活动* 的选定交易。</span><span class="sxs-lookup"><span data-stu-id="d0416-120">Only selected deals that have calculation periods that are ready to be calculated and that have a status of *Active* will be processed.</span></span> <span data-ttu-id="d0416-121">处理完成后，系统将生成一组交易记录，您可以查看这些交易记录，然后将其过帐。</span><span class="sxs-lookup"><span data-stu-id="d0416-121">After processing is completed, the system generates a set of transactions that you can review and then post.</span></span>

> [!NOTE]
> <span data-ttu-id="d0416-122">在所有情况下，在按每个交易的 **对帐依据** 设置（*交易* 或 *行*）指定的级别上处理返点。</span><span class="sxs-lookup"><span data-stu-id="d0416-122">In all cases, rebates are processed at the level that is specified by each deal's **Reconcile by** setting (*Deal* or *Line*).</span></span> <span data-ttu-id="d0416-123">仅可以对 **对帐依据** 字段设置为 *行* 的交易执行单行计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-123">You can do single-line calculations only for deals where the **Reconcile by** field is set to *Line*.</span></span>

### <a name="process-all-lines-for-one-or-more-deals"></a><span data-ttu-id="d0416-124">处理一个或多个交易的所有行</span><span class="sxs-lookup"><span data-stu-id="d0416-124">Process all lines for one or more deals</span></span>

1. <span data-ttu-id="d0416-125">针对要处理的交易类型打开适当的[返点交易列表页面](rebate-management-deals.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-125">Open the appropriate [rebate deals list page](rebate-management-deals.md) for the type of deal that you want to work with.</span></span>
1. <span data-ttu-id="d0416-126">选择要处理的每个交易的行（或打开要处理的交易）。</span><span class="sxs-lookup"><span data-stu-id="d0416-126">Select the row for each deal that you want to process (or open the deal that you want to process).</span></span>
1. <span data-ttu-id="d0416-127">在操作窗格的 **返点管理交易** 选项卡上，在 **生成** 组中，选择以下命令之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-127">On the Action Pane, on the **Rebate management deals** tab, in the **Generate** group, select one of the following commands:</span></span>

    - <span data-ttu-id="d0416-128">**处理 \> 预配** – 为每个相关的返点交易预配一组应计，但不要过帐它们。</span><span class="sxs-lookup"><span data-stu-id="d0416-128">**Process \> Provision** – Provision a set of accruals for each relevant rebate deal, but don't post them.</span></span>
    - <span data-ttu-id="d0416-129">**处理 \> 返点管理** – 处理提供每个交易的返点价值的一系列交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-129">**Process \> Rebate management** – Process a series of transactions that provide the value of the rebate for each deal.</span></span>
    - <span data-ttu-id="d0416-130">**处理 \> 勾销** – 冲销之前过帐的交易记录以将其勾销，以便可以计算新的返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-130">**Process \> Write off** – Reverse previously posted transactions to write them off so that new rebate deal transactions can be calculated.</span></span>

1. <span data-ttu-id="d0416-131">在显示的对话框中，设置 **开始日期** 和 **结束日期** 字段以定义计算的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-131">In the dialog box that appears, set the **From date** and **To date** fields to define the date range for the calculation.</span></span>
1. <span data-ttu-id="d0416-132">选择 **确定** 以运行计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-132">Select **OK** to run the calculation.</span></span>

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a><span data-ttu-id="d0416-133">处理选定交易的一个或多个特定交易行</span><span class="sxs-lookup"><span data-stu-id="d0416-133">Process one or more specific deal lines for a selected deal</span></span>

1. <span data-ttu-id="d0416-134">针对要处理的交易类型打开适当的[返点交易列表页面](rebate-management-deals.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-134">Open the appropriate [rebate deals list page](rebate-management-deals.md) for the type of deal that you want to work with.</span></span>
1. <span data-ttu-id="d0416-135">打开要处理行的交易。</span><span class="sxs-lookup"><span data-stu-id="d0416-135">Open the deal that you want to process a line from.</span></span>
1. <span data-ttu-id="d0416-136">选择右上角的 **行** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d0416-136">Select the **Lines** tab in the upper-right corner.</span></span>
1. <span data-ttu-id="d0416-137">在 **返点管理** 快速选项卡上，选择要处理的每个交易行的行。</span><span class="sxs-lookup"><span data-stu-id="d0416-137">On **Rebate management** FastTab, select the row for each deal line that you want to process.</span></span>
1. <span data-ttu-id="d0416-138">在 **返点管理** 快速选项卡的工具栏上，选择以下命令之一。</span><span class="sxs-lookup"><span data-stu-id="d0416-138">On the toolbar of the **Rebate management** FastTab, select one of the following commands.</span></span> <span data-ttu-id="d0416-139">（这些命令仅适用于 **对帐依据** 字段设置为 *行* 的交易。）</span><span class="sxs-lookup"><span data-stu-id="d0416-139">(These commands are available only for deals where the **Reconcile by** field is set to *Line*.)</span></span>

    - <span data-ttu-id="d0416-140">**处理 \> 预配** – 为每个相关的交易行预配一组应计，但不要过帐它们。</span><span class="sxs-lookup"><span data-stu-id="d0416-140">**Process \> Provision** – Provision a set of accruals for each relevant deal line, but don't post them.</span></span>
    - <span data-ttu-id="d0416-141">**处理 \> 返点管理** – 处理提供每个交易行的返点价值的一系列交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-141">**Process \> Rebate management** – Process a series of transactions that provide the value of the rebate for each deal line.</span></span>
    - <span data-ttu-id="d0416-142">**处理 \> 勾销** – 冲销之前过帐的交易记录以将其勾销，以便可以计算新的返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-142">**Process \> Write off** – Reverse previously posted transactions to write them off so that new rebate deal transactions can be calculated.</span></span>

1. <span data-ttu-id="d0416-143">在显示的对话框中，设置 **开始日期** 和 **结束日期** 字段以定义计算的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-143">In the dialog box that appears, set the **From date** and **To date** fields to define the date range for the calculation.</span></span>
1. <span data-ttu-id="d0416-144">选择 **确定** 以运行计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-144">Select **OK** to run the calculation.</span></span>

### <a name="process-deals-using-a-batch-job"></a><span data-ttu-id="d0416-145">使用批处理作业处理交易</span><span class="sxs-lookup"><span data-stu-id="d0416-145">Process deals using a batch job</span></span>

<span data-ttu-id="d0416-146">您可以运行批处理作业来同时处理多个交易，而不是处理特定交易或交易行。</span><span class="sxs-lookup"><span data-stu-id="d0416-146">Instead of processing specific deals or deal lines, you can run a batch job to process several deals at the same time.</span></span> <span data-ttu-id="d0416-147">您可以选择应用记录筛选器和/或设置定期计划。</span><span class="sxs-lookup"><span data-stu-id="d0416-147">You can optionally apply record filters and/or set up a recurring schedule.</span></span> <span data-ttu-id="d0416-148">若要使用批处理作业处理交易，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d0416-148">To process deals by using a batch job, follow these steps.</span></span>

1. <span data-ttu-id="d0416-149">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-149">Follow one of these steps:</span></span>

    - <span data-ttu-id="d0416-150">转到 **返点管理 \> 定期任务 \> 处理 \> 预配** 以为每个相关交易预配一组应计，但不要过帐它们。</span><span class="sxs-lookup"><span data-stu-id="d0416-150">Go to **Rebate management \> Periodic tasks \> Process \> Provision** to provision a set of accruals for each relevant deal, but without posting them.</span></span>
    - <span data-ttu-id="d0416-151">转到 **返点管理 \> 定期任务 \> 处理 \> 返点管理** 以处理提供每个交易的返点价值的一系列交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-151">Go to **Rebate management \> Periodic tasks \> Process \> Rebate management** to process a series of transactions that provide the value of the rebate for each deal.</span></span>
    - <span data-ttu-id="d0416-152">转到 **返点管理 \> 定期任务 \> 处理 \> 勾销** 以冲销之前过帐的交易记录以将其勾销，以便可以计算新的返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-152">Go to **Rebate management \> Periodic tasks \> Process \> Write off** to reverse previously posted transactions to write them off so that new rebate deal transactions can be calculated.</span></span>

1. <span data-ttu-id="d0416-153">在显示的对话框中，在 **参数** 快速选项卡上的 **期间** 部分中，设置 **开始日期** 和 **结束日期** 字段以定义计算的交易记录的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-153">In the dialog box that appears, on the **Parameters** FastTab, in the **Period** section, set the **From date** and **To date** fields to define the date range for transactions for the calculation.</span></span>
1. <span data-ttu-id="d0416-154">在 **担保期间** 部分中，设置 **开始日期** 和 **结束日期** 字段以定义计算的担保的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-154">In the **Guarantee Period** section, set the **From date** and **To date** fields to define the date range for guarantees for the calculation.</span></span>
1. <span data-ttu-id="d0416-155">在 **要包括的记录** 快速选项卡上，您可以设置筛选器以限制批处理作业将处理的交易集。</span><span class="sxs-lookup"><span data-stu-id="d0416-155">On the **Records to include** FastTab, you can set up filters to limit the set of deals that the batch job will process.</span></span> <span data-ttu-id="d0416-156">这些设置的工作方式与其他类型的批处理作业的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="d0416-156">These settings work in the same way that they work for other types of batch jobs.</span></span>
1. <span data-ttu-id="d0416-157">在 **在后台运行** 快速选项卡上，您可以根据需要设置批处理和计划选项。</span><span class="sxs-lookup"><span data-stu-id="d0416-157">On the **Run in the background** FastTab, you can set up batch processing and scheduling options as required.</span></span> <span data-ttu-id="d0416-158">这些设置的工作方式与其他类型的批处理作业的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="d0416-158">These settings work in the same way that they work for other types of batch jobs.</span></span>
1. <span data-ttu-id="d0416-159">选择 **确定** 以运行和/或计划计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-159">Select **OK** to run and/or schedule the calculation.</span></span>

## <a name="view-and-edit-rebate-management-transactions"></a><span data-ttu-id="d0416-160">查看和编辑返点管理交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-160">View and edit Rebate management transactions</span></span>

<span data-ttu-id="d0416-161">处理一个或多个交易时，系统将创建交易记录，您可以查看并且可以在过帐之前编辑这些交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-161">When you process one or more deals, the system creates transactions that you can view and, perhaps, edit before you post them.</span></span>

1. <span data-ttu-id="d0416-162">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-162">Follow one of these steps:</span></span>

    - <span data-ttu-id="d0416-163">选择要查看交易记录的交易（例如，在 [**所有返点管理交易** 页面](rebate-management-deals.md)上）。</span><span class="sxs-lookup"><span data-stu-id="d0416-163">Select the deal to view transactions for (for example, on the [**All rebate management deals** page](rebate-management-deals.md)).</span></span> <span data-ttu-id="d0416-164">在操作窗格的 **返点管理交易** 选项卡上，在 **交易记录** 组中，选择 **交易记录** 或 **担保交易记录**，具体取决于要查看的交易记录的类型。</span><span class="sxs-lookup"><span data-stu-id="d0416-164">On the Action Pane, on the **Rebate management deals** tab, in the **Transactions** group, select **Transactions** or **Guarantee transactions**, depending on the type of transaction that you want to view.</span></span>
    - <span data-ttu-id="d0416-165">打开交易（例如，在 [**所有返点管理交易** 页面](rebate-management-deals.md)上）以查看其详细信息。</span><span class="sxs-lookup"><span data-stu-id="d0416-165">Open a deal (for example, on the [**All rebate management deals** page](rebate-management-deals.md)) to view its details.</span></span> <span data-ttu-id="d0416-166">在 **返点管理** 快速选项卡上，选择要查看交易记录的交易行。</span><span class="sxs-lookup"><span data-stu-id="d0416-166">On the **Rebate management** FastTab, select the deal line to view transactions for.</span></span> <span data-ttu-id="d0416-167">然后，在工具栏上，选择 **交易记录** 或 **担保交易记录**，具体取决于要查看的交易记录的类型。</span><span class="sxs-lookup"><span data-stu-id="d0416-167">Then, on the toolbar, select **Transactions** or **Guarantee transactions**, depending on the type of transaction that you want to view.</span></span> <span data-ttu-id="d0416-168">（这些按钮仅适用于 **对帐依据** 字段设置为 *行* 的交易。）</span><span class="sxs-lookup"><span data-stu-id="d0416-168">(These buttons are available only for deals where the **Reconcile by** field is set to *Line*.)</span></span>

1. <span data-ttu-id="d0416-169">显示 **返点管理日期交易记录** 或 **返点管理担保交易记录** 页面。</span><span class="sxs-lookup"><span data-stu-id="d0416-169">The **Rebate management date transactions** or **Rebate management guarantee transactions** page appears.</span></span> <span data-ttu-id="d0416-170">它包含一个网格，其中每行代表一个返点或担保期间的交易记录集合。</span><span class="sxs-lookup"><span data-stu-id="d0416-170">It contains a grid, where each line represents a collection of transactions from a single rebate or guarantee period.</span></span> <span data-ttu-id="d0416-171">在网格中选择一行，然后在操作窗格上，选择 **源交易记录** 以查看属于该行的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-171">Select a row in the grid, and then, on the Action Pane, select **Source transactions** to view the transactions that belong to that row.</span></span>
1. <span data-ttu-id="d0416-172">显示的页面显示了属于选定行的选定类型的交易记录列表。</span><span class="sxs-lookup"><span data-stu-id="d0416-172">The page that appears shows a list of the transactions of the selected type that belong to the selected row.</span></span> <span data-ttu-id="d0416-173">每个交易记录都提供相关的详细信息，具体取决于交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="d0416-173">Each transaction provides relevant details, depending on the transaction type.</span></span> <span data-ttu-id="d0416-174">对于担保交易记录，您只能查看列表。</span><span class="sxs-lookup"><span data-stu-id="d0416-174">For guarantee transactions, you can only view the list.</span></span> <span data-ttu-id="d0416-175">对于其他类型的交易记录，您可以在此页面上执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d0416-175">For other types of transactions, you can perform the following actions on this page:</span></span>

    - <span data-ttu-id="d0416-176">若要在页面上验证所有已声明交易记录的总价值，请查看 **已声明金额** 字段。</span><span class="sxs-lookup"><span data-stu-id="d0416-176">To verify the total value of all claimed transactions on the page, view the **Claimed amount** field.</span></span>
    - <span data-ttu-id="d0416-177">若要查看有关任何交易记录的详细信息，请选择交易记录，然后选择 **常规**、**财务维度** 或 **维度** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d0416-177">To view more information about any transaction, select it, and then select the **General**, **Financial dimension**, or **Dimension** tab.</span></span>
    - <span data-ttu-id="d0416-178">若要查看任何适用的缩减，请在操作窗格上选择 **缩减交易记录**。</span><span class="sxs-lookup"><span data-stu-id="d0416-178">To view any reductions that apply, select **Reduction transactions** on the Action Pane.</span></span> <span data-ttu-id="d0416-179">有关详细信息，请参阅[返点缩减原则](rebate-reduction-principle.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-179">For more information, see [Rebate reduction principles](rebate-reduction-principle.md).</span></span>
    - <span data-ttu-id="d0416-180">若要将交易记录标记为已声明或未声明（如果使用声明流程），请选择相关行，然后在操作窗格上选择以下命令之一。</span><span class="sxs-lookup"><span data-stu-id="d0416-180">To mark transactions as either claimed or unclaimed if you're using a claims process, select the relevant rows, and then, on the Action Pane, select one of the following commands.</span></span> <span data-ttu-id="d0416-181">（在 [**返点管理参数** 页面](rebate-management-parameters.md)上启用声明流程。）</span><span class="sxs-lookup"><span data-stu-id="d0416-181">(You enable claims processes on the [**Rebate management parameters** page](rebate-management-parameters.md).)</span></span>

        - <span data-ttu-id="d0416-182">**设置已声明 \> 全部** – 将所有交易记录标记为已声明。</span><span class="sxs-lookup"><span data-stu-id="d0416-182">**Set claimed \> All** – Mark all transactions as claimed.</span></span>
        - <span data-ttu-id="d0416-183">**设置已声明 \> 选定** – 将选定交易记录标记为已声明。</span><span class="sxs-lookup"><span data-stu-id="d0416-183">**Set claimed \> Selected** – Mark the selected transactions as claimed.</span></span>
        - <span data-ttu-id="d0416-184">**设置未声明 \> 全部** – 将所有交易记录标记为未声明。</span><span class="sxs-lookup"><span data-stu-id="d0416-184">**Set unclaimed \> All** – Mark all transactions as unclaimed.</span></span>
        - <span data-ttu-id="d0416-185">**设置未声明 \> 选定** – 将选定交易记录标记为未声明。</span><span class="sxs-lookup"><span data-stu-id="d0416-185">**Set unclaimed \> Selected** – Mark the selected transactions as unclaimed.</span></span>

    - <span data-ttu-id="d0416-186">若要过帐一个或多个行的声明，请选择相关行，然后在操作窗格上选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="d0416-186">To post the claim for one or more lines, select the relevant lines, and then, on the Action Pane, select **Post**.</span></span> <span data-ttu-id="d0416-187">（**过帐** 按钮仅适用于返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-187">(The **Post** button is available only for rebate transactions.</span></span> <span data-ttu-id="d0416-188">它不适用于预配和勾销交易记录。）在 **过帐** 对话框中，自动设置 **开始日期** 和 **结束日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="d0416-188">It's unavailable for provision and write-off transactions.) In the **Post** dialog box, the **From date** and **To date** fields are automatically set.</span></span> <span data-ttu-id="d0416-189">设置 **过帐日期** 字段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0416-189">Set the **Posting date** field, and then select **OK**.</span></span>
    - <span data-ttu-id="d0416-190">若要调整针对任何未结或未过帐交易记录显示的金额，请选择交易记录，然后执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-190">To adjust the amount that is shown for any open or unposted transaction, select the transaction, and then follow one of these steps:</span></span>

        - <span data-ttu-id="d0416-191">在 **更正的金额** 字段中编辑价值。</span><span class="sxs-lookup"><span data-stu-id="d0416-191">Edit the value in the **Corrected amount** field.</span></span>
        - <span data-ttu-id="d0416-192">在操作窗格上，选择 **设置更正**。</span><span class="sxs-lookup"><span data-stu-id="d0416-192">On the Action Pane, select **Set correction**.</span></span> <span data-ttu-id="d0416-193">然后，在显示的下拉对话框中，在 **更正的金额** 字段中，输入价值。</span><span class="sxs-lookup"><span data-stu-id="d0416-193">Then, in the drop-down dialog box that appears, in the **Corrected amount** field, enter a value.</span></span>

> [!NOTE]
> <span data-ttu-id="d0416-194">当处理下一个期间时，交易记录列表将包括上一个过帐中的所有未声明交易记录，以及选定期间的任何新交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-194">When you process the next period, the transaction list will include any unclaimed transactions from the previous posting, plus any new transactions for the selected period.</span></span>

## <a name="post-rebates-transactions"></a><span data-ttu-id="d0416-195">过帐返点交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-195">Post rebates transactions</span></span>

<span data-ttu-id="d0416-196">若要过帐返点和扣缴的价值，您必须运行过帐流程，除非已将系统设置为自动过帐它们。</span><span class="sxs-lookup"><span data-stu-id="d0416-196">To post the value of the rebates and deductions, you must run the posting process, unless you've set up your system to post them automatically.</span></span>

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a><span data-ttu-id="d0416-197">将系统设置为自动过帐所有交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-197">Set up the system to post all transactions automatically</span></span>

<span data-ttu-id="d0416-198">若要将系统设置为在生成后立即过帐所有交易记录，请在 **返点管理参数** 页面上打开 **自动过帐日记帐** 和/或 **自动过帐普通发票** 选项。</span><span class="sxs-lookup"><span data-stu-id="d0416-198">To set up your system to post all transactions as soon as they are generated, turn on the **Automatically post journals** and/or **Automatically post free text invoices** option on the **Rebate management parameters** page.</span></span> <span data-ttu-id="d0416-199">有关详细信息，请参阅[返点管理参数](rebate-management-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-199">For more information, see [Rebate management parameters](rebate-management-parameters.md).</span></span>

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a><span data-ttu-id="d0416-200">过帐一个或多个交易的所有行的交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-200">Post transactions for all lines for one or more deals</span></span>

<span data-ttu-id="d0416-201">如果您不使用自动过帐，请在处理相关交易后，按照以下步骤审核和过帐一个或多个交易的所有行的已生成交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-201">If you aren't using automatic posting, after you've processed the relevant deals, follow these steps to review and post the generated transactions for all lines for one or more deals.</span></span>

1. <span data-ttu-id="d0416-202">针对要处理的交易类型打开适当的[返点交易列表页面](rebate-management-deals.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-202">Open the appropriate [rebate deals list page](rebate-management-deals.md) for the type of deal that you want to work with.</span></span>
1. <span data-ttu-id="d0416-203">选择要过帐的每个交易的行（或打开要过帐的交易）。</span><span class="sxs-lookup"><span data-stu-id="d0416-203">Select the row for each deal that you want to post (or open the deal that you want to post).</span></span>
1. <span data-ttu-id="d0416-204">在操作窗格的 **返点管理交易** 选项卡上，在 **生成** 组中，选择以下命令之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-204">On the Action Pane, on the **Rebate management deals** tab, in the **Generate** group, select one of the following commands:</span></span>

    - <span data-ttu-id="d0416-205">**过帐 \> 预配** – 过帐已创建的可用应计交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-205">**Post \> Provision** – Post available accruals transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-206">**过帐 \> 返点管理** – 过帐已创建的可用返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-206">**Post \> Rebate management** – Post available rebate transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-207">**过帐 \> 勾销** – 过帐已创建的可用勾销交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-207">**Post \> Write off** – Post available write-off transactions that you've created.</span></span>

1. <span data-ttu-id="d0416-208">在显示的对话框中，设置 **过帐日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="d0416-208">In the dialog box that appears, set the **Posting date** field.</span></span> <span data-ttu-id="d0416-209">然后，设置 **开始日期** 和 **结束日期** 字段以定义必须过帐的交易记录的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-209">Then set the **From date** and **To date** fields to define the date range for the transactions that must be posted.</span></span>
1. <span data-ttu-id="d0416-210">选择 **确定** 以过帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-210">Select **OK** to post the transactions.</span></span>

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a><span data-ttu-id="d0416-211">过帐选定交易的一个或多个特定交易行的交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-211">Post transactions for one or more specific deal lines for a selected deal</span></span>

<span data-ttu-id="d0416-212">如果您不使用自动过帐，请在处理相关交易后，按照以下步骤审核和过帐选定交易的一个或多个特定交易行的已生成交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-212">If you aren't using automatic posting, after you've processed the relevant deals, follow these steps to review and post the generated transactions for one or more specific deal lines for a selected deal.</span></span>

1. <span data-ttu-id="d0416-213">针对要处理的交易类型打开适当的[返点交易列表页面](rebate-management-deals.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-213">Open the appropriate [rebate deals list page](rebate-management-deals.md) for the type of deal that you want to work with.</span></span>
1. <span data-ttu-id="d0416-214">打开具有要过帐交易记录的行的交易。</span><span class="sxs-lookup"><span data-stu-id="d0416-214">Open the deal that has a line that you want to post transactions for.</span></span>
1. <span data-ttu-id="d0416-215">选择右上角的 **行** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d0416-215">Select the **Lines** tab in the upper-right corner.</span></span>
1. <span data-ttu-id="d0416-216">在 **返点管理** 快速选项卡上，选择要过帐的每个交易行的行。</span><span class="sxs-lookup"><span data-stu-id="d0416-216">On **Rebate management** FastTab, select the row for each deal line that you want to post.</span></span>
1. <span data-ttu-id="d0416-217">在 **返点管理** 快速选项卡的工具栏上，选择以下命令之一。</span><span class="sxs-lookup"><span data-stu-id="d0416-217">On the toolbar of the **Rebate management** FastTab, select one of the following commands.</span></span> <span data-ttu-id="d0416-218">（这些命令仅适用于 **对帐依据** 设置为 *行* 的交易。）</span><span class="sxs-lookup"><span data-stu-id="d0416-218">(These commands are available only for deals where **Reconcile by** is set to *Line*.)</span></span>

    - <span data-ttu-id="d0416-219">**过帐 \> 预配** – 过帐已创建的可用应计交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-219">**Post \> Provision** – Post available accruals transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-220">**过帐 \> 返点管理** – 过帐已创建的可用返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-220">**Post \> Rebate management** – Post available rebate transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-221">**过帐 \> 勾销** – 过帐已创建的可用勾销交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-221">**Post \> Write off** – Post available write-off transactions that you've created.</span></span>

1. <span data-ttu-id="d0416-222">在显示的对话框中，设置 **过帐日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="d0416-222">In the dialog box that appears, set the **Posting date** field.</span></span> <span data-ttu-id="d0416-223">然后，设置 **开始日期** 和 **结束日期** 字段以定义必须过帐的交易记录的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-223">Then set the **From date** and **To date** fields to define the date range for the transactions that must be posted.</span></span>
1. <span data-ttu-id="d0416-224">选择 **确定** 以过帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-224">Select **OK** to post the transactions.</span></span>

### <a name="post-transactions-using-a-batch-job"></a><span data-ttu-id="d0416-225">使用批处理作业过帐交易记录</span><span class="sxs-lookup"><span data-stu-id="d0416-225">Post transactions using a batch job</span></span>

<span data-ttu-id="d0416-226">您可以运行批处理作业来同时过帐多个交易的交易记录，而不是过帐特定交易或交易行的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-226">Instead of posting transactions for specific deals or deal lines, you can run a batch job to post transactions for several deals at the same time.</span></span> <span data-ttu-id="d0416-227">您可以选择应用记录筛选器和/或设置定期计划。</span><span class="sxs-lookup"><span data-stu-id="d0416-227">You can optionally apply record filters and/or set up a recurring schedule.</span></span> <span data-ttu-id="d0416-228">若要使用批处理作业过帐交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d0416-228">To post transactions by using a batch job, follow these steps.</span></span>

1. <span data-ttu-id="d0416-229">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d0416-229">Follow one of these steps:</span></span>

    - <span data-ttu-id="d0416-230">转到 **返点管理 \> 定期任务 \> 过帐 \> 预配** 以过帐已创建的可用应计交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-230">Go to **Rebate management \> Periodic tasks \> Post \> Provision** to post available accrual transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-231">转到 **返点管理 \> 定期任务 \> 过帐 \> 返点管理** 以过帐已创建的可用返点交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-231">Go to **Rebate management \> Periodic tasks \> Post \> Rebate management** to post available rebate transactions that you've created.</span></span>
    - <span data-ttu-id="d0416-232">转到 **返点管理 \> 定期任务 \> 过帐 \> 勾销** 以过帐已创建的可用勾销交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0416-232">Go to **Rebate management \> Periodic tasks \> Post \> Write off** to post available write-off transactions that you've created.</span></span>

1. <span data-ttu-id="d0416-233">在显示的对话框中，在 **参数** 快速选项卡上的 **期间** 部分中，设置 **过帐日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="d0416-233">In the dialog box that appears, on the **Parameters** FastTab, in the **Period** section, set the **Posting date** field.</span></span> <span data-ttu-id="d0416-234">然后，设置 **开始日期** 和 **结束日期** 字段以定义必须过帐的交易记录的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-234">Then set the **From date** and **To date** fields to define the date range for the transactions that must be posted.</span></span> 
1. <span data-ttu-id="d0416-235">在 **担保期间** 部分中，设置 **开始日期** 和 **结束日期** 字段以定义必须过帐的担保的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d0416-235">In the **Guarantee Period** section, set the **From date** and **To date** fields to define the date range for the guarantees that must be posted.</span></span>
1. <span data-ttu-id="d0416-236">在 **要包括的记录** 快速选项卡上，您可以设置筛选器以限制批处理作业将处理的交易集。</span><span class="sxs-lookup"><span data-stu-id="d0416-236">On the **Records to include** FastTab, you can set up filters to limit the set of deals that the batch job will process.</span></span> <span data-ttu-id="d0416-237">这些设置的工作方式与其他类型的批处理作业的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="d0416-237">These settings work in the same way that they work for other types of batch jobs.</span></span>
1. <span data-ttu-id="d0416-238">在 **在后台运行** 快速选项卡上，您可以根据需要设置批处理和计划选项。</span><span class="sxs-lookup"><span data-stu-id="d0416-238">On the **Run in the background** FastTab, you can set up batch processing and scheduling options as required.</span></span> <span data-ttu-id="d0416-239">这些设置的工作方式与其他类型的批处理作业的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="d0416-239">These settings work in the same way that they work for other types of batch jobs.</span></span>
1. <span data-ttu-id="d0416-240">选择 **确定** 以运行和/或计划计算。</span><span class="sxs-lookup"><span data-stu-id="d0416-240">Select **OK** to run and/or schedule the calculation.</span></span>

## <a name="review-rebate-management-journals"></a><span data-ttu-id="d0416-241">查看返点管理日记帐</span><span class="sxs-lookup"><span data-stu-id="d0416-241">Review Rebate management journals</span></span>

<span data-ttu-id="d0416-242">过帐交易记录后，您可以查看生成的日记帐、单据或项目。</span><span class="sxs-lookup"><span data-stu-id="d0416-242">After your transactions have been posted, you can review the resulting journals, documents, or items.</span></span> <span data-ttu-id="d0416-243">返点和特许使用费的目标交易记录基于在过帐配置文件中设置的付款类型和返点的输出类型。</span><span class="sxs-lookup"><span data-stu-id="d0416-243">Target transactions for rebates and royalties are based on the payment type that is set in the posting profile and the rebate's output type.</span></span> <span data-ttu-id="d0416-244">例如，如果返点输出设置为 *项目*，将创建销售订单，并且可以通过目标交易记录进行查看。</span><span class="sxs-lookup"><span data-stu-id="d0416-244">For example, if the rebate output is set to *Item*, a sales order will be created and can be viewed via the target transactions.</span></span> <span data-ttu-id="d0416-245">或者，如果将付款设置为使用应付帐款，则将为客户返点创建在客户上设置的供应商的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="d0416-245">Alternatively, if the payment is set up to use Accounts payable, a vendor invoice for the vendor that is set up on the customer will be created for customer rebates.</span></span>

<span data-ttu-id="d0416-246">若要查看与返点管理交易相关联的日记帐条目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d0416-246">To review the journal entries that are associated with a Rebate management deal, follow these steps.</span></span>

1. <span data-ttu-id="d0416-247">针对要处理的交易类型打开适当的[返点交易列表页面](rebate-management-deals.md)。</span><span class="sxs-lookup"><span data-stu-id="d0416-247">Open the appropriate [rebate deals list page](rebate-management-deals.md) for the type of deal that you want to work with.</span></span>
1. <span data-ttu-id="d0416-248">选择要检查日记帐条目的交易。</span><span class="sxs-lookup"><span data-stu-id="d0416-248">Select the deal to inspect journal entries for.</span></span>
1. <span data-ttu-id="d0416-249">在操作窗格的 **返点管理交易** 选项卡上，在 **交易记录** 组中，选择 **交易记录** 或 **返点交易记录**，具体取决于要查看的交易记录的类型。</span><span class="sxs-lookup"><span data-stu-id="d0416-249">On the Action Pane, on the **Rebate management deals** tab, in the **Transactions** group, select either **Transactions** or **Rebate transactions**, depending on the type of transactions that you want to look at.</span></span>
1. <span data-ttu-id="d0416-250">确保 **显示** 字段设置为 *全部* 或 *已过帐*。</span><span class="sxs-lookup"><span data-stu-id="d0416-250">Make sure that the **Show** field is set to *All* or *Posted*.</span></span>
1. <span data-ttu-id="d0416-251">查找并选择要检查的交易记录集合，然后在操作窗格上，选择以下按钮之一。</span><span class="sxs-lookup"><span data-stu-id="d0416-251">Find and select the transaction collection that you want to inspect, and then, on the Action Pane, select one of the following buttons.</span></span> <span data-ttu-id="d0416-252">（仅当所选交易记录集合存在相关过帐时，这些按钮才可用。）</span><span class="sxs-lookup"><span data-stu-id="d0416-252">(These buttons are available only when relevant postings exist for the selected transaction collection.)</span></span>

    - <span data-ttu-id="d0416-253">**目标交易记录** – 审核选定交易生成的相关日记帐和其他类型的单据。</span><span class="sxs-lookup"><span data-stu-id="d0416-253">**Target transactions** – Review relevant journals and other types of documents that were generated by the selected deal.</span></span>
    - <span data-ttu-id="d0416-254">**项目** – 审核选定交易生成的相关项目。</span><span class="sxs-lookup"><span data-stu-id="d0416-254">**Items** – Review relevant items that were generated by the selected deal.</span></span>

1. <span data-ttu-id="d0416-255">显示相关日记帐、单据或项目的列表。</span><span class="sxs-lookup"><span data-stu-id="d0416-255">A list of relevant journals, documents, or items appears.</span></span> <span data-ttu-id="d0416-256">若要查看有关任何日记帐、单据或项目的详细信息，请选择其行，然后在操作窗格上选择 **查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="d0416-256">To view more information about any journal, document, or item, select its row, and then, on the Action Pane, select **View details**.</span></span>
