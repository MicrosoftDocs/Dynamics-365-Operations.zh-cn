---
title: 收入确认捆绑
description: 本主题介绍应收帐款的收入确认功能中包含的捆绑功能。 捆绑包含一个父级项目和多个组件项目。
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 857078e0b97bd136f5236c999a939d3fd263c39f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238368"
---
# <a name="revenue-recognition-bundles"></a><span data-ttu-id="e548d-104">收入确认捆绑</span><span class="sxs-lookup"><span data-stu-id="e548d-104">Revenue recognition bundles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e548d-105">本主题介绍应收帐款的收入确认功能中包含的捆绑功能。</span><span class="sxs-lookup"><span data-stu-id="e548d-105">This topic describes the bundle functionality that is included in the revenue recognition capability in Accounts receivable.</span></span> <span data-ttu-id="e548d-106">捆绑包含一个父级项目和多个组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-106">A bundle comprises a parent item and multiple component items.</span></span> <span data-ttu-id="e548d-107">父级项目在销售订单上输入，因此订单条目效率更高。</span><span class="sxs-lookup"><span data-stu-id="e548d-107">The parent item is entered on a sales order, so that order entry is more efficient.</span></span> <span data-ttu-id="e548d-108">但是，它随后将分解为组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-108">However, it's then exploded into the component items.</span></span> <span data-ttu-id="e548d-109">内部文档（例如装箱单）将列出组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-109">Internal documents, such as the packing slip, will list the component items.</span></span> <span data-ttu-id="e548d-110">但是，外部文档将仅显示父级项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-110">However, external documents will show only the parent item.</span></span>

> [!NOTE]
> <span data-ttu-id="e548d-111">Microsoft Dynamics 365 Commerce 渠道（例如在线、销售点 (POS) 和呼叫中心）不支持收入确认（包括捆绑功能）。</span><span class="sxs-lookup"><span data-stu-id="e548d-111">Microsoft Dynamics 365 Commerce  channels, such as online, point of sale (POS), and call centers, don't support revenue recognition (including the bundle functionality).</span></span> <span data-ttu-id="e548d-112">此外，还包括适用于 Dynamics 365 Supply Chain Management 和 Dynamics 365 Sales 的目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="e548d-112">This also includes the Prospect to cash solution for Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="e548d-113">配置为使用收入确认的项目不应添加到在 Commerce 渠道或目标客户到现金解决方案中创建的订单或交易记录中。</span><span class="sxs-lookup"><span data-stu-id="e548d-113">Items that are configured to use revenue recognition should not be added to orders or transactions that are created in Commerce channels or in the Prospect to cash solution.</span></span>

<span data-ttu-id="e548d-114">要设置捆绑，必须输入用于收入确认的 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="e548d-114">To set up bundles, you must enter the configuration keys for revenue recognition.</span></span> <span data-ttu-id="e548d-115">但是，即使未设置收入确认，您也可以使用捆绑。</span><span class="sxs-lookup"><span data-stu-id="e548d-115">However, you can use bundles even if revenue recognition isn't set up.</span></span> <span data-ttu-id="e548d-116">同样，即使未设置捆绑，您也可以使用收入确认。</span><span class="sxs-lookup"><span data-stu-id="e548d-116">Likewise, you can use revenue recognition if bundles aren't set up.</span></span> <span data-ttu-id="e548d-117">如果设置了收入确认，则组件项目将确定在对销售订单开票时用于收入确认或延期的收入价格和收入计划。</span><span class="sxs-lookup"><span data-stu-id="e548d-117">If revenue recognition is set up, the component items determine the revenue price and the revenue schedule that is used for revenue recognition or deferral when a sales order is invoiced.</span></span>

<span data-ttu-id="e548d-118">捆绑设置使用物料清单 (BOM) 功能。</span><span class="sxs-lookup"><span data-stu-id="e548d-118">The setup for bundles uses the bill of materials (BOM) functionality.</span></span> <span data-ttu-id="e548d-119">有关如何设置捆绑项目的信息，请参阅[收入确认设置](revenue-recognition-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="e548d-119">For information about how to set up a bundle item, see [Revenue recognition setup](revenue-recognition-setup.md).</span></span> <span data-ttu-id="e548d-120">如果将父级项目标记为捆绑，其将以与其他物料清单项目不同的方式进行处理。</span><span class="sxs-lookup"><span data-stu-id="e548d-120">If the parent item is flagged as a bundle, it's treated differently than other BOM items.</span></span> <span data-ttu-id="e548d-121">下面列出了具体的差异：</span><span class="sxs-lookup"><span data-stu-id="e548d-121">Here is a list of the differences:</span></span>

- <span data-ttu-id="e548d-122">必须通过销售订单确认来分解捆绑，方法是在销售订单页面上的操作窗格的 **销售** 选项卡上选择 **确认销售订单**。</span><span class="sxs-lookup"><span data-stu-id="e548d-122">Bundles must be exploded through sales order confirmation, by selecting **Confirm sales order** on the **Sell** tab of the Action Pane on the sales order page.</span></span> <span data-ttu-id="e548d-123">不得通过在 **销售订单行** 快速选项卡的 **销售订单行** 菜单上的 **分解** 下选择 **物料清单行**，来分解捆绑项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-123">Bundle items must never be exploded by selecting **BOM line** under **Explode** on the **Sales order line** menu on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="e548d-124">否则，该项目将视为物料清单而不是捆绑。</span><span class="sxs-lookup"><span data-stu-id="e548d-124">Otherwise, the item will be treated as a BOM, not as a bundle.</span></span>
- <span data-ttu-id="e548d-125">在创建装箱单或账单之前，必须确认包含捆绑项目的销售订单。</span><span class="sxs-lookup"><span data-stu-id="e548d-125">A sales order that contains a bundle item must be confirmed before the packing slip or invoice is created.</span></span>
- <span data-ttu-id="e548d-126">通过销售订单确认分解捆绑时，父级项目将被取消，并且其单价和折扣将分配到捆绑的组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-126">When a bundle is exploded through sales order confirmation, the parent item is canceled, and its unit price and discounts are allocated to the component items of the bundle.</span></span>
- <span data-ttu-id="e548d-127">组件项目的总和必须始终等于父级项目的价格。</span><span class="sxs-lookup"><span data-stu-id="e548d-127">The sum of the component items must always equal the price on the parent item.</span></span> <span data-ttu-id="e548d-128">因此，组件项目中可以更新或更改的字段存在限制。</span><span class="sxs-lookup"><span data-stu-id="e548d-128">Therefore, there are limitations on the fields that can be updated or changed for component items.</span></span> <span data-ttu-id="e548d-129">例如，不能手动更改单价。</span><span class="sxs-lookup"><span data-stu-id="e548d-129">For example, the unit price can't be manually changed.</span></span> <span data-ttu-id="e548d-130">此外，无法通过将新的价格协议设为生效来间接更改单价。</span><span class="sxs-lookup"><span data-stu-id="e548d-130">It also can't be indirectly changed by making a new price agreement go into effect.</span></span> <span data-ttu-id="e548d-131">要阻止新的价格协议，不能更改组件项目中的库存尺寸。</span><span class="sxs-lookup"><span data-stu-id="e548d-131">To prevent a new price agreement, inventory dimensions can't be changed on the component items.</span></span>
- <span data-ttu-id="e548d-132">当打印面向外部的文档（例如销售订单确认或账单）时，将打印父级项目，而不是组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-132">When an external-facing document such as the sales order confirmation or invoice is printed, the parent item is printed, not the component items.</span></span>

## <a name="bundles-on-sales-orders"></a><span data-ttu-id="e548d-133">销售订单上的捆绑</span><span class="sxs-lookup"><span data-stu-id="e548d-133">Bundles on sales orders</span></span>

<span data-ttu-id="e548d-134">USMF 演示公司包括以下捆绑设置。</span><span class="sxs-lookup"><span data-stu-id="e548d-134">The USMF demo company includes the following bundle setup.</span></span> <span data-ttu-id="e548d-135">请注意，用于收入确认的所有设置（例如收入计划设置）已从此方案中包括的项目中删除。</span><span class="sxs-lookup"><span data-stu-id="e548d-135">Note that all setup for revenue recognition, such as the setup of revenue schedules, has been removed from the items that are included in this scenario.</span></span>

<span data-ttu-id="e548d-136">**父级项目：** 笔记本电脑捆绑</span><span class="sxs-lookup"><span data-stu-id="e548d-136">**Parent item:** Laptop bundle</span></span>

- <span data-ttu-id="e548d-137">**组件项目：** 项目 1000 的数量为 1</span><span class="sxs-lookup"><span data-stu-id="e548d-137">**Component item:** A quantity of 1 of item 1000</span></span>
- <span data-ttu-id="e548d-138">**组件项目：** 项目 S0021 的数量为 1</span><span class="sxs-lookup"><span data-stu-id="e548d-138">**Component item:** A quantity of 1 of item S0021</span></span>
- <span data-ttu-id="e548d-139">**组件项目：** 项目支持的数量为 1</span><span class="sxs-lookup"><span data-stu-id="e548d-139">**Component item:** A quantity of 1 of item Support</span></span>

<span data-ttu-id="e548d-140">组件项目的 *基本销售价* 是组件设置的重要部分。</span><span class="sxs-lookup"><span data-stu-id="e548d-140">The *base sales price* of the component items is an essential part of the setup of the components.</span></span> <span data-ttu-id="e548d-141">基本销售价在项目的 **销售** 快速选项卡上定义。</span><span class="sxs-lookup"><span data-stu-id="e548d-141">The base sales price is defined on the **Sell** FastTab of an item.</span></span> <span data-ttu-id="e548d-142">当将父级项目的单价分配给组件项目时，将使用基本销售价计算分配系数。</span><span class="sxs-lookup"><span data-stu-id="e548d-142">It's used to calculate the allocation factor when the parent item's unit price is allocated to the component items.</span></span> <span data-ttu-id="e548d-143">不得将贸易协议销售价用于此目的。</span><span class="sxs-lookup"><span data-stu-id="e548d-143">The trade agreement sale prices are never used for this purpose.</span></span>

<span data-ttu-id="e548d-144">为组件项目定义了以下基本销售价：</span><span class="sxs-lookup"><span data-stu-id="e548d-144">The following base sales prices are defined for the component items:</span></span>

- <span data-ttu-id="e548d-145">**1000：**$1,900.00</span><span class="sxs-lookup"><span data-stu-id="e548d-145">**1000:** $1,900.00</span></span>
- <span data-ttu-id="e548d-146">**S0021：**$150.00</span><span class="sxs-lookup"><span data-stu-id="e548d-146">**S0021:** $150.00</span></span>
- <span data-ttu-id="e548d-147">**支持：**$500.00</span><span class="sxs-lookup"><span data-stu-id="e548d-147">**Support:** $500.00</span></span>

<span data-ttu-id="e548d-148">为客户 US-004 Cave Wholesales 输入了销售订单。</span><span class="sxs-lookup"><span data-stu-id="e548d-148">A sales order is entered for customer US-004, Cave Wholesales.</span></span> <span data-ttu-id="e548d-149">为笔记本电脑捆绑项目输入了唯一行。</span><span class="sxs-lookup"><span data-stu-id="e548d-149">The only line that is entered is for the Laptop bundle item.</span></span> <span data-ttu-id="e548d-150">可以从多个位置获取父行的默认单价，例如贸易协议或基本销售价。</span><span class="sxs-lookup"><span data-stu-id="e548d-150">The default unit price for the parent line can be taken from numerous places, such as the trade agreement or the base sales price.</span></span> <span data-ttu-id="e548d-151">在此示例中，将单价手动输入为 $2,300。</span><span class="sxs-lookup"><span data-stu-id="e548d-151">In this example, $2,300 was manually entered as the unit price.</span></span>

<span data-ttu-id="e548d-152">[![销售订单上的笔记本电脑捆绑项目](./media/bundle-01.png)](./media/bundle-01.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-152">[![Laptop bundle item on a sales order](./media/bundle-01.png)](./media/bundle-01.png)</span></span>

<span data-ttu-id="e548d-153">由于销售订单包含捆绑，因此必须进行确认。</span><span class="sxs-lookup"><span data-stu-id="e548d-153">Because the sales order contains a bundle, it must be confirmed.</span></span> <span data-ttu-id="e548d-154">确认对话框显示捆绑的组件。</span><span class="sxs-lookup"><span data-stu-id="e548d-154">The confirmation dialog box shows the components of the bundle.</span></span>

<span data-ttu-id="e548d-155">[![确认显示组件项目的销售订单对话框](./media/bundle-02.png)](./media/bundle-02.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-155">[![Confirm sales order dialog box that shows the component items](./media/bundle-02.png)](./media/bundle-02.png)</span></span>

<span data-ttu-id="e548d-156">但是，打印的确认报告将仅显示捆绑的父级项目，因为该报告是面向外部的客户文档。</span><span class="sxs-lookup"><span data-stu-id="e548d-156">However, the printed confirmation report will show only the parent item of the bundle, because that report is the external-facing document for the customer.</span></span>

<span data-ttu-id="e548d-157">[![仅显示父级项目的确认报告](./media/bundle-03.png)](./media/bundle-03.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-157">[![Confirmation report that shows only the parent item](./media/bundle-03.png)](./media/bundle-03.png)</span></span>

<span data-ttu-id="e548d-158">确认销售订单后，父级项目仍显示在销售订单上，但其状态已更改为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="e548d-158">After the sales order is confirmed, the parent item is still shown on the sales order, but its status has been changed to **Canceled**.</span></span> <span data-ttu-id="e548d-159">此外，还将在 **捆绑净额** 字段中跟踪净额。</span><span class="sxs-lookup"><span data-stu-id="e548d-159">Additionally, the net amount is tracked in the **Bundle net amount** field.</span></span> <span data-ttu-id="e548d-160">需要此金额以打印账单，因为账单显示父级项目而不是组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-160">This amount is required to print the invoice, because the invoice shows the parent item, not the component items.</span></span>

<span data-ttu-id="e548d-161">组件项目的总和必须等于父级项目的 **捆绑净额** 值，因为该值是在打印的账单上显示给客户的金额。</span><span class="sxs-lookup"><span data-stu-id="e548d-161">The sum of the component items must equal the **Bundle net amount** value of the parent item, because that value is the amount that is presented to the customer on the printed invoice.</span></span> <span data-ttu-id="e548d-162">要确保账单与过帐到总帐的金额匹配，对组件项目的编辑将受到限制。</span><span class="sxs-lookup"><span data-stu-id="e548d-162">To ensure that the invoice matches the amounts that are posted to the general ledger, edits to the component items are limited.</span></span> <span data-ttu-id="e548d-163">例如，无法更改站点和仓库，因为根据贸易协议，这些更改可能会触发价格变化。</span><span class="sxs-lookup"><span data-stu-id="e548d-163">For example, the site and Warehouse can't be changed, because those changes might trigger a price change, based on a trade agreement.</span></span>

<span data-ttu-id="e548d-164">父级项目的行中的单价将按以下方式分配到组件：</span><span class="sxs-lookup"><span data-stu-id="e548d-164">The unit price from the line for the parent item is allocated to the components in the following manner:</span></span>

<span data-ttu-id="e548d-165">**组件中的基本销售价总计：**$1,900 + $500 + $150 = $2,550</span><span class="sxs-lookup"><span data-stu-id="e548d-165">**Total base sales prices from components:** $1,900 + $500 + $150 = $2,550</span></span>

- <span data-ttu-id="e548d-166">**组件 1：**$2,300 × (1,900 ÷ 2,550) = $1,713.73</span><span class="sxs-lookup"><span data-stu-id="e548d-166">**Component 1:** $2,300 × (1,900 ÷ 2,550) = $1,713.73</span></span>
- <span data-ttu-id="e548d-167">**组件 2：**$2,300 × (500 ÷ 2,550) = $450.98</span><span class="sxs-lookup"><span data-stu-id="e548d-167">**Component 2:** $2,300 × (500 ÷ 2,550) = $450.98</span></span>
- <span data-ttu-id="e548d-168">**组件 3：**$2,300 × (150 ÷ 2,550) = $135.29</span><span class="sxs-lookup"><span data-stu-id="e548d-168">**Component 3:** $2,300 × (150 ÷ 2,550) = $135.29</span></span>

<span data-ttu-id="e548d-169">组件的总和必须等于 $2,300，计算方式为 ($1,713.73 + $450.98 + $135.29 = $2,300)。</span><span class="sxs-lookup"><span data-stu-id="e548d-169">The sum of the components must equal $2,300, and it does ($1,713.73 + $450.98 + $135.29 = $2,300).</span></span>

<span data-ttu-id="e548d-170">如果所有组件项目都需要更改，则可以删除父级项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-170">If changes are required for all component items, the parent item can be removed.</span></span> <span data-ttu-id="e548d-171">在这种情况下，还将删除组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-171">In this case, the component items are also removed.</span></span> <span data-ttu-id="e548d-172">然后，可以再次添加父级项目，并且可以在确认销售订单之前完成所需的编辑。</span><span class="sxs-lookup"><span data-stu-id="e548d-172">The parent item can then be added again, and the required edits can be completed before the sales order is confirmed.</span></span>

<span data-ttu-id="e548d-173">[![包括对组件项目的更改的捆绑项目](./media/bundle-04.png)](./media/bundle-04.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-173">[![Bundle item that includes changes to the component items](./media/bundle-04.png)](./media/bundle-04.png)</span></span>

<span data-ttu-id="e548d-174">选取和打包销售订单后，文档将仅包括捆绑的组件。</span><span class="sxs-lookup"><span data-stu-id="e548d-174">When the sales order is picked and packed, the documents will include only the components of the bundle.</span></span> <span data-ttu-id="e548d-175">装箱单和账单必须包括完整捆绑。</span><span class="sxs-lookup"><span data-stu-id="e548d-175">The packing slip and invoice must include a full bundle.</span></span> <span data-ttu-id="e548d-176">否则，将无法发布它们。</span><span class="sxs-lookup"><span data-stu-id="e548d-176">Otherwise, they can't be posted.</span></span> <span data-ttu-id="e548d-177">例如，对话框显示三个组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-177">For example, the dialog box shows three component items.</span></span> <span data-ttu-id="e548d-178">如果您尝试删除其中之一，将会显示一条错误消息，指出必须先对捆绑中的所有产品发货，然后才能开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-178">If you try to delete one of them, you receive an error message that states that all products in the bundle must be shipped before they can be invoiced.</span></span>

<span data-ttu-id="e548d-179">必须先将捆绑作为完整捆绑进行发货和开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-179">A bundle must be shipped and invoiced as a full bundle.</span></span> <span data-ttu-id="e548d-180">例如，如果将项目 1000 的数量更改为 4，但将其他组件项目的数量保留为 5，则无法过帐装箱单和账单。</span><span class="sxs-lookup"><span data-stu-id="e548d-180">For example, if you change the quantity of item 1000 to 4, but you leave the quantity of the other component items at 5, the packing slip and invoice can't be posted.</span></span>

<span data-ttu-id="e548d-181">仅当减少捆绑中所有组件的数量时，才可以对部分金额进行发货和开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-181">A partial amount can be shipped and invoiced only if the quantity is reduced for all components of the bundle.</span></span> <span data-ttu-id="e548d-182">例如，在销售订单上为笔记本电脑捆绑项目输入数量 5。</span><span class="sxs-lookup"><span data-stu-id="e548d-182">For example, a quantity of 5 of the Laptop bundle item is entered on a sales order.</span></span> <span data-ttu-id="e548d-183">确认销售订单后，销售订单上将显示三个组件项目，每个项目的数量为 5。</span><span class="sxs-lookup"><span data-stu-id="e548d-183">After the sales order is confirmed, the three component items are shown on the sales order, and the quantity of each is 5.</span></span> <span data-ttu-id="e548d-184">默认情况下，在发货和开票期间，每个组件的数量将设置为 5。</span><span class="sxs-lookup"><span data-stu-id="e548d-184">By default, during shipping and invoicing, the quantity will be set to 5 for each component.</span></span> <span data-ttu-id="e548d-185">但是，您可以将所有三个组件项目的数量降低至 3。</span><span class="sxs-lookup"><span data-stu-id="e548d-185">However, you can adjust the quantity down to 3 for all three component items.</span></span> <span data-ttu-id="e548d-186">在这种情况下，将对三个完整捆绑进行发货和开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-186">In this case, three full bundles will be shipped and invoiced.</span></span> <span data-ttu-id="e548d-187">剩余的两个捆绑项目（三个组件项目中每一个的数量都为 2）可以在以后进行发货和开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-187">The remaining two bundle items (a quantity of 2 of each of the three component items) can be shipped and invoiced later.</span></span>

<span data-ttu-id="e548d-188">最后一步是对销售订单开票。</span><span class="sxs-lookup"><span data-stu-id="e548d-188">The final step is to invoice the sales order.</span></span> <span data-ttu-id="e548d-189">在开票期间，“开票”对话框将显示组件项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-189">During invoicing, the invoice dialog box will show the component items.</span></span>

<span data-ttu-id="e548d-190">[![显示组件项目的“开票”对话框](./media/bundle-06.png)](./media/bundle-06.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-190">[![Invoice dialog box that shows the component items](./media/bundle-06.png)](./media/bundle-06.png)</span></span>

<span data-ttu-id="e548d-191">但是，打印的账单将仅显示父级项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-191">However, the printed invoice will show only the parent item.</span></span>
 
<span data-ttu-id="e548d-192">[![仅显示父级项目的打印账单](./media/bundle-07.png)](./media/bundle-07.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-192">[![Printed invoice that shows only the parent item](./media/bundle-07.png)](./media/bundle-07.png)</span></span>

<span data-ttu-id="e548d-193">过帐后创建的账单日记帐不包含捆绑中的父级项目，因为该项目的状态为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="e548d-193">The invoice journal that is created after posting occurs doesn't include the parent item from the bundle, because that item has a status of **Canceled**.</span></span>

<span data-ttu-id="e548d-194">[![不包含父级项目的账单日记帐](./media/bundle-08.png)](./media/bundle-08.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-194">[![Invoice journal that doesn't include the parent item](./media/bundle-08.png)](./media/bundle-08.png)</span></span>

<span data-ttu-id="e548d-195">务必注意，账单日记帐不包含捆绑中的父级项目，因为过帐账单后执行的任何流程都将基于该账单日记帐。</span><span class="sxs-lookup"><span data-stu-id="e548d-195">It's important that the invoice journal not include the parent item from the bundle, because any processes that are performed after the invoice is posted are based on that invoice journal.</span></span> <span data-ttu-id="e548d-196">例如，如果您从操作窗格上的 **销售** 选项卡中创建贷方通知单，所创建的贷方通知单将包含组件项目而不是父级项目。</span><span class="sxs-lookup"><span data-stu-id="e548d-196">For example, if you create a credit note from the **Sell** tab on the Action Pane, the credit note that is created will include the component items but not the parent item.</span></span>

<span data-ttu-id="e548d-197">[![显示组件项目而不是父级项目的贷方通知单](./media/bundle-09.png)](./media/bundle-09.png)</span><span class="sxs-lookup"><span data-stu-id="e548d-197">[![Credit note that shows the component items but not the parent item](./media/bundle-09.png)](./media/bundle-09.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]