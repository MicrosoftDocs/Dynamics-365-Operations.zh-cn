---
title: "条码扫描仪的看板转移面板支持"
description: "看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1dc40de2b77be5c5c2399fd55c3c3bd15a9f24ec
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="ea800-103">条码扫描仪的看板转移面板支持</span><span class="sxs-lookup"><span data-stu-id="ea800-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ea800-104">看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。</span><span class="sxs-lookup"><span data-stu-id="ea800-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="ea800-105">登记模式</span><span class="sxs-lookup"><span data-stu-id="ea800-105">Registration modes</span></span>
------------------

<span data-ttu-id="ea800-106">在**扫描仪登记**快速选项卡中，您可以选择登记模式，其控制您扫描看板卡号或在“看板卡号”字段中手动输入该编号的操作。</span><span class="sxs-lookup"><span data-stu-id="ea800-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="ea800-107">设置登记模式</span><span class="sxs-lookup"><span data-stu-id="ea800-107">Set registration mode</span></span> | <span data-ttu-id="ea800-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea800-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea800-109">启动</span><span class="sxs-lookup"><span data-stu-id="ea800-109">Start</span></span>                 | <span data-ttu-id="ea800-110">将看板转移作业登记为进行中。</span><span class="sxs-lookup"><span data-stu-id="ea800-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="ea800-111">已完成</span><span class="sxs-lookup"><span data-stu-id="ea800-111">Complete</span></span>              | <span data-ttu-id="ea800-112">将看板转移作业登记为已完成。</span><span class="sxs-lookup"><span data-stu-id="ea800-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="ea800-113">空</span><span class="sxs-lookup"><span data-stu-id="ea800-113">Empty</span></span>                 | <span data-ttu-id="ea800-114">将由看板卡引用的物料处理单元登记为空。</span><span class="sxs-lookup"><span data-stu-id="ea800-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="ea800-115">选择</span><span class="sxs-lookup"><span data-stu-id="ea800-115">Select</span></span>                | <span data-ttu-id="ea800-116">登记看板卡号并在看板列表中自动选择引用的作业。</span><span class="sxs-lookup"><span data-stu-id="ea800-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="ea800-117">登记模式选择</span><span class="sxs-lookup"><span data-stu-id="ea800-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="ea800-118">当您使用条码阅读器选择作业时，看板面板的显示方式更改。</span><span class="sxs-lookup"><span data-stu-id="ea800-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="ea800-119">在此模式中，以下条件适用：</span><span class="sxs-lookup"><span data-stu-id="ea800-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="ea800-120">仅显示扫描的看板作业。</span><span class="sxs-lookup"><span data-stu-id="ea800-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="ea800-121">所选作业的详细信息显示在**详细信息**快速选项卡中。</span><span class="sxs-lookup"><span data-stu-id="ea800-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="ea800-122">**消息**快速选项卡只为所选作业显示消息。</span><span class="sxs-lookup"><span data-stu-id="ea800-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="ea800-123">您可以通过使用操作窗格上提供的功能更改作业的状态。</span><span class="sxs-lookup"><span data-stu-id="ea800-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="ea800-124">看板转移面板在此时间只显示单个作业。</span><span class="sxs-lookup"><span data-stu-id="ea800-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="ea800-125">您可以通过单击操作窗格的**刷新** (Shift+F5) 手动更新作业列表中的信息。</span><span class="sxs-lookup"><span data-stu-id="ea800-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="ea800-126">在刷新信息后，作业筛选器的完整结果再次将显示。</span><span class="sxs-lookup"><span data-stu-id="ea800-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="ea800-127">作业状态和可能的操作</span><span class="sxs-lookup"><span data-stu-id="ea800-127">Job status and possible actions</span></span>
<span data-ttu-id="ea800-128">所选作业的状态和事件看板的任何限定作业的状态确定是否可以进一步处理作业。</span><span class="sxs-lookup"><span data-stu-id="ea800-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="ea800-129">下表显示有关这些状态和任务的信息：</span><span class="sxs-lookup"><span data-stu-id="ea800-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="ea800-130">可用与作业或可用于作业引用的处理单元的状态。</span><span class="sxs-lookup"><span data-stu-id="ea800-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="ea800-131">您可为作业执行的每个任务。</span><span class="sxs-lookup"><span data-stu-id="ea800-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="ea800-132">作业类型</span><span class="sxs-lookup"><span data-stu-id="ea800-132">Job type</span></span></th>
<th><span data-ttu-id="ea800-133">作业状态或处理单元状态</span><span class="sxs-lookup"><span data-stu-id="ea800-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="ea800-134">更新领料单</span><span class="sxs-lookup"><span data-stu-id="ea800-134">Update picking list</span></span></th>
<th><span data-ttu-id="ea800-135">启动</span><span class="sxs-lookup"><span data-stu-id="ea800-135">Start</span></span></th>
<th><span data-ttu-id="ea800-136">更新登记</span><span class="sxs-lookup"><span data-stu-id="ea800-136">Update registration</span></span></th>
<th><span data-ttu-id="ea800-137">已完成</span><span class="sxs-lookup"><span data-stu-id="ea800-137">Complete</span></span></th>
<th><span data-ttu-id="ea800-138">空</span><span class="sxs-lookup"><span data-stu-id="ea800-138">Empty</span></span></th>
<th><span data-ttu-id="ea800-139">创建事件看板</span><span class="sxs-lookup"><span data-stu-id="ea800-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea800-140">转移</span><span class="sxs-lookup"><span data-stu-id="ea800-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="ea800-141">未计划</span><span class="sxs-lookup"><span data-stu-id="ea800-141">Not planned</span></span></li>
<li><span data-ttu-id="ea800-142">无限定的作业或限定的作业已完成</span><span class="sxs-lookup"><span data-stu-id="ea800-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="ea800-143">是</span><span class="sxs-lookup"><span data-stu-id="ea800-143">Yes</span></span></td>
<td><span data-ttu-id="ea800-144">是</span><span class="sxs-lookup"><span data-stu-id="ea800-144">Yes</span></span></td>
<td><span data-ttu-id="ea800-145">是</span><span class="sxs-lookup"><span data-stu-id="ea800-145">Yes</span></span></td>
<td><span data-ttu-id="ea800-146">是</span><span class="sxs-lookup"><span data-stu-id="ea800-146">Yes</span></span></td>
<td><span data-ttu-id="ea800-147">否</span><span class="sxs-lookup"><span data-stu-id="ea800-147">No</span></span></td>
<td><span data-ttu-id="ea800-148">是</span><span class="sxs-lookup"><span data-stu-id="ea800-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea800-149">转移</span><span class="sxs-lookup"><span data-stu-id="ea800-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="ea800-150">未计划</span><span class="sxs-lookup"><span data-stu-id="ea800-150">Not planned</span></span></li>
<li><span data-ttu-id="ea800-151">限定的作业未完成</span><span class="sxs-lookup"><span data-stu-id="ea800-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="ea800-152">是</span><span class="sxs-lookup"><span data-stu-id="ea800-152">Yes</span></span></td>
<td><span data-ttu-id="ea800-153">否</span><span class="sxs-lookup"><span data-stu-id="ea800-153">No</span></span></td>
<td><span data-ttu-id="ea800-154">是</span><span class="sxs-lookup"><span data-stu-id="ea800-154">Yes</span></span></td>
<td><span data-ttu-id="ea800-155">否</span><span class="sxs-lookup"><span data-stu-id="ea800-155">No</span></span></td>
<td><span data-ttu-id="ea800-156">否</span><span class="sxs-lookup"><span data-stu-id="ea800-156">No</span></span></td>
<td><span data-ttu-id="ea800-157">否</span><span class="sxs-lookup"><span data-stu-id="ea800-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea800-158">转移</span><span class="sxs-lookup"><span data-stu-id="ea800-158">Transfer</span></span></td>
<td><span data-ttu-id="ea800-159">进行中</span><span class="sxs-lookup"><span data-stu-id="ea800-159">In progress</span></span></td>
<td><span data-ttu-id="ea800-160">是</span><span class="sxs-lookup"><span data-stu-id="ea800-160">Yes</span></span></td>
<td><span data-ttu-id="ea800-161">否</span><span class="sxs-lookup"><span data-stu-id="ea800-161">No</span></span></td>
<td><span data-ttu-id="ea800-162">是</span><span class="sxs-lookup"><span data-stu-id="ea800-162">Yes</span></span></td>
<td><span data-ttu-id="ea800-163">是</span><span class="sxs-lookup"><span data-stu-id="ea800-163">Yes</span></span></td>
<td><span data-ttu-id="ea800-164">否</span><span class="sxs-lookup"><span data-stu-id="ea800-164">No</span></span></td>
<td><span data-ttu-id="ea800-165">否</span><span class="sxs-lookup"><span data-stu-id="ea800-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea800-166">转移</span><span class="sxs-lookup"><span data-stu-id="ea800-166">Transfer</span></span></td>
<td><span data-ttu-id="ea800-167">已完成</span><span class="sxs-lookup"><span data-stu-id="ea800-167">Completed</span></span></td>
<td><span data-ttu-id="ea800-168">否</span><span class="sxs-lookup"><span data-stu-id="ea800-168">No</span></span></td>
<td><span data-ttu-id="ea800-169">否</span><span class="sxs-lookup"><span data-stu-id="ea800-169">No</span></span></td>
<td><span data-ttu-id="ea800-170">否</span><span class="sxs-lookup"><span data-stu-id="ea800-170">No</span></span></td>
<td><span data-ttu-id="ea800-171">否</span><span class="sxs-lookup"><span data-stu-id="ea800-171">No</span></span></td>
<td><span data-ttu-id="ea800-172">是</span><span class="sxs-lookup"><span data-stu-id="ea800-172">Yes</span></span></td>
<td><span data-ttu-id="ea800-173">否</span><span class="sxs-lookup"><span data-stu-id="ea800-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea800-174">转换或处理</span><span class="sxs-lookup"><span data-stu-id="ea800-174">Transfer or process</span></span></td>
<td><span data-ttu-id="ea800-175">空</span><span class="sxs-lookup"><span data-stu-id="ea800-175">Empty</span></span></td>
<td><span data-ttu-id="ea800-176">否</span><span class="sxs-lookup"><span data-stu-id="ea800-176">No</span></span></td>
<td><span data-ttu-id="ea800-177">否</span><span class="sxs-lookup"><span data-stu-id="ea800-177">No</span></span></td>
<td><span data-ttu-id="ea800-178">否</span><span class="sxs-lookup"><span data-stu-id="ea800-178">No</span></span></td>
<td><span data-ttu-id="ea800-179">否</span><span class="sxs-lookup"><span data-stu-id="ea800-179">No</span></span></td>
<td><span data-ttu-id="ea800-180">否</span><span class="sxs-lookup"><span data-stu-id="ea800-180">No</span></span></td>
<td><span data-ttu-id="ea800-181">否</span><span class="sxs-lookup"><span data-stu-id="ea800-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea800-182">转换或处理</span><span class="sxs-lookup"><span data-stu-id="ea800-182">Transfer or process</span></span></td>
<td><span data-ttu-id="ea800-183">找不到看板卡</span><span class="sxs-lookup"><span data-stu-id="ea800-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="ea800-184">否</span><span class="sxs-lookup"><span data-stu-id="ea800-184">No</span></span></td>
<td><span data-ttu-id="ea800-185">否</span><span class="sxs-lookup"><span data-stu-id="ea800-185">No</span></span></td>
<td><span data-ttu-id="ea800-186">否</span><span class="sxs-lookup"><span data-stu-id="ea800-186">No</span></span></td>
<td><span data-ttu-id="ea800-187">否</span><span class="sxs-lookup"><span data-stu-id="ea800-187">No</span></span></td>
<td><span data-ttu-id="ea800-188">否</span><span class="sxs-lookup"><span data-stu-id="ea800-188">No</span></span></td>
<td><span data-ttu-id="ea800-189">否</span><span class="sxs-lookup"><span data-stu-id="ea800-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea800-190">转换或处理</span><span class="sxs-lookup"><span data-stu-id="ea800-190">Transfer or process</span></span></td>
<td><span data-ttu-id="ea800-191">找到看板卡，但为分配给看板。</span><span class="sxs-lookup"><span data-stu-id="ea800-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="ea800-192">否</span><span class="sxs-lookup"><span data-stu-id="ea800-192">No</span></span></td>
<td><span data-ttu-id="ea800-193">否</span><span class="sxs-lookup"><span data-stu-id="ea800-193">No</span></span></td>
<td><span data-ttu-id="ea800-194">否</span><span class="sxs-lookup"><span data-stu-id="ea800-194">No</span></span></td>
<td><span data-ttu-id="ea800-195">否</span><span class="sxs-lookup"><span data-stu-id="ea800-195">No</span></span></td>
<td><span data-ttu-id="ea800-196">否</span><span class="sxs-lookup"><span data-stu-id="ea800-196">No</span></span></td>
<td><span data-ttu-id="ea800-197">否</span><span class="sxs-lookup"><span data-stu-id="ea800-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea800-198">处理</span><span class="sxs-lookup"><span data-stu-id="ea800-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="ea800-199">未计划</span><span class="sxs-lookup"><span data-stu-id="ea800-199">Not planned</span></span></li>
<li><span data-ttu-id="ea800-200">已准备</span><span class="sxs-lookup"><span data-stu-id="ea800-200">Prepared</span></span></li>
<li><span data-ttu-id="ea800-201">进行中</span><span class="sxs-lookup"><span data-stu-id="ea800-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="ea800-202">否</span><span class="sxs-lookup"><span data-stu-id="ea800-202">No</span></span></td>
<td><span data-ttu-id="ea800-203">否</span><span class="sxs-lookup"><span data-stu-id="ea800-203">No</span></span></td>
<td><span data-ttu-id="ea800-204">否</span><span class="sxs-lookup"><span data-stu-id="ea800-204">No</span></span></td>
<td><span data-ttu-id="ea800-205">否</span><span class="sxs-lookup"><span data-stu-id="ea800-205">No</span></span></td>
<td><span data-ttu-id="ea800-206">否</span><span class="sxs-lookup"><span data-stu-id="ea800-206">No</span></span></td>
<td><span data-ttu-id="ea800-207">否</span><span class="sxs-lookup"><span data-stu-id="ea800-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea800-208">处理</span><span class="sxs-lookup"><span data-stu-id="ea800-208">Process</span></span></td>
<td><span data-ttu-id="ea800-209">已完成</span><span class="sxs-lookup"><span data-stu-id="ea800-209">Completed</span></span></td>
<td><span data-ttu-id="ea800-210">否</span><span class="sxs-lookup"><span data-stu-id="ea800-210">No</span></span></td>
<td><span data-ttu-id="ea800-211">否</span><span class="sxs-lookup"><span data-stu-id="ea800-211">No</span></span></td>
<td><span data-ttu-id="ea800-212">否</span><span class="sxs-lookup"><span data-stu-id="ea800-212">No</span></span></td>
<td><span data-ttu-id="ea800-213">否</span><span class="sxs-lookup"><span data-stu-id="ea800-213">No</span></span></td>
<td><span data-ttu-id="ea800-214">否</span><span class="sxs-lookup"><span data-stu-id="ea800-214">No</span></span></td>
<td><span data-ttu-id="ea800-215">否</span><span class="sxs-lookup"><span data-stu-id="ea800-215">No</span></span></td>
</tr>
</tbody>
</table>






