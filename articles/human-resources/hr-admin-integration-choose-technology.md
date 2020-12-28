---
title: 选择数据集成技术
description: 本文介绍如何与 Human Resources 管理的数据集成。 其介绍可帮助您决定哪些技术最适合您的需要的不同集成技术。
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528333"
---
# <a name="choose-a-data-integration-technology"></a>选择数据集成技术

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍如何与 Dynamics 365 Human Resources 管理的数据集成。 其介绍可帮助您决定哪些技术最适合您的需要的不同集成技术。

## <a name="data-integration-background"></a>数据集成背景

业务数据是使您的公司与众不同的关键资产。 您的业务数据非常有价值。 可使用通过业务收集的数据之间的关系改进业务流程和组织中的业务智能。 无论系统来自何处，我们都致力于提供轻松、安全、稳定访问您的业务数据的方法。

从历史上看，在多个系统之间集成数据一直很困难。
Microsoft 正在采取措施使数据集成变得更加容易，朝着该目标迈出的一大步是通过 [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)。

Human Resources 正在使 Common Data Service 成为 Human Resources 数据的首选公共接口。 随着时间的推移，我们期望 Human Resources 管理的所有最重要数据都将在 Common Data Service 中公开。 我们推荐 Common Data Service 作为大多数集成应用程序的首选技术。

我们发现 Common Data Service 可能尚不包含您的应用程序所需全部数据。 我们还发现您的项目时间线可能需要备用技术。 如果 Common Data Service 不能满足您的集成需要，请务必告诉我们。

## <a name="integration-technologies"></a>集成技术

以下各节介绍可用于 Human Resources 的不同数据集成技术。

### <a name="common-data-service-entities"></a>Common Data Service 实体

Common Data Service 是 Human Resources 的首选公共数据接口。 其源自 Dynamics 365 XRM 平台，后者由 [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) 解决方案使用。

Common Data Service 为数据实体提供平台和 API。 部署 Human Resources 时，其将连接到 Common Data Service 实例。 Human Resources 数据的实体部署到该 Common Data Service 实例中。 这些实体及其数据可供可连接到 Common Data Service 实例的任何应用程序使用。 Human Resources 与 Common Data Service 实体同步数据。

集成应用所需数据实体位于 Common Data Service 中时，可充分使用[其支持的 Common Data Service 和 API](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer)。 在受支持的 API 中，[Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api) 提供了用于访问 Common Data Service 数据的 OData 实现。

Common Data Service 实体及其关联的 API 是从 Web 应用程序、Web 服务/API 以及连接到 OData 源的任何其他应用程序访问 Human Resources 数据的最佳选择。

> [!NOTE]
> 决定将 Common Data Service 作为 Human Resources 的首选数据接口是相对较新的，您可能会发现，集成所需的 Human Resources 数据实体在 Common Data Service 中尚不可用。
</br>
> 有关 Common Data Service 中可用的 Human Resources 实体的列表，请参阅 [Human Resources 和 Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities)。
> </br>
> 如果集成所需的 Human Resources 实体尚不可用，则需要等待数据实体可用，或者需要使用下面介绍的其他集成技术之一。
> </br>
> 默认情况下，Common Data Service 集成在不包含提供的演示数据的新环境中处于关闭状态。 它将在包含演示数据的新环境中打开，环境将在预配好后开始同步数据。 环境准备好可以同步数据后，可以打开集成。

### <a name="dmfdixf-entities"></a>DMF/DIXF 实体

Human Resources 主要基于与 Finance and Operations 应用程序相同的平台构建，并提供[数据管理框架 (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)。 DMF 也称为数据导入导出框架 (DIXF)。 Human Resources 提供一组数据实体，可用于导入和导出 Human Resources 数据。 尽管 Common Data Service 实体是 Human Resources 的首选数据集成接口，但 DMF 实体在某些情况下仍然有用，例如：

- Common Data Service 实体尚不可用。

- 集成需要高性能的批量数据导入/导出功能。

DMF 实体当前为 Human Resources 数据提供最完整的数据覆盖。

DMF 不适用于实时集成，如用户界面中立即需要用户反馈时。 包操作是计划的批处理作业，在批处理服务选择要执行的作业之前通常至少有 1-2 分钟的延迟，还有完成导入/导出操作所需的任何时间。

当需要高吞吐量时（例如每晚计划导入/导出成千上万条记录），DMF 可能是最佳选择。

> [!NOTE]
> DMF 对 Attract 和 Onboard 不可用。

### <a name="dmf-package-rest-api"></a>DMF 包 REST API

DMF 提供用于处理数据包的 [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api)。 此 API 可用于以编程方式与 DMF 交互，从而允许诸如以下操作：

- 导入数据包。

- 导出数据包。

- 检查导入/导出操作的状态。

DMF 包 REST API 在 Human Resources: Core HR 中完全受支持。

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF 还提供强大的功能（称为[提供您自己的数据库](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)或 BYOD），从而允许 Human Resources 将数据导出到您自己的 Microsoft Azure SQL 数据库。 此功能提供了极大的灵活性。 当数据存在于您自己的 SQL 数据库中时，您可以利用可以连接到 SQL 数据存储的任何应用程序或中间件。

BYOD 主要是只读解决方案。 尽管您可以在 Azure SQL 数据库中处理和存储所需的任何数据（例如进行数据混合），但是存储在 Azure SQL 数据库中的数据将不会同步到 Human Resources。

作为 [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) 管道的数据源，BYOD 适用于报告解决方案、数据集成、数据混合。

> [!NOTE]
> BYOD 对 Attract 和 Onboard 不可用。

### <a name="odata-enabled-entities"></a>启用 OData 的实体

大多数 DMF 实体也可以通过 Human Resources 数据服务 (OData) 进行访问。 为 [Finance and Operations OData 服务](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata)提供的文档适用于 Human Resources，但创建您自己的公开 OData 实体时除外。

虽然 Common Data Service 和 Common Data Service 提供的 OData 实现（通过 [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))）优先于 Human Resources 数据服务，但 Human Resources 数据服务当前对于 Human Resources 数据的实体覆盖更完整。

### <a name="excel-add-in"></a>Excel 加载项

[Excel 加载项](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json)在后台利用启用 OData 的实体。 它为最终用户提供一种方便的方式，可以通过熟悉的 Excel UI 检索和修改 Human Resources 数据。

Excel 加载项适用于业务领域专家的专门数据导入/导出。 对于需要程序自动化的重复数据集成，另一种集成技术会更合适。

### <a name="data-integrator"></a>数据集成器

可使用[数据集成器服务](https://docs.microsoft.com/powerapps/administrator/data-integrator)集成与 Common Data Service 之间往来的数据。 数据集成器可以用于定义集成项目（通常基于应用程序开发人员针对特定集成定制的预定义模板）。 可以将集成项目计划为按重复执行的计划自动运行或手动运行。

数据集成器项目适用于 Common Data Service 批处理集成。 它们非常适合 Dynamics 365 系列应用程序之间的集成。 例如，Microsoft 提供了一个数据集成器模板，用于将 Human Resources 中的数据集成到 Dynamics 365 Finance。 可以在 [Dynamics 365 Human Resources 与 Dynamics 365 Finance 的集成](hr-admin-integration-finance.md)中了解有关该模板的详细信息。

### <a name="power-query"></a>Power Query

数据集成器通过其[高级查询功能](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)支持 [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query)。 Power Query 提供强大、灵活的数据筛选和转换，包括丰富的 M 配方语言。 如果您已经部署过 Power BI 报表，很可能熟悉 Power Query。

## <a name="deciding-on-an-integration-technology"></a>决定集成技术

由于有许多不同的集成技术可供使用，因此决定使用哪种集成方法有时会令人不知所措。 随着 Common Data Service 中数据覆盖的成熟，这一决定将变得更加容易，因为 Common Data Service 在大多数情况下是首选的数据接口。 但在那之前，您可能会发现 Common Data Service 还不能满足您的需求。 下表总结了各种集成技术选项的关键特性。

| 技术/工具/API    | 定期集成                   | 同步/异步                    | 通过 API 进行编程访问        | 适当的数据卷                                   | 数据覆盖                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service 实体           | 是，使用数据集成器或中间件 | 同步异步，批处理（通过数据集成器） | 是，通过 Dynamics 365 Web API (OData) | 因使用案例而异（交互使用支持分页） | 正在改进<sup>2</sup>                       |
| DMF 实体           | 是，通过中间件计划        | 异步，批处理                                | 是，通过 DMF 包 REST API         | 高（成千上万条记录）                    | 高                                |
| DMF 包 REST API   | 是，通过中间件计划        | 异步，批处理                                | 是                                       | 高（成千上万条记录）                    | API 支持所有 DMF 实体       |
| BYOD                   | 是，由 Human Resources 中的管理员计划        | 异步，批处理                                | 否<sup>3</sup>                                    | 高（成千上万条记录）                    | 支持所有 DMF 实体           |
| 启用 OData 的实体 | 是，使用中间件                    | 同步                                        | 是，通过 Human Resources 数据服务 (OData)  | 因使用案例而异（交互使用支持分页） | 高                                |
| Excel 加载项           | 否                                       | 同步                                        | 否                                        | 中（成千上万条记录）                      | 支持所有启用 OData 的实体 |
| 数据集成器        | 是，在数据集成器中计划        | 异步，批处理                                | 否                                        | 因使用案例而异                                       | 支持所有 Common Data Service 实体           |

<sup>2</sup>Microsoft 正大力投资以增加 Common Data Service 实体的数据覆盖。 建议实现覆盖后使用 Common Data Service。 目前，Common Data Service 相对于 DMF 和启用 OData 的实体，数据覆盖较低。

<sup>3</sup>可以通过编程方式访问 SQL 数据库。
