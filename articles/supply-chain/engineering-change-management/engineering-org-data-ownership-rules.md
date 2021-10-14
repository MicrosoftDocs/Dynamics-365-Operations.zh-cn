---
title: 工程公司和数据所有权规则
description: 本主题说明如何使用一个或多个工程公司来确保集中创建和维护产品的主数据。 工程公司代表拥有工程产品及其工程相关数据的公司。
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1a05ad1a9d24239e2659c1ffecc21e5e186b1e96
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572905"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>工程公司和数据所有权规则

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>工程公司和运营公司

若要确保集中创建和维护产品的主数据，您可以使用一个或多个 *工程公司*。 工程公司拥有工程产品及其工程相关数据。 它总是连接到（基于）现有的 *法人*，这也是一家公司。 通过此连接，系统为工程公司中工程产品的所有工程相关数据建立一个中央入口点。 在此中央入口点中，将创建工程产品，并维护工程相关数据。 从此入口点中，工程产品和工程相关数据将发布到 *运营公司*，这是其他法人。 （有关发布管理的详细信息，请参阅[发布产品结构](release-product-structure.md)。）这些运营公司将使用由工程公司设计的工程数据。 任何物流数据均由每个工程公司和运营公司在本地维护。

若要创建工程公司，请转到 **工程更改管理 \> 设置 \> 工程组织**。 选择 **新建**，输入工程公司的名称，然后选择所基于的现有公司（法人）。

如果要与外部产品生命周期管理 (PLM) 系统集成，您必须创建将成为外部公司的业务单位（公司类型）。

## <a name="engineering-product-categories-and-engineering-companies"></a>工程产品类别和工程公司

*工程产品类别* 帮助确保根据您公司的业务规则创建工程产品并根据需要运行。 有关工程产品类别的详细信息，请参阅[工程版本和工程产品类别](engineering-versions-product-category.md)。

每个工程产品类别都属于特定的工程公司，并且只能创建属于该公司的产品。 同样，维护工程产品的权限也属于与该产品的工程产品类别相关的公司。

## <a name="data-that-is-owned-by-the-engineering-company"></a>工程公司拥有的数据

因为工程公司拥有工程相关数据，因此它控制以下流程：

- **工程产品的创建：** 每个工程公司只能创建基于其拥有的工程产品类别的新工程产品。 在某些情况下，运营公司将维护与这些产品相关的自己的本地数据。
- **工程版本的创建：** 当公司创建新的工程产品时，系统将自动为其创建初始工程版本。 只有拥有的工程公司才能创建该产品的新版本。
- **工程属性的创建和维护：** 当公司创建新的工程产品时，系统将自动向其添加工程属性。 只有拥有的工程公司才能创建和维护这些属性的值。 有关工程属性的详细信息，请参阅[工程属性和工程属性搜索](engineering-attributes-and-search.md)。
- **连接到工程版本的物料清单 (BOM) 的创建和维护：** 拥有的工程公司可以将 BOM 直接连接到工程产品版本。 当将这些 BOM 发布给其他法人时，将通过以下方式限制对 BOM 上工程数据的更改：

    - 运营公司无法删除已发布的 BOM 行。
    - BOM 行上的工程字段对于运营公司是只读的。 所有其他字段均为物流实施字段，可以由运营公司进行编辑。
    - 运营公司可以将 BOM 行添加到同一 BOM 中。 这样，它可以添加本地附加项，例如包装材料或润滑液。
    - 运营公司可以添加全新的本地 BOM。 例如，在发布期间未提供 BOM 的情况下，可能需要进行此更改。 运营公司拥有和维护这些本地 BOM。 有关发布管理的详细信息，请参阅[发布产品结构](release-product-structure.md)。
    - 当工程公司更新其 BOM 时，将保留所有本地 BOM 和 BOM 行。

- **连接到工程版本的工艺路线的创建和维护：** 工程公司可以将工艺路线直接连接到每个工程版本。 当将这些工艺路线发布给其他法人时，将通过以下方式限制对工艺路线上数据的更改：

    - 其他法人无法删除工艺路线上的工程数据。
    - 其他法人可以向工艺路线添加工序。 这样，他们可以添加本地工艺路线步骤。
    - 运营公司可以添加全新的本地工艺路线。 例如，如果在发布期间未包括工艺路线，可能需要进行此更改。 运营公司拥有和维护这些本地工艺路线。 有关发布管理的详细信息，请参阅[发布产品结构](release-product-structure.md)。
    - 当再次向工艺路线发布工程公司的更新时，将保留在本地进行的所有更改。

- **工程文档的创建和维护：** 工程公司可以将工程文档附加到每个工程版本。

    - 当向其他法人发布这些文档时，将保护文档以免被运营公司删除。
    - 其他法人可以添加全新的本地文档。 运营公司拥有和维护这些本地文档。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]