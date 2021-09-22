---
title: 有存货和生产订单时生成了计划订单
description: 即使物料有存货且这些物料已有生产订单也生成计划订单
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475737"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>有存货和生产订单时生成了计划订单

## <a name="symptoms"></a>故障特征

即使物料有存货且这些物料已有生产订单也生成计划订单。

## <a name="resolution"></a>解决方法

您可以通过在 **覆盖范围组** 页上为相关组增加 **正天数** 值来解决此问题。 此更改会让系统确定现有库存量是否可用于需求。 之后就不会为库存中的物料生成新的计划订单。
