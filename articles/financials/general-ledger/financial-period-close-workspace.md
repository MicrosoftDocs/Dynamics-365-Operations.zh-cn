---
title: "财务期间结帐工作区"
description: "本文提供财务期间结帐工作区和相关配置的概览。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0bbf8f979aeb8b861164e345f9e46bb396f370ce
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="financial-period-close-workspace"></a><span data-ttu-id="f65f9-103">财务期间结帐工作区</span><span class="sxs-lookup"><span data-stu-id="f65f9-103">Financial period close workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f65f9-104">本文提供财务期间结帐工作区和相关配置的概览。</span><span class="sxs-lookup"><span data-stu-id="f65f9-104">This article provides an overview of the Financial period close workspace and the associated configuration.</span></span>

<span data-ttu-id="f65f9-105">财务期间结帐工作区</span><span class="sxs-lookup"><span data-stu-id="f65f9-105">Financial period close workspace</span></span>

<span data-ttu-id="f65f9-106">**财务期间结帐**工作区用于跨公司、区域和人员跟踪财务结帐流程。</span><span class="sxs-lookup"><span data-stu-id="f65f9-106">The **Financial period close** workspace lets you track your financial closing processes across companies, areas, and people.</span></span> <span data-ttu-id="f65f9-107">根据**财务期间结帐**工作区的视图，您将看到结帐计划的所有任务和状态，或仅分配给您的任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-107">Depending on your view of the **Financial period close** workspace, you'll see either of all tasks and statuses for a closing schedule, or just the tasks that are assigned to you.</span></span> 

<span data-ttu-id="f65f9-108">首先必须在该工作区顶部选择一个结帐计划。</span><span class="sxs-lookup"><span data-stu-id="f65f9-108">You must first select a closing schedule at the top of the workspace.</span></span> <span data-ttu-id="f65f9-109">然后将按所选结帐计划筛选该工作区中显示的所有数据。</span><span class="sxs-lookup"><span data-stu-id="f65f9-109">All data that is shown on the workspace is then filtered by the selected closing schedule.</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="f65f9-110">汇总磁贴</span><span class="sxs-lookup"><span data-stu-id="f65f9-110">Summary tiles</span></span>

<span data-ttu-id="f65f9-111">**摘要**磁贴提供流程概述以及帮助您保持跟踪结帐流程的指示器。您可以查看到期任务、当天的剩余任务、当天到期但因为依赖项而被阻止的任务，以及流程的所有剩余任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-111">The **Summary** tiles give an overview of the process, and indicators help you keep the closing process on track. You can see tasks that are past due, remaining tasks for today, tasks that are due today but are blocked because of dependencies, and all remaining tasks for the process.</span></span> <span data-ttu-id="f65f9-112">此信息针对选定结帐计划内安排的所有公司。</span><span class="sxs-lookup"><span data-stu-id="f65f9-112">This information is for all companies that are included in the selected closing schedule.</span></span>

### <a name="tasks-and-status-section"></a><span data-ttu-id="f65f9-113">任务和状态部分</span><span class="sxs-lookup"><span data-stu-id="f65f9-113">Tasks and status section</span></span>

<span data-ttu-id="f65f9-114">在**任务和状态**部分中，将按照各种方式细分整体结帐计划的状态：按公司分类的状态、按区域分类的状态，以及按负责人分类的状态。</span><span class="sxs-lookup"><span data-stu-id="f65f9-114">In the **Tasks and status** section, the status of the overall closing schedule is broken down in various ways: status by company, status by area, and status by person who is responsible.</span></span> <span data-ttu-id="f65f9-115">可以通过更改卡列表顶部的筛选器，查看结帐计划中所有任务的状态、仅当天到期的任务的状态，或者已到期的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="f65f9-115">You can view the status for all tasks in the closing schedule, just tasks that are due today, or tasks that are past due by changing the filter at the top of the card list.</span></span> <span data-ttu-id="f65f9-116">还可以选择公司筛选器以查看特定公司的状态。</span><span class="sxs-lookup"><span data-stu-id="f65f9-116">You can also select the company filter to view the status for a specific company.</span></span> <span data-ttu-id="f65f9-117">每个状态选项卡同时按已完成百分比和剩余任务数量提供细分。</span><span class="sxs-lookup"><span data-stu-id="f65f9-117">Each status tab gives a breakdown by both the percentage that has been completed and the number of tasks that remain.</span></span> <span data-ttu-id="f65f9-118">单击卡或查看**详细信息**操作可按选定卡筛选详细任务列表。</span><span class="sxs-lookup"><span data-stu-id="f65f9-118">Click the card or the **View details** action to filter the detailed task list by the selected card.</span></span> 

<span data-ttu-id="f65f9-119">最后一个卡针对详细任务列表。</span><span class="sxs-lookup"><span data-stu-id="f65f9-119">The last tab is for the detailed task list.</span></span> <span data-ttu-id="f65f9-120">此列表显示完整的任务列表，并可进行筛选，以便仅显示您感兴趣的任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-120">This list shows the full task list and can be filtered so that it shows only the tasks that you're interested in.</span></span> <span data-ttu-id="f65f9-121">可以通过多种方式筛选任务列表。</span><span class="sxs-lookup"><span data-stu-id="f65f9-121">You can filter the task list in several ways.</span></span> <span data-ttu-id="f65f9-122">例如，可以按任务到期日期、关联公司和关联区域进行筛选。</span><span class="sxs-lookup"><span data-stu-id="f65f9-122">For example, you can filter by task due date, associated company, and associated area.</span></span> <span data-ttu-id="f65f9-123">还可以选择在任务列表中显示或隐藏已完成的任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-123">You can also select to show or hide completed tasks in the task list.</span></span> 

<span data-ttu-id="f65f9-124">用于任务的两个指示器：</span><span class="sxs-lookup"><span data-stu-id="f65f9-124">Two indicators are used for tasks:</span></span>

-   <span data-ttu-id="f65f9-125">感叹号图标指示任务已到期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-125">An exclamation point icon indicates that the task is past due.</span></span> <span data-ttu-id="f65f9-126">对于已到期的任务，还将以红色突出显示到期日期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-126">For tasks that are past due, the due date is also highlighted in red.</span></span>
-   <span data-ttu-id="f65f9-127">挂锁图标指示任务依赖于尚未完成的其他任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-127">A padlock icon indicates that the task depends on other tasks that aren't yet completed.</span></span> <span data-ttu-id="f65f9-128">不能将依赖项阻止的任务标记为已完成。</span><span class="sxs-lookup"><span data-stu-id="f65f9-128">A task that is blocked by dependencies can't be marked as completed.</span></span> <span data-ttu-id="f65f9-129">可以通过使用**设置依赖项**操作为任务设置依赖项。</span><span class="sxs-lookup"><span data-stu-id="f65f9-129">You can set dependencies for a task by using the **Set dependency** action.</span></span>

<span data-ttu-id="f65f9-130">任务名称是 Microsoft Dynamics 365 for Operations 页面或用户必须访问才能完成工作的网页的链接。</span><span class="sxs-lookup"><span data-stu-id="f65f9-130">The task name is a hyperlink to the Microsoft Dynamics 365 for Operations page or other webpage where the user must go to complete the work.</span></span> <span data-ttu-id="f65f9-131">可通过在编辑或创建任务时使用**任务链接**字段设置此超链接。</span><span class="sxs-lookup"><span data-stu-id="f65f9-131">You can set this hyperlink by using the **Task link** field when you edit or create a task.</span></span> 

<span data-ttu-id="f65f9-132">可通过使用**附件**操作将文件、注释、图像和 URL 附加到任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-132">You can attach files, notes, images, and URLs to a task by using the **Attachments** action.</span></span> <span data-ttu-id="f65f9-133">例如，可以指示用作任务一部分的日记帐编号，添加有关特定任务的注释，或附加为任务打印的报表文件。</span><span class="sxs-lookup"><span data-stu-id="f65f9-133">For example, you can indicate journal numbers that are used as part of a task, add comments about a specific task, or attach a report file that was printed for a task.</span></span> <span data-ttu-id="f65f9-134">如果有附件，任务的**附件**列中将显示一个图标。</span><span class="sxs-lookup"><span data-stu-id="f65f9-134">An icon appears in the **Attachment** column for the task if an attachment is present.</span></span> 

<span data-ttu-id="f65f9-135">完成任务后，必须手动选择**任务已完成**选项。</span><span class="sxs-lookup"><span data-stu-id="f65f9-135">The **Task complete** option must be manually selected after the task is completed.</span></span> <span data-ttu-id="f65f9-136">任务标记为已完成时，**完成日期**字段将自动更新为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f65f9-136">When a task is marked as completed, the **Completed date** field is automatically updated to the current date and time.</span></span> <span data-ttu-id="f65f9-137">还将根据需要更新依赖项指示器。</span><span class="sxs-lookup"><span data-stu-id="f65f9-137">Dependency indicators are also updated as appropriate.</span></span>

## <a name="all-financial-period-close-tasks-list-page"></a><span data-ttu-id="f65f9-138">所有财务期间结帐任务列表页</span><span class="sxs-lookup"><span data-stu-id="f65f9-138">All financial period close tasks list page</span></span>
<span data-ttu-id="f65f9-139">可以从**所有财务期间结帐任务**列表页查看所有当前和之前期间结帐任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-139">You can view all current and previous period close tasks from the **All financial period close tasks** list page.</span></span> <span data-ttu-id="f65f9-140">此列表页最适合用于对结转流程执行历史分析，因为其中包含有关计划的到期日期、实际完成日期和任务完成人的信息。</span><span class="sxs-lookup"><span data-stu-id="f65f9-140">This list page is best used for historical analysis of your closing process, because it includes information about the scheduled due date, the actual completion date, and the person who completed the task.</span></span> <span data-ttu-id="f65f9-141">可以出于报告和审计目的，将此列表页中的信息轻松导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="f65f9-141">You can easily export the information on this list page to Microsoft Excel for reporting and auditing purposes.</span></span>

## <a name="financial-period-close-configuration-page"></a><span data-ttu-id="f65f9-142">财务期间结帐配置页</span><span class="sxs-lookup"><span data-stu-id="f65f9-142">Financial period close configuration page</span></span>
<span data-ttu-id="f65f9-143">在您可以使用**财务期间结帐**工作区前，您必须使用**财务期间结帐配置**页配置 Microsoft Dynamics 365 for Finance and Operations 中的流程。</span><span class="sxs-lookup"><span data-stu-id="f65f9-143">Before you can use the **Financial period close** workspace, you must configure the process in Microsoft Dynamics 365 for Finance and Operations by using the **Financial period close configuration** page.</span></span> <span data-ttu-id="f65f9-144">（单击**总帐** &gt; **期间结帐** &gt; **财务期间结帐配置**）。</span><span class="sxs-lookup"><span data-stu-id="f65f9-144">(Click **General ledger** &gt; **Period close** &gt; **Financial period close configuration**.)</span></span>

### <a name="resources"></a><span data-ttu-id="f65f9-145">资源</span><span class="sxs-lookup"><span data-stu-id="f65f9-145">Resources</span></span>

<span data-ttu-id="f65f9-146">在**资源**选项卡上，定义结转流程中涉及的人员。</span><span class="sxs-lookup"><span data-stu-id="f65f9-146">On the **Resources** tab, you define the people who are involved in the closing processes.</span></span> <span data-ttu-id="f65f9-147">必须先在此处分配任何负责结帐任务的员工。</span><span class="sxs-lookup"><span data-stu-id="f65f9-147">Any employee who will be responsible for a closing task must first be assigned here.</span></span> <span data-ttu-id="f65f9-148">还必须指定该员工的工作区视图。</span><span class="sxs-lookup"><span data-stu-id="f65f9-148">You must also specify the employee's view of the workspace.</span></span> <span data-ttu-id="f65f9-149">选项如下：</span><span class="sxs-lookup"><span data-stu-id="f65f9-149">The following options are available:</span></span>

-   <span data-ttu-id="f65f9-150">**仅分配的任务** – 用户将只看到分配给他或她的任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-150">**Only assigned tasks** – The user will see only the tasks that are assigned to him or her.</span></span>
-   <span data-ttu-id="f65f9-151">**所有任务和状态** – 用户将看到整个流程的所有结算任务和状态。</span><span class="sxs-lookup"><span data-stu-id="f65f9-151">**All tasks and status** – The user will see all closing tasks and the status of the overall process.</span></span>

<span data-ttu-id="f65f9-152">有权仅查看为其分配的任务的用户不能添加任务到任务列表、不能编辑任务或从任务列表中删除任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-152">Users who have permissions to view only their assigned tasks won't be able to add tasks to the task list, edit tasks, or remove tasks from the task list.</span></span>

### <a name="task-areas"></a><span data-ttu-id="f65f9-153">任务区域</span><span class="sxs-lookup"><span data-stu-id="f65f9-153">Task areas</span></span>

<span data-ttu-id="f65f9-154">您使用任务区域将结算任务分组到您的组织中的逻辑所有权区域。</span><span class="sxs-lookup"><span data-stu-id="f65f9-154">You use task areas to group closing tasks into logical areas of ownership within your organization.</span></span> <span data-ttu-id="f65f9-155">例如，应付账款、应收账款或总帐可以使用为任务区域。</span><span class="sxs-lookup"><span data-stu-id="f65f9-155">For example, Accounts payable, Accounts receivable, or General ledger might be used as task areas.</span></span>

### <a name="calendars"></a><span data-ttu-id="f65f9-156">日历</span><span class="sxs-lookup"><span data-stu-id="f65f9-156">Calendars</span></span>

<span data-ttu-id="f65f9-157">通过使用日历选项卡创建和编辑财务结算日历。在此选项卡上，您将定义结帐流程的工作天数，并还可以使用它来计划结帐任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-157">Create and edit financial closing calendars using the Calendars tab.  This is where you will define the working days for closing processes, and will be used for scheduling closing tasks.</span></span>  <span data-ttu-id="f65f9-158">创建新日历，并指示要用于计划任务的工作日。</span><span class="sxs-lookup"><span data-stu-id="f65f9-158">Create a new calendar, and indicate the working days to be used for task scheduling.</span></span>  <span data-ttu-id="f65f9-159">最好为长期时间创建日历，如一年或多年，因为这样的日历在创建后可以编辑。</span><span class="sxs-lookup"><span data-stu-id="f65f9-159">It is best to create a calendar for long period of time, such as a year or multiple years, since it can be edited after creation.</span></span>  <span data-ttu-id="f65f9-160">在创建日历后，单击“编辑”按钮以针对特定日期（如假期）更新日历。</span><span class="sxs-lookup"><span data-stu-id="f65f9-160">After creating the calendar, click the Edit button to update the calendar for specific days, such as holidays.</span></span>  <span data-ttu-id="f65f9-161">将把结帐任务安排在“控制”值设置为“开放”的日期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-161">Closing tasks will be scheduled on days when the Control value is set to Open.</span></span>  <span data-ttu-id="f65f9-162">如果不应将结帐任务安排在特定日期，应将该日期的“控制”值设置为“已关闭”。</span><span class="sxs-lookup"><span data-stu-id="f65f9-162">If closing tasks should not be schedule on a specific day, that day should have the Control value set to Closed.</span></span>

### <a name="templates"></a><span data-ttu-id="f65f9-163">模板</span><span class="sxs-lookup"><span data-stu-id="f65f9-163">Templates</span></span>

<span data-ttu-id="f65f9-164">可使用财务结帐模板定义结帐流程的所有任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-164">You use a financial close template to define all tasks that are part of a closing process.</span></span> <span data-ttu-id="f65f9-165">结帐任务是每个结帐流程中分配给个人完成的循环工作。</span><span class="sxs-lookup"><span data-stu-id="f65f9-165">A closing task is a recurring work effort that is assigned to an individual to complete as part of each closing process.</span></span> <span data-ttu-id="f65f9-166">在模板中，必须为每个结帐任务定义相对到期日期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-166">In the template, a relative due date must be defined for each closing task.</span></span> <span data-ttu-id="f65f9-167">相对到期日期是每个期间中任务将到期的所定义期间结束日期之前或之后的天数。</span><span class="sxs-lookup"><span data-stu-id="f65f9-167">The relative due date is the number of days before or after the defined period end date that the task will be due each period.</span></span> <span data-ttu-id="f65f9-168">还将为每个任务分配到期时间。</span><span class="sxs-lookup"><span data-stu-id="f65f9-168">A due time is also assigned to each task.</span></span> <span data-ttu-id="f65f9-169">到期时间通过使用您的时区的环境设置，并转换为每个用户的时区。</span><span class="sxs-lookup"><span data-stu-id="f65f9-169">The due time is set by using the context of your time zone and will be converted to the time zone for each user.</span></span> 

<span data-ttu-id="f65f9-170">可以将模板中的任务分配给适合该任务的一家或多家公司。</span><span class="sxs-lookup"><span data-stu-id="f65f9-170">You can assign a task in the template to one or more companies where that task applies.</span></span> <span data-ttu-id="f65f9-171">如果分配其他人以完成每家公司中的工作，您可能发现为相同工作创建多个任务非常有用。</span><span class="sxs-lookup"><span data-stu-id="f65f9-171">If a different person is assigned to complete that work effort in each company, you might find it helpful to create multiple tasks for the same work effort.</span></span> <span data-ttu-id="f65f9-172">为每个公司创建一个任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-172">Create one task for each company.</span></span> 

<span data-ttu-id="f65f9-173">**任务链接**菜单项与任务工作关联，可用于从工作区中的任务链接直接访问关联页面。</span><span class="sxs-lookup"><span data-stu-id="f65f9-173">The **Task link** menu item is associated with the task work effort and can be used to go directly to the associated page from the task link in the workspace.</span></span> <span data-ttu-id="f65f9-174">例如，可将为应付账款运行币种重估的结帐任务链接到 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中关联的**外币重估**页面。</span><span class="sxs-lookup"><span data-stu-id="f65f9-174">For example, a closing task to run the currency revaluation process for Accounts payable can be linked to the associated **Foreign currency revaluation** page in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="f65f9-175">您还可以链接到外部 URL。</span><span class="sxs-lookup"><span data-stu-id="f65f9-175">You can also link to an external URL.</span></span> 

> <span data-ttu-id="f65f9-176">提示：如果要链接特定的 Management Reporter 报表到财务期间结算任务，则可以使用报表 URL。</span><span class="sxs-lookup"><span data-stu-id="f65f9-176">[!Hint] If you want to link a specific Management Reporter report to a financial period close task, you can use the report URL.</span></span> <span data-ttu-id="f65f9-177">若要访问报表 URL，请打开报表设计器中的报表，然后单击**文件** &gt; **查看报表**以在 Web 浏览器中打开报表。</span><span class="sxs-lookup"><span data-stu-id="f65f9-177">To access the report URL, open the report in the report designer, and then click **File** &gt; **View report** to open the report in a web browser.</span></span> <span data-ttu-id="f65f9-178">然后可以复制浏览器地址栏中的 URL 并将其粘贴到**任务链接** **URL** 字段中。</span><span class="sxs-lookup"><span data-stu-id="f65f9-178">You can then copy the URL in the browser's address bar and paste it into the **Task link** **URL** field.</span></span> 

<span data-ttu-id="f65f9-179">可以在模板中定义任务依赖项。</span><span class="sxs-lookup"><span data-stu-id="f65f9-179">You can define task dependencies in the template.</span></span> <span data-ttu-id="f65f9-180">已设置为依赖于一个或多个任务的任务不能将该任务标记为完成，直到所有依赖项完成。</span><span class="sxs-lookup"><span data-stu-id="f65f9-180">If a task has been set up to depend on one or more tasks, that task can't be marked as completed until all the dependencies have been completed.</span></span> 

<span data-ttu-id="f65f9-181">您可以创建多个财务结帐模板。</span><span class="sxs-lookup"><span data-stu-id="f65f9-181">You can create multiple financial close templates.</span></span> <span data-ttu-id="f65f9-182">然后可以使用不同模板跟踪不同期间类型的结算流程，例如月底或年末，或者跟踪使用不同结算流程的公司。</span><span class="sxs-lookup"><span data-stu-id="f65f9-182">You can then use the various templates to track the closing processes for different period types, such as month end or year end, or to track companies that use different closing processes.</span></span> <span data-ttu-id="f65f9-183">在某一模板创建后，可以将其复制到新模板并进行所需的更改。</span><span class="sxs-lookup"><span data-stu-id="f65f9-183">After one template is created, you can copy it to a new template and make the required changes.</span></span> <span data-ttu-id="f65f9-184">只能将一个模板分配到每个结算计划。</span><span class="sxs-lookup"><span data-stu-id="f65f9-184">You can assign only one template to each closing schedule.</span></span>

### <a name="closing-schedules"></a><span data-ttu-id="f65f9-185">结帐计划</span><span class="sxs-lookup"><span data-stu-id="f65f9-185">Closing schedules</span></span>

<span data-ttu-id="f65f9-186">您使用结算计划分配财务结算模板到必须关闭的特定财务期间。</span><span class="sxs-lookup"><span data-stu-id="f65f9-186">You use a closing schedule to assign a financial close template to a specific financial period that must be closed.</span></span> <span data-ttu-id="f65f9-187">模板中的任务然后将为指定期间自动生成，并且，新的结算计划将添加到该工作区。</span><span class="sxs-lookup"><span data-stu-id="f65f9-187">The tasks from the template are then automatically generated for the specified period, and the new closing schedule is added to the workspace.</span></span> <span data-ttu-id="f65f9-188">当您创建新的结算计划时，**期间结束日期**字段用于基于在财务结算模板中分配的相对到期日期确定结算任务的实际到期日期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-188">When you create a new closing schedule, the **Period end date** field is used to determine the actual due dates for the closing tasks, based on the relative due date that is assigned in the financial close template.</span></span> 

<span data-ttu-id="f65f9-189">为结算计划分配相应的日历，指示在任务计划中使用的工作日。</span><span class="sxs-lookup"><span data-stu-id="f65f9-189">Assign the calendar appropriate for the closing schedule, to indicate the working days to be used in task scheduling.</span></span> <span data-ttu-id="f65f9-190">如果未定义特定日历，任务到期日期将使用一周的所有日期。</span><span class="sxs-lookup"><span data-stu-id="f65f9-190">If you don't define a specific calendar, the task due dates will use all days of the week.</span></span> 

<span data-ttu-id="f65f9-191">您还必须定义要与结算计划关联的公司。</span><span class="sxs-lookup"><span data-stu-id="f65f9-191">You must also define the companies that will be associated with the closing schedule.</span></span> <span data-ttu-id="f65f9-192">如果模板任务分配给多个公司，单独的任务将为结算计划中的每个公司创建并且分配给模板任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-192">If template tasks are assigned to multiple companies, separate tasks will be created for each company that is in the closing schedule and assigned to the template task.</span></span> 

<span data-ttu-id="f65f9-193">在结算计划完成后，为其选择**已关闭**选项。</span><span class="sxs-lookup"><span data-stu-id="f65f9-193">After a closing schedule is completed, select the **Closed** option for it.</span></span> <span data-ttu-id="f65f9-194">任务历史记录将仍然在**所有财务期间结帐任务**列表页显示，但是结算计划将从工作区中删除。</span><span class="sxs-lookup"><span data-stu-id="f65f9-194">The task history will still be available from the **All financial period close tasks** list page, but the closing schedule will be removed from the workspace.</span></span> <span data-ttu-id="f65f9-195">在结算计划标记为**已关闭**后，您不能为其添加任务、编辑任务或从中删除任务。</span><span class="sxs-lookup"><span data-stu-id="f65f9-195">After a closing schedule has been marked as **Closed**, you won't be able to add tasks to it, edit tasks, or remove tasks from it.</span></span>



