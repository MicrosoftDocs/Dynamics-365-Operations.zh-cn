---
title: 在 Supply Chain Management 和 Field Service 之间集成采购
description: 本主题介绍双写入集成如何支持采购订单的创建以及来自 Supply Chain Management 和 Field Service 的更新。
author: RichardLuan
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d61fdbb8efd8251cac6db7d5acab3caeb03f7879
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346586"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>在 Supply Chain Management 和 Field Service 之间集成采购

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management 提供强大的采购功能。 Dynamics 365 Field Service 提供支持与服务流程关联的采购流程的类似功能。 这两个应用中的功能通过双写入进行集成，并通过表映射、解决方案逻辑、视图和窗体支持生成的跨功能用例。

此集成支持创建采购订单，并在大多数情况下支持两个应用的更新。 但是，Supply Chain Management 控制定价、地址和产品收据。 为同时使用 Field Service 和 Supply Chain Management 的组织支持多个强大的跨功能用例。 这些用例可以跨两个系统发起和跟踪采购。

下图显示了这两个系统中的表以及它们如何相互映射。 Field Service 中的采购订单引用 *帐户* 行，而 Supply Chain Management 中的采购订单引用 *供应商* 行。 为处理集成，双写入使用引用将 *供应商* 行与 *帐户* 行关联起来。 有关详细信息，请参阅[集成供应商主数据](vendor-mapping.md)。

![采购映射。](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>先决条件

要将 Supply Chain Management 与 Field Service 集成在一起，必须安装以下组件：

- Field Service 版本 8.8.31.60 或更高版本，用于全面的采购订单集成
- Supply Chain Management 版本 10.0.14 或更高版本
- 双写入，用于运行 OneFSSCM 解决方案

## <a name="installation-guidelines"></a>安装指南

### <a name="prerequisites"></a>先决条件

- **双写入** – 有关详细信息，请参阅[双写入主页](dual-write-home-page.md#dual-write-setup)。
- **Dynamics 365 Field Service** – 有关详细信息，请参阅[如何安装 Dynamics 365 Field Service](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service)。

在 Microsoft Dataverse 中启用时，双写入和 Field Service 将引入几个解决方案层，它们通过新的元数据、窗体、视图和逻辑扩展环境。 这些解决方案可以按任何顺序启用，通常会按以下给定顺序安装：

1. **Field Service Common** – Field Service Common 在环境中安装了 Field Service 时安装。
2. **Field Service（定位点）** – Field Service（定位点）在环境中安装了 Field Service 时安装。 
3. **Supply Chain Management 扩展版** – Supply Chain Management 扩展版在环境中启用了双写入时自动安装。 
4. **OneFSSCM 解决方案** – 无论最后安装的是哪个解决方案（Field Service 或 Supply Chain Management），都会自动安装 OneFSSCM。

    - 如果环境中已经安装 Field Service，并且您启用了双写入（这会安装 Supply Chain Management 扩展版），将安装 OneFSSCM。
    - 如果环境中已经安装 Supply Chain Management 扩展版，并且您安装了 Field Service，将安装 OneFSSCM。

## <a name="initial-synchronization"></a>初始同步

若要创建新采购订单并处理现有采购订单，必须在 Supply Chain Management 和 Dataverse 之间同步参考数据。 您使用初始写入功能来检测表关系和查找必须为给定映射启用的表。

您必须同步以下表：

- 产品模板

    运行初始写入时，将获得所需表的完整列表。 以下是这些模板的一些示例：

    - 所有产品
    - 已发布产品 V2
    - Dataverse 发布的独特产品

- 站点
- 仓库
- 采购类别模板

    以下是这些模板的一些示例：

    - 采购类别
    - 专业
    - 产品类别层次结构
    - 产品类别分配

- 供应商模板，如“供应商 V2”
- 联系人模板，如“Dataverse 联系人 V2”
- 工作人员模板，如“工作人员”

同步表可确保 Supply Chain Management 中的所有单据（采购订单和产品收据）在 Dataverse 中可用。

### <a name="account-and-vendor-tables"></a>帐户和供应商表

Field Service 中的采购订单依赖“帐户”表来跟踪供应商。 因此，Dataverse 采购订单表使用帐户来跟踪供应商。 为了适应这一主要差异，必须激活以下四个工作流来让帐户和供应商保持同步： 

- 在“客户”表中创建供应商
- 在“供应商”表中创建供应商
- 在“客户”表中更新供应商
- 在“供应商”表中更新供应商

如果安装了 OneFSSCM，由于同时安装了 Field Service 和 Supply Chain Management 扩展版，这些工作流将自动激活。 如果未安装 Field Service，但您想要将采购订单表与 Dataverse 集成，则必须激活这些工作流。 在这两种情况下，除非您从头开始，否则，您都可能必须要确保在创建采购订单之前在 Dataverse 中作为帐户创建所有供应商。 否则，可能会发生错误。

### <a name="initial-synchronization"></a>初始同步

满足所有先决条件之后，如果您希望现有的采购订单和产品收据在两个系统中都可以使用，必须对以下模板执行初始同步：

- 采购订单头 V2
- CDS 采购订单行
- CDS 采购订单行软删除
- 采购订单收货
- 采购订单收货产品

## <a name="mappings-with-logic"></a>使用逻辑进行映射

采购集成使用以下逻辑扩展产品映射，以确保在 Dataverse 中的产品表中正确设置 **Field Service 产品类型** 列：

- 如果 **产品类型** 设置为 *产品*，**物料模型组, 贮存的产品** 设置为 *True*，**Field Service 产品类型** 将设置为 *库存*。
- 如果 **产品类型** 设置为 *产品*，**物料模型组, 贮存的产品** 设置为 *False*，**Field Service 产品类型** 将设置为 *非库存*。
- 如果 **产品类型** 设置为 *服务*，**Field Service 产品类型** 将设置为 *服务*。

此外，Dataverse 还包括用于将供应商与其相关帐户进行映射的逻辑。 此逻辑设置默认发票供应商帐户。 创建时，服务器端插件逻辑从与该帐户相关的供应商设置默认发票供应商帐户。 供应商具有对用于设置此值的发票帐户的引用。

## <a name="supported-scenarios"></a>支持的方案

- 采购订单可以由 Dataverse 用户创建和更新。 但是，流程和数据由 Supply Chain Management 控制。 对 Supply Chain Management 中采购订单列的更新的约束在更新来自 Field Service 时应用。 例如，如果采购订单已完成，则无法进行更新。 
- 如果采购订单由 Supply Chain Management 中的更改管理控制，Field Service 用户则只能在 Supply Chain Management 审核状态为 *草稿* 时更新采购订单。
- 有几列仅由 Supply Chain Management 管理，无法在 Field Service 中更新。 要了解哪些列无法更新，请查看产品中的映射表。 为了简单起见，这些列中的大多数在 Dataverse 页上都设置为只读。 

    例如，价格信息的列由 Supply Chain Management 管理。 Supply Chain Management 有可以使 Field Service 受益的贸易协议。 **单价**、**折扣** 和 **净额** 仅来自 Supply Chain Management。 为确保将价格同步到 Field Service，在输入采购订单数据后，应在 Dataverse  中的 **采购订单** 和 **采购订单产品** 页上使用 **同步** 功能。 有关详细信息，请参阅[按需与 Dynamics 365 Supply Chain Management 采购数据同步](#sync-procurement)。

- **总计** 列仅在 Field Service 中可用，因为 Supply Chain Management 中没有采购订单的最新总计。 Supply Chain Management 中的总计是根据 Field Service 中不可用的多个参数计算得出的。
- 仅指定了采购类别，或所指定产品是 *服务* 产品类型或 Field Service 产品类型的物料的采购订单行，只能在 Supply Chain Management 中启动。 这些行然后会同步到 Dataverse，并且在 Field Service 中可见。
- 如果仅安装了 Field Service，没有安装 Supply Chain Management，**仓库** 列在采购订单上则是强制的。 但是，如果安装了 Supply Chain Management，此要求会放宽，因为 Supply Chain Management 允许有某些情况下未指定仓库的采购订单行。
- 产品收据（Dataverse 中的采购订单收据）由 Supply Chain Management 管理，如果安装了Supply Chain Management，则无法从 Dataverse 创建。 Supply Chain Management 中的产品收据从 Supply Chain Management 同步到 Dataverse。
- Supply Chain Management 中允许欠交。 OneFSSCM 解决方案增加了逻辑，以在创建或更新产品收据行（或 Dataverse 中的采购订单收货产品）时，在 Dataverse 中创建库存日记帐行，以针对欠交的情况调整订单上的剩余数量。

## <a name="unsupported-scenarios"></a>不支持的方案

- Field Service 阻止将行添加到 Supply Chain Management 中已取消的采购订单中。 解决方法是，可以在 Field Service 中更改采购订单的系统状态，然后在 Field Service 或 Supply Chain Management 中添加新行。
- 虽然采购行会影响两个系统中的库存级别，但是此集成不能确保库存跨 Supply Chain Management 和 Field Service 保持一致。 Field Service 和 Supply Chain Management 都有其他更新库存级别的流程。 这些流程在采购范围之外。

## <a name="status-management"></a>状态管理

Field Service 中采购订单的状态与 Supply Chain Management 中的状态不同。

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Service 采购订单和采购订单产品状态

| 标头 – 系统状态 | 标头 - 审核状态 | 物料状态 |
|---|---|---|
| <ul><li>草案</li><li>提交日期</li><li>已取消</li><li>产品已接收</li><li>已结算</li></ul> | <ul><li>空</li><li>批准额</li><li>已拒绝</li></ul> | <ul><li>待处理</li><li>已收货</li><li>已取消</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Management 采购订单和采购订单行状态

仅当存在行工作流时，行审核状态才有效。

| 标头 – 单据状态 | 标头 - 审核状态 | 行状态 | 行审核状态 |
|---|---|---|---|
| <ul><li>未结订单（欠交订单）</li><li>已收货</li><li>已开单</li><li>已取消</li></ul> | <ul><li>草案</li><li>正在审核</li><li>批准额</li><li>已拒绝</li><li>正在进行外部审核</li><li>已确认</li><li>定案</li></ul> | <ul><li>未结订单（欠交订单）</li><li>已收货</li><li>已开单</li><li>已取消</li></ul> | <ul><li>未提交</li><li>正在审核</li><li>批准额</li><li>已拒绝</li></ul> |

以下规则将应用于状态列：

- Supply Chain Management 中的状态无法从 Field Service 更新。 但是，在有些情况下，当 Supply Chain Management 中的采购订单状态更改时，Field Service 中的状态将更新。
- 如果 Supply Chain Management 中的采购订单正在接受更改管理，并且更改正在处理中，审核状态将为 *草稿* 或 *正在审核*。 在这种情况下，Field Service 审核状态将设置为 *Null*。
- 如果 Supply Chain Management 中的采购订单审核状态设置为 *已审核*、*正在进行外部审核*、*已确认* 或 *完成*，Field Service 采购订单审核状态将设置为 *已审核*。
- 如果 Supply Chain Management 中的采购订单审核状态设置为 *已拒绝*，Field Service 采购订单审核状态将设置为 *已拒绝*。
- 如果 Supply Chain Management 中的单据标题状态更改为 *未结订单(欠交订单)*，Field Service 采购订单状态为 *草稿* 或 *已取消*，Field Service 采购订单状态将更改为 *已提交*。
- 如果 Supply Chain Management 中的单据标题状态更改为 *已取消*，并且未将 Field Service 中的采购订单收货产品与采购订单相关联（通过采购订单产品），Field Service 系统状态将设置为 *已取消*。
- 如果 Supply Chain Management 中的采购订单行状态为 *已取消*，Field Service 中的采购订单产品状态将设置为 *已取消*。 此外，如果 Supply Chain Management 中的采购订单行状态从 *已取消* 更改为 *欠交订单*，Field Service 中的采购订单产品物料状态将设置为 *待定*。

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>按需与 Supply Chain Management 采购数据同步

Supply Chain Management 包括处理贸易协议、折扣和其他依赖于 Supply Chain Management 中辅助流程的场景的采购数据。 采购引擎使用复杂的规则来确定给定采购订单的最佳价格。 当您使用双写入时，数据并不总是跨两个环境保持同步，特别是在从 Dataverse 创建或更新行并可能触发 Supply Chain Management 中的跟进流程的情况下。

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>同步 Supply Chain Management 中的采购数据

1. 在 Dataverse 中，转到 **库存 \> 采购订单**。
2. 选择 **新建** 创建新的采购订单，或选择现有采购订单的行。
3. 从采购订单或采购订单行。
4. 在操作窗格上，选择 **同步**。

Supply Chain Management 共享的 Dataverse 和 Field Service 中的所有列都将同步。

以下是您可能会使用 **同步** 功能的情况：

- 如果您从 Dataverse 对同一行进行了多次连续的更改，请运行 **同步** 功能。
- 如果您不确定某个更改是否可能是 Dataverse 中的第二次连续更改，可能需要运行 **同步** 功能。
- 如果从 Supply Chain Management 收到有关更新值的错误消息，请运行 **同步** 功能，然后在 Dataverse 中重试更新。

## <a name="cancelling-the-posting-process"></a>取消发布流程

如果在处理过程中取消了产品收据发布流程，双写入可能会在 Dataverse 中创建产品收据行，但不会在 Supply Chain Management 中创建产品收据行。 发生此情况是因为双写入不支持分布式事务。

## <a name="templates"></a>模板

以下模板可用于集成与采购相关的单据。

| 供应链管理 | Field Service | 说明 |
|---|---|---|
| [采购订单头 V2](mapping-reference.md#183) | msdyn\_Purchaseorders | 此表包含表示采购订单头的列。 |
| [采购订单行实体](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | 此表包含表示采购订单上的行的行。 产品编号用于同步。 这会将产品标识为库存单位 (SKU)，包括产品维度。 有关与 Dataverse 进行产品集成的详细信息，请参阅[统一的产品体验](product-mapping.md)。 |
| [物料收货标题](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | 此表包含在 Supply Chain Management 中发布产品收据时创建的产品收据标题。 |
| [物料收货行](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | 此表包含在 Supply Chain Management 中发布产品收据时创建的产品收据行。 |
| [采购订单行软删除实体](mapping-reference.md#182) | msdyn\_purchaseorderproducts | 此表包含有关已软删除的采购订单行的信息。 如果启用了更改管理，则只有在确认或审核了采购订单后，才能软删除 Supply Chain Management 中的采购订单行。 此行存在于 Supply Chain Management 数据库中，标记为 **IsDeleted**。 由于 Dataverse 没有软删除概念，所以将此信息同步到 Dataverse 非常重要。 这样，在 Supply Chain Management 中被软删除的行可以从 Dataverse 中自动删除。 在这种情况下，在 Dataverse 中删除行的逻辑位于 Supply Chain Management 扩展版中。 |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
