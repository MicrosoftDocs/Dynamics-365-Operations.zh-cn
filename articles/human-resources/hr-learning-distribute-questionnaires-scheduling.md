---
title: 使用计划分发调查表
description: 调查表编制计划允许您将调查表分发给多个回应者。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d233938fe553dbd7da7fcc5477097fd885665102
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417520"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="2a017-103">使用计划分发调查表</span><span class="sxs-lookup"><span data-stu-id="2a017-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="2a017-104">调查表编制计划允许您将调查表分发给多个回应者。</span><span class="sxs-lookup"><span data-stu-id="2a017-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="2a017-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="2a017-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="2a017-106">创建调查表计划</span><span class="sxs-lookup"><span data-stu-id="2a017-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="2a017-107">转到“调查表”>“分配”>“调查表计划”。</span><span class="sxs-lookup"><span data-stu-id="2a017-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="2a017-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2a017-108">Click New.</span></span>

3. <span data-ttu-id="2a017-109">在“计划”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2a017-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="2a017-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2a017-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2a017-111">如果响应应记录，而无需关联的名称，则将计划设置为“匿名”。</span><span class="sxs-lookup"><span data-stu-id="2a017-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="2a017-112">必须首先在“HR 参数”中设置允许匿名结果。</span><span class="sxs-lookup"><span data-stu-id="2a017-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="2a017-113">在“类型”字段中，选择计划类型。</span><span class="sxs-lookup"><span data-stu-id="2a017-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="2a017-114">在此示例中，我们将使用满意度类型。</span><span class="sxs-lookup"><span data-stu-id="2a017-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="2a017-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2a017-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="2a017-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2a017-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="2a017-117">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="2a017-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="2a017-118">展开“员工自助服务的电子邮件”部分。</span><span class="sxs-lookup"><span data-stu-id="2a017-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="2a017-119">在“主题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2a017-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="2a017-120">示例：可用的调查表</span><span class="sxs-lookup"><span data-stu-id="2a017-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="2a017-121">在“文本”字段中，键入电子邮件的正文。</span><span class="sxs-lookup"><span data-stu-id="2a017-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="2a017-122">请注意，此变量可用于替换系统中的值。</span><span class="sxs-lookup"><span data-stu-id="2a017-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="2a017-123">示例：尊敬的 %P%，请登录“员工自助服务”填写《员工健康》调查表。</span><span class="sxs-lookup"><span data-stu-id="2a017-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="2a017-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="2a017-124">Contoso</span></span>  

12. <span data-ttu-id="2a017-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2a017-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="2a017-126">使用设置详细信息选择要回答的调查表，以及用于选择回应者的任何查询。</span><span class="sxs-lookup"><span data-stu-id="2a017-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="2a017-127">单击“设置详细信息”。</span><span class="sxs-lookup"><span data-stu-id="2a017-127">Click Setup details.</span></span>

2. <span data-ttu-id="2a017-128">在列表中，选择用于搜索系统以查找调查表回应者的查询。</span><span class="sxs-lookup"><span data-stu-id="2a017-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="2a017-129">示例：工作人员</span><span class="sxs-lookup"><span data-stu-id="2a017-129">Example: Workers</span></span>  

3. <span data-ttu-id="2a017-130">单击“查看”或修改查询来选择特定人员或调整查询来查找满足特定条件的人员。</span><span class="sxs-lookup"><span data-stu-id="2a017-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="2a017-131">请注意，所有回应者还必须是系统中的用户。</span><span class="sxs-lookup"><span data-stu-id="2a017-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="2a017-132">在列表中，标记“人员”的行</span><span class="sxs-lookup"><span data-stu-id="2a017-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="2a017-133">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2a017-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="2a017-134">选择“Julia Funderburk”</span><span class="sxs-lookup"><span data-stu-id="2a017-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="2a017-135">在列表中，选择“Julia Funderburk”</span><span class="sxs-lookup"><span data-stu-id="2a017-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="2a017-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2a017-136">Click OK.</span></span>

8. <span data-ttu-id="2a017-137">单击“调查表”选项卡。</span><span class="sxs-lookup"><span data-stu-id="2a017-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="2a017-138">在树中，展开类型为“满意度调查”的调查表的节点。</span><span class="sxs-lookup"><span data-stu-id="2a017-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="2a017-139">在树中，选中“员工健康评估”。</span><span class="sxs-lookup"><span data-stu-id="2a017-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="2a017-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2a017-140">Click OK.</span></span>

12. <span data-ttu-id="2a017-141">单击“计划应答期”。</span><span class="sxs-lookup"><span data-stu-id="2a017-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="2a017-142">请注意，计划应答期已为每个所选/查询用户创建。</span><span class="sxs-lookup"><span data-stu-id="2a017-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="2a017-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2a017-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="2a017-144">开始调查表计划以使调查表可供回应者完成。</span><span class="sxs-lookup"><span data-stu-id="2a017-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="2a017-145">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2a017-145">Click Functions.</span></span>

2. <span data-ttu-id="2a017-146">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="2a017-146">Click Start.</span></span>

3. <span data-ttu-id="2a017-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2a017-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="2a017-148">发送电子邮件通知可用调查表的回应者。</span><span class="sxs-lookup"><span data-stu-id="2a017-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="2a017-149">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2a017-149">Click Functions.</span></span>

2. <span data-ttu-id="2a017-150">单击“发送电子邮件”。</span><span class="sxs-lookup"><span data-stu-id="2a017-150">Click Send email.</span></span>

3. <span data-ttu-id="2a017-151">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="2a017-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="2a017-152">使用“计划应答期”监控谁需要完成调查表。</span><span class="sxs-lookup"><span data-stu-id="2a017-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="2a017-153">单击“计划应答期”。</span><span class="sxs-lookup"><span data-stu-id="2a017-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="2a017-154">在您可以结束计划会话时，删除所有其余计划应答期。</span><span class="sxs-lookup"><span data-stu-id="2a017-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="2a017-155">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="2a017-155">Click Delete.</span></span>

3. <span data-ttu-id="2a017-156">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="2a017-156">Click Yes.</span></span>

4. <span data-ttu-id="2a017-157">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2a017-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="2a017-158">当所有回应者均已完成调查表且/或已删除其余所有计划应答期时结束计划。</span><span class="sxs-lookup"><span data-stu-id="2a017-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="2a017-159">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2a017-159">Click Functions.</span></span>
2. <span data-ttu-id="2a017-160">单击“结束”。</span><span class="sxs-lookup"><span data-stu-id="2a017-160">Click End.</span></span>
3. <span data-ttu-id="2a017-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2a017-161">Click OK.</span></span>

