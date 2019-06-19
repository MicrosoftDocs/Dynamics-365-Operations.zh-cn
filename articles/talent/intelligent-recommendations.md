---
title: 智能建议
description: 此主题说明如何使用机器学习来为工作和工作应聘者提供建议。
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 301e3213fa0988faba83ee42b840646a20c70a98
ms.sourcegitcommit: fcae2e7938d7dbd94b76b0948b084d90d5fc919c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620612"
---
# <a name="intelligent-recommendations"></a><span data-ttu-id="a7b88-103">智能建议</span><span class="sxs-lookup"><span data-stu-id="a7b88-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a7b88-104">机器学习能够帮助招聘人员和招聘经理快速发现最适合职位的应聘者。</span><span class="sxs-lookup"><span data-stu-id="a7b88-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="a7b88-105">它还可以帮助应聘者找到最适合其个人资料和兴趣的职位。</span><span class="sxs-lookup"><span data-stu-id="a7b88-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="a7b88-106">使用这些功能并且提供反馈，推荐将有所改善。</span><span class="sxs-lookup"><span data-stu-id="a7b88-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="a7b88-107">智能推荐功能仅通过[综合招聘加载项](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring)提供。</span><span class="sxs-lookup"><span data-stu-id="a7b88-107">The intelligent recommendation features are available only with the [Comprehensive hiring add-on](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="a7b88-108">本主题中介绍的功能作为预览版的一部分提供给目标用户。</span><span class="sxs-lookup"><span data-stu-id="a7b88-108">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="a7b88-109">内容和功能可能会发生变化。</span><span class="sxs-lookup"><span data-stu-id="a7b88-109">The content and the functionality are subject to change.</span></span> <span data-ttu-id="a7b88-110">若要使用此功能，请让管理员使用 Attract 中的**管理中心**启用。</span><span class="sxs-lookup"><span data-stu-id="a7b88-110">To use this feature, ask an administrator to enable it using the **Admin center** in Attract.</span></span> <span data-ttu-id="a7b88-111">将**应聘者推荐**、**工作推荐**和**潜在人选推荐**设置为**开**。</span><span class="sxs-lookup"><span data-stu-id="a7b88-111">Set **Candidate recommendation**, **Job recommendation**, and **Prospect recommendation** to **On**.</span></span> <span data-ttu-id="a7b88-112">有关详细信息，请参阅[访问 Talent 中的预览功能](./access-preview-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="a7b88-112">For more information, see [Access preview features in Talent](./access-preview-feature.md).</span></span> 


## <a name="candidate-recommendations"></a><span data-ttu-id="a7b88-113">应聘者推荐</span><span class="sxs-lookup"><span data-stu-id="a7b88-113">Candidate recommendations</span></span>

<span data-ttu-id="a7b88-114">由于工作发布可能吸引成百上千个申请人，对于招聘人员和招聘经理来说找到技能和背景最适合职位的应聘者很难。</span><span class="sxs-lookup"><span data-stu-id="a7b88-114">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="a7b88-115">通过分析工作描述和要求之间的相关性，以及来自应聘者简历和个人资料的数据，机器学习可以用于生成应聘者推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-115">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="a7b88-116">应聘者推荐可以帮助招聘人员和招聘经理发现最适合的人才，并快速地将他们移至面试阶段。</span><span class="sxs-lookup"><span data-stu-id="a7b88-116">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="a7b88-117">对于任何工作，如果有超过十名应聘者有简历或完整的个人资料，与工作要求最接近的应聘者将显示在**工作**页的**要考虑的申请人**部分。</span><span class="sxs-lookup"><span data-stu-id="a7b88-117">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="a7b88-118">对于任何推荐的应聘者，您都可以选择应聘者卡上的**查看应聘者**来查看该应聘者的个人资料并对其申请采取行动。</span><span class="sxs-lookup"><span data-stu-id="a7b88-118">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="a7b88-119">您可以使用省略号按钮 (**...**) 在新选项卡上打开应聘者的个人资料。您还可以使用省略号按钮提供有关推荐的反馈。</span><span class="sxs-lookup"><span data-stu-id="a7b88-119">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="a7b88-120">这样，您可以帮助优化推荐引擎并改进将来的推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-120">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="a7b88-121">您不想要的任何推荐在您刷新**工作**页时将从**要考虑的申请人**部分删除。</span><span class="sxs-lookup"><span data-stu-id="a7b88-121">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="a7b88-122">您可以使用反馈卡表示为何未找到有用的推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-122">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="a7b88-123">工作推荐</span><span class="sxs-lookup"><span data-stu-id="a7b88-123">Job recommendations</span></span> 

<span data-ttu-id="a7b88-124">在潜在的员工使用求职站点申请工作时，Attract 将推荐组织中的其他空缺职位。</span><span class="sxs-lookup"><span data-stu-id="a7b88-124">When a prospective employee uses the career site to apply to a job, Attract recommends other open positions at the organization.</span></span> <span data-ttu-id="a7b88-125">这些推荐基于潜在人选过去的申请表，以及简历或应聘者个人资料。</span><span class="sxs-lookup"><span data-stu-id="a7b88-125">These recommendations are based on past applications and the resume or candidate profile of the prospect.</span></span> <span data-ttu-id="a7b88-126">因此，工作推荐帮助应聘者快速发现最适合自己的工作。</span><span class="sxs-lookup"><span data-stu-id="a7b88-126">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="a7b88-127">如果有超过十个工作在求职站点上发布，将为应聘者提供工作推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-127">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="a7b88-128">应聘者可以从推荐卡打开工作发布的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a7b88-128">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="a7b88-129">他们还可以提供有关推荐的反馈以帮助改进将来的推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-129">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

## <a name="prospect-recommendations"></a><span data-ttu-id="a7b88-130">潜在人选推荐</span><span class="sxs-lookup"><span data-stu-id="a7b88-130">Prospect recommendations</span></span> 

<span data-ttu-id="a7b88-131">新职位开放时，浏览所有过去的申请人和整个人才网络可能需要一段时间。</span><span class="sxs-lookup"><span data-stu-id="a7b88-131">When a new position becomes available, looking through all your past applicants and your entire talent network can take a while.</span></span> <span data-ttu-id="a7b88-132">若要让 Attract 帮助您执行此操作，可使用智能机器学习算法。</span><span class="sxs-lookup"><span data-stu-id="a7b88-132">To have Attract help you do this, you can use intelligent machine learning algorithms.</span></span> <span data-ttu-id="a7b88-133">这意味着在您创建工作帐户，Attract 将立即查看所有应聘者，并推荐匹配度高的应聘者。</span><span class="sxs-lookup"><span data-stu-id="a7b88-133">This means that Attract reviews all the candidates and suggests those who are a good match as soon as you create the job.</span></span> <span data-ttu-id="a7b88-134">若要查看这些推荐，请为工作启用**潜在人选**阶段。</span><span class="sxs-lookup"><span data-stu-id="a7b88-134">To view these recommendations, enable the **Prospect** stage for the job.</span></span> <span data-ttu-id="a7b88-135">Attract 可能需要最多一分钟扫描整个应聘者数据库来作出推荐。</span><span class="sxs-lookup"><span data-stu-id="a7b88-135">It may take up to a minute for Attract to scan your entire candidate database to make recommendations.</span></span>

<span data-ttu-id="a7b88-136">将在已启用了**潜在人选**阶段的所有工作的**潜在人选**选项卡上以卡的形式显示建议。</span><span class="sxs-lookup"><span data-stu-id="a7b88-136">The recommendations appear as cards in the **Prospects** tab of any job that has the **Prospect** stage enabled.</span></span> <span data-ttu-id="a7b88-137">这些卡列出潜在人选的个人资料中发现的技能，以及所有教育资格信息。</span><span class="sxs-lookup"><span data-stu-id="a7b88-137">These cards list the skills found in the prospect's profile, as well as any education qualification information.</span></span> <span data-ttu-id="a7b88-138">如果找到您喜欢的建议，可以将应聘者作为该工作的潜在人选添加。</span><span class="sxs-lookup"><span data-stu-id="a7b88-138">If you find a recommendation that you like, you can add the candidate as a prospect for that job.</span></span>

> [!NOTE]
> <span data-ttu-id="a7b88-139">如果现在已开始使用 Attract，则需要等到有 10 个或更多具有完整个人资料或简历的申请人，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="a7b88-139">If you recently started using Attract, you’ll need to wait until you have 10 or more applicants who have full profiles or resumes before you can use this capability.</span></span>

<span data-ttu-id="a7b88-140">为了避免推荐中存在潜在偏见，Attract 仅扫描应聘者个人资料以查找技能、资格和其他与工作描述匹配的关键字。</span><span class="sxs-lookup"><span data-stu-id="a7b88-140">To avoid potential bias in the recommendations, Attract only scans candidate profiles for skills, qualifications, and other keywords that match the job description.</span></span> <span data-ttu-id="a7b88-141">此外，Attract 还会在评估之前从应聘者个人资料中删除个人身份信息。</span><span class="sxs-lookup"><span data-stu-id="a7b88-141">In addition, Attract removes personally identifying information from candidate profiles prior to evaluation.</span></span>
