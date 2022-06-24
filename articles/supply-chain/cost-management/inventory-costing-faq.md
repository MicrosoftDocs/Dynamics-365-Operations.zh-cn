---
title: 库存成本计算常见问题解答
description: 本文解答有关 Microsoft Dynamics 365 Supply Chain Management 中的库存成本计算的某些常见问题。
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 467839b1d0ca6788a92ae60d46686374d0a58046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850835"
---
# <a name="inventory-costing-faq"></a>库存成本计算常见问题解答

[!include [banner](../includes/banner.md)]

本文解答有关 Microsoft Dynamics 365 Supply Chain Management 中的库存成本计算的某些常见问题。

## <a name="inventory-close-adjustments-and-recalculation"></a>库存结转、调整和重新计算

### <a name="is-the-inventory-close-required"></a>是否需要进行库存结转？

如果您计划使用库存存档功能，则需要进行库存结转。 如果您不打算使用库存存档功能，那么无论您使用哪些成本计算模型，仍强烈建议您仍运行库存结转。

### <a name="how-often-should-the-inventory-close-be-run"></a>应多久运行一次库存结转？

每个分类帐期间至少应运行一次库存结转。 例如，如果您的分类帐设置为基于日历月的会计日历，则应每月运行一次库存结转。

### <a name="is-the-inventory-recalculation-required"></a>是否需要进行库存重新计算？

不，不需要进行库存重新计算。 如果您使用定期成本计算模型，例如先进先出 (FIFO)、后进先出 (LIFO) 或加权平均，则您应仔细考虑是否将运行库存重新计算。 它可以在您选择的启发式模型中提供更准确的成本计算。

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>应多久运行一次库存重新计算？

如果您计划运行库存重新计算，那么我们建议您考虑每天以批处理方式运行一次。 如果您的组织不需要频繁报告定期成本计算模型的库存值，则可以考虑减少运行库存计算的频率。

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>何时应在“结转和调整”页上使用现有库存调整？

只有在完成库存结转后，才能运行现有库存调整。 它通常是在上次结转之后的日期运行的。 在运行调整时，现有量调整只能调整截至该日期的现有库存。

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>何时应在“结转和调整”页上使用库存交易调整？

在运行库存结算之前，您应使用库存交易调整。 它通常用于更正不正确的收据。 运行库存结转并结算交易后，无法过帐库存交易调整。

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>是否在库存结转期间将采购订单退货视为其他发货？

是。 采购订单收货是结算到您为物料选择的启发式模型中的收货的发货。 如果您使用的是定期成本计算模型，则可以使用标记替代启发性成本。

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>库存结转期间销售订单退货会怎样？

运行库存结转时，将销售订单退货视为库存收货。 根据您为物料选择的启发式模型对库存结算发货。

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>对销售订单退货使用了什么成本价？

创建与销售订单相关的退货时，将从原始销售订单复制 **单价** 字段的值，并且退货的 **退货成本价** 字段将设置为退货销售订单行的原始库存交易记录的调整后成本价。 如果相关库存交易的 **财务未记帐** 选项设置为 *是*，则库存结转可能会导致对原始销售订单上的发货成本进行更新。 此方案中未更新 **退货成本价** 字段。 但是，当您过帐退货单装箱单时，系统将检查成本价并在退货库存交易中使用更新的成本。

对于与销售订单相关的标准成本物料的退货，系统将使用原始销售订单时间的标准成本，即使该物料的新标准成本处于活动状态也是如此。

当您创建与销售订单无关的退货时，**退货成本价** 字段将设置为站点中您为其创建退货单的物料的有效物料价格。 如果您在物料的成本计算版本中没有有效的成本价，则该值将为 0（零）。 如果您将该值保留为 0（零），您将收到一条警告，该警告指示未指定退货批次 ID 或退货成本价。

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>库存结转的预期性能是什么？

许多因素可能会影响库存结转的性能。 这些因素包括物料总数、期间中的交易总数、您使用的库存模型以及您在库存和仓库管理参数中配置的批处理帮助程序的数量。 您预计结束时间可能只需几分钟或几小时。 没有有关运行结转所需时间的特定指导。 您应为库存结转的性能定义非功能性业务要求，并与您的合作伙伴紧密联系以确定运行库存结转流程的计划。 如果您遇到意外的库存结转流程性能低下，则应打开支持票证。

## <a name="costing-sheet-and-indirect-costs"></a>成本计算单和间接成本

### <a name="which-costing-models-support-the-costing-sheet"></a>哪些成本计算模型支持成本计算单？

尽管成本计算单最常在使用标准成本计算的组织中使用，但您可以将其与 Supply Chain Management 中可用的任何成本计算模型一起使用。

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>我是否可以为组织的各个部分提供多个成本计算单？

否。 每个法人只能有一个成本计算单。

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>我是否可以对每个站点使用不同的成本计算单？

不，您不能对每个站点使用不同的成本计算单。 您只能为每个法人创建一个成本计算单。 但是，您可以为每个站点配置总节点数、成本组或间接成本节点。 此配置是一个手动流程，当发生组织或运营更改时，您必须维护成本计算单上的层次结构和物料分配。 如果在多个站点中生产或购买了一个物料，则没有一种机制可让您在每个站点的成本计算单上以不同的方式处理该物料。 此外，请注意，所有间接成本代码都有在成本计算版本中定义的费率或附加费。 您定义的成本始终特定于站点。

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>我能否停用和激活成本计算单的版本？

虽然没有为成本计算单保留详细版本历史记录，但您可以对成本计算单进行更改，然后在准备好后保存并对其进行验证。 没有允许您返回到成本计算单的较旧版本或查看对成本计算单所做的更改的机制。 如果您开始更改并且不希望它们生效，您可以关闭页面而不保存和验证更改。 将提示您放弃这些更改。

### <a name="can-i-create-indirect-costs-for-each-item"></a>我可以为每个物料创建间接成本吗？

在成本计算单上，您可以创建间接成本代码，其中 **节点类型** 字段设置为 *附加费*、*费率* 或 *基于输出单位*。 然后，您可以定义费率或附加费，以便它特定于物料编号。 在 **费率** 或 **附加费** 快速选项卡上，向网格中添加一行。 将 **有效** 字段设置为 *表*，将 **关系** 字段设置为特定物料编号。

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>我能否创建与特定物料无关的间接成本？

是。 您可以创建一个间接成本代码，其中 **节点类型** 字段设置为 *基于输出单位*。 然后，您可以将 **子类型** 字段设置为 *数量*、*重量* 或 *体积*，以指定您要生产的物料的数量、重量或体积。 您在 **费率** 快速选项卡上指定的费率将应用于所选子类型。 例如，您将 **子类型** 字段设置为 *数量*，将 **费率** 字段设置为 *1.00 美元*，然后创建数量为 10 的生产或批次订单。 在这种情况下，将添加到成品的间接成本为 10.00 美元。

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>我是否可以使用成本计算单按工时和材料拆分我的生产成本？

是。 您可以在成本计算单上创建 **总计** 节点，以通过选择的任何分组来分隔成本。 例如，您可以创建一个名为 **工时** 的 *总计* 节点，以及名为 *材料* 的另一个节点。 在 **工时** 节点下，添加与您的工时相关的每个代码组。 在 **材料** 节点下，添加与您的材料相关的每个成本组。

## <a name="dimension-groups"></a>维度组

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>我可以在批处理或序列号级别管理成本吗？

可以，如果您使用的是定期成本计算模型，如 FIFO、LIFO、LIFO 日期、加权平均或加权平均日期，则可以在跟踪维度组中启用 **批处理** 或 **序列号** 维度的 **财务库存** 选项，以在详细级别跟踪成本。

### <a name="can-i-manage-costs-at-the-location-level"></a>我可以在库位级别管理成本吗？

不可以，您无法为存储维度组中的 **库位** 维度启用 **财务库存** 选项。 如果您的组织必须在更详细的级别跟踪成本，请考虑是否可以创建虚拟仓库，然后在存储维度组中为 **仓库** 维度选择 **财务库存** 选项。

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>我应该为存储维度组启用“使用仓库管理流程”选项吗？

如果您认为将来可能要使用高级仓库管理功能，则应启用 **使用仓库管理流程** 选项。 保存存储维度组后，您将无法再为其更改 **使用仓库管理流程** 选项的设置。 如果您决定稍后使用仓库管理流程，则必须创建启用了该选项的新仓库。 没有可用于将所有库存从一个仓库移动到另一个仓库或将相关配置复制到新仓库的自动化流程。

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>即使我不打算使用高级仓库，我也能为存储维度组启用“使用仓库管理流程”吗？

是，即使您不打算使用高级仓库管理功能，也可以为存储维度组启用 **使用仓库管理流程** 选项。 要创建和处理交易，您必须完成最小配置，如预留层次结构和单位序列组。 但是，当您手动处理领料单、装箱单和产品收据时（例如，在销售订单和采购订单页上），通常会忽略高级仓库的设置。

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>何时应为存储或跟踪维度组启用“物理库存”选项？

当您必须基于该维度保留详细的库存记录时，您应为存储和跟踪维度组启用 **物理库存** 选项。 通常，也将实际跟踪任何有效的维度。 因此，将按所选维度跟踪库存的任何收货、发货或移动。 如果维度不是必需维度（例如牌照），则您可以启用 **允许空收货** 和 **允许空发货** 选项，以便即使未指定维度，用户也能接收、发放或移动库存。

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>何时应为存储或跟踪维度组启用“财务库存”选项？

当您必须基于该维度保留详细的财务记录时，您应为存储和跟踪维度组启用 **财务库存** 选项。 始终会对 **站点** 维度进行财务跟踪，而对其他维度进行选择性的财务跟踪。 如果您使用定期成本计算模型（如 FIFO、LIFO 或加权平均），则为维度启用 **财务库存** 选项表示您仅在收货和发货具有相同维度值的情况下进行结算。 例如，如果为 **仓库** 维度启用 **财务库存** 选项，则每个仓库中的成本将不同，无法结算不同仓库的收货和发货。

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>在存在交易后，我能否对产品、存储或跟踪维度组进行更改？

创建物料模型组后，如果为物料模型组中的维度选中了 **可用** 复选框，则可以更改 **按维度的覆盖范围计划**、**对于采购价** 和 **对于销售价** 字段的设置。 不允许进行其他更改。 例如，您无法启用或禁用 **有效**、**允许空发货**、**允许空收货**、**实际库存** 和 **财务库存** 选项。

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>我可以更改已发布产品的产品、存储或跟踪维度组吗？

如果产品的现有库存量为 0（零），并且所有库存交易的 **财务未记帐** 选项设置为 *否*，则您可以更改已发布生产页面上的存储和跟踪维度组。 创建记录后，无法更改产品维度组。

## <a name="item-model-groups"></a>物料模型组

### <a name="when-should-i-enable-the-stocked-product-option"></a>何时应启用“贮存的产品”选项？

您应为将在库存中跟踪的任何物料启用 **贮存的产品** 选项。 启用此选项后，将保留跟踪物料收货和发货的详细库存交易。 例如，通常会为您在仓库中保留的任何有形物料启用此选项。 如果您计划将非有形物料（如服务项）添加到物料清单 (BOM) 或配方，您还应启用此选项。 如果未启用 **贮存的产品** 选项，则在库存子分类帐中不会跟踪任何库存交易，并且这些物料的成本费用通常将计入到总帐中。 例如，此选项通常用于采购未包含在物料清单或配方中的用品或服务。

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>何时应启用“过帐实际库存”选项？

启用 **贮存的产品** 选项后，通常会启用 **过帐实际库存** 选项。 启用此选项后，系统将跟踪库存交易中物料的实际更新。 此选项用于与应付帐款、应收帐款和生产控制中的参数协调使用，这些参数指定实际更新应创建凭证。 当您希望在实际更新库存时更新分类帐时，您通常会启用此选项。 如果 Supply Chain Management 不是您的财务记录系统，则您可能需要禁用此选项。

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>何时应启用“过帐财务库存”选项？

启用 **贮存的产品** 选项后，通常会启用 **过帐财务库存** 选项。 此选项用于与应付帐款、应收帐款和生产控制中的参数协调使用，这些参数指定财务更新应创建凭证。 当您希望在财务上更新库存时更新分类帐时，通常会启用此选项（例如，通过为销售订单和采购订单开票或结束生产订单）。 如果 Supply Chain Management 不是您的财务记录系统，则您可能需要禁用此选项。

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>我应该何时启用“过帐到销售交货上的延期收入帐户”选项？

您可以使用 **过帐到销售交货上的延期收入帐户** 选项，以指示在过帐销售订单的装箱单时是否要确认总帐中的收入。 当您在销售订单的装箱单和发票之间有很长的延迟时，或者无法为该期间的所有销售订单开票时，通常使用此选项。 通常，如果您在过帐装箱单后立即过帐销售订单发票，您将禁用此选项。 这样，您将避免生成额外的总帐过帐，当您为销售订单开票时，将立即冲销这些过帐。

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>何时应启用“产品收货时的应计负债”选项？

在大多数组织中，无论您具有的是贮存的产品还是非贮存的产品，您都希望为所有物料模型组启用 **产品收货时的应计负债** 选项。 此选项用于根据物料收货价将应计项过帐到总帐。 由于采购订单的产品收货过帐与发票过帐之间通常存在延迟，因此大多数组织必须确认资产负债表上的负债以遵守当地法规，例如通用会计制度 (GAAP)。 如果 Supply Chain Management 不是您的财务记录系统，则您可能需要禁用此选项。 如果您的组织使用采购订单上的采购类别，则通过在 **采购策略** 页上为类别策略规则启用 **接收后的应计采购支出** 选项，可以控制应计要求。

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>如果尚未过帐收货登记，那么如何阻止用户过帐采购订单产品收货？

如果尚未进行采购订单登记，则可以对物料模型组启用 **登记要求** 选项，来阻止用户过帐采购订单产品收货。 此选项通常用于使用双步骤接收流程的组织，或用于必须登记批处理或序列号（例如您正在接收的物料）的方案。 **登记要求** 选项适用于物料的 *所有* 库存收货，而不仅仅适用于采购订单。 例如，它适用于具有正数量的库存日记帐，以及完工入库日记帐形式的生产订单报表。

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>如果尚未过帐产品收货，那么如何阻止用户过帐采购订单发票？

如果尚未进行采购订单产品收货，则可以对物料模型组启用 **接收要求** 选项，来阻止用户过帐采购订单产品发票。 此选项通常用于要求在应计总帐中实际确认收据的组织。 **接收要求** 选项适用于物料的 *所有* 库存收货，而不仅仅适用于采购订单。 例如，它适用于具有正数量的库存日记帐，以及完工入库日记帐形式的生产订单报表。 如果您的组织使用采购订单上的采购类别，则通过在 **采购策略** 页上为类别策略规则启用 **接收要求** 选项，可以控制接收要求。

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>如果尚未过帐销售订单领料单，那么如何阻止用户过帐销售订单装箱单？

如果还没有销售订单领料单，则可以对物料模型组启用 **领料要求** 选项，来阻止用户过帐销售订单领料单或发票。 此选项通常用于在仓库中执行实际领料流程的组织（例如，通过使用仓库移动设备进行领料）。 **领料要求** 选项适用于物料的 *所有* 库存发货，而不仅仅适用于销售订单。 例如，它适用于具有负数量的库存日记帐和生产订单领料单日记帐。

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>如果尚未过帐销售订单装箱单，那么如何阻止用户过帐销售订单发票？

如果还没有销售订单装箱单，则可以对物料模型组启用 **扣缴要求** 选项，来阻止用户过帐销售订单发票。 此选项通常用于在仓库中执行实际装箱流程的组织（例如，通过使用 Warehouse Management 移动应用进行包装，或者通过生成将包含在已装运物料中的单据）。 **扣缴要求** 选项适用于物料的 *所有* 库存发货，而不仅仅适用于销售订单。 例如，它适用于具有负数量的库存日记帐和生产订单领料单日记帐。

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>我能否阻止销售登记的物料？

在 Supply Chain Management 的库存中登记物料后，该数量实际上可在系统中发放。 例如，如果已登记但尚未接收的物料 *不能* 发放到销售订单或生产订单，请考虑使用库存状态、库存锁定、质检订单、检验单或预留功能来管理业务流程。

## <a name="production-costing"></a>生产成本计算

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>我能否对原材料使用一个成本计算模型而对成品使用另一个成本计算模型？

能，您可以对每个物料使用不同的成本计算模型。 制造商对原材料使用定期成本计算模型而对半成品和成品使用标准成本很常见。

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>如何降低机器成本的开销？

为了降低机器成本的开销，您必须根据您的业务需求为每台机器创建资源和资源组。 每个资源或资源组都可以分配给成本类别以控制机器成本。 每个成本类别都可以链接到一个成本组，每个成本组都可以用作成本计算表上的间接成本的计算基准。

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>如何识别与成本计算单上的能源消耗（例如水、能源或天然气消耗量）相关的成本？

您通常可以通过以下两种方式之一确认与能源消耗相关的成本：

- 在物料清单或配方中创建一行。 通常，此行被创建为服务项，您可以指定您要使用的计量单位与您生产的数量之间的关系。 这样，用户可以在生产流程中使用其他数额。 您可以根据您在 **刷新原则** 字段中选择的值自动使用物料。
- 在成本计算单上创建间接成本。 通常，此方法用于在生产流程中分配能源消耗的总成本。 例如，您可以使用成本组和吸收基准根据工艺路线中的材料或人工来缩放消耗量。

您应根据报告、对帐和运营要求选择最佳选项。

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>我可以在物料清单或配方中捕获资源详细信息吗？

只能在工艺路线工序中捕获资源详细信息。 虽然您可以创建服务项来表示资源并分配成本来增加成品成本计算，但我们通常不会推荐此方法。 相反，我们建议您创建一个包含一行的简单工艺路线以跟踪资源成本，并配置工序，以便在生产订单开始或结束时自动使用该工序。

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>如果手动输入成本，那么我能否查看计算详细信息？

否。 如果在 **物料价格** 页上手动输入价格，则 **查看计算详细信息** 和 **报告计算明细** 按钮不可用。 如果您为手动输入的成本价格选择 **按成本组的成本累积** 按钮，则将显示汇总行，并且所有成本都将汇总到成品物料。

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>当我手动输入成本时，系统是否会计算生产订单上的差异？

是，当您手动输入标准成本时，系统会计算差异。 但是，当您手动输入标准成本而不是计算标准成本时，生产订单中的所有材料、工艺路线和间接成本消耗量将被视为替代差异。 如果存在其他差异，例如额外材料或人工消耗量，那么它们也将被记录为生产物料清单中的差异。 因此，我们强烈建议您始终对具有物料清单、工艺路线或间接成本的物料运行计算。

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>如何将子生产订单中的差异结转到父生产订单？

当您使用定期成本计算模型（如 FIFO、LIFO 或加权平均）时，将在您为物料选择的启发式模型中确认子生产的成本。 如果您需要实际成本计算，请考虑使用标记原则指示将哪些子生产发放到父生产订单。 或者，例如，请考虑对跟踪维度组中的 **批处理** 或 **序列号** 维度使用 **财务库存** 选项。

### <a name="how-does-the-flushing-principle-affect-consumption"></a>刷新原则对消耗量有何影响？

物料清单、配方或工艺路线行上的刷新原则控制用于使用物料或人工的时间和技术。 如果您选择 *开始*，则在开始处理生产订单时将自动使用物料或人工。 如果您选择 *完成*，则在将生产订单报告为完成时将自动使用物料或人工。 如果您选择 *手动*，则用户必须手动领取材料，或在作业或工艺路线卡日记帐中记录时间。 物料清单和配方还具有 *在库位可用* 选项。 如果选择此选项，则在将物料转移到生产车间位置后将自动使用这些物料。

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>如果我有多级物料清单或配方，我应如何运行成本计算？

一般情况下，我们建议您从最低级别的物料清单或配方开始进行计算。 要在批量运行成本计算时简化筛选，您可以使用计算组帮助划分产品。 我们还建议您在开始成批运行成本计算之前，先运行 *重新计算物料清单级别* 定期作业。 每个组织都应考虑产品组合并定义满足产品和物料清单或配方结构特定需求的策略。

## <a name="transfer-order-costing"></a>转移单成本计算

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>是否有将运费分配到转移单成本的方法？

您可以将费用添加到转移单以添加成本。 费用代码定义您要添加的费用的借方和贷方。 您必须首先在 **库存管理** 模块中创建费用代码。 要将费用添加到转移单，请选择要将费用添加到的转移单行上的 **费用**。

## <a name="variances"></a>差异

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>我可以根据站点或仓库以不同方式处理差异吗？

没有按站点配置差异帐户的选项。 当您对已发布产品使用标准成本计算时，您可以在 **过帐** 页上选择用于标准成本差异过帐的主科目。 可以选择为一个物料、一组物料或所有物料配置帐户。 您还可以配置一个成本组、一组成本组或所有成本组。

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>我可以将由货币汇率导致的差异与其他类型的差异分开吗？

如果差异由物料的采购订单价格与标准成本之间的货币汇率差异造成，则无法将汇率差异与其他差异区分开来。

## <a name="reporting"></a>报告

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>我可以创建和使用多少个库存值报表配置？

您可创建的库存值报表配置的数量没有限制。 您应评估您的特定报告要求并创建满足这些要求所需的配置数。 您将需要至少一个库存值报表配置才能运行报表或报表存储选项。

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>我是否可以使用库存值报表分析每个仓库中的物料的成本？

是。 您可以在库存值报表配置中为每个 **仓库** 维度启用 **视图** 或 **总计** 选项。 但是，该报表将仅显示为存储维度组启用了 **财务库存** 选项的维度的值。 对于其他维度，它将显示空白列。 有关详细信息，请参阅[库存值存储报表示例和逻辑](inventory-value-report-examples.md)。

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>如何查看截至特定日期的库存数量与加权平均值？

您可以使用 **库存帐龄** 报表，其中包括一个显示截至特定日期的库存值的 **平均单位成本** 列。 有关详细信息，请参阅[库存帐龄报表示例和逻辑](inventory-aging-report.md)。

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>如何查看针对发货交易结算的收货交易？

通过在 **库存交易** 或 **库存交易详细信息** 页的操作窗格上的 **库存** 选项卡上选择 **结算** 或 **成本资源管理器**，您可以查看库存交易的结算。 如果您选择收货以查看与交易相关的发货，则成本资源管理器不会显示详细信息。 仅当您选择发货交易时，才会显示详细信息。

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>库存值报表如何显示具有正实际数量和负财务值的物料？

库存值报表将实际和财务金额和数量分成其自己的列。 报表上显示的值位于您在运行报表时选择的日期范围内。 显示的汇总级别取决于您选择的设置。 如果物料具有实际收货和财务发货的交易，则将独立汇总数量和值。 如果您已选择查看交易形式的详细信息级别，则将分别显示每个收货和发货的行，并分别显示实际数量和财务数量和金额。 有关详细信息，请参阅[库存值存储报表示例和逻辑](inventory-value-report-examples.md)。

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>存储和跟踪维度组对库存值报表有何影响？

如果为存储或跟踪维度组中的维度启用 **财务值** 选项，则可以在库存值报表配置中为维度选择 **视图** 或 **总计** 选项。 如果您为未选择 **财务值** 选项的维度选择 **视图** 或 **合计** 选项，则此列将在报表输出中为空。 如果您已为存储或跟踪维度组中的维度启用了 **财务值** 选项，并且您未在库存值报表配置中选择 **视图** 或 **总计** 选项，则系统将汇总进行了财务跟踪的选定维度的值。

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>我可以自定义 Power BI Embedded 报表以进行成本计算吗？

可以，具有正确安全权限的用户可以更新 Supply Chain Management 中任何 Power BI Embedded 报表的报表设计区域。 有关详细信息，请参阅[在分析工作区中自定义嵌入式报表](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md)。

### <a name="where-can-i-view-the-variance-analysis-statement"></a>在哪里可以查看差异分析报表？

通过转到 **成本管理 \> 查询和报表 \> 库存会计 - 分析报表** 或 **成本管理 \> 查询和报表 \> 制造会计 - 分析报表**，您可以访问差异分析报表。 这两个选项都会打开同一个报表，并且报表具有相同的行为。

## <a name="item-prices-and-default-costs"></a>物料价格和默认成本

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>我是否可以维护每个产品变型的成本？

是。 您可以在 **已发布产品** 页面的 **管理成本** 快速选项上启用 **按变型使用成本价** 选项，以按产品变型启用定价。 （此选项仅适用于基础产品。）然后，在 **物料价格** 页面上（您可以从 **成本计算版本** 页或 **已发布产品** 页面中打开此页面），您可以选择 **维度显示** 以指定是否要显示 **配置**、**大小**、**颜色** 或 **样式** 维度。 要保存设置并在每次打开页面时使用所选维度，请启用 **保存设置** 选项，然后选择 **确定**。 您只能为维度在产品维度组中处于活动状态的物料输入维度。

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>我是否可以维护每个仓库的成本？

否，无法按仓库维护物料价格。 但是，您可以按仓库维护采购价格或销售价的贸易协议。 首先，在 **存储维度组** 页上对维度选择 **对于采购价** 或 **对于销售价** 选项。 然后，当您创建贸易协议日记帐并打开维度的行时，选择 **库存 \> 显示维度** 以选择应在网格中显示的维度。 要保存设置并在每次打开页面时使用所选维度，请启用 **保存设置** 选项，然后选择 **确定**。 您只能为维度在产品维度组中处于活动状态的物料输入维度。

### <a name="what-are-price-charges"></a>什么是价格费用？

价格费用提供了一种将固定金额添加到物料价格或贸易协议的单价上的方法。 当您在 **价格费用** 字段中输入金额时，也可以在 **费用数量** 字段中输入一个值。 按照指定的费用数量分期清偿价格费用。 如果您要将价格费用包括在物料的单价中，则启用 **包括在单位价格中** 选项。 对于标准成本，始终启用了此选项。

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>我应如何配置以多种货币采购的物料的价格？

如果您在 **已发布产品** 页面的 **采购价格** 字段中输入了默认价格，则假定该价格采用您所在法人实体的分类帐记帐币种。 同样，如果您在 **价格类型** 字段设置为 *采购* 的成本计算版本中输入采购价格，则假定该价格采用法人的记帐币种。 当您为具有不同币种的供应商创建采购订单时，系统将使用您在分类帐内的 **记帐币种汇率类型** 字段中指定的汇率，将该货币从记帐币种金额自动转换为交易币种。

创建贸易协议日记帐时，可以指定您在每行中表达价格所用的币种。 您可以为多种货币、特定供应商和多种其他因素组合创建贸易协议。 如果您创建的采购订单中存在所选货币的相关贸易协议，系统将使用具有匹配货币的贸易协议。 当您过帐产品收据或发票等交易时，金额将使用您在分类帐中指定的记帐币种汇率转换为分类帐的记帐币种。

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>我应如何配置以多种货币采购的物料的成本？

无法用多个币种配置成本。 您为物料价格指定的成本或您在 **已发布产品** 页面的 **管理成本** 快速选项卡上的 **价格** 字段中输入的默认成本始终以您所选法人的分类帐的记帐币种表示。

如果您的组织使用标准成本计算，则应定义存在多种货币时定义成本的策略。 您还应定义用于定期更新成本的流程，以帮助减少已过帐的差异数。

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>我是否可以使用“成本组”页面上的“利润”设置来计算销售价？

是，您可以使用 **成本组** 页面上的 **利润** 设置在使用成本计算功能计算销售价时添加百分比。 有关详细信息，请参阅[物料清单计算](bom-calculations.md)。

## <a name="marking"></a>标记

### <a name="how-does-marking-affect-periodic-costing-models"></a>标记如何影响定期成本计算模型？

如果您使用定期成本计算模型（如 FIFO、LIFO 或加权平均值），并且您已针对发货交易标记了收货交易，则在库存结转过程中将忽略该物料的启发式模型。 相反，系统将使用收货的实际成本来计算发货成本。

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>我使用标记时库存结转期间会发生什么？

当您标记收货和发货时，库存结转将结算一起标记的交易。 当标记用于创建结算时，**结算** 页面上的 **原则** 字段将设置为 *标记*。 如果实际或在财务上更新交易之前标记了该交易，则该发货将使用标记的收货成本，而不是移动平均成本。 如果在财务更新之后标记了交易，则库存结转和调整流程将调整发货成本，使其与收货成本相匹配。

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>我可以在使用标准成本计算或移动平均值时手动标记交易吗？

不可以，当您使用标准成本计算或移动平均值时，无法手动标记收货或发货。 如果自动标记交易（例如直接交货或内部公司订单），则标记记录将保留并充当硬性预留。 但是，当您使用标准成本计算或移动平均值时，记录的标记不会影响物料的成本。

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>标记对损益表有何影响？

当您根据收货标记发货交易时，发货成本将与所选收货相匹配。 当您实际和在财务上过帐发货时，过帐将影响您在库存过帐模板中指定的 **所售货物成本(已交付)** 和 **已开票的所售货物成本** 帐户。 如果在实际或财务更新之后标记了交易，则 *库存结转和调整* 流程将创建一个具有匹配凭证的调整，该凭证将调整 **已开票的所售货物成本** 帐户，以及您为 **已开票的单位成本**（库存）指定的帐户抵销科目。

### <a name="how-does-marking-affect-master-planning"></a>标记对主计划有何影响？

**主计划参数** 页上的 **标准更新** 选项卡包含一个名为 **更新标记** 的字段。 确认由主计划生成的计划订单时，将使用您在此处选择的选项。 选项如下：

- *否* - 系统不执行任何标记。
- *标准* - 系统根据限定标准针对发货标记收货。 需求订单根据履行订单来标记。 如果履行上仍有一些数量，则不标记履行订单。
- *扩展* – 无论履行订单上是否仍然存在任何数量，系统都同时标记需求订单和履行订单。

## <a name="negative-inventory"></a><a name="negative-inventory"></a>负库存

### <a name="when-should-i-allow-physical-negative-inventory"></a>我应何时允许实际负库存？

一般情况下，我们不建议您允许使用实际负库存，因为您的仓库中的有形物料不能小于 0（零）。 但是，某些行业和业务方案的业务流程可能会限制要求允许库存实际为负的工序。 例如，即使系统指示商品没货，零售商也可能不希望阻止销售被带到收银机的商品。 流程制造商提供另一个示例。 对于这些制造商，使用的数额可以超过配方中建议的数额。 或者，可以估计而非精确计算消耗量，以便消耗量超出特定库位（如水箱）中的数额。

如果可能，您应评估您的业务流程，并尝试改进该流程以确保库存不能为负数。 如果必须允许负库存，则您应该具有一个明确的业务流程来更正负库存，因为负库存会对成本计算产生不利影响。

### <a name="when-should-i-allow-financial-negative-inventory"></a>我应何时允许财务负库存？

一般情况下，我们建议大多数组织允许财务负库存。 （在大多数情况下，在装运物料之前不会处理采购订单发票。）当您具有要求销售价格反映采购订单最终成本的特定业务流程时，您应启用此选项。 例如，此要求可能适用于按订单生产的行业或法律规定的特定地区。

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>当库存为负时，我的发货成本会怎样？

当您的物料库存为负数，并且您发出的物料多于实际拥有量时，如果您使用定期成本计算模型（例如 FIFO、LIFO 或加权平均），则系统将使用默认物料价格来计算移动平均值。 如果未为物料指定默认价格，系统将发放值为 0（零）的库存。 此行为可能导致您的移动平均值的未来计算结果不准确。

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>如果现有库存不足，我是否能对销售订单和生产订单阻止领料、包装物料或出售物料？

是。 我们建议您对物料模型组禁用 **实际负值** 选项，以对销售订单和生产订单阻止领料、包装物料或出售物料。

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>如果没有为同一物料的采购订单开票，那么我是否可以阻止对销售订单上的物料开票？

是。 我们建议您对物料模型组禁用 **财务负值** 选项，以防止在没有为同一物料的采购订单开票的情况下阻止对销售订单上的物料开票。

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>负库存对财务比率（如利润率）有何影响？

当您允许库存变为负值时，资产负债表中的库存值和损益表中的所售货物成本可能被低估，特别是在没有为您的物料配置默认价格的情况下。 因此，财务报表和毛利润率等比率可能被高估，因为成本不正确。 如果您使用定期成本计算模型（如 FIFO、LIFO 或加权平均值），则在纠正负库存数量后运行库存结转和调整流程时，可以调整发货值。 但是，如果您使用移动平均值，则无法重估单个交易。

### <a name="how-should-i-correct-negative-inventory"></a>我应如何更正负库存？

我们建议您在组织或业务要求指示您允许库存变为负值时，经常监视和更正负库存。 您可以通过执行周期盘点、过帐调整或过帐移动日记帐来更正库存值。 如果必须识别特定总帐帐户中的库存意外增加，则应计划使用移动日记帐。 否则，当您使用周期盘点或库存调整流程时，系统会将库存调整过帐到 **库存收货** 帐户，以及您在库存过帐模板上指定的 **库存支出，利润** 帐户的抵销科目。

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>如果我的库存已变为负值并且我使用的是移动平均值，我是否必须创建新物料？

否。 如果您的组织允许库存实际变为负值，并且您正在将移动平均值用作库存模型，则系统将使用在 **库存和仓库管理参数** 页面上分配的回退成本序列，来确定如何将成本分配给您的发货。 一般来说，我们建议您不要允许您的库存实际变为负数。 有关详细信息，请参阅本文的[负库存](#negative-inventory)一节中的其他问题。

## <a name="not-stocked-products"></a>非贮存的产品

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>我可以过帐非贮存的产品的销售订单领料单吗？

当您为销售订单生成领料单时，且该领料单包括物料模型组中未贮存的物料，则您不会看到这些非贮存的物料的任何行。 您无法使用 Warehouse Management 移动应用处理非贮存的物料。

当您为销售订单生成装箱单时，且该装箱单包括物料模型组中未贮存的物料，请将 **数量** 字段设置为 *领料数量和未贮存产品*，以在单据生成中包括非贮存的物料。 如果选择 *全部*，则装箱单中将仅包含贮存的物料。

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>我应使用非贮存的产品还是类别（销售类别或采购类别）？

非贮存的产品与类别之间的选择取决于您的特定业务要求。 非贮存的产品通常可以更好地控制默认值，例如采购订单和销售订单上的数量和价格。 因此，在多次购买或销售同一产品或服务的情况下，非贮存的产品是首选。 类别在价格、物料、描述等因交易而不一致的情况下很有用。 类别也可以用于任何产品，以帮助对正在销售或购买的产品的类型进行分类。

## <a name="service-items"></a>服务项

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>服务项与非贮存的产品有什么区别？

服务项是产品类型。 创建新发布的产品时，可以将 **产品类型** 字段设置为 *物料* 或 *服务*。 通常选择 *物料* 来指示物料是有形物料，而通常选择 *服务* 来指示物料为无形物料。

任何已发布产品，无论它是物料还是服务产品，都可以贮存或不贮存。 贮存或不贮存设置由您为已发布产品选择的物料模型组控制。 例如，当您选择未贮存的物料组时，系统不会为相关的销售订单或采购订单创建库存交易。

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>我可以在物料清单中包括非贮存的物料吗？

不可以，您不能包含链接到物料模型组（在物料清单或配方中禁用了 **已贮存** 选项）的已发布产品。 **产品类型** 字段设置为 *物料* 还是 *服务* 并不重要。 物料清单或配方行中只能包含贮存的物料。

## <a name="costing-modelspecific-questions"></a>成本计算模型的特定问题

### <a name="which-costing-model-should-i-use"></a>我应使用哪个成本计算模型？

您应选择的成本计算模型取决于您的业务要求。 选择要在 Supply Chain Management 中使用的成本计算模型之前，您应验证本地法规是否允许使用该模型。 我们建议您通过所在地区的注册会计师验证您的选择。

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>我可以在我的组织中使用多个成本计算模型吗？

是。 您可在 Supply Chain Management 中选择的物料模型组或成本计算模型的数量没有限制。

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>我能否对每个物料使用多个成本计算模型吗？

否。 只能为每个已发布产品选择一个成本计算模型。 此行为由物料模型组控制。 如果您必须使用多个成本计算模型来报告库存值，则应考虑使用全球库存核算加载项。

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>当我使用制造执行功能时，我应使用哪种成本计算方法？

您应选择的成本计算模型取决于您的业务要求。 当您的组织也使用制造执行功能时，使用任何成本计算模型没有特定的优点或缺点。

### <a name="when-is-fefo-used"></a>何时使用 FEFO？

先过期先出 (FEFO) 不是成本计算方法。 相反，它是一种在制造组织中常用的预留方法。 您可以通过启用 **受先过期先出日期控制** 选项，然后在 **选择标准** 字段中选择值，为物料模型组启用 FEFO 预留。

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>选择一个成本计算模型而不选择另一个成本计算模型是否具有性能优势？

一般来说，您为物料选择的成本计算模型对系统的总体性能影响最小。 但是，运行库存结转或重新计算流程所需的时间量可能受您选择的库存成本计算模型的影响。 例如，如果您使用标准成本或移动平均值，则库存结转流程对系统的影响最小，因为它不会更新每个库存交易并创建结算。 但是，定期成本计算模型（如 FIFO、LIFO 或加权平均值）可能会增加完成库存结转流程所需的时间。 具体来说，对于 *转结库存* 流程，当您在 **每个物料允许的最大迭代次数** 字段中输入一个高值，或在 **允许的最小金额** 字段中输入一个低值时，结转流程可能时间更长。

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>我应何时使用“固定收货价”选项？

当您在物料的 **物料模型组** 页上选择 **固定收货价** 复选框时，系统将收货价用作库存收据的标准成本。 如果为产品配置的采购价格和默认物料成本价存在差异，则差额将过帐到 **固定收货价利润** 或 **固定收货价损失** 帐户，以及 **固定收货价抵销** 帐户的抵销科目。 （所有这些帐户均在 **过帐** 页面上指定。）

当您使用定期成本计算模型（如 FIFO、LIFO 或加权平均值）时，您应选中 **固定收货价** 复选框。如果收货价与默认物料成本不同，则要求在分类帐中跟踪采购价格差异。

### <a name="moving-average"></a>移动平均

### <a name="is-moving-average-the-same-as-a-floating-average"></a>移动平均值是否与浮动平均值相同？

术语移动平均值、浮动平均值和移动平均经常作为同义词使用。 在这些条款中，移动平均值是 Supply Chain Management 中唯一可用的正式成本计算模型。 虽然移动平均值不是官方成本计算模型，但它是在使用定期成本计算模型（如 FIFO、LIFO 或加权平均值）时使用的方法。 术语“浮动平均值”未在 Supply Chain Management 中使用，并且可能在其他系统中具有不同的含义。

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>当我使用移动平均值时，如何适应物料收货价和发票价格之间的差异？

当您使用移动平均值时，实际成本（收货价格）用于计算所有发货交易的移动平均值。 如果实际成本（收货价格）与财务成本（发票价格）之间存在差异，系统会自动将差额过帐到为 **库存过帐模板** 页 **库存** 选项卡上的 **移动平均价差** 过帐类型指定的主科目。

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>总帐中显示的移动平均值的价格差异在哪里？

当收货的实际更新和财务更新的过帐之间存在价格差异时，差额会过帐到为 **库存过帐模板** 页 **库存** 选项卡上的 **移动平均价差** 过帐类型指定的主科目。 有关详细信息，请参阅[移动平均值](moving-average.md)。

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>当我使用移动平均值时，如果收货前出现问题，会发生什么情况？

通常，收货前可能会有发货，因为您允许物料模型组的实际负库存，或者因为已追溯该发货。 有关详细信息，请参阅本文的[负库存](#negative-inventory)一节。

如果您正在追溯交易，那么我们建议您仔细考虑您的业务流程和运营，以确定是否有避免此情形的方法。 如果为使用移动平均值的物料追溯交易，则系统会将当前移动平均值分配给此交易。 未调整以后的发货。 有关移动平均值与追溯交易的详细信息，请参阅[移动平均值](moving-average.md)。

### <a name="standard-costing"></a>标准成本计算

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>标准成本计算和固定收货价有什么区别？

标准成本计算要求您定义物料价格并在成本计算版本中激活成本。 该成本用于所有收货和发货。 通过使用您在 **库存过帐模板** 页的 **标准成本** 选项卡上指定的标准成本差异帐户，在总帐中记录库存收货的差异。

但是，当您使用固定收货价时，只有收货成本是固定的，并且系统使用您在 **已发布产品** 页面的 **管理成本** 快速选项卡上指定的成本。 默认成本与采购订单价格之间的差异将导致采购价格差异过帐到固定收货价损益帐户。 发货不使用固定收货价。 相反，在过帐时，发货将按移动平均值进行估价（除非您使用标记），并且它们将重估为您在运行库存结转时选择的启发式模型。

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>我是否可以将 FEFO 预留与标准成本计算一起使用？

是，您可以在选择标准成本计算时对物料模型组使用 FEFO 预留。 FEFO 预留控制用于物料实际处理的预留逻辑，而标准成本计算控制物料的实际成本和财务成本。

### <a name="can-i-upload-pending-prices"></a>我是否可以上传未决价格？

是，您可以使用 Excel 加载项或数据管理框架上传未决价格。 我们建议您使用以下实体：

- 待定物料价格 (V2)
- 待定工艺路线成本类别单位成本
- 成本计算单节点计算系数 (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>我可多久更新一次物料的标准成本？

您可激活新标准成本的频率没有限制。 如果在激活最后一个成本的同一天激活物料的新成本，系统将对新交易或更新（如对现有交易的更新）使用最近激活的成本。

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>我是否可以停用或删除激活的成本？

否，您不能停用或删除激活的成本。 如果您错误地激活了成本，则可以激活具有正确成本的新成本。

### <a name="are-calculation-groups-used-with-standard-costing"></a>计算组是否用于标准成本计算？

无论您选择的物料模型组如何，计算组都可用于任何物料。 计算组在成本汇总或成本计算过程中用于确定应该用于您正在为其运行计算的物料的设置。 有关计算组的详细信息，请参阅[物料清单计算组](bom-calculation-groups.md)。

### <a name="when-should-i-use-a-planned-costing-version"></a>我应何时使用计划的成本计算版本？

成本计算版本可以具有 *标准成本* 或 *计划成本* 类型。 *标准成本* 类型用于系统中有效且将在交易中过帐的成本。 *计划成本* 类型用于运行成本模拟，不会影响交易成本。

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>是否可以将一个实体的总成本作为销售成本转移到另一个实体？

没有自动将成本从一家公司复制到另一家公司的方法。 此外，没有自动将成本从采购价复制到销售价的方法。 如果您的组织必须完成这些任务之一，请考虑您是否可以使用数据管理框架从成本计算版本中导出数据，并作为成本计算版本中的销售价或作为贸易协议上传到其他公司。 可能需要手动操作文件。

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>将计划成本复制到标准成本计算版本的最佳方法是什么？

您可以使用 **成本计算版本** 页上的 **复制** 按钮将物料价格、成本类别价格或间接成本从一个成本计算版本复制到另一个成本计算版本。
