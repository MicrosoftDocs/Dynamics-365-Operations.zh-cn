---
title: "POS 脱机功能"
description: "本文提供有关 Retail Modern POS 的脱机模式的信息，POS 设备在其中从渠道数据库自动切换到脱机数据库（如果零售服务器不可用）。 本文还包括脱机模式的一般设置信息并说明脱机数据库和渠道数据库之间的数据同步。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS 脱机功能

本文提供有关 Retail Modern POS 的脱机模式的信息，POS 设备在其中从渠道数据库自动切换到脱机数据库（如果零售服务器不可用）。 本文还包括脱机模式的一般设置信息并说明脱机数据库和渠道数据库之间的数据同步。

<a name="overview"></a>概览
--------

在 Retail Modern POS，销售终端 (POS) 设备脱机输入模式，每当零售服务器不可用。 因此，具有，如果 Retail Server 的连接失去，到脱机数据库中零售自动 Modern POS 切换。 销售交易记录期间，如果数据请求在脱机配置文件中配置的超时间隔内未成功，则 Retail Modern POS 会自动切换到脱机数据库并继续销售交易记录。 当 POS 设备处于脱机模式时，Retail Modern POS 会在脱机配置文件中配置的重新连接尝试间隔后尝试重新连接到零售服务器。 此重新连接尝试仅在交易记录开始时发生。

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>确定 Retail Modern POS 的连接模式

Retail Modern POS 中的状态标头指示当前连接状态，**“连接状态”**窗口显示上次尝试与脱机数据库同步的状态。 [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>创建用于手动切换联机模式和脱机模式的按钮

您可以向 Retail Modern POS 添加一个按钮来手动切换联机模式和脱机模式。 创建用于 POS 操作**“917 – 数据库连接状态”**的按钮。 当 Retail Modern POS 已连接到零售服务器时，此按钮的名称为**“断开连接”**；当断开连接时，此按钮的名称为**“连接”**。 使用此按钮，可以查看连接，也可断开与零售服务器的连接或连接到零售服务器。 [![在 Retail Modern POS 的拆接键] (。/media/details-1024x537.png)](。/media/details.png)

## <a name="setup"></a>设置
若要支持 POS 的设备 (登记) 脱机支持，请设置**脱机的支持选项** **是** **在登记**页。 新通道数据库实体创建和添加到商店的通道数据组。 然后，运行所有必需的分配计划以生成脱机数据库的数据包。 接下来，安装 Retail Modern POS 脱机版本。 设置过程创建脱机数据库。 此外，如果需要，请安装快的 Microsoft SQL Server 2014。 脱机数据同步将在首次登录 Retail Modern POS 后启动。

## <a name="data-synchronization"></a>数据同步
零售调度用于将主数据发送到脱机数据库。 默认情况下，当运行分配计划时，数据更改将发送到渠道数据库和脱机数据库。 Retail Modern POS 包含异步同步库，该库下载任何可用的数据包并将这些数据包插入脱机数据库中。 如果脱机创建任何交易记录，则 Retail Modern POS 会将这些记录上载到零售服务器，以便将它们插入渠道数据库中。 脱机数据同步只能在 Retail Modern POS 正在运行时发生。 [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


