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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422909"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="2dfe2-104">成本计算级别</span><span class="sxs-lookup"><span data-stu-id="2dfe2-104">Cost calculation level</span></span>

<span data-ttu-id="2dfe2-105">名为 **成本计算级别** 的物料清单 (BOM) 级别从计算中排除生产订单和批次订单。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="2dfe2-106">系统在成本核算版本中运行成本计算时将使用此级别。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="2dfe2-107">在重新计算和库存结转等流程中，系统改用 **成本核算级别** 物料清单级别。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="2dfe2-108">以下简单场景显示了 **成本计算级别** 物料清单级别和 **成本核算级别** 物料清单级别。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="2dfe2-109">您有三个产品：A、B 和 C。产品 C 是产品 B 的组件，产品 B 是产品 A 的组件。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="2dfe2-110">**成本核算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="2dfe2-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="2dfe2-111">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="2dfe2-111">**Product A:** 0</span></span>
    - <span data-ttu-id="2dfe2-112">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="2dfe2-112">**Product B:** 1</span></span>
    - <span data-ttu-id="2dfe2-113">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="2dfe2-113">**Product C:** 2</span></span>

- <span data-ttu-id="2dfe2-114">**成本计算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="2dfe2-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="2dfe2-115">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="2dfe2-115">**Product A:** 0</span></span>
    - <span data-ttu-id="2dfe2-116">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="2dfe2-116">**Product B:** 1</span></span>
    - <span data-ttu-id="2dfe2-117">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="2dfe2-117">**Product C:** 2</span></span>

<span data-ttu-id="2dfe2-118">随后将创建产品 C 的生产订单，并将产品 A 添加到生产订单物料清单。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="2dfe2-119">估计订单后，物料清单级别将以以下方式更新：</span><span class="sxs-lookup"><span data-stu-id="2dfe2-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="2dfe2-120">**成本核算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="2dfe2-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="2dfe2-121">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="2dfe2-121">**Product B:** 1</span></span>
    - <span data-ttu-id="2dfe2-122">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="2dfe2-122">**Product C:** 2</span></span>
    - <span data-ttu-id="2dfe2-123">**产品 A：** 3</span><span class="sxs-lookup"><span data-stu-id="2dfe2-123">**Product A:** 3</span></span>

- <span data-ttu-id="2dfe2-124">**成本计算级别** 分配以下物料清单级别：</span><span class="sxs-lookup"><span data-stu-id="2dfe2-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="2dfe2-125">**产品 A：** 0</span><span class="sxs-lookup"><span data-stu-id="2dfe2-125">**Product A:** 0</span></span>
    - <span data-ttu-id="2dfe2-126">**产品 B：** 1</span><span class="sxs-lookup"><span data-stu-id="2dfe2-126">**Product B:** 1</span></span>
    - <span data-ttu-id="2dfe2-127">**产品 C：** 2</span><span class="sxs-lookup"><span data-stu-id="2dfe2-127">**Product C:** 2</span></span>

<span data-ttu-id="2dfe2-128">此行为可确保对生产订单物料单的更改不会影响后续的成本计算。</span><span class="sxs-lookup"><span data-stu-id="2dfe2-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
