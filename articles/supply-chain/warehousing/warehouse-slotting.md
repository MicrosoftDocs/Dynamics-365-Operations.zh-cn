---
title: 仓库时隙
description: 文主题提供有关仓库时隙的信息。 仓库时隙用于按物料和度量单位合并状态为“订购”、“预留”或“下达”的订单中的需求。 其可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料货位。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017406"
---
# <a name="warehouse-slotting"></a>仓库时隙

[!include [banner](../includes/banner.md)]

仓库时隙用于按物料和度量单位合并状态为 *订购* 、 *预留* 或 *下达* 的订单中的需求。 然后可以根据数量、单位、物理维度、固定货位等将生成的需求应用于将用于领料的货位。 建立时隙计划之后，可以创建补货工作以将相应数量的库存运到各货位。

此功能可帮助仓库经理在将订单下达到仓库并创建领料工作之前，智能计划领料货位。

## <a name="turn-on-the-warehouse-slotting-feature"></a>开启“仓库时隙”功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块** ： *仓库管理*
- **功能名称** ： *仓库时隙功能*

## <a name="set-up-warehouse-slotting"></a>设置仓库时隙功能

若要使用仓库时隙功能，必须在系统中设置以下元素。

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>为时隙创建度量单位层

可通过度量单位层将多个度量单位组合到一起来达到时隙目的。 例如，如果多个尺寸的箱子全部从同一个箱子领取区领取，则可以为所有这些尺寸创建一个层。 **必须为应该属于层的每个度量单位创建一行。**

1. 转到 **仓库管理 \> 设置 \> 补货 \> 时隙度量单位层** 。
1. 选择 **新建** 。
1. 在标题中，设置以下值：

    - **度量单位层** ： *EaBoxPl*
    - **说明** ： *每个箱托盘*

1. 选择 **保存** 。
1. 在 **度量单位** 快速选项卡上，选择 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **单位** ： *箱*
    - **说明：** 将此字段保留为空。 保存更改时，将自动填写。
    - **单位类** ： *数量*

1. 选择 **新建** 向网格添加第二行。
1. 在新行中，设置以下值：

    - **单位：** *ea*
    - **说明：** 将此字段保留为空。 保存更改时，将自动填写。
    - **单位类** ： *数量*

1. 选择 **新建** 向网格添加第三行。
1. 在新行中，设置以下值：

    - **单位** ： *PL*
    - **说明：** 将此字段保留为空。 保存更改时，将自动填写。
    - **单位类** ： *数量*

1. 选择 **保存** 以保存层。

### <a name="create-a-directive-code-for-slotting"></a>为时隙创建指令代码

必须选择应与模板关联的指令代码。

1. 转到 **库存管理 \> 设置 \> 指令代码** 。
1. 在操作窗格上，选择 **新建** 。
1. 在 **指令代码** 字段中，输入 *时隙* 。
1. 在 **指令说明** 字段中，输入 *时隙* 。

### <a name="set-up-slotting-templates"></a>设置时隙模板

各时隙模板控制如何将库存分配给特定仓库的货位。 每个时隙规范在每个模板中必须有一行。 可使用此部分中的过程设置时隙模板。

1. 转到 **仓库管理 \> 设置 \> 补货 \> 时隙模板** 。
1. 选择 **新建** 以创建模板。

接下来，必须按照下面子部分中的说明设置模板标题、时隙规范和货位指令。

#### <a name="set-up-a-slotting-template-header"></a>设置时隙模板标题

1. 在模板的标题中，设置以下值：

    - **时隙模板：**_61_
    - **说明：**_61_
    - **需求类型** ： *销售订单*

        现在， *销售订单* 是唯一支持的需求类型。

    - **需求策略：**_订购_

        此字段中提供以下值：

        - **订购** – 应该将销售订单中的所有订购数量视为需求。
        - **预留** – 仅应将预留的销售订单行数量（订购的实物）视为需求。

    - **仓库** ： _61_
    - **允许波次需求使用未预留数量：**_是_

还可以指定查询以缩小评估的需求范围。

#### <a name="set-up-slotting-specifications-for-each-template"></a>为每个模板设置时隙规范

对于创建的每个模板，执行以下步骤为每个时隙规范添加一行。

1. 在 **时隙模板详细信息** 快速选项卡上，选择 **新建** 创建一个模板行。
1. 在新行中，设置以下值：

    - **序列：** _1_
    - **说明：**_固定货位_
    - **最小数量：**_1_

        此字段定义行需要的最小需求数量。

    - **最大数量：**_1000000_

        此字段定义行的最大有效需求数量。

    - **单位** ：保持此字段为空。

        此字段定义最小数量和最大数量引用的度量单位。

    - **度量单位层：**_EaBoxPl_

        此字段定义行的有效需求度量单位。 （有关详细信息，请参阅本主题前面的[为时隙设置度量单位层](#unit-tiers)部分。）

    - **分配时隙条件：**_考虑数量_

        此字段中提供以下值：

        - **假设为空** – 该系统应假设领料区中的所有货位均为空，并且不应检查这些货位是否有库存。
        - **考虑数量** – 系统应检查领料区中的货位是否有库存，并且应该跳过所有非空货位。

    - **指令代码：**_时隙_

        此字段定义货位指令，用于查找补货工作的领料货位。

    - **溢出货位：** 将此字段保持为空。

        此字段定义如果在处理行时找不到货位，应将库存放入的货位。

    - **允许放弃：**_是_

        如果此选项设置为 *是* ，并且不能为任何需求划分时隙，将创建移动工作把库存移出有库存，但未划分时隙的货位。 然后再次运行模板。 这次将忽略货位中的库存。 如果 **分配时隙条件** 字段设置为 _考虑数量_ ，此功能效果最好。

    - **固定货位用法：**_仅限产品的固定货位_

        此字段中提供以下值：

        - **固定货位和非固定货位** – 不应将系统限制为只能使用固定货位。
        - **仅限产品的固定货位** – 系统应该将货位的时隙划分给仅限产品的固定货位。
        - **仅限产品变型的固定货位** – 系统应该将货位的时隙划分给仅限产品变型的固定货位。

1. 选择 **保存** 。
1. 选择 **新建** 创建第二个模板行。
1. 在新行中，设置以下值：

    - **序列：** _2_
    - **说明：**_其他_
    - **最小数量：**_1_
    - **最大数量：**_1000000_
    - **单位** ：保持此字段为空。
    - **度量单位层：**_EaBoxPl_
    - **分配时隙条件：**_考虑数量_
    - **指令代码：**_时隙_
    - **溢出货位：** 将此字段保持为空。
    - **允许放弃：**_是_
    - **使用固定货位：**_固定货位和非固定货位_

    在查询第二个行时，现在指定用于确定可以将该行的需求时隙划分给哪些货位。

1. 选择其中的 **序列** 字段设置为 *2* 的行。
1. 选择 **编辑查询** 。
1. 在 **范围** 选项卡中，选择 **添加** 向网格添加一行。
1. 在新行中，设置以下值：

    - **表：** *位置*
    - **派生表** ： *货位*
    - **字段：***位置模板 ID*
    - **条件** ： *Pick-06* （选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Pick-06* - *领料点 6* 。）

1. 选择 **确定** 。

#### <a name="set-up-location-directives"></a>设置货位指令

必须设置至少一个货位指令来支持时隙领料。 请按照此部分中的过程为时隙领料设置一个新的 *补货货位指令* 。

1. 转到 **库存管理 \> 设置 \> 位置指令** 。
1. 在左窗格的 **工作订单类型** 字段中，选择 *补货* 。
1. 在操作窗格上，选择 **新建** 。
1. 在新货位指令的标题中 **名称** 字段内，输入 *61 时隙领料* 。

##### <a name="configure-the-location-directives-fasttab"></a>配置“货位指令”快速选项卡

1. 在 **货位指令** 快速选项卡上，设置以下值。 接受其他所有字段的默认值。

    - **工作类型：**_领料_
    - **站点** ： _6_
    - **仓库** ： _61_
    - **指令代码** ： _时隙_

1. 选择 **保存** 激活 **行** 快速选项卡。

##### <a name="configure-the-lines-fasttab"></a>配置“行”快速选项卡

1. 在 **行** 快速选项卡上，选择 **新建** 创建一行。
1. 在新行中，设置以下值。 接受其他所有字段的默认值。

    - **起始数量：**_0_
    - **目标数量：**_1000000_

1. 选择 **保存** 激活 **货位指令操作** 快速选项卡。

##### <a name="configure-the-location-directive-actions-fasttab"></a>配置“货位指令操作”快速选项卡

1. 在 **货位指令操作** 快速选项卡上，选择 **新建** 创建一行。
1. 在新行中，设置以下值。 接受其他所有字段的默认值。

    - **名称** ： _Bulk_
    - **策略** ： _无_

1. 选择 **保存** 激活 **编辑查询** 按钮。

##### <a name="edit-the-query"></a>编辑查询

1. 在 **位置指令操作** 快速选项卡上，选择 **编辑查询** 。
1. 在 **范围** 选项卡中，选择 **添加** 向网格添加一行。
1. 在新行中，设置以下值：

    - **表：** *位置*
    - **派生表** ： *货位*
    - **字段：** *区域 ID*
    - **条件** ： *Bulk* （选择字段中的双加号 \[**++**\] 展开列表，然后选择 *Bulk* 。）

1. 选择 **确定** 。

## <a name="scenario"></a>应用场景

### <a name="set-up-the-scenario"></a>设置场景

对于此场景，请使用内置示例数据，然后创建本部分中介绍的记录。

#### <a name="use-the-usmf-sample-data"></a>使用 USMF 示例数据

若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。 此外，开始前，还必须选择 **USMF** 法人。

#### <a name="create-demand"></a>创建需求

执行以下步骤创建将为其应用时隙的需求。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单** 。
1. 选择 **新建** 以创建新的销售订单。
1. 在 **创建销售订单** 对话框的 **客户帐户** 字段中，选择 _US-007_ 。
1. 在 **仓库** 字段中，选择 _61_ 。
1. 选择 **确定** 。
1. 将打开新销售订单。 将在 **销售订单行** 快速选项卡中添加一个空行。 在这个行中，设置以下值：

    - **物料：**_L0101_
    - **数量：** _20_

1. 选择 **添加行** 添加新行，然后设置以下值：

    - **物料：**_T0100_
    - **数量：** _8_

1. 选择 **保存** 。
1. 选择 **新建** 以创建第二个销售订单。
1. 在 **创建销售订单** 对话框的 **客户帐户** 字段中，选择 _US-008_ 。
1. 在 **仓库** 字段中，选择 _61_ 。
1. 将打开新销售订单。 将在 **销售订单行** 快速选项卡中添加一个空行。 在这个行中，设置以下值：

    - **物料：**_T0100_
    - **数量：** _1_

1. 选择 **保存** 。

### <a name="walk-through-a-typical-slotting-scenario"></a>完成典型时隙场景

按照上一部分中的说明准备好所有先决元素之后，可以通过完成本部分中的每个练习试用此功能。

#### <a name="generate-demand"></a>生成需求

1. 转到 **仓库管理 \> 设置 \> 补货 \> 时隙模板** ，然后选择前面创建的时隙模板。
1. 在操作窗格上，选择 **生成需求** 。 此命令评估系统中的所有需求，并且与时隙模板查询匹配。 然后将所有订单中的总需求合并到行，每个数量/度量单位一行。 完成此流程时，将显示参考消息。

#### <a name="slotting-demand"></a>时隙需求

*时隙需求* 根据时隙模板的设置显示生成需求的结果。

- 在操作窗格上，选择 **时隙需求** 查看 **生成需求** 命令的结果。 可以编辑时隙需求中的行。 可以删除行，添加新行，或编辑行详细信息。

> [!NOTE]
> 可以手动编辑需求，也可以使用数据管理从外部系统导入需求。 无论时隙中是什么，也无论其来自何处，都将在下一步使用需求。

#### <a name="locate-demand"></a>查找需求

生成需求后，必须使用 **查找需求** 命令生成 *时隙计划* 。

- 在操作窗格上，选择 **查找需求** 。 将运行时隙流程。 完成此流程时，将显示参考消息。

#### <a name="slotting-plan"></a>时隙计划

时隙计划显示将每个物料/数量分配给了哪个货位，是否使用了溢出，是否创建了放弃工作，以及是否使用了模板行。 **所有无法划分时隙的需求均以红色突出显示。**

- 在操作窗格上，选择 **时隙计划** 查看结果。

#### <a name="create-replenishment"></a>创建补货

创建时隙计划之后，必须根据计划创建 *补货工作* 。

- 在操作窗格上，选择 **运行补货** 。 完成此流程时，将显示参考消息。 此消息指示为工作生成 ID 创建的标题的数量。

将根据在每个模板行中指定的指令代码确定将使用的货位指令。

## <a name="tips"></a>提示

### <a name="set-up-automatic-slotting"></a>设置自动时隙

准备好所有必需元素之后，可以执行以下步骤将时隙设置为自动运行。

1. 转到 **仓库管理 \> 补货 \> 运行时隙** 。
1. 指定要运行的时隙步骤。 选择下面的一个或多个时隙步骤：

    - 生成需求
    - 查找需求
    - 创建补货工作

    > [!NOTE]
    > 时隙步骤是渐进的。 如果要选择 *查找需求* ，必须先选择 *生成需求* 。

1. 指定要使用的时隙模板。
1. 如果需要，设置要自动运行的发生次数。

对于此场景中的练习，请 **勿** 设置自动时隙。