---
title: 已确认生产订单和估计生产订单之间的物料清单分解差异
description: 物料清单分解行为对于确定的生产订单和人工创建工作的估计生产订单是不同的
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
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475685"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>已确认生产订单和估计生产订单之间的物料清单分解差异

## <a name="symptoms"></a>故障特征

生产订单确定后，物料在您分解物料清单 (BOM) 时不会分解。 但是，当您手动创建工作订单然后估计生产订单时，物料将被分解。

### <a name="resolution"></a>解决方法

确定生产订单时发生的分解将指向计划订单，但似乎计划订单在这种情况下目前不会确定。 但是，如果已经估计了生产订单，分解将从不存在计划订单的已下达生产订单触发。
