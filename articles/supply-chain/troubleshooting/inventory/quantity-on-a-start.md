---
title: 拆分订单后，已开始的隔离订单上的数量不更新
description: 当您创建隔离订单并尝试拆分它时，订单数量未更新为拆分后的剩余数量。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026316"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="2cf8c-103">拆分订单后，已开始的隔离订单上的数量不更新</span><span class="sxs-lookup"><span data-stu-id="2cf8c-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="2cf8c-104">知识库编号：4613113</span><span class="sxs-lookup"><span data-stu-id="2cf8c-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="2cf8c-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="2cf8c-105">Symptoms</span></span>

<span data-ttu-id="2cf8c-106">当您创建隔离订单并尝试拆分它时，订单数量未更新为拆分之后的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="2cf8c-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="2cf8c-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="2cf8c-107">Resolution</span></span>

<span data-ttu-id="2cf8c-108">系统不会更改隔离订单的原始数量，以确保您可以跟踪为该隔离订单创建的原始数量。</span><span class="sxs-lookup"><span data-stu-id="2cf8c-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="2cf8c-109">但是，系统会跟踪从隔离订单拆分的数量。</span><span class="sxs-lookup"><span data-stu-id="2cf8c-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="2cf8c-110">为进行此跟踪，它使用名为 `QuantityThatHasSplitIntoOtherQuarantineOrders` 的数据库字段。</span><span class="sxs-lookup"><span data-stu-id="2cf8c-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="2cf8c-111">但是，此字段在用户界面 (UI) 中不可见。</span><span class="sxs-lookup"><span data-stu-id="2cf8c-111">However, this field isn't visible in the user interface (UI).</span></span>
