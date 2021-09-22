---
title: 取消剩余交货量将采购订单移至“已确认”状态
description: 如果在打开了更改管理的采购订单上取消了剩余交货量，采购订单将进入“已确认”状态
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475700"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>取消剩余交货量将采购订单移至“已确认”状态

## <a name="symptoms"></a>故障特征

对于需要接受更改管理的采购订单，如果请求的唯一更改是取消一个或多个行上的剩余交货量，该采购订单在获得批准后将直接进入 *已确认* 状态，不会创建日记帐。

## <a name="resolution"></a>解决方法

取消剩余交货量不会影响确认日记帐的内容。 此功能应在部分接收行时使用，剩余数量应在与供应商确认采购订单后，在流程步骤中取消。

如果这应该反映在采购订单确认中，数量应在采购订单行上调整，以要求进行确认。 或者，如果行上未进行任何接收，可以删除数量。 在这种情况下，将需要重新确认。
