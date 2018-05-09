---
title: "移动平均成本价"
description: "库存结转过程基于在物料的物料模型组中选择的库存评估方法将发货交易记录结算到收货交易记录。 但在运行库存结转前，此系统将计算通常在过帐发货交易记录时使用的移动平均成本价。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ee7b8098278b89c19504ebde6745c598fff1a581
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="running-average-cost-price"></a><span data-ttu-id="2e973-104">移动平均成本价</span><span class="sxs-lookup"><span data-stu-id="2e973-104">Running average cost price</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="2e973-105">库存结转过程基于在物料的物料模型组中选择的库存评估方法将发货交易记录结算到收货交易记录。</span><span class="sxs-lookup"><span data-stu-id="2e973-105">The inventory close process settles issue transactions to receipt transactions, based on the inventory valuation method that is selected in the item’s item model group.</span></span> <span data-ttu-id="2e973-106">但在运行库存结转前，此系统将计算通常在过帐发货交易记录时使用的移动平均成本价。</span><span class="sxs-lookup"><span data-stu-id="2e973-106">However, before inventory close is run, the system calculates a running average cost price that is typically used when issue transactions are posted.</span></span>

<span data-ttu-id="2e973-107">此系统通过使用以下公式，评估物料的这一移动平均成本价：</span><span class="sxs-lookup"><span data-stu-id="2e973-107">The system estimates this running average cost price for an item by using the following formula:</span></span> 

<span data-ttu-id="2e973-108">估计价格 = (实际金额 + 财务金额) ÷ (实际数量 + 财务数量)</span><span class="sxs-lookup"><span data-stu-id="2e973-108">Estimated price = (Physical amount + Financial amount) ÷ (Physical quantity + Financial quantity)</span></span>

## <a name="using-the-running-average-cost-price"></a><span data-ttu-id="2e973-109">使用移动平均成本价</span><span class="sxs-lookup"><span data-stu-id="2e973-109">Using the running average cost price</span></span>
<span data-ttu-id="2e973-110">下表显示此系统何时使用移动平均成本价过帐库存交易记录，以及何时改为使用在物料主记录上定义的成本价。</span><span class="sxs-lookup"><span data-stu-id="2e973-110">The following table shows when the system posts inventory transactions by using the running average cost price, and when it uses the cost price that is defined on the item master record instead.</span></span>

| <span data-ttu-id="2e973-111">条件</span><span class="sxs-lookup"><span data-stu-id="2e973-111">Condition</span></span>                                               | <span data-ttu-id="2e973-112">此系统使用估计的移动平均成本价</span><span class="sxs-lookup"><span data-stu-id="2e973-112">The system uses the estimated running average cost price</span></span> | <span data-ttu-id="2e973-113">此系统使用物料主记录上定义的成本价</span><span class="sxs-lookup"><span data-stu-id="2e973-113">The system uses the cost price that is defined on the item master</span></span> |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e973-114">分子\* 和分母\*\* 均为正。</span><span class="sxs-lookup"><span data-stu-id="2e973-114">Both the numerator\* and denominator\*\* are positive.</span></span>  | <span data-ttu-id="2e973-115">是</span><span class="sxs-lookup"><span data-stu-id="2e973-115">Yes</span></span>                                                      | <span data-ttu-id="2e973-116">无</span><span class="sxs-lookup"><span data-stu-id="2e973-116">No</span></span>                                                                |
| <span data-ttu-id="2e973-117">分子\*、分母\*\* 或二者均为负。</span><span class="sxs-lookup"><span data-stu-id="2e973-117">The numerator\*, denominator\*\*, or both are negative.</span></span> | <span data-ttu-id="2e973-118">无</span><span class="sxs-lookup"><span data-stu-id="2e973-118">No</span></span>                                                       | <span data-ttu-id="2e973-119">是</span><span class="sxs-lookup"><span data-stu-id="2e973-119">Yes</span></span>                                                               |
| <span data-ttu-id="2e973-120">分母\*\* 为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="2e973-120">The denominator\*\* is 0 (zero).</span></span>                        | <span data-ttu-id="2e973-121">无</span><span class="sxs-lookup"><span data-stu-id="2e973-121">No</span></span>                                                       | <span data-ttu-id="2e973-122">是</span><span class="sxs-lookup"><span data-stu-id="2e973-122">Yes</span></span>                                                               |

<span data-ttu-id="2e973-123">\* 分子 = (实际金额 + 财务金额) \*\* 分母 = (实际数量 + 财务数量)</span><span class="sxs-lookup"><span data-stu-id="2e973-123">\* Numerator = (Physical amount + Financial amount) \*\* Denominator = (Physical quantity + Financial quantity)</span></span> 

<span data-ttu-id="2e973-124">**注意：**如果没有为某一物料选择**包括实际成本**选项，则系统使用 0（零）来用于实际金额和实际数量。</span><span class="sxs-lookup"><span data-stu-id="2e973-124">**Note:** If the **Include physical value** option isn't selected for an item, the system uses 0 (zero) for both the physical amount and the physical quantity.</span></span> <span data-ttu-id="2e973-125">有关此选项的信息，请参阅[包括实际成本](include-physical-value.md)。</span><span class="sxs-lookup"><span data-stu-id="2e973-125">For information about this option, see [Include physical value](include-physical-value.md).</span></span>

## <a name="avoiding-pricing-amplification"></a><span data-ttu-id="2e973-126">避免价格放大</span><span class="sxs-lookup"><span data-stu-id="2e973-126">Avoiding pricing amplification</span></span>
<span data-ttu-id="2e973-127">偶尔，此系统在不具有标价所基于的足够收货前就给若干发货标价。</span><span class="sxs-lookup"><span data-stu-id="2e973-127">On rare occasions, the system prices several issues before it has enough receipts to base the price on.</span></span> <span data-ttu-id="2e973-128">此情况可能导致移动平均成本价的估计过度膨胀。</span><span class="sxs-lookup"><span data-stu-id="2e973-128">This scenario can cause estimates of the running average cost price to be overly inflated.</span></span> <span data-ttu-id="2e973-129">不过，您可以采取一些步骤来避免价格放大，或者在该情况发生后减少其影响。</span><span class="sxs-lookup"><span data-stu-id="2e973-129">However, there are steps that you can take to avoid pricing amplification, or to reduce its impact when it does occur.</span></span> <span data-ttu-id="2e973-130">**场景**以下交易记录发生于您为其选择**包括实际成本**的物料：</span><span class="sxs-lookup"><span data-stu-id="2e973-130">**Scenario** The following transactions occur for an item that you've selected the **Include physical value** option for:</span></span>

1.  <span data-ttu-id="2e973-131">您在财务上收到数量 100（USD 100.00）。</span><span class="sxs-lookup"><span data-stu-id="2e973-131">You financially receive a quantity of 100 at USD 100.00.</span></span>
2.  <span data-ttu-id="2e973-132">您在财务上发货数量为 200。</span><span class="sxs-lookup"><span data-stu-id="2e973-132">You financially issue a quantity of 200.</span></span>
3.  <span data-ttu-id="2e973-133">您实际上收到数量 101（USD 202.00）。</span><span class="sxs-lookup"><span data-stu-id="2e973-133">You physically receive a quantity of 101 at USD 202.00.</span></span>

<span data-ttu-id="2e973-134">在您检查该物料的估计移动平均成本价时，您预期成本价为 USD 1.51。</span><span class="sxs-lookup"><span data-stu-id="2e973-134">When you examine the estimated running average cost price for the item, you expect a cost price of USD 1.51.</span></span> <span data-ttu-id="2e973-135">相反，您发现估计移动平均成本价为 USD 102.00，其基于以下公式：估计价格 = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 此价格放大发生，因为，在第 2 步中财务发货 200 个物料时，此系统必须在具有任何相应收货前将物料定价为 100。</span><span class="sxs-lookup"><span data-stu-id="2e973-135">Instead, you find an estimated running average of USD 102.00, which is based on the following formula: Estimated price = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 This pricing amplification occurs because, when 200 items are issued financially in step 2, the system must price 100 of the items before it has any corresponding receipts.</span></span> <span data-ttu-id="2e973-136">此情况导致负库存。</span><span class="sxs-lookup"><span data-stu-id="2e973-136">This situation causes negative inventory.</span></span> <span data-ttu-id="2e973-137">此系统然后估计为 USD 1.00，如我们的预期。</span><span class="sxs-lookup"><span data-stu-id="2e973-137">The system then estimates a unit price of USD 1.00, as we might expect.</span></span> <span data-ttu-id="2e973-138">但是，在相应的 100 收货到达时，其每个收货的单位价格为 USD 2.00。</span><span class="sxs-lookup"><span data-stu-id="2e973-138">However, when the corresponding 100 receipts arrive, they are at a unit price of USD 2.00 each.</span></span> 

<span data-ttu-id="2e973-139">**注意：**尽管这些发货生成负库存，但在计算发货价格时，库存为正。</span><span class="sxs-lookup"><span data-stu-id="2e973-139">**Note:** Although the issues create negative inventory, inventory is positive when the issue price is calculated.</span></span> <span data-ttu-id="2e973-140">因此，使用移动平均成本价，而非物料主记录上的价格。</span><span class="sxs-lookup"><span data-stu-id="2e973-140">Therefore, the running average cost price is used instead of the price on the item master.</span></span> <span data-ttu-id="2e973-141">此时，此系统将具有 USD 100.00 的库存价值抵消。</span><span class="sxs-lookup"><span data-stu-id="2e973-141">At this point, the system has an inventory value offset of USD 100.00.</span></span> <span data-ttu-id="2e973-142">虽然该抵消累积到高于 100 件，每件的单位抵消为 USD 1.00，但我们现在库存中只有一件。</span><span class="sxs-lookup"><span data-stu-id="2e973-142">Although that offset was built up over 100 pieces, where there was a unit offset of USD 1.00 each, we now have only one piece in inventory.</span></span> <span data-ttu-id="2e973-143">因此，将抵消 USD 100.00 分配给此单件。</span><span class="sxs-lookup"><span data-stu-id="2e973-143">Therefore, the offset of USD 100.00 is allocated to this one piece.</span></span> <span data-ttu-id="2e973-144">结果是过度膨胀的估计成本价。</span><span class="sxs-lookup"><span data-stu-id="2e973-144">The result is the overly inflated estimated cost price.</span></span> 

<span data-ttu-id="2e973-145">**注意：**为了进行比较，请注意，如果在此情况中撤消第 2 步和第 3 步，则 200 个物料将按单位价格 USD 1.51 发货，并且一件仍将保持在单位价格 USD 1.51。</span><span class="sxs-lookup"><span data-stu-id="2e973-145">**Note:** For comparison, notice that if steps 2 and 3 are reversed in the scenario, 200 items will be issued at a unit price of USD 1.51, and one piece will remain at a unit price of USD 1.51.</span></span> <span data-ttu-id="2e973-146">因为在涉及负库存时可能发生此价格放大的情况，所以，在以下情况下很难避免：</span><span class="sxs-lookup"><span data-stu-id="2e973-146">Because this pricing amplification scenario can occur when negative inventory is involved, it's difficult to avoid in the following cases:</span></span>

-   <span data-ttu-id="2e973-147">您必须基于现有价值和数量评估发货价格。</span><span class="sxs-lookup"><span data-stu-id="2e973-147">You must estimate issue prices on the on-hand value and quantity.</span></span>
-   <span data-ttu-id="2e973-148">您必须调整针对发货和收货的现有价值和数量。</span><span class="sxs-lookup"><span data-stu-id="2e973-148">You must adjust the on-hand value and quantity on issues and receipts.</span></span>
-   <span data-ttu-id="2e973-149">您的业务模型允许您对超过现有件数的物料进行发货或标价。</span><span class="sxs-lookup"><span data-stu-id="2e973-149">Your business model allows you to send out, or price, more pieces than you have.</span></span>
-   <span data-ttu-id="2e973-150">您必须接受提交给您的任何收货价值和数量。</span><span class="sxs-lookup"><span data-stu-id="2e973-150">You must accept any receipt value and quantity that are submitted to you.</span></span>

<span data-ttu-id="2e973-151">不过，如果您的业务模型允许以下行为，则它们可帮助您避免可能造成价格放大情况的负数量：</span><span class="sxs-lookup"><span data-stu-id="2e973-151">However, if your business model allows for the following practices, they can help you avoid the negative quantities that make the pricing amplification scenario possible:</span></span>

-   <span data-ttu-id="2e973-152">如果您为物料选中**包括实际成本**选项，则取消选中**物料模型组**页上的**允许实际负库存**复选框。</span><span class="sxs-lookup"><span data-stu-id="2e973-152">If you select the **Include physical value** option for an item, clear the **Physical negative inventory** check box on the **Item model groups** page.</span></span>
-   <span data-ttu-id="2e973-153">如果您*没有*为物料选中**包括实际成本**选项，则取消选中**物料模型组**页上的**允许财务负库存**选项。</span><span class="sxs-lookup"><span data-stu-id="2e973-153">If you do *not* select the **Include physical value** option for an item, clear the **Financial negative inventory** option on the **Item model groups** page.</span></span>

<span data-ttu-id="2e973-154">此外，请考虑您的实际库存价值中的最大抵消受到实际交易记录的数目以及实际价格和财务价格之间的差异的限制。</span><span class="sxs-lookup"><span data-stu-id="2e973-154">Additionally, consider that the maximum offset in your physical inventory value is limited by the number of physical transactions, and the difference between physical and financial prices.</span></span> <span data-ttu-id="2e973-155">假设最终在财务上更新了所有实际交易记录，实际价值就不会突升。</span><span class="sxs-lookup"><span data-stu-id="2e973-155">Provided that all physical transactions are eventually updated financially, the physical value can't rise to extreme levels.</span></span> <span data-ttu-id="2e973-156">最后，请注意，如果累积的抵消分散到多个现有件数上，而非只是一件上时，这一价格放大的影响会显著降低。</span><span class="sxs-lookup"><span data-stu-id="2e973-156">Finally, note that the amplification effect decreases significantly when the accumulated offset is spread out over several on-hand pieces instead of just one.</span></span>




