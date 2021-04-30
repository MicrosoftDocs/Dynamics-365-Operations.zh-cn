---
title: Cloud Scale Unit 和 Edge Scale Unit 的制造执行工作负荷
description: 本主题介绍制造执行工作负荷如何使用 Cloud Scale Unit 和 Edge Scale Unit。
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a6d6979093c67d2d89b88678712f4c0205c63194
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899087"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="914e5-103">云和边缘缩放单元的制造执行工作负载</span><span class="sxs-lookup"><span data-stu-id="914e5-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="914e5-104">此时，制造执行工作负荷在预览状态下可用。</span><span class="sxs-lookup"><span data-stu-id="914e5-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="914e5-105">当使用工作负荷缩放单元时，公开预览版中不完全支持某些业务功能。</span><span class="sxs-lookup"><span data-stu-id="914e5-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="914e5-106">在制造执行中，缩放单元提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="914e5-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="914e5-107">机器操作员和车间主管可以访问操作生产计划。</span><span class="sxs-lookup"><span data-stu-id="914e5-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="914e5-108">机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。</span><span class="sxs-lookup"><span data-stu-id="914e5-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="914e5-109">车间主管可以调整操作计划。</span><span class="sxs-lookup"><span data-stu-id="914e5-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="914e5-110">工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。</span><span class="sxs-lookup"><span data-stu-id="914e5-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="914e5-111">本主题介绍制造执行工作负荷如何使用 Cloud Scale Unit 和 Edge Scale Unit。</span><span class="sxs-lookup"><span data-stu-id="914e5-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="914e5-112">制造生命周期</span><span class="sxs-lookup"><span data-stu-id="914e5-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="914e5-113">如下图所示，制造生命周期分为三个阶段：*计划*、*执行* 和 *完成*。</span><span class="sxs-lookup"><span data-stu-id="914e5-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="914e5-114">[![使用单个环境时的制造执行阶段](media/mes-phases.png "使用单个环境时的制造执行阶段")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="914e5-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="914e5-115">_计划_ 阶段包括产品定义、计划、订单创建和计划编制以及发放。</span><span class="sxs-lookup"><span data-stu-id="914e5-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="914e5-116">发放步骤指示从 _计划_ 阶段转换为 _执行_ 阶段。</span><span class="sxs-lookup"><span data-stu-id="914e5-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="914e5-117">发放生产订单后，生产订单作业将在生产车间可见并准备好执行。</span><span class="sxs-lookup"><span data-stu-id="914e5-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="914e5-118">当生产作业标记为已完成时，它将从 _执行_ 阶段移动到 _完成_ 阶段。</span><span class="sxs-lookup"><span data-stu-id="914e5-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="914e5-119">在 _完成_ 阶段中，*执行* 阶段中的登记将完成审批工作流，在该工作流中计算、批准和传输它们。</span><span class="sxs-lookup"><span data-stu-id="914e5-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="914e5-120">此时，生产订单已完成。</span><span class="sxs-lookup"><span data-stu-id="914e5-120">At that point, the production order is completed.</span></span> <span data-ttu-id="914e5-121">因此，将生成工作人员工资的基础。</span><span class="sxs-lookup"><span data-stu-id="914e5-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="914e5-122">将执行阶段拆分为单独的工作负荷</span><span class="sxs-lookup"><span data-stu-id="914e5-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="914e5-123">如下图所示，使用缩放单元时，_执行_ 阶段将拆分为单独的工作负荷。</span><span class="sxs-lookup"><span data-stu-id="914e5-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="914e5-124">[![使用缩放单元时的制造执行阶段](media/mes-phases-workloads.png "使用缩放单元时的制造执行阶段")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="914e5-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="914e5-125">现在，该模型将从单实例安装变为基于中心和缩放单元的模型。</span><span class="sxs-lookup"><span data-stu-id="914e5-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="914e5-126">_计划_ 和 _完成_ 阶段在中心上作为后台操作运行，制造执行工作负荷在缩放单元上运行。</span><span class="sxs-lookup"><span data-stu-id="914e5-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="914e5-127">在中心和缩放单元之间异步传输数据。</span><span class="sxs-lookup"><span data-stu-id="914e5-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="914e5-128">在中心上发放生产订单后，处理生产作业所需的所有数据都将传输到缩放单元。</span><span class="sxs-lookup"><span data-stu-id="914e5-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="914e5-129">此数据包括生产订单、生产工艺路线、物料清单和产品。</span><span class="sxs-lookup"><span data-stu-id="914e5-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="914e5-130">与生产订单无关的数据（例如间接活动、缺勤代码和生产参数）也将从中心传输到缩放单元。</span><span class="sxs-lookup"><span data-stu-id="914e5-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="914e5-131">通常，只能在中心上创建或更新源自中心且传输到缩放单元的数据。</span><span class="sxs-lookup"><span data-stu-id="914e5-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="914e5-132">例如，不能在缩放单元上创建新的缺勤代码或间接活动&mdash;它们只能用于登记。</span><span class="sxs-lookup"><span data-stu-id="914e5-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="914e5-133">然后，在执行过程中在缩放单元上进行的登记将传输到中心，可在该中心上处理考勤管理审批、库存和财务更新。</span><span class="sxs-lookup"><span data-stu-id="914e5-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="914e5-134">可在工作负荷上运行的制造执行任务</span><span class="sxs-lookup"><span data-stu-id="914e5-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="914e5-135">使用缩放单元时，以下制造执行任务当前可以在工作负荷上运行：</span><span class="sxs-lookup"><span data-stu-id="914e5-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="914e5-136">上班打卡、登录、下班打卡和缺勤</span><span class="sxs-lookup"><span data-stu-id="914e5-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="914e5-137">开始作业</span><span class="sxs-lookup"><span data-stu-id="914e5-137">Start job</span></span>
- <span data-ttu-id="914e5-138">捆绑作业</span><span class="sxs-lookup"><span data-stu-id="914e5-138">Bundle jobs</span></span>
- <span data-ttu-id="914e5-139">报告进度</span><span class="sxs-lookup"><span data-stu-id="914e5-139">Report progress</span></span>
- <span data-ttu-id="914e5-140">报告报废物料</span><span class="sxs-lookup"><span data-stu-id="914e5-140">Report scrap</span></span>
- <span data-ttu-id="914e5-141">间接活动</span><span class="sxs-lookup"><span data-stu-id="914e5-141">Indirect activity</span></span>
- <span data-ttu-id="914e5-142">休息</span><span class="sxs-lookup"><span data-stu-id="914e5-142">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="914e5-143">在中心上使用制造执行工作负荷</span><span class="sxs-lookup"><span data-stu-id="914e5-143">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="914e5-144">通常，运行制造执行工作负荷所需的流程会自动运行，以根据需要使中心和所有缩放单元保持同步。</span><span class="sxs-lookup"><span data-stu-id="914e5-144">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="914e5-145">但是，如果遇到问题，可以手动触发从工作负荷收到的原始登记的处理和/或查看登记处理日志。</span><span class="sxs-lookup"><span data-stu-id="914e5-145">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="914e5-146">手动处理原始登记</span><span class="sxs-lookup"><span data-stu-id="914e5-146">Manually process raw registrations</span></span>

<span data-ttu-id="914e5-147">Supply Chain Management 中的批处理作业会自动运行，以处理从工作负荷收到的所有登记。</span><span class="sxs-lookup"><span data-stu-id="914e5-147">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="914e5-148">在针对工作负荷上的已完成作业处理登记时，此作业将创建所需的生产日记帐和日志条目。</span><span class="sxs-lookup"><span data-stu-id="914e5-148">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="914e5-149">尽管作业通常会自动运行，但您可以通过登录到中心并转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 处理原始登记** 随时手动运行它。</span><span class="sxs-lookup"><span data-stu-id="914e5-149">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="914e5-150">查看原始登记处理日志</span><span class="sxs-lookup"><span data-stu-id="914e5-150">Check the raw registration processing log</span></span>

<span data-ttu-id="914e5-151">若要查看登记处理日志，请登录到中心，然后转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 原始登记处理日志**。</span><span class="sxs-lookup"><span data-stu-id="914e5-151">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="914e5-152">**原始登记处理日志** 页面显示已处理的原始登记的列表以及每个登记的状态。</span><span class="sxs-lookup"><span data-stu-id="914e5-152">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="914e5-153">![原始登记处理日志页面](media/mes-processing-log.png "原始登记处理日志页面")</span><span class="sxs-lookup"><span data-stu-id="914e5-153">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="914e5-154">您可以通过选择列表中的任何登记，然后选择操作窗格上的以下按钮之一来处理登记：</span><span class="sxs-lookup"><span data-stu-id="914e5-154">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="914e5-155">**处理** – 手动处理选定的登记。</span><span class="sxs-lookup"><span data-stu-id="914e5-155">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="914e5-156">如果 _处理原始登记_ 作业未运行或者已失败，此操作可能有用。</span><span class="sxs-lookup"><span data-stu-id="914e5-156">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="914e5-157">**取消** – 取消选定的登记。</span><span class="sxs-lookup"><span data-stu-id="914e5-157">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="914e5-158">在缩放单元上使用制造执行工作负荷</span><span class="sxs-lookup"><span data-stu-id="914e5-158">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="914e5-159">通常，运行制造执行工作负荷所需的流程会自动运行，以根据需要使中心和所有缩放单元保持同步。</span><span class="sxs-lookup"><span data-stu-id="914e5-159">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="914e5-160">但是，如果遇到问题，您可以查看缩放单元上已处理的订单历史记录或手动运行 _制造中心到缩放单元消息处理器_ 作业。</span><span class="sxs-lookup"><span data-stu-id="914e5-160">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="914e5-161">查看缩放单元上已处理的制造作业的历史记录</span><span class="sxs-lookup"><span data-stu-id="914e5-161">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="914e5-162">若要查看缩放单元上已处理的制造作业的历史记录，然后转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 制造作业处理历史记录**。</span><span class="sxs-lookup"><span data-stu-id="914e5-162">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="914e5-163">**制造作业处理历史记录** 页面显示缩放单元上生产订单的处理历史记录。</span><span class="sxs-lookup"><span data-stu-id="914e5-163">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="914e5-164">您可以通过选择列表中的任何生产订单，然后选择操作窗格上的以下按钮之一来处理生产订单：</span><span class="sxs-lookup"><span data-stu-id="914e5-164">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="914e5-165">**处理** – 手动处理选定的生产订单。</span><span class="sxs-lookup"><span data-stu-id="914e5-165">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="914e5-166">**取消** – 取消选定的生产订单。</span><span class="sxs-lookup"><span data-stu-id="914e5-166">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="914e5-167">制造中心到缩放单元消息处理器作业</span><span class="sxs-lookup"><span data-stu-id="914e5-167">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="914e5-168">_制造中心到缩放单元消息处理器_ 作业处理从中心到缩放单元的数据。</span><span class="sxs-lookup"><span data-stu-id="914e5-168">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="914e5-169">在部署制造执行工作负荷时将自动启动此作业。</span><span class="sxs-lookup"><span data-stu-id="914e5-169">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="914e5-170">但是，您可以通过转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 制造中心到缩放单元消息处理器** 随时手动运行它。</span><span class="sxs-lookup"><span data-stu-id="914e5-170">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
