---
title: 发票审核移动工作区
description: 此主题提供有关发票审核移动工作区的信息。
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c3414d6ef5f2df62f37f1ef2e7e2ff43ce040e5e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752242"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="d07d9-103">发票审核移动工作区</span><span class="sxs-lookup"><span data-stu-id="d07d9-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d07d9-104">此主题提供有关 **发票审核** 移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="d07d9-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="d07d9-105">此工作区提供通过供应商发票抬头工作流程分配给您的发票的列表。</span><span class="sxs-lookup"><span data-stu-id="d07d9-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="d07d9-106">此工作区应该与 Finance and Operations 移动应用结合使用。</span><span class="sxs-lookup"><span data-stu-id="d07d9-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d07d9-107">概览</span><span class="sxs-lookup"><span data-stu-id="d07d9-107">Overview</span></span>

<span data-ttu-id="d07d9-108">**发票审核** 移动工作区让应付帐款职员和经理能够查看已作为供应商发票抬头工作流程的一部分分配给他们的发票。</span><span class="sxs-lookup"><span data-stu-id="d07d9-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="d07d9-109">您可以查看发票信息，甚至还可以查看行和分配详细信息，以帮助您做出合理的审核决定。</span><span class="sxs-lookup"><span data-stu-id="d07d9-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="d07d9-110">从工作区可以执行操作以通过工作流程移动发票。</span><span class="sxs-lookup"><span data-stu-id="d07d9-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d07d9-111">必备项</span><span class="sxs-lookup"><span data-stu-id="d07d9-111">Prerequisites</span></span>

<span data-ttu-id="d07d9-112">在使用此移动工作区之前，必须满足以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="d07d9-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d07d9-113">必备项</span><span class="sxs-lookup"><span data-stu-id="d07d9-113">Prerequisite</span></span></th>
<th><span data-ttu-id="d07d9-114">角色</span><span class="sxs-lookup"><span data-stu-id="d07d9-114">Role</span></span></th>
<th><span data-ttu-id="d07d9-115">说明</span><span class="sxs-lookup"><span data-stu-id="d07d9-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d07d9-116">必须在您的组织中部署 Microsoft Dynamics 365 Finance。</span><span class="sxs-lookup"><span data-stu-id="d07d9-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="d07d9-117">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d07d9-117">System administrator</span></span></td>
<td><span data-ttu-id="d07d9-118">请查阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="d07d9-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d07d9-119">必须发布<strong>发票审核</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="d07d9-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="d07d9-120">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d07d9-120">System administrator</span></span></td>
<td><span data-ttu-id="d07d9-121">请查阅<a href="publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="d07d9-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d07d9-122">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="d07d9-122">Download and install the mobile app</span></span>

<span data-ttu-id="d07d9-123">下载并安装 Finance and Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="d07d9-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="d07d9-124">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="d07d9-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d07d9-125">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="d07d9-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d07d9-126">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="d07d9-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="d07d9-127">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="d07d9-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d07d9-128">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="d07d9-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d07d9-129">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="d07d9-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d07d9-130">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="d07d9-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="d07d9-131">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="d07d9-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d07d9-132">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="d07d9-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="d07d9-133">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d07d9-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="d07d9-134">使用发票审核移动工作区审核发票</span><span class="sxs-lookup"><span data-stu-id="d07d9-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="d07d9-135">在移动设备上，选择 **发票审核** 工作区。</span><span class="sxs-lookup"><span data-stu-id="d07d9-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="d07d9-136">通过供应商发票抬头工作流程选择已经分配给您的发票。</span><span class="sxs-lookup"><span data-stu-id="d07d9-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="d07d9-137">在 **发票详细信息** 页，查看发票抬头信息，如供应商和日期信息。</span><span class="sxs-lookup"><span data-stu-id="d07d9-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="d07d9-138">选择发票上的一行以在 **发票行明细** 视图中查看关于它的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="d07d9-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="d07d9-139">在 **发票行明细** 视图中，选择 **分配** 以查看行分配。</span><span class="sxs-lookup"><span data-stu-id="d07d9-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="d07d9-140">此处可以查看发票行的核算。</span><span class="sxs-lookup"><span data-stu-id="d07d9-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="d07d9-141">显示的信息包括财务维度和主科目。</span><span class="sxs-lookup"><span data-stu-id="d07d9-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="d07d9-142">在 **发票详细信息** 页，选择 **分配** 以显示所有分配。</span><span class="sxs-lookup"><span data-stu-id="d07d9-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="d07d9-143">此处可以查看整个发票的核算。</span><span class="sxs-lookup"><span data-stu-id="d07d9-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="d07d9-144">显示的信息包括财务维度和主科目。</span><span class="sxs-lookup"><span data-stu-id="d07d9-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="d07d9-145">选择 **附件** 以查看附加到发票的所有附注或文件。</span><span class="sxs-lookup"><span data-stu-id="d07d9-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="d07d9-146">在 **发票详细信息** 页，选择相应的工作流操作完成您的审核流程。</span><span class="sxs-lookup"><span data-stu-id="d07d9-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="d07d9-147">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="d07d9-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]