---
title: 配置技能
description: 您可以在 Dynamics 365 Human Resources 中跟踪工作人员的技能。 您还可以指定特定工作所需的技能。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076551"
---
# <a name="configure-skills"></a><span data-ttu-id="56b02-104">配置技能</span><span class="sxs-lookup"><span data-stu-id="56b02-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="56b02-105">您可以在 Dynamics 365 Human Resources 中跟踪工作人员的技能。</span><span class="sxs-lookup"><span data-stu-id="56b02-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="56b02-106">您还可以指定特定工作所需的技能。</span><span class="sxs-lookup"><span data-stu-id="56b02-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="56b02-107">您可以跟踪的技能示例包括：</span><span class="sxs-lookup"><span data-stu-id="56b02-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="56b02-108">监督能力 - 监督其他人的工作的能力。</span><span class="sxs-lookup"><span data-stu-id="56b02-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="56b02-109">领导能力 - 在员工和业务领域中起领导作用的能力。</span><span class="sxs-lookup"><span data-stu-id="56b02-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="56b02-110">计划 – 能够预测未来、建立愿景，并能够深入理解。</span><span class="sxs-lookup"><span data-stu-id="56b02-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="56b02-111">HTML – 编写 HTML 代码的能力。</span><span class="sxs-lookup"><span data-stu-id="56b02-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="56b02-112">如果尚未设置技能类型和评级模型，您需要在创建技能之前添加一部分。</span><span class="sxs-lookup"><span data-stu-id="56b02-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="56b02-113">以下人员可以为工作人员输入技能：</span><span class="sxs-lookup"><span data-stu-id="56b02-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="56b02-114">工作人员可以在员工自助服务中为自己输入技能。</span><span class="sxs-lookup"><span data-stu-id="56b02-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="56b02-115">这些技能需要经理审核。</span><span class="sxs-lookup"><span data-stu-id="56b02-115">These skills require manager approval.</span></span>
- <span data-ttu-id="56b02-116">经理可以为他的工作人员输入技能。</span><span class="sxs-lookup"><span data-stu-id="56b02-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="56b02-117">您可以创建自动审核这些技能的工作流。</span><span class="sxs-lookup"><span data-stu-id="56b02-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="56b02-118">创建技能类型</span><span class="sxs-lookup"><span data-stu-id="56b02-118">Create a skill type</span></span>

<span data-ttu-id="56b02-119">技能类型是各个技能所属的类别，如管理或销售。</span><span class="sxs-lookup"><span data-stu-id="56b02-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="56b02-120">在 **员工发展** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="56b02-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="56b02-121">在 **能力设置** 下，选择 **技能类型**。</span><span class="sxs-lookup"><span data-stu-id="56b02-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="56b02-122">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56b02-122">Select **New**.</span></span>

4. <span data-ttu-id="56b02-123">完成以下字段：</span><span class="sxs-lookup"><span data-stu-id="56b02-123">Complete the following fields:</span></span>

   - <span data-ttu-id="56b02-124">**技能类型**：为技能类型输入名称。</span><span class="sxs-lookup"><span data-stu-id="56b02-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="56b02-125">**描述**：为技能类型输入描述。</span><span class="sxs-lookup"><span data-stu-id="56b02-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="56b02-126">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56b02-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="56b02-127">创建评级模型</span><span class="sxs-lookup"><span data-stu-id="56b02-127">Create a rating model</span></span>

<span data-ttu-id="56b02-128">评级模型帮助评估人员的实际技能级别，应达到的级别或工作需要的技能级别。</span><span class="sxs-lookup"><span data-stu-id="56b02-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="56b02-129">评级模型中的每个级别都会被分配一个系数。</span><span class="sxs-lookup"><span data-stu-id="56b02-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="56b02-130">在 **员工发展** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="56b02-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="56b02-131">在 **能力设置** 下，选择 **评级模型**。</span><span class="sxs-lookup"><span data-stu-id="56b02-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="56b02-132">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56b02-132">Select **New**.</span></span>

4. <span data-ttu-id="56b02-133">完成以下字段：</span><span class="sxs-lookup"><span data-stu-id="56b02-133">Complete the following fields:</span></span>

   - <span data-ttu-id="56b02-134">**评级**：为评级模型输入名称，如 **技能**。</span><span class="sxs-lookup"><span data-stu-id="56b02-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="56b02-135">**描述**：为评级模型输入描述，如 **技能评级**。</span><span class="sxs-lookup"><span data-stu-id="56b02-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="56b02-136">在 **级别** 部分，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56b02-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="56b02-137">对于要添加的每个级别，填写以下字段：</span><span class="sxs-lookup"><span data-stu-id="56b02-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="56b02-138">**级别**：为级别输入名称。</span><span class="sxs-lookup"><span data-stu-id="56b02-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="56b02-139">**描述**：为级别输入描述。</span><span class="sxs-lookup"><span data-stu-id="56b02-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="56b02-140">**系数**：输入一个 0 到 9 的系数值。</span><span class="sxs-lookup"><span data-stu-id="56b02-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="56b02-141">系数帮助标准化使用不同评级模型的技能分数。</span><span class="sxs-lookup"><span data-stu-id="56b02-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="56b02-142">每个级别必须有一个唯一系数。</span><span class="sxs-lookup"><span data-stu-id="56b02-142">Each level must have a unique factor.</span></span> <span data-ttu-id="56b02-143">用更高系数值的级别在评级模型中更有重量。</span><span class="sxs-lookup"><span data-stu-id="56b02-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="56b02-144">继续根据需要添加级别。</span><span class="sxs-lookup"><span data-stu-id="56b02-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="56b02-145">最多可以为每个评级模型输入 10 个级别。</span><span class="sxs-lookup"><span data-stu-id="56b02-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="56b02-146">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56b02-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="56b02-147">创建技能</span><span class="sxs-lookup"><span data-stu-id="56b02-147">Create a skill</span></span>

<span data-ttu-id="56b02-148">您必须先在 **技能** 页上输入有关技能的信息，然后才能够分配技能或创建技能映射搜索或技能模板。</span><span class="sxs-lookup"><span data-stu-id="56b02-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="56b02-149">对于每个技能，您可以选择技能类型和评级模型。</span><span class="sxs-lookup"><span data-stu-id="56b02-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="56b02-150">在 **员工发展** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="56b02-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="56b02-151">在 **能力设置** 下，选择 **技能**。</span><span class="sxs-lookup"><span data-stu-id="56b02-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="56b02-152">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56b02-152">Select **New**.</span></span>

4. <span data-ttu-id="56b02-153">完成以下字段：</span><span class="sxs-lookup"><span data-stu-id="56b02-153">Complete the following fields:</span></span>

   - <span data-ttu-id="56b02-154">**技能**：为技能输入名称。</span><span class="sxs-lookup"><span data-stu-id="56b02-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="56b02-155">**描述**：为技能输入描述。</span><span class="sxs-lookup"><span data-stu-id="56b02-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="56b02-156">**评级**：选择您要用于此技能的评级模型。</span><span class="sxs-lookup"><span data-stu-id="56b02-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="56b02-157">**技能类型**：从技能类型列表中选择。</span><span class="sxs-lookup"><span data-stu-id="56b02-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="56b02-158">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56b02-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="56b02-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="56b02-159">See also</span></span>

[<span data-ttu-id="56b02-160">输入技能</span><span class="sxs-lookup"><span data-stu-id="56b02-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="56b02-161">映射技能</span><span class="sxs-lookup"><span data-stu-id="56b02-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]