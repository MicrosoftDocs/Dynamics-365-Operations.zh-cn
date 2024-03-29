---
title: 库位容量范围内的补货
description: 本文提供有关“按位置容量补货”功能的信息。 此功能使创建当天所需的所有补货工作成为可能，并管理该补货工作的可用性，以确保领料位置既不会用完库存，也不会超出容量。
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 543afe2e689fa787158551bec64e2458141be71c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220078"
---
# <a name="replenishment-over-location-capacity"></a>库位容量范围内的补货

[!include [banner](../includes/banner.md)]

有些大容量或空间受限的仓库每天必须装运比领料位置将容纳的更多数量的物料。 *按位置容量补货* 功能使创建当天所需的所有补货工作成为可能，并管理该补货工作的可用性，以确保领料位置既不会用完库存，也不会超出容量。

此功能使创建的补货工作多于某个位置所能容纳的数量，当该位置已满时，它将阻止完成补货工作。 随着领料位置的库存下降到可配置阈值以下，可以进行更多的补货工作。

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>启用“按位置容量补货”功能

要使此功能可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：

1. 组织范围内的工作锁定（从 Supply Chain Management 版本 10.0.21 开始，此功能是强制性的，因此默认情况下处于开启状态，无法再次关闭。）
1. 库位容量范围内的补货

## <a name="set-up-the-feature-for-the-example-scenario"></a>为示例方案设置此功能

本节提供指南和示例，演示如何设置此功能，以及如何为本文后面提供的示例方案准备示例数据。

### <a name="enable-sample-data"></a>启用示例数据

若要使用此处指定的示例记录和值演练[示例方案](#example-scenario)，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)。 此外，开始前，还必须选择 **USMF** 法人。

### <a name="location-profile"></a>位置模板

在位置模板上启用按容量补货功能。

1. 转到 **仓库管理 \> 设置 \> 仓库 \> 位置模板**。
1. 在左窗格中，选择 **PICK-06**。
1. 在操作窗格上，选择 **编辑**。
1. 在 **补货** 快速选项卡上，设置以下值：

    - **超出位置容量**：*是*

        在启用时，补货工作将允许超过库位的最大产能。 这也会启用 **补货** 快速选项卡上的其他字段。

    - **工作可用性阈值类型**：*数量*

        此字段定义用于确定何时应释放更多工作的方法。 您可以按数量或百分比释放：

        - *百分比* – 选择此选项可以使用基于库存限制或容量的百分比容量。 选择此选项将启用 **溢出百分比** 字段，并禁用两个数量相关字段 **溢出数量** 和 **溢流单位**。

            如果领料位置使用容量，可以使用此选项。

            如果选择此选项，请将 **溢出百分比** 字段设置为可以进行更多补货工作的百分比。

        - *数量* – 选择此选项可以使用特定的数量值。 选择此选项将禁用 **溢出百分比** 字段，并启用 **溢出数量** 和 **溢流单位** 字段。

            当您没有对要补货的位置使用容量时，或者您希望在将更多库存放入该位置时数量保持一致时，使用此选项。

           如果选择此选项，请将 **溢出数量** 和 **溢流单位** 字段设置为可进行更多补货工作的数量和单位。

    - **溢出数量**：*0.65*

        此字段定义位置溢出的数量。

        只要位置的现有数量与工作数量的总和低于此值，工作就可以进行。 超过此值的任何补货工作将被锁定，并且必须手动解锁。

        计算工作数量时将考虑位置库存限制。

    - **溢出单位**：*托盘*

        此字段定义与溢出量关联的单位。

        在此例中，当位置降至 0.65 托盘 (PL) 时，可以进行更多补货工作。

    - **超额百分比**

        此字段定义位置溢出的百分比。

        只要位置的现有数量与工作数量的总和低于此百分比，工作就可以进行。 超过此值的任何补货工作数量百分比将被锁定，并且必须手动解锁。

        计算工作数量百分比时将考虑位置库存限制。 如果未定义库位库存限制，则在位置模板中定义了体积约束后，将按体积计算工作数量百分比。

> [!IMPORTANT]
> 如果您使用的是 **USMF** 法人的演示数据，并且先前已打开 *位置牌照定位* 功能，则必须关闭 **BULK-06** 位置模板的 **启用牌照定位** 设置，才能完成示例方案中的移动步骤。

### <a name="wave-step-code"></a>波次步骤代码

> [!NOTE]
> 要按照此处所述设置波次步骤代码，您可能首先必须使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)打开名为 *组织范围内的波次步骤代码* 的功能。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次步骤代码**。
1. 选择 **新建**，设置以下值：

    - **波次步骤代码**：*Replen*
    - **波次步骤描述**：*补货*
    - **波次步骤类型**：*补货*

1. 选择 **保存**。

### <a name="replenishment-template"></a>补货模板

补货模板是控制何时和如何为货位补货的一系列规则。

1. 转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。
1. 在操作窗格上，选择 **编辑**。
1. 在 **概览** 部分，选择 **补货模板** 字段设置为 *需求补货* 的行。
1. 设置以下值：

    - **波次步骤代码**：*Replen*
    - **允许波次需求使用未预留数量：***是*

1. 选择 **保存**。

### <a name="wave-template"></a>波次模板

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。
1. 在左窗格中，将 **波次模板类型** 设置为 *装运*。
1. 在列表中选择模板 **61 装运**。
1. 在操作窗格上，选择 **编辑**。
1. 在 **常规** 快速选项卡上，将 **自动化补货工作释放** 选项设置为 *是*。

    将此选项设置为 *是* 来创建基于需求的补货工作并将其自动释放。 您必须将补货波次方法添加到波次模板，然后创建 **波次需求** 类型的补货模板。 在 **补货模板** 页设置一个补货模板。 要设置补货模板，必须将补货方法添加到波次模板。

1. 在 **方法** 快速选项卡上，在 **选定方法** 列中，找到以下行：

    - **方法名称**：*补货*
    - **名称**：*补货*

1. 将此行的 **波次步骤代码** 字段设置为 *Replen*。
1. 选择 **保存**。

## <a name="example-scenario"></a>示例场景

在使所有前面描述的示例数据可用并进行设置之后，您可以演练此方案来试用 *按位置容量补货* 功能了。 此方案中显示的值假设您使用的是标准演示数据，选择了 **USMF** 法人，并且您准备了本文前面介绍的示例记录。 此方案还可以用作说明如何在生产设置中使用此功能的示例。

### <a name="create-replenishment-work"></a>创建补货工作

#### <a name="create-sales-order-1"></a>创建销售订单 1

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。
1. 在对话框中，设置以下值：

    - **客户帐户**：*US-007*
    - **仓库**：*61*

1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 将在 **销售订单行** 快速选项卡中添加一个新的空行。 在这个行中，设置以下值：

    - **物料编号：***T0100*
    - **数量：** *40*

1. 在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。
1. 在 **预留** 页上，选择 **预留批次**。
1. 关闭该页面。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。

    您将收到显示创建的波次 ID 和装运 ID 的信息性消息。 补货波次也将创建。

    您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”

#### <a name="create-sales-order-2"></a>创建销售订单 2

1. 在 **所有销售订单** 页面上，在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。
1. 在对话框中，设置以下值：

    - **客户帐户**：*US-001*
    - **仓库**：*61*

1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 将在 **销售订单行** 快速选项卡中添加一个新的空行。 在这个行中，设置以下值：

    - **物料编号：***T0100*
    - **数量：** *60*

1. 在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。
1. 在 **预留** 页上，选择 **预留批次**。
1. 关闭该页面。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。

    您将收到显示创建的波次 ID 和装运 ID 的信息性消息。 补货波次也将创建。

    您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”

#### <a name="create-sales-order-3"></a>创建销售订单 3

1. 在 **所有销售订单** 页面上，在操作窗格上，选择 **新建** 打开创建新销售订单的对话框。
1. 在对话框中，设置以下值：

    - **客户帐户**：*US-004*
    - **仓库**：*61*

1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 将在 **销售订单行** 快速选项卡中添加一个新的空行。 在这个行中，设置以下值：

    - **物料编号：***T0100*
    - **数量：** *30*

1. 在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。
1. 在 **预留** 页上，选择 **预留批次**。
1. 关闭该页面。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。

    您将收到显示创建的波次 ID 和装运 ID 的信息性消息。 补货波次也将创建。

    您还会收到一条警告消息，指示“工作 ID XXXX 无法解锁，它有未完成的补货工作。”

#### <a name="view-work-details"></a>查看工作详细信息

1. 转到 **仓库管理 \> 工作 \> 工作详细信息**。
1. 在 **概览** 部分，筛选仓库 *61* 的 **仓库** 列。
1. 您应该看到为三个需求销售订单创建了七个工作 ID。

    - 七个工作 ID 中有三个的 **工作订单类型** 值为 *补货*，四个的 **工作订单类型** 值为 *销售订单*。
    - **工作订单类型** 值为 *补货* 的所有三个工作 ID 在 **行** 部分有相同的 *领料* 和 *放置* 位置：

        - **领料**：*02A01R5S1B*
        - **放置**：*06A01R2S1B*

    - 为销售订单 1 创建了两个工作 ID。

1. 记下销售订单的工作 ID。

根据您的现有数量，创建的工作数量可能会略有不同。 但是，总体上，创建的工作标题应与此方案示例匹配。

#### <a name="on-hand-inventory-license-plate-id"></a>现有库存量牌照 ID

在此方案的后面，您将使用仓库管理移动应用（或模拟器），这时，您必须确定牌照才能完成领料和补货方案。

要查找以后需要的牌照 ID，请按照以下步骤操作。

1. 转到 **库存管理 \> 查询和报表 \> 现有量列表**。
1. 选择 **显示筛选器** 按钮打开筛选器窗格。
1. 输入以下筛选条件以获取方案的车牌。 使用 *开头为* 筛选器。

    - **物料编号：***T0100*
    - **仓库**：*61*

1. 选择 **应用**。
1. 在操作窗格上，选择 **维度**。
1. 在 **维度显示** 对话框的 **存储维度** 部分，选择所有值。
1. 在 **事务** 部分，选择 **物料编号** 和 **数量 \<\> 0**。
1. 完成后，选择 **确定** 关闭对话框。
1. **现有** 网格显示每个位置物料 *T0100* 的牌照编号。 记下每个位置的牌照，稍后您将需要此信息。
1. 关闭该页面。

### <a name="process-steps"></a>流程步骤

您将为前两个工作 ID 执行仓库位置补货。 第三项补货工作的工作将被阻止，直到领料位置的库存级别降至阈值以下。

#### <a name="replenishment"></a>补货

1. 以仓库 *61* 用户身份登录到仓库管理移动应用。 （用户 ID 输入 *61*，密码输入 *1*。）
1. 转到 **库存 \> 补货**。

    系统将提示您完成第一项补货工作。 物料编号、数量和要领料的位置将显示。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。
1. 选择 **确定** 按钮（复选标记符号）。

    系统将为所领取物料的新牌照生成目标牌照编号。

1. 选择 **确定** 确认值。

    放置工作将显示，指示用户将目标牌照放到补货位置。 *放置* 位置应该是 **06A01R2S1B**。

1. 确认放置详细信息，然后选择 **确定**。

    您将收到“工作已完成”消息，同时显示下一个补货领料任务的详细信息：物料编号、数量、要领料的位置。 领料位置将与第一个补货位置相同。 因此，牌照将具有与第一项补货工作任务使用的相同的牌照 ID。

1. 重复上述步骤完成第二项工作任务的补货工作。 数量和目标牌照将不同于第一项工作任务的数量和目标牌照。

在第二项补货工作完成后，您会收到“工作已完成”消息。 移动设备也会通知您没有可进行的工作，即使剩余了一些补货工作。 发生此行为的原因是补货工作的可用性状态为 *暂停*，因此被标记为 **已锁定**。

*暂停* 状态被触发，是因为分配了工作的领料位置的位置模板的 **溢流数量** 值为 *0.65 PL*。 之前的两项补货工作任务几乎已将位置填充到物料 *T0100* 的溢出限制。 （物料的单位转换为 *1 托盘 = 100 个*。）因此，剩余的补货工作将导致该位置超出其溢出限制。

直到从该位置领取了足够库存才能降低到移动设备菜单项上的工作释放阈值以下，此补货工作仍将处于锁定状态。

#### <a name="sales-order-pick"></a>销售订单领料

领料位置的库存必须消耗到可以解锁其余补货工作的级别，才能够完成剩余补货工作任务。 换言之，该位置的现有库存数量与补货数量之和不能超过 **溢出数量** 值。 当此和低于溢出数量时，剩余补货工作将被解锁。

1. 以仓库 *61* 用户身份登录到仓库管理移动应用。 （用户 ID 输入 *61*，密码输入 *1*。）
1. 转到 **出站 \> 销售领料**。
1. 输入销售订单 1 的第一个工作 ID。

    请参考您先前记下的 **工作详细信息** 页面上的销售订单的工作 ID。 您在此处输入的工作 ID 将分别在两个位置生成数量为 10 个的领料工作。

1. 选择 **确定**。

    **销售订单：领料** 任务页面将显示第一个位置的物料编号、数量和要领料的位置。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。
1. 选择 **确定** 按钮（复选标记符号）。

    **销售订单：领料** 任务页面将显示下一个位置的物料编号、数量和要领料的位置。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。
1. 选择 **确定** 按钮（复选标记符号）。

    **销售订单：放置** 页面将指示您将完成的两项领料工作放到出站暂存位置。

1. 选择 **确定**。

    您将收到“工作已完成”消息。

1. 输入销售订单 1 的第二个工作 ID。

    此工作 ID 只有一个领料任务。

1. 选择 **确定**。

    **销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。

    您指定的牌照将是补货工作任务中系统生成的牌照之一。 为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。

1. 选择 **确定** 按钮（复选标记符号）。
1. 确认将任务放置到出站暂存位置的指示。
1. 选择 **确定**。

    您将收到“工作已完成”消息。

由于与其关联的补货任务未完成，销售订单 2 被锁定，无法领料。 当前，领料位置的数量仍然为 30 个，销售订单 2 的补货数量为 60 个。 现有库存量和补货库存量的总和（90 个）超出溢出数量 0.65 托盘（或 65 个）。 销售订单 3 必须先领料，然后才能够完成补货工作。

1. 输入销售订单 3 的工作 ID。

    此工作 ID 只有一个领料任务。

1. 选择 **确定**。

    **销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。

    您指定的牌照将是补货工作任务中系统生成的牌照之一。 为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。

1. 选择 **确定** 按钮（复选标记符号）。
1. 确认将任务放置到出站暂存位置的指示。
1. 选择 **确定**。

    您将收到“工作已完成”消息。

一旦领料位置的现有数量与补货数量之和低于阈值，您便可以处理剩余的补货工作。

返回 **工作详细信息** 页面，注意补货最后一项工作（销售订单 2）的补货工作可用性为 *开放*，因为现在该位置有足够的空间来接受补货。

您现在可以通过移动设备处理此补货工作。

1. 转到 **库存 \> 补货**。

    系统将提示您完成剩余补货工作。 物料编号、数量和要领料的位置将显示。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。
1. 选择 **确定** 按钮（复选标记符号）。

    系统将为所领取物料的新牌照生成目标牌照编号。

1. 选择 **确定** 确认值。

    放置工作将显示，指示用户将目标牌照放到补货位置。 *放置* 位置应该是 **06A01R2S1B**。

1. 确认放置详细信息，然后选择 **确定**。

    您将收到“工作已完成”和“没有可进行的工作”消息。

现在，您可以为销售订单 2 领料。 当与此销售订单关联的补货工作完成时，它将变为解锁状态。

1. 输入销售订单 2 的工作 ID。

    此工作 ID 只有一个领料任务。

1. 选择 **确定**。

    **销售订单：领料** 任务页面将显示物料编号、数量和要领料的位置。

1. 在 **牌照** 字段中，在显示的位置中输入物料的牌照编号。

    您指定的牌照将是补货工作任务中系统生成的牌照。 为确保您捕获了正确的牌照 ID，请在 **现有量列表** 页面检查库存的物料、位置和数量。

1. 选择 **确定** 按钮（复选标记符号）。
1. 确认将任务放置到出站暂存位置的指示。
1. 选择 **确定**。

    您将收到“工作已完成”消息。

## <a name="notes-and-tips"></a>说明和提示

- 此功能适用于所有类型的补货：波次需求、最小/最大、负荷需求和时隙。
- 如果需要，您可以从 **工作详细信息** 页面手动覆盖每个工作标题的补货工作可用性。
- 当系统设置补货工作可用性时，将考虑在完成任何工作之前该位置已经存在的任何库存
- 销售订单工作的每项工作都将关联到特定的补货工作。 没有相应的销售工作可用性功能。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]