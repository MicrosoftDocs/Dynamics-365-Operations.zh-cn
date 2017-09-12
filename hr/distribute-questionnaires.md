---
title: "分配和完成调查表"
description: "本主题描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b2b1b99fd4c7c439ad89440827ad78173d371855
ms.openlocfilehash: c3afd12ed82935cd3d4b1c4ebeab62892cfe7178
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="fab5d-103">分配和完成调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fab5d-104">本主题描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="fab5d-105">有多种方式来分配调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="fab5d-106">将调查表标记为有效。</span><span class="sxs-lookup"><span data-stu-id="fab5d-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="fab5d-107">然后，调查表可用于所有员工，除非设置调查表组来限制对它的访问。</span><span class="sxs-lookup"><span data-stu-id="fab5d-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="fab5d-108">向调查表组分配权限。</span><span class="sxs-lookup"><span data-stu-id="fab5d-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="fab5d-109">然后，调查表可供所选组的所有成员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="fab5d-110">创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-110">Create planned answer sessions.</span></span> <span data-ttu-id="fab5d-111">然后，调查表只可供特定人员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="fab5d-112">创建计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-112">Create a schedule.</span></span> <span data-ttu-id="fab5d-113">然后，调查表中可供多个人员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="fab5d-114">将调查表标记为有效</span><span class="sxs-lookup"><span data-stu-id="fab5d-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="fab5d-115">通过在**调查表**页上将**有效**字段设置为**是**，您使调查表可供所有员工使用并完成。</span><span class="sxs-lookup"><span data-stu-id="fab5d-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="fab5d-116">调查对象可以多次完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="fab5d-117">如果您要全年收集连续反馈，则此功能十分有用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="fab5d-118">例如，您可以让员工使用调查表来提供有关在自助服务餐厅享用午餐服务的反馈。</span><span class="sxs-lookup"><span data-stu-id="fab5d-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="fab5d-119">调查表组</span><span class="sxs-lookup"><span data-stu-id="fab5d-119">Questionnaire groups</span></span>
<span data-ttu-id="fab5d-120">您可以设置调查表组，然后包括调查表应分配到的调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="fab5d-121">可以从以下页面创建调查表组：</span><span class="sxs-lookup"><span data-stu-id="fab5d-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="fab5d-122">**调查表组**– 只有调查表组中的个人可以完成选定的调查表组。</span><span class="sxs-lookup"><span data-stu-id="fab5d-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="fab5d-123">例如，您的预期受众是承包商，因此您可以创建特定于这些调查对象的调查表组。</span><span class="sxs-lookup"><span data-stu-id="fab5d-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="fab5d-124">**调查表组成员** – 您可以向调查表组添加人员。</span><span class="sxs-lookup"><span data-stu-id="fab5d-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="fab5d-125">若要将调查表组分配给某一调查表，请在**调查表**页上，单击**用户权限**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="fab5d-126">在调查表保存为有效后，调查表组的成员可以完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="fab5d-127">如果您想要先对一组特定的人员测试某一调查表，然后再将其展开到一个更大的组，或者，如果您想要使调查表面向非常具体的受众，则此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="fab5d-128">调查表中的计划应答期</span><span class="sxs-lookup"><span data-stu-id="fab5d-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="fab5d-129">计划应答期是您设计并选择调查对象的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="fab5d-130">**注释**在您可以设置计划应答期之前，必须设计调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="fab5d-131">在**“计划应答期”**页上，您可为单独的员工创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="fab5d-132">该页面上的列表显示所有已编制的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="fab5d-133">计划应答期还用于**“调查表计划”**页上，在那里您可以为多人计划调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="fab5d-134">员工</span><span class="sxs-lookup"><span data-stu-id="fab5d-134">Employees</span></span>
-   <span data-ttu-id="fab5d-135">课程参与者</span><span class="sxs-lookup"><span data-stu-id="fab5d-135">Course participants</span></span>
-   <span data-ttu-id="fab5d-136">组织单位</span><span class="sxs-lookup"><span data-stu-id="fab5d-136">Organizational units</span></span>

<span data-ttu-id="fab5d-137">每个人只能回答调查表一次。</span><span class="sxs-lookup"><span data-stu-id="fab5d-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="fab5d-138">计划调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="fab5d-139">（可选）您可以为多个调查对象计划调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="fab5d-140">计划类型</span><span class="sxs-lookup"><span data-stu-id="fab5d-140">Planning types</span></span>

<span data-ttu-id="fab5d-141">如果您想要为多个调查对象安排计划的回答会话，则需要计划类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="fab5d-142">计划类型用于对调查表计划分类。</span><span class="sxs-lookup"><span data-stu-id="fab5d-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="fab5d-143">例如，您可能会出于以下目的计划调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="fab5d-144">评估</span><span class="sxs-lookup"><span data-stu-id="fab5d-144">Evaluation</span></span>
-   <span data-ttu-id="fab5d-145">调查</span><span class="sxs-lookup"><span data-stu-id="fab5d-145">Survey</span></span>
-   <span data-ttu-id="fab5d-146">正在测试</span><span class="sxs-lookup"><span data-stu-id="fab5d-146">Testing</span></span>

<span data-ttu-id="fab5d-147">您可以在**“调查表计划”**页上为调查表计划指定计划类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="fab5d-148">调查表的参考类型</span><span class="sxs-lookup"><span data-stu-id="fab5d-148">Reference types for questionnaire</span></span>

<span data-ttu-id="fab5d-149">您可以使用参考类型输入您可以在计划调查表时选择的回应者的条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="fab5d-150">使用**“参考类型”**页可以设置调查表的参考类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="fab5d-151">每个参考类型对应于 Microsoft Dynamics 365 for Finance and Operations 中的某个表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fab5d-152">在您创建调查表计划时，可以指定表中记录或指定调查表将关联的一系列记录。</span><span class="sxs-lookup"><span data-stu-id="fab5d-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="fab5d-153">例如，如果您选择“课程”表，您可以确定调查表将针对哪一个特定课程。</span><span class="sxs-lookup"><span data-stu-id="fab5d-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="fab5d-154">在您为“课程”表设置参考时，**“课程”**页上的某些字段和按钮将可用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="fab5d-155">调查表计划</span><span class="sxs-lookup"><span data-stu-id="fab5d-155">Questionnaire schedules</span></span>

<span data-ttu-id="fab5d-156">您可以使用调查表计划基于参考类型为一组用户生成多个计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="fab5d-157">在**调查表计划**页上创建计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="fab5d-158">选择计划类型对计划进行分类，并且选择应用于在系统中查询特定用户的参考类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="fab5d-159">例如，如果您将参考类型设置为“课程”表，则您可以在**参考**字段中选择特定课程。</span><span class="sxs-lookup"><span data-stu-id="fab5d-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="fab5d-160">单击**“设置详细信息”**可以选择调查表和其他条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="fab5d-161">例如，如果调查表是对教师的评估，则指定教师的名称作为条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="fab5d-162">在您完成输入设置详细信息后，系统将为查询中包括的用户生成计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="fab5d-163">单击**“计划应答期”**可以查看计划的应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="fab5d-164">然后，您可以手动创建附加计划应答期或删除尚未回答的计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="fab5d-165">单击**功能** &gt; **开始**可以使计划调查表在相关计划应答期中可供用户使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="fab5d-166">单击**“回答”**可以查看该调查表的已完成响应。</span><span class="sxs-lookup"><span data-stu-id="fab5d-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="fab5d-167">（可选）您可以复制调查表计划设置、计划应答期和对新计划调查表的回答。</span><span class="sxs-lookup"><span data-stu-id="fab5d-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="fab5d-168">告知调查对象调查表对其可用</span><span class="sxs-lookup"><span data-stu-id="fab5d-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="fab5d-169">在分发调查表时，您必须通知调查对象调查表对其可用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="fab5d-170">向调查对象通知计划应答期</span><span class="sxs-lookup"><span data-stu-id="fab5d-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="fab5d-171">如果您使用计划应答期，您必须直接通知人员，例如通过电话或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fab5d-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="fab5d-172">向调查对象通知相关计划</span><span class="sxs-lookup"><span data-stu-id="fab5d-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="fab5d-173">使用“**调查表计划**”页可以准备电子邮件并将其发送给分配有调查表的调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="fab5d-174">在**“员工自助服务的电子邮件”**选项卡上输入电子邮件文本。</span><span class="sxs-lookup"><span data-stu-id="fab5d-174">Enter the email text on the **E-mail for employee self service** tab.</span></span> <span data-ttu-id="fab5d-175">在计划开始后，单击**功能** &gt; **发送电子邮件**以生成电子邮件并将其发送给调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-175">After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="fab5d-176">然后调查对象可以登录到该网站并完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-176">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="fab5d-177">**注释**在您可以使用电子邮件功能之前，您的 IT 管理员必须在**电子邮件参数**页上输入电子邮件设置。</span><span class="sxs-lookup"><span data-stu-id="fab5d-177">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="fab5d-178">结束预定的调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-178">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="fab5d-179">您可以在所有回应者都已完成他们的分配的应答期后，结束计划的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-179">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="fab5d-180">在结束后某一计划的调查表，您不能将其设置为新计划编制。</span><span class="sxs-lookup"><span data-stu-id="fab5d-180">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="fab5d-181">**注释**如果一个或多个调查对象尚未完成调查表并且您仍要结束计划编制，则首先在**计划应答期**页上的列表中删除这些调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-181">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="fab5d-182">然后，即可结束计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-182">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="fab5d-183">填写调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-183">Completing questionnaires</span></span>
<span data-ttu-id="fab5d-184">在您设计并分配某一调查表后，该调查表可由所选调查对象完成。</span><span class="sxs-lookup"><span data-stu-id="fab5d-184">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="fab5d-185">您可以从以下两个位置完成可供您使用的调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-185">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="fab5d-186">在导航窗格中，单击**调查表** &gt; **分配** &gt; **填写调查表**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-186">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="fab5d-187">在员工自助服务中，单击**要完成的调查表**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-187">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="fab5d-188">调查表可用于网络中的所有人士，或者可用于特定的用户组或所有用户。</span><span class="sxs-lookup"><span data-stu-id="fab5d-188">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="fab5d-189">请参阅</span><span class="sxs-lookup"><span data-stu-id="fab5d-189">See also</span></span>
--------

[<span data-ttu-id="fab5d-190">设计调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-190">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="fab5d-191">使用调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-191">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="fab5d-192">查看和评估调查表的结果</span><span class="sxs-lookup"><span data-stu-id="fab5d-192">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



<a name=""></a>=======
---
# <a name="required-metadata"></a><span data-ttu-id="fab5d-193">必需元数据</span><span class="sxs-lookup"><span data-stu-id="fab5d-193">required metadata</span></span>

<span data-ttu-id="fab5d-194">标题: 分配和完成调查表描述: 本主题描述如何分配你设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-194">title: Distribute and complete a questionnaire description: This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> <span data-ttu-id="fab5d-195">作者: twheeloc 管理员: AnnBe ms.date: 06/20/2017 ms.topic: 文章 ms.prod: ms.service: Dynamics365Operations ms.technology:</span><span class="sxs-lookup"><span data-stu-id="fab5d-195">author: twheeloc manager: AnnBe ms.date: 06/20/2017 ms.topic: article ms.prod: ms.service: Dynamics365Operations ms.technology:</span></span> 

# <a name="optional-metadata"></a><span data-ttu-id="fab5d-196">可选元数据</span><span class="sxs-lookup"><span data-stu-id="fab5d-196">optional metadata</span></span>

<span data-ttu-id="fab5d-197">ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters</span><span class="sxs-lookup"><span data-stu-id="fab5d-197">ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters</span></span>
# <a name="robots"></a><span data-ttu-id="fab5d-198">ROBOTS:</span><span class="sxs-lookup"><span data-stu-id="fab5d-198">ROBOTS:</span></span> 
<span data-ttu-id="fab5d-199">受众: 应用程序用户</span><span class="sxs-lookup"><span data-stu-id="fab5d-199">audience: Application User</span></span>
# <a name="msdevlang"></a><span data-ttu-id="fab5d-200">ms.devlang:</span><span class="sxs-lookup"><span data-stu-id="fab5d-200">ms.devlang:</span></span> 
<span data-ttu-id="fab5d-201">ms.reviewer: twheeloc ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations</span><span class="sxs-lookup"><span data-stu-id="fab5d-201">ms.reviewer: twheeloc ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations</span></span>
# <a name="mstgtpltfrm"></a><span data-ttu-id="fab5d-202">ms.tgt_pltfrm:</span><span class="sxs-lookup"><span data-stu-id="fab5d-202">ms.tgt_pltfrm:</span></span> 
<span data-ttu-id="fab5d-203">ms.custom: 17424 ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470 ms.search.region: 全局</span><span class="sxs-lookup"><span data-stu-id="fab5d-203">ms.custom: 17424 ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470 ms.search.region: Global</span></span>
# <a name="mssearchindustry"></a><span data-ttu-id="fab5d-204">ms.search.industry:</span><span class="sxs-lookup"><span data-stu-id="fab5d-204">ms.search.industry:</span></span> 
<span data-ttu-id="fab5d-205">ms.author: twheeloc ms.search.validFrom: 2016-02-28 ms.dyn365.ops.version: AX 7.0.0, Talent 2017 年 7 月更新</span><span class="sxs-lookup"><span data-stu-id="fab5d-205">ms.author: twheeloc ms.search.validFrom: 2016-02-28 ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update</span></span>

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="fab5d-206">分配和完成调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-206">Distribute and complete a questionnaire</span></span>

<span data-ttu-id="fab5d-207">本主题描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-207">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="fab5d-208">有多种方式来分配调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-208">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="fab5d-209">将调查表标记为有效。</span><span class="sxs-lookup"><span data-stu-id="fab5d-209">Mark the questionnaire as active.</span></span> <span data-ttu-id="fab5d-210">然后，调查表可用于所有员工，除非设置调查表组来限制对它的访问。</span><span class="sxs-lookup"><span data-stu-id="fab5d-210">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="fab5d-211">向调查表组分配权限。</span><span class="sxs-lookup"><span data-stu-id="fab5d-211">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="fab5d-212">然后，调查表可供所选组的所有成员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-212">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="fab5d-213">创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-213">Create planned answer sessions.</span></span> <span data-ttu-id="fab5d-214">然后，调查表只可供特定人员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-214">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="fab5d-215">创建计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-215">Create a schedule.</span></span> <span data-ttu-id="fab5d-216">然后，调查表中可供多个人员使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-216">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="fab5d-217">将调查表标记为有效</span><span class="sxs-lookup"><span data-stu-id="fab5d-217">Marking a questionnaire as active</span></span>
<span data-ttu-id="fab5d-218">通过在**调查表**页上将**有效**字段设置为**是**，您使调查表可供所有员工使用并完成。</span><span class="sxs-lookup"><span data-stu-id="fab5d-218">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="fab5d-219">调查对象可以多次完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-219">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="fab5d-220">如果您要全年收集连续反馈，则此功能十分有用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-220">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="fab5d-221">例如，您可以让员工使用调查表来提供有关在自助服务餐厅享用午餐服务的反馈。</span><span class="sxs-lookup"><span data-stu-id="fab5d-221">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="fab5d-222">调查表组</span><span class="sxs-lookup"><span data-stu-id="fab5d-222">Questionnaire groups</span></span>
<span data-ttu-id="fab5d-223">您可以设置调查表组，然后包括调查表应分配到的调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-223">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="fab5d-224">可以从以下页面创建调查表组：</span><span class="sxs-lookup"><span data-stu-id="fab5d-224">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="fab5d-225">**调查表组**– 只有调查表组中的个人可以完成选定的调查表组。</span><span class="sxs-lookup"><span data-stu-id="fab5d-225">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="fab5d-226">例如，您的预期受众是承包商，因此您可以创建特定于这些调查对象的调查表组。</span><span class="sxs-lookup"><span data-stu-id="fab5d-226">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="fab5d-227">**调查表组成员** – 您可以向调查表组添加人员。</span><span class="sxs-lookup"><span data-stu-id="fab5d-227">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="fab5d-228">若要将调查表组分配给某一调查表，请在**调查表**页上，单击**用户权限**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-228">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="fab5d-229">在调查表保存为有效后，调查表组的成员可以完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-229">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="fab5d-230">如果您想要先对一组特定的人员测试某一调查表，然后再将其展开到一个更大的组，或者，如果您想要使调查表面向非常具体的受众，则此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-230">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="fab5d-231">调查表中的计划应答期</span><span class="sxs-lookup"><span data-stu-id="fab5d-231">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="fab5d-232">计划应答期是您设计并选择调查对象的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-232">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

<span data-ttu-id="fab5d-233">**注释：**在您可以设置计划应答期之前，必须设计调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-233">**Note:** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="fab5d-234">在**“计划应答期”**页上，您可为单独的员工创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-234">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="fab5d-235">该页面上的列表显示所有已编制的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-235">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="fab5d-236">计划应答期还用于**“调查表计划”**页上，在那里您可以为多人计划调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-236">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="fab5d-237">员工</span><span class="sxs-lookup"><span data-stu-id="fab5d-237">Employees</span></span>
-   <span data-ttu-id="fab5d-238">课程参与者</span><span class="sxs-lookup"><span data-stu-id="fab5d-238">Course participants</span></span>
-   <span data-ttu-id="fab5d-239">组织单位</span><span class="sxs-lookup"><span data-stu-id="fab5d-239">Organizational units</span></span>

<span data-ttu-id="fab5d-240">每个人只能回答调查表一次。</span><span class="sxs-lookup"><span data-stu-id="fab5d-240">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="fab5d-241">计划调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-241">Scheduling a questionnaire</span></span>
<span data-ttu-id="fab5d-242">（可选）您可以为多个调查对象计划调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-242">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="fab5d-243">计划类型</span><span class="sxs-lookup"><span data-stu-id="fab5d-243">Planning types</span></span>

<span data-ttu-id="fab5d-244">如果您想要为多个调查对象安排计划的回答会话，则需要计划类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-244">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="fab5d-245">计划类型用于对调查表计划分类。</span><span class="sxs-lookup"><span data-stu-id="fab5d-245">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="fab5d-246">例如，您可能会出于以下目的计划调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-246">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="fab5d-247">评估</span><span class="sxs-lookup"><span data-stu-id="fab5d-247">Evaluation</span></span>
-   <span data-ttu-id="fab5d-248">调查</span><span class="sxs-lookup"><span data-stu-id="fab5d-248">Survey</span></span>
-   <span data-ttu-id="fab5d-249">正在测试</span><span class="sxs-lookup"><span data-stu-id="fab5d-249">Testing</span></span>

<span data-ttu-id="fab5d-250">您可以在**“调查表计划”**页上为调查表计划指定计划类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-250">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="fab5d-251">调查表的参考类型</span><span class="sxs-lookup"><span data-stu-id="fab5d-251">Reference types for questionnaire</span></span>

<span data-ttu-id="fab5d-252">您可以使用参考类型输入您可以在计划调查表时选择的回应者的条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-252">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="fab5d-253">使用**“参考类型”**页可以设置调查表的参考类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-253">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="fab5d-254">每个参考类型对应于 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本中的某个表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-254">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span></span> <span data-ttu-id="fab5d-255">在您创建调查表计划时，可以指定表中记录或指定调查表将关联的一系列记录。</span><span class="sxs-lookup"><span data-stu-id="fab5d-255">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="fab5d-256">例如，如果您选择“课程”表，您可以确定调查表将针对哪一个特定课程。</span><span class="sxs-lookup"><span data-stu-id="fab5d-256">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="fab5d-257">在您为“课程”表设置参考时，**“课程”**页上的某些字段和按钮将可用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-257">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="fab5d-258">调查表计划</span><span class="sxs-lookup"><span data-stu-id="fab5d-258">Questionnaire schedules</span></span>

<span data-ttu-id="fab5d-259">您可以使用调查表计划基于参考类型为一组用户生成多个计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-259">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="fab5d-260">在**调查表计划**页上创建计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-260">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="fab5d-261">选择计划类型对计划进行分类，并且选择应用于在系统中查询特定用户的参考类型。</span><span class="sxs-lookup"><span data-stu-id="fab5d-261">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="fab5d-262">例如，如果您将参考类型设置为“课程”表，则您可以在**参考**字段中选择特定课程。</span><span class="sxs-lookup"><span data-stu-id="fab5d-262">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="fab5d-263">单击**“设置详细信息”**可以选择调查表和其他条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-263">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="fab5d-264">例如，如果调查表是对教师的评估，则指定教师的名称作为条件。</span><span class="sxs-lookup"><span data-stu-id="fab5d-264">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="fab5d-265">在您完成输入设置详细信息后，系统将为查询中包括的用户生成计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-265">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="fab5d-266">单击**“计划应答期”**可以查看计划的应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-266">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="fab5d-267">然后，您可以手动创建附加计划应答期或删除尚未回答的计划应答期。</span><span class="sxs-lookup"><span data-stu-id="fab5d-267">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="fab5d-268">单击**功能** &gt; **开始**可以使计划调查表在相关计划应答期中可供用户使用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-268">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="fab5d-269">单击**“回答”**可以查看该调查表的已完成响应。</span><span class="sxs-lookup"><span data-stu-id="fab5d-269">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="fab5d-270">（可选）您可以复制调查表计划设置、计划应答期和对新计划调查表的回答。</span><span class="sxs-lookup"><span data-stu-id="fab5d-270">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="fab5d-271">告知调查对象调查表对其可用</span><span class="sxs-lookup"><span data-stu-id="fab5d-271">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="fab5d-272">在分发调查表时，您必须通知调查对象调查表对其可用。</span><span class="sxs-lookup"><span data-stu-id="fab5d-272">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

<span data-ttu-id="fab5d-273">**注意：**调查对象必须是 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本中的用户，才能完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-273">**Note:** Respondents must be users in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition to complete a questionnaire.</span></span>

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="fab5d-274">向调查对象通知计划应答期</span><span class="sxs-lookup"><span data-stu-id="fab5d-274">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="fab5d-275">如果您使用计划应答期，您必须直接通知人员，例如通过电话或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fab5d-275">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="fab5d-276">向调查对象通知相关计划</span><span class="sxs-lookup"><span data-stu-id="fab5d-276">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="fab5d-277">使用“**调查表计划**”页可以准备电子邮件并将其发送给分配有调查表的调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-277">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="fab5d-278">在**“员工自助服务的电子邮件”**选项卡上输入电子邮件文本。</span><span class="sxs-lookup"><span data-stu-id="fab5d-278">Enter the email text on the **E-mail for employee self service** tab.</span></span> <span data-ttu-id="fab5d-279">在计划开始后，单击**功能** &gt; **发送电子邮件**以生成电子邮件并将其发送给调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-279">After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="fab5d-280">然后调查对象可以登录到该网站并完成调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-280">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

<span data-ttu-id="fab5d-281">**注释：**在您可以使用电子邮件功能之前，您的 IT 管理员必须在**“电子邮件参数”**页上输入电子邮件设置。</span><span class="sxs-lookup"><span data-stu-id="fab5d-281">**Note:** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="fab5d-282">结束预定的调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-282">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="fab5d-283">您可以在所有回应者都已完成他们的分配的应答期后，结束计划的调查表。</span><span class="sxs-lookup"><span data-stu-id="fab5d-283">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="fab5d-284">在结束后某一计划的调查表，您不能将其设置为新计划编制。</span><span class="sxs-lookup"><span data-stu-id="fab5d-284">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

<span data-ttu-id="fab5d-285">**注释：**如果一个或多个调查对象尚未完成调查表并且您仍要结束计划编制，则首先在“**计划应答期**”页上的列表中删除这些调查对象。</span><span class="sxs-lookup"><span data-stu-id="fab5d-285">**Note:** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="fab5d-286">然后，即可结束计划。</span><span class="sxs-lookup"><span data-stu-id="fab5d-286">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="fab5d-287">填写调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-287">Completing questionnaires</span></span>
<span data-ttu-id="fab5d-288">在您设计并分配某一调查表后，该调查表可由所选调查对象完成。</span><span class="sxs-lookup"><span data-stu-id="fab5d-288">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="fab5d-289">您可以从以下两个位置完成可供您使用的调查表：</span><span class="sxs-lookup"><span data-stu-id="fab5d-289">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="fab5d-290">在导航窗格中，单击**调查表** &gt; **分配** &gt; **填写调查表**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-290">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="fab5d-291">在员工自助服务中，单击**要完成的调查表**。</span><span class="sxs-lookup"><span data-stu-id="fab5d-291">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="fab5d-292">调查表可用于网络中的所有人士，或者可用于特定的用户组或所有用户。</span><span class="sxs-lookup"><span data-stu-id="fab5d-292">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="fab5d-293">请参阅</span><span class="sxs-lookup"><span data-stu-id="fab5d-293">See also</span></span>
--------

[<span data-ttu-id="fab5d-294">设计调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-294">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="fab5d-295">使用调查表</span><span class="sxs-lookup"><span data-stu-id="fab5d-295">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="fab5d-296">查看和评估调查表的结果</span><span class="sxs-lookup"><span data-stu-id="fab5d-296">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)

<span data-ttu-id="fab5d-297">母版</span><span class="sxs-lookup"><span data-stu-id="fab5d-297">master</span></span>

