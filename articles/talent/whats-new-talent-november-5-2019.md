---
title: Dynamics 365 Talent 中的新增功能和更改（2019 年 11 月 5 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778374"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Dynamics 365 Talent 中的新增功能和更改（2019 年 11 月 5 日）

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2598。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="copy-a-core-hr-instance"></a>复制 Core HR 实例

在本周的发布中，您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Talent: Core HR 数据库复制到沙盒环境。 如果您有另一个沙盒环境，还可以将数据库从该环境复制到目标沙盒环境。 有关详细信息，请参阅：

- “Dynamics 365: 2019 发布波次 2 计划”中的[更广泛的环境管理](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)

- Talent 文档中的[复制 Core HR 实例](hr-copy-instance.md)

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>启用 Common Data Service 集成后，不创建 Common Data Service 集成批处理作业 (388030)

启用此更改后，将为 Common Data Service 集成创建批处理作业。

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity 在上载时不调整人员图像的大小 (369469)

本周的发布更改了通过数据管理导入图像时如何调整图像大小以改善效果。

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>职位的“可用于分配日期”可以早于“启用日期”(340103)

进行此更改后，如果您选择早于职位**启用日期**的**可用于分配日期**，会出现警告。

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>无法在基于步骤的计划的员工自助服务中创建薪酬更改请求 (376872)

此发布更正了通过基于步骤的计划的员工自助服务请求薪酬更改时出现的问题。 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>如果描述超过 30 个字符，原因码将不同步到 Common Data Service，Core HR 允许 60 个 (352682)

进行此更改后，将在 Common Data Service 中更新具有 30 个以上字符的原因代码。 Common Data Service 中所做的更改也将反映在 Talent 中。

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>从 Talent 到 Finance and Operations 的地址集成 (351961)

此发布修复了在 Talent 中更新的地址不在 Finance and Operations 中更新的问题。 对地址块的更改现在将更新。

## <a name="coming-soon"></a>即将到期

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。

### <a name="feature-management-workspace"></a>“功能管理”工作区

每个版本中都会增加和更新功能。 功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。

要了解有关功能管理带来的更改的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。
