---
title: 在下达生产订单时无法预留物料 RM
description: 下达生产订单时，可能会出现以下错误：“可能无法完全预留物料 RM。” 请确保全部数量可用，或手动预留物料。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475715"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>在下达生产订单时无法完全预留物料 RM

## <a name="symptoms"></a>故障特征

如果在将生产订单下达到仓库时，不是所有物料清单行项实际都可用，并且 **下达到仓库** 策略设置为 *需要全部预留*，您将收到以下错误消息：

> 物料 RM 无法完全预留。 请确保全部数量都可用，或者如果物料清单行上的“预留”字段设置为“手动”或“已开始”，则手动预留物料。 无法将订单发放到仓库，因为某些材料无法预留。

## <a name="resolution"></a>解决方法

此行为是有意设计的，属于正常工作。 若要解决此问题，请按照以下错误消息中提供的说明操作：“请确保全部数量都可用，或者如果物料清单行上的预留字段设置为手动或已开始，则手动预留物料。”
