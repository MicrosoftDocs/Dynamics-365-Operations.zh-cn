---
title: 在 Microsoft Dynamics 365 Talent - Attract 中设置求职站点
description: 本主题概述 Microsoft Dynamics 365 Talent - Attract 中面向应聘者的求职站点功能。
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: ec5fe31c6547b008b29e656729c35863d90bffc1
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026271"
---
# <a name="set-up-your-career-site"></a><span data-ttu-id="139ff-103">设置您的求职站点</span><span class="sxs-lookup"><span data-stu-id="139ff-103">Set up your career site</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="139ff-104">本主题概述了 Microsoft Dynamics 365 Talent: Attract 中面向应聘者的求职站点功能。</span><span class="sxs-lookup"><span data-stu-id="139ff-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="139ff-105">另外还介绍如何设置此功能。</span><span class="sxs-lookup"><span data-stu-id="139ff-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="139ff-106">Attract 为租户中的每个环境提供一个求职站点。</span><span class="sxs-lookup"><span data-stu-id="139ff-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="139ff-107">例如，如果组织具有开发环境和测试环境，一个求职站点为开发环境设置，另一个求职站点为测试环境设置。</span><span class="sxs-lookup"><span data-stu-id="139ff-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="139ff-108">各求职站点是完全隔离的，并且具有自己的身份验证机制。</span><span class="sxs-lookup"><span data-stu-id="139ff-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="139ff-109">工作和应聘者个人资料不在求职站点之间共享。</span><span class="sxs-lookup"><span data-stu-id="139ff-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="139ff-110">默认情况下，求职站点是公共的。</span><span class="sxs-lookup"><span data-stu-id="139ff-110">By default, the career site is public.</span></span> <span data-ttu-id="139ff-111">因此，应聘者可以查看标记为外部的所有工作，而不必登录。</span><span class="sxs-lookup"><span data-stu-id="139ff-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="139ff-112">但是，其他所有操作都需要应聘者登录。</span><span class="sxs-lookup"><span data-stu-id="139ff-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="139ff-113">求职站点管理</span><span class="sxs-lookup"><span data-stu-id="139ff-113">Career site management</span></span>

<span data-ttu-id="139ff-114">若要设置以下项，作为管理员登录到 Attract，在**设置**菜单（齿轮符号）上选择**管理员中心**，然后选择**公司信息**选项卡。</span><span class="sxs-lookup"><span data-stu-id="139ff-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="139ff-115">**组织名称** - 组织名称显示在求职站点顶部的导航栏中。</span><span class="sxs-lookup"><span data-stu-id="139ff-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="139ff-116">通过选择组织名称，应聘者可以转到列出所有空缺职位的页面。</span><span class="sxs-lookup"><span data-stu-id="139ff-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="139ff-117">**组织徽标** - 组织徽标的图像显示在求职站点的左上角。</span><span class="sxs-lookup"><span data-stu-id="139ff-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="139ff-118">通过选择徽标图像，应聘者可以转到列出所有空缺职位的页面。</span><span class="sxs-lookup"><span data-stu-id="139ff-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="139ff-119">显示在求职站点的徽标图像具有固定高度 20 像素 (px)。</span><span class="sxs-lookup"><span data-stu-id="139ff-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="139ff-120">在管理员中心添加的图像会缩放以适应此高度。</span><span class="sxs-lookup"><span data-stu-id="139ff-120">The image that you add in the Admin center is  scaled to fit.</span></span> <span data-ttu-id="139ff-121">因此，根据图像，宽度可能会变化。</span><span class="sxs-lookup"><span data-stu-id="139ff-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="139ff-122">若要设置以下项，作为管理员登录到 Attract，在**设置**菜单上选择**管理员中心**，然后选择**求职站点管理**选项卡。</span><span class="sxs-lookup"><span data-stu-id="139ff-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="139ff-123">**搜索引擎优化** - 如果启用，可使用 Bing 和 Google 之类搜索引擎搜索 Attract 求职站点中发布的所有公开职位。</span><span class="sxs-lookup"><span data-stu-id="139ff-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span> 

    > [!NOTE] 
    > <span data-ttu-id="139ff-124">开启此设置到搜索结果显示之间可能存在延迟，具体取决于所用搜索引擎。</span><span class="sxs-lookup"><span data-stu-id="139ff-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
    
-   <span data-ttu-id="139ff-125">**条款和条件** - 启用后，所有应聘者在申请任何工作时，都必须遵守组织的条款和条件。</span><span class="sxs-lookup"><span data-stu-id="139ff-125">**Terms and Conditions** - When enabled, all candidates must consent to the organization's terms and conditions when applying for any job.</span></span> <span data-ttu-id="139ff-126">Attract 管理员可配置自己的同意文本，以及其“条款和条件”页面的链接。</span><span class="sxs-lookup"><span data-stu-id="139ff-126">The Attract Administrator is able to configure their own Consent text as well as the link to their Terms and Conditions page.</span></span> 

        
## <a name="career-site-urls"></a><span data-ttu-id="139ff-127">求职站点 URL</span><span class="sxs-lookup"><span data-stu-id="139ff-127">Career site URLs</span></span>

<span data-ttu-id="139ff-128">以下列表中包含常用求职站点 URL 及其访问方法。</span><span class="sxs-lookup"><span data-stu-id="139ff-128">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="139ff-129">**求职站点主页 URL** - 若要查看求职站点主页 URL，请以管理员身份登录 Attract，选择**设置**菜单中的**管理员中心**，然后选择**求职站点管理**选项卡。</span><span class="sxs-lookup"><span data-stu-id="139ff-129">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="139ff-130">**单个工作发布申请 URL** - 在您首次[发布外部工作](Creating-jobs-Attract.md#postings)时，您可以从 Attract 复制**申请**链接。</span><span class="sxs-lookup"><span data-stu-id="139ff-130">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from Attract.</span></span> <span data-ttu-id="139ff-131">此链接的 URL 将使用以下格式：[https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="139ff-131">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="139ff-132">**单个工作发布 URL** - 充当“申请 URL”的子字符串的工作发布 URL。</span><span class="sxs-lookup"><span data-stu-id="139ff-132">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="139ff-133">它包含工作编号的所有内容。</span><span class="sxs-lookup"><span data-stu-id="139ff-133">It consists of everything up through the job number.</span></span> <span data-ttu-id="139ff-134">因此，对于前面的申请 URL，工作发布 URL 为 [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)。</span><span class="sxs-lookup"><span data-stu-id="139ff-134">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="139ff-135">身份验证选项</span><span class="sxs-lookup"><span data-stu-id="139ff-135">Authentication options</span></span>

<span data-ttu-id="139ff-136">应聘者具有以下 Attract 求职站点登录选项：</span><span class="sxs-lookup"><span data-stu-id="139ff-136">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="139ff-137">个人帐户：</span><span class="sxs-lookup"><span data-stu-id="139ff-137">Personal account:</span></span>

    -   <span data-ttu-id="139ff-138">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="139ff-138">LinkedIn</span></span>

    -   <span data-ttu-id="139ff-139">Microsoft</span><span class="sxs-lookup"><span data-stu-id="139ff-139">Microsoft</span></span>

    -   <span data-ttu-id="139ff-140">Google</span><span class="sxs-lookup"><span data-stu-id="139ff-140">Google</span></span>

    -   <span data-ttu-id="139ff-141">Facebook</span><span class="sxs-lookup"><span data-stu-id="139ff-141">Facebook</span></span>

-   <span data-ttu-id="139ff-142">工作或学校帐户：</span><span class="sxs-lookup"><span data-stu-id="139ff-142">Work or school account:</span></span>

    -   <span data-ttu-id="139ff-143">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="139ff-143">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="139ff-144">Azure AD 登录仅用于内部应聘者。</span><span class="sxs-lookup"><span data-stu-id="139ff-144">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="139ff-145">因此，它只对使用其公司 Azure AD 凭据的内部应聘者有效。</span><span class="sxs-lookup"><span data-stu-id="139ff-145">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="139ff-146">例如，当前是 Contoso Ltd 员工的应聘者希望申请一家不相关公司 Alpine Ski House 的工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-146">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="139ff-147">在这种情况下，如果员工尝试使用 Contoso Ltd 的 Azure AD 凭据，登录将不成功。</span><span class="sxs-lookup"><span data-stu-id="139ff-147">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span> 

<span data-ttu-id="139ff-148">如果应聘者查看或申请的工作列出为仅限内部，则应聘者必须使用 Azure AD 登录。</span><span class="sxs-lookup"><span data-stu-id="139ff-148">Candidates must sign in by using Azure AD if the job that they are viewing or applying for is listed as internal only.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="139ff-149">创建和维护个人资料</span><span class="sxs-lookup"><span data-stu-id="139ff-149">Create and maintain a profile</span></span>

<span data-ttu-id="139ff-150">在应聘者登录到求职站点后，他们可以在页面顶部的导航栏中选择**我的个人资料**来创建和维护其个人资料。</span><span class="sxs-lookup"><span data-stu-id="139ff-150">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="139ff-151">个人资料包括个人信息、工作经验相关信息、教育详细信息、文档、链接以及技能信息。</span><span class="sxs-lookup"><span data-stu-id="139ff-151">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="139ff-152">个人资料创建后，可用于申请应聘者感兴趣的工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-152">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="139ff-153">个人资料还可以帮助 Attract 向应聘者推荐合适的工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-153">Profiles also help Attract recommend the right jobs to candidates.</span></span>

> [!NOTE]
> <span data-ttu-id="139ff-154">如果应聘者使用电子邮件 ID 和上面列举的一个身份验证提供商登录，该电子邮件 ID 默认为与个人资料关联的联系人电子邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="139ff-154">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="139ff-155">但是，后者随时可更改，完全独立于前者。</span><span class="sxs-lookup"><span data-stu-id="139ff-155">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="139ff-156">Attract 将始终使用联系人电子邮件 ID 与您的个人资料关联来进行所有电子邮件通信。</span><span class="sxs-lookup"><span data-stu-id="139ff-156">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="139ff-157">查找合适的工作</span><span class="sxs-lookup"><span data-stu-id="139ff-157">Find the right job</span></span>

<span data-ttu-id="139ff-158">在工作列表页，应聘者可以通过输入搜索词搜索特定工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-158">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="139ff-159">搜索功能查找职务和工作描述中的搜索词，然后在结果中显示相关工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-159">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="139ff-160">应聘者可以随时基于工作位置或工作职能筛选结果。</span><span class="sxs-lookup"><span data-stu-id="139ff-160">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="139ff-161">应聘者还可以在求职站点上查看一组推荐的工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-161">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="139ff-162">向应聘者推荐的工作基于应聘者过去的申请、个人资料和简历。</span><span class="sxs-lookup"><span data-stu-id="139ff-162">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE] 
> <span data-ttu-id="139ff-163">仅当求职站点上至少发布了 10 个工作并且应聘者已经完成了个人资料时，工作推荐才会显示。</span><span class="sxs-lookup"><span data-stu-id="139ff-163">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

<span data-ttu-id="139ff-164">如果内部应聘者要联系招聘团队的成员，他们也可以查看工作的招聘经理和/或招聘人员是谁。</span><span class="sxs-lookup"><span data-stu-id="139ff-164">Internal candidates can also see who the hiring manager and/or recruiter for a job is, in case they want to contact those members of the hiring team.</span></span> <span data-ttu-id="139ff-165">而外部应聘者不能查看任何工作的招聘团队成员。</span><span class="sxs-lookup"><span data-stu-id="139ff-165">However, external candidates have no visibility into the members of the hiring team for any job.</span></span>

## <a name="contact-the-hiring-team"></a><span data-ttu-id="139ff-166">联系招聘团队</span><span class="sxs-lookup"><span data-stu-id="139ff-166">Contact the hiring team</span></span>
<span data-ttu-id="139ff-167">只有内部应聘者才能联系招聘团队。</span><span class="sxs-lookup"><span data-stu-id="139ff-167">Only internal candidates can contact the hiring team.</span></span> <span data-ttu-id="139ff-168">无论工作是仅限内部还是公开发布，此项限制都适用于所有工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-168">This limitation applies to all jobs, regardless of whether they are internal only or were publicly posted.</span></span>

<span data-ttu-id="139ff-169">应聘者可能希望联系招聘团队以表示对发布的工作感兴趣或了解更多相关信息。</span><span class="sxs-lookup"><span data-stu-id="139ff-169">Candidates might want to contact the hiring team to express interest in a job that was posted or learn more about it.</span></span> <span data-ttu-id="139ff-170">他们可以联系列出的任何招聘团队成员（招聘经理或招聘人员）。</span><span class="sxs-lookup"><span data-stu-id="139ff-170">They can contact any of the hiring team members who are listed (hiring manager or recruiters).</span></span> <span data-ttu-id="139ff-171">他们也可以选择在邮件中附上简历，或选择个人资料中以前上传的现有简历。</span><span class="sxs-lookup"><span data-stu-id="139ff-171">They can also optionally attach a resume to the message, or they can select an existing resume they previously uploaded as part of their profile.</span></span>

<span data-ttu-id="139ff-172">内部应聘者选择要联系的招聘团队成员之后，Attract 将代表应聘者向他们发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="139ff-172">After an internal candidate selects the hiring team members to contact, Attract sends an email to those people on the candidate's behalf.</span></span> <span data-ttu-id="139ff-173">同时，将把应聘者的个人资料添加到**潜在人选**阶段（如果工作支持此阶段）。</span><span class="sxs-lookup"><span data-stu-id="139ff-173">At the same time, the candidate's profile is added to the **Prospect** stage, if that stage is available for the job.</span></span> <span data-ttu-id="139ff-174">在**潜在人选**阶段，招聘人员或招聘经理可以查看与他们联系过的应聘者。</span><span class="sxs-lookup"><span data-stu-id="139ff-174">Under the **Prospect** stage, recruiters or hiring managers can view the candidates who have contacted them.</span></span> <span data-ttu-id="139ff-175">他们还可以查看应聘者个人资料和邀请潜在应聘者申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-175">They can also review candidate profiles and invite potential candidates to apply.</span></span>

<span data-ttu-id="139ff-176">应聘者可以申请自己已经联系招聘团队成员讨论的工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-176">Candidates can apply for a job that they have already contacted hiring team members about.</span></span> <span data-ttu-id="139ff-177">应聘者在申请后不再可以通过求职站点联系招聘团队。</span><span class="sxs-lookup"><span data-stu-id="139ff-177">After they apply, candidates can no longer contact the hiring team through the career site.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="139ff-178">申请工作</span><span class="sxs-lookup"><span data-stu-id="139ff-178">Apply for jobs</span></span>

<span data-ttu-id="139ff-179">应聘者找到合适的工作后，可以使用 **工作详细信息**页面的 **申请** 按钮进行申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-179">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="139ff-180">此时，应聘者可以创建新的个人资料或审查现有个人资料的信息。</span><span class="sxs-lookup"><span data-stu-id="139ff-180">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="139ff-181">应聘者还可以根据需要上载简历，然后提交工作申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-181">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a><span data-ttu-id="139ff-182">启用使用 LinkedIn 个人资料申请工作</span><span class="sxs-lookup"><span data-stu-id="139ff-182">Enable applying for jobs with LinkedIn profiles</span></span>

<span data-ttu-id="139ff-183">可以通过将 Attract 配置为允许应聘者通过 LinkedIn 申请职位，让应聘者轻松申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-183">You can make it easy for candidates to apply for your positions by configuring Attract to allow them to apply through LinkedIn.</span></span>

> [!NOTE] 
> <span data-ttu-id="139ff-184">需要先从 LinkedIn 获得一个或多个招聘人员许可证，才能允许应聘者通过 LinkedIn 申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-184">You need to have one or more recruiter licenses from LinkedIn before you can allow candidates to apply with LinkedIn.</span></span>

1. <span data-ttu-id="139ff-185">以管理员身份登录 Attract。</span><span class="sxs-lookup"><span data-stu-id="139ff-185">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="139ff-186">选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。</span><span class="sxs-lookup"><span data-stu-id="139ff-186">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="139ff-187">选择 **LinkedIn 集成**选项卡并与 LinkedIn Recruiter 帐户连接。</span><span class="sxs-lookup"><span data-stu-id="139ff-187">Select the **LinkedIn Integration** tab and connect with a LinkedIn recruiter account.</span></span>
4. <span data-ttu-id="139ff-188">在**LinkedIn Recruiter System Connect集成**部分中，为**通过 LinkedIn 申请**设置选择**启用**。</span><span class="sxs-lookup"><span data-stu-id="139ff-188">In the **LinkedIn Recruiter System Connect Integration** section, select **Enabled** for the **Apply with LinkedIn** setting.</span></span>

<span data-ttu-id="139ff-189">启用此设置之后，应聘者可使用自己的现有 LinkedIn 个人资料数据进行申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-189">After you've enabled the setting, candidates can apply using their existing LinkedIn profile data.</span></span> <span data-ttu-id="139ff-190">当应聘者通过选择**通过 LinkedIn 申请**按钮进行申请时，如果他们尚未登录，还将请他们向 LinkedIn 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="139ff-190">When candidates apply by choosing the **Apply with LinkedIn** button, they are asked to authenticate with LinkedIn if they're not already signed in.</span></span> <span data-ttu-id="139ff-191">通过了身份验证之后，其 LinkedIn 个人资料将替换申请页面中显示的所有现有个人资料数据。</span><span class="sxs-lookup"><span data-stu-id="139ff-191">After they've authenticated, their LinkedIn profile replaces any existing profile data shown in the application page.</span></span> <span data-ttu-id="139ff-192">应聘者可以根据需要编辑信息，然后提交申请表。</span><span class="sxs-lookup"><span data-stu-id="139ff-192">Candidates can edit the information as needed and then submit the application.</span></span> <span data-ttu-id="139ff-193">如果应聘者在不申请工作的情况下离开该页面，Attract 中将不更新其个人资料数据。</span><span class="sxs-lookup"><span data-stu-id="139ff-193">If a candidate navigates away from the page without applying for the job, their profile data is not updated in Attract.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="139ff-194">检查申请状态</span><span class="sxs-lookup"><span data-stu-id="139ff-194">Check application status</span></span>

<span data-ttu-id="139ff-195">应聘者申请一个或多个工作后，可以在页面顶部的导航栏上选择**申请**来查看其打开和关闭的申请。</span><span class="sxs-lookup"><span data-stu-id="139ff-195">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="139ff-196">在应聘者打开一个申请时，他们将看到当前阶段以及他们必须完成的任何待处理的操作项目。</span><span class="sxs-lookup"><span data-stu-id="139ff-196">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="139ff-197">例如，如果应聘者必须为面对面面试提供潜在日期，页面将显示可用选项。</span><span class="sxs-lookup"><span data-stu-id="139ff-197">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="139ff-198">内部工作</span><span class="sxs-lookup"><span data-stu-id="139ff-198">Internal jobs</span></span>

<span data-ttu-id="139ff-199">目前，标记为内部并发布到 Attract 求职站点的工作不出现在求职站点上。</span><span class="sxs-lookup"><span data-stu-id="139ff-199">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="139ff-200">只能使用直接的**申请** URL（可以从 Attract 应用程序复制）访问这些工作。</span><span class="sxs-lookup"><span data-stu-id="139ff-200">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
