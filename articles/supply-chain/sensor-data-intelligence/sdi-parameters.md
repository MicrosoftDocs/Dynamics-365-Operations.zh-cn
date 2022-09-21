---
title: Sensor Data Intelligence 参数
description: 本文提供有关 Sensor Data Intelligence 参数页面可用的配置设置的信息。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428291"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence 参数

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

**Sensor Data Intelligence 参数** 页面提供了一些可用于配置此功能的设置。 这些设置包括 Azure 连接参数和用于因响应传感器度量而发送给用户的警报消息的生存期参数。

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>读取和更改 Azure IoT 解决方案的连接详细信息

通常，您将设置您的 Azure IoT 解决方案并将其从 **部署和连接 Azure 资源** 页面连接到 Microsoft Dynamics 365 Supply Chain Management，这将指导您完成这两个过程。 （有关详细信息，请参阅[在 Azure 上部署 IoT 解决方案](sdi-deploy-iot-solution-on-azure.md)。）您还可以按照以下步骤随时在 Supply Chain Management 中查看和编辑连接详细信息。

1. 转到 **系统管理 \> 设置 \> Sensor Data Intelligence \> Sensor Data Intelligence 参数**。
1. 在 **时序** 选项卡的 **Redis 指标存储连接字符串** 字段中，输入您要连接的 Azure IoT 解决方案的 **主连接字符串 (StackExchange.Redis)** 值。 有关如何查找此值的详细信息，请参阅[在 Azure 上部署 IoT 解决方案](sdi-deploy-iot-solution-on-azure.md)。
1. 在 **集成** 选项卡的 **Azure AD 应用程序客户端 ID** 字段中，输入您要连接的 Azure IoT 解决方案的 **客户端 ID** 值。 有关如何查找此值的详细信息，请参阅[在 Azure 上部署 IoT 解决方案](sdi-deploy-iot-solution-on-azure.md)。

## <a name="set-the-lifetime-of-alert-messages"></a>设置警报消息的生存期

每次 Sensor Data Intelligence 检测到需要用户注意的情况时，它都会向相关用户发送通知。 要防止这些通知在系统中堆积，您应该将它们设置为在几天后过期。

1. 转到 **系统管理 \> 设置 \> Sensor Data Intelligence \> Sensor Data Intelligence 参数**。
1. 在 **通知** 选项卡的 **通知有效天数** 字段中，输入保留通知的天数。 指定的时间过后，通知将被删除。
