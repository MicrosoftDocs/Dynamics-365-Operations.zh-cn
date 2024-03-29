---
title: 带仓库管理的实际称重产品处理
description: 本文介绍如何使用工作模板和货位指令确定在仓库中如何以及在哪里完成工作。
author: perlynne
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench, WHSCatchWeightTagRegistration, WHSCatchWeightTagFullDimDiscrepancies, WHSCatchWeightTagChangeWeightDropDownDialog, WHSCatchWeightLinkWorkLineTagDropDownDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 881c3c4aa655a5ad30adffce108ba2fc3e6691c5
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070400"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>使用仓库管理进行实际称重产品处理

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>功能曝光

若要使用仓库管理处理实际称重产品，必须使用许可证配置键打开功能。 转到 **系统管理 \> 设置 \> 许可证配置**。 然后，在 **配置键** 选项卡上，展开 **贸易 \> 仓库和运输管理**，然后选择 **面向仓库的实际称重** 复选框。

> [!NOTE]
> 还必须打开 **仓库和运输管理** 许可证配置键和 **流程分配 \> 实际称重** 许可证配置键。 要设置实际称重的配置键，还必须使用 **功能管理** 工作区打开此功能。 必须打开的主要功能是 **使用仓库管理进行实际称重产品处理**。 **实际称重产品的库存状态更改** 和 **在将生产订单报告为完工入库时使用现有的实际称重标记** 是您可能希望开启，但可选的两项相关功能。

在许可证配置键打开后，在您创建已发放产品时，您可以选择 **实际称重**。 您还可以将发放的产品与为其选择了 **使用仓库管理流程** 参数的存储维度组关联。

您必须为实际称重进行某些基本产品的特定设置，然后才可以在“仓库管理”中使用产品：

- 在单位转换定义中定义实际称重单位（箱）和库存单位（千克）\[kg\] 之间的标称重量转换。
- 在实际称重单位设置中，定义最小和最大重量容差。
- 设置实际称重单位定义为最低库存单位 (SKU) 的单位序列组。
- 设置实际称重物料处理策略。

有关详细信息，请参阅[设置和维护实际称重物料](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)。

## <a name="transaction-adjustments"></a>交易记录调整

由于库存重量在涉及到仓库时可能不同于库存从仓库发放时的重量，所以实际称重产品处理必须调整库存。

> [!NOTE]
> 仅当物料的实际称重物料处理策略的出库重量差异方法为 **允许重量差异** 时，移动设备活动才会触发交易调整。

### <a name="example-1"></a>示例 1

在 **完工入库** 生产流程中，包含八箱实际称重产品的牌照的入库重量捕获为 80.1 千克。 牌照之后存储在成品区域，存储期间，部分重量在空气中流失。

之后，在销售订单领料流程中，同一个牌照的重量捕获为 79.8 千克。 因此，在系统中，您现在在物理维度设置中将有重量差异。

在这种情况下，系统将通过过帐缺少的 0.3 千克的交易记录来自动调整此差异。

### <a name="example-2"></a>示例 2

在其定义中，产品被设置为最多允许 **箱** 实际称重单位的最小 8 千克重量、最大 12 千克重量。

您有两箱产品，它们登记的重量为 16 千克。 如果仓库工作人员领取其中一箱并称重，重量捕获为 9 千克，另一箱重量将为 7 千克。 但是，因为 7 千克低于最小重量，系统将执行自动调整，将现有库存重量增加 1 千克。

若要设置这些调整所过帐到的科目，请转到 **成本管理 \> 分类帐集成策略设置 \> 过帐**。 然后，在 **库存** 选项卡上，定义以下科目：

- 实际称重损失科目
- 实际称重利润科目

## <a name="catch-weight-item-handling-policy"></a>实际称重物料处理策略

实际称重物料处理策略定义物料的两个主要仓库管理流程：何时捕获物料重量，以及如何捕获。

您可以定义什么时候为销售和转移单处理捕获重量。 重量可以在以下流程的任意一个流程期间捕获：

- **领料** – 重量在订单工作的初始领料工作行期间捕获。
- **装箱** – 重量在人工装箱期间捕获。 （必须将物料发送到装箱工作站。）

如果实际重量在集装箱装箱流程期间在装箱工作站捕获，在领料工作期间，将不提示仓库工作人员捕获重量。 物理库存的平均重量被用作转到装箱区域的已领取库存的重量。 此概念也适用于通过标签跟踪的实际称重物料。 对于标签跟踪的物料，这些参数确定捕获标签的时间。 可以在领料时使用移动设备捕获标签，也可以在手动装箱过程中捕获标签。

> [!NOTE]
> 因为 **装箱** 选项会导致库存被平均已领料重量更新，所以这可能会引起差异，从而导致实际称重损/益调整，并且/或者现有库存重量和实际称重标签重量之间存在差异。

对于内部流程，如盘点和调整更正，可以确定是否应捕获重量。 如果未捕获，则会使用标称重量。 利用其他选项，您可以按实际称重单位和盘点数量来捕获重量。

您还可以定义如何捕获重量。 在两个主要流之一，实际称重标记被跟踪并用于捕获重量。 在另一个流中，不跟踪实际称重标记。

- **是** – 物料使用实际称重标记。 每个标记编号表示一个实际称重单位（箱），重量以及其他信息与标记关联。 对于出库流程，使用与标记关联的重量。
- **否** – 物料不使用实际称重标记。 入库和出库称重流程基于在每个流程中捕获的实际重量。

跟踪实际称重标记的流程可以用于存储期间不会更改重量的物料。 重量将仅在入库仓库流程中捕获。 在出库流程中，将只扫描实际称重标记，与这些标记关联的重量将用于出库交易处理。

与实际称重标签处理有关的另一个重要参数是 **实际称重标签维度跟踪方法**。 标签可以部分跟踪，也可以完全跟踪。 如果部分跟踪标签，则将跟踪产品维度、跟踪维度和库存状态。 如果完全跟踪标签，则将跟踪产品维度、跟踪维度和 **所有** 存储维度。

此外，对物料进行标签跟踪时，存在一个 **出库标签捕获方法** 参数。 您可以设置此参数，以便始终提示您输入来自移动设备的出库交易标签。 另外，您可以设置参数，以便仅在需要标签时才提示您输入标签。 例如，在给定的牌照上，库存中有五个实际称重标签，并且您已指示要从牌照中选择所有这五个标签。 在此例中，如果 **出库标签捕获方法** 参数设置为 **仅在需要时提示输入标签**，则会自动选择这五个标签。 您不必扫描每个标签。 如果参数设置为 **总是提示输入标签**，那么即使选择了所有五个标签，也必须扫描每个标签。

> [!NOTE]
> 通常，仅通过移动设备菜单项捕获并更新标签。 但是，在某些情况下，会在其他位置捕获标签（例如，从人工装箱工作站捕获）。 但是，通常，如果使用标签，则应将移动设备菜单项用于所有仓库活动。

### <a name="how-to-capture-catch-weight"></a>如果捕获实际称重

**在使用实际称重标签跟踪时**，必须始终为收到的每个实际称重单位创建标签，并且每个标签必须始终与重量关联。

例如，**箱** 是实际称重单位，您将收到一个托盘（八箱）。 在这种情况下，必须创建八个唯一的实际称重标记，并且重量必须与每个标记关联。 根据入库实际称重标记，可以捕获全部八箱的重量，然后可以将平均重量分配到每箱，也可以为每箱捕获唯一重量。
在使用 **在将生产订单报告为完工入库时使用现有的实际称重标记** 功能并通过移动设备菜单项启用了流程时，将根据现有实际称重标记更新库存。 因此，在将生产报告为完工操作时，仓库管理移动应用不会提示捕获实际称重标签数据。

**在不使用实际称重标签跟踪时**，可以针对每个维度集捕获重量（例如，对每个牌照和跟踪维度）。 或者，重量可以基于聚合级别捕获，如五个牌照（托盘）。

对于捕获出库重量的方法，您可以使用 **每个实际称重单位** 选项指定应为每个实际称重单位（例如，每箱）进行称重。 利用 **每个领料单位** 选项，您可以指定应根据将要领料的数量（例如，三框）来捕获重量。 请注意，对于生产订单行领料和内部移动流程，如果使用了 **未捕获** 选项，将使用平均重量。

根据实际称重物料处理策略定义了多种重量捕获方法。 各种交易会使用每个重量捕获方法参数。 下表总结了哪些交易使用哪些参数。

| 方法                                     | 交易                                |
|--------------------------------------------|--------------------------------------------|
| 出库重量捕获方法           | 销售领料，转移领料            |
| 生产领料重量捕获方法 | 生产领料，生产消耗 |
| 变动重量捕获方法           | 变动                                   |
| 何时捕获重量更正       | 调整，盘点                      |
| 计数重量捕获方法           | 盘点                                   |
| 仓库转移重量捕获方法 | 仓库转移                         |

若要阻止仓库管理领料流程捕获会导致实际称重损/益调整的重量，可使用出库重量差异方法。 出库重量差异方法在以下移动设备过程中适用：销售领料、转移领料、生产领料、移动、盘点和仓库转移。 如果实际称重物料的重量在仓库存储期间没有发生波动，并且不需要进行实际称重损/益调整，则可以使用 **限制重量差异** 选项。 如果重量会发生波动，并且在记录重量波动时需要进行实际称重损/益调整，则可以使用 **允许重量差异** 选项。

## <a name="unsupported-scenarios"></a>不支持的方案

并非所有工作流都支持使用仓库管理进行实际称重产品处理。 当前应用以下限制。 它们适用于所有实际称重物料，无论是有标记。

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>针对仓库管理流程配置实际称重产品

- 实际称重产品（不是物料清单）仅支持配方处理。
- 实际称重产品不能使用所有者维度与跟踪维度组关联。
- 实际称重产品不能作为服务使用。
- 实际称重产品只能作为物料模型组的一部分用作“贮存产品”。
- 实际称重产品不能与此功能一起用于跟踪“在销售流程中有效”。
- 实际称重产品不能与此功能一起用于捕获序列号。 因此，产品不能作为领料/装箱流程的一部分从“空白”转为序列号。
- 实际称重产品不能与此功能一起用于在消耗前登记序列。
- 启用变量的实际称重产品不能与此功能一起用于转换不同的度量单位。
- 实际称重产品不能标记为商业“产品配套件”。
- 实际称重产品只能与具有实际称重处理单位且将实际称重单位作为最低序列的单位序列组一起使用。
- 实际称重产品的条码设置不支持可变重量设置。

### <a name="order-processing"></a>订单处理

- 发货通知（ASN/装箱结构）的创建不支持重量信息。
- 订单数量必须基于实际称重单位维护。

### <a name="inbound-warehouse-processing"></a>入库仓库处理

- 接收牌照需要重量在登记时分配，因为重量信息不支持作为发货通知的一部分。 在使用实际称重标记流程时，标记编号必须按实际称重单位手动分配。
- 实际称重产品不支持入库质量检查工作。 如果已配置，则将跳过质量检查工作。

### <a name="inventory-and-warehouse-operations"></a>库存和仓库操作

- 实际称重产品不支持手动创建检验单。
- 实际称重产品不支持手动移动与未完成工作相关的库存。
- 实际称重产品不支持加载来初始化仓库库存的牌照。
- 实际称重产品不支持批次平衡流程。
- 实际称重产品不支持处理负实际库存。
- 库存标记不能用于实际称重产品。

### <a name="outbound-warehouse-processing"></a>出库仓库处理

- 实际称重产品不支持群集领料功能。
- 实际称重产品不支持领料和装箱仓库处理。
- 对于实际称重产品，在工作模板中定义的工作无法自动运行。
- 对于实际称重产品，系统不支持在集装箱关闭后创建已装箱集装箱领料工作的手动装箱工作站处理。
- 实际称重产品不支持逐件扫描功能。

### <a name="production-processing"></a>生产处理

- 对于实际称重产品，仅支持配方产品的批次订单。
- 实际称重产品不支持看板功能。
- 对于实际称重产品，序列号不能在消耗前登记。
- 实际称重产品不支持从生产冲销牌照的功能。
- 对于实际称重产品，完工入库不能通过序列号注册。

### <a name="transportation-management-processing"></a>运输管理处理

- 实际称重产品不支持装载计划工作台处理。
- 实际称重产品不支持运输请求行。

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>使用仓库管理的实际称重产品处理的其他限制和行为

- 在没有提示用户标识跟踪维度的领料流程中，重量分配基于平均重量进行。 例如，此行为在以下情况下发生：在同一位置使用跟踪维度组合，并且在用户处理领料后，该位置只剩一个跟踪维度值。
- 在库存为针对仓库管理流程 (WMS) 配置的实际称重产品预留时，预留将基于定义的最小重量进行，即使此数量是现有的最后一个处理数量。 此行为与未为 WMS 配置的物料的行为不同。 此限制有一个例外。 对于生产领料，当序列号控制的实际称重产品的最后一个处理量被领料后，将使用实际重量。
- 将重量作为产能计算（波次阈值、工作最大休息时间、集装箱最大数、货位负荷产能等）的一部分使用的流程不使用库存的实际重量。 流程基于为产品定义的实际处理重量。
- 通常，实际称重产品不支持商业功能。
- 对于实际称重产品，无法通过 **仓库状态更改** 来更新库存状态。

### <a name="catch-weight-tags"></a>实际称重标记

实际称重标签可以使用仓库管理移动应用流程来创建，在窗体 **仓库管理 > 查询和报表 > 实际称重标签** 中手动创建，或者使用数据实体流程来创建。 如果实际称重标签与入货源文档行（如采购订单行）关联，将注册此标签。 如果该行用于出库处理，则标签将在装运时进行更新。 您可以通过 **实际称重标签** 页面中的 **实际称重标签登记** 选项查看所有历史实际称重标签登记事件。

您可以使用 **更改标签捕获的重量** 选项以手动更新实际称重标签的重量值。 请注意，在此手动过程中，不会调整现有库存的重量，但是您可以轻松使用 **带实际称重标签的物料的现有差异** 页面以查找当前活动的实际称重标签和当前库存之间的任何差异。

其他手动选项是针对现有仓库工作 **登记标签** 到源单据行和 **登记工作**。

除了当前适用于实际称重产品的限制外，标记的实际称重产品还具有当前适用的其他限制。

- 所有库存手动更新（即未使用移动设备完成的更新）都必须包括对关联的实际称重标签的相应手动更新，因为这些更新不会自动完成。 例如，手动调整日记帐将更新库存，但不会更新关联的实际称重标签。
- 您必须手动更新实际称重标签以反映补货工作变动。 这是因为系统在处理补货工作时无法捕获重量，因此会改为记录平均重量。
- 标记的实际称重物料目前不支持接收混合牌照。
- 销售退货单接收的处理可以记录实际称重标签。 但是，此过程不会验证返回的标签是否是最初针对销售订单装运的相同标签。
- 具有 **登记物料消耗量** 活动代码的移动设备菜单项当前不支持记录实际称重标签。
- 尽管标记的实际称重物料支持盘点过程，但会受到限制。 例如，您可以使用移动设备选项来盘点标记的实际称重物料，并且使用平均重量。 但是，盘点交易不会自动更新实际称重标签。 盘点交易完成后，必须手动更新实际称重标签，以便它们能够反映库存。 如果原先未在某个位置的物料被计入该位置，则会使用标称重量。
- 牌照合并目前不支持标记的实际称重物料。
- 标签编号跟踪的实际称重物料不支持冲销工作功能。

> [!NOTE]
> 仅在实际称重产品采用完全跟踪的实际称重标签维度跟踪方法时（也就是说，仅当实际称重物料处理策略中的 **实际称重标签维度跟踪方法** 参数设置为 **跟踪产品维度、跟踪维度和所有存储维度** 时），上述有关实际称重标签的信息才有效。 如果对实际称重物料仅进行部分标签跟踪（也就是说，如果实际称重物料处理策略中的 **实际称重标签维度跟踪方法** 参数设置为 **产品维度、跟踪维度和库存状态**），则适用其他限制。 由于这种情况下标签和库存之间会丢失可见性，因此不支持某些其他方案。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]