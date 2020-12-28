---
title: 使用跟踪进行分解
description: 本文说明如何可以使用跟踪来探索订单分解结果背后的原因。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422772"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="a83a9-103">使用跟踪进行分解</span><span class="sxs-lookup"><span data-stu-id="a83a9-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a83a9-104">本文说明如何可以使用跟踪来探索订单分解结果背后的原因。</span><span class="sxs-lookup"><span data-stu-id="a83a9-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="a83a9-105">通过启用跟踪，您可以查看有关对特定订单的分解结果有贡献的因素的信息。</span><span class="sxs-lookup"><span data-stu-id="a83a9-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="a83a9-106">以下示例显示如何使用跟踪信息：</span><span class="sxs-lookup"><span data-stu-id="a83a9-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="a83a9-107">查看操作与计划的订单之间的关系，以优化供应链和库存预留。</span><span class="sxs-lookup"><span data-stu-id="a83a9-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="a83a9-108">查看已审核的订单的关系。</span><span class="sxs-lookup"><span data-stu-id="a83a9-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="a83a9-109">您可以自动关注固定派生的需求，然后更准确地设置订单的优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="a83a9-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="a83a9-110">模拟计划结果以确定计划参数是否最佳。</span><span class="sxs-lookup"><span data-stu-id="a83a9-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="a83a9-111">标识如何确定信息（如订单的生产日期、数量和优先级）。</span><span class="sxs-lookup"><span data-stu-id="a83a9-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="a83a9-112">您可以查看有关所选订单的预期和操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a83a9-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="a83a9-113">在 **分解** 页中，跟踪信息在上部窗格的 **说明** 选项卡中提供。</span><span class="sxs-lookup"><span data-stu-id="a83a9-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="a83a9-114">跟踪在分解订单时进行。</span><span class="sxs-lookup"><span data-stu-id="a83a9-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="a83a9-115">若要开始跟踪计划订单，请单击 **更新**，然后选中 **启用跟踪功能** 复选框。</span><span class="sxs-lookup"><span data-stu-id="a83a9-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="a83a9-116">您可以使用 **查找文本** 字段搜索记录的特定信息。</span><span class="sxs-lookup"><span data-stu-id="a83a9-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="a83a9-117">搜索结果在树中突出显示。</span><span class="sxs-lookup"><span data-stu-id="a83a9-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a83a9-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="a83a9-118">Additional resources</span></span>
--------

[<span data-ttu-id="a83a9-119">主计划概览</span><span class="sxs-lookup"><span data-stu-id="a83a9-119">Master plans overview</span></span>](master-plans.md)



