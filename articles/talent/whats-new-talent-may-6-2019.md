---
title: Dynamics 365 Talent（2019 年 5 月 6 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529700"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Dynamics 365 Talent（2019 年 5 月 6 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="select-optional-documents-upon-offer-creation"></a>创建聘约后选择可选文档

选择聘约包模板时，Attract 现在会提示您从该包模板中选择适用的可选文档。 可以在准备聘约时添加其他可选文档。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2282。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="platform-update-26-for-finance-and-operations"></a>Finance and Operations 平台更新 26

有关 Finance and Operations 平台更新 26 的其他详细信息，请参阅 [Dynamics 365 Finance and Operations 平台更新 26（2019 年 5 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26)。 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

在本周的发布中，下列实体现在支持自定义字段：福利计算频率、福利计算比率、福利类型、工作日历、工作日历假日、付薪周期和工作人员标识类型。

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>休假大批登记，将标题基础更改为“受聘日期”不会刷新初始应计费率 (318526)

大批登记员工并更改层基础时，初始应计现在会体现您选择的层基础。

### <a name="workflow-showing-duplicate-place-holders-313636"></a>工作流显示重复占位符 (313636)

此版本中的更改消除了发送工作流通知时占位符重复的问题。

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>使用“在 Excel 中打开”时不更新维度字段 (176261)

在此版本中，现在可从 **工作人员** 页面中使用 **在 Excel 中打开** 更新财务维度。 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Common Data Service 中创建的工作人员地址不同步到 Talent (317555)

应用此更改之后，Common Data Service 中创建的地址将在 Talent: Core HR 中更新。


## <a name="in-preview"></a>预览模式

### <a name="new-page-to-validate-position-hierarchy-data"></a>用于验证职位层次结构数据的新页面

人力资源 (HR) 和管理员现在可以验证管理层次结构以查找任何可能已无意导入的循环引用。 可从 **组织管理 > 链接 > 职位 > 职位层次结构验证** 访问这个新页面。

### <a name="specify-reason-codes-on-leave-types"></a>指定休假类型的原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。 可能因为公司政策或法规要求导致存在此项要求。 现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助 HR 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看余额背后的原因。

## <a name="coming-soon"></a>即将到期

### <a name="indicate-instance-type-when-provisioning-talent"></a>配置 Talent 时指示实例类型

配置新的 Talent 时，可以指示实例类型为 **生产** 还是 **沙盒**，这样就可以提前测试新功能。 将把所有现有 Talent 实例更新为生产实例类型。 如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。


[!INCLUDE[footer-include](../includes/footer-banner.md)]