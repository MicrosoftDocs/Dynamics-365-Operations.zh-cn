---
title: 资产维护场景
description: 本文介绍资产维护场景，它允许您使用传感器数据创建跟踪机器资产使用情况的计数器记录。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ff3944b987314a688a5829b05f8627479e3e79ed
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428285"
---
# <a name="the-asset-maintenance-scenario"></a>资产维护场景

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*资产维护* 场景允许您使用传感器数据创建计数器记录。 计数器记录跟踪机器资产的使用情况，用作生成机器资产维护安排的输入。

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>为资产维护场景准备演示数据

如果您想要使用演示系统测试 *资产维护* 场景，请使用安装了 [演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)的系统，选择 *USMF* 法人（公司），然后按照本节所述准备其他演示数据。 如果您使用自己的传感器和数据，可以跳过此节。

在本节中，您将以演示数据中的 *AK-101，气刀* 资产为例进行设置。 然后，您将看到如何根据度量气刀运行小时数的传感器信号预测即将进行的维护工作。 您还将设置维护计划：必须每 10,000 小时维护一次气刀。

### <a name="set-up-a-sensor-simulator"></a>设置传感器模拟器

如果您想在不使用物理传感器的情况下尝试此场景，可以设置一个模拟器来生成所需的信号。 有关详细信息，请参阅[设置模拟传感器以进行测试](sdi-set-up-simulated-sensor.md)。

### <a name="create-an-asset-counter-to-track-production-hours"></a>创建资产计数器来跟踪生产工时

按照以下步骤创建资产计数器来跟踪生产工时。

1. 转到 **资产管理 \> 设置 \> 资产类型 \> 计数器**。
1. 在“操作窗格”中，选择 **新建** 创建一个计数器。
1. 在标题中，设置以下值：

    - **计数器**：*ProductionHr*
    - **名称**：*生产工时*

1. 在 **常规** 快速选项卡上，设置以下值：

    - **单位**：*小时*
    - **更新**：*手动*
    - **总计聚合**：*总和*

1. 在 **资产类型** 快速选项卡中，选择 **添加行**。
1. 在新行上，将 **资产类型** 字段设置为 *气刀*。

### <a name="create-a-maintenance-plan-for-the-asset"></a>为资产创建维护计划

按照以下步骤为资产创建维护计划。

1. 转到 **资产管理 \> 设置 \> 预防性维护 \> 维护计划**。
1. 在“操作窗格”中，选择 **新建** 创建维护计划。
1. 在标题中，设置以下值：

    - **维护计划**：*AirKnife*
    - **名称**：*气刀计划*

1. 在 **详细信息** 快速选项卡上，设置以下值：

    - **计划日期：** 输入今天的日期。
    - **有效：***是*

1. 在 **行** 快速选项卡上，选择 **添加资产计数器行** 向网格添加一行。 然后为行设置以下值：

    - **工作订单描述**：*气刀维护*
    - **维护作业类型**：*预防*
    - **间隔类型**：*从上次工作订单开始重复*
    - **期间频率**：*10000*
    - **计数器**：*ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>设置资产维护场景

按照以下步骤在 Supply Chain Management 中设置 *资产维护* 场景。

1. 转到 **资产管理 \> 设置 \> Sensor Data Intelligence \> 场景**。
1. 在 **资产维护** 场景框中，选择 **配置** 打开此场景的设置向导。
1. 在 **传感器** 页面，选择 **新增** 将传感器添加到网格中。 然后为新传感器设置以下字段：

    - **传感器 ID** – 输入您正在使用的传感器的 ID。 （如果您使用的是 Raspberry PI Azure IoT 联机模拟器并已按照 [设置模拟传感器以进行测试](sdi-set-up-simulated-sensor.md)中所述进行设置，输入 *AssetMaintenance*。）
    - **传感器描述** – 输入传感器的描述。

1. 对您现在要添加的每个其他传感器重复上一个步骤。 您可以随时返回添加更多传感器。
1. 选择 **下一步**。
1. 在 **业务记录映射** 页面的 **传感器** 部分，选择您刚才添加的其中一个传感器的记录。
1. 在 **业务记录映射** 部分，选择 **新建** 在网格中添加一行。
1. 在新行上，**业务记录类型** 字段应会自动设置为 *Assets(EntAssetObjectTable)*。 将 **业务记录** 字段设置为您使用所选传感器监视的资源。 （如果您使用的是您在本文前面创建的演示数据，将其设置为 *AK-101，行 1 AK-101 气刀*。）
1. 为您在上一步中添加的行选择业务记录类型后，第二行会立即被自动添加到网格。 在这一行中，**业务记录类型** 字段应设置为 *Counters(EntAssetCounterType)*。 将 **业务记录** 字段设置为您根据来自所选传感器的信号更新的资产计数器。 （如果您使用的是您在本文前面创建的演示数据，将其设置为 *ProductionHr，生产工时*。）
1. 选择 **下一步**。
1. 在 **激活传感器** 页面的网格中，选择您添加的传感器，然后选择 **激活**。 对于网格中每个激活的传感器，**可用** 列中会出现一个复选标记。
1. 选择 **完成**。

## <a name="work-with-the-asset-maintenance-scenario"></a>处理资产维护场景

### <a name="view-counter-values"></a>查看计数器值

准备好数据并配置并激活 *资产维护* 场景后，您可以看到资产计数器的记录是如何根据传感器数据插入的。

1. 转到 **资产管理 \> 资产 \> 所有资产**。
1. 查找并选择您想要检查的资产。 （如果您使用的是在本文前面创建的演示数据，选择 *AK-101*。）
1. 在操作窗格上的 **资产** 选项卡上，在 **预防** 组中，选择 **计数器** 打开资产 *AK-101* 的计数器记录页面。

### <a name="generate-maintenance-work-orders"></a>生成维护工作订单

启用 *资产维护* 场景并设置维护计划后，您可以运行维护安排来生成维护工作订单。 有关如何处理预防性维护的详细信息，请参阅[预防性维护概述](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md)。
