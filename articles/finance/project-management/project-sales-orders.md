---
title: 时间和材料项目的项目销售订单
description: 本主题介绍如何为时间和材料项目创建基于项目的销售订单。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551194"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>时间和材料项目的项目销售订单

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

此主题描述如何为项目创建销售订单。 只能为类型为**时间和材料**的项目创建销售订单。

如果时间和材料项目的项目合同中有多个融资来源，则必须启用**项目管理与核算参数**页面上的**允许项目的销售订单具有多个融资来源**参数。 

> [!NOTE]
> - 从应用程序版本 10.0.2 及更高版本开始，支持具有多个融资来源的项目销售订单。
> - 2020 年 4 月发布波次中将删除用于启用对具有多个融资来源的项目销售订单的支持的参数，之后将始终启用此功能。

可通过两种方法创建基于项目的销售订单：

- 转到项目本身。 在操作窗格上，选择**管理 > 物料任务 > 销售订单**。 项目信息默认为项目的销售订单。 如果项目合同有多个融资来源，您将需要选择融资来源才能为销售订单设置客户。 如果项目只有一个融资来源，将自动设置客户。
- 转到**所有销售订单**列表页并创建一个新的销售订单。 您将需要为销售订单选择项目。 选择项目之后，将从融资来源设置客户，而如果项目合同有多个融资来源，则您将需要选择此融资来源。

