---
title: 商店库存管理
description: 本主题描述可用于管理库存的文档类型。
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "339226"
---
# <a name="store-inventory-management"></a>商店库存管理

[!include [banner](includes/banner.md)]

本主题描述可用于管理库存的文档类型。

您可以使用以下文档的类型管理您的组织的库存。

在 Dynamics 365 for Retail 中处理库存和使用 POS 应用程序时，请务必记住 POS 为库存维度和某些库存物料类型提供有限支持。  

POS 解决方案不支持以下物料配置：
- 物料清单物料（除套件产品外，其使用物料清单框架的某些组件）
- 实际称重物料
- 批次控制物料

POS 应用程序当前在 POS 中不支持以下跟踪维度：
- 批次跟踪维度
- 所有者维度

POS 解决方案为以下维度提供有限支持。 有限支持指示 POS 可以根据仓库/商店设置配置将其中的一些维度自动默认为库存交易记录中的维度。 如果销售交易记录手动输入到 ERP，POS 将不以维度支持方式完全支持这些维度。 

- 库位
- 牌照（仅当在物料和商店仓库上启用了 **Uuse 仓库管理流程**时适用）
- 序列号
- 库存状态

> [!NOTE]
> 所有组织均必须在将配置部署到生产前在开发或测试环境中通过 POS 测试物料配置。 通过您的物料的 POS 通过执行常规的付现自运的销售交易并创建客户订单来测试您的物料（如果适用）。 测试必须包括在测试环境中运行完整的对帐单过帐流程并确认没有问题。
> 按 POS 应用程序不支持的方式配置物料，且不进行适当的测试，可能导致对帐单过帐流程在生产中失败，且没有更正问题的简便方法。 可以有选择地考虑对应用程序进行合作伙伴或客户自定义以允许这些过帐流程成功完成。 如果不需要自定义，组织必须确保您的产品的产品配置已经以标准 POS 应用程序/订单创建/对帐单过帐流程支持的方式完成。

## <a name="purchase-orders"></a>采购订单

采购订单在总部创建。 如果零售仓库包括在采购订单头中，通过使用 Microsoft Dynamics 365 for Retail 中的 Modern POS (MPOS) 或 Cloud POS 订货可以在商店接收。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店接收的数量将在 Dynamics 365 for Retail 中在采购订单的**当前接收量**字段中显示。

## <a name="transfer-orders"></a>转移单

转移单可指定特定商店为可用于装运物料的位置。 在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 内的拣货请求。 在请求的领料数量后，它们承诺和发送总部。 在总部，在商店已领料的数量将在 Dynamics 365 for Retail 中在转移单上的**当前装运量**字段中显示。 转移单可以指定该物料可以装运到的位置的特定商店。 在这种情况下，转移单在商店中显示为 MPOS 或 Cloud POS 中的接收请求。 在商店输入已接收数量后，可以保存本地以供附加修改。 或者，数量可承诺和发送给总部。 在总部，在商店接收的数量将在 Dynamics 365 for Retail 中在转移单的**当前接收量**字段中显示。

## <a name="stock-counts"></a>存货盘点

存货盘点可以是计划或不定期的。 存货盘点在总部启动，总部指定必须盘点的物料。 总部会创建盘点文档，并将商店接收，将实际的现有存货数量输入 MPOS 或 Cloud POS.。 计划外存货盘点在商店启动，在 MPOS 或 Cloud POS. 中更新实际的现有存货数量。 与周期盘点不同，计划外存货盘点没有物料的预定义列表。 在存货盘点类型为已完工入库时，它承诺和发送给总部。 在总部，将验证和过帐盘点。

## <a name="inventory-lookup"></a>库存查找

在库存查找页可以查看多个商店和仓库的当前现有产品数量。 除了当前现有数量以外，还可以查看各个商店的未来可承诺 (ATP) 数量。 为此，选择你要查看 ATP 的商店，然后单击**查看商店可用性**。
