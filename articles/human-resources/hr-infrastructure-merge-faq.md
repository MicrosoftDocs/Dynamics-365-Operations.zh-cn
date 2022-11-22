---
title: Dynamics 365 Human Resources 基础结构合并常见问题
description: 本文回答有关 Microsoft Dynamics 365 Human Resources 与财务和运营应用的基础结构合并的常见问题。
author: twheeloc
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7325231718d7387450391b16b2866f9a2c05bdc4
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779627"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources 基础结构合并常见问题

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>什么是 Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources 提供了一些工具，用于帮助 HR 团队提高组织敏捷性、转换员工体验和优化 HR 计划，以创建可供人员和企业茁壮成长的工作场所。 要了解有关 Dynamics 365 Human Resources 的详细信息，请参阅 [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/)。

- **转换员工体验。** 通过推动敬业度和增长的互联自助服务体验来帮助经理和员工，从而留住业绩最佳员工。
- **优化 HR 计划。** 降低运营成本，并创建以人为本的休假和缺勤、时间、福利和薪酬管理计划。
- **提高组织敏捷性。** 通过使用 Dataverse 和 Microsoft Power Platform 集中人员数据并轻松扩展 Dynamics 365 Human Resources，使 HR 能够以业务所需的灵巧度进行运作。
- **发现劳动力见解。** 通过在任何设备上都可用的大量仪表板上分析和显示人员数据的功能，做出数据驱动型决策。

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>基础结构合并的价值和好处

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>什么是 Dynamics 365 Human Resources 基础结构合并？

目前在 Dynamics 365 中的两个不同基础结构上有两组单独的 HR 功能：

- **Dynamics 365 Human Resources** - 在独立基础结构上运行的独立应用。 启动此应用后，基础结构将与其他 Dynamics 365 运营应用分离。 我们的客户使用此应用来提高组织敏捷性、优化 HR 计划、转变员工体验并获得劳动力见解。
- **HR 模块** - 一组旧版功能，以前是 Unified Operations 许可库存单位 (SKU) 的一部分。 HR 模块在财务和运营基础结构上运行，这在所有运营应用中都相同。 这些应用包括 Dynamics 365 Finance、Dynamics 365 Project Operations 和 Dynamics 365 Supply Chain Management。 客户获得了 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 中的 HR 功能。

在过去三年中，Microsoft 没有向 HR 模块添加任何新功能或增强功能。 相反，我们的路线图投资重点已放在 Dynamics 365 Human Resources 应用上。

通过将这两组功能引入同一基础结构，我们将帮助客户获得以下好处：

- 在过去三年中添加到 Dynamics 365 Human Resources 的增强功能，包括增强的休假和缺勤、福利管理和报告。
- 通过 Microsoft Power Platform 提高的可扩展性，以及扩展业务逻辑以个性化页面的功能。
- 改进的部署、更新和维护，它们在应用程序生命周期管理 (ALM)、Lifecycle Services、地理可用性等方面是一致的。
- 更多的技术创新（因为我们的工程团队使用了共享服务和工具并且降低了平台成本）。

此转换将影响当前使用 Dynamics 365 Human Resources 或旧版 HR 模块的客户。

## <a name="glossary-of-terms-used-in-this-faq"></a>此常见问题解答中使用的术语词汇表

- **Dynamics 365 Human Resources** - 我们的向市场提供 HR 功能的当前和未来产品。
- **HR 模块** - 一组以前通过 Unified Operations 产品获得许可的旧功能。 这些功能在客户拥有 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 时已启用。
- **财务和运营基础结构** - 运营产品组合使用的开发体系结构，包括 Dynamics 365 Finance、Dynamics 365 Supply Chain Management 和 Dynamics 365 Project Operations。 该基础结构是未来将使用的基础结构。 在此常见问题解答中，*合并的基础结构* 一词是指财务和运营环境。
- **人力资源基础结构** - 过去用于 Dynamics 365 Human Resources 应用的开发体系结构。 基础结构合并项目将 Dynamics 365 Human Resources 引入到财务和运营基础结构。 将停止使用独立的基础结构。

## <a name="general-questions-about-the-infrastructure-merge"></a>有关基础结构合并的一般问题

### <a name="will-customers-lose-any-features-or-capabilities"></a>客户会失去任何功能吗？

我们的目标是尽量减少此过渡对客户的影响。 我们不会删除任何特性或功能。 Dynamics 365 Human Resources 和 HR 模块之间在功能上是等同的。 如果两个基础结构中都存在某个功能，则将使用 Dynamics 365 Human Resources 体验。

### <a name="will-the-user-experience-change"></a>用户体验是否会改变？

用户体验将与标准 Dynamics 365 平台体验一致。 尽管仪表板和菜单的一般体验将保持相似，但它将与标准 Dynamics 365 Finance 应用体验保持一致。 导航将包括模块和工作区，允许使用收藏夹等等。 Dynamics 365 Human Resources 工作区（如 **人事管理** 和 **人员**）将合并到财务和运营基础结构上。 将来，将通过功能管理提供新功能，让客户能够查看新功能并决定他们想要使用的功能。 有关详细信息，请参阅[功能管理概览](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)和[用户界面文档](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json)。

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>何时将完成 Dynamics 365 Human Resources 基础结构合并？

基础结构合并将分阶段推出，以便客户有时间计划并完成必要的步骤。 我们在 Dynamics 2021 版本第 2 波中已开始推出这些功能。 我们计划在 2022 年第 2 波发布结束前完成该项目的所有产品开发工作。 请注意，日程表可能会发生更改。 有关最新信息，请查看[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance)。

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>哪些培训和资源可用来帮助执行基础结构合并？

我们将提供文档来详细描述基础结构合并过程中的每个步骤。 我们将根据需要提供额外的培训资源，例如视频和研讨会，以帮助客户和合作伙伴顺利过渡。

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>基础结构合并完成后，开发功能会有变化吗？

要详细了解开发功能，请参阅[开发和自定义主页](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md)。

## <a name="feature-availability-questions"></a>功能可用性问题

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>LinkedIn Talent Hub 集成是否适用于财务和运营基础结构？

不，LinkedIn Talent Hub 集成不是合并的基础结构的一部分。 公共应用程序编程接口 (API) 可用于生成与招聘和申请人跟踪解决方案的集成。 计划使用 LinkedIn Talent Hub 的客户应与其 Microsoft 合作伙伴一起使用提供的 API 进行集成。 有关申请人跟踪系统 (ATS) 集成 API 的更多信息，请参阅[申请人跟踪系统集成 API 介绍](./hr-admin-integration-ats-api-introduction.md)。

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>合并完成后，当前仅在 Dynamics 365 Human Resources 中可用的功能（例如，休假管理和福利管理）是否可用？

是。 所有 Dynamics 365 Human Resources 应用程序功能都将引入到财务和运营基础结构中。 这些功能将在阶段性方法中提供。 有关合并基础结构的功能可用性的最新信息，请定期查看[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance)。

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>基础结构合并完成后，Ceridian 与 Dynamics 365 Human Resources 的集成是否可用？

Ceridian 正在创建与 Dynamics 365 Human Resources 的 V2 集成，以利用工资单 API。 Dynamics 365 Human Resources 中当前存在的基于文件的集成不会迁移到财务和运营基础结构。 有关详细信息，请参阅[工资单 API 简介](./hr-admin-integration-payroll-api-introduction.md)。

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>是否包括员工功能中的申请人跟踪或入职/离职？

在以前的版本中，我们创建了 ATS 集成 API，以使合作伙伴和客户能够创建与 Human Resources 的 ATS 集成。 其他 ATS 相关功能在 2022 年第 1 波中提供。 我们将在以后的版本中继续增强这些 API。

财务和运营基础结构中当前存在的 HR 功能包括 Dynamics 365 Human Resources 中不存在的一些招聘管理功能。 基础结构合并完成后，所有 Human Resources 客户都可以使用此功能。 此功能提供轻量级 ATS 功能。 但是，我们不打算将来扩展此功能。 需要更高级功能的客户可以利用合作伙伴 ATS 集成。 有关 ATS 集成 API 的更多信息，请参阅[申请人跟踪系统集成 API 介绍](./hr-admin-integration-ats-api-introduction.md)。

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>是否将使用 Dynamics AX 2012 升级工具将 AX 2012 中的 HR 模块升级到 Dynamics 365 Human Resources 应用？

是。 从 Dynamics AX 2012 升级到 Dynamics 365 Human Resources 将遵循用于升级到最新版本的其他 Dynamics 365 运营应用（例如 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management）的相同升级路径和工具。

有关迁移到财务和运营基础结构的详细信息，请参阅 [Human Resources 客户迁移常见问题解答](./customer-migration.md)。
