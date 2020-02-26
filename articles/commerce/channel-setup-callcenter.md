---
title: 设置呼叫中心渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002442"
---
# <a name="set-up-a-call-center-channel"></a>设置呼叫中心渠道


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。

## <a name="overview"></a>概览

在 Dynamics 365 Commerce 中，呼叫中心是一种可在应用程序中定义的零售渠道。 为呼叫中心实体定义渠道使系统能够将特定数据和订单处理默认值绑定到销售订单。 一家公司可在 Commerce 中定义多个呼叫中心渠道。 

在创建新呼叫中心渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。

## <a name="create-and-configure-a-new-call-center-channel"></a>创建和配置新呼叫中心渠道

要创建和配置新呼叫中心渠道，请按照以下步骤操作。

1. 在导航窗格中，转到**模块 \> 渠道 \> 呼叫中心 \> 所有呼叫中心**。
1. 在操作窗格上，选择**新建**。
1. 在**名称**字段中，为新渠道提供名称。
1. 从下拉列表中选择适当的**法人**。
1. 从下拉列表中选择适当的**仓库**位置。
1. 在**默认客户**字段中，请提供有效的默认客户。
1. 在**电子邮件通知配置文件**字段中，请提供有效的电子邮件通知配置文件。
1. 提供**价格覆盖**信息代码。 请注意，您可能首先需要为此创建一个信息代码。
1. 提供一个**保留代码**信息代码。 请注意，您可能首先需要为此创建一个信息代码。
1. 提供一个**贷记**信息代码。 请注意，您可能首先需要为此创建一个信息代码。
1. 选择**保存**。

下图显示了新呼叫中心渠道的创建过程。

![新呼叫中心渠道](media/channel-setup-callcenter-1.png)

下图显示了一个呼叫中心渠道示例。

![呼叫中心渠道示例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>其他渠道设置

呼叫中心渠道设置所需的其他任务包括设置付款方式和交货方式。

下图显示了**设置**选项卡上的**交货方式**和**付款方式**设置选项。

![其他呼叫中心渠道设置操作](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>设置付款方式

要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。

1. 在操作窗格上，选择**设置**选项卡，然后选择**付款方式**。
1. 在操作窗格上，选择**新建**。
1. 在导航窗格中，选择所需的付款方式。
1. 在**常规**部分，提供**操作名称**并配置任何其他所需的设置。
1. 根据付款类型的要求配置任何其他设置。
1. 在操作窗格上，选择**保存**。

下图显示了现金支付方式的示例。

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>设置交货方式

您可以从**操作窗格**上的**设置**选项卡中选择**交货方式**来查看已配置的交货方式。  

要更改或添加交货方式，请按照下列步骤操作。

1. 在导航窗格中，转到**模块 \> 库存管理 \> 交货方式**。
1. 在操作窗格上，选择**新增**以创建新的交货方式，或选择现有方式。
1. 在**零售渠道**部分，选择**添加行**以添加渠道。 使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。

下图显示了交货方式的示例。

![设置交货方式](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>其他资源

[渠道设置先决条件](channels-prerequisites.md)

[呼叫中心销售功能](call-center-functionality.md)

[设置呼叫中心订单处理选项](set-up-order-processing-options.md)

[呼叫中心目录](call-center-catalogs.md)

[设置和使用欺诈预警](set-up-fraud-alerts.md)

[设置呼叫中心的连续性计划](set-up-continuity-program.md)
