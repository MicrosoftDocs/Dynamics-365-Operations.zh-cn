---
title: 分发和计划调查表
description: 本文描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5372841c841e82d116381d7ce8fe48af8ddfb036
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008209"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="920f9-103">分发和计划调查表</span><span class="sxs-lookup"><span data-stu-id="920f9-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="920f9-104">本文描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。</span><span class="sxs-lookup"><span data-stu-id="920f9-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="920f9-105">有多种方式来分配调查表：</span><span class="sxs-lookup"><span data-stu-id="920f9-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="920f9-106">将调查表标记为有效。</span><span class="sxs-lookup"><span data-stu-id="920f9-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="920f9-107">然后，调查表可用于所有员工，除非设置调查表组来限制对它的访问。</span><span class="sxs-lookup"><span data-stu-id="920f9-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="920f9-108">向调查表组分配权限。</span><span class="sxs-lookup"><span data-stu-id="920f9-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="920f9-109">然后，调查表可供所选组的所有成员使用。</span><span class="sxs-lookup"><span data-stu-id="920f9-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="920f9-110">创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-110">Create planned answer sessions.</span></span> <span data-ttu-id="920f9-111">然后，调查表只可供特定人员使用。</span><span class="sxs-lookup"><span data-stu-id="920f9-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="920f9-112">创建计划。</span><span class="sxs-lookup"><span data-stu-id="920f9-112">Create a schedule.</span></span> <span data-ttu-id="920f9-113">然后，调查表中可供多个人员使用。</span><span class="sxs-lookup"><span data-stu-id="920f9-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="920f9-114">将调查表标记为有效</span><span class="sxs-lookup"><span data-stu-id="920f9-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="920f9-115">通过在**调查表**页上将**有效**字段设置为**是**，您使调查表可供所有员工使用并完成。</span><span class="sxs-lookup"><span data-stu-id="920f9-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="920f9-116">调查对象可以多次完成调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="920f9-117">如果您要全年收集连续反馈，则此功能十分有用。</span><span class="sxs-lookup"><span data-stu-id="920f9-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="920f9-118">例如，您可以让员工使用调查表来提供有关在自助服务餐厅享用午餐服务的反馈。</span><span class="sxs-lookup"><span data-stu-id="920f9-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="920f9-119">调查表组</span><span class="sxs-lookup"><span data-stu-id="920f9-119">Questionnaire groups</span></span>

<span data-ttu-id="920f9-120">您可以设置调查表组，然后包括调查表应分配到的调查对象。</span><span class="sxs-lookup"><span data-stu-id="920f9-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="920f9-121">可以从以下页面创建调查表组：</span><span class="sxs-lookup"><span data-stu-id="920f9-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="920f9-122">**调查表组**– 只有调查表组中的个人可以完成选定的调查表组。</span><span class="sxs-lookup"><span data-stu-id="920f9-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="920f9-123">例如，您的预期受众是承包商，因此您可以创建特定于这些调查对象的调查表组。</span><span class="sxs-lookup"><span data-stu-id="920f9-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="920f9-124">**调查表组成员** – 您可以向调查表组添加人员。</span><span class="sxs-lookup"><span data-stu-id="920f9-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="920f9-125">若要将调查表组分配给某一调查表，请在**调查表**页上，单击**用户权限**。</span><span class="sxs-lookup"><span data-stu-id="920f9-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="920f9-126">在调查表保存为有效后，调查表组的成员可以完成调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="920f9-127">如果您想要先对一组特定的人员测试某一调查表，然后再将其展开到一个更大的组，或者，如果您想要使调查表面向非常具体的受众，则此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="920f9-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="920f9-128">调查表中的计划应答期</span><span class="sxs-lookup"><span data-stu-id="920f9-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="920f9-129">计划应答期是您设计并选择调查对象的调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="920f9-130">在您可以设置计划应答期之前，必须设计调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="920f9-131">在**计划应答期**页上，您可为单独的员工创建计划应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="920f9-132">该页面上的列表显示所有已编制的调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="920f9-133">计划应答期还用于**调查表计划**页上，在那里您可以为多人计划调查表：</span><span class="sxs-lookup"><span data-stu-id="920f9-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="920f9-134">员工</span><span class="sxs-lookup"><span data-stu-id="920f9-134">Employees</span></span>
-   <span data-ttu-id="920f9-135">课程参与者</span><span class="sxs-lookup"><span data-stu-id="920f9-135">Course participants</span></span>
-   <span data-ttu-id="920f9-136">组织单位</span><span class="sxs-lookup"><span data-stu-id="920f9-136">Organizational units</span></span>

<span data-ttu-id="920f9-137">每个人只能回答调查表一次。</span><span class="sxs-lookup"><span data-stu-id="920f9-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="920f9-138">计划调查表</span><span class="sxs-lookup"><span data-stu-id="920f9-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="920f9-139">（可选）您可以为多个调查对象计划调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="920f9-140">计划类型</span><span class="sxs-lookup"><span data-stu-id="920f9-140">Planning types</span></span>

<span data-ttu-id="920f9-141">如果您想要为多个调查对象安排计划的回答会话，则需要计划类型。</span><span class="sxs-lookup"><span data-stu-id="920f9-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="920f9-142">计划类型用于对调查表计划分类。</span><span class="sxs-lookup"><span data-stu-id="920f9-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="920f9-143">例如，您可能会出于以下目的计划调查表：</span><span class="sxs-lookup"><span data-stu-id="920f9-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="920f9-144">评估</span><span class="sxs-lookup"><span data-stu-id="920f9-144">Evaluation</span></span>
-   <span data-ttu-id="920f9-145">调查</span><span class="sxs-lookup"><span data-stu-id="920f9-145">Survey</span></span>
-   <span data-ttu-id="920f9-146">正在测试</span><span class="sxs-lookup"><span data-stu-id="920f9-146">Testing</span></span>

<span data-ttu-id="920f9-147">您可以在**调查表计划**页上为调查表计划指定计划类型。</span><span class="sxs-lookup"><span data-stu-id="920f9-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="920f9-148">调查表的参考类型</span><span class="sxs-lookup"><span data-stu-id="920f9-148">Reference types for questionnaire</span></span>

<span data-ttu-id="920f9-149">您可以使用参考类型输入您可以在计划调查表时选择的回应者的条件。</span><span class="sxs-lookup"><span data-stu-id="920f9-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="920f9-150">使用**参考类型**页可以设置调查表的参考类型。</span><span class="sxs-lookup"><span data-stu-id="920f9-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="920f9-151">每个参考类型对应于 Microsoft Dynamics 365 Finance 中的某个表。</span><span class="sxs-lookup"><span data-stu-id="920f9-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="920f9-152">在您创建调查表计划时，可以指定表中记录或指定调查表将关联的一系列记录。</span><span class="sxs-lookup"><span data-stu-id="920f9-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="920f9-153">例如，如果您选择“课程”表，您可以确定调查表将针对哪一个特定课程。</span><span class="sxs-lookup"><span data-stu-id="920f9-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="920f9-154">在您为“课程”表设置参考时，**课程**页上的某些字段和按钮将可用。</span><span class="sxs-lookup"><span data-stu-id="920f9-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="920f9-155">调查表计划</span><span class="sxs-lookup"><span data-stu-id="920f9-155">Questionnaire schedules</span></span>

<span data-ttu-id="920f9-156">您可以使用调查表计划基于参考类型为一组用户生成多个计划应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="920f9-157">在**调查表计划**页上创建计划。</span><span class="sxs-lookup"><span data-stu-id="920f9-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="920f9-158">选择计划类型对计划进行分类，并且选择应用于在系统中查询特定用户的参考类型。</span><span class="sxs-lookup"><span data-stu-id="920f9-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="920f9-159">例如，如果您将参考类型设置为“课程”表，则您可以在**参考**字段中选择特定课程。</span><span class="sxs-lookup"><span data-stu-id="920f9-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="920f9-160">单击**设置详细信息**可以选择调查表和其他条件。</span><span class="sxs-lookup"><span data-stu-id="920f9-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="920f9-161">例如，如果调查表是对教师的评估，则指定教师的名称作为条件。</span><span class="sxs-lookup"><span data-stu-id="920f9-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="920f9-162">在您完成输入设置详细信息后，系统将为查询中包括的用户生成计划应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="920f9-163">单击**计划应答期**可以查看计划的应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="920f9-164">然后，您可以手动创建附加计划应答期或删除尚未回答的计划应答期。</span><span class="sxs-lookup"><span data-stu-id="920f9-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="920f9-165">单击**功能** &gt; **开始**可以使计划调查表在相关计划应答期中可供用户使用。</span><span class="sxs-lookup"><span data-stu-id="920f9-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="920f9-166">单击**回答**可以查看该调查表的已完成响应。</span><span class="sxs-lookup"><span data-stu-id="920f9-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="920f9-167">（可选）您可以复制调查表计划设置、计划应答期和对新计划调查表的回答。</span><span class="sxs-lookup"><span data-stu-id="920f9-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="920f9-168">告知调查对象调查表对其可用</span><span class="sxs-lookup"><span data-stu-id="920f9-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="920f9-169">在分发调查表时，您必须通知调查对象调查表对其可用。</span><span class="sxs-lookup"><span data-stu-id="920f9-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="920f9-170">向调查对象通知计划应答期</span><span class="sxs-lookup"><span data-stu-id="920f9-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="920f9-171">如果您使用计划应答期，您必须直接通知人员，例如通过电话或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="920f9-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="920f9-172">向调查对象通知相关计划</span><span class="sxs-lookup"><span data-stu-id="920f9-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="920f9-173">使用**调查表计划**页可以准备电子邮件并将其发送给分配有调查表的调查对象。</span><span class="sxs-lookup"><span data-stu-id="920f9-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="920f9-174">在**员工自助服务的电子邮件**选项卡上输入电子邮件文本。在计划开始后，单击**功能** &gt; **发送电子邮件**以生成电子邮件并将其发送给调查对象。</span><span class="sxs-lookup"><span data-stu-id="920f9-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="920f9-175">然后调查对象可以登录到该网站并完成调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="920f9-176">在您可以使用电子邮件功能之前，您的 IT 管理员必须在**电子邮件参数**页上输入电子邮件设置。</span><span class="sxs-lookup"><span data-stu-id="920f9-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="920f9-177">结束预定的调查表</span><span class="sxs-lookup"><span data-stu-id="920f9-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="920f9-178">您可以在所有回应者都已完成他们的分配的应答期后，结束计划的调查表。</span><span class="sxs-lookup"><span data-stu-id="920f9-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="920f9-179">在结束后某一计划的调查表，您不能将其设置为新计划编制。</span><span class="sxs-lookup"><span data-stu-id="920f9-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="920f9-180">如果一个或多个调查对象尚未完成调查表并且您仍要结束计划编制，则首先在**计划应答期**页上的列表中删除这些调查对象。</span><span class="sxs-lookup"><span data-stu-id="920f9-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="920f9-181">然后，即可结束计划。</span><span class="sxs-lookup"><span data-stu-id="920f9-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="920f9-182">填写调查表</span><span class="sxs-lookup"><span data-stu-id="920f9-182">Completing questionnaires</span></span>

<span data-ttu-id="920f9-183">在您设计并分配某一调查表后，该调查表可由所选调查对象完成。</span><span class="sxs-lookup"><span data-stu-id="920f9-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="920f9-184">您可以从以下两个位置完成可供您使用的调查表：</span><span class="sxs-lookup"><span data-stu-id="920f9-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="920f9-185">在导航窗格中，单击**调查表** &gt; **分配** &gt; **填写调查表**。</span><span class="sxs-lookup"><span data-stu-id="920f9-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="920f9-186">在员工自助服务中，单击**要完成的调查表**。</span><span class="sxs-lookup"><span data-stu-id="920f9-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="920f9-187">调查表可用于网络中的所有人士，或者可用于特定的用户组或所有用户。</span><span class="sxs-lookup"><span data-stu-id="920f9-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>


