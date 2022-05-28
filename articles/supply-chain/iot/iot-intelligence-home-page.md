---
title: IoT 智能主页
description: 本主题提供有关 IoT 智能的信息的链接。
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674412"
---
# <a name="iot-intelligence-home-page"></a>IoT 智能主页

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> 此功能目前只在以下国家/地区提供：
>
> - US（美利坚合众国）
> - EU（欧盟）
> - AU（澳大利亚）
> - CA（加拿大）
> - UK（英国）

IoT 智能是 Microsoft Dynamics 365 Supply Chain Management 一个的加载项。 它将物联网 (IoT) 信号与 Supply Chain Management 中的数据集成，以生成可操作的见解。

IoT 智能支持以下方案：

- **生产延迟** – 此方案将实际周期时间与计划周期时间进行比较。 当生产未按计划进行时，Supply Chain Management 会通知您，以便您可以进行干预以最大化运营效率，避免订单延迟。
- **设备停机时间** – 此方案将度量的运行时间与用户定义的参数进行比较。 超过中断阈值时，Supply Chain Management 会通知您，以便您可以采取诸如重新计划生产工作订单或创建维护工作订单等行动。
- **产品质量** – 此方案将传感器读数（如湿度和温度）与用户定义的质量指标进行比较。 发生偏差时，Supply Chain Management 会通知您，以便您可以进行干预以维护质量标准，尽量减少废品。

下图显示了 Azure IoT 中心、IoT 智能和 Supply Chain Management 的交互。

![IoT 中心、IoT 智能和 Supply Chain Management。](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>跟踪和维护

- [在 Dynamics 365 Supply Chain Management 中监视方案](iot-management.md#monitor-scenarios)
- [禁用方案](iot-scenario-setup.md#disable-a-scenario)
- [修改正在运行的 IoT 智能方案](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [模拟选项](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]