---
title: Human Resources 客户迁移常见问题解答
description: 本文回答有关将 Microsoft Dynamics 365 Human Resources 迁移到财务和运营合并基础结构的常见问题。
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734350"
---
# <a name="human-resources-customer-migration"></a>Human Resources 客户迁移

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Dynamics 365 Human Resources 客户应如何计划迁移到财务和运营基础结构？

两类 Microsoft Dynamics 365 Human Resources 客户将受到影响，因此必须进行更改，以确保他们在最新的财务和运营基础结构中：

- 使用 Dynamics 365 Human Resources 并且没有 Dynamics 365 中的任何其他运营应用的客户
- 同时使用 Dynamics 365 Human Resources 和 Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 或 Dynamics 365 Project Operations 的客户

无论客户属于哪个类别，客户都必须将数据移到财务和运营基础结构上新创建的环境中，并验证合并是否已成功完成。

今后，Dynamics 365 Human Resources 应用将拥有其自己的财务和运营环境，此环境独立于其他运营应用。 这样，客户将能够利用可扩展性选项，而无需合并其当前数据。 Microsoft 将提供工具和沙盒环境，客户可在迁移到生产环境之前使用所提供的工具和沙盒环境测试和验证数据迁移。 此工具将启用近乎自动化的流程，并且将在 2022 年 8 月到 11 月之间可用。

使用财务和运营基础结构中的其他应用的客户将可以选择将其 Human Resources 数据与现有环境合并。 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>客户何时会迁移到财务和运营基础结构？

每家公司的过渡将取决于该公司当前的配置，以及迁移到财务和运营基础结构的准备情况。 我们建议客户与其 Microsoft 合作伙伴一起确定最佳前进路径。

- 使用 Dynamics 365 Finance 中的 **Human Resources** 模块的组织将能够在常规 One Version 更新过程启用 Dynamics 365 Human Resources 中的新功能。 新功能计划从 2022 年 1 月开始正式发布。
- 使用 Dynamics 365 Human Resources 的组织将有权访问可用于完成基础结构合并的工具。 在过渡时，Microsoft 将与客户合作以帮助防止任何服务中断。 从迁移工具可用时开始，客户将有 12 个月的时间进行转换。
- 同时使用 Dynamics 365 Human Resources 和 **Human Resources** 模块的组织可以将其独立的 Human Resources 基础结构迁移到财务和运营基础结构上。 另一个选项是使用合并工具将环境引入单个环境。 合并这两个环境没有任何要求或时间表。

有关最新信息，请定期查看[发布计划](/dynamics365/release-plans/)。

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>客户是否仍需要在 Dynamics 365 Human Resources 和 Human Resources 模块之间进行自定义集成？

- 同时拥有 Dynamics 365 Human Resources 和当前已集成的其他财务和运营基础架构环境的客户将不得不在合并后继续集成这两个环境。
- 选择将 Dynamics 365 Human Resources 环境与其现有财务和运营应用环境分开的客户将不得不继续集成这些环境，以使数据在这两个环境中都可用。
- 客户可以继续使用数据集成器在为两个环境之间复制数据。 迁移后将数据合并到单个环境中的客户将不必再集成数据，因为所有数据都将位于单个数据库中。

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>客户 ISV 解决方案会自动迁移吗？

每个独立软件供应商 (ISV) 解决方案的迁移体验会不同，具体取决于解决方案的集成方法。 Microsoft 将与 ISV 密切合作，以帮助顺利过渡到财务和运营基础结构。 许多 ISV 解决方案都是使用 Microsoft Power Platform 的功能在 Dataverse 上构建的。 这些解决方案依赖于 Dynamics 365 Human Resources 环境和 Dataverse 环境之间的 Dataverse 集成。 作为基础结构合并的一部分，Dataverse 集成将被弃用。 在财务和运营基础结构中，计划使用新的双重写入映射来取代 Dataverse 集成的功能。

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>在 Dynamics 365 Human Resources 和其他 Dynamics 365 应用之间移动数据的数据集成器将受到怎样的影响？

客户迁移到财务和运营基础结构后，他们将不得不继续在两个环境之间集成数据。 客户可以继续使用数据集成器执行这些数据迁移任务。 计划将 Dynamics 365 Human Resources 环境与其现有财务和运营应用环境分开的客户将不得不继续在这两个环境之间集成数据。 对于将两个环境合并为一个环境的客户，将不再需要两个环境之间的集成。

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>迁移后，如何在财务和运营基础结构上的 Dynamics 365 Human Resources 与 Dataverse 之间移动数据？

作为财务和运营基础结构的一部分，Dynamics 365 Human Resources 和 Dataverse 之间的当前 Dataverse 集成将被弃用。 有计划引入双重写入映射以将财务和运营实体映射到 Dataverse 表。 客户必须决定他们的实施需要哪些双重写入映射。 我们建议将虚拟表用于集成和 ISV 解决方案，除非特定业务需要在 Dataverse 中复制数据以运行业务逻辑。

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>迁移对 Dynamics 365 Human Resources 的 Dataverse 扩展有何影响？

在迁移生产环境之前，客户必须迁移到沙盒环境。 当客户迁移他们的沙盒环境时，他们必须创建其 Dataverse 环境的副本，以连接到新的财务和运营迁移环境。 我们建议客户复制该环境的数据和解决方案，以便它们与客户的当前生产环境匹配。

当客户准备迁移其生产 Dynamics 365 Human Resources 环境时，Microsoft 将自动迁移数据库和 Azure Blob 存储。 迁移的数据库和存储将财务和运营基础结构上的新环境指向相同的生产 Dataverse 环境。 在继续将数据复制到 Dataverse 之前，客户必须启用基于 Dataverse 构建的集成、扩展和 ISV 解决方案所需的任何双重写入映射。

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>基础结构迁移完成后，为 Dynamics 365 Human Resources 生成的 Microsoft Power Platform 组件是否会自动工作？

在 Power Apps 中创建的应用、在 Power Automate 中创建的流以及其他 Microsoft Power Platform 自定义项类似于 Dataverse 扩展。 在客户生产环境迁移过程中，对包括任何扩展在内的 Dataverse 环境没有影响。 应用、流和其他 Microsoft Power Platform 自定义项应该会继续工作，无需额外配置。

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>在迁移期间，Dynamics 365 Human Resources 的 Dataverse 虚拟表实体会怎样？

当客户将其 Dynamics 365 Human Resources 环境迁移到财务和运营基础结构时，该环境将一直连接到当前连接到 Dynamics 365 Human Resources 的 Dataverse 环境。 环境中已生成的 Dataverse 虚拟表将继续工作，无需任何额外配置。 可能必须在连接到客户现有财务和运营环境的 Dataverse 环境中重新生成虚拟表。

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>基础结构合并完成后，使用申请人跟踪系统 (ATS) API、薪资 API、适用于 Dynamics 365 Human Resources 的 Dataverse 虚拟表或 Dataverse Web API 中的其他实体的集成将如何工作？

当客户将其 Dynamics 365 Human Resources 环境迁移到财务和运营基础结构时，该环境将一直连接到当前连接到 Dynamics 365 Human Resources 的 Dataverse 环境。 迁移完成后，针对 Dataverse Web API 开发的任何集成都将继续工作。

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>我们的组织已在 Dynamics 365 Human Resources 中配置自定义安全性。 基础设施迁移完成后是否仍将应用它？

是，自定义安全配置将包含在数据迁移中。

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Dynamics 365 Human Resources 中的工作流是否会自动迁移？

是，工作流配置、工作流历史记录和当前正在进行的工作流都会迁移到合并的基础结构。

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>是否会自动迁移 Dynamics 365 Human Resources 中保存的视图？

是，已保存视图将迁移到合并的基础结构。

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>在基础结构合并后，Dynamics 365 Human Resources 中启用的功能是否会自动可用？

- 对于使用 **Human Resources** 模块的客户，将通过功能管理来管理仅在 Dynamics 365 Human Resources 中可用的功能。 通常，默认情况下不会启用这些功能。 默认情况下必须启用的任何功能都将被记录。
- 对于使用 Dynamics 365 Human Resources 的客户，功能将在基础结构中可用。 将记录不可用的任何功能。 将在合并的基础结构中启用当前 Dynamics 365 Human Resources 环境中启用的每个功能管理密钥。 有关更多信息，请参见[功能管理概述](/fin-ops/get-started/feature-management-overview.md)。

## <a name="what-happens-to-byod-databases-during-the-migration"></a>迁移期间 BYOD 数据库会怎样？

“提供您自己的数据库 (BYOD)”的导入和导出配置将迁移到财务和运营基础结构。

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>客户环境迁移后是否对 Azure 区域有影响？

该 Dynamics 365 Human Resources 环境将保留在同一 Azure 区域以进行迁移。 如果需要将环境移动到不同的 Azure 区域，客户必须在迁移完成后按照标准步骤迁移到新区域。

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>迁移期间 Azure Data Lake 会怎样？

当前在财务和运营应用中为 Azure Data Lake 配置的任何导出在迁移后都将保留相同配置。

> [!NOTE]
> 必须启用双重写入映射才能继续将来自 Human Resources 环境的数据写入 Dataverse。

要将 Human Resources 数据导出到数据湖的客户可以在迁移到财务和运营基础结构后启用此功能。 有关详细信息，请参阅 [Data Lake - Azure 体系结构中心](/azure/architecture/data-guide/scenarios/data-lake)。

客户可以将多个财务和运营环境链接到相同的 Data Lake。 但是，每个环境都将指向其他文件夹和容器。 计划稍后合并环境的客户应仔细计划其方法。
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>如果客户当前正在使用 Human Resources 模块，则需要怎样的迁移？

使用 **Human Resources** 模块的客户将通过标准的 One Version 更新过程将 Dynamics 365 Human Resources 的新功能应用到他们的环境中。 客户可以期待当新功能在每个更新中提供时，会在其环境中看到它。 客户可以使用功能管理来启用这些功能。 客户应计划使用他们已部署并用于验证对其环境的其他更新的流程来验证这些新功能。

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>与外部系统的自定义集成将会怎样？

客户必须将其集成迁移到财务和运营环境。 由于此环境的终结点不同，客户可能必须更新或更改集成，以便集成指向新环境。 此任务将主要是手动流程，所需的更改将取决于集成的体系结构。 客户应与其 Microsoft 合作伙伴一起确定移动集成的最佳方法。

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>如果客户将 Dynamics 365 Human Resources 环境与现有财务和运营环境合并，Microsoft Power Platform (Dataverse) 扩展将会怎样？

如果客户决定在迁移后将 Dynamics 365 Human Resources 环境与现有财务和运营环境合并到单个 Dataverse 实例中，则必须在合并过程中合并其 Dataverse 环境。 此任务将要求在新环境中重新部署使用 Power Apps 创建的任何应用以及任何其他自定义项。

## <a name="what-will-happen-to-documents-during-the-migration"></a>迁移期间文档会怎样？

当客户将 Dynamics 365 Human Resources 环境迁移到财务和运营基础结构时，文档将保留在现有文档存储中，并自动映射到财务和运营基础结构中的新环境。

在以后的版本中，将提供新的数据实体。 进行该更改后，选择将其 Dynamics 365 Human Resources 环境与现有财务和运营环境合并的客户将能够导出文档并将其移动到现有环境中。

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>迁移后，Dynamics 365 Human Resources 中配置的批处理作业会怎样？

必须在财务和运营环境中重新配置批处理作业。 客户必须评估每个批处理作业，并将其与财务和运营环境中的当前批处理作业列表进行比较。 客户在合并两组批处理作业时还应分析整体批处理计划，以确定是否应更改批处理计划、优先级或批处理组。

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>迁移会对 Dynamics 365 Human Resources LCS 项目有怎样的影响？

客户将需要创建一个新的 Microsoft Dynamics Lifecycle Service (LCS) 项目，并且他们必须选择财务和运营应用作为产品，并选择 **实施** 作为项目类型。 此外，创建 LCS 项目时，子项目类型的新字段可用。 客户必须选择迁移 Dynamics 365 Human Resources 的选项，才能将现有 Human Resources LCS 项目迁移到财务和运营基础结构。

财务和运营 LCS 项目的特点不同于 Human Resources LCS 项目的特点。

若要启用，新客户必须完成以下任务：

- 完成项目入门指导。
- 完成方法。
- 填写订阅估算器。
- 完成启用准备情况流程。

## <a name="how-will-the-business-process-modeler-be-migrated"></a>将如何迁移业务流程建模器？

客户将需要从 Human Resources LCS 项目中导出其业务流程建模器库，并将其导入到财务和运营 LCS 项目中。 此外，客户必须更新应用程序中的“帮助”设置，以便其指向新的 LCS 项目。

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>迁移将如何影响服务更新流程？

迁移后，客户将在应用程序生命周期管理 (ALM) 和服务更新方面拥有更大的灵活性。 服务更新将不再自动应用于 Human Resources 环境。 相反，该服务将遵循 One Version 服务更新流程和功能，并且将启用通过 LCS 进行更新的配置选项。

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>客户是否有资格在基础结构合并方面获得 FastTrack 帮助？

Microsoft 仍在确定 FastTrack 将提供具体工具和资源来帮助合并。

## <a name="licensing-impact"></a>许可影响

有关如何影响许可的详细信息，请参阅 [Dynamics 365 Human Resources 基础结构合并](hr-infrastructure-merge.md#licensing)。
