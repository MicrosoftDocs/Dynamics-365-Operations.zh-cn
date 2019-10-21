---
title: 创建新用户
description: 用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180936"
---
# <a name="create-new-users"></a>创建新用户

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

用户是您的组织的内部员工或外部客户和供应商，该用户需要访问系统以履行职责。

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>将用户与许可证相关联（仅适用于新许可证类型）
对于具有 2019 年 10 月添加的新许可证类型之一的客户，用户必须与许可证相关联。 与许可证相关联的用户会在第一次登录时自动添加为没有角色的系统用户。 未与许可证关联的用户会收到警告消息。

系统管理员可以在 [Microsoft 365 管理中心](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)[向用户分配许可证](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)。

## <a name="add-a-new-user"></a>添加新用户
1. 转到**系统管理 \> 用户 \> 用户**。
2. 在操作窗格上，选择**新建**。
3. 在**用户 ID** 字段中，输入用户的唯一标识符。 用户 ID 是必填项。  
4. 在**用户名称**字段中，输入用户的名称。  
5. 在**域**字段中，输入用户的域。  
6. 在**别名**字段，输入用户的别名。  
7. 在**公司**字段中，选择所需公司。 
8. 在**用户的角色**快速选项卡中，选择**分配角色**[向用户分配安全角色](assign-users-security-roles.md)
9. 选择**确定**。
10. 选择**保存**。

## <a name="import-users"></a>导入用户
1. 在操作窗格上，选择**导入用户**。
2. 在列表中，标记所选的行。
3. 选择**导入用户**。
4. 选择**关闭**。

