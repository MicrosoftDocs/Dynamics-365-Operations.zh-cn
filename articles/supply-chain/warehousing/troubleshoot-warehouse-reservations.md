---
title: 仓库管理中的预留疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
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
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993837"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="bde15-103">仓库管理中的预留疑难解答</span><span class="sxs-lookup"><span data-stu-id="bde15-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde15-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="bde15-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="bde15-105">我收到以下错误消息：“已创建了依赖预留的工作，因此无法删除这些预留。”</span><span class="sxs-lookup"><span data-stu-id="bde15-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bde15-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="bde15-106">Issue description</span></span>

<span data-ttu-id="bde15-107">您不能在销售行上取消库存的预留，因为该行有未结工作。</span><span class="sxs-lookup"><span data-stu-id="bde15-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bde15-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="bde15-108">Issue resolution</span></span>

<span data-ttu-id="bde15-109">调查是否存在要将物料从装箱工作站运送到另一个位置（如 *货架门*）的未结包装组工作。</span><span class="sxs-lookup"><span data-stu-id="bde15-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="bde15-110">查看 **工作创建历史记录日志** 和 **工作详细信息** 页的记录，确定哪个工作在实际预留库存，然后完成或删除工作，释放预留。</span><span class="sxs-lookup"><span data-stu-id="bde15-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="bde15-111">我收到以下错误消息：“库存数量 -%1 由于物料 %2 的库存交易不足无法更新....”</span><span class="sxs-lookup"><span data-stu-id="bde15-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bde15-112">问题描述</span><span class="sxs-lookup"><span data-stu-id="bde15-112">Issue description</span></span>

<span data-ttu-id="bde15-113">如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="bde15-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="bde15-114">以下是完整错误消息的完整文本：</span><span class="sxs-lookup"><span data-stu-id="bde15-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="bde15-115">库存数量 -%1 由于批次 ID %12 上的物料 %2（维度为尺寸=%3、颜色=%4、附加物=%5、站点%6、仓库=%7、位置=%8、库存状态=可用、牌照=%9、引用 ID %11 的批处理号=%10）的库存交易不足无法更新。</span><span class="sxs-lookup"><span data-stu-id="bde15-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bde15-116">解决问题</span><span class="sxs-lookup"><span data-stu-id="bde15-116">Issue resolution</span></span>

<span data-ttu-id="bde15-117">请确保没有库存交易在实际预留数量。</span><span class="sxs-lookup"><span data-stu-id="bde15-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="bde15-118">例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。</span><span class="sxs-lookup"><span data-stu-id="bde15-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="bde15-119">我收到以下错误消息：“实际现有量...无法预留，因为库存中只有 0.00。”</span><span class="sxs-lookup"><span data-stu-id="bde15-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bde15-120">问题描述</span><span class="sxs-lookup"><span data-stu-id="bde15-120">Issue description</span></span>

<span data-ttu-id="bde15-121">如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="bde15-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="bde15-122">以下是完整错误消息的完整文本：</span><span class="sxs-lookup"><span data-stu-id="bde15-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="bde15-123">实际现有量站点=%1、仓库=%2、库存状态=可用、批处理号=%3、所有者=%4：%5 无法预留，因为库存中只有 0.00。</span><span class="sxs-lookup"><span data-stu-id="bde15-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bde15-124">解决问题</span><span class="sxs-lookup"><span data-stu-id="bde15-124">Issue resolution</span></span>

<span data-ttu-id="bde15-125">此问题可能是由于未结工作引起的。</span><span class="sxs-lookup"><span data-stu-id="bde15-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="bde15-126">请完成工作或在不创建工作时接收。</span><span class="sxs-lookup"><span data-stu-id="bde15-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="bde15-127">请确保没有库存交易在实际预留数量。</span><span class="sxs-lookup"><span data-stu-id="bde15-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="bde15-128">例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。</span><span class="sxs-lookup"><span data-stu-id="bde15-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="bde15-129">我收到以下错误消息：“要分配到波次，负荷行必须指定位置以上的维度。</span><span class="sxs-lookup"><span data-stu-id="bde15-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="bde15-130">要分配这些维度，请预留并重新创建负荷行。”</span><span class="sxs-lookup"><span data-stu-id="bde15-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bde15-131">问题描述</span><span class="sxs-lookup"><span data-stu-id="bde15-131">Issue description</span></span>

<span data-ttu-id="bde15-132">当您使用具有“批以上”预留层次结构的物料（**批处理号** 维度放在 **位置** 维度 *以上*）时，部分数量的 **负荷计划工作台** 页的 **发放到仓库** 命令将不起作用。</span><span class="sxs-lookup"><span data-stu-id="bde15-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="bde15-133">您将收到此错误消息，而且不会为部分数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="bde15-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="bde15-134">但是，如果您使用具有“批以下”预留层次结构的物料（**批处理号** 维度放在 **位置** 维度 *以下*）时，您可以从部分数量的 **负荷计划工作台** 页发放负荷。</span><span class="sxs-lookup"><span data-stu-id="bde15-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bde15-135">解决问题</span><span class="sxs-lookup"><span data-stu-id="bde15-135">Issue resolution</span></span>

<span data-ttu-id="bde15-136">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="bde15-136">This behavior is by design.</span></span> <span data-ttu-id="bde15-137">如果您在预留层次结构中将维度放在 **位置** 维度以上，则必须在发放到仓库之前指定该维度。</span><span class="sxs-lookup"><span data-stu-id="bde15-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="bde15-138">Microsoft 已评估此问题，确定这是从负荷计划工作台发放到仓库期间存在的功能限制。</span><span class="sxs-lookup"><span data-stu-id="bde15-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="bde15-139">如果未指定一个或多个 **位置** 以上维度，部分数量无法发放。</span><span class="sxs-lookup"><span data-stu-id="bde15-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="bde15-140">有关详细信息，请参阅[灵活的仓库级维度预留策略](flexible-warehouse-level-dimension-reservation.md)。</span><span class="sxs-lookup"><span data-stu-id="bde15-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
