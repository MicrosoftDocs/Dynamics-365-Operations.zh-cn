---
title: 映射技能
description: 您可以创建技能映射搜索来在 Dynamics 365 Human Resources 中查找合格人员。
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
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076579"
---
# <a name="map-skills"></a><span data-ttu-id="e5de0-103">映射技能</span><span class="sxs-lookup"><span data-stu-id="e5de0-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e5de0-104">您可以创建技能映射搜索来在 Dynamics 365 Human Resources 中查找合格人员。</span><span class="sxs-lookup"><span data-stu-id="e5de0-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e5de0-105">技能映射搜索通过在以下信息中查找返回满足您输入的条件的结果：</span><span class="sxs-lookup"><span data-stu-id="e5de0-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="e5de0-106">技能</span><span class="sxs-lookup"><span data-stu-id="e5de0-106">Skills</span></span>
- <span data-ttu-id="e5de0-107">教育程度</span><span class="sxs-lookup"><span data-stu-id="e5de0-107">Education</span></span>
- <span data-ttu-id="e5de0-108">证书</span><span class="sxs-lookup"><span data-stu-id="e5de0-108">Certificates</span></span>
- <span data-ttu-id="e5de0-109">职位</span><span class="sxs-lookup"><span data-stu-id="e5de0-109">Positions</span></span>
- <span data-ttu-id="e5de0-110">项目经验</span><span class="sxs-lookup"><span data-stu-id="e5de0-110">Project experience</span></span>

<span data-ttu-id="e5de0-111">例如，您可以查找组织中已获得 CPA 的人员。</span><span class="sxs-lookup"><span data-stu-id="e5de0-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="e5de0-112">技能表模板允许您查找具备具有直接符合业务需要的当前员工或候选人。</span><span class="sxs-lookup"><span data-stu-id="e5de0-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="e5de0-113">只有在技能映射搜索中包括的所选工作人员、申请人和联系人会在技能映射结果列表中显示或包含在技能模板中。</span><span class="sxs-lookup"><span data-stu-id="e5de0-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="e5de0-114">若要将某个人员包括到技能映射搜索中，在以下页面中将 **包括在技能映射中** 选择项设置为 **是**：</span><span class="sxs-lookup"><span data-stu-id="e5de0-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="e5de0-115">工作线程</span><span class="sxs-lookup"><span data-stu-id="e5de0-115">Worker</span></span><br>
> - <span data-ttu-id="e5de0-116">盘点责任人</span><span class="sxs-lookup"><span data-stu-id="e5de0-116">Employee</span></span><br>
> - <span data-ttu-id="e5de0-117">申请人</span><span class="sxs-lookup"><span data-stu-id="e5de0-117">Applicant</span></span><br>
> - <span data-ttu-id="e5de0-118">联系人</span><span class="sxs-lookup"><span data-stu-id="e5de0-118">Contacts</span></span><br>

<span data-ttu-id="e5de0-119">要创建技能映射，转到 **员工发展 > 链接 > 技能映射**。</span><span class="sxs-lookup"><span data-stu-id="e5de0-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="e5de0-120">要创建技能映射模板，转到 **员工发展 > 链接 > 技能映射模板**。</span><span class="sxs-lookup"><span data-stu-id="e5de0-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="e5de0-121">技能差距分析和技能模板分析</span><span class="sxs-lookup"><span data-stu-id="e5de0-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="e5de0-122">您可以创建技能模板分析来查看某个人员的能力列表。</span><span class="sxs-lookup"><span data-stu-id="e5de0-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="e5de0-123">您可以创建技能差距分析来将人员的技能与为工作所需要的技能进行比较。</span><span class="sxs-lookup"><span data-stu-id="e5de0-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="e5de0-124">要创建差距分析，转到 **员工发展 > 链接 > 技能差距分析作业 - 人员**。</span><span class="sxs-lookup"><span data-stu-id="e5de0-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="e5de0-125">要创建技能模板分析，转到 **员工发展 > 链接 > 技能模板分析**。</span><span class="sxs-lookup"><span data-stu-id="e5de0-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5de0-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5de0-126">See also</span></span>

[<span data-ttu-id="e5de0-127">配置技能</span><span class="sxs-lookup"><span data-stu-id="e5de0-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="e5de0-128">输入技能</span><span class="sxs-lookup"><span data-stu-id="e5de0-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]