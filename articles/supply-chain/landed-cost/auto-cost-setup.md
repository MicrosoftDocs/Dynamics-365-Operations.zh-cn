---
title: 自动成本设置
description: 本文介绍如何为各个入站航行级别设置成本规则。 根据这些规则，系统计算成本并自动添加。 因此，用户不必手动添加成本。
author: Weijiesa
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 02c78789fc7531c267cee936fa30a395e6d0b62f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852380"
---
# <a name="auto-costs-setup"></a>自动成本设置

[!include [banner](../../includes/banner.md)]

您可以使用 **自动成本** 页设置各个成本区域（如航行、装运集装箱、帐页、采购订单、物料或转移单行）的成本规则。 根据规则以及用户在创建成本区域之一的记录时选择的字段，系统计算成本并自动添加。 因此，用户不必手动添加成本。

要使用自动成本，请转到 **登陆成本 \> 成本计算设置 \> 自动成本**。 然后按照本文其余部分的说明设置自动成本规则。

## <a name="work-with-cost-areas"></a>使用成本区域

自动成本的工作方式类似于贸易协议或自动杂项费用。 每个自动成本记录属于一个特定的成本级别。 使用 **自动成本** 页的列表窗格中的 **成本区域** 字段来选择您要使用的成本区域。 列表窗格仅显示属于当前选定成本区域的自动成本。 您创建的任何自动成本将属于当前选定的成本区域。

成本区域让系统能够在成本区域中的采购订单行之间分摊成本。 例如，一个装运集装箱的成本会将值分摊到该装运集装箱中的所有产品。 如果有两个或更多装运集装箱，可以为每个装运集装箱指定相同的成本类型。 因此，可以使用集装箱类型来查找正确的自动成本。

## <a name="buttons-on-the-action-pane"></a>操作窗格上的按钮

下表描述了 **自动成本** 页上操作窗格上可用的按钮。

| 按钮 | 说明 |
|---|---|
| 编辑​​ | 编辑现有的自动成本。 |
| 新项 | 创建自动成本。 |
| Delete | 删除自动成本。 |
| 复制自 | 创建基于现有记录的新自动成本记录。 然后，您可以随意编辑新记录。 此按钮可帮助您快速创建新的自动成本。 |
| 显示维度 | 打开一个对话框，您可以在其中选择针对您查看的成本交易记录显示的库存维度。 如果清除复选框，成本交易记录将显示更少的库存维度。 因此，将显示更少的交易记录详细信息。 如果为自动成本指定了库存维度，仅当将指定的库存维度用于航行中的物料时，才应用自动成本。 |

## <a name="settings-on-the-header"></a>标头上的设置

标头部分的设置组合确定何时以及如何将特定的自动成本添加到航行中。 仅当自动成本的详细信息与该成本区域的抬头的详细信息匹配时，才会将自动成本应用于航行、装运集装箱或帐页。 所有匹配的自动成本的总和确定航行的估计登陆成本。 此成本在船只或航行中的所有物料之间分摊。

下表描述了标头部分可能出现的所有字段。 但是，可用的特定字段会因当前选择的成本区域和显示维度而异。

| 字段 | 说明 |
|---|---|
| **帐户编码** | <p>选择以下值之一：</p><ul><li>**表** – 此成本规则仅适用于特定供应商。</li><li>**组** – 此成本规则适用于特定供应商组。 系统将查找与供应商记录关联的[供应商成本类型组](costing-parameters-setup.md)。</li><li>**所有** – 此成本规则适用于所有供应商。 |
| **装运公司** | 选择成本规则适用的供应商或供应商组。 只有当您在 **帐户代码** 字段中选择 *表* 或 *组* 时，此字段才可用。 |
| **关税代理** | 选择成本规则适用的供应商或供应商组。 只有当您在 **帐户代码** 字段中选择 *表* 或 *组* 时，此字段才可用。 |
| **物料代码** | <p>选择以下值之一：</p><ul><li>**表** – 此成本规则仅适用于特定物料。</li><li>**组** – 此成本规则适用于特定物料组。 系统将查找与物料记录关联的[物料成本类型组](costing-parameters-setup.md)。</li><li>**所有** – 此成本规则适用于所有物料。|
| **物料关系** | 选择成本规则适用的物料或物料组。 只有当您在 **物料代码** 字段中选择 *表* 或 *组* 时，此字段才可用。 |
| **交货模式** | 选择成本规则适用的交货方式（如空运或海运）。 |
| **集装箱类型** | 将用于装运货物的装运集装箱的类型。 仅当自动成本设置中的集装箱类型与航行的集装箱类型匹配时，才可以将自动成本应用于航行。 |
| **发运港口** 和 **到达港口** | 航行的源（“发运”）港口和目标（“到达”）港口。 （有些装运集装箱可能具有不同的“到达”港口，因为航行可能会在多个港口停留。）只有自动成本设置中的“发运”和“到达”港口与航行的“发运”和“到达”港口匹配时，才可以将自动成本应用于航行。 |
| **自动成本编号** | 自动成本规则的唯一标识符。 此字段的值根据 **登陆成本参数** 页上设置的编号规则自动生成。 |
| **库存维度** | 有些成本区域让您可以在标头中包括一个或多个物料维度（如大小、颜色、仓库和批处理号）。 在操作窗格上选择 **显示维度** 来选择应包括的维度。 |

## <a name="settings-on-the-lines-fasttab"></a>行快速选项卡上的设置

在 **行** 快速选项卡上，为对航行中的采购订单行应用成本时可以使用的每个货币添加一行。 

对于物料和采购订单，系统会将每个采购订单行的货币与 **行** 快速选项卡上指定的货币进行匹配。 将仅应用为匹配的行或物料设置的成本价值。 如果没有为行或物料的货币设置行，自动成本不会应用于该行或物料。

对于其他类型的成本区域，**行** 快速选项卡上的所有行将应用于与标头上建立的值匹配的每个航行、装运集装箱、帐页或转移单行。

下表描述了每个行上可能出现的所有字段。 但是，可用的特定字段会因当前选择的成本区域而异。

| 字段 | 说明 |
|---|---|
| **货币** | 选择行要应用的货币。 此货币与采购订单相关。 当系统尝试查找应该应用于航行及其航行行的自动成本时，会选择与采购订单具有相同货币的行。 仅当 **成本区域** 字段设置为 *采购订单* 或 *物料* 时，此字段才可用。 |
| **成本类型代码** | 成本类型。 |
| **分摊方法** | <p>用于将成本分摊到行的方法。 选项如下：</p><ul><li><p>**百分比** – **成本价值** 字段的值是应用于商品总值的百分比。</p><p>例如，如果 **成本价值** 字段设置为 *10*，商品总价值为 800 美元，成本价值则为 80 美元（= 800 美元 × 10%）。</p></li><li>**数量** – 成本将根据商品的数量进行分摊。</li><li>**金额** – 成本将根据商品的价值进行分摊。</li><li>**体积** – 成本将根据商品的体积进行分摊。 体积在物料主记录中指定。</li><li>**重量** – 成本将根据商品的重量进行分摊。 重量在物料主记录中指定。</li><li>**容量** – 成本将根据商品的容量度量进行分摊。</li><li><p>**度量** – 此选项支持在 **登陆成本** 模块中指定度量。 不知道商品单个体积或重量，但需要比 **金额** 和 **数量** 选项允许执行的更准确分摊的组织经常使用此选项。 货运转运商或代理将在物料级别或采购订单级别向组织提供重量或体积度量。</p><p>例如，海运运费等于 900 美元。 物料 A 的重量为 800 千克 (kg)，体积为 2 立方米 (m³)。 物料 B 的重量为 100 kg，体积为 1 m³。 以下是按重量分摊成本的结果：</p><ul><li>物料 A = 800 美元</li><li>物料 B = 100 美元</li></ul><p>以下是按体积分摊成本的结果：</p><ul><li>物料 A = 600 美元</li><li>物料 B = 300 美元</li></ul><p>**注意：** 当 **分摊方法** 字段设置为 *度量* 时，系统将使用为成本区域（装运集装箱）和行输入的度量。 这些度量不一定要加和计算出预期的总数。 但是，如果您需要它们加和得出预期的总数，可以使用统计信息查看总度量值来进行检查。 装运或集装箱级别的度量提示设置和度量自动更新在航行标头上设置。</p></li></ul> |
| **开始日期** | 如果存在日期范围，指定成本计算日期范围的开始日期。 此日期是应用自动成本的第一个日期。 |
| **截止日期** | 如果存在日期范围，指定成本计算日期范围的结束日期。 此日期是应用自动成本的最后一个日期。 |
| **类别** | <p>选择应用于计算成本的方法。 选项如下：</p><ul><li>**固定** – 成本将根据分摊方法进行分摊。</li><li>**件** – 成本将按件分摊。 因此，不会使用分摊方法。</li><li>**百分比** – 将添加商品价值的百分比。 因此，不会使用分摊方法。</li><li>**比率** – 如果存在数量明细，则选择此选项。 行的 **分摊方法** 字段必须设置为 *度量*。</li><ul> |
| **已按数量细分** | <p>选中此复选框，可使 **行** 快速选项卡上的 **数量分段** 按钮可用。 数量分段支持根据航行的采购订单行上的数量将成本分解，让不同的成本可以变化。 此功能通常在交货方式为空运时使用。 行的 **类别** 字段必须设置为 *比率*。</p><p>数量与在 **摊分方法** 字段中选择的选项有关。 成本价值将取决于在 **成本价值** 字段中输入的数量。<p>例如，数量为 45–100 kg，每个度量（如 kg/m³）将产生 6.00 美元的费用。 数量超过 100 kg，每个度量（如 kg/m³）将产生 5.50 美元的费用。</p> |
| **成本价值** | 输入成本的值。 |
| **成本币种代码** | 选择成本使用的货币。 |
| **物料销售税组** | 选择成本的税码。 |
| **最低成本** | <p>此字段仅在选中 **按数量细分** 复选框时应用。 如果度量未达到此值，无论在 **数量分段** 页上指定的成本是多少，都将选择最小值。<p>例如，数量为 0–45 kg，每个度量 (kg/m³) 将产生 6 美元的费用。 数量为 46–100 kg，每个度量 (kg/m³) 将产生 5.50 美元的费用。 如果装运了 2 kg，数量分段将创建 12 美元的成本价值。 但是，如果 **最低成本** 字段设置为 *100 美元*，最终成本将为 100 美元。</p> |
| **聚合** | 选中此复选框将允许用户将此成本从装运集装箱级别移到航行级别。 在这种情况下，可以在装运集装箱级别自动计算成本。 不过，也可以将它们合并，然后在航行所有集装箱中的所有物料之间分摊，而不是单个装运集装箱中的所有物料。 |
| **链接的成本类型** | <p>通过指定要链接到的行的 **成本类型代码** 值，将当前行链接到同一自动成本记录中的另一行。 仅当当前行的 **类别** 字段设置为 *百分比* 时，此功能才可用。 当当前行链接到另一行时，当前行的成本将基于另一行的成本。</p><p>例如，运费为 1,000 美元，您希望燃油附加费是运费成本的 10%。 在这种情况下，行的 **类别** 值必须为 *百分比*，**成本价值** 值必须为 *10%*，**链接成本类型** 值必须为 *运费*。</p> |
| **价值调整** 和 **调整金额** | <p>使用这些字段可以调整各个百分比值的价值和金额。 它们仅在 **成本区域** 字段设置为 *物料* 时可用。</p><p>可以为物料的不同组件设置不同的成本计算。 物料的一个组件可能与该物料的其他组件具有不同的成本百分比。 有时需要使用此方法来以不同的比率对商品的特定部分进行估价。</p><p>例如，手表的关税以两种比率计算：手表的一个组件的关税税率为 10%，另一个组件的关税税率为 2%。 在这种情况下，成本计算将在两个组件之间拆分。</p><p>将为物料计算成本，但成本价值将按具有不同成本类别的组件的值进行调整。 然后，可以使用按其调整之前计算的金额来计算其余组件的成本。</p><p>例如，手表的组件 A 的成本为 9.50 美元，10% 关税，组件 B 的成本为 0.50 美元，2% 关税。 因此，总成本为 10.00 美元。 第一个条目对应 10% 行。 使用以下值：</p><ul><li>**类别**：*百分比*</li><li>**成本价值**：*10*</li><li>**值已调整**：*调整依据*</li><li>**调整值**：*-0.50*</li></ul><p>此设置指定在计算 10% 关税费用之前，必须将物料成本（10 美元）降低 0.50 美元（组件 B 的价格）。 因此，将对 9.50 美元应用 10%。</p><p>第二个条目对应 2% 行（按其调整前一个条目的 0.50 美元）。 使用以下值：</p><ul><li>**类别**：*百分比*</li><li>**成本价值**：*2*</li><li>**值已调整**：*使用*</li><li>**调整**：*0.50*</li></ul><p>此设置计算组件 B 应支付的其余关税。</p> |
