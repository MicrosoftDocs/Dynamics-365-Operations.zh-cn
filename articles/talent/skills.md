---
title: 让劳动力技能符合业务需要
description: 您可以跟踪工作人员、申请人或联系人具有或应该具有的技能，以有效地履行其角色。 您还可以指定特定工作所需的技能。
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 0dd1f00cd2558c69941279e5f41256be621d7c74
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "857167"
---
# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="b124e-104">让劳动力技能符合业务需要</span><span class="sxs-lookup"><span data-stu-id="b124e-104">Align workforce skills with business needs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b124e-105">您可以跟踪工作人员、申请人或联系人具有或应该具有的技能，以有效地履行其角色。</span><span class="sxs-lookup"><span data-stu-id="b124e-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="b124e-106">您还可以指定特定工作所需的技能。</span><span class="sxs-lookup"><span data-stu-id="b124e-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="b124e-107">您可以跟踪的技能示例包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="b124e-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="b124e-108">监督能力 - 监督其他人的工作的能力。</span><span class="sxs-lookup"><span data-stu-id="b124e-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="b124e-109">领导能力 - 在员工和业务领域中起领导作用的能力。</span><span class="sxs-lookup"><span data-stu-id="b124e-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="b124e-110">计划能力 - 洞察未来发展趋势的能力。</span><span class="sxs-lookup"><span data-stu-id="b124e-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="b124e-111">HTML – 编写 HTML 代码的能力。</span><span class="sxs-lookup"><span data-stu-id="b124e-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="b124e-112">在您可以将技能分配给人员或工作，创建技能表搜索或创建技能模板之前，必须在**技能**页上输入有关技能的信息。</span><span class="sxs-lookup"><span data-stu-id="b124e-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="b124e-113">对于每个技能，您可以选择技能类型和评级模型。</span><span class="sxs-lookup"><span data-stu-id="b124e-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="b124e-114">评级模型</span><span class="sxs-lookup"><span data-stu-id="b124e-114">Rating models</span></span>
<span data-ttu-id="b124e-115">评级模型帮助评估人员的实际技能级别，应达到的级别或工作需要的技能级别。</span><span class="sxs-lookup"><span data-stu-id="b124e-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="b124e-116">您最多可以输入评级模型的 10 个级别。</span><span class="sxs-lookup"><span data-stu-id="b124e-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="b124e-117">评级模型中的每个级别都会被分配一个系数。</span><span class="sxs-lookup"><span data-stu-id="b124e-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="b124e-118">系数值将用于标准化使用不同评级模型的技能分数。</span><span class="sxs-lookup"><span data-stu-id="b124e-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="b124e-119">该系数必须是 0-9 之间的数字，并且每个级别都必须有唯一的系数。</span><span class="sxs-lookup"><span data-stu-id="b124e-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="b124e-120">用更高系数值的级别在评级模型中更有重量。</span><span class="sxs-lookup"><span data-stu-id="b124e-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="b124e-121">指定工作技能</span><span class="sxs-lookup"><span data-stu-id="b124e-121">Specify job skills</span></span>
<span data-ttu-id="b124e-122">在您输入该工作信息时，您可以指定用户在可以承担该职务的工作前应该具有的技能。</span><span class="sxs-lookup"><span data-stu-id="b124e-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="b124e-123">此外，您还可以为每个技能指定所需级别以及技能的重要程度。</span><span class="sxs-lookup"><span data-stu-id="b124e-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="b124e-124">同一技能对不同工作的重要程度各不相同。</span><span class="sxs-lookup"><span data-stu-id="b124e-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="b124e-125">输入工作人员、申请人或联系人的技能</span><span class="sxs-lookup"><span data-stu-id="b124e-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="b124e-126">您可以输入工作人员、申请人或联系人的目标技能或实际技能。</span><span class="sxs-lookup"><span data-stu-id="b124e-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="b124e-127">目标技能是计划达到的技能。</span><span class="sxs-lookup"><span data-stu-id="b124e-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b124e-128">实际技能是当前具有的技能。</span><span class="sxs-lookup"><span data-stu-id="b124e-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="b124e-129">技能表和技能表模板</span><span class="sxs-lookup"><span data-stu-id="b124e-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="b124e-130">您可以创建技能表搜索找到有资格执行特定类型任务的工作人员、申请人或联系人。</span><span class="sxs-lookup"><span data-stu-id="b124e-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="b124e-131">技能表搜索会跨技能、教育、证书、诚信职位和项目经验进行查找并返回与输入的条件匹配的结果。</span><span class="sxs-lookup"><span data-stu-id="b124e-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="b124e-132">例如，知道您的组织中哪些工作人员获得了其 CPA 可能很有用。</span><span class="sxs-lookup"><span data-stu-id="b124e-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="b124e-133">技能表模板允许您查找具备具有直接符合业务需要的当前员工或候选人。</span><span class="sxs-lookup"><span data-stu-id="b124e-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="b124e-134">例如，您可以为您的组织中的一个空缺职位创建技能表模板。</span><span class="sxs-lookup"><span data-stu-id="b124e-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="b124e-135">通过为特定工作创建模板并从该工作将技能、教育和证书复制到模板，您可以迅速搜索与模板中输入的一个或多个条件匹配的工作人员、申请人，并查看其技能最密切匹配该工作所要求的技能的候选人列表。</span><span class="sxs-lookup"><span data-stu-id="b124e-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="b124e-136">**注意**只有在技能表搜索中包括的所选工作人员、申请人和联系人可以在技能表搜索结果列表中显示或包含在技能模板中。</span><span class="sxs-lookup"><span data-stu-id="b124e-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="b124e-137">若要将工作人员、申请人或联系人包括到技能表搜索中，请在以下页面中将**包括在技能表中**选择设置为“是”：</span><span class="sxs-lookup"><span data-stu-id="b124e-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="b124e-138">工作线程</span><span class="sxs-lookup"><span data-stu-id="b124e-138">Worker</span></span>
> + <span data-ttu-id="b124e-139">员工</span><span class="sxs-lookup"><span data-stu-id="b124e-139">Employee</span></span>
> + <span data-ttu-id="b124e-140">申请人</span><span class="sxs-lookup"><span data-stu-id="b124e-140">Applicant</span></span>
> + <span data-ttu-id="b124e-141">联系人</span><span class="sxs-lookup"><span data-stu-id="b124e-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="b124e-142">技能差距分析和技能模板分析</span><span class="sxs-lookup"><span data-stu-id="b124e-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="b124e-143">您可以创建技能模板分析查看截至特定日期工作人员、申请人或联系人的能力列表。</span><span class="sxs-lookup"><span data-stu-id="b124e-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="b124e-144">可以创建一个技能差距分析将人员的技能与某一特定工作所要求的技能加以比较</span><span class="sxs-lookup"><span data-stu-id="b124e-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="additional-resources"></a><span data-ttu-id="b124e-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="b124e-145">Additional resources</span></span>
--------

[<span data-ttu-id="b124e-146">人力资源</span><span class="sxs-lookup"><span data-stu-id="b124e-146">Human resources</span></span>](index.md)



