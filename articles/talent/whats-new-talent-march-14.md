---
title: Dynamics 365 Talent（2019 年 3 月 14 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a3bb5792e6395e6fe593691f050cae03362cf659
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528613"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Dynamics 365 Talent（2019 年 3 月 14 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
此版本中包含一些小缺陷修复。

## <a name="changes-in-onboarding"></a>Onboarding 中的更改
此版本中包含一些小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
**内部版本 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>使用重复安全角色时任何场景中性能管理都不起作用
在使用自带或重复角色时，此版本中的更改会启用性能管理场景。

### <a name="mass-assign-checklists-to-workers"></a>为工作人员批量分配核对清单
通过此更改，您现在可以选择多个员工并为这些员工批量分配一个或多个核对清单。 

### <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operations 平台更新 24
有关 Finance and Operations 平台更新 24 的更多详细信息，请参阅 [Finance and Operations 平台更新 24（2019 年 3 月）中的新增或更改功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)。 平台 24 中的重大更改包括： 

- 在 Talent 中启用警报。
- 更新后的导航栏现在与 Office 标题对齐。

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>更新 Office 位置将把上下文切换到工作人员列表顶部。
通过当前版本，更改 Office 位置将不再切换您在分配 Office 位置时查看的工作人员上下文。

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>工作人员招聘和转移操作的职位分配结束日期无法正常显示
职位分配结束日期现在根据使用操作时用户的首选时区正确显示。

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service工作实体不允许更新“工作类型”和“工作职能”字段
在使用 Common Data Service 更新后，Common Data Service 实体现在可以正确同步。

## <a name="coming-soon"></a>即将到期

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）
在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。 这些记录可能是有关管理层或地区员工的记录。 通过此更改，HR 可以管理和维护组织中不同员工组的薪酬计划。 您可以为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。 只有授予了访问权限的角色才能处理这些员工的薪酬。

###  <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装 Finance and Operations 平台更新 24 之后，用户可创建警报规则，用于在被事件触发后自动向联系人派遣电子邮件通知。

### <a name="duplicate-employee-check-interface-changes"></a>重复员工检查：界面更改
借助此更改，输入名称字段时可检测重复项，而状态将显示找到的数量。 您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。 重复项窗体不会自动打开，以免中断数据输入。


[!INCLUDE[footer-include](../includes/footer-banner.md)]