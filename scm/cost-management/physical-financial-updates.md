---
title: "实际和财务更新"
description: "本主题提供哪些类型的交易记录将增减库存数量的概要。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>实际和财务更新

[!include[banner](../includes/banner.md)]


本主题提供哪些类型的交易记录将增减库存数量的概要。 

库存交易记录可以在 Microsoft Dynamics 365 for Operations 中完成实际更新和财务更新。 某些实际交易记录和财务交易记录类型会增加库存数量，而其他则会减少数量。

## <a name="physical-increases"></a>实际增加
在过帐某一实际交易记录时，该交易记录的状态为**已接收**。 以下交易记录被视为实际增加：

-   采购订单收货
-   销售订单装箱单返回
-   将生产订单报告为已完工入库
-   生产订单领料单上的副产品

## <a name="financial-increases"></a>财务增加
在过帐某一财务收货交易记录时，增加数量的交易记录的状态为**已采购**。 以下交易记录被视为财务增加：

-   供应商发票
-   用于退货的销售订单发票
-   生产订单成本计算
-   正数量库存日记帐，例如移动、损益、盘点、物料清单和转移

## <a name="transactions-that-increase-quantity"></a>增加数量的交易记录
以移动平均成本价过帐增加数量的交易记录。 Dynamics 365 for Operations 计算移动平均成本价（基于每个财务跟踪的库存维度的上述各交易记录的成本）。 有关移动平均成本价的信息，请参阅[移动平均成本价](running-average-cost-price.md)。

## <a name="transactions-that-decrease-quantity"></a>减少数量的交易记录
过帐减少数量的交易记录时，Dynamics 365 for Operations 使用计算出的移动平均成本价，而不考虑与该库存关联的库存模型。 减少数量的交易记录不得在另一个交易记录过帐前标记为该交易记录。 如果实际现有库存量变为负值，Dynamics 365 for Operations 使用为**物料**页上的物料定义的库存成本。 **注意：**如果启用多站点功能，则该成本将改为在**默认订单设置**页上定义的库存成本。

## <a name="physical-issues-vs-financial-issues"></a>实际发货与财务发货
在过帐某一实际发货交易记录时，该交易记录的状态为**已减少**。 以下交易记录被视为实际发货：

-   生产订单领料单日志
-   销售订单装箱单
-   采购订单装箱单退货

在过帐某一财务交易记录时，该交易记录的状态为**已销售**。 以下交易记录被视为财务发货：

-   结束生产订单
-   销售订单发票
-   供应商发票退货
-   负数量库存日记帐，例如移动、损益、盘点、物料清单和转移

以移动平均成本价过帐减少数量的交易记录。 因此，需要库存结转过程以将发货交易记录结算到基于分配给每个物料的库存模型的收货交易记录。




