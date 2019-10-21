---
title: Dynamics 365 Talent（2019 年 5 月 28 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4c56971628de12823b254f2a68dedfac50c996b0
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008838"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>Dynamics 365 Talent（2019 年 5 月 28 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="coming-soon-in-attract"></a>Attract 中即将推出

### <a name="job-approvals-on-home-page"></a>主页中的工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、头衔、其他审核人和分配的日期）下查看自己的审核。 提交工作共审核的用户可以在**您请求的**（其中显示仍然需要审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2319。

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

在此版本中，以下 Common Data Service 实体现在支持自定义字段：“福利计算比率详细信息”、“工作日历假期行”和“雇用”。

### <a name="copy-position-now-includes-payroll-details"></a>复制职位现在包含工资明细
使用**复制职位**并选择所有职位时，复制信息中现在包含工资明细信息。 

## <a name="in-preview-in-core-hr"></a>Core HR 中的预览中

### <a name="restrict-the-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种不同的休假类型。 这些休假类型中的某些可能不适合提交休假的员工，应该改由人力资源 (HR) 管理。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

### <a name="new-page-to-validate-position-hierarchy-data"></a>用于验证职位层次结构数据的新页面

HR 和管理员现在可以验证管理层次结构以查找任何可能已无意导入的循环引用。 可从**组织管理 > 链接 > 职位 > 职位层次结构验证**访问这个新页面。

### <a name="specify-reason-codes-on-leave-types"></a>指定休假类型的原因代码

组织可能需要有关休假请求的更多信息。 现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休假请求中的特定休假类型需要原因代码

组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。 可能因为公司政策或法规要求导致存在此项要求。 可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>为 HR 提供休假和缺勤交易记录列表

跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助 HR 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。 HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看休假余额背后的原因。
