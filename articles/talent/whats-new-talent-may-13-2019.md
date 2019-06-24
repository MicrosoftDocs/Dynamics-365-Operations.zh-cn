---
title: Dynamics 365 for Talent（2019 年 5 月 13 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591494"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Dynamics 365 for Talent（2019 年 5 月 13 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="coming-soon-in-attract"></a>Attract 中即将推出

### <a name="job-approvals-on-home-page"></a>主页中的工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、头衔、其他审核人和分配的日期）下查看自己的审核。 提交工作共审核的用户可以在**您请求的**（其中显示仍然需要审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2297。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="indicate-instance-type-when-provisioning-talent"></a>配置 Talent 时指示实例类型

配置新的 Talent 时，可以指示实例类型为**生产**还是**沙盒**，这样就可以提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

在本周的发布中，下列 Common Data Service 实体现在支持自定义字段：雇用、福利计算频率、福利计算比率、工作日历、工作日历假日和标识类型。

### <a name="common-data-service-integration-page"></a>Common Data Service 集成页

此版本在**系统管理 > 链接 > 集成 > Common Data Service 配置**中提供一个新选项。 **Common Data Service 配置**选项为管理员或数据管理管理员提供了一些灵活性和对 Common Data Service 的见解。 在此版本中，您可以启用或禁用 Common Data Service 与 Talent 实例的集成，以及查看 Talent 实例与 Common Data Service 之间的同步细节。

### <a name="import-performance-data-with-final-employee-rating-316710"></a>导入绩效数据和最终员工评级 (316710)

在此版本中，可以导入员工评级历史数据。 **FinalEmployeeRatingId** 字段现在拥有写入权限。

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>不能在 Common Data Service 中创建工作人员地址并与 Talent 同步 (317555)

此更改允许将 Common Data Service 中创建的地址数据与 Talent 同步。

## <a name="in-preview"></a>预览模式

### <a name="new-page-to-validate-position-hierarchy-data"></a>用于验证职位层次结构数据的新页面

人力资源 (HR) 和管理员可以验证管理层次结构以查找任何可能已无意导入的循环引用。 可从**组织管理 > 链接 > 职位 > 职位层次结构验证**访问这个新页面。

### <a name="specify-reason-codes-on-leave-types"></a>指定休假类型的原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。 可能因为公司政策或法规要求导致存在此项要求。 可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助 HR 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看休假余额背后的原因。
