---
title: 存档库存交易记录
description: 本主题介绍如何存档库存交易记录数据以帮助提高系统性能。
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556407"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="f253a-103">存档库存交易记录</span><span class="sxs-lookup"><span data-stu-id="f253a-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f253a-104">随着时间的推移，库存交易记录表 (`InventTrans`) 会继续增长，消耗更多数据库空间。</span><span class="sxs-lookup"><span data-stu-id="f253a-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="f253a-105">因此，针对表进行的查询将逐渐变慢。</span><span class="sxs-lookup"><span data-stu-id="f253a-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="f253a-106">本主题介绍如何使用 *库存交易记录存档* 功能来存档有关库存交易记录的数据，以帮助提高系统性能。</span><span class="sxs-lookup"><span data-stu-id="f253a-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="f253a-107">只有财务更新的库存交易记录可以在选定的已关闭分类帐期间内存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="f253a-108">要进行存档，财务更新的出站库存交易记录的发货状态必须为 *已售出*，而入站库存交易记录的收货状态必须为 *已购买*。</span><span class="sxs-lookup"><span data-stu-id="f253a-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="f253a-109">存档库存交易记录时，所有相关交易记录都将移至 `InventTransArchive` 表。</span><span class="sxs-lookup"><span data-stu-id="f253a-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="f253a-110">库存发货交易记录和库存收货交易记录基于物料 ID (`itemId`) 和库存维度 ID (`inventDimId`) 的组合分别存档，并被放入汇总发货和汇总收货交易记录中。</span><span class="sxs-lookup"><span data-stu-id="f253a-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="f253a-111">如果 `itemId` 和 `inventDimId` 组合仅包含一个收货或发货交易记录，该交易记录将不会被存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="f253a-112">在系统中开启此功能</span><span class="sxs-lookup"><span data-stu-id="f253a-112">Turn on the feature in your system</span></span>

<span data-ttu-id="f253a-113">如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *库存交易记录存档* 功能。</span><span class="sxs-lookup"><span data-stu-id="f253a-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="f253a-114">存档库存交易记录之前要考虑的事项</span><span class="sxs-lookup"><span data-stu-id="f253a-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="f253a-115">在归档库存交易记录之前，应考虑以下业务场景，因为它们会受到操作的影响：</span><span class="sxs-lookup"><span data-stu-id="f253a-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="f253a-116">当您审计相关文档（如采购订单行）中的库存交易记录时，它们将显示为已存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="f253a-117">要查看已存档的交易记录，您必须转到 **库存管理 \> 定期任务 \> 清理 \> 库存交易记录存档**。</span><span class="sxs-lookup"><span data-stu-id="f253a-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="f253a-118">存档期间的库存结转无法取消。</span><span class="sxs-lookup"><span data-stu-id="f253a-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="f253a-119">您必须先撤消相关期间的库存交易记录存档，然后才可以取消库存结转。</span><span class="sxs-lookup"><span data-stu-id="f253a-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="f253a-120">存档期间无法执行标准成本转换。</span><span class="sxs-lookup"><span data-stu-id="f253a-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="f253a-121">您必须先撤消相关期间的库存交易记录存档，然后才可以执行标准成本转换。</span><span class="sxs-lookup"><span data-stu-id="f253a-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="f253a-122">存档库存交易记录时，源自库存交易记录的库存报表将受到影响。</span><span class="sxs-lookup"><span data-stu-id="f253a-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="f253a-123">这些报表包括库存帐龄报表和库存值报表。</span><span class="sxs-lookup"><span data-stu-id="f253a-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="f253a-124">如果库存预测在存档期间的时间范围内运行，可能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="f253a-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f253a-125">先决条件</span><span class="sxs-lookup"><span data-stu-id="f253a-125">Prerequisites</span></span>

<span data-ttu-id="f253a-126">库存交易记录只能在满足以下条件的期间存档：</span><span class="sxs-lookup"><span data-stu-id="f253a-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="f253a-127">分类帐期间必须已关闭。</span><span class="sxs-lookup"><span data-stu-id="f253a-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="f253a-128">库存结转必须在存档的到期日期或之后运行。</span><span class="sxs-lookup"><span data-stu-id="f253a-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="f253a-129">期间必须至少为存档起始日期之前一年。</span><span class="sxs-lookup"><span data-stu-id="f253a-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="f253a-130">不能进行任何现有的库存重新计算。</span><span class="sxs-lookup"><span data-stu-id="f253a-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="f253a-131">存档库存交易记录</span><span class="sxs-lookup"><span data-stu-id="f253a-131">Archive inventory transactions</span></span>

<span data-ttu-id="f253a-132">若要存档库存交易记录，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f253a-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="f253a-133">转到 **库存管理** \> **定期任务** \> **清理** \> **库存交易记录存档**。</span><span class="sxs-lookup"><span data-stu-id="f253a-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="f253a-134">**库存交易记录存档** 页将出现，显示已存档流程记录的列表。</span><span class="sxs-lookup"><span data-stu-id="f253a-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="f253a-135">![库存交易记录存档页](media/archive-inventory-empty.png "库存交易记录存档页")</span><span class="sxs-lookup"><span data-stu-id="f253a-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="f253a-136">在操作窗格上，选择 **库存交易记录存档** 创建库存交易记录存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="f253a-137">在 **库存交易记录存档** 对话框中，在 **参数** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f253a-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="f253a-138">**已关闭分类帐期间中的开始日期** – 选择要包括在存档中的最早的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="f253a-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="f253a-139">**已关闭分类帐期间中的结束日期** – 选择要包括在存档中的最晚的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="f253a-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="f253a-140">![库存交易记录存档对话框](media/archive-inventory-dates.png "库存交易记录存档对话框")</span><span class="sxs-lookup"><span data-stu-id="f253a-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="f253a-141">只有满足[先决条件](#prerequisites)的期间才可以选择。</span><span class="sxs-lookup"><span data-stu-id="f253a-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="f253a-142">在 **在后台运行** 快速选项卡上，根据需要设置批处理详细信息。</span><span class="sxs-lookup"><span data-stu-id="f253a-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="f253a-143">按照 Microsoft Dynamics 365 Supply Chain Management 中批处理作业的通常步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f253a-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="f253a-144">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f253a-144">Select **OK**.</span></span>
1. <span data-ttu-id="f253a-145">您将收到一条消息，提示您确认您希望继续。</span><span class="sxs-lookup"><span data-stu-id="f253a-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="f253a-146">仔细阅读消息，如果您希望继续，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="f253a-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="f253a-147">您将收到一条消息，指出您的库存交易记录存档作业已添加到批处理队列中。</span><span class="sxs-lookup"><span data-stu-id="f253a-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="f253a-148">此作业现在将开始存档所选期间的库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="f253a-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="f253a-149">查看已存档的库存交易记录</span><span class="sxs-lookup"><span data-stu-id="f253a-149">View archived inventory transactions</span></span>

<span data-ttu-id="f253a-150">**库存交易记录存档** 页将显示完整存档历史记录。</span><span class="sxs-lookup"><span data-stu-id="f253a-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="f253a-151">网格中的每一行显示存档创建日期、创建存档的用户以及存档的状态等信息。</span><span class="sxs-lookup"><span data-stu-id="f253a-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="f253a-152">![库存交易记录存档页上的存档历史记录](media/archive-inventory-full.png "库存交易记录存档页上的存档历史记录")</span><span class="sxs-lookup"><span data-stu-id="f253a-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="f253a-153">在页面顶部的下拉列表中，选择以下值之一以筛选显示在网格中的存档：</span><span class="sxs-lookup"><span data-stu-id="f253a-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="f253a-154">**活动** – 仅显示活动存档，不显示已撤消的存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="f253a-155">**所有** – 显示所有存档，包括活动和已撤消存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="f253a-156">对于网格中的每个存档，将提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="f253a-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="f253a-157">**活动** – 指示存档处于活动状态的复选标记。</span><span class="sxs-lookup"><span data-stu-id="f253a-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="f253a-158">**开始日期** – 可以包含在存档中的最早交易记录的日期。</span><span class="sxs-lookup"><span data-stu-id="f253a-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="f253a-159">**结束日期** – 可以包含在存档中的最近交易记录的日期。</span><span class="sxs-lookup"><span data-stu-id="f253a-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="f253a-160">**计划者** – 创建存档的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="f253a-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="f253a-161">**执行日期** – 存档创建的日期。</span><span class="sxs-lookup"><span data-stu-id="f253a-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="f253a-162">**撤消** – 指示存档已撤消的复选标记。</span><span class="sxs-lookup"><span data-stu-id="f253a-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="f253a-163">**停止当前更新** – 指示存档正在进行，但已暂停的复选标记。</span><span class="sxs-lookup"><span data-stu-id="f253a-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="f253a-164">**状态** – 存档的处理状态。</span><span class="sxs-lookup"><span data-stu-id="f253a-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="f253a-165">可能的值为 *等待*、*进行中* 和 *已完成*。</span><span class="sxs-lookup"><span data-stu-id="f253a-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="f253a-166">网格上方的工具栏提供以下按钮，可用于处理选定的存档：</span><span class="sxs-lookup"><span data-stu-id="f253a-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="f253a-167">**已存档的交易记录** – 查看所选存档的全部详细信息。</span><span class="sxs-lookup"><span data-stu-id="f253a-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="f253a-168">出现的 **已存档的交易记录** 页将显示存档中的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="f253a-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="f253a-169">![已存档的交易记录页](media/archive-inventory-transactions.png "已存档的交易记录页")</span><span class="sxs-lookup"><span data-stu-id="f253a-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="f253a-170">要在 **已存档的交易记录** 页上查看有关特定交易记录的详细信息，请在网格中选择它，然后在操作窗格上，选择 **已存档的交易记录详细信息**。</span><span class="sxs-lookup"><span data-stu-id="f253a-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="f253a-171">出现的 **已存档的交易记录详细信息** 页将显示分类帐过帐、相关子分类帐参考和财务维度等信息。</span><span class="sxs-lookup"><span data-stu-id="f253a-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="f253a-172">**暂停存档** – 暂停当前正在处理的选定存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="f253a-173">暂停仅在生成存档任务后生效。</span><span class="sxs-lookup"><span data-stu-id="f253a-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="f253a-174">因此，暂停生效之前可能会有短暂的延迟。</span><span class="sxs-lookup"><span data-stu-id="f253a-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="f253a-175">如果存档已暂停，**停止当前更新** 字段中会出现一个复选标记。</span><span class="sxs-lookup"><span data-stu-id="f253a-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="f253a-176">**恢复存档** – 恢复当前暂停的选定存档的处理。</span><span class="sxs-lookup"><span data-stu-id="f253a-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="f253a-177">**撤消** – 撤消所选择的存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="f253a-178">仅当存档的 **状态** 字段设置为 *已完成* 时，才可以撤消存档。</span><span class="sxs-lookup"><span data-stu-id="f253a-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="f253a-179">如果存档已撤消，**撤消** 字段中会出现一个复选标记。</span><span class="sxs-lookup"><span data-stu-id="f253a-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
