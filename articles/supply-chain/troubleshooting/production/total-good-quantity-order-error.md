---
title: 尝试结束订单时发生良品总数错误
description: 尝试结束生产订单并完工入库时，可能会收到良品总数错误。 此页面介绍此问题的原因和缓解方法。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475678"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>尝试结束生产订单时发生良品总数错误

## <a name="symptoms"></a>故障特征

当您尝试在生产订单上过帐完工入库日记帐时，会收到以下错误消息：

> 生产完工入库的完好数量合计将是 %1。 最后一道工序的反馈总计为 0.00 个。

## <a name="cause"></a>原因

如果最后工序中过帐的数量不正确，将发生此问题。 例如，如果生产已开始，但未分配必须开始的数量，工艺卡日记帐在过帐时将没有任何行。 要确认情况，请打开生产订单，然后在操作窗格上的 **视图** 选项卡上，选择 **工艺卡**。

## <a name="resolution"></a>解决方法

您可以通过为日记帐未正确过帐的操作过帐其他日记帐来解决此问题。 重新启动生产订单，然后选择过帐其他日记帐。 此操作不会启动生产订单，但会过帐日记帐。 然后，工艺卡应会显示已过帐的数量，您应该能够成功结束生产订单。
