---
title: 负数天内存在采购时会创建计划采购订单
description: 如果覆盖范围代码为“最小值/最大值”，在负数天内存在采购时，计划优化会创建计划采购订单。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026309"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="d4467-103">负数天内存在采购时会创建计划采购订单</span><span class="sxs-lookup"><span data-stu-id="d4467-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="d4467-104">知识库编号：4614298</span><span class="sxs-lookup"><span data-stu-id="d4467-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="d4467-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="d4467-105">Symptoms</span></span>

<span data-ttu-id="d4467-106">如果覆盖范围代码为 *最小值/最大值*，在负数天内存在采购时，计划优化会创建计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="d4467-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4467-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="d4467-107">Resolution</span></span>

<span data-ttu-id="d4467-108">计划优化不支持负天数。</span><span class="sxs-lookup"><span data-stu-id="d4467-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="d4467-109">但是，它始终确保不会在相对于当前日期的提前时间内安排计划订单。</span><span class="sxs-lookup"><span data-stu-id="d4467-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="d4467-110">例如，采购提前期为 10 天，采购订单预计从今天起八天到达。</span><span class="sxs-lookup"><span data-stu-id="d4467-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="d4467-111">在这种情况下，采购订单将用作从今天起五天的需求供应。</span><span class="sxs-lookup"><span data-stu-id="d4467-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="d4467-112">因此，我们建议您调整提前期来覆盖所有（或几乎所有）场景。</span><span class="sxs-lookup"><span data-stu-id="d4467-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
