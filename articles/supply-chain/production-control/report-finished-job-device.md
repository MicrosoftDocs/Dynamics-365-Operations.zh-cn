---
title: 从作业卡设备报告完工入库
description: 本主题介绍如何配置系统，以让作业卡设备的用户可以将生产订单中的成品报告到库存。
author: johanhoffmann
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6ba5d8bc0c22f97e6d2ce61c636090e04fae5abd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422930"
---
# <a name="report-as-finished-from-the-job-card-device"></a>从作业卡设备报告完工入库

[!include [banner](../includes/banner.md)]

工作人员使用作业卡设备上的 **报告进度** 页面报告生产作业已完成的数量。 本主题介绍如何设置各个选项，来确立工作人员使用此页面报告完工入库的方法以及接下来要执行的事项。 选项包括：

- 控制是否以及如何将报告为完工入库的数量添加到库存中。
- 控制在报告完工入库时是否以及如何生成和应用批号。
- 控制在报告完工入库时是否以及如何生成和应用序列号。
- 控制是否以及如何向牌照报告完工入库。

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>控制是否将报告为完工入库的数量添加到库存中

若要控制是否以及如何将最后工序中报告为完工入库的数量添加到库存中，请按照下列步骤操作。

1. 转到 **产品控制 \> 设置 \> 制造执行 \> 生产订单默认值**。
1. 在 **完工入库** 选项卡上，将 **联机更新已完成的报告** 字段设置为以下值之一：

    - **无** – 在最后工序中报告数量后，不会将任何数量添加到库存。 生产订单的状态永远不会更改。
    - **状态 + 数量** – 生产订单的状态将更改为 *完工入库*，数量将报告为已完工入库。
    - **数量** – 数量将报告为已完工入库，但生产订单的状态永远不会更改。
    - **状态** – 仅生产订单的状态将更改。 在最后工序中报告数量后，不会将任何数量添加到库存。

> [!NOTE]
> 如果报告为完工入库的工序未定义为最后工序，将不会在库存中跟踪数量。 但是，这些数量可用于查看进度。 另外还可以包含在规则中，帮助控制工作人员是否可以在达到上一个工序报告数量的定义阈值之前开始下一个工序。 您可以在 **生产订单默认值** 页面的 **数量验证** 选项卡上定义这些规则。

有关如何使用 **生产订单默认值** 页面的详细信息，请参阅[制造执行中的生产参数](production-parameters-manufacturing-execution.md)。

## <a name="report-batch-controlled-items-as-finished"></a>将批次控制物料报告为完工入库

作业卡设备支持三种方案来报告批物料。 这些方案既适用于高级仓库流程支持的物料，也适用于高级仓库流程不支持的物料。

- **手动分配的批号** - 工作人员输入自定义批号。 此批号可能来自系统未知的外部来源。
- **预定义的批号** - 工作人员在生产订单下达到作业卡设备之前，系统自动生成的批号列表中选择一个批号。
- **固定批号** - 工作人员不输入或选择批号。 系统会在生产订单下达之前自动向其分配批号。


### <a name="enable-the-feature-on-your-system"></a>在系统中启用此功能

要让您的作业卡设备在报告完工入库过程中接受批号，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：

1. 改进的作业卡设备中“报告进度”对话框的用户体验
1. 允许在从作业卡设备（预览）报告为完工入库时输入批号和序列号

### <a name="configure-products-that-require-batch-number-reporting"></a>配置需要报告批号的产品

要使产品支持任何可用的批次控制方案，请按照下列步骤操作：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择要配置的产品。
1. 在 **管理库存** 快速选项卡上，在 **批号组** 字段中，选择为支持您的方案而设置的跟踪号组。

> [!NOTE]
> 默认情况下，如果批号未分配给批次控制产品，作业卡设备将在报告完工入库期间为批号提供手动输入。

以下各节介绍如何设置跟踪号组，以支持批次物料报告的三种方案。

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>设置让工作人员可以手动分配批号的跟踪号组

要允许手动分配批号，请按以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **手动** 选项设置为 **是**。

    ![手动批号的跟踪号组](media/tracking-number-group-manual.png "手动批号的跟踪号组")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批号** 字段是一个文本框，工作人员可以在其中输入任何值。

![具有手动批号字段的报告进度页面](media/job-card-device-batch-manual.png "具有手动批处理号字段的报告进度页面")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>设置提供预定义批号列表的跟踪号组

要提供预定义批号列表，请按以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 > 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **是**。
1. 使用 **按数量** 字段根据您输入的值按数量拆分批号。 例如，您有一个十件产品的生产订单，**按数量** 字段设置为 *2*。 在这种情况下，将在生产订单创建时向其分配五个批号。

    ![预定义批号的跟踪号组](media/tracking-number-group-predefined.png "预定义批号的跟踪号组")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批处理号** 字段是一个下拉列表，工作人员必须在其中选择预定义值。

![具有预定义批号列表的报告进度页面](media/job-card-device-batch-predefined.png "具有预定义批号列表的报告进度页面")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>设置自动分配批号的跟踪号组

如果应在没有工作人员输入的情况下自动分配批号，请按照以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **否**。
1. 将 **手动** 选项设置为 **否**。

    ![固定批号的跟踪号组](media/tracking-number-group-fixed.png "固定批号的跟踪号组")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批处理号** 字段将显示一个值，但工作人员不能进行编辑。

![具有固定批号的报告进度页面](media/job-card-device-batch-fixed.png "具有固定批号的报告进度页面")

## <a name="report-serial-controlled-items-as-finished"></a>将序列控制物料报告为完工入库

作业卡设备支持三种方案来报告序列控制物料。 这些方案既适用于高级仓库流程支持的物料，也适用于高级仓库流程不支持的物料。

- **手动分配的序列号** - 工作人员输入自定义序列号。 此序列号可能来自系统未知的外部来源。
- **预定义序列号** - 工作人员在生产订单下达到作业卡设备之前，系统自动生成的序列号列表中选择一个序列号。
- **固定序列号** - 工作人员不输入或选择序列号。 系统会在生产订单下达之前自动向其分配序列号。

### <a name="enable-the-feature-on-your-system"></a>在系统中启用此功能

要让您的作业卡设备在报告完工入库过程中接受序列号，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：

1. 改进的作业卡设备中“报告进度”对话框的用户体验
1. 允许在从作业卡设备（预览）报告为完工入库时输入批号和序列号

### <a name="configure-products-that-require-serial-number-reporting"></a>配置需要报告序列号的产品

要使产品支持任何可用的序列控制方案，请按照下列步骤操作：

若要启用每个方案，请执行以下步骤。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择要配置的产品。
1. 在 **管理库存** 快速选项卡上，在 **序列号组** 字段中，选择为支持您的方案而设置的跟踪号组。

> [!NOTE]
> 默认情况下，如果序列号未分配给序列控制产品，作业卡设备将在报告完工入库期间为序列号提供手动输入。

以下各节介绍如何设置跟踪号组，以支持序列控制物料报告的三种方案。

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>设置让工作人员可以手动分配序列号的跟踪号组

要允许手动分配序列号，请按以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **手动** 选项设置为 **是**。

    ![跟踪号组页面，序列号](media/tracking-number-group-manual-serial.png "跟踪号组页面，序列号")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段是一个文本框，工作人员可以在其中输入任何序列号值。 输入值后，它将被添加到序列号列表中。 在此列表中，工作人员可以执行以下操作：

- 要将序列号标记为报废，请选择相应行的 **报废** 按钮。 系统将提示工作人员提供 **错误原因**。
- 要删除序列号，请选择相应行的 **删除** 按钮。

![具有手动序列号字段的报告进度页面](media/job-card-device-serial-manual.png "具有手动序列号字段的报告进度页面")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>设置提供预定义序列号列表的跟踪号组

要提供预定义序列号列表，请按以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **是**。
1. 使用 **按数量** 字段按数量一拆分序列号。

    ![预定义序列号的跟踪号组](media/tracking-number-group-predefined-sn.png "预定义序列号的跟踪号组")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段是一个下拉列表，工作人员必须在其中选择预定义值。

![具有预定义序列号列表的报告进度页面](media/job-card-device-serial-predefined.png "具有预定义序列号列表的报告进度页面")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>设置自动分配序列号的跟踪号组

如果应在没有工作人员输入的情况下自动分配序列号，请按照以下步骤设置跟踪号组。

1. 转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。
1. 创建或选择要设置的跟踪号组。
1. 在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **否**。
1. 将 **手动** 选项设置为 **否**。

    ![固定序列号的跟踪号组](media/tracking-number-group-fixed-sn.png "固定序列号的跟踪号组")

1. 根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。

使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段将显示一个值，但工作人员不能进行编辑。 此方案仅在为数量为一件序列号控制物料创建生产订单时有用。

![具有固定序列号的报告进度页面](media/job-card-device-serial-fixed.png "具有固定序列号的报告进度页面")

## <a name="report-as-finished-to-a-license-plate"></a>报告为已完工入库到牌照

高级仓库流程可以使用牌照维度来跟踪为此目的设置的仓库位置的库存。 在这种情况下，工作人员报告完工入库数量时需要牌照编号。

### <a name="enable-license-plate-reporting-and-label-printing"></a>启用牌照报告和标签打印

要使用本节介绍的功能，必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：

1. 用于报告为完工入库的牌照已添加作业卡设备
1. 在作业卡设备中报告为完工入库时，启用牌照编号的自动生成
1. 从作业卡设备打印标签

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>设置报告为已完工入库到牌照

要控制工作人员在报告完工入库数量后是应该重用现有牌照还是生成新牌照，请按照以下步骤操作。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 为设备配置作业卡**。
2. 为每个设备设置以下选项：

    - **生成牌照** – 将此项设置为 **是** 将为每次报告完工入库生成新牌照。 如果应为每次报告完工入库使用现有牌照，则设置为 **否**。
    - **打印标签** – 如果工作人员必须为每次报告完工入库打印牌照标签，将此项设置为 **是**。 如果不需要标签，则设置为 **否**。 

![配置设备的作业卡页面](media/config-job-card-raf.png "配置设备的作业卡页面")

> [!NOTE]
> 要配置标签，转到 **仓库管理 \> 设置 \> 文档路径 \> 文档路径**。 有关详细信息，请参阅[启用牌照标签打印](../warehousing/tasks/license-plate-label-printing.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]