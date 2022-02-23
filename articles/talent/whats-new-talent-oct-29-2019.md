---
title: Dynamics 365 Talent 中的新增功能或更改（2019 年 10 月 29 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529676"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Dynamics 365 Talent 中的新增功能或更改（2019 年 10 月 29 日）

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2586。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>“删除不含角色的当事方”默认应启用 (371233)

在 Talent 中预配新环境时，**如果没有角色则删除当事方** 默认打开。 当您删除工作人员时，除非启用此设置，否则不会删除与该工作人员关联的当事方。 当您需要导入、更改或重新导入工作人员时，此更改将限制全球通讯簿中的重复记录。

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>应允许在 Common Data Service 中删除草稿和已取消的休假请求 (376999)

通过此更改，您现在可以在 Common Data Service 中删除状态为 **草稿** 或 **已取消** 的休假请求。

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>单击自定义字段窗体上的“应用”后，自定义字段中的其他列表值不会反映在 Common Data Service 中 (379599)

当您将新列表值添加到已与 Common Data Service 同步的现有自定义字段时，在 **自定义字段** 窗体中应用更改后，它们现在可在 Common Data Serivce 中提供。

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>存在多个雇用时，跨法人应用入职核对清单 (371270)

在本周的版本中，您可以在 **工作人员窗体 > 核对清单** 中将核对清单应用于具有一个或多个雇用的员工。

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>福利开放登记预览功能已删除

连同我们在[Core HR 的战略投资推动卓越运营](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)博客文章中宣布的消息，Microsoft 已从公开预览中删除福利开放登记功能。 将来会发布新功能。 不支持福利开放登记功能的生产使用。

## <a name="coming-soon"></a>即将到期

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。

### <a name="feature-management-workspace"></a>“功能管理”工作区

每个版本中都会增加和更新功能。 功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。

要了解有关功能管理带来的更改的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。
