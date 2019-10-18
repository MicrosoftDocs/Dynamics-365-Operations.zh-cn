---
title: 成本控制移动工作区
description: 此主题提供有关成本控制移动工作区的信息。 此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 27381a408df64b8f11323b2f164d242bb2c4b6c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249693"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="7764d-104">成本控制移动工作区</span><span class="sxs-lookup"><span data-stu-id="7764d-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7764d-105">此主题提供有关**成本控制**移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="7764d-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="7764d-106">此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。</span><span class="sxs-lookup"><span data-stu-id="7764d-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="7764d-107">此工作区应该与 Finance and Operations mobile 应用程序结合使用。</span><span class="sxs-lookup"><span data-stu-id="7764d-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="7764d-108">概览</span><span class="sxs-lookup"><span data-stu-id="7764d-108">Overview</span></span>
<span data-ttu-id="7764d-109">**成本控制**移动工作区通过比较实际成本与预算成本，提供成本中心当前绩效的即时视图。</span><span class="sxs-lookup"><span data-stu-id="7764d-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="7764d-110">可以向下钻取单个成本元素的状态。</span><span class="sxs-lookup"><span data-stu-id="7764d-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="7764d-111">例如，员工收到国际会议的邀请，但组织必须支付所有差旅费。</span><span class="sxs-lookup"><span data-stu-id="7764d-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="7764d-112">员工询问经理是否可参加此会议。</span><span class="sxs-lookup"><span data-stu-id="7764d-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="7764d-113">经理使用自己的移动设备打开**成本控制**移动工作区，查看她是否有员工参加此会议的预算。</span><span class="sxs-lookup"><span data-stu-id="7764d-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="7764d-114">数据安全</span><span class="sxs-lookup"><span data-stu-id="7764d-114">Data security</span></span>
<span data-ttu-id="7764d-115">**成本控制**移动工作区中的数据通过用户凭据加以保护。</span><span class="sxs-lookup"><span data-stu-id="7764d-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="7764d-116">成本中心经理只能查看自己成本中心的数据。</span><span class="sxs-lookup"><span data-stu-id="7764d-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="7764d-117">访问级别安全在**成本核算**模板内管理。</span><span class="sxs-lookup"><span data-stu-id="7764d-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="7764d-118">成本会计员定义**成本核算**模块中的**成本控制**移动工作区的配置。</span><span class="sxs-lookup"><span data-stu-id="7764d-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="7764d-119">此工作区发布到移动应用之后，可在此应用程序中使用。</span><span class="sxs-lookup"><span data-stu-id="7764d-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="7764d-120">因此，组织中的所有成本中心经理均可以相同格式查看数据。</span><span class="sxs-lookup"><span data-stu-id="7764d-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="7764d-121">操作、视图和链接</span><span class="sxs-lookup"><span data-stu-id="7764d-121">Actions, views, and links</span></span>
<span data-ttu-id="7764d-122">**成本控制**移动工作区提供以下操作、视图和链接：</span><span class="sxs-lookup"><span data-stu-id="7764d-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="7764d-123">**操作：**</span><span class="sxs-lookup"><span data-stu-id="7764d-123">**Actions:**</span></span>

    -   <span data-ttu-id="7764d-124">使用**选择配置**选择布局。</span><span class="sxs-lookup"><span data-stu-id="7764d-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="7764d-125">使用**选择成本对象**选择要筛选数据的成本中心。</span><span class="sxs-lookup"><span data-stu-id="7764d-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="7764d-126">显示在列表中的成本中心取决于**成本核算**模块中授予的访问权限。</span><span class="sxs-lookup"><span data-stu-id="7764d-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="7764d-127">**视图：** 基于选择的操作和**成本核算**模块中的配置，可以查看卡中的以下信息：</span><span class="sxs-lookup"><span data-stu-id="7764d-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="7764d-128">实际值与预算(当前期间)</span><span class="sxs-lookup"><span data-stu-id="7764d-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="7764d-129">实际值与已修订的预算(当前期间)</span><span class="sxs-lookup"><span data-stu-id="7764d-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="7764d-130">实际值与预算（上一期间）</span><span class="sxs-lookup"><span data-stu-id="7764d-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="7764d-131">实际值与已修订的预算（上一期间）</span><span class="sxs-lookup"><span data-stu-id="7764d-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="7764d-132">实际值与预算（本年迄今）</span><span class="sxs-lookup"><span data-stu-id="7764d-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="7764d-133">实际值与已修订的预算（本年迄今）</span><span class="sxs-lookup"><span data-stu-id="7764d-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="7764d-134">以下金额在每个卡显示：实际值、预算、差异和差异百分比。</span><span class="sxs-lookup"><span data-stu-id="7764d-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="7764d-135">**链接：**</span><span class="sxs-lookup"><span data-stu-id="7764d-135">**Links:**</span></span>

    -   <span data-ttu-id="7764d-136">当前期间的详细信息</span><span class="sxs-lookup"><span data-stu-id="7764d-136">Details for current period</span></span>
    -   <span data-ttu-id="7764d-137">上一期间的详细信息</span><span class="sxs-lookup"><span data-stu-id="7764d-137">Details for previous period</span></span>
    -   <span data-ttu-id="7764d-138">本年迄今的详细信息</span><span class="sxs-lookup"><span data-stu-id="7764d-138">Details for year to date</span></span>

    <span data-ttu-id="7764d-139">当您选择链接时，为各成本要素显示卡。</span><span class="sxs-lookup"><span data-stu-id="7764d-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="7764d-140">将显示每个卡中的以下金额：“实际值”、“预算差异”、“预算差异百分比”、“已修订的预算”、“已修订的预算差异”和“已修订的预算差异百分比”。</span><span class="sxs-lookup"><span data-stu-id="7764d-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="7764d-141">[![成本元素的卡](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="7764d-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7764d-142">先决条件</span><span class="sxs-lookup"><span data-stu-id="7764d-142">Prerequisites</span></span>
<span data-ttu-id="7764d-143">先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。</span><span class="sxs-lookup"><span data-stu-id="7764d-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="7764d-144">使用 Microsoft Dynamics 365 Finance 的先决条件</span><span class="sxs-lookup"><span data-stu-id="7764d-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="7764d-145">如果已经为您的组织部署 Finance，系统管理员必须发布**成本控制**移动工作区。</span><span class="sxs-lookup"><span data-stu-id="7764d-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="7764d-146">有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="7764d-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="7764d-147">使用带平台更新 3 或更高版本的版本 1611 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="7764d-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="7764d-148">如果已经为您的组织部署带平台更新 3 或更高版本的版本 1611，系统管理员必须完成以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="7764d-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7764d-149">必备项</span><span class="sxs-lookup"><span data-stu-id="7764d-149">Prerequisite</span></span></th>
<th><span data-ttu-id="7764d-150">角色</span><span class="sxs-lookup"><span data-stu-id="7764d-150">Role</span></span></th>
<th><span data-ttu-id="7764d-151">说明</span><span class="sxs-lookup"><span data-stu-id="7764d-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7764d-152">实现 KB 4013633。</span><span class="sxs-lookup"><span data-stu-id="7764d-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="7764d-153">系统管理员</span><span class="sxs-lookup"><span data-stu-id="7764d-153">System administrator</span></span></td>

<td><span data-ttu-id="7764d-154">KB 4013633 是包含<strong>成本控制</strong>移动工作区的 X++ 更新或元数据修补程序。</span><span class="sxs-lookup"><span data-stu-id="7764d-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="7764d-155">若要实施 KB 4013633，系统管理员必须遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7764d-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="7764d-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="7764d-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="7764d-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="7764d-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="7764d-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="7764d-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="7764d-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</span><span class="sxs-lookup"><span data-stu-id="7764d-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7764d-160">发布<strong>成本控制</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="7764d-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="7764d-161">系统管理员</span><span class="sxs-lookup"><span data-stu-id="7764d-161">System administrator</span></span></td>
<td><span data-ttu-id="7764d-162">请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="7764d-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="7764d-163">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="7764d-163">Download and install the mobile app</span></span>
<span data-ttu-id="7764d-164">下载并安装 Finance and Operations 移动应用程序：</span><span class="sxs-lookup"><span data-stu-id="7764d-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="7764d-165">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="7764d-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="7764d-166">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="7764d-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="7764d-167">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="7764d-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="7764d-168">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="7764d-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="7764d-169">输入您的 Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="7764d-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="7764d-170">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="7764d-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="7764d-171">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="7764d-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="7764d-172">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="7764d-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="7764d-173">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="7764d-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="7764d-174">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="7764d-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="7764d-175">使用成本控制移动工作区查看成本中心的绩效</span><span class="sxs-lookup"><span data-stu-id="7764d-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="7764d-176">在移动设备上，选择**成本控制**工作区。</span><span class="sxs-lookup"><span data-stu-id="7764d-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="7764d-177">选择**成本对象控制**。</span><span class="sxs-lookup"><span data-stu-id="7764d-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="7764d-178">选择**操作**。</span><span class="sxs-lookup"><span data-stu-id="7764d-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="7764d-179">选择**选择配置**以选择成本控制布局。</span><span class="sxs-lookup"><span data-stu-id="7764d-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="7764d-180">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="7764d-180">Select **Done**.</span></span>
6.  <span data-ttu-id="7764d-181">选择**操作**。</span><span class="sxs-lookup"><span data-stu-id="7764d-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="7764d-182">选择**选择成本对象**以选择为您授予了访问权限的成本中心。</span><span class="sxs-lookup"><span data-stu-id="7764d-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="7764d-183">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="7764d-183">Select **Done**.</span></span>
9.  <span data-ttu-id="7764d-184">查看成本中心的整体绩效。</span><span class="sxs-lookup"><span data-stu-id="7764d-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="7764d-185">选择**当前期间的详细信息**链接。</span><span class="sxs-lookup"><span data-stu-id="7764d-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="7764d-186">查看单个成本元素的绩效。</span><span class="sxs-lookup"><span data-stu-id="7764d-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="7764d-187">也可以搜索特定成本元素。</span><span class="sxs-lookup"><span data-stu-id="7764d-187">You can also search for specific cost elements.</span></span>

