---
title: 包装材料和费用
description: 此主题介绍按特定间隔支付给回收公司的包装材料费用。
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b9ca8653bb3dc00285774d4ead9a8c14c606f24
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234721"
---
# <a name="packing-materials-and-fees"></a><span data-ttu-id="c40eb-103">包装材料和费用</span><span class="sxs-lookup"><span data-stu-id="c40eb-103">Packing materials and fees</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c40eb-104">按特定间隔向回收公司支付包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-104">Packing material fees are paid to a recycling company at specific intervals.</span></span> <span data-ttu-id="c40eb-105">为包装单位中包含的每种材料支付每个单位重量的金额。</span><span class="sxs-lookup"><span data-stu-id="c40eb-105">An amount is paid, per unit of weight, for each material that a packing unit consists of.</span></span> <span data-ttu-id="c40eb-106">虽然程序将计算和报告包装材料费用，但是不过帐分录，因为没有将这些费用视为必须向主管机构缴纳的税款。</span><span class="sxs-lookup"><span data-stu-id="c40eb-106">Although packing material fees are calculated and reported, no ledger transactions are posted, because the fees aren't considered taxes that must be paid to an authority.</span></span>

<span data-ttu-id="c40eb-107">程序将为销售订单行和采购订单行计算包装材料重量和费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-107">Packing material weights and fees are calculated for sales order lines and purchase order lines.</span></span>

<span data-ttu-id="c40eb-108">可以为一种物料、一组物料（包装组）或所有物料定义一个或多个包装单位。</span><span class="sxs-lookup"><span data-stu-id="c40eb-108">You can define one or more packing units for a single item, a group of items (packing group), or all items.</span></span> <span data-ttu-id="c40eb-109">包装单位包含包装材料、其重量和该包装单位中包括的物料数量。</span><span class="sxs-lookup"><span data-stu-id="c40eb-109">A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit.</span></span> <span data-ttu-id="c40eb-110">将包装材料代码分配给定义的包装材料的每种类型。</span><span class="sxs-lookup"><span data-stu-id="c40eb-110">A packing material code is assigned to each type of packing material that is defined.</span></span> <span data-ttu-id="c40eb-111">根据包装材料代码，您可以指定特定期间的价格。</span><span class="sxs-lookup"><span data-stu-id="c40eb-111">Based on the packing material code, you can specify a price for a specific period.</span></span> <span data-ttu-id="c40eb-112">基于此信息计算包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-112">The packing material fee is calculated based on this information.</span></span>

> [!NOTE]
> <span data-ttu-id="c40eb-113">即使您的公司不支付包装材料费用，您也可以使用此功能来计算包装材料重量的统计。</span><span class="sxs-lookup"><span data-stu-id="c40eb-113">Even if your company doesn't pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials.</span></span>

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a><span data-ttu-id="c40eb-114">设置包装材料分配</span><span class="sxs-lookup"><span data-stu-id="c40eb-114">Set up packing material allocation</span></span>

<span data-ttu-id="c40eb-115">必须先开启计算和定义哪些材料和费用适用于哪些物料，才能计算包装材料的重量和/或费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-115">Before you can calculate packing material weights, packing material fees, or both, you must turn on the calculation and define which materials and fees apply to which items.</span></span>

1. <span data-ttu-id="c40eb-116">转到 **库存管理 \> 设置 \> 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-116">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="c40eb-117">在 **常规** 选项卡的 **包装材料** 部分中，将 **计算包装材料费用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-117">On the **General** tab, in the **Packing material** section, set the **Calculate packing material fees** option to **Yes**.</span></span>
1. <span data-ttu-id="c40eb-118">转到 **库存管理 \> 设置 \> 包装材料 \> 包装组**，然后创建您使用的所有包装组。</span><span class="sxs-lookup"><span data-stu-id="c40eb-118">Go to **Inventory management \> Setup \> Packing material \> Packing groups**, and create all the packing groups that you use.</span></span> <span data-ttu-id="c40eb-119">包装组中的所有物料都将使用相同的包装材料分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-119">All the items in a packing group will use the same packing material allocation.</span></span> <span data-ttu-id="c40eb-120">如果不使用包装组，可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="c40eb-120">If you don't use packing groups, you can skip this step.</span></span>

    > [!TIP]
    > <span data-ttu-id="c40eb-121">创建包装组之后，可以根据需要为每个产品分配组。</span><span class="sxs-lookup"><span data-stu-id="c40eb-121">After you've created your packing groups, can assign a group to each product as you require.</span></span> <span data-ttu-id="c40eb-122">转到 **产品信息管理 \> 产品 \> 已发布产品**，选择产品，然后在 **管理库存** 快速选项卡的 **包装组** 字段中，选择相应包装组。</span><span class="sxs-lookup"><span data-stu-id="c40eb-122">Go to **Product information management \> Products \> Released products**, select a product, and then, on the **Manage inventory** FastTab, in the **Packing group** field, select the appropriate packing group.</span></span>

1. <span data-ttu-id="c40eb-123">转到 **库存管理 \> 设置 \> 包装材料 \> 包装材料代码**，定义使用的每种包装材料，然后指定准备装运时所用包装材料单位。</span><span class="sxs-lookup"><span data-stu-id="c40eb-123">Go to **Inventory management \> Setup \> Packing material \> Packing material codes**, define each type of packing material that you use, and specify the unit that the packing material is consumed in when you prepare shipments.</span></span>
1. <span data-ttu-id="c40eb-124">转到 **库存管理 \> 设置 \> 包装材料 \> 包装材料费用**，然后为刚才定义的每种包装材料设置费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-124">Go to **Inventory management \> Setup \> Packing material \> Packing material fees**, and set a fee for each type of packing material that you just defined.</span></span> <span data-ttu-id="c40eb-125">将基于所用单位的单价计算费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-125">Fees are calculated based on the price per unit that is consumed.</span></span>
1. <span data-ttu-id="c40eb-126">若要为物料分配包装材料，请转到 **库存管理 \> 设置 \> 包装材料 \> 包装材料分配**，然后创建分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-126">To allocate packing materials to items, go to **Inventory management \> Setup \> Packing material \> Packaging material allocation**, and create allocations.</span></span> <span data-ttu-id="c40eb-127">可以根据需要创建任意数量的分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-127">You can create as many allocations as you require.</span></span> <span data-ttu-id="c40eb-128">可以根据分配组所需详细程度为单个物料、物料组（包装组）或所有物料分配包装材料。</span><span class="sxs-lookup"><span data-stu-id="c40eb-128">You can allocate packing materials for individual items, groups of items (packing groups), or all items, depending on how detailed your allocations should be.</span></span>

    <span data-ttu-id="c40eb-129">针对您创建的每个分配，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c40eb-129">For each allocation that you create, follow these steps.</span></span>

    1. <span data-ttu-id="c40eb-130">在 **常规** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c40eb-130">On the **General** FastTab, set the following fields:</span></span>

        - <span data-ttu-id="c40eb-131">**物料代码** – 选择分配范围：</span><span class="sxs-lookup"><span data-stu-id="c40eb-131">**Item code** – Select the scope of the allocation:</span></span>

            - <span data-ttu-id="c40eb-132">**表** – 为单个特定物料创建分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-132">**Table** – Create an allocation for a single specific item.</span></span>
            - <span data-ttu-id="c40eb-133">**组** – 为属于 **包装组** 页中定义的包装组的所有物料定义分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-133">**Group** – Create an allocation for all the items the belong to a packing group that is defined on the **Packing groups** page.</span></span>
            - <span data-ttu-id="c40eb-134">**全部** – 为全部物料创建分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-134">**All** – Create an allocation for all items.</span></span>

            > [!NOTE]
            > <span data-ttu-id="c40eb-135">通常所有分配应该为同一个级别（**表**、**组** 或 **全部**）。</span><span class="sxs-lookup"><span data-stu-id="c40eb-135">Usually, you should make all your allocations at the same level (**Table**, **Group**, or **All**).</span></span> <span data-ttu-id="c40eb-136">如果使用多个级别，将为每个物料使用最具体的匹配分配。</span><span class="sxs-lookup"><span data-stu-id="c40eb-136">If you use more than one level, the most specific matching allocation will be used for each item.</span></span> <span data-ttu-id="c40eb-137">（**表** 级别的优先级高于 **组** 级别，这两个级别的优先级都高于 **全部** 级别。）</span><span class="sxs-lookup"><span data-stu-id="c40eb-137">(The **Table** level takes precedence over the **Group** level, and both those levels take precedence over the **All** level.)</span></span>

        - <span data-ttu-id="c40eb-138">**物料关系** – 如果要为单个物料分配，请选择此项。</span><span class="sxs-lookup"><span data-stu-id="c40eb-138">**Item relation** – If you're allocating for a single item, select the item.</span></span> <span data-ttu-id="c40eb-139">如果要为一组物料分配，请选择包装组。</span><span class="sxs-lookup"><span data-stu-id="c40eb-139">If you're allocating for a group of items, select the packing group.</span></span> <span data-ttu-id="c40eb-140">如果要为所有物料分配，请将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="c40eb-140">If you're allocating for all items, leave this field blank.</span></span>
        - <span data-ttu-id="c40eb-141">**配置**、**大小**、**颜色** 和 **样式** – 根据需要输入这些维度的值，以便进一步定义要为其进行分配的物料。</span><span class="sxs-lookup"><span data-stu-id="c40eb-141">**Configuration**, **Size**, **Color**, and **Style** – Enter values for these dimensions as you require, to further define the item that you're allocating for.</span></span>
        - <span data-ttu-id="c40eb-142">**包装单位** – 选择使用包装材料时包装物料所用单位。</span><span class="sxs-lookup"><span data-stu-id="c40eb-142">**Packing unit** – Select the unit that the item is packaged in when the packing material is used.</span></span> <span data-ttu-id="c40eb-143">此单位可能与物料的购买单位和存储单位不同。</span><span class="sxs-lookup"><span data-stu-id="c40eb-143">This unit might differ from the unit that the item is purchased and stored in.</span></span>
        - <span data-ttu-id="c40eb-144">**包装单位因子** – 输入用于将库存单位转换为包装单位的转换因子。</span><span class="sxs-lookup"><span data-stu-id="c40eb-144">**Packing unit factor** – Enter the conversion factor that is used to convert from the inventory unit to the packing unit.</span></span> <span data-ttu-id="c40eb-145">（转换使用公司 *包装单位* = *物料单位* × *包装单位因子*。）</span><span class="sxs-lookup"><span data-stu-id="c40eb-145">(The conversion uses the formula *Packing units* = *Item units* × *Packing unit factor*.)</span></span>

    1. <span data-ttu-id="c40eb-146">在 **包装材料** 快速选项卡上，为当前分配所需每件包装材料添加一行。</span><span class="sxs-lookup"><span data-stu-id="c40eb-146">On the **Packing material** FastTab, add a line for each piece of packing material that is required for the current allocation.</span></span> <span data-ttu-id="c40eb-147">在每行中，指定材料类型（按照 **包装材料代码** 页中的定义）和当前物料每个装运单位所用数量。</span><span class="sxs-lookup"><span data-stu-id="c40eb-147">On each line, specify the type of material (as defined on the **Packing material codes** page) and the amount of it that is consumed for each shipped unit of the current item.</span></span>

## <a name="packing-units-on-sales-order-lines"></a><span data-ttu-id="c40eb-148">销售订单行的包装单位</span><span class="sxs-lookup"><span data-stu-id="c40eb-148">Packing units on sales order lines</span></span>

<span data-ttu-id="c40eb-149">[开启包装材料费用计算并设置分配](#allocations)之后，系统将验证是否为向销售订单添加的每个物料指定了包装单位。</span><span class="sxs-lookup"><span data-stu-id="c40eb-149">After you've [turned on the calculation for packing material fees and set up your allocations](#allocations), the system verifies that packing units are specified for each item that is added to a sales order.</span></span> <span data-ttu-id="c40eb-150">然后计算所需任何费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-150">It then calculates any fees that are required.</span></span> <span data-ttu-id="c40eb-151">将物料添加到销售订单之后，将执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="c40eb-151">When an item is added to a sales order, one of the following steps occurs:</span></span>

- <span data-ttu-id="c40eb-152">**如果为物料应用包装分配：** 系统会使用指定的包装单位和包装单位数量更新销售订单行。</span><span class="sxs-lookup"><span data-stu-id="c40eb-152">**If a packing allocation applies to the item:** The system updates the sales order line with the specified packing unit and the packing unit quantity.</span></span> <span data-ttu-id="c40eb-153">（使用公式 *包装单位数量* = *订购数量* ÷ *所选包装单位的物料数量* 计算包装单位数量。）</span><span class="sxs-lookup"><span data-stu-id="c40eb-153">(The packing unit quantity is calculated by using the formula *Packing unit quantity* = *Ordered quantity* ÷ *Number of items in the selected packing unit*.)</span></span>
- <span data-ttu-id="c40eb-154">**如果不为物料应用保证分配：** 您可以在销售订单行上手动输入包装单位和包装单位数量。</span><span class="sxs-lookup"><span data-stu-id="c40eb-154">**If no packing allocation applies to the item:** You can manually enter a packing unit and a packing unit quantity on the sales order line.</span></span>

<span data-ttu-id="c40eb-155">当您过帐销售订单行时，也可以更改包装单位和包装单位数量。</span><span class="sxs-lookup"><span data-stu-id="c40eb-155">You can also change the packing unit and the packing unit quantity when you post the sales order line.</span></span> <span data-ttu-id="c40eb-156">如果销售订单行部分交货或一部分开发票，将用到这一功能。</span><span class="sxs-lookup"><span data-stu-id="c40eb-156">This capability is relevant if the sales order line is only partly delivered or partly invoiced.</span></span>

<span data-ttu-id="c40eb-157">当您为销售订单开发票时，系统将创建包装材料交易记录。</span><span class="sxs-lookup"><span data-stu-id="c40eb-157">When you invoice the sales order, the system creates packing material transactions.</span></span> <span data-ttu-id="c40eb-158">包装材料交易记录包含销售订单行的包装材料的重量。</span><span class="sxs-lookup"><span data-stu-id="c40eb-158">Packing material transactions contain the weights of the packing materials for the sales line.</span></span> <span data-ttu-id="c40eb-159">您可以在开票后修改交易记录。</span><span class="sxs-lookup"><span data-stu-id="c40eb-159">You can modify the transactions after you invoice them.</span></span> <span data-ttu-id="c40eb-160">然后您可以创建新交易记录。</span><span class="sxs-lookup"><span data-stu-id="c40eb-160">You can then create new transactions.</span></span>

## <a name="packing-units-on-purchase-order-lines"></a><span data-ttu-id="c40eb-161">采购订单行的包装单位</span><span class="sxs-lookup"><span data-stu-id="c40eb-161">Packing units on purchase order lines</span></span>

<span data-ttu-id="c40eb-162">系统不为采购订单行创建包装材料交易记录。</span><span class="sxs-lookup"><span data-stu-id="c40eb-162">The system doesn't create packing material transactions for purchase order lines.</span></span> <span data-ttu-id="c40eb-163">相反，您需要手动在 **包装材料交易记录** 页中为已开票采购订单行创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="c40eb-163">Instead, you manually create transactions for invoiced purchase order lines on the **Packing material transactions** page.</span></span>

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a><span data-ttu-id="c40eb-164">为支付包装材料费用的客户设置许可证编号</span><span class="sxs-lookup"><span data-stu-id="c40eb-164">Set up license numbers for customers that are charged packing material fees</span></span>

<span data-ttu-id="c40eb-165">如果特定客户的销售订单中应包含每个订单所用包装材料的费用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c40eb-165">If the sales orders for a specific customer should include charges for the packing materials that are used for each order, follow these steps.</span></span>

1. <span data-ttu-id="c40eb-166">转到 **应付帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-166">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c40eb-167">选择应该支付包装材料费用的客户。</span><span class="sxs-lookup"><span data-stu-id="c40eb-167">Select the customer that should be charged for packing materials.</span></span>
1. <span data-ttu-id="c40eb-168">在 **发票和交货** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c40eb-168">On the **Invoice and delivery** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="c40eb-169">在 **销售税** 部分的 **包装税许可证编号** 字段中，输入公司的许可证编号。</span><span class="sxs-lookup"><span data-stu-id="c40eb-169">In the **Sales tax** section, in the **Packing duty license number** field, enter the company's license number.</span></span>
    - <span data-ttu-id="c40eb-170">在 **包装材料费用** 部分的 **许可证编号** 字段中，输入公司的许可证编号。</span><span class="sxs-lookup"><span data-stu-id="c40eb-170">In the **Packing material fee** section, in the **License number** field, enter the company's license number.</span></span>

<span data-ttu-id="c40eb-171">现在，当您创建其中包含一个或多个使用包装材料的物料的销售订单并为其开票时，发票将显示包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-171">Now, when you create and invoice a sales order that includes one or more items that use packing materials, the invoice will show the packing material fees.</span></span>

<span data-ttu-id="c40eb-172">对于不应支付包装材料费用的客户，请执行相同步骤，但是清除 **包装税许可证编号** 和 **许可证编号** 字段中的许可证编号。</span><span class="sxs-lookup"><span data-stu-id="c40eb-172">For customers that should not pay packing material fees, follow these same steps, but clear the license numbers from the **Packing duty license number** and **License number** fields.</span></span> <span data-ttu-id="c40eb-173">不支付包装材料费用的客户的发票显示包装材料重量，但是不显示费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-173">Invoices for customers that don't pay packing material fees show the weights of the packing materials, but they don't show the fees.</span></span>

<span data-ttu-id="c40eb-174">若要生成用于显示您的公司在特定期间需要支付的所有包装材料费用的报表，请转到 **库存管理 \> 查询和报表 \> 包装材料报表 \> 包装材料费用计算**，指定日期范围，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-174">To generate a report that shows all the packing material fees that your company will owe for a specific period, go to **Inventory management \> Inquiries and reports \> Packing material reports \> Packing material fee calculation**, specify a range of dates, and then select **OK**.</span></span>

## <a name="print-packing-material-weights-on-invoices"></a><span data-ttu-id="c40eb-175">在发票上打印包装材料重量</span><span class="sxs-lookup"><span data-stu-id="c40eb-175">Print packing material weights on invoices</span></span>

<span data-ttu-id="c40eb-176">可以在发票上打印包装材料重量并指明由谁来支付相关费用。</span><span class="sxs-lookup"><span data-stu-id="c40eb-176">You can print packing material weights on an invoice and indicate who pays the related fees.</span></span> <span data-ttu-id="c40eb-177">重量按包装代码来汇总。</span><span class="sxs-lookup"><span data-stu-id="c40eb-177">The weights are summarized by packaging code.</span></span>

1. <span data-ttu-id="c40eb-178">转至 **应收帐款 \> 设置 \> 应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-178">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
1. <span data-ttu-id="c40eb-179">在 **更新** 选项卡的 **发票** 快速选项卡上，将 **打印包装材料重量** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c40eb-179">On the **Updates** tab, on the **Invoice** FastTab, set the **Print packing material weight** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]