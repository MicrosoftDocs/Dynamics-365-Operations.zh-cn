---
title: 无法将多个产品收货合并到一个采购订单中
description: 如果不同的产品收货行具有不同的会计日期，则不能将多个产品收货合并到一个采购订单中。
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475657"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>无法将多个产品收货合并到一个采购订单中

## <a name="symptoms"></a>故障特征

如果不同的产品收货行具有不同的会计日期，则不能将多个产品收货合并到一个采购订单中。

## <a name="resolution"></a>解决方法

在早期版本的  Dynamics 365 Supply Chain Management 中，这种情况允许合并。 但是，这种做法很容易出错。 创建的采购订单行上的会计日期应与从其创建这些采购订单行的产品收货行上的会计日期相同。 （采购订单行上的会计日期与采购订单标题上的会计日期匹配。）因此，不再允许将多个产品收货合并到一个采购订单中。

例如，会计日期会用于预算预留和保留款。 因此，应在从产品收货到采购订单的转换期间保留此信息。
