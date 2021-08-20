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
ms.openlocfilehash: e8ae7bc937e916195b49df91be73ba906bcd2e593c9222cdc07adfcbf2396c05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733677"
---
# <a name="create-new-users"></a>创建新用户

[!include [banner](../../includes/banner.md)]

您必须先被添加到 **用户** 页（**系统管理 \> 用户 \> 用户**），然后才能访问 Finance and Operations 应用。 用户包括您组织的内部员工，或外部客户和供应商。 用户可以手动导入或添加。 所有用户都必须获得正确的许可才符合使用要求。

有关如何购买 Finance and Operations 应用和获得许可的信息，请参阅 [Microsoft Dynamics 365 许可指南](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)。

## <a name="assign-a-license-to-a-user"></a>向用户分配许可证
系统管理员可以在 [Microsoft 365 管理中心](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>在 Azure AD 中添加外部用户并分配许可证 
外部用户必须在您的租户目录 (Azure Active Directory (Azure AD)) 中出现，才可以为他们分配许可证。 应将这些外部用户作为来宾用户添加到 Azure AD 内的租户中，然后为其分配适当的许可证。 Finance and Operations 应用的要求是，来宾用户的公司必须使用 Azure AD。 有关更多信息，请参见[在 Azure 门户中添加 Azure Active Directory B2B 协作用户](/azure/active-directory/b2b/add-users-administrator)。

## <a name="import-new-users-from-azure-ad"></a>从 Azure AD 导入新用户 
1. 转到 **系统管理** \> **用户** \> **用户**。
2. 在操作窗格上，选择 **导入用户**。
3. 选择要导入的用户。 列表中包括当前不是此环境中的用户的 Azure AD 用户。
4. 选择 **导入用户**。
5. 选择 **关闭**。

> [!NOTE]
> **公司** 字段的值将根据管理员的当前会话公司设置。导入之后，您必须根据需要分配角色和组织。 有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。 有条件地，可能还需要将用户与 **人员** 关联，并更新用户选项（如语言）。

## <a name="manually-add-a-new-user"></a>手动添加新用户
1. 转到 **系统管理** \> **用户** \> **用户**。
2. 在操作窗格上，选择 **新建**。
3. 在 **用户 ID** 字段中，输入用户的唯一标识符。   
4. 在 **用户名称** 字段中，输入用户的名称。  
5. 在 **提供者** 字段中：
 - 对于内部用户，使用默认值。 例如，您的以 https://sts.windows.net/ 为前缀的 Azure AD 租户。  
 - 对于非 Azure AD 用户，如服务到服务客户，输入基本文本值。 例如，NA。 如果使用了有效的标识提供者值，此值会帮助避免可能导致错误的不正确的身份验证调用。  
 - 对于外部或来宾用户，在 https://sts.windows.net/ 后面添加其 Azure AD 租户名称。
6. 在 **电子邮件** 字段中，输入用户的完整电子邮件/用户主体名称。  
7. 在 **公司** 字段中，为用户选择默认启动公司。 
8. 选择 **保存**。

保存用户记录时，将基于 [Microsoft graph](/graph/overview) 调用更新标识提供者和遥测 ID 的值。 遥测 ID 基于 Azure AD 中用户的对象 ID/安全标识符 (SID)。

> [!NOTE]
> 添加用户后，必须根据需要分配角色和组织。 有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。 有条件地，可能还需要将用户与 **人员** 关联，并更新 **用户选项**（如语言）。

## <a name="change-a-user-id"></a>更改用户 ID
要更改用户 ID，必须在数据库中重命名键。 使用此过程更改用户 ID 时，所有相关的用户设置都将被修改为使用新的用户 ID。 例如，**SysLastValue** 表中的使用情况信息将更新以引用新的用户 ID。

> [!NOTE]
> 用户 ID 是用户信息表的主键。 为现有用户重命名主键可能要花费一些时间，因为对键的所有引用也会在数据库中更新。 

1. 转到 **系统管理 \> 用户 \> 用户**。
2. 在列表中选择一个用户，然后选择 **选项 \> 记录信息**。
3. 选择 **重命名**。
4. 为用户 ID 输入一个新的唯一值，然后选择 **确定**。 
5. 选择 **是** 进行确认。

## <a name="additional-resources"></a>其他资源

有关实现 B2B 用户的更多选项，请参阅[将 B2B 用户导出到 Azure AD](../implement-b2b.md)。

有关预配置系统帐户的信息，请参阅[预配置系统帐户](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]