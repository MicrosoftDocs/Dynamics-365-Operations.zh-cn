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
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294018"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="f40fd-103">取消产品收货后不会将交易状态更新为“已登记”</span><span class="sxs-lookup"><span data-stu-id="f40fd-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="f40fd-104">故障特征</span><span class="sxs-lookup"><span data-stu-id="f40fd-104">Symptoms</span></span>

<span data-ttu-id="f40fd-105">为入站负荷运行 **取消产品收货** 操作后，系统自动将库存交易的状态从 *已收货* 更新为 *已订购*。</span><span class="sxs-lookup"><span data-stu-id="f40fd-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f40fd-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="f40fd-106">Resolution</span></span>

<span data-ttu-id="f40fd-107">为出站负荷取消装箱单时，库存交易的状态将保持 *已领料*。</span><span class="sxs-lookup"><span data-stu-id="f40fd-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="f40fd-108">但是，当取消入站负荷的产品收货时，库存交易的状态不会还原到 *已登记*。</span><span class="sxs-lookup"><span data-stu-id="f40fd-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="f40fd-109">因此，取消入站负荷的产品收货后，仓库工作人员必须重新登记负荷的物料数量。</span><span class="sxs-lookup"><span data-stu-id="f40fd-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="f40fd-110">有关详细信息，请参阅[为入站负荷登记到达的物料数量](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving)。</span><span class="sxs-lookup"><span data-stu-id="f40fd-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
