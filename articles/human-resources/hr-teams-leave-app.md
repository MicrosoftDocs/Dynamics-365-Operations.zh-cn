---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766752"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="0fb61-103">在 Teams 中管理请假</span><span class="sxs-lookup"><span data-stu-id="0fb61-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="0fb61-104">可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="0fb61-105">可以与机器人交互以请求信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="0fb61-106">**休假**选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="0fb61-107">安装应用</span><span class="sxs-lookup"><span data-stu-id="0fb61-107">Install the app</span></span>

<span data-ttu-id="0fb61-108">可以在 Teams 商店中找到 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="0fb61-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="0fb61-109">在 Microsoft Teams 中，选择省略号。</span><span class="sxs-lookup"><span data-stu-id="0fb61-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams 休假应用省略号](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="0fb61-111">搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="0fb61-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams 休假应用 HR 磁贴](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="0fb61-113">选择**添加**按钮安装应用。</span><span class="sxs-lookup"><span data-stu-id="0fb61-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams 休假应用安装](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="0fb61-115">如果应用不让您自动登录，请选择**设置**选项卡登录。</span><span class="sxs-lookup"><span data-stu-id="0fb61-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams 休假应用“设置”选项卡](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="0fb61-117">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="0fb61-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="0fb61-118">如果可以访问多个 Human Resources 实例，可以在**设置**选项卡中选择要连接哪个环境。</span><span class="sxs-lookup"><span data-stu-id="0fb61-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="0fb61-119">此应用现在支持系统管理员安全角色，并且在您使用系统管理员帐户时显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="0fb61-120">若要使用其他帐户登录，请在**设置**选项卡上选择**切换帐户**按钮，然后使用无系统管理员权限的用户帐户登录。</span><span class="sxs-lookup"><span data-stu-id="0fb61-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="0fb61-121">使用机器人</span><span class="sxs-lookup"><span data-stu-id="0fb61-121">Use the bot</span></span>

<span data-ttu-id="0fb61-122">安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。</span><span class="sxs-lookup"><span data-stu-id="0fb61-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams 休假应用机器人欢迎消息](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="0fb61-124">首次与机器人交互时，可能需要登录。</span><span class="sxs-lookup"><span data-stu-id="0fb61-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="0fb61-125">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="0fb61-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="0fb61-126">可以让机器人：</span><span class="sxs-lookup"><span data-stu-id="0fb61-126">You can ask the bot to:</span></span>

- <span data-ttu-id="0fb61-127">显示您等记的每个休假类型的休假余额信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams 休假应用显示余额](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="0fb61-129">显示有关特定休假类型的其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams 休假应用显示详细信息](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="0fb61-131">为您启动休假请求。</span><span class="sxs-lookup"><span data-stu-id="0fb61-131">Start a leave request for you.</span></span>

   ![Human Resources Teams 休假应用请假](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="0fb61-133">开始请假后，可以直接在卡片内调整天数。</span><span class="sxs-lookup"><span data-stu-id="0fb61-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teams 休假应用编辑请求](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="0fb61-135">输入完信息后，选择**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="0fb61-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="0fb61-136">也可以选择**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="0fb61-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teams 休假应用提交请求](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="0fb61-138">在 Teams 中管理休假</span><span class="sxs-lookup"><span data-stu-id="0fb61-138">Manage your leave in Teams</span></span>

<span data-ttu-id="0fb61-139">**休假**选项卡可用于查看：</span><span class="sxs-lookup"><span data-stu-id="0fb61-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="0fb61-140">您等记的每个休假类型的余额信息</span><span class="sxs-lookup"><span data-stu-id="0fb61-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="0fb61-141">近期请假</span><span class="sxs-lookup"><span data-stu-id="0fb61-141">Upcoming leave requests</span></span>

- <span data-ttu-id="0fb61-142">休假请求</span><span class="sxs-lookup"><span data-stu-id="0fb61-142">Time-off requests</span></span>

- <span data-ttu-id="0fb61-143">草稿请假</span><span class="sxs-lookup"><span data-stu-id="0fb61-143">Draft leave requests</span></span>

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="0fb61-145">创建新请求</span><span class="sxs-lookup"><span data-stu-id="0fb61-145">Create a new request</span></span>

1. <span data-ttu-id="0fb61-146">若要创建新休假请求，请选择**新请求**。</span><span class="sxs-lookup"><span data-stu-id="0fb61-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams 休假应用新请求](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="0fb61-148">输入请假天数，然后选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="0fb61-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams 休假应用添加休假](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="0fb61-150">如果适用，输入原因代码。</span><span class="sxs-lookup"><span data-stu-id="0fb61-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="0fb61-151">并且输入任何注释和添加任何附件。</span><span class="sxs-lookup"><span data-stu-id="0fb61-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="0fb61-152">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="0fb61-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="0fb61-153">也可以键入**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="0fb61-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="0fb61-154">管理草稿请求</span><span class="sxs-lookup"><span data-stu-id="0fb61-154">Manage draft requests</span></span>

1. <span data-ttu-id="0fb61-155">选择**草稿**选项卡。</span><span class="sxs-lookup"><span data-stu-id="0fb61-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams 休假应用“草稿”选项卡](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="0fb61-157">选择铅笔编辑请求，或选择废纸篓删除请求。</span><span class="sxs-lookup"><span data-stu-id="0fb61-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="0fb61-158">进行任何必要更改。</span><span class="sxs-lookup"><span data-stu-id="0fb61-158">Make any necessary changes.</span></span> <span data-ttu-id="0fb61-159">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="0fb61-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="0fb61-160">也可以选择**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="0fb61-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams 休假应用编辑草稿](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="0fb61-162">Teams 通知</span><span class="sxs-lookup"><span data-stu-id="0fb61-162">Teams notifications</span></span>

<span data-ttu-id="0fb61-163">当您或作为审批者的您的下属工作人员提交请假时，您将在 Teams 中的 Human Resources 应用内收到通知。</span><span class="sxs-lookup"><span data-stu-id="0fb61-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="0fb61-164">您可以选择通知进行查看。</span><span class="sxs-lookup"><span data-stu-id="0fb61-164">You can select the notification to view it.</span></span> <span data-ttu-id="0fb61-165">也会在**聊天**区域中显示通知。</span><span class="sxs-lookup"><span data-stu-id="0fb61-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="0fb61-166">如果您是审批者，您可以在通知中选择**批准**或**拒绝**。</span><span class="sxs-lookup"><span data-stu-id="0fb61-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="0fb61-167">还可以提供可选消息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-167">You can also provide an optional message.</span></span>

![Human Resources Teams 中的请假通知](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="0fb61-169">查看您的休假日历</span><span class="sxs-lookup"><span data-stu-id="0fb61-169">View your team's leave calendar</span></span>

<span data-ttu-id="0fb61-170">如果您是具有直接下属的的经理，则可以查看团队的批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="0fb61-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="0fb61-171">在 Teams 中的 Human Resources 应用内，选择**请假**。</span><span class="sxs-lookup"><span data-stu-id="0fb61-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="0fb61-172">选择 **Team 日历**。</span><span class="sxs-lookup"><span data-stu-id="0fb61-172">Select **Team calendar**.</span></span>

   ![在 Human Resources Teams 应用中查看日历](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="0fb61-174">日历显示直接下属的已批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="0fb61-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Human Resources Teams 应用中的请假](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="0fb61-176">隐私声明</span><span class="sxs-lookup"><span data-stu-id="0fb61-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0fb61-177">Microsoft 语言理解智能服务 (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0fb61-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0fb61-178">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="0fb61-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0fb61-179">“搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="0fb61-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0fb61-180">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="0fb61-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0fb61-181">LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="0fb61-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0fb61-182">然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="0fb61-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="0fb61-183">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="0fb61-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0fb61-184">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="0fb61-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0fb61-185">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="0fb61-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0fb61-186">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="0fb61-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0fb61-187">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="0fb61-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0fb61-188">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="0fb61-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="0fb61-189">Microsoft Azure 事件网格和 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0fb61-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="0fb61-190">使用 Teams 中的 Dynamics 365 Human Resources 应用的通知功能时，某些客户数据会流到租户的 Human Resources 服务的部署地理区域之外。</span><span class="sxs-lookup"><span data-stu-id="0fb61-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="0fb61-191">Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="0fb61-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0fb61-192">此数据可以存储最多 24 小时和在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。</span><span class="sxs-lookup"><span data-stu-id="0fb61-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fb61-193">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fb61-193">See also</span></span>

[<span data-ttu-id="0fb61-194">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0fb61-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0fb61-195">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="0fb61-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0fb61-196">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="0fb61-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
