---
title: 使用工作流管理员工信息
description: 本文说明如何使用人力资源的工作流功能管理员工信息。 例如，可以将工作流与职位关联，以及配置员工更改其记录时启动的批准工作流。
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058744"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="8cac6-104">使用工作流管理员工信息</span><span class="sxs-lookup"><span data-stu-id="8cac6-104">Use workflows to manage employee information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8cac6-105">本文说明如何使用人力资源的工作流功能管理员工信息。</span><span class="sxs-lookup"><span data-stu-id="8cac6-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="8cac6-106">例如，可以将工作流与职位关联，以及配置员工更改其记录时启动的批准工作流。</span><span class="sxs-lookup"><span data-stu-id="8cac6-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="8cac6-107">人力资源的工作流功能提供各种工作流，用于管理人力资源活动。</span><span class="sxs-lookup"><span data-stu-id="8cac6-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="8cac6-108">此外，有许多可用选项，所以您可以修改工作流并将其与申报层次结构关联。</span><span class="sxs-lookup"><span data-stu-id="8cac6-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="8cac6-109">提供工作流是为了帮助管理对多种标准员工信息类型的更改。</span><span class="sxs-lookup"><span data-stu-id="8cac6-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="8cac6-110">您可以将工作流与职位相关联。</span><span class="sxs-lookup"><span data-stu-id="8cac6-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="8cac6-111">然后，如果员工更改其员工记录，将在保存新信息之前启动要求批准的工作流。</span><span class="sxs-lookup"><span data-stu-id="8cac6-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="8cac6-112">为以下类型的信息预定义了工作流，帮助您有效管理更改和维护员工数据的精确性：</span><span class="sxs-lookup"><span data-stu-id="8cac6-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="8cac6-113">标识号</span><span class="sxs-lookup"><span data-stu-id="8cac6-113">Identification numbers</span></span>
-   <span data-ttu-id="8cac6-114">课程</span><span class="sxs-lookup"><span data-stu-id="8cac6-114">Courses</span></span>
-   <span data-ttu-id="8cac6-115">教育程度</span><span class="sxs-lookup"><span data-stu-id="8cac6-115">Education</span></span>
-   <span data-ttu-id="8cac6-116">图像</span><span class="sxs-lookup"><span data-stu-id="8cac6-116">Image</span></span>
-   <span data-ttu-id="8cac6-117">借出物品</span><span class="sxs-lookup"><span data-stu-id="8cac6-117">Loaned items</span></span>
-   <span data-ttu-id="8cac6-118">专业经验</span><span class="sxs-lookup"><span data-stu-id="8cac6-118">Professional experience</span></span>
-   <span data-ttu-id="8cac6-119">项目经验</span><span class="sxs-lookup"><span data-stu-id="8cac6-119">Project experience</span></span>
-   <span data-ttu-id="8cac6-120">技能</span><span class="sxs-lookup"><span data-stu-id="8cac6-120">Skills</span></span>
-   <span data-ttu-id="8cac6-121">诚信职位</span><span class="sxs-lookup"><span data-stu-id="8cac6-121">Positions of trust</span></span>
-   <span data-ttu-id="8cac6-122">人力资源行动</span><span class="sxs-lookup"><span data-stu-id="8cac6-122">Human resources actions</span></span>
-   <span data-ttu-id="8cac6-123">课程登记</span><span class="sxs-lookup"><span data-stu-id="8cac6-123">Course registration</span></span>

<span data-ttu-id="8cac6-124">员工受聘、转岗或退休后，工作流中可以包含审核流程。</span><span class="sxs-lookup"><span data-stu-id="8cac6-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="8cac6-125">可以按照这种方式修订票据，或将行为的条款定义为工作流的一部分。</span><span class="sxs-lookup"><span data-stu-id="8cac6-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="8cac6-126">审核流程完成时，将完成票据或行为，而工作流将进入最后的批准步骤。</span><span class="sxs-lookup"><span data-stu-id="8cac6-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="8cac6-127">将工作流与职位层次结构关联</span><span class="sxs-lookup"><span data-stu-id="8cac6-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="8cac6-128">您可以将工作流与您正在配置的任何层次结构关联。</span><span class="sxs-lookup"><span data-stu-id="8cac6-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="8cac6-129">例如，如果某一职位矩阵报告层次结构关联，您可以配置一个工作流，用于将特定项目的费用发送给项目主管，而不是与该职位关联的员工的经理。</span><span class="sxs-lookup"><span data-stu-id="8cac6-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="8cac6-130">若要创建新工作流或修改现有工作流，请在 **人力资源工作流** 页上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="8cac6-131">选择列表中的工作流来启动工作流设计器。</span><span class="sxs-lookup"><span data-stu-id="8cac6-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="8cac6-132">可以使用该设计器创建新工作流或更改现有工作流中的步骤。</span><span class="sxs-lookup"><span data-stu-id="8cac6-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="8cac6-133">更改现有工作流时，更改保存为新版本。</span><span class="sxs-lookup"><span data-stu-id="8cac6-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="8cac6-134">因此，如有必要，始终可以恢复为以前的版本。</span><span class="sxs-lookup"><span data-stu-id="8cac6-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="8cac6-135">配置人力资源工作流</span><span class="sxs-lookup"><span data-stu-id="8cac6-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="8cac6-136">若要配置员工请求更改其个人身份时启动的基本工作流，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8cac6-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="8cac6-137">在 **人力资源工作流** 页中，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="8cac6-138">在可用工作流列表中，选择 **标识号**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="8cac6-139">单击 **运行** 启动工作流设计器，然后在系统提示时输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="8cac6-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="8cac6-140">将 **审核标识号** 元素从工作流元素列表拖到设计器画布。</span><span class="sxs-lookup"><span data-stu-id="8cac6-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="8cac6-141">将审核元素连接到 **开始** 和 **完成**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="8cac6-142">双击 **审核元素**，右键单击，然后选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="8cac6-143">执行以下步骤添加工作项说明：</span><span class="sxs-lookup"><span data-stu-id="8cac6-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="8cac6-144">选择 **分配**，然后选择分配类型下的 **层次结构**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="8cac6-145">在 **层次结构** 下，选择 **可配置的层次结构**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="8cac6-146">添加停止条件，然后关闭该页。</span><span class="sxs-lookup"><span data-stu-id="8cac6-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="8cac6-147">完成其他所有说明（不应存在更多警告）。</span><span class="sxs-lookup"><span data-stu-id="8cac6-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="8cac6-148">单击 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-148">Click **Save and close**.</span></span> <span data-ttu-id="8cac6-149">对话框打开时激活新工作流，然后选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="8cac6-150">转至 **人力资源** &gt; **职位** &gt; **职位层次结构类型**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="8cac6-151">选择 **矩阵**。</span><span class="sxs-lookup"><span data-stu-id="8cac6-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="8cac6-152">将 **工作人员标识号** 工作流添加到列表。</span><span class="sxs-lookup"><span data-stu-id="8cac6-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cac6-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="8cac6-153">Additional resources</span></span>

[<span data-ttu-id="8cac6-154">查看和管理地址更改</span><span class="sxs-lookup"><span data-stu-id="8cac6-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]