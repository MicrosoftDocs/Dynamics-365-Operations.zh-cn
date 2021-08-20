---
title: 装运信息设置
description: 本主题介绍如何为登陆成本模块设置装运信息。
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 4760a87bdcf0f109d5f78dae289446efa12bf359e7fe4b4beb0a983f68d95f34
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758608"
---
# <a name="shipping-information-setup"></a>装运信息设置

[!include [banner](../../includes/banner.md)]

本主题介绍如何为 **登陆成本** 模块设置装运信息。

## <a name="description-of-goods"></a><a name="description-of-goods"></a>货物描述

货物描述帮助确定货物的航行、装运集装箱或帐页以及其中的货物。 您可以在装运集装箱标头或帐页标头上选择货物描述。

要使用货物描述，转到 **登陆成本 \> 装运信息设置 \> 货物描述**。 在那里，您可以查看、打开、创建和删除货物描述的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 货物描述 | 为将使用此描述的货物类型输入唯一标识名称/编号。 |
| 说明 | 输入此类别中的货物类型的描述。 |

## <a name="vessels"></a><a name="vessels"></a>船舶

船只是装运公司或代理使用的船舶或船只的唯一名称。 创建航行时，必须始终为航行选择或输入船只。 如果您经常使用相同船只，那么可以通过为每个船只创建船只记录来更快、更轻松地创建新航行，从而允许用户从列表中选择船只，而不是每次都要手动输入名称或编号。

要使用船只，请转到 **登陆成本 \> 装运信息设置 \> 船只**。 在那里，您可以查看、打开、创建和删除船只的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 船舶 | 输入将用于在航行中运输货物的船的唯一标识名称/编号。 |
| 说明 | 输入船只的描述。 通常，此描述确定船的名称以及装运公司/代理。 |
| 交货模式 | 选择船只使用的交货方式（如 _空运_、_海运_ 或 _火车_）。 |

## <a name="exporters"></a>出口商

每个出口商记录确定可以定义为航行的供应商的供应商或出口商。 出口商可以与航行关联，并可以用于报告。

要使用出口商，请转到 **登陆成本 \> 装运信息设置 \> 出口商**。 在那里，您可以查看、打开、创建和删除出口商的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 出口商 | 输入在航行中运输的货物出口商的唯一标识名称/编号。 |
| 说明 | 输入出口商的描述。 通常，此描述确定装运公司/代理的完整名称。 |

## <a name="commodity-codes"></a>商品代码

您将使用商品代码来帮助海关查验和计算航行中货物的关税税率。 您可以在 **已发布产品** 页选择商品代码。

要使用商品代码，请转到 **登陆成本 \> 装运信息设置 \> 商品代码**。 在那里，您可以查看、打开、创建和删除商品代码的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 商品代码 | 为此商品类型输入唯一代码。 |
| 说明 | 输入商品类型的描述。 |

## <a name="customs-description"></a>海关描述

海关描述帮助出于海关目的识别货物。 您可以在 **已发布产品** 页或采购订单行上选择海关描述。

要使用海关描述，转到 **登陆成本 \> 装运信息设置 \> 海关描述**。 在那里，您可以查看、打开、创建和删除海关描述的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 海关描述 | 为此海关分类类型输入唯一代码。 通常，此代码将是关税主管机构为货物的描述和性质提供的官方描述。 |
| 说明 | 输入海关分类的描述。 |
