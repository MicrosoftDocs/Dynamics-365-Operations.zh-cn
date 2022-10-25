---
title: Sensor Data Intelligence 主页
description: 本文提供 Sensor Data Intelligence 的概览。 基于来自生产车间机器和设备的物联网 (IoT) 信号，组织可以使用此功能来推动 Microsoft Dynamics 365 Supply Chain Management 中的业务流程。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689849"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence 主页

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

基于来自生产车间机器和设备的物联网 (IoT) 信号，Microsoft Dynamics 365 Supply Chain Management 的Sensor Data Intelligence 让组织能够推动 Supply Chain Management 中的业务流程。 它是以前可用于 Supply Chain Management 的 *IoT 智能* 功能的更新的重命名版本。

Sensor Data Intelligence 让您可以执行以下任务：

- 收集机器和设备的详细信息，来更新 Supply Chain Management 中的维护资产计数器值并推动预测性维护。
- 使用简单的注册向导设置解决方案，而不是在 Microsoft Dynamics Lifecycle Services (LCS) 中手动安装和配置组件。
- 在您自己的订阅上部署组件，以便您更灵活地管理 Azure 组件。
- 将解决方案配置为在 Azure 组件上运行的业务逻辑，并进行扩展。 这些组件现在通过您自己的订阅进行管理。 因此，您可以根据需要自定义它们来满足您的特殊业务需求。

## <a name="business-scenarios"></a>业务场景

Sensor Data Intelligence 支持多种类型的功能，每一种功能由系统中的特定 *场景* 表示。 每个场景在系统中提供一组专门的配置选项，下表提供了详细介绍。

| 应用场景 | Description |
|---|---|
| [资产停机](sdi-scenario-asset-downtime.md) | 通过使用传感器数据跟踪机器停机时间，准确跟踪机器资产的效率。 |
| [资产维护](sdi-scenario-asset-maintenance.md) | 通过根据机器资产关键控制点的传感器读数改进维护计划，来最大限度地降低维护成本和延长资产寿命。 |
| [计算机状态](sdi-scenario-equipment-downtime.md) | 通过使用传感器读数通知计划人员机器停机并提供减少潜在延迟的选项来确保运营效率。 |
| [产品质量](sdi-scenario-product-quality.md) | 通过比较每个产品批次的实际属性（如湿度、温度或自定义质量指标）的传感器读数来确保产品批次的质量。 当出现偏差时，系统会通知用户。 |
| [生产延迟](sdi-scenario-production-delays.md) | 使用传感器读数将实际周期时间与计划周期时间进行比较，在生产未按计划进行时通知主管。 然后，主管可以根据需要进行干预，以确保最大的运营效率。 |

## <a name="architecture"></a>体系结构

以下体系结构图提供了解决方案及其组件的概览。

![Sensor Data Intelligence 体系结构图。](media/sdi-architecture.png "Sensor Data Intelligence 体系结构图")
