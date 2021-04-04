---
title: 向安全角色分配用户
description: 若要访问 Finance and Operations 应用，用户必须分配给安全角色。
author: Peakerbl
manager: AnnBe
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
ms.openlocfilehash: 1a6d904ae3df23dd1c602cfdfecc40411aba5724
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569866"
---
# <a name="assign-users-to-security-roles"></a>向安全角色分配用户

[!include [banner](../../includes/banner.md)]

要使用 Finance and Operations 应用中的常用功能以外的其他功能，必须将用户分配给安全角色。 您可以根据规则和业务数据自动将用户分配给角色，不为用户自动分配角色，也可以手动将用户添加到角色。

## <a name="automatically-assign-users-to-roles"></a>将用户自动分配到角色
此过程说明系统管理员如何基于业务数据将用户自动分配到角色。 
1. 转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。
2. 在树结构中，选择“会计主管”。 选择要为其配置规则的角色。 在此示例中，选择会计主管。 
3. 选择 **添加规则** 以打开对话框菜单。
4. 在 **选择查询** 列表中，查找并选择所需的记录。 选择要用于此规则的查询。  
5. 在 **成员资格规则名称** 列表中，单击所选行中的链接。
6. 选择 **编辑查询**。 编辑查询（根据需要）。  
7. 选择 **确定**。
8. 选择 **运行自动角色分配**。
9. 转到 **导航窗格 > 模块 > 系统管理 > 用户 > 用户**（最好在单独的浏览器选项卡中）。
10. 查看分配给各个用户的角色，以确认角色分配查询是否正确。 根据需要调整并重新运行。

## <a name="exclude-users-from-automatic-role-assignment"></a>将用户从自动角色分配中排除
1. 关闭该页面。
2. 转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。
3. 在树结构中，选择“会计主管”。 选择一个角色。 在此示例中，选择会计主管。  
4. 在 **分配到角色的用户** 菜单中，选择 **手动分配/排除用户**。
5. 在 **将用户分配到角色或从角色中排除用户** 列表中，标记所选行。 选择用户。  
6. 在 **操作窗格** 中，选择 **从角色中排除**。
7. 选择 **从角色中排除** 以从角色中排除所选用户。 若要删除排除，选择要删除排除的用户，然后单击 **重置状态**。 通过重置用户状态删除排除项时，将自动分配用户角色。 但是，用户不立即分配给角色或在重置状态时从角色中排除。 相反，用户在下一次运行自动角色分配规则时分配给角色或从角色中删除。  

## <a name="manually-assign-users-to-roles"></a>手动将用户分配给角色
手动分配给安全角色的用户也必须由管理员手动删除。 不会通过自动角色分配规则从角色中删除这些用户。

1. 转到 **导航窗格 > 模块 > 系统管理 > 安全 > 将用户分配到角色**。
2. 在树中，选择一个角色，然后在 **分配给角色的用户** 菜单中，选择 **手动分配/排除用户**。
4. 在 **将用户分配给角色或从角色中排除用户** 中，列出了未分配有角色的用户，并且其 **分配模式** 设置为 **无**。 选择一个或多个应该为其分配角色的用户。
5. 在 **操作窗格** 上，选择 **分配给角色**。 **分配模式** 会更新为 **手动**，并且现在为用户分配了新角色。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]