---
title: 未入帐间接成本报表包括已删除的生产订单
description: 未入帐间接成本报表显示有关已部分处理并随后删除的生产订单的信息。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751761"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>未入帐间接成本报表包括已删除的生产订单

知识库编号：4612748

## <a name="symptoms"></a>故障特征

**未入帐间接成本** 报表显示有关已部分处理并随后删除的生产订单的信息。

## <a name="resolution"></a>解决方法

冲销生产订单时，还将冲销该生产订单的所有交易。 删除生产订单时，子分类帐表和总帐会保留与该订单有关的所有交易。 报表将在子分类帐表中显示这些交易。 对于该生产订单，净值应为 0.00。
