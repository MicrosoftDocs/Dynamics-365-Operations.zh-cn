---
title: 确定和解决职责划分冲突
description: 本主题介绍如何确定和解决职责划分冲突。
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daf303a6bc3115363b27a6ebf7cc1832fdb6229d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571021"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>确定和解决职责划分冲突

[!include [banner](../../includes/banner.md)]

本主题介绍如何确定和解决职责划分冲突。 您可以设置规则，以分离必须由不同用户执行的职责。 此概念被称作职责划分。 当安全角色定义或用户的角色分配违反规则时，会记录冲突。 所有冲突必须由管理员解决。 完成以下过程以确定和解决冲突。

添加规则后，请验证所有现有角色是否符合规则。 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>验证现有角色和职责是否符合新的职责划分规则
1. 转到 **系统管理** > **安全** > **职责划分** > **职责划分规则**。
3. 选择 **验证职责和角色**。 如果任何角色违反规则，会显示包含规则名称、角色和冲突职责的名称的消息。 冲突角色必须使用 **安全配置** 修改，并且不能包含冲突职责。 如果没有角色违反选定的规则，会显示一条消息，以指明所有角色都符合规则。   

> [!NOTE]
> 验证仅针对所选规则执行。 验证对每个规则的合规性很重要。   

创建或修改角色时，会自动执行职责划分规则。 您无法为角色分配冲突职责。

接下来，验证所有现有角色分配均符合规则。

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>验证用户角色分配是否符合新的职责划分规则
1. 转到 **系统管理 > 安全 > 职责划分 > 验证用户角色分配的合规性**。
2. 选择 **确定**。 通知会显示核实结果。 **职责划分未解决的冲突** 页会记录冲突。   

将用户分配给角色时，会自动执行职责划分规则。 如果您尝试将用户分配给包含冲突职责的角色，会收到错误消息。 然后，您必须通过拒绝或允许其他角色分配来解决冲突。 允许分配后，将分配其他角色。 

> [!NOTE]
> 当前不对基于 Active Directory 域组分配了角色的用户验证冲突。

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>查看并解决存在冲突的用户角色分配
1. 转到 **系统管理** > **安全** > **职责划分** > **职责划分未解决的冲突**。 
2. 选择某一冲突，然后选择以下操作之一： 

  - **拒绝分配**：这将拒绝分配给该用户其他的安全角色。 如果您拒绝自动角色分配，用户会被标记为从角色中排除。 被排除的用户不会被授予与该角色关联的访问权限，并且不会被分配角色，直到管理员删除排除。 
-  **允许分配**：这将覆盖冲突，并允许分配给用户其他安全角色。 如果您覆盖冲突，您必须在 **覆盖原因** 字段中输入原因。 所有被覆盖的角色分配可以在 **职责划分冲突** 页上查看。  

> [!NOTE]
> 如果为同一用户列出了多个冲突，在 **用户** 页上选择用户记录并评估分配的角色。 为避免这一冲突，请在添加或修改每个规则后对其进行验证。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]