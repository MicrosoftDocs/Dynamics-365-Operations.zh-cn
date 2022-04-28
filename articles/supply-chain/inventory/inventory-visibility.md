---
title: 库存可见性加载项概述
description: 本主题介绍库存可见性的定义及其功能。
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eb8a135d2415c867c746a1c40a80cdb84819c0e
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547892"
---
# <a name="inventory-visibility-add-in-overview"></a>库存可见性加载项概述

[!include [banner](../includes/banner.md)]

库存可见性加载项（也称为 *库存可见性服务*）提供了一个独立且高度可扩展的微服务，可跨所有数据源和渠道实现实时的现有库存更改发布和可见性跟踪。 它提供了一个平台，让您可以使用包括（但不限于）以下列表的功能来管理您的全球库存：

- 通过将您的 Supply Chain Management 或第三方物流数据源（如订单管理系统、第三方企业资源计划 \[ERP\] 系统、销售点 \[POS\] 系统和仓库管理系统）连接到库存可见性服务，集中跟踪所有数据源、仓库和位置的最新库存状态（如现有量、已订购、已购买、在途、已退货和已检验）。
- 查询现有存货可用性和短缺情况，以及通过直接调用库存可见性服务来获取即时响应。
- 通过在库存可见性服务中进行实时软预留避免超额销售，尤其是当您的需求来自不同渠道时。
- 通过提供准确的当前或未来可用日期来更好地管理承诺订单和客户期望，以使全渠道可承诺 (ATP) 功能可以计算预期的订单履行日期。

## <a name="extensibility"></a>可扩展性

库存可见性服务具有高度可扩展性，因为数据输入和输出不限于 Microsoft 应用程序。 外部系统可以通过 RESTful 应用程序编程接口 (API) 访问此服务。 除了使用为 Supply Chain Management 数据源和维度提供的现成映射之外，您还可以通过使用配置应用设置其他数据源、库存状态度量值（在库存可见性服务中称为 *实际度量值*）和库存维度将库存可见性与多个第三方系统集成。 通过这种方式，您可以灵活地查询和更改多个数据源和预定义的库存维度

此外，由于库存可见性基于 Microsoft Dataverse 构建，其数据可用于构建 Power Apps 并与之集成。 您还可以使用 Power BI 创建满足您业务要求的自定义仪表板。

## <a name="scalability"></a>可扩展性

库存可见性服务可以向上或向下扩展，具体取决于您的数据量。 可扩展性体验大多是无缝的，由 Microsoft 平台团队根据您的交易数据量的自动检测和评估进行。

## <a name="feature-highlights"></a>功能亮点

### <a name="get-a-global-view-of-real-time-inventory"></a>获取实时库存的全局视图

库存可见性确保您可以随时访问所有渠道、位置和仓库的最新库存数量。 每当您必须获取库存记录时，您将从使用它来支持您的日常运营业务中受益最大。 实际现有库存量、销售数量和购买数量都现成可用。 您还可以根据需要配置其他实际库存度量值（如已退货、已检验和已发布数据），以实时获取这些详细信息。 库存可见性可以有效地处理数百万个库存更改发布。 此数据可以立即聚合并反映在服务中的最新库存数量中，基于每秒或每分钟，具体取决于数据发布的时间间隔。 有关详细信息，请参阅[库存可见性公共 API](inventory-visibility-api.md)。

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>避免所有订单渠道中发生超额销售的软预留

*软预留* 可让您分配或标记特定数量以履行订单或需求。 软预留不会影响实际库存，但会从 *可预留* 库存数量中扣除，将为未来的订单履行提供更新的数量。 如果销售请求或订单从您的记录系统企业资源计划 (ERP) 系统之外的一个或多个渠道或数据源进入您的业务，此功能将非常有用。

如果您未在库存可见性服务中使用软预留，则必须等到订单同步到您的 ERP 系统并由您的 ERP 系统处理才能获得实际库存数量更新。 此过程通常具有巨大的延迟。 但是，每次在您的销售渠道中生成销售请求或订单时，软预留都会立即生效。 因此，它们通过确保您的全渠道订单在最终到达 ERP 系统时不会相互干扰，来帮助防止超额销售情况。 软预留还会确保您可以履行已经承诺的所有订单。 因此，它们可以帮助您满足客户期望并维护客户忠诚度。 有关详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

### <a name="immediate-response-of-atp-dates-confirmation"></a>ATP 日期确认的即时响应

了解您近期的预计库存（包括供应、需求和预计的现有库存详细信息）非常重要，因为它可以帮助您的公司实现以下目标：

- 最小化库存级别以降低库存管理成本。
- 加快内部订单处理，让销售人员可以根据所订购产品的可用性计算装运和交货日期。
- 通过提供下一个可用日期，提供有关客户何时可以期待缺货物料将可用的透明度。

ATP 功能很容易在日常订单履行流程中采用。 最重要的是，与其他库存可见性服务一样，ATP 功能是 *全局和实时的*。 因此，您可以设置多个 ATP 计算公式，来执行覆盖所有业务渠道和数据源的完整的库存可用性查询。 有关详细信息，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md)。

### <a name="compatibility-with-advanced-warehouse-management-items"></a>与高级仓库管理物料的兼容性

Microsoft 旨在提供与高级仓库管理 (WHS) 的现成集成，以便 WHS 客户也可以享受库存可见性服务的好处。 根据 2022 第 1 波版本（3 月的公开预览版），库存服务支持 WHS 物料现有库存查询和 ATP。 下一波中将针对 WHS 客户支持软预留和分配功能。 有关详细信息，请参阅 [WHS 物料的库存可见性支持](inventory-visibility-whs-support.md)。

## <a name="licensing"></a>许可授权

库存可见性服务在以下版本中可用：

- **Microsoft Dynamics 365 Supply Chain Management 的库存可见性加载项** – 对于具有有效 Supply Chain Management 许可证的公司，无需额外的许可证费用即可使用库存可见性。 您今天就可以开始试用了。 有关安装方面的详细信息，请参阅[安装和设置库存可见性](inventory-visibility-setup.md)。
- **作为 IOM 的组件的库存可见性服务** – 此版本适用于未使用 Supply Chain Management 作为 ERP 系统的 Intelligent Order Management (IOM) 客户或公司。 许可证包含在 IOM 捆绑销售中。 有关详细信息，请参阅 [Intelligent Order Management 概述](/dynamics365/intelligent-order-management/overview)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
