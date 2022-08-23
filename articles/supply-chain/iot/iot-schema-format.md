---
title: IoT 中心消息的架构格式
description: 本文介绍您应如何设计可在 IoT 智能中使用的消息架构。
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228623"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT 中心消息的架构格式

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

本文介绍您应如何设计可在 IoT 智能中使用的消息架构。

## <a name="message-requirements"></a>消息要求

以下规则适用于 IoT 智能中消息的监视：

+ 消息架构必须采用 JavaScript 对象表示法 (JSON) 格式。
+ Microsoft Azure IoT 中心消息中必须包含 UNIX **timestamp** 属性，其中值以毫秒 (ms) 表示。
+ 仅当消息包含在方案设置中定义的所有属性时，才会跟踪该消息。 例如，如果您定义 **id**、**timestamp** 和 **value** 属性，将会监视以下消息。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    未监视此消息，因为缺少 **value** 属性。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT 智能会忽略未在方案配置中定义的消息中的属性。 例如，如果您定义 **id**、**timestamp** 和 **value** 属性，IoT 智能将会监视以下所有消息。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT 智能会以静默方式忽略与方案配置条件不匹配的消息。
+ 您可以定义和使用多种类型的消息架构。
+ 并非所有类型的消息架构都必须定义。 只有将用于 IoT 智能方案的架构必须定义。

## <a name="id-value-pair-schema"></a>Id-value 对架构

id-value 对是 IoT 智能消息架构的常见模式。 使用 id-value 对，可以确保所有方案中的消息架构相同。 例如，以下是 **设备停机时间** 或 **生产延迟** 方案的消息。

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

以下是 **产品质量** 方案的消息。

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

之前的两条消息都包含 **id** 和 **value** 属性。 **id** 值可以在方案设置期间映射到 **信号数据值** 表中。 对于 **设备停机时间** 方案，您将映射 **IoTInt.Machine1225.PartOut** 值。 对于 **产品质量** 方案，您将映射 **IoTInt.Machine1225.Temperature** 值。

有关详细信息，请参阅 [Azure IoT 中心文档](/azure/iot-hub/)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]