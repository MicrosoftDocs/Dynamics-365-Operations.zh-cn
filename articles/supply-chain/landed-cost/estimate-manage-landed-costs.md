---
title: 估计和管理登陆成本
description: 系统使用您的自动成本设置来确定您的登陆成本的估计。 本文说明如何定义各个方案以提供更准确的估计。
author: Weijiesa
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2e7cdd7c7439a24ec75a59bcee1e8f42f37bb2cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854432"
---
# <a name="estimate-and-manage-landed-costs"></a>估计和管理登陆成本

[!include [banner](../../includes/banner.md)]

系统使用您的[自动成本设置](auto-cost-setup.md)来确定您的登陆成本的估计。 此外，您可以定义各个方案以提供更准确的估计。 这些方案将被存储。 因此，您可以在以后查看，将其与报表中的实际值进行比较。 您还可以更新物料价格。

## <a name="set-up-cost-estimates"></a>设置成本估计

### <a name="set-up-cost-templates"></a>设置成本模板

成本模板建立获取估计的用户不一定会知道的默认设置。 模板可以通过最小化用户为获取准确的估计而必须指定的选择来帮助降低估计流程的复杂性。 如果您使用的是标准成本模型，可以在设置商品成本时使用成本模板。

要设置成本模板，请转到 **登陆成本 \> 成本计算设置 \> 成本模板**。 在 **成本模板** 页上，左侧的列表窗格将显示所有当前成本模板。 您可以使用操作窗格上的按钮创建、删除和编辑模板。

下表说明了可用于每个模板的字段。

| 字段 | 说明 |
|---|---|
| 成本模板 | 为成本模板输入唯一名称。 此名称通常描述模板的系数或成本倍数。 |
| 说明 | 输入成本模板的描述。 |
| 装运公司 | 选择使用模板时应该应用的装运公司。 |
| 交货模式 | 选择使用模板时应该应用的交货方式，如海运或空运。 此字段帮助确定成本估计中与商品关联的自动成本。 |
| 装运集装箱类型 | 选择使用模板时应该应用的装运集装箱类型。 此字段帮助确定成本估计中与商品关联的自动成本。 |
| 关税代理 | 选择使用模板时应该应用的关税代理（供应商）。 此字段帮助确定与成本估计关联的自动成本。 |
| 系数 | 输入使用模板时应该自动应用于成本估计的乘数（百分比）。 例如，要在计算出的成本估计中增加 10%，输入 *1.10*。 |

### <a name="create-a-cost-estimate"></a>创建成本估计

使用 **成本估计** 对话框生成新的基于所选成本模板、一组选定的物料以及行程其他详细信息的成本估计。 然后将这些设置用于确定估计的货物登陆成本。 这些成本估计主要用于处理标准成本物料。 将估计的登陆成本与库存中货物的标准成本相加，在将货物添加到航行中时，差额交易应该会更小，因为标准成本将反映这些登陆成本的估计。

要打开 **成本估计** 对话框，转到 **登陆成本 \> 定期任务 \> 成本估计**。 然后设置以下小节中所述的字段。 最后，选择 **确定** 创建估计。 **成本估计** 页（**登陆成本 \> 查询 \> 成本估计**）然后将出现，显示您的新估计，如本文后面所述。

### <a name="settings-on-the-parameters-tab"></a>参数选项卡上的设置

下表描述了 **成本估计** 对话框的 **参数** 选项卡上的可用字段。


| 字段 | 说明 |
|---|---|
| 成本模板 | 选择成本模板。 与所选模板关联的设置将用于确定所应用的自动成本。 |
| 预计日期 | 默认情况下，此字段设置为今天的日期，不过您可以更改此值。 如果使用了装运费用，指定日期将用于选择适当的销售价、采购价、自动成本和汇率。 |
| 量化指标 | 成本可能取决于度量。 例如，使用空运时，可能适用容量定价。 如果成本取决于度量，应输入该度量的值。 否则，建议您将此字段设置为 *1*，除非您确定使用度量不会发生分摊。 输入十进制值。 此单位是适用的自动成本记录中定义的单位。 |
| 行程模板 | 选择[行程模板](multi-leg-journey-setup.md)。 此字段用于确定应该应用的正确自动成本。 |
| 发运港口 | 发运物料的港口。 此字段根据所选行程模板设置。 |
| 目标港口 | 物料将送达的港口。 此字段根据所选行程模板设置。 |
| 货币 | 选择购买物料使用的货币。 |
| 集装箱 | 如果通常使用多个集装箱，应指定集装箱的数量。 然后，系统在估计成本时将使用多个集装箱的成本。 |
| 帐页 | 如果通常使用多个帐页，应指定数量。 （此数量通常为 *1*。） |
| 站点 | 指定货物交货的站点。 |

### <a name="settings-on-the-items-tab"></a>物料选项卡上的设置

在 **物料** 选项卡上，您可以根据需要向估计添加任意数量的物料。 使用工具栏将物料添加到网格中或删除物料。 在工具栏上选择 **库存 \> 显示维度** 打开一个对话框，您可以在其中向网格添加维度列或删除列。

下表说明了可用于每个物料的字段。

| 字段 | 说明 |
|---|---|
| 物料编号 | 选择要确定其价格的物料。 （如果系统中尚不存在该物料，创建一个虚拟物料，可以选择将其附加到航行物料成本组，然后将价格留空，或者创建或更改价格。） |
| 供应商帐户 | 选择要用于此物料的估计的供应商。 如果为物料分配了默认供应商，此字段会自动设置。 |
| 数量 | 选择要购买的数量。 |
| 成本价 | 系统使用其定价规则来查找初始价格，但如有必要，您可以替代该价格。 |
| 销售价 | 输入商品的预期销售价。 |
| 量化指标 | 为商品度量输入一个十进制值。 单位是为适用的已发布产品设置的单位。 |
| 更新物料重量/体积 | 选中此复选框可更新已发布产品的重量或体积度量，使其与为此行输入的 **度量** 值匹配。 |
| （其他维度） | 根据您选择显示的维度，您可能会看到有关每个物料的其他信息列。 |

要查看或调整物料的体积和/或重量详细信息，在网格中选择物料，然后使用页面底部的字段。

## <a name="manage-estimated-costs"></a>管理估计成本

要查看和编辑您创建的成本估计，转到 **登陆成本 \> 查询 \> 成本估计**。 在 **成本估计** 页上，左侧的列表窗格将显示所有当前的成本估计。 您可以使用操作窗格上的按钮处理选定的估计。 请注意，您无法从 **成本估计** 页创建新的成本估计。 而应使用 **成本估计** 对话框（**登陆成本 \> 定期任务 \> 成本估计**），如本文前面所述。

**成本估计** 页显示每个估计成本的派生方式。 另外还显示每个物料的估计登陆成本。 您可以通过更改与各个商品关联的成本价和/或货币来修改成本估计。 您还可以在航行级别和集装箱级别同时修改关联的航行成本。 使用此页面修改成本时，系统会提示您重新计算成本估计中物料的估计成本。 准备就绪后，可以使用估计来更新成本模板中物料的成本价。

### <a name="information-on-the-header"></a>标头上的信息

**成本估计** 页的顶部显示用于生成所选成本估计的设置，如上一节所述。 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>行快速选项卡上的设置和按钮

**行** 快速选项卡列出当前估计中包括的每个物料。 下表说明了可用于每个行的字段。

| 字段 | 说明 |
|---|---|
| 供应商帐户 | 与物料关联的供应商帐户。 |
| 物料编号 | 物料编号。 |
| 数量 | 用于确定成本的物料数量。 |
| 成本价 | 根据贸易协议确定的成本价。 此值以本币显示。 |
| 量化指标 | 单个度量。 单位是为适用的已发布产品定义的单位。 |
| 预计登岸成本 | 总数量的估计登陆成本。 |
| 每单位 | 估计登陆成本除以数量。 |
| （其他维度） | 根据您选择显示的维度，您可能会看到有关每个物料的其他信息列。 |

下表描述了 **行** 快速选项卡上工具栏上的可用按钮。

| 按钮 | 说明 |
|---|---|
| 添加 | 将物料添加到成本估计中。 添加物料后，必须在操作窗格上选择 **重新计算**。 |
| 移动 | 从成本估计中删除物料。 删除物料后，必须在操作窗格上选择 **重新计算**。 |
| 航行成本 | 打开一个页面，您可以在其中查看和编辑物料的各个航行成本类型。 |
| 库存 \> 显示维度 | 打开一个对话框，您可以在其中将维度列添加到网格中或删除列。 |

### <a name="settings-on-the-general-fasttab"></a>常规快速选项卡上的设置

**常规** 快速选项卡显示有关当前在 **行** 快速选项卡上选择的物料的详细信息。 此信息很多是来自 **行** 快速选项卡，可以在这两个位置进行编辑。 不过，此处还提供其他详细信息。 额外字段的值基于适用的已发布产品的设置。

### <a name="settings-on-the-dimension-fasttab"></a>维度快速选项卡上的设置

**维度** 快速选项卡显示在 **行** 快速选项卡上选择的物料的所有可用库存维度的值，无论您选择在那里显示哪些维度。 此处显示的任何值均来自适用的成本估计模板。 它们在成本估计模板中是可选的。

### <a name="buttons-on-the-action-pane"></a>操作窗格上的按钮

您可以使用 **成本估计** 页上操作窗格上的按钮来处理选定的成本估计。 下表描述了可用按钮。

| 行为 | 说明 |
|---|---|
| 成本查询 | 查看航行的所有成本。 您可以根据需要在单个物料级别查看成本。 |
| 更新标准成本 | <p>使用在 **登陆成本参数** 页上定义的默认成本计算版本更新标准成本。 您可以替代此版本。</p><p>**注意：** 如果物料有多个物料维度（例如，不同尺寸、颜色和配置），但是还没有为估计选择这些维度，系统将为每个组合创建未决价格。</p><p>**重要信息：** 价格明细将创建，用于确定每个登陆成本的标准成本差额。</p> |
| 航行成本 | 查看和编辑装运中所有货物的航行成本。 |
| 重新计算 | 在更新、添加或删除航行成本后，更新估计的登陆成本。 |
| 锁定 | 锁定成本估计记录，以不能进行其他更改。 |

## <a name="item-cost-price-update"></a>物料成本价格更新

**物料成本价更新** 定期任务将更新与您在运行任务时设置的筛选器匹配的所有成本估计。 效果类似于在操作窗格上为单个估计选择 **更新标准成本** 的效果。 但是，在这种情况下，更新将应用于所有匹配的估计。

要运行此定期任务，请按照下列步骤操作。

1. 转到 **登陆成本 \> 定期任务 \> 物料成本价更新**。
1. 在 **从估计更新成本价** 对话框中，根据需要设置以下字段来限制更新范围：

    - **版本** – 仅更新使用指定成本计算版本的估计。
    - **站点** – 仅更新使用指定站点的估计。
    - **成本模板** – 仅更新使用指定模板的估计。
    - **到达港口** – 仅更新使用指定“到达”港口的估计。
    - **估计日期** – 仅更新具有指定日期的估计。

1. 与定期任务通常的设置一样设置 **要包括的记录** 和 **在后台运行** 快速选项卡上的选项。
1. 选择 **确定** 运行任务。

> [!NOTE]
> 仅当提供以下信息时，此定期任务才会成功执行：
>
> - 每个相关产品必须已经定义了 **总深度**、**总宽度** 和 **总高度**。
> - 每个相关供应商必须已经定义了 **发运港口**。
