---
title: "智能建议"
description: "此主题说明如何使用机器学习来为工作和工作应聘者提供建议。"
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/12/2018

---

# <a name="intelligent-recommendations"></a><span data-ttu-id="753a0-103">智能建议</span><span class="sxs-lookup"><span data-stu-id="753a0-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="753a0-104">机器学习能够帮助招聘人员和招聘经理快速发现最适合职位的应聘者。</span><span class="sxs-lookup"><span data-stu-id="753a0-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="753a0-105">它还可以帮助应聘者找到最适合其个人资料和兴趣的职位。</span><span class="sxs-lookup"><span data-stu-id="753a0-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="753a0-106">使用这些功能并且提供反馈，推荐将有所改善。</span><span class="sxs-lookup"><span data-stu-id="753a0-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="753a0-107">智能推荐功能仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="753a0-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="753a0-108">若要启用应聘者和工作推荐功能，管理员必须为其打开预览选项。</span><span class="sxs-lookup"><span data-stu-id="753a0-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="753a0-109">在管理员中心，在**功能管理**选项卡上，请确保**预览功能**选项设置为**开**。</span><span class="sxs-lookup"><span data-stu-id="753a0-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="753a0-110">然后确保各个**应聘者推荐**和**工作推荐**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="753a0-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="753a0-111">应聘者推荐</span><span class="sxs-lookup"><span data-stu-id="753a0-111">Candidate recommendations</span></span>

<span data-ttu-id="753a0-112">由于工作发布可能吸引成百上千个申请人，对于招聘人员和招聘经理来说找到技能和背景最适合职位的应聘者很难。</span><span class="sxs-lookup"><span data-stu-id="753a0-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="753a0-113">通过分析工作描述和要求之间的相关性，以及来自应聘者简历和个人资料的数据，机器学习可以用于生成应聘者推荐。</span><span class="sxs-lookup"><span data-stu-id="753a0-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="753a0-114">应聘者推荐可以帮助招聘人员和招聘经理发现最适合的人才，并快速地将他们移至面试阶段。</span><span class="sxs-lookup"><span data-stu-id="753a0-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="753a0-115">对于任何工作，如果有超过十名应聘者有简历或完整的个人资料，与工作要求最接近的应聘者将显示在**工作**页的**要考虑的申请人**部分。</span><span class="sxs-lookup"><span data-stu-id="753a0-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="753a0-116">对于任何推荐的应聘者，您都可以选择应聘者卡上的**查看应聘者**来查看该应聘者的个人资料并对其申请采取行动。</span><span class="sxs-lookup"><span data-stu-id="753a0-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="753a0-117">您可以使用省略号按钮 (**...**) 在新选项卡上打开应聘者的个人资料。您还可以使用省略号按钮提供有关推荐的反馈。</span><span class="sxs-lookup"><span data-stu-id="753a0-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="753a0-118">这样，您可以帮助优化推荐引擎并改进将来的推荐。</span><span class="sxs-lookup"><span data-stu-id="753a0-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="753a0-119">您不想要的任何推荐在您刷新**工作**页时将从**要考虑的申请人**部分删除。</span><span class="sxs-lookup"><span data-stu-id="753a0-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="753a0-120">您可以使用反馈卡表示为何未找到有用的推荐。</span><span class="sxs-lookup"><span data-stu-id="753a0-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="753a0-121">工作推荐</span><span class="sxs-lookup"><span data-stu-id="753a0-121">Job recommendations</span></span> 

<span data-ttu-id="753a0-122">在潜在的员工使用求职站点申请工作时，将推荐组织中的其他空缺职位。</span><span class="sxs-lookup"><span data-stu-id="753a0-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="753a0-123">这些推荐基于应聘者过去的申请，以及其简历或应聘者个人资料。</span><span class="sxs-lookup"><span data-stu-id="753a0-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="753a0-124">因此，工作推荐帮助应聘者快速发现最适合自己的工作。</span><span class="sxs-lookup"><span data-stu-id="753a0-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="753a0-125">如果有超过十个工作在求职站点上发布，将为应聘者提供工作推荐。</span><span class="sxs-lookup"><span data-stu-id="753a0-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="753a0-126">应聘者可以从推荐卡打开工作发布的详细信息。</span><span class="sxs-lookup"><span data-stu-id="753a0-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="753a0-127">他们还可以提供有关推荐的反馈以帮助改进将来的推荐。</span><span class="sxs-lookup"><span data-stu-id="753a0-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

