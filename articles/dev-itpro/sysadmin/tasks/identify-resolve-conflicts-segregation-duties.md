--- 
title: "确定和解决职责划分冲突"
description: "您可以设置规则，以分离必须由不同用户执行的任务。"
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>确定和解决职责划分冲突

[!include[task guide banner](../../includes/task-guide-banner.md)]

您可以设置规则，以分离必须由不同用户执行的任务。 此概念被称作职责划分。 当安全角色定义或用户的角色分配违反规则时，会记录冲突。 所有冲突必须由管理员解决。 完成以下过程以确定和解决冲突。 创建此程序的演示数据公司是 USMF。


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>核实用户角色分配是否符合新的职责划分规则
1. 转到“系统管理”>“安全”>“职责划分”>“核实用户角色分配的合规性”。
2. 单击“确定”。
    * 通知会显示核实结果。      如果存在冲突，您可以打开“用户”页面，然后更改用户的角色分配。 此外，职责划分冲突页面也会记录冲突。     要运行核实流程作为批处理作业，选择批处理，然后设置其他批处理参数。 在批处理作业运行之后，您可以审查职责划分冲突页面上的冲突。  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>查看并解决存在冲突的用户角色分配
1. 转到“系统管理”>“安全”>“职责划分”>“职责划分冲突”。
    * 选择某一冲突，然后单击以下按钮之一：     拒绝分配 - 拒绝分配给该用户其他的安全角色。 如果您拒绝自动角色分配，用户会被标记为从角色中排除。 被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。      允许分配 – 覆盖冲突，并允许分配给用户两个安全角色。 如果您覆盖冲突，您必须在“覆盖原因”字段中输入原因。  
2. 关闭该页面。
3. 转到“系统管理”>“安全”>“职责划分”>“职责划分未解决的冲突”。
    * 选择某一冲突，然后单击以下按钮之一：     拒绝分配 - 拒绝分配给该用户其他的安全角色。 如果您拒绝自动角色分配，用户会被标记为从角色中排除。 被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。      允许分配 – 覆盖冲突，并允许分配给用户两个安全角色。 如果您覆盖冲突，您必须在“覆盖原因”字段中输入原因。    
4. 关闭该页面。

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>核实现有角色是否符合新的职责划分规则
1. 转到“系统管理”>“安全”>“职责划分”>“职责划分规则”。
    * 选择一个规则。  
2. 单击“核实职责和角色”。
    * 如果任何现有角色违反选定的规则，会显示包含角色名称和冲突职责的名称。 管理员必须指明减少安全风险或修改角色，以确保不违反职责划分规则。      如果没有角色违反选定的规则，会显示一条消息，以指明所有角色都遵从规则。  


