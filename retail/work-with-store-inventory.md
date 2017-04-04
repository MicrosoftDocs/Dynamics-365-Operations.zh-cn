---
title: "管理商店库存"
description: "文章此描述可用于管理库存文档的类型。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>管理商店库存

文章此描述可用于管理库存文档的类型。

您可以使用以下文档的类型管理您的组织的库存。

## <a name="purchase-orders"></a>采购订单
采购订单在总部创建。 如果零售该仓库在采购订单头中，则此命令。Microsoft Dynamics 365 中可在接收商店使用 Modern POS (MPOS) 或云的零售 POS -的工序。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店中接收的数量。工序的 Dynamics 365 在采购订单上显示，请现在收到** **在字段。

## <a name="transfer-orders"></a>转移单
转移单可指定特定商店为可用于装运物料的位置。 在这种情况下，在转移单商店显示为端或云 POS 的领料请求。 在请求的领料数量后，它们承诺和发送总部。 在总部，在商店领料的数量。工序的 Dynamics 365 在转移单，将显示当前装运** **在字段。 转移单可以指定该物料可以装运到的位置的特定商店。 在这种情况下，在转移单商店显示为端或云的 POS 一个接收的请求。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店中接收的数量。工序的 Dynamics 365。将显示转移单，请现在收到** **在字段。

## <a name="stock-counts"></a>存货盘点
存货盘点可以是计划或不定期的。 存货盘点在总部启动，总部指定必须盘点的物料。 总部创建可向商店在接收数量，实际现有量库存中 MPOS 输入或覆盖 POS 的盘点文档。 计划外存货盘点在商店启动，并且，数量实际现有量库存中 MPOS 更新或覆盖 POS。 与周期盘点不同，计划外存货盘点没有物料的预定义列表。 在存货盘点类型为已完工入库时，它承诺和发送给总部。 在总部，将验证和过帐盘点。




