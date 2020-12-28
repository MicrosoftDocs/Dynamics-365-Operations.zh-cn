---
title: 我的团队移动工作区
description: 此主题提供关于我的团队移动工作区的信息，此工作区允许经理查看其直接下属和扩展职员。 用户还可以向其报告链中的人员发送表扬。
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6ac3bf0a6ce20866f749b0c14030b70770e5589c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680962"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="da0c1-104">我的团队移动工作区</span><span class="sxs-lookup"><span data-stu-id="da0c1-104">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da0c1-105">此主题提供有关 **我的团队** 移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="da0c1-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="da0c1-106">此工作区允许经理查看其直接下属和扩展职员。</span><span class="sxs-lookup"><span data-stu-id="da0c1-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="da0c1-107">他们还可以向其报告链中的人员发送表扬。</span><span class="sxs-lookup"><span data-stu-id="da0c1-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="da0c1-108">此工作区应该与 Finance and Operations 移动应用结合使用。</span><span class="sxs-lookup"><span data-stu-id="da0c1-108">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="da0c1-109">概览</span><span class="sxs-lookup"><span data-stu-id="da0c1-109">Overview</span></span> 
<span data-ttu-id="da0c1-110">**我的团队** 移动工作区让经理能够执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="da0c1-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="da0c1-111">显示经理的直接下属的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="da0c1-112">显示经理的扩展报告团队的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="da0c1-113">查看每个团队成员的详细信息，例如出生日期、受聘日期、工作年限以及薪酬和绩效信息。</span><span class="sxs-lookup"><span data-stu-id="da0c1-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="da0c1-114">向经理扩展报告团队中的任何人员发送表扬。</span><span class="sxs-lookup"><span data-stu-id="da0c1-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="da0c1-115">必备项</span><span class="sxs-lookup"><span data-stu-id="da0c1-115">Prerequisites</span></span>
<span data-ttu-id="da0c1-116">在使用此移动工作区之前，必须满足以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="da0c1-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="da0c1-117">必备项</span><span class="sxs-lookup"><span data-stu-id="da0c1-117">Prerequisite</span></span></th>
<th><span data-ttu-id="da0c1-118">角色</span><span class="sxs-lookup"><span data-stu-id="da0c1-118">Role</span></span></th>
<th><span data-ttu-id="da0c1-119">说明</span><span class="sxs-lookup"><span data-stu-id="da0c1-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da0c1-120">必须在您的组织中部署以下产品之一：</span><span class="sxs-lookup"><span data-stu-id="da0c1-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="da0c1-121">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="da0c1-121">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="da0c1-122">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="da0c1-122">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="da0c1-123">系统管理员</span><span class="sxs-lookup"><span data-stu-id="da0c1-123">System administrator</span></span></td>
<td><span data-ttu-id="da0c1-124">如果您的组织中还没有部署 Finance and Operations 应用，请参阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="da0c1-124">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="da0c1-125">如果组织中尚未部署 Human Resources，系统管理员可从 <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources 网页</a>访问试用版。</span><span class="sxs-lookup"><span data-stu-id="da0c1-125">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="da0c1-126">必须发布<strong>我的团队</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="da0c1-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="da0c1-127">系统管理员</span><span class="sxs-lookup"><span data-stu-id="da0c1-127">System administrator</span></span></td>
<td><span data-ttu-id="da0c1-128">请查阅<a href="publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="da0c1-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="da0c1-129">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="da0c1-129">Download and install the mobile app</span></span>

<span data-ttu-id="da0c1-130">下载并安装 Finance and Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="da0c1-130">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="da0c1-131">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="da0c1-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="da0c1-132">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="da0c1-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="da0c1-133">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="da0c1-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="da0c1-134">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="da0c1-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="da0c1-135">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="da0c1-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="da0c1-136">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="da0c1-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="da0c1-137">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="da0c1-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="da0c1-138">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="da0c1-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="da0c1-139">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="da0c1-140">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="da0c1-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="da0c1-141">使用我的团队移动工作区查看团队成员</span><span class="sxs-lookup"><span data-stu-id="da0c1-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="da0c1-142">在移动应用中，选择 **我的团队** 工作区。</span><span class="sxs-lookup"><span data-stu-id="da0c1-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="da0c1-143">此时将显示团队成员的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-143">A list of team members is shown.</span></span> <span data-ttu-id="da0c1-144">此列表还显示每个团队成员的职务及其拥有的任何直接下属。</span><span class="sxs-lookup"><span data-stu-id="da0c1-144">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="da0c1-145">选择一个团队成员。</span><span class="sxs-lookup"><span data-stu-id="da0c1-145">Select a team member.</span></span> <span data-ttu-id="da0c1-146">此时将显示 **团队成员汇总** 页。</span><span class="sxs-lookup"><span data-stu-id="da0c1-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="da0c1-147">此页上的信息包括团队成员的出生日期、受聘日期、工作年限、当前职务工作年限以及薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="da0c1-147">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="da0c1-148">使用我的团队移动工作区查看扩展团队成员</span><span class="sxs-lookup"><span data-stu-id="da0c1-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="da0c1-149">在移动应用中，选择 **我的团队** 工作区。</span><span class="sxs-lookup"><span data-stu-id="da0c1-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="da0c1-150">此时将显示团队成员的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-150">A list of team members is shown.</span></span> <span data-ttu-id="da0c1-151">此列表还显示每个团队成员的职务及其拥有的任何直接下属。</span><span class="sxs-lookup"><span data-stu-id="da0c1-151">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="da0c1-152">选择 **直接下属** 链接。</span><span class="sxs-lookup"><span data-stu-id="da0c1-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="da0c1-153">此时将显示您的扩展团队的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="da0c1-154">选择一个团队成员。</span><span class="sxs-lookup"><span data-stu-id="da0c1-154">Select a team member.</span></span> <span data-ttu-id="da0c1-155">此时将显示 **团队成员汇总** 页。</span><span class="sxs-lookup"><span data-stu-id="da0c1-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="da0c1-156">此页上的信息包括团队成员的出生日期、受聘日期、工作年限、当前职务工作年限以及薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="da0c1-156">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="da0c1-157">使用我的团队移动工作区发送团队成员表扬</span><span class="sxs-lookup"><span data-stu-id="da0c1-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="da0c1-158">在移动应用中，选择 **我的团队** 工作区。</span><span class="sxs-lookup"><span data-stu-id="da0c1-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="da0c1-159">此时将显示团队成员的列表。</span><span class="sxs-lookup"><span data-stu-id="da0c1-159">A list of team members is shown.</span></span> <span data-ttu-id="da0c1-160">此列表还显示每个团队成员的职务及其拥有的任何直接下属。</span><span class="sxs-lookup"><span data-stu-id="da0c1-160">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="da0c1-161">选择一个团队成员。</span><span class="sxs-lookup"><span data-stu-id="da0c1-161">Select a team member.</span></span> <span data-ttu-id="da0c1-162">此时将显示 **团队成员汇总** 页。</span><span class="sxs-lookup"><span data-stu-id="da0c1-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="da0c1-163">选择 **发送表扬**。</span><span class="sxs-lookup"><span data-stu-id="da0c1-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="da0c1-164">输入您要发送的表扬的文本。</span><span class="sxs-lookup"><span data-stu-id="da0c1-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="da0c1-165">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="da0c1-165">Select **Done**.</span></span>
