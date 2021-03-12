---
title: 供应商返利
description: 本主题对您在使用供应商返利时可能要执行的最常见任务进行了概述。 供应商返利有助于公司自动执行管理、跟踪和索赔其所获返利所需的任务，从而更好地管理其供应商返利计划。
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: 46d6beb287f7d034c6fde09999f7854695a4987c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966647"
---
# <a name="vendor-rebates"></a><span data-ttu-id="3e70b-104">供应商返利</span><span class="sxs-lookup"><span data-stu-id="3e70b-104">Vendor rebates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e70b-105">供应商返利有助于公司自动执行管理、跟踪和索赔其所获返利所需的任务，从而更好地管理其供应商返利计划。</span><span class="sxs-lookup"><span data-stu-id="3e70b-105">Vendor rebates help companies better manage their supplier rebate programs by automating tasks that are required in order to administer, track, and claim rebates that are earned.</span></span>

<span data-ttu-id="3e70b-106">本主题对您在使用供应商返利时可能要执行的最常见任务进行了概述。</span><span class="sxs-lookup"><span data-stu-id="3e70b-106">This topic provides an overview of the most common tasks that you might want to perform when you work with vendor rebates.</span></span> <span data-ttu-id="3e70b-107">概述内容涵盖以下任务：</span><span class="sxs-lookup"><span data-stu-id="3e70b-107">The overview covers the following tasks:</span></span>

- <span data-ttu-id="3e70b-108">查看返利协议的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3e70b-108">Review details of a rebate agreement.</span></span>
- <span data-ttu-id="3e70b-109">标识获得返利资格的订单，并生成返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-109">Identify orders that qualify for rebates, and generate rebate claims.</span></span>
- <span data-ttu-id="3e70b-110">审查和批准索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-110">Review and approve claims.</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="3e70b-111">受众和目的</span><span class="sxs-lookup"><span data-stu-id="3e70b-111">Audience and purpose</span></span>

<span data-ttu-id="3e70b-112">此主题中的信息面向在企业公司承担采购经理、首席财务官 (CFO) 和会计经理等职务，并承担以下职责的业务决策者：</span><span class="sxs-lookup"><span data-stu-id="3e70b-112">The information in this topic is intended for business decision makers in enterprise companies, in positions such as purchase manager, chief financial officer (CFO), and accounting manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="3e70b-113">协商供应商价格、折扣和返利协议。</span><span class="sxs-lookup"><span data-stu-id="3e70b-113">Negotiate vendor price, discount, and rebate agreements.</span></span>
- <span data-ttu-id="3e70b-114">管理负责处理返利索赔和收款的职员。</span><span class="sxs-lookup"><span data-stu-id="3e70b-114">Manage staff that processes rebate claims and collects payments.</span></span>
- <span data-ttu-id="3e70b-115">以尽可能最优的价格订购库存。</span><span class="sxs-lookup"><span data-stu-id="3e70b-115">Order inventory at the best possible prices.</span></span>

<span data-ttu-id="3e70b-116">担任这些职务的人正在寻找实现各种目标的途径。</span><span class="sxs-lookup"><span data-stu-id="3e70b-116">People in these positions are looking for ways to achieve various goals.</span></span> <span data-ttu-id="3e70b-117">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="3e70b-117">Here are some examples:</span></span>

- <span data-ttu-id="3e70b-118">灵活地满足不同类型的供应商促销计划和返利条件。</span><span class="sxs-lookup"><span data-stu-id="3e70b-118">Flexibly accommodate different types of vendor promotion programs and rebate conditions.</span></span>
- <span data-ttu-id="3e70b-119">减少与监控促销计划和处理索赔有关的行政管理负担和错误。</span><span class="sxs-lookup"><span data-stu-id="3e70b-119">Reduce the administrative burden and errors that are associated with monitoring promotion performance and processing claims.</span></span>
- <span data-ttu-id="3e70b-120">通过应计未来应收账款提高现金流。</span><span class="sxs-lookup"><span data-stu-id="3e70b-120">Improve cash flow forecasts by accruing for future receivables.</span></span>
- <span data-ttu-id="3e70b-121">具有针对与供应商就返利进行的当前及未来的协商的量化依据。</span><span class="sxs-lookup"><span data-stu-id="3e70b-121">Have a quantified basis for ongoing and future negotiations with vendors about rebates.</span></span>

## <a name="review-details-of-a-vendor-rebate-agreement"></a><span data-ttu-id="3e70b-122">审核供应商返利协议的详细信息</span><span class="sxs-lookup"><span data-stu-id="3e70b-122">Review details of a vendor rebate agreement</span></span>

<span data-ttu-id="3e70b-123">供应商返利协议是与供应商之间的一份合同记录，该合同指定在公司实现预设的采购目标后向该公司授予货币奖励资格所依据的经协商的条款和条件。</span><span class="sxs-lookup"><span data-stu-id="3e70b-123">A vendor rebate agreement is a record of a contract with a vendor that specifies the negotiated terms and conditions under which the company qualifies for a monetary reward in return for achieving preset purchase targets.</span></span> <span data-ttu-id="3e70b-124">供应商返利协议在 **返利协议** 页上进行记录。</span><span class="sxs-lookup"><span data-stu-id="3e70b-124">Vendor rebate agreements are recorded on the **Rebate agreements** page.</span></span>

<span data-ttu-id="3e70b-125">若要打开 **供应商返利协议** 页，请选择 **采购** &gt; **供应商返利** &gt; **返利协议**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-125">To open the **Vendor rebate agreements** page, select **Procurement and sourcing** &gt; **Vendor rebates** &gt; **Rebate agreements**.</span></span>

![采购协议](media/purchase-agreement.PNG)

<span data-ttu-id="3e70b-127">在 **供应商返利协议** 页，可以查看与供应商协议的经协商条件有关的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3e70b-127">On the **Vendor rebate agreements** page, you can view details about the negotiated conditions of a vendor agreement.</span></span>

<span data-ttu-id="3e70b-128">协议标头指定授予公司返利资格的一般要求。</span><span class="sxs-lookup"><span data-stu-id="3e70b-128">The agreement's header specifies the general conditions that qualify a company for rebates.</span></span> <span data-ttu-id="3e70b-129">事实上，标头信息指定当购买特定数量的特定产品时，供应商授予返利。</span><span class="sxs-lookup"><span data-stu-id="3e70b-129">In effect, the header information specifies that a vendor grants a rebate when a specific product is bought in a specific quantity.</span></span> <span data-ttu-id="3e70b-130">在标头上，还可以指定返利度量单位选项和计算日期类型。</span><span class="sxs-lookup"><span data-stu-id="3e70b-130">On the header, you also specify the unit of measure rebate option and the calculation date type.</span></span>

- <span data-ttu-id="3e70b-131">在 **概览** 选项卡上，如果您将 **物料代码** 设置为 *表* 的行用于指定物料，协议将适用于该物料。</span><span class="sxs-lookup"><span data-stu-id="3e70b-131">On the **Overview** tab, if you have lines with **Item code** set to *table* to specify the item, then the agreement is for that specific item.</span></span> <span data-ttu-id="3e70b-132">如果您将 **物料代码** 设置为 *组* 或 *所有* 的行用于指定物料，将针对具有该物料代码的每个物料单独处理供应商返点协议，而不是针对具有该物料代码的所有物料进行处理。</span><span class="sxs-lookup"><span data-stu-id="3e70b-132">If you have lines with **Item code** set to *Group* or *All* to specify the items, then the vendor rebate agreement will be individually processed per item qualifying for the item code, not across all items qualifying for the item code.</span></span>

- <span data-ttu-id="3e70b-133">在 **常规** 选项卡的 **返利度量单位选项** 字段中，可以定义度量单位是否应为采购订单行获得返利索赔资格的条件。</span><span class="sxs-lookup"><span data-stu-id="3e70b-133">On the **General** tab, in the **Unit of measure rebate option** field, you can define whether a unit of measure should be a condition for the purchase order line to qualify for a rebate claim.</span></span>

    - <span data-ttu-id="3e70b-134">**转换** - 采购订单行按返利协议获得供应商返利资格。</span><span class="sxs-lookup"><span data-stu-id="3e70b-134">**Convert** – A purchase order line qualifies for a vendor rebate per the rebate agreement.</span></span> <span data-ttu-id="3e70b-135">您将收到返利，与在该行上应用的度量单位无关。</span><span class="sxs-lookup"><span data-stu-id="3e70b-135">You will receive a rebate regardless of the unit of measure that is applied on the line.</span></span>
    - <span data-ttu-id="3e70b-136">**精确匹配** - 要获得返利资格，采购行的度量单位必须与协议上指定的度量单位相同。</span><span class="sxs-lookup"><span data-stu-id="3e70b-136">**Exact match** – To qualify for a rebate, a purchase line must have the same unit of measure that is specified on the agreement.</span></span>

- <span data-ttu-id="3e70b-137">在 **常规** 选项卡的 **计算日期类型** 字段中，选择日期以用于确定采购是否发生在返利协议的有效期间。</span><span class="sxs-lookup"><span data-stu-id="3e70b-137">On the **General** tab, in the **Calculation date type** field, select the date that is used to determine whether the purchase occurs in the validity period of the rebate agreement.</span></span>

    - <span data-ttu-id="3e70b-138">**创建** - 输入采购订单的创建日期。</span><span class="sxs-lookup"><span data-stu-id="3e70b-138">**Created** – Use the creation date of the purchase order.</span></span>
    - <span data-ttu-id="3e70b-139">**请求的交货** - 使用请求的交货日期。</span><span class="sxs-lookup"><span data-stu-id="3e70b-139">**Requested delivery** – Use the requested delivery date.</span></span>

<span data-ttu-id="3e70b-140">在协议行上，可以更加详细地指定供应商返利协议。</span><span class="sxs-lookup"><span data-stu-id="3e70b-140">On the agreement lines, you can specify the vendor rebate agreement in more detail.</span></span>

- <span data-ttu-id="3e70b-141">在 **采购累计方式** 字段中，可以设置返利索赔的计算。</span><span class="sxs-lookup"><span data-stu-id="3e70b-141">In the **Cumulate purchase by** field, you can set the calculation of the rebate claim.</span></span> <span data-ttu-id="3e70b-142">金额可设置为取决于时间段（周、月、年、生存期或自定义期间）。</span><span class="sxs-lookup"><span data-stu-id="3e70b-142">The amount can be set to depend on a period (of week, month, year, lifetime or a customized period).</span></span> <span data-ttu-id="3e70b-143">**发票** 值指示在每次对采购订单行开发票时确定返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-143">The **Invoice** value indicates that a rebate claim will be determined every time that a purchase order line is invoiced.</span></span>
- <span data-ttu-id="3e70b-144">在 **取自** 字段中，可以指定计算返利的依据。</span><span class="sxs-lookup"><span data-stu-id="3e70b-144">In the **Taken from** field, you can specify the basis for the rebate calculation.</span></span>

    - <span data-ttu-id="3e70b-145">**总金额** - 基于物料的总价计算返利。</span><span class="sxs-lookup"><span data-stu-id="3e70b-145">**Gross** – The rebate is calculated based on the gross price of the item.</span></span>
    - <span data-ttu-id="3e70b-146">**净金额** - 基于物料的净价格（即应用其他折扣后的价格）计算返利。</span><span class="sxs-lookup"><span data-stu-id="3e70b-146">**Net** – The rebate is calculated based on the net price of the item (that is, the price after other discounts have been applied).</span></span>

- <span data-ttu-id="3e70b-147">**返利计划应计帐户** 和 **返利计划支出帐户** 字段指定将在审批与处理之间的中间阶段收到应计返利金额的帐号。</span><span class="sxs-lookup"><span data-stu-id="3e70b-147">The **Rebate program accrual account** and **Rebate program expense account** fields specify account numbers that will receive accrued rebate amounts during the intermediate stage between approval and processing.</span></span>
- <span data-ttu-id="3e70b-148">当 **需要审批** 选项设置为 **是** 时，返利索赔必须先经过批准后才能应计或支付。</span><span class="sxs-lookup"><span data-stu-id="3e70b-148">When the **Approval required** option is set to **Yes**, the rebate claim must be approved before it can be accrued or paid out.</span></span>
- <span data-ttu-id="3e70b-149">在 **返利换行符类型** 字段中，指定返利的依据。</span><span class="sxs-lookup"><span data-stu-id="3e70b-149">The **Rebate line break type** field specifies the basis for the rebates.</span></span>

    - <span data-ttu-id="3e70b-150">**数量** –返利以数量为基础。</span><span class="sxs-lookup"><span data-stu-id="3e70b-150">**Quantity** – The rebates are volume-based.</span></span>
    - <span data-ttu-id="3e70b-151">**金额** - 返利以金额为基础。</span><span class="sxs-lookup"><span data-stu-id="3e70b-151">**Amount** – The rebates are amount-based.</span></span>

- <span data-ttu-id="3e70b-152">在 **行** 快速选项卡上，可以看到如何设置不同的数量层以授予不同的返利。</span><span class="sxs-lookup"><span data-stu-id="3e70b-152">On the **Lines** FastTab, you can see how different quantity tiers can be set up to grant different rebates.</span></span> <span data-ttu-id="3e70b-153">例如，在上面的示意图中，**起始值** 和 **结束值** 字段指示介于 10 至 19 之间的产品数量将获得每个单位 15 美元的返利资格。</span><span class="sxs-lookup"><span data-stu-id="3e70b-153">For example, in the previous illustration, the **From value** and **To value** fields indicate that a product quantity between 10 and 19 units will qualify for a rebate of USD 15 per unit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e70b-154">**起始值** 值包含该起始值，而 **结束值** 不包含该结束值。</span><span class="sxs-lookup"><span data-stu-id="3e70b-154">The **From value** value is inclusive, whereas the **To value** value is exclusive.</span></span> <span data-ttu-id="3e70b-155">例如，**返利换行符类型** 字段设置为 **数量**，且您在 **起始值** 字段中输入 **1**，在 **结束值** 字段中输入 **3**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-155">For example, the **Rebate line break type** field is set to **Quantity**, and you enter **1** in the **From value** field and **3** in the **To value** field.</span></span> <span data-ttu-id="3e70b-156">在这种情况下，采购一个或两个物料时，适用返利金额，采购三个物料时不适用。</span><span class="sxs-lookup"><span data-stu-id="3e70b-156">In this case, the rebate amount applies when you purchase one or two items, but not when you purchase three items.</span></span>

- <span data-ttu-id="3e70b-157">在 **工作流审核状态** 字段中，**审核** 值指示协议可应用到满足该协议条款的采购订单。</span><span class="sxs-lookup"><span data-stu-id="3e70b-157">In the **Workflow approval status** field, the **Approved** value indicates that the agreement can be applied to purchase orders that meet the agreement’s conditions.</span></span>

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a><span data-ttu-id="3e70b-158">标识获得返利资格的订单，并生成返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-158">Identify orders that qualify for rebates, and generate rebate claims</span></span>

<span data-ttu-id="3e70b-159">向与公司签订了返利协议的供应商下达采购订单时，该程序标识未来的所有供应商贷记付款。</span><span class="sxs-lookup"><span data-stu-id="3e70b-159">When purchase orders are placed with a vendor that the company has a rebate agreement with, the program identifies any future vendor credit payments.</span></span> <span data-ttu-id="3e70b-160">如果采购订单获得返利资格，则一旦采购发票过帐，便为每个订单行生成一个返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-160">If the purchase orders qualify for a rebate, a rebate claim is generated for every order line as soon as a purchase invoice has been posted.</span></span> <span data-ttu-id="3e70b-161">此流程是自动执行的。</span><span class="sxs-lookup"><span data-stu-id="3e70b-161">This process is automatic.</span></span> <span data-ttu-id="3e70b-162">之后，您可以查看预期返利以及这些返利对产品成本和利润率的影响。</span><span class="sxs-lookup"><span data-stu-id="3e70b-162">Later, you can review the expected rebates and see the impact of those rebates on the product’s cost and profit margin.</span></span>

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a><span data-ttu-id="3e70b-163">查看应用于每个供应商返利协议的采购订单行的返利的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3e70b-163">View details of rebates that are applied to a purchase order line per the vendor rebate agreement</span></span>

1. <span data-ttu-id="3e70b-164">在 **采购订单** 页上，选择订单行，然后选择 **采购订单行** &gt; **查看** &gt; **价格详细信息**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-164">On the **Purchase order** page, select an order line, and then select **Purchase order line** &gt; **View** &gt; **Price details**.</span></span>
2. <span data-ttu-id="3e70b-165">在 **价格详细信息** 页上，选择 **返利** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="3e70b-165">On the **Price details** page, select the **Rebates** FastTab.</span></span>

<span data-ttu-id="3e70b-166">返利信息也在 **价格详细信息** 页的 **毛利估计** 部分的 **供应商返利** 字段中显示。</span><span class="sxs-lookup"><span data-stu-id="3e70b-166">The rebate information is also shown in the **Vendor rebate** field in the **Margin estimation** section of the **Price details** page.</span></span>

> [!NOTE]
> <span data-ttu-id="3e70b-167">在 **采购参数** 页的 **价格** 选项卡，验证 **启用价格详细信息** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-167">On the **Procurement and sourcing parameters** page, on the **Prices** tab, verify that the **Enable price details** option is set to **Yes**.</span></span> <span data-ttu-id="3e70b-168">如果此选项设置为 **否**，则您无法查看返利。</span><span class="sxs-lookup"><span data-stu-id="3e70b-168">If the option is set to **No**, you won’t be able to view the rebates.</span></span>

## <a name="review-and-approve-claims"></a><span data-ttu-id="3e70b-169">审查和批准索赔</span><span class="sxs-lookup"><span data-stu-id="3e70b-169">Review and approve claims</span></span>

<span data-ttu-id="3e70b-170">生成的返利索赔表示预期将来可从供应商获得的付款。</span><span class="sxs-lookup"><span data-stu-id="3e70b-170">Rebate claims that are generated represent the future payments that can be expected from the vendor.</span></span> <span data-ttu-id="3e70b-171">将贷方通知单签发给供应商之前，协议所有者通常要审查并批准索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-171">Before a credit note is issued to the vendor, the agreement owner typically wants to review the claims and approve them.</span></span> <span data-ttu-id="3e70b-172">但请注意，索赔的状态决定索赔是否已准备好进入审核流程。</span><span class="sxs-lookup"><span data-stu-id="3e70b-172">However, note that the status of a claim determines whether the claim is ready to go through the approval process.</span></span>

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a><span data-ttu-id="3e70b-173">索赔的状态及对审核流程的影响</span><span class="sxs-lookup"><span data-stu-id="3e70b-173">The status of claims and the effect on the approval process</span></span>

<span data-ttu-id="3e70b-174">生成索赔时，如果以累计为基础授予返利，则索赔状态设置为 **待计算**，如果按发票授予返利，则索赔状态设置为 **已计算**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-174">When a claim is generated, its status is set to **To be calculated** if the rebate is granted on a cumulative basis or **Calculated** if the rebate is granted per invoice.</span></span> <span data-ttu-id="3e70b-175">如果索赔的状态是 **待计算**，则索赔必须进入计算流程并由累计函数进行处理。</span><span class="sxs-lookup"><span data-stu-id="3e70b-175">If the status of a claim is **To be calculated**, the claim must go through a calculation process that is handled by the Cumulate function.</span></span> <span data-ttu-id="3e70b-176">只有状态为 **已计算** 的索赔才能包括在审核流程中。</span><span class="sxs-lookup"><span data-stu-id="3e70b-176">Only claims that have a status of **Calculated** can be included in the approval process.</span></span>

> [!NOTE]
> <span data-ttu-id="3e70b-177">如果供应商返利协议上的 **需要审核** 选项设置为 **否**，则生成的任何索赔的状态都将为 **已审核**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-177">If the **Approval required** option on a vendor rebate agreement is set to **No**, any claims that are generated will have a status of **Approved**.</span></span> <span data-ttu-id="3e70b-178">以累计基础授予的索赔必须进行审核。</span><span class="sxs-lookup"><span data-stu-id="3e70b-178">The approval is mandatory for claims that are granted on a cumulative basis.</span></span>

### <a name="approve-claims-and-view-postings-and-invoice-details"></a><span data-ttu-id="3e70b-179">审核索赔并查看过帐和发票详细信息</span><span class="sxs-lookup"><span data-stu-id="3e70b-179">Approve claims, and view postings and invoice details</span></span>

<span data-ttu-id="3e70b-180">审核索赔后，可以由应付账款 (A/P) 进行处理。</span><span class="sxs-lookup"><span data-stu-id="3e70b-180">When claims have been approved, they can be processed by Accounts payable (A/P).</span></span> <span data-ttu-id="3e70b-181">返利索赔金额的贷项通知单（供应商发票）是自动生成的。</span><span class="sxs-lookup"><span data-stu-id="3e70b-181">A credit memo (vendor invoice) for the rebate claim amount is automatically generated.</span></span> <span data-ttu-id="3e70b-182">随后可以将贷记添加到供应商余额中，且 A/P 团队可以将其包括在定期结算流程中。</span><span class="sxs-lookup"><span data-stu-id="3e70b-182">The credit can then be added to the vendor balance, and the A/P team can include it in the regular settlement process.</span></span>

1. <span data-ttu-id="3e70b-183">选择 **采购** &gt; **供应商返利** &gt; **返利索赔** 以打开返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-183">Select **Procurement and sourcing** &gt; **Vendor Rebates** &gt; **Rebate claims** to open a rebate claim.</span></span>
2. <span data-ttu-id="3e70b-184">关闭返利索赔。</span><span class="sxs-lookup"><span data-stu-id="3e70b-184">Close the rebate claim.</span></span>
3. <span data-ttu-id="3e70b-185">标记索赔，然后在操作窗格上选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-185">Mark the claim, and then, on the Action Pane, select **Approve**.</span></span>
4. <span data-ttu-id="3e70b-186">在请求页的 **供应商** 字段中，选择您有权收取其返利的供应商，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-186">On the request page, in the **Vendor** field, select the vendor that you’re authorized to receive a rebate from, and then select **OK**.</span></span>

    <span data-ttu-id="3e70b-187">为索赔金额过帐应计返利日记帐。</span><span class="sxs-lookup"><span data-stu-id="3e70b-187">A Rebate accrual journal is posted for the claim amount.</span></span> <span data-ttu-id="3e70b-188">此过帐将应计供应商返利应收账款借记为预期供应商贷记，将临时应计供应商返利应收账款贷记为预期收益。</span><span class="sxs-lookup"><span data-stu-id="3e70b-188">This posting debits the Accrued Vendor Rebates Receivable account for the expected vendor credit and credits the interim Accrued Vendor Rebates Received account for the expected gain.</span></span>

    ![消息](media/message.png)

5. <span data-ttu-id="3e70b-190">在返利列表中，选择行，然后在操作窗格中，选择 **返利交易记录** 以查看并导航到此返利应计过帐的日记帐批号。</span><span class="sxs-lookup"><span data-stu-id="3e70b-190">In the rebate list, select the line, and then, on the Action Pane, select **Rebate transactions** to see and navigate to the journal batch number for this rebate accrual posting.</span></span>

    <span data-ttu-id="3e70b-191">若要将索赔移动到定期 A/P 流程中，A/P 职员现在必须运行“处理”函数以完成返利索赔处理。</span><span class="sxs-lookup"><span data-stu-id="3e70b-191">To move the claims to the regular A/P process, the A/P clerk must now complete the rebate claim handling by running the Process function.</span></span>

6. <span data-ttu-id="3e70b-192">在操作窗格上，选择 **处理**，然后选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-192">On the Action Pane, select **Process**, and then select **Filter**.</span></span> <span data-ttu-id="3e70b-193">在 **供应商帐户** 字段的 **条件** 字段中，选择要处理其返利索赔的供应商，选择其他相关筛选器，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-193">In the **Criteria** field for the **Vendor account** field, select the vendor to process rebate claims for, select other relevant filters, and then select **OK**.</span></span>

    <span data-ttu-id="3e70b-194">消息栏以及状态已更改为 **已完成** 的事实表示发生了以下事件：</span><span class="sxs-lookup"><span data-stu-id="3e70b-194">The message bars and the fact that the status is changed to **Completed** indicate that the following events have occurred:</span></span>

    - <span data-ttu-id="3e70b-195">应计返利日记帐过帐已冲销应计应收账款和支出帐户上的临时金额。</span><span class="sxs-lookup"><span data-stu-id="3e70b-195">A Rebate accrual journal posting has reversed the previous interim amounts on the accrual receivable and expense accounts.</span></span>
    - <span data-ttu-id="3e70b-196">已创建返利金额的供应商发票（贷方通知单）。</span><span class="sxs-lookup"><span data-stu-id="3e70b-196">A vendor invoice (credit note) for the rebate amount has been created.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3e70b-197">**采购参数页** 上的 **返利计划** 选项卡上的 **手动发票过帐** 的设置决定是否对供应商发票手动过帐或作为索赔处理的一部分自动过帐。</span><span class="sxs-lookup"><span data-stu-id="3e70b-197">The setting of the **Manual invoice posting** option on the **Rebate program** tab of the **Procurement and sourcing parameters** page determines whether a vendor invoice is posted manually or automatically as part of claim processing.</span></span>

    - <span data-ttu-id="3e70b-198">自动或手动将供应商发票过帐时，供应商的应付账款已借记，已收折扣和折让金额已贷记。</span><span class="sxs-lookup"><span data-stu-id="3e70b-198">When the vendor invoice is posted, either automatically or manually, the vendor’s Payable account has been debited, and the Discounts and Allowances Received account has been credited.</span></span>

        > [!NOTE] 
        > <span data-ttu-id="3e70b-199">已收折扣和折让帐号针对在返利的采购发票行上使用的采购类别进行指定。</span><span class="sxs-lookup"><span data-stu-id="3e70b-199">The Discounts and Allowances Received account number is specified for the procurement category that is used on the purchase invoice line for the rebate.</span></span> <span data-ttu-id="3e70b-200">反过来，采购类别在 **采购参数** 页上的 **返利计划** 选项卡上进行设置。</span><span class="sxs-lookup"><span data-stu-id="3e70b-200">The procurement category, in turn, is set on the **Rebate program** tab of the **Procurement and sourcing parameters** page.</span></span>

7. <span data-ttu-id="3e70b-201">在返利列表中，选择行，然后在操作窗格中，选择 **返利交易记录** 以查看并导航到此返利应计过帐的日记帐批号和供应商发票编号。</span><span class="sxs-lookup"><span data-stu-id="3e70b-201">In the rebate list, select the line, and then, on the Action Pane, select **Rebate transactions** to see and navigate to the journal batch number for this rebate accrual posting and also the vendor invoice number.</span></span>
8. <span data-ttu-id="3e70b-202">选择供应商发票交易记录的行，然后在操作窗格中选择 **供应商发票**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-202">Select the line for the vendor invoice transaction, and then, on the Action Pane, select **Vendor invoice**.</span></span> <span data-ttu-id="3e70b-203">如果供应商发票已过帐，您将看到发票日记帐。</span><span class="sxs-lookup"><span data-stu-id="3e70b-203">If the vendor invoice has been posted, you will see the Invoice journal.</span></span> <span data-ttu-id="3e70b-204">否则，您将看到供应商发票为需要手动过帐的待定供应商发票。</span><span class="sxs-lookup"><span data-stu-id="3e70b-204">Otherwise, you will see the vendor invoice as a pending vendor invoice that requires manual posting.</span></span>

    <span data-ttu-id="3e70b-205">发票行指定 **佣金和返利** 采购类别的供应商发票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3e70b-205">The invoice line specifies the details of the vendor invoice for the **Commissions and Rebates** procurement category.</span></span>

9. <span data-ttu-id="3e70b-206">在 **所有供应商** 页，选择您已收到其返利的供应商，然后在操作窗格上选择 **交易记录**。</span><span class="sxs-lookup"><span data-stu-id="3e70b-206">On the **All vendors** page, select the vendor that you receive a rebate from, and then, on the Action Pane, select **Transactions**.</span></span> <span data-ttu-id="3e70b-207">找到发票的行。</span><span class="sxs-lookup"><span data-stu-id="3e70b-207">Find the line for the invoice.</span></span> <span data-ttu-id="3e70b-208">返利金额现在已添加到供应商余额。</span><span class="sxs-lookup"><span data-stu-id="3e70b-208">The rebate amount has now been added to the vendor balance.</span></span>

## <a name="summary"></a><span data-ttu-id="3e70b-209">摘要</span><span class="sxs-lookup"><span data-stu-id="3e70b-209">Summary</span></span>

<span data-ttu-id="3e70b-210">处理供应商返利的流程涉及到通常较为繁琐的多个手动跟踪任务。</span><span class="sxs-lookup"><span data-stu-id="3e70b-210">The process for handling vendor rebates involves multiple manual tracking tasks that are often tedious.</span></span> <span data-ttu-id="3e70b-211">通过自动执行这些任务，供应商返利管理功能可帮助您完成以下流程：</span><span class="sxs-lookup"><span data-stu-id="3e70b-211">By automating these tasks, the vendor rebate management feature can help you move through the following processes:</span></span>

- <span data-ttu-id="3e70b-212">生成准确的返利索赔</span><span class="sxs-lookup"><span data-stu-id="3e70b-212">Generating accurate rebate claims</span></span>
- <span data-ttu-id="3e70b-213">在总帐中应计预期应收账款和临时收益</span><span class="sxs-lookup"><span data-stu-id="3e70b-213">Accruing the expected receivable and interim gain in the general ledger</span></span>
- <span data-ttu-id="3e70b-214">使用到期的折让更新供应商余额和利润表</span><span class="sxs-lookup"><span data-stu-id="3e70b-214">Updating the vendor balance and the income statement with the allowance that is due</span></span>
