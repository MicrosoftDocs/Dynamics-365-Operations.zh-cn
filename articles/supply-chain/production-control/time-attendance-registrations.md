---
title: "考勤管理登记"
description: "时间登记工作人员可以输入上班打卡、下班打卡、登记间接活动、缺勤登记等不同类型的时间登记。 本主题介绍工作流的登记、计算、审核和使用以将结构和自动审核添加到时间表审核流程。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ec008cd65fe7c11eb24ae8c5088d53f11dc2c88
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="time-and-attendance-registration"></a><span data-ttu-id="771da-104">考勤管理登记</span><span class="sxs-lookup"><span data-stu-id="771da-104">Time and attendance registration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="771da-105">时间登记工作人员可以输入上班打卡、下班打卡、登记间接活动、缺勤登记等不同类型的时间登记。</span><span class="sxs-lookup"><span data-stu-id="771da-105">Time registration workers can enter different types of time registrations, for example, clock in, clock out, register indirect activities, and absence registration.</span></span> <span data-ttu-id="771da-106">本主题介绍工作流的登记、计算、审核和使用以将结构和自动审核添加到时间表审核流程。</span><span class="sxs-lookup"><span data-stu-id="771da-106">This topic describes registrations, their calculation, approval, and the use of workflow to add structure and automated approval to the process of approving timesheets.</span></span> 

<a name="registrations"></a><span data-ttu-id="771da-107">登记</span><span class="sxs-lookup"><span data-stu-id="771da-107">Registrations</span></span>
-------------

<span data-ttu-id="771da-108">在使用“考勤管理”的公司中，工作人员必须登记自己在工作上花费的时间，以及他们的出勤情况。</span><span class="sxs-lookup"><span data-stu-id="771da-108">In companies that use Time and attendance, workers must register the time that they spend at work, as well as their attendance.</span></span> <span data-ttu-id="771da-109">一些公司可能只要求工作人员上班打卡登记和下班打卡登记。</span><span class="sxs-lookup"><span data-stu-id="771da-109">Some companies may only require workers to register clocking-in and clocking-out times.</span></span> <span data-ttu-id="771da-110">在其他公司中，还要求工作人员登记实际活动以及休息中的时间消耗量。</span><span class="sxs-lookup"><span data-stu-id="771da-110">In other companies, workers may also be required to register time consumption on the actual activities they perform as well as the breaks they take.</span></span> <span data-ttu-id="771da-111">考勤管理的预期用户是：</span><span class="sxs-lookup"><span data-stu-id="771da-111">The intended users of Time and attendance are:</span></span>
-   <span data-ttu-id="771da-112">要求按照每天、每周或每两周等定期登记时间和出勤的工作人员。</span><span class="sxs-lookup"><span data-stu-id="771da-112">Workers, who are required to register time and attendance at regular intervals, for example daily, weekly or bi-weekly.</span></span>
-   <span data-ttu-id="771da-113">计算、审核并转移工作人员登记以进一步处理的主管、经理和工资专员。</span><span class="sxs-lookup"><span data-stu-id="771da-113">Supervisors, managers, and payroll officers who calculate, approve, and transfer worker registrations for further processing.</span></span>

| <span data-ttu-id="771da-114">**注意**</span><span class="sxs-lookup"><span data-stu-id="771da-114">**Note**</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771da-115">如果您将“考勤管理”和“制造执行”一起运行，则项目、项目活动、间接活动、考勤代码、加班时间和弹性时间的所有登记都将得以记录并用于在这两个模块中计算工资。</span><span class="sxs-lookup"><span data-stu-id="771da-115">If you run Time and attendance together with Manufacturing execution, all registrations on projects, project activities, indirect activities, absence codes, and overtime and flex time will be recorded and are used to calculate payroll in both modules.</span></span> |

## <a name="time-registrations-workers"></a><span data-ttu-id="771da-116"> 时间登记工作人员</span><span class="sxs-lookup"><span data-stu-id="771da-116">Time registrations workers</span></span>
<span data-ttu-id="771da-117">若要在登记时间和考勤，工作人员必须在雇佣他们的公司中被设置为了时间登记工作人员。</span><span class="sxs-lookup"><span data-stu-id="771da-117">To be able to register time and absence, workers must be set up as time registration workers in the company they are employed in.</span></span>

<span data-ttu-id="771da-118">在设置后，工作人员可以输入不同类型的登记。</span><span class="sxs-lookup"><span data-stu-id="771da-118">After setup, the workers can enter different types of registrations.</span></span>

-   <span data-ttu-id="771da-119">在上班或下班时进行上下班打卡。</span><span class="sxs-lookup"><span data-stu-id="771da-119">Clocking in- and out when arriving or leaving work.</span></span>
-   <span data-ttu-id="771da-120">生产工作中的时间和物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="771da-120">Time and item consumption on production jobs.</span></span>
-   <span data-ttu-id="771da-121">在车间的机器上使用的时间（如果机器已定义为资源）。</span><span class="sxs-lookup"><span data-stu-id="771da-121">Time used on a machine on the shop floor, if the machine has been defined as a resource.</span></span>

| <span data-ttu-id="771da-122">**注意**</span><span class="sxs-lookup"><span data-stu-id="771da-122">**Note**</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771da-123">可以自动为工作人员分配在车间的特殊设备上进行的时间登记（如果工作人员在开始生产工作时选择其作为机器的助手）。</span><span class="sxs-lookup"><span data-stu-id="771da-123">A worker can be automatically assigned the time registrations that are made on a particular machine on the shop floor, if the worker chooses to work as an assistant to the machine when he or she starts the production job.</span></span> |

-   <span data-ttu-id="771da-124">项目和项目活动上的时间登记。</span><span class="sxs-lookup"><span data-stu-id="771da-124">Time registrations on projects and project activities.</span></span>
-   <span data-ttu-id="771da-125">通过各自的项目费用日记帐和项目物料日记帐，登记项目费用和物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="771da-125">Registering project fees and item consumption via the respective project fee journals and project item journals.</span></span>
-   <span data-ttu-id="771da-126">计划缺勤。</span><span class="sxs-lookup"><span data-stu-id="771da-126">Planned absence.</span></span>
-   <span data-ttu-id="771da-127">在上班迟到或早于计划离开时的缺勤。</span><span class="sxs-lookup"><span data-stu-id="771da-127">Absence when arriving late to work or leaving earlier than planned.</span></span>
-   <span data-ttu-id="771da-128">工休，手动登记或由系统自动计算。</span><span class="sxs-lookup"><span data-stu-id="771da-128">Work breaks, either manually registered or automatically calculated by the system.</span></span>
-   <span data-ttu-id="771da-129">间接活动，即，工作人员可能在工作日期间涉及的非生产活动。</span><span class="sxs-lookup"><span data-stu-id="771da-129">Indirect activities, which are non-productive activities a worker might engage in during a workday.</span></span> <span data-ttu-id="771da-130">这些活动的示例包括会议或清洁其工作区。</span><span class="sxs-lookup"><span data-stu-id="771da-130">Examples of these activities include meetings or cleaning their workspace.</span></span>
-   <span data-ttu-id="771da-131">加班，可以登记为额外工时、弹性工作时间或加班时间。</span><span class="sxs-lookup"><span data-stu-id="771da-131">Overtime, which can be registered either as extra hours, flextime, or overtime.</span></span>

## <a name="adding-clock-out-registrations"></a><span data-ttu-id="771da-132">添加下班打卡登记</span><span class="sxs-lookup"><span data-stu-id="771da-132">Adding clock-out registrations</span></span>
<span data-ttu-id="771da-133">如果某个员工忘记在工作日结束时下班打卡，则可以通过运行批处理作业添加遗漏的登记。</span><span class="sxs-lookup"><span data-stu-id="771da-133">If a worker forgets to clock-out at the end of their workday, the missing registration can be added by running a batch job.</span></span> <span data-ttu-id="771da-134">系统将根据工作人员的关联模板比较上班打卡时间和下班打卡时间，而且自动插入遗漏的下班打卡登记并与模板的结束时间匹配。</span><span class="sxs-lookup"><span data-stu-id="771da-134">The system will compare the clock-in time and the clock-out time according to the associated profile of the worker, and automatically insert the missing clock-out registration to match the profile’s end time.</span></span> <span data-ttu-id="771da-135">上班打卡和下班打卡登记对于时间登记的后续计算和审核很重要，然后它们才能转移到工资单。</span><span class="sxs-lookup"><span data-stu-id="771da-135">Both the clock-in and clock-out registrations are vital for the subsequent calculation and approval of time registrations before they can be transferred to payroll.</span></span>

## <a name="calculating-registrations"></a><span data-ttu-id="771da-136">计算登记</span><span class="sxs-lookup"><span data-stu-id="771da-136">Calculating registrations</span></span>
<span data-ttu-id="771da-137">当为登记工作人员分配一个通常与特定团队、班次或工作组关联的计算组时。</span><span class="sxs-lookup"><span data-stu-id="771da-137">When a registration worker is assigned a calculation group that typically relates to a specific team, shift, or work group.</span></span> <span data-ttu-id="771da-138">团队经理或主管通常验证工作人员进行的登记，并且因此也是负责人每天都为各自的计算组运行计算。</span><span class="sxs-lookup"><span data-stu-id="771da-138">The team manager or supervisor typically validates the registrations made by the workers, and is therefore also the responsible person to run the calculation for the respective calculation groups on a daily basis.</span></span> <span data-ttu-id="771da-139">作为计算流程的一部分，团队经理或主管可以：</span><span class="sxs-lookup"><span data-stu-id="771da-139">As part of the calculation process the team manager or supervisor is able to:</span></span>
-   <span data-ttu-id="771da-140">更正错误的登记。</span><span class="sxs-lookup"><span data-stu-id="771da-140">Correct erroneous registrations.</span></span> <span data-ttu-id="771da-141">例如，更改切换代码并调整有关生产工作的反馈。</span><span class="sxs-lookup"><span data-stu-id="771da-141">For example, change switch codes and adjust feedback on production jobs.</span></span>
-   <span data-ttu-id="771da-142">添加遗漏的登记。</span><span class="sxs-lookup"><span data-stu-id="771da-142">Add missing registrations.</span></span> <span data-ttu-id="771da-143">例如，创建下班打卡登记并创建缺勤交易记录。</span><span class="sxs-lookup"><span data-stu-id="771da-143">For example, create clock-out registrations and create absence transactions.</span></span>
-   <span data-ttu-id="771da-144">删除不正确的登记。</span><span class="sxs-lookup"><span data-stu-id="771da-144">Delete incorrect registrations.</span></span>

<span data-ttu-id="771da-145">由于在计算登记之前，登记时间必须与工作人员的时间模板匹配，因此对于任何对比标准工作时间模板有异常的工作人员，您必须覆盖其工作时间模板。</span><span class="sxs-lookup"><span data-stu-id="771da-145">Because the registered time must match the worker’s time profile prior to calculating the registrations, you must override the work time profile for any worker who has an exception to his standard work time profile.</span></span> <span data-ttu-id="771da-146">如果工作人员模板是白班，并且工作人员已同意在没有夜班费的情况下上夜班，则团队经理或主管人员必须覆盖默认工作模板，才能以标准比率而不是作为加班时间来计算工作时间。</span><span class="sxs-lookup"><span data-stu-id="771da-146">In the case, where the worker profile is day shift, and the worker has agreed to work a night shift with no overtime pay, the team manager or supervisor must override the default worker profile in order to calculate the working time at the standard night rate and not as overtime.</span></span> <span data-ttu-id="771da-147">该计算还将在缺少缺勤登记时显示错误。</span><span class="sxs-lookup"><span data-stu-id="771da-147">The calculation will also display an error if an absence registration is missing.</span></span> <span data-ttu-id="771da-148">必须先添加它，然后才能完成计算。</span><span class="sxs-lookup"><span data-stu-id="771da-148">It must be added before the calculation can be completed.</span></span>

## <a name="approving-registrations"></a><span data-ttu-id="771da-149">审核登记</span><span class="sxs-lookup"><span data-stu-id="771da-149">Approving registrations</span></span>
<span data-ttu-id="771da-150">如同您将计算组分配给时间登记工作人员一样，您还必须分配审核组。</span><span class="sxs-lookup"><span data-stu-id="771da-150">Just as you assign a calculation group to a time registration worker, you must assign an approval group as well.</span></span> <span data-ttu-id="771da-151">通常，计算组将特定于团队、班次或工作组。</span><span class="sxs-lookup"><span data-stu-id="771da-151">Typically the group will be specific to a team, shift, or work group.</span></span> <span data-ttu-id="771da-152">您必须审核正确计算（这意味着，没有任何错误地执行计算）的时间登记，然后才可以生成付薪项，以便以后转移到工资系统。</span><span class="sxs-lookup"><span data-stu-id="771da-152">You must approve the time registrations that were calculated correctly – this means doing a calculation without errors – before pay items can be generated that afterward can be transferred to a payroll system.</span></span> <span data-ttu-id="771da-153">工资管理员通常会执行审核登记，并且在审核之前他可以：</span><span class="sxs-lookup"><span data-stu-id="771da-153">The payroll administrator will typically do the approval of registrations, and prior to the approval he is able to:</span></span>
-   <span data-ttu-id="771da-154">覆盖各个工作人员的付薪协议。</span><span class="sxs-lookup"><span data-stu-id="771da-154">Override pay agreements for individual workers.</span></span>
-   <span data-ttu-id="771da-155">添加人工津贴。</span><span class="sxs-lookup"><span data-stu-id="771da-155">Add manual premiums.</span></span>
-   <span data-ttu-id="771da-156">输入有关缺勤登记的更多信息。</span><span class="sxs-lookup"><span data-stu-id="771da-156">Enter additional information about absence registrations.</span></span>

| <span data-ttu-id="771da-157">**注意**</span><span class="sxs-lookup"><span data-stu-id="771da-157">**Note**</span></span>                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771da-158">如果已经为特定员工作人员计算了加班，则可以将加班分配给当天中的特定工作。</span><span class="sxs-lookup"><span data-stu-id="771da-158">If overtime has been calculated for specific workers, the overtime can be allocated to specific jobs during the day.</span></span> <span data-ttu-id="771da-159">如果基于工作人员工资计算作业成本，这将是相关的。</span><span class="sxs-lookup"><span data-stu-id="771da-159">This is relevant if job cost is calculated based on worker pay.</span></span> |

## <a name="approving-registrations-using-workflow"></a><span data-ttu-id="771da-160">使用工作流审核登记</span><span class="sxs-lookup"><span data-stu-id="771da-160">Approving registrations using workflow</span></span>
<span data-ttu-id="771da-161">您可以设置工作流审核自动，用以自动审核符合工作流规则的登记，只留下可手动处理的偏差。</span><span class="sxs-lookup"><span data-stu-id="771da-161">You can set up a workflow approval process that automatically approves registrations which comply with workflow rules, leaving only deviations to be handled manually.</span></span> <span data-ttu-id="771da-162">如果启用工作流审核，团队经理或主管提交已计算登记以供审核。</span><span class="sxs-lookup"><span data-stu-id="771da-162">If workflow approval is activated, the team manager or supervisor submits the calculated registrations for approval.</span></span> <span data-ttu-id="771da-163">工作流流程将会生成相应的审核和任务，然后将它们分配到正确的用户和角色，如工作流中所标识。</span><span class="sxs-lookup"><span data-stu-id="771da-163">The workflow process will generate the appropriate approvals and tasks, and then assign them to the right users and roles as identified in the workflow.</span></span> <span data-ttu-id="771da-164">有两个工作流审核可用于考勤管理。</span><span class="sxs-lookup"><span data-stu-id="771da-164">There are two workflow approvals for time and attendance.</span></span>

| <span data-ttu-id="771da-165">工作流</span><span class="sxs-lookup"><span data-stu-id="771da-165">Workflow</span></span>                                  | <span data-ttu-id="771da-166">用途</span><span class="sxs-lookup"><span data-stu-id="771da-166">Purpose</span></span>                                                                                                   | <span data-ttu-id="771da-167">登记类型</span><span class="sxs-lookup"><span data-stu-id="771da-167">Registration type</span></span>                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771da-168">考勤管理天数总计</span><span class="sxs-lookup"><span data-stu-id="771da-168">Time and attendance days total</span></span>            | <span data-ttu-id="771da-169">该工作流根据当天的预期工作时数等验证登记。</span><span class="sxs-lookup"><span data-stu-id="771da-169">The workflow validates registrations against, for example, the expected number of work hours for the day.</span></span> |                                                                                                                                                                                                                                                       |
| <span data-ttu-id="771da-170">考勤管理日记帐登记。</span><span class="sxs-lookup"><span data-stu-id="771da-170">Time and attendance journal registration.</span></span> | <span data-ttu-id="771da-171">该工作流针对每个登记日期验证每个登记类型。</span><span class="sxs-lookup"><span data-stu-id="771da-171">The workflow validates each registration type for the date of the registration.</span></span>                           | <span data-ttu-id="771da-172">考勤管理 • 上班打卡 • 下班打卡 • 缺勤 • 休息 • 切换代码 • 项目 • 项目活动 • 间接活动生产工作 • 之前的队列 • 设置 • 流程 • 重叠 • 运输 • 之后的队列 • 开始帮助 • 停止帮助</span><span class="sxs-lookup"><span data-stu-id="771da-172">Time and attendance • Clock-in • Clock-out • Absence • Break • Switch code • Project • Project activity • Indirect activity Production jobs • Queue before • Setup • Process • Overlap • Transport • Queue after • Start assistance • Stop assistance</span></span> |



## <a name="transferring-approved-registrations"></a><span data-ttu-id="771da-173">转移和审核登记</span><span class="sxs-lookup"><span data-stu-id="771da-173">Transferring approved registrations</span></span>
<span data-ttu-id="771da-174">在审核登记后，才能将其转移到定期的工资单工作。</span><span class="sxs-lookup"><span data-stu-id="771da-174">After approval of the registrations you can transfer them to a periodic payroll job.</span></span> <span data-ttu-id="771da-175">将已转移的登记过账到与生产订单或项目等相关的活动或作业。</span><span class="sxs-lookup"><span data-stu-id="771da-175">A transferred registration is posted to an activity or job that it relates to, for example, a production order or a project.</span></span> <span data-ttu-id="771da-176">基于登记为每个工作人员生成工资交易记录。</span><span class="sxs-lookup"><span data-stu-id="771da-176">Payroll transactions are generated for each worker based on the registrations.</span></span>  

## <a name="reversing-transferred-registrations"></a><span data-ttu-id="771da-177">冲销已转移的登记</span><span class="sxs-lookup"><span data-stu-id="771da-177">Reversing transferred registrations</span></span>
<span data-ttu-id="771da-178">直到运行工资单期间的付薪转移时，才能完成冲销交易记录的任务（将它们回滚）。</span><span class="sxs-lookup"><span data-stu-id="771da-178">The task of reversing transactions – rolling them back – can be done until the time when the payroll period’s pay transfer is run.</span></span> <span data-ttu-id="771da-179">这意味着工资单数据已转移到外部文件。</span><span class="sxs-lookup"><span data-stu-id="771da-179">This means that payroll data has been transferred to an external file.</span></span> <span data-ttu-id="771da-180">当冲销时，撤除所有登记，在特定生产订单或项目上过帐的所有交易记录都被抵消并中立化。</span><span class="sxs-lookup"><span data-stu-id="771da-180">When reversed, all registrations are withdrawn, and any transactions posted on production orders or projects are offset and neutralized.</span></span>

| <span data-ttu-id="771da-181">**注意**</span><span class="sxs-lookup"><span data-stu-id="771da-181">**Note**</span></span>                                                 |
|----------------------------------------------------------|
| <span data-ttu-id="771da-182">外部文件可以导入到工资系统。</span><span class="sxs-lookup"><span data-stu-id="771da-182">The external file can be imported into a payroll system.</span></span> |

## <a name="registrations-in-electronic-timecards"></a><span data-ttu-id="771da-183">电子工时记录卡中的登记</span><span class="sxs-lookup"><span data-stu-id="771da-183">Registrations in electronic timecards</span></span>
<span data-ttu-id="771da-184">具有工作任务的工作人员不需要立即反馈，就像生产工作一样，但在项目活动上工作的人员可以从使用电子工时记录卡中获益。</span><span class="sxs-lookup"><span data-stu-id="771da-184">Workers with job tasks that do not require immediate feedback, as is the case with production jobs, but who work on project activities, can benefit from using the electronic timecard.</span></span> <span data-ttu-id="771da-185">电子工时记录卡提供了灵活性，能让您随时以最适合您的业务计划的方式输入登记 – 每天、每周，或者，当工作人员在不上班后再次回到办公室时。</span><span class="sxs-lookup"><span data-stu-id="771da-185">Electronic timecards offer the flexibility to enter registrations any time and in the best way for your business schedule – daily, weekly, or when a worker is in the office again after being away.</span></span> <span data-ttu-id="771da-186">若要使用电子工时记录卡或这些工作人员，您必须在工作人员详细信息中指定“使用电子工时记录卡”。</span><span class="sxs-lookup"><span data-stu-id="771da-186">To use electronic timecards or these workers, you must specify, Use timecard, in the worker details.</span></span> <span data-ttu-id="771da-187">电子工时记录卡使工作人员能够登记：</span><span class="sxs-lookup"><span data-stu-id="771da-187">Electronic timecards enable the worker to register:</span></span>

-   <span data-ttu-id="771da-188">日期</span><span class="sxs-lookup"><span data-stu-id="771da-188">Date</span></span>
-   <span data-ttu-id="771da-189">登记类型</span><span class="sxs-lookup"><span data-stu-id="771da-189">Registration type</span></span>
-   <span data-ttu-id="771da-190">工作参考，例如项目、间接活动或生产订单</span><span class="sxs-lookup"><span data-stu-id="771da-190">Job reference, such as project, indirect activity, or production order</span></span>
-   <span data-ttu-id="771da-191">作业标识</span><span class="sxs-lookup"><span data-stu-id="771da-191">Job identification</span></span>
-   <span data-ttu-id="771da-192">时间消耗量</span><span class="sxs-lookup"><span data-stu-id="771da-192">Time consumption</span></span>
-   <span data-ttu-id="771da-193">项目费用</span><span class="sxs-lookup"><span data-stu-id="771da-193">Project fees</span></span>
-   <span data-ttu-id="771da-194">项目物料</span><span class="sxs-lookup"><span data-stu-id="771da-194">Project items</span></span>





