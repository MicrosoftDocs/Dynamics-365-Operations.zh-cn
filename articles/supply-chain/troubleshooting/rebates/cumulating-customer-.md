---
title: 使用物料返点组时客户返点累计失败
description: 当您将客户返点协议与物料返点组结合使用时，将计算返点，但累计将失败。
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026293"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="54bc7-103">使用物料返点组时客户返点累计失败</span><span class="sxs-lookup"><span data-stu-id="54bc7-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="54bc7-104">知识库编号：4611372</span><span class="sxs-lookup"><span data-stu-id="54bc7-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="54bc7-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="54bc7-105">Symptoms</span></span>

<span data-ttu-id="54bc7-106">当您将客户返点协议（*金额* 类型）与物料返点组结合使用时，将计算返点，但累计将失败。</span><span class="sxs-lookup"><span data-stu-id="54bc7-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="54bc7-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="54bc7-107">Resolution</span></span>

<span data-ttu-id="54bc7-108">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="54bc7-108">The system is behaving as designed.</span></span> <span data-ttu-id="54bc7-109">物料组仅将具有相同阈值条件的物料分组在一起。</span><span class="sxs-lookup"><span data-stu-id="54bc7-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="54bc7-110">返点条件（阈值）针对每个物料的金额设置，不是针对物料组中任何物料的累计金额设置。</span><span class="sxs-lookup"><span data-stu-id="54bc7-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
