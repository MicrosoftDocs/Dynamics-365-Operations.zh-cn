---
title: 条码扫描仪的看板转移面板支持
description: 看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7073fb5d77e2d11569e86b92433864371f0e1d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825859"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="161e5-103">条码扫描仪的看板转移面板支持</span><span class="sxs-lookup"><span data-stu-id="161e5-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="161e5-104">看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。</span><span class="sxs-lookup"><span data-stu-id="161e5-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="161e5-105">登记模式</span><span class="sxs-lookup"><span data-stu-id="161e5-105">Registration modes</span></span>
------------------

<span data-ttu-id="161e5-106">在 **扫描仪登记** 快速选项卡中，您可以选择登记模式，其控制您扫描看板卡号或在“看板卡号”字段中手动输入该编号的操作。</span><span class="sxs-lookup"><span data-stu-id="161e5-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="161e5-107">设置登记模式</span><span class="sxs-lookup"><span data-stu-id="161e5-107">Set registration mode</span></span> | <span data-ttu-id="161e5-108">描述</span><span class="sxs-lookup"><span data-stu-id="161e5-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="161e5-109">启动</span><span class="sxs-lookup"><span data-stu-id="161e5-109">Start</span></span>                 | <span data-ttu-id="161e5-110">将看板转移作业登记为进行中。</span><span class="sxs-lookup"><span data-stu-id="161e5-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="161e5-111">已完成</span><span class="sxs-lookup"><span data-stu-id="161e5-111">Complete</span></span>              | <span data-ttu-id="161e5-112">将看板转移作业登记为已完成。</span><span class="sxs-lookup"><span data-stu-id="161e5-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="161e5-113">空</span><span class="sxs-lookup"><span data-stu-id="161e5-113">Empty</span></span>                 | <span data-ttu-id="161e5-114">将由看板卡引用的物料处理单元登记为空。</span><span class="sxs-lookup"><span data-stu-id="161e5-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="161e5-115">选择</span><span class="sxs-lookup"><span data-stu-id="161e5-115">Select</span></span>                | <span data-ttu-id="161e5-116">登记看板卡号并在看板列表中自动选择引用的作业。</span><span class="sxs-lookup"><span data-stu-id="161e5-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="161e5-117">登记模式选择</span><span class="sxs-lookup"><span data-stu-id="161e5-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="161e5-118">当您使用条码阅读器选择作业时，看板面板的显示方式更改。</span><span class="sxs-lookup"><span data-stu-id="161e5-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="161e5-119">在此模式中，以下条件适用：</span><span class="sxs-lookup"><span data-stu-id="161e5-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="161e5-120">仅显示扫描的看板作业。</span><span class="sxs-lookup"><span data-stu-id="161e5-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="161e5-121">所选作业的详细信息显示在 **详细信息** 快速选项卡中。</span><span class="sxs-lookup"><span data-stu-id="161e5-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="161e5-122">**消息** 快速选项卡只为所选作业显示消息。</span><span class="sxs-lookup"><span data-stu-id="161e5-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="161e5-123">您可以通过使用操作窗格上提供的功能更改作业的状态。</span><span class="sxs-lookup"><span data-stu-id="161e5-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="161e5-124">看板转移面板在此时间只显示单个作业。</span><span class="sxs-lookup"><span data-stu-id="161e5-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="161e5-125">您可以通过单击操作窗格的 **刷新** (Shift+F5) 手动更新作业列表中的信息。</span><span class="sxs-lookup"><span data-stu-id="161e5-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="161e5-126">在刷新信息后，作业筛选器的完整结果再次将显示。</span><span class="sxs-lookup"><span data-stu-id="161e5-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="161e5-127">作业状态和可能的操作</span><span class="sxs-lookup"><span data-stu-id="161e5-127">Job status and possible actions</span></span>
<span data-ttu-id="161e5-128">所选作业的状态和事件看板的任何限定作业的状态确定是否可以进一步处理作业。</span><span class="sxs-lookup"><span data-stu-id="161e5-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="161e5-129">下表显示有关这些状态和任务的信息：</span><span class="sxs-lookup"><span data-stu-id="161e5-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="161e5-130">可用与作业或可用于作业引用的处理单元的状态。</span><span class="sxs-lookup"><span data-stu-id="161e5-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="161e5-131">您可为作业执行的每个任务。</span><span class="sxs-lookup"><span data-stu-id="161e5-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="161e5-132">作业类型</span><span class="sxs-lookup"><span data-stu-id="161e5-132">Job type</span></span></th>
<th><span data-ttu-id="161e5-133">作业状态或处理单元状态</span><span class="sxs-lookup"><span data-stu-id="161e5-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="161e5-134">更新领料单</span><span class="sxs-lookup"><span data-stu-id="161e5-134">Update picking list</span></span></th>
<th><span data-ttu-id="161e5-135">启动</span><span class="sxs-lookup"><span data-stu-id="161e5-135">Start</span></span></th>
<th><span data-ttu-id="161e5-136">更新登记</span><span class="sxs-lookup"><span data-stu-id="161e5-136">Update registration</span></span></th>
<th><span data-ttu-id="161e5-137">已完成</span><span class="sxs-lookup"><span data-stu-id="161e5-137">Complete</span></span></th>
<th><span data-ttu-id="161e5-138">空</span><span class="sxs-lookup"><span data-stu-id="161e5-138">Empty</span></span></th>
<th><span data-ttu-id="161e5-139">创建事件看板</span><span class="sxs-lookup"><span data-stu-id="161e5-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="161e5-140">转移</span><span class="sxs-lookup"><span data-stu-id="161e5-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="161e5-141">未计划</span><span class="sxs-lookup"><span data-stu-id="161e5-141">Not planned</span></span></li>
<li><span data-ttu-id="161e5-142">无限定的作业或限定的作业已完成</span><span class="sxs-lookup"><span data-stu-id="161e5-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="161e5-143">是</span><span class="sxs-lookup"><span data-stu-id="161e5-143">Yes</span></span></td>
<td><span data-ttu-id="161e5-144">是</span><span class="sxs-lookup"><span data-stu-id="161e5-144">Yes</span></span></td>
<td><span data-ttu-id="161e5-145">是</span><span class="sxs-lookup"><span data-stu-id="161e5-145">Yes</span></span></td>
<td><span data-ttu-id="161e5-146">是</span><span class="sxs-lookup"><span data-stu-id="161e5-146">Yes</span></span></td>
<td><span data-ttu-id="161e5-147">否</span><span class="sxs-lookup"><span data-stu-id="161e5-147">No</span></span></td>
<td><span data-ttu-id="161e5-148">是</span><span class="sxs-lookup"><span data-stu-id="161e5-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="161e5-149">转移</span><span class="sxs-lookup"><span data-stu-id="161e5-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="161e5-150">未计划</span><span class="sxs-lookup"><span data-stu-id="161e5-150">Not planned</span></span></li>
<li><span data-ttu-id="161e5-151">限定的作业未完成</span><span class="sxs-lookup"><span data-stu-id="161e5-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="161e5-152">是</span><span class="sxs-lookup"><span data-stu-id="161e5-152">Yes</span></span></td>
<td><span data-ttu-id="161e5-153">否</span><span class="sxs-lookup"><span data-stu-id="161e5-153">No</span></span></td>
<td><span data-ttu-id="161e5-154">是</span><span class="sxs-lookup"><span data-stu-id="161e5-154">Yes</span></span></td>
<td><span data-ttu-id="161e5-155">否</span><span class="sxs-lookup"><span data-stu-id="161e5-155">No</span></span></td>
<td><span data-ttu-id="161e5-156">否</span><span class="sxs-lookup"><span data-stu-id="161e5-156">No</span></span></td>
<td><span data-ttu-id="161e5-157">否</span><span class="sxs-lookup"><span data-stu-id="161e5-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="161e5-158">转移</span><span class="sxs-lookup"><span data-stu-id="161e5-158">Transfer</span></span></td>
<td><span data-ttu-id="161e5-159">进行中</span><span class="sxs-lookup"><span data-stu-id="161e5-159">In progress</span></span></td>
<td><span data-ttu-id="161e5-160">是</span><span class="sxs-lookup"><span data-stu-id="161e5-160">Yes</span></span></td>
<td><span data-ttu-id="161e5-161">否</span><span class="sxs-lookup"><span data-stu-id="161e5-161">No</span></span></td>
<td><span data-ttu-id="161e5-162">是</span><span class="sxs-lookup"><span data-stu-id="161e5-162">Yes</span></span></td>
<td><span data-ttu-id="161e5-163">是</span><span class="sxs-lookup"><span data-stu-id="161e5-163">Yes</span></span></td>
<td><span data-ttu-id="161e5-164">否</span><span class="sxs-lookup"><span data-stu-id="161e5-164">No</span></span></td>
<td><span data-ttu-id="161e5-165">否</span><span class="sxs-lookup"><span data-stu-id="161e5-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="161e5-166">转移</span><span class="sxs-lookup"><span data-stu-id="161e5-166">Transfer</span></span></td>
<td><span data-ttu-id="161e5-167">已完成</span><span class="sxs-lookup"><span data-stu-id="161e5-167">Completed</span></span></td>
<td><span data-ttu-id="161e5-168">否</span><span class="sxs-lookup"><span data-stu-id="161e5-168">No</span></span></td>
<td><span data-ttu-id="161e5-169">否</span><span class="sxs-lookup"><span data-stu-id="161e5-169">No</span></span></td>
<td><span data-ttu-id="161e5-170">否</span><span class="sxs-lookup"><span data-stu-id="161e5-170">No</span></span></td>
<td><span data-ttu-id="161e5-171">否</span><span class="sxs-lookup"><span data-stu-id="161e5-171">No</span></span></td>
<td><span data-ttu-id="161e5-172">是</span><span class="sxs-lookup"><span data-stu-id="161e5-172">Yes</span></span></td>
<td><span data-ttu-id="161e5-173">否</span><span class="sxs-lookup"><span data-stu-id="161e5-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="161e5-174">转换或处理</span><span class="sxs-lookup"><span data-stu-id="161e5-174">Transfer or process</span></span></td>
<td><span data-ttu-id="161e5-175">空</span><span class="sxs-lookup"><span data-stu-id="161e5-175">Empty</span></span></td>
<td><span data-ttu-id="161e5-176">否</span><span class="sxs-lookup"><span data-stu-id="161e5-176">No</span></span></td>
<td><span data-ttu-id="161e5-177">否</span><span class="sxs-lookup"><span data-stu-id="161e5-177">No</span></span></td>
<td><span data-ttu-id="161e5-178">否</span><span class="sxs-lookup"><span data-stu-id="161e5-178">No</span></span></td>
<td><span data-ttu-id="161e5-179">否</span><span class="sxs-lookup"><span data-stu-id="161e5-179">No</span></span></td>
<td><span data-ttu-id="161e5-180">否</span><span class="sxs-lookup"><span data-stu-id="161e5-180">No</span></span></td>
<td><span data-ttu-id="161e5-181">否</span><span class="sxs-lookup"><span data-stu-id="161e5-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="161e5-182">转换或处理</span><span class="sxs-lookup"><span data-stu-id="161e5-182">Transfer or process</span></span></td>
<td><span data-ttu-id="161e5-183">找不到看板卡</span><span class="sxs-lookup"><span data-stu-id="161e5-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="161e5-184">否</span><span class="sxs-lookup"><span data-stu-id="161e5-184">No</span></span></td>
<td><span data-ttu-id="161e5-185">否</span><span class="sxs-lookup"><span data-stu-id="161e5-185">No</span></span></td>
<td><span data-ttu-id="161e5-186">否</span><span class="sxs-lookup"><span data-stu-id="161e5-186">No</span></span></td>
<td><span data-ttu-id="161e5-187">否</span><span class="sxs-lookup"><span data-stu-id="161e5-187">No</span></span></td>
<td><span data-ttu-id="161e5-188">否</span><span class="sxs-lookup"><span data-stu-id="161e5-188">No</span></span></td>
<td><span data-ttu-id="161e5-189">否</span><span class="sxs-lookup"><span data-stu-id="161e5-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="161e5-190">转换或处理</span><span class="sxs-lookup"><span data-stu-id="161e5-190">Transfer or process</span></span></td>
<td><span data-ttu-id="161e5-191">找到看板卡，但为分配给看板。</span><span class="sxs-lookup"><span data-stu-id="161e5-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="161e5-192">否</span><span class="sxs-lookup"><span data-stu-id="161e5-192">No</span></span></td>
<td><span data-ttu-id="161e5-193">否</span><span class="sxs-lookup"><span data-stu-id="161e5-193">No</span></span></td>
<td><span data-ttu-id="161e5-194">否</span><span class="sxs-lookup"><span data-stu-id="161e5-194">No</span></span></td>
<td><span data-ttu-id="161e5-195">否</span><span class="sxs-lookup"><span data-stu-id="161e5-195">No</span></span></td>
<td><span data-ttu-id="161e5-196">否</span><span class="sxs-lookup"><span data-stu-id="161e5-196">No</span></span></td>
<td><span data-ttu-id="161e5-197">否</span><span class="sxs-lookup"><span data-stu-id="161e5-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="161e5-198">处理</span><span class="sxs-lookup"><span data-stu-id="161e5-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="161e5-199">未计划</span><span class="sxs-lookup"><span data-stu-id="161e5-199">Not planned</span></span></li>
<li><span data-ttu-id="161e5-200">已准备</span><span class="sxs-lookup"><span data-stu-id="161e5-200">Prepared</span></span></li>
<li><span data-ttu-id="161e5-201">进行中</span><span class="sxs-lookup"><span data-stu-id="161e5-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="161e5-202">否</span><span class="sxs-lookup"><span data-stu-id="161e5-202">No</span></span></td>
<td><span data-ttu-id="161e5-203">否</span><span class="sxs-lookup"><span data-stu-id="161e5-203">No</span></span></td>
<td><span data-ttu-id="161e5-204">否</span><span class="sxs-lookup"><span data-stu-id="161e5-204">No</span></span></td>
<td><span data-ttu-id="161e5-205">否</span><span class="sxs-lookup"><span data-stu-id="161e5-205">No</span></span></td>
<td><span data-ttu-id="161e5-206">否</span><span class="sxs-lookup"><span data-stu-id="161e5-206">No</span></span></td>
<td><span data-ttu-id="161e5-207">否</span><span class="sxs-lookup"><span data-stu-id="161e5-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="161e5-208">处理</span><span class="sxs-lookup"><span data-stu-id="161e5-208">Process</span></span></td>
<td><span data-ttu-id="161e5-209">已完成</span><span class="sxs-lookup"><span data-stu-id="161e5-209">Completed</span></span></td>
<td><span data-ttu-id="161e5-210">否</span><span class="sxs-lookup"><span data-stu-id="161e5-210">No</span></span></td>
<td><span data-ttu-id="161e5-211">否</span><span class="sxs-lookup"><span data-stu-id="161e5-211">No</span></span></td>
<td><span data-ttu-id="161e5-212">否</span><span class="sxs-lookup"><span data-stu-id="161e5-212">No</span></span></td>
<td><span data-ttu-id="161e5-213">否</span><span class="sxs-lookup"><span data-stu-id="161e5-213">No</span></span></td>
<td><span data-ttu-id="161e5-214">否</span><span class="sxs-lookup"><span data-stu-id="161e5-214">No</span></span></td>
<td><span data-ttu-id="161e5-215">否</span><span class="sxs-lookup"><span data-stu-id="161e5-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]