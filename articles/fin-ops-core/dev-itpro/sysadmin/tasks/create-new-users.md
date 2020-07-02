---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435576"
---
# <a name="create-new-users"></a>创建新用户

[!include [banner](../../includes/banner.md)]

用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>将用户与许可证相关联（仅适用于新许可证类型）
对于具有 2019 年 10 月添加的新许可证类型之一的客户，用户必须与许可证相关联。 与许可证相关联的用户会在第一次登录时自动添加为没有角色的系统用户。

系统管理员可以在 [Microsoft 365 管理中心](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>将外部用户与许可证相关联（仅适用于新许可证类型）
需要在托管租户目录中表示环境所部署到的租户外部的用户 (Azure Active Directory (Azure AD))，以便可以为其分配许可证。 应将这些外部用户作为来宾用户添加到 Azure AD 内的租户中，然后为其分配适当的许可证。 有关更多信息，请参见[在 Azure 门户中添加 Azure Active Directory B2B 协作用户](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)。

## <a name="add-a-new-user"></a>添加新用户
1. 转到**系统管理 \> 用户 \> 用户**。
2. 在操作窗格上，选择**新建**。
3. 在**用户 ID** 字段中，输入用户的唯一标识符。 用户 ID 是必填项。  
4. 在**用户名称**字段中，输入用户的名称。  
5. 在**域**字段中，输入用户的域。  
6. 在**别名**字段，输入用户的别名。  
7. 在**公司**字段中，选择所需公司。 
8. 在**用户的角色**快速选项卡中，选择**分配角色**向用户分配安全角色。 有关更多信息，请参阅[向安全角色分配用户](assign-users-security-roles.md)。
9. 选择**确定**。
10. 选择**保存**。

## <a name="import-users"></a>导入用户
1. 转到**系统管理 \> 用户 \> 用户**。
2. 在操作窗格上，选择**导入用户**。
3. 在列表中，标记所选的行。
4. 选择**导入用户**。
5. 选择**关闭**。

