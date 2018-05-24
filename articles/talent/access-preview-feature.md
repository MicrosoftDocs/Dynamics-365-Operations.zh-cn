---
title: "访问 Dynamics 365 for Talent 中的预览功能"
description: "此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。"
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2e5dd8f852ac1a6c2997a50a60f03db6adfd218c
ms.openlocfilehash: 5500bfc1cdd1949d301ae82fad5506dfdbeb59f3
ms.contentlocale: zh-cn
ms.lasthandoff: 05/01/2018

---

# <a name="access-preview-features-in-dynamics-365-for-talent"></a><span data-ttu-id="71f33-103">访问 Dynamics 365 for Talent 中的预览功能</span><span class="sxs-lookup"><span data-stu-id="71f33-103">Access preview features in Dynamics 365 for Talent</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="71f33-104">在持续推出产品功能时，我们希望让客户尽快体验新功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-104">As part of our continuous rollout of product capabilities, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="71f33-105">管理员可以在自己的环境中查看和使用预览功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="71f33-106">这些功能几乎已针对普通使用准备就绪，并经过了大量测试。</span><span class="sxs-lookup"><span data-stu-id="71f33-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="71f33-107">我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。</span><span class="sxs-lookup"><span data-stu-id="71f33-107">We are just looking for a final round of customer feedback and validation before we generally release them.</span></span>

<span data-ttu-id="71f33-108">此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-108">This topic describes how an administrator can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="71f33-109">发布功能以公开推出和发布新功能以预览时，将更新此列表。</span><span class="sxs-lookup"><span data-stu-id="71f33-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="71f33-110">发布新功能以预览时，不提供通知。</span><span class="sxs-lookup"><span data-stu-id="71f33-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="71f33-111">用户只需启动即可查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-111">Users will just start to see the features.</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="71f33-112">启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="71f33-112">Enable or disable preview features</span></span>

<span data-ttu-id="71f33-113">可使用 Microsoft Dynamics 365 for Talent 管理员中心中的**预览功能**设置启用或禁用预览功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-113">You can use the **Preview Features** setting in the Microsoft Dynamics 365 for Talent admin center to enable or disable preview features.</span></span> <span data-ttu-id="71f33-114">默认情况下，已关闭此设置。</span><span class="sxs-lookup"><span data-stu-id="71f33-114">By default, the setting is turned off.</span></span> <span data-ttu-id="71f33-115">预览功能的启用或禁用操作特定于环境。</span><span class="sxs-lookup"><span data-stu-id="71f33-115">The action of enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71f33-116">通过开启**预览功能**设置，即对组织中该环境的所有用户启用了预览功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-116">By turning on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="71f33-117">通过关闭此设置，即禁用了预览功能，并且您的用户不能访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-117">By turning off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="71f33-118">在 Talent 中，对预览功能的支持受限。</span><span class="sxs-lookup"><span data-stu-id="71f33-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="71f33-119">预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议中不涵盖预览功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement.</span></span> <span data-ttu-id="71f33-120">不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。</span><span class="sxs-lookup"><span data-stu-id="71f33-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="enable-or-disable-preview-features-for-your-organization"></a><span data-ttu-id="71f33-121">为组织启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="71f33-121">Enable or disable preview features for your organization</span></span>

#### <a name="attract"></a><span data-ttu-id="71f33-122">Attract</span><span class="sxs-lookup"><span data-stu-id="71f33-122">Attract</span></span>

1. <span data-ttu-id="71f33-123">登录 Microsoft Dynamics 365 for Talent: Attract。</span><span class="sxs-lookup"><span data-stu-id="71f33-123">Sign in to Microsoft Dynamics 365 for Talent: Attract.</span></span>
2. <span data-ttu-id="71f33-124">在右上角的**设置**菜单（齿轮符号）中，选择**管理员设置**。</span><span class="sxs-lookup"><span data-stu-id="71f33-124">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin settings**.</span></span>
3. <span data-ttu-id="71f33-125">在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色。</span><span class="sxs-lookup"><span data-stu-id="71f33-125">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue.</span></span>
4. <span data-ttu-id="71f33-126">刷新浏览器以开始查看新功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-126">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="71f33-127">（所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。）</span><span class="sxs-lookup"><span data-stu-id="71f33-127">(Any users who are already signed in will see the features the next time that they sign in, or they can refresh their browser to see the features immediately.)</span></span>

#### <a name="core-hr"></a><span data-ttu-id="71f33-128">Core HR</span><span class="sxs-lookup"><span data-stu-id="71f33-128">Core HR</span></span>

1. <span data-ttu-id="71f33-129">登录 Talent。</span><span class="sxs-lookup"><span data-stu-id="71f33-129">Sign in to Talent.</span></span> <span data-ttu-id="71f33-130">将打开“核心人力资源”工作区，可在其中完成其余步骤。</span><span class="sxs-lookup"><span data-stu-id="71f33-130">The core Human resources workspace will open, from which you'll complete the remaining steps.</span></span> 
2. <span data-ttu-id="71f33-131">选择**系统管理 \> 链接系统参数**。</span><span class="sxs-lookup"><span data-stu-id="71f33-131">Select **System administration \> Links System parameters**.</span></span>
3. <span data-ttu-id="71f33-132">在**系统参数**页**预览功能**选项卡上，将**为所有用户启用预览模式**选项设置为**是**，以便启用预览功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-132">On the **System Parameters page**, on the **Preview features** tab, set the **Enable preview mode for all users** option to **Yes** to make preview features available.</span></span>

> [!NOTE]
> <span data-ttu-id="71f33-133">若要禁用预览功能，请使用相同的基本步骤。</span><span class="sxs-lookup"><span data-stu-id="71f33-133">To disable preview features, use the same basic steps.</span></span> <span data-ttu-id="71f33-134">禁用后，您的用户不能访问预览功能，并且预览功能的相关流程中可能出错。</span><span class="sxs-lookup"><span data-stu-id="71f33-134">When you disable preview features, they become inaccessible to your users, and errors might occur in processes that are associated with the features.</span></span>

## <a name="features-that-are-currently-in-preview"></a><span data-ttu-id="71f33-135">当前的预览功能</span><span class="sxs-lookup"><span data-stu-id="71f33-135">Features that are currently in preview</span></span>

### <a name="attract"></a><span data-ttu-id="71f33-136">Attract</span><span class="sxs-lookup"><span data-stu-id="71f33-136">Attract</span></span>

- <span data-ttu-id="71f33-137">**工作模板** – 现在可以创建聘用流程模板。</span><span class="sxs-lookup"><span data-stu-id="71f33-137">**Job templates** – You can now create hiring process templates.</span></span> <span data-ttu-id="71f33-138">用户已经可以自定义特定工作的聘用流程。</span><span class="sxs-lookup"><span data-stu-id="71f33-138">Users can already customize the hiring process for a specific job.</span></span> <span data-ttu-id="71f33-139">但是，现在则可以为该流程创建模板，然后在创建特定工作时选择相应模板。</span><span class="sxs-lookup"><span data-stu-id="71f33-139">However, they can now create templates for the process and then select the appropriate template when a specific job is created.</span></span> <span data-ttu-id="71f33-140">因此，此功能可帮助简化工作设置流程。</span><span class="sxs-lookup"><span data-stu-id="71f33-140">Therefore, this feature helps streamline the job setup process.</span></span>
- <span data-ttu-id="71f33-141">**求职站点** – 现在的求职站点版本仅列举所有开放工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-141">**Career site** – The current version of the career site just lists all open jobs.</span></span> <span data-ttu-id="71f33-142">但是，以后将向该站点添加更多功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-142">However, more capabilities will be added to the site in the future.</span></span> <span data-ttu-id="71f33-143">可以将工作标记为内部或外部。</span><span class="sxs-lookup"><span data-stu-id="71f33-143">Jobs can be marked as either internal or external.</span></span> <span data-ttu-id="71f33-144">登录该站点的内部用户将看到内部工作和外部工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-144">Internal users who sign in to the site will see both internal jobs and external jobs.</span></span> <span data-ttu-id="71f33-145">但是，非内部用户和未登录用户只能查看外部工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-145">However, non-internal users and users who aren't signed in will see only external jobs.</span></span>
- <span data-ttu-id="71f33-146">**工作发布** – 现在可向求职站点发布工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-146">**Job posting** – You can now post jobs to the career site.</span></span>
- <span data-ttu-id="71f33-147">**LinkedIn 工作发布** – 现在可向 LinkedIn 发布工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-147">**LinkedIn job posting** – You can now post jobs to LinkedIn.</span></span>

    > [!NOTE]
    > <span data-ttu-id="71f33-148">只有订阅了一个或多个 LinkedIn 工作清单产品的客户才可查看发布的工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-148">Jobs that are posted are visible only to customers who subscribe to one or more LinkedIn job listing products.</span></span> <span data-ttu-id="71f33-149">否则，客户只有明确搜索某个工作，才能看到该工作。</span><span class="sxs-lookup"><span data-stu-id="71f33-149">Otherwise, customers see a job only if they explicitly search for it.</span></span> <span data-ttu-id="71f33-150">工作发布到 LinkedIn 时，存在延迟。</span><span class="sxs-lookup"><span data-stu-id="71f33-150">There is a delay when jobs are posted to LinkedIn.</span></span> <span data-ttu-id="71f33-151">工作从 Attract 发布后，可能需要几小时才会显示。</span><span class="sxs-lookup"><span data-stu-id="71f33-151">A job might take up to a few hours to appear after it's posted from Attract.</span></span>

- <span data-ttu-id="71f33-152">**候选人申请** – 内部候选人和外部候选人现在都可以直接从求职站点的工作页申请。</span><span class="sxs-lookup"><span data-stu-id="71f33-152">**Candidate apply** – Both internal and external candidates can now apply directly from the job page on the career site.</span></span>
- <span data-ttu-id="71f33-153">**评估** – 在可配置聘用流程中，不论是针对具体工作还是使用工作模板，用户现在都可以访问新的**评估**活动类型。</span><span class="sxs-lookup"><span data-stu-id="71f33-153">**Assessments** – As part of the configurable hiring process, either for a specific a job or when a job template is used, users now have access to a new **Assessment** activity type.</span></span> <span data-ttu-id="71f33-154">用户可以使用 Talent 中的“项目: Gauge”应用程序创建可发给候选人的基本评估。</span><span class="sxs-lookup"><span data-stu-id="71f33-154">They can then use the Project: "Gauge" app in Talent to build basic assessments that they can send to candidates.</span></span> <span data-ttu-id="71f33-155">“项目: Gauge”也处于公开预览状态。</span><span class="sxs-lookup"><span data-stu-id="71f33-155">Project: "Gauge" is also in public preview.</span></span> <span data-ttu-id="71f33-156">将来会增加更多提供程序。</span><span class="sxs-lookup"><span data-stu-id="71f33-156">Additional providers will be added in the future.</span></span>
- <span data-ttu-id="71f33-157">**项目: Gauge** –“项目: Gauge”是 Talent 中的一个应用程序，用于供用户创建简单评估或调查。</span><span class="sxs-lookup"><span data-stu-id="71f33-157">**Project: "Gauge"** – Project: "Gauge" is an app in Talent that lets users create simple assessments or surveys.</span></span>
- <span data-ttu-id="71f33-158">**聘约管理** – 用户现在可通过包含占位符的模板创建录用信。</span><span class="sxs-lookup"><span data-stu-id="71f33-158">**Offer management** – Users can now create offer letters from templates that include placeholders.</span></span> <span data-ttu-id="71f33-159">在候选人推进到聘约阶段，招聘人员和和招聘经理可使用录用工具通过模板准备候选人的正式聘约，发送聘约供内部批准，最后将聘约发给候选人签署。</span><span class="sxs-lookup"><span data-stu-id="71f33-159">As candidates advance to the Offer stage, recruiters and hiring managers can use the Offer tool to prepare a candidate's formal offer via templates, send the offer for internal approval, and finally send the offer to the candidate for signature.</span></span> <span data-ttu-id="71f33-160">将随时间向聘约工具增加大量新功能，而在我们准备好发布这些功能供预览时，将使用这些功能更新以前的功能。</span><span class="sxs-lookup"><span data-stu-id="71f33-160">Many new capabilities will be added to the Offer tool over time, and the preview feature will be updated with these capabilities as we are ready to release them to preview.</span></span>

### <a name="core-hr"></a><span data-ttu-id="71f33-161">Core HR</span><span class="sxs-lookup"><span data-stu-id="71f33-161">Core HR</span></span>

- <span data-ttu-id="71f33-162">**开放登记** – 福利开放登记让员工可以在选择福利时获得简单的自助式体验。</span><span class="sxs-lookup"><span data-stu-id="71f33-162">**Open Enrollment** – Benefits open enrollment gives employees a simple, self-service experience for selecting their benefits.</span></span> <span data-ttu-id="71f33-163">人力资源 (HR) 管理员可使用易于使用的引导式解决方案针对组织和针对员工的登记体验配置福利开放登记流程。</span><span class="sxs-lookup"><span data-stu-id="71f33-163">Human Resource (HR) administrators can configure the benefits open enrollment process for their organization, and the enrollment experience for employees, by using an easy-to-follow guided solution.</span></span>

## <a name="feedback"></a><span data-ttu-id="71f33-164">反馈</span><span class="sxs-lookup"><span data-stu-id="71f33-164">Feedback</span></span>

<span data-ttu-id="71f33-165">无论反馈正面还是负面，我们都希望倾听您对使用预览功能的看法。</span><span class="sxs-lookup"><span data-stu-id="71f33-165">Regardless of whether the feedback is positive or negative, we want to hear from you about your use of the preview features.</span></span> <span data-ttu-id="71f33-166">希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈。</span><span class="sxs-lookup"><span data-stu-id="71f33-166">We encourage you to regularly post your feedback on the following sites as you use these or any other features.</span></span>

- <span data-ttu-id="71f33-167">[社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。</span><span class="sxs-lookup"><span data-stu-id="71f33-167">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="71f33-168">可使用以下站点提供产品观点方面的建议。</span><span class="sxs-lookup"><span data-stu-id="71f33-168">Use the following sites to suggest product ideas.</span></span> <span data-ttu-id="71f33-169">告知我们您希望在产品中看到的功能，以及您认为应对现有功能进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="71f33-169">Let us know about features that you want to see in the product, and also any changes that you think should be made to existing features.</span></span>

    - [<span data-ttu-id="71f33-170">Attract 观点</span><span class="sxs-lookup"><span data-stu-id="71f33-170">Attract Ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="71f33-171">Core HR</span><span class="sxs-lookup"><span data-stu-id="71f33-171">Core HR</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

<span data-ttu-id="71f33-172">请勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。</span><span class="sxs-lookup"><span data-stu-id="71f33-172">Don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="71f33-173">可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。</span><span class="sxs-lookup"><span data-stu-id="71f33-173">Information that is collected might be analyzed further, and it won't be used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="71f33-174">在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/en-us/privacystatement)。</span><span class="sxs-lookup"><span data-stu-id="71f33-174">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="71f33-175">将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。</span><span class="sxs-lookup"><span data-stu-id="71f33-175">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

