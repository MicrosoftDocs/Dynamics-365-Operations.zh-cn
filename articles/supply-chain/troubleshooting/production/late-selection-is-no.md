---
title: 通过批处理作业重置生产订单时，未遵从后期选择
description: 当您使用定期批处理作业重置生产订单的状态时，系统未遵从后期选择。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026297"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="7b636-103">通过批处理作业重置生产订单时，未遵从后期选择</span><span class="sxs-lookup"><span data-stu-id="7b636-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="7b636-104">知识库编号：4614634</span><span class="sxs-lookup"><span data-stu-id="7b636-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b636-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="7b636-105">Symptoms</span></span>

<span data-ttu-id="7b636-106">当您使用定期批处理作业重置生产订单的状态时，系统未遵从后期选择。</span><span class="sxs-lookup"><span data-stu-id="7b636-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b636-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="7b636-107">Resolution</span></span>

<span data-ttu-id="7b636-108">当前设计不支持在 *重置状态* 流程中使用后期选择。</span><span class="sxs-lookup"><span data-stu-id="7b636-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
