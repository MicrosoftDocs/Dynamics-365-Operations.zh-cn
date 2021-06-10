---
title: Teams 中的 Human Resources 应用
description: 此主题介绍 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用。
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1cceb15d64215cb8d5c996df792e863d466f87d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053555"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="0414d-103">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="0414d-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0414d-104">员工可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="0414d-105">员工可以与机器人交互以请求信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="0414d-106">**休假** 选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="0414d-107">此外，他们可以在 Human Resources 应用之外在团队和聊天中发送有关近期休假的人员信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams 休假应用机器人](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources 休假请求卡](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="0414d-111">安装和设置</span><span class="sxs-lookup"><span data-stu-id="0414d-111">Install and setup</span></span>

<span data-ttu-id="0414d-112">可以在 Teams 商店中找到 Dynamics 365 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="0414d-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="0414d-113">有关安装 Teams 应用的信息，请参阅[在 Teams 中管理请假](hr-teams-leave-app.md)。</span><span class="sxs-lookup"><span data-stu-id="0414d-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="0414d-114">有关在 Teams 中管理应用权限的信息，请参阅[在 Microsoft Teams 中管理应用权限策略](/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="0414d-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="0414d-115">如果要让用户在应用中查看休假和缺勤日历，您需要在“功能管理”中启用 **Teams 中的休假和缺勤日历**。</span><span class="sxs-lookup"><span data-stu-id="0414d-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="0414d-116">有关启用功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="0414d-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="0414d-117">在 Teams 中启用 Human Resources 应用通知</span><span class="sxs-lookup"><span data-stu-id="0414d-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="0414d-118">如果希望用户在 Teams 应用中接收请假通知，必须在 Dynamics 365 Human Resources 中启用通知。</span><span class="sxs-lookup"><span data-stu-id="0414d-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="0414d-119">只有已登录 Teams 且使用 Dynamics 365 Human Resources Teams 应用的用户才会收到通知。</span><span class="sxs-lookup"><span data-stu-id="0414d-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="0414d-120">在 Human Resources 中，选择 **系统管理**。</span><span class="sxs-lookup"><span data-stu-id="0414d-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="0414d-121">选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="0414d-121">Select **Links**.</span></span>

3. <span data-ttu-id="0414d-122">在 **设置** 下，选择 **系统参数**。</span><span class="sxs-lookup"><span data-stu-id="0414d-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="0414d-123">在 **常规** 选项卡中，将 **启用 Teams 应用通知** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="0414d-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![在系统参数中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="0414d-125">若要为所有用户打开 Teams 通知，请在提示符处选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="0414d-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![为所有用户启用 Teams 通知](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="0414d-127">为单个用户打开或关闭 Teams 通知</span><span class="sxs-lookup"><span data-stu-id="0414d-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="0414d-128">启用 Dynamics 365 Human Resources Teams 应用通知最后，可以为单个用户打开或关闭通知。</span><span class="sxs-lookup"><span data-stu-id="0414d-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="0414d-129">在 Human Resources 中，选择 **系统管理**。</span><span class="sxs-lookup"><span data-stu-id="0414d-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="0414d-130">选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="0414d-130">Select **Links**.</span></span>

3. <span data-ttu-id="0414d-131">在 **用户** 下，选择 **用户选项**。</span><span class="sxs-lookup"><span data-stu-id="0414d-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="0414d-132">选择 **工作流** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="0414d-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="0414d-133">将 **启用 Teams 应用通知** 设置为 **是** 为用户启用通知，或设置为 **否** 为用户禁用通知。</span><span class="sxs-lookup"><span data-stu-id="0414d-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![在“用户选项工作流”选项卡中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="0414d-135">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0414d-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="0414d-136">支持的语言</span><span class="sxs-lookup"><span data-stu-id="0414d-136">Supported languages</span></span>

<span data-ttu-id="0414d-137">Teams 中的 Dynamics 365 Human Resources 应用支持以下语言：</span><span class="sxs-lookup"><span data-stu-id="0414d-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="0414d-138">区域设置 ID</span><span class="sxs-lookup"><span data-stu-id="0414d-138">Locale ID</span></span> | <span data-ttu-id="0414d-139">语言</span><span class="sxs-lookup"><span data-stu-id="0414d-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="0414d-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="0414d-140">de-DE</span></span> | <span data-ttu-id="0414d-141">德语(德国)</span><span class="sxs-lookup"><span data-stu-id="0414d-141">German (Germany)</span></span> |
| <span data-ttu-id="0414d-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="0414d-142">es-ES</span></span> | <span data-ttu-id="0414d-143">西班牙语(西班牙)</span><span class="sxs-lookup"><span data-stu-id="0414d-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="0414d-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="0414d-144">es-MX</span></span> | <span data-ttu-id="0414d-145">西班牙语(墨西哥)</span><span class="sxs-lookup"><span data-stu-id="0414d-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="0414d-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="0414d-146">fr-CA</span></span> | <span data-ttu-id="0414d-147">法语(加拿大)</span><span class="sxs-lookup"><span data-stu-id="0414d-147">French (Canada)</span></span> |
| <span data-ttu-id="0414d-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="0414d-148">fr-FR</span></span> | <span data-ttu-id="0414d-149">法语(法国)</span><span class="sxs-lookup"><span data-stu-id="0414d-149">French (France)</span></span> |
| <span data-ttu-id="0414d-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="0414d-150">it-IT</span></span> | <span data-ttu-id="0414d-151">意大利语(意大利)</span><span class="sxs-lookup"><span data-stu-id="0414d-151">Italian (Italy)</span></span> |
| <span data-ttu-id="0414d-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="0414d-152">nl-NL</span></span> | <span data-ttu-id="0414d-153">荷兰语(荷兰)</span><span class="sxs-lookup"><span data-stu-id="0414d-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="0414d-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0414d-154">pt-BR</span></span> | <span data-ttu-id="0414d-155">葡萄牙语(巴西)</span><span class="sxs-lookup"><span data-stu-id="0414d-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="0414d-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="0414d-156">tr-TR</span></span> | <span data-ttu-id="0414d-157">土耳其语(土耳其)</span><span class="sxs-lookup"><span data-stu-id="0414d-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="0414d-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="0414d-158">zh-CN</span></span> | <span data-ttu-id="0414d-159">中文(简体)</span><span class="sxs-lookup"><span data-stu-id="0414d-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="0414d-160">说明</span><span class="sxs-lookup"><span data-stu-id="0414d-160">Notes</span></span>

<span data-ttu-id="0414d-161">以下工作项计划用于将来版本：</span><span class="sxs-lookup"><span data-stu-id="0414d-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="0414d-162">工作项</span><span class="sxs-lookup"><span data-stu-id="0414d-162">Work item</span></span> | <span data-ttu-id="0414d-163">状态</span><span class="sxs-lookup"><span data-stu-id="0414d-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="0414d-164">提交将来日期的请假时，余额不正确。</span><span class="sxs-lookup"><span data-stu-id="0414d-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="0414d-165">预测尚不可用。</span><span class="sxs-lookup"><span data-stu-id="0414d-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="0414d-166">显示当前日期的余额。</span><span class="sxs-lookup"><span data-stu-id="0414d-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="0414d-167">不能取消 **审查中** 请求。</span><span class="sxs-lookup"><span data-stu-id="0414d-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="0414d-168">现在不支持此功能，将来的版本中将增加此功能。</span><span class="sxs-lookup"><span data-stu-id="0414d-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="0414d-169">将计算截止当天的余额信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="0414d-170">系统现在不显示截止实际期间的余额，即使已在“休假和缺勤”参数中配置。</span><span class="sxs-lookup"><span data-stu-id="0414d-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="0414d-171">疑难解答</span><span class="sxs-lookup"><span data-stu-id="0414d-171">Troubleshooting</span></span>

<span data-ttu-id="0414d-172">如果用户在登录或使用 Human Resources Teams 应用时遇到问题，请尝试按照以下疑难解答说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="0414d-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="0414d-173">如果在进行疑难解答后仍有问题，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="0414d-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="0414d-174">有关详细信息，请参阅[获取支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。</span><span class="sxs-lookup"><span data-stu-id="0414d-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="0414d-175">无法登录到 Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="0414d-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="0414d-176">如果用户由于无法登录应用而与您联系，请确认他们在 Human Resources 中具有关联的员工记录。</span><span class="sxs-lookup"><span data-stu-id="0414d-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="0414d-177">在 Teams 中的 Human Resources 应用中审批请假请求时出错</span><span class="sxs-lookup"><span data-stu-id="0414d-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="0414d-178">如果用户在尝试批准 Teams 应用中的请假请求时收到错误，请尝试以下疑难解答步骤：</span><span class="sxs-lookup"><span data-stu-id="0414d-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="0414d-179">验证其 Teams 帐户与用于访问 Human Resources 的帐户相同。</span><span class="sxs-lookup"><span data-stu-id="0414d-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="0414d-180">通过检查请假审批的工作流设置，验证他们是否是该请求的有效审批者。</span><span class="sxs-lookup"><span data-stu-id="0414d-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="0414d-181">有关请假请求工作流的详细信息，请参阅[创建请假请求工作流](hr-leave-and-absence-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="0414d-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="0414d-182">休假审批者收不到审批休假申请的 Teams 聊天消息</span><span class="sxs-lookup"><span data-stu-id="0414d-182">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="0414d-183">请确保为环境和用户启用了通知。</span><span class="sxs-lookup"><span data-stu-id="0414d-183">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="0414d-184">有关详细信息，请参阅[在 Teams 中启用 Human Resources 应用通知](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)和[为单个用户打开或关闭 Teams 通知](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)。</span><span class="sxs-lookup"><span data-stu-id="0414d-184">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="0414d-185">确保用户使用与用于审批休假申请相同的凭据登录到 **聊天** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="0414d-185">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="0414d-186">使用消息“注销”，然后使用“登录”以正确的凭据登录。</span><span class="sxs-lookup"><span data-stu-id="0414d-186">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="0414d-187">如果问题仍然存在，请以系统管理员身份检查业务事件系统批处理作业的状态。</span><span class="sxs-lookup"><span data-stu-id="0414d-187">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="0414d-188">如果是处于等待或执行阶段，请过几分钟再次检查。</span><span class="sxs-lookup"><span data-stu-id="0414d-188">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="0414d-189">如果状态保持不变，请记录支持票证，以便我们的团队可以帮助解决问题。</span><span class="sxs-lookup"><span data-stu-id="0414d-189">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0414d-190">隐私声明</span><span class="sxs-lookup"><span data-stu-id="0414d-190">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0414d-191">Microsoft 语言理解智能服务 (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0414d-191">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0414d-192">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="0414d-192">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0414d-193">“搜索帐户 Contoso”之类的用户输入将传递到一个名为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="0414d-193">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0414d-194">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="0414d-194">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0414d-195">LUIS 服务用于理清或了解用户输入的意图（在此示例中，意图为查找信息）和目标实体（在此示例中，意图实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="0414d-195">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0414d-196">然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="0414d-196">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span>

<span data-ttu-id="0414d-197">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="0414d-197">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0414d-198">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="0414d-198">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0414d-199">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="0414d-199">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0414d-200">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="0414d-200">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0414d-201">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="0414d-201">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0414d-202">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="0414d-202">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="0414d-203">Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0414d-203">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="0414d-204">使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。</span><span class="sxs-lookup"><span data-stu-id="0414d-204">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="0414d-205">Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="0414d-205">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0414d-206">此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。</span><span class="sxs-lookup"><span data-stu-id="0414d-206">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0414d-207">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="0414d-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="0414d-208">与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="0414d-208">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="0414d-209">此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。</span><span class="sxs-lookup"><span data-stu-id="0414d-209">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0414d-210">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="0414d-210">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="0414d-211">要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="0414d-211">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="0414d-212">请参阅</span><span class="sxs-lookup"><span data-stu-id="0414d-212">See also</span></span> 

[<span data-ttu-id="0414d-213">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0414d-213">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0414d-214">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="0414d-214">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0414d-215">管理 Teams 中的休假申请</span><span class="sxs-lookup"><span data-stu-id="0414d-215">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]