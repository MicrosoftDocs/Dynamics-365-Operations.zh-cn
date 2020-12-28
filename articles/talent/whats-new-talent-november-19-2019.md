---
title: Dynamics 365 Talent 中的新增功能或更改（2019 年 11 月 19 日）
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527136"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Dynamics 365 Talent 中的新增功能或更改（2019 年 11 月 19 日）

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Talent 中的新增功能或更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2621。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Finance and Operations 应用平台更新 31

有关详细信息，请参阅 [Finance and Operations 应用平台更新 31 的预览功能（2020 年 1 月）](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31)。

### <a name="feature-management-workspace-383856"></a>功能管理工作区 (383856)

**功能管理** 工作区提供了每个版本提供的功能列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。 有关功能管理的更多信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在 **功能管理** 工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。
 
有时，完整功能默认启用，并且无法关闭（例如，**功能管理** 工作区）。
 
某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理** 工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>当职位存在已取消的操作时会出现消息 (382887)

当您选择一个特定职位并且该职位只有已取消的操作时，不再显示以下消息：**职位 xxxxxx 有未完成的操作正在进行**。

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>在学习分析中，“课程类型”和“状态”显示不正确的数据 (381151)

本周发布的版本更新了学习分析，可以正确显示 **课程类型** 和 **状态**。

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>人员编号应显示在“新工作人员”窗体横幅中 (383832)

现在，在 **新工作人员** 窗体中，**人员编号** 显示在横幅中，以供快速参考。

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>职位开始日期确定在雇用期间检索薪酬级别时要使用的职位记录 (350361)

在此版本中，**薪酬开始日期** 确定分配给新职位的级别。

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>职位表中的自定义选择列表字段未同步到 Common Data Service (387503)

在此版本中，选择列表项现已与 Common Data Service 同步。

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>导入新数据时，工作地址实体未与 Common Data Service 同步 (349673)

在本周的发布中，地址数据现在在导入新数据时与 Common Data Service 同步。

## <a name="in-preview"></a>预览模式

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。
