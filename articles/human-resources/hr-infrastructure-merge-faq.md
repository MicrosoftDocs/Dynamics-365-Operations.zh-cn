---
title: Dynamics 365 Human Resources 基础结构合并常见问题
description: 本主题回答有关 Microsoft Dynamics 365 Human Resources 和 Finance and Operations 应用的基础结构合并的常见问题。
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee4fea9b67ff8a0c8d813940a65cf882bd13abe
ms.sourcegitcommit: bf2daeccbe3f2826e734f409bfc823820144aa23
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617983"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources 基础结构合并常见问题

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题回答有关 Microsoft Dynamics 365 Human Resources 和 Finance and Operations 应用的基础结构合并的常见问题。

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>什么是 Dynamics 365 Human Resources 基础结构合并？

Dynamics 365 Human Resources 是一个独立的应用程序，使用与其他 Finance and Operations 应用不同的基础架构，如 Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 和 Dynamics 365 Project Operations。 基础结构合并将 Dynamics 365 Human Resources 引入与其他 Finance and Operations 应用相同的基础结构。

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>基础结构合并的价值和好处

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>我的组织使用 Dynamics 365 Human Resources 管理 HR 运转。 我们将从这些更改中获得哪些好处？

- 这些更改将消除 Dynamics 365 中的多组人力资源 (HR) 功能。
- 它们既既提供 Microsoft Power Platform 可扩展性，也提供扩展业务逻辑和功能选项的方法。
- 它们在应用程序生命周期管理 (ALM)、Microsoft Dynamics Lifecycle Services (LCS)、地理可用性、可扩展性等方面使 Dynamics 365 Human Resources 与其他 Finance and Operations 应用保持一致。
- 它们让您可以利用共享服务和工具，并帮助降低成本。

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>我的组织在 Dynamics 365 Finance、Supply Chain Management、Commerce 或 Project Operations 中使用 Dynamics 365 Human Resources。 我们将从这些更改中获得哪些好处？

在 Dynamics 365 Human Resources 中创建的功能和投入的投资现在可供使用 Dynamics 365 Finance 中的 HR 模块的客户使用。 其中一些功能包括休假和缺勤管理、福利管理和任务管理。

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>我是否会丢失当前使用的功能或能力？

Dynamics 365 Human Resources 和 Finance and Operations 应用中的 HR 模块之间在功能上是等同的。 Dynamics 365 Human Resources 将优先使用相似功能。 有关更多信息，请参见[功能管理概述](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

### <a name="will-the-experience-change-for-my-users"></a>我的用户的体验是否会改变？

新的 HR 功能将通过功能管理进行管理。 将由客户决定是否要接受它们。 在某些情况下，功能可能会被修改。 在这些情况下，将提供文档。

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>如果我是现有客户，我通过自定义集成同时使用 Finance and Operations 基础架构上的 HR 模块和 Dynamics 365 Human Resources，此更改会对我有哪些影响？

不需要再在 Dynamics 365 Human Resources 和 Dynamics 365 Finance 中的 HR 模块之间进行自定义集成。 所有 HR 数据将与其他 Finance and Operations 应用驻留在同一数据库中。

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>从 Dynamics 365 Human Resources 迁移到 Finance and Operations 应用

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>我的组织使用 Dynamics 365 Human Resources 管理 HR 运转。 要迁移到新体验，我们必须进行哪些计划？

如果您的组织使用 Dynamics 365 Human Resources，但不使用任何其他 Finance and Operations 应用，您的 Human Resources 环境将迁移到新的基础结构。 此迁移过程的大部分都将自动化。 需要制定迁移数据库并将其与新基础结构同步的流程。

此外，需要准备好工具，以便您可以在迁移生产环境之前测试迁移流程，并验证您的数据和体验。

如果您的组织同时使用 Dynamics 365 Human Resources 和其他 Finance and Operations 应用，您应该计划更多时间进行验证以确保您的数据正确迁移到新环境。 迁移到新基础结构会将来自您的 Human Resources 环境的数据与您的 Finance and Operations 环境合并。 需要准备工具，以尽可能多地自动执行数据合并流程。 但是，冲突数据实例需要用户输入来定义应如何解决冲突。 用户和管理员必须管理存在冲突的数据映射，并在生产环境迁移之前测试沙盒环境中的迁移。

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>我的组织在 Dynamics 365 Finance、Supply Chain Management、Commerce 或 Project Operations 中使用 Dynamics 365 Human Resources。 要迁移到新体验，我们必须进行哪些计划？

对于在 Finance and Operations 应用中使用 HR 模块的组织，Dynamics 365 Human Resources 的新功能将通过标准的 One Version 更新流程应用于您的环境。 您可以期待当新功能在每个更新中提供时，你会在您的环境中看到它。 您可以使用功能管理打开新功能。 但是，您应该计划验证这些功能。 请按照您为验证环境的其他更新而制定的流程操作。 有关如何将更新应用于 Finance and Operations 应用的详细信息，请参阅 [One Version 概述](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md)。

### <a name="when-will-my-organization-be-migrated"></a>我的组织会在何时迁移？

每个组织的迁移取决于其当前配置和迁移到新基础结构的准备情况。 这些日期会发生更改。

- 当前使用 Finance and Operations 应用中的 HR 模块的组织将作为常规 One Version 更新流程的一部分收到 Dynamics 365 Human Resources 的 HR 功能。 新功能计划从 2021 年 10 月开始正式发布。
- 目前仅使用 Dynamics 365 Human Resources 的组织有权访问迁移工具，以便他们可以开始测试，然后从 2022 年年中开始迁移。 必须迁移到新基础结构的截止日期尚未确定。 但至少是在迁移工具可用之日之后至少一年。
- 目前同时使用 Dynamics 365 Human Resources 和其他 Finance and Operations 应用的组织有权访问迁移工具，以便他们可以开始测试，然后从 2022 年年末开始迁移。 必须迁移到新基础结构的截止日期尚未确定。 但至少是在迁移工具可用之日之后至少一年。

有关 Dynamics 365 Human Resources 的新功能的详细信息，请参阅 [Human Resources 中的新增功能或更改](./hr-admin-whats-new.md)。

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>我正在使用仅在 Dynamics 365 Human Resources 中可用的新功能（如 **休假和缺勤** 和 **福利管理**）。 这些功能现在在 Finance and Operations 基础结构上的 Human Resources 模块中也可用吗？

是的，Dynamics 365 Human Resources 的所有模块都将在 Finance and Operations 应用中按原样运行，功能 100% 等同。 作为当前在 HR 中使用这些功能的客户的整体迁移策略的一部分，客户数据将被迁移，以让它继续在 Finance and Operations 基础结构中工作。

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>我使用新的 Dynamics 365 Human Resources 福利管理功能。 我在 Finance and Operations 基础结构上构建了与 HR 模块的自定义集成，以便我可以通过使用福利数据来利用工资单功能。 这些自定义集成以后会需要吗？

作为基础结构合并的一部分，HR 数据与其他 Finance and Operations 应用被引入同一个数据库。 Finance and Operations 应用中的模块之间不再需要集成。

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>我的组织将一个或多个 ISV 解决方案与 Dynamics 365 Human Resources 结合使用。 我们的 ISV 解决方案是否会自动迁移？

每个独立软件供应商 (ISV) 解决方案的迁移体验会不同，具体取决于解决方案的集成方法。 Microsoft 将与 ISV 紧密合作，确保顺利转换到新基础结构。

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>我的组织使用 LinkedIn Talent Hub 与 Dynamics 365 Human Resources 的集成。 完成基础结构更改后，此集成是否会继续工作？

是，迁移到新基础结构后，LinkedIn Talent Hub 集成将继续工作。

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>我的组织使用 Teams 的 Human Resources 应用。 完成基础结构更改后，此应用是否会继续工作？

是，迁移到新基础结构后，Teams 的 Human Resources 应用将继续工作。

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>我的组织已在 Dynamics 365 Human Resources 中配置自定义安全性。 完成基础结构更改后，我们的自定义安全性是否仍会应用？

是，自定义安全配置将包含在向新基础结构的数据迁移中。

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>我们使用数据集成器在 Dynamics 365 Human Resources 和 Finance and Operations 应用之间移动数据。 当前正在集成的数据会受到怎样的影响？

当前在 Dynamics 365 Human Resources 中掌握的 HR 数据将与 Dataverse 同步。 然后可以使用数据集成器与 Finance and Operations 应用进行单向同步。 迁移到新基础结构后，HR 数据将是 Finance and Operations 应用的本地数据。 数据集成器将不再需要在 Finance and Operations 应用和 Human Resources 之间同步数据。

Human Resources 的当前 Dataverse 本地数据表将继续在新基础结构上同步环境中的数据。 实体将转换为支持双重写入。 通过数据集成器针对其他 Dynamics 365 应用的这些表配置的任何其他数据集成将继续工作，因为它们当前已配置。

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>我们使用双重写入在 Dataverse 和其他 Finance and Operations 应用之间移动 HR 数据。 当前正在集成的数据在迁移到新基础结构时会受到怎样的影响？

HR 数据将是新基础结构上环境中的 Finance and Operations 应用的本地数据。 然后将使用双重写在新环境与 Dataverse 环境之间移动 HR 数据。

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>我们已经构建了从 Dynamics 365 Human Resources 到一个或多个外部系统的自定义集成。 完成基础结构更改后，我们是否需要开发新集成？

这取决于集成终结点。 有关 Finance and Operations 应用中可用的集成技术以及如何选择最佳集成技术的详细信息，请参阅[集成概述](../fin-ops-core/dev-itpro/data-entities/integration-overview.md)。

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>我们为 Dynamics 365 Human Resources 扩展了 Dataverse。 这些扩展是否会自动迁移？

如果将加入新基础结构上的环境中的 Dynamics 365 Human Resources 和 Finance and Operations 环境连接到同一个 Dataverse 环境，迁移后这两个应用将继续连接到同一个 Dataverse 环境。 因此，任何 Dataverse 扩展都不需要迁移。

但是，如果 Dynamics 365 Human Resources 和 Finance and Operations 环境当前连接到单独的 Dataverse 环境，两个 Dataverse 环境必须合并，以让它们连接到新基础结构上的单个环境。 对于此 Dataverse 迁移，Human Resources 决方案标准 Dataverse 表可以连接到新 Dataverse 环境并与新环境重新同步。 但是，Dataverse 环境的任何扩展都不会自动迁移，而必须在新环境中重新部署。 我们建议您使用托管解决方案来管理您的 Dataverse 扩展。 有关详细信息，请参阅[解决方案简介](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions)。

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>我们已将 Microsoft Power Automate 流和/或 Microsoft Power Apps 配置为与 Dynamics 365 Human Resources 配合使用。 在完成基础结构更改后，这些 Microsoft Power Platform 组件是否会迁移并自动工作？

Power Apps、Power Automate 流和其他 Microsoft Power Platform 自定义与 Dataverse 扩展类似。 它们在迁移到新基础结构后是否自动工作取决于 Human Resources 应用和 Finance and Operations 应用是否在迁移前连接到同一个 Power Apps 环境。

如果应用当前连接到同一个 Power Apps 环境，在迁移到新基础结构后，它们将继续连接到该 Power Apps 环境。 在这种情况下，Power Apps，Power Automate 流和其他 Microsoft Power Platform 自定义将继续工作，无需任何额外配置。 我们建议您使用托管解决方案来管理 Dataverse 上的应用程序扩展。 有关详细信息，请参阅[解决方案简介](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions)。

但是，如果 Human Resources 应用和 Finance and Operations 应用连接到单独的 Power Apps 环境，它们则必须作为迁移的一部分合并。 此任务将要求在新环境中重新部署任何 Power Apps 和其他自定义。

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>我们已为 Dynamics 365 Human Resources 启用了 Dataverse 虚拟表。 迁移期间这些表将会怎样？

迁移后，如果新基础结构上的环境仍然连接到当前连接到 Dynamics 365 Human Resources 的 Dataverse 环境，在该环境中生成的 Dataverse 虚拟表将继续工作，无需任何额外配置。

但是，如果迁移后新基础结构上的环境连接到不同的 Dataverse 环境，则必须在新 Dataverse 环境中重新生成虚拟表。

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>我们已经使用申请人跟踪系统 (ATS) API、工资单 API、Dynamics 365 Human Resources 的 Dataverse 虚拟表或 Dataverse Web API 中的其他实体开发了一个集成。 完成基础结构更改后，这些集成是否会继续工作？

迁移后，如果新基础结构上的环境仍连接到当前连接到 Dynamics 365 Human Resources 的 Dataverse 环境，针对 Dataverse Web API 开发的任何集成都将在迁移完成后继续工作。

但是，如果新基础结构上的环境在迁移后连接到不同的 Dataverse 环境，则必须重新配置针对 Dataverse Web API 开发的任何集成，让它们连接到新的 Dataverse 环境。

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>我的环境迁移后是否对 Azure 区域有影响？

预计您的 Human Resources 环境在迁移期间通常会继续在同一个 Azure 区域中。 如果 Human Resources 环境将与位于不同区域的 Finance and Operations 环境合并，则会出现唯一的例外。 在这种情况下，Human Resources 环境将迁移到 Finance and Operations 环境的 Azure 区域。

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>我的组织依赖 Dynamics 365 Human Resources 中的工作流来处理一个或多个业务流程。 这些工作流是否会自动迁移？

是，工作流配置、工作流历史记录和当前正在进行的工作流都会迁移。

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>哪些培训和资源可用来帮助执行迁移流程？

我们将提供完整文档来详细介绍迁移流程的每个步骤。 其他培训资源（如视频和研讨会）也可能会提供，具体取决于需求。

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>我的组织在 Dynamics 365 Human Resources 中创建了已保存视图以提高界面的可用性。 已保存视图是否会自动迁移？

是，已保存视图将迁移到新的基础结构。

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>我们现在将 Ceridian 与 Dynamics 365 Human Resources 结合使用。 完成基础结构更改后，Ceridian 集成是否可用？ 

与 Ceridian 的集成将迁移到基于工资单 API 的集成。 Dynamics 365 Human Resources 中当前存在的基于文件的集成不会迁移到 Finance and Operations 基础结构。 有关详细信息，请参阅[工资单 API 简介](./hr-admin-integration-payroll-api-introduction.md)。

### <a name="how-will-the-migration-affect-the-service-update-process"></a>迁移将如何影响服务更新流程？

迁移之后，客户在 ALM 和服务更新方面将具有更大的灵活性。 服务更新将不再自动应用于 Human Resources 环境。 而是遵循 One Version 服务更新流程和功能。 因此，更新的配置选项将通过 LCS 提供。 有关详细信息，请参阅 [One Version 概述](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md)。

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>迁移会对我的 Dynamics 365 Human Resources LCS 项目有怎样的影响？

迁移到新基础结构会将 Dynamics 365 Human Resources 环境的管理转移到 LCS 实施项目中。 如果迁移将 Dynamics 365 Human Resources 与现有 Finance and Operations 环境合并，您的 Human Resources LCS 项目将合并到 Finance and Operations 应用的 LCS 实施项目中。 如果您当前仅使用 Dynamics 365 Human Resources，将会创建新的 LCS 实施项目，您现有的 Human Resources LCS 项目将迁移到新项目。

新项目将与 Finance and Operations 应用使用的项目类型相同。 它将具有相同的环境管理功能。 有关详细信息，请参阅 [Lifecycle Services 资源](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)。

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>我们已将任务录制链接到 Human Resources 中的业务流程建模器。 业务流程建模器将如何迁移、合并到 LCS 中？

LCS 项目的业务流程库将迁移到新的 Human Resources LCS 项目。

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>我的组织当前仅使用 Dynamics 365 Human Resources。 有哪些资源可以让我们在基础结构更改完成后了解更多的开发能力？

Microsoft Power Platform 可扩展性选项和 Finance and Operations 可扩展性选项都将会提供，可以用于开发。 有关详细信息，请参阅[开发和自定义主页](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md)。

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>我们在 Dynamics 365 Human Resources 中启用了功能。 迁移期间是否将自动启用这些功能？

是否在新基础结构中自动启用功能将针对每项功能单独确定。 此信息将包含在功能文档中。

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>迁移期间我的 BYOD 数据库会怎样？

“提供您自己的数据库 (BYOD)”的导入和导出配置将迁移到新的基础结构。

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>迁移期间我的 Azure Data Lake 会怎样？

当前在 Finance and Operations 应用中为 Azure Data Lake Storage 配置的任何导出在迁移后都将保留相同配置。

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>我们当前在使用 Dynamics AX 2012。 当前可用的升级工具是否可用于将 AX 2012 中的 HR 模块升级到 Dynamics 365 Human Resources？

是。 Dynamics 365 Human Resources 将包含在 Finance and Operations 应用的合并代码库和基础结构中。 从 Dynamics AX 2012 升级到 Dynamics 365 Human Resources 将使用与升级到最新版本 Finance and Operations 应用相同的升级路径和工具。

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>我们使用 Dynamics 365 Human Resources 的文档处理。 迁移期间文档会怎样？

文档将保留在现有文档存储中。 它们将重新映射到新基础结构中的环境。

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>迁移后，我们在 Dynamics 365 Human Resources 中配置的批处理作业会发生什么变化？

适用的批处理作业将自动迁移到新基础结构。

## <a name="licensing-impact"></a>许可影响

此文档不会取代或替换任何覆盖使用权利的法律文档。

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>我的组织使用 Dynamics 365 Human Resources 管理 HR 运转。 我们的许可或成本是否会改变？

已购买 Dynamics 365 Human Resources 许可证的客户不会受到影响。 这些客户不存在许可迁移。 特定于 Human Resources 的其他沙盒库存单位 (SKU) 不再适用。 客户可以选择以略低的成本购买 Finance and Operations 应用第 2 层沙盒。 已购买 Human Resources 沙盒的现有客户将迁移到 Finance and Operations 应用第 2 层沙盒，没有额外成本。

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>我的组织在 Dynamics 365 Finance、Supply Chain Management、Commerce 或 Project Operations 中使用 Dynamics 365 Human Resources。 我的许可或成本是否会改变？

Dynamics 365 应用的现有用户和独立 Dynamics 365 Finance、Supply Chain Management、Commerce 和 Project Operations 的用户可以在 2025 年 2 月或当前许可协议到期前（以较早者为准），作为这些许可证的一部分访问 Human Resources。 如果能够帮助您实现更好的成本节省，您可以选择提前转移到 Human Resources 许可证。 从 2025 年 2 月开始，所有现有的 CSP 和 EA 客户都必须退出 HR 模块，购买 Human Resources 许可证，以利用 Finance and Operations 应用中引入的新功能。

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>我的组织使用 Dynamics 365 Finance、Supply Chain Management、Commerce 或 Project Operations 运转。 是否需要购买其他环境以支持基础结构合并？

不需要其他环境来支持基础结构更改。

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>如果我对产品许可有其他问题，我应该去哪里询问？

如果您有许可问题，您可以在 [Biz 应用中心 – D365 定价和许可](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering)中找到更多信息。 如果该信息对您的问题没有帮助，请使用 LicenseQ 提交请求。
