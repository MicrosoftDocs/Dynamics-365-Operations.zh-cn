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
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026304"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>未入帐间接成本报表包括已删除的生产订单

知识库编号：4612748

## <a name="symptoms"></a>故障特征

**未入帐间接成本** 报表显示有关已部分处理并随后删除的生产订单的信息。

## <a name="resolution"></a>解决方法

冲销生产订单时，还将冲销该生产订单的所有交易。 删除生产订单时，子分类帐表和总帐会保留与该订单有关的所有交易。 报表将在子分类帐表中显示这些交易。 对于该生产订单，净值应为 0.00。
