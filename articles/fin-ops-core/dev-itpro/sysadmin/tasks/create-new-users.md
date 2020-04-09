---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143555"
---
# <a name="create-new-users"></a><span data-ttu-id="bbf59-103">创建新用户</span><span class="sxs-lookup"><span data-stu-id="bbf59-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbf59-104">用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。</span><span class="sxs-lookup"><span data-stu-id="bbf59-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="bbf59-105">将用户与许可证相关联（仅适用于新许可证类型）</span><span class="sxs-lookup"><span data-stu-id="bbf59-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="bbf59-106">对于具有 2019 年 10 月添加的新许可证类型之一的客户，用户必须与许可证相关联。</span><span class="sxs-lookup"><span data-stu-id="bbf59-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="bbf59-107">与许可证相关联的用户会在第一次登录时自动添加为没有角色的系统用户。</span><span class="sxs-lookup"><span data-stu-id="bbf59-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="bbf59-108">系统管理员可以在 [Microsoft 365 管理中心](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="bbf59-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="bbf59-109">将外部用户与许可证相关联（仅适用于新许可证类型）</span><span class="sxs-lookup"><span data-stu-id="bbf59-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="bbf59-110">需要在托管租户目录中表示环境所部署到的租户外部的用户 (Azure Active Directory (Azure AD))，以便可以为其分配许可证。</span><span class="sxs-lookup"><span data-stu-id="bbf59-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="bbf59-111">应将这些外部用户作为来宾用户添加到 Azure AD 内的租户中，然后为其分配适当的许可证。</span><span class="sxs-lookup"><span data-stu-id="bbf59-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="bbf59-112">有关更多信息，请参见[在 Azure 门户中添加 Azure Active Directory B2B 协作用户](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)。</span><span class="sxs-lookup"><span data-stu-id="bbf59-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="bbf59-113">添加新用户</span><span class="sxs-lookup"><span data-stu-id="bbf59-113">Add a new user</span></span>
1. <span data-ttu-id="bbf59-114">转到**系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="bbf59-115">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="bbf59-116">在**用户 ID** 字段中，输入用户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="bbf59-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="bbf59-117">用户 ID 是必填项。</span><span class="sxs-lookup"><span data-stu-id="bbf59-117">A user ID is required.</span></span>  
4. <span data-ttu-id="bbf59-118">在**用户名称**字段中，输入用户的名称。</span><span class="sxs-lookup"><span data-stu-id="bbf59-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="bbf59-119">在**域**字段中，输入用户的域。</span><span class="sxs-lookup"><span data-stu-id="bbf59-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="bbf59-120">在**别名**字段，输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="bbf59-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="bbf59-121">在**公司**字段中，选择所需公司。</span><span class="sxs-lookup"><span data-stu-id="bbf59-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="bbf59-122">在**用户的角色**快速选项卡中，选择**分配角色**向用户分配安全角色。</span><span class="sxs-lookup"><span data-stu-id="bbf59-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="bbf59-123">有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf59-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="bbf59-124">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-124">Select **OK**.</span></span>
10. <span data-ttu-id="bbf59-125">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="bbf59-126">导入用户</span><span class="sxs-lookup"><span data-stu-id="bbf59-126">Import users</span></span>
1. <span data-ttu-id="bbf59-127">在操作窗格上，选择**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-127">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="bbf59-128">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="bbf59-128">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bbf59-129">选择**导入用户**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-129">Select **Import users**.</span></span>
4. <span data-ttu-id="bbf59-130">选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="bbf59-130">Select **Close**.</span></span>

