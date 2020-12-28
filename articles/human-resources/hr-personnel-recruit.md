---
title: 招聘工作应聘者
description: 本主题显示如何在 Dynamics 365 Human Resources 中招聘应聘者。
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669155"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="eca72-103">招聘工作应聘者</span><span class="sxs-lookup"><span data-stu-id="eca72-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="eca72-104">Dynamics 365 Human Resources 帮助您管理招聘请求。</span><span class="sxs-lookup"><span data-stu-id="eca72-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="eca72-105">它还帮助您无缝地将工作应聘者转换为员工。</span><span class="sxs-lookup"><span data-stu-id="eca72-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="eca72-106">如果您的组织使用单独的招聘应用程序，您的招聘流程可能包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="eca72-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="eca72-107">在 Human Resources 中输入您的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="eca72-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="eca72-108">从招聘应用程序接收 Human Resources 中的应聘者引荐。</span><span class="sxs-lookup"><span data-stu-id="eca72-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="eca72-109">在 Human Resources 中完成应聘者审批流程。</span><span class="sxs-lookup"><span data-stu-id="eca72-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="eca72-110">如果您不使用单独的招聘应用程序，还可以在 Human Resources 中手动管理应聘者。</span><span class="sxs-lookup"><span data-stu-id="eca72-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="eca72-111">如果您是管理员或开发人员，并且想要将 Human Resources 与第三方招聘应用程序集成，请参阅[配置 Common Data Service 集成](hr-admin-integration-common-data-service.md)和[配置 Common Data Service 虚拟实体](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="eca72-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="eca72-112">您还可以在 [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) 上找到招聘集成应用。</span><span class="sxs-lookup"><span data-stu-id="eca72-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="eca72-113">若要试用与 LinkedIn Talent Hub 集成的预览功能，请参阅[与 LinkedIn Talent Hub 集成](hr-admin-integration-linkedin.md)。</span><span class="sxs-lookup"><span data-stu-id="eca72-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="eca72-114">启用招聘请求</span><span class="sxs-lookup"><span data-stu-id="eca72-114">Enable recruiting requests</span></span>

<span data-ttu-id="eca72-115">如果要在 Human Resources 中提交招聘请求，您必须先在 **Human Resources 参数** 中启用该功能。</span><span class="sxs-lookup"><span data-stu-id="eca72-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="eca72-116">在 **人事管理** 工作区中，选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="eca72-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="eca72-117">在 **设置** 下，选择 **人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="eca72-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="eca72-118">在 **常规** 选项卡上，在 **招聘** 下，将 **启用招聘请求** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eca72-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![启用招聘请求](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="eca72-120">添加招聘请求位置</span><span class="sxs-lookup"><span data-stu-id="eca72-120">Add a recruiting request location</span></span>

<span data-ttu-id="eca72-121">如果您的组织有多个位置，可以添加它们，以便请求者可以选择新招聘的工作位置。</span><span class="sxs-lookup"><span data-stu-id="eca72-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="eca72-122">位置将包含在工作发布中。</span><span class="sxs-lookup"><span data-stu-id="eca72-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="eca72-123">在搜索栏中，输入 **招聘请求位置**。</span><span class="sxs-lookup"><span data-stu-id="eca72-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="eca72-124">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eca72-124">Select **New**.</span></span>

3. <span data-ttu-id="eca72-125">在 **招聘请求位置** 字段中，输入位置名称。</span><span class="sxs-lookup"><span data-stu-id="eca72-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![添加招聘请求位置](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="eca72-127">在 **描述** 中，输入位置的描述。</span><span class="sxs-lookup"><span data-stu-id="eca72-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="eca72-128">在 **位置** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="eca72-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="eca72-129">如果显示 **新地址** 弹出窗口，输入位置的地址。</span><span class="sxs-lookup"><span data-stu-id="eca72-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![请输入地址](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="eca72-131">在 **联系人信息** 下，输入该位置的联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="eca72-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="eca72-132">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eca72-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="eca72-133">添加招聘请求</span><span class="sxs-lookup"><span data-stu-id="eca72-133">Add a recruiting request</span></span>

<span data-ttu-id="eca72-134">经理可以在 Human Resources 中提交招聘请求。</span><span class="sxs-lookup"><span data-stu-id="eca72-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="eca72-135">如果您使用单独的招聘应用程序，完成这些步骤将发送一个招聘请求，并在该应用程序中开始招聘流程。</span><span class="sxs-lookup"><span data-stu-id="eca72-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="eca72-136">否则，完成此过程以开始您自己的内部招聘流程的工作流。</span><span class="sxs-lookup"><span data-stu-id="eca72-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="eca72-137">选择 **员工自助服务**。</span><span class="sxs-lookup"><span data-stu-id="eca72-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="eca72-138">选择 **我的团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="eca72-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="eca72-139">选择 **招聘请求**。</span><span class="sxs-lookup"><span data-stu-id="eca72-139">Select  **Request to recruit**.</span></span>

   ![开始招聘请求](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="eca72-141">填写 **描述**、**工作** 和 **预计开始日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="eca72-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![完成招聘请求](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="eca72-143">选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="eca72-143">Select **Continue**.</span></span> <span data-ttu-id="eca72-144">将显示您的职位的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="eca72-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="eca72-145">在 **常规** 下，从 **招聘人员** 下拉菜单中选择招聘人员，然后从 **招聘请求位置** 中选择位置。</span><span class="sxs-lookup"><span data-stu-id="eca72-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="eca72-146">在 **工作** 下，根据需要更改任何信息，然后选择 **通过工作创建详细信息**。</span><span class="sxs-lookup"><span data-stu-id="eca72-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![通过作业创建详细信息](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="eca72-148">将使用您输入的工作的默认信息填充招聘请求的其余部分。</span><span class="sxs-lookup"><span data-stu-id="eca72-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="eca72-149">在 **外部描述** 下，输入一个外部工作描述。</span><span class="sxs-lookup"><span data-stu-id="eca72-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="eca72-150">在 **职位** 下，选择 **添加**，然后为此招聘请求选择一个职位。</span><span class="sxs-lookup"><span data-stu-id="eca72-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![添加职位](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="eca72-152">在 **技能** 下，选择 **添加**，然后选择一项技能。</span><span class="sxs-lookup"><span data-stu-id="eca72-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="eca72-153">在 **教育要求** 下，选择 **添加**，然后从 **教育** 和 **教育程度** 下拉菜单中选择值。</span><span class="sxs-lookup"><span data-stu-id="eca72-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![添加教育要求](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="eca72-155">在 **注释** 下，根据需要添加注释。</span><span class="sxs-lookup"><span data-stu-id="eca72-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="eca72-156">在 **薪酬** 下，从 **级别** 下拉菜单中选择一个级别，然后根据需要调整 **低阈值**、**控制点** 和 **高阈值**。</span><span class="sxs-lookup"><span data-stu-id="eca72-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="eca72-157">在完成招聘请求并且您准备好开始招聘流程时，在菜单栏中选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="eca72-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![激活招聘请求](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="eca72-159">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eca72-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="eca72-160">查看和编辑您的招聘请求</span><span class="sxs-lookup"><span data-stu-id="eca72-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="eca72-161">如果您是经理，并且想要查看自己的请求：</span><span class="sxs-lookup"><span data-stu-id="eca72-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="eca72-162">选择 **员工自助服务**。</span><span class="sxs-lookup"><span data-stu-id="eca72-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="eca72-163">选择 **我的团队** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="eca72-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="eca72-164">在 **我的团队信息** 下，选择 **招聘请求** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="eca72-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![选择“招聘请求”选项卡](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="eca72-166">若要查看或编辑招聘请求，请在网格中选择它。</span><span class="sxs-lookup"><span data-stu-id="eca72-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="eca72-167">如果您是 HR 专业人员，并且想要查看所有招聘请求：</span><span class="sxs-lookup"><span data-stu-id="eca72-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="eca72-168">选择 **人事管理**。</span><span class="sxs-lookup"><span data-stu-id="eca72-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="eca72-169">选择 **招聘请求**。</span><span class="sxs-lookup"><span data-stu-id="eca72-169">Select **Recruiting requests**.</span></span>

   ![在人事管理中查看招聘请求](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="eca72-171">若要查看或编辑招聘请求，请在网格中选择它。</span><span class="sxs-lookup"><span data-stu-id="eca72-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="eca72-172">添加或编辑应聘者个人资料</span><span class="sxs-lookup"><span data-stu-id="eca72-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="eca72-173">如果您的组织已与另一个应用程序集成以管理招聘请求，招聘请求将转发到该应用程序。</span><span class="sxs-lookup"><span data-stu-id="eca72-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="eca72-174">然后，招聘应用程序将应聘者信息发送回 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="eca72-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="eca72-175">否则，您可以遵循自己的内部招聘流程并手动输入应聘者信息。</span><span class="sxs-lookup"><span data-stu-id="eca72-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="eca72-176">选择 **人事管理**。</span><span class="sxs-lookup"><span data-stu-id="eca72-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="eca72-177">选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="eca72-177">Select **Links**.</span></span>

3. <span data-ttu-id="eca72-178">在 **招聘** 下，选择 **应聘者**。</span><span class="sxs-lookup"><span data-stu-id="eca72-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![查看应聘者](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="eca72-180">若要添加应聘者，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eca72-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="eca72-181">若要编辑现有应聘者，请从列表中选择应聘者，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eca72-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="eca72-182">将显示应聘者个人资料。</span><span class="sxs-lookup"><span data-stu-id="eca72-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="eca72-183">在 **应聘者汇总** 下，根据需要输入或编辑应聘者信息。</span><span class="sxs-lookup"><span data-stu-id="eca72-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="eca72-184">在 **招聘请求** 下，选择将应聘者链接到的招聘请求。</span><span class="sxs-lookup"><span data-stu-id="eca72-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="eca72-185">然后，根据需要填写 **预计开始日期**、**雇用经理**、**职位** 和 **描述** 字段。</span><span class="sxs-lookup"><span data-stu-id="eca72-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![链接到招聘请求](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="eca72-187">填写要包含在应聘者记录中的以下区域中的所有信息：</span><span class="sxs-lookup"><span data-stu-id="eca72-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="eca72-188">**注释**</span><span class="sxs-lookup"><span data-stu-id="eca72-188">**Comments**</span></span>
   - <span data-ttu-id="eca72-189">**工作经验**</span><span class="sxs-lookup"><span data-stu-id="eca72-189">**Professional experience**</span></span>
   - <span data-ttu-id="eca72-190">**联系人信息**</span><span class="sxs-lookup"><span data-stu-id="eca72-190">**Contact information**</span></span>
   - <span data-ttu-id="eca72-191">**教育程度**</span><span class="sxs-lookup"><span data-stu-id="eca72-191">**Education**</span></span>
   - <span data-ttu-id="eca72-192">**技能**</span><span class="sxs-lookup"><span data-stu-id="eca72-192">**Skills**</span></span>
   - <span data-ttu-id="eca72-193">**证书**</span><span class="sxs-lookup"><span data-stu-id="eca72-193">**Certificates**</span></span>
   - <span data-ttu-id="eca72-194">**筛选**</span><span class="sxs-lookup"><span data-stu-id="eca72-194">**Screenings**</span></span>

8. <span data-ttu-id="eca72-195">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eca72-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="eca72-196">雇用应聘者</span><span class="sxs-lookup"><span data-stu-id="eca72-196">Hire a candidate</span></span>

<span data-ttu-id="eca72-197">当您准备雇用应聘者时，请遵循此过程将应聘者转换为员工。</span><span class="sxs-lookup"><span data-stu-id="eca72-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="eca72-198">在应聘者窗体上，选择 **雇用**。</span><span class="sxs-lookup"><span data-stu-id="eca72-198">On the candidate form, select **Hire**.</span></span>

   ![雇用应聘者](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="eca72-200">在 **雇用新工作人员** 窗体上，在 **详细信息** 下，填写所有字段。</span><span class="sxs-lookup"><span data-stu-id="eca72-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![输入新雇用详细信息](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="eca72-202">在 **职位详细信息** 下，根据需要验证和更改信息。</span><span class="sxs-lookup"><span data-stu-id="eca72-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="eca72-203">在 **入职核对清单** 下，为此员工选择相关的入职核对清单。</span><span class="sxs-lookup"><span data-stu-id="eca72-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="eca72-204">选择 **继续** 以创建员工记录。</span><span class="sxs-lookup"><span data-stu-id="eca72-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="eca72-205">根据您组织的工作流，应聘者记录在成为员工记录之前，可能要完成其他审批步骤。</span><span class="sxs-lookup"><span data-stu-id="eca72-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="eca72-206">决定不雇用应聘者</span><span class="sxs-lookup"><span data-stu-id="eca72-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="eca72-207">如果您决定不雇用应聘者，请遵循此过程将其从审核流程中删除。</span><span class="sxs-lookup"><span data-stu-id="eca72-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="eca72-208">在应聘者窗体上，选择 **不雇用**。</span><span class="sxs-lookup"><span data-stu-id="eca72-208">On the candidate form, select **Do not hire**.</span></span>

   ![不雇用应聘者](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="eca72-210">选择一个 **原因代码** 并包括任何注释。</span><span class="sxs-lookup"><span data-stu-id="eca72-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="eca72-211">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eca72-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="eca72-212">解雇应聘者</span><span class="sxs-lookup"><span data-stu-id="eca72-212">Dismiss a candidate</span></span>

<span data-ttu-id="eca72-213">如果需要，您可以在雇用应聘者后将其解雇。</span><span class="sxs-lookup"><span data-stu-id="eca72-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="eca72-214">例如，应聘者可能拒绝您的聘约或在第一天不露面。</span><span class="sxs-lookup"><span data-stu-id="eca72-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="eca72-215">在应聘者窗体上，选择 **解雇应聘者**。</span><span class="sxs-lookup"><span data-stu-id="eca72-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![消除应聘者](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="eca72-217">请参阅</span><span class="sxs-lookup"><span data-stu-id="eca72-217">See also</span></span>

[<span data-ttu-id="eca72-218">配置 Common Data Service 虚拟实体</span><span class="sxs-lookup"><span data-stu-id="eca72-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="eca72-219">组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="eca72-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="eca72-220">设置工作组件</span><span class="sxs-lookup"><span data-stu-id="eca72-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)