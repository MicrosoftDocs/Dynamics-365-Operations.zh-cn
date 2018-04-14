---
title: "发票审核移动工作区"
description: "此主题提供有关发票审核移动工作区的信息。 此工作区提供通过供应商发票抬头工作流程分配给您的发票的列表。"
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8554d868e675a152ff6e2ff25dd08ab49f02359c
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="26d63-104">发票审核移动工作区</span><span class="sxs-lookup"><span data-stu-id="26d63-104">Invoice approvals mobile workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="26d63-105">此主题提供有关**发票审核**移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="26d63-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="26d63-106">此工作区提供通过供应商发票抬头工作流程分配给您的发票的列表。</span><span class="sxs-lookup"><span data-stu-id="26d63-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="26d63-107">将此工作区用于与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。</span><span class="sxs-lookup"><span data-stu-id="26d63-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="26d63-108">概览</span><span class="sxs-lookup"><span data-stu-id="26d63-108">Overview</span></span>

<span data-ttu-id="26d63-109">**发票审核**移动工作区让应付账款职员和经理能够查看已作为供应商发票抬头工作流程的一部分分配给他们的发票。</span><span class="sxs-lookup"><span data-stu-id="26d63-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="26d63-110">您可以查看发票信息，甚至还可以查看行和分配详细信息，以帮助您做出合理的审核决定。</span><span class="sxs-lookup"><span data-stu-id="26d63-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="26d63-111">从工作区可以执行操作以通过工作流程移动发票。</span><span class="sxs-lookup"><span data-stu-id="26d63-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="26d63-112">必备项</span><span class="sxs-lookup"><span data-stu-id="26d63-112">Prerequisites</span></span>

<span data-ttu-id="26d63-113">在使用此移动工作区之前，必须满足以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="26d63-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26d63-114">必备项</span><span class="sxs-lookup"><span data-stu-id="26d63-114">Prerequisite</span></span></th>
<th><span data-ttu-id="26d63-115">角色</span><span class="sxs-lookup"><span data-stu-id="26d63-115">Role</span></span></th>
<th><span data-ttu-id="26d63-116">说明</span><span class="sxs-lookup"><span data-stu-id="26d63-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26d63-117">必须在您的组织中部署 Microsoft Dynamics 365 for Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="26d63-117">Microsoft Dynamics 365 for Finance and Operations must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="26d63-118">系统管理员</span><span class="sxs-lookup"><span data-stu-id="26d63-118">System administrator</span></span></td>
<td><span data-ttu-id="26d63-119">请查阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="26d63-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="26d63-120">必须发布<strong>发票审核</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="26d63-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="26d63-121">系统管理员</span><span class="sxs-lookup"><span data-stu-id="26d63-121">System administrator</span></span></td>
<td><span data-ttu-id="26d63-122">请查阅<a href="publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="26d63-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="26d63-123">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="26d63-123">Download and install the mobile app</span></span>

<span data-ttu-id="26d63-124">下载并安装 Dynamics 365 for Unified Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="26d63-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="26d63-125">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="26d63-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="26d63-126">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="26d63-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="26d63-127">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="26d63-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="26d63-128">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="26d63-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="26d63-129">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="26d63-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="26d63-130">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="26d63-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="26d63-131">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="26d63-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="26d63-132">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="26d63-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="26d63-133">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="26d63-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="26d63-134">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="26d63-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="26d63-135">使用发票审核移动工作区审核发票</span><span class="sxs-lookup"><span data-stu-id="26d63-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="26d63-136">在移动设备上，选择**发票审核**工作区。</span><span class="sxs-lookup"><span data-stu-id="26d63-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="26d63-137">通过供应商发票抬头工作流程选择已经分配给您的发票。</span><span class="sxs-lookup"><span data-stu-id="26d63-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="26d63-138">在**发票详细信息**页，查看发票抬头信息，如供应商和日期信息。</span><span class="sxs-lookup"><span data-stu-id="26d63-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="26d63-139">选择发票上的一行以在**发票行明细**视图中查看关于它的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="26d63-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="26d63-140">在**发票行明细**视图中，选择**分配**以查看行分配。</span><span class="sxs-lookup"><span data-stu-id="26d63-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="26d63-141">此处可以查看发票行的核算。</span><span class="sxs-lookup"><span data-stu-id="26d63-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="26d63-142">显示的信息包括财务维度和主科目。</span><span class="sxs-lookup"><span data-stu-id="26d63-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="26d63-143">在**发票详细信息**页，选择**分配**以显示所有分配。</span><span class="sxs-lookup"><span data-stu-id="26d63-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="26d63-144">此处可以查看整个发票的核算。</span><span class="sxs-lookup"><span data-stu-id="26d63-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="26d63-145">显示的信息包括财务维度和主科目。</span><span class="sxs-lookup"><span data-stu-id="26d63-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="26d63-146">选择**附件**以查看附加到发票的所有附注或文件。</span><span class="sxs-lookup"><span data-stu-id="26d63-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="26d63-147">在**发票详细信息**页，选择相应的工作流操作完成您的审核流程。</span><span class="sxs-lookup"><span data-stu-id="26d63-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="26d63-148">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="26d63-148">Select **Done**.</span></span>

