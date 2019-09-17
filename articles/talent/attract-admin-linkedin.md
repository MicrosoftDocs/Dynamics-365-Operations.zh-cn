---
title: 为 Microsoft Dynamics 365 for Talent - Attract 设置与 LinkedIn 的集成
description: 本主题说明如何为 Microsoft Dynamics 365 for Talent - Attract 配置 LinkedIn 集成，以便您可以轻松地将工作从 Attract 发布到 LinkedIn，并让您的招聘人员可以将他们的招聘信息与应聘者的 LinkedIn 个人资料同步。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8e42ec7d0bb74089b4e915b5a30277401e694cf9
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756214"
---
# <a name="set-up-linkedin-integration"></a><span data-ttu-id="747df-103">设置 LinkedIn 集成</span><span class="sxs-lookup"><span data-stu-id="747df-103">Set up LinkedIn integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="747df-104">通过配置与 Microsoft Dynamics 365 for Talent: Attract 的 LinkedIn 集成，帮助您的招聘人员和招聘经理吸引顶尖人才。</span><span class="sxs-lookup"><span data-stu-id="747df-104">Help your recruiters and hiring managers attract top talent by configuring LinkedIn integration with Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="747df-105">通过 Attract，您可以将工作直接发布到最大的在线职业网站 LinkedIn。</span><span class="sxs-lookup"><span data-stu-id="747df-105">Attract lets you post jobs directly to LinkedIn, the largest professional online network.</span></span>

<span data-ttu-id="747df-106">您通过 Attract 发布到 LinkedIn 的工作属于 Limited Listings（有限列表），您的公司无需支付额外费用。</span><span class="sxs-lookup"><span data-stu-id="747df-106">Jobs that you post to LinkedIn through Attract are Limited Listings and are provided at no extra cost to your company.</span></span> <span data-ttu-id="747df-107">这些列表仅通过 LinkedIn 软件合作伙伴（如 Attract）提供。</span><span class="sxs-lookup"><span data-stu-id="747df-107">These listings are available only through LinkedIn software partners such as Attract.</span></span> <span data-ttu-id="747df-108">它们不会出现在您公司的 LinkedIn 页面的**求职**面板中，因为只有付费列表出现在那里。</span><span class="sxs-lookup"><span data-stu-id="747df-108">They don't appear in the **Careers** panel on your company's LinkedIn page, because only paid listings appear there.</span></span> <span data-ttu-id="747df-109">但会在潜在应聘者查看所有可申请工作时显示。</span><span class="sxs-lookup"><span data-stu-id="747df-109">However, they are shown when potential candidates view all available jobs.</span></span> <span data-ttu-id="747df-110">Limited Listings（有限列表）还显示在 LinkedIn 工作搜索中。</span><span class="sxs-lookup"><span data-stu-id="747df-110">Limited Listings are also shown in LinkedIn job searches.</span></span>

<span data-ttu-id="747df-111">Attract 提供了两种与 LinkedIn 集成的方式，以帮助您从这个受欢迎的职业网站中找到应聘者：</span><span class="sxs-lookup"><span data-stu-id="747df-111">Attract provides two ways to integrate with LinkedIn to help you source candidates from this popular career site:</span></span>

- <span data-ttu-id="747df-112">将工作从 Attract 发布到 LinkedIn。</span><span class="sxs-lookup"><span data-stu-id="747df-112">Post jobs from Attract to LinkedIn.</span></span>
- <span data-ttu-id="747df-113">从 LinkedIn 为 Attract 寻求应聘者。</span><span class="sxs-lookup"><span data-stu-id="747df-113">Source candidates from LinkedIn to Attract.</span></span>

<span data-ttu-id="747df-114">您可以在“管理中心”的 **LinkedIn 集成**选项卡上配置这两个选项。</span><span class="sxs-lookup"><span data-stu-id="747df-114">You configure both options on the **LinkedIn Integration** tab in the Admin center.</span></span> <span data-ttu-id="747df-115">要打开“管理中心”，请转到 <https://attract.talent.dynamics.com/adminsettings>。</span><span class="sxs-lookup"><span data-stu-id="747df-115">To open the Admin center, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>

> [!NOTE]
> <span data-ttu-id="747df-116">要使用 Attract 的 LinkedIn Recruiter 集成，您需要[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)和 [LinkedIn Recruiter 许可证](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18)。</span><span class="sxs-lookup"><span data-stu-id="747df-116">To use LinkedIn Recruiter integration with Attract, you need the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) and [LinkedIn Recruiter licenses](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18).</span></span> <span data-ttu-id="747df-117">有关详细信息，请参阅[哪个 Attract 版本？](./attract-comprehensive-hiring.md)。</span><span class="sxs-lookup"><span data-stu-id="747df-117">For more information, see [Which version of Attract?](./attract-comprehensive-hiring.md).</span></span>

<span data-ttu-id="747df-118">如果您在向 LinkedIn 发布工作时遇到问题，请参阅 [LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)。</span><span class="sxs-lookup"><span data-stu-id="747df-118">If you're having trouble posting jobs to LinkedIn, see [Troubleshoot integration with LinkedIn](./attract-troubleshoot-linkedin.md).</span></span>

<span data-ttu-id="747df-119">有关将工作发布到 LinkedIn 的其他方式的信息，请参阅 [LinkedIn 常见问题](./attract-linkedin-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="747df-119">For information about other ways to post jobs to LinkedIn, see [LinkedIn FAQ](./attract-linkedin-faq.md).</span></span>

## <a name="configure-job-posting-to-linkedin"></a><span data-ttu-id="747df-120">配置 LinkedIn 工作发布</span><span class="sxs-lookup"><span data-stu-id="747df-120">Configure job posting to LinkedIn</span></span>

<span data-ttu-id="747df-121">您需要一个 [LinkedIn 公司 ID](https://aka.ms/findID)，然后才能将工作从 Attract 发布到 LinkedIn。</span><span class="sxs-lookup"><span data-stu-id="747df-121">Before you can post jobs from Attract to LinkedIn, you need a [LinkedIn Company ID](https://aka.ms/findID).</span></span> <span data-ttu-id="747df-122">您的 LinkedIn 公司 ID 是一串数字，用于在 LinkedIn 中唯一标识您的公司。</span><span class="sxs-lookup"><span data-stu-id="747df-122">Your LinkedIn Company ID is a string of numbers that uniquely identifies your company in LinkedIn.</span></span> <span data-ttu-id="747df-123">有关详细信息，请参阅[将您的 LinkedIn 公司 ID 与 LinkedIn Job Board 关联 - 常见问题](https://aka.ms/findID)。</span><span class="sxs-lookup"><span data-stu-id="747df-123">For more information, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://aka.ms/findID).</span></span>

<span data-ttu-id="747df-124">Attract 将您的工作发布源发送给 LinkedIn，LinkedIn 大约每天检查一次源。</span><span class="sxs-lookup"><span data-stu-id="747df-124">Attract sends a feed of your job postings to LinkedIn, and LinkedIn checks for the feed approximately once per day.</span></span> <span data-ttu-id="747df-125">您的工作最多可能需要 48 小时发布到网站上。</span><span class="sxs-lookup"><span data-stu-id="747df-125">It can take up to 48 hours for your jobs to be posted to the site.</span></span>

<span data-ttu-id="747df-126">发布到 LinkedIn 的工作将显示在实际的 LinkedIn 网站上。</span><span class="sxs-lookup"><span data-stu-id="747df-126">Jobs that are posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="747df-127">LinkedIn 没有发布工作的测试环境。</span><span class="sxs-lookup"><span data-stu-id="747df-127">LinkedIn doesn't have a test environment for posting jobs.</span></span> <span data-ttu-id="747df-128">因此，请确保您不会意外发布任何测试工作。</span><span class="sxs-lookup"><span data-stu-id="747df-128">Therefore, make sure that you don't accidentally post any test jobs.</span></span> 

1. <span data-ttu-id="747df-129">在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="747df-129">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="747df-130">或者，转到 <https://attract.talent.dynamics.com/adminsettings>。</span><span class="sxs-lookup"><span data-stu-id="747df-130">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="747df-131">选择 **LinkedIn 集成**选项卡。</span><span class="sxs-lookup"><span data-stu-id="747df-131">Select the **LinkedIn Integration** tab.</span></span>
3. <span data-ttu-id="747df-132">在**公司名称**下，输入您公司的名称，在**公司ID** 下，输入您的 LinkedIn 公司 ID。</span><span class="sxs-lookup"><span data-stu-id="747df-132">Under **Company name**, enter the name of your company, and under **Company ID**, enter your LinkedIn Company ID.</span></span> <span data-ttu-id="747df-133">确保公司名称与公司 LinkedIn 页面上显示的名称相匹配。</span><span class="sxs-lookup"><span data-stu-id="747df-133">Make sure that the company name matches the name that appears on your company's LinkedIn page.</span></span> <span data-ttu-id="747df-134">有关 LinkedIn 公司 ID 的详细信息，请参阅[将您的 LinkedIn 公司 ID 与 LinkedIn Job Board 关联 - 常见问题](https://www.linkedin.com/help/linkedin/answer/98972)。</span><span class="sxs-lookup"><span data-stu-id="747df-134">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>

    <span data-ttu-id="747df-135">如果您需要更改组织的任何信息，请参阅[更改组织的地址、技术联系人等](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more)。</span><span class="sxs-lookup"><span data-stu-id="747df-135">If you need to change any information for your organization, see [Change your organization's address, technical contact, and more](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more).</span></span> <span data-ttu-id="747df-136">如果您仍有问题，请联系 [LinkedIn 支持](https://www.linkedin.com/help/linkedin)。</span><span class="sxs-lookup"><span data-stu-id="747df-136">If you still have issues, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>

4. <span data-ttu-id="747df-137">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="747df-137">Select **Save**.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="747df-138">为 LinkedIn Recruiter 设置 Attract</span><span class="sxs-lookup"><span data-stu-id="747df-138">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="747df-139">要允许招聘人员通过 LinkedIn Recruiter 寻找工作，您必须在 Attract 中配置与 LinkedIn Recruiter 的集成。</span><span class="sxs-lookup"><span data-stu-id="747df-139">To allow recruiters to source jobs through LinkedIn Recruiter, you must configure integration with LinkedIn Recruiter in Attract.</span></span> <span data-ttu-id="747df-140">要完成配置过程，您必须与组织的 LinkedIn Recruiter 合同中的管理员用户合作。</span><span class="sxs-lookup"><span data-stu-id="747df-140">To complete the configuration process, you must work with the user who is an admin on your organization's LinkedIn Recruiter contract.</span></span>

1. <span data-ttu-id="747df-141">在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="747df-141">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="747df-142">或者，转到 <https://attract.talent.dynamics.com/adminsettings>。</span><span class="sxs-lookup"><span data-stu-id="747df-142">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="747df-143">选择 **LinkedIn 集成**选项卡。</span><span class="sxs-lookup"><span data-stu-id="747df-143">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="747df-144">[![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="747df-144">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="747df-145">选择**连接**开始设置。</span><span class="sxs-lookup"><span data-stu-id="747df-145">Select **Connect** to start the setup.</span></span> <span data-ttu-id="747df-146">您将被引导进入 LinkedIn 登录过程。</span><span class="sxs-lookup"><span data-stu-id="747df-146">You will be guided through the LinkedIn sign-in process.</span></span>
4. <span data-ttu-id="747df-147">如果您在多个 LinkedIn 合同中有席位，请选择要连接到 Attract 系统的合同。</span><span class="sxs-lookup"><span data-stu-id="747df-147">If you have seats on multiple LinkedIn contracts, select the contract that you want to connect to the Attract system.</span></span> <span data-ttu-id="747df-148">如果您只在一个 LinkedIn 合同中有席位，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="747df-148">If you have a seat on only one LinkedIn contract, you can skip this step.</span></span>
5. <span data-ttu-id="747df-149">在 **Recruiter System Connect (RSC)** 下，选择**请求**。</span><span class="sxs-lookup"><span data-stu-id="747df-149">Under **Recruiter System Connect (RSC)**, select **Request**.</span></span>

    <span data-ttu-id="747df-150">[![请求 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="747df-150">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6. <span data-ttu-id="747df-151">**Recruiter System Connect (RSC)** 设置现在应显示为**合作伙伴就绪**。</span><span class="sxs-lookup"><span data-stu-id="747df-151">The **Recruiter System Connect (RSC)** setting should now appear as **Partner ready**.</span></span> <span data-ttu-id="747df-152">如果您在此页面上看到**通知合作伙伴**，请等待几秒钟，选择**通知合作伙伴**，然后刷新页面。</span><span class="sxs-lookup"><span data-stu-id="747df-152">If you see **Notify partner** on this page, wait a few seconds, select **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="747df-153">设置现在应显示为**合作伙伴就绪**。</span><span class="sxs-lookup"><span data-stu-id="747df-153">The setting should now appear as **Partner ready**.</span></span>

    <span data-ttu-id="747df-154">[![指示请求的 Attract 端已完成的 Attract 视图](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="747df-154">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

7. <span data-ttu-id="747df-155">要完成以下步骤，您必须拥有 LinkedIn Recruiter 合同的管理员权限。</span><span class="sxs-lookup"><span data-stu-id="747df-155">To complete the following steps, you must have admin privileges on your LinkedIn Recruiter contract.</span></span>

    1. <span data-ttu-id="747df-156">使用您的管理员帐户登录 LinkedIn，然后在右上角选择 **LinkedIn Recruiter**。</span><span class="sxs-lookup"><span data-stu-id="747df-156">Sign in to LinkedIn by using your admin account, and then select **LinkedIn Recruiter** in the upper right.</span></span> 
    2. <span data-ttu-id="747df-157">在页面顶部的**更多**菜单中，选择**管理员设置**，然后选择 **ATS** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="747df-157">On the **More** menu at the top of the page, select **Admin Settings**, and then select the **ATS** tab.</span></span>
    3. <span data-ttu-id="747df-158">要只为一个合同启用一键导出，请启用**合同级别访问(此合同的每个席位)**。</span><span class="sxs-lookup"><span data-stu-id="747df-158">To enable one-click export for just one contract, turn on **Contract Level access (for every seat on this contract**.</span></span> <span data-ttu-id="747df-159">要为整个公司启用，请启用**公司级别访问(公司的每个合同)**。</span><span class="sxs-lookup"><span data-stu-id="747df-159">To enable it for the whole company, turn on **Company Level access (for every contract in your company**.</span></span>

    <span data-ttu-id="747df-160">[![从 LinkedIn Recruiter 管理员打开 Attract 集成的视图](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="747df-160">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

8. <span data-ttu-id="747df-161">在“Attract 管理中心”，选择 **LinkedIn集成**选项卡。**Recruiter System Connect (RSC)** 设置现在应显示为**已启用**。</span><span class="sxs-lookup"><span data-stu-id="747df-161">In the Attract Admin center, select the **LinkedIn integration** tab. The **Recruiter System Connect (RSC)** setting should now appear as **Enabled**.</span></span>

    <span data-ttu-id="747df-162">[![LinkedIn Recruiter 集成完成](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="747df-162">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="set-up-apply-with-linkedin-in-attract"></a><span data-ttu-id="747df-163">在 Attract 中设置“通过 LinkedIn 申请”</span><span class="sxs-lookup"><span data-stu-id="747df-163">Set up Apply with LinkedIn in Attract</span></span>

<span data-ttu-id="747df-164">您可以允许应聘者使用他们的 LinkedIn 个人资料申请您的工作。</span><span class="sxs-lookup"><span data-stu-id="747df-164">You can allow candidates to apply to your jobs by using their LinkedIn profiles.</span></span> <span data-ttu-id="747df-165">有关“通过 LinkedIn 申请”的详细信息，请参阅 [LinkedIn 的力量无处不在：通过 LinkedIn 申请](https://blog.linkedin.com/2011/07/24/apply-with-linkedin)。</span><span class="sxs-lookup"><span data-stu-id="747df-165">For more information about Apply with LinkedIn, see [The Power of LinkedIn Everywhere: Apply with LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).</span></span>

<span data-ttu-id="747df-166">此功能现在处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="747df-166">This feature is currently in preview.</span></span> <span data-ttu-id="747df-167">在执行这些步骤之前，请确保已启用“通过 LinkedIn 申请”。</span><span class="sxs-lookup"><span data-stu-id="747df-167">Before you follow these steps, make sure that Apply with LinkedIn is enabled.</span></span> <span data-ttu-id="747df-168">有关如何启用预览功能的详细信息，请参阅[访问 Talent 中的预览功能](./access-preview-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="747df-168">For more information about how to enable preview features, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

1. <span data-ttu-id="747df-169">在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="747df-169">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="747df-170">或者，转到 <https://attract.talent.dynamics.com/adminsettings>。</span><span class="sxs-lookup"><span data-stu-id="747df-170">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="747df-171">选择 **LinkedIn 集成**选项卡。</span><span class="sxs-lookup"><span data-stu-id="747df-171">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="747df-172">[![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="747df-172">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="747df-173">在**通过 LinkedIn 申请**旁边，选择**连接**开始设置。</span><span class="sxs-lookup"><span data-stu-id="747df-173">Next to **Apply with LinkedIn**, select **Connect** to start the setup.</span></span> <span data-ttu-id="747df-174">您将在引导下了解 LinkedIn 中此流程的其余部分。</span><span class="sxs-lookup"><span data-stu-id="747df-174">You will be guided through the rest of the process with LinkedIn.</span></span>

## <a name="see-also"></a><span data-ttu-id="747df-175">请参阅</span><span class="sxs-lookup"><span data-stu-id="747df-175">See also</span></span>

[<span data-ttu-id="747df-176">LinkedIn 常见问题</span><span class="sxs-lookup"><span data-stu-id="747df-176">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="747df-177">将工作从 Attract 发布到外部站点</span><span class="sxs-lookup"><span data-stu-id="747df-177">Post jobs to external sites from Attract</span></span>](./posting-jobs-external.md)

[<span data-ttu-id="747df-178">使用 LinkedIn Recruiter 寻求应聘者</span><span class="sxs-lookup"><span data-stu-id="747df-178">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="747df-179">创建工作</span><span class="sxs-lookup"><span data-stu-id="747df-179">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="747df-180">LinkedIn 集成疑难解答</span><span class="sxs-lookup"><span data-stu-id="747df-180">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
