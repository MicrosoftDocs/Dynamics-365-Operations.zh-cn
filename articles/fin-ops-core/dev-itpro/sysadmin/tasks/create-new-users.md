---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b994473b4535c255f87551a6d97e197516fc2a9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745829"
---
# <a name="create-new-users"></a><span data-ttu-id="40054-103">创建新用户</span><span class="sxs-lookup"><span data-stu-id="40054-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40054-104">您必须先被添加到 **用户** 页（**系统管理 \> 用户 \> 用户**），然后才能访问 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="40054-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="40054-105">用户包括您组织的内部员工，或外部客户和供应商。</span><span class="sxs-lookup"><span data-stu-id="40054-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="40054-106">用户可以手动导入或添加。</span><span class="sxs-lookup"><span data-stu-id="40054-106">Users can be imported or added manually.</span></span> <span data-ttu-id="40054-107">所有用户都必须获得正确的许可才符合使用要求。</span><span class="sxs-lookup"><span data-stu-id="40054-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="40054-108">有关如何购买 Finance and Operations 应用和获得许可的信息，请参阅 [Microsoft Dynamics 365 许可指南](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)。</span><span class="sxs-lookup"><span data-stu-id="40054-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="40054-109">向用户分配许可证</span><span class="sxs-lookup"><span data-stu-id="40054-109">Assign a license to a user</span></span>
<span data-ttu-id="40054-110">系统管理员可以在 [Microsoft 365 管理中心](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="40054-110">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="40054-111">在 Azure AD 中添加外部用户并分配许可证</span><span class="sxs-lookup"><span data-stu-id="40054-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="40054-112">外部用户必须在您的租户目录 (Azure Active Directory (Azure AD)) 中出现，才可以为他们分配许可证。</span><span class="sxs-lookup"><span data-stu-id="40054-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="40054-113">应将这些外部用户作为来宾用户添加到 Azure AD 内的租户中，然后为其分配适当的许可证。</span><span class="sxs-lookup"><span data-stu-id="40054-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="40054-114">Finance and Operations 应用的要求是，来宾用户的公司必须使用 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="40054-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="40054-115">有关更多信息，请参见[在 Azure 门户中添加 Azure Active Directory B2B 协作用户](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)。</span><span class="sxs-lookup"><span data-stu-id="40054-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="40054-116">从 Azure AD 导入新用户</span><span class="sxs-lookup"><span data-stu-id="40054-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="40054-117">转到 **系统管理** \> **用户** \> **用户**。</span><span class="sxs-lookup"><span data-stu-id="40054-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="40054-118">在操作窗格上，选择 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="40054-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="40054-119">选择要导入的用户。</span><span class="sxs-lookup"><span data-stu-id="40054-119">Select the users to be imported.</span></span> <span data-ttu-id="40054-120">列表中包括当前不是此环境中的用户的 Azure AD 用户。</span><span class="sxs-lookup"><span data-stu-id="40054-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="40054-121">选择 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="40054-121">Select **Import users**.</span></span>
5. <span data-ttu-id="40054-122">选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="40054-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="40054-123">**公司** 字段的值将根据管理员的当前会话公司设置。导入之后，您必须根据需要分配角色和组织。</span><span class="sxs-lookup"><span data-stu-id="40054-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="40054-124">有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="40054-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="40054-125">有条件地，可能还需要将用户与 **人员** 关联，并更新用户选项（如语言）。</span><span class="sxs-lookup"><span data-stu-id="40054-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="40054-126">手动添加新用户</span><span class="sxs-lookup"><span data-stu-id="40054-126">Manually add a new user</span></span>
1. <span data-ttu-id="40054-127">转到 **系统管理** \> **用户** \> **用户**。</span><span class="sxs-lookup"><span data-stu-id="40054-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="40054-128">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="40054-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="40054-129">在 **用户 ID** 字段中，输入用户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="40054-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="40054-130">在 **用户名称** 字段中，输入用户的名称。</span><span class="sxs-lookup"><span data-stu-id="40054-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="40054-131">在 **提供者** 字段中：</span><span class="sxs-lookup"><span data-stu-id="40054-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="40054-132">对于内部用户，使用默认值。</span><span class="sxs-lookup"><span data-stu-id="40054-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="40054-133">例如，您的以 https://sts.windows.net/ 为前缀的 Azure AD 租户。</span><span class="sxs-lookup"><span data-stu-id="40054-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="40054-134">对于非 Azure AD 用户，如服务到服务客户，输入基本文本值。</span><span class="sxs-lookup"><span data-stu-id="40054-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="40054-135">例如，NA。</span><span class="sxs-lookup"><span data-stu-id="40054-135">For example, NA.</span></span> <span data-ttu-id="40054-136">如果使用了有效的标识提供者值，此值会帮助避免可能导致错误的不正确的身份验证调用。</span><span class="sxs-lookup"><span data-stu-id="40054-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="40054-137">对于外部或来宾用户，在 https://sts.windows.net/ 后面添加其 Azure AD 租户名称。</span><span class="sxs-lookup"><span data-stu-id="40054-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="40054-138">在 **电子邮件** 字段中，输入用户的完整电子邮件/用户主体名称。</span><span class="sxs-lookup"><span data-stu-id="40054-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="40054-139">在 **公司** 字段中，为用户选择默认启动公司。</span><span class="sxs-lookup"><span data-stu-id="40054-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="40054-140">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="40054-140">Select **Save**.</span></span>

<span data-ttu-id="40054-141">保存用户记录时，将基于 [Microsoft graph](https://docs.microsoft.com/graph/overview) 调用更新标识提供者和遥测 ID 的值。</span><span class="sxs-lookup"><span data-stu-id="40054-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](https://docs.microsoft.com/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="40054-142">遥测 ID 基于 Azure AD 中用户的对象 ID/安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="40054-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="40054-143">添加用户后，必须根据需要分配角色和组织。</span><span class="sxs-lookup"><span data-stu-id="40054-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="40054-144">有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="40054-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="40054-145">有条件地，可能还需要将用户与 **人员** 关联，并更新 **用户选项**（如语言）。</span><span class="sxs-lookup"><span data-stu-id="40054-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="40054-146">更改用户 ID</span><span class="sxs-lookup"><span data-stu-id="40054-146">Change a user ID</span></span>
<span data-ttu-id="40054-147">要更改用户 ID，必须在数据库中重命名键。</span><span class="sxs-lookup"><span data-stu-id="40054-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="40054-148">使用此过程更改用户 ID 时，所有相关的用户设置都将被修改为使用新的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="40054-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="40054-149">例如，**SysLastValue** 表中的使用情况信息将更新以引用新的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="40054-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="40054-150">用户 ID 是用户信息表的主键。</span><span class="sxs-lookup"><span data-stu-id="40054-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="40054-151">为现有用户重命名主键可能要花费一些时间，因为对键的所有引用也会在数据库中更新。</span><span class="sxs-lookup"><span data-stu-id="40054-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="40054-152">转到 **系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="40054-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="40054-153">在列表中选择一个用户，然后选择 **选项 \> 记录信息**。</span><span class="sxs-lookup"><span data-stu-id="40054-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="40054-154">选择 **重命名**。</span><span class="sxs-lookup"><span data-stu-id="40054-154">Select **Rename**.</span></span>
4. <span data-ttu-id="40054-155">为用户 ID 输入一个新的唯一值，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="40054-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="40054-156">选择 **是** 进行确认。</span><span class="sxs-lookup"><span data-stu-id="40054-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40054-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="40054-157">Additional resources</span></span>

<span data-ttu-id="40054-158">有关实现 B2B 用户的更多选项，请参阅[将 B2B 用户导出到 Azure AD](../implement-b2b.md)。</span><span class="sxs-lookup"><span data-stu-id="40054-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="40054-159">有关预配置系统帐户的信息，请参阅[预配置系统帐户](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="40054-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]