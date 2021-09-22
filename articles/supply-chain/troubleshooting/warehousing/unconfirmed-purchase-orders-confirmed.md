---
title: 更新物料收货任务会确认未确认的订单
description: 运行更新物料收货后，系统会确认状态为“已登记”的未确认订单。 了解用于解决此问题的功能。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475653"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>运行“更新产品收货”之后会确认未确认的采购订单

## <a name="symptoms"></a>故障特征

在运行 *更新产品收货* 定期任务后，系统会自动确认库存交易状态为 *已登记* 的未确认采购订单。

## <a name="resolution"></a>解决方法

新的入站负荷处理功能 *负荷数量超收* 解决了这个问题。 要启用此功能，转到[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)工作区，安装列出顺序启用以下功能：

1. 将采购订单库存交易记录与负荷相关联
2. 负荷数量超收

有关详细信息，请参阅[针对采购订单过帐登记的产品数量](/dynamics365/supply-chain/warehousing/inbound-load-handling)。
