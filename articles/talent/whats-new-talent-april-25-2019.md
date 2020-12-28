---
title: Dynamics 365 Talent（2019 年 4 月 23 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527167"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Dynamics 365 Talent（2019 年 4 月 23 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2253。 括号内的数字是 Lifecycle Services (LCS) 中的支持号码。

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持
安装本周的版本后，下列实体支持自定义字段：薪酬级别、福利选项、技能类型和薪酬区域。

### <a name="additional-odata-entities-302992"></a>其他 OData 实体 (302992)
OData 内现在支持下列实体：工作人员工作经验和工作人员教育。
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>经理和员工的绩效日记帐附件 (308248)
在此版本中，创建和更新绩效日记帐条目时，可以为经理和员工添加附件。

### <a name="employee-rehire-flag-always-available-310047"></a>员工重新聘用标签始终可用 (310047)
现在可在解除雇用流程外更新员工重新雇用选项。 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>不能更改 **我的付款方式** 的名称 (308815)
已启用了个性化，允许在员工自助服务中更改 **我的付款方式** 标签。

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>不能删除针对职位的财务维度 (293908)
请求更改现有跨公司范围的职位和财务维度时，现在可删除财务维度。 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>从 Excel 打开数据时，客户不能将数据发布回 Talent (302955)
此项更改解决了使用相关表时的发布问题。

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
## <a name="known-issues"></a>已知问题

### <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装 Finance and Operations 的平台更新 26 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。
