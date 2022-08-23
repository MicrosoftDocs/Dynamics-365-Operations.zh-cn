---
title: 创建在线功能配置文件
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建在线功能配置文件。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276793"
---
# <a name="create-an-online-functionality-profile"></a>创建在线功能配置文件

[!include [banner](includes/banner.md)]

本文概述为 Microsoft Dynamics 365 Commerce 设置在线功能配置文件的过程。

在线功能配置文件提供了用于在线渠道的各种设置。 每个在线渠道必须指定一个在线功能配置文件。

## <a name="create-an-online-functionality-profile"></a>创建在线功能配置文件

以下过程说明了如何从 Commerce Headquarters 应用创建在线功能配置文件。

1. 在导航窗格中，转到 **模块 \> 渠道设置 \> 在线商店设置 \> 功能配置文件**。
1. 在操作窗格上，选择 **新建**。
1. 在 **配置文件** 字段中，为配置文件输入 ID。
1. 在 **描述** 字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。
1. 在 **功能** 部分，根据需要修改 **购物车**、**零售客户** 或 **结帐** 设置。
1. 在操作窗格上，选择 **保存**。

下图显示了一个在线功能配置文件示例。
  
![在线功能配置文件示例。](media/online-functionality-profile.png)

## <a name="functions"></a>功能

- **聚合产品**：启用后，此功能允许购物车在多次添加同一商品时更新数量。
- **允许不付款结帐**：启用后，此功能可以处理添加到购物车中的商品价格为 0.00 美元的情况。
- **在异步模式下创建客户**：这是适用于第三方电子商务渠道的旧设置，不适用于 Dynamics 365 电子商务站点。

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[设置在线渠道](channel-setup-online.md)

[设置零售渠道](channel-setup-retail.md)

[设置呼叫中心渠道](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
