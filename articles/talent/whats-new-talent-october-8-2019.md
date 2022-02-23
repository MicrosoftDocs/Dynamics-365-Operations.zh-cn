---
title: Dynamics 365 Talent（2019 年 10 月 8 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529472"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Dynamics 365 Talent（2019 年 10 月 8 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中介绍的更改适用于内部版本号 8.1.2542。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>从公共预览中删除福利开放登记

连同我们在[Core HR 的战略投资推动卓越运营](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/)博客文章中宣布的消息，Microsoft 将在 2019 年 10 月 18 日的公开预览中删除福利开放登记功能。 将来会发布新功能。 当前处于公共预览的福利开放登记功能的生产使用将不受支持。 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>现在，默认在新设置中关闭了 Common Data Service 集成 (343675)
 
设置新环境后，现在将关闭 Common Data Service 集成。 有关详细信息，请参阅[配置 Common Data Service 集成](hr-common-data-service-integration.md)。

### <a name="streamlined-employee-entry-and-navigation"></a>简化的员工条目和导航

现在，在所有环境中都可以使用员工输入和导航功能。 要启用此功能，请转到 **系统管理 \> 链接 \> 设置 \> 系统参数 \> 预览功能**，然后选择 **增强的工作人员窗体和导航**。 然后为所有用户打开此功能。 您可以随时关闭此选项。

有关详细信息，请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[简化的员工输入和导航](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry)。

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract 和 Onboard 在 Core HR 中创建不活动的工作人员 (380517)

本周的发布更正了 Attract 和 Onboard 在 Core HR 中创建不活动工作人员的问题。

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>当经理在终止员工时登录到另一家公司时，工作流失败 (346852)

工作流不再基于经理登录的法人而失败。

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>缺少有关 HcmOnboardingWorkerChecklistTaskEntity 的信息 (349591)

此版本包括有关 **HcmOnboardingWorkerChecklistTaskEntity** 的附加信息。 下面举了一些示例加以说明：

- 分配的类型为 **组** 时的 **组名称**
- 分配的类型为 **员工** 时的 **员工姓名**
- 分配的类型为 **经理** 时的 **经理姓名**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>在 Common Data Service 管理中未按字母顺序列出实体 (377414)

现在，实体在 **CDS 管理** 页面上按字母顺序列出。

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>更改具有未来日期的雇用类型不允许进行职位分配 (339958)

更改工作人员类型时（例如，从员工到合同工），此更改允许进行职位分配。

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>更新 Common Data Service 休假银行交易记录实体会在 Talent 中创建新记录 (352938)

现在，当对 Common Data Service 的休假银行交易记录进行更新时，休假交易记录将更新。

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>反馈项的附件标题显示反馈说明 (343765)

反馈说明不再出现在附件标题中。

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>薪酬工作流的“注释”字段显示不正确的内容 (339297)

此更改显示 **%HcmActionState.HcmWorkerActionComment.Comments%** 字段的内容。

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity 和 WorkCalendarDayEntity 不通过 OData 公开 (376329)

在此版本中，**WorkCalendarEntity** 和 **WorkCalendarDayEntity** 现在通过开放数据协议 (OData) 提供。

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>使用 OData 时 HCMWorkerEntity 变慢 (375221)

使用 Microsoft Excel 工作簿设计器时，更改将提高 **HCMWorkerEntity** 的性能。

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>在删除绩效日记帐并创建新的绩效日记帐后，经理绩效日记帐条目显示错误 (336061)

此版本更正了删除一个绩效日记帐并在此之后立即创建新绩效日记帐后发生的问题。 此更正更改了经理自助服务中的行为。

## <a name="coming-soon"></a>即将到期

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。
