---
title: 输入技能
description: 工作人员和经理可以在 Dynamics 365 Human Resources 中输入技能。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076580"
---
# <a name="enter-skills"></a><span data-ttu-id="9a903-103">输入技能</span><span class="sxs-lookup"><span data-stu-id="9a903-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9a903-104">您可以在 Dynamics 365 Human Resources 中输入工作人员、申请人或联系人的目标技能或实际技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9a903-105">目标技能是计划达到的技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="9a903-106">实际技能是当前具有的技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="9a903-107">创建工作流来自动审核技能</span><span class="sxs-lookup"><span data-stu-id="9a903-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="9a903-108">要输入技能而无需审核，您必须创建一个工作流来自动审核技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="9a903-109">工作人员输入的技能始终需要经理审核。</span><span class="sxs-lookup"><span data-stu-id="9a903-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="9a903-110">此工作流仅自动审核经理代表其工作人员输入的技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="9a903-111">在 **人事管理** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="9a903-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="9a903-112">在 **设置** 下，选择 **人力资源工作流**。</span><span class="sxs-lookup"><span data-stu-id="9a903-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="9a903-113">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9a903-113">Select **New**.</span></span>

4. <span data-ttu-id="9a903-114">在 **创建工作流** 窗格中，选择 **工作人员技能**。</span><span class="sxs-lookup"><span data-stu-id="9a903-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="9a903-115">[![选择工作人员技能工作流](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="9a903-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="9a903-116">在 **打开此文件?** 对话中，选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="9a903-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="9a903-117">出现提示时，输入您的凭据。</span><span class="sxs-lookup"><span data-stu-id="9a903-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="9a903-118">在工作流编辑器中，选择 **审核技能** 工作流元素并将其拖到画布上。</span><span class="sxs-lookup"><span data-stu-id="9a903-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="9a903-119">[![选择审核技能工作流元素](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="9a903-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="9a903-120">将 **开始** 元素连接到 **审核技能 1** 元素，然后将 **审核技能 1** 元素连接到 **结束** 元素。</span><span class="sxs-lookup"><span data-stu-id="9a903-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="9a903-121">您可能需要向下滚动来查看 **结束** 元素。</span><span class="sxs-lookup"><span data-stu-id="9a903-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="9a903-122">您可以将其拖到更靠近其他元素的位置。</span><span class="sxs-lookup"><span data-stu-id="9a903-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="9a903-123">[![连接工作流元素](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="9a903-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="9a903-124">双击 **审核技能 1** 工作流元素，然后右键单击 **步骤 1** 元素。</span><span class="sxs-lookup"><span data-stu-id="9a903-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="9a903-125">右键单击 **步骤 1** 元素，然后选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="9a903-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="9a903-126">在 **属性** 窗口中，在左侧导航栏上选择 **条件**。</span><span class="sxs-lookup"><span data-stu-id="9a903-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="9a903-127">选择 **仅当满足以下条件时运行此步骤**。</span><span class="sxs-lookup"><span data-stu-id="9a903-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="9a903-128">选择 **添加条件**。</span><span class="sxs-lookup"><span data-stu-id="9a903-128">Select **Add condition**.</span></span> <span data-ttu-id="9a903-129">在 **位置** 之后，选择 **员工自助服务技能**，然后选择 **员工自助服务技能.人员**。</span><span class="sxs-lookup"><span data-stu-id="9a903-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="9a903-130">在 **是** 之后，选择 **现场**，然后选择 **用户与人员的关系.人员**。</span><span class="sxs-lookup"><span data-stu-id="9a903-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="9a903-131">[![指定条件](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="9a903-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="9a903-132">在左侧导航栏上选择 **分配**。</span><span class="sxs-lookup"><span data-stu-id="9a903-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="9a903-133">在 **分配类型** 选项卡上，选择 **层次结构**。</span><span class="sxs-lookup"><span data-stu-id="9a903-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="9a903-134">在 **层次结构选择** 选项卡上，在 **层次结构类型:** 字段中，选择 **管理层次结构**。</span><span class="sxs-lookup"><span data-stu-id="9a903-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="9a903-135">[![指定管理层次结构](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="9a903-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="9a903-136">选择 **关闭**，在画布痕迹导航中选择 **工作流**，然后选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="9a903-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="9a903-137">有关创建工作流的详细信息，请参阅[工作流系统概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="9a903-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="9a903-138">输入工作人员的技能</span><span class="sxs-lookup"><span data-stu-id="9a903-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="9a903-139">选择一个工作人员。</span><span class="sxs-lookup"><span data-stu-id="9a903-139">Select a worker.</span></span>

2. <span data-ttu-id="9a903-140">在 **工作人员** 页面的操作栏中，选择 **人员**，然后选择 **技能**。</span><span class="sxs-lookup"><span data-stu-id="9a903-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="9a903-141">在 **技能** 页面上，为每个技能完成以下字段：</span><span class="sxs-lookup"><span data-stu-id="9a903-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="9a903-142">**技能**：选择一项技能。</span><span class="sxs-lookup"><span data-stu-id="9a903-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="9a903-143">**级别类型**：对于工作人员已有的技能，选择 **实际**，对于工作人员正在努力掌握的技能，选择 **目标**。</span><span class="sxs-lookup"><span data-stu-id="9a903-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="9a903-144">**级别**：为工作人员的技能选择级别。</span><span class="sxs-lookup"><span data-stu-id="9a903-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="9a903-145">**级别日期**：在日历工具中选择一个日期。</span><span class="sxs-lookup"><span data-stu-id="9a903-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="9a903-146">**主考人**：如果适用，从列表中选择主考人。</span><span class="sxs-lookup"><span data-stu-id="9a903-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="9a903-147">您可以对搜索进行筛选。</span><span class="sxs-lookup"><span data-stu-id="9a903-147">You can filter your search.</span></span>
   - <span data-ttu-id="9a903-148">**年资**：输入拥有经验的年数。</span><span class="sxs-lookup"><span data-stu-id="9a903-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="9a903-149">**已验证**：如果技能已经过验证，选中此框。</span><span class="sxs-lookup"><span data-stu-id="9a903-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="9a903-150">**验证人**：输入验证者的姓名。</span><span class="sxs-lookup"><span data-stu-id="9a903-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="9a903-151">输入技能后，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9a903-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a903-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a903-152">See also</span></span>

[<span data-ttu-id="9a903-153">配置技能</span><span class="sxs-lookup"><span data-stu-id="9a903-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="9a903-154">映射技能</span><span class="sxs-lookup"><span data-stu-id="9a903-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]