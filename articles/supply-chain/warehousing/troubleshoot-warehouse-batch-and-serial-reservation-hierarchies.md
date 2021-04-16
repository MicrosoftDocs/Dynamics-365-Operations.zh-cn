---
title: 仓库批次和序列预留层次结构故障排除
description: 本主题介绍如何解决在处理使用批次或序列维度的预留层次结构时可能遇到的常见问题。
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838170"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="bd43a-103">仓库批次和序列预留层次结构故障排除</span><span class="sxs-lookup"><span data-stu-id="bd43a-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd43a-104">本主题介绍如何解决在处理使用批次或序列维度的预留层次结构时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="bd43a-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="bd43a-105">有关详细信息，请参阅[灵活的仓库级维度预留策略](flexible-warehouse-level-dimension-reservation.md)。</span><span class="sxs-lookup"><span data-stu-id="bd43a-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="bd43a-106">物料的预留层次结构指示，必须满足存储维度的要求才能将库位分配到需求订单。</span><span class="sxs-lookup"><span data-stu-id="bd43a-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="bd43a-107">对于在分配库位之前必须满足的所有维度，这些维度可以描述为 *库位上方的维度*；对于可以在库位分配到需求订单之后分配的维度，这些维度可以描述为 *库位下方的维度*。</span><span class="sxs-lookup"><span data-stu-id="bd43a-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="bd43a-108">这些预留层次结构也称为 *batch-above* 和 *batch-below* 预留层次结构，或者 *serial-above* 和 *serial-below* 预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="bd43a-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="bd43a-109">仅在库位上方的维度中没有间隙时才能成功分配库存。</span><span class="sxs-lookup"><span data-stu-id="bd43a-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="bd43a-110">例如，在 *batch-above* 预留层次结构中，您希望在需求订单上指定 **场地**、**仓库** 和 **批号** 维度。</span><span class="sxs-lookup"><span data-stu-id="bd43a-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="bd43a-111">如果缺少其中任何维度，分配流程将失败。</span><span class="sxs-lookup"><span data-stu-id="bd43a-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="bd43a-112">相反，在 *batch-below* 或 *serial-below* 预留层次结构中，可能在需求订单上指定批号或序列号，但分配流程不需要它。</span><span class="sxs-lookup"><span data-stu-id="bd43a-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="bd43a-113">我收到以下错误消息：“要分配到波次，负荷行必须指定位置以上的维度。</span><span class="sxs-lookup"><span data-stu-id="bd43a-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="bd43a-114">要分配这些维度，请预留并重新创建负荷行。”</span><span class="sxs-lookup"><span data-stu-id="bd43a-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bd43a-115">问题描述</span><span class="sxs-lookup"><span data-stu-id="bd43a-115">Issue description</span></span>

<span data-ttu-id="bd43a-116">当您使用具有 *batch-above* 预留层次结构的物料时，如果尝试发放部分数量的装载，**装载计划工作台** 页面的 **发放到仓库** 命令将不起作用。</span><span class="sxs-lookup"><span data-stu-id="bd43a-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="bd43a-117">您将收到此错误消息，而且不会为部分数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="bd43a-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="bd43a-118">但是，当您使用具有 *batch-below* 预留层次结构的物料时，您可以从 **装载计划工作台** 页面发放部分数量的装载。</span><span class="sxs-lookup"><span data-stu-id="bd43a-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="bd43a-119">问题原因</span><span class="sxs-lookup"><span data-stu-id="bd43a-119">Issue cause</span></span>

<span data-ttu-id="bd43a-120">当某个维度在预留层次结构中位于 **库位** 维度上方时，必须在发放到仓库之前指定该维度。</span><span class="sxs-lookup"><span data-stu-id="bd43a-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="bd43a-121">如果未指定一个或多个 **位置** 以上维度，部分数量无法发放。</span><span class="sxs-lookup"><span data-stu-id="bd43a-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="bd43a-122">即使有可用库存，也会触发批号的自动预留提示。</span><span class="sxs-lookup"><span data-stu-id="bd43a-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bd43a-123">问题描述</span><span class="sxs-lookup"><span data-stu-id="bd43a-123">Issue description</span></span>

<span data-ttu-id="bd43a-124">当您在未启用仓库流程但启用了自动预留的仓库中使用具有 *batch-above* 预留层次结构的物料时，即使只有一个批次可供领料，也会显示批号的自动预留提示。</span><span class="sxs-lookup"><span data-stu-id="bd43a-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="bd43a-125">但是，当您在启用了仓库流程的仓库中使用同一物料时，不会显示自动预留提示。</span><span class="sxs-lookup"><span data-stu-id="bd43a-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="bd43a-126">问题原因</span><span class="sxs-lookup"><span data-stu-id="bd43a-126">Issue cause</span></span>

<span data-ttu-id="bd43a-127">如果预留层次结构定义为 *batch-above* 或 *serial-above* ，必须始终在需求订单上指定引用的维度（**批号** 或 **序列号**）。</span><span class="sxs-lookup"><span data-stu-id="bd43a-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="bd43a-128">如果单个批号或序列号可用，则仓库流程可能能够完成信息。</span><span class="sxs-lookup"><span data-stu-id="bd43a-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="bd43a-129">但是，由于没有为仓库流程启用仓库，因此用户必须始终指定 **库位** 上方的所有维度。</span><span class="sxs-lookup"><span data-stu-id="bd43a-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="bd43a-130">具有“考虑现有”时隙标准的时隙模板不考虑启用批次的物料的当前现有库存。</span><span class="sxs-lookup"><span data-stu-id="bd43a-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="bd43a-131">有关详细信息，请参阅[仓库时隙](warehouse-slotting.md)。</span><span class="sxs-lookup"><span data-stu-id="bd43a-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="bd43a-132">问题描述</span><span class="sxs-lookup"><span data-stu-id="bd43a-132">Issue description</span></span>

<span data-ttu-id="bd43a-133">具有 *考虑现有* 时隙标准的时隙模板不考虑 *batch-above* 物料的当前现有库存。</span><span class="sxs-lookup"><span data-stu-id="bd43a-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="bd43a-134">它们仅在销售订单行上指定了批号时才考虑。</span><span class="sxs-lookup"><span data-stu-id="bd43a-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="bd43a-135">但是，当您使用 *batch-below* 物料时，将按预期考虑当前的现有库存。</span><span class="sxs-lookup"><span data-stu-id="bd43a-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="bd43a-136">问题原因</span><span class="sxs-lookup"><span data-stu-id="bd43a-136">Issue cause</span></span>

<span data-ttu-id="bd43a-137">可以为 *已订购*、*已预留* 或 *已发放* 需求策略定义时隙模板标题。</span><span class="sxs-lookup"><span data-stu-id="bd43a-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="bd43a-138">对于 *已订购* 需求策略，将应用适用于预留或发放到仓库流程的相同预留层次结构要求。</span><span class="sxs-lookup"><span data-stu-id="bd43a-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="bd43a-139">因此，对于具有 *batch-above* 和 *serial-below* 预留层次结构的物料，必须在需求订单（销售或转移）上指定批号或序列号。</span><span class="sxs-lookup"><span data-stu-id="bd43a-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="bd43a-140">或者，可以使用 *已预留* 需求策略在生成仓库时隙需求之前选择批号或序列号。</span><span class="sxs-lookup"><span data-stu-id="bd43a-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
