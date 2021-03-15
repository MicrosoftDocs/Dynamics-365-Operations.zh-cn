---
title: 在 LCS 中安装 IoT 智能加载项
description: 此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d55ca1975589699cbce03dcc7bf81e0762738d24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963477"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>在 LCS 中安装 IoT 智能加载项

[!include [banner](../../includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。 请注意，加载项不能安装在演示/试用环境中。 必须先[创建 Azure 资源](iot-azure-setup.md)，然后才能安装此加载项。

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