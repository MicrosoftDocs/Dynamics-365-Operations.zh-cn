--- 
title: "将用户分配给安全角色"
description: "若要访问 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition，必须为用户分配安全角色。"
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>将用户分配给安全角色

[!include [task guide banner](../../includes/task-guide-banner.md)]

若要访问 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition，必须为用户分配安全角色。 此过程说明系统管理员如何基于业务数据将用户自动分配到角色。 创建此程序的演示数据公司是 USMF。


## <a name="automatically-assign-users-to-roles"></a>将用户自动分配到角色
1. 转到“系统管理”>“安全”>“将用户分配到角色”。
2. 在树结构中，选择“会计主管”。
    * 选择要为其配置规则的角色。 在此示例中，选择会计主管。  
3. 单击“添加规则”打开下拉对话框。
4. 在列表中，找到并选择所需记录。
    * 选择要用于此规则的查询。  
5. 在列表中，单击所选行中的链接。
6. 单击“编辑查询”。
    * 编辑查询（根据需要）。  
7. 单击“确定”。

## <a name="exclude-users-from-automatic-role-assignment"></a>将用户从自动角色分配中排除
1. 关闭该页面。
2. 转到“系统管理”>“安全”>“将用户分配到角色”。
3. 在树结构中，选择“会计主管”。
    * 选择一个角色。 在此示例中，选择会计主管。  
4. 单击“手动分配/排除用户”。
5. 在列表中，标记所选的行。
    * 选择用户。  
6. 单击“从角色中排除”。
    * 单击“从角色中排除”从角色中排除所选用户。 若要删除排除，选择要删除排除的用户，然后单击“重置状态”。 在您通过重置用户状态删除排除时，用户角色自动重新分配。 但是，用户不立即分配给角色或在重置状态时从角色中排除。 相反，用户在下一次运行自动角色分配规则时分配给角色或从角色中删除。  


