---
title: IoT 智能主页
description: 本主题提供有关 IoT 智能的信息的链接。
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782673"
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

+ **生产延迟** – 此方案将实际周期时间与计划周期时间进行比较。 当生产未按计划进行时，Supply Chain Management 会通知您，以便您可以进行干预以最大化运营效率，避免订单延迟。
+ **设备停机时间** – 此方案将度量的运行时间与用户定义的参数进行比较。 超过中断阈值时，Supply Chain Management 会通知您，以便您可以采取诸如重新计划生产工作订单或创建维护工作订单等行动。
+ **产品质量** – 此方案将传感器读数（如湿度和温度）与用户定义的质量指标进行比较。 发生偏差时，Supply Chain Management 会通知您，以便您可以进行干预以维护质量标准，尽量减少废品。

下图显示了 Azure IoT 中心、IoT 智能和 Supply Chain Management 的交互。

![IoT 中心、IoT 智能和 Supply Chain Management。](media/iot_intelligence.png)

## <a name="setup"></a>设置

您可以在不编写任何代码的情况下设置和配置 IoT 智能。 以下是基本步骤。

1. [设置 Azure 资源](iot-azure-setup.md) – 创建 IoT 中心、Redis 缓存以及可从 Supply Chain Management 访问的密钥保管库。
2. [IoT 中心的消息架构格式](iot-schema-format.md) – 配置您的设备以将消息发送到 IoT 中心，并定义 JavaScript 对象表示法 (JSON) 消息格式。
3. 在“功能管理”中，启用 IoT 智能功能标志。 
4. [在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项](iot-lcs-setup.md) – 在 LCS 中安装加载项并配置 Azure 密码。
5. [设置指标](iot-metrics-setup.md) – 在 Supply Chain Management 中设置指标。
6. [方案设置](iot-scenario-setup.md) – 在 Supply Chain Management 中设置方案。

## <a name="tracking-and-maintenance"></a>跟踪和维护

+ [在 Dynamics 365 Supply Chain Management 中监视方案](iot-management.md#monitor-scenarios)
+ [禁用方案](iot-scenario-setup.md#disable-a-scenario)
+ [卸载加载项](iot-lcs-setup.md#uninstall-addin)
+ [修改正在运行的 IoT 智能方案](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [模拟选项](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]