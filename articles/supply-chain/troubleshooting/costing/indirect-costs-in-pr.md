---
title: 未入帐间接成本报表包括已删除的生产订单
description: 未入帐间接成本报表显示有关已部分处理并随后删除的生产订单的信息。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026304"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="0761a-103">未入帐间接成本报表包括已删除的生产订单</span><span class="sxs-lookup"><span data-stu-id="0761a-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="0761a-104">知识库编号：4612748</span><span class="sxs-lookup"><span data-stu-id="0761a-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="0761a-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="0761a-105">Symptoms</span></span>

<span data-ttu-id="0761a-106">**未入帐间接成本** 报表显示有关已部分处理并随后删除的生产订单的信息。</span><span class="sxs-lookup"><span data-stu-id="0761a-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="0761a-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="0761a-107">Resolution</span></span>

<span data-ttu-id="0761a-108">冲销生产订单时，还将冲销该生产订单的所有交易。</span><span class="sxs-lookup"><span data-stu-id="0761a-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="0761a-109">删除生产订单时，子分类帐表和总帐会保留与该订单有关的所有交易。</span><span class="sxs-lookup"><span data-stu-id="0761a-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="0761a-110">报表将在子分类帐表中显示这些交易。</span><span class="sxs-lookup"><span data-stu-id="0761a-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="0761a-111">对于该生产订单，净值应为 0.00。</span><span class="sxs-lookup"><span data-stu-id="0761a-111">For the specific production order, the net value should be 0.00.</span></span>
