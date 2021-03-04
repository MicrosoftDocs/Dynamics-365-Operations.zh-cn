---
title: Dynamics 365 Talent（2019 年 4 月 30 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528187"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Dynamics 365 Talent（2019 年 4 月 30 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中介绍的更改适用于内部版本号 8.1.2270。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="provide-feedback"></a>提供反馈

Talent 中用于提供反馈的选项位于 **帮助** 菜单 (**?**) 上。 可通过此菜单访问下列资源：

- 反馈
- 帮助
- 开始
- 支持
- 灵感
- 关于

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>改进了用户界面中的重复员工检测

由于此更改，现在设置名称字段时会检测重复项，并通过状态指示器显示已检测到的重复项数。 提供的链接将打开一个页面，可在其中评估是否应使用其中一个重复项。 为了避免中断数据输入，不会自动打开重复项页。 必须选择该链接以打开页面。

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

在本周的版本中，以下实体现在支持自定义字段：雇用、福利类型和付薪周期。

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>分配离职核对清单时出错 (299877)

此项更改更正了在非解除雇用流程中将离职核对清单分配给员工时显示的错误消息。

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>离职工作人员链接打开不正确的工作人员 (309939)

此项更改解决了重新雇用其他法人的员工并尝试从离职员工列表访问该员工时出现的问题。

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>开启了高级安全后员工自助服务薪酬卡不显示汇总值 (315231)

此项更改解决了使用高级薪酬安全时发生的问题。 开启高级安全后，员工自助服务现在同时显示员工和经理的薪酬汇总金额。 此项更改之前，汇总值显示为 0（零）。

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>如果在 Common Data Service 中创建不带职称的职位，则不在 Talent 中创建任何职位 (314562)

本周的更改解决了在 Common Data Service 中创建职位但不提供职称时发生的问题。

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>员工自助服务中的绩效日记帐条目中的错误消息 (314134)

此项更改解决了在员工自助服务中向绩效日记帐条目附加绩效目标时发生的问题。

## <a name="in-preview"></a>预览模式

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>允许为休假类型指定原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。 可能因为公司政策或法规要求导致存在此项要求。 现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助人力资源 (HR) 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看余额背后的原因。

## <a name="coming-soon"></a>即将推出

### <a name="email-support-for-alerts"></a>警报的电子邮件支持

安装 Finance and Operations 平台更新 26 之后，用户可创建警报规则，用于在事件触发通知后自动向联系人发送电子邮件通知。


[!INCLUDE[footer-include](../includes/footer-banner.md)]