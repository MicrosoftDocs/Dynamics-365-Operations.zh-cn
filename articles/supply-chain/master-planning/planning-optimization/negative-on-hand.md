---
title: 使用负现有数量进行计划
description: 此主题介绍在使用计划优化时如何处理负现有量。
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077476"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="501da-103">使用负现有数量进行计划</span><span class="sxs-lookup"><span data-stu-id="501da-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="501da-104">如果系统显示负聚合现有数量，计划引擎将把该数量视为 0（零），以帮助避免超额供应。</span><span class="sxs-lookup"><span data-stu-id="501da-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="501da-105">下面是此功能的工作原理：</span><span class="sxs-lookup"><span data-stu-id="501da-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="501da-106">计划优化功能聚合较低级别覆盖范围维度的现有数量。</span><span class="sxs-lookup"><span data-stu-id="501da-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="501da-107">（例如，如果*库位*不是覆盖范围维度，则计划优化聚合*仓库*级别的现有数量。）</span><span class="sxs-lookup"><span data-stu-id="501da-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="501da-108">如果最低级别覆盖范围维度的聚合现有数量为负，系统将假设现有数量的确为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="501da-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="501da-109">计划系统的精确程度只能达到输入数据的程度。</span><span class="sxs-lookup"><span data-stu-id="501da-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="501da-110">如果输入数据不准确，负现有记录将指示 Microsoft Dynamics 365 Supply Chain Management 中的库存信息与现实不同步。</span><span class="sxs-lookup"><span data-stu-id="501da-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="501da-111">因此，计划结果将有瑕疵。</span><span class="sxs-lookup"><span data-stu-id="501da-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="501da-112">若要获取精确的计划结果，应该尽量减少显示负现有数量的记录的数量。</span><span class="sxs-lookup"><span data-stu-id="501da-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="501da-113">示例 1</span><span class="sxs-lookup"><span data-stu-id="501da-113">Example 1</span></span>

<span data-ttu-id="501da-114">仓库 13 的配置方式如下：</span><span class="sxs-lookup"><span data-stu-id="501da-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="501da-115">**覆盖范围代码：** 最小值/最大值</span><span class="sxs-lookup"><span data-stu-id="501da-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="501da-116">**最小值：** 15 件</span><span class="sxs-lookup"><span data-stu-id="501da-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="501da-117">**最大值：** 25 件</span><span class="sxs-lookup"><span data-stu-id="501da-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="501da-118">覆盖范围维度的最低级别为*仓库*，而以下现有数量的记录级别为*库位*：</span><span class="sxs-lookup"><span data-stu-id="501da-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="501da-119">**站点 1，仓库 13，库位 1：** 20 件</span><span class="sxs-lookup"><span data-stu-id="501da-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="501da-120">**站点 1，仓库 13，库位 2：**&minus;8 件</span><span class="sxs-lookup"><span data-stu-id="501da-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="501da-121">因此，仓库 13 的聚合现有数量为 12 件</span><span class="sxs-lookup"><span data-stu-id="501da-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="501da-122">（= 20 件</span><span class="sxs-lookup"><span data-stu-id="501da-122">(= 20 pcs.</span></span> <span data-ttu-id="501da-123">&minus; 8 件）。</span><span class="sxs-lookup"><span data-stu-id="501da-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="501da-124">在此情况下，计划引擎对仓库 13 使用聚合现有数量 12 件</span><span class="sxs-lookup"><span data-stu-id="501da-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="501da-125">。</span><span class="sxs-lookup"><span data-stu-id="501da-125">for warehouse 13.</span></span>

<span data-ttu-id="501da-126">结果是，计划的订单为 13 件</span><span class="sxs-lookup"><span data-stu-id="501da-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="501da-127">（= 25 件</span><span class="sxs-lookup"><span data-stu-id="501da-127">(= 25 pcs.</span></span> <span data-ttu-id="501da-128">&minus; 12 件）以将仓库 13 从 12 件装</span><span class="sxs-lookup"><span data-stu-id="501da-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="501da-129">到 25 件。</span><span class="sxs-lookup"><span data-stu-id="501da-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="501da-130">示例 2</span><span class="sxs-lookup"><span data-stu-id="501da-130">Example 2</span></span>

<span data-ttu-id="501da-131">仓库 13 的配置方式如下：</span><span class="sxs-lookup"><span data-stu-id="501da-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="501da-132">**覆盖范围代码：** 最小值/最大值</span><span class="sxs-lookup"><span data-stu-id="501da-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="501da-133">**最小值：** 15 件</span><span class="sxs-lookup"><span data-stu-id="501da-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="501da-134">**最大值：** 25 件</span><span class="sxs-lookup"><span data-stu-id="501da-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="501da-135">覆盖范围维度的最低级别为*仓库*，而以下现有数量的记录级别为*库位*：</span><span class="sxs-lookup"><span data-stu-id="501da-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="501da-136">**站点 1，仓库 13，库位 1：** 4 件</span><span class="sxs-lookup"><span data-stu-id="501da-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="501da-137">**站点 1，仓库 13，库位 2：**&minus;8 件</span><span class="sxs-lookup"><span data-stu-id="501da-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="501da-138">因此，仓库 13 的聚合现有数量为 &minus;4 件</span><span class="sxs-lookup"><span data-stu-id="501da-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="501da-139">（= 4 件</span><span class="sxs-lookup"><span data-stu-id="501da-139">(= 4 pcs.</span></span> <span data-ttu-id="501da-140">&minus; 8 件）。</span><span class="sxs-lookup"><span data-stu-id="501da-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="501da-141">换句话说，小于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="501da-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="501da-142">在此情况下，计划引擎假设仓库 13 的现有数量为 0 件，</span><span class="sxs-lookup"><span data-stu-id="501da-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="501da-143">而不是 &minus;4 件。</span><span class="sxs-lookup"><span data-stu-id="501da-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="501da-144">结果是，计划的订单为 25 件</span><span class="sxs-lookup"><span data-stu-id="501da-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="501da-145">（= 25 件</span><span class="sxs-lookup"><span data-stu-id="501da-145">(= 25 pcs.</span></span> <span data-ttu-id="501da-146">&minus; 0 件）以将仓库 13 从 0 件装</span><span class="sxs-lookup"><span data-stu-id="501da-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="501da-147">到 25 件。</span><span class="sxs-lookup"><span data-stu-id="501da-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="501da-148">相关资源</span><span class="sxs-lookup"><span data-stu-id="501da-148">Related resources</span></span>

[<span data-ttu-id="501da-149">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="501da-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="501da-150">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="501da-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="501da-151">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="501da-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="501da-152">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="501da-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="501da-153">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="501da-153">Cancel a planning job</span></span>](cancel-planning-job.md)
