---
title: 访问 Microsoft Dynamics 365 for Talent 中的预览功能
description: 此主题介绍管理员可如何启用 Microsoft Dynamics 365 for Talent 中的预览功能，并且列出了当前可预览的功能。
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
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
ms.openlocfilehash: 6a5aa8d6ea72ec3d3910edea291c4340ab607326
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739579"
---
# <a name="manage-preview-features"></a><span data-ttu-id="5f5a6-103">管理预览功能</span><span class="sxs-lookup"><span data-stu-id="5f5a6-103">Manage preview features</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f5a6-104">在持续推出适用于 Microsoft Dynamics 365 for Talent 的人力资本管理 (HCM) 功能时，我们希望让客户尽快体验新功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 for Talent, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="5f5a6-105">管理员可以在自己的环境中查看和使用预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="5f5a6-106">这些功能几乎已针对普通使用准备就绪，并经过了大量测试。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="5f5a6-107">我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="5f5a6-108">此主题介绍如何启用预览功能，并且列出了当前可预览的功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="5f5a6-109">发布功能以公开推出和发布新功能以预览时，将更新此列表。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="5f5a6-110">发布新功能以预览时，不提供通知。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="5f5a6-111">用户只需启动即可查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-111">Users will just start to see the features.</span></span> <span data-ttu-id="5f5a6-112">有关 Talent 中的新功能的详细信息，请参阅 [Dynamics 365 for Talent 新增功能或更改](./whats-new.md)和 [Dynamics 365 和 Power Platform 发行说明](https://docs.microsoft.com/business-applications-release-notes)。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 for Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="5f5a6-113">启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="5f5a6-113">Enable or disable preview features</span></span>

<span data-ttu-id="5f5a6-114">若要访问预览功能，必须首先在您的环境中启用。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="5f5a6-115">预览功能的启用或禁用特定于环境。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f5a6-116">开启**预览功能**设置时，即对组织中该环境的所有用户启用了预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="5f5a6-117">关闭此设置时，即禁用了预览功能，并且您的用户不能访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="5f5a6-118">在 Talent 中，对预览功能的支持受限。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="5f5a6-119">预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议 (SLA) 中不涵盖预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="5f5a6-120">不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="5f5a6-121">吸引</span><span class="sxs-lookup"><span data-stu-id="5f5a6-121">Attract</span></span>

1. <span data-ttu-id="5f5a6-122">登录到 Microsoft Dynamics 365 for Talent: Attract。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-122">Sign in to Microsoft Dynamics 365 for Talent: Attract.</span></span>
2. <span data-ttu-id="5f5a6-123">在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="5f5a6-124">在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色，然后说出**打开**。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![启用 Attract 中的预览功能](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="5f5a6-126">选择或取消单个预览功能的选择。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="5f5a6-127">如果不执行任何操作，则启用所有可用预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="5f5a6-128">刷新浏览器以开始查看新功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="5f5a6-129">所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="5f5a6-130">可能需要为某些预览功能执行更多配置。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="5f5a6-131">单击预览功能旁边的链接完成该功能的设置。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

### <a name="core-hr"></a><span data-ttu-id="5f5a6-132">Core HR</span><span class="sxs-lookup"><span data-stu-id="5f5a6-132">Core HR</span></span>

1. <span data-ttu-id="5f5a6-133">登录 Talent。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-133">Sign in to Talent.</span></span>
2. <span data-ttu-id="5f5a6-134">选择 **系统管理**，然后选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-134">Select **System administration**, and then select the **Links** tab.</span></span>
3. <span data-ttu-id="5f5a6-135">在**系统管理**页中的**设置**下，选择**系统参数**。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-135">On the **System administration** page, under **Setup**, select **System parameters**.</span></span>
4. <span data-ttu-id="5f5a6-136">在**系统参数**页中，选择**预览功能**选项卡。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-136">On the **System parameters** page, select the **Preview features** tab.</span></span>
5. <span data-ttu-id="5f5a6-137">将**为所有用户启用预览模式**选项设置为**是**以启用预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-137">Set the **Enable preview mode for all users** option to **Yes** to make preview features available.</span></span>

    ![启用 Core HR 中的预览功能](./media/corehr-enable-preview-features.png)

> [!NOTE]
> <span data-ttu-id="5f5a6-139">要禁用预览功能，请执行相同步骤，但将**为所有用户启用预览模式**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-139">To disable preview features, use the same steps, but set the **Enable preview mode for all users** option to **No**.</span></span> <span data-ttu-id="5f5a6-140">禁用后，您的用户不能访问预览功能，并且预览功能的相关流程中可能出错。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-140">When you disable preview features, they become inaccessible to your users, and errors might occur in processes that are associated with the features.</span></span>

### <a name="onboard"></a><span data-ttu-id="5f5a6-141">入职</span><span class="sxs-lookup"><span data-stu-id="5f5a6-141">Onboard</span></span>

<span data-ttu-id="5f5a6-142">Microsoft Dynamics 365 for Talent: Onboard 当前无预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-142">No preview features are currently available for Microsoft Dynamics 365 for Talent: Onboard.</span></span>

## <a name="features-that-are-currently-in-preview"></a><span data-ttu-id="5f5a6-143">当前的预览功能</span><span class="sxs-lookup"><span data-stu-id="5f5a6-143">Features that are currently in preview</span></span>

### <a name="attract"></a><span data-ttu-id="5f5a6-144">吸引</span><span class="sxs-lookup"><span data-stu-id="5f5a6-144">Attract</span></span>

- <span data-ttu-id="5f5a6-145">[应聘者推荐](./intelligent-recommendations.md#candidate-recommendations) - 如果有超过十名应聘者有简历或完整的个人资料，与工作要求最接近的应聘者将显示在“工作”页的**要考虑的申请人**部分。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-145">[Candidate recommendation](./intelligent-recommendations.md#candidate-recommendations) – If more than ten candidates have resumes or complete profiles, the candidates who most closely meet a job's requirements appear in the **Applicants to consider** section on that job's page.</span></span>
- <span data-ttu-id="5f5a6-146">[工作推荐](./intelligent-recommendations.md#job-recommendations) - 如果您的求职站点上发布的工作超过十个，Attract 将为应聘者提供工作推荐。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-146">[Job recommendation](./intelligent-recommendations.md#job-recommendations) – If more than ten jobs are posted on your career site, Attract provides job recommendations to prospects.</span></span>
- <span data-ttu-id="5f5a6-147">[Broadbean 集成](./posting-jobs-external.md#post-jobs-to-broadbean) – 可将工作从 Attract 发布到 Broadbean，后者是一个外部工作发布站点。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-147">[Broadbean integration](./posting-jobs-external.md#post-jobs-to-broadbean) – You can post jobs from Attract to Broadbean, an external job posting site.</span></span> <span data-ttu-id="5f5a6-148">启用此预览功能后，您必须通过输入您的 Broadbean 用户名、客户 ID 和加密标记来完成安装。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-148">After you enable this preview feature, you must complete the setup by entering your Broadbean username, client ID, and encryption token.</span></span>
- <span data-ttu-id="5f5a6-149">[分析](./analytic-reports.md) - 在分析中心中，招聘团队可以查看单个工作的关键指标，以及所有工作的聚合指标。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-149">[Analytics](./analytic-reports.md) – In the Analytics Hub, hiring teams can view key metrics for a single job, plus aggregated metrics across all jobs.</span></span>
- <span data-ttu-id="5f5a6-150">[EEO](./activities-attract.md) – 可通过新活动类型使用预定义的窗体从应聘者处收集平等就业机会 (EEO) 和联邦合同合规性计划办公室 (OFCCP) 数据。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-150">[EEO](./activities-attract.md) – New activity types let you use a predefined form to collect Equal Employment Opportunity (EEO) and Office of Federal Contract Compliance Program (OFCCP) data from a candidate.</span></span> <span data-ttu-id="5f5a6-151">不能编辑预定义的窗体。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-151">The predefined form can't be edited.</span></span>
- <span data-ttu-id="5f5a6-152">[应聘者建议](./intelligent-recommendations.md#prospect-recommendations) – Attract 可以检查过去的申请人和当前应聘者，以便提供非常适合您的工作的应聘者列表。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-152">[Prospect recommendation](./intelligent-recommendations.md#prospect-recommendations) – Attract reviews past applicants and current candidates to provide a list of prospects who are a good match for your job.</span></span>
- <span data-ttu-id="5f5a6-153">[相关性搜索](./attract-talent-pools.md#search-and-view-candidate-profiles) – 可搜索整个应聘者数据库以查找特定技能、姓名或教育背景。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-153">[Relevance search](./attract-talent-pools.md#search-and-view-candidate-profiles) – You can search your whole candidate database for specific skills, names, or educational backgrounds.</span></span> <span data-ttu-id="5f5a6-154">Attract 搜索整个个人资料并突出显示找到的所有匹配项。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-154">Attract searches the whole profile and highlights all the matches that it finds.</span></span> <span data-ttu-id="5f5a6-155">Attract 还搜索应聘者的所有可用文档并为搜索结果智能分级。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-155">Attract also searches all documents that are available for a candidate and intelligently ranks the search results.</span></span>
- <span data-ttu-id="5f5a6-156">[活动受众](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – 可将活动（如面试、计划或反馈）的受众设置为**所有应聘者**、**内部应聘者**或**外部应聘者**。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-156">[Activity audience](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – You can set the audience for activities (such as Interview, Schedule, or Feedback) to **All candidates**, **Internal candidates**, or **External candidates**.</span></span> <span data-ttu-id="5f5a6-157">可以将客户活动（如 YouTube 视频、Web 内容和 Microsoft 窗体）交付给所有应聘者、仅内部应聘者、仅外部应聘者或招聘团队。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-157">You can deliver customer activities, such as YouTube videos, web content, and Microsoft Forms, to all candidates, internal candidates only, external candidates only, or the hiring team.</span></span>
- <span data-ttu-id="5f5a6-158">[通过 LinkedIn 申请](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – 可在 Attract 求职站点上设置选项，以便让工作应聘者使用 LinkedIn 申请。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-158">[Apply with LinkedIn](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – You can set up an option on your Attract career site to let job candidates apply by using LinkedIn.</span></span> <span data-ttu-id="5f5a6-159">此功能可以简化应聘者的申请流程，方法是让应聘者使用自己的 LinkedIn 个人资料在您的求职站点上自动填写申请表。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-159">This feature streamlines the application process for your candidates by letting them use their LinkedIn profile to automatically fill in their applications on your career site.</span></span>
- <span data-ttu-id="5f5a6-160">[来源跟踪](./source-tracking.md) – Attract 跟踪应聘者申请表的来源，以便提供宝贵信息，帮助您有针对性地开展招聘工作。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-160">[Source tracking](./source-tracking.md) – Attract tracks the source of candidate applications to provide valuable information that can help you target your recruiting efforts.</span></span> <span data-ttu-id="5f5a6-161">您也可以在向工作或人才池添加应聘者时选择申请来源。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-161">You can also select an application source when you're adding a candidate to a job or talent pool.</span></span>
- <span data-ttu-id="5f5a6-162">[银奖获得者](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – 如果任何应聘者非常适合您的组织，但是您曾经不能为其提供当前职位的延伸聘约，则可将其指定为银奖获得者。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-162">[Silver medalist](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – If any candidates are a great fit for your organization, but you didn't extend an offer to them for your current position, you can designate them as silver medalists.</span></span> <span data-ttu-id="5f5a6-163">在您下次有类似职位时，此功能可帮助缩短您的招聘时间。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-163">This feature helps reduce your time to hire the next time you have a similar position available.</span></span>

### <a name="core-hr"></a><span data-ttu-id="5f5a6-164">Core HR</span><span class="sxs-lookup"><span data-stu-id="5f5a6-164">Core HR</span></span>

- <span data-ttu-id="5f5a6-165">[验证职位层次结构数据](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – 您可以验证管理层次结构，以查找无意中导入的任何循环引用。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-165">[Validate position hierarchy data](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – You can validate the managerial hierarchy for any circular references that were inadvertently imported.</span></span>
- <span data-ttu-id="5f5a6-166">[指定休假类型的原因代码](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – 您可为休假类型指定原因代码。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-166">[Specify reason codes on leave types](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – You can specify reason codes for leave types.</span></span>
- <span data-ttu-id="5f5a6-167">[休假请求需要原因代码](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – 除了指定休假类型的原因代码之外，您还可以要求为休假请求提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-167">[Require reason codes on time-off requests](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – In addition to specifying reason codes for leave types, you can require reason codes for time-off requests.</span></span>
- <span data-ttu-id="5f5a6-168">[为 HR 提供休假和缺勤交易记录列表](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – 您可以查看休假和缺勤交易的列表，以便帮助提供对休假余额的见解。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-168">[Provide a leave and absence transaction list for HR](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – You can view a list of leave and absence transactions to help provide insights into time-off balances.</span></span>

### <a name="onboard"></a><span data-ttu-id="5f5a6-169">入职</span><span class="sxs-lookup"><span data-stu-id="5f5a6-169">Onboard</span></span>

<span data-ttu-id="5f5a6-170">Onboard 当前无预览功能。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-170">No preview features are currently available for Onboard.</span></span>

## <a name="feedback"></a><span data-ttu-id="5f5a6-171">反馈</span><span class="sxs-lookup"><span data-stu-id="5f5a6-171">Feedback</span></span>

<span data-ttu-id="5f5a6-172">希望您提供有关以上任何预览功能的体验信息。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-172">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="5f5a6-173">希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈：</span><span class="sxs-lookup"><span data-stu-id="5f5a6-173">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="5f5a6-174">[社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-174">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="5f5a6-175">告知我们您希望在产品中看到的功能，或您认为我们应对现有功能进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-175">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="5f5a6-176">请在以下站点提供产品观点方面的建议：</span><span class="sxs-lookup"><span data-stu-id="5f5a6-176">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="5f5a6-177">Attract 观点</span><span class="sxs-lookup"><span data-stu-id="5f5a6-177">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="5f5a6-178">Core HR 观点</span><span class="sxs-lookup"><span data-stu-id="5f5a6-178">Core HR ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [<span data-ttu-id="5f5a6-179">Onboard 观点</span><span class="sxs-lookup"><span data-stu-id="5f5a6-179">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="5f5a6-180">切勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-180">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="5f5a6-181">可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-181">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="5f5a6-182">在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-182">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="5f5a6-183">将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。</span><span class="sxs-lookup"><span data-stu-id="5f5a6-183">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f5a6-184">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f5a6-184">See also</span></span>

- [<span data-ttu-id="5f5a6-185">试用或购买 Talent 应用</span><span class="sxs-lookup"><span data-stu-id="5f5a6-185">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="5f5a6-186">新增功能</span><span class="sxs-lookup"><span data-stu-id="5f5a6-186">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="5f5a6-187">版本说明</span><span class="sxs-lookup"><span data-stu-id="5f5a6-187">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="5f5a6-188">获取 Talent 支持</span><span class="sxs-lookup"><span data-stu-id="5f5a6-188">Get support for Talent</span></span>](./talent-support.md)
