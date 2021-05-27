---
title: 您无法为面向客户的销售订单开票
description: 启用“自动过帐发票”选项后，您无法再为原始销售订单和原始直接交货采购订单开票。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026299"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="16469-103">您无法为面向客户的销售订单开票</span><span class="sxs-lookup"><span data-stu-id="16469-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="16469-104">知识库编号：4611793</span><span class="sxs-lookup"><span data-stu-id="16469-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="16469-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="16469-105">Symptoms</span></span>

<span data-ttu-id="16469-106">在供应商的 **内部公司** 页上启用 **自动过帐发票** 选项后，您无法再为原始销售订单和原始直接交货采购订单开票。</span><span class="sxs-lookup"><span data-stu-id="16469-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="16469-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="16469-107">Resolution</span></span>

<span data-ttu-id="16469-108">内部公司和直接交货订单发票的同步行为由[设置用于过帐内部公司订单的参数](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order)中所述的参数控制和强制执行。</span><span class="sxs-lookup"><span data-stu-id="16469-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="16469-109">设置这些参数后，必须首先为内部公司销售订单开票。</span><span class="sxs-lookup"><span data-stu-id="16469-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="16469-110">然后原始销售订单和采购订单将同步。</span><span class="sxs-lookup"><span data-stu-id="16469-110">The original sales orders and purchase orders will then be synchronized.</span></span>
