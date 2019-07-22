---
title: Dynamics 365 for Talent（2019 年 6 月 11 日）新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634472"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>Dynamics 365 for Talent（2019 年 6 月 11 日）新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="search-engine-optimization-for-job-posts"></a>针对工作发布的搜索引擎优化

在 Dynamics 365 for Talent: Attract 管理中心中开启**搜索引擎优化**之后，只要激活并发布新工作或更新现有工作，Attract 都会通知 Google Indexing 应用程序编程接口 (API) 去抓取网页。 这样就会在 Google 和其他搜索引擎的搜索结果中显示该作业。

同样，只要取消发布工作，Attract 就会通知 Indexing API，这样取消发布的工作就会不再在搜索结果中显示。

> [!NOTE]
> Web 爬网程序没有为抓取网页或更新搜索结果定义时间范围。

## <a name="coming-soon-in-attract"></a>Attract 中即将推出

### <a name="job-approvals-appear-on-the-home-page"></a>主页中显示工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。 提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 for Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中介绍的更改适用于内部版本号 8.1.2337。

### <a name="platform-update-27"></a>平台 update 27

有关平台更新 27 的其他详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 27（2019 年 6 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27)。

### <a name="feature-management-workspace-in-talent"></a>Talent 中的功能管理工作区

可使用**系统管理**中的**功能管理**工作区查看、启用、禁用和计划各版本中提供的功能。 默认情况下，新功能处于关闭状态。 可使用**功能管理**工作区开启这些功能并查看其文档。

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

颁发机构实体现在支持自定义字段。

### <a name="new-common-data-service-entities"></a>新增 Common Data Service 实体

增加了任务组实体。

## <a name="in-preview"></a>预览模式

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>仅在沙盒环境中才会启用预览功能。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)。

配置新的 Talent 实例时，可指示实例类型为“生产”还是“沙盒”。 “沙盒”实例类型可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

### <a name="restrict-the-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用人力资源 (HR) 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

## <a name="coming-soon-in-core-hr"></a>Core HR 中即将推出

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>在经理自助服务中查看有关报表性能的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。

### <a name="print-performance-reviews"></a>打印绩效复查

员工、经理和 HR 可以打印员工的绩效复查。
