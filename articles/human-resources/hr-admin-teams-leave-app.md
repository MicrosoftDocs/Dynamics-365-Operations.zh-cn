---
title: Teams 中的 Human Resources 应用
description: 此主题介绍 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用。
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
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388108"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="2246d-103">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="2246d-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2246d-104">员工可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用在 Microsoft Teams 中快速请假和查看自己的请假余额信息。</span><span class="sxs-lookup"><span data-stu-id="2246d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="2246d-105">员工可以与机器人交互以请求信息。</span><span class="sxs-lookup"><span data-stu-id="2246d-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="2246d-106">**休假**选项卡提供更详细信息。</span><span class="sxs-lookup"><span data-stu-id="2246d-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teams 休假应用机器人](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="2246d-109">安装和设置</span><span class="sxs-lookup"><span data-stu-id="2246d-109">Install and setup</span></span>

<span data-ttu-id="2246d-110">可以在 Teams 商店中找到 Human Resources 应用。</span><span class="sxs-lookup"><span data-stu-id="2246d-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="2246d-111">有关安装 Teams 应用的信息，请参阅[在 Teams 中管理请假](hr-teams-leave-app.md)。</span><span class="sxs-lookup"><span data-stu-id="2246d-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="2246d-112">有关在 Teams 中管理应用权限的信息，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。</span><span class="sxs-lookup"><span data-stu-id="2246d-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2246d-113">已知问题</span><span class="sxs-lookup"><span data-stu-id="2246d-113">Known issues</span></span>

| <span data-ttu-id="2246d-114">发货</span><span class="sxs-lookup"><span data-stu-id="2246d-114">Issue</span></span> | <span data-ttu-id="2246d-115">状态</span><span class="sxs-lookup"><span data-stu-id="2246d-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="2246d-116">提交将来日期的请假时，余额不正确。</span><span class="sxs-lookup"><span data-stu-id="2246d-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="2246d-117">预测尚不可用。</span><span class="sxs-lookup"><span data-stu-id="2246d-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="2246d-118">显示当前日期的余额。</span><span class="sxs-lookup"><span data-stu-id="2246d-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="2246d-119">减少现有请求所用小时数时，**余额**变小而不是变大。</span><span class="sxs-lookup"><span data-stu-id="2246d-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="2246d-120">我们将在以后解决这个已知问题。</span><span class="sxs-lookup"><span data-stu-id="2246d-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="2246d-121">显示不正确，但是提交后会调整正确金额。</span><span class="sxs-lookup"><span data-stu-id="2246d-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="2246d-122">为相同日期显示两个**近期请假**卡。</span><span class="sxs-lookup"><span data-stu-id="2246d-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="2246d-123">这些卡显示各项提交。</span><span class="sxs-lookup"><span data-stu-id="2246d-123">The cards represent individual submissions.</span></span> <span data-ttu-id="2246d-124">我们将继续征集反馈并进行调整。</span><span class="sxs-lookup"><span data-stu-id="2246d-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="2246d-125">不能取消**审查中**请求。</span><span class="sxs-lookup"><span data-stu-id="2246d-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="2246d-126">现在不支持此功能，将来的版本中将增加此功能。</span><span class="sxs-lookup"><span data-stu-id="2246d-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="2246d-127">将计算截止当天的余额信息。</span><span class="sxs-lookup"><span data-stu-id="2246d-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="2246d-128">系统现在不显示截止实际期间的余额，即使已在“休假和缺勤”参数中配置。</span><span class="sxs-lookup"><span data-stu-id="2246d-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2246d-129">隐私声明</span><span class="sxs-lookup"><span data-stu-id="2246d-129">Privacy notice</span></span>

<span data-ttu-id="2246d-130">Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。</span><span class="sxs-lookup"><span data-stu-id="2246d-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2246d-131">“搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。</span><span class="sxs-lookup"><span data-stu-id="2246d-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2246d-132">请在 [此处](https://www.luis.ai/)详细了解 LUIS。</span><span class="sxs-lookup"><span data-stu-id="2246d-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2246d-133">LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。</span><span class="sxs-lookup"><span data-stu-id="2246d-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2246d-134">然后将此信息继续传递到 Microsoft 的  [Azure 机器人框架](https://azure.microsoft.com/services/bot-service/) 后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。</span><span class="sxs-lookup"><span data-stu-id="2246d-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2246d-135">安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。</span><span class="sxs-lookup"><span data-stu-id="2246d-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2246d-136">与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。</span><span class="sxs-lookup"><span data-stu-id="2246d-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2246d-137">由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。</span><span class="sxs-lookup"><span data-stu-id="2246d-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2246d-138">用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。</span><span class="sxs-lookup"><span data-stu-id="2246d-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2246d-139">请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。</span><span class="sxs-lookup"><span data-stu-id="2246d-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2246d-140">若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="2246d-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="2246d-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="2246d-141">See also</span></span> 

[<span data-ttu-id="2246d-142">下载和安装 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2246d-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2246d-143">Microsoft Teams 帮助中心</span><span class="sxs-lookup"><span data-stu-id="2246d-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2246d-144">在 Teams 中管理请假</span><span class="sxs-lookup"><span data-stu-id="2246d-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

