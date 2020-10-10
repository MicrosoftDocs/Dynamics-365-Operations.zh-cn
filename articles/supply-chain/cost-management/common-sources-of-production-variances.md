---
title: 生产差异的常见来源
description: 本文说明生产差异的每个生产类型的各个典型来源。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc310f1d5e1f99a320b803f68395d0926d39780b
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826735"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="0acd5-103">生产差异的常见来源</span><span class="sxs-lookup"><span data-stu-id="0acd5-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0acd5-104">本文说明生产差异的每个生产类型的各个典型来源。</span><span class="sxs-lookup"><span data-stu-id="0acd5-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="0acd5-105">以下是**批次规模**差异的一些典型来源：</span><span class="sxs-lookup"><span data-stu-id="0acd5-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="0acd5-106">某一生产订单的完好数量不同于在标准成本计算中使用的计算数量。</span><span class="sxs-lookup"><span data-stu-id="0acd5-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="0acd5-107">该数量提供用于摊销固定成本的基础。</span><span class="sxs-lookup"><span data-stu-id="0acd5-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="0acd5-108">生产订单固定成本的价值不同于在标准成本计算中使用的固定成本。</span><span class="sxs-lookup"><span data-stu-id="0acd5-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="0acd5-109">出于若干原因，生产订单的固定成本可能不同。</span><span class="sxs-lookup"><span data-stu-id="0acd5-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="0acd5-110">例如，固定成本可能反映以下因素：</span><span class="sxs-lookup"><span data-stu-id="0acd5-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="0acd5-111">手动更改生产物料清单 (BOM) 或工艺路线</span><span class="sxs-lookup"><span data-stu-id="0acd5-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="0acd5-112">当您创建生产订单时的不同的物料清单版本或工艺路线版本的选择</span><span class="sxs-lookup"><span data-stu-id="0acd5-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="0acd5-113">对分配给物料的物料清单版本和工艺路线版本的计划的工程更改</span><span class="sxs-lookup"><span data-stu-id="0acd5-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="0acd5-114">以下是**生产价格**差异的一些典型来源：</span><span class="sxs-lookup"><span data-stu-id="0acd5-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="0acd5-115">工艺路线工序的报告的消耗量的成本类别（及成本类别价格）不同于在标准成本计算中使用的成本类别。</span><span class="sxs-lookup"><span data-stu-id="0acd5-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="0acd5-116">成本类别价格的有效成本不同于在标准成本计算中使用的成本类别价格。</span><span class="sxs-lookup"><span data-stu-id="0acd5-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="0acd5-117">以下是**生产数量**差异的一些典型来源：</span><span class="sxs-lookup"><span data-stu-id="0acd5-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="0acd5-118">材料组件发货过多或发货不足。</span><span class="sxs-lookup"><span data-stu-id="0acd5-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="0acd5-119">针对工艺路线工序过多报告时间或过少报告时间。</span><span class="sxs-lookup"><span data-stu-id="0acd5-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="0acd5-120">您过多接收或过少接收了相对于订单数量的父物料的完好数量。</span><span class="sxs-lookup"><span data-stu-id="0acd5-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="0acd5-121">不过，您基于生产订单的订单数量将组件完全发货和完全报告工序。</span><span class="sxs-lookup"><span data-stu-id="0acd5-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="0acd5-122">以下是**生产替代**差异的一些典型来源：</span><span class="sxs-lookup"><span data-stu-id="0acd5-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="0acd5-123">您发货的材料组件不在生产物料清单中。</span><span class="sxs-lookup"><span data-stu-id="0acd5-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="0acd5-124">您手动将组件添加到生产物料清单并将该组件报告为已消耗。</span><span class="sxs-lookup"><span data-stu-id="0acd5-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="0acd5-125">您将物料报告为已消耗，但不手动将它添加到生产物料清单中。</span><span class="sxs-lookup"><span data-stu-id="0acd5-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="0acd5-126">您手动将工序添加到生产工艺路线并将该工序报告为已消耗。</span><span class="sxs-lookup"><span data-stu-id="0acd5-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="0acd5-127">在创建生产订单时您选择不同于在标准成本计算中使用的物料清单版本的物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="0acd5-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="0acd5-128">在创建生产订单时您选择不同于在标准成本计算中使用的工艺路线版本的工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="0acd5-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




