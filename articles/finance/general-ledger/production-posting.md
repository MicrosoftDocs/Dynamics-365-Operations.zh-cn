---
title: 生产订单过帐
description: 本文提供有关不同类型的生产订单过帐的信息。
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d41725325a82b24c1e5aa6bd2c1a5322f3078ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879615"
---
# <a name="production-postings"></a>生产过帐

本文提供有关生产订单流程中不同过帐类型的信息。


## <a name="material-consumption"></a>物料消耗量

在过帐生产领料单日记帐时，将物料登记为在生产中被消耗。 此流程创建扣减现有库存量的交易。 在 **生产参数** 中，您可以指定是否应在分类帐中过帐生产中的原材料（称为 WIP）的值。

生产中的原材料 (WIP) 的值将过帐到 **估计的已消耗物料的成本** 和 **估计的已消耗物料的成本，WIP** 帐户。 生产订单的领料单流程是与生产订单相关的库存交易的实际更新。 将生产订单登记为结束时，将冲销实际交易并对相关库存交易进行财务更新。 过帐期末日记帐时，将使用 **已消耗物料的成本** 和 **已消耗物料的成本，WIP** 过帐类型。

**库存过帐模板** 页上的 **生产** 选项卡控制如何将生产订单过帐到总帐。 当 **分类帐过帐** 字段设置为 **生产控制参数** 页上的 **物料和资源** 或 **物料和类别** 时，将使用此项。 

要将领料单日记帐过帐到生产订单的总帐，必须满足以下条件：

-   在 **生产控制参数** 页面上，必须选中 **过帐分类帐中的领料单** 复选框。 可以在 **按站点的生产控制参数** 页面上为特定站点覆盖此设置。
-   对于在采购订单行上选择的物料，必须在 **物料模型组** 页面上选中 **过帐实际库存** 复选框。
-   必须在 **库存过帐模板** 页上为以下过帐类型指定主科目：
    -   **估计的已消耗物料的成本**
    -   **估计的已消耗物料的成本，WIP**

## <a name="time-consumption"></a>时间消耗量

工作人员在生产作业上花费的时间将记录在 **工艺卡日记帐** 或 **作业卡日记帐** 中。 在过帐这些日记帐时，将处理过帐到生产中 (WIP) 的资源的专用帐户的分类帐。 此过帐表示在生产订单上花费的时间的值。 在将生产订单登记为已结束后，将结算 WIP 帐户。

根据 **生产控制参数** 页上 **分类帐过帐** 字段中选择的选项，有三种过帐时间消耗量的可能的方法。

## <a name="reporting-finished-goods-and-error-quantities"></a>报告成品和残次数量

在生产订单 **报告为完工入库** 时，会在库存中通过 **报告为完工入库** 日记帐更新已完成的成品。 如果使用的是 WIP 会计，过帐分类帐日记帐以减少 WIP 帐户和增加成品库存。 日记帐使用已为产品定义的标准成本。 如果在 **生产控制参数** 页面上选择了 **使用估计的成本价** 选项，则将使用生产订单中的估计成本。

生产中的原材料 (WIP) 的值将过帐到 **估计的制造成本** 和 **估计的制造成本，WIP** 帐户。 生产订单的 **报告为完工入库** 流程是与生产订单相关的库存交易的实际更新。 结束生产订单时，将冲销实际交易并对相关库存交易进行财务更新。 过帐期末日记帐时，将使用 **制造成本** 和 **制造成本，WIP** 过帐类型。

**库存过帐模板** 页上的 **生产** 选项卡用于控制生产订单将如何过帐到总帐。 当 **分类帐过帐** 字段设置为 **生产控制参数** 页上的 **物料和资源** 或 **物料和类别** 时，将使用此项。 将此字段设置为 **生产组** 后，**生产组** 页面上的 **分类帐物料** 快速选项卡也可用于控制生产订单过帐。

要将 **报告为完工入库** 日记帐过帐到生产订单的总帐，必须满足以下条件：
-   在 **生产控制参数** 页面中，必须选中 **过帐分类帐中的报告为完工入库部分** 复选框。 可以在 **按站点的生产控制参数** 页面上为特定站点覆盖此设置。
-   对于在采购订单行上选择的物料，必须在 **物料模型组** 页面上选中 **过帐实际库存** 复选框。
-   必须在 **库存过帐模板** 页中为以下过帐类型指定主科目：
    -   **估计的制造成本**
    -   **估计的制造成本，WIP**

## <a name="ending-the-production-order"></a>结束生产订单

在结束生产订单前，为生产的数量计算实际成本。 物料、人工和开销的所有预估成本都被冲销，并用实际成本替代。 成品的总计成本从 **制造成本** 帐户中借记，并贷记到 **制造成本，WIP** 帐户。 生产订单期间消耗的材料会贷记到 **已消耗物料的成本**，并借记到 **物料的成本，WIP** 帐户。

如果您在运行成本计算时选中 **结束作业** 复选框，则生产订单的状态将更改为 **已结束**。 此状态将阻止将任何额外成本无意中过帐到已完成的生产订单。 您可以指定应将报告为完工入库的残次数量的值分配到报告为已完工入库的完好数量。 或者，您可以指定将残次数量的值过帐到专用的报废科目。 

要指定特定的报废科目，请执行以下步骤：
1.  转到 **生产控制** > **设置** > **生产控制参数**。
2.  选择 **标准更新** 选项卡。
3.  在 **报废方法** 字段中，选择 **报废科目**。
4.  在 **报废科目** 字段中，选择结束生产订单时应过帐错误数量的废料的主科目。 例如，选择支出帐户，如“510380：生产废料”。

要将结束日记帐过帐到生产订单的总帐，必须满足以下条件：
-   必须在 **库存过帐模板** 或 **生产组** 页中为以下过帐类型指定主科目：
    -   **已消耗物料的成本**
    -   **已消耗物料的成本，WIP**
    -   **制造成本**
    -   **制造成本，WIP**
-   必须在 **成本类别**、**资源** 或 **资源组** 页面中为以下类型指定主科目：
    -   **已吸收的制造成本**
    -   **已消耗的制造成本，WIP**

## <a name="indirect-costs-for-production-orders"></a>生产订单的间接成本

处理生产订单的交易时，可以配置间接成本以捕获总帐中的开销成本或附加费用。 当您过帐领料单日记帐或报告为完工入库日记帐时，库存中将确认间接成本的实际交易。 过帐结束日记帐时，会在库存中确认间接成本的财务交易。

您可以确认与 **工艺卡** 日记帐或 **作业卡** 日记帐相关的时间消耗量间接成本。 当您结束生产订单时，这些交易会被冲销并过帐到财务帐户。 有关详细信息，请转到[成本计算单](/supply-chain/cost-management/costing-sheets.md)。

## <a name="controlling-the-level-of-ledger-posting"></a>控制分类帐过帐的级别

在 **生产控制参数** 页上，可以使用 **分类帐过帐** 字段设置生产流程的分类帐过帐级别。 

提供以下字段：

### <a name="item-and-resource"></a>物料和资源

在 **分类帐过帐** 字段中选择 **物料和资源** 选项时，过帐帐户来自工艺路线中工序的资源或资源组。 特定资源的相关帐户将是第一个过帐选项。 如果未指定帐户，则将使用针对资源组指定的帐户。 对于工艺路线中的每个工序行，都可以指定一个资源作为 **成本计算资源**。 此资源用于确定要使用的帐户。 当组织将运营成本分配给资源时，通常使用此选项。 资源的成本通常较高，用于帮助做出“生产与购买”决策。 这是最详细的过帐配置，并且允许对过帐进行最精细的控制，还可以对生产流程进行非常详细的分析。

### <a name="item-and-category"></a>物料和类别

在 **分类帐过帐** 字段中选择 **物料和类别** 选项时，过帐帐户将来自与工艺路线中的每一行相关的 **成本类别** 页面。 工艺路线中的每个工序行都可以包含三个成本类别：**设置** 时间、**运行** 时间和 **数量**。 当您组织的主要关注点是流程效率和活动持续时间时，通常使用此选项。 此选项是一种更汇总的过帐方式，并且仍然会提供一种按类别对成本进行分组的方法。

### <a name="production-group"></a>生产组

当您在 **分类帐过帐** 字段中选择 **生产组** 选项时，过帐帐户来自 **生产组** 页面。 **生产组** 通常在多个生产线运行相似产品或具有相似设备时使用。 您可以使用此选项比较两个不同的生产组之间的成本。  
  
> [!NOTE]
> 如果使用了计算成品成本的标准方法，则最终交易将反映此情况。 如果实际成本和使用标准方法计算的成本之间存在差别，它将过帐到显示利润或损失的科目中。

### <a name="route-groups-and-ledger-posting"></a>工艺路线组和分类帐过帐

对于工艺路线中的每个工序行，都指定了 **工艺路线组**。 **估计和成本核算** 组中 **工艺路线组** 上的 **设置时间**、**运行时间** 和 **数量** 字段用于控制对生产订单过帐 **作业卡** 或 **工艺卡日记帐** 时，是否将时间用于成本计算。 如果禁用了这些选项，则将不会在总帐中为时间消耗量创建凭证。

要将 **工艺卡** 或 **作业卡日记帐** 过帐到生产订单的总帐，必须满足以下条件：

-   必须在 **工艺路线组** 页上的 **估计和成本核算** 组中选择 **设置时间**、**运行时间** 或 **数量** 字段。
-   必须在 **成本类别**、**工艺路线**、**工艺路线组** 或 **生产组** 页中为以下过帐类型指定主科目：
    -   估计的已吸收制造成本
    -   估计的已消耗制造成本，WIP

以下图表显示工艺路线组与给定工艺路线中每个工序（工艺路线行）的总成本计算的关系。 每个工艺路线行都有一个工艺路线组。 工艺路线组控制设置时间、运行时间和数量的参数。 **成本类别** 选项卡具有基于工艺路线组设置启用的 **设置**、**运行** 和 **数量** 这三个选项。 **计时** 快速选项卡具有三个基于工艺路线组的字段。

使用的配方基于是否在工艺路线组中启用了该选项。 所选成本类别的成本乘以时间计时中输入的数量以计算总成本。

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="工艺路线组与总计算成本的关系。":::
工艺路线组与总计算成本的关系。 每个工艺路线行都有一个工艺路线组。 工艺路线组控制设置时间、运行时间和数量的参数。 “成本类别”选项卡具有基于工艺路线组设置启用的“设置”、“运行”和“数量”这三个选项。 “计时”快速选项卡具有三个基于工艺路线组输入和成本计算的字段。 使用的配方基于是否在工艺路线组中启用了该选项。 所选成本类别的成本乘以时间计时中输入的数量以计算总成本。
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>示例过帐模板配置

下表显示具有示例主帐户和描述的默认过帐类型的示例。 

 - **借记/贷记** 列指示交易通常是借记还是贷记，在某些情况下可以过帐任意一方。 
 - **结算帐户** 列指示过帐类型是否为结算帐户。 在过帐以后的交易记录时，将自动冲销此帐户中过帐的金额。 
 - **P/F** 列指示 **P** 表示实际过帐，**F** 表示财务过帐。 
 - **跟随** 列指示特定过帐类型的主科目通常是否与其他过帐类型相同。 列中的值指示通常采用的过帐类型。

> [!NOTE]
> 推荐的主科目和主科目名称为建议值。 我们建议您与您的会计师合作，确定适合您的业务需求的最佳配置。


| 过帐类型  | 主帐户示例 | 主帐户名称示例| 帐户类型 | 借方/贷方？ | 结算帐户 | 实际或财务 | 跟随 | Description |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| 估计的已消耗物料的成本      | 140100               | 材料库存        | 资产        | 贷方         | Y                | P                     | 已消耗物料的成本                | 过帐生产订单的领料单日记帐时使用此帐户。 此帐户的抵销科目是“物料的估计成本，WIP”。 在生产订单结束时，将自动冲销此帐户中的金额。 此帐户表示资产负债表中的库存科目。       |
| 估计的已消耗物料的成本，WIP | 150150               | 生产 WIP – 材料 | 资产        | 借方          | Y                | P                     | 估计的制造成本，WIP          | 过帐生产订单的领料单日记帐时使用此帐户。 此帐户的抵销科目是“估计的已消耗物料的成本”。 在生产订单结束时，将自动冲销此帐户中的金额。 此帐户表示资产负债表中的 WIP。                  |
| 估计的制造成本               | 140200               | 成品库存   | 资产        | 借方          | Y                | P                     | 制造成本                         | 过帐生产订单的“报告为完工入库”日记帐时使用此帐户。 此帐户的抵销科目是“估计的制造成本，WIP”。 在生产订单结束时，将自动冲销此帐户中的金额。 此帐户表示资产负债表中的库存科目。 |
| 估计的制造成本，WIP          | 150150               | 生产 WIP – 材料 | 资产        | 贷方         | Y                | P                     | 制造成本，WIP                    | 过帐生产订单的“报告为完工入库”日记帐时使用此帐户。 此帐户的抵销科目是“估计的制造成本”。 在生产订单结束时，将自动冲销此帐户中的金额。 此帐户表示资产负债表中的 WIP。                     |
| 已消耗物料的成本                | 140100               | 材料库存        | 资产        | 贷方         | N                 | 周五                     | 估计的已消耗物料的成本      | 此帐户用于识别结束流程期间在生产订单中消耗的物料。 此帐户的抵销科目是“已消耗物料的成本，WIP”。                                                                                                    |
| 已消耗物料的成本，WIP           | 150150               | 生产 WIP – 材料 | 资产        | 借方          | N                 | 周五                     | 估计的已消耗物料的成本，WIP | 此帐户用于确认结束流程期间在生产订单中消耗的 WIP 中的物料。 此帐户的抵销科目是“已消耗物料的成本”。                                                |
| 制造成本                         | 140200               | 成品库存   | 资产        | 借方          | N                 | 周五                     | 估计的制造成本               | 此帐户用于确认结束生产订单时按生产订单生产的成品的成本。 此帐户的抵销科目是“制造成本，WIP”帐户。                                                                  |
| 制造成本，WIP                    | 150150               | 生产 WIP – 材料 | 资产        | 贷方         | N                 | 周五                     | 估计的制造成本，WIP          | 此帐户用于确认结束生产订单时按生产订单生产的 WIP 中成品的成本。 此帐户的抵销科目是“制造成本”帐户。                                     |

> [!NOTE]
> **精益服务 WIP 收据** 和 **精益服务 WIP 结算帐户** 与倒冲成本计算法一起用于精益制造。 有关详细信息，请转到[倒冲成本计算法](/supply-chain/cost-management/backflush-costing.md)。
