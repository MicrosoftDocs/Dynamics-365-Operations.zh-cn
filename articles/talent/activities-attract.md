---
title: 流程中的活动
description: 本主题提供有关可用于招聘流程的活动的各个类型的信息。
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2019
ms.locfileid: "374749"
---
# <a name="activities-in-the-hiring-processes"></a><span data-ttu-id="f7ac0-103">招聘流程中的活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-103">Activities in the hiring processes</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f7ac0-104">活动可以在 Microsoft Dynamics 365 for Talent: Attract 中作为招聘流程的一部分添加。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-104">Activities can be added as a part of the hiring process in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="f7ac0-105">活动可以添加到流程模板，或者它们可以直接添加到工作中的招聘流程。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-105">Activities can be added to a process template, or they can be added directly to the hiring process in the job.</span></span> <span data-ttu-id="f7ac0-106">当定义工作后，会选择流程模板，模板中包含的活动将应用到工作。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-106">When a job is defined, a process template is selected, and the activities that are included in the template are applied to the job.</span></span> <span data-ttu-id="f7ac0-107">如果模板没有选择，则使用默认模板。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-107">If a template isn't selected, the default template is used.</span></span> <span data-ttu-id="f7ac0-108">招聘流程也可以在应用模板后在工作上修改。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-108">The hiring process can also be modified on the job after the template is applied.</span></span>

> [!NOTE] 
> <span data-ttu-id="f7ac0-109">流程模板随综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-109">Process templates are available with the Comprehensive hiring add-on.</span></span>

## <a name="prospect-activity"></a><span data-ttu-id="f7ac0-110">应聘者活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-110">Prospect activity</span></span>

<span data-ttu-id="f7ac0-111">应聘者活动控制应聘者是否可以添加到工作中。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-111">The Prospect activity controls whether prospects can be added to a job.</span></span> <span data-ttu-id="f7ac0-112">默认情况下，应聘者可以添加到工作中。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-112">By default, prospects can be added to a job.</span></span> <span data-ttu-id="f7ac0-113">若要关闭应聘者活动，请将**启用应聘者**选项设置为**关**。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-113">To turn off the Prospect activity, set the **Enable prospects** option to **Off**.</span></span> <span data-ttu-id="f7ac0-114">在应聘者活动打开时，招聘经理可以添加和查看应聘者，**应聘者**选项卡显示在工作上。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-114">When the Prospect activity is turned on, hiring managers can add and view prospects, and the **Prospect** tab is shown on the job.</span></span>

## <a name="application-activity"></a><span data-ttu-id="f7ac0-115">申请活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-115">Application activity</span></span>

<span data-ttu-id="f7ac0-116">申请活动是招聘流程模板的必要项目。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-116">The Application activity is required in the hiring process template.</span></span> <span data-ttu-id="f7ac0-117">要在应聘者发送申请或被添加到申请阶段时向其发送电子邮件，请将**向应聘者发送邮件**选项设置为**开**。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-117">To send email to candidates when they submit their application or are added to the Application stage, set the **Send mail to candidate** option to **On**.</span></span>

## <a name="interview-schedule-and-feedback-activity"></a><span data-ttu-id="f7ac0-118">面试时间表和反馈活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-118">Interview schedule and feedback activity</span></span>

<span data-ttu-id="f7ac0-119">此活动具有三个组件：应聘者可用日期请求、计划和反馈。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-119">This activity has three components: Candidate availability request, Schedule, and Feedback.</span></span> <span data-ttu-id="f7ac0-120">如果您希望作为流程的一部分包含候选人可用日期请求、计划和反馈，而不是作为招聘流程的一部分单独使用它们，应在工作模板中使用面试活动。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-120">Use the interview activity in the job template if you want to include the candidate’s availability request, schedule, and feedback as part of the process instead of using them individually as part of the hiring process.</span></span> <span data-ttu-id="f7ac0-121">有关详细信息，请参阅[面试计划和反馈](interview-scheduling-feedback.md)。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-121">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

## <a name="powerapps-activity"></a><span data-ttu-id="f7ac0-122">PowerApps 活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-122">PowerApps activity</span></span>

<span data-ttu-id="f7ac0-123">PowerApps 活动让您可以在招聘流程中嵌入 Microsoft PowerApps 应用。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-123">The PowerApps activity lets you embed a Microsoft PowerApps app in your hiring process.</span></span> <span data-ttu-id="f7ac0-124">此应用可能对所有申请人、仅内部申请人、仅外部申请人是必要的，也可能不是必要的。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-124">The app can be required for all applicants, internal applicants only, external applicants only, or no applicants.</span></span> <span data-ttu-id="f7ac0-125">如果此应用被标记为必要，则必须在推进此阶段前完成它。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-125">If the app is marked as required, it must be completed before the stage can be advanced.</span></span> <span data-ttu-id="f7ac0-126">如果此应用未标记为必要，此活动是可选步骤，即使未完成应用仍可以推进此阶段。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-126">If the app isn't marked as required, the activity is an optional step, and the stage can be advanced even if the app isn't completed.</span></span>

<span data-ttu-id="f7ac0-127">若要将 PowerApps 活动保存到招聘流程，您必须输入 PowerApps ID。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-127">To save the PowerApps activity to the hiring process, you must enter a PowerApps ID.</span></span> <span data-ttu-id="f7ac0-128">若要查找 PowerApps ID，请转到 [PowerApps](https://web.powerapps.com)，选择**应用**，然后选择**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-128">To find the PowerApps ID, go to [PowerApps](https://web.powerapps.com), select **Apps**, and then select **Details**.</span></span>

<span data-ttu-id="f7ac0-129">如果您选择**允许为此活动添加参与者**选项，可以为使用 PowerApps 活动的申请添加其他参与者。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-129">If you select the **Allow adding participants for this activity** option, additional contributors can be added for an application that uses the PowerApps activity.</span></span> <span data-ttu-id="f7ac0-130">例如，组织为技术角色创建了作为面试问题库的 PowerApps 应用。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-130">For example, an organization has created a PowerApps app that is a library of interview questions for technical roles.</span></span> <span data-ttu-id="f7ac0-131">组织现在在招聘新的软件开发人员并向软件开发人员角色的招聘流程添加了 PowerApps 活动。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-131">The organization is now hiring a new software developer and has added the PowerApps activity to the hiring process for the Software Developer role.</span></span> <span data-ttu-id="f7ac0-132">如果选择了**允许为此活动添加参与者**选项，查看软件开发人员角色申请人的招聘人员或招聘经理可以向 PowerApps 活动添加人员。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-132">If the **Allow adding participants for this activity** option is selected, a recruiter or hiring manager who is viewing an applicant for the Software Developer role can add people to the PowerApps activity.</span></span> <span data-ttu-id="f7ac0-133">这些人员然后可以查看具有面试问题的应用。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-133">Those people can then view the app that has the interview questions.</span></span>

> [!NOTE]
> <span data-ttu-id="f7ac0-134">PowerApps 活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-134">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="youtube-activity"></a><span data-ttu-id="f7ac0-135">YouTube 活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-135">YouTube activity</span></span>

<span data-ttu-id="f7ac0-136">YouTube 活动允许您作为招聘流程的一部分共享 YouTube 视频。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-136">The YouTube activity lets you share a YouTube video as part of your hiring process.</span></span> <span data-ttu-id="f7ac0-137">若要将 YouTube 活动保存到招聘流程，您必须指定 YouTube 视频的 URL。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-137">To save the YouTube activity to the hiring process, you must specify the URL of the YouTube video.</span></span> <span data-ttu-id="f7ac0-138">对于 PowerApps 活动，您可以允许参与者被添加到活动。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-138">As for the PowerApps activity, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="f7ac0-139">如果您选择**仅对应聘者显示**选项，视频将仅作为应聘者体验的一部分显示。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-139">If you select the **Show only to candidate** option, the video is shown only as part of the candidate experience.</span></span> <span data-ttu-id="f7ac0-140">它不会显示在 Attract 中的招聘流程中。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-140">It isn't shown in the hiring process in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="f7ac0-141">YouTube 活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-141">The YouTube activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="web-content-activity"></a><span data-ttu-id="f7ac0-142">Web 内容活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-142">Web content activity</span></span>

<span data-ttu-id="f7ac0-143">Web 内容活动允许您在招聘流程中嵌入在线内容。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-143">The Web content activity lets you embed online content in your hiring process.</span></span> <span data-ttu-id="f7ac0-144">若要将 Web 内容活动保存到招聘流程，您必须指定内容的 URL。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-144">To save the Web content activity to the hiring process, you must specify the URL of the content.</span></span> <span data-ttu-id="f7ac0-145">对于 PowerApps 和 YouTube 活动，您可以允许参与者被添加到活动。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-145">As for the PowerApps and YouTube activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="f7ac0-146">如果您选择**仅对应聘者显示**选项，内容将仅作为应聘者体验的一部分显示。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-146">If you select the **Show only to candidate** option, the content is shown only as part of the candidate experience.</span></span> <span data-ttu-id="f7ac0-147">它不会显示在 Attract 中的招聘流程中。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-147">It isn't shown in the hiring process in Attract.</span></span> <span data-ttu-id="f7ac0-148">您可以选择内容的显示尺寸。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-148">You can select the size of the content that is shown.</span></span>

> [!NOTE]
> <span data-ttu-id="f7ac0-149">Web 内容活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-149">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="microsoft-forms-activity"></a><span data-ttu-id="f7ac0-150">Microsoft 窗体活动</span><span class="sxs-lookup"><span data-stu-id="f7ac0-150">Microsoft Forms activity</span></span>

<span data-ttu-id="f7ac0-151">Microsoft 窗体活动让您可以在招聘流程中嵌入 Microsoft 窗体。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-151">The Microsoft Forms activity lets you embed a Microsoft Forms form in your hiring process.</span></span> <span data-ttu-id="f7ac0-152">Microsoft 窗体允许您创建测试、调查和轮询。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-152">Microsoft Forms lets you create quizzes, surveys, and polls.</span></span> <span data-ttu-id="f7ac0-153">若要将 Microsoft 窗体活动保存到招聘流程，您必须指定窗体的 URL。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-153">To save the Microsoft Forms activity to the hiring process, you must specify of the URL of the form.</span></span> <span data-ttu-id="f7ac0-154">对于 PowerApps、YouTube 和 Web 内容活动，您可以允许参与者被添加到活动。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-154">As for the PowerApps, YouTube, and Web content activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="f7ac0-155">如果您选择**仅对应聘者显示**选项，窗体将仅作为应聘者体验的一部分显示。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-155">If you select the **Show only to candidate** option, the form is shown only as part of the candidate experience.</span></span> <span data-ttu-id="f7ac0-156">它不会显示在 Attract 中的招聘流程中。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-156">It isn't shown in the hiring process in Attract.</span></span>

<span data-ttu-id="f7ac0-157">在 Microsoft 窗体中，作者可以更改其设置以允许其组织外的用户对调查或测试作出响应。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-157">In Microsoft Forms, authors can change their settings to let users outside their organization respond to their survey or quiz.</span></span> <span data-ttu-id="f7ac0-158">在这种情况下，用户匿名提交响应。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-158">In this case, users submit responses anonymously.</span></span> <span data-ttu-id="f7ac0-159">如果要查看哪些人参与了您的调查或测试，您可以要求回应者在调查或测试中输入其姓名。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-159">If you want to see who has filled out your survey or quiz, you can require that respondents enter their names as part of the survey or quiz.</span></span>

> [!NOTE]
> <span data-ttu-id="f7ac0-160">Microsoft 窗体活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="f7ac0-160">The Microsoft Forms activity is available only with the Comprehensive hiring add-on.</span></span>
