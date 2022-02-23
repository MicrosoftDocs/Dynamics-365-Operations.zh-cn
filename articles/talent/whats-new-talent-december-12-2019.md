---
title: Dynamics 365 Talent（2019 年 12 月 10 日）中的新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528163"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Dynamics 365 Talent（2019 年 12 月 10 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2660。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="feature-management-workspace"></a>“功能管理”工作区

**功能管理** 工作区提供了每个版本提供的功能列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。 有关功能管理的更多信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在 **功能管理** 工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。
 
有时，完整功能默认启用，并且无法关闭（例如，**功能管理** 工作区）。
 
某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理** 工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>简化的工作人员窗体已移至“功能管理”工作区 (390583)

进行此更改后，现在可以在 **功能管理** 工作区启用简化的工作人员窗体。 此功能已从 **系统管理** 中的 **系统参数** 窗体移走。

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>在没有工作人员值时阻止 HcmWorkerPayrollInfo 记录写入 (394526)

在此版本中，如果此场景中没有工作人员引用，将不再创建 **HcmWorkerPayrollInfo** 记录。 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>当操作无法完成时，不填充与操作关联的消息日志 (374007)

此版本包括一项更改，可以在某些情况下在操作失败时填充操作消息日志。 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Common data service 集成批处理作业创建 (388030)

进行此更改后，启用服务后，将创建 Common Data Service 集成的批处理作业。

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>单击自定义字段窗体上的“应用”后，自定义字段的其他领料单值不会反映在 Common Data Service 中 (379599)

进行此更改后，现在当您应用更改时，Talent 中输入的新领料单值将同步到 Common Data Service。

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>针对休假银行交易记录实体的 Common Data Service 更新在 Talent 一端变成插入内容 (352938)

此更改更正了对休假银行交易记录的更新在 Talent 中创建新记录的问题。

## <a name="in-preview"></a>预览模式

仅在 **沙盒** 环境中才能使用预览功能。

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。

