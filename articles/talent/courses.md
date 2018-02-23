---
title: "设置培训课程"
description: "人力资源管理员和经理可以使用课程功能维护有关为工作人员提供的培训的信息。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 27fbc54afca384b804f2b0468206242ff89d4031
ms.contentlocale: zh-cn
ms.lasthandoff: 02/23/2018

---

# <a name="set-up-training-courses"></a><span data-ttu-id="40ea2-103">设置培训课程</span><span class="sxs-lookup"><span data-stu-id="40ea2-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="40ea2-104">人力资源管理员和经理可以使用课程功能维护有关为工作人员提供的培训的信息。</span><span class="sxs-lookup"><span data-stu-id="40ea2-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="40ea2-105"> 设置先决条件</span><span class="sxs-lookup"><span data-stu-id="40ea2-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="40ea2-106">以下信息是必需的，而且必须在创建课程之前设置。</span><span class="sxs-lookup"><span data-stu-id="40ea2-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="40ea2-107">**课程类型**</span><span class="sxs-lookup"><span data-stu-id="40ea2-107">**Course types**</span></span>

<span data-ttu-id="40ea2-108">以下信息是可以为课程指定的可选信息。</span><span class="sxs-lookup"><span data-stu-id="40ea2-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="40ea2-109">如果您知道您将为课程输入此信息，则应在创建课程记录之前设置此信息。</span><span class="sxs-lookup"><span data-stu-id="40ea2-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="40ea2-110">**教室组**</span><span class="sxs-lookup"><span data-stu-id="40ea2-110">**Classroom groups**</span></span>
-   <span data-ttu-id="40ea2-111">**课程组**</span><span class="sxs-lookup"><span data-stu-id="40ea2-111">**Course groups**</span></span>
-   <span data-ttu-id="40ea2-112">**上课地点**</span><span class="sxs-lookup"><span data-stu-id="40ea2-112">**Course locations**</span></span>
-   <span data-ttu-id="40ea2-113">**教室**</span><span class="sxs-lookup"><span data-stu-id="40ea2-113">**Classrooms**</span></span>
-   <span data-ttu-id="40ea2-114">**教师**</span><span class="sxs-lookup"><span data-stu-id="40ea2-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="40ea2-115">课程类型</span><span class="sxs-lookup"><span data-stu-id="40ea2-115">Course types</span></span>
<span data-ttu-id="40ea2-116">您可以使用课程类型根据课程结构或内容对课程进行分类。</span><span class="sxs-lookup"><span data-stu-id="40ea2-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="40ea2-117">您可以在**“课程类型”**页上创建课程类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="40ea2-118">创建课程记录时，必须选择课程类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="40ea2-119">课程设置类型</span><span class="sxs-lookup"><span data-stu-id="40ea2-119">Course setup type</span></span>
<span data-ttu-id="40ea2-120">下表列出了课程的三种设置类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="40ea2-121">设置类型确定课程结构。</span><span class="sxs-lookup"><span data-stu-id="40ea2-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="40ea2-122">设置类型</span><span class="sxs-lookup"><span data-stu-id="40ea2-122">Setup type</span></span></th>
<th><span data-ttu-id="40ea2-123">描述</span><span class="sxs-lookup"><span data-stu-id="40ea2-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40ea2-124"><strong>标准</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="40ea2-125">为没有日程安排的课程选择此类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="40ea2-126">新建课程时，这是默认设置类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40ea2-127"><strong>课程安排</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="40ea2-128">选择此类型以规划多天课程的每一天的详细信息。</span><span class="sxs-lookup"><span data-stu-id="40ea2-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40ea2-129"><strong>课程安排 + 会话</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="40ea2-130">为更复杂的课程选择此类型。</span><span class="sxs-lookup"><span data-stu-id="40ea2-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="40ea2-131">例如，您可以将课程日程分为轨道和会话。</span><span class="sxs-lookup"><span data-stu-id="40ea2-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="40ea2-132"><strong>“班组”</strong>– 班组是课程特定的主题区域。</span><span class="sxs-lookup"><span data-stu-id="40ea2-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="40ea2-133"><strong>“学期”</strong>– 学期将班组划分开来，并且帮助确定与轨道相关的特定流程或技巧。</span><span class="sxs-lookup"><span data-stu-id="40ea2-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="40ea2-134">课程任务</span><span class="sxs-lookup"><span data-stu-id="40ea2-134">Course tasks</span></span>
<span data-ttu-id="40ea2-135">对于每个课程，都可以完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="40ea2-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="40ea2-136">登记参与者</span><span class="sxs-lookup"><span data-stu-id="40ea2-136">Register participants</span></span>
-   <span data-ttu-id="40ea2-137">指定登记截止日期</span><span class="sxs-lookup"><span data-stu-id="40ea2-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="40ea2-138">定义参与者的最小和最大数目</span><span class="sxs-lookup"><span data-stu-id="40ea2-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="40ea2-139">分配课程所在的地点和教室</span><span class="sxs-lookup"><span data-stu-id="40ea2-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="40ea2-140">为课程参与者推荐旅馆</span><span class="sxs-lookup"><span data-stu-id="40ea2-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="40ea2-141">创建课程描述，然后您可以在员工自助服务上进行建议</span><span class="sxs-lookup"><span data-stu-id="40ea2-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="40ea2-142">**注意** 只有当没有人登记课程时，您才可以删除它。</span><span class="sxs-lookup"><span data-stu-id="40ea2-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="40ea2-143">课程状态</span><span class="sxs-lookup"><span data-stu-id="40ea2-143">Course statuses</span></span>
<span data-ttu-id="40ea2-144">下表列出了可能的课程状态，以及在课程具有特定状态时您可以完成的操作。</span><span class="sxs-lookup"><span data-stu-id="40ea2-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="40ea2-145">状态</span><span class="sxs-lookup"><span data-stu-id="40ea2-145">Status</span></span></th>
<th><span data-ttu-id="40ea2-146">行为</span><span class="sxs-lookup"><span data-stu-id="40ea2-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40ea2-147"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="40ea2-148">输入并修改课程信息。</span><span class="sxs-lookup"><span data-stu-id="40ea2-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="40ea2-149">将课程状态更改为<strong>“打开”</strong>，这样工作人员可以登记该课程。</span><span class="sxs-lookup"><span data-stu-id="40ea2-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40ea2-150"><strong>打开</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="40ea2-151">为课程登记参与者。</span><span class="sxs-lookup"><span data-stu-id="40ea2-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="40ea2-152">将参与者从课程中移除。</span><span class="sxs-lookup"><span data-stu-id="40ea2-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="40ea2-153">确认课程的参与者。</span><span class="sxs-lookup"><span data-stu-id="40ea2-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="40ea2-154">将课程状态更改为<strong>“已关闭”</strong>或<strong>“已取消”</strong>。</span><span class="sxs-lookup"><span data-stu-id="40ea2-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="40ea2-155">为状态为<strong>“已确认”</strong>的参与者规划调查表。</span><span class="sxs-lookup"><span data-stu-id="40ea2-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40ea2-156"><strong>已关闭</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="40ea2-157">可以重新打开课程。</span><span class="sxs-lookup"><span data-stu-id="40ea2-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40ea2-158"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="40ea2-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="40ea2-159">可以重新打开课程。</span><span class="sxs-lookup"><span data-stu-id="40ea2-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="40ea2-160">课程参与者</span><span class="sxs-lookup"><span data-stu-id="40ea2-160">Course participants</span></span>
<span data-ttu-id="40ea2-161">课程参与者有工作人员、申请者或参加培训课程或事件的承包商。</span><span class="sxs-lookup"><span data-stu-id="40ea2-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="40ea2-162">仅可为开放式课程登记参与者。</span><span class="sxs-lookup"><span data-stu-id="40ea2-162">You can only register participants for open courses.</span></span> <span data-ttu-id="40ea2-163">可以为课程登记的参与者最大和最小人数在**“课程”**页上的**“常规”**快速选项卡中进行了定义。</span><span class="sxs-lookup"><span data-stu-id="40ea2-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="40ea2-164">工作流</span><span class="sxs-lookup"><span data-stu-id="40ea2-164">Workflow</span></span>
--------

<span data-ttu-id="40ea2-165">通过**工自助服务**页登记课程的员工可以让其注册工作流传送以供审核。</span><span class="sxs-lookup"><span data-stu-id="40ea2-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="40ea2-166">工作流可以分配到**课程**页上的**常规**快速选项卡中的课程。</span><span class="sxs-lookup"><span data-stu-id="40ea2-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






