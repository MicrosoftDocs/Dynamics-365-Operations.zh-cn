---
title: 配置波次处理
description: 此指南描述了如何设置确定在处理波次时为仓库生成的工作的条件，以及是手动还是自动处理波次。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399146d35388a0151abb23e57bc36ec0173be928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571878"
---
# <a name="configure-wave-processing"></a><span data-ttu-id="7d271-103">配置波次处理</span><span class="sxs-lookup"><span data-stu-id="7d271-103">Configure wave processing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d271-104">此指南描述了如何设置确定在处理波次时为仓库生成的工作的条件，以及是手动还是自动处理波次。</span><span class="sxs-lookup"><span data-stu-id="7d271-104">This guide describes how to set up the criteria that determine what work is generated for a warehouse when a wave is processed, and whether waves are processed manually or automatically.</span></span> <span data-ttu-id="7d271-105">在销售订单、生产订单或看板订单中，通过设置波模板和将波与已发布行匹配的查询来指定条件</span><span class="sxs-lookup"><span data-stu-id="7d271-105">You specify the criteria by setting up wave templates and queries that match a wave with released lines in sales orders, production orders, or kanban orders.</span></span> <span data-ttu-id="7d271-106">波次处理在使用仓库管理模块中的功能的仓库中使用，而不是那些使用库存管理模块中的功能的仓库。</span><span class="sxs-lookup"><span data-stu-id="7d271-106">Wave processing is used in warehouses that use the functionality in the Warehouse management module, and not those that use the functionality in the Inventory management module.</span></span> <span data-ttu-id="7d271-107">您可以使用演示数据公司 USMF 运行此程序。</span><span class="sxs-lookup"><span data-stu-id="7d271-107">You can run this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="7d271-108">转到“仓库管理”>“设置”>“波次”>“波次模板”。</span><span class="sxs-lookup"><span data-stu-id="7d271-108">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="7d271-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7d271-109">Click New.</span></span>
3. <span data-ttu-id="7d271-110">在“波次模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7d271-110">In the Wave template name field, type a value.</span></span>
    * <span data-ttu-id="7d271-111">在您设置波次模板时，您指定模板将在销售订单、生产订单或看板上与已发布行匹配的顺序。</span><span class="sxs-lookup"><span data-stu-id="7d271-111">When you set up a wave template, you specify the sequence in which the templates will be matched to released lines on sales orders, production orders, or kanbans.</span></span> <span data-ttu-id="7d271-112">在行发布到仓库或生产时，它使用第一个与条件匹配的波次模板。</span><span class="sxs-lookup"><span data-stu-id="7d271-112">When a line is released to the warehouse or to production, it uses the first wave template that it meets the criteria for.</span></span> <span data-ttu-id="7d271-113">我们建议您将具有最具体条件的模板置于列表顶部。</span><span class="sxs-lookup"><span data-stu-id="7d271-113">We recommend that you put templates with the most specific criteria at the top of the list.</span></span> <span data-ttu-id="7d271-114">条件越宽泛，行符合条件的可能性就越大，这可能导致将行分配各错误的波。</span><span class="sxs-lookup"><span data-stu-id="7d271-114">The broader the criteria, the more likely it is for a line to meet the criteria, and this could lead to lines being assigned to the wrong wave.</span></span>  
4. <span data-ttu-id="7d271-115">在“波次模板描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7d271-115">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="7d271-116">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d271-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7d271-117">如果您使用 USMF，您可以选择站点 2。</span><span class="sxs-lookup"><span data-stu-id="7d271-117">If you’re using USMF, you can select site 2.</span></span>  
6. <span data-ttu-id="7d271-118">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d271-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7d271-119">如果您使用 USMF，您可以选择仓库 24。</span><span class="sxs-lookup"><span data-stu-id="7d271-119">If you’re using USMF, you can select warehouse 24.</span></span>  
7. <span data-ttu-id="7d271-120">将“自动波次创建”字段设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="7d271-120">Set the Automate wave creation field to Yes.</span></span>
    * <span data-ttu-id="7d271-121">在将销售订单、生产订单或看板发布到仓库时，选择此选项可自动创建波。</span><span class="sxs-lookup"><span data-stu-id="7d271-121">Select this option to automatically create a wave when a sales order, production order, or kanban is released to the warehouse.</span></span>  
8. <span data-ttu-id="7d271-122">设置“在发布到仓库时处理波次”选项为是。</span><span class="sxs-lookup"><span data-stu-id="7d271-122">Set the Process wave at release to warehouse option to Yes.</span></span> 
    * <span data-ttu-id="7d271-123">在将某一行发布到仓库时，选择此选项可自动处理波并创建工作。</span><span class="sxs-lookup"><span data-stu-id="7d271-123">Select this option to automatically process the wave and create work when a line is released to the warehouse.</span></span>  
9. <span data-ttu-id="7d271-124">将“自动波次发布”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="7d271-124">Set the Automate wave release option to Yes.</span></span> 
    * <span data-ttu-id="7d271-125">选择此选项可自动释放波。</span><span class="sxs-lookup"><span data-stu-id="7d271-125">Select this option to automatically release the wave.</span></span> <span data-ttu-id="7d271-126">创建领料工作并使其在移动设备上可用。</span><span class="sxs-lookup"><span data-stu-id="7d271-126">The picking work is created and made available on mobile devices.</span></span>  
10. <span data-ttu-id="7d271-127">设置“分配给开放波次”选项为“是”。</span><span class="sxs-lookup"><span data-stu-id="7d271-127">Set the Assign to open waves option to Yes.</span></span> 
    * <span data-ttu-id="7d271-128">分配给波的各行基于波模板的查询筛选器。</span><span class="sxs-lookup"><span data-stu-id="7d271-128">Lines are assigned to waves based on the query filter for the wave template.</span></span>  
11. <span data-ttu-id="7d271-129">设置“达到阈值时自动处理波次”选项为是。</span><span class="sxs-lookup"><span data-stu-id="7d271-129">Set the Process wave automatically at threshold option to Yes.</span></span> 
    * <span data-ttu-id="7d271-130">在波的值达到“波次阈值”字段组中指定的重量、装运和行的阈值时，选择此选项可自动处理波。</span><span class="sxs-lookup"><span data-stu-id="7d271-130">Select this option to automatically process the wave when its values reach the thresholds for weight, shipment, and lines specified in the Wave thresholds field group.</span></span> <span data-ttu-id="7d271-131">仅当在“波次模板类型”字段中选择“装运”后，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="7d271-131">This option is available only if Shipping is selected in the Wave template type field.</span></span>  
12. <span data-ttu-id="7d271-132">将“自动化补货工作发放”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="7d271-132">Set the Automate replenishment work release option to Yes.</span></span> 
    * <span data-ttu-id="7d271-133">选择此选项可创建基于需求的补货工作并将其自动释放。</span><span class="sxs-lookup"><span data-stu-id="7d271-133">Select this option to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="7d271-134">您必须将补货波方式添加到波模板，然后创建波次需求类型的补货模板。</span><span class="sxs-lookup"><span data-stu-id="7d271-134">You must add the replenishment wave method to the wave template, and create a replenishment template of the type Wave demand.</span></span>  
13. <span data-ttu-id="7d271-135">展开“方法”部分。</span><span class="sxs-lookup"><span data-stu-id="7d271-135">Expand the Methods section.</span></span>
    * <span data-ttu-id="7d271-136">波次模板方法允许您控制每个波次在处理时使用的顺序。</span><span class="sxs-lookup"><span data-stu-id="7d271-136">Wave template methods allow you to control the sequence of activities that each wave is going through when it’s processed.</span></span> <span data-ttu-id="7d271-137">例如，您可能具有波次补货方法。</span><span class="sxs-lookup"><span data-stu-id="7d271-137">For example, you might have a method for wave replenishment.</span></span> <span data-ttu-id="7d271-138">在您添加方法时，它会按照步骤顺序自动在合适的位置列出。</span><span class="sxs-lookup"><span data-stu-id="7d271-138">When you add a method, it’s automatically listed in the appropriate location in the sequence of steps.</span></span> <span data-ttu-id="7d271-139">如果您将“自动化补货工作发放”选项设置为“是”，您需要在此添加补货方法。</span><span class="sxs-lookup"><span data-stu-id="7d271-139">If you’ve set the Automate replenishment work release option to Yes, you need to add the replenish method here.</span></span>  
    * <span data-ttu-id="7d271-140">波次属性充当筛选器，限制可使用该波次的物料类型。</span><span class="sxs-lookup"><span data-stu-id="7d271-140">Wave attributes act as filters, to restrict the kind of items that can use the wave.</span></span> <span data-ttu-id="7d271-141">例如，您可以指定物料组。</span><span class="sxs-lookup"><span data-stu-id="7d271-141">For example, you could specify an item group.</span></span>  
14. <span data-ttu-id="7d271-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7d271-142">Click Save.</span></span>
15. <span data-ttu-id="7d271-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d271-143">Close the page.</span></span>
16. <span data-ttu-id="7d271-144">转到“仓库管理”>“设置”>“仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="7d271-144">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
17. <span data-ttu-id="7d271-145">展开“波次处理”部分。</span><span class="sxs-lookup"><span data-stu-id="7d271-145">Expand the Wave processing section.</span></span>
18. <span data-ttu-id="7d271-146">在“波次处理批处理组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d271-146">In the Wave processing batch group field, enter or select a value.</span></span>
19. <span data-ttu-id="7d271-147">设置“批量处理波次”选项为“是”。</span><span class="sxs-lookup"><span data-stu-id="7d271-147">Set the Process waves in batch option to Yes.</span></span>
20. <span data-ttu-id="7d271-148">在“等待锁定(毫秒)”字段中，输入数字。</span><span class="sxs-lookup"><span data-stu-id="7d271-148">In the Wait for lock (ms) field, enter a number.</span></span>
    * <span data-ttu-id="7d271-149">以毫秒为单位输入分配步骤等待由另一分配步骤锁定的系统资源的时间。</span><span class="sxs-lookup"><span data-stu-id="7d271-149">Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="7d271-150">当超过该时间，将不处理波次，并且显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="7d271-150">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span>  
21. <span data-ttu-id="7d271-151">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7d271-151">Click Save.</span></span>
22. <span data-ttu-id="7d271-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d271-152">Close the page.</span></span>
23. <span data-ttu-id="7d271-153">转到“生产控制”>“设置”>“生产控制参数”。</span><span class="sxs-lookup"><span data-stu-id="7d271-153">Go to Production control > Setup > Production control parameters.</span></span>
24. <span data-ttu-id="7d271-154">在“发放到仓库”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7d271-154">In the Release to warehouse field, select an option.</span></span>
    * <span data-ttu-id="7d271-155">对于销售订单和看板订单，在订单发放到仓库前，必须预留库存。</span><span class="sxs-lookup"><span data-stu-id="7d271-155">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="7d271-156">否则，无法以波次处理物料或分配行。</span><span class="sxs-lookup"><span data-stu-id="7d271-156">Otherwise, the items or allocation lines cannot be processed in a wave.</span></span> <span data-ttu-id="7d271-157">对于生产订单，您还可以选择“允许部分预留”。</span><span class="sxs-lookup"><span data-stu-id="7d271-157">For production orders, you also have the option of choosing Allow partial reservation.</span></span> <span data-ttu-id="7d271-158">例如，如果您有开始生产所需的材料，然后可以等待附加材料变为可用以完成此流程，这很有用。</span><span class="sxs-lookup"><span data-stu-id="7d271-158">For example, this is useful if you have the materials that you need to start production, and can then wait until the additional materials become available to finish the process.</span></span> <span data-ttu-id="7d271-159">如果选择此选项，则当附加材料变为可用时必须手动重复对仓库流程的发放。</span><span class="sxs-lookup"><span data-stu-id="7d271-159">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span>  
25. <span data-ttu-id="7d271-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d271-160">Close the page.</span></span>

