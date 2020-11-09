---
title: 工作策略
description: 本主题说明如何设置工作策略。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 08c04caeace7b8ced40915ace1561d817426cba3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017659"
---
# <a name="work-policies"></a><span data-ttu-id="99510-103">工作策略</span><span class="sxs-lookup"><span data-stu-id="99510-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99510-104">本主题说明如何设置系统和仓库应用，让它们支持工作策略。</span><span class="sxs-lookup"><span data-stu-id="99510-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="99510-105">您可以使用此功能在收到采购订单或转移单或完成制造流程时快速登记库存，而无需创建储存工作。</span><span class="sxs-lookup"><span data-stu-id="99510-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="99510-106">本主题提供一般性信息。</span><span class="sxs-lookup"><span data-stu-id="99510-106">This topic provides general information.</span></span> <span data-ttu-id="99510-107">有关牌照接收的详细信息，请参阅[通过仓库应用进行的牌照接收](warehousing-mobile-device-app-license-plate-receiving.md)。</span><span class="sxs-lookup"><span data-stu-id="99510-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="99510-108">工作策略控制在将制造的物料报告为完工入库时，或在使用仓库应用接收商品时是否创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="99510-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="99510-109">您可以通过定义工作策略所应用的条件来设置每个工作策略：工作订单类型和流程、库存位置和（可选）产品。</span><span class="sxs-lookup"><span data-stu-id="99510-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="99510-110">例如，必须在仓库 *24* 的位置 *RECV* 接收产品 *A0001* 的采购订单。</span><span class="sxs-lookup"><span data-stu-id="99510-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="99510-111">以后，该产品将在位置 *RECV* 的另一个流程中使用。</span><span class="sxs-lookup"><span data-stu-id="99510-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="99510-112">在这种情况下，您可以设置工作策略来阻止当工作人员报告在位置 *RECV* 接收的产品 *A0001* 时创建储存工作。</span><span class="sxs-lookup"><span data-stu-id="99510-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="99510-113">为了使工作策略生效，您必须在 **工作策略** 页面的 **库存位置** 快速选项卡上为其至少定义一个位置。</span><span class="sxs-lookup"><span data-stu-id="99510-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="99510-114">您不能为多个工作政策指定相同的位置。</span><span class="sxs-lookup"><span data-stu-id="99510-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="99510-115">除非创建工作，否则移动设备菜单项的 **打印标签** 选项不会打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="99510-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="99510-116">激活系统中的功能</span><span class="sxs-lookup"><span data-stu-id="99510-116">Activate the features in your system</span></span>

<span data-ttu-id="99510-117">要使本主题中介绍的所有功能在您的系统中可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中启用以下两项功能：</span><span class="sxs-lookup"><span data-stu-id="99510-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="99510-118">牌照接收增强功能</span><span class="sxs-lookup"><span data-stu-id="99510-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="99510-119">入站工作的工作策略增强</span><span class="sxs-lookup"><span data-stu-id="99510-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="99510-120">工作策略页面</span><span class="sxs-lookup"><span data-stu-id="99510-120">The Work policies page</span></span>

<span data-ttu-id="99510-121">要设置工作策略，请转到 **仓库管理 \> 设置 \> 工作 \> 工作策略** 。</span><span class="sxs-lookup"><span data-stu-id="99510-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="99510-122">然后，在每个快速选项卡上，按照以下小节中的说明设置字段。</span><span class="sxs-lookup"><span data-stu-id="99510-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="99510-123">“工作订单类型”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="99510-123">The Work order types FastTab</span></span>

<span data-ttu-id="99510-124">在 **工作订单类型** 快速选项卡上，添加工作策略要应用的所有工作订单类型以及相关的工作流程。</span><span class="sxs-lookup"><span data-stu-id="99510-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="99510-125">工作策略支持以下工作订单类型和相关工作流程。</span><span class="sxs-lookup"><span data-stu-id="99510-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="99510-126">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="99510-126">Work order type</span></span> | <span data-ttu-id="99510-127">工作流程</span><span class="sxs-lookup"><span data-stu-id="99510-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="99510-128">原材料领取</span><span class="sxs-lookup"><span data-stu-id="99510-128">Raw material picking</span></span>| <span data-ttu-id="99510-129">所有相关流程</span><span class="sxs-lookup"><span data-stu-id="99510-129">All related processes</span></span> |
| <span data-ttu-id="99510-130">联产品和副产品储存</span><span class="sxs-lookup"><span data-stu-id="99510-130">Co-product and by-product put away</span></span> | <span data-ttu-id="99510-131">所有相关流程</span><span class="sxs-lookup"><span data-stu-id="99510-131">All related processes</span></span> |
| <span data-ttu-id="99510-132">成品储存</span><span class="sxs-lookup"><span data-stu-id="99510-132">Finished goods putaway</span></span> | <span data-ttu-id="99510-133">所有相关流程</span><span class="sxs-lookup"><span data-stu-id="99510-133">All related processes</span></span> |
| <span data-ttu-id="99510-134">转移收货</span><span class="sxs-lookup"><span data-stu-id="99510-134">Transfer receipt</span></span> | <span data-ttu-id="99510-135">牌照接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="99510-136">采购订单</span><span class="sxs-lookup"><span data-stu-id="99510-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="99510-137">牌照接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="99510-138">加载物料接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="99510-139">采购订单行接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="99510-140">采购订单物料接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="99510-141">要设置工作策略以使其应用于相同工作订单类型的多个工作流程，请在网格中为每个工作流程添加单独的一行。</span><span class="sxs-lookup"><span data-stu-id="99510-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="99510-142">对于网格中的每一行，将 **工作创建方法** 字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="99510-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="99510-143">**从不** – 工作策略将阻止为选定的工作订单类型和相关工作流程创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="99510-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="99510-144">**越库配送** – 工作策略将使用您在 **越库配送策略名称** 字段中选择的策略来创建越库配送工作。</span><span class="sxs-lookup"><span data-stu-id="99510-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="99510-145">“库存位置”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="99510-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="99510-146">在 **库存位置** 快速选项卡上，添加应该应用此工作策略的所有位置。</span><span class="sxs-lookup"><span data-stu-id="99510-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="99510-147">如果工作策略没有关联任何位置，工作策略将不会应用到任何流程。</span><span class="sxs-lookup"><span data-stu-id="99510-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="99510-148">您不能为多个工作政策指定相同的位置。</span><span class="sxs-lookup"><span data-stu-id="99510-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="99510-149">您可以使用分配给 **使用牌照跟踪** 选项关闭的位置模板的仓库位置。</span><span class="sxs-lookup"><span data-stu-id="99510-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="99510-150">在这种情况下，工作人员将直接登记现有库存。</span><span class="sxs-lookup"><span data-stu-id="99510-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="99510-151">“产品”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="99510-151">The Products FastTab</span></span>

<span data-ttu-id="99510-152">在 **产品** 选项卡上，设置 **产品选择** 字段来控制策略应该应用于哪些产品：</span><span class="sxs-lookup"><span data-stu-id="99510-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="99510-153">**所有** – 政策应该应用于所有产品。</span><span class="sxs-lookup"><span data-stu-id="99510-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="99510-154">**选定** – 策略应该仅应用于网格中列出的产品。</span><span class="sxs-lookup"><span data-stu-id="99510-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="99510-155">使用 **产品** 快速选项卡上的工具栏将产品添加到网格或从网格中删除。</span><span class="sxs-lookup"><span data-stu-id="99510-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="99510-156">默认和自定义“目标”位置</span><span class="sxs-lookup"><span data-stu-id="99510-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="99510-157">要使本节中描述的功能在您的系统中可用，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *牌照接收增强* 和 *入站工作的工作策略增强* 功能。</span><span class="sxs-lookup"><span data-stu-id="99510-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="99510-158">以前，系统仅支持在为每个仓库定义的默认位置接收。</span><span class="sxs-lookup"><span data-stu-id="99510-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="99510-159">但是，使用以下工作创建过程的移动设备菜单项现在提供 **使用默认数据** 选项。</span><span class="sxs-lookup"><span data-stu-id="99510-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="99510-160">此选项使您可以将自定义“目标”位置分配给一个或多个菜单项。</span><span class="sxs-lookup"><span data-stu-id="99510-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="99510-161">（此选项已经可用于某些其他类型的菜单项。）</span><span class="sxs-lookup"><span data-stu-id="99510-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="99510-162">牌照接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="99510-163">加载物料接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="99510-164">采购订单行接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="99510-165">采购订单物料接收（和储存）</span><span class="sxs-lookup"><span data-stu-id="99510-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="99510-166">对于使用该菜单项处理的所有订单，菜单项的 **目标位置** 设置将覆盖仓库的默认接收位置。</span><span class="sxs-lookup"><span data-stu-id="99510-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="99510-167">要设置移动设备菜单项以支持在自定义位置接收，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="99510-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="99510-168">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="99510-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="99510-169">选择或创建一个菜单项，该菜单项使用本节前面列出的工作创建流程之一。</span><span class="sxs-lookup"><span data-stu-id="99510-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="99510-170">在 **常规** 快速选项卡上，将 **使用默认数据** 选项设置为 **是** 。</span><span class="sxs-lookup"><span data-stu-id="99510-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="99510-171">在操作窗格中，选择 **默认数据** 。</span><span class="sxs-lookup"><span data-stu-id="99510-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="99510-172">在 **默认数据** 页面，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="99510-173">**默认数据字段：** 将此字段设置为 *目标位置* 。</span><span class="sxs-lookup"><span data-stu-id="99510-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="99510-174">**仓库：** 选择要与此菜单项一起使用的目标仓库。</span><span class="sxs-lookup"><span data-stu-id="99510-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="99510-175">**位置：** 此字段将列出可用于所选仓库的所有位置 ID。</span><span class="sxs-lookup"><span data-stu-id="99510-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="99510-176">但是，此字段的设置实际上没有任何作用。</span><span class="sxs-lookup"><span data-stu-id="99510-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="99510-177">因此，您可以将其留为空白。</span><span class="sxs-lookup"><span data-stu-id="99510-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="99510-178">不过，您可以使用列表来确认必须在 **硬编码值** 字段中输入的 ID。</span><span class="sxs-lookup"><span data-stu-id="99510-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="99510-179">**硬编码值：** 输入适用于此菜单项的接收位置的位置 ID。</span><span class="sxs-lookup"><span data-stu-id="99510-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="99510-180">仅当在相关工作策略设置中列出了所有接收位置时，才能应用工作策略。</span><span class="sxs-lookup"><span data-stu-id="99510-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="99510-181">无论您使用的是默认仓库接收位置还是自定义“目标”位置，此要求均适用。</span><span class="sxs-lookup"><span data-stu-id="99510-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="99510-182">示例方案：仓库接收</span><span class="sxs-lookup"><span data-stu-id="99510-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="99510-183">*采购订单物料接收（和储存）* 流程接收的所有产品都必须在位置 *FL-001* 登记，并且必须在仓库 *24* 中提供。</span><span class="sxs-lookup"><span data-stu-id="99510-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001* , and they must be available in warehouse *24*.</span></span> <span data-ttu-id="99510-184">但是，不应该创建工作。</span><span class="sxs-lookup"><span data-stu-id="99510-184">However, work should not be created.</span></span> <span data-ttu-id="99510-185">通过其他任何流程（即使用其他移动设备菜单项）接收的产品应在默认的仓库接收位置 ( *RECV* ) 登记，并应该照常创建工作。</span><span class="sxs-lookup"><span data-stu-id="99510-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location ( *RECV* ), and work should be created as usual.</span></span> <span data-ttu-id="99510-186">（此方案不显示默认接收设置。）</span><span class="sxs-lookup"><span data-stu-id="99510-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="99510-187">此方案需要以下元素：</span><span class="sxs-lookup"><span data-stu-id="99510-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="99510-188">对于所有产品，位置 *FL-001* 中 *采购订单物料接收（和储存）* 流程的工作策略</span><span class="sxs-lookup"><span data-stu-id="99510-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001* , for all products</span></span>
- <span data-ttu-id="99510-189">一个移动设备菜单项，具有默认数据，并将 **目标位置** 字段设置为 *FL-001*</span><span class="sxs-lookup"><span data-stu-id="99510-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="99510-190">先决条件</span><span class="sxs-lookup"><span data-stu-id="99510-190">Prerequisites</span></span>

<span data-ttu-id="99510-191">要使此方案中描述的功能在您的系统中可用，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *牌照接收增强* 和 *入站工作的工作策略增强* 功能。</span><span class="sxs-lookup"><span data-stu-id="99510-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="99510-192">此方案使用标准演示数据。</span><span class="sxs-lookup"><span data-stu-id="99510-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="99510-193">因此，如果要使用此处提供的值来进行演练，您必须在安装了演示数据的系统上工作。</span><span class="sxs-lookup"><span data-stu-id="99510-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="99510-194">此外，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="99510-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="99510-195">设置工作策略</span><span class="sxs-lookup"><span data-stu-id="99510-195">Set up a work policy</span></span>

1. <span data-ttu-id="99510-196">转到 **仓库管理 \> 设置 \> 工作 \> 工作策略** 。</span><span class="sxs-lookup"><span data-stu-id="99510-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="99510-197">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="99510-197">Select **New**.</span></span>
1. <span data-ttu-id="99510-198">在 **工作策略名称** 字段中，输入 *无采购物料储存工作* 。</span><span class="sxs-lookup"><span data-stu-id="99510-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="99510-199">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-199">Select **Save**.</span></span>
1. <span data-ttu-id="99510-200">在 **工作订单类型** 快速选项卡上，选择 **添加** 将一行添加到网格，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-201">**工作订单类型** ： *采购订单*</span><span class="sxs-lookup"><span data-stu-id="99510-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="99510-202">**工作流程** ： *采购订单物料接收（和储存）*</span><span class="sxs-lookup"><span data-stu-id="99510-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="99510-203">**工作创建方法** ： *从不*</span><span class="sxs-lookup"><span data-stu-id="99510-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="99510-204">**越库配送策略名称：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="99510-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="99510-205">在 **库存位置** 快速选项卡上，选择 **添加** 将一行添加到网格，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-206">**仓库** ： *24*</span><span class="sxs-lookup"><span data-stu-id="99510-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="99510-207">**位置** ： *FL-001*</span><span class="sxs-lookup"><span data-stu-id="99510-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="99510-208">在 **产品** 快速选项卡上，将 **产品选择** 字段设置为 *所有* 。</span><span class="sxs-lookup"><span data-stu-id="99510-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="99510-209">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="99510-210">设置移动设备菜单项以更改接收位置</span><span class="sxs-lookup"><span data-stu-id="99510-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="99510-211">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="99510-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="99510-212">在左窗格中，选择现有的 **采购接收** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="99510-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="99510-213">在 **常规** 快速选项卡上，将 **使用默认数据** 选项设置为 *是* 。</span><span class="sxs-lookup"><span data-stu-id="99510-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="99510-214">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-214">Select **Save**.</span></span>
1. <span data-ttu-id="99510-215">在操作窗格中，选择 **默认数据** 。</span><span class="sxs-lookup"><span data-stu-id="99510-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="99510-216">在 **默认数据** 页面上的操作窗格上，选择 **新建** 将一行添加到网格，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-217">**默认数据字段** ： *目标位置*</span><span class="sxs-lookup"><span data-stu-id="99510-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="99510-218">**仓库** ： *24*</span><span class="sxs-lookup"><span data-stu-id="99510-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="99510-219">**位置：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="99510-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="99510-220">**硬编码值** ： *FL-001*</span><span class="sxs-lookup"><span data-stu-id="99510-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="99510-221">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="99510-222">接收采购订单而不创建工作</span><span class="sxs-lookup"><span data-stu-id="99510-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="99510-223">本节中的示例演示如何在与为仓库设置的默认接收位置不同的位置接收采购订单物料，但不创建工作。</span><span class="sxs-lookup"><span data-stu-id="99510-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="99510-224">此示例使用您先前在此方案中创建的工作策略和移动设备项。</span><span class="sxs-lookup"><span data-stu-id="99510-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="99510-225">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="99510-225">Create a purchase order</span></span>

1. <span data-ttu-id="99510-226">转到 **采购 \> 采购订单 \> 所有采购订单** 。</span><span class="sxs-lookup"><span data-stu-id="99510-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="99510-227">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="99510-227">Select **New**.</span></span>
1. <span data-ttu-id="99510-228">在 **创建采购订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="99510-229">**供应商帐户** ： *US-101*</span><span class="sxs-lookup"><span data-stu-id="99510-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="99510-230">**站点** ： *2*</span><span class="sxs-lookup"><span data-stu-id="99510-230">**Site:** *2*</span></span>
    - <span data-ttu-id="99510-231">**仓库** ： *24*</span><span class="sxs-lookup"><span data-stu-id="99510-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="99510-232">选择 **确定** 关闭对话框并打开新的采购订单。</span><span class="sxs-lookup"><span data-stu-id="99510-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="99510-233">在 **采购订单行** 快速选项卡上，为空行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="99510-234">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="99510-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="99510-235">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="99510-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="99510-236">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-236">Select **Save**.</span></span>
1. <span data-ttu-id="99510-237">记下采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="99510-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="99510-238">接收采购订单</span><span class="sxs-lookup"><span data-stu-id="99510-238">Receive a purchase order</span></span>

1. <span data-ttu-id="99510-239">在移动设备上，使用 *24* 作为用户 ID、 *1* 作为密码登录到仓库 *24* 。</span><span class="sxs-lookup"><span data-stu-id="99510-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="99510-240">选择 **入站** 。</span><span class="sxs-lookup"><span data-stu-id="99510-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="99510-241">选择 **采购接收** 。</span><span class="sxs-lookup"><span data-stu-id="99510-241">Select **Purchase receive**.</span></span> <span data-ttu-id="99510-242">**位置** 字段应设置为 *FL-001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="99510-243">输入您在上一过程中创建的采购订单的采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="99510-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="99510-244">在 **物料编号** 字段中输入 *A0001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="99510-245">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="99510-245">Select **OK**.</span></span>
1. <span data-ttu-id="99510-246">在 **数量** 字段中，输入 *1* 。</span><span class="sxs-lookup"><span data-stu-id="99510-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="99510-247">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="99510-247">Select **OK**.</span></span>

<span data-ttu-id="99510-248">现在已接收了采购订单，但没有工作与之关联。</span><span class="sxs-lookup"><span data-stu-id="99510-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="99510-249">现有库存量已更新，位置 *FL-001* 现在提供数量 *1* 的物料 *A0001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="99510-250">示例方案：制造</span><span class="sxs-lookup"><span data-stu-id="99510-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="99510-251">在以下示例中，有两个生产订单， *PRD-001* 和 *PRD-002* 。</span><span class="sxs-lookup"><span data-stu-id="99510-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="99510-252">生产订单 *PRD-001* 具有名为 *装配* 的工序，其中的产品 *SC1* 正报告为完工入库到位置 *001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-252">Production order *PRD-001* has an operation that is named *Assembly* , where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="99510-253">生产订单 *PRD-002* 具有名为 *喷涂* 的工序，使用来自位置 *001* 的产品 *SC1* 。</span><span class="sxs-lookup"><span data-stu-id="99510-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="99510-254">生产订单 *PRD-002* 还使用来自位置 *001* 的原材料 *RM1* 。</span><span class="sxs-lookup"><span data-stu-id="99510-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="99510-255">原材料 *RM1* 存储在仓库位置 *BULK-001* ，将通过原材料领料的仓库工作领取到位置 *001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="99510-256">生产 *PRD-002* 发放时生成领料工作。</span><span class="sxs-lookup"><span data-stu-id="99510-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="99510-257">[![仓库工作策略](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="99510-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="99510-258">当您计划为此方案配置仓库工作策略时，您应该考虑以下几点：</span><span class="sxs-lookup"><span data-stu-id="99510-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="99510-259">当您报告产品 *SC1* 从生产订单 *PRD-001* 完工到位置 *001* 时，不要求创建成品储存的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="99510-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="99510-260">原因是生产订单 *PRD-002* 的 *喷涂* 工序使用同一位置的产品 *SC1* 。</span><span class="sxs-lookup"><span data-stu-id="99510-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="99510-261">需要原材料领料的仓库工作来将原材料 *RM1* 从仓库位置 *BULK-001* 移到位置 *001* 。</span><span class="sxs-lookup"><span data-stu-id="99510-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="99510-262">这是您基于这些注意事项可以设置的工作策略示例：</span><span class="sxs-lookup"><span data-stu-id="99510-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="99510-263">**工作策略名称** ： *无储存工作*</span><span class="sxs-lookup"><span data-stu-id="99510-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="99510-264">**工作订单类型** ： *成品储存* 和 *联产品和副产品储存*</span><span class="sxs-lookup"><span data-stu-id="99510-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="99510-265">**库存位置：** 仓库 *51* 和位置 *001*</span><span class="sxs-lookup"><span data-stu-id="99510-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="99510-266">**产品** ： *SC1*</span><span class="sxs-lookup"><span data-stu-id="99510-266">**Products:** *SC1*</span></span>

<span data-ttu-id="99510-267">以下示例方案提供了针对此方案设置仓库工作策略的分步说明。</span><span class="sxs-lookup"><span data-stu-id="99510-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="99510-268">示例方案：报告完工入库到非牌照控制的位置</span><span class="sxs-lookup"><span data-stu-id="99510-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="99510-269">此方案演示了一个生产订单被报告为完工入库到非牌照控制的位置的示例。</span><span class="sxs-lookup"><span data-stu-id="99510-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="99510-270">此方案使用标准演示数据。</span><span class="sxs-lookup"><span data-stu-id="99510-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="99510-271">因此，如果要使用此处提供的值来进行演练，您必须在安装了演示数据的系统上工作。</span><span class="sxs-lookup"><span data-stu-id="99510-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="99510-272">此外，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="99510-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="99510-273">设置仓库工作策略</span><span class="sxs-lookup"><span data-stu-id="99510-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="99510-274">仓库流程不是始终包括仓库工作。</span><span class="sxs-lookup"><span data-stu-id="99510-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="99510-275">通过定义工作策略，您可以防止为原材料领料创建工作，并将一组产品的成品储存在特定位置。</span><span class="sxs-lookup"><span data-stu-id="99510-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="99510-276">转到 **仓库管理 \> 设置 \> 工作 \> 工作策略** 。</span><span class="sxs-lookup"><span data-stu-id="99510-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="99510-277">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="99510-277">Select **New**.</span></span>
1. <span data-ttu-id="99510-278">在 **工作策略名称** 字段中，输入 *无储存工作* 。</span><span class="sxs-lookup"><span data-stu-id="99510-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="99510-279">在操作窗格上，选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="99510-280">在 **工作订单类型** 快速选项卡上，选择 **添加** 将一行添加到网格，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-281">**工作订单类型** ： *成品入库*</span><span class="sxs-lookup"><span data-stu-id="99510-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="99510-282">**工作流程** ： *所有相关工作流程*</span><span class="sxs-lookup"><span data-stu-id="99510-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="99510-283">**工作创建方法** ： *从不*</span><span class="sxs-lookup"><span data-stu-id="99510-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="99510-284">**越库配送策略名称：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="99510-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="99510-285">再次选择 **添加** 向网格添加第二行，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-286">**工作订单类型** ： *联产品和副产品储存*</span><span class="sxs-lookup"><span data-stu-id="99510-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="99510-287">**工作流程** ： *所有相关工作流程*</span><span class="sxs-lookup"><span data-stu-id="99510-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="99510-288">**工作创建方法** ： *从不*</span><span class="sxs-lookup"><span data-stu-id="99510-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="99510-289">**越库配送策略名称：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="99510-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="99510-290">在 **库存位置** 快速选项卡上，选择 **添加** 将一行添加到网格，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="99510-291">**仓库：** *51*</span><span class="sxs-lookup"><span data-stu-id="99510-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="99510-292">**位置** ： *001*</span><span class="sxs-lookup"><span data-stu-id="99510-292">**Location:** *001*</span></span>

1. <span data-ttu-id="99510-293">在 **产品** 快速选项卡上，将 **产品选择** 字段设置为 *选定* 。</span><span class="sxs-lookup"><span data-stu-id="99510-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="99510-294">在 **产品** 快速选项卡上，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="99510-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="99510-295">在新行中，将 **物料编号** 字段设置为 *L0101* 。</span><span class="sxs-lookup"><span data-stu-id="99510-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="99510-296">在操作窗格上，选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="99510-297">设置输出库位</span><span class="sxs-lookup"><span data-stu-id="99510-297">Set up an output location</span></span>

1. <span data-ttu-id="99510-298">转到 **组织管理 \> 资源 \> 资源组** 。</span><span class="sxs-lookup"><span data-stu-id="99510-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="99510-299">在左窗格中，选择资源组 **5102** 。</span><span class="sxs-lookup"><span data-stu-id="99510-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="99510-300">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="99510-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="99510-301">**输出仓库** ： *51*</span><span class="sxs-lookup"><span data-stu-id="99510-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="99510-302">**输出位置** ： *001*</span><span class="sxs-lookup"><span data-stu-id="99510-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="99510-303">在操作窗格上，选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="99510-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="99510-304">位置 *001* 不是牌照控制的位置。</span><span class="sxs-lookup"><span data-stu-id="99510-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="99510-305">只有当位置存在适用的工作策略时，您才可以设置非牌照控制的输出位置。</span><span class="sxs-lookup"><span data-stu-id="99510-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="99510-306">创建生产订单并报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="99510-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="99510-307">转到 **生产控制 \> 生产订单 \> 所有生产订单** 。</span><span class="sxs-lookup"><span data-stu-id="99510-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="99510-308">在操作窗格中，选择 **新建生产订单** 。</span><span class="sxs-lookup"><span data-stu-id="99510-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="99510-309">在 **创建生产订单** 对话框中，将 **物料编号** 字段设置为 *L0101* 。</span><span class="sxs-lookup"><span data-stu-id="99510-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="99510-310">选择 **创建** 创建订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="99510-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="99510-311">新生产订单将添加到 **所有生产订单** 页面上的网格中。</span><span class="sxs-lookup"><span data-stu-id="99510-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="99510-312">保持选择新生产订单。</span><span class="sxs-lookup"><span data-stu-id="99510-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="99510-313">在操作窗格上，在 **生产订单** 选项卡的 **流程** 组中，选择 **估计** 。</span><span class="sxs-lookup"><span data-stu-id="99510-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="99510-314">在 **估计** 对话框中，读取估计值，然后选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="99510-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="99510-315">在操作窗格上，在 **生产订单** 选项卡的 **流程** 组中，选择 **开始** 。</span><span class="sxs-lookup"><span data-stu-id="99510-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="99510-316">在 **开始** 对话框的 **常规** 选项卡上，将 **自动物料清单消耗量** 字段设置为 *从不* 。</span><span class="sxs-lookup"><span data-stu-id="99510-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="99510-317">选择 **确定** 保存设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="99510-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="99510-318">在操作窗格上，在 **生产订单** 选项卡上，在 **流程** 组中，选择 **完工入库** 。</span><span class="sxs-lookup"><span data-stu-id="99510-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="99510-319">在 **完工入库** 对话框中的 **常规** 选项卡上，将 **接受错误** 选项设置为 *是* 。</span><span class="sxs-lookup"><span data-stu-id="99510-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="99510-320">选择 **确定** 保存设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="99510-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="99510-321">在“操作”窗格的 **仓库** 选项卡上，在 **常规** 组中，选择 **工作详细信息** 。</span><span class="sxs-lookup"><span data-stu-id="99510-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="99510-322">在生产订单报告为完工入库时，未为储存生成工作。</span><span class="sxs-lookup"><span data-stu-id="99510-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="99510-323">发生此行为是因为将工作策略定义为在产品 *L0101* 报告为已完工入库到位置 *001* 时阻止生成工作。</span><span class="sxs-lookup"><span data-stu-id="99510-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="99510-324">更多信息</span><span class="sxs-lookup"><span data-stu-id="99510-324">More information</span></span>

<span data-ttu-id="99510-325">有关移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="99510-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="99510-326">有关牌照接收和工作策略的详细信息，请参阅[通过仓库应用进行的牌照接收](warehousing-mobile-device-app-license-plate-receiving.md)。</span><span class="sxs-lookup"><span data-stu-id="99510-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="99510-327">有关入站负荷管理的详细信息，请参阅[仓库对采购订单入站负荷的处理](inbound-load-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="99510-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
