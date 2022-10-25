---
title: 资产停机时间场景
description: 本文介绍资产停机时间场景，它允许您使用传感器数据来监视资产的可用性。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689421"
---
# <a name="the-asset-downtime-scenario"></a>资产停机时间场景

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

如果在收到最后一个信号后的定义时间阈值内没有从机器接收到信号，资产停机时间场景会生成维护停机时间记录。 此场景需要您为机器安装一个传感器，以在机器运行时定期向您的 Azure IoT 中心发送信号，但在机器不运行时不发送信号。

## <a name="set-up-the-asset-downtime-scenario"></a>设置资产停机时间场景

按照以下步骤在 Supply Chain Management 中设置 *资产停机时间* 场景。

1. 转到 **资产管理 \> 设置 \> Sensor Data Intelligence \> 场景** 打开 **场景** 页面。
2. 在 **资产停机时间** 场景框中，选择 **配置** 打开此场景的设置向导。
3. 在 **传感器** 页面，选择 **新增** 将传感器添加到网格中。 然后为新传感器设置以下字段：

    - **传感器 ID** – 输入您正在使用的传感器的 ID。 （如果您使用的是 Raspberry PI Azure IoT 联机模拟器并已按照 [设置模拟传感器以进行测试](sdi-set-up-simulated-sensor.md)中所述进行设置，输入 *AssetDownTime*。）
    - **传感器描述** – 输入传感器的描述。

4. 对您现在要添加的每个其他传感器重复上一个步骤。 您可以随时返回添加更多传感器。
5. 选择 **下一步**。
6. 在 **业务记录映射** 页面的 **传感器** 部分，选择您刚才添加的其中一个传感器的记录。
7. 在 **业务记录映射** 部分，选择 **新建** 在网格中添加一行。
8. 在新行上，将 **业务记录** 字段设置为您使用所选传感器监视的资源。 （如果您使用的是演示数据，选择 *AK-101，行 1 气刀*。）
9. 选择 **下一步**。
10. 在 **资产停机时间阈值** 页面，定义系统在最后一个信号出现后到发送资产停机通知之前应等待的时间。 定义此阈值的方法有两种：

    - **默认阈值（分钟）** – 设置此字段可定义默认阈值。 此值适用于 **通知阈值（分钟）** 字段设置为两分钟或以下的所有资源。 最小值为 *2*（分钟）。
    - **用于确定机器未响应的阈值（分钟）** – 对于网格中不想使用默认阈值的每个资源，在此字段中输入替代值。 设置为使用两分钟或以下阈值的资源将改为使用 **默认阈值（分钟）** 设置。
11. 选择 **下一步**。
12. 在 **激活传感器** 页面的网格中，选择您设置的传感器，然后选择 **激活**。 对于网格中每个激活的传感器，**可用** 列中会出现一个复选标记。
13. 选择 **完成**。

## <a name="work-with-the-asset-downtime-scenario"></a>处理资产停机时间场景

如果在场景配置中定义的阈值内没有从资产接收到传感器信号，系统将为该资产创建维护停机时间记录。 经理应定期检查停机时间记录（例如，每个工作班次期间检查一次），并为每个停机时间登记应用适当的原因代码和结束时间。 按照以下步骤查看资产的维护停机时间记录：

1. 转到 **资产管理 > 资产 > 所有资产**。
2. 查找并选择您想要检查的资产。 （如果您使用的是演示数据，选择 *AK-101*。）
3. 在操作窗格上，打开 **资产** 选项卡，然后从 **工作订单** 组，选择 **维护停机时间** 打开所选资产的维护停机时间记录页面。
