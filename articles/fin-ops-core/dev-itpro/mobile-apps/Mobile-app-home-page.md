---
title: 移动应用主页
description: 此主题描述 Finance and Operations (Dynamics 365) 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。
author: ChrisGarty
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: e4a9d6424e2d214624c148c0565c88ea4cf4ccf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683450"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="aafbb-103">移动应用主页</span><span class="sxs-lookup"><span data-stu-id="aafbb-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aafbb-104">此主题描述 **Finance and Operations (Dynamics 365)** 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。</span><span class="sxs-lookup"><span data-stu-id="aafbb-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="aafbb-105">概览</span><span class="sxs-lookup"><span data-stu-id="aafbb-105">Overview</span></span>
--------

<span data-ttu-id="aafbb-106">此移动应用让您的组织可以允许移动设备使用此应用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="aafbb-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="aafbb-107">在您的 IT 管理员为您的组织启用此移动工作区后，用户可以登录到此应用并立即开始从其移动设备运行业务流程。</span><span class="sxs-lookup"><span data-stu-id="aafbb-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="aafbb-108">此移动应用包括可帮助提高生产率的以下功能：</span><span class="sxs-lookup"><span data-stu-id="aafbb-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="aafbb-109">用户可以查看、编辑并对业务数据进行操作，即使他们具有间歇的网络或其移动设备完全脱机。</span><span class="sxs-lookup"><span data-stu-id="aafbb-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="aafbb-110">在设备重新建立网络连接时，脱机数据操作自动同步。</span><span class="sxs-lookup"><span data-stu-id="aafbb-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="aafbb-111">IT 管理员或开发人员可以构建和发布为组织量身定制的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="aafbb-112">此应用使用您现有的代码资产。</span><span class="sxs-lookup"><span data-stu-id="aafbb-112">The app uses your existing code assets.</span></span> <span data-ttu-id="aafbb-113">因此，无需再次实施您的验证过程、业务逻辑或安全配置。</span><span class="sxs-lookup"><span data-stu-id="aafbb-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="aafbb-114">IT 管理员或开发人员通过使用包含在 Web 客户端内的指向-点击工作区设计器轻松设计移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="aafbb-115">通过使用业务逻辑可扩展性框架，IT 管理员或开发人员可以有选择地优化工作区的脱机功能。</span><span class="sxs-lookup"><span data-stu-id="aafbb-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="aafbb-116">由于数据在设备脱机时继续处理，移动方案仍然丰富、可变，即使设备没有固定的网络连接。</span><span class="sxs-lookup"><span data-stu-id="aafbb-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="aafbb-117">移动应用的元素</span><span class="sxs-lookup"><span data-stu-id="aafbb-117">Elements of the mobile app</span></span>
<span data-ttu-id="aafbb-118">移动应用的导航包括四个基本的概念：仪表板、工作区、页面和操作。</span><span class="sxs-lookup"><span data-stu-id="aafbb-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="aafbb-119">[![移动应用的导航概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="aafbb-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="aafbb-120">当您启动应用后，转到 **仪表板**。</span><span class="sxs-lookup"><span data-stu-id="aafbb-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="aafbb-121">在仪表板上，可以看到已发布的 **工作区**。</span><span class="sxs-lookup"><span data-stu-id="aafbb-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="aafbb-122">在各个工作区，您可看到该工作区可用的 **页面** 的列表。</span><span class="sxs-lookup"><span data-stu-id="aafbb-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="aafbb-123">进入页面后，可以执行若干操作。</span><span class="sxs-lookup"><span data-stu-id="aafbb-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="aafbb-124">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="aafbb-124">Here are some examples:</span></span>

    - <span data-ttu-id="aafbb-125">查看详细数据。</span><span class="sxs-lookup"><span data-stu-id="aafbb-125">View detailed data.</span></span>
    - <span data-ttu-id="aafbb-126">导航到相关数据的其他页面，如实体详细信息或行。</span><span class="sxs-lookup"><span data-stu-id="aafbb-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="aafbb-127">参阅对该页面可用的 **操作** 列表。</span><span class="sxs-lookup"><span data-stu-id="aafbb-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="aafbb-128">操作允许您创建或编辑现有数据。</span><span class="sxs-lookup"><span data-stu-id="aafbb-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="aafbb-129">实施流程</span><span class="sxs-lookup"><span data-stu-id="aafbb-129">Implementation process</span></span>
<span data-ttu-id="aafbb-130">下图显示实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的流程。</span><span class="sxs-lookup"><span data-stu-id="aafbb-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="aafbb-131">[![移动应用实现流程](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="aafbb-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="aafbb-132">下表包括可以帮助您实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的资源的链接。</span><span class="sxs-lookup"><span data-stu-id="aafbb-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="aafbb-133">第一列的数字对应上一图中已编号的步骤。</span><span class="sxs-lookup"><span data-stu-id="aafbb-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aafbb-134">步骤</span><span class="sxs-lookup"><span data-stu-id="aafbb-134">Step</span></span></th>
<th><span data-ttu-id="aafbb-135">角色</span><span class="sxs-lookup"><span data-stu-id="aafbb-135">Role</span></span></th>
<th><span data-ttu-id="aafbb-136">行动</span><span class="sxs-lookup"><span data-stu-id="aafbb-136">Action</span></span></th>
<th><span data-ttu-id="aafbb-137">帮助您完成操作的资源</span><span class="sxs-lookup"><span data-stu-id="aafbb-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aafbb-138">1</span><span class="sxs-lookup"><span data-stu-id="aafbb-138">1</span></span></td>
<td><span data-ttu-id="aafbb-139">系统管理员</span><span class="sxs-lookup"><span data-stu-id="aafbb-139">System administrator</span></span></td>
<td><span data-ttu-id="aafbb-140">在您的组织中实施 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="aafbb-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="aafbb-141">如果尚未部署 Microsoft Dynamics 365 的一个版本，请参阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="aafbb-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="aafbb-142">若要查看可以使用的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="aafbb-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aafbb-143">2</span><span class="sxs-lookup"><span data-stu-id="aafbb-143">2</span></span></td>
<td><span data-ttu-id="aafbb-144">系统管理员</span><span class="sxs-lookup"><span data-stu-id="aafbb-144">System administrator</span></span></td>
<td><span data-ttu-id="aafbb-145"><strong>如果您使用的是 Microsoft Dynamics 365 for Operations 版本 1611：</strong>下载并安装支持 Microsoft 提供的移动工作区的 KB。</span><span class="sxs-lookup"><span data-stu-id="aafbb-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="aafbb-146">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aafbb-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="aafbb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">成本控制移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="aafbb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">现有库存量移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="aafbb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">销售订单移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="aafbb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">供应商协作移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="aafbb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">项目时间条目移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="aafbb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">费用报销管理移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aafbb-153">3</span><span class="sxs-lookup"><span data-stu-id="aafbb-153">3</span></span></td>
<td><span data-ttu-id="aafbb-154">系统管理员</span><span class="sxs-lookup"><span data-stu-id="aafbb-154">System administrator</span></span></td>
<td><span data-ttu-id="aafbb-155">发布 Microsoft 提供的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="aafbb-156"><a href="publish-mobile-workspace.md">发布移动工作区</a>
</span><span class="sxs-lookup"><span data-stu-id="aafbb-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aafbb-157">4</span><span class="sxs-lookup"><span data-stu-id="aafbb-157">4</span></span></td>
<td><span data-ttu-id="aafbb-158">开发商或独立软件供应商 (ISV)</span><span class="sxs-lookup"><span data-stu-id="aafbb-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="aafbb-159">使用移动平台创建自定义移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="aafbb-160"><a href="platform/mobile-platform-home-page.md">移动平台</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aafbb-161">5</span><span class="sxs-lookup"><span data-stu-id="aafbb-161">5</span></span></td>
<td><span data-ttu-id="aafbb-162">ISV / 独立软件供应商</span><span class="sxs-lookup"><span data-stu-id="aafbb-162">ISV</span></span></td>
<td><span data-ttu-id="aafbb-163">创建包含自定义移动工作区的可部署包，并上载包到 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="aafbb-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="aafbb-164"><a href="../deployment/create-apply-deployable-package.md">创建可部署包</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aafbb-165">6</span><span class="sxs-lookup"><span data-stu-id="aafbb-165">6</span></span></td>
<td><span data-ttu-id="aafbb-166">系统管理员</span><span class="sxs-lookup"><span data-stu-id="aafbb-166">System administrator</span></span></td>
<td><span data-ttu-id="aafbb-167">应用包含独立软件供应商 (ISV) 提供的自定义工作区的可部署包。</span><span class="sxs-lookup"><span data-stu-id="aafbb-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="aafbb-168"><a href="../deployment/apply-deployable-package-system.md">应用可部署包</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aafbb-169">7</span><span class="sxs-lookup"><span data-stu-id="aafbb-169">7</span></span></td>
<td><span data-ttu-id="aafbb-170">系统管理员</span><span class="sxs-lookup"><span data-stu-id="aafbb-170">System administrator</span></span></td>
<td><span data-ttu-id="aafbb-171">发布 ISV 提供的自定义移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="aafbb-172"><a href="publish-mobile-workspace.md">发布移动工作区</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aafbb-173">8</span><span class="sxs-lookup"><span data-stu-id="aafbb-173">8</span></span></td>
<td><span data-ttu-id="aafbb-174">用户</span><span class="sxs-lookup"><span data-stu-id="aafbb-174">User</span></span></td>
<td><span data-ttu-id="aafbb-175">下载并安装移动应用。</span><span class="sxs-lookup"><span data-stu-id="aafbb-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="aafbb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">适用于 Android 的 Finance and Operations 应用</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="aafbb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">适用于 iOS 的 Finance and Operations 应用</a></span><span class="sxs-lookup"><span data-stu-id="aafbb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="aafbb-178">（支持 Windows Phone）</span><span class="sxs-lookup"><span data-stu-id="aafbb-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aafbb-179">9</span><span class="sxs-lookup"><span data-stu-id="aafbb-179">9</span></span></td>
<td><span data-ttu-id="aafbb-180">用户</span><span class="sxs-lookup"><span data-stu-id="aafbb-180">User</span></span></td>
<td><span data-ttu-id="aafbb-181">登录并使用移动应用。</span><span class="sxs-lookup"><span data-stu-id="aafbb-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="aafbb-182">此应用中包括系统管理员已发布的移动工作区。</span><span class="sxs-lookup"><span data-stu-id="aafbb-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="aafbb-183">若要查看由 Microsoft 提供的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="aafbb-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="aafbb-184">疑难解答</span><span class="sxs-lookup"><span data-stu-id="aafbb-184">Troubleshooting</span></span>
[<span data-ttu-id="aafbb-185">移动平台资源</span><span class="sxs-lookup"><span data-stu-id="aafbb-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
