---
title: 产品生命周期状态概览
description: 产品生命周期状态记载已发布产品或产品变型的生命周期状态。
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 51a6b19e84f368bf72b664e120f262ddcf7c7611
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423457"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="15a02-103">产品生命周期状态概览</span><span class="sxs-lookup"><span data-stu-id="15a02-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15a02-104">产品生命周期状态记载已发布产品或产品变型的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="15a02-105">产品生命周期状态由用户定义，通常是产品经理或产品主数据经理。</span><span class="sxs-lookup"><span data-stu-id="15a02-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="15a02-106">特定业务流程，例如主计划，可能受特定生命周期状态的影响。</span><span class="sxs-lookup"><span data-stu-id="15a02-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>

<span data-ttu-id="15a02-107">已发布产品或产品变型可以与记载特定产品或变型目前所处生命周期状态的产品生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="15a02-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="15a02-108">您可以通过指定状态名称和描述的方式定义任何数量的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="15a02-109">您可以选择一个生命周期状态作为新发布产品的默认状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="15a02-110">已发布产品变型在创建时从它们已发布的基础产品继承其产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="15a02-111">在已发布基础产品上更改生命周期状态时，您可以选择更新具有相同原始状态的所有现有变型。</span><span class="sxs-lookup"><span data-stu-id="15a02-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="15a02-112">创建新产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-112">Create a new product lifecycle state</span></span>

- <span data-ttu-id="15a02-113">要创建新的产品生命周期状态，请参阅[创建新的产品生命周期状态](tasks/new-product-lifecycle-state.md)。</span><span class="sxs-lookup"><span data-stu-id="15a02-113">To create a new product lifecycle state, see [Create a new product lifecycle state](tasks/new-product-lifecycle-state.md).</span></span>

- <span data-ttu-id="15a02-114">要创建默认产品生命周期状态，请参阅[创建默认产品生命周期状态](tasks/default-product-lifecycle-state.md)。</span><span class="sxs-lookup"><span data-stu-id="15a02-114">To create a default product lifecycle state, see [Create a default product lifecycle state](tasks/default-product-lifecycle-state.md).</span></span>

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="15a02-115">将产品生命周期状态关联到发布的产品</span><span class="sxs-lookup"><span data-stu-id="15a02-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="15a02-116">有多种方式将产品生命周期状态关联到发布的产品或产品变型。</span><span class="sxs-lookup"><span data-stu-id="15a02-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

- <span data-ttu-id="15a02-117">在创建新发布产品时，自动分配默认的 **产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="15a02-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="15a02-118">在将产品发布到法人时，自动分配默认的 **产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="15a02-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="15a02-119">在将产品变型发布到法人时，与该法人中的已发布产品变型关联的 **产品生命周期状态** 自动分配到新的变型。</span><span class="sxs-lookup"><span data-stu-id="15a02-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span>

<span data-ttu-id="15a02-120">您可以使用以下方式手动更新产品生命周期状态：</span><span class="sxs-lookup"><span data-stu-id="15a02-120">You can manually update the product lifecycle state by using:</span></span>

- <span data-ttu-id="15a02-121">**已发布产品** 列表页或 **详细信息视图**。</span><span class="sxs-lookup"><span data-stu-id="15a02-121">The **Released products** list page or **Details view**.</span></span>
- <span data-ttu-id="15a02-122">**已发布的产品变型** 列表页或 **详细信息视图**。</span><span class="sxs-lookup"><span data-stu-id="15a02-122">The **Released product variants** list page or **Details view**.</span></span>
- <span data-ttu-id="15a02-123">基于需求查找过时的产品或产品变型并关联生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="15a02-124">有关详细信息：</span><span class="sxs-lookup"><span data-stu-id="15a02-124">For more information:</span></span>

- <span data-ttu-id="15a02-125">要将产品生命周期状态关联到已发布的基础产品，请参阅[对已发布的基础产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product-master.md)。</span><span class="sxs-lookup"><span data-stu-id="15a02-125">To associate a product lifecycle state to a released product master, see [Assign a product lifecycle state to a released product master](tasks/product-lifecycle-state-released-product-master.md).</span></span>

- <span data-ttu-id="15a02-126">要将产品生命周期状态关联到发布产品，请参阅[对已发布产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15a02-126">To associate a product lifecycle state to a release product, see [Assign a product lifecycle state to a released product](tasks/product-lifecycle-state-released-product.md).</span></span>

## <a name="impact-on-master-planning"></a><span data-ttu-id="15a02-127">对主计划的影响</span><span class="sxs-lookup"><span data-stu-id="15a02-127">Impact on master planning</span></span>

<span data-ttu-id="15a02-128">产品生命周期状态只有一个控制标志：**对于计划有效**。</span><span class="sxs-lookup"><span data-stu-id="15a02-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="15a02-129">默认情况下对所有创建的产品生命周期状态设置为 **是**，但可以更改为 **否**。</span><span class="sxs-lookup"><span data-stu-id="15a02-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="15a02-130">设置为 **否** 时，关联的已发布产品或已发布产品变型为：</span><span class="sxs-lookup"><span data-stu-id="15a02-130">When set to **No**, the associated released products or released product variants are:</span></span>

- <span data-ttu-id="15a02-131">从主计划排除。</span><span class="sxs-lookup"><span data-stu-id="15a02-131">Excluded from master planning.</span></span>
- <span data-ttu-id="15a02-132">从物料清单级别计算中排除。</span><span class="sxs-lookup"><span data-stu-id="15a02-132">Excluded from BOM-level calculation.</span></span>

<span data-ttu-id="15a02-133">有关如何使用产品生命周期状态从主计划和物料清单级别计算中排除产品的详细信息，请参阅[创建产品生命周期状态以从主计划中排除产品](tasks/exclude-products-master-planning.md)</span><span class="sxs-lookup"><span data-stu-id="15a02-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, see [Create a product lifecycle state to exclude products from Master planning](tasks/exclude-products-master-planning.md)</span></span>

> [!NOTE]
> <span data-ttu-id="15a02-134">由于性能原因，强烈建议使用对主计划禁用的产品生命周期状态关联所有过时的已发布产品或产品变型，尤其是当使用不可重复使用的产品配置变型时。</span><span class="sxs-lookup"><span data-stu-id="15a02-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="15a02-135">默认迁移、导入和导出</span><span class="sxs-lookup"><span data-stu-id="15a02-135">Default migration, import, and export</span></span>

<span data-ttu-id="15a02-136">产品生命周期状态受数据实体的支持，生命周期状态可以通过已发布产品的数据实体或已发布变型的数据实体设置为可变状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="15a02-137">查找过时的产品和产品变型</span><span class="sxs-lookup"><span data-stu-id="15a02-137">Find obsolete products and products variants</span></span>

<span data-ttu-id="15a02-138">您可以运行模拟分析以查找过时的已发布产品或产品变型，然后更新它们的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="15a02-139">要查找过时的产品，请参阅[查找过时的产品变型并分配产品生命周期状态](tasks/obsolete-product-variants.md)。</span><span class="sxs-lookup"><span data-stu-id="15a02-139">To find obsolete products, see [Find obsolete product variants and assign a product lifecycle state](tasks/obsolete-product-variants.md).</span></span> <span data-ttu-id="15a02-140">此主题介绍如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。</span><span class="sxs-lookup"><span data-stu-id="15a02-140">This topic shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="15a02-141">它还显示如何查看模拟结果以及评估在不通过模拟运行更新时有多少产品和产品变型将与新产品生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="15a02-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="15a02-142">通过在模拟模式中运行分析，标识为过时的产品和产品变型显示在特定窗体中，可以轻松地查看。</span><span class="sxs-lookup"><span data-stu-id="15a02-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="15a02-143">分析过程将搜索交易记录和特定主数据，以识别在特定可变期间内没有需求且没有可以产生需求的主数据的产品。</span><span class="sxs-lookup"><span data-stu-id="15a02-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="15a02-144">在可变期间内新发布的产品可以从分析中排除。</span><span class="sxs-lookup"><span data-stu-id="15a02-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="15a02-145">当分析模拟返回预期结果时，用户可以运行分析并对在分析过程中识别为过时的所有产品设置新的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="15a02-146">请注意，所有分析和更新必须在相同法人内进行。</span><span class="sxs-lookup"><span data-stu-id="15a02-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="15a02-147">选择和更新已发布产品或产品变型的条件</span><span class="sxs-lookup"><span data-stu-id="15a02-147">Criteria to select and update released products or product variants</span></span>

<span data-ttu-id="15a02-148">使用以下条件选择和更新已发布的产品和产品变型：</span><span class="sxs-lookup"><span data-stu-id="15a02-148">Use the following criteria to select and update the released products and product variants:</span></span>

- <span data-ttu-id="15a02-149">产品或产品变型的产品生命周期状态必须不同于新的所需状态。</span><span class="sxs-lookup"><span data-stu-id="15a02-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span>
- <span data-ttu-id="15a02-150">产品或产品变型基于您在选择对话框中输入的天数提前几天创建。</span><span class="sxs-lookup"><span data-stu-id="15a02-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span>
- <span data-ttu-id="15a02-151">没有针对该产品或产品变型的开放生产订单（= 状态 < 已结束）。</span><span class="sxs-lookup"><span data-stu-id="15a02-151">There are no open production orders (= status < ended) for the product or product variant.</span></span>
- <span data-ttu-id="15a02-152">没有针对该产品或产品变型的开放库存交易记录（= 状态发货 ReservPhysical 到 QuotationIssue 或状态收货已登记到 QuotationReceipt）。</span><span class="sxs-lookup"><span data-stu-id="15a02-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span>
- <span data-ttu-id="15a02-153">在过去几天内没有针对该产品或产品变型的库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="15a02-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span>
- <span data-ttu-id="15a02-154">没有针对该产品或产品变型的未来需求或供应预测。</span><span class="sxs-lookup"><span data-stu-id="15a02-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
- <span data-ttu-id="15a02-155">在物料覆盖范围中没有针对该产品或产品变型设定最低存货水平。</span><span class="sxs-lookup"><span data-stu-id="15a02-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span>
- <span data-ttu-id="15a02-156">没有针对该产品或产品变型的有效固定数量看板规则。</span><span class="sxs-lookup"><span data-stu-id="15a02-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
- <span data-ttu-id="15a02-157">没有针对该产品或产品变型的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="15a02-157">No service order line for the product or product variant.</span></span>
- <span data-ttu-id="15a02-158">没有针对该产品或产品变型的活跃或未来销售或购买协议行。</span><span class="sxs-lookup"><span data-stu-id="15a02-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span>
- <span data-ttu-id="15a02-159">产品或产品变型在与对于计划有效的产品或变型的未过期的已核准的物料清单版本关联的物料清单中不使用。</span><span class="sxs-lookup"><span data-stu-id="15a02-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a02-160">相关主题</span><span class="sxs-lookup"><span data-stu-id="15a02-160">Related topics</span></span>

- [<span data-ttu-id="15a02-161">创建新产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
- [<span data-ttu-id="15a02-162">创建默认产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
- [<span data-ttu-id="15a02-163">为已发布的基础产品分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
- [<span data-ttu-id="15a02-164">为已发布的产品分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
- [<span data-ttu-id="15a02-165">查找过时的产品变型并分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="15a02-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
- [<span data-ttu-id="15a02-166">创建产品生命周期状态以从主计划中排除产品</span><span class="sxs-lookup"><span data-stu-id="15a02-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)
