---
title: IoT 智能的方案设置
description: 此主题介绍如何在 Supply Chain Management 中为 IoT 智能创建方案。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597160"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT 智能的方案设置

[!include [banner](../../includes/banner.md)]

此主题介绍如何在 Supply Chain Management 中为 IoT 智能创建方案。 首先必须[设置 LCS](iot-lcs-setup.md)，才能设置此类方案。

在此主题中，将配置**设备停机时间**方案，以便在机器停机时在 Supply Chain Management 中生成通知。

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置**设备停机时间**方案

**设备停机时间**方案将部件停止信号映射到机器警报阈值。 仅当为此方案选择机器，并且在 Supply Chain Management 中将其设置为正在运行，才监视此机器。 如果机器上次收到部件停止信号以后经过的时间超过了警报阈值，将触发**机器停机**通知。 如果机器仍在运行，下次收到**部件停止**信号时，将触发**机器开机**通知。 如果机器停机时间达到 30 分钟，将触发新的**机器停机**通知。

**设备停机时间**方案具有以下依赖性：

+ 必须正在映射的机器上运行生产订单，才能触发警报。
+ 必须将表示映射的机器部件停机信号的型号发送到具有唯一属性名称的 IoT 中心。
+ IoT 中心消息中必须包含 Unix 毫秒时间戳属性。

若要配置此方案，请执行以下步骤：

1. 登录 Supply Chain Management。
2. 启用 IoT 智能功能标志。 有关更多信息，请参见[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。
3. 配置指标。 有关详细信息，请参阅[如何配置指标](iot-metrics-setup.md#configure-metrics)。
4. 导航到**生产控制**。
5. 导航到**设置 \> IoT 智能 \> 方案管理**。
6. 请单击**设备停机时间**磁贴中的**配置**。 将启动配置向导并显示**设备传感器架构定义**页。 此处的目标是在 Supply Chain Management 中设置架构以匹配 IoT 消息的 JSON 格式。 可以定义多个消息架构。 有关详细信息，请参阅 [IoT 中心的消息架构格式](iot-schema-format.md)。 在此示例中，消息有效负载中包含一批以下格式的消息：

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. 在表中添加一行。

    1. 将**架构名称**设置为 **ID**。
    2. 将**架构路径**设置为 **/payload[\*]/id**。
    3. 将**说明**设置为**消息 ID**。

8. 在表中添加一行。

    1. 将**架构名称**设置为**时间戳**。
    2. 将**架构路径**设置为 **/payload[\*]/timestamp**。
    3. 将**说明**设置为**消息时间戳**。

9. 在表中添加一行。

    1. 将**架构名称**设置为**值**。
    2. 将**架构路径**设置为 **/payload[\*]/value**。
    3. 将**说明**设置为**消息值**。

    无需在消息中定义所有属性，只需要定义需要的属性。 在此示例中，没有为**根时间戳**定义行。 **根时间戳**的路径将为 **/timestamp**。
  
10. 单击**下一步**转到**设备传感器架构映射**页。
11. 在**设备资源 ID** 的行中，将**架构名称**设置为 **ID**。 将在下拉表中显示有效值。
12. 在 **UTC 时间**的行中，将**架构名称**设置为**时间戳**。 将在下拉表中显示有效值。
13. 在**部件生成的信号** 的行中，将**架构名称**设置为**值**。 将在下拉表中显示有效值。
14. 单击**下一步**转到**设备资源 ID 配置**页。
15. 在此步骤中，将把 IoT 中心消息值映射到 Supply Chain Management 资源。

    1. 在**信号数据值**标准，添加一个新行，然后在**值**列中输入 **IoTInt.Machine1225.PartOut**。 值 **IoTInt.Machine1225.PartOut** 来自 IoT 中心消息中的 JSON **id** 属性。
    2. 单击**保存**。
    3. 在**业务记录映射**表中，单击**新建**。 将自动填充**业务记录类型**的值，您无需更改。
    4. 在**业务记录**列中，选择此信号值来自的 Supple Chain Management 机器资源。
    5. 单击**保存**。
    6. 重复这些步骤，并为 **Machine1226** 添加新业务记录映射。 可将多个信号数据值映射到 Supply Chain Management 中的一个记录。

16. 可使用**所选**列选择要处理哪些机器。 不必定义所有信号值，也不必选择所有机器。
17. 单击**下一步**转到**部件生成的信号配置**页。
18. 在**信号数据值**标准，添加一行，然后将**值**设置为 **True**。 值 **True** 来自 IoT 中心消息中的 JSON **value** 属性。 可以根据需要为方案添加任意数量的值。
19. 单击**保存**。
20. 单击**下一步**转到**设备停机时间阈值**页。 列出的机器是之前映射到信号值的机器。 在此步骤中，将定义阈值以确定某个机器是否已停机。 例如，如果将此阈值设置为 10，并且机器有 10 秒钟无部件停机消息，Supply Chain Management 将生成通知。
21. 单击**下一步**转到**启用方案**页。 切换滑块以启用方案。
22. 单击**完成**。

方案设置完成。 IoT 智能将自动开始处理 IoT 中心消息。

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置**产品质量**方案

如果某个物料的属性超出指定范围，**产品质量**方案将生成通知。 例如，传感器可以将每个物料的重量发送到 IoT 中心。 如果物料太重或太轻，将在 Supply Chain Management 中生成通知。

该方案具有以下依赖性：

+ 必须在映射的机器上运行生产订单，并使用映射的批处理属性生成产品以触发警报。
+ 必须将表示批处理属性的信号发送到具有唯一属性名称的 IoT 中心。
+ IoT 中心消息中必须包含 Unix 毫秒时间戳属性。

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置**生产延迟**方案

如果生产完全降到阈值下，**生产延迟**方案将生成通知。 在此方案中，将为生成的每个物料向 IoT 中心发送**部件停止**信号。 在 Supply Chain Management 中，将根据安排的生产订单运行时长，应该生成的物料数量，以及接收多少**部件停止**信号计算订单延迟。 如果作业的**部件停止**信号数量低于预期值的阈值，将生成延迟通知。

该方案具有以下依赖性：

+ 必须正在映射的机器上运行生产订单，才能触发警报。
+ 必须将表示映射的机器部件停机信号的型号发送到具有唯一属性名称的 IoT 中心。
+ IoT 中心消息中必须包含 Unix 毫秒时间戳属性。

## <a name="how-to-disable-a-scenario"></a>如何禁用方案

若要禁用方案，请执行以下步骤：

1. 在 Supply Chain Management 中，导航到**生产控制 \> 设置 \> IoT 智能 \> 方案管理**。
2. 在方案中单击**配置**。
3. 单击**下一步**转到上一个向导选项卡。
4. 切换滑块以禁用方案。
