---
title: 在 POS 的装运选项中隐藏非承运人交货方式
description: 本主题介绍一个配置选项，当在销售点 (POS) 应用程序中创建装运订单时，该配置选项可以防止选择中出现非承运人交货方式。
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982981"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>在 POS 的装运选项中隐藏非承运人交货方式


[!include [banner](includes/banner.md)]

本主题介绍可用于销售点 (POS) 应用程序的配置选项。 此配置选项更改了在 POS 中创建装运订单时，选择交货方式的行为。

用户在 POS 中创建客户装运订单时，他们可以选择装运的交货方式。 无论是装运整个订单还是仅选定的行，此功能都可用。

默认情况下，选择了交货方式的对话框将显示渠道、物料和交货地址的组合的所有有效交货方式。 这些交货方式在 Headquarters 的**交货方式**页面上定义（**销售和市场 \> 设置 \> 配送 \> 交货方式**）。 对话框中还会出现供选择的“非承运人”交货方式，如 **Carryout** 或 **Pickup**。

但是，已增加了一项功能，使您可以在对话框中隐藏非承运人交货方式。 要启用此功能，请在 **Commerce 参数**页面上的**客户订单**选项卡上，将**仅显示装运订单的承运人模式选项**选项设置为**是**。 启用此功能并运行适当的配送作业以将信息同步到渠道数据库后，在 POS 中创建装运订单的流程中将不会出现供选择的非承运人交货方式。
