---
title: Teams 中的 Human Resources 应用
description: 此主题介绍 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用。
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828906"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="bd8ea-103">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="bd8ea-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bd8ea-104">员工可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="bd8ea-105">员工可以与机器人交互以请求信息。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="bd8ea-106">**休假**选项卡提供更详细的信息。此外，他们还可以发送有关团队中的近期休假以及 Human Resources 应用外的聊天的人员信息。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams 休假应用机器人](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources 休假请求卡](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="bd8ea-110">安装和设置</span><span class="sxs-lookup"><span data-stu-id="bd8ea-110">Install and setup</span></span>

<span data-ttu-id="bd8ea-111">可以在 Teams 商店中找到 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="bd8ea-112">有关安装 Teams 应用的信息，请参阅[在 Teams 中管理请假](hr-teams-leave-app.md)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="bd8ea-113">有关在 Teams 中管理应用权限的信息，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="bd8ea-114">在 Teams 中启用 Human Resources 应用通知</span><span class="sxs-lookup"><span data-stu-id="bd8ea-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="bd8ea-115">如果希望用户在 Teams 应用中接收请假通知，必须在 Human Resources 中启用通知。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="bd8ea-116">只有已登录 Teams 且使用 Human Resources Teams 应用的用户才会收到通知。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="bd8ea-117">在 Human Resources 中，选择**系统管理**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="bd8ea-118">选择**链接**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-118">Select **Links**.</span></span>

3. <span data-ttu-id="bd8ea-119">在**设置**下，选择**系统参数**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="bd8ea-120">在**常规**选项卡中，将**启用 Teams 应用通知**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![在系统参数中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="bd8ea-122">若要为所有用户打开 Teams 通知，请在提示符处选择**是**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![为所有用户启用 Teams 通知](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="bd8ea-124">为单个用户打开或关闭 Teams 通知</span><span class="sxs-lookup"><span data-stu-id="bd8ea-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="bd8ea-125">启用 Human Resources Teams 应用通知最后，可以为单个用户打开或关闭通知。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="bd8ea-126">在 Human Resources 中，选择**系统管理**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="bd8ea-127">选择**链接**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-127">Select **Links**.</span></span>

3. <span data-ttu-id="bd8ea-128">在**用户**下，选择**用户选项**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="bd8ea-129">选择**工作流**选项卡。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="bd8ea-130">将**启用 Teams 应用通知**设置为**是**为用户启用通知，或设置为**否**为用户禁用通知。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![在“用户选项工作流”选项卡中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="bd8ea-132">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="bd8ea-133">已知问题</span><span class="sxs-lookup"><span data-stu-id="bd8ea-133">Known issues</span></span>

| <span data-ttu-id="bd8ea-134">签发</span><span class="sxs-lookup"><span data-stu-id="bd8ea-134">Issue</span></span> | <span data-ttu-id="bd8ea-135">状态</span><span class="sxs-lookup"><span data-stu-id="bd8ea-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="bd8ea-136">水平滚动不适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="bd8ea-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="bd8ea-137">水平滚动在 iOS 或台式机设备上不是问题。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="bd8ea-138">我们正在解决 Android 上的问题。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="bd8ea-139">提交将来日期的请假时，余额不正确。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="bd8ea-140">预测尚不可用。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="bd8ea-141">显示当前日期的余额。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="bd8ea-142">不能取消**审查中**请求。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="bd8ea-143">现在不支持此功能，将来的版本中将增加此功能。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="bd8ea-144">将计算截止当天的余额信息。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="bd8ea-145">系统现在不显示截止实际期间的余额，即使已在“休假和缺勤”参数中配置。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="bd8ea-146">隐私声明</span><span class="sxs-lookup"><span data-stu-id="bd8ea-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="bd8ea-147">Microsoft 语言理解智能服务 (LUIS)</span><span class="sxs-lookup"><span data-stu-id="bd8ea-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="bd8ea-148">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="bd8ea-149">“搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="bd8ea-150">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="bd8ea-151">LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="bd8ea-152">然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="bd8ea-153">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="bd8ea-154">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bd8ea-155">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="bd8ea-156">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="bd8ea-157">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="bd8ea-158">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="bd8ea-159">Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="bd8ea-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="bd8ea-160">使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="bd8ea-161">Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="bd8ea-162">此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="bd8ea-163">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="bd8ea-164">与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="bd8ea-165">此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="bd8ea-166">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="bd8ea-167">要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="bd8ea-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="bd8ea-168">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd8ea-168">See also</span></span> 

[<span data-ttu-id="bd8ea-169">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd8ea-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="bd8ea-170">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="bd8ea-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="bd8ea-171">管理 Teams 中的休假申请</span><span class="sxs-lookup"><span data-stu-id="bd8ea-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

