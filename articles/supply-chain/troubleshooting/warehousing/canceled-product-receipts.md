---
title: 取消产品收货后不会将交易状态更新为“已登记”
description: 为入站负荷取消产品收货后，系统自动将库存交易状态从“已收货”更新为“已订购”。
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731095"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>取消产品收货后不会将交易状态更新为“已登记”

## <a name="symptoms"></a>故障特征

为入站负荷运行 **取消产品收货** 操作后，系统自动将库存交易的状态从 *已收货* 更新为 *已订购*。

## <a name="resolution"></a>解决方法

为出站负荷取消装箱单时，库存交易的状态将保持 *已领料*。 但是，当取消入站负荷的产品收货时，库存交易的状态不会还原到 *已登记*。 因此，取消入站负荷的产品收货后，仓库工作人员必须重新登记负荷的物料数量。

有关详细信息，请参阅[为入站负荷登记到达的物料数量](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving)。
