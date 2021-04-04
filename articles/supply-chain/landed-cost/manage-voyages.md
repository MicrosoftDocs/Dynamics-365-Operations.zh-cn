---
title: 管理航行
description: 本主题介绍如何使用航行。 航行通常代表船只。 但是，根据您的实践和过程，它可以代表供应商、采购订单或其他对您的组织有意义的项目。
author: sherry-zheng
manager: tfehr
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 850fbb2077a592ec4ba8578cab4795d573464f54
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500998"
---
# <a name="manage-voyages"></a>管理航行

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

航行通常代表船只。 但是，根据您的实践和过程，它可以代表供应商、采购订单或其他对您的组织有意义的项目。

**所有航行** 页提供航行详细信息、交货和成本计算信息，以及有关物料、采购订单和转移单的信息。 要打开 **所有航行** 页，转到 **登陆成本 \> 航行 \> 所有航行**。 此页面显示所有当前航行的列表。 您可以使用操作窗格上的按钮创建、删除和使用航行。 在列表中选择任意航行查看它的详细信息。

> [!NOTE]
> 装运集装箱和帐页将链接到航行。 采购订单行将链接到装运集装箱。 如果装运集装箱和帐页关闭，它们也可以直接链接到航行。 此外，在此处输入的成本将分摊到所有附加的采购订单行。

## <a name="action-pane"></a>操作窗格

**航行** 页的操作窗格提供让您可以使用选定航行的按钮。 每个按钮执行一个操作。 操作窗格还包含选项卡，每个选项卡又提供一组相关按钮。 除非另有说明，否则在 **所有航行** 页的列表视图和单个所选航行的详细视图中均提供所有按钮和选项卡。

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>直接显示在操作窗格上的按钮

下表描述了直接操作窗格上提供的按钮。

| 按钮 | 说明 |
|---|---|
| 新项 | 创建航行。 <!-- KFM: Link to scenario --> |
| Delete | 删除当前航行。 只能删除航行状态为 *已确认* 的航行。 航行离开港口并处理在途货物后，将无法再将其删除。 |
| 航行编辑器 | 打开 **航行编辑器** 页，您可以在其中添加或删除航行的采购订单行、创建新集装箱，以及修改航行本身的详细信息。 |
| 航行成本 | 打开 **航行成本** 页，您可以在其中查看航行成本并将其添加到航行中的所有货物。 将航行成本手动添加到航行后，它们会自动添加到 **成本查询** 页，并根据 **航行成本** 页指定的方法分摊到每个货物。 |

### <a name="buttons-on-the-voyage-tab"></a>航行选项卡上的按钮

下表描述了操作窗格的 **航行** 选项卡上的可用按钮。 仅当您在 **所有航行** 页的列表视图中工作时，此选项卡才可用。

| 按钮 | 说明 |
|---|---|
| 装运集装箱 | 打开一个页面，显示与所选航行关联的所有装运集装箱。 可能有一个集装箱或很多集装箱。 |
| 帐页 | 打开一个页面，显示与所选航行关联的所有帐页。 可能有一个帐页或很多帐页。 |

### <a name="buttons-on-the-manage-tab"></a>“管理”选项卡上的按钮

下表描述了操作窗格的 **管理** 选项卡上的可用操作。

| 按钮 | 说明 |
|---|---|
| 已收到单据 | 更新航行，让 **已收到单据** 选项设置为 *是*。 您可以使用此按钮锁定物料和/或采购行，使其无法进一步更新。 |
| 在途 | 将 **航行状态** 字段更新为在 **[登陆成本参数](landed-cost-parameters.md)** 页建立的在途状态。 此流程没有其他逻辑。 根据[跟踪控制中心](delivery-information-setup.md)中的设置，航行也可以自动更新为在途状态。
| 成本计算就绪 | 将 **航行状态** 字段更新为在 **[登陆成本参数](landed-cost-parameters.md)** 页建立的成本计算就绪状态。 处理所有发票（存货发票和航行成本发票）和接收货物后，可以计算航行的成本。 如果尚未计算与航行关联的估计成本，当您尝试处理航行的成本计算时会发生错误。 |
| 已计算成本 | 在所有采购订单和航行成本均存在发票后，清理所有成本计算违规行为。 选择此按钮时，**航行更新 - 已计算成本** 对话框将出现。 在那里，您可以选择在标准财务日期过帐或指定过帐日期，然后运行操作。 您可以根据需要多次重新运行操作。 您还可以使用 **航行更新 - 已计算成本** 对话框建立计划来将操作作为定期任务（批处理作业）运行。 我们建议您通过将操作设置为批处理作业来定期运行操作。 |
| 将收货清单过帐 | 为航行中的所有采购订单行过帐收货清单。 如果使用多公司航行，将为每个公司打开一个新的收货清单过帐对话框，并且必须在每个法人中对其进行处理。 |
| 将物料收货过帐 | 为航行中的所有采购订单行过帐产品收货。 仅当货物 **不** 经过在途货物处理时，才使用与航行关联的采购订单行的产品收货流程。 如果货物将经过在途货物处理，当您尝试过帐采购订单行的产品收货时会收到错误。 如果使用多公司航行，将为每个公司打开一个新的交货通知过帐对话框。 |
| 将账单过帐 | 为航行中的所有采购订单行过帐发票。 如果航行中的货物将经过在途货物处理，将在完成接收流程之前对采购订单行开票。 对原始采购订单开票时，将创建与原始采购订单行关联的在途货物订单。 这些订单然后可以由仓库接收。 如果使用多公司装运，将为每个公司打开一个新的发票过帐对话框。 |
| 装运转移单 | 为航行中的所有转移单行过帐转移单航行。 选择此按钮后，仅转移单可以更新。 |
| 接收转移单 | 为航行中的所有转移单行过帐转移单接收。 |
| 接收在途货物 | 接收航行中正在运输中的所有订单行。 此按钮是可用于接收航行中的在途货物的货物的三个选项之一。 （其他两个选项是此表后面说明的 **创建到达日记帐** 按钮和仓库应用。）此选项是最简单的选项，它将处理从在途货物仓库移出、进入最终目标仓库的在途货物。 如果您想对流程进行更多控制，请使用到达日记帐或移动设备处理货物收货。 |
| 查找自动成本 | 查找所有相关的航行成本。 如果已经找到或更新了这些成本，您将收到以下消息：“存在未开票成本行。 是否要覆盖它们？” 将找到创建时未与航行关联的所有成本。 附加到航行且已开票的航行成本不会被覆盖。 |
| 创建到达日记帐 | <p>打开 **创建到达日记帐** 对话框，您可以在其中创建指定位置的到达日记帐。 此对话框提供以下选项：</p><ul><li>**从在途货物创建** 或 **从转移单创建** – 此选项的标签会根据您是否正在使用在途货物流程而变化。 将其设置为 *是* 打开到达日记帐页面，该页面可让您处理与航行关联的在途货物的标准到达日记帐。 如果已在最终目标仓库中接收物料，不会将其添加到到达日记帐行中。</li><li>**初始化数量** – 将此选项设置为 *是* 将根据航行行上指定的货物数量初始化将要接收的数量。 如果已部分接收航行行，此数量将为剩余数量。 我们建议您将此选项设置为 *是*。</li><li>**从订单行创建** – 将此选项设置为 *是* 将从订单行获取值。</li></ul><p>此按钮是可用于接收航行中的货物的三个选项之一。 （其他选项是此表前面说明的 **接收在途货物** 按钮和仓库应用。）</p> |
| 应计成本 | 您可以在成本类型具有为借方指定的会计科目时应计成本。 此按钮通常在存货在运输途中或货物已接收和开票时使用。 |
| 合计成本 | 将成本从装运集装箱级别移到航行级别。 您可以在共享服务/装运场景中使用此按钮，在这种情况下，多个实体共享一个装运集装箱或纸箱空间。 例如，航行有一个 40 英尺长的装运集装箱和一个 20 英尺长的装运集装箱，分摊按体积进行。 在这种情况下，可能会对共享或使用 20 英尺集装箱中空间的货物/实体不利。 为了公平地分配成本，有些组织可能希望将成本转移到航行中，然后根据航行级分摊方法进行分配。 |
| 更改行程模板 | 打开一个对话框，您可以在其中更改行程模板。 更改模板后，航行成本将被删除。 因此，您可能必须选择 **查找成本费用**（请参阅此表前面的描述）或再次手动添加成本。 |

### <a name="buttons-on-the-general-tab"></a>“常规”选项卡上的按钮

下表描述了操作窗格的 **常规** 选项卡上的可用按钮。

| 按钮 | 说明 |
|---|---|
| 收货清单 | 打开航行中所有采购订单行的产品收货清单。 如果使用多公司航行，将为每个公司打开一个新的收货清单。 如果未处理产品收货清单，此按钮将不可用。 |
| 产品收据 | 打开与航行关联的采购订单行的产品收货记录（如果使用了该记录）。 如果未过帐产品收货，此按钮将不可用。 如果您使用的是在途货物处理，则不会使用产品收货流程。 |
| 物料到达 | 打开物料到达日记帐（如果已使用）。 |
| 跟踪 | 打开 **入站跟踪** 页，您可以在其中更新装运集装箱和航行中货物的预期到达日期，随后可以更新采购订单行的预期交货日期。 |
| 成本查询 | <p>打开 **成本查询** 页，其中显示航行的所有成本。</p><p>在操作窗格中选择 **视图** 调整视图。 您可以查看任何级别，以及物料和成本类型代码。</p><p>只有与库存交易直接相关的成本类型代码会显示在 **成本查询** 页上。 通过删除成本类型代码，您可以通过将成本分组在一起来调整此页面。 如果您使用尺寸和颜色，此功能可能会很有用。</p><p>**成本查询** 页仅显示将 **借记** 字段设置为 *物料* 的成本类型代码。</p> |
| 在途货物订单 | 打开 **在途货物订单** 页，该页面仅显示选定航行的在途货物记录。 |

## <a name="lines-view"></a>行视图

要打开 **行** 视图，打开一个航行，然后在航行标题的右上角选择 **行** 选项卡。

### <a name="information-on-the-voyage-header-fasttab"></a>航行标头快速选项卡上的信息

航行的 **行** 视图中的 **航行标头** 快速选项卡包含描述航行的基本信息。 出现在此快速选项卡上的很多字段也会出现在 **标头** 视图中，如本主题后面所述。

### <a name="information-on-the-voyage-lines-fasttab"></a>航行行快速选项卡上的信息

航行的 **行** 视图中的 **航行行** 快速选项卡与在航行级应用的航行详细信息和成本计算信息相关。 在这里，您可以查看附加到航行的装运集装箱、帐页和物料。 另外还显示航行中物料的价格和数量。 您可以通过选择相关链接来查看列出的任何装运集装箱或帐页。

### <a name="information-on-the-line-details-fasttab"></a>行详细信息快速选项卡上的信息

航行的 **行** 视图中的 **行详细信息** 快速选项卡提供有关当前在 **航行行** 快速选项卡上选择的行的更多信息。 请注意，此快速选项卡包含有关每个行在集装箱中的位置以及它的声明数量的详细信息。

## <a name="header-view"></a>标头视图

要打开 **标头** 视图，打开一个航行，然后在航行标题的右上角选择 **标头** 选项卡。

### <a name="settings-on-the-general-fasttab"></a>常规快速选项卡上的设置

下表描述了航行的 **标头** 视图中的 **常规** 快速选项卡上可用的字段。

| 字段 | 说明 |
|---|---|
| 航行 | 输入航行或航班号。 |
| 记帐引用 | 如果您的发货人或装运中心提供了参考号来标识航行（即发货人或装运中心的内部参考），请在此处输入。 |
| 船舶 | 输入或选择船只。 如果船只未作为值列出，可以作为自由文本输入船只 ID。 在这种情况下，主表不会更新，以可以在以后在此字段中选择船只 ID。 |
| 外部航行 ID | 输入航行的公共 ID（如航班号）。 |
| 主航空运单/提单 | 输入主航空运单或提单编号。 在进行空运装运时可以指定此值。 |
| 内部航空运单/提单 | 为装运集装箱指定内部航空运单或提单。 |
| 租赁 | 选中此复选框以指示集装箱是必须退还的租赁集装箱。 |
| 说明 | 输入航行的描述，以使其更易于识别。 |
| 航行状态 | 航行的状态。 值包括 *已创建*、*在途*、*已收到单据* 和 *已计算成本*。 此字段不基于逻辑计算。 它仅通过过帐操作更新。 *已计算成本* 值指示已收到存货和所有航行成本的发票。 除非收到发票，否则航行无法到达 *已计算成本* 状态。 |
| 采购订单状态 | 与航行关联的所有采购订单中已到达的最高状态。 |
| 已收到单据 | 一个值，指示您的公司是否已收到与航行关联的所有单据。 要更改此值，在操作窗格的 **管理** 选项卡上的 **航行更新** 组中选择 **已收到单据**。 |
| 装运公司 | 选择此航行的装运公司。 此字段可用于确定自动成本。 |
| 姓名 | 在 **装运公司** 字段中选择的公司的名称。 |
| 量化指标 | 此字段支持在自动成本中指定度量。 不知道商品单个体积或重量，但需要比金额或数量提供的更准确分摊的组织经常使用度量。 货运转运商将提供重量或体积度量，您可以将其放在物料或采购订单级别。 如果选择了参数，它可以自动更新，也可以手动输入。 |
| 度量单位 | 将应用于 **度量** 字段中的数字的度量单位。 |
| 托盘数 | 在航行行上指定托盘数量。 如果在 **登陆成本参数** 页的 **常规** 选项卡上将 **自动更新纸箱数量** 选项设置为 *是*，此字段将自动更新。 |

### <a name="settings-on-the-delivery-fasttab"></a>交货快速选项卡上的设置

下表描述了航行的 **标头** 视图中的 **交货** 快速选项卡上的可用字段。

| 字段 | 说明 |
|---|---|
| 创建日期和时间 | 创建航行记录的日期和时间。 |
| 出厂日期 | 此字段在链接到航行的采购订单中选择最早的出厂日期。 出厂日期可在采购订单头上找到，使用跟踪控制功能进行更新。 |
| 装运日期 | 飞机或船只离开起始点的估计日期。 |
| 出发日期 | 出发日期通常是飞机或船只实际离开海外港口的日期。 装运日期和出发日期不必匹配。 **出发日期** 字段仅提供信息。 不用于估计预期交货日期。 跟踪控制功能用于估计预期交货日期，可以将此字段设置为由跟踪控制功能自动填充。 |
| 到店日期 | 此字段将选择链接到航行的采购订单中的货物可供销售的最早日期。 |
| 预计交货日期 | 估计交货日期通常是货物应到达仓库的日期。 此字段仅供参考。 它不用于货物的主计划。 采购订单行上的预期交货日期用于航行中货物的主计划，使用跟踪控制功能进行更新。 可以设置此字段，让它由跟踪控制功能填充。 |
| 实际交货日期 | 最早的交货日期，基于链接到航行的货物。 |
| 装运港口 ETA | 根据装运代理提供的信息，输入您期望航行到达装运港口的日期。 |
| 已收到原始单据 | 输入收到原始单据的日期。 |
| 已建议代理 | 输入通知代理的日期。 |
| 已发送原始提单 | 输入发送原始提单的日期。 |
| 已发放货物 | 输入从海关发放货物的日期。 |
| 客户预约 | 输入客户预约日期，这是您期望客户获得货物所有权的日期。 |
| 已在仓库交货 | 输入货物交付到仓库的日期。 |
| 验证日期 | 输入验证日期。 |
| 交货说明 | 输入收到交货说明的日期。 |
| 交货模式 | 此字段提供用于交付航行的方法，以及与该交货方法关联的自动成本的成本选择的信息。 |
| 发运港口 | 航行出发的装运港口。 |
| 目标港口 | 航行到达的装运港口。 装运集装箱可能有不同的港口，因为船可能会在多个港口停留。 通过在装运集装箱级别验证“到达”港口，您为航行中的每个装运集装箱提供准确的港口详细信息。 与货运关联的自动成本基于装运集装箱类型、“到达”港口和“发运”港口的组合确定。 |
| 本地转运商 | 此字段仅供参考。 当地转运商应该可以从供应商表中选择。 |
| 本地运输日期 | 预订使用当地运输的日期。 此字段可以帮助仓库进行计划。 |
| 本地运输时间 | 预订使用当地运输的时隙。 此字段可以帮助仓库进行计划。 |
| 行程模板 | 为航行指定的行程模板。 行程模板用于输入装运集装箱和航行的“到达”港口和“发运”港口。 这些值进而帮助确定与航行关联的自动成本。 |

### <a name="settings-on-the-other-fasttab"></a>其他快速选项卡上的设置

下表描述了航行的 **标头** 视图中的 **其他** 快速选项卡上的可用字段。

| 字段 | 说明 |
|---|---|
| 注解 | 输入与航行相关的其他信息。 |
| 估价日期 | 选择链接到航行的采购订单的最早出厂日期。 |
| 待定航行 | 您可以使用此选项指示您的货物或航行是否已经离开。 它仅用于提供信息。  |
| 重命名装运集装箱 | 对于具有多个集装箱的航行，为尚未收到的集装箱数量。 |

## <a name="voyage-update-periodic-tasks"></a>航行更新定期任务

**登陆成本** 模块包括几个与航行相关的定期任务，这些任务可以批量更新航行的多个方面。 要运行或计划这些定期任务，转到 **登陆成本 \> 定期任务 \> 航行更新**，然后选择以下任务类型之一：

- **已收到单据** – 通过此任务，您可以同时为多个航行将 **已收到单据** 设置为 *是*。 使用 **筛选器** 设置定义要更新的航行集。
- **在途** – 通过此任务，您可以同时为多个航行将 **航行状态** 字段设置为在 **[登陆成本参数](landed-cost-parameters.md)** 页上建立的在途状态。 使用 **筛选器** 设置定义要更新的航行集。
- **成本计算就绪** – 通过此任务，您可以同时为多个航行将 **航行状态** 字段设置为在 **[登陆成本参数](landed-cost-parameters.md)** 页上建立的成本计算就绪状态。 通常，您会将此任务设置为按定期计划运行。
- **已计算成本** – 通过此任务，您可以同时为多个航行将 **航行状态** 字段设置为在 **[登陆成本参数](landed-cost-parameters.md)** 页上建立的已计算成本状态，前提是它们已计算成本但尚未在航行中更新。 通常，您会将此任务设置为按定期计划运行。