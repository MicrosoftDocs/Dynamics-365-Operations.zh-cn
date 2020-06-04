---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393000"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="721d2-103">在 Teams 中管理请假</span><span class="sxs-lookup"><span data-stu-id="721d2-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="721d2-104">可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="721d2-105">可以与机器人交互以请求信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="721d2-106">**休假**选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="721d2-107">安装应用</span><span class="sxs-lookup"><span data-stu-id="721d2-107">Install the app</span></span>

<span data-ttu-id="721d2-108">可以在 Teams 商店中找到 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="721d2-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="721d2-109">在 Microsoft Teams 中，选择省略号。</span><span class="sxs-lookup"><span data-stu-id="721d2-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teams 休假应用省略号](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="721d2-111">搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="721d2-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teams 休假应用 HR 磁贴](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="721d2-113">选择**添加**按钮安装应用。</span><span class="sxs-lookup"><span data-stu-id="721d2-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teams 休假应用安装](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="721d2-115">如果应用不让您自动登录，请选择**设置**选项卡登录。</span><span class="sxs-lookup"><span data-stu-id="721d2-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teams 休假应用“设置”选项卡](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="721d2-117">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="721d2-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="721d2-118">如果可以访问多个 Human Resources 实例，可以在**设置**选项卡中选择要连接哪个环境。</span><span class="sxs-lookup"><span data-stu-id="721d2-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="721d2-119">此应用现在支持系统管理员安全角色，并且在您使用系统管理员帐户时显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="721d2-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="721d2-120">若要使用其他帐户登录，请在**设置**选项卡上选择**切换帐户**按钮，然后使用无系统管理员权限的用户帐户登录。</span><span class="sxs-lookup"><span data-stu-id="721d2-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="721d2-121">使用机器人</span><span class="sxs-lookup"><span data-stu-id="721d2-121">Use the bot</span></span>

<span data-ttu-id="721d2-122">安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。</span><span class="sxs-lookup"><span data-stu-id="721d2-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams 休假应用机器人欢迎消息](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="721d2-124">首次与机器人交互时，可能需要登录。</span><span class="sxs-lookup"><span data-stu-id="721d2-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="721d2-125">如果未看到登录对话框，请检查浏览器设置允许弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="721d2-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="721d2-126">可以让机器人：</span><span class="sxs-lookup"><span data-stu-id="721d2-126">You can ask the bot to:</span></span>

- <span data-ttu-id="721d2-127">显示您等记的每个休假类型的休假余额信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teams 休假应用显示余额](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="721d2-129">显示有关特定休假类型的其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teams 休假应用显示详细信息](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="721d2-131">为您启动休假请求。</span><span class="sxs-lookup"><span data-stu-id="721d2-131">Start a leave request for you.</span></span>

   ![Human Resources Teams 休假应用请假](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="721d2-133">启动请假后，可以直接在卡中调整天数，也可以选择**编辑详细信息**向请求添加更多信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Human Resources Teams 休假应用编辑请求](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="721d2-135">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="721d2-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="721d2-136">也可以键入**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="721d2-136">You can also type **Save as draft** to come back to it later.</span></span>

![Human Resources Teams 休假应用提交请求](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="721d2-138">在 Teams 中管理休假</span><span class="sxs-lookup"><span data-stu-id="721d2-138">Manage your leave in Teams</span></span>

<span data-ttu-id="721d2-139">**休假**选项卡可用于查看：</span><span class="sxs-lookup"><span data-stu-id="721d2-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="721d2-140">您等记的每个休假类型的余额信息</span><span class="sxs-lookup"><span data-stu-id="721d2-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="721d2-141">近期请假</span><span class="sxs-lookup"><span data-stu-id="721d2-141">Upcoming leave requests</span></span>

- <span data-ttu-id="721d2-142">休假请求</span><span class="sxs-lookup"><span data-stu-id="721d2-142">Time-off requests</span></span>

- <span data-ttu-id="721d2-143">草稿请假</span><span class="sxs-lookup"><span data-stu-id="721d2-143">Draft leave requests</span></span>

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="721d2-145">创建新请求</span><span class="sxs-lookup"><span data-stu-id="721d2-145">Create a new request</span></span>

1. <span data-ttu-id="721d2-146">若要创建新休假请求，请选择**新请求**。</span><span class="sxs-lookup"><span data-stu-id="721d2-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teams 休假应用新请求](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="721d2-148">输入请假天数，然后选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="721d2-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teams 休假应用添加休假](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="721d2-150">如果适用，输入原因代码。</span><span class="sxs-lookup"><span data-stu-id="721d2-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="721d2-151">并且输入任何注释和添加任何附件。</span><span class="sxs-lookup"><span data-stu-id="721d2-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="721d2-152">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="721d2-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="721d2-153">也可以键入**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="721d2-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="721d2-154">管理草稿请求</span><span class="sxs-lookup"><span data-stu-id="721d2-154">Manage draft requests</span></span>

1. <span data-ttu-id="721d2-155">选择**草稿**选项卡。</span><span class="sxs-lookup"><span data-stu-id="721d2-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teams 休假应用“草稿”选项卡](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="721d2-157">选择铅笔编辑请求，或选择废纸篓删除请求。</span><span class="sxs-lookup"><span data-stu-id="721d2-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="721d2-158">进行任何必要更改。</span><span class="sxs-lookup"><span data-stu-id="721d2-158">Make any necessary changes.</span></span> <span data-ttu-id="721d2-159">输入完信息后，键入**提交**提交请求供批准。</span><span class="sxs-lookup"><span data-stu-id="721d2-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="721d2-160">也可以选择**另存为草稿**以后再回来。</span><span class="sxs-lookup"><span data-stu-id="721d2-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teams 休假应用编辑草稿](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="721d2-162">隐私声明</span><span class="sxs-lookup"><span data-stu-id="721d2-162">Privacy notice</span></span>

<span data-ttu-id="721d2-163">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="721d2-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="721d2-164">“搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="721d2-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="721d2-165">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="721d2-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="721d2-166">LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="721d2-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="721d2-167">然后将此信息继续传递到 Microsoft 的  [Azure 机器人框架](https://azure.microsoft.com/services/bot-service/) 后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="721d2-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="721d2-168">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="721d2-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="721d2-169">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="721d2-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="721d2-170">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="721d2-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="721d2-171">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="721d2-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="721d2-172">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="721d2-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="721d2-173">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="721d2-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="721d2-174">请参阅</span><span class="sxs-lookup"><span data-stu-id="721d2-174">See also</span></span>

[<span data-ttu-id="721d2-175">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="721d2-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="721d2-176">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="721d2-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="721d2-177">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="721d2-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
