---
title: 直接派生的确认订单被正在审核工作流处理
description: 直接派生的确认订单被状态为“正在审核”的工作流处理。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026311"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="c2af2-103">直接派生的确认订单被正在审核工作流处理</span><span class="sxs-lookup"><span data-stu-id="c2af2-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="c2af2-104">知识库编号：4612450</span><span class="sxs-lookup"><span data-stu-id="c2af2-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="c2af2-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="c2af2-105">Symptoms</span></span>

<span data-ttu-id="c2af2-106">直接派生的确认订单被状态为 *正在审核* 的工作流处理。</span><span class="sxs-lookup"><span data-stu-id="c2af2-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c2af2-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="c2af2-107">Resolution</span></span>

<span data-ttu-id="c2af2-108">启用更改跟踪后，状态为 *正在审核* 将被分配给确认的派生订单（分包合同采购订单）。</span><span class="sxs-lookup"><span data-stu-id="c2af2-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="c2af2-109">因此，如果派生了采购订单（分包合同采购订单），会仅将该采购订单提交给工作流。</span><span class="sxs-lookup"><span data-stu-id="c2af2-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="c2af2-110">如果采购订单是确认的计划采购订单，将会自动获得批准，以确保计划引擎不会在采购订单仍处于 *草稿* 状态时创建新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="c2af2-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
