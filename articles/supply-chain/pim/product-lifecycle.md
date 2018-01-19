---
title: "产品生命周期状态"
description: "产品生命周期状态记载已发布产品或产品变型的生命周期状态。"
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8337f1dfb938f9fa69924e77a25a68ee56dbd2ac
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="daa61-103">产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="daa61-104">产品生命周期状态记载已发布产品或产品变型的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="daa61-105">产品生命周期状态由用户定义，通常是产品经理或产品主数据经理。</span><span class="sxs-lookup"><span data-stu-id="daa61-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="daa61-106">特定业务流程，例如主计划，可能受特定生命周期状态的影响。</span><span class="sxs-lookup"><span data-stu-id="daa61-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="daa61-107">已发布产品或产品变型可以与记载特定产品或变型目前所处生命周期状态的产品生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="daa61-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="daa61-108">您可以通过指定状态名称和描述的方式定义任何数量的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="daa61-109">您可以选择一个生命周期状态作为新发布产品的默认状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="daa61-110">已发布产品变型在创建时从它们已发布的基础产品继承其产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="daa61-111">在已发布基础产品上更改生命周期状态时，您可以选择更新具有相同原始状态的所有现有变型。</span><span class="sxs-lookup"><span data-stu-id="daa61-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="daa61-112">创建新的产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="daa61-113">要创建新的产品生命周期状态，请播放或阅读任务指南**创建新的产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="daa61-114">要创建默认的产品生命周期状态，请播放或阅读任务指南**创建默认的产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="daa61-115">将产品生命周期状态关联到发布的产品</span><span class="sxs-lookup"><span data-stu-id="daa61-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="daa61-116">有多种方式将产品生命周期状态关联到发布的产品或产品变型。</span><span class="sxs-lookup"><span data-stu-id="daa61-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="daa61-117">在创建新发布产品时，自动分配默认的**产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="daa61-118">在将产品发布到法人时，自动分配默认的**产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="daa61-119">在将产品变型发布到法人时，与该法人中的已发布产品变型关联的**产品生命周期状态**自动分配到新的变型。</span><span class="sxs-lookup"><span data-stu-id="daa61-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="daa61-120">您可以使用以下方式手动更新产品生命周期状态：</span><span class="sxs-lookup"><span data-stu-id="daa61-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="daa61-121">**已发布产品**列表页或**详细信息视图**。</span><span class="sxs-lookup"><span data-stu-id="daa61-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="daa61-122">**已发布的产品变型**列表页或**详细信息视图**。</span><span class="sxs-lookup"><span data-stu-id="daa61-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="daa61-123">基于需求查找过时的产品或产品变型并关联生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="daa61-124">有关如何关联产品生命周期状态的详细信息，请播放或阅读以下两个任务指南。</span><span class="sxs-lookup"><span data-stu-id="daa61-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="daa61-125">要将产品生命周期状态关联到已发布的基础产品，请播放或阅读任务指南**对已发布的基础产品分配产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="daa61-126">要将产品生命周期状态关联到发布产品，请播放或阅读任务指南**对已发布的产品分配产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="daa61-127">对主计划的影响</span><span class="sxs-lookup"><span data-stu-id="daa61-127">Impact on master planning</span></span> 

<span data-ttu-id="daa61-128">产品生命周期状态只有一个控制标志：**对于计划有效**。</span><span class="sxs-lookup"><span data-stu-id="daa61-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="daa61-129">默认情况下对所有创建的产品生命周期状态设置为**是**，但可以更改为**否**。</span><span class="sxs-lookup"><span data-stu-id="daa61-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="daa61-130">设置为**否**时，关联的已发布产品或已发布产品变型为：</span><span class="sxs-lookup"><span data-stu-id="daa61-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="daa61-131">从主计划排除。</span><span class="sxs-lookup"><span data-stu-id="daa61-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="daa61-132">从物料清单级别计算中排除。</span><span class="sxs-lookup"><span data-stu-id="daa61-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="daa61-133">有关如何使用产品生命周期状态从主计划和物料清单级别计算中排除产品的详细信息，请播放或阅读任务指南**创建产品生命周期状态以从主计划中排除产品**。</span><span class="sxs-lookup"><span data-stu-id="daa61-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="daa61-134">由于性能原因，强烈建议使用对主计划禁用的产品生命周期状态关联所有过时的已发布产品或产品变型，尤其是当使用不可重复使用的产品配置变型时。</span><span class="sxs-lookup"><span data-stu-id="daa61-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="daa61-135">默认迁移、导入和导出</span><span class="sxs-lookup"><span data-stu-id="daa61-135">Default migration, import, and export</span></span> 

<span data-ttu-id="daa61-136">产品生命周期状态不受数据实体的支持，且生命周期状态无法通过已发布的产品数据实体设置为可变状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="daa61-137">从以前的版本中迁移时，所有产品和产品变型的生命周期状态将为空。</span><span class="sxs-lookup"><span data-stu-id="daa61-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="daa61-138">通过数据实体导入已发布的产品时，将在创建时应用默认的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="daa61-139">通过数据实体导入已发布的产品变型时，将导入已发布的基础产品的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="daa61-140">查找过时的产品和产品变型</span><span class="sxs-lookup"><span data-stu-id="daa61-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="daa61-141">您可以运行模拟分析以查找过时的已发布产品或产品变型，然后更新它们的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="daa61-142">要查找过时的产品，请播放和阅读任务指南**查找过时的产品变型并分配产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="daa61-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="daa61-143">此任务指南显示如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。</span><span class="sxs-lookup"><span data-stu-id="daa61-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="daa61-144">它还显示如何查看模拟结果以及评估在不通过模拟运行更新时有多少产品和产品变型将与新产品生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="daa61-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="daa61-145">通过在模拟模式中运行分析，标识为过时的产品和产品变型显示在特定窗体中，可以轻松地查看。</span><span class="sxs-lookup"><span data-stu-id="daa61-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="daa61-146">分析过程将搜索交易记录和特定主数据，以识别在特定可变期间内没有需求且没有可以产生需求的主数据的产品。</span><span class="sxs-lookup"><span data-stu-id="daa61-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="daa61-147">在可变期间内新发布的产品可以从分析中排除。</span><span class="sxs-lookup"><span data-stu-id="daa61-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="daa61-148">当分析模拟返回预期结果时，用户可以运行分析并对在分析过程中识别为过时的所有产品设置新的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="daa61-149">请注意，所有分析和更新必须在相同法人内进行。</span><span class="sxs-lookup"><span data-stu-id="daa61-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="daa61-150">选择和更新已发布产品或产品变型的条件</span><span class="sxs-lookup"><span data-stu-id="daa61-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="daa61-151">使用以下条件选择和更新已发布的产品和产品变型：</span><span class="sxs-lookup"><span data-stu-id="daa61-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="daa61-152">产品或产品变型的产品生命周期状态必须不同于新的所需状态。</span><span class="sxs-lookup"><span data-stu-id="daa61-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="daa61-153">产品或产品变型基于您在选择对话框中输入的天数提前几天创建。</span><span class="sxs-lookup"><span data-stu-id="daa61-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="daa61-154">没有针对该产品或产品变型的开放生产订单（= 状态 < 已结束）。</span><span class="sxs-lookup"><span data-stu-id="daa61-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-155">没有针对该产品或产品变型的开放库存交易记录（= 状态发货 ReservPhysical 到 QuotationIssue 或状态收货已登记到 QuotationReceipt）。</span><span class="sxs-lookup"><span data-stu-id="daa61-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-156">在过去几天内没有针对该产品或产品变型的库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="daa61-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-157">没有针对该产品或产品变型的未来需求或供应预测。</span><span class="sxs-lookup"><span data-stu-id="daa61-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="daa61-158">在物料覆盖范围中没有针对该产品或产品变型设定最低存货水平。</span><span class="sxs-lookup"><span data-stu-id="daa61-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-159">没有针对该产品或产品变型的有效固定数量看板规则。</span><span class="sxs-lookup"><span data-stu-id="daa61-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="daa61-160">没有针对该产品或产品变型的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="daa61-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-161">没有针对该产品或产品变型的活跃或未来销售或购买协议行。</span><span class="sxs-lookup"><span data-stu-id="daa61-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="daa61-162">产品或产品变型在与对于计划有效的产品或变型的未过期的已核准的物料清单版本关联的物料清单中不使用。</span><span class="sxs-lookup"><span data-stu-id="daa61-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daa61-163">相关主题</span><span class="sxs-lookup"><span data-stu-id="daa61-163">Related topics</span></span>

-  <span data-ttu-id="daa61-164">创建新的产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="daa61-165">创建默认的新产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="daa61-166">对已发布的基础产品分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="daa61-167">对已发布的产品分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="daa61-168">查找过时的产品变型并分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="daa61-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="daa61-169">创建产品生命周期状态以从主计划中排除产品</span><span class="sxs-lookup"><span data-stu-id="daa61-169">Create a product lifecycle state to exclude products from Master planning</span></span>

