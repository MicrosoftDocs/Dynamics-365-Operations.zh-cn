---
title: 在领料单登记期间选择位置时发生错误
description: 在领料单登记期间选择位置时发生错误。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026287"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="bd294-103">在领料单登记期间选择位置时发生错误</span><span class="sxs-lookup"><span data-stu-id="bd294-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="bd294-104">知识库编号：4613106</span><span class="sxs-lookup"><span data-stu-id="bd294-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="bd294-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="bd294-105">Symptoms</span></span>

<span data-ttu-id="bd294-106">当您的系统配置为自动预留销售订单时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="bd294-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="bd294-107">如果您尝试选择领料单登记行的位置，在使用仓库管理 (WMS) 预留流程时会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="bd294-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="bd294-108">无法使用新维度更新数量</span><span class="sxs-lookup"><span data-stu-id="bd294-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="bd294-109">发生此问题的原因可能是由于您在指定位置没有足够的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="bd294-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd294-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="bd294-110">Resolution</span></span>

<span data-ttu-id="bd294-111">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="bd294-111">The system is behaving as designed.</span></span>

<span data-ttu-id="bd294-112">在使用仓库级预留流程的场景中，如果不会在所有库存维度级别预留现有库存量，并且您在指定位置没有足够的现有库存量，建议您从领料行使用手动预留流程。</span><span class="sxs-lookup"><span data-stu-id="bd294-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="bd294-113">然后，您可以使用 *预留批次* 功能为所有可用的现有数量分配更低级别的预留，如位置。</span><span class="sxs-lookup"><span data-stu-id="bd294-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
