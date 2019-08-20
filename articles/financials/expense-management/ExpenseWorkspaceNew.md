---
title: 已重构的费用报表
description: 本主题介绍 Microsoft Dynamics 365 for Finance and Operations 中经过重新设计和重构的费用报表录入体验。 新体验简化了填写费用报表的流程，并缩短了所需时间。
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 320984fc6be231c941df17abb7246e92f6aa4b9a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841049"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="753c4-104">已重构的费用报表</span><span class="sxs-lookup"><span data-stu-id="753c4-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="753c4-105">重新设计了费用报表录入，以便简化填写费用报表的流程和缩短所需时间。</span><span class="sxs-lookup"><span data-stu-id="753c4-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="753c4-106">下面是新费用体验的主要组件：</span><span class="sxs-lookup"><span data-stu-id="753c4-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="753c4-107">新的费用管理工作区，用于访问委托人的费用。</span><span class="sxs-lookup"><span data-stu-id="753c4-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="753c4-108">新的收据匹配体验，用于更好地显示抬头级收据和简化将收据附加到费用行的流程。</span><span class="sxs-lookup"><span data-stu-id="753c4-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="753c4-109">新的只读网格，用于查看更多费用行和更多数据列。</span><span class="sxs-lookup"><span data-stu-id="753c4-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="753c4-110">现在可以查看所有明细化行和拆分行，及其父费用。</span><span class="sxs-lookup"><span data-stu-id="753c4-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="753c4-111">经过简化的费用编辑窗格。</span><span class="sxs-lookup"><span data-stu-id="753c4-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="753c4-112">错误、警告和策略消息已经过重新设计，可以帮助确保为您提供正确的上下文来了解问题及其解决方法。</span><span class="sxs-lookup"><span data-stu-id="753c4-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="753c4-113">Microsoft 已删除了用户有机会完成任务之前显示的大量消息，并解决了明细化消息之类问题。</span><span class="sxs-lookup"><span data-stu-id="753c4-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="753c4-114">一个新页面，用于指定哪些字段是组织必需的，哪些字段可选和哪些字段不应捕获。</span><span class="sxs-lookup"><span data-stu-id="753c4-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="753c4-115">此页面将减少用户必须设置的字段数量。</span><span class="sxs-lookup"><span data-stu-id="753c4-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="753c4-116">新的费用报表外观，这样此类报表外观不再像为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="753c4-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="753c4-117">若要开启新体验，请使用**功能管理**工作区开启**已重构的费用报表**功能。</span><span class="sxs-lookup"><span data-stu-id="753c4-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="753c4-118">开启此功能时，将执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="753c4-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="753c4-119">现有费用工作区替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="753c4-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="753c4-120">为费用字段可见性添加一个新菜单项。</span><span class="sxs-lookup"><span data-stu-id="753c4-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="753c4-121">不删除费用报表（现有页面）和费用报表字段的任何现有菜单项。</span><span class="sxs-lookup"><span data-stu-id="753c4-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="753c4-122">工作流和所有审核仍然会将您带到现有费用报表页。</span><span class="sxs-lookup"><span data-stu-id="753c4-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="753c4-123">面向新用户的入门视频</span><span class="sxs-lookup"><span data-stu-id="753c4-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="753c4-124">YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含 [Dynamics 365 for Finance and Operations 中的费用体验](https://youtu.be/Ocy-MsTvEE0)视频（上面显示的）。</span><span class="sxs-lookup"><span data-stu-id="753c4-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="753c4-125">新功能</span><span class="sxs-lookup"><span data-stu-id="753c4-125">New features</span></span>

| <span data-ttu-id="753c4-126">新功能</span><span class="sxs-lookup"><span data-stu-id="753c4-126">New feature</span></span> | <span data-ttu-id="753c4-127">说明</span><span class="sxs-lookup"><span data-stu-id="753c4-127">Description</span></span> |
|---|----|
| <span data-ttu-id="753c4-128">费用字段可见性</span><span class="sxs-lookup"><span data-stu-id="753c4-128">Expense field visibility</span></span> | <span data-ttu-id="753c4-129">可通过一个新的设置页面指定应对组织禁用哪些字段，哪些字段应该为必填字段，以及哪些字段为推荐字段。</span><span class="sxs-lookup"><span data-stu-id="753c4-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="753c4-130">必填字段</span><span class="sxs-lookup"><span data-stu-id="753c4-130">Required fields</span></span> | <span data-ttu-id="753c4-131">新的简单配置让您不必使用策略框架即可将某些字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="753c4-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="753c4-132">可选字段</span><span class="sxs-lookup"><span data-stu-id="753c4-132">Optional fields</span></span> | <span data-ttu-id="753c4-133">为可选字段增加了第二页面。</span><span class="sxs-lookup"><span data-stu-id="753c4-133">A second page for optional fields is added.</span></span> <span data-ttu-id="753c4-134">这样员工不会觉得必须设置字段，但是字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="753c4-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="753c4-135">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="753c4-135">Add unattached receipts</span></span> | <span data-ttu-id="753c4-136">更容易在工作区和费用报表中查看向费用报表添加未附加的收据这一功能。</span><span class="sxs-lookup"><span data-stu-id="753c4-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="753c4-137">改进了消息</span><span class="sxs-lookup"><span data-stu-id="753c4-137">Improved messaging</span></span> | <span data-ttu-id="753c4-138">更容易查看具有警告或错误的费用行。</span><span class="sxs-lookup"><span data-stu-id="753c4-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="753c4-139">消息栏中减少了消息数量</span><span class="sxs-lookup"><span data-stu-id="753c4-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="753c4-140">减少了信息日志消息的数量，进行了防止许多情况下显示重复消息的工作。</span><span class="sxs-lookup"><span data-stu-id="753c4-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="753c4-141">常用操作分组</span><span class="sxs-lookup"><span data-stu-id="753c4-141">Grouped together common actions</span></span> | <span data-ttu-id="753c4-142">对界面进行了清理，新增了针对大多数行级常用操作的操作按钮，以及针对抬头操作和其他不太常用操作的省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="753c4-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="753c4-143">新增了用于提高可见性的工作区</span><span class="sxs-lookup"><span data-stu-id="753c4-143">New workspace to increase visibility</span></span> | <span data-ttu-id="753c4-144">新的工作区统一了用户用于转到其他区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="753c4-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="753c4-145">创建费用期间添加现有费用和收据</span><span class="sxs-lookup"><span data-stu-id="753c4-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="753c4-146">创建费用报表时，可添加所有或所选费用和收据。</span><span class="sxs-lookup"><span data-stu-id="753c4-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="753c4-147">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="753c4-147">Exchange rate calculator</span></span> | <span data-ttu-id="753c4-148">增加了汇率计算器，用于计算多币种付现交易记录的汇率。</span><span class="sxs-lookup"><span data-stu-id="753c4-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="753c4-149">保存和新增费用行</span><span class="sxs-lookup"><span data-stu-id="753c4-149">Save and add new expense lines</span></span> | <span data-ttu-id="753c4-150">输入新费用时可使用**保存**和**新建**按钮来帮助您快速输入费用行。</span><span class="sxs-lookup"><span data-stu-id="753c4-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="753c4-151">更容易查看拆分行和明细化行</span><span class="sxs-lookup"><span data-stu-id="753c4-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="753c4-152">明细化行和拆分行直接添加到费用列表，从而可以提高可见性和帮助您轻松确定是否发生了策略错误或其他错误。</span><span class="sxs-lookup"><span data-stu-id="753c4-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="753c4-153">明细化期间显示收据</span><span class="sxs-lookup"><span data-stu-id="753c4-153">Show receipts during itemization</span></span> | <span data-ttu-id="753c4-154">可以在明细化期间显示收据。</span><span class="sxs-lookup"><span data-stu-id="753c4-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="753c4-155">初始版本重点关注费用录入方案。</span><span class="sxs-lookup"><span data-stu-id="753c4-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="753c4-156">所有费用报表检查或审核方案都将继续使用现有费用录入页。</span><span class="sxs-lookup"><span data-stu-id="753c4-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="753c4-157">现有页面中有下列功能，但新页面中还没有。</span><span class="sxs-lookup"><span data-stu-id="753c4-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="753c4-158">接下来的一些版本中将重新引入这些功能：</span><span class="sxs-lookup"><span data-stu-id="753c4-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="753c4-159">审核</span><span class="sxs-lookup"><span data-stu-id="753c4-159">Approvals</span></span>
- <span data-ttu-id="753c4-160">应付帐款审核和会计编辑功能</span><span class="sxs-lookup"><span data-stu-id="753c4-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="753c4-161">多个入口点</span><span class="sxs-lookup"><span data-stu-id="753c4-161">Multiple entry points</span></span>
- <span data-ttu-id="753c4-162">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="753c4-162">Travel requisition integration</span></span>
- <span data-ttu-id="753c4-163">费用的数据实体字段可见性</span><span class="sxs-lookup"><span data-stu-id="753c4-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="753c4-164">出差津贴的录入</span><span class="sxs-lookup"><span data-stu-id="753c4-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="753c4-165">行级别工作流</span><span class="sxs-lookup"><span data-stu-id="753c4-165">Line-level workflow</span></span>
- <span data-ttu-id="753c4-166">临时审核人支持</span><span class="sxs-lookup"><span data-stu-id="753c4-166">Interim approver support</span></span>
- <span data-ttu-id="753c4-167">高级明细</span><span class="sxs-lookup"><span data-stu-id="753c4-167">Advanced itemization</span></span>
