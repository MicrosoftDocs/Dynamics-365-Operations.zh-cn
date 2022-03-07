---
title: 通过批处理作业重置生产订单时，未遵从后期选择
description: 当您使用定期批处理作业重置生产订单的状态时，系统未遵从后期选择。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026297"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>通过批处理作业重置生产订单时，未遵从后期选择

知识库编号：4614634

## <a name="symptoms"></a>故障特征

当您使用定期批处理作业重置生产订单的状态时，系统未遵从后期选择。

## <a name="resolution"></a>解决方法

当前设计不支持在 *重置状态* 流程中使用后期选择。
