---
title: "分类管理"
description: "此主题介绍 Microsoft Dynamics 365 for Retail 中分类管理的基本概念，并提供有关项目的实施注意事项。"
author: jblucher
manager: AnnBe
ms.date: 3/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.translationtype: HT
ms.sourcegitcommit: 44b0c4e39ac7410d27ce531c898bb8c423af334a
ms.openlocfilehash: 303f86d6a57e039cb51700744697949845239b10
ms.contentlocale: zh-cn
ms.lasthandoff: 03/12/2018

---

# <a name="assortment-management"></a>分类管理
[!include[banner](../includes/banner.md)]

## <a name="overview"></a>概览
Microsoft Dynamics 365 for Retail 提供*分类*，供您管理渠道中的产品可用性。 分类决定哪些产品在特定商店和特定时间段内可用。

在 Retail 中，分类是将一个或多个渠道（当使用了组织层次结构时则为渠道组）映射到一个或多个产品（当使用了类别层次结构时为产品组）。

渠道的总体产品组合由分配给该渠道的所发布分类决定。 因此，可以为每个渠道配置多个活动分类。

### <a name="basic-assortment-setup"></a>基本分类设置
在以下示例中，为每个商店配置了一个唯一的分类。 在此情况下，商店 1 中只有产品 1 可用，商店 2 中只有产品 2 可用。

![每个产品在一个商店中可用](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure1.png?raw=true "每个产品在一个商店中可用")

若要让产品 2 在商店 1 可用，可将该产品添加到分类 1。

![产品 2 已添加到分类 1](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure2.png?raw=true "产品 2 已添加到分类 1")

也可以将商店 1 添加到分类 2。

![商店 1 已添加到分类 2](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure3.png?raw=true "商店 1 已添加到分类 2")

### <a name="organization-hierarchies"></a>组织层次结构
如果多个渠道共用同一个产品分类，则可使用零售分类组织层次结构配置分类。 添加此层次结构中的节点时，将包括该节点及其子节点中的所有渠道。

![组织层次结构](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure4.png?raw=true "组织层次结构")

### <a name="product-categories"></a>产品类别
同样，在产品方面，可使用产品类别层次结构包括产品组。 可通过包括一个或多个类别层次结构节点配置分类。 在此情况下，分类将包括该类别节点及其子节点中的所有产品。

![产品类别](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure5.png?raw=true "产品类别")

### <a name="excluded-products-or-categories"></a>排除的产品或类别
除了在分类中包括产品和类别，还可以使用“排除”选项定义分类中应排除的特定产品或类别。 在以下示例中，要包括特定类别中除产品 2 之外的所有产品。 在此情况下，不必逐个产品定义分类或创建更多分类节点。 而是只需包括分类，但排除该产品。

> [!NOTE]
> 如果按照定义某个产品同时在一个或多个分类中既包括又排除，将始终把该产品视为排除。

![排除的产品](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/jblucher-manage-assortments/articles/retail/media/Managing-assortments-figure6.png?raw=true "排除的产品")

### <a name="global-and-released-products"></a>全局产品和已发放产品
分类在全局级别定义，可包含来自多个法人的渠道。 分类中包含的产品和类别也在法人之间共享。 但是，产品必须先发放，才能真正在渠道（例如，销售点 \[POS\]）中出售、订购、盘点或接收。 因此，尽管不同法人的两家商店可以共享包含相同产品的分类，但是这些产品仅当已发放给这些法人时，才可用。

### <a name="dynamic-and-static-assortments"></a>动态分类和静态分类
可以使用特定渠道和产品或通过包括组织单位和类别来定义分类。 包括对这些组的引用的分类视为动态分类。 如果分类处于活动状态时这些组的定义或内容改变，分类的定义也将改变。

例如，最初定义并发布了一个分类，因此其引用一个产品类别。 如果以后向该类别添加更多产品，现有分类的定义中将自动包括这些产品。 您不必手动向分类添加产品。 同样，如果向其他节点添加组织单位，将根据该定义自动调整这个组织单位的分类。

### <a name="stopped-products"></a>已停止的产品 
可通过在**默认订单**设置中开启设置来为销售流程“停止”已发放的产品。 该设置在产品处于使用寿命末期，因此不应在任何渠道出售时最常用。 分类遵守此设置，因此无论分类配置如何，将不为已停止的产品分类。

### <a name="blocked-products"></a>阻止的产品
除了停止销售产品，还可以临时阻止销售产品。 可在已发放产品的**零售**选项卡上配置此设置。 仍将对已阻止的产品分类，但您将在 POS 中收到一条消息，说明不能出售该产品。

### <a name="date-effectivity"></a>日期有效性
分类具有时效性。 因此，零售商可按渠道配置产品何时应可用，何时应不可用。 可提前定义和发布分类，还可以指定开始日期和结束日期。 产品将在指定的日期自动变为可用或不可用。

### <a name="process-assortments-batch-job"></a>处理分类批处理作业
“零售”中定义的分类必须先经过处理，才能生效。 执行此项处理是因为：

- 分类定义必须去常态化，以便可供渠道更容易使用。 可通过跨多个日期范围的多个分类为渠道定义混合产品。 提前在服务器上计算此信息中的一部分时，将提高渠道的绩效。
- 分类中的产品和渠道可在分类本身外部改变。 必须定期处理包含对类别或组织单位的引用的动态分类，以使其根据自己的的当前分配情况包括或排除记录。

## <a name="implementation-considerations"></a>实施注意事项
计划和管理零售实施的分类时，请注意以下实施要求：

- **数据复制和数据库大小** – 虽然分类有助于满足企业对管理产品可用性的需要，却也是管理渠道规模和脱机数据库大小的重要工具。 管理有方的分类可帮助减少必须处理并复制到渠道和脱机数据库的数据量。 还可以帮助减少必须保留的记录数量。 这些数据库中更少的记录将在向交易记录添加项，搜索和浏览产品时提高性能。
- **时效性/到期分类** – 用于管理渠道和脱机数据库中的产品数量的最有效工具之一是分类的时效性。 如果保留季节性产品或处于使用周期结束阶段的产品的开放式（不到期）分类，这些数据库的大小将一直增加下去。 您可以使用各种方法来帮助应对这种情况。 例如，可为季节性产品和始终可用的产品维护单独的分类。
- **分类外销售和退货** – 此功能帮助零售商有效管理分类，方法是将可用产品的数量限制为属于商店核心产品组合的产品。 此功能还可以帮助零售商处理下面的情况：分类中错误地遗漏了某个产品，或者产品因超出分类的有效期而退货。

如果产品数据在渠道数据库中不存在，POS 将实时调用总部数据以检索所需信息，以便出售、退回产品或将产品放入客户订单中。 通过这种方式检索的产品信息只能在交易记录范围内可用。 将不会把产品添加到分类定义。 因此，必须执行后续实时调用。
