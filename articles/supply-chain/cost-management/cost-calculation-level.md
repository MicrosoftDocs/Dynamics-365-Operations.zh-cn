---
title: 成本计算级别
description: 本主题介绍名为“成本计算级别”的物料清单 (BOM) 级别。 此物料清单级别从计算中排除了生产订单和批次订单。
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251018"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="ce4d7-104">成本计算级别</span><span class="sxs-lookup"><span data-stu-id="ce4d7-104">Cost calculation level</span></span>

<span data-ttu-id="ce4d7-105">名为 **成本计算级别** 的物料清单 (BOM) 级别从计算中排除生产订单和批次订单。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="ce4d7-106">系统在成本核算版本中运行成本计算时将使用此级别。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="ce4d7-107">在重新计算和库存结转等流程中，系统改用 **成本核算级别** 物料清单级别。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="ce4d7-108">以下简单场景显示了 **成本计算级别** 物料清单级别和 **成本核算级别** 物料清单级别。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="ce4d7-109">您有三个产品：A、B 和 C。产品 C 是产品 B 的组件，产品 B 是产品 A 的组件。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="ce4d7-110">**成本核算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="ce4d7-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ce4d7-111">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="ce4d7-111">**Product A:** 0</span></span>
    - <span data-ttu-id="ce4d7-112">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="ce4d7-112">**Product B:** 1</span></span>
    - <span data-ttu-id="ce4d7-113">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="ce4d7-113">**Product C:** 2</span></span>

- <span data-ttu-id="ce4d7-114">**成本计算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="ce4d7-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ce4d7-115">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="ce4d7-115">**Product A:** 0</span></span>
    - <span data-ttu-id="ce4d7-116">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="ce4d7-116">**Product B:** 1</span></span>
    - <span data-ttu-id="ce4d7-117">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="ce4d7-117">**Product C:** 2</span></span>

<span data-ttu-id="ce4d7-118">随后将创建产品 C 的生产订单，并将产品 A 添加到生产订单物料清单。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="ce4d7-119">估计订单后，物料清单级别将以以下方式更新：</span><span class="sxs-lookup"><span data-stu-id="ce4d7-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="ce4d7-120">**成本核算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="ce4d7-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ce4d7-121">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="ce4d7-121">**Product B:** 1</span></span>
    - <span data-ttu-id="ce4d7-122">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="ce4d7-122">**Product C:** 2</span></span>
    - <span data-ttu-id="ce4d7-123">**产品 A：** 3</span><span class="sxs-lookup"><span data-stu-id="ce4d7-123">**Product A:** 3</span></span>

- <span data-ttu-id="ce4d7-124">**成本计算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="ce4d7-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="ce4d7-125">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="ce4d7-125">**Product A:** 0</span></span>
    - <span data-ttu-id="ce4d7-126">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="ce4d7-126">**Product B:** 1</span></span>
    - <span data-ttu-id="ce4d7-127">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="ce4d7-127">**Product C:** 2</span></span>

<span data-ttu-id="ce4d7-128">此行为可确保对生产订单物料单的更改不会影响后续的成本计算。</span><span class="sxs-lookup"><span data-stu-id="ce4d7-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]