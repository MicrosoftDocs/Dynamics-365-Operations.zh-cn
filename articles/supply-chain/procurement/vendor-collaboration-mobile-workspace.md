---
title: 供应商协作移动工作区
description: 此主题提供有关供应商协作移动工作区的信息。 此工作区帮助您的供应商实时了解已经发送给他们进行审核的采购订单的最新信息。 它们还可以查看有关新的和更新的采购订单和联系人的信息。
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: dabourq
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: dee77f6967cc72fdcc81d5cff9a39d13248af588
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811030"
---
# <a name="vendor-collaboration-mobile-workspace"></a><span data-ttu-id="03005-105">供应商协作移动工作区</span><span class="sxs-lookup"><span data-stu-id="03005-105">Vendor collaboration mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03005-106">此主题提供有关 **供应商协作** 移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="03005-106">This topic provides information about the **Vendor collaboration** mobile workspace.</span></span> <span data-ttu-id="03005-107">此工作区帮助您的供应商实时了解已经发送给他们进行审核的采购订单的最新信息。</span><span class="sxs-lookup"><span data-stu-id="03005-107">This workspace helps your vendors stay up to date about the purchase orders that have been sent to them for approval.</span></span> <span data-ttu-id="03005-108">它们还可以查看有关新的和更新的采购订单和联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="03005-108">They can also view information about new and updated purchase orders and contacts.</span></span>

<span data-ttu-id="03005-109">此工作区应该与 Finance and Operations 移动应用结合使用。</span><span class="sxs-lookup"><span data-stu-id="03005-109">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="03005-110">概览</span><span class="sxs-lookup"><span data-stu-id="03005-110">Overview</span></span> 
<span data-ttu-id="03005-111">**供应商协作** 移动工作区通知供应商有关新采购订单的信息，以便供应商可以在 Web 客户端中查看和响应采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-111">The **Vendor collaboration** mobile workspace keeps vendors informed about new purchase orders, so that they can view purchase orders and then respond to them in the web client.</span></span> 

>[!NOTE]
> <span data-ttu-id="03005-112">此移动工作区将用作供应商协作 Web 界面的补充，但不代替后者。</span><span class="sxs-lookup"><span data-stu-id="03005-112">The mobile workspace should be used as a supplement to the vendor collaboration web interface, not a replacement for it.</span></span> 

<span data-ttu-id="03005-113">您的供应商可以使用 **供应商协作** 移动工作区查看发送给他们进行审核的新采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-113">Your vendors can use the **Vendor collaboration** mobile workspace to view new purchase orders that are sent to them for approval.</span></span> <span data-ttu-id="03005-114">其中显示采购订单信息，如产品、数量和请求的交货日期。</span><span class="sxs-lookup"><span data-stu-id="03005-114">It shows purchase order information, such as products, quantities, and requested delivery dates.</span></span> <span data-ttu-id="03005-115">根据各供应商的配置决定是否显示价格信息。</span><span class="sxs-lookup"><span data-stu-id="03005-115">Price information is also available, depending on the configuration of each vendor.</span></span> 

<span data-ttu-id="03005-116">作为供应商登录的用户将看到已响应了哪些采购订单，以及哪些采购订单仍在等待客户操作。</span><span class="sxs-lookup"><span data-stu-id="03005-116">A user who signs in as a vendor will see which purchase orders have been responded to, and which purchase orders are still awaiting customer action.</span></span> <span data-ttu-id="03005-117">例如，采购订单可能正在等待客户操作，因为供应商建议了其他交货日期，但客户尚未同意该日期。</span><span class="sxs-lookup"><span data-stu-id="03005-117">For example, a purchase order might be awaiting customer action because the vendor suggested another delivery date, but the customer hasn't yet agreed to that date.</span></span> <span data-ttu-id="03005-118">供应商还将看到已确认但尚未交货的采购订单的列表。</span><span class="sxs-lookup"><span data-stu-id="03005-118">The vendor will also see a list of purchase orders that have been confirmed but haven't yet been delivered.</span></span> 

<span data-ttu-id="03005-119">若要响应采购订单，供应商必须使用在 Web 客户端中提供的供应商协作 Web 界面。</span><span class="sxs-lookup"><span data-stu-id="03005-119">To respond to a purchase order, the vendor must use the vendor collaboration web interface that is available in the web client.</span></span> <span data-ttu-id="03005-120">供应商也可以在此处获取有关订单的更多信息，如票据附件、按行的交货地址，以及供应商的相关费用。</span><span class="sxs-lookup"><span data-stu-id="03005-120">There, the vendor can also get more information about the order, such as document attachments, the delivery address per line, and charges that are associated with the vendor.</span></span> 

<span data-ttu-id="03005-121">具有特殊安全角色的供应商可以查看为供应商帐户注册了哪些联系人。</span><span class="sxs-lookup"><span data-stu-id="03005-121">Vendors that have a special security role can see which contact persons are registered for a vendor account.</span></span> <span data-ttu-id="03005-122">通过相同的安全角色，供应商可以查看已提交的任何用户请求的状态。</span><span class="sxs-lookup"><span data-stu-id="03005-122">The same security role lets a vendor view the status of any user request that has been submitted.</span></span> 

<span data-ttu-id="03005-123">必须使用 Web 客户端中的供应商协作 Web 界面创建新联系人和提交新用户请求。</span><span class="sxs-lookup"><span data-stu-id="03005-123">The vendor collaboration web interface in the web client must be used to create new contacts and submit new user requests.</span></span> 

<span data-ttu-id="03005-124">**供应商协作** 移动工作区使供应商可以执行这些任务：</span><span class="sxs-lookup"><span data-stu-id="03005-124">The **Vendor collaboration** mobile workspace lets a vendor perform these tasks:</span></span>

-   <span data-ttu-id="03005-125">查看发送给供应商的新采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-125">View new purchase orders that are sent to the vendor.</span></span>
-   <span data-ttu-id="03005-126">查看供应商已响应的采购订单和正在等待客户操作的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-126">View purchase orders that the vendor has responded to, and that are awaiting customer action.</span></span>
-   <span data-ttu-id="03005-127">查看已确认但尚未完全收货的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-127">View purchase orders that have been confirmed but haven't yet been fully received.</span></span>
-   <span data-ttu-id="03005-128">查看为供应商帐户注册的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="03005-128">View contact person information that is registered for the vendor account.</span></span> <span data-ttu-id="03005-129">（此任务需要其他的安全角色。）</span><span class="sxs-lookup"><span data-stu-id="03005-129">(This task requires an additional security role.)</span></span>
-   <span data-ttu-id="03005-130">查看关于供应商已提交的用户请求的信息和跟踪请求的状态。</span><span class="sxs-lookup"><span data-stu-id="03005-130">View information about a user request that was submitted by the vendor, and follow the status of the request.</span></span> <span data-ttu-id="03005-131">（此任务需要其他的安全角色。）</span><span class="sxs-lookup"><span data-stu-id="03005-131">(This task requires an additional security role.)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03005-132">先决条件</span><span class="sxs-lookup"><span data-stu-id="03005-132">Prerequisites</span></span>
<span data-ttu-id="03005-133">先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本而异。</span><span class="sxs-lookup"><span data-stu-id="03005-133">The prerequisites vary, depending on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="03005-134">使用 Supply Chain Management 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="03005-134">Prerequisites if you use Supply Chain Management</span></span>
<span data-ttu-id="03005-135">如果已经为您的组织部署 Supply Chain Management，系统管理员必须发布 **供应商协作** 移动工作区。</span><span class="sxs-lookup"><span data-stu-id="03005-135">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Vendor collaboration** mobile workspace.</span></span> <span data-ttu-id="03005-136">有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="03005-136">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="03005-137">使用带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="03005-137">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="03005-138">如果已经为您的组织部署带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611，系统管理员必须完成以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="03005-138">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="03005-139">必备项</span><span class="sxs-lookup"><span data-stu-id="03005-139">Prerequisite</span></span></th>
<th><span data-ttu-id="03005-140">角色</span><span class="sxs-lookup"><span data-stu-id="03005-140">Role</span></span></th>
<th><span data-ttu-id="03005-141">说明</span><span class="sxs-lookup"><span data-stu-id="03005-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03005-142">如果您正在使用平台更新 3，则必须实施 KB 3216943。</span><span class="sxs-lookup"><span data-stu-id="03005-142">KB 3216943 must be implemented if you&#39;re using Platform update 3.</span></span></td>
<td><span data-ttu-id="03005-143">系统管理员</span><span class="sxs-lookup"><span data-stu-id="03005-143">System administrator</span></span></td>
<td><span data-ttu-id="03005-144">KB 3216943 是您使用平台更新 3 时必需的二进制更新。</span><span class="sxs-lookup"><span data-stu-id="03005-144">KB 3216943 is a binary update that is required if you&#39;re using Platform update 3.</span></span> <span data-ttu-id="03005-145">要实施此 KB，系统管理员必须遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="03005-145">To implement this KB, the system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="03005-146">从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 3216943。</span><span class="sxs-lookup"><span data-stu-id="03005-146">Download KB 3216943 from Microsoft Dynamics Lifecycle Services (LCS).</span></span></li>
<li><span data-ttu-id="03005-147">安装交货为可部署包的二进制更新。</span><span class="sxs-lookup"><span data-stu-id="03005-147">Install the binary update, which is delivered as a deployable package.</span></span> <span data-ttu-id="03005-148">有关如何应用可部署包的信息，请参阅 <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</span><span class="sxs-lookup"><span data-stu-id="03005-148">For information about how to apply a deployable package, see <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply a deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03005-149">必须实施 KB 4013633。</span><span class="sxs-lookup"><span data-stu-id="03005-149">KB 4013633 must be implemented.</span></span></td>
<td><span data-ttu-id="03005-150">系统管理员</span><span class="sxs-lookup"><span data-stu-id="03005-150">System administrator</span></span></td>
<td><span data-ttu-id="03005-151">KB 4013633 是包含<strong>现有库存量</strong>移动工作区的 X++ 更新或元数据修补程序。</span><span class="sxs-lookup"><span data-stu-id="03005-151">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Inventory on-hand</strong> mobile workspace.</span></span> <span data-ttu-id="03005-152">若要实施 KB 4013633，系统管理员必须遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="03005-152">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="03005-153"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 LCS 下载元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="03005-153"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from LCS</a>.</span></span></li>
<li><span data-ttu-id="03005-154"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="03005-154"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li><li><span data-ttu-id="03005-155"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="03005-155"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="03005-156"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</span><span class="sxs-lookup"><span data-stu-id="03005-156"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03005-157">必须发布<strong>供应商协作</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="03005-157">The <strong>Vendor collaboration</strong> mobile workspace must be published.</span></span></td><td><span data-ttu-id="03005-158">系统管理员</span><span class="sxs-lookup"><span data-stu-id="03005-158">System administrator</span></span></td>
<td><span data-ttu-id="03005-159">请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="03005-159">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03005-160">供应商用户必须有权访问 Web 客户端中的供应商协作 Web 界面和设置供应商协作用户。</span><span class="sxs-lookup"><span data-stu-id="03005-160">The vendor user must have access to the vendor collaboration web interface in the web client and must set up a vendor collaboration user.</span></span></td><td><span data-ttu-id="03005-161">专业采购人员和系统管理员</span><span class="sxs-lookup"><span data-stu-id="03005-161">Purchasing professionals and the system administrator</span></span></td>
<td><span data-ttu-id="03005-162">请按照以下主题中的步骤设置和使用供应商协作 Web 界面。</span><span class="sxs-lookup"><span data-stu-id="03005-162">Follow the steps in the following topics to set up and work with the vendor collaboration web interface.</span></span>
<ul>
<li><span data-ttu-id="03005-163"><a href="vendor-collaboration-work-external-vendors.md">使用供应商协作与外部供应商合作</a></span><span class="sxs-lookup"><span data-stu-id="03005-163"><a href="vendor-collaboration-work-external-vendors.md">Use vendor collaboration to work with external vendors</a></span></span></li>
<li><span data-ttu-id="03005-164"><a href="manage-vendor-collaboration-users.md">管理供应商协作用户</a></span><span class="sxs-lookup"><span data-stu-id="03005-164"><a href="manage-vendor-collaboration-users.md">Manage vendor collaboration users</a></span></span></li>
<li><span data-ttu-id="03005-165"><a href="set-up-maintain-vendor-collaboration.md">设置和维护供应商协作</a></span><span class="sxs-lookup"><span data-stu-id="03005-165"><a href="set-up-maintain-vendor-collaboration.md">Set up and maintain vendor collaboration</a></span></span></li>
<li><span data-ttu-id="03005-166"><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">使用供应商协作在 Supply Chain Management 中与客户合作</a></span><span class="sxs-lookup"><span data-stu-id="03005-166"><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Use vendor collaboration to work with customers in Supply Chain Managements</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="03005-167">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="03005-167">Download and install the mobile app</span></span>

<span data-ttu-id="03005-168">下载并安装 Finance and Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="03005-168">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="03005-169">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="03005-169">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="03005-170">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="03005-170">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="03005-171">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="03005-171">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="03005-172">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="03005-172">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="03005-173">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="03005-173">Enter your Microsoft Dynamics 365 URL.</span></span>
4.  <span data-ttu-id="03005-174">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="03005-174">The first time that you sign in, you’re prompted for your user name and password.</span></span> <span data-ttu-id="03005-175">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="03005-175">Enter your credentials.</span></span>
5.  <span data-ttu-id="03005-176">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="03005-176">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="03005-177">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="03005-177">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="03005-178">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="03005-178">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="use-the-vendor-collaboration-mobile-workspace"></a><span data-ttu-id="03005-179">使用供应商协作移动工作区</span><span class="sxs-lookup"><span data-stu-id="03005-179">Use the Vendor collaboration mobile workspace</span></span>
<span data-ttu-id="03005-180">当您选择 **供应商协作** 工作区时，您将看到以下选项。</span><span class="sxs-lookup"><span data-stu-id="03005-180">When you select the **Vendor collaboration** workspace, you’ll see the following options.</span></span>

![供应商协作移动工作区](./media/vendor-collaboration-mobile-app.png)

<span data-ttu-id="03005-182">**供应商协作** 工作区包括以下页面。</span><span class="sxs-lookup"><span data-stu-id="03005-182">The **Vendor collaboration** workspace includes the following pages.</span></span>

### <a name="contacts"></a><span data-ttu-id="03005-183">联系人</span><span class="sxs-lookup"><span data-stu-id="03005-183">Contacts</span></span>
<span data-ttu-id="03005-184">**联系人** 页面将显示已为供应商帐户设置的所有联系人。</span><span class="sxs-lookup"><span data-stu-id="03005-184">The **Contacts** page lets you see all the contacts that have been set up for the vendor account.</span></span> <span data-ttu-id="03005-185">显示联系人的姓名、要电子邮件地址和用户别名（如果联系人具有别名）。</span><span class="sxs-lookup"><span data-stu-id="03005-185">It shows the contact person's name, primary email address, and user alias, if the contact person has an alias.</span></span> <span data-ttu-id="03005-186">此页还显示联系人的用户帐户是否有效。</span><span class="sxs-lookup"><span data-stu-id="03005-186">This page also shows whether the contact person's user account is active.</span></span> <span data-ttu-id="03005-187">在您选择联系人时，将会看到联系人详细信息，例如该人士作为其联系人的法人。</span><span class="sxs-lookup"><span data-stu-id="03005-187">When you select a contact, you see contact details, such as the legal entities that the person is a contact for.</span></span> <span data-ttu-id="03005-188">您还可以查看联系信息，如电话号码或备选电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="03005-188">You also see contact information, such as a telephone number or an alternative email address.</span></span>

### <a name="user-requests"></a><span data-ttu-id="03005-189">用户请求</span><span class="sxs-lookup"><span data-stu-id="03005-189">User requests</span></span>
<span data-ttu-id="03005-190">可通过 **用户请求** 页面查看您已通过供应商协作 Web 界面提交的所有用户请求。</span><span class="sxs-lookup"><span data-stu-id="03005-190">The **User requests** page lets you see all the user requests that you've submitted via the vendor collaboration web interface.</span></span> <span data-ttu-id="03005-191">还可以跟踪这些请求的状态。</span><span class="sxs-lookup"><span data-stu-id="03005-191">You can also follow the status of those requests.</span></span> <span data-ttu-id="03005-192">选择用户请求时，可以查看请求的内容，添加或停用用户，更改安全性，以及查看为用户注册了哪些安全角色。</span><span class="sxs-lookup"><span data-stu-id="03005-192">When you select a user request, you can see what was requested, add or inactivate a user, change security, and see which security roles were requested for the user.</span></span>

### <a name="purchase-orders-ready-for-review"></a><span data-ttu-id="03005-193">准备就绪可供审核的采购订单</span><span class="sxs-lookup"><span data-stu-id="03005-193">Purchase orders ready for review</span></span>
<span data-ttu-id="03005-194">可通过 **准备就绪可供审核的采购订单** 页面查看客户已发送但尚未响应的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-194">The **Purchase orders ready for review** page lets you see all the purchase orders that the customer has sent, but that haven't yet been responded to.</span></span> <span data-ttu-id="03005-195">可查看有关此类订单的选定信息，如请求了哪些产品和何时交货。</span><span class="sxs-lookup"><span data-stu-id="03005-195">You can view selected information about the order, such as which products were requested and when those products should be delivered.</span></span> <span data-ttu-id="03005-196">根据供应商的配置决定是否显示价格信息。</span><span class="sxs-lookup"><span data-stu-id="03005-196">Price information is also available, depending on the configuration of the vendor.</span></span>

<span data-ttu-id="03005-197">还可查看采购订单是否有附注或附件。</span><span class="sxs-lookup"><span data-stu-id="03005-197">You can also see whether the purchase order has notes or attachments.</span></span> <span data-ttu-id="03005-198">但是，要打开注释和附件，必须使用 Web 客户端中的供应商协作 Web 界面。</span><span class="sxs-lookup"><span data-stu-id="03005-198">However, to open notes and attachments, you must use vendor collaboration web interface in the web client.</span></span> <span data-ttu-id="03005-199">选择 **采购订单行** 以查看所有行及其明细。</span><span class="sxs-lookup"><span data-stu-id="03005-199">Select **Purchase order line** to see all the lines together with their details.</span></span> <span data-ttu-id="03005-200">对于每行，将有一个指示器显示是否有注释或附件，或者交货地址是否与抬头中所示的交货地址不同。</span><span class="sxs-lookup"><span data-stu-id="03005-200">For each line, an indicator will show whether there are notes or attachments, or whether the delivery address differs from the delivery address that is shown on the header.</span></span>

<span data-ttu-id="03005-201">若要响应采购订单，必须使用 Web 客户端中的供应商协作 Web 界面。</span><span class="sxs-lookup"><span data-stu-id="03005-201">To respond to the purchase order, you must use the vendor collaboration web interface in the web client.</span></span>

### <a name="awaiting-customer-action"></a><span data-ttu-id="03005-202">正在等待客户操作</span><span class="sxs-lookup"><span data-stu-id="03005-202">Awaiting customer action</span></span>
<span data-ttu-id="03005-203">可通过 **正在等待客户操作** 页面查找您或您公司中有权访问供应商协作的其他人已响应的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-203">The **Awaiting customer action** page lets you find purchase orders that you or another person in your company who has access to vendor collaboration has responded to.</span></span> <span data-ttu-id="03005-204">仅当客户必须对采购订单执行以下操作之一时，才在此列表中显示采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-204">The purchase orders are visible in this list only if the customer must take one of the following actions on the purchase order:</span></span>

-   <span data-ttu-id="03005-205">如果已拒绝了采购订单，客户必须更新或取消原始订单，然后再重新发送。</span><span class="sxs-lookup"><span data-stu-id="03005-205">If the purchase order was rejected, the customer must either update or cancel the original order, and then send it again.</span></span> <span data-ttu-id="03005-206">再次发送采购订单后，将不再显示在 **正在等待客户操作** 页上。</span><span class="sxs-lookup"><span data-stu-id="03005-206">When the purchase order is sent again, it no longer appears on the **Awaiting customer action** page.</span></span>
-   <span data-ttu-id="03005-207">如果接受了带更改的采购订单，客户必须更新原始订单并重新发送供审核，或根据请求的更改更新订单并立即确认。</span><span class="sxs-lookup"><span data-stu-id="03005-207">If the purchase order was accepted with changes, the customer must either update the original order and then send it again for review, or update the order per the requested changes and then confirm it immediately.</span></span> <span data-ttu-id="03005-208">在两种情况下，采购订单都不再显示在 **正在等待客户操作** 页上。</span><span class="sxs-lookup"><span data-stu-id="03005-208">In both cases, the purchase order no longer appears on the **Awaiting customer action** page.</span></span>
-   <span data-ttu-id="03005-209">如果采购订单已被接受但仍显示在 **正在等待客户操作** 页上，则在接受采购订单时未自动确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="03005-209">If the purchase order was accepted but still appears on the **Awaiting customer action** page, the purchase order wasn't automatically confirmed when it was accepted.</span></span> <span data-ttu-id="03005-210">它现在在等待采购代理将订单状态更改为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="03005-210">It's now waiting for a purchasing agent to change the order status to **Confirmed**.</span></span> <span data-ttu-id="03005-211">一旦供应商接受了订单，通常将把采购订单视为客户与供应商之间的协议。</span><span class="sxs-lookup"><span data-stu-id="03005-211">Typically, a purchase order is considered an agreement between the customer and the vendor as soon as the vendor accepts the order.</span></span> <span data-ttu-id="03005-212">因此，更新至 **已确认** 状态通常只是一种形式。</span><span class="sxs-lookup"><span data-stu-id="03005-212">Therefore, the update to **Confirmed** status is usually just a formality.</span></span>

<span data-ttu-id="03005-213">选择采购订单后，将显示有关响应的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="03005-213">When you select a purchase order, additional details appear about the response.</span></span> <span data-ttu-id="03005-214">可查看每行的行明细和响应。</span><span class="sxs-lookup"><span data-stu-id="03005-214">You can see the line details and response for every line.</span></span> <span data-ttu-id="03005-215">行状态显示已提供了以下响应中的哪些响应：</span><span class="sxs-lookup"><span data-stu-id="03005-215">The line status shows which of the following responses has been given:</span></span>

-   <span data-ttu-id="03005-216">已接受</span><span class="sxs-lookup"><span data-stu-id="03005-216">Accepted</span></span>
-   <span data-ttu-id="03005-217">已拒绝</span><span class="sxs-lookup"><span data-stu-id="03005-217">Rejected</span></span>
-   <span data-ttu-id="03005-218">已接受更改</span><span class="sxs-lookup"><span data-stu-id="03005-218">Accepted with changes</span></span>
-   <span data-ttu-id="03005-219">已替代/替代</span><span class="sxs-lookup"><span data-stu-id="03005-219">Substituted/Substitute</span></span>
-   <span data-ttu-id="03005-220">拆分为计划/计划行</span><span class="sxs-lookup"><span data-stu-id="03005-220">Split into schedule/Schedule line</span></span>

<span data-ttu-id="03005-221">请注意，**交货** 字段设置为 **是** 或 **否** 以指示行是否要完全交货。</span><span class="sxs-lookup"><span data-stu-id="03005-221">Note that the **Delivering** field is set to either **Yes** or **No** to indicate whether the lines will be delivered.</span></span> <span data-ttu-id="03005-222">行可能因为以下原因而无法交货：</span><span class="sxs-lookup"><span data-stu-id="03005-222">A line might not be delivered because for the following reasons:</span></span>

- <span data-ttu-id="03005-223">行被拒绝。</span><span class="sxs-lookup"><span data-stu-id="03005-223">The line was rejected.</span></span>
- <span data-ttu-id="03005-224">已进行替换，且预计原始行不会按照已接收订单中的请求交货。</span><span class="sxs-lookup"><span data-stu-id="03005-224">A substitution was made, and the original line isn't expected to be delivered as requested in the received order.</span></span>
- <span data-ttu-id="03005-225">行拆分为多个计划行，且预计原始行不会按照已接收订单中的请求交货。</span><span class="sxs-lookup"><span data-stu-id="03005-225">The line was split into multiple schedule lines, and the original line isn't expected to be delivered as requested in the received order.</span></span>

<span data-ttu-id="03005-226">显示已对订单行响应做出的任何更改。</span><span class="sxs-lookup"><span data-stu-id="03005-226">Any changes that have been made to the order line response are shown.</span></span> <span data-ttu-id="03005-227">但是不显示已上载的注释和附件。</span><span class="sxs-lookup"><span data-stu-id="03005-227">However, uploaded notes and attachments aren't shown.</span></span> <span data-ttu-id="03005-228">要查看注释和附件，必须使用 Web 客户端中的供应商协作 Web 界面。</span><span class="sxs-lookup"><span data-stu-id="03005-228">To view notes and attachments, you must use the vendor collaboration web interface in the web client.</span></span>

### <a name="open-confirmed-orders"></a><span data-ttu-id="03005-229">打开已确认的订单</span><span class="sxs-lookup"><span data-stu-id="03005-229">Open confirmed orders</span></span>
<span data-ttu-id="03005-230">客户确认了采购订单之后（即采购订单的状态已更改为 **已确认**），将显示在未结已确认订单中。</span><span class="sxs-lookup"><span data-stu-id="03005-230">When the purchase order is confirmed by the customer (that is, the status of the purchase order is changed to **Confirmed**), it appears in the open confirmed order.</span></span> <span data-ttu-id="03005-231">它将一直留在列表中，直到客户将其登记为已收货。</span><span class="sxs-lookup"><span data-stu-id="03005-231">It will remain in the list until it's registered as received by the customer.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]