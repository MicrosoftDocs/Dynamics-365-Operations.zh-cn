---
title: Dynamics 365 Talent（2019 年 4 月 2 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 04b5a006d4580fe419d81986a90851bc8d611722
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528211"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Dynamics 365 Talent（2019 年 4 月 2 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="approval-emails-in-attract"></a>Attract 中的审核电子邮件
新增的审核电子邮件可以提高对审核流程的认识。 如果出现下面的一种场景，将向审核人发送电子邮件：

- 请求者提交工作待审核。
- 拒绝或批准了工作。
- 审核人在 24 小时内未处理审核请求。

可以使用新模板自定义审核电子邮件的内容。

### <a name="application-and-profile-attachments"></a>申请表和个人资料附件
申请表和人才池个人资料上的 **文档** 选项卡的附件现在同时显示文档名和类型。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="coming-soon-attract-and-onboard"></a>即将推出（Attract 和 Onboard）

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) 与“报告问题”集成
在 Attract 和 Onboard 中，最终用户通过报告问题功能记录的问题现在会在客户的 LCS 项目中自动创建报告问题。 管理员然后可以诊断问题并在需要时提交给 Microsoft。 这与 Core HR 处理最终用户支持问题的方式一致。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2216。

### <a name="platform-update-25-for-finance-and-operations"></a>Finance and Operations 平台更新 25
有关 Finance and Operations 平台更新 25 的详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 25（2019 年 4 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25)。

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）
在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。 其中可能包含有关管理层或地区员工的记录。 此更改让 HR 可以管理和维护组织中不同员工组的薪酬计划。 可以为固定计划和可变计划分配安全角色。 这些安全角色决定计划和相关员工数据（如工资或福利记录）的访问权限，因此只有这些角色可以处理员工组的薪酬。

### <a name="upgrade-to-common-data-service"></a>升级到 Common Data Service
很快将到达 Common Data Service 的升级截止时间。 请登录 Microsoft Power Apps 管理员中心以确定是否需要升级您的数据库。 有关截止时间和必要升级步骤的详细信息，请参阅[升级到 Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)。

## <a name="in-preview"></a>预览模式

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>允许为休假类型指定原因代码
组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码
组织可能会要求当员工提交请假时为特定休假类型设置原因代码。 可能是因为公司政策或法规要求所致。 现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

## <a name="coming-soon"></a>即将到期

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>改进了用户界面中的重复员工检查
借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。 您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。 为了避免中断数据输入，重复项窗体不会自动打开。

###  <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装 Finance and Operations 的平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。 
