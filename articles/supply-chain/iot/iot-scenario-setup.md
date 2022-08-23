---
title: IoT 智能的方案设置
description: 本文介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中配置 IoT 智能的方案。
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2f097f33abb55dd69d4a38a9a7b0b2e9bdfbaea1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227794"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT 智能的方案设置

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

本文介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中配置 IoT 智能的方案。 <!-- KFM: Hide setup info for now: Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md). -->

在本文中，将配置 **设备停机时间** 方案，以便在机器停机时在 Supply Chain Management 中生成通知。 本文还介绍如何配置 **产品质量** 方案，以便在物料的属性超出指定范围时生成通知，以及如何配置 **生产延迟** 方案，以便在生产吞吐量低于阈值时生成通知。

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置设备停机时间方案

**设备停机时间** 方案将 **部件停止** 信号映射到机器警报阈值。 仅当为此方案选择机器，并且在 Supply Chain Management 中将其设置为 **正在运行**，才监视此机器。 如果上次收到的机器 **部件停止** 信号以后经过的时间超过了警报阈值，将触发 **机器停机** 通知。 如果机器仍在运行，下次收到 **部件停止** 信号时，将触发 **机器开机** 通知。 如果机器停机时间达到 30 分钟，将触发新的 **机器停机** 通知。

**设备停机时间** 方案具有以下依赖性：

+ 仅当正在映射的机器上运行生产订单，才能触发警报。
+ 必须将表示映射的机器 **部件停机** 信号的型号发送到 IoT 中心，并且必须包含唯一属性名称。
+ Azure IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以毫秒 (ms) 表示。

若要配置此方案，请执行以下步骤。

1. 登录 Supply Chain Management。
2. 启用 IoT 智能功能标志。 有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。
3. 配置指标。 有关详细信息，请参阅[如何配置指标](iot-metrics-setup.md#configure-metrics)。
4. 转到 **生产控制 \> 设置 \> IoT 智能 \> 方案管理**。
6. 在 **设备停机时间** 磁贴中，选择 **配置** 打开配置向导。

   向导中的第一个页面是 **设备传感器架构定义** 页面。 在此页面中，目标是在 Supply Chain Management 中设置架构，以使其与 IoT 中心消息的 JavaScript Object Notation (JSON) 格式匹配。 可以定义多个消息架构。 有关详细信息，请参阅 [IoT 中心消息的架构格式](iot-schema-format.md)。 在此示例中，消息有效负载中包含一批采用以下格式的消息。

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

7. 向表添加一行，然后设置以下值：

    1. 将 **架构名称** 字段设置为 **ID**。
    2. 将 **架构路径** 字段设置为 **/payload\[\*\]/id**。
    3. 将 **说明** 字段设置为 **消息 ID**。

8. 向表再添加一行，然后设置以下值：

    1. 将 **架构名称** 字段设置为 **时间戳**。
    2. 将 **架构路径** 字段设置为 **/payload\[\*\]/timestamp**。
    3. 将 **说明** 字段设置为 **消息时间戳**。

9. 向表再添加一行，然后设置以下值：

    1. 将 **架构名称** 字段设置为 **值**。
    2. 将 **架构路径** 字段设置为 **/payload\[\*\]/value**。
    3. 将 **说明** 字段设置为 **消息值**。

    > [!NOTE]
    > 不必定义消息中的全部属性。 仅定义所需的属性。 在前面的步骤中，您没有为 **根时间戳** 创建行。 **根时间戳** 的路径将为 **/timestamp**。

10. 选择 **下一步** 转到 **设备传感器架构映射** 页。
11. 在 **设备资源 ID** 的行的 **架构名称** 字段中，选择 **ID**。
12. 在 **UTC 时间** 的行的 **架构名称** 字段中，选择 **时间戳**。
13. 在 **部件生成的信号** 的行的 **架构名称** 字段中，选择 **值**。
14. 选择 **下一步** 转到 **设备资源 ID 配置** 页。
15. 执行以下步骤将 IoT 中心消息中的值映射到 Supply Chain Management 资源：

    1. 在 **信号数据值** 标准，添加一个新行。 在 **值** 字段中，输入 **IoTInt.Machine1225.PartOut**。 此值来自 IoT 中心消息中的 JSON **id** 属性。
    2. 选择 **保存**。
    3. 在 **业务记录映射** 表中，选择 **新建**。 将自动填充 **业务记录类型** 字段的值，您不必更改。
    4. 在 **业务记录** 字段中，选择此信号值来自的 Supply Chain Management 机器资源。
    5. 选择 **保存**。
    6. 重复这些步骤，为 **Machine1226** 添加新业务记录映射。 可将多个信号数据值映射到 Supply Chain Management 中的一个记录。

16. 可使用 **所选** 列选择要处理的机器。 不必定义所有信号值，也不必选择所有机器。
17. 选择 **下一步** 转到 **部件生成的信号配置** 页。
18. 在 **信号数据值** 标准，添加一行，然后将 **值** 字段设置为 **True**。 此值来自 IoT 中心消息中的 JSON **值** 属性。 可以根据需要为方案添加任意数量的值。
19. 选择 **保存**。
20. 选择 **下一步** 转到 **设备停机时间阈值** 页。 列出的机器是之前映射到信号值的机器。 在此页面中，将定义阈值以确定某个机器是否已停机。 例如，如果将此阈值设置为 **10**，并且有 10 秒钟未收到机器的 **部件停机** 消息，Supply Chain Management 将生成通知。
21. 选择 **下一步** 转到 **启用方案** 页。 设置用于启用方案的选项。
22. 选择 **完成**。

方案设置现在已完成。 IoT 智能将自动开始处理 IoT 中心消息。

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置产品质量方案

如果某个物料的属性超出指定范围，**产品质量** 方案将生成通知。 例如，传感器将每个物料的重量发送到 IoT 中心。 如果物料太重或太轻，将在 Supply Chain Management 中生成通知。

**产品质量** 方案具有以下依赖性：

+ 仅当在映射的机器上运行生产订单，并生成具有映射的批处理属性生成产品时，才可以触发警报。
+ 必须将表示批处理属性的信号发送到 IoT 中心，并且必须包含唯一属性名称。
+ IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以 ms 表示。

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>在 Supply Chain Management 中配置生产延迟方案

如果生产完全降到阈值下，**生产延迟** 方案将生成通知。 在此方案中，将为生成的每个物料向 IoT 中心发送 **部件停止** 信号。 在 Supply Chain Management 中，订单延迟基于计划运行的生产订单时间量、应生成的物料数量、作业已运行的时间量和收到的 **部件停止** 信号数量计算订单延迟。 如果作业的 **部件停止** 信号数量低于阈值，将生成延迟通知。

**生产延迟** 方案具有以下依赖性：

+ 仅当正在映射的机器上运行生产订单，才能触发警报。
+ 必须将表示映射的机器 **部件停机** 信号的型号发送到 Azure IoT 中心，并且必须包含唯一属性名称。
+ IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以 ms 表示。

## <a name="disable-a-scenario"></a>禁用方案

若要禁用方案，请执行以下步骤。

1. 在 Supply Chain Management 中，转到 **生产控制 \> 设置 \> IoT 智能 \> 方案管理**。
2. 在方案的磁贴中，选择 **配置**。
3. 选择 **下一步** 转到向导的最后一页。
4. 设置用于禁用方案的选项。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]