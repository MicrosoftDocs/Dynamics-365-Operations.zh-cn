---
title: 确定和解决职责划分冲突
description: 本主题介绍如何确定和解决职责划分冲突。
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c89d27eb8b587e8936258aae3ec1fee4574ccfb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180913"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>确定和解决职责划分冲突

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍如何确定和解决职责划分冲突。 您可以设置规则，以分离必须由不同用户执行的任务。 此概念被称作职责划分。 当安全角色定义或用户的角色分配违反规则时，会记录冲突。 所有冲突必须由管理员解决。 完成以下过程以确定和解决冲突。 创建此程序的演示数据公司是 USMF。


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>核实用户角色分配是否符合新的职责划分规则
1. 转到**导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 核实用户角色分配的合规性**。
2. 选择**确定**。 通知会显示核实结果。  如果存在冲突，您可以打开**用户**页面，然后更改用户的角色分配。 此外，**职责划分冲突**页面也会记录冲突。 要运行核实流程作为批处理作业，选择**批处理**，然后设置其他批处理参数。 在批处理作业运行之后，您可以审查**职责划分冲突**页面上的冲突。  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>查看并解决存在冲突的用户角色分配
1. 转到**导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 职责划分冲突**。 选择某一冲突，然后选择以下按钮之一：**拒绝分配 - 拒绝分配给该用户其他的安全角色**。 如果您拒绝自动角色分配，用户会被标记为从角色中排除。 被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。  允许分配 – **覆盖**冲突，并允许分配给用户两个安全角色。 如果您覆盖冲突，您必须在**覆盖原因**字段中输入原因。  
2. 关闭该页面。
3. 转到**导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 职责划分未解决的冲突**。 选择某一冲突，然后选择以下按钮之一：**拒绝分配 - 拒绝分配给该用户其他的安全角色**。 如果您拒绝自动角色分配，用户会被标记为从角色中排除。 被排除的用户不会被授予与该角色关联的访问权限，并且该用户不会被分配角色，直到管理员删除排除。  允许分配 – **覆盖**冲突，并允许分配给用户两个安全角色。 如果您覆盖冲突，您必须在**覆盖原因**字段中输入原因。    
4. 关闭该页面。

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>核实现有角色是否符合新的职责划分规则
1. 转到**导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 职责划分规则**。 选择一个规则。  
2. 选择**验证职责和角色**。 如果任何现有角色违反选定的规则，会显示包含角色名称和冲突职责的名称。 管理员必须指明减少安全风险或修改角色，以确保不违反职责划分规则。  如果没有角色违反选定的规则，会显示一条消息，以指明所有角色都遵从规则。  

