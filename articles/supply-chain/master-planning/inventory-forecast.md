---
title: 库存预测
description: 本文介绍了可用于在 Microsoft Dynamics 365 Supply Chain Management 中创建库存预测的供应和需求预测功能。
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 16e806de9014e76404ee2807ec9132ae836e300f
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739970"
---
# <a name="inventory-forecasts"></a>库存预测

[!include [banner](../includes/banner.md)]

本文介绍了如何查看和创建库存预测。 您可以为物料、物料组、物料分配参数、客户帐户、客户组、供应商帐户和供应商组创建和查看供应和需求预测行。

对于每个预测行，您都可以选择使用的预测模型。 然后，可以指定物料或物料组，以及数量或交易金额。 还可以设置时间计划以分配预测数量。

供应和需求预测行为物料和模型的相同组合生成库存预测。 此库存预测表示为同一物料输入的供应和需求之间的平衡。 不可编辑。 库存预测可帮助库存管理团队审查在已预测的即将到来的期间内物料现有库存的预期变化。

在输入需求和/或供应后，您可以运行预测计划以计算对材料的总需求和产能，并生成计划订单。

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>查看并手动输入预测行

使用此过程手动创建产品的预测行。

还有其他方法可以创建预测行：

- [生成统计基准预测](generate-statistical-baseline-forecast.md)。
- [导入历史数据以进行需求预测](import-historical-data.md)。
- [使用 Microsoft Azure 机器学习 Web 服务生成预测](demand-forecasting-setup.md)。
- [使用数据管理框架（ForecastDemandForecastEntryStaging 和 ForecastSupplyForecastEntryStaging 数据实体）导入需求或供应预测行](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)。

如步骤 1 中的表所示，可通过不同方式访问使用的页面。

1. 根据您要为其创建预测的实体类型以及您要创建的预测类型，打开供应、需求或库存预测页面，如下表所述。

    | 实体 | 描述 |
    |---|---|
    | 已发布产品 | <ol><li>转到 **产品信息管理 \> 产品 \> 已发布产品**。</li><li>选择要为其创建预测的产品。</li><li>在操作窗格上，在 **计划** 选项卡的 **预测** 组中，选择 **需求预测**、**供应预测** 或 **库存预测**，具体取决于您要使用的预测类型。</li></ol> |
    | 已发布的产品变型 | <ol><li>转到 **产品信息管理 \> 产品 \> 已发布产品变型**。</li><li>选择要为其创建预测的变型。</li><li>在操作窗格上，在 **计划** 选项卡的 **预测** 组中，选择 **需求预测**、**供应预测** 或 **库存预测**，具体取决于您要使用的预测类型。</li></ol> |
    | 物料组 | <ol><li>转到 **库存管理 \> 设置 \> 库存 \> 物料组**。</li><li>选择要为其创建预测的物料组。</li><li>在操作窗格上，选择 **预测 \> 需求**、**预测 \> 供应** 或 **预测 \> 库存预测**，具体取决于您要使用的预测类型。</li></ol> |
    | 物料分配参数 | <ol><li>转到 **库存管理 \> 设置 \> 预测**。</li><li>选择要为其创建预测的物料分配参数。</li><li>在操作窗格上，选择 **需求预测**。</li></ol> |
    | 客户 | <ol><li>转到 **主计划 \> 预测 \> 手动预测条目 \> 客户**。</li><li>选择要为其创建预测的客户。</li><li>在操作窗格上，选择 **定义需求预测**。</li></ol> |
    | 客户组 | <ol><li>转到 **主计划 \> 预测 \> 手动预测条目 \> 客户组**。</li><li>选择要为其创建预测的客户组。</li><li>在操作窗格上，选择 **定义需求预测**。</li></ol> |
    | 供应商 | <ol><li>转到 **主计划 \> 预测 \> 手动预测条目 \> 供应商**。</li><li>选择要为其创建预测的供应商。</li><li>在操作窗格上，选择 **条目** 以打开 **供应预测** 页面。</li></ol> |
    | 供应商组 | <ol><li>转到 **主计划 \> 预测 \> 手动预测条目 \> 供应商组**。</li><li>选择要为其创建预测的供应商组。</li><li>在操作窗格上，选择 **条目** 以打开 **供应预测** 页面。</li></ol> | 
    | 所有行 | <ul><li>转到 **主计划 \> 预测 \> 需求预测行** 或 **主计划 \> 预测 \> 供应预测行**，具体取决于您要使用的预测类型。</li></ul> |

    根据您的选择，显示 **供应预测** 或 **需求预测** 页面。 它显示您在打开页面之前选择的记录的任何现有预测行。

1. 在操作窗格上，选择 **新建** 以在页面上部的网格中添加预测行。
1. 在新行上，在 **模型** 字段中，选择要使用的预测模型。 然后，根据需要输入其他详细信息，例如物料、物料组、客户或供应商帐户或组、物料数量或交易总额。 有关 **供应预测** 和 **需求预测** 页面上的可用字段的完整详细信息，请参阅本文的后面一节。
1. 若要在整个期间分发预测，请在 **概述** 选项卡上，在工具栏上选择 **分配预测**。
1. 在 **分配** 网格中，查看用于分发预测数量的时间范围和时间间隔。

## <a name="supply-forecast-lines"></a>供应预测行

供应预测使您可以为必须购买的物料创建计划。 它告诉采购和寻料人员他们希望订购什么物料。

您可以按物料、物料组、物料分配参数、供应商和供应商组输入供应预测。 有关为各种实体和记录打开 **供应预测** 页面的所有方法的信息，请参阅本文前面的[查看并手动输入预测行](#manual-entry)一节。

**供应预测** 页面上部提供供应预测行网格和一组选项卡，可用于查看和设置有关选定预测行的更多信息。 页面下部提供 **分配** 网格。

以下子部分介绍了每个选项卡上可用的所有字段，以及页面的操作窗格上和 **概述** 选项卡的工具栏上可用的所有命令。

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>供应预测页面上的操作窗格命令

下表介绍了 **供应预测** 页面的操作窗格上可用的命令。

| 命令 | 说明 |
|---|---|
| 保存 | 保存您的当前设置。 |
| 编辑​​ | 启用页面上要编辑的设置。 |
| 新项 | 将预测行添加到上部网格。 |
| Delete | 从上部网格中删除选定的预测行。 |
| 预测余额 | 查看为当前会计年度的选定行的模型 ID 计算的预测余额。 余额按期间（月）拆分。 |
| 现金流量预测 | 查看已分配到总帐的预测交易。 有关详细信息，请参阅[现金流预测](../../finance/cash-bank-management/cash-flow-forecasting.md)。 |
| 库存 \> 显示维度 | 选择应显示在 **概述** 选项卡的网格中的库存维度。 |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>供应预测页面的概述选项卡上的工具栏命令

下表介绍了 **供应预测** 页面的 **概述** 选项卡的工具栏上可用的命令。

| 命令 | 说明 |
|---|---|
| 分配预测 | 如果要使用分配方法，为预测交易生成单独的计划行。 然后，按日期（根据选定的时间间隔）、数量和整个时间范围的金额分发行的数量。 （请参阅本文后面的[分配预测](#allocate-forecast)一节。） |
| 批量更新 | 打开 **编辑预测交易** 页面。 （请参阅本文后面的[批量更新预测交易](#bulk-update)一节。） |
| 库存预测 | 打开为选定物料/模型组合筛选的 **库存预测** 页面的视图。 （请参阅本文后面的[库存预测](#inventory-forecast)一节。） |
| 创建物料需求 | 打开一个对话框，您可以在其中为与项目相关的预测交易创建物料需求和销售订单或物料日记帐行。 尽管此命令可用于供应预测行和需求预测行，但不能用于 **供应预测** 页面。 |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>供应预测页面上的概述选项卡

下表介绍了 **供应预测** 页面的 **概述** 选项卡上的字段。

| 字段 | 说明 |
|---|---|
| **型号** | 交易所关联的预测模型。 |
| **日期** | 交易记录的开始日期。 |
| **供应商帐户** | 交易所关联的供应商帐户。 |
| **供应商组** | 交易所关联的供应商组。 |
| **物料编号** | 物料的标识符。 |
| **物料组** | 交易所关联的物料组。 |
| **物料分配参数** | 与预测关联的物料分配参数。 |
| **CW 数量** | 采用指定的实际称重单位的预测数量。 |
| **CW 单位** | 采购物料所采用的实际称重单位。 自动从物料设置中检索值。 |
| **数量** | 采用指定的采购单位的预测数量。 |
| **单位** | 采购物料所采用的单位。 自动从物料设置中检索值。 但是，如果设置了单位转换，您可以修改它。 |
| **金额** | 预测交易占该预测的份额，即总额减去折扣。 |
| **货币** | 用于预测交易的货币。 默认货币将自动输入，当您可以选择其他货币。 |
| （其他维度） | 其他维度可以在网格中显示为列。 若要选择显示的其他维度，请在操作窗格上选择 **显示维度**。 |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>供应预测页面上的常规选项卡

**常规** 选项卡显示有关当前在 **概述** 选项卡上选定的行的详细信息。其中一些信息与 **概述** 选项卡中重复。下表介绍了对 **常规** 选项卡唯一的字段。

| 字段 | 说明 |
|---|---|
| 报表 | 将此选项设置为 *是* 以将交易包括在报告中。 |
| 注释 | 输入有关预测交易的任何注释。 |
| 可用 | 选中该复选框以将交易包括在预算报告中。 |
| 包含在现金流量预测中 | 选中该复选框以将预测交易分配给总帐。 不能为报告交易修改此复选框的设置。 |
| 销售税组 | 用于为预测交易指定税务的税组。 |
| 物料销售税组 | 用于为预测交易指定税务的物料税组。 |
| 方法 | <p>选择用于分配预测交易的方法：</p><ul><li>**无** – 不进行分配。</li><li>**期间** – 预测每个期间的相同数量。 如果选择此值，在 **每** 字段中指定数量并在 **单位** 字段中指定时间单位。</li><li>**参数** – 根据在 **期间参数** 字段中指定的期间分配参数分配预测。 要考虑季节性变动时可以使用此方法。</li></ol>|
| 每 | <p>输入预测向前延长的时间间隔数。 此字段仅在 **方法** 字段中选择 *期间* 时才可用。</p><p>例如，在 **方法** 字段中选择 *期间*，在 **每** 字段中输入 *1*，在 **单位** 字段中选择 *月*。 在 **结束** 字段中，指定向前延伸一年的结束日期。 在此情况下，基于在标头行中指定的物料和数量为明年的每个月创建一个预测行。</p> |
| 单位 | 选择时间间隔的单位：*天*、*月* 或 *年*。 然后，分配对应于您在 **每** 字段中指定的天数、月数或年数。|
| 期间参数 | 指定期间分配参数。 |
| 结束日期 | 使用 **每** 和 **单位** 字段时，指定结束日期。 |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>供应预测页面上的物料选项卡

**物料** 选项卡显示有关当前在 **概览** 选项卡上选择的行的更多物料信息。

**物料** 选项卡顶部的网格中的物料信息还与 **概述** 选项卡上显示的信息重复。此外，它还包括 **单位价格** 字段，其中显示在 **单位** 字段中指定的单位数的采购价格。 单位价格自动从物料设置中检索，但您可以修改它。

网格下方的字段提供更多物料详细信息。 其中一些信息与 **概述** 选项卡中重复。下表介绍了对 **物料** 选项卡唯一的字段。

| 字段 | 说明 |
|---|---|
| 计价单位 | 采购价格适用的单位数量。 值自动从物料表中检索，但您可以修改它。 |
| 采购费用 | 采购价格的固定费用。 该费用与数量无关。 |
| 折扣率 | 用百分比表示的折扣。 |
| 折扣金额 | 用每个销售单位的金额表示的折扣。 |
| 总额 | 未应用折扣时的金额。 |
| 数量 | 用物料的库存单位表示的交易数量。 |
| 下级物料清单 | 特定的下级物料清单的物料清单 (BOM) 编号。 |
| 下级运输路线 | 特定的下级工艺路线的工艺路线编号。 |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>供应预测页面上的财务维度选项卡

**财务维度** 选项卡显示当前在 **概述** 选项卡上选定的行的所有财务维度值。

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>供应预测页面上的库存维度选项卡

**库存维度** 选项卡显示当前在 **概述** 选项卡上选定的行的所有库存维度值。

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>供应预测页面上的分配网格

如果您使用的是物料分配参数，或者如果您已针对一个或多个未来期间输入物料预测，可以通过在 **概述** 选项卡的工具栏上选择 **分配预测** 来分配预测。然后，按照 **分配** 网格中的行指示的方式分发数量。

## <a name="demand-forecast-lines"></a>需求预测行

需求预测允许您输入或生成客户的需求。 它可以帮助销售和市场营销人员通知主计划人员有关即将到来的预测期间内的预期需求。

您可以按物料、物料组、物料分配参数、客户和客户组输入需求预测。 有关为各种实体和记录打开 **需求预测** 页面的所有方法的信息，请参阅本文前面的[查看并手动输入预测行](#manual-entry)一节。

**需求预测** 页面上部提供需求预测行网格和一组选项卡，可用于查看和设置有关选定预测行的更多信息。 页面下部提供 **分配** 网格。

以下子部分介绍了每个选项卡上可用的所有字段，以及页面的操作窗格上和 **概述** 选项卡的工具栏上可用的所有命令。

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>需求预测页面上的操作窗格命令

下表介绍了 **需求预测** 页面的操作窗格上可用的命令。

| 命令 | 说明 |
|---|---|
| 保存 | 保存您的当前设置。 |
| 编辑​​ | 启用页面上要编辑的设置。 |
| 新项 | 将预测行添加到上部网格。 |
| Delete | 从上部网格中删除选定的预测行。 |
| 预测余额 | 查看为当前会计年度的选定行的模型 ID 计算的预测余额。 余额按期间（月）拆分。 |
| 现金流量预测 | 查看必须分配到总帐的预测交易。 有关详细信息，请参阅[现金流预测](../../finance/cash-bank-management/cash-flow-forecasting.md)。 |
| 显示维度 | 选择应显示在 **概述** 选项卡的网格中的产品、存储和跟踪维度。 |
| 总帐预览 | 查看选定交易的总帐条目。 |
| 转移报价行 | 将报价单行转移到选定项目。 |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>需求预测页面的概述选项卡上的工具栏命令

下表介绍了 **需求预测** 页面的 **概述** 选项卡的工具栏上可用的命令。

| 命令 | 说明 |
|---|---|
| 分配预测 | 如果要使用分配方法，为预测交易生成单独的计划行。 然后，按日期（根据选定的时间间隔）、数量和整个时间范围的金额分发行的数量。 （请参阅本文后面的[分配预测](#allocate-forecast)一节。）|
| 批量更新 | 打开 **编辑预测交易** 页面。 （请参阅本文后面的[批量更新预测交易](#bulk-update)一节。） |
| 库存预测 | 打开为选定物料/模型组合筛选的 **库存预测** 页面的视图。 （请参阅本文后面的[库存预测](#inventory-forecast)一节。） |
| 创建物料需求 | 打开一个对话框，您可以在其中为与项目相关的预测交易创建物料需求和销售订单或物料日记帐行。 |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>需求预测页面上的概述选项卡

下表介绍了 **需求预测** 页面的 **概述** 选项卡上的字段。

| 字段 | 说明 |
|---|---|
| **任务名称** | 用于创建预测行的批处理任务的名称。 |
| **型号** | 交易所关联的预测模型。 |
| **日期** | 交易记录的开始日期。 |
| **客户帐户** | 交易所关联的客户帐户。 |
| **客户组** | 交易所关联的客户组。 |
| **物料编号** | 物料的标识符。 |
| **产品名称** | 物料的描述。 |
| **物料分配参数** | 库存预测分配期间使用的物料分配参数。 |
| **销售数量** | 采用指定的销售单位的交易数量。 |
| **单位** | 销售物料所采用的单位。 |
| **金额** | 预测交易占该预测的份额，即不包括折扣的总额。 |
| **销售价** | 在 **价格单位** 字段中指定的单位数量的销售价格。 值从物料设置中检索，但您可以修改它。 |
| **销售币种** | 用于预测交易的货币。 默认货币将自动输入，当您可以选择其他货币。 |
| **CW 数量** | 采用指定的实际称重单位的预测数量。 |
| **CW 单位** | 出售物料所采用的实际称重单位。 自动从物料设置中检索值。 |
| （其他维度） | 其他产品、存储和跟踪维度可以在网格中显示为列。 若要选择显示的其他维度，请在操作窗格上选择 **显示维度**。 |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>需求预测页面上的常规选项卡

**常规** 选项卡显示有关当前在 **概述** 选项卡上选定的行的详细信息。其中一些信息与 **概述** 选项卡中重复。下表介绍了对 **常规** 选项卡唯一的字段。

| 字段 | 说明 |
|---|---|
| 需求预测序列号 | 需求预测行的唯一编号。 通过使用在 **主计划参数** 页面上为需求预测选定的编号规则生成此编号。 |
| 物料组 | 交易所关联的物料组。 |
| 报表 | 将此选项设置为 *是* 以将交易包括在报告中。 |
| 注释 | 输入有关预测交易的任何注释。 |
| 可用 | 选中该复选框以将交易包括在预算报告中。 不能为报告交易修改此复选框的设置。 |
| 包含在现金流量预测中 | 选中该复选框以将预测交易分配给总帐。 不能为报告交易修改此复选框的设置。 有关详细信息，请参阅[现金流预测](../../finance/cash-bank-management/cash-flow-forecasting.md)。 |
| 销售税组 | 用于为预测交易指定税务的税组。 |
| 物料销售税组 | 用于为预测交易指定税务的物料税组。 |
| 方法 | <p>选择用于分配预测交易的方法：</p><ul><li>**无** – 不进行分配。</li><li>**期间** – 预测每个期间的相同数量。 如果选择此值，在 **每** 字段中指定数量并在 **单位** 字段中指定时间单位。</li><li>**参数** – 根据在 **期间参数** 字段中指定的期间分配参数分配预测。 要考虑季节性变动时可以使用此方法。</li><ul>|
| 每 | <p>输入预测向前延长的时间间隔数。 此字段仅在 **方法** 字段中选择 *期间* 时才可用。</p><p>例如，在 **方法** 字段中选择 *期间*，在 **每** 字段中输入 *1*，在 **单位** 字段中选择 *月*。 在 **结束** 字段中，指定向前延伸一年的结束日期。 在此情况下，基于在标头行中指定的物料和数量为明年的每个月创建一个预测行。 |
| 单位 | 选择时间间隔的单位：*天*、*月* 或 *年*。 然后，分配对应于您在 **每** 字段中指定的天数、月数或年数。|
| 期间参数 | 指定用于分配预测的期间分配参数。 有关详细信息，请参阅[预算计划数据分配](../../finance/budgeting/budget-planning-data-allocation.md)。 |
| 结束日期 | 使用 **每** 和 **单位** 字段时，指定结束日期。 |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>需求预测页面上的物料选项卡

**物料** 选项卡显示有关当前在 **概述** 选项卡上选定的行的更多物料信息。其中一些信息与 **概述** 选项卡中重复。下表介绍了对 **物料** 选项卡唯一的字段。

| 字段 | 说明 |
|---|---|
| 计价单位 | 销售价格适用的销售单位数。 值自动从物料表中检索，但您可以修改它。 |
| 销售费用 | 销售价的固定费用。 该费用与数量无关。 |
| 成本价 | 当前预测交易记录的成本（按库存单位计算）。 值从物料表中检索，但您可以修改它。 |
| 折扣率 | 用百分比表示的折扣。 |
| 折扣金额 | 用每个销售单位的金额表示的折扣。 |
| 总额 | 未应用折扣时的金额。 |
| 库存数量 | 用物料的库存单位表示的交易数量。 |
| 使用特定物料清单 | 特定物料清单的物料清单编号。 |
| 使用特定工艺路线 | 特定的下级工艺路线的工艺路线编号。 |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>需求预测页面上的项目选项卡

**项目** 选项卡显示有关当前在 **概述** 选项卡上选定的行的更多项目信息。其中一些信息与 **概述**、**常规** 或 **物料** 选项卡中重复。下表介绍了对 **项目** 选项卡唯一的字段。

| 字段 | 说明 |
|---|---|
| 项目日期 | 需求预测交易的日期。 |
| 项目 ID | 当前交易引用的项目的标识符。 |
| 融资来源 | 需求预测所关联的融资来源。 |
| 活动编号 | 与需求预测交易关联的活动。 |
| 类别 | 当前交易的成本类别。 |
| 行属性 | 交易记录所关联的状态。 |
| 交易记录 ID | 需求预测交易的系统标识符。 |
| 成本额 | 需求预测交易的金额。 |
| 单位价格 | 单价。 |
| 修改者 | 最后修改选定交易的工作人员的标识符。 |
| 账单日期 | 输入预期发票日期。 |
| 取消日期 | 查看或修改取消日期。 创建预测时，将取消日期设置为项目的结束日期。 如果项目没有结束日期，将采用项目日期。 此字段适用于固定价格项目和投资项目。 |
| 成本付款日期 | 输入采购付款的预期日期。 |
| 销售付款日期 | 输入销售付款的预期日期。 |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>需求预测页面上的财务维度选项卡

**财务维度** 选项卡显示当前在 **概述** 选项卡上选定的行的所有财务维度值。

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>需求预测页面上的库存维度选项卡

**库存维度** 选项卡显示当前在 **概述** 选项卡上选定的行的所有库存维度值。

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>需求预测页面上的分配网格

如果您使用的是物料分配参数，或者如果您已针对一个或多个未来期间输入物料预测，可以通过在 **概述** 选项卡的工具栏上选择 **分配预测** 来分配预测。然后，按照 **分配** 网格中的行指示的方式分发数量。 （请参阅本文后面的[分配预测](#allocate-forecast)一节。）

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>库存预测

供应和需求预测行页面具有 **库存预测** 按钮，用于打开为相同物料/模型组合筛选的 **库存预测** 的视图。 库存预测表示为同一物料输入的供应和需求之间的平衡。 不可编辑。 库存预测可帮助库存管理团队审查在已预测的即将到来的期间内物料现有库存的预期变化。

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>库存预测页面上的操作窗格

下表介绍了 **库存预测** 页面的操作窗格上可用的命令。

| 变动 | 说明 |
|---|---|
| 供应预测 | 打开为相同料/模型/日期组合筛选的 **供应预测** 页面的视图。 |
| 需求预测 | 打开为相同物料/模型/日期组合筛选的 **供应预测** 页面的视图。 |
| 库存 \> 显示维度 | 选择应显示在 **概述** 网格中的产品、存储和跟踪维度。 |

### <a name="the-grid-on-the-inventory-forecast-page"></a>库存预测页面上的网格

下表介绍了 **库存预测** 页面上的网格中的字段。

| 字段 | 说明 |
|---|---|
| **型号** | 交易所关联的预测模型。 |
| **物料编号** | 物料的标识符。 |
| **预算日期** | 预测交易的日期。 |
| **预测类型** | 交易来源（*需求预测* 或 *供应预测*）。 |
| **CW 数量** | 采用实际称重单位的预测数量。 |
| **数量** | 采用库存单位的预测数量。 |
| **CW 累计** | 当为相同物料累积多个预测行时，采用实际称重单位的累积预测数量。 |
| **下级物料清单** | 特定的下级物料清单的物料清单编号。 |
| **下级运输路线** | 特定的下级工艺路线的工艺路线编号。 |
| （其他维度） | 其他维度可以在网格中显示为列。 若要选择显示的其他维度，请在操作窗格上选择 **库存 \> 显示维度**。 |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>分配预测

使用以下过程处理所选预测交易记录行。 在分配预测时，将按照 **分配** 网格中的行的指示分配数量。

1. 根据您要为其创建预测的实体类型以及您要创建的预测类型，按照[查看和手动输入预测行](#manual-entry)中的说明打开供应或需求预测页面。
1. 在供应或需求预测行页面上，选择预测行，然后在 **概览** 选项卡上选择工具栏上的 **分配预测**。
1. 在 **分配预测** 对话框中，设置下表中描述的字段。 （您在 **方法** 字段中选择的值决定其他可用字段。）

    | 字段 | 说明 |
    |---|---|
    | 方法 | <p>选择用于分配预测交易的方法：</p><ul><li>**无** – 不进行分配。</li><li>**期间** – 预测每个期间的相同数量。 如果选择此值，在 **每** 字段中指定数量并在 **单位** 字段中指定时间单位。</li><li>**参数** – 根据在 **期间参数** 字段中指定的期间分配参数分配预测。 要考虑季节性变动时可以使用此方法。</li><ul>|
    | 每 | <p>输入预测向前延长的时间间隔数。 此字段仅在 **方法** 字段中选择 *期间* 时才可用。</p><p>例如，在 **方法** 字段中选择 *期间*，在 **每** 字段中输入 *1*，在 **单位** 字段中选择 *月*。 然后在 **结束** 字段中，指定向前延伸一年的结束日期。 在此情况下，基于在标头行中指定的物料和数量为明年的每个月创建一个预测行。 |
    | 单位 | 选择时间间隔的单位：*天*、*月* 或 *年*。 然后，分配对应于您在 **每** 字段中指定的天数、月数或年数。|
    | 期间参数 | 指定用于分配预测的期间分配参数。 有关详细信息，请参阅[预算计划数据分配](../../finance/budgeting/budget-planning-data-allocation.md)。 |
    | 结束日期 | 指定应用于 **按** 和 **单位** 字段中的设置的结束日期。 |

1. 选择 **确定** 确认您的设置。
1. 您可以在 **分配** 选项卡上查看同一行的结果。

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>批量更新预测交易

使用此过程处理现有的预测交易行。 您可以复制、编辑和删除预测交易行。

1. 在供应或需求预测行页面上，选择 **批量更新**。
1. 在对话框中，选择 **筛选器**。
1. 在 **范围** 选项卡上，选择标识您要复制、编辑或删除的来源预测数据的条件。 此数据可能包括预测模型、物料编号和客户帐户。
1. 选择 **确定** 确认您的选择。

    选择数据后，您可以使用 **编辑预测交易** 对话框定义您想要如何复制、编辑或删除它。

    > [!NOTE]
    > 在使用 **批量编辑** 功能之前，必须执行筛选步骤。 如果跳过它，程序会选择并更新 **所有** 预测行。 因此，您可能会无意中导致重复或删除交易。

1. 在 **管理** 部分中，选择是否要复制、更新或删除选定的预测交易。
1. 使用 **字段中的修改** 部分更改预测的参数。 选中参数的复选框，然后在可用选项中进行选择。 例如，选中 **模型** 复选框，然后选择预测模型编号。 现有预测行将复制到选定预测模型。
1. 使用 **期间的更改** 部分以向前或向后移动预测的开始和结束日期。 选中该复选框，然后使用数量和期间字段以定义应如何移动预测日期。 您可以输入一个负数来向前移动开始日期（即，使日期提前）。

    例如，若要将预测交易开始日期延迟六个月，请选中该复选框，输入 *6* 作为数量，然后选择 *月* 作为期间。

1. 使用 **更正字段** 部分更新实际预测数据。 在 **字段** 字段中，选择您要更改的条件。 在 **系数** 字段中，输入应用于选定条件的乘法系数，或者输入一个要增加或减去的常数。 例如，选择 *数量* 作为条件，然后输入 *1.5* 的系数以将物料数量乘以 1.5。 或者，输入常数 *-25*，以将物料数量减去 25 个单位。
1. 使用 **财务维度** 部分以更新预测行的财务维度。 选择要更改的财务维度，然后输入要应用于选定维度的值。
1. 选择 **确定** 以应用更改。

## <a name="use-forecasts-with-master-planning"></a>将预测用于主计划

在输入需求预测和/或供应预测后，您可以在主计划期间包括这些预测，以在主计划运行时考虑预期的需求和/或供应。 当主计划中包括这些预测时，将计算物料和产能的总需求，并生成计划订单。

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>设置主计划以包括库存预测

若要设置主计划以使其包括库存预测，请按照以下步骤操作。

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 选择一个现有计划，或创建新计划。
1. 在 **常规** 快速选项卡上，设置以下字段：

    - **预测模型** – 选择要应用的预测模型。 当为当前主计划生成供应建议时，将考虑该模型。
    - **包括供应预测** – 将此选项设置为 *是* 以在当前主计划中包括供应预测。 如果将其设置为 *否*，供应预测交易将不包括在主计划中。
    - **包括需求预测** – 将此选项设置为 *是* 以在当前主计划中包括需求预测。 如果设置为 *否*，需求预测交易将不包含在主计划中。
    - **用于减少预测需求的方法** – 选择应用于减少预测需求的方法。 有关详细信息，请参阅[预测缩减参数](planning-optimization/demand-forecast.md#reduction-keys)。

1. 在 **按天计算的时限** 快速选项卡上，您可以设置以下字段来指定包括预测的期间：

    - **预测计划** – 将此选项设置为 *是* 以替代源自各个覆盖范围组的预测计划时限。 设置为 *否* 以使用来自当前主计划的各个覆盖范围组中的值。
    - **预测时段** – 如果您将 **预测计划** 选项设置为 *是*，请指定应该应用需求预测的天数（从今天开始）。

    > [!IMPORTANT]
    > 计划优化不支持 **预测计划** 选项。

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>运行包括库存预测的主计划

若要运行包括库存预测的主计划，请按照以下步骤操作。

1. 转到 **主计划 \> 工作区 \> 主计划**。
1. 在 **主计划** 字段中，输入或选择您在上一过程中设置的主计划。
1. 在 **主计划** 磁贴上，选择 **运行**。
1. 在 **主计划** 对话框中，将 **跟踪处理时间** 选项设置为 *是*。
1. 在 **线程数** 字段中，输入一个数字。
1. 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 将显示标准查询编辑器对话框。 在 **范围** 选项卡上，选择 **字段** 字段设置为 *物料编号* 的行。
1. 在 **条件** 字段中，选择要包括在计划中的物料编号。
1. 选择 **确定**。

若要查看计算的需求，请打开 **总需求** 页面。 例如，在 **发布产品** 页面上的操作窗格上，在 **计划** 选项卡上的 **需求** 组中，选择 **总需求**。

若要查看生成的计划订单，请转到 **主计划 \> 常见 \> 计划订单**，然后选择适当的预测计划。

## <a name="additional-resources"></a>其他资源

- [需求预测概览](introduction-demand-forecasting.md)
- [需求预测设置](demand-forecasting-setup.md)
- [生成统计基准预测](generate-statistical-baseline-forecast.md)
- [对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)
- [具有需求预测的主计划](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]