---
title: 即时补货
description: 本主题介绍如何在位置指令无法分配库存时使用即时补货为库存补货。
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 6e2919c003d1dc67b988345260b2747364752222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004769"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="32588-103">即时补货</span><span class="sxs-lookup"><span data-stu-id="32588-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32588-104">位置指令行无法分配库存时，可立即通过即时补货为库存补货。</span><span class="sxs-lookup"><span data-stu-id="32588-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="32588-105">这种补货基于位置指令设置中的一行。</span><span class="sxs-lookup"><span data-stu-id="32588-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="32588-106">如果库存现货的度量单位不是该行指定的度量单位，将立即使用该度量单位补货。</span><span class="sxs-lookup"><span data-stu-id="32588-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="32588-107">即时补货可以替代以下方法：库存分配基于位置指令中的多行，以及需求在分配结束时汇总，并使用位置指令中最后一行指定的度量单位补货。</span><span class="sxs-lookup"><span data-stu-id="32588-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="32588-108">使用即时补货的优点时可以按特定单位限制补货，并且可指示从特定位置领取数量。</span><span class="sxs-lookup"><span data-stu-id="32588-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="32588-109">业务方案</span><span class="sxs-lookup"><span data-stu-id="32588-109">Business scenario</span></span>

<span data-ttu-id="32588-110">例如，您有一个仓库有单独的领料区域，这些区域采用“箱”和“单件”度量单位。</span><span class="sxs-lookup"><span data-stu-id="32588-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="32588-111">您希望通过尽量以箱为单位领料，然后从“单件”区域领取不足一箱的剩余数量，优化领料过程。</span><span class="sxs-lookup"><span data-stu-id="32588-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="32588-112">在这种情况下，可以使用即时补货。</span><span class="sxs-lookup"><span data-stu-id="32588-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="32588-113">在位置指令中，可为箱设置即时补货，这样只要需求数量的可领料箱数不足，就会立即使用需求补货。</span><span class="sxs-lookup"><span data-stu-id="32588-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="32588-114">通过这种方法，就优化了领料过程，所以领料中包含尽可能多的箱数。</span><span class="sxs-lookup"><span data-stu-id="32588-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="32588-115">即时补货将生成以箱为单位的补货，而需求不会传递，所以将以“单件”度量单位领取数量。</span><span class="sxs-lookup"><span data-stu-id="32588-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="32588-116">换言之，将从“单件”区域仅领取应以“单件”度量单位领取的数量（即不足一箱的数量）。</span><span class="sxs-lookup"><span data-stu-id="32588-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="32588-117">如果“箱”区域中产品短缺，则可领取总需求中尽量多箱的产品。</span><span class="sxs-lookup"><span data-stu-id="32588-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="32588-118">然后从“单件”区域领取其余数量。</span><span class="sxs-lookup"><span data-stu-id="32588-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="32588-119">适用情况</span><span class="sxs-lookup"><span data-stu-id="32588-119">Where it applies</span></span>

<span data-ttu-id="32588-120">如果设置了补货模板的位置指令行的分配失败，则在执行波次期间使用即时补货。</span><span class="sxs-lookup"><span data-stu-id="32588-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="32588-121">设置即时补货</span><span class="sxs-lookup"><span data-stu-id="32588-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="32588-122">转至 **仓库管理** \> **设置** \> **位置指令**，然后在 **行** 选项卡的 **即时补货模板** 列表中为波形需求选择补货模板。</span><span class="sxs-lookup"><span data-stu-id="32588-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="32588-123">如果位置指令行未能分配专用度量单位，则应用补货模板。</span><span class="sxs-lookup"><span data-stu-id="32588-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="32588-124">疑难解答</span><span class="sxs-lookup"><span data-stu-id="32588-124">Troubleshooting</span></span>

<span data-ttu-id="32588-125">如果为位置指令行选择了即时补货，但是对该位置指令行使用需求补货模板时未生成补货工作，则必须调查下面的两种主要原因：</span><span class="sxs-lookup"><span data-stu-id="32588-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="32588-126">确保应用的需求补货模板设置为使用 **补货** 类型的正确位置模板和工作模板。</span><span class="sxs-lookup"><span data-stu-id="32588-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="32588-127">确保需求补货模板在其中为补货搜索现货库存的位置中现货库存充足。</span><span class="sxs-lookup"><span data-stu-id="32588-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
