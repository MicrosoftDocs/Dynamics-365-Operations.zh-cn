---
title: "总成本分摊方法"
description: "本主题提供使用总成本分摊 (TCA) 的指南。 TCA 是计算批次订单的主要配方物料和为配方定义的联产品之间的成本的方法。"
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 43227e495ba25610718a7914167cd6dfb19976c5
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="total-cost-allocation-method"></a><span data-ttu-id="5b63f-104">总成本分摊方法</span><span class="sxs-lookup"><span data-stu-id="5b63f-104">Total cost allocation method</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b63f-105">本主题提供使用总成本分摊 (TCA) 的指南。</span><span class="sxs-lookup"><span data-stu-id="5b63f-105">This topic provides guidelines for using total cost allocation (TCA).</span></span> <span data-ttu-id="5b63f-106">TCA 是计算批次订单的主要配方物料和为配方定义的联产品之间的成本的方法。</span><span class="sxs-lookup"><span data-stu-id="5b63f-106">TCA is a method of calculating the cost between the main formula item for a batch order and the co-products that are defined for the formula.</span></span>

<span data-ttu-id="5b63f-107">总成本分摊 (TCA) 是计算批次订单的主要配方物料和为配方定义的联产品之间的成本的方法。</span><span class="sxs-lookup"><span data-stu-id="5b63f-107">Total cost allocation (TCA) is a method of calculating the cost between the main formula item for a batch order and the co-products that are defined for the formula.</span></span> <span data-ttu-id="5b63f-108">此方法是动态的。</span><span class="sxs-lookup"><span data-stu-id="5b63f-108">This method is dynamic.</span></span> <span data-ttu-id="5b63f-109">它计算作为报告为已完成的配方物料和联产品的数量之间的加权平均。</span><span class="sxs-lookup"><span data-stu-id="5b63f-109">It calculates the cost as a weighted average between the quantities that are reported as finished for the formula item and the co-products.</span></span> <span data-ttu-id="5b63f-110">在使用 TCA 时，您不必查看各批次订单的成本分摊。</span><span class="sxs-lookup"><span data-stu-id="5b63f-110">When TCA is used, you don't have to review cost allocations for every batch order.</span></span> <span data-ttu-id="5b63f-111">如果不使用 TCA，则配方计算使用现有的功能。</span><span class="sxs-lookup"><span data-stu-id="5b63f-111">If TCA isn't used, the formula calculation uses existing functionality.</span></span>

## <a name="using-tca-for-coproducts"></a><span data-ttu-id="5b63f-112">使用联产品的 TCA</span><span class="sxs-lookup"><span data-stu-id="5b63f-112">Using TCA for coproducts</span></span>
<span data-ttu-id="5b63f-113">以下是使用联产品的 TCA 的某些指南：</span><span class="sxs-lookup"><span data-stu-id="5b63f-113">Here are some of the guidelines for using TCA for co-products:</span></span>

-   <span data-ttu-id="5b63f-114">如果您为配方版本将**总成本分摊**滑块设置为**是**，联产品必须具有大于 0（零）的成本价。</span><span class="sxs-lookup"><span data-stu-id="5b63f-114">If you set the **Total Cost Allocation** slider to **Yes** for a formula version, co-products must have a cost price that is more than 0 (zero).</span></span> <span data-ttu-id="5b63f-115">该值可以从同一个站点的有效成本版本或非特定于站点的配方的第一个站点中检索。</span><span class="sxs-lookup"><span data-stu-id="5b63f-115">The value can be retrieved from the active cost version for the same site, or for the first site for a formula that isn't site-specific.</span></span> <span data-ttu-id="5b63f-116">在审核配方时，此条件已验证。</span><span class="sxs-lookup"><span data-stu-id="5b63f-116">This condition is validated when the formula is approved.</span></span>

    -   <span data-ttu-id="5b63f-117">您无需手动输入联产品的成本分摊百分比。</span><span class="sxs-lookup"><span data-stu-id="5b63f-117">You don’t need to manually enter cost allocation percentages for co-products.</span></span> <span data-ttu-id="5b63f-118">而系统自动创建成本分摊百分比作为联产品有效成本价的平均值。</span><span class="sxs-lookup"><span data-stu-id="5b63f-118">Instead, the system automatically creates the cost allocation percentage as the average of active cost prices of co-products.</span></span> 
    -   <span data-ttu-id="5b63f-119">您不需要为属于联产品的非标准成本物料输入标准成本。</span><span class="sxs-lookup"><span data-stu-id="5b63f-119">You don’t need to enter standard cost for non-standard cost items that are co-products.</span></span> <span data-ttu-id="5b63f-120">系统中存在两个成本计算版本类型：标准成本与计划成本</span><span class="sxs-lookup"><span data-stu-id="5b63f-120">There are two types of costing versions in the system: standard cost and planned cost</span></span> 
    -   <span data-ttu-id="5b63f-121">如果物料不通过标准成本评估方法评估，我们建议您在计划成本版本中使用有效的成本价。</span><span class="sxs-lookup"><span data-stu-id="5b63f-121">If an item isn’t valuated by the standard cost valuation method, we recommend you use an active cost price in the planned cost version.</span></span> <span data-ttu-id="5b63f-122">此价格用于成本估计，例如，库存估价流程中的物料清单计算、生产成本估计和回退价格。</span><span class="sxs-lookup"><span data-stu-id="5b63f-122">This price is used for cost estimation, for example, BOM calculation, production cost estimation, and fallback price in the inventory valuation process.</span></span> 

-   <span data-ttu-id="5b63f-123">如果您设置配方版本的**总成本分摊**滑块为**是**且以下条件成立，成本分摊方法为 **TCA**，并且成本分摊百分比将不更改：</span><span class="sxs-lookup"><span data-stu-id="5b63f-123">If you set the **Total Cost Allocation** slider to **Yes** for the formula version and the following conditions are true, the method of cost allocation is **TCA**, and the percentage of cost allocation is unchanged:</span></span>
    -   <span data-ttu-id="5b63f-124">您添加了联产品。</span><span class="sxs-lookup"><span data-stu-id="5b63f-124">You added co-products.</span></span>
    -   <span data-ttu-id="5b63f-125">为联产品您使用了成本分配不同的方法。</span><span class="sxs-lookup"><span data-stu-id="5b63f-125">You used a different method of cost allocation for the co-products.</span></span>
-   <span data-ttu-id="5b63f-126">如果您设置配方版本的**总成本分摊**滑块为**否**且以下条件成立，成本分摊方法更改为**手动**，并且成本分摊百分比将不更改：</span><span class="sxs-lookup"><span data-stu-id="5b63f-126">If you set the **Total Cost Allocation** slider to **No** for the formula version and the following conditions are true, the method of cost allocation is changed to **Manual**, and the percentage of cost allocation is unchanged:</span></span>
    -   <span data-ttu-id="5b63f-127">您添加了联产品。</span><span class="sxs-lookup"><span data-stu-id="5b63f-127">You added co-products.</span></span>
    -   <span data-ttu-id="5b63f-128">成本分摊百分比大于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="5b63f-128">The percentage of cost allocation is more than 0 (zero).</span></span>
-   <span data-ttu-id="5b63f-129">在您可以成功执行配方计算之前，必须估计成本分摊百分比。</span><span class="sxs-lookup"><span data-stu-id="5b63f-129">Before you can successfully perform a formula calculation, you must estimate the percentages of cost allocation.</span></span> <span data-ttu-id="5b63f-130">您可以手动或通过使用**联产品**页中的**估计成本**完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="5b63f-130">You can complete this step either manually or by using the **Estimate cost** option on the **Co-products** page.</span></span> <span data-ttu-id="5b63f-131">**注意：**仅当**总成本分摊**滑块为配方版本设置为**是**时，**估计成本**选项才可用。</span><span class="sxs-lookup"><span data-stu-id="5b63f-131">**Note:** The **Estimate cost** option is available only when the **Total Cost Allocation** slider is set to **Yes** for the formula version.</span></span> <span data-ttu-id="5b63f-132">如果报告为完成的批次订单数量与在配方上出现的数量匹配，您就可以查看预期的分摊。</span><span class="sxs-lookup"><span data-stu-id="5b63f-132">You can view the expected allocation if the batch order quantities that are reported as finished match quantities that appear on the formula.</span></span>
-   <span data-ttu-id="5b63f-133">在批次订单是手动创建或计划批次订单确认时，配方版本的**总成本分摊**滑块的值将复制到批次订单。</span><span class="sxs-lookup"><span data-stu-id="5b63f-133">When a batch order is created manually or a planned batch order is firmed, the value of the **Total Cost Allocation** slider for the formula version is copied to the batch order.</span></span> <span data-ttu-id="5b63f-134">不过，您可以更改该批次订单的此设置。</span><span class="sxs-lookup"><span data-stu-id="5b63f-134">However, you can change this setting on the batch order.</span></span> <span data-ttu-id="5b63f-135">如果**总成本分摊**滑块为配方版本设置为**否**，然后为批次订单更改为**是**，设置为**手动**的每一行的成本分摊方法将更改为 **TCA**。</span><span class="sxs-lookup"><span data-stu-id="5b63f-135">If the **Total Cost Allocation** slider is set to **No** for the formula version and then changed to **Yes** for the batch order, the method of cost allocation for each line that was set to **Manual** is changed to **TCA**.</span></span> <span data-ttu-id="5b63f-136">**无**的成本分摊将不更改。</span><span class="sxs-lookup"><span data-stu-id="5b63f-136">A cost allocation of **None** is unchanged.</span></span> <span data-ttu-id="5b63f-137">如果**总成本分摊**滑块为配方版本设置为**是**，然后为批次订单更改为**否**，每个**生产**类型的联产品的成本分摊方法将更改为**手动**。</span><span class="sxs-lookup"><span data-stu-id="5b63f-137">If the **Total Cost Allocation** slider is set to **Yes** for the formula version and then changed to **No** for the batch order, the method of cost allocation for each co-product of the **Production** type is changed to **Manual**.</span></span> <span data-ttu-id="5b63f-138">成本分摊的所有估计的百分比将不更改。</span><span class="sxs-lookup"><span data-stu-id="5b63f-138">Any estimated percentage of cost allocation is unchanged.</span></span>
-   <span data-ttu-id="5b63f-139">**联产品成本分摊**页显示计算成本分摊百分比。</span><span class="sxs-lookup"><span data-stu-id="5b63f-139">The **Co-product cost allocation** page shows the calculated cost allocation percentage.</span></span> <span data-ttu-id="5b63f-140">您可以从**批次订单**页打开此页。</span><span class="sxs-lookup"><span data-stu-id="5b63f-140">You can open this page from the **Batch order** page.</span></span> <span data-ttu-id="5b63f-141">在报告的产品和数量不同于批次订单上的计划或开始的数量时，此信息很有用。</span><span class="sxs-lookup"><span data-stu-id="5b63f-141">This information is useful when the products and quantities that are reported differ from the scheduled or started quantities on the batch order.</span></span> <span data-ttu-id="5b63f-142">在成本完成后，TCA 中的这些新的百分比将显示在**联产品成本分摊**页。</span><span class="sxs-lookup"><span data-stu-id="5b63f-142">When the cost is complete, these new percentage allocations from TCA are shown on the **Co-product cost allocation** page.</span></span>

## <a name="calculating-the-burden-for-byproducts"></a><span data-ttu-id="5b63f-143">副产品负担的计算</span><span class="sxs-lookup"><span data-stu-id="5b63f-143">Calculating the burden for byproducts</span></span>
<span data-ttu-id="5b63f-144">**联产品**页上上的**副产品成本分配**字段是仅用于副产品的枚举器字段。</span><span class="sxs-lookup"><span data-stu-id="5b63f-144">The **By-product cost allocation** field on the **Co-products** page is an enumerator field that is used only for by-products.</span></span> <span data-ttu-id="5b63f-145">对于联产品，此字段的值始终为**无**。</span><span class="sxs-lookup"><span data-stu-id="5b63f-145">For co-products, the value of this field is always **None**.</span></span> <span data-ttu-id="5b63f-146">对于副产品行，则此字段确定副产品行的成本额如何添加到生产的总成本。</span><span class="sxs-lookup"><span data-stu-id="5b63f-146">For by-product lines, this field determines how the cost amount for the by-product line is added to the total cost of the production.</span></span> <span data-ttu-id="5b63f-147">选项如下：</span><span class="sxs-lookup"><span data-stu-id="5b63f-147">The following options are available:</span></span>

-   <span data-ttu-id="5b63f-148">**“无”**─ 对于此副产品行没有金额添加到生产的总成本。</span><span class="sxs-lookup"><span data-stu-id="5b63f-148">**None** ─ No amount is added to the total cost of the production for this by-product line.</span></span>
-   <span data-ttu-id="5b63f-149">**“百分比”**─ 成本额按在生产中消耗的原材料总成本的百分比计算。</span><span class="sxs-lookup"><span data-stu-id="5b63f-149">**Percent** ─ The cost amount is calculated as a percentage of the total cost of raw materials that are consumed in the production.</span></span> <span data-ttu-id="5b63f-150">在字段中输入用于该计算的百分比。</span><span class="sxs-lookup"><span data-stu-id="5b63f-150">The percentage that is used for the calculation is entered in the field.</span></span>
-   <span data-ttu-id="5b63f-151">**“按系列”**─ 成本金额按照生产订单的每条件批次规模的金额计算。</span><span class="sxs-lookup"><span data-stu-id="5b63f-151">**Per series** ─ The cost amount is calculated as an amount per standard batch size of the production order.</span></span> <span data-ttu-id="5b63f-152">此金额与在生产中报告的数量无关。</span><span class="sxs-lookup"><span data-stu-id="5b63f-152">This amount is independent of the reported quantity in the production.</span></span> <span data-ttu-id="5b63f-153">在字段中输入用于该计算的金额。</span><span class="sxs-lookup"><span data-stu-id="5b63f-153">The amount that is used for the calculation is entered in the field.</span></span>
-   <span data-ttu-id="5b63f-154">**按数量** ─ 成本金额按照生产中每配方物料报告的数量的金额计算。</span><span class="sxs-lookup"><span data-stu-id="5b63f-154">**Per quantity** ─ The cost amount is calculated as an amount per reported quantity of the formula item in the production.</span></span> <span data-ttu-id="5b63f-155">在字段中输入用于该计算的金额。</span><span class="sxs-lookup"><span data-stu-id="5b63f-155">The amount that is used for the calculation is entered in the field.</span></span>





