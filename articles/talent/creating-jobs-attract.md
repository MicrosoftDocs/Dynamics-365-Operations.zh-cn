---
title: 在 Attract 中创建、审核和发布工作
description: 此主题描述 Attract 中的工作元素。 它还介绍了如何创建工作。
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
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1e76572c1a843fe7abd515333d5b7cb03b91eb11
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/12/2019
ms.locfileid: "969341"
---
# <a name="create-approve-and-post-jobs-in-attract"></a><span data-ttu-id="2eccd-104">在 Attract 中创建、审核和发布工作</span><span class="sxs-lookup"><span data-stu-id="2eccd-104">Create, approve, and post jobs in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2eccd-105">此主题描述 Microsoft Dynamics 365 for Talent: Attract 中的工作元素。</span><span class="sxs-lookup"><span data-stu-id="2eccd-105">This topic describes the elements of a job in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="2eccd-106">它还介绍了如何创建工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-106">It also explains how to create a job.</span></span>

## <a name="job-creation"></a><span data-ttu-id="2eccd-107">工作创建</span><span class="sxs-lookup"><span data-stu-id="2eccd-107">Job creation</span></span>

<span data-ttu-id="2eccd-108">管理员、招聘人员和招聘经理可以创建工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-108">Admins, recruiters, and hiring managers can create jobs.</span></span> <span data-ttu-id="2eccd-109">当创建工作时，系统将提示您选择您在流程中的角色：招聘经理或招聘人员。</span><span class="sxs-lookup"><span data-stu-id="2eccd-109">When you create a job, you're prompted to select your role in the process: hiring manager or recruiter.</span></span> <span data-ttu-id="2eccd-110">在选择角色之后，将提示您选择流程模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-110">After you select a role, you're prompted to select a process template.</span></span> <span data-ttu-id="2eccd-111">如果您选择**跳过**，将使用默认模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-111">If you select **Skip**, the default template is used.</span></span> <span data-ttu-id="2eccd-112">有关流程模板的详细信息，请参阅[在 Attract 中创建流程模板](./process-templates-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-112">For more information about process templates, see [Create a process template in Attract](./process-templates-attract.md).</span></span>

<span data-ttu-id="2eccd-113">Attract 中的工作包含工作详细信息、招聘团队、招聘流程、工作发布和分析。</span><span class="sxs-lookup"><span data-stu-id="2eccd-113">A job in Attract has job details, a hiring team, a hiring process, job postings, and analytics.</span></span>

## <a name="job-details"></a><span data-ttu-id="2eccd-114">工作详细信息</span><span class="sxs-lookup"><span data-stu-id="2eccd-114">Job details</span></span>

<span data-ttu-id="2eccd-115">**工作详细信息**选项卡包含有关工作职责和属性的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2eccd-115">The **Job details** tab contains details about the job's responsibilities and attributes.</span></span> <span data-ttu-id="2eccd-116">职务、工作描述和工作位置字段是必填字段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-116">The fields for the job title, job description, and job location are required.</span></span> <span data-ttu-id="2eccd-117">其他字段是可选的。</span><span class="sxs-lookup"><span data-stu-id="2eccd-117">The other fields are optional.</span></span>

<span data-ttu-id="2eccd-118">默认情况下，**空缺数量**字段设置为 **1**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-118">By default, the **Number of openings** field is set to **1**.</span></span> <span data-ttu-id="2eccd-119">然而，您可以更改值。</span><span class="sxs-lookup"><span data-stu-id="2eccd-119">However, you can change the value.</span></span> <span data-ttu-id="2eccd-120">当为工作准备好了聘约时，**可用空缺数量**字段的值将减少。</span><span class="sxs-lookup"><span data-stu-id="2eccd-120">When an offer has been prepared for a job, the value of the **Number of openings available** field is decremented.</span></span>

<span data-ttu-id="2eccd-121">如果职位管理在管理员中心已打开，**更新职位**查找将可用。</span><span class="sxs-lookup"><span data-stu-id="2eccd-121">If position management has been turned on in the Admin Center, the **Update positions** lookup is available.</span></span> <span data-ttu-id="2eccd-122">此查找读取 Common Data Service 中的 JobPosition 实体并返回可为工作选择的职位列表。</span><span class="sxs-lookup"><span data-stu-id="2eccd-122">This lookup reads the JobPosition entity in Common Data Service and returns a list of positions that can be selected for the job.</span></span> <span data-ttu-id="2eccd-123">如果选择的职位数量超出空缺职位数量，将收到警告。</span><span class="sxs-lookup"><span data-stu-id="2eccd-123">If the number of positions that you select exceeds the number of open positions, you receive a warning.</span></span> <span data-ttu-id="2eccd-124">如果一个职位用于多个工作，您也会收到警告。</span><span class="sxs-lookup"><span data-stu-id="2eccd-124">You also receive a warning if a position is used on multiple jobs.</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-125">职位管理随综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="2eccd-125">Position management is available with the Comprehensive Hiring Add-on.</span></span>

<span data-ttu-id="2eccd-126">根据招聘流程的聘约活动的设置，职位编号可以在聘约中使用两次。</span><span class="sxs-lookup"><span data-stu-id="2eccd-126">Depending on the settings in the Offer activity of the hiring process, a position number can be used twice in an offer.</span></span> <span data-ttu-id="2eccd-127">有关详细信息，请参阅[招聘流程](./activities-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-127">For more information, see [Hiring process](./activities-attract.md).</span></span>

<span data-ttu-id="2eccd-128">Attract 包含一组默认**技能**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-128">Attract includes a default set of **Skills**.</span></span> <span data-ttu-id="2eccd-129">在键入时，这些技能作为建议出现。</span><span class="sxs-lookup"><span data-stu-id="2eccd-129">These skills appear as suggestions as you type.</span></span> <span data-ttu-id="2eccd-130">您可以通过在字段中输入新技能文本然后按 Enter 来添加更多技能。</span><span class="sxs-lookup"><span data-stu-id="2eccd-130">You can add more skills by entering the new skill text in the field and then pressing Enter.</span></span>

<span data-ttu-id="2eccd-131">Attract 包含一组默认的**工作职能**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-131">Attract includes a default set of **Job functions**.</span></span> <span data-ttu-id="2eccd-132">您可以通过在字段中输入新的工作职能然后按 Enter 来最多再添加三个工作职能。</span><span class="sxs-lookup"><span data-stu-id="2eccd-132">You can add up to three more job functions by entering the new job function in the field and then pressing Enter.</span></span>

<span data-ttu-id="2eccd-133">Attract 包含一组默认的**公司行业**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-133">Attract includes a default set of **Company industry**.</span></span> <span data-ttu-id="2eccd-134">您可以通过在字段中输入新的公司行业然后按 Enter 来最多再添加三个公司行业。</span><span class="sxs-lookup"><span data-stu-id="2eccd-134">You can add up to three more company industries by entering the new company industry in the field and then pressing Enter.</span></span>

## <a name="hiring-team"></a><span data-ttu-id="2eccd-135">招聘团队</span><span class="sxs-lookup"><span data-stu-id="2eccd-135">Hiring team</span></span>

<span data-ttu-id="2eccd-136">**招聘团队**选项卡包含工作所涉及的个人的列表。</span><span class="sxs-lookup"><span data-stu-id="2eccd-136">The **Hiring team** tab contains the list of individuals who will be involved in the job.</span></span> <span data-ttu-id="2eccd-137">在用户被添加到招聘团队时，必须为他们分配在招聘团队中的角色。</span><span class="sxs-lookup"><span data-stu-id="2eccd-137">When users are added to a hiring team, they must be assigned a role on the hiring team.</span></span> <span data-ttu-id="2eccd-138">角色确定用户有权访问的数据和他们将收到的通知。</span><span class="sxs-lookup"><span data-stu-id="2eccd-138">The role determines the data that the users have access to and the notifications that they receive.</span></span> <span data-ttu-id="2eccd-139">可以选择的角色有**招聘人员**、**招聘经理**、**委托人**和**面试官**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-139">The roles that can be selected are **Recruiter**, **Hiring manager**, **Delegate**, and **Interviewer**.</span></span> <span data-ttu-id="2eccd-140">有关角色权限的详细信息，请参阅“角色管理”文档。</span><span class="sxs-lookup"><span data-stu-id="2eccd-140">For more information about role privileges, see the "Role management" document.</span></span> <span data-ttu-id="2eccd-141">招聘人员和招聘经理可以指派一个或多个委托人来代表他们工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-141">Recruiters and hiring managers can appoint one or more delegates to work on their behalf.</span></span> <span data-ttu-id="2eccd-142">有关委托人的详细信息，请参阅 [Attract 中的安全和角色管理](./security-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-142">For more information about delegates, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="2eccd-143">招聘团队可以在激活工作后更新。</span><span class="sxs-lookup"><span data-stu-id="2eccd-143">The hiring team can be updated after the job is activated.</span></span>

## <a name="process"></a><span data-ttu-id="2eccd-144">进程</span><span class="sxs-lookup"><span data-stu-id="2eccd-144">Process</span></span>

<span data-ttu-id="2eccd-145">有关招聘流程的默认信息基于创建工作时选择的流程模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-145">Default information about the hiring process is based on the process template that was selected when the job was created.</span></span> <span data-ttu-id="2eccd-146">如果当时未选择特定模板，将使用默认模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-146">If a specific template wasn't selected at that time, the default template is used.</span></span> <span data-ttu-id="2eccd-147">在您定义招聘流程时，您可以添加或删除各个阶段，“应聘者”、“申请”和“聘约”阶段除外。</span><span class="sxs-lookup"><span data-stu-id="2eccd-147">When you define the hiring process, you can add or remove various stages, except the Prospect, Application, and Offer stages.</span></span> <span data-ttu-id="2eccd-148">虽然不能删除“应聘者”阶段，但可以将其关闭。</span><span class="sxs-lookup"><span data-stu-id="2eccd-148">Although the Prospect stage can't be removed, it can be turned off.</span></span> <span data-ttu-id="2eccd-149">在每个阶段中，可以添加或移除一个或多个预定义的活动。</span><span class="sxs-lookup"><span data-stu-id="2eccd-149">Within each stage, you can add or remove one or more predefined activities.</span></span>

<span data-ttu-id="2eccd-150">有关可以添加到招聘流程的活动的详细信息，请参阅 [Attract 中的招聘流程活动](./activities-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-150">For more information about activities that can be added to the hiring process, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-151">招聘流程不能在激活工作后更新。</span><span class="sxs-lookup"><span data-stu-id="2eccd-151">The process hiring can't be updated after a job is activated.</span></span>

## <a name="postings"></a><span data-ttu-id="2eccd-152">过帐记录</span><span class="sxs-lookup"><span data-stu-id="2eccd-152">Postings</span></span>

<span data-ttu-id="2eccd-153">在激活工作后，便可以发布工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-153">After a job is activated, it can be posted.</span></span> <span data-ttu-id="2eccd-154">只有招聘人员和管理员可以发布工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-154">Only recruiters and admins can post jobs.</span></span> <span data-ttu-id="2eccd-155">工作可以发布到 Talent Careers（Microsoft Dynamics 365 for Talent 求职站点）或 LinkedIn。</span><span class="sxs-lookup"><span data-stu-id="2eccd-155">The job can be posted to either Talent Careers (a Microsoft Dynamics 365 for Talent career site) or LinkedIn.</span></span> <span data-ttu-id="2eccd-156">Attract 团队正在继续努力与工作面板整合者合作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-156">The Attract team is continually working to partner with job board aggregators.</span></span> <span data-ttu-id="2eccd-157">此列表一段时间后将扩展。</span><span class="sxs-lookup"><span data-stu-id="2eccd-157">This list will expand over time.</span></span> <span data-ttu-id="2eccd-158">如果工作作为仅内部工作发布，应聘者需要 AAD 帐户才能查看和申请该工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-158">When a job is posted as internal only, candidates need an AAD account to view and apply for the job.</span></span> <span data-ttu-id="2eccd-159">如果工作作为公开工作列出，则应聘者可使用所有身份验证选项查看和申请工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-159">If the job is listed as public, candidates can view and apply for jobs using all authentication options.</span></span> 

<span data-ttu-id="2eccd-160">有关工作发布的详细信息，请参阅 [Attract 中的求职站点功能](career-site.md)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-160">For more information about job postings, see [Career site functionality in Attract](career-site.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-161">工作发布功能只随 Attract 的综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="2eccd-161">The job posting functionality is available only with the Comprehensive Hiring Add-on for Attract.</span></span>

### <a name="posting-jobs-to-linkedin"></a><span data-ttu-id="2eccd-162">将工作发布到 LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2eccd-162">Posting jobs to LinkedIn</span></span> 

<span data-ttu-id="2eccd-163">将工作从 Attract 发布到 LinkedIn 之前，管理员必须在**管理中心**中添加 LinkedIn 公司 ID 和 LinkedIn 公司名。</span><span class="sxs-lookup"><span data-stu-id="2eccd-163">Before posting a job from Attract to LinkedIn, the administrator must add the LinkedIn Company ID and LinkedIn Company name in the **Admin Settings**.</span></span> <span data-ttu-id="2eccd-164">需要 LinkedIn 公司 ID 才能确保将从 Attract 发布的工作映射到正确的公司页面。</span><span class="sxs-lookup"><span data-stu-id="2eccd-164">The LinkedIn Company ID is required to ensure your jobs posted from Attract are mapped to the correct company page.</span></span>

<span data-ttu-id="2eccd-165">LinkedIn 公司 ID 是一个数字字符串，用于在 LinkedIn 内唯一标识您的公司。</span><span class="sxs-lookup"><span data-stu-id="2eccd-165">Your LinkedIn Company ID is a string of numbers that uniquely identifies your company within LinkedIn.</span></span> <span data-ttu-id="2eccd-166">有关如何查找 LinkedIn 公司 ID 的详细信息，请访问 [LinkedIn 站点](https://aka.ms/findID)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-166">For more information on how to find your LinkedIn company ID, please visit the [LinkedIn site](https://aka.ms/findID).</span></span>

<span data-ttu-id="2eccd-167">若要更新 LinkedIn 公司，请选择 **设置** 菜单（齿轮符号）中的 **管理中心** ，然后选择  **LinkedIn 集成** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2eccd-167">To update your LinkedIn company, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **LinkedIn Integration** tab.</span></span> <span data-ttu-id="2eccd-168">在**连接到 LinkedIn**部分下，输入你的 LinkedIn 公司名和公司 ID，然后保存设置。</span><span class="sxs-lookup"><span data-stu-id="2eccd-168">Under the **Connect to LinkedIn** section, enter your LinkedIn Company Name and Company ID, and then save the settings.</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-169">将流程发布到 LinkedIn 的作业有四个重要事项需要说明。</span><span class="sxs-lookup"><span data-stu-id="2eccd-169">There are four important things to note about job posting process to LinkedIn.</span></span>
> 1. <span data-ttu-id="2eccd-170">发布到 LinkedIn 的作业作为“限制清单”作业发布。</span><span class="sxs-lookup"><span data-stu-id="2eccd-170">Jobs posted to LinkedIn are posted as "Limited Listings" jobs.</span></span> <span data-ttu-id="2eccd-171">限制清单作业不能跨 LinkedIn 站点提升。</span><span class="sxs-lookup"><span data-stu-id="2eccd-171">Limited listing jobs cannot be promoted across the LinkedIn site.</span></span> <span data-ttu-id="2eccd-172">如果您要从 Attract 提升发布到 LinkedIn 的限制清单作业，您应使用 LinkedIn 启用“作业包装”。</span><span class="sxs-lookup"><span data-stu-id="2eccd-172">If you want to promote limited listing jobs posted to LinkedIn from Attract, you should work with LinkedIn to enable "Job Wrapping".</span></span> <span data-ttu-id="2eccd-173">有关更多详细信息，请参阅以下链接或联系 LinkedIn 支持。</span><span class="sxs-lookup"><span data-stu-id="2eccd-173">Please refer to links below and contact LinkedIn support for more details.</span></span>
>
>    [<span data-ttu-id="2eccd-174">作业包装的限制清单与津贴作业时隙</span><span class="sxs-lookup"><span data-stu-id="2eccd-174">Limited Listings vs Premium Job Slots for Job Wrapping</span></span>](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [<span data-ttu-id="2eccd-175">作业包装常见问题</span><span class="sxs-lookup"><span data-stu-id="2eccd-175">Job Wrapping FAQ</span></span>](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. <span data-ttu-id="2eccd-176">在将作业发布到 LinkedIn 时，Attract 根据作业传递 Microsoft 365 组织的名称。</span><span class="sxs-lookup"><span data-stu-id="2eccd-176">When posting jobs to LinkedIn, Attract passes the Microsoft 365 Organization name against the job.</span></span> <span data-ttu-id="2eccd-177">LinkedIn 基于传递的组织名称将作业链接到 LinkedIn 端的公司。</span><span class="sxs-lookup"><span data-stu-id="2eccd-177">LinkedIn links the jobs to a company on the LinkedIn side based on the organization name that is passed.</span></span> <span data-ttu-id="2eccd-178">如果您的作业根据 LinkedIn 上的错误公司列出，请检查您的 Microsoft 365 组织的名称是否与 LinkedIn 上的公司名称匹配。</span><span class="sxs-lookup"><span data-stu-id="2eccd-178">If your job is listed against the wrong company on LinkedIn, check that your Microsoft 365 Organization name matches the company name on LinkedIn.</span></span>  
>
>    [<span data-ttu-id="2eccd-179">更改地址联系人等信息</span><span class="sxs-lookup"><span data-stu-id="2eccd-179">Change Address Contact and more</span></span>](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    <span data-ttu-id="2eccd-180">如果您在执行此步骤后有问题，请与 LinkedIn 支持联系。</span><span class="sxs-lookup"><span data-stu-id="2eccd-180">If you have problems after this step, please contact LinkedIn support.</span></span> 
> 
> 1. <span data-ttu-id="2eccd-181">发布到 LinkedIn 的工作将在 LinkedIn 站点上实时显示。</span><span class="sxs-lookup"><span data-stu-id="2eccd-181">Jobs posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="2eccd-182">不存在用于将工作发布到 LinkedIn 的测试环境。</span><span class="sxs-lookup"><span data-stu-id="2eccd-182">There is no test environment for posting jobs to LinkedIn.</span></span> 
>
> 1. <span data-ttu-id="2eccd-183">由于当前的 LinkedIn 批处理作业发布流程，发布到 LinkedIn 的作业在 LinkedIn 中最多可能需要 24 小时显示给应聘者。</span><span class="sxs-lookup"><span data-stu-id="2eccd-183">It may take up to 24 hours for jobs posted to LinkedIn to be visible to candidates from within in LinkedIn, due to the current LinkedIn batch job posting process.</span></span>


## <a name="activate"></a><span data-ttu-id="2eccd-184">启用</span><span class="sxs-lookup"><span data-stu-id="2eccd-184">Activate</span></span>

<span data-ttu-id="2eccd-185">在激活工作后，可以发布工作，并且可以将应聘者和申请人添加到工作中。</span><span class="sxs-lookup"><span data-stu-id="2eccd-185">After a job is activated, it can be posted, and prospects and applicants can be added to it.</span></span> <span data-ttu-id="2eccd-186">向工作添加应聘者的选项在招聘流程中的“应聘者”活动中设置。</span><span class="sxs-lookup"><span data-stu-id="2eccd-186">The option to add prospects to a job is set in the Prospect activity in the hiring process.</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-187">招聘流程不能在激活工作后更新。</span><span class="sxs-lookup"><span data-stu-id="2eccd-187">The process hiring can't be updated after a job is activated.</span></span>

## <a name="prospects-and-applicants"></a><span data-ttu-id="2eccd-188">应聘者和申请人</span><span class="sxs-lookup"><span data-stu-id="2eccd-188">Prospects and applicants</span></span>

<span data-ttu-id="2eccd-189">向工作添加应聘者的选项在招聘流程中的[应聘者活动](./activities-attract.md#prospect-activity)中设置。</span><span class="sxs-lookup"><span data-stu-id="2eccd-189">The option to add prospects to a job is set in the [Prospect activity](./activities-attract.md#prospect-activity) in the hiring process.</span></span> <span data-ttu-id="2eccd-190">此选项应在激活工作之前设置。</span><span class="sxs-lookup"><span data-stu-id="2eccd-190">This option should be set before you activate the job.</span></span> <span data-ttu-id="2eccd-191">在激活工作后，可以将应聘者和申请人添加到工作中。</span><span class="sxs-lookup"><span data-stu-id="2eccd-191">After a job is activated, prospects and applicants can be added to it.</span></span>

## <a name="approvals"></a><span data-ttu-id="2eccd-192">审核</span><span class="sxs-lookup"><span data-stu-id="2eccd-192">Approvals</span></span>

<span data-ttu-id="2eccd-193">Attract 工作可以提交以供审核。</span><span class="sxs-lookup"><span data-stu-id="2eccd-193">Attract jobs can be submitted for approval.</span></span> <span data-ttu-id="2eccd-194">并非所有工作都需要审核。</span><span class="sxs-lookup"><span data-stu-id="2eccd-194">Not all jobs require approval.</span></span> <span data-ttu-id="2eccd-195">要求在模板级别设置。</span><span class="sxs-lookup"><span data-stu-id="2eccd-195">The requirement is set at the template level.</span></span> <span data-ttu-id="2eccd-196">默认情况下，审核在模板中是关闭的。</span><span class="sxs-lookup"><span data-stu-id="2eccd-196">By default, approvals are turned off on the template.</span></span> <span data-ttu-id="2eccd-197">若要设置审核，请转到流程模板，将**审核**字段设置为“默认”。</span><span class="sxs-lookup"><span data-stu-id="2eccd-197">To set up approvals, go to a process template, and set the **Approval** field to Default.</span></span> <span data-ttu-id="2eccd-198">然后在您创建工作时选择该模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-198">Then select that template when you create the job.</span></span>

<span data-ttu-id="2eccd-199">在保存工作之后，可以提交工作以供审核。</span><span class="sxs-lookup"><span data-stu-id="2eccd-199">After a job is saved, it can be submitted for approval.</span></span> <span data-ttu-id="2eccd-200">下表列出了使用审核的文档的状态。</span><span class="sxs-lookup"><span data-stu-id="2eccd-200">The following table lists the statuses of a document that uses approvals.</span></span>

| <span data-ttu-id="2eccd-201">状态</span><span class="sxs-lookup"><span data-stu-id="2eccd-201">Status</span></span>   | <span data-ttu-id="2eccd-202">状态</span><span class="sxs-lookup"><span data-stu-id="2eccd-202">State</span></span>                                                               |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="2eccd-203">草案</span><span class="sxs-lookup"><span data-stu-id="2eccd-203">Draft</span></span>    | <span data-ttu-id="2eccd-204">工作已保存，但未提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="2eccd-204">The job has been saved, but it hasn't been submitted to a workflow.</span></span> |
| <span data-ttu-id="2eccd-205">挂起</span><span class="sxs-lookup"><span data-stu-id="2eccd-205">Pending</span></span>  | <span data-ttu-id="2eccd-206">工作已提交给审核人。</span><span class="sxs-lookup"><span data-stu-id="2eccd-206">The job has been submitted to approvers.</span></span>                            |
| <span data-ttu-id="2eccd-207">已审批</span><span class="sxs-lookup"><span data-stu-id="2eccd-207">Approved</span></span> | <span data-ttu-id="2eccd-208">工作已审核，但未激活。</span><span class="sxs-lookup"><span data-stu-id="2eccd-208">The job has been approved, but it hasn't been activated.</span></span>            |
| <span data-ttu-id="2eccd-209">已拒绝</span><span class="sxs-lookup"><span data-stu-id="2eccd-209">Rejected</span></span> | <span data-ttu-id="2eccd-210">工作被拒绝，无法激活。</span><span class="sxs-lookup"><span data-stu-id="2eccd-210">The job has been rejected, and it can't be activated.</span></span>               |
| <span data-ttu-id="2eccd-211">有效的</span><span class="sxs-lookup"><span data-stu-id="2eccd-211">Active</span></span>   | <span data-ttu-id="2eccd-212">工作已审核并激活。</span><span class="sxs-lookup"><span data-stu-id="2eccd-212">The job has been approved and activated.</span></span>                            |

<span data-ttu-id="2eccd-213">在工作列表中，您可以筛选工作状态。</span><span class="sxs-lookup"><span data-stu-id="2eccd-213">In the job list, you can filter on the job statuses.</span></span>

<span data-ttu-id="2eccd-214">审核可以发送给公司中的任何 Microsoft Azure Active Directory (Azure AD) 用户。</span><span class="sxs-lookup"><span data-stu-id="2eccd-214">Approvals can be sent to any Microsoft Azure Active Directory (Azure AD) user in the company.</span></span> <span data-ttu-id="2eccd-215">审核可以同时发送给列出为审核人的所有人员。</span><span class="sxs-lookup"><span data-stu-id="2eccd-215">The approvals are sent in parallel to all the people who are listed as approvers.</span></span> <span data-ttu-id="2eccd-216">工作只有在经过所有审核人的审核后，才能进入下一阶段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-216">All approvers must approve the job before it can move forward.</span></span> <span data-ttu-id="2eccd-217">如果一位审核人拒绝工作，该工作将显示**已拒绝**状态。</span><span class="sxs-lookup"><span data-stu-id="2eccd-217">If a single approver rejects the job, the job will display a **Rejected** status.</span></span> <span data-ttu-id="2eccd-218">在审核工作后，便可以激活工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-218">After a job is approved, it can be activated.</span></span>

<span data-ttu-id="2eccd-219">如果用户编辑已审核但未激活的工作，工作状态将重置为**草稿**，并且必须重新提交该工作以供审核。</span><span class="sxs-lookup"><span data-stu-id="2eccd-219">If a user edits the job after it is approved, but not activated, the job status will be reset to **Draft**, and the job must be re-submitted for approval.</span></span> <span data-ttu-id="2eccd-220">不能编辑已审核且已激活的工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-220">After an approved job has been activated, you can't edit it.</span></span>

<span data-ttu-id="2eccd-221">列出为审核人的人员将在 Attract 中收到通知和电子邮件，通知他们有要审核的项目。</span><span class="sxs-lookup"><span data-stu-id="2eccd-221">The people who are listed as approvers will receive a notification in Attract and an email to inform them they have an item to approve.</span></span>  <span data-ttu-id="2eccd-222">审核人可单击电子邮件中的链接打开工作，查看详细信息，然后批准或拒绝。</span><span class="sxs-lookup"><span data-stu-id="2eccd-222">In the email, approvers can click the link to open the job, review the details, and either approve or reject.</span></span> <span data-ttu-id="2eccd-223">工作的状态设置为**已批准**或**已拒绝**之后，提交者将在 Attract 中收到通知，并且还会收到一封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="2eccd-223">After the job's status is set to **Approved** or **Rejected**, the submitter will be notified in Attract and they will receive an email.</span></span> <span data-ttu-id="2eccd-224">此外，如果审核人在 24 小时内尚未响应审核请求，审核人还会收到提醒电子邮件。</span><span class="sxs-lookup"><span data-stu-id="2eccd-224">Also, the approvers will receive a reminder email if they have not responded to the approval request within 24 hours.</span></span>

> [!NOTE]
> <span data-ttu-id="2eccd-225">您可以为审核电子邮件创建自定义电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-225">You can create custom email templates for Approval emails.</span></span> <span data-ttu-id="2eccd-226">有关详细信息，请参阅[创建和管理电子邮件模板](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/email-templates)。</span><span class="sxs-lookup"><span data-stu-id="2eccd-226">For more information, see [Creating and managing email templates](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/email-templates).</span></span>

## <a name="create-a-job"></a><span data-ttu-id="2eccd-227">创建工作</span><span class="sxs-lookup"><span data-stu-id="2eccd-227">Create a job</span></span>

<span data-ttu-id="2eccd-228">请遵从这些步骤创建工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-228">Follow these steps to create a job.</span></span>

1. <span data-ttu-id="2eccd-229">转至**工作**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-229">Go to **Jobs**.</span></span>
2. <span data-ttu-id="2eccd-230">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-230">Select **New**.</span></span>
3. <span data-ttu-id="2eccd-231">在**职务**字段中，输入职务。</span><span class="sxs-lookup"><span data-stu-id="2eccd-231">In the **Job title** field, enter the job title.</span></span> <span data-ttu-id="2eccd-232">在**角色**字段中，输入您的角色。</span><span class="sxs-lookup"><span data-stu-id="2eccd-232">In the **Role** field, enter your role.</span></span>
4. <span data-ttu-id="2eccd-233">在**模板**字段中，选择模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-233">In the **Template** field, select a template.</span></span> <span data-ttu-id="2eccd-234">或者，选择**跳过**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-234">Alternatively, select **Skip**.</span></span> <span data-ttu-id="2eccd-235">如果您选择**跳过**，将使用标记为默认模板的模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-235">If you select **Skip**, the template that is marked as the default template is used.</span></span>

    <span data-ttu-id="2eccd-236">如果文档应经过审核流程，请选择**审核流程**字段设置为**默认**的模板。</span><span class="sxs-lookup"><span data-stu-id="2eccd-236">If the document should go through an approval process, select a template where the **Approval process** field is set to **Default**.</span></span>

5. <span data-ttu-id="2eccd-237">在**详细信息**选项卡上，输入工作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2eccd-237">On the **Details** tab, enter the details of the job.</span></span> <span data-ttu-id="2eccd-238">**职务**、**工作描述**和**位置**字段是必填字段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-238">The **Title**, **Job description**, and **Location** fields are required.</span></span>
6. <span data-ttu-id="2eccd-239">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-239">Select **Save**.</span></span>
7. <span data-ttu-id="2eccd-240">在**招聘团队**选项卡上，添加招聘经理、招聘人员或面试官。</span><span class="sxs-lookup"><span data-stu-id="2eccd-240">On the **Hiring team** tab, add a hiring manager, recruiter, or interviewer.</span></span>
8. <span data-ttu-id="2eccd-241">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-241">Select **Save**.</span></span>
9. <span data-ttu-id="2eccd-242">在**流程**选项卡上，根据需要添加或删除阶段：</span><span class="sxs-lookup"><span data-stu-id="2eccd-242">On the **Process** tab, add or remove stages as you require:</span></span>

    - <span data-ttu-id="2eccd-243">若要添加阶段，请选择 **+ 新阶段**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-243">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="2eccd-244">若要删除阶段，将指针悬停在要删除的阶段上，然后选择出现的垃圾桶按钮。</span><span class="sxs-lookup"><span data-stu-id="2eccd-244">To remove a stage, hover the pointer over the stage to remove, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="2eccd-245">不能删除“应聘者”、“申请”和“聘约”阶段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-245">The Prospect, Application, and Offer stages can't be removed.</span></span>

10. <span data-ttu-id="2eccd-246">根据需要添加或删除活动：</span><span class="sxs-lookup"><span data-stu-id="2eccd-246">Add or remove activities as you require:</span></span>

    - <span data-ttu-id="2eccd-247">要添加活动，请将其从右侧的列表拖到相应的阶段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-247">To add an activity, drag it from the list on the right to the appropriate stage.</span></span> <span data-ttu-id="2eccd-248">或者，双击活动，然后选择要添加到的阶段。</span><span class="sxs-lookup"><span data-stu-id="2eccd-248">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="2eccd-249">若要删除活动，展开活动，然后选择活动标题上的垃圾桶按钮。</span><span class="sxs-lookup"><span data-stu-id="2eccd-249">To remove an activity, expand the activity, and then select the trash can button on the activity header.</span></span>

11. <span data-ttu-id="2eccd-250">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-250">Select **Save**.</span></span>
12. <span data-ttu-id="2eccd-251">如果您选择了使用审核流程，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="2eccd-251">If you selected to use an approval process, follow these steps:</span></span>

    1. <span data-ttu-id="2eccd-252">选择 **+ 添加审核人**，然后输入具有 Azure AD 帐户的用户。</span><span class="sxs-lookup"><span data-stu-id="2eccd-252">Select **+ Add approver**, and then enter a user who has an Azure AD account.</span></span> <span data-ttu-id="2eccd-253">您可以添加多个审核人。</span><span class="sxs-lookup"><span data-stu-id="2eccd-253">You can add multiple approvers.</span></span>
    2. <span data-ttu-id="2eccd-254">选择**发送给审核人**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-254">Select **Send to approvers**.</span></span>

    <span data-ttu-id="2eccd-255">工作的**工作状态**字段设置为**待处理**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-255">The **Job status** field of the job is set to **Pending**.</span></span> <span data-ttu-id="2eccd-256">在**工作状态**字段的值更改为**已审核**后，可以激活该工作。</span><span class="sxs-lookup"><span data-stu-id="2eccd-256">After the value of the **Job status** field changes to **Approved**, the job can be activated.</span></span>

13. <span data-ttu-id="2eccd-257">若要激活工作，请选择**激活**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-257">To activate the job, select **Activate**.</span></span>
14. <span data-ttu-id="2eccd-258">要发布工作，请转到**发布**，然后选择 Talent Careers 站点或 LinkedIn 下的**立即发布**。</span><span class="sxs-lookup"><span data-stu-id="2eccd-258">To post the job, go to **Postings**, and then select **Post Now** under the Talent Careers site or LinkedIn.</span></span>
