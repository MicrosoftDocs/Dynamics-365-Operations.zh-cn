---
title: 生产差异的常见来源
description: 本文说明生产差异的每个生产类型的各个典型来源。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f627cb1d15d0fa858abae588d149875967cff97c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813235"
---
# <a name="common-sources-of-production-variances"></a>生产差异的常见来源

[!include [banner](../includes/banner.md)]

本文说明生产差异的每个生产类型的各个典型来源。 

以下是 **批次规模** 差异的一些典型来源：

-   某一生产订单的完好数量不同于在标准成本计算中使用的计算数量。 该数量提供用于摊销固定成本的基础。
-   生产订单固定成本的价值不同于在标准成本计算中使用的固定成本。 出于若干原因，生产订单的固定成本可能不同。 例如，固定成本可能反映以下因素：
    -   手动更改生产物料清单 (BOM) 或工艺路线
    -   当您创建生产订单时的不同的物料清单版本或工艺路线版本的选择
    -   对分配给物料的物料清单版本和工艺路线版本的计划的工程更改

以下是 **生产价格** 差异的一些典型来源：

-   工艺路线工序的报告的消耗量的成本类别（及成本类别价格）不同于在标准成本计算中使用的成本类别。
-   成本类别价格的有效成本不同于在标准成本计算中使用的成本类别价格。

以下是 **生产数量** 差异的一些典型来源：

-   材料组件发货过多或发货不足。
-   针对工艺路线工序过多报告时间或过少报告时间。
-   您过多接收或过少接收了相对于订单数量的父物料的完好数量。 不过，您基于生产订单的订单数量将组件完全发货和完全报告工序。

以下是 **生产替代** 差异的一些典型来源：

-   您发货的材料组件不在生产物料清单中。
-   您手动将组件添加到生产物料清单并将该组件报告为已消耗。
-   您将物料报告为已消耗，但不手动将它添加到生产物料清单中。
-   您手动将工序添加到生产工艺路线并将该工序报告为已消耗。
-   在创建生产订单时您选择不同于在标准成本计算中使用的物料清单版本的物料清单版本。
-   在创建生产订单时您选择不同于在标准成本计算中使用的工艺路线版本的工艺路线版本。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]