---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097251"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="0350b-103">管理 Teams 中的休假申请</span><span class="sxs-lookup"><span data-stu-id="0350b-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0350b-104">可通过 Microsoft Teams 中的 Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="0350b-105">您可以与机器人交互来请求信息和开始请假请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="0350b-106">**休假** 选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="0350b-107">您还可以在 Human Resources 应用之外在 Teams 和聊天中发送有关您的近期休假的人员信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="0350b-108">安装应用</span><span class="sxs-lookup"><span data-stu-id="0350b-108">Install the app</span></span>

<span data-ttu-id="0350b-109">可以在 Teams 商店中找到 Dynamics 365 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="0350b-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="0350b-110">在 Microsoft Teams 中，导航到应用列表。</span><span class="sxs-lookup"><span data-stu-id="0350b-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="0350b-111">搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="0350b-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="0350b-112">选择 **添加** 按钮安装应用。</span><span class="sxs-lookup"><span data-stu-id="0350b-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="0350b-113">如果应用不让您自动登录，请选择 **设置** 选项卡登录。</span><span class="sxs-lookup"><span data-stu-id="0350b-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="0350b-114">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="0350b-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="0350b-115">如果可以访问多个 Human Resources 实例，可以在 **设置** 选项卡中选择要连接哪个环境。</span><span class="sxs-lookup"><span data-stu-id="0350b-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="0350b-116">此应用现在支持系统管理员安全角色。</span><span class="sxs-lookup"><span data-stu-id="0350b-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="0350b-117">使用机器人</span><span class="sxs-lookup"><span data-stu-id="0350b-117">Use the bot</span></span>

<span data-ttu-id="0350b-118">安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。</span><span class="sxs-lookup"><span data-stu-id="0350b-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="0350b-119">首次与机器人交互时，可能需要登录。</span><span class="sxs-lookup"><span data-stu-id="0350b-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="0350b-120">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="0350b-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="0350b-121">可以让机器人：</span><span class="sxs-lookup"><span data-stu-id="0350b-121">You can ask the bot to:</span></span>

- <span data-ttu-id="0350b-122">查看您当前的休假余额。</span><span class="sxs-lookup"><span data-stu-id="0350b-122">View your current leave balances.</span></span> <span data-ttu-id="0350b-123">例如，发送一条消息“查看休假余额”。</span><span class="sxs-lookup"><span data-stu-id="0350b-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="0350b-124">为您启动休假请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-124">Start a leave request for you.</span></span> <span data-ttu-id="0350b-125">例如，发送一条消息“休假”或“我想在下周四和周五休假”，以更具体地提出休假类型的休假请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![在 Teams 聊天中发起休假请求](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="0350b-127">聊天机器人将为您填充休假请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="0350b-128">选择 **请求休假**，然后编辑您的请求的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="0350b-129">如果您想为同一日期的多个休假类型提交休假请求，从 **更多选项** 菜单中选择 **拆分休假日** 选项。</span><span class="sxs-lookup"><span data-stu-id="0350b-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="0350b-130">如果您在休假请求单位为天时选择半天休假，您可以通过从 **更多选项** 菜单中选择 **半天定义** 选项来指定是要申请上半天还是下半天休息时间。</span><span class="sxs-lookup"><span data-stu-id="0350b-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![半天定义](./media/HalfDayDefinitions.png)

- <span data-ttu-id="0350b-132">完成休假请求详细信息的编辑后，选择 **提交** 提交请求进行审批。</span><span class="sxs-lookup"><span data-stu-id="0350b-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![提交休假请求](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="0350b-134">在 Teams 中管理休假</span><span class="sxs-lookup"><span data-stu-id="0350b-134">Manage your leave in Teams</span></span>

<span data-ttu-id="0350b-135">**休假** 选项卡可用于查看：</span><span class="sxs-lookup"><span data-stu-id="0350b-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="0350b-136">您等记的每个休假类型的余额信息</span><span class="sxs-lookup"><span data-stu-id="0350b-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="0350b-137">近期请假</span><span class="sxs-lookup"><span data-stu-id="0350b-137">Upcoming leave requests</span></span>

- <span data-ttu-id="0350b-138">休假请求</span><span class="sxs-lookup"><span data-stu-id="0350b-138">Time-off requests</span></span>

- <span data-ttu-id="0350b-139">草稿请假</span><span class="sxs-lookup"><span data-stu-id="0350b-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="0350b-140">创建新请求</span><span class="sxs-lookup"><span data-stu-id="0350b-140">Create a new request</span></span>

1. <span data-ttu-id="0350b-141">若要创建新休假请求，请选择 **新请求**。</span><span class="sxs-lookup"><span data-stu-id="0350b-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="0350b-142">输入请假天数，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0350b-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams 休假应用添加休假](./media/TimeOffHours.png)

3. <span data-ttu-id="0350b-144">如果适用，输入原因代码。</span><span class="sxs-lookup"><span data-stu-id="0350b-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="0350b-145">并且输入任何注释和添加任何附件。</span><span class="sxs-lookup"><span data-stu-id="0350b-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="0350b-146">如果您想针对不同的休假类型提交同一日期的多个休假请求条目，从 **更多选项** 菜单中选择 **拆分休假日** 选项。</span><span class="sxs-lookup"><span data-stu-id="0350b-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="0350b-147">选择 **半天定义** 选项指定您要申请上半天还是下半天休假。</span><span class="sxs-lookup"><span data-stu-id="0350b-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="0350b-148">当休假请求单位为天且申请的金额为 0.5 天时，此选项可用。</span><span class="sxs-lookup"><span data-stu-id="0350b-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="0350b-149">输入完信息后，输入 **提交** 提交请求进行审批。</span><span class="sxs-lookup"><span data-stu-id="0350b-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="0350b-150">您也可以输入 **另存为草稿**，以后再回来提交。</span><span class="sxs-lookup"><span data-stu-id="0350b-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="0350b-151">管理草稿请求</span><span class="sxs-lookup"><span data-stu-id="0350b-151">Manage draft requests</span></span>

1. <span data-ttu-id="0350b-152">选择 **草稿** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="0350b-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="0350b-153">选择铅笔编辑请求，或选择废纸篓删除请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="0350b-154">进行任何必要更改。</span><span class="sxs-lookup"><span data-stu-id="0350b-154">Make any necessary changes.</span></span> <span data-ttu-id="0350b-155">输入完信息后，键入 **提交** 提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="0350b-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="0350b-156">也可以选择 **另存为草稿** 以后再回来。</span><span class="sxs-lookup"><span data-stu-id="0350b-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="0350b-157">响应 Teams 通知</span><span class="sxs-lookup"><span data-stu-id="0350b-157">Respond to Teams notifications</span></span>

<span data-ttu-id="0350b-158">当您或作为审批者的您的下属工作人员提交请假时，您将在 Teams 中的 Human Resources 应用内收到通知。</span><span class="sxs-lookup"><span data-stu-id="0350b-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="0350b-159">您可以选择通知进行查看。</span><span class="sxs-lookup"><span data-stu-id="0350b-159">You can select the notification to view it.</span></span> <span data-ttu-id="0350b-160">也会在 **聊天** 区域中显示通知。</span><span class="sxs-lookup"><span data-stu-id="0350b-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="0350b-161">如果您是审批者，您可以在通知中选择 **批准** 或 **拒绝**。</span><span class="sxs-lookup"><span data-stu-id="0350b-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="0350b-162">还可以提供可选消息。</span><span class="sxs-lookup"><span data-stu-id="0350b-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="0350b-163">向您的同事发送近期休假信息</span><span class="sxs-lookup"><span data-stu-id="0350b-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="0350b-164">安装 Teams 的 Human Resources 应用后，您可以轻松地在团队或聊天中向同事发送您的近期休假的信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="0350b-165">在 Teams 中的团队或聊天中，选择聊天窗口下方的 Human Resources 按钮。</span><span class="sxs-lookup"><span data-stu-id="0350b-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![聊天窗口下的 Human Resources 按钮](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="0350b-167">选择您要共享的休假请求。</span><span class="sxs-lookup"><span data-stu-id="0350b-167">Select the leave request you want to share.</span></span> <span data-ttu-id="0350b-168">如果要共享休假请求草稿，请先选择 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="0350b-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="0350b-169">您的休假请求将显示在聊天中。</span><span class="sxs-lookup"><span data-stu-id="0350b-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="0350b-170">如果您共享了草稿请求，它将显示为草稿。</span><span class="sxs-lookup"><span data-stu-id="0350b-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="0350b-171">查看您的休假日历</span><span class="sxs-lookup"><span data-stu-id="0350b-171">View your team's leave calendar</span></span>

<span data-ttu-id="0350b-172">如果您是具有直接下属的的经理，则可以查看团队的批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="0350b-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="0350b-173">在 Teams 中的 Human Resources 应用内，选择 **请假**。</span><span class="sxs-lookup"><span data-stu-id="0350b-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="0350b-174">选择 **Team 日历**。</span><span class="sxs-lookup"><span data-stu-id="0350b-174">Select **Team calendar**.</span></span> <span data-ttu-id="0350b-175">日历显示直接下属的已批准和待定请假。</span><span class="sxs-lookup"><span data-stu-id="0350b-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0350b-176">如果您看不到团队日历，请让管理员启用它。</span><span class="sxs-lookup"><span data-stu-id="0350b-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="0350b-177">有关详细信息，请参阅[安装和设置](hr-admin-teams-leave-app.md#install-and-setup)。</span><span class="sxs-lookup"><span data-stu-id="0350b-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="0350b-178">支持的语言</span><span class="sxs-lookup"><span data-stu-id="0350b-178">Supported languages</span></span>

<span data-ttu-id="0350b-179">Teams 中的 Dynamics 365 Human Resources 应用支持以下语言：</span><span class="sxs-lookup"><span data-stu-id="0350b-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="0350b-180">区域设置 ID</span><span class="sxs-lookup"><span data-stu-id="0350b-180">Locale ID</span></span> | <span data-ttu-id="0350b-181">语言</span><span class="sxs-lookup"><span data-stu-id="0350b-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="0350b-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="0350b-182">de-DE</span></span> | <span data-ttu-id="0350b-183">德语(德国)</span><span class="sxs-lookup"><span data-stu-id="0350b-183">German (Germany)</span></span> |
| <span data-ttu-id="0350b-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="0350b-184">es-ES</span></span> | <span data-ttu-id="0350b-185">西班牙语(西班牙)</span><span class="sxs-lookup"><span data-stu-id="0350b-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="0350b-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="0350b-186">es-MX</span></span> | <span data-ttu-id="0350b-187">西班牙语(墨西哥)</span><span class="sxs-lookup"><span data-stu-id="0350b-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="0350b-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="0350b-188">fr-CA</span></span> | <span data-ttu-id="0350b-189">法语(加拿大)</span><span class="sxs-lookup"><span data-stu-id="0350b-189">French (Canada)</span></span> |
| <span data-ttu-id="0350b-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="0350b-190">fr-FR</span></span> | <span data-ttu-id="0350b-191">法语(法国)</span><span class="sxs-lookup"><span data-stu-id="0350b-191">French (France)</span></span> |
| <span data-ttu-id="0350b-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="0350b-192">it-IT</span></span> | <span data-ttu-id="0350b-193">意大利语(意大利)</span><span class="sxs-lookup"><span data-stu-id="0350b-193">Italian (Italy)</span></span> |
| <span data-ttu-id="0350b-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="0350b-194">nl-NL</span></span> | <span data-ttu-id="0350b-195">荷兰语(荷兰)</span><span class="sxs-lookup"><span data-stu-id="0350b-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="0350b-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0350b-196">pt-BR</span></span> | <span data-ttu-id="0350b-197">葡萄牙语(巴西)</span><span class="sxs-lookup"><span data-stu-id="0350b-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="0350b-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="0350b-198">tr-TR</span></span> | <span data-ttu-id="0350b-199">土耳其语(土耳其)</span><span class="sxs-lookup"><span data-stu-id="0350b-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="0350b-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="0350b-200">zh-CN</span></span> | <span data-ttu-id="0350b-201">中文(简体)</span><span class="sxs-lookup"><span data-stu-id="0350b-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="0350b-202">疑难解答</span><span class="sxs-lookup"><span data-stu-id="0350b-202">Troubleshooting</span></span>

<span data-ttu-id="0350b-203">如果您在登录或使用 Dynamics 365 Human Resources Teams 应用时遇到问题，请尝试按照以下疑难解答说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="0350b-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="0350b-204">如果在进行疑难解答后仍有问题，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="0350b-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="0350b-205">有关详细信息，请参阅[获取支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。</span><span class="sxs-lookup"><span data-stu-id="0350b-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="0350b-206">无法登录到 Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="0350b-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="0350b-207">如果您无法登录该应用，则可能是您用来登录 Microsoft Teams 的帐户与 Dynamics 365 Human Resources 中的员工记录无关。</span><span class="sxs-lookup"><span data-stu-id="0350b-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0350b-208">请与系统管理员联系，以确保您的员工记录已正确关联。</span><span class="sxs-lookup"><span data-stu-id="0350b-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="0350b-209">翻译未正确显示</span><span class="sxs-lookup"><span data-stu-id="0350b-209">Translations don't display correctly</span></span>

<span data-ttu-id="0350b-210">如果翻译未按预期显示，请确保您在 Teams 中选择的语言与在 Human Resources **用户选项** 中选择的语言匹配。</span><span class="sxs-lookup"><span data-stu-id="0350b-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="0350b-211">在 Teams 中，查看 **设置** 中的 **应用语言**。</span><span class="sxs-lookup"><span data-stu-id="0350b-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams 设置](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="0350b-213">在 Human Resources 中，选择 **设置**，然后选择 **用户选项**。</span><span class="sxs-lookup"><span data-stu-id="0350b-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="0350b-214">验证 Teams 中的 **语言** 字段是否与 **应用语言** 字段匹配。</span><span class="sxs-lookup"><span data-stu-id="0350b-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources 用户选项](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="0350b-216">如果您仍然遇到翻译问题，请告诉我们。</span><span class="sxs-lookup"><span data-stu-id="0350b-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="0350b-217">有关信息，请参阅[获取对 Finance and Operations 应用或 Lifecycle Services (LCS) 的支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="0350b-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="0350b-218">在 Teams 中的 Human Resources 应用中审批请假请求时出错</span><span class="sxs-lookup"><span data-stu-id="0350b-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="0350b-219">如果您在尝试在 Teams 应用中审核休假请求时收到错误，请尝试以下疑难解答步骤：</span><span class="sxs-lookup"><span data-stu-id="0350b-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="0350b-220">验证您用于登录 Microsoft Teams 的帐户是否与用于访问 Dynamics 365 Human Resources 的帐户相同。</span><span class="sxs-lookup"><span data-stu-id="0350b-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="0350b-221">通过检查请假审批的工作流设置，验证您是否是该请求的有效审批者。</span><span class="sxs-lookup"><span data-stu-id="0350b-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="0350b-222">有关请假请求工作流的详细信息，请参阅[创建请假请求工作流](hr-leave-and-absence-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="0350b-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="0350b-223">休假审批者收不到审批休假申请的 Teams 聊天消息</span><span class="sxs-lookup"><span data-stu-id="0350b-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="0350b-224">请确保为环境和用户启用了通知。</span><span class="sxs-lookup"><span data-stu-id="0350b-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="0350b-225">有关详细信息，请参阅[在 Teams 中启用 Human Resources 应用通知](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)和[为单个用户打开或关闭 Teams 通知](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)。</span><span class="sxs-lookup"><span data-stu-id="0350b-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="0350b-226">确保用户使用与用于审批休假申请相同的凭据登录到 **聊天** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="0350b-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="0350b-227">使用消息“注销”，然后使用“登录”以正确的凭据登录。</span><span class="sxs-lookup"><span data-stu-id="0350b-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="0350b-228">如果问题仍然存在，请以系统管理员身份检查业务事件系统批处理作业的状态。</span><span class="sxs-lookup"><span data-stu-id="0350b-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="0350b-229">如果是处于等待或执行阶段，请过几分钟再次检查。</span><span class="sxs-lookup"><span data-stu-id="0350b-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="0350b-230">如果状态保持不变，请记录支持票证，以便我们的团队可以帮助解决问题。</span><span class="sxs-lookup"><span data-stu-id="0350b-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="0350b-231">已知的可访问性问题</span><span class="sxs-lookup"><span data-stu-id="0350b-231">Known accessibility issues</span></span>

<span data-ttu-id="0350b-232">Teams 中的 Human Resources 应用具有以下可访问性问题，我们正在努力在将来的版本中修复这些问题。</span><span class="sxs-lookup"><span data-stu-id="0350b-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="0350b-233">签发</span><span class="sxs-lookup"><span data-stu-id="0350b-233">Issue</span></span> | <span data-ttu-id="0350b-234">解决方法或说明</span><span class="sxs-lookup"><span data-stu-id="0350b-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="0350b-235">在桌面上放大到 400％ 时，将看不见某些操作按钮。</span><span class="sxs-lookup"><span data-stu-id="0350b-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="0350b-236">建议您改用放大镜，直到我们可以支持此缩放级别为止。</span><span class="sxs-lookup"><span data-stu-id="0350b-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="0350b-237">在 **休假** 选项卡上，在读出休假网格的标题时，VoiceOver 将宣布一个按钮操作。</span><span class="sxs-lookup"><span data-stu-id="0350b-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="0350b-238">网格中的标题和元素按年份分组，并且可以折叠。</span><span class="sxs-lookup"><span data-stu-id="0350b-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="0350b-239">VoiceOver 将此解释为可操作的项目，但并非如此。</span><span class="sxs-lookup"><span data-stu-id="0350b-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="0350b-240">在 **休假** 选项卡上，当在新请求中导航到 **原因代码** 时，有一个额外的轻扫手势。</span><span class="sxs-lookup"><span data-stu-id="0350b-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="0350b-241">没有轻扫导航要尝试获取的隐藏控件。</span><span class="sxs-lookup"><span data-stu-id="0350b-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="0350b-242">在 **休假** 选项卡上，如果您在打开日历时进行轻扫，您最终位于控件之外，而不是在新请求中或编辑请求时位于顶部。</span><span class="sxs-lookup"><span data-stu-id="0350b-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="0350b-243">当您到达 **立即前往** 时，将其视为控件的结束，然后以相反方向轻扫以返回到顶部。</span><span class="sxs-lookup"><span data-stu-id="0350b-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="0350b-244">在 **聊天** 选项卡上，在使用辅助工具或键盘导航的同时输入日期时，焦点会跳回到顶部。</span><span class="sxs-lookup"><span data-stu-id="0350b-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="0350b-245">按 Tab 键，直到再次到达输入区域。</span><span class="sxs-lookup"><span data-stu-id="0350b-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="0350b-246">隐私声明</span><span class="sxs-lookup"><span data-stu-id="0350b-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0350b-247">Microsoft 语言理解智能服务 (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0350b-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0350b-248">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="0350b-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0350b-249">“搜索帐户 Contoso”之类的用户输入将传递到一个名为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="0350b-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0350b-250">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="0350b-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0350b-251">LUIS 服务用于理清或了解用户输入的意图（在此示例中，意图为查找信息）和目标实体（在此示例中，意图实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="0350b-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0350b-252">然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="0350b-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="0350b-253">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="0350b-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0350b-254">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="0350b-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0350b-255">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="0350b-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0350b-256">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="0350b-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0350b-257">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="0350b-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0350b-258">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="0350b-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="0350b-259">Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0350b-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="0350b-260">使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。</span><span class="sxs-lookup"><span data-stu-id="0350b-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="0350b-261">Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="0350b-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0350b-262">此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。</span><span class="sxs-lookup"><span data-stu-id="0350b-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0350b-263">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="0350b-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="0350b-264">与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="0350b-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="0350b-265">此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。</span><span class="sxs-lookup"><span data-stu-id="0350b-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0350b-266">要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="0350b-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="0350b-267">要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="0350b-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="0350b-268">请参阅</span><span class="sxs-lookup"><span data-stu-id="0350b-268">See also</span></span>

[<span data-ttu-id="0350b-269">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0350b-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0350b-270">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="0350b-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0350b-271">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="0350b-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
