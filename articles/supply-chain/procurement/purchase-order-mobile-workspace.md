---
title: 采购订单审核移动工作区
description: 此主题提供有关采购订单审核移动工作区的信息，以便您查看采购订单和通过操作作出响应。 例如，您可以审核或拒绝采购订单。
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b7f5d61ade071e75d53d5036a47fea438d8afbe6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249417"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="0ce06-104">采购订单审核移动工作区</span><span class="sxs-lookup"><span data-stu-id="0ce06-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="0ce06-105">此主题提供有关**采购订单审核**移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="0ce06-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="0ce06-106">此工作区可让您查看采购订单和通过操作作出响应。</span><span class="sxs-lookup"><span data-stu-id="0ce06-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="0ce06-107">例如，您可以审核或拒绝采购订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="0ce06-108">概览</span><span class="sxs-lookup"><span data-stu-id="0ce06-108">Overview</span></span> 
<span data-ttu-id="0ce06-109">要求审核的采购订单通过审核工作流。</span><span class="sxs-lookup"><span data-stu-id="0ce06-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="0ce06-110">工作流可能包括要求一个或多个人员采取操作的不同步骤。</span><span class="sxs-lookup"><span data-stu-id="0ce06-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="0ce06-111">例如，人员可能必须完成任务或审核采购订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="0ce06-112">**采购订单审核**移动工作区能让您轻松地从移动设备查看和响应采购订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="0ce06-113">此工作区还可以让您执行可从客户端执行的相同工作流操作。</span><span class="sxs-lookup"><span data-stu-id="0ce06-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ce06-114">先决条件</span><span class="sxs-lookup"><span data-stu-id="0ce06-114">Prerequisites</span></span>
<span data-ttu-id="0ce06-115">先决条件根据为您的组织部署的 Supply Chain Management 版本不同。</span><span class="sxs-lookup"><span data-stu-id="0ce06-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="0ce06-116">使用 Supply Chain Management 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="0ce06-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="0ce06-117">如果已经为您的组织部署 Finance and Operations，系统管理员必须发布**采购订单审核**移动工作区。</span><span class="sxs-lookup"><span data-stu-id="0ce06-117">If Finance and Operations has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="0ce06-118">有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="0ce06-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="0ce06-119">使用带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="0ce06-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="0ce06-120">如果已经为您的组织部署带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611，系统管理员必须完成以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="0ce06-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ce06-121">必备项</span><span class="sxs-lookup"><span data-stu-id="0ce06-121">Prerequisite</span></span></th>
<th><span data-ttu-id="0ce06-122">角色</span><span class="sxs-lookup"><span data-stu-id="0ce06-122">Role</span></span></th>
<th><span data-ttu-id="0ce06-123">说明</span><span class="sxs-lookup"><span data-stu-id="0ce06-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ce06-124">实现 KB 4017918。</span><span class="sxs-lookup"><span data-stu-id="0ce06-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="0ce06-125">系统管理员</span><span class="sxs-lookup"><span data-stu-id="0ce06-125">System administrator</span></span></td>
<td><span data-ttu-id="0ce06-126">KB 4017918 是包含<strong>采购订单审核</strong>移动工作区的 X++ 更新或元数据修补程序。</span><span class="sxs-lookup"><span data-stu-id="0ce06-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="0ce06-127">若要实施 KB 4017918，系统管理员必须遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="0ce06-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="0ce06-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="0ce06-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="0ce06-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="0ce06-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="0ce06-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="0ce06-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="0ce06-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</span><span class="sxs-lookup"><span data-stu-id="0ce06-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ce06-132">发布<strong>采购订单审核</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="0ce06-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="0ce06-133">系统管理员</span><span class="sxs-lookup"><span data-stu-id="0ce06-133">System administrator</span></span></td>
<td><span data-ttu-id="0ce06-134">请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="0ce06-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="0ce06-135">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="0ce06-135">Download and install the mobile app</span></span>
<span data-ttu-id="0ce06-136">下载并安装 Finance and Operations 移动应用程序：</span><span class="sxs-lookup"><span data-stu-id="0ce06-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="0ce06-137">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="0ce06-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="0ce06-138">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="0ce06-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="0ce06-139">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="0ce06-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="0ce06-140">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="0ce06-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="0ce06-141">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="0ce06-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="0ce06-142">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="0ce06-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="0ce06-143">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="0ce06-143">Enter your credentials.</span></span>
4. <span data-ttu-id="0ce06-144">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="0ce06-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="0ce06-145">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="0ce06-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![可用工作区列表中的采购订单审核工作区](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="0ce06-147">查看分配给您的订单</span><span class="sxs-lookup"><span data-stu-id="0ce06-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="0ce06-148">在移动设备上，选择**采购订单审核**工作区。</span><span class="sxs-lookup"><span data-stu-id="0ce06-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="0ce06-149">选择**分配给我的订单**以查看要求您在采购订单审核工作流中对其执行操作的所有采购订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="0ce06-150">选择订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-150">Select an order.</span></span> <span data-ttu-id="0ce06-151">在**订单明细**页，您将看到订单头信息和行。</span><span class="sxs-lookup"><span data-stu-id="0ce06-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="0ce06-152">还可以从工作流任务查找指南。</span><span class="sxs-lookup"><span data-stu-id="0ce06-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="0ce06-153">选择**会计分配**以打开**标头会计分配**页。</span><span class="sxs-lookup"><span data-stu-id="0ce06-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="0ce06-154">返回到**订单明细**页，然后选择行。</span><span class="sxs-lookup"><span data-stu-id="0ce06-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="0ce06-155">从订单行明细还可以探索特定行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="0ce06-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="0ce06-156">完成对采购订单的操作</span><span class="sxs-lookup"><span data-stu-id="0ce06-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="0ce06-157">在查看分配给您的采购订单和阅读工作流说明后，应准备执行操作。</span><span class="sxs-lookup"><span data-stu-id="0ce06-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="0ce06-158">在移动设备上，选择**采购订单审核**工作区。</span><span class="sxs-lookup"><span data-stu-id="0ce06-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="0ce06-159">选择**分配给我的订单**以查看要求您在采购订单审核工作流中对其执行操作的所有采购订单。</span><span class="sxs-lookup"><span data-stu-id="0ce06-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="0ce06-160">选择一个订单，然后查看详细信息页。</span><span class="sxs-lookup"><span data-stu-id="0ce06-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="0ce06-161">选择**操作**以显示可用操作。</span><span class="sxs-lookup"><span data-stu-id="0ce06-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="0ce06-162">可用操作取决于分配给您的任务。</span><span class="sxs-lookup"><span data-stu-id="0ce06-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="0ce06-163">任务操作</span><span class="sxs-lookup"><span data-stu-id="0ce06-163">Task action</span></span>    | <span data-ttu-id="0ce06-164">审核行为</span><span class="sxs-lookup"><span data-stu-id="0ce06-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="0ce06-165">已完成</span><span class="sxs-lookup"><span data-stu-id="0ce06-165">Complete</span></span>       | <span data-ttu-id="0ce06-166">审核</span><span class="sxs-lookup"><span data-stu-id="0ce06-166">Approve</span></span>          |
    | <span data-ttu-id="0ce06-167">退回</span><span class="sxs-lookup"><span data-stu-id="0ce06-167">Return</span></span>         | <span data-ttu-id="0ce06-168">拒绝</span><span class="sxs-lookup"><span data-stu-id="0ce06-168">Reject</span></span>           |
    | <span data-ttu-id="0ce06-169">请求更改</span><span class="sxs-lookup"><span data-stu-id="0ce06-169">Request change</span></span> | <span data-ttu-id="0ce06-170">请求更改</span><span class="sxs-lookup"><span data-stu-id="0ce06-170">Request change</span></span>   |
    | <span data-ttu-id="0ce06-171">委托人</span><span class="sxs-lookup"><span data-stu-id="0ce06-171">Delegate</span></span>       | <span data-ttu-id="0ce06-172">委托人</span><span class="sxs-lookup"><span data-stu-id="0ce06-172">Delegate</span></span>         |

5. <span data-ttu-id="0ce06-173">选择相应的操作。</span><span class="sxs-lookup"><span data-stu-id="0ce06-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="0ce06-174">在**完成任务**页输入注释。</span><span class="sxs-lookup"><span data-stu-id="0ce06-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="0ce06-175">请注意，如果选择**委托**操作，必须选择要委托任务的用户。</span><span class="sxs-lookup"><span data-stu-id="0ce06-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="0ce06-176">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="0ce06-176">Select **Done**.</span></span> <span data-ttu-id="0ce06-177">刷新您的工作区后，采购订单不再显示在列表中。</span><span class="sxs-lookup"><span data-stu-id="0ce06-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
