---
title: 生产延迟场景
description: 本文介绍生产延迟场景，如果生产吞吐量低于特定阈值，此场景会生成通知。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 073762581d84646ba12b570e57327b7cab8efd3b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428287"
---
# <a name="the-production-delays-scenario"></a>生产延迟场景

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

如果生产完全降到特定阈值下，*生产延迟* 场景将生成通知。 在此场景中，将为生成的每个物料向 Microsoft Azure IoT 中心发送 *部件输出* 信号。 在 Dynamics 365 Supply Chain Management 中，订单延迟基于计划运行的生产订单时间量、应生成的物料数量、作业已运行的时间量和收到的 *部件输出* 信号数量计算。 如果作业的 *部件输出* 信号数量低于阈值，将生成延迟通知。

## <a name="scenario-dependencies"></a>场景依赖关系

*生产延迟* 场景具有以下依赖关系：

- 仅当正在映射的机器上运行生产订单，才能触发警报。
- 必须将表示映射的机器 *部件输出* 信号的型号发送到 IoT 中心，并且必须包含唯一属性名称。
- Azure IoT 中心消息中必须包含 UNIX 时间戳记属性，其中值以毫秒 (ms) 表示。

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>为产品延迟场景准备演示数据

如果您想要使用演示系统测试 *生产延迟* 场景，请使用安装了 [演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)的系统，选择 *USMF* 法人（公司），然后按照本节所述准备其他演示数据。 如果您使用自己的传感器和数据，可以跳过此节。

### <a name="set-up-sensor-simulator"></a>设置传感器模拟器

如果您想在不使用物理传感器的情况下尝试此场景，可以设置一个模拟器来生成所需的信号。 有关详细信息，请参阅[设置模拟传感器以进行测试](sdi-set-up-simulated-sensor.md)。

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>验证资源 3118 是否用于产品 P0111

将计划并下达生产订单。 因此，将生产作业发布到资源 *3118*（*泡沫切割机*）。 按照以下步骤验证资源 *3118* 是否用于演示数据中的产品 *P0111*。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 找到并选择 **物料编号** 字段设置为 *P0111* 的产品。
1. 在操作窗格的 **设计** 选项卡的 **视图** 组中，选择 **工艺路线**。
1. 在 **工艺路线** 页面上，在页面底部的 **概览** 选项卡上，选择 **工序编号** 字段设置为 *30* 的行。
1. 在页面底部的 **资源要求** 选项卡上，确保资源 *3118*（*泡沫切割机*）与此工序关联。

### <a name="create-and-release-a-production-order-for-product-p0111"></a>为产品 P0111 创建和下达生产订单

按照以下步骤为产品 *P0111* 创建和下达生产订单。

1. 转到 **生产控制 \> 生产订单 \> 所有生产订单**。
1. 在 **所有生产订单** 页面，在操作窗格上，选择 **新建批次订单**。
1. 在 **创建批次** 对话框中，设置以下值：

    - **物料编号：***P0111*
    - **数量：** *10*

1. 选择 **创建** 创建订单并返回到 **所有生产订单** 页。
1. 使用 **筛选** 字段搜索 **物料编号** 字段设置为 *P0111* 的生产订单。 然后找到并选择您刚才创建的生产订单。
1. 在操作窗格上，在 **生产订单** 选项卡的 **流程** 组中，选择 **估计**。
1. 在 **估计** 对话框中，选择 **确定** 运行估计。
1. 在操作窗格上，在 **生产订单** 选项卡的 **流程** 组中，选择 **下达**。
1. 在 **下达** 对话框中，记下您刚才创建的批次订单的编号。
1. 选择 **确定** 下达订单。

### <a name="configure-the-production-floor-execution-interface"></a>配置生产车间执行界面

如果您还没有配置，请配置生产车间执行界面以显示分配给资源 *3118*（*泡沫切割机*）的作业。 有关说明，请参阅以下各节：

- [配置生产车间执行界面](sdi-scenario-equipment-downtime.md#config-pfe)
- [在生产车间执行界面启用搜索选项](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>开始批次订单中的第一个作业

按照以下步骤开始批次订单中的第一个作业。

1. 转到 **生产控制 \> 制造执行 \> 生产车间执行**。
1. 在 **标记 ID** 字段中，输入 *123*。 然后选择 **登录**。
1. 如果系统提示您提供缺勤原因，选择一张缺勤卡，然后选择 **确定**。
1. 在 **搜索** 字段中，输入您之前记下的批次订单编号。 然后选择 **返回** 键。
1. 选择订单，然后选择 **开始作业**。
1. 在 **开始作业** 对话框中，选择 **开始**。

## <a name="set-up-the-production-delays-scenario"></a>设置生产延迟场景

按照以下步骤在 Supply Chain Management 中设置 *生产延迟* 场景。

1. 转到 **生产控制 \> 设置 \> Sensor Data Intelligence \> 场景**。
1. 在 **生产延迟** 场景框中，选择 **配置** 打开此场景的设置向导。
1. 在 **传感器** 页面，选择 **新增** 将传感器添加到网格中。 然后为新传感器设置以下字段：

    - **传感器 ID** – 输入您正在使用的传感器的 ID。 （如果您使用的是 Raspberry PI Azure IoT 联机模拟器并已按照 [设置模拟传感器以进行测试](sdi-set-up-simulated-sensor.md)中所述进行设置，输入 *ProductionDelay*。）
    - **传感器描述** – 输入传感器的描述。

1. 对您现在要添加的每个其他传感器重复上一个步骤。 您可以随时返回添加更多传感器。
1. 选择 **下一步**。
1. 在 **业务记录映射** 页面的 **传感器** 部分，选择您刚才添加的其中一个传感器的记录。
1. 在 **业务记录映射** 部分，选择 **新建** 在网格中添加一行。
1. 在新行上，将 **业务记录** 设置为您使用所选传感器监视的资源。 （如果您使用的是您在本文前面创建的演示数据，将此字段设置为 *3118，泡沫切割机*。）
1. 选择 **下一步**。
1. 在 **生产延迟偏差阈值** 页面，如果您使用的是在本文前面创建的演示数据，请按照以下步骤操作：

    1. 选择 **物料关系** 列标题打开包含该列的搜索筛选器的下拉对话框。 在搜索框中输入 *P0111*，然后选择 **应用**。
    2. 选择 **工序** 字段设置为 *修剪/切割* 的行。 将 **延迟的通知阈值(%)** 字段设置为应发送通知的阈值（百分比）。

1. 选择 **下一步**。
1. 在 **激活传感器** 页面的网格中，选择您添加的传感器，然后选择 **激活**。 对于网格中每个激活的传感器，**可用** 列中会出现一个复选标记。
1. 选择 **完成**。

## <a name="work-with-the-production-delays-scenario"></a>处理生产延迟场景

### <a name="view-production-delay-data-on-the-resource-status-page"></a>在资源状态页面查看生产延迟数据

在 **资源状态** 页面，主管可以监视从映射到每个机器资源的传感器接收到的信号的时间线。 按照以下步骤配置时间线。

1. 转到 **生产控制 \> 制造执行 \> 资源状态**。
1. 在 **配置** 对话框中，设置以下字段：

    - **资源** – 选择您要监视的资源。 （如果您使用的是演示数据，选择 *3118*。）
    - **时序 1** – 选择名称具有以下格式的记录（指标键）：*ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **显示名称** – 输入 *部件输出信号*。
