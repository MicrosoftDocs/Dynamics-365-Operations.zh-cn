---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570513"
---
# <a name="create-new-users"></a><span data-ttu-id="da083-103">创建新用户</span><span class="sxs-lookup"><span data-stu-id="da083-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da083-104">用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。</span><span class="sxs-lookup"><span data-stu-id="da083-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="da083-105">将用户与许可证相关联（仅适用于新许可证类型）</span><span class="sxs-lookup"><span data-stu-id="da083-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="da083-106">对于具有 2019 年 10 月添加的新许可证类型之一的客户，用户必须与许可证相关联。</span><span class="sxs-lookup"><span data-stu-id="da083-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="da083-107">与许可证相关联的用户会在第一次登录时自动添加为没有角色的系统用户。</span><span class="sxs-lookup"><span data-stu-id="da083-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="da083-108">未与许可证关联的用户会收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="da083-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="da083-109">系统管理员可以在 [Microsoft 365 管理中心](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="da083-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="da083-110">添加新用户</span><span class="sxs-lookup"><span data-stu-id="da083-110">Add a new user</span></span>
1. <span data-ttu-id="da083-111">转到**系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="da083-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="da083-112">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="da083-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="da083-113">在**用户 ID** 字段中，输入用户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="da083-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="da083-114">用户 ID 是必填项。</span><span class="sxs-lookup"><span data-stu-id="da083-114">A user ID is required.</span></span>  
4. <span data-ttu-id="da083-115">在**用户名称**字段中，输入用户的名称。</span><span class="sxs-lookup"><span data-stu-id="da083-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="da083-116">在**域**字段中，输入用户的域。</span><span class="sxs-lookup"><span data-stu-id="da083-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="da083-117">在**别名**字段，输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="da083-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="da083-118">在**公司**字段中，选择所需公司。</span><span class="sxs-lookup"><span data-stu-id="da083-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="da083-119">在**用户的角色**快速选项卡中，选择**分配角色**[向用户分配安全角色](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="da083-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="da083-120">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="da083-120">Select **OK**.</span></span>
10. <span data-ttu-id="da083-121">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="da083-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="da083-122">导入用户</span><span class="sxs-lookup"><span data-stu-id="da083-122">Import users</span></span>
1. <span data-ttu-id="da083-123">在操作窗格上，选择**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="da083-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="da083-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="da083-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="da083-125">选择**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="da083-125">Select **Import users**.</span></span>
4. <span data-ttu-id="da083-126">选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="da083-126">Select **Close**.</span></span>

