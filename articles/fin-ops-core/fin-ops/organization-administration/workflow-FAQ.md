---
title: 工作流常见问题
description: 本主题解答有关工作流系统的常见问题。
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772689"
---
# <a name="workflow-faq"></a><span data-ttu-id="28a98-103">工作流常见问题</span><span class="sxs-lookup"><span data-stu-id="28a98-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28a98-104">本主题解答有关工作流系统的常见问题。</span><span class="sxs-lookup"><span data-stu-id="28a98-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="28a98-105">为什么在拒绝一个工作项后会收到多个通知？</span><span class="sxs-lookup"><span data-stu-id="28a98-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="28a98-106">如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。</span><span class="sxs-lookup"><span data-stu-id="28a98-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="28a98-107">将再创建一个工作项，并将其分配给发起方。</span><span class="sxs-lookup"><span data-stu-id="28a98-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="28a98-108">这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。</span><span class="sxs-lookup"><span data-stu-id="28a98-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="28a98-109">每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。</span><span class="sxs-lookup"><span data-stu-id="28a98-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="28a98-110">我们在想办法在将来的版本中改进这个问题。</span><span class="sxs-lookup"><span data-stu-id="28a98-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="28a98-111">我在导出工作流时为什么失败了？</span><span class="sxs-lookup"><span data-stu-id="28a98-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="28a98-112">这是现有工作流导出功能的一项限制，它会阻止超过 48 个字符的工作流名称。</span><span class="sxs-lookup"><span data-stu-id="28a98-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="28a98-113">使用超过 48 个字符的名称可能会导致“服务器未能对请求进行身份验证”错误，以及/或者阻止导出无文件类型的文件。</span><span class="sxs-lookup"><span data-stu-id="28a98-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="28a98-114">以下博客文章提供了有关[工作流导出疑难解答](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="28a98-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="28a98-115">工作流的提交者是否也可以审核工作流？</span><span class="sxs-lookup"><span data-stu-id="28a98-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="28a98-116">可以。如果按照这种方式配置，工作流的提交者也可以审核工作流。</span><span class="sxs-lookup"><span data-stu-id="28a98-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="28a98-117">若要避免此行为，请将**工作流参数 > 常规 > 审核人 > 不允许提交者进行审核**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="28a98-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="28a98-118">是否可向工作流添加预警以向用户提供通知？</span><span class="sxs-lookup"><span data-stu-id="28a98-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="28a98-119">下面是向工作流添加预警以提供通知时需要注意的一些关键方面：</span><span class="sxs-lookup"><span data-stu-id="28a98-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="28a98-120">预警与工作流通知机制</span><span class="sxs-lookup"><span data-stu-id="28a98-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="28a98-121">可以为录制更改设置预警。</span><span class="sxs-lookup"><span data-stu-id="28a98-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="28a98-122">工作流将更改录制，这样就可以设置与工作流导致的录制更改有关的预警。</span><span class="sxs-lookup"><span data-stu-id="28a98-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="28a98-123">但是，因为工作流具有不同的内置通知选项，所以使用预警的效果不理想。</span><span class="sxs-lookup"><span data-stu-id="28a98-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="28a98-124">来自工作流的标准通知</span><span class="sxs-lookup"><span data-stu-id="28a98-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="28a98-125">工作流有内置电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="28a98-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="28a98-126">客户可以配置通知，以便向用户发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="28a98-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="28a98-127">这些通知不会为用户生成操作中心消息。</span><span class="sxs-lookup"><span data-stu-id="28a98-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="28a98-128">将来的更新中，将添加操作中心消息，以便为用户分配工作流工作项。</span><span class="sxs-lookup"><span data-stu-id="28a98-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="28a98-129">向工作流添加通知</span><span class="sxs-lookup"><span data-stu-id="28a98-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="28a98-130">可以为特定用户创建操作中心消息，如使用 X++ 从工作流创建的消息。</span><span class="sxs-lookup"><span data-stu-id="28a98-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="28a98-131">[工作流具有业务事件](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)，可供客户用于触发具有客户在寻找的通知的流。</span><span class="sxs-lookup"><span data-stu-id="28a98-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="28a98-132">总之，如果在为用户分配工作流工作项时，该用户未收到来自操作中心的正确通知，请利用[工作流业务事件](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)和 Microsoft Power Automate 提供更多通知或不同通知。</span><span class="sxs-lookup"><span data-stu-id="28a98-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>
