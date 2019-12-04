---
title: 向安全角色分配用户
description: 若要访问 Finance and Operations 应用，必须为用户分配安全角色。
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807988"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="ae753-103">向安全角色分配用户</span><span class="sxs-lookup"><span data-stu-id="ae753-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae753-104">要使用除常用功能以外的任何功能，必须将用户分配到安全角色。</span><span class="sxs-lookup"><span data-stu-id="ae753-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="ae753-105">此过程说明系统管理员如何基于业务数据将用户自动分配到角色。</span><span class="sxs-lookup"><span data-stu-id="ae753-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="ae753-106">将用户自动分配到角色</span><span class="sxs-lookup"><span data-stu-id="ae753-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="ae753-107">转到**导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="ae753-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="ae753-108">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="ae753-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="ae753-109">选择要为其配置规则的角色。</span><span class="sxs-lookup"><span data-stu-id="ae753-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="ae753-110">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="ae753-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="ae753-111">单击**添加规则**打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ae753-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="ae753-112">在**选择查询**列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ae753-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="ae753-113">选择要用于此规则的查询。</span><span class="sxs-lookup"><span data-stu-id="ae753-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="ae753-114">在**成员资格规则名称**列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ae753-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ae753-115">单击**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="ae753-115">Click **Edit query**.</span></span> <span data-ttu-id="ae753-116">编辑查询（根据需要）。</span><span class="sxs-lookup"><span data-stu-id="ae753-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="ae753-117">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ae753-117">Click **OK**.</span></span>
8. <span data-ttu-id="ae753-118">单击**运行自动角色分配**。</span><span class="sxs-lookup"><span data-stu-id="ae753-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="ae753-119">转到**导航窗格 > 模块 > 系统管理 > 用户 > 用户**（最好在单独的浏览器选项卡中）。</span><span class="sxs-lookup"><span data-stu-id="ae753-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="ae753-120">查看分配给各个用户的角色，以确认角色分配查询是否正确。</span><span class="sxs-lookup"><span data-stu-id="ae753-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="ae753-121">根据需要调整并重新运行。</span><span class="sxs-lookup"><span data-stu-id="ae753-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="ae753-122">将用户从自动角色分配中排除</span><span class="sxs-lookup"><span data-stu-id="ae753-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="ae753-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ae753-123">Close the page.</span></span>
2. <span data-ttu-id="ae753-124">转到**导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="ae753-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="ae753-125">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="ae753-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="ae753-126">选择一个角色。</span><span class="sxs-lookup"><span data-stu-id="ae753-126">Select a role.</span></span> <span data-ttu-id="ae753-127">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="ae753-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="ae753-128">在**分配到角色的用户**菜单中，选择**手动分配/排除用户**。</span><span class="sxs-lookup"><span data-stu-id="ae753-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="ae753-129">在**将用户分配到角色或从角色中排除用户** 列表中，标记所选行。</span><span class="sxs-lookup"><span data-stu-id="ae753-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="ae753-130">选择用户。</span><span class="sxs-lookup"><span data-stu-id="ae753-130">Select a user.</span></span>  
6. <span data-ttu-id="ae753-131">在**操作窗格**中，选择**从角色中排除**。</span><span class="sxs-lookup"><span data-stu-id="ae753-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="ae753-132">单击**从角色中排除**从角色中排除所选用户。</span><span class="sxs-lookup"><span data-stu-id="ae753-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="ae753-133">若要删除排除，选择要删除排除的用户，然后单击**重置状态**。</span><span class="sxs-lookup"><span data-stu-id="ae753-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="ae753-134">在您通过重置用户状态删除排除时，用户角色自动重新分配。</span><span class="sxs-lookup"><span data-stu-id="ae753-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="ae753-135">但是，用户不立即分配给角色或在重置状态时从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="ae753-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="ae753-136">相反，用户在下一次运行自动角色分配规则时分配给角色或从角色中删除。</span><span class="sxs-lookup"><span data-stu-id="ae753-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
