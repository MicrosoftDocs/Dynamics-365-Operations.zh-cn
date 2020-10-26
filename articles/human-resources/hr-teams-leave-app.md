---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929985"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="5bc8e-103">在 Teams 中管理请假</span><span class="sxs-lookup"><span data-stu-id="5bc8e-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5bc8e-104">可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="5bc8e-105">您可以与机器人交互来请求信息和开始请假请求。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="5bc8e-106">**休假**选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="5bc8e-107">此外，您可以在 Human Resources 应用之外在团队和聊天中发送有关您的近期休假的人员信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="5bc8e-108">安装应用</span><span class="sxs-lookup"><span data-stu-id="5bc8e-108">Install the app</span></span>

<span data-ttu-id="5bc8e-109">可以在 Teams 商店中找到 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="5bc8e-110">在 Microsoft Teams 中，选择省略号。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams 休假应用省略号](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="5bc8e-112">搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams 休假应用 HR 磁贴](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="5bc8e-114">选择**添加**按钮安装应用。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams 休假应用安装](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="5bc8e-116">如果应用不让您自动登录，请选择**设置**选项卡登录。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams 休假应用“设置”选项卡](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="5bc8e-118">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="5bc8e-119">如果可以访问多个 Human Resources 实例，可以在**设置**选项卡中选择要连接哪个环境。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="5bc8e-120">此应用现在支持系统管理员安全角色。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="5bc8e-121">使用机器人</span><span class="sxs-lookup"><span data-stu-id="5bc8e-121">Use the bot</span></span>

<span data-ttu-id="5bc8e-122">安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams 休假应用机器人欢迎消息](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="5bc8e-124">首次与机器人交互时，可能需要登录。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="5bc8e-125">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="5bc8e-126">可以让机器人：</span><span class="sxs-lookup"><span data-stu-id="5bc8e-126">You can ask the bot to:</span></span>

- <span data-ttu-id="5bc8e-127">显示您等记的每个休假类型的休假余额信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams 休假应用显示余额](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="5bc8e-129">显示有关特定休假类型的其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams 休假应用显示详细信息](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="5bc8e-131">为您启动休假请求。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-131">Start a leave request for you.</span></span>

   ![Human Resources Teams 休假应用请假](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="5bc8e-133">开始请假后，可以直接在卡片内调整天数。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teams 休假应用编辑请求](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="5bc8e-135">输入完信息后，选择**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="5bc8e-136">也可以选择**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teams 休假应用提交请求](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="5bc8e-138">在 Teams 中管理休假</span><span class="sxs-lookup"><span data-stu-id="5bc8e-138">Manage your leave in Teams</span></span>

<span data-ttu-id="5bc8e-139">**休假**选项卡可用于查看：</span><span class="sxs-lookup"><span data-stu-id="5bc8e-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="5bc8e-140">您等记的每个休假类型的余额信息</span><span class="sxs-lookup"><span data-stu-id="5bc8e-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="5bc8e-141">近期请假</span><span class="sxs-lookup"><span data-stu-id="5bc8e-141">Upcoming leave requests</span></span>

- <span data-ttu-id="5bc8e-142">休假请求</span><span class="sxs-lookup"><span data-stu-id="5bc8e-142">Time-off requests</span></span>

- <span data-ttu-id="5bc8e-143">草稿请假</span><span class="sxs-lookup"><span data-stu-id="5bc8e-143">Draft leave requests</span></span>

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="5bc8e-145">创建新请求</span><span class="sxs-lookup"><span data-stu-id="5bc8e-145">Create a new request</span></span>

1. <span data-ttu-id="5bc8e-146">若要创建新休假请求，请选择**新请求**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams 休假应用新请求](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="5bc8e-148">输入请假天数，然后选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams 休假应用添加休假](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="5bc8e-150">如果适用，输入原因代码。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="5bc8e-151">并且输入任何注释和添加任何附件。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="5bc8e-152">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5bc8e-153">也可以键入**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="5bc8e-154">管理草稿请求</span><span class="sxs-lookup"><span data-stu-id="5bc8e-154">Manage draft requests</span></span>

1. <span data-ttu-id="5bc8e-155">选择**草稿**选项卡。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams 休假应用“草稿”选项卡](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="5bc8e-157">选择铅笔编辑请求，或选择废纸篓删除请求。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="5bc8e-158">进行任何必要更改。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-158">Make any necessary changes.</span></span> <span data-ttu-id="5bc8e-159">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5bc8e-160">也可以选择**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams 休假应用编辑草稿](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="5bc8e-162">响应 Teams 通知</span><span class="sxs-lookup"><span data-stu-id="5bc8e-162">Respond to Teams notifications</span></span>

<span data-ttu-id="5bc8e-163">当您或作为审批者的您的下属工作人员提交请假时，您将在 Teams 中的 Human Resources 应用内收到通知。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="5bc8e-164">您可以选择通知进行查看。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-164">You can select the notification to view it.</span></span> <span data-ttu-id="5bc8e-165">也会在**聊天**区域中显示通知。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="5bc8e-166">如果您是审批者，您可以在通知中选择**批准**或**拒绝**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="5bc8e-167">还可以提供可选消息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-167">You can also provide an optional message.</span></span>

![Human Resources Teams 中的请假通知](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="5bc8e-169">向您的同事发送近期休假信息</span><span class="sxs-lookup"><span data-stu-id="5bc8e-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="5bc8e-170">安装 Teams 的 Human Resources 应用后，您可以轻松地在团队或聊天中向同事发送您的近期休假的信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="5bc8e-171">在 Teams 中的团队或聊天中，选择聊天窗口下方的 Human Resources 按钮。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![聊天窗口下的 Human Resources 按钮](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="5bc8e-173">选择您要共享的休假请求。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-173">Select the leave request you want to share.</span></span> <span data-ttu-id="5bc8e-174">如果要共享休假请求草稿，请先选择**草稿**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![选择要共享的近期休假请求](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="5bc8e-176">您的休假请求将显示在聊天中。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-176">Your leave request will display in the chat.</span></span>

![Human Resources 休假请求卡](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="5bc8e-178">如果您共享了请求草稿，它将显示为草稿：</span><span class="sxs-lookup"><span data-stu-id="5bc8e-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources 休假请求草稿卡](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="5bc8e-180">查看您的休假日历</span><span class="sxs-lookup"><span data-stu-id="5bc8e-180">View your team's leave calendar</span></span>

<span data-ttu-id="5bc8e-181">如果您是具有直接下属的的经理，则可以查看团队的批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="5bc8e-182">在 Teams 中的 Human Resources 应用内，选择**请假**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="5bc8e-183">选择 **Team 日历**。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-183">Select **Team calendar**.</span></span>

   ![在 Human Resources Teams 应用中查看日历](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="5bc8e-185">日历显示直接下属的已批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Human Resources Teams 应用中的请假](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="5bc8e-187">疑难解答</span><span class="sxs-lookup"><span data-stu-id="5bc8e-187">Troubleshooting</span></span>

<span data-ttu-id="5bc8e-188">如果您在登录或使用 Human Resources Teams 应用时遇到问题，请尝试按照以下疑难解答说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="5bc8e-189">如果在进行疑难解答后仍有问题，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="5bc8e-190">有关详细信息，请参阅[获取支持](hr-admin-troubleshooting-support.md)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="5bc8e-191">无法登录到 Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="5bc8e-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="5bc8e-192">如果您无法登录该应用，则可能是您用来登录 Microsoft Teams 的帐户与 Dynamics 365 Human Resources 中的员工记录无关。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5bc8e-193">请与系统管理员联系，以确保您的员工记录已正确关联。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="5bc8e-194">在 Teams 中的 Human Resources 应用中审批请假请求时出错</span><span class="sxs-lookup"><span data-stu-id="5bc8e-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="5bc8e-195">如果您在尝试在 Teams 应用中审批请假请求时收到错误，请执行以下疑难解答步骤：</span><span class="sxs-lookup"><span data-stu-id="5bc8e-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="5bc8e-196">验证您用于登录 Microsoft Teams 的帐户是否与用于访问 Dynamics 365 Human Resources 的帐户相同。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="5bc8e-197">通过检查请假审批的工作流设置，验证您是否是该请求的有效审批者。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="5bc8e-198">有关请假请求工作流的详细信息，请参阅[创建请假请求工作流](hr-leave-and-absence-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="5bc8e-199">隐私声明</span><span class="sxs-lookup"><span data-stu-id="5bc8e-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="5bc8e-200">Microsoft 语言理解智能服务 (LUIS)</span><span class="sxs-lookup"><span data-stu-id="5bc8e-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="5bc8e-201">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="5bc8e-202">“搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="5bc8e-203">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="5bc8e-204">LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="5bc8e-205">然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="5bc8e-206">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="5bc8e-207">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5bc8e-208">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="5bc8e-209">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="5bc8e-210">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="5bc8e-211">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="5bc8e-212">Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="5bc8e-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="5bc8e-213">使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="5bc8e-214">Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="5bc8e-215">此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="5bc8e-216">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="5bc8e-217">与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="5bc8e-218">此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="5bc8e-219">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="5bc8e-220">要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="5bc8e-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc8e-221">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bc8e-221">See also</span></span>

[<span data-ttu-id="5bc8e-222">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5bc8e-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="5bc8e-223">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="5bc8e-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="5bc8e-224">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="5bc8e-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
