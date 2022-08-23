---
title: 设置 IoT 智能的指标
description: 本文说明如何设置 IoT 智能的指标。
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
ms.openlocfilehash: fddfee837761a4f23b42257424582a3c76c3d493
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228318"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>设置 IoT 智能的指标

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

## <a name="configure-metrics"></a>配置指标

如果要在 Microsoft Dynamics 365 Supply Chain Management 中查看消息的时序图表，必须按照以下步骤设置指标。

1. 复制 Redis 缓存的连接字符串：

    1. 在 Azure 门户中，转到 Redis 缓存。
    2. 转到 **设置** \> **访问密钥**。
    3. 复制 **主连接字符串** 字段中的值。

2. 在 Supply Chain Management 中，转到 **生产控制 \> 设置 \> IoT 智能 \> 方案参数**。
3. 在 **方案参数** 页面上，在 **时序** 选项卡上，在 **Redis 指标存储连接字符串** 字段中，粘贴之前复制的连接字符串。 此步骤将在 Supply Chain Management 中显示 Azure IoT 中心的指标。 将值粘贴到字段中时，值将显示 **\*\*\*\*\*\***。

    > [!NOTE]
    > 每当您更新 Redis 缓存连接字符串时，还必须更新此字段。

4. 转到 **生产控制 \> 查询和报表 \> IoT 智能 \> 指标键**。
5. 在 **指标键** 页面上，选择 **更新**。
6. 在 **更新指标键** 对话框中，注意字段中选择了 **在后台运行**。 选择 **确定**。

Redis 缓存中的所有指标键将被检索并添加到 **指标键** 列表中。 在您[启用方案](iot-scenario-setup.md)之前，不会显示指标值。

## <a name="configure-the-resource-status-time-series"></a>配置资源状态时序

要配置 **资源状态** 时序，请按照这些步骤操作。

1. 在 Supply Chain Management 中，转到 **生产控制 \> 制造执行 \> 资源状态**。
2. 在 **资源状态** 页上，选择 **配置**。
2. 在 **配置** 对话框中，在 **资源** 列表中，选择要监视的项。
3. 选择 **时序 1** 的 **编辑** 按钮。
4. 在 **选择时序** 对话框中，在网格中选择一个指标。 （您也可以使用 **更新指标键** 链接从此对话框更新指标键。）
5. 选择 **确定** 返回 **配置** 对话框。
6. 输入显示名称。
7. 在 **显示数据来源** 字段中，选择一个期限。
8. 选择 **确定**。

图表将显示。

## <a name="delete-a-metric-key"></a>删除指标键

1. 在 Supply Chain Management 中，转到 **生产控制 \> 查询和报表 \> IoT 智能 \> 指标键**。
2. 在 **指标键** 页面上，选择要删除的指标键。
3. 选择 **删除**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]