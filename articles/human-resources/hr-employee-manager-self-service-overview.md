---
title: 员工和经理自助服务概述
description: 本文提供了员工和经理自助服务工作区的概述。
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cda6166bff926e362ee35221b9c204c2ead5503
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464144"
---
# <a name="employee-and-manager-self-service-overview"></a><span data-ttu-id="8725b-103">员工和经理自助服务概述</span><span class="sxs-lookup"><span data-stu-id="8725b-103">Employee and Manager self service overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8725b-104">本文提供了员工和经理自助服务工作区的概述。</span><span class="sxs-lookup"><span data-stu-id="8725b-104">This article provides an overview of the employee and manager self service workspace.</span></span>

## <a name="edit-personal-details"></a><span data-ttu-id="8725b-105">编辑个人详细信息</span><span class="sxs-lookup"><span data-stu-id="8725b-105">Edit personal details</span></span>

<span data-ttu-id="8725b-106">如果您需要添加或更改任何个人信息，请参阅[编辑个人信息](hr-employee-manager-self-service-edit-personal-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8725b-106">If you need to add or change any personal information, see [Edit personal information](hr-employee-manager-self-service-edit-personal-information.md).</span></span>

## <a name="user-not-assigned-to-a-worker-record"></a><span data-ttu-id="8725b-107">用户未分配给工作人员记录</span><span class="sxs-lookup"><span data-stu-id="8725b-107">User not assigned to a worker record</span></span>

<span data-ttu-id="8725b-108">如果您尚未将用户链接到 **用户** 页面中的 **工作人员** 记录，将显示以下消息：</span><span class="sxs-lookup"><span data-stu-id="8725b-108">If you haven't linked your user to a **Worker** record in the **Users** page, the following message will display:</span></span>

<span data-ttu-id="8725b-109">**您的用户 ID 未与系统中的员工记录关联。在二者关联之前，您将无法查看或更新您的信息。请与您的经理或支持团队联系以获取帮助。**</span><span class="sxs-lookup"><span data-stu-id="8725b-109">**Your user ID is not associated with your employee record in the system. You won't be able to view or update your information until it is. Contact your manager or support team for assistance.**</span></span>

<span data-ttu-id="8725b-110">要将用户与 **工作人员** 记录关联，请导航到 **用户** 并选择用户。</span><span class="sxs-lookup"><span data-stu-id="8725b-110">To associate a user with a **Worker** record, navigate to **Users** and select the user.</span></span> <span data-ttu-id="8725b-111">选择 **编辑**，在窗体的 **人员** 字段中添加相应的工作人员，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8725b-111">Select **Edit**, add the corresponding worker in the **Person** field on the form, and the select **Save**.</span></span> <span data-ttu-id="8725b-112">您现在应该可以访问“员工自助服务”。</span><span class="sxs-lookup"><span data-stu-id="8725b-112">You should now have access to Employee self service.</span></span>

## <a name="security-requirements-for-employee-and-manager-self-service"></a><span data-ttu-id="8725b-113">员工和经理自助服务的安全性要求</span><span class="sxs-lookup"><span data-stu-id="8725b-113">Security requirements for Employee and Manager self service</span></span>

<span data-ttu-id="8725b-114">员工和经理自助服务需要两个安全角色：</span><span class="sxs-lookup"><span data-stu-id="8725b-114">Employee and Manager self service require two security roles:</span></span>

- <span data-ttu-id="8725b-115">员工需要员工角色。</span><span class="sxs-lookup"><span data-stu-id="8725b-115">Employees require the Employee role.</span></span>
- <span data-ttu-id="8725b-116">经理同时需要员工和经理角色。</span><span class="sxs-lookup"><span data-stu-id="8725b-116">Managers require both the Employee and Manager roles.</span></span>

>[!NOTE]
><span data-ttu-id="8725b-117">您还可以使用自定义角色来访问员工和经理自助服务，只要它们已被授予对员工和经理工作区的访问权限。</span><span class="sxs-lookup"><span data-stu-id="8725b-117">You can also use custom roles to access Employee and Manager self service as long as they've been granted access to Employee and Manager workspaces.</span></span><br>
><span data-ttu-id="8725b-118">经理对员工信息的访问基于 Human Resources 中定义的当前职位行层次结构。</span><span class="sxs-lookup"><span data-stu-id="8725b-118">Manager access to employee information is based on the current position line hierarchy defined in Human Resources.</span></span>

## <a name="employee-self-service"></a><span data-ttu-id="8725b-119">员工自助服务</span><span class="sxs-lookup"><span data-stu-id="8725b-119">Employee self service</span></span>

<span data-ttu-id="8725b-120">**我的信息** 选项卡显示员工自助服务的以下信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-120">The **My information** tab displays the following information for Employee self service.</span></span>  

### <a name="summary"></a><span data-ttu-id="8725b-121">摘要</span><span class="sxs-lookup"><span data-stu-id="8725b-121">Summary</span></span>

<span data-ttu-id="8725b-122">**分配给我的工作项** 显示分配给员工的所有审核和工作流项目。</span><span class="sxs-lookup"><span data-stu-id="8725b-122">**Work items assigned to me** displays all approvals and workflow items that are assigned to the employee.</span></span> <span data-ttu-id="8725b-123">您可以配置工作流项目以向用户发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="8725b-123">You can configure workflow items to send emails to the user.</span></span>

<span data-ttu-id="8725b-124">**分配给我的调查表** 显示所有直接分配给员工或组的计划的调查表。</span><span class="sxs-lookup"><span data-stu-id="8725b-124">**Questionnaires assigned to me** display all scheduled questionnaires assigned directly to the employee or group.</span></span>

<span data-ttu-id="8725b-125">**公司目录** 让员工可以查找与组织中的个人相关的信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-125">**Company directory** lets employees look up information related to individuals in the organization.</span></span> <span data-ttu-id="8725b-126">所有员工都可以使用公共联系信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-126">Public contact information is available to all employees.</span></span> <span data-ttu-id="8725b-127">公司目录仅限于员工已登录的公司。</span><span class="sxs-lookup"><span data-stu-id="8725b-127">The company directory is restricted to the company that the employee has signed into.</span></span>

<span data-ttu-id="8725b-128">**团队日历** 显示您团队的日历信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-128">**Team calendar** shows your team's calendar information.</span></span> <span data-ttu-id="8725b-129">有关详细信息，请参阅[查看团队和公司日历](hr-employee-self-service-calendar.md)。</span><span class="sxs-lookup"><span data-stu-id="8725b-129">For more information, see [View team and company calendars](hr-employee-self-service-calendar.md).</span></span>

### <a name="my-career-information"></a><span data-ttu-id="8725b-130">我的职业信息</span><span class="sxs-lookup"><span data-stu-id="8725b-130">My career information</span></span>

<span data-ttu-id="8725b-131">员工自助服务的 **我的职业信息** 部分包含与休假和缺勤、绩效管理、能力、福利、任务和附件相关的卡片。</span><span class="sxs-lookup"><span data-stu-id="8725b-131">The **My career information** section of Employee self-service contains cards related to Leave and Absence, Performance Management, Competencies, Benefits, Tasks, and Attachments.</span></span>

<span data-ttu-id="8725b-132">**休息时间余额** 卡显示所有已登记计划的余额。</span><span class="sxs-lookup"><span data-stu-id="8725b-132">The **Time Off Balances** card displays the balances for any enrolled plans.</span></span> <span data-ttu-id="8725b-133">此卡根据您的应计方式预测您的余额。</span><span class="sxs-lookup"><span data-stu-id="8725b-133">This card forecasts your balance based on your accrual method.</span></span> <span data-ttu-id="8725b-134">您可以输入和提交休息请求，之后请求将经过审核工作流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-134">You can enter and submit time-off requests, which will then go through an approval workflow process.</span></span> <span data-ttu-id="8725b-135">有关休假和缺勤的详细信息，请参阅[休假和缺勤概述](hr-leave-and-absence-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="8725b-135">For more information about Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

<span data-ttu-id="8725b-136">**任务** 卡显示分配给您的任务，允许您查看和管理它们。</span><span class="sxs-lookup"><span data-stu-id="8725b-136">The **Tasks** card displays tasks that are assigned to you and lets you view and manage them.</span></span>

<span data-ttu-id="8725b-137">**下一个注册的课程** 卡显示您注册的下一个课程。</span><span class="sxs-lookup"><span data-stu-id="8725b-137">The **Next Registered Course** card displays the next course you're registered for.</span></span> <span data-ttu-id="8725b-138">您可以查看和注册任何公开课程。</span><span class="sxs-lookup"><span data-stu-id="8725b-138">You can view and register for any open courses.</span></span> <span data-ttu-id="8725b-139">所有公开的可供注册的课程的状态为 **已开始**，允许员工自助注册以显示在此卡上。</span><span class="sxs-lookup"><span data-stu-id="8725b-139">All courses that are open for sign-up have a status of **Started**, and allow employees to self-register appear on this card.</span></span> <span data-ttu-id="8725b-140">根据您组织的设置，您的课程注册可能会经过审核流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-140">Depending on your organization's settings, your course registration might go through an approval process.</span></span>

<span data-ttu-id="8725b-141">**证书** 卡显示证书和最接近当前日期的证书的到期日期。</span><span class="sxs-lookup"><span data-stu-id="8725b-141">The **Certificates** card displays the certificate and expiration date of the certificate expiring closest to the current date.</span></span> <span data-ttu-id="8725b-142">您可以更新、添加或删除证书。</span><span class="sxs-lookup"><span data-stu-id="8725b-142">You can update, add, or remove certificates.</span></span> <span data-ttu-id="8725b-143">根据您组织的设置，证书更新可能会经过审核流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-143">Depending on your organization's settings, certificate updates might go through an approval process.</span></span>

<span data-ttu-id="8725b-144">**已计划的下一次审核** 卡显示您的下一次绩效审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-144">The **Next Scheduled Review** card displays your next performance review.</span></span> <span data-ttu-id="8725b-145">您可以从此卡开始新的审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-145">You can start a new review from this card.</span></span> <span data-ttu-id="8725b-146">您的经理或人力资源代表也可以发起审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-146">Your manager or HR representative can also initiate reviews.</span></span> <span data-ttu-id="8725b-147">根据组织的设置，您可能还可以从此卡查看、更新、提交、退出审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-147">Depending on your organization's settings, you might also be able to view, update, and submit exit reviews from this card.</span></span>

<span data-ttu-id="8725b-148">您可以使用 **绩效目标** 卡管理您的目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-148">You can manage your goals with the **Performance Goals** card.</span></span> <span data-ttu-id="8725b-149">此卡显示您所具有的每种状态（**未开始**、**正在跟踪** 和 **需要改进**）的目标数。</span><span class="sxs-lookup"><span data-stu-id="8725b-149">This card displays the number of goals you have in each status (**Not started**, **On track**, and **Needs improvement**).</span></span> <span data-ttu-id="8725b-150">您可以根据基于被分配角色的安全性来创建、更新和删除目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-150">You can create, update, and remove goals, depending on your assigned role-based security.</span></span> <span data-ttu-id="8725b-151">如果需要，可以从组或模板添加新目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-151">If you want, you can add new goals from groups or templates.</span></span> <span data-ttu-id="8725b-152">经理和人力资源也可以代表员工创建目标，并确定每个目标的详细程度。</span><span class="sxs-lookup"><span data-stu-id="8725b-152">Managers and HR can also create goals on behalf of employees and determine how detailed each goal will be.</span></span> <span data-ttu-id="8725b-153">经理和员工可以就目标进行协作，并更新活动、度量和状态。</span><span class="sxs-lookup"><span data-stu-id="8725b-153">Managers and employees can collaborate on goals and update activities, measurements, and status.</span></span> <span data-ttu-id="8725b-154">您还可以包含附件。</span><span class="sxs-lookup"><span data-stu-id="8725b-154">You can also include attachments.</span></span>

<span data-ttu-id="8725b-155">您可以在 **技能** 卡上查看您的现有技能。</span><span class="sxs-lookup"><span data-stu-id="8725b-155">You can view your existing skills on the **Skills** card.</span></span> <span data-ttu-id="8725b-156">您可以更新技能、添加新技能或删除不再相关的技能。</span><span class="sxs-lookup"><span data-stu-id="8725b-156">You can update skills, add new ones, or remove any that are no longer relevant.</span></span> <span data-ttu-id="8725b-157">根据您组织的设置，对技能的更改可能会经过审核流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-157">Depending on your organization's settings, changes to your skills might go through an approval process.</span></span>

<span data-ttu-id="8725b-158">您可以通过 **薪酬** 卡查看您当前的薪酬。</span><span class="sxs-lookup"><span data-stu-id="8725b-158">You can view your current compensation through the **Compensation** card.</span></span> <span data-ttu-id="8725b-159">选择 **显示** 查看您的年度付薪和上一次的增加金额。</span><span class="sxs-lookup"><span data-stu-id="8725b-159">Select **Show** to view your annual pay and last increase amount.</span></span> <span data-ttu-id="8725b-160">如果您受雇于多家公司，每个年度金额都会显示在卡上。</span><span class="sxs-lookup"><span data-stu-id="8725b-160">If you're employed in more than one company, each annual amount displays on the card.</span></span> <span data-ttu-id="8725b-161">要查看详细的薪酬历史记录，请选择年度薪水金额打开 **固定和可变薪酬历史记录** 窗体。</span><span class="sxs-lookup"><span data-stu-id="8725b-161">To view your detailed compensation history, select the annual salary amount to open the **Fixed and variable compensation history** form.</span></span> <span data-ttu-id="8725b-162">将来的薪酬不会在此窗体中显示。</span><span class="sxs-lookup"><span data-stu-id="8725b-162">Future compensation doesn't display in this form.</span></span> <span data-ttu-id="8725b-163">如果您有一份以上的工作，可以在此窗体中在公司之间切换来查看您的薪酬历史记录，无需登录每个公司。</span><span class="sxs-lookup"><span data-stu-id="8725b-163">If you have more than one employment, you can switch between companies within this form to view your compensation history without logging into each company.</span></span>

<span data-ttu-id="8725b-164">使用 **附件** 卡查看和管理文档。</span><span class="sxs-lookup"><span data-stu-id="8725b-164">View and manage documents with the **Attachments** card.</span></span> <span data-ttu-id="8725b-165">您可以管理所有 **外部** 附件。</span><span class="sxs-lookup"><span data-stu-id="8725b-165">You can manage all **External** attachments.</span></span> <span data-ttu-id="8725b-166">人力资源和员工均可通过员工自助服务或 **工作人员** 窗体添加附件。</span><span class="sxs-lookup"><span data-stu-id="8725b-166">Both HR and employees can add attachments through Employee self service or the **Worker** form.</span></span> <span data-ttu-id="8725b-167">附件默认设置为 **外部**。</span><span class="sxs-lookup"><span data-stu-id="8725b-167">Attachments are set to **External** by default.</span></span>

### <a name="additional-information"></a><span data-ttu-id="8725b-168">附加信息</span><span class="sxs-lookup"><span data-stu-id="8725b-168">Additional information</span></span>

<span data-ttu-id="8725b-169">此部分提供其他员工自助服务区域的链接，类似于 **我的职业信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="8725b-169">This section provides links to other Employee self service areas, similar to the **My Career Information** section.</span></span>

<span data-ttu-id="8725b-170">通过 **福利** 链接注册福利。</span><span class="sxs-lookup"><span data-stu-id="8725b-170">Sign up for benefits through the **Benefits** link.</span></span> <span data-ttu-id="8725b-171">有关福利管理的详细信息，请参阅[福利概述](hr-benefits-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8725b-171">For more information about Benefits management, see [Benefits overview](hr-benefits-management-overview.md)</span></span>

<span data-ttu-id="8725b-172">在 **绩效** 下，您可以选择 **绩效日记帐** 来创建同时用于绩效目标和审核的绩效日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8725b-172">Under **Performance**, you can select **Performance journals** to create performance journal entries to use on both performance goals and reviews.</span></span> <span data-ttu-id="8725b-173">您可以选择 **发送反馈** 为组织内的其他员工提供反馈。</span><span class="sxs-lookup"><span data-stu-id="8725b-173">You can select **Send feedback** to provide feedback for other employees within your organization.</span></span> <span data-ttu-id="8725b-174">根据组织的设置，电子邮件可能会发送给收件人、发件人和经理。</span><span class="sxs-lookup"><span data-stu-id="8725b-174">Depending on your organization's settings, emails might be sent to the recipient, sender, and managers.</span></span> <span data-ttu-id="8725b-175">您可以将反馈发送给组织内的所有员工。</span><span class="sxs-lookup"><span data-stu-id="8725b-175">You can send feedback to all employees within the organization.</span></span> <span data-ttu-id="8725b-176">发送反馈不受公司的限制。</span><span class="sxs-lookup"><span data-stu-id="8725b-176">Sending feedback isn't restricted by company.</span></span>

<span data-ttu-id="8725b-177">在 **能力** 下，您可以对 **课程**、**教育**、**诚信职位** 和 **专业经验** 进行更改。</span><span class="sxs-lookup"><span data-stu-id="8725b-177">Under **Competencies**, you can make changes to **Courses**, **Education**, **Positions of trust**, and **Professional experience**.</span></span> <span data-ttu-id="8725b-178">根据您组织的设置，对这些能力的更新可能会经过审核流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-178">Depending on your organization's settings, updates to these competencies might go through an approval process.</span></span>

<span data-ttu-id="8725b-179">您可以在 **组织** 下查看工作详细信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-179">You can view job details under **Organization**.</span></span> <span data-ttu-id="8725b-180">工作详细信息包括技能、证书以及您的主要职位的职责范围。</span><span class="sxs-lookup"><span data-stu-id="8725b-180">Job details include skills, certificates, and areas of responsibility for your primary position.</span></span> <span data-ttu-id="8725b-181">您还可以查看登记到您名下的任何借出设备。</span><span class="sxs-lookup"><span data-stu-id="8725b-181">You can also see any loaned equipment checked out to you.</span></span> <span data-ttu-id="8725b-182">根据您组织的设置，对借出设备的更改可能会经过审核流程。</span><span class="sxs-lookup"><span data-stu-id="8725b-182">Depending on your organization's settings, changes to loaned equipment might go through an approval process.</span></span>

<span data-ttu-id="8725b-183">在 **调查表** 下，您可以看到完整的调查表。</span><span class="sxs-lookup"><span data-stu-id="8725b-183">Under **Questionnaire**, you can see completed questionnaires.</span></span> <span data-ttu-id="8725b-184">您还可以查看尚未完成的公司范围的调查表。</span><span class="sxs-lookup"><span data-stu-id="8725b-184">You can also see company-wide questionnaires that haven't been completed.</span></span> <span data-ttu-id="8725b-185">您可以选择在任何时间完成调查表。</span><span class="sxs-lookup"><span data-stu-id="8725b-185">You can choose to complete a questionnaire at any time.</span></span> <span data-ttu-id="8725b-186">调查表的作者可以确定时间范围以及该调查表适用的对象。</span><span class="sxs-lookup"><span data-stu-id="8725b-186">The author of the questionnaire can determine the time frame and for whom the questionnaire is applicable.</span></span>

<span data-ttu-id="8725b-187">您可以在 **人力资源参数** 中配置用户定义的链接。</span><span class="sxs-lookup"><span data-stu-id="8725b-187">You can configure user-defined links in **Human Resources parameters**.</span></span> <span data-ttu-id="8725b-188">例如，您可以定义指向工资单、年终文档或外部解决方案的链接。</span><span class="sxs-lookup"><span data-stu-id="8725b-188">For example, you can define links to pay statements, year-end documentation, or external solutions.</span></span> <span data-ttu-id="8725b-189">这些链接显示在此部分的底部，但您可以使用个性化设置来移动它们。</span><span class="sxs-lookup"><span data-stu-id="8725b-189">These links display at the bottom of this section, but you can move them by using personalization.</span></span>

<span data-ttu-id="8725b-190">您还可以通过在员工自助服务工作区嵌入 Power Apps 来创建其他选项卡。</span><span class="sxs-lookup"><span data-stu-id="8725b-190">You can also create additional tabs by embedding Power Apps within the Employee self service workspace.</span></span> <span data-ttu-id="8725b-191">使用 **设置** 菜单个性化任何 Power Apps 的页面。</span><span class="sxs-lookup"><span data-stu-id="8725b-191">Use the **Settings** menu to personalize the page with any Power Apps.</span></span> <span data-ttu-id="8725b-192">在 **设置** 菜单中，您可以选择添加 Power App、完成详细信息、插入应用。</span><span class="sxs-lookup"><span data-stu-id="8725b-192">In the **Settings** menu, you can choose to add a Power App, complete the details, and insert the app.</span></span> <span data-ttu-id="8725b-193">默认情况下，Power Apps 显示为序列中的第一个选项卡。</span><span class="sxs-lookup"><span data-stu-id="8725b-193">By default, Power Apps appears as the first tab in the sequence.</span></span> <span data-ttu-id="8725b-194">您可以使用标准个性化设置更改此顺序。</span><span class="sxs-lookup"><span data-stu-id="8725b-194">You can change the order by using standard personalization.</span></span>

## <a name="my-team"></a><span data-ttu-id="8725b-195">我的团队</span><span class="sxs-lookup"><span data-stu-id="8725b-195">My team</span></span>

<span data-ttu-id="8725b-196">**我的团队** 选项卡显示经理自助服务的以下信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-196">The **My team** tab displays the following information for Manager self service.</span></span> <span data-ttu-id="8725b-197">只有经理可以访问 **我的团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8725b-197">Only managers can access the **My team** tab.</span></span>

### <a name="personnel-actions"></a><span data-ttu-id="8725b-198">人事行动</span><span class="sxs-lookup"><span data-stu-id="8725b-198">Personnel actions</span></span>

<span data-ttu-id="8725b-199">人事行动根据 **人力资源共享参数** 和 **人力资源参数** 中的配置选项显示。</span><span class="sxs-lookup"><span data-stu-id="8725b-199">Personnel actions display based on configuration options within **Human resources shared parameters** and **Human resources parameters**.</span></span> <span data-ttu-id="8725b-200">为 **工作人员** 启用后，人事行动将启用新的菜单选项，包括：</span><span class="sxs-lookup"><span data-stu-id="8725b-200">When enabled for **Workers**, personnel actions enable new menu options, including:</span></span>

- <span data-ttu-id="8725b-201">**请求新员工**</span><span class="sxs-lookup"><span data-stu-id="8725b-201">**Request new employee**</span></span>
- <span data-ttu-id="8725b-202">**请求新的合同工**</span><span class="sxs-lookup"><span data-stu-id="8725b-202">**Request new contractor**</span></span>
- <span data-ttu-id="8725b-203">**请求工作人员重新分配**</span><span class="sxs-lookup"><span data-stu-id="8725b-203">**Request worker reassignment**</span></span>
- <span data-ttu-id="8725b-204">**请求终止**</span><span class="sxs-lookup"><span data-stu-id="8725b-204">**Request termination**</span></span>
- <span data-ttu-id="8725b-205">**请求更改薪酬**</span><span class="sxs-lookup"><span data-stu-id="8725b-205">**Request compensation change**</span></span>

<span data-ttu-id="8725b-206">您可以将这些选项配置为经过可选的审核与审批工作流。</span><span class="sxs-lookup"><span data-stu-id="8725b-206">You can configure these options to go through an optional review and approval workflow.</span></span>

<span data-ttu-id="8725b-207">启用 **职位行动** 将启用以下选项：</span><span class="sxs-lookup"><span data-stu-id="8725b-207">Enabling **Position actions** enable the following options:</span></span>

- <span data-ttu-id="8725b-208">**请求新职位**</span><span class="sxs-lookup"><span data-stu-id="8725b-208">**Request new position**</span></span>
- <span data-ttu-id="8725b-209">**请求更改职位详细信息**</span><span class="sxs-lookup"><span data-stu-id="8725b-209">**Request change to position details**</span></span>

<span data-ttu-id="8725b-210">您还可以将这些选项配置为经过可选的审核与审批工作流。</span><span class="sxs-lookup"><span data-stu-id="8725b-210">You can also configure these options to go through an optional review and approval workflow.</span></span>

### <a name="summary"></a><span data-ttu-id="8725b-211">摘要</span><span class="sxs-lookup"><span data-stu-id="8725b-211">Summary</span></span>

<span data-ttu-id="8725b-212">**摘要** 部分中的信息取决于人力资源在 **人力资源参数** 中选择的选项。</span><span class="sxs-lookup"><span data-stu-id="8725b-212">Information in the **Summary** section depends on the options HR has selected in **Human resource parameters**.</span></span> <span data-ttu-id="8725b-213">在 **人力资源参数** 页面的 **经理自助服务** 选项卡上，您可以配置显示即将过期的记录和空缺职位的选项。</span><span class="sxs-lookup"><span data-stu-id="8725b-213">On the **Manager self service** tab of the **Human Resources parameters** page, you can configure options for displaying expiring records and open positions.</span></span> <span data-ttu-id="8725b-214">启用这些选项将确定经理可以在 **摘要** 部分看到的信息。</span><span class="sxs-lookup"><span data-stu-id="8725b-214">Enabling these options determines what managers can see in the **Summary** section.</span></span>

<span data-ttu-id="8725b-215">您可以为经理配置以下磁贴：</span><span class="sxs-lookup"><span data-stu-id="8725b-215">You can configure the following tiles for managers:</span></span>

- <span data-ttu-id="8725b-216">**我的团队的过期证书**</span><span class="sxs-lookup"><span data-stu-id="8725b-216">**Certificates expiring for my team**</span></span>
- <span data-ttu-id="8725b-217">**我的团队的即将过期的标识号**</span><span class="sxs-lookup"><span data-stu-id="8725b-217">**Identification numbers expiring for my team**</span></span>
- <span data-ttu-id="8725b-218">**我的团队的即将过期的检查**</span><span class="sxs-lookup"><span data-stu-id="8725b-218">**Probations expiring for my team**</span></span>
- <span data-ttu-id="8725b-219">**我的团队的即将过期的筛选**</span><span class="sxs-lookup"><span data-stu-id="8725b-219">**Screenings expiring for my team**</span></span>
- <span data-ttu-id="8725b-220">**我的团队的即将过期的测试**</span><span class="sxs-lookup"><span data-stu-id="8725b-220">**Tests expiring for my team**</span></span>
- <span data-ttu-id="8725b-221">**直接和/或间接下属空缺职位**</span><span class="sxs-lookup"><span data-stu-id="8725b-221">**Open positions for direct and/or extended reports**</span></span>
- <span data-ttu-id="8725b-222">**我的团队的待处理休息请求**</span><span class="sxs-lookup"><span data-stu-id="8725b-222">**Pending time off requests for my team**</span></span>
- <span data-ttu-id="8725b-223">**团队技能评估**</span><span class="sxs-lookup"><span data-stu-id="8725b-223">**Team skills assessment**</span></span>
- <span data-ttu-id="8725b-224">**技能差距分析**</span><span class="sxs-lookup"><span data-stu-id="8725b-224">**Skill gap analysis**</span></span>
- <span data-ttu-id="8725b-225">**团队绩效日记帐**</span><span class="sxs-lookup"><span data-stu-id="8725b-225">**Team performance journals**</span></span>
- <span data-ttu-id="8725b-226">**团队绩效目标**</span><span class="sxs-lookup"><span data-stu-id="8725b-226">**Team performance goals**</span></span>
- <span data-ttu-id="8725b-227">**团队绩效审核**</span><span class="sxs-lookup"><span data-stu-id="8725b-227">**Team performance reviews**</span></span>
- <span data-ttu-id="8725b-228">**正离职的工作人员**</span><span class="sxs-lookup"><span data-stu-id="8725b-228">**Exiting workers**</span></span>

<span data-ttu-id="8725b-229">您可以配置以下选项，让经理可以代表他们的直接下属进行更改或添加休假请求：</span><span class="sxs-lookup"><span data-stu-id="8725b-229">You can configure the following options for managers to make changes or add leave requests on behalf of their direct reports:</span></span>

- <span data-ttu-id="8725b-230">证书</span><span class="sxs-lookup"><span data-stu-id="8725b-230">Certificates</span></span>
- <span data-ttu-id="8725b-231">课程</span><span class="sxs-lookup"><span data-stu-id="8725b-231">Courses</span></span>
- <span data-ttu-id="8725b-232">借出物品</span><span class="sxs-lookup"><span data-stu-id="8725b-232">Loan items</span></span>
- <span data-ttu-id="8725b-233">技能</span><span class="sxs-lookup"><span data-stu-id="8725b-233">Skills</span></span>
- <span data-ttu-id="8725b-234">休假和缺勤请求</span><span class="sxs-lookup"><span data-stu-id="8725b-234">Leave and absence requests</span></span>

### <a name="my-team-information"></a><span data-ttu-id="8725b-235">我的团队信息</span><span class="sxs-lookup"><span data-stu-id="8725b-235">My team information</span></span>

<span data-ttu-id="8725b-236">我的团队信息让经理可以查看和更新直接和间接下属。</span><span class="sxs-lookup"><span data-stu-id="8725b-236">My team information allows managers to view and update direct and extended reports.</span></span> <span data-ttu-id="8725b-237">要访问间接下属，请选择具有直接下属的员工，然后在卡上选择 **查看团队**。</span><span class="sxs-lookup"><span data-stu-id="8725b-237">To access extended reports, select the employee who has directs, and then choose **View team** on the card.</span></span> <span data-ttu-id="8725b-238">所有相同的选项都会作为直接下属应用于间接下属。</span><span class="sxs-lookup"><span data-stu-id="8725b-238">All of the same options apply to extended reports as direct reports.</span></span> 

#### <a name="summary-tab"></a><span data-ttu-id="8725b-239">“摘要”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-239">Summary tab</span></span>

<span data-ttu-id="8725b-240">**摘要** 选项卡可让您快速查看您的直接下属。</span><span class="sxs-lookup"><span data-stu-id="8725b-240">The **Summary** tab provides a quick view of your direct reports.</span></span> <span data-ttu-id="8725b-241">如果直接下属也有向他们报告工作的工作人员，卡会在上面部分显示直接下属的数量，以及 **查看团队** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8725b-241">If a direct report also has workers reporting to them, the card displays the number of direct reports in the upper section, along with a **View team** button.</span></span> <span data-ttu-id="8725b-242">每个卡上方的选项将应用于所选员工。</span><span class="sxs-lookup"><span data-stu-id="8725b-242">Options above each card apply to the selected employee.</span></span> <span data-ttu-id="8725b-243">例如，如果您要代表员工输入休假请求，请选择该员工，然后选择卡上方的 **请求休息**。</span><span class="sxs-lookup"><span data-stu-id="8725b-243">For example, if you want to enter a leave request on behalf of an employee, you select the employee and then choose **Request time off** above the cards.</span></span> 

<span data-ttu-id="8725b-244">如果您在选择员工后选择 **详细信息** 按钮，将显示以下选项：</span><span class="sxs-lookup"><span data-stu-id="8725b-244">If you select the **Details** button after selecting an employee, the following options display:</span></span>

- <span data-ttu-id="8725b-245">**证书**</span><span class="sxs-lookup"><span data-stu-id="8725b-245">**Certificates**</span></span>
- <span data-ttu-id="8725b-246">**薪酬**</span><span class="sxs-lookup"><span data-stu-id="8725b-246">**Compensation**</span></span>
- <span data-ttu-id="8725b-247">**课程**</span><span class="sxs-lookup"><span data-stu-id="8725b-247">**Courses**</span></span>
- <span data-ttu-id="8725b-248">**审查**</span><span class="sxs-lookup"><span data-stu-id="8725b-248">**Reviews**</span></span>
- <span data-ttu-id="8725b-249">**休假**</span><span class="sxs-lookup"><span data-stu-id="8725b-249">**Time off**</span></span>
- <span data-ttu-id="8725b-250">**借出物品**</span><span class="sxs-lookup"><span data-stu-id="8725b-250">**Loaned items**</span></span>
- <span data-ttu-id="8725b-251">**绩效目标**</span><span class="sxs-lookup"><span data-stu-id="8725b-251">**Performance goals**</span></span>
- <span data-ttu-id="8725b-252">**已登记的课程**</span><span class="sxs-lookup"><span data-stu-id="8725b-252">**Registered courses**</span></span>
- <span data-ttu-id="8725b-253">**技能**</span><span class="sxs-lookup"><span data-stu-id="8725b-253">**Skills**</span></span>
- <span data-ttu-id="8725b-254">**发送反馈**</span><span class="sxs-lookup"><span data-stu-id="8725b-254">**Send feedback**</span></span>

<span data-ttu-id="8725b-255">根据组织的设置，您可以进行更改或只能查看。</span><span class="sxs-lookup"><span data-stu-id="8725b-255">Depending on your organization's settings, you can either make changes or view only.</span></span>

#### <a name="position-tab"></a><span data-ttu-id="8725b-256">“职位”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-256">Position tab</span></span>

<span data-ttu-id="8725b-257">**职位** 选项卡在员工的主要职位中提供员工的摘要视图。</span><span class="sxs-lookup"><span data-stu-id="8725b-257">The **Positions** tab provides a summary view of employees in their primary position.</span></span> <span data-ttu-id="8725b-258">姓名、职位名称和部门显示在每张卡的标题区域内。</span><span class="sxs-lookup"><span data-stu-id="8725b-258">Name, tile, and department displays in the heading area of each card.</span></span> <span data-ttu-id="8725b-259">此卡包括：</span><span class="sxs-lookup"><span data-stu-id="8725b-259">This card includes:</span></span>

- <span data-ttu-id="8725b-260">**受聘日期** - 从工作人员窗体的工作人员摘要部分显示</span><span class="sxs-lookup"><span data-stu-id="8725b-260">**Seniority date** - Displayed from the worker summary section of the worker form</span></span>
- <span data-ttu-id="8725b-261">**工作年限** - 根据员工的雇用开始日期计算</span><span class="sxs-lookup"><span data-stu-id="8725b-261">**Years of service** - Calculated based on the employee's employment start date</span></span>
- <span data-ttu-id="8725b-262">**先前职位数** - 根据职位历史记录，选择此数字将打开所有先前曾担任职位的详细视图</span><span class="sxs-lookup"><span data-stu-id="8725b-262">**Number of previous positions** - Based on position history, selecting this number opens the detailed view of all previously held positions</span></span>
- <span data-ttu-id="8725b-263">**出生日期** - 员工出生日期的月和日</span><span class="sxs-lookup"><span data-stu-id="8725b-263">**Birth date** - The month and day of the employee's birth date</span></span>

<span data-ttu-id="8725b-264">您可以查看直接和间接下属的职位数据。</span><span class="sxs-lookup"><span data-stu-id="8725b-264">You can view position data for both direct and extended reports.</span></span>

#### <a name="compensation-tab"></a><span data-ttu-id="8725b-265">“薪酬”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-265">Compensation tab</span></span>

<span data-ttu-id="8725b-266">**薪酬** 选项卡显示员工的年度薪水。</span><span class="sxs-lookup"><span data-stu-id="8725b-266">The **Compensation** tab displays the employee's annual salary.</span></span> <span data-ttu-id="8725b-267">公司标识符在薪水金额下显示。</span><span class="sxs-lookup"><span data-stu-id="8725b-267">A company identifier displays under the salary amount.</span></span> <span data-ttu-id="8725b-268">如果某个员工有多个工作并且从多个法人那里领工资，该员工将有多个薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="8725b-268">If an employee has more than one employment and is getting paid from multiple legal entities, the employee will have multiple compensation plans.</span></span> <span data-ttu-id="8725b-269">若要在不切换公司的情况下跨法人查看所有薪酬计划，您必须在 **Human Resources > 共享参数 > 高级访问 > 启用跨公司薪酬** 下启用跨薪酬。</span><span class="sxs-lookup"><span data-stu-id="8725b-269">To see all compensation plans across legal entities without switching companies, you must enable cross compensation under **Human Resources > Shared parameters > Advanced access > Enable cross company compensation**.</span></span>

<span data-ttu-id="8725b-270">要查看薪酬历史记录，请选择薪水金额打开 **详细信息** 窗体。</span><span class="sxs-lookup"><span data-stu-id="8725b-270">To view compensation history, select the salary amount to open the **Details** form.</span></span> <span data-ttu-id="8725b-271">仅当前和历史固定和可变薪酬记录显示在 **薪酬** 窗体中。</span><span class="sxs-lookup"><span data-stu-id="8725b-271">Only current and historical fixed and variable compensation records display in the **Compensation** form.</span></span> <span data-ttu-id="8725b-272">如果某个员工有多个工作，您可以在公司之间切换以查看每个公司的薪酬历史记录，或在 Human Resources 共享参数中启用跨公司薪酬以查看所有薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="8725b-272">If an employee has more than one employment, you can switch between companies to view compensation history in each company or enable cross company compensation in Human Resources Shared parameters to view all compensation plans.</span></span>

<span data-ttu-id="8725b-273">您可以查看直接和间接下属的薪酬。</span><span class="sxs-lookup"><span data-stu-id="8725b-273">You can view compensation for both direct and extended reports.</span></span>

#### <a name="leave-and-absence-tab"></a><span data-ttu-id="8725b-274">“休假和缺勤”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-274">Leave and absence tab</span></span>

<span data-ttu-id="8725b-275">**休假和缺勤** 选项卡显示有活动的员工的最高余额。</span><span class="sxs-lookup"><span data-stu-id="8725b-275">The **Leave and absence** tab displays the top balances for employees that have activity.</span></span> <span data-ttu-id="8725b-276">要执行操作或查看活动的完整列表，请选择 **详细信息**，然后选择 **休息时间**。</span><span class="sxs-lookup"><span data-stu-id="8725b-276">To take action or view a full list of activities, select **Details** and then select **Time off**.</span></span> <span data-ttu-id="8725b-277">在 **休息时间** 窗体中，您可以查看余额、请求、批准的休息时间和预测余额，以帮助员工更好地管理时间。</span><span class="sxs-lookup"><span data-stu-id="8725b-277">On the **Time off** form, you can view balances, requests, approved time off, and forecast balances to help employees better manage time.</span></span> <span data-ttu-id="8725b-278">根据组织的设置，您还可以为直接和间接下属请求休息时间。</span><span class="sxs-lookup"><span data-stu-id="8725b-278">Depending on your organization's settings, you can also request time off for your directs and extended reports.</span></span>

#### <a name="performance-goals-tab"></a><span data-ttu-id="8725b-279">“绩效目标”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-279">Performance goals tab</span></span>

<span data-ttu-id="8725b-280">**绩效目标** 选项卡按状态汇总绩效目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-280">The **Performance goals** tab summarizes performance goals by status.</span></span> <span data-ttu-id="8725b-281">选择一个状态编号或从 **详细信息** 选择绩效目标可以查看员工的所有目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-281">Select a number for a status or select performance goals from the **Details** to see all goals for an employee.</span></span> <span data-ttu-id="8725b-282">经理和员工可以在目标的持续时间内根据需要更新目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-282">Managers and employees can update goals as needed over the duration of the goal.</span></span>

<span data-ttu-id="8725b-283">经理可以通过 **我的团队** 的 **摘要** 部分中的 **团队绩效目标** 磁贴查看其团队的所有目标。</span><span class="sxs-lookup"><span data-stu-id="8725b-283">Managers can see all goals for their team through the **Team performance goals** tile in the **Summary** section of **My team**.</span></span>

#### <a name="reviews-tab"></a><span data-ttu-id="8725b-284">“审核”选项卡</span><span class="sxs-lookup"><span data-stu-id="8725b-284">Reviews tab</span></span>

<span data-ttu-id="8725b-285">**审核** 选项卡汇总员工所有的每个状态的审核：**进行中**、**审核就绪** 和 **最终审核**。</span><span class="sxs-lookup"><span data-stu-id="8725b-285">The **Reviews** tab summarizes the reviews the employee has in each state: **In progress**, **Ready for review**, and **Final review**.</span></span> <span data-ttu-id="8725b-286">要访问员工的审核，请选择 **详细信息** 按钮，然后选择要协作进行的审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-286">To access an employee's review, select the **Details** button and then select reviews to collaborate on.</span></span> <span data-ttu-id="8725b-287">根据审核在工作流程中的位置，您可以查看审核是否可以更新。</span><span class="sxs-lookup"><span data-stu-id="8725b-287">Based on where a review is within the workflow process, you can see if the review is available for updating.</span></span> 

<span data-ttu-id="8725b-288">您可以通过 **我的团队** 的 **摘要** 部分中的 **团队绩效审核** 磁贴查看您团队的所有审核。</span><span class="sxs-lookup"><span data-stu-id="8725b-288">You can see all reviews for your team through the **Team performance reviews** tile in the **Summary** section of **My team**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]