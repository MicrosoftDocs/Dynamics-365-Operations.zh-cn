---
title: "使用跟踪进行分解"
description: "本文说明如何可以使用跟踪来探索订单分解结果背后的原因。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e7f765f31ba34481cca78155e77eca61b106d50
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="9596b-103">使用跟踪进行分解</span><span class="sxs-lookup"><span data-stu-id="9596b-103">Use tracing for explosion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9596b-104">本文说明如何可以使用跟踪来探索订单分解结果背后的原因。</span><span class="sxs-lookup"><span data-stu-id="9596b-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="9596b-105">通过启用跟踪，您可以查看有关对特定订单的分解结果有贡献的因素的信息。</span><span class="sxs-lookup"><span data-stu-id="9596b-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="9596b-106">以下示例显示如何使用跟踪信息：</span><span class="sxs-lookup"><span data-stu-id="9596b-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="9596b-107">查看操作与计划的订单之间的关系，以优化供应链和库存预留。</span><span class="sxs-lookup"><span data-stu-id="9596b-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="9596b-108">查看已审核的订单的关系。</span><span class="sxs-lookup"><span data-stu-id="9596b-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="9596b-109">您可以自动关注固定派生的需求，然后更准确地设置订单的优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="9596b-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="9596b-110">模拟计划结果以确定计划参数是否最佳。</span><span class="sxs-lookup"><span data-stu-id="9596b-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="9596b-111">标识如何确定信息（如订单的生产日期、数量和优先级）。</span><span class="sxs-lookup"><span data-stu-id="9596b-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="9596b-112">您可以查看有关所选订单的预期和操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9596b-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="9596b-113">在**“分解”**页中，跟踪信息在上部窗格的**“说明”**选项卡中提供。</span><span class="sxs-lookup"><span data-stu-id="9596b-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="9596b-114">跟踪在分解订单时进行。</span><span class="sxs-lookup"><span data-stu-id="9596b-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="9596b-115">若要开始跟踪计划订单，请单击**“更新”**，然后选中**“启用跟踪功能”**复选框。</span><span class="sxs-lookup"><span data-stu-id="9596b-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="9596b-116">您可以使用**“查找文本”**字段搜索记录的特定信息。</span><span class="sxs-lookup"><span data-stu-id="9596b-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="9596b-117">搜索结果在树中突出显示。</span><span class="sxs-lookup"><span data-stu-id="9596b-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="9596b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="9596b-118">See also</span></span>
--------

[<span data-ttu-id="9596b-119">主计划</span><span class="sxs-lookup"><span data-stu-id="9596b-119">Master plans</span></span>](master-plans.md)



