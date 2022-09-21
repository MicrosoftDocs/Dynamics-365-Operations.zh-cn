---
title: 在 Azure 上部署 IoT 解决方案
description: Sensor Data Intelligence 使用来自连接到 Microsoft Azure 的传感器的数据。 本文介绍如何在 Azure 订阅上部署物联网 (IoT) 解决方案。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428331"
---
# <a name="deploy-an-iot-solution-on-azure"></a>在 Azure 上部署 IoT 解决方案

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence 使用来自连接到 Microsoft Azure 的传感器的数据。 要使 Azure 能够从您的传感器中检索数据并与 Dynamics 365 Supply Chain Management 共享，您必须在您的 Azure 订阅上部署物联网 (IoT) 解决方案。 以下体系结构图提供了解决方案及其组件的概览。

![Sensor Data Intelligence 体系结构图。](media/sdi-architecture.png "Sensor Data Intelligence 体系结构图")

按照以下步骤在 Azure 上部署所需资源。

1. 以管理员身份登录到 Supply Chain Management 环境
1. 转到 **系统管理 \> 设置 \> Sensor Data Intelligence \> 部署和连接Azure 资源** 打开部署向导。
1. 在 **欢迎** 页面上，阅读信息，然后选择 **下一步**。
1. 在 **将示例 IoT 解决方案部署到 Azure** 页面上，阅读信息，然后在 **说明** 部分中，选择 **部署**。
1. 一个新的浏览器选项卡将打开，您将转到 Azure 门户，可以在那里部署 Azure 资源。 如果系统提示，使用您的 Azure 订阅的凭据登录。
1. 在 **自定义部署** 页面，在 **订阅** 字段中，选择您的订阅。
1. 在 **资源组** 字段下，选择 **新建** 为要部署的 Azure 组件创建资源组。
1. 在出现的下拉对话框中，在 **名称** 字段中，为新资源组输入名称（例如，*IoT-demo*）。 然后选择 **确定**。
1. 设置以下字段：

    - **资源组** – 选择您刚才创建的资源组。
    - **区域** – 选择一个区域，最好是部署 Supply Chain Management 环境的区域。 请记住，各 Azure 区域有不同的定价。 您可以使用 [Sensor Data Intelligence 价格计算器](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68)查看您所在区域的估计成本。
    - **Supply Chain Management 环境 URL** – 输入您的 Supply Chain Management 环境的 URL。
    - **重用现有的 Azure IoT 中心** – 保持清除此复选框。

1. 选择 **下一步：查看 + 创建**。
1. 在 **自定义部署** 页面，确认验证已通过，然后选择 **创建**。
1. **正在部署** 页面将跟踪您的部署进度。 部署过程最多可能需要 30 分钟。 当 **正在部署** 页面指示部署已完成时，选择资源组名称的链接打开显示组中部署的资源列表的页面。
1. 在资源列表中，找到 **类型** 字段设置为 *托管标识* 的记录。 在 **名称** 列中，选择名称打开资源的详细信息页面。
1. 复制 **客户端 ID** 字段中的值（例如，通过选择 **复制到剪贴板** 按钮）。
1. 返回到 Supply Chain Management 运行的浏览器选项卡，*但不要关闭 Azure 门户的选项卡*。 **将示例 IoT 解决方案部署到 Azure** 向导页面应该仍是打开的。 
1. 选择 **下一步**。
1. 在 **连接 Azure 资源** 页面的 **Azure AD 应用程序客户端 ID** 字段中，粘贴您复制的 **客户端 ID** 值。
1. 返回到 Azure 门户打开的浏览器选项卡，*但不要关闭 Supply Chain Management 的选项卡*。 资源的详细信息页面应该仍是打开的。
1. 选择浏览器的 **返回** 按钮返回到新资源组中的资源列表。
1. 在资源列表中，找到 **类型** 字段设置为 *Azure Cache for Redis* 的记录。 在 **名称** 列中，选择名称打开资源的详细信息页面。
1. 在左侧导航窗格中，选择 **访问密钥**。
1. 在 **访问密钥** 页面上，复制为 **主连接字符串 (StackExchange.Redis)** 显示的值（例如，通过选择 **复制到剪贴板** 按钮）。
1. 返回到 Supply Chain Management 运行的浏览器选项卡。 **连接 Azure 资源** 页面应该仍是打开的。
1. 在 **Redis 指标存储连接字符串** 字段中，粘贴您复制的 **主连接字符串 (StackExchange.Redis)** 值。
1. 选择 **完成**。

Sensor Data Intelligence 的 Azure 资源现在已部署在你的 Azure 订阅上。

> [!NOTE]
> 您可以打开 **Sensor Data Intelligence 参数** 页面随时查看或编辑保存 Supply Chain Management 中保存的连接信息。 有关详细信息，请参阅 [Sensor Data Intelligence 参数](sdi-parameters.md)。
