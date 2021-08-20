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
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741948"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>通过批处理作业重置生产订单时，未遵从后期选择

知识库编号：4614634

## <a name="symptoms"></a>故障特征

当您使用定期批处理作业重置生产订单的状态时，系统未遵从后期选择。

## <a name="resolution"></a>解决方法

当前设计不支持在 *重置状态* 流程中使用后期选择。
