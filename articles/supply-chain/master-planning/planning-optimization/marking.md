---
title: 通过计划优化进行库存标记
description: 本主题提供有关可用于在使用计划优化时在确认订单中标记库存的选项的信息。
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263342"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="a677c-103">通过计划优化进行库存标记</span><span class="sxs-lookup"><span data-stu-id="a677c-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a677c-104">本主题提供有关可用于在使用计划优化时在确认订单中标记库存的选项的信息。</span><span class="sxs-lookup"><span data-stu-id="a677c-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="a677c-105">*标记* 用于链接供应和需求。</span><span class="sxs-lookup"><span data-stu-id="a677c-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="a677c-106">它类似于 *限定标准*，指示主计划预计如何满足需求。</span><span class="sxs-lookup"><span data-stu-id="a677c-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="a677c-107">从计划的角度看，主要区别在于标记比限定标准更具永久性。</span><span class="sxs-lookup"><span data-stu-id="a677c-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="a677c-108">引入标记以支持先进先出 (FIFO) 和后进先出 (LIFO) 的特殊成本计算方案。</span><span class="sxs-lookup"><span data-stu-id="a677c-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="a677c-109">但是，它现在还用于某些非成本计算方案。</span><span class="sxs-lookup"><span data-stu-id="a677c-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="a677c-110">供应和需求之间的标记是可选的，并且几乎是永久的。</span><span class="sxs-lookup"><span data-stu-id="a677c-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="a677c-111">标记可以由用户手动删除，也可以通过运行在其中选择 **删除标记** 选项的销售订单行分解来删除。</span><span class="sxs-lookup"><span data-stu-id="a677c-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="a677c-112">限定标准在覆盖范围期间由主计划控制，以将需求与所需供应链接在一起。</span><span class="sxs-lookup"><span data-stu-id="a677c-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="a677c-113">可针对每个计划运行限定标准，以优化满足需求所需的供应。</span><span class="sxs-lookup"><span data-stu-id="a677c-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="a677c-114">当主计划更新限定标准信息时，它将遵守任何现有标记。</span><span class="sxs-lookup"><span data-stu-id="a677c-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="a677c-115">限定标准首先包括相关标记、现有数量预留和在单数量预留，顺序如下：</span><span class="sxs-lookup"><span data-stu-id="a677c-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="a677c-116">需求和供应之间的标记</span><span class="sxs-lookup"><span data-stu-id="a677c-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="a677c-117">现有数量预留</span><span class="sxs-lookup"><span data-stu-id="a677c-117">On-hand reservations</span></span>
1. <span data-ttu-id="a677c-118">在单数量预留</span><span class="sxs-lookup"><span data-stu-id="a677c-118">On-order reservations</span></span>

<span data-ttu-id="a677c-119">确认计划订单后，**确认** 对话框提供用于为在确认期间创建的订单设置标记选项的 **更新标记** 字段。</span><span class="sxs-lookup"><span data-stu-id="a677c-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="a677c-120">选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="a677c-120">Select one of the following values:</span></span>

- <span data-ttu-id="a677c-121">**无** – 不应用库存标记。</span><span class="sxs-lookup"><span data-stu-id="a677c-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="a677c-122">**标准** – 根据限定标准更新库存标记。</span><span class="sxs-lookup"><span data-stu-id="a677c-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="a677c-123">针对履行订单（供应）标记需求订单（需求）。</span><span class="sxs-lookup"><span data-stu-id="a677c-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="a677c-124">如果履行订单上还有一些数量，不会对其进行标记，并且参考信息将保留为空白。</span><span class="sxs-lookup"><span data-stu-id="a677c-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="a677c-125">例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将仅分配给销售订单。</span><span class="sxs-lookup"><span data-stu-id="a677c-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="a677c-126">**扩展** – 同时标记需求订单（需求）和履行订单（供应），不管履行订单上仍然存在的任何数量。</span><span class="sxs-lookup"><span data-stu-id="a677c-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="a677c-127">例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将分配给销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="a677c-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]