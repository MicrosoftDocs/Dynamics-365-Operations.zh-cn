---
title: Dynamics 365 Talent（2019 年 4 月 16 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa61a70e14b7997258376beaf389129a4ad2fa73
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197259"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Dynamics 365 Talent（2019 年 4 月 16 日）中的新增功能或更改

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="process-auditing"></a>流程审核

现在可跟踪对应聘者、职位空缺和工作申请进行的更改。 有关详细信息，请参阅[跟踪招聘数据的变化](process-auditing.md)。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2239。 括号内的数字是 Lifecycle Services (LCS) 中的支持号码。

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Common Data Service 中的“薪酬区域”、“薪酬级别”、“福利选项”和“技能类型”实体已更新，现在包含客户字段支持。

在此版本中，已将这些 Common Data Service 实体更新为可包含通过 Talent: Core HR 添加的自定义字段。

### <a name="powerbi-refresh-issues-314342"></a>PowerBI 刷新问题 (314342)

此项更改解决了 PowerBI 报告正确刷新的问题。

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>无法在员工自助服务中直接单击浏览转移任务 (303309)

此项更改让具有员工角色的用户可从 Talent 待办事宜列表中选择和更新转换任务。

### <a name="performance-feedback-email-message-updated-309615"></a>更新了性能反馈电子邮件消息 (309615)

在此版本中，成功提交反馈后，将显示确认消息。

### <a name="missing-tables-in-word-template-308048"></a>Word 模板中缺少表 (308048)

通过此更改，创建包含员工和技能信息的 Word 模板时，Word 文档中仅显示所选员工的技能。

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>应用离职核对清单时显示错误。 (299877)

此项更改解决了直接从工作人员表单应用离职核对清单时的问题。

## <a name="in-preview"></a>预览模式

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>允许为休假类型指定原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交请假时为特定休假类型设置原因代码。 可能是因为公司政策或法规要求所致。 现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法不仅可以帮助 HR 解答员工的问题，还可以确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），以查看余额背后的原因。

## <a name="coming-soon"></a>即将到期

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>改进了用户界面中的重复员工检查

借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。 您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。 为了避免中断数据输入，重复项窗体不会自动打开。

### <a name="email-support-for-alerts"></a>警报的电子邮件支持

安装 Finance and Operations 的平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。


