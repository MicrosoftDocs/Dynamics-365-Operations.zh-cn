---
title: 分类管理
description: 此主题介绍 Dynamics 365 Commerce 中分类管理的基本概念，并提供有关项目的实施注意事项。
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: e1b177989065740eef0bd917a7ce1e0a2c79088b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410412"
---
# <a name="assortment-management"></a><span data-ttu-id="a0de3-103">分类管理</span><span class="sxs-lookup"><span data-stu-id="a0de3-103">Assortment management</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="a0de3-104">概览</span><span class="sxs-lookup"><span data-stu-id="a0de3-104">Overview</span></span>

<span data-ttu-id="a0de3-105">Dynamics 365 Commerce 提供 *分类*，供您管理渠道中的产品可用性。</span><span class="sxs-lookup"><span data-stu-id="a0de3-105">Dynamics 365 Commerce provides *assortments* that let you manage product availability across channels.</span></span> <span data-ttu-id="a0de3-106">分类决定哪些产品在特定商店和特定时间段内可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-106">Assortments determine which products are available at specific stores and during a specific period.</span></span>

<span data-ttu-id="a0de3-107">在 Commerce 中，分类是将一个或多个渠道（当使用了组织层次结构时则为渠道组）映射到一个或多个产品（当使用了类别层次结构时为产品组）。</span><span class="sxs-lookup"><span data-stu-id="a0de3-107">In Commerce, an assortment is a mapping of one or more channels (or groups of channels, when organization hierarchies are used) to one or more products (or groups of products, when category hierarchies are used).</span></span>

<span data-ttu-id="a0de3-108">渠道的总体产品组合由分配给该渠道的所发布分类决定。</span><span class="sxs-lookup"><span data-stu-id="a0de3-108">The overall product mix of a channel is determined by the published assortments that are assigned to the channel.</span></span> <span data-ttu-id="a0de3-109">因此，可以为每个渠道配置多个活动分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-109">Therefore, you can configure multiple active assortments per channel.</span></span>

### <a name="basic-assortment-setup"></a><span data-ttu-id="a0de3-110">基本分类设置</span><span class="sxs-lookup"><span data-stu-id="a0de3-110">Basic assortment setup</span></span>

<span data-ttu-id="a0de3-111">在以下示例中，为每个商店配置了一个唯一的分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-111">In the following example, a unique assortment is configured for each store.</span></span> <span data-ttu-id="a0de3-112">在此情况下，商店 1 中只有产品 1 可用，商店 2 中只有产品 2 可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-112">In this case, only product 1 is available at store 1, and only product 2 is available at store 2.</span></span>

![每个产品可在一个商店提供](./media/Managing-assortments-figure1.png)

<span data-ttu-id="a0de3-114">若要让产品 2 在商店 1 可用，可将该产品添加到分类 1。</span><span class="sxs-lookup"><span data-stu-id="a0de3-114">To make product 2 available at store 1, you can add the product to assortment 1.</span></span>

![添加到分类 1 的产品 2](./media/Managing-assortments-figure2.png)

<span data-ttu-id="a0de3-116">也可以将商店 1 添加到分类 2。</span><span class="sxs-lookup"><span data-stu-id="a0de3-116">Alternatively, you can add store 1 to assortment 2.</span></span>

![添加到分类 2 的商店 1](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a><span data-ttu-id="a0de3-118">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="a0de3-118">Organization hierarchies</span></span>

<span data-ttu-id="a0de3-119">如果多个渠道共用同一个产品分类，则可使用 Commerce 分类组织层次结构配置分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-119">In situations where multiple channels share the same product assortments, you can configure the assortments by using the Commerce assortment organization hierarchy.</span></span> <span data-ttu-id="a0de3-120">添加此层次结构中的节点时，将包括该节点及其子节点中的所有渠道。</span><span class="sxs-lookup"><span data-stu-id="a0de3-120">When nodes from this hierarchy are added, all channels in that node and its child nodes will be included.</span></span>

![组织层次结构](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a><span data-ttu-id="a0de3-122">产品类别</span><span class="sxs-lookup"><span data-stu-id="a0de3-122">Product categories</span></span>

<span data-ttu-id="a0de3-123">同样，在产品方面，可使用产品类别层次结构包括产品组。</span><span class="sxs-lookup"><span data-stu-id="a0de3-123">Similarly, on the product side, you can include groups of products by using product category hierarchies.</span></span> <span data-ttu-id="a0de3-124">可通过包括一个或多个类别层次结构节点配置分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-124">You can configure assortments by including one or more category hierarchy nodes.</span></span> <span data-ttu-id="a0de3-125">在此情况下，分类将包括该类别节点及其子节点中的所有产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-125">In this case, the assortment will include all products in that category node and its child nodes.</span></span>

![产品类别](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a><span data-ttu-id="a0de3-127">排除的产品或类别</span><span class="sxs-lookup"><span data-stu-id="a0de3-127">Excluded products or categories</span></span>

<span data-ttu-id="a0de3-128">除了在分类中包括产品和类别，还可以使用“排除”选项定义分类中应排除的特定产品或类别。</span><span class="sxs-lookup"><span data-stu-id="a0de3-128">In addition to including products and categories in assortments, you can use the Exclude option to define specific products or categories that should be excluded from assortments.</span></span> <span data-ttu-id="a0de3-129">在以下示例中，要包括特定类别中除产品 2 之外的所有产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-129">In the following example, you want to include all the products in a specific category, except product 2.</span></span> <span data-ttu-id="a0de3-130">在此情况下，不必逐个产品定义分类或创建更多分类节点。</span><span class="sxs-lookup"><span data-stu-id="a0de3-130">In this case, you don't have to define the assortment product by product or create additional category nodes.</span></span> <span data-ttu-id="a0de3-131">而是只需包括分类，但排除该产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-131">Instead, you can just include the category but exclude the product.</span></span>

> [!NOTE]
> <span data-ttu-id="a0de3-132">如果按照定义某个产品同时在一个或多个分类中既包括又排除，将始终把该产品视为排除。</span><span class="sxs-lookup"><span data-stu-id="a0de3-132">If a product is both included and excluded in one or more assortments by definition, the product will always be considered excluded.</span></span>

![排除的产品](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a><span data-ttu-id="a0de3-134">全局产品和已发放产品</span><span class="sxs-lookup"><span data-stu-id="a0de3-134">Global and released products</span></span>

<span data-ttu-id="a0de3-135">分类在全局级别定义，可包含来自多个法人的渠道。</span><span class="sxs-lookup"><span data-stu-id="a0de3-135">Assortments are defined at a global level and can contain channels from multiple legal entities.</span></span> <span data-ttu-id="a0de3-136">分类中包含的产品和类别也在法人之间共享。</span><span class="sxs-lookup"><span data-stu-id="a0de3-136">The products and categories that are included in assortments are also shared across legal entities.</span></span> <span data-ttu-id="a0de3-137">但是，产品必须先发放，才能真正在渠道（例如，销售点 \[POS\]）中出售、订购、盘点或接收。</span><span class="sxs-lookup"><span data-stu-id="a0de3-137">However, a product must be released before it can actually be sold, ordered, counted, or received in the channel (for example, in the point of sale \[POS\]).</span></span> <span data-ttu-id="a0de3-138">因此，尽管不同法人的两家商店可以共享包含相同产品的分类，但是这些产品仅当已发放给这些法人时，才可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-138">Therefore, although two stores in different legal entities can share an assortment that contains the same products, the products are available only if they have been released to those legal entities.</span></span>

### <a name="dynamic-and-static-assortments"></a><span data-ttu-id="a0de3-139">动态分类和静态分类</span><span class="sxs-lookup"><span data-stu-id="a0de3-139">Dynamic and static assortments</span></span>

<span data-ttu-id="a0de3-140">可以使用特定渠道和产品或通过包括组织单位和类别来定义分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-140">Assortments can be defined with specific channels and products or by including organization units and categories.</span></span> <span data-ttu-id="a0de3-141">包括对这些组的引用的分类视为动态分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-141">Assortments including references to these groups are considered dynamic assortments.</span></span> <span data-ttu-id="a0de3-142">如果分类处于活动状态时这些组的定义或内容改变，分类的定义也将改变。</span><span class="sxs-lookup"><span data-stu-id="a0de3-142">If the definition or contents of those groups change while the assortment is active, the definition of the assortment will also change.</span></span>

<span data-ttu-id="a0de3-143">例如，最初定义并发布了一个分类，因此其引用一个产品类别。</span><span class="sxs-lookup"><span data-stu-id="a0de3-143">For example, an assortment is originally defined and published so that it references a category of products.</span></span> <span data-ttu-id="a0de3-144">如果以后向该类别添加更多产品，现有分类的定义中将自动包括这些产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-144">If additional products are later added to the category, those products are automatically included in the definition of the existing assortment.</span></span> <span data-ttu-id="a0de3-145">您不必手动向分类添加产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-145">You don't have to manually add the products to the assortment.</span></span> <span data-ttu-id="a0de3-146">同样，如果向其他节点添加组织单位，将根据该定义自动调整这个组织单位的分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-146">Similarly, if an organization unit is added to a different node, the organization unit's assortment is automatically adjusted based on that definition.</span></span>

### <a name="stopped-products"></a><span data-ttu-id="a0de3-147">已停止的产品</span><span class="sxs-lookup"><span data-stu-id="a0de3-147">Stopped products</span></span>

<span data-ttu-id="a0de3-148">可通过在 **默认订单** 设置中开启设置来为销售流程“停止”已发放的产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-148">You can "stop" released products for the sales process by turning on a setting in the **Default order** settings.</span></span> <span data-ttu-id="a0de3-149">该设置在产品处于使用寿命末期，因此不应在任何渠道出售时最常用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-149">This setting is most often used when a product is at the end of its life and should not be sold at any channel.</span></span> <span data-ttu-id="a0de3-150">分类遵守此设置，因此无论分类配置如何，将不为已停止的产品分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-150">Assortments respect this setting, and stopped products won't be assorted, regardless of the assortment configuration.</span></span>

### <a name="blocked-products"></a><span data-ttu-id="a0de3-151">阻止的产品</span><span class="sxs-lookup"><span data-stu-id="a0de3-151">Blocked products</span></span>

<span data-ttu-id="a0de3-152">除了停止销售产品，还可以临时阻止销售产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-152">In addition to stopping sales of a product, you can temporarily block sales of a product.</span></span> <span data-ttu-id="a0de3-153">可在已发放产品的 **Commerce** 选项卡上配置此设置。</span><span class="sxs-lookup"><span data-stu-id="a0de3-153">You can configure this setting on the **Commerce** tab of a released product.</span></span> <span data-ttu-id="a0de3-154">仍将对已阻止的产品分类，但您将在 POS 中收到一条消息，说明不能出售该产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-154">Blocked products are still assorted, but you will receive a message in the POS that states that the product can't be sold.</span></span>

### <a name="date-effectivity"></a><span data-ttu-id="a0de3-155">日期有效性</span><span class="sxs-lookup"><span data-stu-id="a0de3-155">Date effectivity</span></span>

<span data-ttu-id="a0de3-156">分类具有时效性。</span><span class="sxs-lookup"><span data-stu-id="a0de3-156">Assortments are date-effective.</span></span> <span data-ttu-id="a0de3-157">因此，零售商可按渠道配置产品何时应可用，何时应不可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-157">Therefore, retailers can configure when products should or should not be available per channel.</span></span> <span data-ttu-id="a0de3-158">可提前定义和发布分类，还可以指定开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="a0de3-158">You can define and publish assortments ahead of time, and specify the start and end dates.</span></span> <span data-ttu-id="a0de3-159">产品将在指定的日期自动变为可用或不可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-159">The products will automatically become available or unavailable on the specified dates.</span></span>

### <a name="process-assortments-batch-job"></a><span data-ttu-id="a0de3-160">处理分类批处理作业</span><span class="sxs-lookup"><span data-stu-id="a0de3-160">Process assortments batch job</span></span>

<span data-ttu-id="a0de3-161">Commerce 中定义的分类必须先经过处理，才能生效。</span><span class="sxs-lookup"><span data-stu-id="a0de3-161">Assortments that are defined in Commerce must be processed before they take effect.</span></span> <span data-ttu-id="a0de3-162">执行此项处理是因为：</span><span class="sxs-lookup"><span data-stu-id="a0de3-162">This processing is done for the following reasons:</span></span>

- <span data-ttu-id="a0de3-163">分类定义必须去常态化，以便可供渠道更容易使用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-163">Assortment definitions must be de-normalized so that channels can more easily consume them.</span></span> <span data-ttu-id="a0de3-164">可通过跨多个日期范围的多个分类为渠道定义混合产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-164">A product mix for a channel can be defined through multiple assortments that span various date ranges.</span></span> <span data-ttu-id="a0de3-165">提前在服务器上计算此信息中的一部分时，将提高渠道的绩效。</span><span class="sxs-lookup"><span data-stu-id="a0de3-165">When some of this information is calculated ahead of time on the server, performance at the channel is improved.</span></span>
- <span data-ttu-id="a0de3-166">分类中的产品和渠道可在分类本身外部改变。</span><span class="sxs-lookup"><span data-stu-id="a0de3-166">The products and channels in the assortment can change outside the assortment itself.</span></span> <span data-ttu-id="a0de3-167">必须定期处理包含对类别或组织单位的引用的动态分类，以使其根据自己的的当前分配情况包括或排除记录。</span><span class="sxs-lookup"><span data-stu-id="a0de3-167">Dynamic assortments that contain references to categories or organization units must be processed periodically so that they include or exclude records, based on their current assignment.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="a0de3-168">实施注意事项</span><span class="sxs-lookup"><span data-stu-id="a0de3-168">Implementation considerations</span></span>

<span data-ttu-id="a0de3-169">计划和管理 Commerce 实施的分类时，请注意以下实施要求：</span><span class="sxs-lookup"><span data-stu-id="a0de3-169">Consider the following implementation requirements as you plan and manage assortments for your Commerce implementation:</span></span>

- <span data-ttu-id="a0de3-170">**数据复制和数据库大小** – 虽然分类有助于满足企业对管理产品可用性的需要，却也是管理渠道规模和脱机数据库大小的重要工具。</span><span class="sxs-lookup"><span data-stu-id="a0de3-170">**Data replication and database size** – Although assortments help serve the business need to manage product availability, they are also an important tool for managing the size of channel and offline databases.</span></span> <span data-ttu-id="a0de3-171">管理有方的分类可帮助减少必须处理并复制到渠道和脱机数据库的数据量。</span><span class="sxs-lookup"><span data-stu-id="a0de3-171">Well-managed assortments help reduce the amount of data that must be processed and replicated to channel and offline databases.</span></span> <span data-ttu-id="a0de3-172">还可以帮助减少必须保留的记录数量。</span><span class="sxs-lookup"><span data-stu-id="a0de3-172">They also help reduce the number of records that must be persisted.</span></span> <span data-ttu-id="a0de3-173">这些数据库中更少的记录将在向交易记录添加项，搜索和浏览产品时提高性能。</span><span class="sxs-lookup"><span data-stu-id="a0de3-173">Fewer records in these databases will increase performance when you add items to a transaction, search, and browse for products.</span></span>
- <span data-ttu-id="a0de3-174">**时效性/到期分类** – 用于管理渠道和脱机数据库中的产品数量的最有效工具之一是分类的时效性。</span><span class="sxs-lookup"><span data-stu-id="a0de3-174">**Date-effective/expiring assortments** – One of the most effective tools for managing the number of products in channel and offline databases is the date effectivity of assortments.</span></span> <span data-ttu-id="a0de3-175">如果保留季节性产品或处于使用周期结束阶段的产品的开放式（不到期）分类，这些数据库的大小将一直增加下去。</span><span class="sxs-lookup"><span data-stu-id="a0de3-175">If you leave open-ended (non-expiring) assortments for seasonal products or products that are at the end of their life, these databases will grow indefinitely.</span></span> <span data-ttu-id="a0de3-176">您可以使用各种方法来帮助应对这种情况。</span><span class="sxs-lookup"><span data-stu-id="a0de3-176">You can use various approaches to help manage this situation.</span></span> <span data-ttu-id="a0de3-177">例如，可为季节性产品和始终可用的产品维护单独的分类。</span><span class="sxs-lookup"><span data-stu-id="a0de3-177">For example, you can maintain separate assortments for seasonal products and products that are always available.</span></span>
- <span data-ttu-id="a0de3-178">**分类外销售和退货** – 此功能帮助零售商有效管理分类，方法是将可用产品的数量限制为属于商店核心产品组合的产品。</span><span class="sxs-lookup"><span data-stu-id="a0de3-178">**Sales and returns outside assortments** – This capability helps retailers effectively manage their assortments by letting them limit the number of available products to products that belong to the core product mix for the store.</span></span> <span data-ttu-id="a0de3-179">此功能还可以帮助零售商处理下面的情况：分类中错误地遗漏了某个产品，或者产品因超出分类的有效期而退货。</span><span class="sxs-lookup"><span data-stu-id="a0de3-179">This capability also helps retailers handle situations where a product was mistakenly omitted from an assortment, or where a product was returned outside the effective dates for the assortment.</span></span>

<span data-ttu-id="a0de3-180">如果产品数据在渠道数据库中不存在，POS 将实时调用总部数据以检索所需信息，以便出售、退回产品或将产品放入客户订单中。</span><span class="sxs-lookup"><span data-stu-id="a0de3-180">If product data doesn't exist in the channel database, the POS makes real-time calls to headquarters to retrieve the required information, so that the product can be sold, returned, or put on a customer order.</span></span> <span data-ttu-id="a0de3-181">通过这种方式检索的产品信息只能在交易记录范围内可用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-181">Product information that is retrieved in this manner is available only during the scope of that transaction.</span></span> <span data-ttu-id="a0de3-182">将不会把产品添加到分类定义。</span><span class="sxs-lookup"><span data-stu-id="a0de3-182">The product isn't added to the assortment definition.</span></span> <span data-ttu-id="a0de3-183">因此，必须执行后续实时调用。</span><span class="sxs-lookup"><span data-stu-id="a0de3-183">Therefore, subsequent real-time calls will be made as required.</span></span>
