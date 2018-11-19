---
title: "Attract 中的求职站点功能"
description: "本文提供 Microsoft Dynamics 365 for Talent - Attract 中面向应聘者的求职站点功能的概览。 另外还介绍如何设置此功能。"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: zh-cn
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="92928-104">Attract 中的求职站点功能</span><span class="sxs-lookup"><span data-stu-id="92928-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92928-105">本文提供 Microsoft Dynamics 365 for Talent: Attract 中面向应聘者的求职站点功能的概览。</span><span class="sxs-lookup"><span data-stu-id="92928-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="92928-106">另外还介绍如何设置此功能。</span><span class="sxs-lookup"><span data-stu-id="92928-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="92928-107">概览</span><span class="sxs-lookup"><span data-stu-id="92928-107">Overview</span></span>

<span data-ttu-id="92928-108">Attract 为租户中的每个环境提供一个求职站点。</span><span class="sxs-lookup"><span data-stu-id="92928-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="92928-109">例如，如果组织具有开发环境和测试环境，一个求职站点为开发环境设置，另一个求职站点为测试环境设置。</span><span class="sxs-lookup"><span data-stu-id="92928-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="92928-110">各求职站点是**完全隔离**的，并且具有自己的身份验证机制。</span><span class="sxs-lookup"><span data-stu-id="92928-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="92928-111">工作和应聘者个人资料不在求职站点之间共享。</span><span class="sxs-lookup"><span data-stu-id="92928-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="92928-112">默认情况下，求职站点是公共的。</span><span class="sxs-lookup"><span data-stu-id="92928-112">By default, the career site is public.</span></span> <span data-ttu-id="92928-113">因此，应聘者可以查看标记为外部的所有工作，而不必登录。</span><span class="sxs-lookup"><span data-stu-id="92928-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="92928-114">但是，其他所有操作都需要应聘者登录。</span><span class="sxs-lookup"><span data-stu-id="92928-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="92928-115">求职站点管理</span><span class="sxs-lookup"><span data-stu-id="92928-115">Career site management</span></span>

<span data-ttu-id="92928-116">求职站点的以下项目由设置控制：</span><span class="sxs-lookup"><span data-stu-id="92928-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="92928-117">**组织名称：** 组织名称显示在求职站点顶部的导航栏中。</span><span class="sxs-lookup"><span data-stu-id="92928-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="92928-118">通过选择组织名称，应聘者可以转到列出所有空缺职位的页面。</span><span class="sxs-lookup"><span data-stu-id="92928-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="92928-119">**组织徽标：** 组织徽标的图像显示在求职站点的左上角。</span><span class="sxs-lookup"><span data-stu-id="92928-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="92928-120">通过选择徽标图像，应聘者可以转到列出所有空缺职位的页面。</span><span class="sxs-lookup"><span data-stu-id="92928-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="92928-121">若要设置组织名称和徽标值，作为管理员登录到 Attract，在**设置**菜单（齿轮符号）上选择**管理员中心**，然后选择**公司信息**选项卡。</span><span class="sxs-lookup"><span data-stu-id="92928-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="92928-122">显示在求职站点的徽标图像具有固定高度 20 像素 (px)。</span><span class="sxs-lookup"><span data-stu-id="92928-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="92928-123">在管理员中心添加的图像会缩放以适应此高度。</span><span class="sxs-lookup"><span data-stu-id="92928-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="92928-124">因此，根据图像，宽度可能会变化。</span><span class="sxs-lookup"><span data-stu-id="92928-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="92928-125">求职站点 URL</span><span class="sxs-lookup"><span data-stu-id="92928-125">Career site URL</span></span>

<span data-ttu-id="92928-126">在您首次[发布外部工作](./Creating-jobs-Attract.md#postings)时，您可以从 Attract 应用程序复制**申请**链接。</span><span class="sxs-lookup"><span data-stu-id="92928-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="92928-127">此链接的 URL 将使用以下格式：`https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="92928-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="92928-128">求职站点的 URL 是**申请** URL 的子字符串。</span><span class="sxs-lookup"><span data-stu-id="92928-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="92928-129">它包含公司名称的所有内容。</span><span class="sxs-lookup"><span data-stu-id="92928-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="92928-130">因此，对于前面的**申请** URL，求职站点 URL 为 `https://jobs.talent.dynamics.com/jobs/<company_name>/`。</span><span class="sxs-lookup"><span data-stu-id="92928-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="92928-131">身份验证选项</span><span class="sxs-lookup"><span data-stu-id="92928-131">Authentication options</span></span>

<span data-ttu-id="92928-132">应聘者具有以下 Attract 求职站点登录选项：</span><span class="sxs-lookup"><span data-stu-id="92928-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="92928-133">个人帐户：</span><span class="sxs-lookup"><span data-stu-id="92928-133">Personal account:</span></span>

    - <span data-ttu-id="92928-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="92928-134">LinkedIn</span></span>
    - <span data-ttu-id="92928-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="92928-135">Microsoft</span></span>
    - <span data-ttu-id="92928-136">Google</span><span class="sxs-lookup"><span data-stu-id="92928-136">Google</span></span>
    - <span data-ttu-id="92928-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="92928-137">Facebook</span></span>

- <span data-ttu-id="92928-138">工作或学校帐户：</span><span class="sxs-lookup"><span data-stu-id="92928-138">Work or school account:</span></span>

    - <span data-ttu-id="92928-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="92928-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="92928-140">Azure AD 登录仅用于内部应聘者。</span><span class="sxs-lookup"><span data-stu-id="92928-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="92928-141">因此，它只对使用其公司 Azure AD 凭据的内部应聘者有效。</span><span class="sxs-lookup"><span data-stu-id="92928-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="92928-142">例如，当前是 Contoso Ltd 员工的应聘者希望申请一家不相关公司 Alpine Ski House 的工作。</span><span class="sxs-lookup"><span data-stu-id="92928-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="92928-143">在这种情况下，如果员工尝试使用其 Contoso Ltd 的 Azure AD 凭据，登录将不成功。</span><span class="sxs-lookup"><span data-stu-id="92928-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="92928-144">创建和维护个人资料</span><span class="sxs-lookup"><span data-stu-id="92928-144">Create and maintain a profile</span></span>

<span data-ttu-id="92928-145">在应聘者登录到求职站点后，他们可以在页面顶部的导航栏中选择**我的个人资料**来创建和维护其个人资料。</span><span class="sxs-lookup"><span data-stu-id="92928-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="92928-146">个人资料包括个人信息、工作经验相关信息、教育详细信息、文档、链接以及技能信息。</span><span class="sxs-lookup"><span data-stu-id="92928-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="92928-147">个人资料创建后，可用于申请应聘者感兴趣的工作。</span><span class="sxs-lookup"><span data-stu-id="92928-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="92928-148">个人资料还可以帮助 Attract 向应聘者推荐合适的工作。</span><span class="sxs-lookup"><span data-stu-id="92928-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="92928-149">查找合适的工作</span><span class="sxs-lookup"><span data-stu-id="92928-149">Find the right job</span></span>

<span data-ttu-id="92928-150">在工作列表页，应聘者可以通过输入搜索词搜索特定工作。</span><span class="sxs-lookup"><span data-stu-id="92928-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="92928-151">搜索功能查找职务和工作描述中的搜索词，然后在结果中显示相关工作。</span><span class="sxs-lookup"><span data-stu-id="92928-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="92928-152">应聘者可以随时基于工作位置或工作职能筛选结果。</span><span class="sxs-lookup"><span data-stu-id="92928-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="92928-153">应聘者还可以在求职站点上查看一组推荐的工作。</span><span class="sxs-lookup"><span data-stu-id="92928-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="92928-154">向应聘者推荐的工作基于应聘者过去的申请、个人资料和简历。</span><span class="sxs-lookup"><span data-stu-id="92928-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="92928-155">仅当求职站点上至少发布了 10 个工作并且应聘者已经完成了个人资料时，工作推荐才会显示。</span><span class="sxs-lookup"><span data-stu-id="92928-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="92928-156">申请工作</span><span class="sxs-lookup"><span data-stu-id="92928-156">Apply for jobs</span></span>

<span data-ttu-id="92928-157">应聘者找到合适的工作后，可以使用工作详细信息页面的**申请**按钮进行申请。</span><span class="sxs-lookup"><span data-stu-id="92928-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="92928-158">此时，应聘者可以创建全新的个人资料或审查现有个人资料的信息。</span><span class="sxs-lookup"><span data-stu-id="92928-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="92928-159">应聘者还可以根据需要上载简历，然后提交工作申请。</span><span class="sxs-lookup"><span data-stu-id="92928-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="92928-160">检查申请状态</span><span class="sxs-lookup"><span data-stu-id="92928-160">Check application status</span></span>

<span data-ttu-id="92928-161">应聘者申请一个或多个工作后，可以在页面顶部的导航栏上选择**申请**来查看其打开和关闭的申请。</span><span class="sxs-lookup"><span data-stu-id="92928-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="92928-162">在应聘者打开一个申请时，他们将看到当前阶段以及他们必须完成的任何待处理的操作项目。</span><span class="sxs-lookup"><span data-stu-id="92928-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="92928-163">例如，如果应聘者必须为面对面面试提供潜在日期，页面将显示其选项。</span><span class="sxs-lookup"><span data-stu-id="92928-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="92928-164">内部工作</span><span class="sxs-lookup"><span data-stu-id="92928-164">Internal jobs</span></span>

<span data-ttu-id="92928-165">目前，标记为内部并发布到 Attract 求职站点的工作不出现在求职站点上。</span><span class="sxs-lookup"><span data-stu-id="92928-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="92928-166">他们只能通直接的**申请** URL（可以从 Attract 应用程序复制）访问。</span><span class="sxs-lookup"><span data-stu-id="92928-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

