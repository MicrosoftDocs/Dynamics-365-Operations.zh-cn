---
title: 访问 Talent 中的预览功能
description: 此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。
author: tracykeya
manager: AnnBe
ms.date: 04/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 72e2a3c62c7aab0f5cf8900c540a22d91be00609
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517466"
---
# <a name="access-preview-features-in-talent"></a><span data-ttu-id="c6f34-103">访问 Talent 中的预览功能</span><span class="sxs-lookup"><span data-stu-id="c6f34-103">Access preview features in Talent</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c6f34-104">在持续推出产品功能时，我们希望让客户尽快体验新功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-104">As part of our continuous rollout of product capabilities, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="c6f34-105">管理员可以在自己的环境中查看和使用预览功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="c6f34-106">这些功能几乎已针对普通使用准备就绪，并经过了大量测试。</span><span class="sxs-lookup"><span data-stu-id="c6f34-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="c6f34-107">我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。</span><span class="sxs-lookup"><span data-stu-id="c6f34-107">We are just looking for a final round of customer feedback and validation before we generally release them.</span></span>

<span data-ttu-id="c6f34-108">此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-108">This topic describes how an administrator can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="c6f34-109">发布功能以公开推出和发布新功能以预览时，将更新此列表。</span><span class="sxs-lookup"><span data-stu-id="c6f34-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="c6f34-110">发布新功能以预览时，不提供通知。</span><span class="sxs-lookup"><span data-stu-id="c6f34-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="c6f34-111">用户只需启动即可查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-111">Users will just start to see the features.</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="c6f34-112">启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="c6f34-112">Enable or disable preview features</span></span>

<span data-ttu-id="c6f34-113">可使用 Microsoft Dynamics 365 for Talent 管理员中心中的**预览功能**设置启用或禁用预览功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-113">You can use the **Preview Features** setting in the Microsoft Dynamics 365 for Talent admin center to enable or disable preview features.</span></span> <span data-ttu-id="c6f34-114">默认情况下，已关闭此设置。</span><span class="sxs-lookup"><span data-stu-id="c6f34-114">By default, the setting is turned off.</span></span> <span data-ttu-id="c6f34-115">预览功能的启用或禁用操作特定于环境。</span><span class="sxs-lookup"><span data-stu-id="c6f34-115">The action of enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6f34-116">通过开启**预览功能**设置，即对组织中该环境的所有用户启用了预览功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-116">By turning on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="c6f34-117">通过关闭此设置，即禁用了预览功能，并且您的用户不能访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-117">By turning off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="c6f34-118">在 Talent 中，对预览功能的支持受限。</span><span class="sxs-lookup"><span data-stu-id="c6f34-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="c6f34-119">预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议中不涵盖预览功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement.</span></span> <span data-ttu-id="c6f34-120">不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。</span><span class="sxs-lookup"><span data-stu-id="c6f34-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="enable-or-disable-preview-features-for-your-organization"></a><span data-ttu-id="c6f34-121">为组织启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="c6f34-121">Enable or disable preview features for your organization</span></span>

#### <a name="attract"></a><span data-ttu-id="c6f34-122">吸引</span><span class="sxs-lookup"><span data-stu-id="c6f34-122">Attract</span></span>

1. <span data-ttu-id="c6f34-123">登录到 Microsoft Dynamics 365 for Talent: Attract。</span><span class="sxs-lookup"><span data-stu-id="c6f34-123">Sign in to Microsoft Dynamics 365 for Talent: Attract.</span></span>
2. <span data-ttu-id="c6f34-124">在右上角的**设置**菜单（齿轮符号）中，选择**管理员设置**。</span><span class="sxs-lookup"><span data-stu-id="c6f34-124">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin settings**.</span></span>
3. <span data-ttu-id="c6f34-125">在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色。</span><span class="sxs-lookup"><span data-stu-id="c6f34-125">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue.</span></span>
4. <span data-ttu-id="c6f34-126">您可以选择通过启用/禁用此页面上的特定功能来控制各个功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-126">Optionally you can control individual features by enabling/disabling specific features on this page.</span></span>
5. <span data-ttu-id="c6f34-127">刷新浏览器以开始查看新功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-127">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="c6f34-128">（所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。）</span><span class="sxs-lookup"><span data-stu-id="c6f34-128">(Any users who are already signed in will see the features the next time that they sign in, or they can refresh their browser to see the features immediately.)</span></span>

#### <a name="core-hr"></a><span data-ttu-id="c6f34-129">Core HR</span><span class="sxs-lookup"><span data-stu-id="c6f34-129">Core HR</span></span>

1. <span data-ttu-id="c6f34-130">登录 Talent。</span><span class="sxs-lookup"><span data-stu-id="c6f34-130">Sign in to Talent.</span></span> <span data-ttu-id="c6f34-131">将打开“核心人力资源”工作区，可在其中完成其余步骤。</span><span class="sxs-lookup"><span data-stu-id="c6f34-131">The core Human resources workspace will open, from which you'll complete the remaining steps.</span></span> 
2. <span data-ttu-id="c6f34-132">选择**系统管理 \> 链接系统参数**。</span><span class="sxs-lookup"><span data-stu-id="c6f34-132">Select **System administration \> Links System parameters**.</span></span>
3. <span data-ttu-id="c6f34-133">在**系统参数**页**预览功能**选项卡上，将**为所有用户启用预览模式**选项设置为**是**，以便启用预览功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-133">On the **System Parameters page**, on the **Preview features** tab, set the **Enable preview mode for all users** option to **Yes** to make preview features available.</span></span>

> [!NOTE]
> <span data-ttu-id="c6f34-134">若要禁用预览功能，请使用相同的基本步骤。</span><span class="sxs-lookup"><span data-stu-id="c6f34-134">To disable preview features, use the same basic steps.</span></span> <span data-ttu-id="c6f34-135">禁用后，您的用户不能访问预览功能，并且预览功能的相关流程中可能出错。</span><span class="sxs-lookup"><span data-stu-id="c6f34-135">When you disable preview features, they become inaccessible to your users, and errors might occur in processes that are associated with the features.</span></span>

## <a name="features-that-are-currently-in-preview"></a><span data-ttu-id="c6f34-136">当前的预览功能</span><span class="sxs-lookup"><span data-stu-id="c6f34-136">Features that are currently in preview</span></span>

### <a name="attract"></a><span data-ttu-id="c6f34-137">吸引</span><span class="sxs-lookup"><span data-stu-id="c6f34-137">Attract</span></span>

- <span data-ttu-id="c6f34-138">**工作中的相关应聘者** – 招聘人员和招聘经理可以轻松地查看哪些应聘者与跨所有申请人的工作最相关。</span><span class="sxs-lookup"><span data-stu-id="c6f34-138">**Relevant Candidates in a Job** – Recruiters and hiring managers can easily see which candidates may be the most relevant for the job across all applicants.</span></span> <span data-ttu-id="c6f34-139">根据简历/模板与工作描述的相关性显示前 5 个申请人。</span><span class="sxs-lookup"><span data-stu-id="c6f34-139">The top 5 applicants are shown based on their the relevance of their resume/profile to the job description.</span></span>
- <span data-ttu-id="c6f34-140">**相关工作** – 应聘者现在可以看到根据其简历/模板和工作描述与其相关的其他工作的列表。</span><span class="sxs-lookup"><span data-stu-id="c6f34-140">**Relevant Jobs** – Candidates now see a list of other jobs that are relevant to them based on their resume/profile and the job descriptions.</span></span>  <span data-ttu-id="c6f34-141">现在，当应聘者作为建议申请其他机会时，这将显示给应聘者。</span><span class="sxs-lookup"><span data-stu-id="c6f34-141">Currently this is shown to candidates once they apply as a suggestion for other opportunities.</span></span>
- <span data-ttu-id="c6f34-142">**EEO/OFCCP 支持** – 新活动类型允许使用预定义的窗体从应聘者处收集平等就业机会 (EEO) 和联邦合同合规性计划办公室 (OFCCP) 数据。</span><span class="sxs-lookup"><span data-stu-id="c6f34-142">**EEO/OFCCP Support** – New activity types enable the use of a predefined form for the collection of Equal Employment Opportunity  (EEO) and Office of Federal Contract Compliance Program (OFCCP) data from the candidate.</span></span>  <span data-ttu-id="c6f34-143">这是预定义的窗体，不可编辑。</span><span class="sxs-lookup"><span data-stu-id="c6f34-143">This is a predefined form and is not editable.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6f34-144">只有订阅了一个或多个 LinkedIn 工作清单产品的客户才可查看发布的工作。</span><span class="sxs-lookup"><span data-stu-id="c6f34-144">Jobs that are posted are visible only to customers who subscribe to one or more LinkedIn job listing products.</span></span> <span data-ttu-id="c6f34-145">否则，客户只有明确搜索某个工作，才能看到该工作。</span><span class="sxs-lookup"><span data-stu-id="c6f34-145">Otherwise, customers see a job only if they explicitly search for it.</span></span> <span data-ttu-id="c6f34-146">工作发布到 LinkedIn 时，存在延迟。</span><span class="sxs-lookup"><span data-stu-id="c6f34-146">There is a delay when jobs are posted to LinkedIn.</span></span> <span data-ttu-id="c6f34-147">工作从 Attract 发布后，可能需要几小时才会显示。</span><span class="sxs-lookup"><span data-stu-id="c6f34-147">A job might take up to a few hours to appear after it's posted from Attract.</span></span>

- <span data-ttu-id="c6f34-148">**候选人申请** – 内部候选人和外部候选人现在都可以直接从求职站点的工作页申请。</span><span class="sxs-lookup"><span data-stu-id="c6f34-148">**Candidate apply** – Both internal and external candidates can now apply directly from the job page on the career site.</span></span>
- <span data-ttu-id="c6f34-149">**聘约管理** – 用户现在可通过包含占位符的模板创建录用信。</span><span class="sxs-lookup"><span data-stu-id="c6f34-149">**Offer management** – Users can now create offer letters from templates that include placeholders.</span></span> <span data-ttu-id="c6f34-150">在候选人推进到聘约阶段，招聘人员和和招聘经理可使用录用工具通过模板准备候选人的正式聘约，发送聘约供内部批准，最后将聘约发给候选人签署。</span><span class="sxs-lookup"><span data-stu-id="c6f34-150">As candidates advance to the Offer stage, recruiters and hiring managers can use the Offer tool to prepare a candidate's formal offer via templates, send the offer for internal approval, and finally send the offer to the candidate for signature.</span></span> <span data-ttu-id="c6f34-151">将随时间向聘约工具增加大量新功能，而在我们准备好发布这些功能供预览时，将使用这些功能更新以前的功能。</span><span class="sxs-lookup"><span data-stu-id="c6f34-151">Many new capabilities will be added to the Offer tool over time, and the preview feature will be updated with these capabilities as we are ready to release them to preview.</span></span>
- <span data-ttu-id="c6f34-152">**[分析报告](analytic-reports.md)** – 招聘团队可以通过工作分析查看单个工作的关键指标，或在分析中心中查看所有工作的聚合指标。</span><span class="sxs-lookup"><span data-stu-id="c6f34-152">**[Analytic reports](analytic-reports.md)** – Hiring teams can view key metrics for a single job with Job Analytics or aggregated metrics accross all jobs in the Analytics Hub.</span></span>

### <a name="core-hr"></a><span data-ttu-id="c6f34-153">Core HR</span><span class="sxs-lookup"><span data-stu-id="c6f34-153">Core HR</span></span>

- <span data-ttu-id="c6f34-154">**开放登记** – 福利开放登记让员工可以在选择福利时获得简单的自助式体验。</span><span class="sxs-lookup"><span data-stu-id="c6f34-154">**Open Enrollment** – Benefits open enrollment gives employees a simple, self-service experience for selecting their benefits.</span></span> <span data-ttu-id="c6f34-155">人力资源 (HR) 管理员可使用易于使用的引导式解决方案针对组织和针对员工的登记体验配置福利开放登记流程。</span><span class="sxs-lookup"><span data-stu-id="c6f34-155">Human Resource (HR) administrators can configure the benefits open enrollment process for their organization, and the enrollment experience for employees, by using an easy-to-follow guided solution.</span></span>

## <a name="feedback"></a><span data-ttu-id="c6f34-156">反馈</span><span class="sxs-lookup"><span data-stu-id="c6f34-156">Feedback</span></span>

<span data-ttu-id="c6f34-157">无论反馈正面还是负面，我们都希望倾听您对使用预览功能的看法。</span><span class="sxs-lookup"><span data-stu-id="c6f34-157">Regardless of whether the feedback is positive or negative, we want to hear from you about your use of the preview features.</span></span> <span data-ttu-id="c6f34-158">希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈。</span><span class="sxs-lookup"><span data-stu-id="c6f34-158">We encourage you to regularly post your feedback on the following sites as you use these or any other features.</span></span>

- <span data-ttu-id="c6f34-159">[社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。</span><span class="sxs-lookup"><span data-stu-id="c6f34-159">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="c6f34-160">可使用以下站点提供产品观点方面的建议。</span><span class="sxs-lookup"><span data-stu-id="c6f34-160">Use the following sites to suggest product ideas.</span></span> <span data-ttu-id="c6f34-161">告知我们您希望在产品中看到的功能，以及您认为应对现有功能进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="c6f34-161">Let us know about features that you want to see in the product, and also any changes that you think should be made to existing features.</span></span>

    - [<span data-ttu-id="c6f34-162">Attract 观点</span><span class="sxs-lookup"><span data-stu-id="c6f34-162">Attract Ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="c6f34-163">Core HR</span><span class="sxs-lookup"><span data-stu-id="c6f34-163">Core HR</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

<span data-ttu-id="c6f34-164">请勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。</span><span class="sxs-lookup"><span data-stu-id="c6f34-164">Don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="c6f34-165">可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。</span><span class="sxs-lookup"><span data-stu-id="c6f34-165">Information that is collected might be analyzed further, and it won't be used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="c6f34-166">在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。</span><span class="sxs-lookup"><span data-stu-id="c6f34-166">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="c6f34-167">将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。</span><span class="sxs-lookup"><span data-stu-id="c6f34-167">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>
