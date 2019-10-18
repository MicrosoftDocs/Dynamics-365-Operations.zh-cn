---
title: 推迟处理仓库工作
description: 本主题介绍 Dynamics 365 Supply Chain Management 中提供的用于将推迟处理仓库工作转化为放置操作的功能。
author: josaw1
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1acfa41b9a94b5f27eefda006c8e2950059f3489
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026905"
---
# <a name="deferred-processing-of-warehouse-work"></a><span data-ttu-id="10590-103">推迟处理仓库工作</span><span class="sxs-lookup"><span data-stu-id="10590-103">Deferred processing of warehouse work</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]

<span data-ttu-id="10590-104">本主题介绍 Dynamics 365 Supply Chain Management 中提供的用于将推迟处理仓库工作转化为放置操作的功能。</span><span class="sxs-lookup"><span data-stu-id="10590-104">This topic describes the functionality that makes deferred processing of put operations for warehouse work available in Dynamics 365 Supply Chain Management.</span></span>


<span data-ttu-id="10590-105">推迟处理功能让仓库工人可以在后台处理放置操作期间继续执行其他工作。</span><span class="sxs-lookup"><span data-stu-id="10590-105">The deferred processing functionality lets warehouse workers continue to do other work while the put operation is processed in the background.</span></span> <span data-ttu-id="10590-106">当必须处理大量工作行，并且工人可以异步处理这些工作时，推迟处理非常有用。</span><span class="sxs-lookup"><span data-stu-id="10590-106">Deferred processing is useful when many work lines must be processed and the worker can let that work be processed asynchronously.</span></span> <span data-ttu-id="10590-107">当服务器的处理时间临时或意外增加，并且增加的处理时间可能影响用户的生产率时，此功能也非常有用。</span><span class="sxs-lookup"><span data-stu-id="10590-107">It's also useful when the server can have ad-hoc or unplanned increases in processing time, and the increased processing time might affect the user's productivity.</span></span>

<span data-ttu-id="10590-108">可使用 SysOperation 框架实现后台处理。</span><span class="sxs-lookup"><span data-stu-id="10590-108">Background processing is achieved by using the SysOperation framework.</span></span> <span data-ttu-id="10590-109">有关详细信息，请参阅 [SysOperation 框架概述](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview)。</span><span class="sxs-lookup"><span data-stu-id="10590-109">For more information, see [SysOperation Framework Overview](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).</span></span>

## <a name="configuring-the-work-processing-policies"></a><span data-ttu-id="10590-110">配置工作处理策略</span><span class="sxs-lookup"><span data-stu-id="10590-110">Configuring the work processing policies</span></span>

<span data-ttu-id="10590-111">若要使用推迟处理，必须配置并使用工作处理策略。</span><span class="sxs-lookup"><span data-stu-id="10590-111">To use deferred processing, you must configure and use a work processing policy.</span></span>

<span data-ttu-id="10590-112">策略在**工作处理策略**页中配置。</span><span class="sxs-lookup"><span data-stu-id="10590-112">Policies are configured on the **Work processing policies** page.</span></span> <span data-ttu-id="10590-113">下表介绍该页中的字段。</span><span class="sxs-lookup"><span data-stu-id="10590-113">The following table describes the fields on that page.</span></span>

| <span data-ttu-id="10590-114">字段</span><span class="sxs-lookup"><span data-stu-id="10590-114">Field</span></span>                           | <span data-ttu-id="10590-115">说明</span><span class="sxs-lookup"><span data-stu-id="10590-115">Description</span></span> |
|---------------------------------|-------------|
| <span data-ttu-id="10590-116">工作处理策略名称</span><span class="sxs-lookup"><span data-stu-id="10590-116">Work processing policy name</span></span>     | <span data-ttu-id="10590-117">工作处理策略的名称。</span><span class="sxs-lookup"><span data-stu-id="10590-117">The name of the work processing policy.</span></span> |
| <span data-ttu-id="10590-118">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="10590-118">Work order type</span></span>                 | <span data-ttu-id="10590-119">应用策略的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="10590-119">The work order type that the policy is applied to.</span></span> |
| <span data-ttu-id="10590-120">操作​</span><span class="sxs-lookup"><span data-stu-id="10590-120">Operation</span></span>                       | <span data-ttu-id="10590-121">使用策略处理的操作。</span><span class="sxs-lookup"><span data-stu-id="10590-121">The operation that is processed by using the policy.</span></span> |
| <span data-ttu-id="10590-122">工作处理方法</span><span class="sxs-lookup"><span data-stu-id="10590-122">Work processing method</span></span>          | <span data-ttu-id="10590-123">用于处理工作行的方法。</span><span class="sxs-lookup"><span data-stu-id="10590-123">The method that is used to process the work line.</span></span> <span data-ttu-id="10590-124">如果方法设置为**立即**，则行为类似未使用任何工作处理策略来处理行时的行为。</span><span class="sxs-lookup"><span data-stu-id="10590-124">If the method is set to **Immediate**, the behavior resembles the behavior when no work processing policies are used to process the line.</span></span> <span data-ttu-id="10590-125">如果方法设置为 **推迟**，则使用的是使用批处理框架的推迟处理。</span><span class="sxs-lookup"><span data-stu-id="10590-125">If the method is set to **Deferred**, deferred processing that uses the batch framework is used.</span></span> |
| <span data-ttu-id="10590-126">延期处理阈值</span><span class="sxs-lookup"><span data-stu-id="10590-126">Deferred processing threshold</span></span>   | <span data-ttu-id="10590-127">如果值为 **0**（零），这表示无阈值。</span><span class="sxs-lookup"><span data-stu-id="10590-127">A value of **0** (zero) indicates that there is no threshold.</span></span> <span data-ttu-id="10590-128">在这种情况下，如果可以，将使用推迟处理。</span><span class="sxs-lookup"><span data-stu-id="10590-128">In this case, deferred processing is used if it can be used.</span></span> <span data-ttu-id="10590-129">如果阈值的具体计算结果低于阈值，则使用“立即”方法。</span><span class="sxs-lookup"><span data-stu-id="10590-129">If the specific threshold calculation is below the threshold, the Immediate method is used.</span></span> <span data-ttu-id="10590-130">否则，如果可以，则使用“推迟”方法。</span><span class="sxs-lookup"><span data-stu-id="10590-130">Otherwise, the Deferred method is used if it can be used.</span></span> <span data-ttu-id="10590-131">对于与销售和运输有关的工作，计算出的阈值是正在为工作处理的关联源负荷行的数量。</span><span class="sxs-lookup"><span data-stu-id="10590-131">For sales and transfer-related work, the threshold is calculated as the number of associated source load lines that are being processed for the work.</span></span> <span data-ttu-id="10590-132">对于补货工作，计算出的阈值是工作正在补货的工作行的数量。</span><span class="sxs-lookup"><span data-stu-id="10590-132">For replenishment work, the threshold is calculated as the number of work lines that are being replenished by the work.</span></span> <span data-ttu-id="10590-133">例如，如果为销售将阈值设置为 **5**，则初始源负荷行少于五个的少量工作不使用推迟处理，但是大量工作则会使用。</span><span class="sxs-lookup"><span data-stu-id="10590-133">By setting a threshold of, for example, **5** for sales, smaller works that have fewer than five initial source load lines won't use deferred processing, but larger works will use it.</span></span> <span data-ttu-id="10590-134">仅当工作处理方法设置为**推迟**时，此阈值才有效。</span><span class="sxs-lookup"><span data-stu-id="10590-134">The threshold has an effect only if the work processing method is set to **Deferred**.</span></span> |
| <span data-ttu-id="10590-135">延迟处理批处理组</span><span class="sxs-lookup"><span data-stu-id="10590-135">Deferred processing batch group</span></span> |<span data-ttu-id="10590-136">用于处理的批处理组。</span><span class="sxs-lookup"><span data-stu-id="10590-136">The batch group that is used for processing.</span></span> |

## <a name="assigning-the-work-creation-policy"></a><span data-ttu-id="10590-137">分配工作创建策略</span><span class="sxs-lookup"><span data-stu-id="10590-137">Assigning the work creation policy</span></span>

<span data-ttu-id="10590-138">可以在仓库管理参数中分配工作创建策略。</span><span class="sxs-lookup"><span data-stu-id="10590-138">The work creation policy can be assigned in the warehouse management parameters.</span></span> <span data-ttu-id="10590-139">还可以在单个仓库级别分配。</span><span class="sxs-lookup"><span data-stu-id="10590-139">It can also be assigned at the level of individual warehouses.</span></span> <span data-ttu-id="10590-140">如果为仓库分配了策略，将把该策略仅应用于为这个仓库创建的工作。</span><span class="sxs-lookup"><span data-stu-id="10590-140">If the policy is assigned to a warehouse, it's applied only to work that is created for that warehouse.</span></span> <span data-ttu-id="10590-141">如果未在仓库级别分配策略，则应用仓库管理参数中的策略。</span><span class="sxs-lookup"><span data-stu-id="10590-141">If no policy is assigned at the warehouse level, the policy from the warehouse management parameters is applied.</span></span>

## <a name="viewing-the-deferred-put-processing-tasks"></a><span data-ttu-id="10590-142">查看推迟放置处理任务</span><span class="sxs-lookup"><span data-stu-id="10590-142">Viewing the deferred put processing tasks</span></span>

<span data-ttu-id="10590-143">可在**推迟放置处理任务**页中查看推迟放置处理任务。</span><span class="sxs-lookup"><span data-stu-id="10590-143">You can view deferred put processing tasks on the **Deferred put processing tasks** page.</span></span>

<span data-ttu-id="10590-144">默认情况下，将显示**已完成**任务。</span><span class="sxs-lookup"><span data-stu-id="10590-144">By default, the **Completed** tasks are shown.</span></span>

| <span data-ttu-id="10590-145">字段</span><span class="sxs-lookup"><span data-stu-id="10590-145">Field</span></span>            | <span data-ttu-id="10590-146">说明</span><span class="sxs-lookup"><span data-stu-id="10590-146">Description</span></span> |
|------------------|-------------|
| <span data-ttu-id="10590-147">状态</span><span class="sxs-lookup"><span data-stu-id="10590-147">Status</span></span>           | <span data-ttu-id="10590-148">任务的状态。</span><span class="sxs-lookup"><span data-stu-id="10590-148">The status of the task.</span></span> |
| <span data-ttu-id="10590-149">批处理作业状态</span><span class="sxs-lookup"><span data-stu-id="10590-149">Batch job status</span></span> | <span data-ttu-id="10590-150">相关批处理作业的状态。</span><span class="sxs-lookup"><span data-stu-id="10590-150">The status of the related batch job.</span></span> <span data-ttu-id="10590-151">如果已处理了批处理作业，则批处理历史记录中包含批处理作业的日志和信息。</span><span class="sxs-lookup"><span data-stu-id="10590-151">If the batch job has been processed, the batch history contains the log and information from the batch job.</span></span> |

<span data-ttu-id="10590-152">以下是对可能的状态的说明：</span><span class="sxs-lookup"><span data-stu-id="10590-152">Here is an explanation of the possible statuses:</span></span>

- <span data-ttu-id="10590-153">**正在等待** – 批处理服务器正在等待处理相关批处理作业。</span><span class="sxs-lookup"><span data-stu-id="10590-153">**Awaiting** – The related batch job is awaiting processing on the batch server.</span></span>
- <span data-ttu-id="10590-154">**失败** – 处理已失败。</span><span class="sxs-lookup"><span data-stu-id="10590-154">**Failed** – The processing failed.</span></span> <span data-ttu-id="10590-155">可以使用**处理推迟的放置**操作重新处理该任务，也可以使用**取消推迟的放置**操作取消该任务。</span><span class="sxs-lookup"><span data-stu-id="10590-155">The task can be reprocessed by using the **Process deferred put** action, or it can be canceled by using the **Cancel deferred put** action.</span></span>
- <span data-ttu-id="10590-156">**已完成** – 作业已完成。</span><span class="sxs-lookup"><span data-stu-id="10590-156">**Completed** – The job was completed.</span></span>

## <a name="impact-on-closed-work-dates"></a><span data-ttu-id="10590-157">对工作关闭日期的影响</span><span class="sxs-lookup"><span data-stu-id="10590-157">Impact on closed work dates</span></span>

<span data-ttu-id="10590-158">如果使用推迟的放置处理，则将工作关闭日期设置为推迟的放置处理任务的创建日期/时间。</span><span class="sxs-lookup"><span data-stu-id="10590-158">When deferred put processing is used, the closed work date is set as the created date/time of the deferred put processing tasks.</span></span> <span data-ttu-id="10590-159">之所以使用工作关闭日期，是因为这是放置操作完成时间的最佳估计结果。</span><span class="sxs-lookup"><span data-stu-id="10590-159">The closed work date is used because it's the best estimate for when the put operation was completed.</span></span>

## <a name="reprocessing-a-failed-task"></a><span data-ttu-id="10590-160">重新处理失败任务</span><span class="sxs-lookup"><span data-stu-id="10590-160">Reprocessing a failed task</span></span>

<span data-ttu-id="10590-161">可重新处理失败任务，方法是在页面中选择该任务，然后选择**处理推迟的放置**。</span><span class="sxs-lookup"><span data-stu-id="10590-161">You can reprocess a failed task by selecting it on the page and then selecting **Process deferred put**.</span></span> <span data-ttu-id="10590-162">重新处理与以下情况对应：用户从移动设备完成入库，就像是为立即处理设置的。</span><span class="sxs-lookup"><span data-stu-id="10590-162">Reprocessing corresponds to a situation where the user completes the put-away from the mobile device as if it was set for immediate processing.</span></span>

## <a name="canceling-failed-tasks"></a><span data-ttu-id="10590-163">取消失败任务</span><span class="sxs-lookup"><span data-stu-id="10590-163">Canceling failed tasks</span></span>

<span data-ttu-id="10590-164">只有失败任务才能取消。</span><span class="sxs-lookup"><span data-stu-id="10590-164">Only failed tasks can be canceled.</span></span> <span data-ttu-id="10590-165">取消任务后，可将其分配给新用户。</span><span class="sxs-lookup"><span data-stu-id="10590-165">When you cancel a task, you can assign it to a new user.</span></span> <span data-ttu-id="10590-166">也可以将任务继续分配给曾处理该工作的用户。</span><span class="sxs-lookup"><span data-stu-id="10590-166">Alternatively, the task can remain assigned to the user who processed the work.</span></span> <span data-ttu-id="10590-167">取消对应于以下情况：将工作带回移动设备，就像刚完成上一个领料步骤，并且工作必须完工入库。</span><span class="sxs-lookup"><span data-stu-id="10590-167">Cancellation corresponds to a situation where the work is brought back to the mobile device as if the last pick step was just completed and the work must be put away.</span></span> <span data-ttu-id="10590-168">但是，用户可以确定工作“不同”，因为该工作只有入库步骤，而位置将继续与第一位处理该工作的用户用作最终放置位置的位置对应。</span><span class="sxs-lookup"><span data-stu-id="10590-168">However, the user will be able to determine that the work is "different," because it will have only a put-away step, and the location will correspond to the location that the first user who processed the work had as a final put location.</span></span>

<span data-ttu-id="10590-169">取消任务后，推迟放置处理阻止原因不再阻止工作。</span><span class="sxs-lookup"><span data-stu-id="10590-169">When a task is canceled, the work is no longer blocked by the deferred put processing blocking reason.</span></span> <span data-ttu-id="10590-170">可以使用移动设备重新处理该任务。</span><span class="sxs-lookup"><span data-stu-id="10590-170">It can be reprocessed by using the mobile device.</span></span>

<span data-ttu-id="10590-171">取消任务后，将删除任务记录。</span><span class="sxs-lookup"><span data-stu-id="10590-171">The task record is deleted when the task canceled.</span></span>

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a><span data-ttu-id="10590-172">配置移动设备菜单以跳过推迟处理策略</span><span class="sxs-lookup"><span data-stu-id="10590-172">Configuring the mobile device menu to skip the deferred processing policy</span></span>

<span data-ttu-id="10590-173">可配置移动设备菜单项，以便不使用推迟处理策略。</span><span class="sxs-lookup"><span data-stu-id="10590-173">You can configure the mobile device menu item so that the deferred processing policy isn't used.</span></span> <span data-ttu-id="10590-174">然后按照不使用推迟处理策略的方式处理工作。</span><span class="sxs-lookup"><span data-stu-id="10590-174">The work is then processed as it is when no deferred processing policy is used.</span></span> <span data-ttu-id="10590-175">此功能让主管可使用其中不使用推迟放置的特定菜单项。</span><span class="sxs-lookup"><span data-stu-id="10590-175">This functionality lets a supervisor use a specific menu item where deferred put isn't used.</span></span> <span data-ttu-id="10590-176">若要配置，请将**推迟放置处理策略**字段设置为**覆盖设置并同步处理放置**。</span><span class="sxs-lookup"><span data-stu-id="10590-176">To configure it, set the **Deferred put processing policy** field to **Override settings and process put synchronously**.</span></span> 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a><span data-ttu-id="10590-177">不应用推迟放置处理时的限制</span><span class="sxs-lookup"><span data-stu-id="10590-177">Restrictions when the deferred put processing isn't applied</span></span>

<span data-ttu-id="10590-178">有几种情况即使配置了策略，也不应用推迟放置处理。</span><span class="sxs-lookup"><span data-stu-id="10590-178">There are several scenarios where deferred put processing isn't applied even though the policy is configured.</span></span> <span data-ttu-id="10590-179">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="10590-179">Here are some examples:</span></span>

- <span data-ttu-id="10590-180">使用了手动完工。</span><span class="sxs-lookup"><span data-stu-id="10590-180">Manual work completion is used.</span></span>
- <span data-ttu-id="10590-181">将使用自动完成完成工作。</span><span class="sxs-lookup"><span data-stu-id="10590-181">The work is completed by using auto-completion.</span></span>
- <span data-ttu-id="10590-182">使用了审计模板。</span><span class="sxs-lookup"><span data-stu-id="10590-182">Audit templates are used.</span></span>
- <span data-ttu-id="10590-183">工作使用容器。</span><span class="sxs-lookup"><span data-stu-id="10590-183">The work uses containers.</span></span>

## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a><span data-ttu-id="10590-184">从“出站工作监视”工作区监视推迟处理的任务</span><span class="sxs-lookup"><span data-stu-id="10590-184">Monitoring the deferred processing tasks from the Outbound work monitoring workspace</span></span>

<span data-ttu-id="10590-185">**出站工作监视**工作区有两个磁贴，可帮助您监视推迟的放置处理任务：</span><span class="sxs-lookup"><span data-stu-id="10590-185">The **Outbound work monitoring** workspace has two tiles that help you monitor deferred put processing tasks:</span></span>

- <span data-ttu-id="10590-186">**失败推迟放置处理任务** – 此磁贴显示失败任务数量。</span><span class="sxs-lookup"><span data-stu-id="10590-186">**Failed deferred put processing tasks** – This tile shows the number of failed tasks.</span></span> <span data-ttu-id="10590-187">如果有失败任务，仓库经理必须重新处理或取消这些任务，因为不会自动重新处理。</span><span class="sxs-lookup"><span data-stu-id="10590-187">If there are failed tasks, the warehouse manager must either reprocess them or cancel them, because they won't be reprocessed automatically.</span></span>
- <span data-ttu-id="10590-188">**等待推迟的放置处理任务** – 此磁贴显示**正在等待**状态超过 10 分钟的任务的数量。</span><span class="sxs-lookup"><span data-stu-id="10590-188">**Awaiting deferred put processing tasks** – This tile shows the number of tasks that have been in the **Awaiting** status for more than 10 minutes.</span></span> <span data-ttu-id="10590-189">如果此磁贴显示数字，可能表示批处理期间发生了问题。</span><span class="sxs-lookup"><span data-stu-id="10590-189">If the tile shows a number, it might indicate that an issue occurred during batch processing.</span></span> <span data-ttu-id="10590-190">可手动处理**正在等待**任务。</span><span class="sxs-lookup"><span data-stu-id="10590-190">You can manually process the **Awaiting** tasks.</span></span> <span data-ttu-id="10590-191">如果以后处理任务的批处理作业，就会失败，因为已经处理过了。</span><span class="sxs-lookup"><span data-stu-id="10590-191">If the batch job for a task is processed later, it will just fail, because it has already been processed.</span></span> <span data-ttu-id="10590-192">不会有影响。</span><span class="sxs-lookup"><span data-stu-id="10590-192">There will be no impact.</span></span>

## <a name="deleting-completed-tasks"></a><span data-ttu-id="10590-193">删除已完成任务</span><span class="sxs-lookup"><span data-stu-id="10590-193">Deleting completed tasks</span></span>

<span data-ttu-id="10590-194">可删除已完成的推迟放置处理任务，方法是在页面中选择这些任务，然后删除。</span><span class="sxs-lookup"><span data-stu-id="10590-194">You can delete deferred put processing tasks that have been completed by selecting them and deleting them on the page.</span></span>
