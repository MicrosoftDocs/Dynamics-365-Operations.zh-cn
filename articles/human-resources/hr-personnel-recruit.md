---
title: 招聘工作应聘者
description: 本主题显示如何在 Dynamics 365 Human Resources 中招聘应聘者。
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 529f419a4e3e4e8807c6938fd2425ae01ce282f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051801"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="e9230-103">招聘工作应聘者</span><span class="sxs-lookup"><span data-stu-id="e9230-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9230-104">Dynamics 365 Human Resources 帮助您管理招聘请求。</span><span class="sxs-lookup"><span data-stu-id="e9230-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="e9230-105">它还帮助您无缝地将工作应聘者转换为员工。</span><span class="sxs-lookup"><span data-stu-id="e9230-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="e9230-106">如果您的组织使用单独的招聘应用程序，您的招聘流程可能包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e9230-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="e9230-107">在 Human Resources 中输入您的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="e9230-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="e9230-108">从招聘应用程序接收 Human Resources 中的应聘者引荐。</span><span class="sxs-lookup"><span data-stu-id="e9230-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="e9230-109">在 Human Resources 中完成应聘者审批流程。</span><span class="sxs-lookup"><span data-stu-id="e9230-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="e9230-110">如果您不使用单独的招聘应用程序，还可以在 Human Resources 中手动管理应聘者。</span><span class="sxs-lookup"><span data-stu-id="e9230-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e9230-111">如果您是管理员或开发人员，并且想要将 Human Resources 与第三方招聘应用程序集成，请参阅[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)和[配置 Dataverse 虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="e9230-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="e9230-112">您还可以在 [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) 上找到招聘集成应用。</span><span class="sxs-lookup"><span data-stu-id="e9230-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="e9230-113">若要试用与 LinkedIn Talent Hub 集成的预览功能，请参阅[与 LinkedIn Talent Hub 集成](hr-admin-integration-linkedin.md)。</span><span class="sxs-lookup"><span data-stu-id="e9230-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="e9230-114">启用招聘请求</span><span class="sxs-lookup"><span data-stu-id="e9230-114">Enable recruiting requests</span></span>

<span data-ttu-id="e9230-115">如果要在 Human Resources 中提交招聘请求，您必须先在 **人力资源共享参数** 中启用该功能。</span><span class="sxs-lookup"><span data-stu-id="e9230-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="e9230-116">在 **人事管理** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="e9230-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="e9230-117">在 **设置** 下，选择 **Human Resources 共享参数**。</span><span class="sxs-lookup"><span data-stu-id="e9230-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="e9230-118">在 **招聘** 选项卡上，在 **招聘** 下，将 **启用招聘请求** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="e9230-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="e9230-119">添加招聘请求位置</span><span class="sxs-lookup"><span data-stu-id="e9230-119">Add a recruiting request location</span></span>

<span data-ttu-id="e9230-120">如果您的组织有多个位置，可以添加它们，以便请求者可以选择新招聘的工作位置。</span><span class="sxs-lookup"><span data-stu-id="e9230-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="e9230-121">位置将包含在工作发布中。</span><span class="sxs-lookup"><span data-stu-id="e9230-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="e9230-122">在搜索栏中，输入 **招聘请求位置**。</span><span class="sxs-lookup"><span data-stu-id="e9230-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="e9230-123">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e9230-123">Select **New**.</span></span>

3. <span data-ttu-id="e9230-124">在 **招聘请求位置** 字段中，输入位置名称。</span><span class="sxs-lookup"><span data-stu-id="e9230-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![添加招聘请求位置](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="e9230-126">在 **描述** 中，输入位置的描述。</span><span class="sxs-lookup"><span data-stu-id="e9230-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="e9230-127">在 **位置** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="e9230-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="e9230-128">如果显示 **新地址** 弹出窗口，输入位置的地址。</span><span class="sxs-lookup"><span data-stu-id="e9230-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![请输入地址](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="e9230-130">在 **联系人信息** 下，输入该位置的联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="e9230-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="e9230-131">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e9230-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="e9230-132">添加招聘请求</span><span class="sxs-lookup"><span data-stu-id="e9230-132">Add a recruiting request</span></span>

<span data-ttu-id="e9230-133">经理可以在 Human Resources 中提交招聘请求。</span><span class="sxs-lookup"><span data-stu-id="e9230-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="e9230-134">如果您使用单独的招聘应用程序，完成这些步骤将发送一个招聘请求，并在该应用程序中开始招聘流程。</span><span class="sxs-lookup"><span data-stu-id="e9230-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="e9230-135">否则，完成此过程以开始您自己的内部招聘流程的工作流。</span><span class="sxs-lookup"><span data-stu-id="e9230-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="e9230-136">选择 **员工自助服务**。</span><span class="sxs-lookup"><span data-stu-id="e9230-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e9230-137">选择 **我的团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9230-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e9230-138">选择 **招聘请求**。</span><span class="sxs-lookup"><span data-stu-id="e9230-138">Select  **Request to recruit**.</span></span>

   ![开始招聘请求](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="e9230-140">填写 **描述**、**工作** 和 **预计开始日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="e9230-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![完成招聘请求](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="e9230-142">选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="e9230-142">Select **Continue**.</span></span> <span data-ttu-id="e9230-143">将显示您的职位的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="e9230-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="e9230-144">在 **常规** 下，从 **招聘人员** 下拉菜单中选择招聘人员，然后从 **招聘请求位置** 中选择位置。</span><span class="sxs-lookup"><span data-stu-id="e9230-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="e9230-145">在 **工作** 下，根据需要更改任何信息，然后选择 **通过工作创建详细信息**。</span><span class="sxs-lookup"><span data-stu-id="e9230-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![通过作业创建详细信息](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="e9230-147">将使用您输入的工作的默认信息填充招聘请求的其余部分。</span><span class="sxs-lookup"><span data-stu-id="e9230-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="e9230-148">在 **外部描述** 下，输入一个外部工作描述。</span><span class="sxs-lookup"><span data-stu-id="e9230-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="e9230-149">在 **职位** 下，选择 **添加**，然后为此招聘请求选择一个职位。</span><span class="sxs-lookup"><span data-stu-id="e9230-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![添加职位](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="e9230-151">在 **技能** 下，选择 **添加**，然后选择一项技能。</span><span class="sxs-lookup"><span data-stu-id="e9230-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="e9230-152">在 **教育要求** 下，选择 **添加**，然后从 **教育** 和 **教育程度** 下拉菜单中选择值。</span><span class="sxs-lookup"><span data-stu-id="e9230-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![添加教育要求](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="e9230-154">在 **注释** 下，根据需要添加注释。</span><span class="sxs-lookup"><span data-stu-id="e9230-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="e9230-155">在 **薪酬** 下，从 **级别** 下拉菜单中选择一个级别，然后根据需要调整 **低阈值**、**控制点** 和 **高阈值**。</span><span class="sxs-lookup"><span data-stu-id="e9230-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="e9230-156">在完成招聘请求并且您准备好开始招聘流程时，在菜单栏中选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="e9230-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![激活招聘请求](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="e9230-158">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e9230-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="e9230-159">查看和编辑您的招聘请求</span><span class="sxs-lookup"><span data-stu-id="e9230-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="e9230-160">如果您是经理，并且想要查看自己的请求：</span><span class="sxs-lookup"><span data-stu-id="e9230-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="e9230-161">选择 **员工自助服务**。</span><span class="sxs-lookup"><span data-stu-id="e9230-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e9230-162">选择 **我的团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9230-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e9230-163">在 **我的团队信息** 下，选择 **招聘请求** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e9230-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![选择“招聘请求”选项卡](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="e9230-165">若要查看或编辑招聘请求，请在网格中选择它。</span><span class="sxs-lookup"><span data-stu-id="e9230-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="e9230-166">如果您是 HR 专业人员，并且想要查看所有招聘请求：</span><span class="sxs-lookup"><span data-stu-id="e9230-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="e9230-167">选择 **人事管理**。</span><span class="sxs-lookup"><span data-stu-id="e9230-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e9230-168">选择 **招聘请求**。</span><span class="sxs-lookup"><span data-stu-id="e9230-168">Select **Recruiting requests**.</span></span>

   ![在人事管理中查看招聘请求](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="e9230-170">若要查看或编辑招聘请求，请在网格中选择它。</span><span class="sxs-lookup"><span data-stu-id="e9230-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="e9230-171">添加或编辑应聘者个人资料</span><span class="sxs-lookup"><span data-stu-id="e9230-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="e9230-172">如果您的组织已与另一个应用程序集成以管理招聘请求，招聘请求将转发到该应用程序。</span><span class="sxs-lookup"><span data-stu-id="e9230-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="e9230-173">然后，招聘应用程序将应聘者信息发送回 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="e9230-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="e9230-174">否则，您可以遵循自己的内部招聘流程并手动输入应聘者信息。</span><span class="sxs-lookup"><span data-stu-id="e9230-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="e9230-175">选择 **人事管理**。</span><span class="sxs-lookup"><span data-stu-id="e9230-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e9230-176">选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="e9230-176">Select **Links**.</span></span>

3. <span data-ttu-id="e9230-177">在 **招聘** 下，选择 **应聘者**。</span><span class="sxs-lookup"><span data-stu-id="e9230-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![查看应聘者](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="e9230-179">若要添加应聘者，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e9230-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="e9230-180">若要编辑现有应聘者，请从列表中选择应聘者，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e9230-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="e9230-181">将显示应聘者个人资料。</span><span class="sxs-lookup"><span data-stu-id="e9230-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="e9230-182">在 **应聘者汇总** 下，根据需要输入或编辑应聘者信息。</span><span class="sxs-lookup"><span data-stu-id="e9230-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="e9230-183">在 **招聘请求** 下，选择将应聘者链接到的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="e9230-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="e9230-184">然后，根据需要填写 **预计开始日期**、**雇用经理**、**职位** 和 **描述** 字段。</span><span class="sxs-lookup"><span data-stu-id="e9230-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![链接到招聘请求](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="e9230-186">填写要包含在应聘者记录中的以下区域中的所有信息：</span><span class="sxs-lookup"><span data-stu-id="e9230-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="e9230-187">**注释**</span><span class="sxs-lookup"><span data-stu-id="e9230-187">**Comments**</span></span>
   - <span data-ttu-id="e9230-188">**工作经验**</span><span class="sxs-lookup"><span data-stu-id="e9230-188">**Professional experience**</span></span>
   - <span data-ttu-id="e9230-189">**联系人信息**</span><span class="sxs-lookup"><span data-stu-id="e9230-189">**Contact information**</span></span>
   - <span data-ttu-id="e9230-190">**教育程度**</span><span class="sxs-lookup"><span data-stu-id="e9230-190">**Education**</span></span>
   - <span data-ttu-id="e9230-191">**技能**</span><span class="sxs-lookup"><span data-stu-id="e9230-191">**Skills**</span></span>
   - <span data-ttu-id="e9230-192">**证书**</span><span class="sxs-lookup"><span data-stu-id="e9230-192">**Certificates**</span></span>
   - <span data-ttu-id="e9230-193">**筛选**</span><span class="sxs-lookup"><span data-stu-id="e9230-193">**Screenings**</span></span>

8. <span data-ttu-id="e9230-194">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e9230-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="e9230-195">雇用应聘者</span><span class="sxs-lookup"><span data-stu-id="e9230-195">Hire a candidate</span></span>

<span data-ttu-id="e9230-196">当您准备雇用应聘者时，请遵循此过程将应聘者转换为员工。</span><span class="sxs-lookup"><span data-stu-id="e9230-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="e9230-197">在应聘者窗体上，选择 **雇用**。</span><span class="sxs-lookup"><span data-stu-id="e9230-197">On the candidate form, select **Hire**.</span></span>

   ![雇用应聘者](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="e9230-199">在 **雇用新工作人员** 窗体上，在 **详细信息** 下，填写所有字段。</span><span class="sxs-lookup"><span data-stu-id="e9230-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![输入新雇用详细信息](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="e9230-201">在 **职位详细信息** 下，根据需要验证和更改信息。</span><span class="sxs-lookup"><span data-stu-id="e9230-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="e9230-202">在 **入职核对清单** 下，为此员工选择相关的入职核对清单。</span><span class="sxs-lookup"><span data-stu-id="e9230-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="e9230-203">选择 **继续** 以创建员工记录。</span><span class="sxs-lookup"><span data-stu-id="e9230-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="e9230-204">根据您组织的工作流，应聘者记录在成为员工记录之前，可能要完成其他审批步骤。</span><span class="sxs-lookup"><span data-stu-id="e9230-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="e9230-205">决定不雇用应聘者</span><span class="sxs-lookup"><span data-stu-id="e9230-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="e9230-206">如果您决定不雇用应聘者，请遵循此过程将其从审核流程中删除。</span><span class="sxs-lookup"><span data-stu-id="e9230-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="e9230-207">在应聘者窗体上，选择 **不雇用**。</span><span class="sxs-lookup"><span data-stu-id="e9230-207">On the candidate form, select **Do not hire**.</span></span>

   ![不雇用应聘者](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="e9230-209">选择一个 **原因代码** 并包括任何注释。</span><span class="sxs-lookup"><span data-stu-id="e9230-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="e9230-210">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e9230-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="e9230-211">解雇应聘者</span><span class="sxs-lookup"><span data-stu-id="e9230-211">Dismiss a candidate</span></span>

<span data-ttu-id="e9230-212">如果需要，您可以在雇用应聘者后将其解雇。</span><span class="sxs-lookup"><span data-stu-id="e9230-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="e9230-213">例如，应聘者可能拒绝您的聘约或在第一天不露面。</span><span class="sxs-lookup"><span data-stu-id="e9230-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="e9230-214">在应聘者窗体上，选择 **解雇应聘者**。</span><span class="sxs-lookup"><span data-stu-id="e9230-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![消除应聘者](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="e9230-216">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9230-216">See also</span></span>

[<span data-ttu-id="e9230-217">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="e9230-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="e9230-218">组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="e9230-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="e9230-219">设置工作组件</span><span class="sxs-lookup"><span data-stu-id="e9230-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
