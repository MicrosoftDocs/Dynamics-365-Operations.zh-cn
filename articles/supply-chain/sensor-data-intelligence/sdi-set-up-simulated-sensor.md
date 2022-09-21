---
title: 设置模拟传感器以进行测试
description: 本文介绍如何设置一个模拟器，您可以使用该模拟器来测试 Sensor Data Intelligence，而无需安装任何物理传感器。
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
ms.openlocfilehash: edfa20bec7438124844f8b6afa91ca4941b6bb56
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428325"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>设置模拟传感器以进行测试

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

如果您想要在不安装任何物理传感器的情况下测试 Sensor Data Intelligence，您可以使用 *Raspberry PI Azure IoT 联机模拟器* 服务来模拟传感器信号，并将它们发送到您在 Microsoft Azure 上的物联网 (IoT) 解决方案。 有关模拟器的更多信息，请参阅[将 Raspberry Pi 联机模拟器连接到 Azure IoT 中心 (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)。

## <a name="create-a-device-in-azure-iot-hub"></a>在 Azure IoT 中心创建设备

您必须首先设置一个设备来验证发送到 Azure IoT 中心的传感器信号。

1. 在 Azure 中，转到为与 Sensor Data Intelligence 一起使用而创建的资源组的资源列表。 （有关详细信息，请参阅[在 Azure 上部署 IoT 解决方案](sdi-deploy-iot-solution-on-azure.md)。）
1. 在资源列表中，找到 **类型** 字段设置为 *IoT 中心* 的记录。 在 **名称** 列中，选择名称打开资源的详细信息页面。
1. 在左侧导航窗格中，选择 **设备**。
1. 在 **设备** 页面，选择 **添加设备**。
1. 在 **创建设备** 页面，设置以下字段：

    - **设备 ID** – 为新设备输入名称（例如，*我的 IoT 设备*）。
    - **身份验证类型** – 选择 *对称密钥*。
    - **自动生成密钥** – 选中此复选框。
    - **将此设备连接到 IoT 中心** – 选择 *启用*。

1. 选择 **保存** 返回 **设备** 页面。
1. 在列表中找到新设备。 在 **设备 ID** 列中，选择名称打开设备的详细信息页面。 如果您没有在列表中看到新设备，请刷新页面。
1. 复制 **主连接字符串** 值（例如，通过选择 **复制到剪贴板** 按钮）。 稍后在设置 Raspberry Pi IoT 模拟器来模拟传感器信号时，您将需要此值。 因此，现在考虑将它粘贴到一个文本文件中。

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>将 Azure 连接字符串添加到 Raspberry Pi IoT 模拟器

按照以下步骤将连接字符串从 Azure IoT 中心中的设备添加到 Raspberry 服务中的脚本。

1. 打开 [Raspberry Pi IoT 模拟器](https://azure-samples.github.io/raspberry-pi-web-simulator/)。
1. 在代码编辑器窗格中，找到包含以下命令的行。

    `const connectionString = '[Your IoT hub device connection string]';`

1. 将包括括号在内的帮助文本替换为您在上一节中复制的 **主连接字符串** 值。 结果应类似于以下示例。

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>将传感器 ID 和值添加到 Raspberry Pi IoT 模拟器中的有效负载

您现在必须使用模拟传感器以及它们将作为有效负载发送的值来设置 Raspberry Pi IoT 模拟器。

- 在 Raspberry Pi IoT 模拟器的代码编辑器中，找到 `getMessage` 函数，并对其进行编辑，使其与以下代码匹配。 （传感器设置在 `cb()` 行中。）

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > 在 Raspberry Pi IoT 模拟器的代码编辑器中定义的传感器 ID 必须与您稍后将为 Supply Chain Management 中的场景指定的传感器 ID 相同。 前面的示例代码使用人类可读的传感器 ID。 但是，在实际场景中，传感器 ID 将是传感器制造商提供的全局唯一标识符 (GUID) 值。 此示例代码中使用的人类可读传感器 ID 也用于[产品质量场景](sdi-scenario-product-quality.md)、[资产维护场景](sdi-scenario-asset-maintenance.md)、[生产延迟场景](sdi-scenario-production-delays.md)和[机器状态场景](sdi-scenario-equipment-downtime.md)的示例。 因此，如果您将处理这些场景，使用此代码。

## <a name="edit-the-interval-for-sending-sensor-signals"></a>编辑发送传感器信号的间隔

您现在必须设置 Raspberry Pi IoT 模拟器发送模拟传感器信号的时间间隔。

1. 在 Raspberry Pi IoT 模拟器的代码编辑器中，找到如下函数调用。

    `setInterval(sendMessage, 2000);`

2. 默认情况下，Raspberry Pi IoT 模拟器每 2,000 毫秒（两秒）发送一个传感器信号。 您可以根据需要调整此值。

## <a name="run-the-raspberry-pi-iot-simulator"></a>运行 Raspberry Pi IoT 模拟器

- 选择 **运行** 启动模拟器并开始发送模拟传感器数据。
