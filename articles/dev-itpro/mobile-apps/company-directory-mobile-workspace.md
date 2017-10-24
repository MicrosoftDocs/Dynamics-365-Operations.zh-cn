---
title: "公司目录移动电话工作区"
description: "此主题提供有关公司目录移动工作区的信息，此工作区让用户能够查看和联系其组织中的其他员工。"
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Talent, Operations, UnifiedOperations
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 6a08be4608d131967eec00fc0d6d0e606a2f9f53
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="49f64-103">公司目录移动电话工作区</span><span class="sxs-lookup"><span data-stu-id="49f64-103">Company directory mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="49f64-104">此主题提供有关**公司目录**移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="49f64-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="49f64-105">此工作区让用户能够查看和联系其组织中的其他员工。</span><span class="sxs-lookup"><span data-stu-id="49f64-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="49f64-106">将此工作区可与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。</span><span class="sxs-lookup"><span data-stu-id="49f64-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="49f64-107">概览</span><span class="sxs-lookup"><span data-stu-id="49f64-107">Overview</span></span>
<span data-ttu-id="49f64-108">**公司目录**移动工作区让用户能够执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="49f64-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="49f64-109">查看组织中的员工列表。</span><span class="sxs-lookup"><span data-stu-id="49f64-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="49f64-110">搜索组织中的员工。</span><span class="sxs-lookup"><span data-stu-id="49f64-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="49f64-111">查看员工的联系信息。</span><span class="sxs-lookup"><span data-stu-id="49f64-111">View contact information for employees.</span></span>
- <span data-ttu-id="49f64-112">从模板信息联系员工。</span><span class="sxs-lookup"><span data-stu-id="49f64-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="49f64-113">必备项</span><span class="sxs-lookup"><span data-stu-id="49f64-113">Prerequisites</span></span>
<span data-ttu-id="49f64-114">在使用此移动工作区之前，必须满足以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="49f64-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="49f64-115">必备项</span><span class="sxs-lookup"><span data-stu-id="49f64-115">Prerequisite</span></span></th>
<th><span data-ttu-id="49f64-116">角色</span><span class="sxs-lookup"><span data-stu-id="49f64-116">Role</span></span></th>
<th><span data-ttu-id="49f64-117">说明</span><span class="sxs-lookup"><span data-stu-id="49f64-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49f64-118">必须在您的组织中部署以下产品之一：</span><span class="sxs-lookup"><span data-stu-id="49f64-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="49f64-119">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="49f64-119">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span></li>
<li><span data-ttu-id="49f64-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="49f64-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="49f64-121">系统管理员</span><span class="sxs-lookup"><span data-stu-id="49f64-121">System administrator</span></span></td>
<td><span data-ttu-id="49f64-122">如果您的组织中没有部署 Finance and Operations，请查阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</span><span class="sxs-lookup"><span data-stu-id="49f64-122">If you don't already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="49f64-123">如果您已经在您的组织中部署人才，系统管理员可以从<a href="https://www.microsoft.com/en-us/dynamics365/talent">人才网页</a>访问试用版本。</span><span class="sxs-lookup"><span data-stu-id="49f64-123">If you don't already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="49f64-124">必须发布<strong>公司目录</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="49f64-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="49f64-125">系统管理员</span><span class="sxs-lookup"><span data-stu-id="49f64-125">System administrator</span></span></td>
<td><span data-ttu-id="49f64-126">请查阅<a href="publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="49f64-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="49f64-127">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="49f64-127">Download and install the mobile app</span></span>
<span data-ttu-id="49f64-128">下载并安装 Dynamics 365 for Unified Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="49f64-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="49f64-129">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="49f64-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="49f64-130">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="49f64-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="49f64-131">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="49f64-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="49f64-132">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="49f64-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="49f64-133">输入您的 Microsoft Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="49f64-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="49f64-134">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="49f64-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="49f64-135">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="49f64-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="49f64-136">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="49f64-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="49f64-137">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="49f64-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="49f64-138">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="49f64-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="49f64-139">使用移动工作区查看公司目录</span><span class="sxs-lookup"><span data-stu-id="49f64-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="49f64-140">在移动应用中，选择**公司目录**工作区。</span><span class="sxs-lookup"><span data-stu-id="49f64-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="49f64-141">此时将显示员工列表。</span><span class="sxs-lookup"><span data-stu-id="49f64-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="49f64-142">选择某一员工。</span><span class="sxs-lookup"><span data-stu-id="49f64-142">Select an employee.</span></span> <span data-ttu-id="49f64-143">此时将显示**员工模板**页。</span><span class="sxs-lookup"><span data-stu-id="49f64-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="49f64-144">此页上的信息包括员工的名字、姓氏、职务和部门。</span><span class="sxs-lookup"><span data-stu-id="49f64-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="49f64-145">使用移动工作区搜索公司目录</span><span class="sxs-lookup"><span data-stu-id="49f64-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="49f64-146">在移动应用中，选择**公司目录**工作区。</span><span class="sxs-lookup"><span data-stu-id="49f64-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="49f64-147">在**搜索**字段中，输入员工的名字、姓氏、职务或部门开始搜索。</span><span class="sxs-lookup"><span data-stu-id="49f64-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="49f64-148">选择某一员工。</span><span class="sxs-lookup"><span data-stu-id="49f64-148">Select an employee.</span></span> <span data-ttu-id="49f64-149">此时将显示**员工模板**页。</span><span class="sxs-lookup"><span data-stu-id="49f64-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="49f64-150">此页上的信息包括员工的名字、姓氏、职务和部门。</span><span class="sxs-lookup"><span data-stu-id="49f64-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
