---
title: 向安全角色分配用户
description: 若要访问 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition，用户必须分配给安全角色。
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851351"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="cf824-103">向安全角色分配用户</span><span class="sxs-lookup"><span data-stu-id="cf824-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf824-104">若要访问 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition，用户必须分配给安全角色。</span><span class="sxs-lookup"><span data-stu-id="cf824-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="cf824-105">此过程说明系统管理员如何基于业务数据将用户自动分配到角色。</span><span class="sxs-lookup"><span data-stu-id="cf824-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="cf824-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="cf824-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="cf824-107">将用户自动分配到角色</span><span class="sxs-lookup"><span data-stu-id="cf824-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="cf824-108">转到**导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="cf824-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="cf824-109">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="cf824-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="cf824-110">选择要为其配置规则的角色。</span><span class="sxs-lookup"><span data-stu-id="cf824-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="cf824-111">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="cf824-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="cf824-112">单击**添加规则**打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cf824-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="cf824-113">在**选择查询**列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf824-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="cf824-114">选择要用于此规则的查询。</span><span class="sxs-lookup"><span data-stu-id="cf824-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="cf824-115">在**成员资格规则名称**列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cf824-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cf824-116">单击**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="cf824-116">Click **Edit query**.</span></span> <span data-ttu-id="cf824-117">编辑查询（根据需要）。</span><span class="sxs-lookup"><span data-stu-id="cf824-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="cf824-118">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="cf824-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="cf824-119">将用户从自动角色分配中排除</span><span class="sxs-lookup"><span data-stu-id="cf824-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="cf824-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf824-120">Close the page.</span></span>
2. <span data-ttu-id="cf824-121">转到**导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。</span><span class="sxs-lookup"><span data-stu-id="cf824-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="cf824-122">在树结构中，选择“会计主管”。</span><span class="sxs-lookup"><span data-stu-id="cf824-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="cf824-123">选择一个角色。</span><span class="sxs-lookup"><span data-stu-id="cf824-123">Select a role.</span></span> <span data-ttu-id="cf824-124">在此示例中，选择会计主管。</span><span class="sxs-lookup"><span data-stu-id="cf824-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="cf824-125">在**分配到角色的用户**菜单中，选择**手动分配/排除用户**。</span><span class="sxs-lookup"><span data-stu-id="cf824-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="cf824-126">在**将用户分配到角色或从角色中排除用户** 列表中，标记所选行。</span><span class="sxs-lookup"><span data-stu-id="cf824-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="cf824-127">选择用户。</span><span class="sxs-lookup"><span data-stu-id="cf824-127">Select a user.</span></span>  
6. <span data-ttu-id="cf824-128">在**操作窗格**中，选择**从角色中排除**。</span><span class="sxs-lookup"><span data-stu-id="cf824-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="cf824-129">单击**从角色中排除**从角色中排除所选用户。</span><span class="sxs-lookup"><span data-stu-id="cf824-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="cf824-130">若要删除排除，选择要删除排除的用户，然后单击**重置状态**。</span><span class="sxs-lookup"><span data-stu-id="cf824-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="cf824-131">在您通过重置用户状态删除排除时，用户角色自动重新分配。</span><span class="sxs-lookup"><span data-stu-id="cf824-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="cf824-132">但是，用户不立即分配给角色或在重置状态时从角色中排除。</span><span class="sxs-lookup"><span data-stu-id="cf824-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="cf824-133">相反，用户在下一次运行自动角色分配规则时分配给角色或从角色中删除。</span><span class="sxs-lookup"><span data-stu-id="cf824-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
