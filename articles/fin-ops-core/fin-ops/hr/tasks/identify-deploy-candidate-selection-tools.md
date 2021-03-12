---
title: 确定和部署候选人选择工具
description: 找到符合条件的候选人填补空缺不是一件容易的事，尤其是在该职位需要一系列独特技能时。
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8015d4e32da2ba80230aa0ad48576948f2fd1678
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797742"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="9fa84-103">确定和部署候选人选择工具</span><span class="sxs-lookup"><span data-stu-id="9fa84-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fa84-104">找到符合条件的候选人填补空缺不是一件容易的事，尤其是在该职位需要一系列独特技能时。</span><span class="sxs-lookup"><span data-stu-id="9fa84-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="9fa84-105">但是，具有所需技能的候选人可能已在您的组织中被雇用。</span><span class="sxs-lookup"><span data-stu-id="9fa84-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="9fa84-106">您可以在现有员工或新申请人之间搜索特定的技能组。</span><span class="sxs-lookup"><span data-stu-id="9fa84-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="9fa84-107">这允许招聘人员快速收集和筛选现在或过去申请空缺位置的申请人，或从现有员工库中找到潜在候选人。</span><span class="sxs-lookup"><span data-stu-id="9fa84-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="9fa84-108">使用此任务记录以学习技能表功能如何帮助您为空缺职位找到合适人选。</span><span class="sxs-lookup"><span data-stu-id="9fa84-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="9fa84-109">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="9fa84-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="9fa84-110">转到“人力资源”>“能力”>“技能分析”>“技能表模板”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="9fa84-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-111">Click New.</span></span>
3. <span data-ttu-id="9fa84-112">在“技能表”字段中，为您的技能表输入名称。</span><span class="sxs-lookup"><span data-stu-id="9fa84-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="9fa84-113">示例：会计师。</span><span class="sxs-lookup"><span data-stu-id="9fa84-113">Example: Accountant.</span></span>
4. <span data-ttu-id="9fa84-114">在“描述”字段中，输入技能表的描述。</span><span class="sxs-lookup"><span data-stu-id="9fa84-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="9fa84-115">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="9fa84-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="9fa84-116">单击“检索模板”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="9fa84-117">使用检索模板拉入所选人员、工作或课程的证书、技能和教育数据作为您搜索的基础。</span><span class="sxs-lookup"><span data-stu-id="9fa84-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="9fa84-118">然后您可以添加或删除条件，注明条件是否可选的，并排定条件的重要性等级。</span><span class="sxs-lookup"><span data-stu-id="9fa84-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="9fa84-119">单击“工作”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-119">Click Job.</span></span>
8. <span data-ttu-id="9fa84-120">在“工作”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9fa84-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="9fa84-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-121">Click OK.</span></span>
10. <span data-ttu-id="9fa84-122">展开“范围”快速选项卡，添加其他附加信息，如部门。</span><span class="sxs-lookup"><span data-stu-id="9fa84-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="9fa84-123">展开“证书”快速选项卡以查看或编辑证书。</span><span class="sxs-lookup"><span data-stu-id="9fa84-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="9fa84-124">展开“技能”快速选项卡以查看或编辑技能。</span><span class="sxs-lookup"><span data-stu-id="9fa84-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="9fa84-125">展开“教育”快速选项卡以查看或编辑教育条件。</span><span class="sxs-lookup"><span data-stu-id="9fa84-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="9fa84-126">单击“执行”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-126">Click Execute.</span></span>
15. <span data-ttu-id="9fa84-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-127">Click OK.</span></span>
16. <span data-ttu-id="9fa84-128">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-128">Click Result.</span></span>
17. <span data-ttu-id="9fa84-129">单击“结果”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-129">Click Result.</span></span>
18. <span data-ttu-id="9fa84-130">单击“恢复”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-130">Click Resume.</span></span>
19. <span data-ttu-id="9fa84-131">单击“证书”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-131">Click Certificates.</span></span>
    * <span data-ttu-id="9fa84-132">您可以深入分析所列出的每个人并查看有关其教育程度、技能、专业经验的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9fa84-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="9fa84-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fa84-133">Close the page.</span></span>
21. <span data-ttu-id="9fa84-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fa84-134">Close the page.</span></span>
22. <span data-ttu-id="9fa84-135">再次选择结果。</span><span class="sxs-lookup"><span data-stu-id="9fa84-135">Select result again.</span></span>
23. <span data-ttu-id="9fa84-136">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-136">Click Report.</span></span>
    * <span data-ttu-id="9fa84-137">报表将在报表顶部列出最佳匹配。</span><span class="sxs-lookup"><span data-stu-id="9fa84-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="9fa84-138">您可以看到列出了一个差距元素。</span><span class="sxs-lookup"><span data-stu-id="9fa84-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="9fa84-139">这是技能表上列出的级别与分配给该人员的技能级别之间的差异。</span><span class="sxs-lookup"><span data-stu-id="9fa84-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="9fa84-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fa84-140">Close the page.</span></span>
25. <span data-ttu-id="9fa84-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9fa84-141">Click Save.</span></span>

