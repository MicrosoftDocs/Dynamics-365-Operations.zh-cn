---
title: "优化顾问概述"
description: "此主题描述如何使用优化顾问来帮助保证 Microsoft Dynamics 365 Finance and Operations 的最佳配置。"
author: roxanadiaconu
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c055c673443255f3e6dda5e1179e1ef28d90e693
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="optimization-advisor-overview"></a>优化顾问概述

[!include[banner](../includes/banner.md)]

此主题描述如何使用优化顾问来帮助保证 Microsoft Dynamics 365 Finance and Operations 的最佳配置。

## <a name="overview"></a>概览

模块的不正确配置和设置可能对 Finance and Operations 功能的可用性、系统性能和业务流程的顺畅使用造成负面影响。 业务数据的质量（例如，数据的正确性、完整性和清洁）还会影响系统性能，以及组织的决策制定能力和效率等。

**优化顾问**工作区是一个工具，让高级用户、业务分析师、功能顾问和 IT 支持职能部门发现模块配置和业务数据中的问题。 优化顾问建议模块配置的最佳实践并确定废弃或不正确的业务数据。

优化顾问会定期运行一组最佳实践规则。 有一组默认规则随 Microsoft Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）一起发布。 但是，用户也可以创建特定于其自定义、来自独立软件供应商 (ISV) 的解决方案和业务数据的规则。 有关如何创建规则的详细信息，请参阅[创建新规则](./create-rules-optimization-advisor.md)。

在检测到违反规则时，优化机会将生成并显示在**优化顾问**工作区中。 用户可以直接从**优化顾问**工作区采取适当的纠正措施。

机会可以是公司特定或跨公司的，具体取决于所验证的设置和数据的类型。 跨公司机会可以从所有公司查看。 若要查看特定公司的机会，必须首先选择公司。

优化机会应用标准安全政策。 例如，与**仓库管理**模块的配置相关的优化机会仅对有权访问“仓库管理”且可以更改其设置的用户可见。

当您对一些优化机会采取行动时，系统将计算机会对业务流程运行时间减少的影响。 很遗憾，此功能不能用于所有优化机会。

若要了解有关“优化顾问”的详细信息，请观看视频短片 [Dynamics 365 for Finance and Operations 中的顾问优化](https://www.youtube.com/watch?v=MRsAzgFCUSQ)。

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

## <a name="optimization-rules"></a>优化规则

要查看优化顾问规则的完整列表并了解规则的评估频率，请转到**系统管理** &gt; **定期任务** &gt; **维护诊断验证规则**。 仅对具有**活动**状态的规则进行评估。 评估频率可以设置为**每日**、**每周**、**每月**或**未计划**。

若要触发对未计划规则的评估，或在预定义的计划外重新评估定期规则，转到**系统管理** &gt; **定期任务** &gt; **计划诊断验证规则**。 然后，在**诊断规则验证**对话框中，选择评估频率。 具有指定频率的所有规则都将重新评估。

当前的优化规则设置可划分为以下几个类别。

### <a name="module-configuration-and-setup"></a>模块配置和设置

仓库管理设置是一个复杂的过程。 为了让这个过程更简单，引入了某些规则来帮助验证设置的正确性。 例如，有一个规则验证销售订单和转移单的固定产品变型位置的仓库库位指令的设置。

此外，某些规则检查是否实际使用了已启用的功能。 例如，有一个规则确定您是否在使用**主计划**模块。 如果规则确定您未使用此模块，优化机会将生成以建议您关闭计划流程。

### <a name="system-configuration"></a>系统配置

如果未使用由 Configuration Key 控制的特定功能，优化机会将生成以建议您禁用 Configuration Key。 Configuration Key 的示例包括**实际称重**、**预算计划**、**项目**和**核准供应商列表**。

### <a name="business-data-consistency-and-cleanup"></a>业务数据的一致性和清理

如果主数据不正确（例如，如果您有未定义单位的度量单位转换，或者您有除以 0 \[零\] 的度量单位转换），优化机会将生成以建议您更正数据。 

如果您的批处理作业历史记录条目、废弃项目、已启用仓库物料的关闭的现有条目等太多，或者如果这些条目和项目过旧，优化机会将生成以建议您清理数据。 通过保持数据的清洁，您可以帮助改善整个系统的性能。

### <a name="best-practices"></a>最佳实践

如果您未根据最佳实践运行某些业务流程（例如，如果您在库存结转之前运行库存预结转，或者，如果您为子分类帐日记帐批处理转移使用计划的批处理），优化机会会通知您最佳实践并要求您照其执行。

## <a name="optimization-opportunities"></a>优化机会

若要查看在优化规则评估时创建的优化机会，打开**优化顾问**工作区。

在此工作区，您可以通过选择**更多信息**查看与机会有关的详细信息。 如果您希望系统采取措施、更正设置、清洁数据等，以便您无需自己打开相应页面，选择**采取措施**。

优化机会没有工作流。 在您选择**采取措施**或使用**更多信息**对话框中提供的导航路径后，优化机会将从列表中消失。 如果该更正操作未完全解决问题，机会将在下次评估规则时再次生成。

如果机会不适用于您的角色，您可以选择**从我的列表中隐藏**。 即使此机会背后的规则后以后再次触发，您也不会在您的列表中看到此机会。

若要禁用特定规则的评估，选择由规则生成的机会，然后选择**禁用分析**。

## <a name="see-also"></a>请参阅

[创建新规则](./create-rules-optimization-advisor.md)

[Dynamics 365 for Finance and Operations 中的优化顾问（视频）](https://www.youtube.com/watch?v=MRsAzgFCUSQ)

