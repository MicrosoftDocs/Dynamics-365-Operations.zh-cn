---
title: 已重构的费用报表
description: 本主题介绍 Microsoft Dynamics 365 for Finance and Operations 中经过重新设计和重构的费用报表录入体验。 新体验简化了填写费用报表的流程，并缩短了所需时间。
author: ryansandness
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 3039cda3f2cf9259ca06207bdf941bc6b0fb28e1
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538674"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="fa11f-104">已重构的费用报表</span><span class="sxs-lookup"><span data-stu-id="fa11f-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fa11f-105">重新设计了费用报表录入，以便简化填写费用报表的流程和缩短所需时间。</span><span class="sxs-lookup"><span data-stu-id="fa11f-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="fa11f-106">下面是新费用体验的主要组件：</span><span class="sxs-lookup"><span data-stu-id="fa11f-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="fa11f-107">新的费用管理工作区，用于访问委托人的费用。</span><span class="sxs-lookup"><span data-stu-id="fa11f-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="fa11f-108">新的收据匹配体验，用于更好地显示抬头级收据和简化将收据附加到费用行的流程。</span><span class="sxs-lookup"><span data-stu-id="fa11f-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="fa11f-109">新的只读网格，用于查看更多费用行和更多数据列。</span><span class="sxs-lookup"><span data-stu-id="fa11f-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="fa11f-110">现在可以查看所有明细化行和拆分行，及其父费用。</span><span class="sxs-lookup"><span data-stu-id="fa11f-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="fa11f-111">经过简化的费用编辑窗格。</span><span class="sxs-lookup"><span data-stu-id="fa11f-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="fa11f-112">错误、警告和策略消息已经过重新设计，可以帮助确保为您提供正确的上下文来了解问题及其解决方法。</span><span class="sxs-lookup"><span data-stu-id="fa11f-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="fa11f-113">Microsoft 已删除了用户有机会完成任务之前显示的大量消息，并解决了明细化消息之类问题。</span><span class="sxs-lookup"><span data-stu-id="fa11f-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="fa11f-114">一个新页面，用于指定哪些字段是组织必需的，哪些字段可选和哪些字段不应捕获。</span><span class="sxs-lookup"><span data-stu-id="fa11f-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="fa11f-115">此页面将减少用户必须设置的字段数量。</span><span class="sxs-lookup"><span data-stu-id="fa11f-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="fa11f-116">新的费用报表外观，这样此类报表外观不再像为会计人员设计的。</span><span class="sxs-lookup"><span data-stu-id="fa11f-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="fa11f-117">若要开启新体验，请使用**功能管理**工作区开启**已重构的费用报表**功能。</span><span class="sxs-lookup"><span data-stu-id="fa11f-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="fa11f-118">开启此功能时，将执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="fa11f-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="fa11f-119">现有费用工作区替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="fa11f-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="fa11f-120">为费用字段可见性添加一个新菜单项。</span><span class="sxs-lookup"><span data-stu-id="fa11f-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="fa11f-121">不删除费用报表（现有页面）和费用报表字段的任何现有菜单项。</span><span class="sxs-lookup"><span data-stu-id="fa11f-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="fa11f-122">工作流和所有审核仍然会将您带到现有费用报表页。</span><span class="sxs-lookup"><span data-stu-id="fa11f-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="fa11f-123">面向新用户的入门视频</span><span class="sxs-lookup"><span data-stu-id="fa11f-123">Getting started video for new users</span></span>

<span data-ttu-id="fa11f-124">可观看一个短视频，该视频演示主要的费用录入功能。</span><span class="sxs-lookup"><span data-stu-id="fa11f-124">You can watch a short video that shows the main features of expense entry.</span></span>

> [!NOTE]
> <span data-ttu-id="fa11f-125">此视频尚未推出。</span><span class="sxs-lookup"><span data-stu-id="fa11f-125">The video isn't available yet.</span></span> <span data-ttu-id="fa11f-126">该视频推出后，将更新本主题。</span><span class="sxs-lookup"><span data-stu-id="fa11f-126">This topic will be updated when the video is available.</span></span>

## <a name="new-features"></a><span data-ttu-id="fa11f-127">新功能</span><span class="sxs-lookup"><span data-stu-id="fa11f-127">New features</span></span>

| <span data-ttu-id="fa11f-128">新功能</span><span class="sxs-lookup"><span data-stu-id="fa11f-128">New feature</span></span> | <span data-ttu-id="fa11f-129">说明</span><span class="sxs-lookup"><span data-stu-id="fa11f-129">Description</span></span> |
|---|----|
| <span data-ttu-id="fa11f-130">费用字段可见性</span><span class="sxs-lookup"><span data-stu-id="fa11f-130">Expense field visibility</span></span> | <span data-ttu-id="fa11f-131">可通过一个新的设置页面指定应对组织禁用哪些字段，哪些字段应该为必填字段，以及哪些字段为推荐字段。</span><span class="sxs-lookup"><span data-stu-id="fa11f-131">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="fa11f-132">必填字段</span><span class="sxs-lookup"><span data-stu-id="fa11f-132">Required fields</span></span> | <span data-ttu-id="fa11f-133">新的简单配置让您不必使用策略框架即可将某些字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="fa11f-133">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="fa11f-134">可选字段</span><span class="sxs-lookup"><span data-stu-id="fa11f-134">Optional fields</span></span> | <span data-ttu-id="fa11f-135">为可选字段增加了第二页面。</span><span class="sxs-lookup"><span data-stu-id="fa11f-135">A second page for optional fields is added.</span></span> <span data-ttu-id="fa11f-136">这样员工不会觉得必须设置字段，但是字段仍然可以轻松访问。</span><span class="sxs-lookup"><span data-stu-id="fa11f-136">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="fa11f-137">添加未附加的收据</span><span class="sxs-lookup"><span data-stu-id="fa11f-137">Add unattached receipts</span></span> | <span data-ttu-id="fa11f-138">更容易在工作区和费用报表中查看向费用报表添加未附加的收据这一功能。</span><span class="sxs-lookup"><span data-stu-id="fa11f-138">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="fa11f-139">改进了消息</span><span class="sxs-lookup"><span data-stu-id="fa11f-139">Improved messaging</span></span> | <span data-ttu-id="fa11f-140">更容易查看具有警告或错误的费用行。</span><span class="sxs-lookup"><span data-stu-id="fa11f-140">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="fa11f-141">消息栏中减少了消息数量</span><span class="sxs-lookup"><span data-stu-id="fa11f-141">Reduction in messages in the message bar</span></span>| <span data-ttu-id="fa11f-142">减少了信息日志消息的数量，进行了防止许多情况下显示重复消息的工作。</span><span class="sxs-lookup"><span data-stu-id="fa11f-142">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="fa11f-143">常用操作分组</span><span class="sxs-lookup"><span data-stu-id="fa11f-143">Grouped together common actions</span></span> | <span data-ttu-id="fa11f-144">对界面进行了清理，新增了针对大多数行级常用操作的操作按钮，以及针对抬头操作和其他不太常用操作的省略号按钮 (...)。</span><span class="sxs-lookup"><span data-stu-id="fa11f-144">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="fa11f-145">新增了用于提高可见性的工作区</span><span class="sxs-lookup"><span data-stu-id="fa11f-145">New workspace to increase visibility</span></span> | <span data-ttu-id="fa11f-146">新的工作区统一了用户用于转到其他区域的功能和链接。</span><span class="sxs-lookup"><span data-stu-id="fa11f-146">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="fa11f-147">创建费用期间添加现有费用和收据</span><span class="sxs-lookup"><span data-stu-id="fa11f-147">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="fa11f-148">创建费用报表时，可添加所有或所选费用和收据。</span><span class="sxs-lookup"><span data-stu-id="fa11f-148">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="fa11f-149">汇率计算器</span><span class="sxs-lookup"><span data-stu-id="fa11f-149">Exchange rate calculator</span></span> | <span data-ttu-id="fa11f-150">增加了汇率计算器，用于计算多币种付现交易记录的汇率。</span><span class="sxs-lookup"><span data-stu-id="fa11f-150">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="fa11f-151">保存和新增费用行</span><span class="sxs-lookup"><span data-stu-id="fa11f-151">Save and add new expense lines</span></span> | <span data-ttu-id="fa11f-152">输入新费用时可使用**保存**和**新建**按钮来帮助您快速输入费用行。</span><span class="sxs-lookup"><span data-stu-id="fa11f-152">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="fa11f-153">更容易查看拆分行和明细化行</span><span class="sxs-lookup"><span data-stu-id="fa11f-153">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="fa11f-154">明细化行和拆分行直接添加到费用列表，从而可以提高可见性和帮助您轻松确定是否发生了策略错误或其他错误。</span><span class="sxs-lookup"><span data-stu-id="fa11f-154">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="fa11f-155">明细化期间显示收据</span><span class="sxs-lookup"><span data-stu-id="fa11f-155">Show receipts during itemization</span></span> | <span data-ttu-id="fa11f-156">可以在明细化期间显示收据。</span><span class="sxs-lookup"><span data-stu-id="fa11f-156">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="fa11f-157">初始版本重点关注费用录入方案。</span><span class="sxs-lookup"><span data-stu-id="fa11f-157">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="fa11f-158">所有费用报表检查或审核方案都将继续使用现有费用录入页。</span><span class="sxs-lookup"><span data-stu-id="fa11f-158">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="fa11f-159">现有页面中有下列功能，但新页面中还没有。</span><span class="sxs-lookup"><span data-stu-id="fa11f-159">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="fa11f-160">接下来的一些版本中将重新引入这些功能：</span><span class="sxs-lookup"><span data-stu-id="fa11f-160">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="fa11f-161">审核</span><span class="sxs-lookup"><span data-stu-id="fa11f-161">Approvals</span></span>
- <span data-ttu-id="fa11f-162">应付帐款审核和会计编辑功能</span><span class="sxs-lookup"><span data-stu-id="fa11f-162">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="fa11f-163">多个入口点</span><span class="sxs-lookup"><span data-stu-id="fa11f-163">Multiple entry points</span></span>
- <span data-ttu-id="fa11f-164">出差申请集成</span><span class="sxs-lookup"><span data-stu-id="fa11f-164">Travel requisition integration</span></span>
- <span data-ttu-id="fa11f-165">费用的数据实体字段可见性</span><span class="sxs-lookup"><span data-stu-id="fa11f-165">Data entity for expense field visibility</span></span>
- <span data-ttu-id="fa11f-166">出差津贴的录入</span><span class="sxs-lookup"><span data-stu-id="fa11f-166">Entry for per-diem expenses</span></span>
- <span data-ttu-id="fa11f-167">行级别工作流</span><span class="sxs-lookup"><span data-stu-id="fa11f-167">Line-level workflow</span></span>
- <span data-ttu-id="fa11f-168">临时审核人支持</span><span class="sxs-lookup"><span data-stu-id="fa11f-168">Interim approver support</span></span>
- <span data-ttu-id="fa11f-169">高级明细</span><span class="sxs-lookup"><span data-stu-id="fa11f-169">Advanced itemization</span></span>
