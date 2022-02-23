---
title: Dynamics 365 Talent（2019 年 3 月 5 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 115d7cd3d71eaddce2434cb1939c503d36bccdf8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527282"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Dynamics 365 Talent（2019 年 3 月 5 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="extending-option-sets-in-attract"></a>扩展了 Attract 中的选项集

在 Attract 中，有多个字段是 Common Data Service 内的选项集。 已引入了新功能，用于扩展选项集，从 **拒绝原因** 字段、**雇佣类型** 字段和 **任职类型** 字段开始。

> [!IMPORTANT]
> 工作发布到 LinkedIn 这一功能要求使用 **工作详细信息** 页中的 **雇佣类型** 和 **任职类型** 字段。 这些字段中的默认值受 LinkedIn 支持，将在发布工作时显示。 如果要将工作发布到 LinkedIn，并且修改这些字段的现有选项集值，仍将发布工作，但是 LinkedIn 不会显示自定义的 **雇佣类型** 和 **任职类型** 值。

## <a name="changes-in-onboarding"></a>Onboarding 中的更改

### <a name="private-preview-for-onboard-teams"></a>Onboard 工作组的专用预览
现在可在整个组织中轻松共享和协作处理模板。 有关详细信息，请参阅[使用 Onboard 工作组在组织中共享最佳实践](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams)。

### <a name="private-preview-for-assignee-placeholders"></a>受托人占位符的专用预览
可通过将活动分配给角色而不是个人来丰富模板。 然后在创建指南时将角色分配给个人。 有关详细信息，请参阅[通过将活动分配给角色简化指南管理](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles)。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
**内部版本 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>将工作流配置为当 HR 或职能经理提交或更新请假时自动批准或执行工作流
已添加了新的工作流条件，以便在员工的经理或 HR 提交了请假时自动批准。 若要实现这种自动批准工作流，其中一种方法是为工作流的批准启用自动操作。

已添加的条件包括：

- 提交者 - 用于评估向工作流提交请求的用户的系统用户 ID。
- 提交的名义人 - 用于在请求是代表其关联的工作人员提交的时进行评估。
- 已由人力资源部门提交 - 用于在提交请求的系统用户属于人力资源角色时进行评估。
- 已由经理提交 - 用于在向工作流提交请假的用户是该请假的关联工作人员在层次结构中的职能经理时进行评估。

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>为将来的职位分配启用员工固定薪酬
通常适用于在将来的开始日期加入组织的员工。 通过此项更改，可以为将来分配的职位所属员工定义固定薪酬。

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>编辑职位时，“职位工资”字段为空
通过此更改，请求更改现有职位时，工资字段现在默认采用当前值。

### <a name="other-miscellaneous-bug-fixes"></a>其他杂项缺陷修复
此版本中还包含其他小缺陷修复。

### <a name="upgrade-to-common-data-service"></a>升级到 Common Data Service
很快将到达 Common Data Service 的升级截止时间。 请登录 Power Apps 管理员中心以确定是否需要升级您的数据库。 有关截止时间和必要升级步骤的详细信息，请参阅[升级到 Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)。

## <a name="coming-soon"></a>即将到期

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）
在许多组织中，薪酬和福利经理只能访问特定薪酬记录，如管理层或区域员工的记录。 通过此更改，您可以管理和维护组织中不同员工群的薪酬计划。 可为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。 只有具有给定访问权限的角色才能处理这些员工的薪酬。

###  <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operations 平台更新 24
有关 Finance and Operations 平台更新 24 的更多详细信息，请参阅 [Finance and Operations 平台更新 24（2019 年 3 月）中的新增或更改功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)。
