---
title: 监视和管理 IoT 智能
description: 本主题说明如何监视和管理 IoT 智能。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423249"
---
# <a name="monitor-and-manage-iot-intelligence"></a>监视和管理 IoT 智能

[!include [banner](../../includes/banner.md)]

本主题说明如何监视和管理 IoT 智能。

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>在Microsoft Dynamics 365 Supply Chain Management 中监视方案

可以从多个位置监视 IoT 智能处理：

+ **模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 通知** – 查看未解决通知列表。
+ **模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 已关闭通知** – 查看已解决或隐藏通知列表。
+ **模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 指标键** – 查看 **资源状态** 时间系列图表的指标键。
+ **模块 \> 生产控制 \> 制造执行 \> 资源状态** – 使用 **配置** 对话框跟踪特定度量。 如果方案检测到异常，通知将显示该异常的详细信息。
+ **工作区 \> 生产车间管理 \> 通知** – 查看未解决通知列表。

## <a name="modify-a-running-iot-intelligence-scenario"></a>修改正在运行的 IoT 智能方案

运行方案时，可以进行以下更改：

+ 添加新传感器架构定义。
+ 选择新信号数据值。
+ 取消选择现有信号数据值。
+ 添加和映射新信号数据值。
+ 更新阈值。

运行方案时，不能进行以下更改：

+ 删除或修改已启用方案当前使用的任何架构定义。
+ 更改所启用方案的所选架构路径。

## <a name="simulation-options"></a>模拟选项

您可以模拟工厂机器信号。 有关详细信息，请参阅以下主题：

+ [将 IoT DevKit AZ3166 连接到 Azure IoT 中心](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [将 Raspberry Pi 联机模拟器连接到 Azure IoT 中心 (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [设备模拟解决方案加速器概述](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]