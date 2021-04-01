---
title: 指定如何处置退回物料
description: 指定如何处置退回物料。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242365"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="68874-103">指定如何处置退回物料</span><span class="sxs-lookup"><span data-stu-id="68874-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="68874-104">在您处理退货单时，必须指定一个退货原因代码来标识产品被退回的原因。</span><span class="sxs-lookup"><span data-stu-id="68874-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="68874-105">您还必须指定一个处置代码和处置操作代码来确定该如何处理被退回的产品。</span><span class="sxs-lookup"><span data-stu-id="68874-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="68874-106">在以下情况下应用处置代码：创建退货单时，登记物料到达或对物料到达执行装箱单更新时，以及结束某一检验单时。</span><span class="sxs-lookup"><span data-stu-id="68874-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="68874-107">您可以定义为支持业务流程所需的任何处置代码。</span><span class="sxs-lookup"><span data-stu-id="68874-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="68874-108">下表提供可分配给退回物料处置的一组常用的代码。</span><span class="sxs-lookup"><span data-stu-id="68874-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68874-109">处置类型</span><span class="sxs-lookup"><span data-stu-id="68874-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="68874-110">常用代码</span><span class="sxs-lookup"><span data-stu-id="68874-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="68874-111">描述</span><span class="sxs-lookup"><span data-stu-id="68874-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68874-112">处置</span><span class="sxs-lookup"><span data-stu-id="68874-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="68874-113">SC</span><span class="sxs-lookup"><span data-stu-id="68874-113">SC</span></span></p></td>
<td><p><span data-ttu-id="68874-114">报废/销毁</span><span class="sxs-lookup"><span data-stu-id="68874-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-115">处置</span><span class="sxs-lookup"><span data-stu-id="68874-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="68874-116">DC</span><span class="sxs-lookup"><span data-stu-id="68874-116">DC</span></span></p></td>
<td><p><span data-ttu-id="68874-117">捐赠给慈善机构</span><span class="sxs-lookup"><span data-stu-id="68874-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-118">处置</span><span class="sxs-lookup"><span data-stu-id="68874-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="68874-119">TD</span><span class="sxs-lookup"><span data-stu-id="68874-119">TD</span></span></p></td>
<td><p><span data-ttu-id="68874-120">第三方处置</span><span class="sxs-lookup"><span data-stu-id="68874-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-121">处置</span><span class="sxs-lookup"><span data-stu-id="68874-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="68874-122">SL</span><span class="sxs-lookup"><span data-stu-id="68874-122">SL</span></span></p></td>
<td><p><span data-ttu-id="68874-123">废物处理</span><span class="sxs-lookup"><span data-stu-id="68874-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-124">处置</span><span class="sxs-lookup"><span data-stu-id="68874-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="68874-125">TS</span><span class="sxs-lookup"><span data-stu-id="68874-125">TS</span></span></p></td>
<td><p><span data-ttu-id="68874-126">第三方销售（二级市场）</span><span class="sxs-lookup"><span data-stu-id="68874-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-127">维修/修改</span><span class="sxs-lookup"><span data-stu-id="68874-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="68874-128">RW</span><span class="sxs-lookup"><span data-stu-id="68874-128">RW</span></span></p></td>
<td><p><span data-ttu-id="68874-129">返工</span><span class="sxs-lookup"><span data-stu-id="68874-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-130">维修/修改</span><span class="sxs-lookup"><span data-stu-id="68874-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="68874-131">RF</span><span class="sxs-lookup"><span data-stu-id="68874-131">RF</span></span></p></td>
<td><p><span data-ttu-id="68874-132">再制造/翻新</span><span class="sxs-lookup"><span data-stu-id="68874-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-133">维修/修改</span><span class="sxs-lookup"><span data-stu-id="68874-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="68874-134">MD</span><span class="sxs-lookup"><span data-stu-id="68874-134">MD</span></span></p></td>
<td><p><span data-ttu-id="68874-135">修改</span><span class="sxs-lookup"><span data-stu-id="68874-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-136">维修/修改</span><span class="sxs-lookup"><span data-stu-id="68874-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="68874-137">RP</span><span class="sxs-lookup"><span data-stu-id="68874-137">RP</span></span></p></td>
<td><p><span data-ttu-id="68874-138">维修</span><span class="sxs-lookup"><span data-stu-id="68874-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-139">维修/修改</span><span class="sxs-lookup"><span data-stu-id="68874-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="68874-140">RV</span><span class="sxs-lookup"><span data-stu-id="68874-140">RV</span></span></p></td>
<td><p><span data-ttu-id="68874-141">退回给供应商</span><span class="sxs-lookup"><span data-stu-id="68874-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-142">其他</span><span class="sxs-lookup"><span data-stu-id="68874-142">Other</span></span></p></td>
<td><p><span data-ttu-id="68874-143">AI</span><span class="sxs-lookup"><span data-stu-id="68874-143">AI</span></span></p></td>
<td><p><span data-ttu-id="68874-144">按原样使用</span><span class="sxs-lookup"><span data-stu-id="68874-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-145">其他</span><span class="sxs-lookup"><span data-stu-id="68874-145">Other</span></span></p></td>
<td><p><span data-ttu-id="68874-146">RS</span><span class="sxs-lookup"><span data-stu-id="68874-146">RS</span></span></p></td>
<td><p><span data-ttu-id="68874-147">转卖</span><span class="sxs-lookup"><span data-stu-id="68874-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-148">其他</span><span class="sxs-lookup"><span data-stu-id="68874-148">Other</span></span></p></td>
<td><p><span data-ttu-id="68874-149">EX</span><span class="sxs-lookup"><span data-stu-id="68874-149">EX</span></span></p></td>
<td><p><span data-ttu-id="68874-150">交换</span><span class="sxs-lookup"><span data-stu-id="68874-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-151">其他</span><span class="sxs-lookup"><span data-stu-id="68874-151">Other</span></span></p></td>
<td><p><span data-ttu-id="68874-152">毫秒</span><span class="sxs-lookup"><span data-stu-id="68874-152">MS</span></span></p></td>
<td><p><span data-ttu-id="68874-153">杂项</span><span class="sxs-lookup"><span data-stu-id="68874-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="68874-154">对于您定义的每个处置代码，您必须选择一个处置操作。</span><span class="sxs-lookup"><span data-stu-id="68874-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="68874-155">处置行为决定处置代码的实际和财务影响。</span><span class="sxs-lookup"><span data-stu-id="68874-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="68874-156">例如，处置代码确定了被退回物品的实际处理方法，被退回物品所产生的财务影响，以及是否必须将更换物品发送给客户。</span><span class="sxs-lookup"><span data-stu-id="68874-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="68874-157">您可以根据业务需要定义数目不限的处置代码，但是仅六个预定义的处置操作可供选择。</span><span class="sxs-lookup"><span data-stu-id="68874-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="68874-158">下表介绍的是处置操作及其定义。</span><span class="sxs-lookup"><span data-stu-id="68874-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68874-159">处置操作</span><span class="sxs-lookup"><span data-stu-id="68874-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="68874-160">说明</span><span class="sxs-lookup"><span data-stu-id="68874-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68874-161"><strong>贷记</strong></span><span class="sxs-lookup"><span data-stu-id="68874-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-162">将物品归入库存并贷记客户。</span><span class="sxs-lookup"><span data-stu-id="68874-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-163"><strong>只贷记</strong></span><span class="sxs-lookup"><span data-stu-id="68874-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-164">贷记客户，不要求或期待客户退回物品。</span><span class="sxs-lookup"><span data-stu-id="68874-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-165"><strong>报废</strong></span><span class="sxs-lookup"><span data-stu-id="68874-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-166">报废物品并贷记客户。</span><span class="sxs-lookup"><span data-stu-id="68874-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-167"><strong>更换并贷记</strong></span><span class="sxs-lookup"><span data-stu-id="68874-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-168">将物品退回库存，创建更换单并贷记客户。</span><span class="sxs-lookup"><span data-stu-id="68874-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68874-169"><strong>更换并报废</strong></span><span class="sxs-lookup"><span data-stu-id="68874-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-170">报废物品，创建更换单，并且贷记客户。</span><span class="sxs-lookup"><span data-stu-id="68874-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68874-171"><strong>返还客户</strong></span><span class="sxs-lookup"><span data-stu-id="68874-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="68874-172">拒绝所退回的物品，并将它退给客户。</span><span class="sxs-lookup"><span data-stu-id="68874-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="68874-173">为检验单选择处置代码</span><span class="sxs-lookup"><span data-stu-id="68874-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="68874-174">单击 **库存管理** \> **定期** \> **质量管理** \> **检验单**。</span><span class="sxs-lookup"><span data-stu-id="68874-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="68874-175">对于现有检验单，请从 **概述** 选项卡上的 **处置代码** 字段中选择某一操作。</span><span class="sxs-lookup"><span data-stu-id="68874-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="68874-176">请参阅</span><span class="sxs-lookup"><span data-stu-id="68874-176">See also</span></span>

<span data-ttu-id="68874-177">[检验单（窗体）](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="68874-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="68874-178">[处置代码（窗体）](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="68874-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]