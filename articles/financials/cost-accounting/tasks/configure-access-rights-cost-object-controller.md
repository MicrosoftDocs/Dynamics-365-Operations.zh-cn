--- 
title: "配置成本对象控制器的访问权限"
description: "此过程用于配置成本对象总监的访问权限。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b0647e1ec55d23607d07f38105e42af498ad1174
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>配置成本对象控制器的访问权限

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程用于配置成本对象总监的访问权限。 此录制使用 USP2 演示数据公司。


## <a name="assign-the-cost-object-controller-role"></a>分配成本对象总监角色
1. 转到“系统管理”>“用户”>“用户”。
2. 使用“快速筛选器”以查找记录。 例如，在“用户名”字段中筛选值“alicia”。
3. 在列表中，单击所选行中的链接。
4. 单击“分配角色”。
5. 在列表中，找到并选择所需记录。
6. 单击“确定”。

## <a name="enable-access-list-security"></a>启用访问列表安全性
1. 转到“成本核算”>“维度”>“维度层次结构”。
2. 在列表中，找到并选择所需记录。
    * 选择“组织”。  
3. 单击“编辑”。
4. 在“访问列表层次结构”字段中选择“是”。
5. 单击“查看层次结构”。

## <a name="assign-access-rights-to-user"></a>为用户分配访问权限
1. 单击“新建”。
2. 在列表中，标记所选的行。
3. 在“用户身份”字段，输入或选一个值。
    * 选择“管理员”。  
4. 在树中，选择“组织\CEO\CFO\FIM”。
5. 单击“新建”。
6. 在列表中，标记所选的行。
7. 在“用户身份”字段，输入或选一个值。
    * 选择“Alicia”。  
8. 单击“保存”。

## <a name="enable-access-rights-in-cost-accounting"></a>在成本核算中启用访问权限
1. 转至“成本核算”>“设置”>“参数”。
2. 单击“常规”选项卡。
3. 在“为成本对象维度成员启用视图访问”字段中选择“是”。
4. 单击“保存”。
5. 关闭该页面。
6. 转至“成本核算”>“设置”>“成本控制工作区配置”。
7. 单击“编辑”。
8. 在“已发布”字段中选择“是”。
    * 如果选择“是”，为其分配了以下四种角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师、成本核算师和成本对象总监。 如果选择“否”，为其分配了以下角色之一的用户可查看报表：成本核算经理、成本会计师和成本核算师。    
9. 单击“保存”。


