---
title: "移动应用主页"
description: "此主题描述 Microsoft Dynamics 365 for Unified Operations 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。"
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 25aad52e2640b671a1c30e42a59516293a2f98e1
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="9b944-103">移动应用主页</span><span class="sxs-lookup"><span data-stu-id="9b944-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9b944-104">此主题描述 Microsoft Dynamics 365 for Unified Operations 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。</span><span class="sxs-lookup"><span data-stu-id="9b944-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="9b944-105">此移动应用以前称为 *Microsoft Dynamics 365 for Finance and Operations*。</span><span class="sxs-lookup"><span data-stu-id="9b944-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="9b944-106">概览</span><span class="sxs-lookup"><span data-stu-id="9b944-106">Overview</span></span>
--------

<span data-ttu-id="9b944-107">此移动应用让您的组织可以允许移动设备使用此应用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="9b944-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="9b944-108">在您的 IT 管理员为您的组织启用此移动工作区后，用户可以登录到此应用并立即开始从其移动设备运行业务流程。</span><span class="sxs-lookup"><span data-stu-id="9b944-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="9b944-109">此移动应用包括可帮助提高生产率的以下功能：</span><span class="sxs-lookup"><span data-stu-id="9b944-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="9b944-110">用户可以查看、编辑并对业务数据进行操作，即使他们具有间歇的网络或其移动设备完全脱机。</span><span class="sxs-lookup"><span data-stu-id="9b944-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="9b944-111">在设备重新建立网络连接后，脱机数据操作自动与 Dynamics 365 for Finance and Operations Enterprise 版本或 Microsoft Dynamics 365 for Finance and Operations 同步。</span><span class="sxs-lookup"><span data-stu-id="9b944-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="9b944-112">IT 管理员或开发人员可以构建和发布为组织量身定制的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="9b944-113">此应用使用您现有的代码资产。</span><span class="sxs-lookup"><span data-stu-id="9b944-113">The app uses your existing code assets.</span></span> <span data-ttu-id="9b944-114">因此，无需再次实施您的验证过程、业务逻辑或安全配置。</span><span class="sxs-lookup"><span data-stu-id="9b944-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="9b944-115">IT 管理员或开发人员通过使用包含在 Web 客户端内的指向-点击工作区设计器轻松设计移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="9b944-116">通过使用业务逻辑可扩展性框架，IT 管理员或开发人员可以有选择地优化工作区的脱机功能。</span><span class="sxs-lookup"><span data-stu-id="9b944-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="9b944-117">由于数据在设备脱机时继续处理，移动方案仍然丰富、可变，即使设备没有固定的网络连接。</span><span class="sxs-lookup"><span data-stu-id="9b944-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="9b944-118">移动应用的元素</span><span class="sxs-lookup"><span data-stu-id="9b944-118">Elements of the mobile app</span></span>
<span data-ttu-id="9b944-119">移动应用的导航包括四个基本的概念：仪表板、工作区、页面和操作。</span><span class="sxs-lookup"><span data-stu-id="9b944-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="9b944-120">[![移动应用的导航概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="9b944-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="9b944-121">当您启动应用后，转到**仪表板**。</span><span class="sxs-lookup"><span data-stu-id="9b944-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="9b944-122">在仪表板上，可以看到已发布的**工作区**。</span><span class="sxs-lookup"><span data-stu-id="9b944-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="9b944-123">在各个工作区，您可看到该工作区可用的**页面**的列表。</span><span class="sxs-lookup"><span data-stu-id="9b944-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="9b944-124">进入页面后，可以执行若干操作。</span><span class="sxs-lookup"><span data-stu-id="9b944-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="9b944-125">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="9b944-125">Here are some examples:</span></span>

    - <span data-ttu-id="9b944-126">查看详细数据。</span><span class="sxs-lookup"><span data-stu-id="9b944-126">View detailed data.</span></span>
    - <span data-ttu-id="9b944-127">导航到相关数据的其他页面，如实体详细信息或行。</span><span class="sxs-lookup"><span data-stu-id="9b944-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="9b944-128">参阅对该页面可用的**操作**列表。</span><span class="sxs-lookup"><span data-stu-id="9b944-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="9b944-129">操作允许您创建或编辑现有数据。</span><span class="sxs-lookup"><span data-stu-id="9b944-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="9b944-130">实施流程</span><span class="sxs-lookup"><span data-stu-id="9b944-130">Implementation process</span></span>
<span data-ttu-id="9b944-131">下图显示实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的流程。</span><span class="sxs-lookup"><span data-stu-id="9b944-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![移动应用实现流程](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="9b944-133">下表包括可以帮助您实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的资源的链接。</span><span class="sxs-lookup"><span data-stu-id="9b944-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="9b944-134">第一列的数字对应上一图中已编号的步骤。</span><span class="sxs-lookup"><span data-stu-id="9b944-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b944-135">步骤</span><span class="sxs-lookup"><span data-stu-id="9b944-135">Step</span></span></th>
<th><span data-ttu-id="9b944-136">角色</span><span class="sxs-lookup"><span data-stu-id="9b944-136">Role</span></span></th>
<th><span data-ttu-id="9b944-137">行动</span><span class="sxs-lookup"><span data-stu-id="9b944-137">Action</span></span></th>
<th><span data-ttu-id="9b944-138">帮助您完成操作的资源</span><span class="sxs-lookup"><span data-stu-id="9b944-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b944-139">1</span><span class="sxs-lookup"><span data-stu-id="9b944-139">1</span></span></td>
<td><span data-ttu-id="9b944-140">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9b944-140">System administrator</span></span></td>
<td><span data-ttu-id="9b944-141">实现 Finance and Operations 或您的组织中的 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9b944-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="9b944-142">如果尚未部署 Microsoft Dynamics 365 的一个版本，请参阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="9b944-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="9b944-143">若要查看可以使用的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="9b944-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b944-144">2</span><span class="sxs-lookup"><span data-stu-id="9b944-144">2</span></span></td>
<td><span data-ttu-id="9b944-145">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9b944-145">System administrator</span></span></td>
<td><span data-ttu-id="9b944-146"><strong>如果您使用的是 Microsoft Dynamics 365 for Finance and Operations 版本 1611：</strong>下载并安装启用 Microsoft 提供的移动工作区的 KB。</span><span class="sxs-lookup"><span data-stu-id="9b944-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="9b944-147">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="9b944-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="9b944-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">成本控制移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="9b944-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">现有库存量移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="9b944-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">销售订单移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="9b944-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">供应商协作移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="9b944-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">项目时间条目移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="9b944-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">费用报销管理移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b944-154">3</span><span class="sxs-lookup"><span data-stu-id="9b944-154">3</span></span></td>
<td><span data-ttu-id="9b944-155">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9b944-155">System administrator</span></span></td>
<td><span data-ttu-id="9b944-156">发布 Microsoft 提供的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="9b944-157"><a href="publish-mobile-workspace.md">发布移动工作区</a>
</span><span class="sxs-lookup"><span data-stu-id="9b944-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b944-158">4</span><span class="sxs-lookup"><span data-stu-id="9b944-158">4</span></span></td>
<td><span data-ttu-id="9b944-159">开发商或独立软件供应商 (ISV)</span><span class="sxs-lookup"><span data-stu-id="9b944-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="9b944-160">使用移动平台创建自定义移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="9b944-161"><a href="platform/mobile-platform-home-page.md">移动平台</a></span><span class="sxs-lookup"><span data-stu-id="9b944-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b944-162">5</span><span class="sxs-lookup"><span data-stu-id="9b944-162">5</span></span></td>
<td><span data-ttu-id="9b944-163">ISV / 独立软件供应商</span><span class="sxs-lookup"><span data-stu-id="9b944-163">ISV</span></span></td>
<td><span data-ttu-id="9b944-164">创建包含自定义移动工作区的可部署包，并上载包到 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="9b944-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="9b944-165"><a href="../deployment/create-apply-deployable-package.md">创建可部署包</a></span><span class="sxs-lookup"><span data-stu-id="9b944-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b944-166">6</span><span class="sxs-lookup"><span data-stu-id="9b944-166">6</span></span></td>
<td><span data-ttu-id="9b944-167">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9b944-167">System administrator</span></span></td>
<td><span data-ttu-id="9b944-168">应用包含独立软件供应商 (ISV) 提供的自定义工作区的可部署包。</span><span class="sxs-lookup"><span data-stu-id="9b944-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="9b944-169"><a href="../deployment/apply-deployable-package-system.md">应用可部署包</a></span><span class="sxs-lookup"><span data-stu-id="9b944-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b944-170">7</span><span class="sxs-lookup"><span data-stu-id="9b944-170">7</span></span></td>
<td><span data-ttu-id="9b944-171">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9b944-171">System administrator</span></span></td>
<td><span data-ttu-id="9b944-172">发布 ISV 提供的自定义移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="9b944-173"><a href="publish-mobile-workspace.md">发布移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="9b944-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b944-174">8</span><span class="sxs-lookup"><span data-stu-id="9b944-174">8</span></span></td>
<td><span data-ttu-id="9b944-175">用户</span><span class="sxs-lookup"><span data-stu-id="9b944-175">User</span></span></td>
<td><span data-ttu-id="9b944-176">下载并安装移动应用。</span><span class="sxs-lookup"><span data-stu-id="9b944-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="9b944-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">适用于 Android 手机</a></span><span class="sxs-lookup"><span data-stu-id="9b944-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="9b944-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">适用于 iPhones</a></span><span class="sxs-lookup"><span data-stu-id="9b944-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b944-179">9</span><span class="sxs-lookup"><span data-stu-id="9b944-179">9</span></span></td>
<td><span data-ttu-id="9b944-180">用户</span><span class="sxs-lookup"><span data-stu-id="9b944-180">User</span></span></td>
<td><span data-ttu-id="9b944-181">登录并使用移动应用。</span><span class="sxs-lookup"><span data-stu-id="9b944-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="9b944-182">此应用中包括系统管理员已发布的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="9b944-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="9b944-183">若要查看由 Microsoft 提供的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="9b944-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

