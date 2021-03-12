---
title: 商店库存管理
description: 本主题描述可用于管理库存的文档类型。
author: rubencdelgado
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 616fb8975543344657c00c419ce7279658694675
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989468"
---
# <a name="commerce-inventory-management"></a>Commerce 库存管理

[!include [banner](includes/banner.md)]

当您在 Microsoft Dynamics 365 Commerce 中使用库存以及使用连接到 Commerce Scale Unit (CSU) 的任何 Commerce 应用程序时，务必要知道 CSU 中的订单处理逻辑为某些库存维度和某些库存物料类型提供有限的支持。 Commerce 应用程序不支持通过 Dynamics 365 Supply Chain Management 中的物料配置选项提供的所有物料配置功能。

在 CSU 上运行的 Commerce 应用程序不支持以下产品维度和物料配置：

- 配置产品维度和物料清单 (BOM) 物料（除了零售包产品，这种产品使用 BOM 框架的某些组件）
- 实际称重物料
- 版本产品维度控制的物料

在 CSU 上运行的 Commerce 应用程序不支持以下跟踪维度：
- 所有者维度

- 销售点 (POS) 应用程序可以为以下维度提供有限的支持。 POS 可能根据仓库或商店设置配置在库存交易记录中自动输入这些维度中的一部分。 但是，如果在 Commerce Headquarters 中手动输入销售交易记录，POS 将不以维度支持方式完全支持这些维度。 

- **仓库位置** – 使用新的[入站操作](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)和[出站操作](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) POS 操作时，用户可以选择物料的接收仓库库存位置或出站转移单物料的发出仓库库存位置。 如果使用过时的 **领料和接收** 操作，为出站转移的接收和领料提供的位置管理支持有限。 仅当为物料和商店仓库开启了 **使用仓库管理流程** 选项，才提供此支持。 现在不能为 **存货盘点** 操作或 **库存查找** 操作使用库存位置。

- **牌照** - 仅当对物料和商店仓库启用了 **使用仓库管理流程** 选项时，牌照才适用。 在 POS，如果使用 **入站操作** 操作或 **领料和接收** 操作（已开启了仓库管理流程）在商店库存中接收了库存，并且已经将选择了用于接收物料的位置链接到了需要牌照控制的位置配置文件，POS 应用程序将向接收行系统化应用牌照。 POS 用户不能更改或管理此牌照数据。 如果需要全面管理牌照，建议商店使用[仓库应用](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app)或后勤办公室客户端管理这些物料的收货。

- **序列号** - POS 应用程序有限支持要在 POS 中使用序列号物料创建且包含序列化物料的订单的交易记录销售行上登记的单个序列号。 不会针对库存中已登记的序列号验证此序列号。 如果某个销售订单是在呼叫中心渠道注册或通过企业资源规划 (ERP)履行的，并且在 ERP 中履行过程中将多个序列号登记到了一个销售行中，那么如果在 POS 中为这些订单处理退货，则不能应用或验证这些序列号。 使用 **入站操作** 操作接收库存时，用户可以[注册或确认接收的序列号](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items)。

- **批处理 ID** - 如果销售受批次控制的物料，POS 应用程序在对帐单过帐期间提供有限的支持，但是 POS 用户无法定义使用 POS 应用程序时销售或选择的批处理 ID。

- **库存状态** - 对于使用仓库管理流程且需要库存状态的物料，则不能通过 POS 应用程序设置或修改此状态字段。 库存中接收物料时，使用商店仓库配置中定义的默认库存状态。

> [!NOTE]
> 所有组织均必须在将物料配置部署到生产环境前，在开发或测试环境中通过 Commerce 应用测试这些物料配置。 使用这些应用在 POS 中执行常规的现金和结转销售交易来测试您的物料，并通过 POS、呼叫中心或电子商务创建客户订单（如果适用）来验证您的物料是否可以得到完全支持。 部署任何新物料配置之前，还应测试 POS 履行和库存流程（如库存接收和订单履行操作），以确保 POS 应用程序可支持这些流程。 测试必须包括在测试环境中运行完整的对帐单/订单过帐流程，以及验证在 Commerce Headquarters 中创建和过帐这些物料的订单时不会出现过帐问题。
>
> 如果以 Commerce 应用程序不支持的方式配置物料，并且未进行适当的测试，则可能会发生无法轻易更正或根本无法更正的数据故障。

## <a name="purchase-orders"></a>采购订单

采购订单在 Commerce Headquarters 中创建。 如果采购订单标题中或采购订单行中包含商店仓库，可以在 POS 中使用[入站操作](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)操作在商店中接收这些行。 

## <a name="transfer-orders"></a>转移单

转移单可以在 Commerce Headquarters 中或通过 POS 中的[入站操作](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)或[出站操作](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)操作创建。 **入站操作** POS 操作用于创建转移单请求以将库存从其他仓库或商店位置发送到商店。 **出站操作** POS 操作用于创建转移单请求以将库存从商店装运到其他仓库或商店位置。 创建了商店的转移单之后，该商店可通过 POS 中的 **入站操作** 操作管理该转移单的库存接收。 如果商店将库存装运到其他位置，将使用 POS 中的 **出站操作** 操作管理该商店的出站装运流程。

## <a name="stock-counts"></a>存货盘点

存货盘点可以是计划或不定期的。 将通过 Commerce Headquarters 创建与商店仓库链接的盘点日记帐单据创建计划的存货盘点。 此日记帐指定必须盘点的物料。 然后，商店可访问这些预定义盘点日记帐，并使用 POS 中的 **存货盘点** 操作处理。 当商店用户使用 POS 中的 **存货盘点** 操作时，需要时可以发起计划的存货盘点。 与周期盘点不同，计划外存货盘点没有物料的预定义列表。 当 POS 中存货盘点类型为已完工入库时，它承诺和发送给总部。 然后必须在总部验证盘点并在 Commerce Headquarters 中作为单独的步骤过帐。

## <a name="inventory-lookup"></a>库存查找

在 **库存查找** 页可以查看多个商店和仓库的当前现有产品数量。 除了当前现有数量以外，还可以查看各个商店的未来可承诺 (ATP) 数量。 选择要查看的 ATP 数量所属商店，然后选择 **显示商店可用性**。 有关可用配置选项的信息，请参阅[计算零售渠道的库存现有量](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels)。
