---
title: 具有 LinkedIn Recruiter 的来源添加
description: 此主题提供有关如何使用机器学习获得工作和工作应聘者推荐的信息。
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517390"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="7dcba-103">具有 LinkedIn Recruiter 的来源添加</span><span class="sxs-lookup"><span data-stu-id="7dcba-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="7dcba-104">LinkedIn 是全世界最大的人才数据库招，通常是招聘人员用来查找、联系和为招聘人员要招聘的工作寻求候选人的主要系统。</span><span class="sxs-lookup"><span data-stu-id="7dcba-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="7dcba-105">LinkedIn Recruiter 与  Dynamics 365 for Talent: Attract 集成让用户可以更轻松地招聘并在两个系统之间保持数据同步。</span><span class="sxs-lookup"><span data-stu-id="7dcba-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="7dcba-106">您需要综合招聘附件和 LinkedIn Recruiter 席位才能够使用 LinkedIn Recruiter 与 Attract 的集成。</span><span class="sxs-lookup"><span data-stu-id="7dcba-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="7dcba-107">为 LinkedIn Recruiter 设置 Attract</span><span class="sxs-lookup"><span data-stu-id="7dcba-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="7dcba-108">您必须先配置对 Attract 实例的合同级别或公司级别的访问才能够使用 LinkedIn Recruiter 功能。</span><span class="sxs-lookup"><span data-stu-id="7dcba-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="7dcba-109">若要完成配置流程，您必须与作为 LinkedIn Recruiter 合同的管理员的用户合作。</span><span class="sxs-lookup"><span data-stu-id="7dcba-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="7dcba-110">请完成以下步骤来配置 LinkedIn Recruiter 与 Attract 集成。</span><span class="sxs-lookup"><span data-stu-id="7dcba-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="7dcba-111">作为管理员登录到 Attract 并转到**管理员设置**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="7dcba-112">在左窗格中，单击 **LinkedIn 集成**选项卡。</span><span class="sxs-lookup"><span data-stu-id="7dcba-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="7dcba-113">[![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="7dcba-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="7dcba-114">单击**连接**开始设置，然后在引导下完成 LinkedIn 登录流程。</span><span class="sxs-lookup"><span data-stu-id="7dcba-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="7dcba-115">如果您有多个 LinkedIn 合同的座位，选择您希望连接到 Attract 系统的合同。</span><span class="sxs-lookup"><span data-stu-id="7dcba-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="7dcba-116">如果只有一个 LinkedIn 合同的座位，则不需要此步骤。</span><span class="sxs-lookup"><span data-stu-id="7dcba-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="7dcba-117">LinkedIn 小组件现在将加载您的管理员设置并显示集成列表。</span><span class="sxs-lookup"><span data-stu-id="7dcba-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="7dcba-118">在**招聘人员系统连接**下，单击**请求**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="7dcba-119">[![请求 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7dcba-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="7dcba-120">在从 Attract 请求集成后，集成将显示为**合作伙伴就绪**，并可以从**招聘人员管理员设置**打开。</span><span class="sxs-lookup"><span data-stu-id="7dcba-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="7dcba-121">如果您在此页面看到**通知合作伙伴**，请等待几秒，单击**通知合作伙伴**，然后刷新页面。</span><span class="sxs-lookup"><span data-stu-id="7dcba-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="7dcba-122">现在应该显示为**合作伙伴就绪**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="7dcba-123">[![指示请求的 Attract 端已完成的 Attract 视图](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7dcba-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="7dcba-124">要完成下一步，您需要有 LinkedIn Recruiter 合同的管理员权限。</span><span class="sxs-lookup"><span data-stu-id="7dcba-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="7dcba-125">使用理员帐户登录到 LinkedIn 并转到右上方的 LinkedIn Recruiter。</span><span class="sxs-lookup"><span data-stu-id="7dcba-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="7dcba-126">在屏幕顶部的**更多**菜单上，单击**管理员设置**，然后单击 **ATS** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="7dcba-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="7dcba-127">Attract 系统将列出，并有可以打开的两三个选项。</span><span class="sxs-lookup"><span data-stu-id="7dcba-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="7dcba-128">如果要为 **ATS 内指标**和 **ATS 内模板小组件**启用一键导出，请选择**公司级别访问**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="7dcba-129">如果您要启用所有公司级别的访问功能以及 InMail 历史记录、注释历史记录和 InMail 存根模板访问，请选择**合同级别访问**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="7dcba-130">从您的 LinkedIn Recruiter **管理员 ATS** 设置打开所需的访问级别。</span><span class="sxs-lookup"><span data-stu-id="7dcba-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="7dcba-131">[![从 LinkedIn Recruiter 管理员打开 Attract 集成的视图](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7dcba-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="7dcba-132">作为 Attract 管理员返回 Attract 管理员设置，选择 **LinkedIn 集成** 选项卡。现在您应会看到显示所选访问级别已打开的**已启用**的 LinkedIn 小组件加载。</span><span class="sxs-lookup"><span data-stu-id="7dcba-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="7dcba-133">[![LinkedIn Recruiter 集成完成](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="7dcba-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="7dcba-134">使用 LinkedIn Recruiter 功能</span><span class="sxs-lookup"><span data-stu-id="7dcba-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="7dcba-135">在 Attract 管理员启用 LinkedIn Recruiter 功能后，招聘经理和招聘人员可以进行访问。</span><span class="sxs-lookup"><span data-stu-id="7dcba-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="7dcba-136">若要使用这些功能，请在**用户设置**下连接您的 LinkedIn 帐户。</span><span class="sxs-lookup"><span data-stu-id="7dcba-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="7dcba-137">管理员和用户设置均连接后，若干功能将可用。</span><span class="sxs-lookup"><span data-stu-id="7dcba-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="7dcba-138">ATS 内模板小组件</span><span class="sxs-lookup"><span data-stu-id="7dcba-138">In-ATS profile widget</span></span>

<span data-ttu-id="7dcba-139">您可以在 Attract 中查看应聘者的 LinkedIn 个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="7dcba-140">在 ATS 信息与其用户的 LinkedIn 信息匹配时，LinkedIn 小组件将显示应聘者的个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="7dcba-141">若要查看个人资料，请从工作或人才池转到应聘者个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="7dcba-142">在应聘者个人资料中，请选择 **LinkedIn** 选项卡，模板小组件将加载。</span><span class="sxs-lookup"><span data-stu-id="7dcba-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="7dcba-143">您还可以从此页将应聘者保存到您的 LinkedIn Recruiter 项目。</span><span class="sxs-lookup"><span data-stu-id="7dcba-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="7dcba-144">如果 LinkedIn 找到了基于电子邮件和 LinkedIn 成员 ID 的匹配项（精确匹配），应聘者的个人资料将显示。</span><span class="sxs-lookup"><span data-stu-id="7dcba-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="7dcba-145">用户仍可以选择链接/取消链接个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="7dcba-146">如果 LinkedIn 根据电子邮件或成员 ID 找不到应聘者，它会显示基于应聘者姓名的可能的应聘者匹配项列表，用户可以从中选择一个并链接个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="7dcba-147">如果 LinkedIn 基于姓名找不到任何应聘者，它将返回未找到匹配项。</span><span class="sxs-lookup"><span data-stu-id="7dcba-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="7dcba-148">一键导出</span><span class="sxs-lookup"><span data-stu-id="7dcba-148">1-click export</span></span> 

<span data-ttu-id="7dcba-149">在 LinkedIn 中寻求应聘者时，您可以将应聘者一键导出到您当前打开的工作中。</span><span class="sxs-lookup"><span data-stu-id="7dcba-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="7dcba-150">完成以下步骤打开一键导出。</span><span class="sxs-lookup"><span data-stu-id="7dcba-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="7dcba-151">在完成这些步骤之前，请确认您被分配了工作的招聘经理或招聘人员角色，并且工作具有**应聘者**阶段。</span><span class="sxs-lookup"><span data-stu-id="7dcba-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="7dcba-152">创建工作，分配适当的角色，并激活工作。</span><span class="sxs-lookup"><span data-stu-id="7dcba-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="7dcba-153">在激活工作后，导航到 LinkedIn Recruiter。</span><span class="sxs-lookup"><span data-stu-id="7dcba-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="7dcba-154">查找您在寻找的应聘者，并转至其个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="7dcba-155">使用联系人卡片中的工作搜索框，使用在 Attract 中激活的职位或工作 ID 查找工作。</span><span class="sxs-lookup"><span data-stu-id="7dcba-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="7dcba-156">如果未找到工作，请单击**更改 ATS** 查找正确的 Attract 实例。</span><span class="sxs-lookup"><span data-stu-id="7dcba-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="7dcba-157">在选择工作后，请单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="7dcba-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="7dcba-158">应聘者现在被 Attract 获取。</span><span class="sxs-lookup"><span data-stu-id="7dcba-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="7dcba-159">转到 Attract，打开各自的工作。</span><span class="sxs-lookup"><span data-stu-id="7dcba-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="7dcba-160">您将找到刚才在工作的**应聘者**阶段导出的应聘者。</span><span class="sxs-lookup"><span data-stu-id="7dcba-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="7dcba-161">ATS 内指标</span><span class="sxs-lookup"><span data-stu-id="7dcba-161">In-ATS indicator</span></span> 

<span data-ttu-id="7dcba-162">使用 LinkedIn recruiter，您可以跟踪应聘者是否已申请组织内的其他工作，查看他们在不同的工作申请阶段所处的位置，并查看 LinkedIn Recruiter 中来自 Attract 的反馈和备注。</span><span class="sxs-lookup"><span data-stu-id="7dcba-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="7dcba-163">打开 LinkedIn Recruiter，找到您要寻找的应聘者的个人资料。</span><span class="sxs-lookup"><span data-stu-id="7dcba-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="7dcba-164">向下滚动查看应聘者个人资料的 **ATS 内**部分。</span><span class="sxs-lookup"><span data-stu-id="7dcba-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="7dcba-165">您可以使用此小组件来在 LinkedIn Recruiter 视图内查看有关 Attract 中显示的应聘者的所有信息。</span><span class="sxs-lookup"><span data-stu-id="7dcba-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="7dcba-166">选择**工作和状态**选项卡查看他们所属的工作、最新状态，以及他们如何在每个工作之间移动。</span><span class="sxs-lookup"><span data-stu-id="7dcba-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="7dcba-167">选择**面试反馈**选项卡查看面试官在 Attract 中提交的反馈。</span><span class="sxs-lookup"><span data-stu-id="7dcba-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="7dcba-168">选择**注释**选项卡查看在 Attract 中为此申请人获取的注释。</span><span class="sxs-lookup"><span data-stu-id="7dcba-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="7dcba-169">如果应聘者未通过“潜在人选”阶段，应聘者和申请数据不会同步到 LinkedIn Recruiter。</span><span class="sxs-lookup"><span data-stu-id="7dcba-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="7dcba-170">InMail 历史记录</span><span class="sxs-lookup"><span data-stu-id="7dcba-170">InMail history</span></span>

<span data-ttu-id="7dcba-171">LinkedIn InMail 历史记录可以通过 LinkedIn Recruiter 的合同级别访问获取。</span><span class="sxs-lookup"><span data-stu-id="7dcba-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7dcba-172">在启用后，您可以查看应聘者的整个 InMail 历史记录。</span><span class="sxs-lookup"><span data-stu-id="7dcba-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="7dcba-173">您还可以看到组织中还有哪些人与应聘者交换了 InMail，但是不能查看他们之间发送的消息。</span><span class="sxs-lookup"><span data-stu-id="7dcba-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="7dcba-174">要查看 InMail 历史记录，转到应聘者的个人资料，转到 **LinkedIn** 选项卡并滚动到页面底部查看历史记录。</span><span class="sxs-lookup"><span data-stu-id="7dcba-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="7dcba-175">如果您与应聘者之间有讨论，您可以查看 InMail 历史记录。</span><span class="sxs-lookup"><span data-stu-id="7dcba-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="7dcba-176">InMail 的消息每隔几小时与 Attract 同步一次。</span><span class="sxs-lookup"><span data-stu-id="7dcba-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="7dcba-177">注释历史记录</span><span class="sxs-lookup"><span data-stu-id="7dcba-177">Notes history</span></span> 

<span data-ttu-id="7dcba-178">LinkedIn 注释历史记录可以通过 LinkedIn Recruiter 的合同级别访问获取。</span><span class="sxs-lookup"><span data-stu-id="7dcba-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7dcba-179">在启用后，您可以查看组织中的不同招聘人员获取的有关该应聘者的注释。</span><span class="sxs-lookup"><span data-stu-id="7dcba-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="7dcba-180">要查看注释历史记录，转到应聘者的个人资料，转到 **LinkedIn** 选项卡并滚动到页面底部查看历史记录。</span><span class="sxs-lookup"><span data-stu-id="7dcba-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="7dcba-181">您可以从 LinkedIn Recruiter 查看有关应聘者的所有注释。</span><span class="sxs-lookup"><span data-stu-id="7dcba-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="7dcba-182">InMail 存根模板</span><span class="sxs-lookup"><span data-stu-id="7dcba-182">InMail stub profile</span></span>

<span data-ttu-id="7dcba-183">InMail 存根模板可以通过 LinkedIn Recruiter 的合同级别访问获取。</span><span class="sxs-lookup"><span data-stu-id="7dcba-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7dcba-184">如果应聘者同意与您组织中的任何用户共享其 LinkedIn 个人资料，您可以在 Attract 中跟踪该应聘者，并且新应聘者记录将为每个应聘者创建。</span><span class="sxs-lookup"><span data-stu-id="7dcba-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="7dcba-185">如果应聘者已经存在于系统中并具有电子邮件地址或已选择与招聘人员共享其地址，您可以查看应聘者的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7dcba-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="7dcba-186">若要查看应聘者列表，请转到**人才池**查看系统创建的 LinkedIn 人才池。</span><span class="sxs-lookup"><span data-stu-id="7dcba-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="7dcba-187">此人才池包含从 LinkedIn 收到的应聘者及其存根模板的列表，显示应聘者的名字和姓氏。</span><span class="sxs-lookup"><span data-stu-id="7dcba-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="7dcba-188">如果应聘者选择共享其电子邮件地址，该候选人的电子邮件 ID 将显示。</span><span class="sxs-lookup"><span data-stu-id="7dcba-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
