---
title: "包装材料和费用"
description: "定期向回收公司支付包装材料费用。 为包装单位中包含的每种材料支付每个单位重量的金额。 程序将计算和报告包装材料费用，但是不过帐分录，因为没有将这些费用视为要向主管机构缴纳的税款。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1565fda25f6b09019899bd9b8dcd921c65a16bcf
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="packing-materials-and-fees"></a><span data-ttu-id="4a229-105">包装材料和费用</span><span class="sxs-lookup"><span data-stu-id="4a229-105">Packing materials and fees</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4a229-106">定期向回收公司支付包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-106">Packing material fees are paid to a recycling company at certain intervals.</span></span> <span data-ttu-id="4a229-107">为包装单位中包含的每种材料支付每个单位重量的金额。</span><span class="sxs-lookup"><span data-stu-id="4a229-107">An amount is paid, per unit of weight, for each material that a packing unit consists of.</span></span> <span data-ttu-id="4a229-108">程序将计算和报告包装材料费用，但是不过帐分录，因为没有将这些费用视为要向主管机构缴纳的税款。</span><span class="sxs-lookup"><span data-stu-id="4a229-108">Packing material fees are calculated and reported, but no ledger transactions are posted because the fees are not regarded as taxes to be paid to an authority.</span></span>

<span data-ttu-id="4a229-109">程序将为销售订单行和采购订单行计算包装材料重量和费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-109">Packing material weights and fees are calculated for sales order lines and for purchase order lines.</span></span>

<span data-ttu-id="4a229-110">可以为一种物料、一个物料包装组或所有物料定义一个或多个包装单位。</span><span class="sxs-lookup"><span data-stu-id="4a229-110">You can define one or more packing units for an item, for a packing group of items, or for all items.</span></span> <span data-ttu-id="4a229-111">包装单位包含包装材料、其重量和该包装单位中包括的物料数量。</span><span class="sxs-lookup"><span data-stu-id="4a229-111">A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit.</span></span> <span data-ttu-id="4a229-112">将包装材料代码分配给定义的包装材料的每种类型。</span><span class="sxs-lookup"><span data-stu-id="4a229-112">A packing material code is assigned to each type of packing material that is defined.</span></span> <span data-ttu-id="4a229-113">根据包装材料代码，您可以指定指定期间的价格。</span><span class="sxs-lookup"><span data-stu-id="4a229-113">Based on the packing material code, you can specify a price for a specified period.</span></span> <span data-ttu-id="4a229-114">基于此信息计算包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-114">The packing material fee is calculated based on this information.</span></span>

| <span data-ttu-id="4a229-115">**注意**</span><span class="sxs-lookup"><span data-stu-id="4a229-115">**Note**</span></span>                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a229-116">即使您的公司不支付包装材料费用，您也可以使用此功能来计算包装材料重量的统计。</span><span class="sxs-lookup"><span data-stu-id="4a229-116">Even if your company does not pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials.</span></span> |

## <a name="setup-requirements-for-packing-material-fees"></a><span data-ttu-id="4a229-117">包装材料费用的设置要求</span><span class="sxs-lookup"><span data-stu-id="4a229-117">Setup requirements for packing material fees</span></span>
<span data-ttu-id="4a229-118">在计算包装材料重量和/或费用之前，必须创建下列基础数据：</span><span class="sxs-lookup"><span data-stu-id="4a229-118">Before you calculate packing material weights or packing material fees, or both, you must create the following base data:</span></span>

-   <span data-ttu-id="4a229-119">包装组 – 创建要分配到物料的包装组。</span><span class="sxs-lookup"><span data-stu-id="4a229-119">Packing groups – Create packing groups to assign to items.</span></span>
-   <span data-ttu-id="4a229-120">包装材料代码 – 为定义的包装材料的每种类型创建包装材料代码。</span><span class="sxs-lookup"><span data-stu-id="4a229-120">Packing material codes – Create packing material codes for each type of packing material that is defined.</span></span>
-   <span data-ttu-id="4a229-121">包装单位 – 为一种物料、一个包装组或所有物料指定包装单位。</span><span class="sxs-lookup"><span data-stu-id="4a229-121">Packing units – Specify a packing unit for an item, for a packing group, or for all items.</span></span> <span data-ttu-id="4a229-122">对于每个包装单位，定义要包含的包装材料、分配重量，并在“包装单位因子”字段中，从库存单位输入换算系数。</span><span class="sxs-lookup"><span data-stu-id="4a229-122">For each packing unit, define which packing materials to include, assign weights, and, in the Packing unit factor field, enter the conversion factor from the inventory unit.</span></span>
-   <span data-ttu-id="4a229-123">包装材料费用 – 按照包装材料代码指定包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-123">Packing material fees – Specify packing material fees per packing material code.</span></span> <span data-ttu-id="4a229-124">为每种类型的材料定义有效期、每种材料的价格、币种和单位。</span><span class="sxs-lookup"><span data-stu-id="4a229-124">For each type of material, define the period of validity, the price per material, the currency, and the unit.</span></span>

## <a name="packing-units-on-sales-order-lines"></a><span data-ttu-id="4a229-125">销售订单行的包装单位</span><span class="sxs-lookup"><span data-stu-id="4a229-125">Packing units on sales order lines</span></span>
<span data-ttu-id="4a229-126">当您创建销售订单行时，检查系统以查看是否为物料指定了包装单位。</span><span class="sxs-lookup"><span data-stu-id="4a229-126">When you create a sales order line, the system checks to see whether packing units are specified for the item.</span></span> <span data-ttu-id="4a229-127">如果指定了包装单位，系统会使用指定的包装单位和包装单位数量更新销售订单行。</span><span class="sxs-lookup"><span data-stu-id="4a229-127">If packing units are specified, the system updates the sales order line with the specified packing unit and the packing unit quantity.</span></span> <span data-ttu-id="4a229-128">包装单位数量基于订购数量除以选定包装单位中的物料数量。</span><span class="sxs-lookup"><span data-stu-id="4a229-128">The packing unit quantity is based on the ordered quantity divided by the number of items in the selected packing unit.</span></span> <span data-ttu-id="4a229-129">如果没有指定包装单位，您可以在销售订单行上手动输入包装单位和包装单位数量。</span><span class="sxs-lookup"><span data-stu-id="4a229-129">If a packing unit has not been specified, you can manually enter a packing unit and a packing unit quantity on the sales order line.</span></span> <span data-ttu-id="4a229-130">当您过帐销售订单行时，也可以更改包装单位和包装单位数量。</span><span class="sxs-lookup"><span data-stu-id="4a229-130">You can also change the packing unit and the packing unit quantity when you post the sales order line.</span></span> <span data-ttu-id="4a229-131">如果销售订单行部分交货或一部分开发票，将用到这一操作。</span><span class="sxs-lookup"><span data-stu-id="4a229-131">This is relevant if the sales order line is only partly delivered or partly invoiced.</span></span> <span data-ttu-id="4a229-132">当您为销售订单开发票时，将创建包装材料交易记录。</span><span class="sxs-lookup"><span data-stu-id="4a229-132">When you invoice the sales order, packing material transactions are created.</span></span> <span data-ttu-id="4a229-133">包装材料交易记录包含销售订单行的包装材料的重量。</span><span class="sxs-lookup"><span data-stu-id="4a229-133">Packing material transactions contain the weights of the packing materials for the sales line.</span></span> <span data-ttu-id="4a229-134">还可以在开票后修改交易记录，然后创建新的交易记录。</span><span class="sxs-lookup"><span data-stu-id="4a229-134">You can also modify the transactions after you invoice them, and then create new transactions.</span></span>

## <a name="packing-units-on-purchase-order-lines"></a><span data-ttu-id="4a229-135">采购订单行的包装单位</span><span class="sxs-lookup"><span data-stu-id="4a229-135">Packing units on purchase order lines</span></span>
<span data-ttu-id="4a229-136">采购订单行的包装材料交易记录不是由系统创建的。</span><span class="sxs-lookup"><span data-stu-id="4a229-136">Packing material transactions for a purchase order line are not created by the system.</span></span> <span data-ttu-id="4a229-137">您将手动在**“包装材料交易记录”**页中为已开票采购订单行创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="4a229-137">You create transactions for invoiced purchase order lines manually in the **Packing material transactions** page.</span></span>

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a><span data-ttu-id="4a229-138">设置客户的包装材料费用许可证编号</span><span class="sxs-lookup"><span data-stu-id="4a229-138">Set up customer packagingmaterialfee license numbers</span></span>
<span data-ttu-id="4a229-139">如果客户支付包装材料费用，请在**“客户”**页中指定客户的包装材料费用许可证编号。</span><span class="sxs-lookup"><span data-stu-id="4a229-139">If the customers pay the packaging material fees, specify the customers' packaging-material-fee license numbers in the **Customers** page.</span></span> <span data-ttu-id="4a229-140">如果为客户指定了许可证编号，则对销售订单开票时将自动计算包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-140">When a license number has been assigned to a customer, the packaging material fees are calculated automatically when sales orders are invoiced.</span></span> <span data-ttu-id="4a229-141">开票后，**“计算费用”**复选框将在**“包装材料交易记录”**页中被取消选中，因为您不必计算和打印报表。</span><span class="sxs-lookup"><span data-stu-id="4a229-141">After invoicing, the **Calculate fee** check box is cleared in the **Packing material transactions** page, because you do not have to calculate and print a report.</span></span> <span data-ttu-id="4a229-142">您可以在发票上打印包装材料重量并告知客户由他们支付该费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-142">You can print the packaging material weights on the invoice, and inform the customers that they pay the fees.</span></span> 

<span data-ttu-id="4a229-143">如果您的公司支付包装材料费用，请不要指定客户许可证编号。</span><span class="sxs-lookup"><span data-stu-id="4a229-143">If your company pays the packaging material fees, do not specify the customer license numbers.</span></span> <span data-ttu-id="4a229-144">开票后，**“计算费用”**复选框在**“包装材料交易记录”**页中被选中。</span><span class="sxs-lookup"><span data-stu-id="4a229-144">After invoicing, the **Calculate fee** check box is selected in the **Packing material transactions** page.</span></span> <span data-ttu-id="4a229-145">这表示创建报表时计算费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-145">This indicates that the fees are calculated when a report is created.</span></span> <span data-ttu-id="4a229-146">您可以在发票上打印重量并指明由您的公司支付费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-146">You can print the weights on the invoice, and indicate that your company pays the fees.</span></span>

## <a name="print-packaging-material-weights-on-invoices"></a><span data-ttu-id="4a229-147">在发票上打印包装材料重量</span><span class="sxs-lookup"><span data-stu-id="4a229-147">Print packaging material weights on invoices</span></span>
<span data-ttu-id="4a229-148">可以在发票上打印包装材料重量并指明由谁来支付包装材料费用。</span><span class="sxs-lookup"><span data-stu-id="4a229-148">You can print the packaging material weights on the invoice, and indicate who pays the packaging material fees.</span></span> <span data-ttu-id="4a229-149">重量按包装代码来汇总。</span><span class="sxs-lookup"><span data-stu-id="4a229-149">The weights are summarized by packaging code.</span></span>
 





