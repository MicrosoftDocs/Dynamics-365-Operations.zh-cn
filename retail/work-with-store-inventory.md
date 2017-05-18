---
title: "管理商店库存"
description: "本文描述可用于管理库存的文档类型。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 37f9cb7d8118c3aa4cf287a8b7ed2dc9270acb52
ms.contentlocale: zh-cn
ms.lasthandoff: 04/26/2017


---

# <a name="manage-store-inventory"></a>管理商店库存

[!include[banner](includes/banner.md)]


本文描述可用于管理库存的文档类型。

您可以使用以下文档的类型管理您的组织的库存。

## <a name="purchase-orders"></a>采购订单
采购订单在总部创建。 如果零售仓库包括在采购订单头中，通过使用 Microsoft Dynamics 365 for Operations - Retail 中的 Modern POS (MPOS) 或 Cloud POS 订货可以在商店接收。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店接收的数量将显示在 Dynamics 365 for Operations 中的采购订单的**当前接收量**字段中。

## <a name="transfer-orders"></a>转移单
转移单可指定特定商店为可用于装运物料的位置。 在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 内的拣货请求。 在请求的领料数量后，它们承诺和发送总部。 在总部，在商店领取的数量将显示在 Dynamics 365 for Operations 中的转移单的**当前装运量**字段中。 转移单可以指定该物料可以装运到的位置的特定商店。 在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 中的接收请求。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店接收的数量将显示在 Dynamics 365 for Operations 中的转移单的**当前接收量**字段中。

## <a name="stock-counts"></a>存货盘点
存货盘点可以是计划或不定期的。 存货盘点在总部启动，总部指定必须盘点的物料。 总部会创建盘点文档，并将商店接收，将实际的现有存货数量输入 MPOS 或 Cloud POS.。 计划外存货盘点在商店启动，在 MPOS 或 Cloud POS. 中更新实际的现有存货数量。 与周期盘点不同，计划外存货盘点没有物料的预定义列表。 在存货盘点类型为已完工入库时，它承诺和发送给总部。 在总部，将验证和过帐盘点。






