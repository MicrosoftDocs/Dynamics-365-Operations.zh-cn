---
title: 在 LCS 中安装 IoT 智能加载项
description: 本文介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。
author: johanhoffmann
ms.date: 07/07/2020
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
ms.openlocfilehash: 52fe4c4a79378aca5f1e64c8b3f4fa85199c9911
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887477"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>在 LCS 中安装 IoT 智能加载项

[!include [banner](../../includes/banner.md)]

本文介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。 请注意，加载项不能安装在演示/试用环境中。 必须先[创建 Azure 资源](iot-azure-setup.md)，然后才能安装此加载项。

您可以在不编写任何代码的情况下设置和配置 IoT 智能。 以下是基本步骤。

1. [设置 Azure 资源](iot-azure-setup.md) – 创建 IoT 中心、Redis 缓存以及可从 Supply Chain Management 访问的密钥保管库。
2. [IoT 中心的消息架构格式](iot-schema-format.md) – 配置您的设备以将消息发送到 IoT 中心，并定义 JavaScript 对象表示法 (JSON) 消息格式。
3. 在“功能管理”中，启用 IoT 智能功能标志。
4. 在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项 – 在 LCS 中安装加载项并配置 Azure 密码（如本文所述）。
5. [设置指标](iot-metrics-setup.md) – 在 Supply Chain Management 中设置指标。
6. [方案设置](iot-scenario-setup.md) – 在 Supply Chain Management 中设置方案。

## <a name="set-up-the-lcs-environment"></a>设置 LCS 环境

1. 打开 LCS，然后转到您的 Microsoft Dynamics 365 Supply Chain Management环境。
2. 滚动到 **环境加载项** 部分。
3. 选择 **安装新加载项** 显示已为环境启用的加载项的列表。
4. 在 **选择要安装的加载项** 对话框中，选择 **IoT 智能**。
5. 在 **设置加载项** 对话框中，提供 IoT 中心和 Redis 缓存的详细信息。 可以在您在[创建 Azure 资源](iot-azure-setup.md)中创建的密钥保管库中找到所需值。

    + **租户 ID** – 在 Azure 门户中，转到密钥保管库，然后在左侧导航窗格中，选择 **概览**，然后复制 **目录 ID** 值。 将该值粘贴到 **设置加载项** 对话框中。
    + **IoT 事件中心兼容的终结点密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择 **概览**，然后复制 **DNS 名称** 值。 将该值粘贴到 **设置加载项** 对话框中。
    + **IoT 事件中心兼容的终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择 **密码**，然后复制其中存储 IoT 中心的事件中心连接字符串的密码的名称。 将该值粘贴到 **设置加载项** 对话框中。
    + **Redis 缓存密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择 **概览**，然后复制 **DNS 名称** 值。 将该值粘贴到 **设置加载项** 对话框中。
    + **Redis 缓存终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择 **密码**，然后复制其中存储 Redis 缓存的连接字符串的密码的名称。 将该值粘贴到 **设置加载项** 对话框中。

6. 选中复选框接受条款和条件。
7. 选择 **安装**。
8. 将显示一个消息框，内容为“已成功触发加载项安装。” 选择 **确定**。

现已完成 LCS 设置。 下一步是[设置方案](iot-scenario-setup.md)。

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>卸载加载项

1. 在 Supply Chain Management 中[禁用方案](iot-scenario-setup.md#disable-a-scenario)。
2. 在 LCS 中，转到您的 Supply Chain Management 环境详细信息。
3. 滚动到 **环境加载项** 部分。
4. 为 IoT 智能加载项选择 **卸载**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]