---
title: Dynamics 365 for Talent（2019 年 4 月 9 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 25ef0d49c2600833aefa84d404e00c0c57cfbf52
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517403"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a>Dynamics 365 for Talent（2019 年 4 月 9 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) 与“报告问题”集成
在 Attract 和 Onboard 中，最终用户使用报告问题功能记录的问题现在会在客户的 LCS 项目中自动创建报告问题。 管理员然后可以诊断问题并在需要时提交给 Microsoft。 这与 Core HR 处理最终用户支持问题的方式一致。

### <a name="relevance-search"></a>相关性搜索
现在可以在人才池中搜索整个应聘者数据库以查找特定技能、姓名或教育背景。 不再需要指定要搜索应聘者个人资料的哪部分。 Attract 搜索整个个人资料并突出显示找到的所有匹配项。 Attract 还搜索应聘者的所有可用文档并为搜索结果智能分级。 错误，还可以按来源或是否为银奖获得者来筛选结果。 有关详细信息，请参阅[搜索和查看应聘者个人资料](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles)。

### <a name="prospect-recommendations"></a>潜在人选推荐
Attract 可以通过搜索组织的应聘者数据库智能推荐应聘者，在您激活工作帐户立即开始为该工作寻找资源。 推荐信息中包括在搜索相关潜在人选时确定的技能和教育信息。 如果您在工作的招聘流程中启用**潜在人选**选项卡，将在工作的该选项卡下显示这些推荐信息。 有关详细信息，请参见[潜在人选推荐](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations)。

### <a name="interviewer-availability-statuses"></a>面试官可用性状态
面试安排人员很快将可以查看面试官的**外出，其他地点办公**状态，从而有助于安排更适合面试官的时间。

### <a name="candidate-interview-experience-save-calendar-invites"></a>应聘者面试体验：保存日历邀请
应聘者现在可以使用发给自己的面试摘要电子邮件中附加的 .ics 文件把自己的面试事件下载并保存到个人日历中。

## <a name="changes-in-onboard"></a>Changes 中的更改

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) 与“报告问题”集成
在 Attract 和 Onboard 中，最终用户使用报告问题功能记录的问题现在会在客户的 LCS 项目中自动创建报告问题。 管理员然后可以诊断问题并在需要时提交给 Microsoft。 这与 Core HR 处理最终用户支持问题的方式一致。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2225。

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>基本可变计划百分比加载的金额不正确
本周的版本更正了使用基本计划百分比加载可变薪酬奖励时出错。
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>“最后工作日期”上的日期选择器无法正常工作
此项更改更正了下面的问题：用户使用日历控件编辑**雇佣结束日期**并选择日期时，向所选日期增加一天。

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>按执行的操作限制个人操作类型
此项更改限制执行特定操作时显示的操作类型。 例如，请求新职位时，要选择的操作列表中仅显示新职位操作。 以前仅显示新建操作和编辑操作。 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>将员工转到下一个法人时带补偿
此版本允许跨公司转移员工时下一个法人中终止补偿。

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>转移期间无法为将来的雇佣关系选择补偿
将员工转给新法人时，现在可以在转移期间为新法人设置补偿。

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>用户无法在分配职位期间指定补偿
由于增加了新的职位分配，所以允许设置固定薪酬记录。 

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

###  <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。 
