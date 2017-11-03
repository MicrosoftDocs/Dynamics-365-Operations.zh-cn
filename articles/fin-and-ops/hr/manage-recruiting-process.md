---
title: "管理招聘流程"
description: "本文介绍招聘人员可以用于跟踪招聘流程的步骤的概念，包括宣传空缺职位和招聘申请人的工作，跟踪申请人和申请信息，面试申请人，以及选择一个或多个候选人以填充您的组织的空缺职位。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4a7dba99c08d4dfc6afd1047130cea51b6bdab1d
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="manage-a-recruiting-process"></a><span data-ttu-id="2a220-103">管理招聘流程</span><span class="sxs-lookup"><span data-stu-id="2a220-103">Manage a recruiting process</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2a220-104">本主题介绍招聘人员可以用于跟踪招聘流程的步骤的概念，包括宣传空缺职位和招聘申请人的工作，跟踪申请人和申请信息，面试申请人，以及选择一个或多个候选人以填充您的组织的空缺职位。</span><span class="sxs-lookup"><span data-stu-id="2a220-104">This topic describes a concept that recruiters can use to track the steps in a recruiting process, including efforts to advertise open positions and recruit applicants, tracking applicant and application information, interviewing applicants, and selecting one or more candidates to fill the open positions in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="2a220-105">概览</span><span class="sxs-lookup"><span data-stu-id="2a220-105">Overview</span></span>
--------

<span data-ttu-id="2a220-106">招聘项目可帮助您组织在法人中填写空缺职位时将完成的步骤。</span><span class="sxs-lookup"><span data-stu-id="2a220-106">Recruitment projects can help you organize the steps you'll complete when filling open positions in a legal entity.</span></span> <span data-ttu-id="2a220-107">申请人是向您的企业申请雇用的人员。</span><span class="sxs-lookup"><span data-stu-id="2a220-107">An applicant is a person who applies for employment to your enterprise.</span></span>  <span data-ttu-id="2a220-108">申请是申请人对被公司雇用感兴趣的表达，可能与招聘项目绑定以表达对特定空缺职位的兴趣。</span><span class="sxs-lookup"><span data-stu-id="2a220-108">An application is an applicant's expression of interest in being employed by a company and may be tied to a recruitment project to express interest in a specific opening.</span></span>  <span data-ttu-id="2a220-109">单个申请人可能在同一法人内或跨组织的多个公司有多个申请。</span><span class="sxs-lookup"><span data-stu-id="2a220-109">A single applicant may have multiple applications within the same legal entity or across multiple companies in your organization.</span></span>

<a name="recruitment-projects"></a><span data-ttu-id="2a220-110">招聘项目</span><span class="sxs-lookup"><span data-stu-id="2a220-110">Recruitment projects</span></span>
--------------------

<span data-ttu-id="2a220-111">招聘项目允许招聘人员跟踪进度填写一个或多个空缺职位的进度。</span><span class="sxs-lookup"><span data-stu-id="2a220-111">Recruitment projects allow recruiters to track progress against filling one or more open positions.</span></span>  <span data-ttu-id="2a220-112">招聘项目确定有一个或多个职位空缺的部门和工作。</span><span class="sxs-lookup"><span data-stu-id="2a220-112">The recruitment project identifies the department and job for which one or more positions are open.</span></span> <span data-ttu-id="2a220-113">招聘项目还跟踪空缺职位的以下信息：</span><span class="sxs-lookup"><span data-stu-id="2a220-113">Recruitment projects also track following information for open positions:</span></span>
-   <span data-ttu-id="2a220-114">空缺职位的具体数量</span><span class="sxs-lookup"><span data-stu-id="2a220-114">The specific number of open positions</span></span>
-   <span data-ttu-id="2a220-115">该职位的招聘经理和备选联系人</span><span class="sxs-lookup"><span data-stu-id="2a220-115">The hiring manager and an alternative contact for the position</span></span>
-   <span data-ttu-id="2a220-116">审核申请的日期</span><span class="sxs-lookup"><span data-stu-id="2a220-116">The date that the requisition was approved</span></span>
-   <span data-ttu-id="2a220-117">申请截止日期</span><span class="sxs-lookup"><span data-stu-id="2a220-117">The application deadline</span></span>
-   <span data-ttu-id="2a220-118">估计的开始日期</span><span class="sxs-lookup"><span data-stu-id="2a220-118">The estimated start date</span></span>

<span data-ttu-id="2a220-119">招聘项目包含在**员工自助服务**上用于宣传空缺职位的**工作广告**。</span><span class="sxs-lookup"><span data-stu-id="2a220-119">The recruitment project contains the **Job ad** used on the **Employee self service** to advertise the opening.</span></span> <span data-ttu-id="2a220-120">若要向员工显示空缺职位，招聘项目必须具有**工作广告**，**显示员工自助服务**字段必须设置为“是”，**申请截止日期**必须设置为一个将来的日期，并且招聘项目必须具有“已开始”**项目状态**。</span><span class="sxs-lookup"><span data-stu-id="2a220-120">To display the opening to employees, the recruitment project must have a **Job ad**, the **Display on employee self service** field must be set to Yes, the **Application deadline** must be set to a future date, and the recruitment project must have a **Project status** of Started.</span></span> <span data-ttu-id="2a220-121">下表列出可能的招聘项目状态和描述。</span><span class="sxs-lookup"><span data-stu-id="2a220-121">The following table lists the possible recruitment project statuses and their description.</span></span>

| <span data-ttu-id="2a220-122">**状态**</span><span class="sxs-lookup"><span data-stu-id="2a220-122">**Status**</span></span>    | <span data-ttu-id="2a220-123">**指示…**</span><span class="sxs-lookup"><span data-stu-id="2a220-123">**Indicates that…**</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a220-124">已计划</span><span class="sxs-lookup"><span data-stu-id="2a220-124">Scheduled</span></span> | <span data-ttu-id="2a220-125">招聘工作正在准备。</span><span class="sxs-lookup"><span data-stu-id="2a220-125">Recruiting efforts are being prepared.</span></span>  <span data-ttu-id="2a220-126">招聘还没有为此项目开始。</span><span class="sxs-lookup"><span data-stu-id="2a220-126">Recruiting has not yet started for this project.</span></span> |
| <span data-ttu-id="2a220-127">已开始</span><span class="sxs-lookup"><span data-stu-id="2a220-127">Started</span></span>   | <span data-ttu-id="2a220-128">正在接受此项目空缺职位的申请。</span><span class="sxs-lookup"><span data-stu-id="2a220-128">Applications are now being accepted for the openings in this project.</span></span>                    |
| <span data-ttu-id="2a220-129">已完成</span><span class="sxs-lookup"><span data-stu-id="2a220-129">Finished</span></span>  | <span data-ttu-id="2a220-130">此项目的所有空缺职位已填写。</span><span class="sxs-lookup"><span data-stu-id="2a220-130">All openings for this project have been filled.</span></span>                                          |
| <span data-ttu-id="2a220-131">已取消</span><span class="sxs-lookup"><span data-stu-id="2a220-131">Canceled</span></span>  | <span data-ttu-id="2a220-132">此项目的招聘已经取消。</span><span class="sxs-lookup"><span data-stu-id="2a220-132">Recruiting has been canceled for this project.</span></span>                                           |

<span data-ttu-id="2a220-133">招聘人员还可以记录用于通过外部机构宣传空缺职位的**媒体**，以及对照项目或申请跟踪**进展情况**。</span><span class="sxs-lookup"><span data-stu-id="2a220-133">Recruiters can also record the **Media** used to advertise the opening through external outlets as well as track **Developments** against the project or applications.</span></span>

<a name="applicants"></a><span data-ttu-id="2a220-134">申请人</span><span class="sxs-lookup"><span data-stu-id="2a220-134">Applicants</span></span>
----------

<span data-ttu-id="2a220-135">申请人是申请您企业的工作的人员。</span><span class="sxs-lookup"><span data-stu-id="2a220-135">An applicant is a person who applies for a job in your enterprise.</span></span>  <span data-ttu-id="2a220-136">申请人在您在的组织中的实体写字间共享，为您提供一个大人才库用于搜索。</span><span class="sxs-lookup"><span data-stu-id="2a220-136">Applicants are shared among all legal entities in your organization giving you a large pool of talent to search from.</span></span> <span data-ttu-id="2a220-137">您可以维护申请人的能力、推荐人、住宿请求和个人信息。</span><span class="sxs-lookup"><span data-stu-id="2a220-137">You can maintain competencies, references, accommodation requests, and personal information for applicants.</span></span> <span data-ttu-id="2a220-138">在您创建申请人记录时，在全球通讯簿中创建该申请人的人员记录。</span><span class="sxs-lookup"><span data-stu-id="2a220-138">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span> <span data-ttu-id="2a220-139">您可以使用**申请人**页为申请人的人员更新以下全球通讯簿信息：</span><span class="sxs-lookup"><span data-stu-id="2a220-139">You can use the **Applicant** page to update the following global address book information for people who are applicants:</span></span>
-   <span data-ttu-id="2a220-140">地址信息</span><span class="sxs-lookup"><span data-stu-id="2a220-140">Address information</span></span>
-   <span data-ttu-id="2a220-141">联系信息</span><span class="sxs-lookup"><span data-stu-id="2a220-141">Contact information</span></span>
-   <span data-ttu-id="2a220-142">标识信息</span><span class="sxs-lookup"><span data-stu-id="2a220-142">Identification information</span></span>
-   <span data-ttu-id="2a220-143">名称详细信息</span><span class="sxs-lookup"><span data-stu-id="2a220-143">Name details</span></span>
-   <span data-ttu-id="2a220-144">个人信息</span><span class="sxs-lookup"><span data-stu-id="2a220-144">Personal information</span></span>

## <a name="applications"></a><span data-ttu-id="2a220-145">应用程序</span><span class="sxs-lookup"><span data-stu-id="2a220-145">Applications</span></span>
<span data-ttu-id="2a220-146">您可以在**申请人**页中记录接收的来自雇用申请的信息。</span><span class="sxs-lookup"><span data-stu-id="2a220-146">You can record information from employment applications that you receive in the **Application** page.</span></span> <span data-ttu-id="2a220-147">申请是申请人对您组织的空缺职位感兴趣的表达。</span><span class="sxs-lookup"><span data-stu-id="2a220-147">The application is the applicant's expression of interest in a job opening in your organization.</span></span>  <span data-ttu-id="2a220-148">若要创建申请，申请人必须已作为您的系统的申请人或人员存在。</span><span class="sxs-lookup"><span data-stu-id="2a220-148">To create an application, the applicant must already exist as an applicant or person in your system.</span></span>
<span data-ttu-id="2a220-149">web 的申请人所提交的雇用申请表已输入响应工作广告的非主动提供的申请，或者是主动提供的申请。</span><span class="sxs-lookup"><span data-stu-id="2a220-149">Employment applications submitted by applicants on the web are either solicited applications that were entered in response to a job ad, or are unsolicited applications.</span></span> <span data-ttu-id="2a220-150">非主动提供的申请自动与从其创建工作广告的招聘项目相关。</span><span class="sxs-lookup"><span data-stu-id="2a220-150">Solicited applications are automatically associated with the recruitment project that the job ad was created from.</span></span> <span data-ttu-id="2a220-151">主动提供的申请与在**人力资源参数**页的**招聘**区域指定的招聘项目关联。</span><span class="sxs-lookup"><span data-stu-id="2a220-151">Unsolicited applications are associated with the recruitment project that is specified in the **Recruitment** area of the **Human resources parameters** page.</span></span>
### <a name="application-status"></a><span data-ttu-id="2a220-152">申请状态</span><span class="sxs-lookup"><span data-stu-id="2a220-152">Application status</span></span>

<span data-ttu-id="2a220-153">申请状态指示申请处于招聘流程。</span><span class="sxs-lookup"><span data-stu-id="2a220-153">The application status indicates where an application is in the recruitment process.</span></span> <span data-ttu-id="2a220-154">下表列出可能的申请状态和描述。</span><span class="sxs-lookup"><span data-stu-id="2a220-154">The following table lists the possible application statuses and their description.</span></span>

| <span data-ttu-id="2a220-155">状态</span><span class="sxs-lookup"><span data-stu-id="2a220-155">Status</span></span>    | <span data-ttu-id="2a220-156">指示…</span><span class="sxs-lookup"><span data-stu-id="2a220-156">Indicates that…</span></span>                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a220-157">已接收</span><span class="sxs-lookup"><span data-stu-id="2a220-157">Received</span></span>  | <span data-ttu-id="2a220-158">已收到申请表。</span><span class="sxs-lookup"><span data-stu-id="2a220-158">The application was received.</span></span>                                                             |
| <span data-ttu-id="2a220-159">已确认</span><span class="sxs-lookup"><span data-stu-id="2a220-159">Confirmed</span></span> | <span data-ttu-id="2a220-160">通知可以发送给申请人，确认收到其申请。</span><span class="sxs-lookup"><span data-stu-id="2a220-160">A notice can be sent to the applicant to confirm receipt of their application.</span></span>            |
| <span data-ttu-id="2a220-161">面试</span><span class="sxs-lookup"><span data-stu-id="2a220-161">Interview</span></span> | <span data-ttu-id="2a220-162">可以向申请人发送面试邀请。</span><span class="sxs-lookup"><span data-stu-id="2a220-162">An interview invitation can be sent to the applicant.</span></span>                                     |
| <span data-ttu-id="2a220-163">拒绝</span><span class="sxs-lookup"><span data-stu-id="2a220-163">Rejection</span></span> | <span data-ttu-id="2a220-164">拒绝函可以发送给申请人。</span><span class="sxs-lookup"><span data-stu-id="2a220-164">A rejection letter can be sent to the applicant.</span></span>                                          |
| <span data-ttu-id="2a220-165">已取消</span><span class="sxs-lookup"><span data-stu-id="2a220-165">Canceled</span></span>  | <span data-ttu-id="2a220-166">撤消确认可以发送给申请人。</span><span class="sxs-lookup"><span data-stu-id="2a220-166">A withdrawal confirmation can be sent to the applicant.</span></span> <span data-ttu-id="2a220-167">该状态手动分配。</span><span class="sxs-lookup"><span data-stu-id="2a220-167">This status is assigned manually.</span></span> |
| <span data-ttu-id="2a220-168">已雇用</span><span class="sxs-lookup"><span data-stu-id="2a220-168">Employed</span></span>  | <span data-ttu-id="2a220-169">雇用信可以发送给申请人。</span><span class="sxs-lookup"><span data-stu-id="2a220-169">An employment offer can be sent to the applicant.</span></span>                                         |

### <a name="correspondence-actions"></a><span data-ttu-id="2a220-170">通信行为</span><span class="sxs-lookup"><span data-stu-id="2a220-170">Correspondence actions</span></span>

<span data-ttu-id="2a220-171">**申请人**的通信行为确定用于和提交申请表的申请人交流的文档或电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="2a220-171">An **Application’s** correspondence action determines the document or e-mail template that you use to communicate with the applicant who submitted the application.</span></span> <span data-ttu-id="2a220-172">您可以将**申请书签**与通信行为关联以允许您在与申请人的通信中使用申请、申请人、面试和招聘项目页面的值。</span><span class="sxs-lookup"><span data-stu-id="2a220-172">You can associate **Application bookmarks** with correspondence actions to allow you to use values from the Application, Applicant, Interview, and Recruitment project pages in your communications with applicants.</span></span>  <span data-ttu-id="2a220-173">**申请电子邮件模板**可以为通信行为创建将电子邮件快速发送到具有某个状态和通信行为组合的申请的申请人。</span><span class="sxs-lookup"><span data-stu-id="2a220-173">**Application e-mail templates** can be created for the correspondence actions to quickly send e-mails to applicants who have an application with a certain status and correspondence action combination.</span></span> <span data-ttu-id="2a220-174">例如，您可以将确认电子邮件发送给所有具有“已接收”**状态**和“已接收”**通信行为**的申请。</span><span class="sxs-lookup"><span data-stu-id="2a220-174">For example, you may send a Confirmation e-mail to all Applications with a **Status** of Received and a **Correspondence action** of Received.</span></span>  <span data-ttu-id="2a220-175">在发送电子邮件后，您可以选择自动更新申请状态。</span><span class="sxs-lookup"><span data-stu-id="2a220-175">After sending the e-mail, you have the option to automatically update the status of the applications.</span></span>

## <a name="application-routing"></a><span data-ttu-id="2a220-176">申请工艺路线</span><span class="sxs-lookup"><span data-stu-id="2a220-176">Application routing</span></span>

<span data-ttu-id="2a220-177">如果必须按若干工作人员审核申请，您可以使用**申请路径**页创建工作人员传阅列表来管理流程。</span><span class="sxs-lookup"><span data-stu-id="2a220-177">If an application must be reviewed by several workers, you can use the **Application routing** page to create a worker circulation list in order to manage the process.</span></span>

## <a name="interviews"></a><span data-ttu-id="2a220-178">面试</span><span class="sxs-lookup"><span data-stu-id="2a220-178">Interviews</span></span>

<span data-ttu-id="2a220-179">**申请人面试**可以从该**申请**页面计划。</span><span class="sxs-lookup"><span data-stu-id="2a220-179">**Applicant interviews** can be scheduled from the **Applications** page.</span></span>  <span data-ttu-id="2a220-180">使用**发送会议信息**按钮可以将包含面试计划信息的日历文件发送给该申请人和面试人员。</span><span class="sxs-lookup"><span data-stu-id="2a220-180">Use the **Send meeting information** button to send a calendar file with the interview schedule information to the applicant and interviewer.</span></span>

## <a name="skill-mapping"></a><span data-ttu-id="2a220-181">技能表</span><span class="sxs-lookup"><span data-stu-id="2a220-181">Skill mapping</span></span>

<span data-ttu-id="2a220-182">**技能表**和**技能表模板**可以用于确定可能是适合空缺职位的候选人。</span><span class="sxs-lookup"><span data-stu-id="2a220-182">**Skill mapping** and **Skill mapping profiles** can be used to identify candidates who may be a good fit for an opening.</span></span>

## <a name="hiring-applicants"></a><span data-ttu-id="2a220-183">雇用申请人</span><span class="sxs-lookup"><span data-stu-id="2a220-183">Hiring applicants</span></span>

<span data-ttu-id="2a220-184">使用**申请**页雇用申请人。</span><span class="sxs-lookup"><span data-stu-id="2a220-184">Use the **Applications** page to hire an applicant.</span></span> <span data-ttu-id="2a220-185">在您雇用申请人时，申请记录将具有**已雇用**的状态，并且申请人的全球通讯簿人员记录与新工作人员记录关联。</span><span class="sxs-lookup"><span data-stu-id="2a220-185">When you hire an applicant, the application record will have a status of **Employed** and the applicant’s global address book person record is associated with the new worker record.</span></span> <span data-ttu-id="2a220-186">修改全球通讯簿信息，新的工作人员记录在申请人记录中显示。</span><span class="sxs-lookup"><span data-stu-id="2a220-186">Modifications to the global address book information for the new worker record are also displayed in the applicant record.</span></span> <span data-ttu-id="2a220-187">如果新工作人员在您的企业中申请不同的工作，这可能有助于减少数据输入。</span><span class="sxs-lookup"><span data-stu-id="2a220-187">This can help reduce data entry if the new worker ever applies for a different job within your enterprise.</span></span>  <span data-ttu-id="2a220-188">若要雇用现有工作人员到新职位，请单击**申请状态**下拉列表中的**变更职位**以开始转移流程。</span><span class="sxs-lookup"><span data-stu-id="2a220-188">To hire an existing worker into a new position, click **Change position** in the **Application status** drop down to initiate the transfer process.</span></span>






