---
title: "生成财务报表"
description: "本主题提供了有关生成财务报表的信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 2986d218318951b7e46cb5dfafcbd17f2d513755
ms.contentlocale: zh-cn
ms.lasthandoff: 11/14/2017

---

# <a name="generate-a-financial-report"></a><span data-ttu-id="04ec0-103">生成财务报表</span><span class="sxs-lookup"><span data-stu-id="04ec0-103">Generate a financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04ec0-104">本主题提供了有关生成财务报表的信息。</span><span class="sxs-lookup"><span data-stu-id="04ec0-104">This topic provides information about generating a financial report.</span></span> 

<span data-ttu-id="04ec0-105">要生成报表，请打开报表定义然后单击工具栏中的“生成”按钮。</span><span class="sxs-lookup"><span data-stu-id="04ec0-105">To generate a report, open the report definition and then click the Generate button in the toolbar.</span></span> <span data-ttu-id="04ec0-106">“报表队列状态”窗口将打开并指示您的报表在队列中的位置。</span><span class="sxs-lookup"><span data-stu-id="04ec0-106">The Report Queue Status window will open and indicate the location of your report in the queue.</span></span> <span data-ttu-id="04ec0-107">默认情况下，生成的报表将在 Web 查看器中打开。</span><span class="sxs-lookup"><span data-stu-id="04ec0-107">By default, the generated report will open in the Web Viewer.</span></span>

> [!NOTE]
> <span data-ttu-id="04ec0-108">您只能在有权访问的文件夹和位置生成报表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-108">You can generate reports only to folders and locations to which you have permission to access.</span></span>

<span data-ttu-id="04ec0-109">下表说明了可用于生成报表的选项。</span><span class="sxs-lookup"><span data-stu-id="04ec0-109">The following table explains the options that are available for generating reports.</span></span>

| <span data-ttu-id="04ec0-110">选项</span><span class="sxs-lookup"><span data-stu-id="04ec0-110">Option</span></span>                                                                                | <span data-ttu-id="04ec0-111">有关详细信息</span><span class="sxs-lookup"><span data-stu-id="04ec0-111">For more information</span></span> |
|---------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="04ec0-112">设置计划以自动生成报表或报表组</span><span class="sxs-lookup"><span data-stu-id="04ec0-112">Set up a schedule to generate a report or group of reports automatically</span></span>              |                      |
| <span data-ttu-id="04ec0-113">检查报表中是否有缺少的科目或数据，并验证报表的准确性</span><span class="sxs-lookup"><span data-stu-id="04ec0-113">Check for missing accounts or data in a report, and validate the accuracy of a report</span></span> |                      |

<span data-ttu-id="04ec0-114">当您生成报表时，将使用您在报表定义选项卡上指定的选项。</span><span class="sxs-lookup"><span data-stu-id="04ec0-114">When you generate a report, the options that you have specified on the Report definition tabs are used.</span></span> <span data-ttu-id="04ec0-115">输出和分配选项卡可让您指定报表库位置，从而提供了一个共享报表的简单方式。</span><span class="sxs-lookup"><span data-stu-id="04ec0-115">The Output and Distribution tab lets you specify a report library location, which provides an easy way to share the report.</span></span>

## <a name="schedule-report-generation"></a><span data-ttu-id="04ec0-116"> 计划报表生成</span><span class="sxs-lookup"><span data-stu-id="04ec0-116">Schedule report generation</span></span>
<span data-ttu-id="04ec0-117">很多公司有一套核心报表，这些报表以计划的间隔运行以便适应其业务流程。</span><span class="sxs-lookup"><span data-stu-id="04ec0-117">Many companies have a core set of reports that are run at scheduled intervals to align with their business processes.</span></span> <span data-ttu-id="04ec0-118">您可以将报表计划为定期生成，如每天，每周、每月或每年。</span><span class="sxs-lookup"><span data-stu-id="04ec0-118">You can schedule a report to be generated regularly, such as daily, weekly, monthly, or annually.</span></span> <span data-ttu-id="04ec0-119">这可以是单个报表或者包括多个公司的报表组。</span><span class="sxs-lookup"><span data-stu-id="04ec0-119">This can be a single report or a group of reports that includes multiple companies.</span></span> <span data-ttu-id="04ec0-120">您必须为指定的每个公司（例如报告树定义中的公司）输入您的凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-120">You must enter your credentials for each of the companies that are specified, such as those in a reporting tree definition.</span></span> <span data-ttu-id="04ec0-121">如果凭据无效，报表将仅显示您有权访问的信息，如您当时登录的公司。</span><span class="sxs-lookup"><span data-stu-id="04ec0-121">If the credentials are not valid, the report will display only the information that you have permission to access, such as the company that you are logged on to at the time.</span></span> <span data-ttu-id="04ec0-122">输出信息首先从报表组读取，然后从各个报表读取。</span><span class="sxs-lookup"><span data-stu-id="04ec0-122">Output information is read first from the report group, and then from the individual reports.</span></span>

<span data-ttu-id="04ec0-123">在创建并保存报表计划后，它们将显示在“报表计划”下的导航窗格中。</span><span class="sxs-lookup"><span data-stu-id="04ec0-123">As report schedules are created and saved, they are displayed in the navigation pane under Report Schedules.</span></span> <span data-ttu-id="04ec0-124">您可以创建文件夹以整理报表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-124">You can create folders to organize the reports.</span></span> <span data-ttu-id="04ec0-125">如果计划中的单个报表没有运行，其他所有报表将继续运行。</span><span class="sxs-lookup"><span data-stu-id="04ec0-125">If a single report in a schedule does not run, all other reports will continue to run.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ec0-126">若要创建、修改和删除报表计划，您必须具有设计者或管理员角色。</span><span class="sxs-lookup"><span data-stu-id="04ec0-126">To create, modify, and delete report schedules, you must have the role of designer or administrator.</span></span> <span data-ttu-id="04ec0-127">当报表运行后，创建计划的用户的凭据将用于生成报表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-127">When a report is run, the credentials of the user who created the schedule are used to generate the report.</span></span>


### <a name="create-a-report-schedule"></a><span data-ttu-id="04ec0-128">创建报表计划</span><span class="sxs-lookup"><span data-stu-id="04ec0-128">Create a report schedule</span></span>

1.  <span data-ttu-id="04ec0-129">在报表设计器中的“文件”菜单上，单击“新建”，然后选择“报表计划”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-129">In Report Designer, on the File menu, click New, and then select Report schedule.</span></span> <span data-ttu-id="04ec0-130">此时将打开“新建报表计划”对话框。</span><span class="sxs-lookup"><span data-stu-id="04ec0-130">The New Report Schedule dialog box opens.</span></span>
2.  <span data-ttu-id="04ec0-131">在“设置”下，选择要计划的单独报表或报表组。</span><span class="sxs-lookup"><span data-stu-id="04ec0-131">Under Settings, select an individual report or a report group to schedule.</span></span> <span data-ttu-id="04ec0-132">只有您当前登录到的公司或所选构建基块的报表或报表组可供使用。</span><span class="sxs-lookup"><span data-stu-id="04ec0-132">Only reports or report groups for the company or building block selection that you are currently logged on to are available.</span></span>
3.  <span data-ttu-id="04ec0-133">选中“活动”复选框以启用报表计划。</span><span class="sxs-lookup"><span data-stu-id="04ec0-133">Select the Active check box to turn on the report schedule.</span></span> <span data-ttu-id="04ec0-134">只有报表的创建者或管理员才能启用或停用报表计划。</span><span class="sxs-lookup"><span data-stu-id="04ec0-134">Only the creator of the report or an administrator can activate or inactivate a report schedule.</span></span>
4.  <span data-ttu-id="04ec0-135">单击“权限”按钮以输入公司凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-135">Click the Permissions button to enter company credentials.</span></span> <span data-ttu-id="04ec0-136">默认情况下，您的登录信息将用于您登录到的公司。</span><span class="sxs-lookup"><span data-stu-id="04ec0-136">By default, your logon information is used for the company that you are logged on to.</span></span> <span data-ttu-id="04ec0-137">如果包括其他公司（例如在报告树定义中），请选择“使用不同凭据”，然后为报表计划中包括的其他任何公司输入凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-137">If other companies are included, such as in reporting tree definitions, select Use separate credentials, and then enter the credentials for any other company that is included in the report schedule.</span></span> <span data-ttu-id="04ec0-138">您可以选择“Windows 身份验证”或为每个公司键入用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="04ec0-138">You can select Windows Authentication or type a user name and password for each company.</span></span> <span data-ttu-id="04ec0-139">选中“保存凭据”复选框以保存这些公司的凭据，然后单击“确定”以关闭该对话框。</span><span class="sxs-lookup"><span data-stu-id="04ec0-139">Select the Save credentials check box to save the credentials for these companies, and then click OK to close the dialog box.</span></span>
5.  <span data-ttu-id="04ec0-140">在“频率”下的“开始重复执行”字段中，选择开始计划的日期。</span><span class="sxs-lookup"><span data-stu-id="04ec0-140">Under Frequency, in the Start recurrence field, select the date when the schedule is to start.</span></span> <span data-ttu-id="04ec0-141">默认情况下，会选择客户端计算机的当前系统日期。</span><span class="sxs-lookup"><span data-stu-id="04ec0-141">By default, the current system date of the client computer is selected.</span></span>
6.  <span data-ttu-id="04ec0-142">在“运行报表的时间”字段中，选择应该运行报表的时间。</span><span class="sxs-lookup"><span data-stu-id="04ec0-142">In the Run report at field, select the time when the report should run.</span></span> <span data-ttu-id="04ec0-143">如果您输入的时间早于当前系统时间，报表将在下一个计划日期运行。</span><span class="sxs-lookup"><span data-stu-id="04ec0-143">If you enter a time that is before the current system time, the report runs on the next scheduled date.</span></span>
7.  <span data-ttu-id="04ec0-144">在“重复模式”区域中，指定运行报表的频率。</span><span class="sxs-lookup"><span data-stu-id="04ec0-144">In the Recurrence pattern area, specify how often the report is run.</span></span> <span data-ttu-id="04ec0-145">默认情况下，系统将选择“每日”并将“间隔(天)”值设为 1。</span><span class="sxs-lookup"><span data-stu-id="04ec0-145">By default, Daily is selected with an Interval (days) value of 1.</span></span> <span data-ttu-id="04ec0-146">其他选项包括“每周”、“每月”和“每年”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-146">Other options include Weekly, Monthly, and Yearly.</span></span>
8.  <span data-ttu-id="04ec0-147">在“重复范围”区域中，选择应停止生成报表的时间。</span><span class="sxs-lookup"><span data-stu-id="04ec0-147">In the Range of recurrence area, select when the report should stop being generated.</span></span>
    -   <span data-ttu-id="04ec0-148">无结束日期 – 报表计划将无限期运行。</span><span class="sxs-lookup"><span data-stu-id="04ec0-148">No end date – The report schedule runs indefinitely.</span></span>
    -   <span data-ttu-id="04ec0-149">设置发生次数 – 报表计划运行指定次数，然后停用报表计划。</span><span class="sxs-lookup"><span data-stu-id="04ec0-149">Set number of occurrences – The report schedule runs for the specified number of times, and then is inactivated.</span></span>
    -   <span data-ttu-id="04ec0-150">结束日期 – 报表计划将于指定日期结束。</span><span class="sxs-lookup"><span data-stu-id="04ec0-150">End by – The report schedule ends on the specified date.</span></span>

9.  <span data-ttu-id="04ec0-151">单击工具栏中的“保存”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-151">Click Save in the toolbar.</span></span> <span data-ttu-id="04ec0-152">在“另存为对话框中，输入报表计划的唯一名称和描述。</span><span class="sxs-lookup"><span data-stu-id="04ec0-152">In the Save As dialog box, enter a unique name and description for the report schedule.</span></span>

<span data-ttu-id="04ec0-153">要复制报表计划，您必须具有设计人员或管理员角色。</span><span class="sxs-lookup"><span data-stu-id="04ec0-153">To copy a report schedule, you must have the role of designer or administrator.</span></span> <span data-ttu-id="04ec0-154">即使管理员修改了报表计划，报表仍将保留创建报表的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-154">Even if an administrator modifies the report schedule, the report maintains the credentials of the user who created the report.</span></span>
### <a name="copy-a-report-schedule"></a><span data-ttu-id="04ec0-155">复制报表计划</span><span class="sxs-lookup"><span data-stu-id="04ec0-155">Copy a report schedule</span></span>

1.  <span data-ttu-id="04ec0-156">在报表设计器中，单击导航窗格中的“报表计划”，然后打开要复制的报表计划。</span><span class="sxs-lookup"><span data-stu-id="04ec0-156">In Report Designer, click Report Schedules in the navigation pane, and open a report schedule to copy.</span></span>
2.  <span data-ttu-id="04ec0-157">在“文件”菜单中，单击“另存为”，然后在“另存为”对话框中为该计划输入新名称和说明。</span><span class="sxs-lookup"><span data-stu-id="04ec0-157">On the File menu, click Save As, and then enter a new name and description for the schedule in the Save As dialog box.</span></span> <span data-ttu-id="04ec0-158">单击“确定”，新计划将显示在导航窗格中。</span><span class="sxs-lookup"><span data-stu-id="04ec0-158">Click OK, and the new schedule is displayed in the navigation pane.</span></span>
3.  <span data-ttu-id="04ec0-159">在新计划中，按需修改字段和信息，然后单击工具栏上的“保存”，或单击“文件”菜单上的“保存”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-159">In the new schedule, modify the fields and information as needed, and then click Save on the toolbar, or click Save on the File menu.</span></span>

<span data-ttu-id="04ec0-160">要删除报表计划，您必须是报表计划的所有者或具有管理员角色。</span><span class="sxs-lookup"><span data-stu-id="04ec0-160">To delete a report schedule, you must be the owner of the report schedule or have a role of administrator.</span></span>
### <a name="delete-a-report-schedule"></a><span data-ttu-id="04ec0-161">删除报表计划</span><span class="sxs-lookup"><span data-stu-id="04ec0-161">Delete a report schedule</span></span>

1.  <span data-ttu-id="04ec0-162">在报表设计器中，单击导航窗格中的“报表计划”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-162">In Report Designer, click Report Schedules in the navigation pane.</span></span>
2.  <span data-ttu-id="04ec0-163">选择要删除的报表计划，然后单击“删除”或者按 Delete 键。</span><span class="sxs-lookup"><span data-stu-id="04ec0-163">Select the report schedule to delete, and then click Delete or press the Delete key.</span></span>
3.  <span data-ttu-id="04ec0-164">在删除确认对话框中，单击“是”以永久删除该报表计划。</span><span class="sxs-lookup"><span data-stu-id="04ec0-164">In the deletion verification dialog box, click Yes to permanently delete the report schedule.</span></span> <span data-ttu-id="04ec0-165">如果您无权删除计划，系统将显示一条消息，并且报表不会删除。</span><span class="sxs-lookup"><span data-stu-id="04ec0-165">If you do not have permission to delete the schedule, a message is displayed and the report is not deleted.</span></span>

### <a name="credentials-and-report-schedules"></a><span data-ttu-id="04ec0-166">凭据和报表计划</span><span class="sxs-lookup"><span data-stu-id="04ec0-166">Credentials and report schedules</span></span>

<span data-ttu-id="04ec0-167">如果您未输入报表中包含的所有公司需要的凭据，则会在保存报表计划时收到以下消息：“您必须输入您针对此报表计划中包含的公司的凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-167">If you do not enter credentials that are required for all companies included in the reports, you receive the following message when you save the report schedule: “You must enter your credentials for the companies that are contained in this report schedule.</span></span> <span data-ttu-id="04ec0-168">选择“权限”按钮以输入您的凭据。”</span><span class="sxs-lookup"><span data-stu-id="04ec0-168">Select the Permissions button to enter in your credentials.”</span></span>

<span data-ttu-id="04ec0-169">例如，Phyllis 使用其登录名和密码登录到公司 A。</span><span class="sxs-lookup"><span data-stu-id="04ec0-169">For example, Phyllis logs on to Company A using her logon and password.</span></span> <span data-ttu-id="04ec0-170">她为使用报告结构树定义的报表创建了一个计划以从多个公司收集数据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-170">She creates a schedule for a report that uses a reporting tree definition to collect data from multiple companies.</span></span> <span data-ttu-id="04ec0-171">保存此报表计划后，系统将提示 Phyllis 为报告树定义中指定的其他公司输入凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-171">When this report schedule is saved, Phyllis is prompted to enter the credentials for the other companies that are specified in the reporting tree definition.</span></span> <span data-ttu-id="04ec0-172">当您的凭据到期时，如果未更新凭据，则报表计划中受影响的报表不会生成。</span><span class="sxs-lookup"><span data-stu-id="04ec0-172">When your credentials expire, the affected reports in the report schedule are not generated until the credentials have been updated.</span></span> <span data-ttu-id="04ec0-173">报表队列中将显示一条消息，指示权限必须更新。</span><span class="sxs-lookup"><span data-stu-id="04ec0-173">A message is displayed in the report queue to indicate that permissions must be updated.</span></span> <span data-ttu-id="04ec0-174">如果出现以下情况，报表计划将失败（因为它们需要凭据）:</span><span class="sxs-lookup"><span data-stu-id="04ec0-174">The report schedule fails if any of the following scenarios occur (because they require credentials):</span></span>
-   <span data-ttu-id="04ec0-175">向单独报表的报告结构树添加了新公司。</span><span class="sxs-lookup"><span data-stu-id="04ec0-175">A new company has been added to a report tree for an individual report.</span></span>
-   <span data-ttu-id="04ec0-176">已修改报表组中的某个报表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-176">A report in a report group has been modified.</span></span>
-   <span data-ttu-id="04ec0-177">已将其他公司的某个新报表添加到报表组。</span><span class="sxs-lookup"><span data-stu-id="04ec0-177">A new report for an additional company has been added to a report group.</span></span>

<span data-ttu-id="04ec0-178">要继续，请单击“报表计划”对话框中的“权限”按钮，然后输入相应的凭据。</span><span class="sxs-lookup"><span data-stu-id="04ec0-178">To continue, click the Permissions button in the Report Scheduling dialog box, and then enter the appropriate credentials.</span></span>

## <a name="missing-account-analysis-feature"></a><span data-ttu-id="04ec0-179">缺少的会计科目分析功能</span><span class="sxs-lookup"><span data-stu-id="04ec0-179">Missing account analysis feature</span></span>
<span data-ttu-id="04ec0-180">您可以在构建基块组中搜索可能在所有行定义、报告结构树定义和报表定义中缺少的财务科目和维度。</span><span class="sxs-lookup"><span data-stu-id="04ec0-180">You can search for financial accounts and dimensions that might be missing across all row definitions, reporting tree definitions, and report definitions in a building block group.</span></span> <span data-ttu-id="04ec0-181">当您在短期内创建或更新了多个科目或构建基块，并且希望验证所有新信息是否都包含在报表中时，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="04ec0-181">This is useful when you create or update several account or building blocks during a short time period, and you want to verify that all new information is included in your reports.</span></span>

<span data-ttu-id="04ec0-182">缺少科目通过使用行定义或报告结构树定义中的最低和最高值确定，然后显示不在行定义或报告结构树定义中但在财务数据中的科目的列表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-182">Missing accounts are determined by using the lowest and highest values from the row definition or reporting tree definition, and then displays a list of accounts that are not in the row definition or reporting tree definition, but that are in the financial data.</span></span> <span data-ttu-id="04ec0-183">如果某个缺少的会计科目大于或小于行定义中的值，则不会在缺少的会计科目列表中包含该会计科目。</span><span class="sxs-lookup"><span data-stu-id="04ec0-183">If a missing account is greater than or less than the values in the row definition, that account is not included in the list of missing accounts.</span></span>

> [!TIP]
> <span data-ttu-id="04ec0-184">出于验证目的，应在生成月报表之前且创建新的构建基块之时执行此过程。</span><span class="sxs-lookup"><span data-stu-id="04ec0-184">For validation purposes, this process should be run before you generate monthly reports and when you create new building blocks.</span></span>

<span data-ttu-id="04ec0-185">包含值的范围的报表不太可能有缺少的科目。</span><span class="sxs-lookup"><span data-stu-id="04ec0-185">Reports that have ranges of values are less likely to have missing accounts.</span></span> <span data-ttu-id="04ec0-186">请尽可能使用构建基块中的范围，以便在创建新科目后将其包含在内。</span><span class="sxs-lookup"><span data-stu-id="04ec0-186">When possible, use ranges in the building block to include new accounts when they are created.</span></span> <span data-ttu-id="04ec0-187">如果任何报表定义设置为 @ANY 公司，则可以登录到某个特定公司并对该公司运行缺少科目分析。</span><span class="sxs-lookup"><span data-stu-id="04ec0-187">If any report definition is set to @ANY company, then you can log on to a specific company and run a missing account analysis for that company.</span></span>

> [!NOTE]
> <span data-ttu-id="04ec0-188">如果添加了一个新公司，您必须将该公司添加到所有现有报表中的报告结构树，否则该公司不会包含在缺少科目分析中。</span><span class="sxs-lookup"><span data-stu-id="04ec0-188">If a new company has been added, you must add the new company to the reporting trees in any existing reports or the company will not be included in the missing account analysis.</span></span>


### <a name="run-missing-account-analysis"></a><span data-ttu-id="04ec0-189">运行缺少科目分析</span><span class="sxs-lookup"><span data-stu-id="04ec0-189">Run missing account analysis</span></span>

1.  <span data-ttu-id="04ec0-190">在报表设计器中，单击“工具”，然后单击“缺少科目分析”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-190">In Report Designer, click Tools, and then click Missing Account Analysis.</span></span>
2.  <span data-ttu-id="04ec0-191">在“公司筛选器”字段中，选择一个要筛选其结果的公司，或选择“全部(不筛选)”以显示所有可用公司的结果。</span><span class="sxs-lookup"><span data-stu-id="04ec0-191">In the Company filter field, select a company to filter results on, or select All (no filter) to display results from all available companies.</span></span>
3.  <span data-ttu-id="04ec0-192">在“维度筛选器”字段中，选择一个要筛选其结果的维度，或选择“全部(不筛选)”以查看所有可用维度的所有维度信息。</span><span class="sxs-lookup"><span data-stu-id="04ec0-192">In the Dimension filter field, select a dimension to filter results on, or select All (no filter) to view all dimension information for all available dimensions.</span></span>
4.  <span data-ttu-id="04ec0-193">在“分组方式”字段中，选择一个用于对结果进行排序的选项。</span><span class="sxs-lookup"><span data-stu-id="04ec0-193">In the Group by field, select an option for sorting the results.</span></span> <span data-ttu-id="04ec0-194">你可以根据受影响的构建基块对结果进行排序，也可以按维度和值集对结果进行排序。</span><span class="sxs-lookup"><span data-stu-id="04ec0-194">You can sort results according to the building block that is affected, or you can sort results by dimension and value sets.</span></span>
5.  <span data-ttu-id="04ec0-195">查看显示的结果。</span><span class="sxs-lookup"><span data-stu-id="04ec0-195">Review the displayed results.</span></span> <span data-ttu-id="04ec0-196">当你在上方窗格中选择某个项目时，下方窗格将显示有关例外的其他信息。</span><span class="sxs-lookup"><span data-stu-id="04ec0-196">When you select an item in the upper pane, the lower pane displays additional information about the exception.</span></span> <span data-ttu-id="04ec0-197">这包括相关维度、值和报表。</span><span class="sxs-lookup"><span data-stu-id="04ec0-197">This includes related dimensions, values, and reports.</span></span>
6.  <span data-ttu-id="04ec0-198">要打开受影响的项目，请单击在列表窗格中显示的关联图标，或者右键单击该项目并选择“打开”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-198">To open the affected item, click the associated icon that is displayed in the list pane, or right-click the item and select Open.</span></span> <span data-ttu-id="04ec0-199">要选择多个项目，请在按住 Ctrl 键的同时选择下部窗格中的项目。</span><span class="sxs-lookup"><span data-stu-id="04ec0-199">To select multiple items, hold down the Ctrl key while you select the items in the lower pane.</span></span>
7.  <span data-ttu-id="04ec0-200">如果返回的任何值、构建基块或报表不应包含在分析中，请右键单击该项目并选择“排除”，或者选中该项目旁边的“排除”复选框以从列表中删除该项目。</span><span class="sxs-lookup"><span data-stu-id="04ec0-200">If any values, building blocks, or reports are returned that should not be included in the analysis, right-click the item and select Exclude, or select the Exclude check box next to the item to remove the item from the list.</span></span> <span data-ttu-id="04ec0-201">刷新列表后，排除的项目不会包含在内。</span><span class="sxs-lookup"><span data-stu-id="04ec0-201">Excluded items are not included when the list is refreshed.</span></span> <span data-ttu-id="04ec0-202">若要选择多个项目，请在下方窗格中选中项目的同时按住 Ctrl 键。</span><span class="sxs-lookup"><span data-stu-id="04ec0-202">To select multiple items, hold down the Ctrl key while you select the items in the lower pane.</span></span> <span data-ttu-id="04ec0-203">若要查看所有项目，包括您以前选择将其排除在分析之外的任何结果，请选中“显示已排除的构建基块和值”复选框，然后单击“刷新”。</span><span class="sxs-lookup"><span data-stu-id="04ec0-203">To view all items, including any results that you previously selected to exclude from the analysis, select the Show excluded building blocks and values check box, and then click Refresh.</span></span>
8.  <span data-ttu-id="04ec0-204">单击“刷新”可刷新已解决的例外。</span><span class="sxs-lookup"><span data-stu-id="04ec0-204">Click Refresh to refresh exceptions that you have addressed.</span></span> <span data-ttu-id="04ec0-205">单击“是”可完全刷新所有结果，单击“否”可部分刷新已解决的项目。</span><span class="sxs-lookup"><span data-stu-id="04ec0-205">Click Yes to perform a full refresh of all of the results, or click No to perform a partial refresh of addressed items.</span></span>

    > [!NOTE]
    > <span data-ttu-id="04ec0-206">此窗体将在打开时自动刷新，除非在过去 15 分钟之内打开过该窗体。</span><span class="sxs-lookup"><span data-stu-id="04ec0-206">The form is automatically refreshed when it opens, unless the form has been opened in the last 15 minutes.</span></span>

9.  <span data-ttu-id="04ec0-207">解决问题后，单击“确定”以关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="04ec0-207">When the issues are resolved, click OK to close the dialog box.</span></span>

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a><span data-ttu-id="04ec0-208">缺少科目分析的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="04ec0-208">Keyboard shortcuts for missing account analysis</span></span>
<span data-ttu-id="04ec0-209">在您运行缺少科目分析时，可使用以下键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="04ec0-209">When you run a missing account analysis, the following keyboard shortcuts are available.</span></span>

| <span data-ttu-id="04ec0-210">要完成的任务</span><span class="sxs-lookup"><span data-stu-id="04ec0-210">To do this</span></span>                           | <span data-ttu-id="04ec0-211">使用此键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="04ec0-211">Use this keyboard shortcut</span></span> |
|--------------------------------------|----------------------------|
| <span data-ttu-id="04ec0-212">按公司筛选</span><span class="sxs-lookup"><span data-stu-id="04ec0-212">Filter by company</span></span>                    | <span data-ttu-id="04ec0-213">Alt+C</span><span class="sxs-lookup"><span data-stu-id="04ec0-213">Alt+C</span></span>                      |
| <span data-ttu-id="04ec0-214">按维度筛选</span><span class="sxs-lookup"><span data-stu-id="04ec0-214">Filter by dimension</span></span>                  | <span data-ttu-id="04ec0-215">Alt+D</span><span class="sxs-lookup"><span data-stu-id="04ec0-215">Alt+D</span></span>                      |
| <span data-ttu-id="04ec0-216">选择“分组方式”字段</span><span class="sxs-lookup"><span data-stu-id="04ec0-216">Select the Group by field</span></span>            | <span data-ttu-id="04ec0-217">Alt+G</span><span class="sxs-lookup"><span data-stu-id="04ec0-217">Alt+G</span></span>                      |
| <span data-ttu-id="04ec0-218">显示已排除的基块和值</span><span class="sxs-lookup"><span data-stu-id="04ec0-218">Show excluded blocks and values</span></span>      | <span data-ttu-id="04ec0-219">Alt+S</span><span class="sxs-lookup"><span data-stu-id="04ec0-219">Alt+S</span></span>                      |
| <span data-ttu-id="04ec0-220">刷新结果</span><span class="sxs-lookup"><span data-stu-id="04ec0-220">Refresh results</span></span>                      | <span data-ttu-id="04ec0-221">Alt+R</span><span class="sxs-lookup"><span data-stu-id="04ec0-221">Alt+R</span></span>                      |
| <span data-ttu-id="04ec0-222">排除所选构建基块</span><span class="sxs-lookup"><span data-stu-id="04ec0-222">Exclude the selected building block</span></span>  | <span data-ttu-id="04ec0-223">Alt+X</span><span class="sxs-lookup"><span data-stu-id="04ec0-223">Alt+X</span></span>                      |
| <span data-ttu-id="04ec0-224">排除所选行定义</span><span class="sxs-lookup"><span data-stu-id="04ec0-224">Exclude the selected row definition</span></span>  | <span data-ttu-id="04ec0-225">Ctrl+B</span><span class="sxs-lookup"><span data-stu-id="04ec0-225">Ctrl+B</span></span>                     |
| <span data-ttu-id="04ec0-226">排除所选维度值</span><span class="sxs-lookup"><span data-stu-id="04ec0-226">Exclude the selected dimension value</span></span> | <span data-ttu-id="04ec0-227">Ctrl+D</span><span class="sxs-lookup"><span data-stu-id="04ec0-227">Ctrl+D</span></span>                     |
| <span data-ttu-id="04ec0-228">打开所选报表定义</span><span class="sxs-lookup"><span data-stu-id="04ec0-228">Open the selected report definition</span></span>  | <span data-ttu-id="04ec0-229">Ctrl+R</span><span class="sxs-lookup"><span data-stu-id="04ec0-229">Ctrl+R</span></span>                     |
| <span data-ttu-id="04ec0-230">打开所选行定义</span><span class="sxs-lookup"><span data-stu-id="04ec0-230">Open the selected row definition</span></span>     | <span data-ttu-id="04ec0-231">Ctrl+O</span><span class="sxs-lookup"><span data-stu-id="04ec0-231">Ctrl+O</span></span>                     |

 
<a name="see-also"></a><span data-ttu-id="04ec0-232">请参阅</span><span class="sxs-lookup"><span data-stu-id="04ec0-232">See also</span></span>
--------

[<span data-ttu-id="04ec0-233">财务申报</span><span class="sxs-lookup"><span data-stu-id="04ec0-233">Financial reporting</span></span>](financial-reporting-intro.md)

[<span data-ttu-id="04ec0-234">报表设计器界面</span><span class="sxs-lookup"><span data-stu-id="04ec0-234">Report Designer interface</span></span>](report-designer-interface.md)



