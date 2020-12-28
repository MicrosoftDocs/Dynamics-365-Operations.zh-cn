---
title: Attract 用户无法通过求职门户申请职位
description: 本主题介绍如何解决 Attract 用户无法通过求职门户申请职位的问题。
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460414"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="2540f-103">Attract 用户无法通过求职门户申请职位</span><span class="sxs-lookup"><span data-stu-id="2540f-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="2540f-104">签发</span><span class="sxs-lookup"><span data-stu-id="2540f-104">Issue</span></span>

<span data-ttu-id="2540f-105">Attract 用户无法通过求职门户申请职位。</span><span class="sxs-lookup"><span data-stu-id="2540f-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="2540f-106">当他们尝试申请在 Dynamics 365 Talent: Attract 中创建的职位时，浏览器将持续加载页面，并且无法完成操作。</span><span class="sxs-lookup"><span data-stu-id="2540f-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="2540f-107">原因</span><span class="sxs-lookup"><span data-stu-id="2540f-107">Cause</span></span>

<span data-ttu-id="2540f-108">当 Talent 关系团队没有 Talent 用户角色时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="2540f-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="2540f-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="2540f-109">Resolution</span></span>

<span data-ttu-id="2540f-110">将 Talent 用户角色分配给 Talent 关系团队。</span><span class="sxs-lookup"><span data-stu-id="2540f-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="2540f-111">使用以下任何管理员凭据登录到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)：</span><span class="sxs-lookup"><span data-stu-id="2540f-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="2540f-112">Dynamics 365 管理员</span><span class="sxs-lookup"><span data-stu-id="2540f-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="2540f-113">全局管理员</span><span class="sxs-lookup"><span data-stu-id="2540f-113">Global admin</span></span>
   - <span data-ttu-id="2540f-114">Power Platform 管理员</span><span class="sxs-lookup"><span data-stu-id="2540f-114">Power Platform admin</span></span>

2. <span data-ttu-id="2540f-115">在导航窗格中，选择 **环境**，然后选择要在其中将 Talent 用户角色分配给 Talent 关系团队的环境。</span><span class="sxs-lookup"><span data-stu-id="2540f-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![选择环境](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="2540f-117">在 **环境** 窗格中，选择 **环境 URL**，然后登录到环境的管理门户（例如 https:<orgname>.crm.dynamics.com）。</span><span class="sxs-lookup"><span data-stu-id="2540f-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="2540f-118">选择 **设置**，选择 **系统**，然后选择 **安全性**。</span><span class="sxs-lookup"><span data-stu-id="2540f-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![导航到安全性](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="2540f-120">选择 **团队**。</span><span class="sxs-lookup"><span data-stu-id="2540f-120">Select **Teams**.</span></span>

   ![选择团队](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="2540f-122">在搜索框中搜索 **Talent 关系团队**，然后从搜索结果中选择团队。</span><span class="sxs-lookup"><span data-stu-id="2540f-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="2540f-123">从功能区中选择 **管理角色**。</span><span class="sxs-lookup"><span data-stu-id="2540f-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="2540f-124">在 **管理团队角色** 对话框中，从可用角色列表中选择 **Talent 用户**，然后选择 **确定** 以应用角色。</span><span class="sxs-lookup"><span data-stu-id="2540f-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![应用角色](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="2540f-126">测试您的更改：</span><span class="sxs-lookup"><span data-stu-id="2540f-126">Test your changes:</span></span>

   1. <span data-ttu-id="2540f-127">从新的浏览器窗口登录到求职门户。</span><span class="sxs-lookup"><span data-stu-id="2540f-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="2540f-128">通过求职门户申请职位。</span><span class="sxs-lookup"><span data-stu-id="2540f-128">Apply for the job from the career portal.</span></span> 