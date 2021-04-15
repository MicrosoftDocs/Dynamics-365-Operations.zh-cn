---
title: 向安全角色分配用户
description: 若要访问 Finance and Operations 应用，用户必须分配给安全角色。
author: Peakerbl
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745877"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="7ac7e-103">向安全角色分配用户</span><span class="sxs-lookup"><span data-stu-id="7ac7e-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ac7e-104">要使用 Finance and Operations 应用中的常用功能以外的其他功能，必须将用户分配给安全角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-104">To use anything other than common capabilities in Finance and Operations apps, users must be assigned to security roles.</span></span> <span data-ttu-id="7ac7e-105">您可以根据规则和业务数据自动将用户分配给角色，不为用户自动分配角色，也可以手动将用户添加到角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-105">You can assign users to roles automatically, based on rules and business data, exclude users from automatic role assignment, or add users to roles manually.</span></span>

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="7ac7e-106">将用户自动分配到角色</span><span class="sxs-lookup"><span data-stu-id="7ac7e-106">Automatically assign users to roles</span></span>
<span data-ttu-id="7ac7e-107">此过程说明系统管理员如何基于业务数据将用户自动分配到角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-107">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 
1. <span data-ttu-id="7ac7e-108">转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="7ac7e-109">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="7ac7e-110">选择要为其配置规则的角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="7ac7e-111">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="7ac7e-112">选择 **添加规则** 以打开对话框菜单。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-112">Select **Add rule** to open the dialog menu.</span></span>
4. <span data-ttu-id="7ac7e-113">在 **选择查询** 列表中，查找并选择所需的记录。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-113">In the **Select a query** list, find and select the desired record.</span></span> <span data-ttu-id="7ac7e-114">选择要用于此规则的查询。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="7ac7e-115">在 **成员资格规则名称** 列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7ac7e-116">选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-116">Select **Edit query**.</span></span> <span data-ttu-id="7ac7e-117">编辑查询（根据需要）。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="7ac7e-118">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-118">Select **OK**.</span></span>
8. <span data-ttu-id="7ac7e-119">选择 **运行自动角色分配**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-119">Select **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="7ac7e-120">转到 **导航窗格 > 模块 > 系统管理 > 用户 > 用户**（最好在单独的浏览器选项卡中）。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-120">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="7ac7e-121">查看分配给各个用户的角色，以确认角色分配查询是否正确。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-121">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="7ac7e-122">根据需要调整并重新运行。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-122">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="7ac7e-123">将用户从自动角色分配中排除</span><span class="sxs-lookup"><span data-stu-id="7ac7e-123">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="7ac7e-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-124">Close the page.</span></span>
2. <span data-ttu-id="7ac7e-125">转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-125">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="7ac7e-126">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-126">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="7ac7e-127">选择一个角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-127">Select a role.</span></span> <span data-ttu-id="7ac7e-128">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-128">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="7ac7e-129">在 **分配到角色的用户** 菜单中，选择 **手动分配/排除用户**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-129">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="7ac7e-130">在 **将用户分配到角色或从角色中排除用户** 列表中，标记所选行。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-130">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="7ac7e-131">选择用户。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-131">Select a user.</span></span>  
6. <span data-ttu-id="7ac7e-132">在 **操作窗格** 中，选择 **从角色中排除**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-132">On the **Action pane**, select **Exclude from role**.</span></span>
7. <span data-ttu-id="7ac7e-133">选择 **从角色中排除** 以从角色中排除所选用户。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-133">Select **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="7ac7e-134">若要删除排除，选择要删除排除的用户，然后单击 **重置状态**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-134">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="7ac7e-135">通过重置用户状态删除排除项时，将自动分配用户角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-135">When you remove an exclusion by resetting the user's status, the user's role is assigned automatically.</span></span> <span data-ttu-id="7ac7e-136">但是，用户不立即分配给角色或在重置状态时从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-136">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="7ac7e-137">相反，用户在下一次运行自动角色分配规则时分配给角色或从角色中删除。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-137">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

## <a name="manually-assign-users-to-roles"></a><span data-ttu-id="7ac7e-138">手动将用户分配给角色</span><span class="sxs-lookup"><span data-stu-id="7ac7e-138">Manually assign users to roles</span></span>
<span data-ttu-id="7ac7e-139">手动分配给安全角色的用户也必须由管理员手动删除。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-139">Users who are manually assigned to security roles must also be manually removed by the administrator.</span></span> <span data-ttu-id="7ac7e-140">不会通过自动角色分配规则从角色中删除这些用户。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-140">These users are not removed from roles by rules for automatic role assignment.</span></span>

1. <span data-ttu-id="7ac7e-141">转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-141">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="7ac7e-142">在树中，选择一个角色，然后在 **分配给角色的用户** 菜单中，选择 **手动分配/排除用户**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-142">In the tree, select a role, and in the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
4. <span data-ttu-id="7ac7e-143">在 **将用户分配给角色或从角色中排除用户** 中，列出了未分配有角色的用户，并且其 **分配模式** 设置为 **无**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-143">In the **Assign users to or exclude users from role**, users that have not been assigned the role are listed with the **Assignment mode** set to **None**.</span></span> <span data-ttu-id="7ac7e-144">选择一个或多个应该为其分配角色的用户。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-144">Select one or more users that should be assigned the role.</span></span>
5. <span data-ttu-id="7ac7e-145">在 **操作窗格** 上，选择 **分配给角色**。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-145">On the **Action pane**, select **Assign to role**.</span></span> <span data-ttu-id="7ac7e-146">**分配模式** 会更新为 **手动**，并且现在为用户分配了新角色。</span><span class="sxs-lookup"><span data-stu-id="7ac7e-146">The **Assignment mode** is updated to **Manual** and the users now have a new role assigned.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]