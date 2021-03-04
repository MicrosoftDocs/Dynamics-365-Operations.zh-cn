---
title: Dynamics 365 Human Resources（2020 年 4 月 13 日）新增功能或更改
description: 本文介绍 2020 年 4 月 13 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7ea8348cfe1c66d6d0cfa39b46c8e69111fe185
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528513"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Dynamics 365 Human Resources（2020 年 4 月 13 日）新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.3136。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="new-production-release-cadence"></a>新产品发布频率

在本周的发布中，Human Resources 的发布频率将从每周更新变为每两周更新。 为了确保符合安全部署实践，并在服务中保持高标准的稳定性和可靠性，现在为期两周把服务更新部署到所有区域。 将部署更多测试和监视人员，以验证流程各个阶段是否成功部署。 有关发布频率的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>指定化整类型后“化整精度”字段不可编辑 (435616)

通过此更改，更新 **化整类型** 字段后，现在可使用 **化整精度** 字段。

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>不能在休假计划中无应计期间时编辑休假登记结束日期 (413628)

现在可以编辑登记结束日期，不会出现“必须填写应计日期基础字段”错误。

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>雇用实体不同步到 Common Data Service (430834)

此更改解决了添加财务维度后雇用数据不同步到 Common Data Service 这一问题。 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>删除工作日历日历时间间隔实体的多父项 (431775)

此更改解决了 **工作日历时间间隔** 实体的多父项问题。

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>采用 CAST 函数的筛选器对 OData 调用位置工作人员分配实体无效 (431699)

此更新中包含一项更改，用于允许 OData 内采用 CAST 函数的筛选器用于 **位置工作人员分配** 实体。

## <a name="in-preview"></a>预览模式

## <a name="leave-suspension"></a>休假暂停

可在 Human Resources 中暂停员工的休假和缺勤。 暂停休假将停止所选休假类型的休假应计。 如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。 有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。

## <a name="carry-forward-rules"></a>结转规则

可为转移了结转调整的结转余额指定结转休假类型。 例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。 有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。

## <a name="known-issues"></a>已知问题

## <a name="employment-details-entity"></a>雇用详细信息实体

已使用以下字段更新了 **雇用详细信息** 实体：

- **付款频率**
- **雇用类别 ID**
- **雇用类型**
- **雇用类型 ID**
- **福利雇用状态**

这些字段的设置数据依赖于 **功能管理** 工作区中启用的福利管理。 请勿填写或更新 **雇用详细信息** 实体中的这些字段，因为将导致导入期间出错。

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint 预览在某些环境下不起作用

如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：

1. 验证管理员用户帐户是否具有与用户记录关联的电子邮件。 可在 **用户** 页面查看这些信息。 如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。 默认情况下，Excel 设计中不显示电子邮件地址。 您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。 完成这些步骤后，您可以更新管理员帐户。

2. 管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。

3. 访问 SharePoint 中的附件启动文档预览。

4. 使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]