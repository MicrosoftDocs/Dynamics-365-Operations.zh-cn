---
title: 贸易折让管理
description: 此主题介绍 Dynamics 365 Supply Chain Management 的贸易折让管理。
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7fdcf8a7294d8c7579f35bc108bdd3804da9a837
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203229"
---
# <a name="trade-allowance-management"></a><span data-ttu-id="945fc-103">贸易折让管理</span><span class="sxs-lookup"><span data-stu-id="945fc-103">Trade allowance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="945fc-104">贸易折让管理帮助公司管理促销计划，促销计划为达到数量和绩效目标的客户提供“绩效付薪体系”货币奖励。</span><span class="sxs-lookup"><span data-stu-id="945fc-104">Trade allowance management helps companies manage sales promotion programs that offer "pay-for-performance" monetary rewards to customers that achieve volume and behavioral goals.</span></span> <span data-ttu-id="945fc-105">该功能的功能是为符合以下条件的公司设计的：注重各种促销到利润过程，从促销资金预算编制和分配，到折让合同制订，到索赔的创建和处理，到付款处理，再到促销效果分析。</span><span class="sxs-lookup"><span data-stu-id="945fc-105">The feature’s capabilities are designed for companies that focus on comprehensive promote-to-profit processes, from promotion fund budgeting and allocation, to allowance contract setup, to claims creation and processing, to payment processing, to promotion effectiveness analysis.</span></span>


<span data-ttu-id="945fc-106">本文概述贸易折让管理功能，帮助您熟悉管理促销计划涉及的各种典型任务。</span><span class="sxs-lookup"><span data-stu-id="945fc-106">This article will provide a broad overview of the Trade allowance management feature and will familiarize you with the typical set of tasks that are involved in managing a sales promotion program.</span></span> <span data-ttu-id="945fc-107">应该由负责运营和决策的几类用户使用此功能实现各自的目标：</span><span class="sxs-lookup"><span data-stu-id="945fc-107">Several types of users who have operational and decision making responsibilities are expected to use this functionality to achieve their respective goals:</span></span>

- <span data-ttu-id="945fc-108">为所选科目分配可任意支配的资金，并根据倒付和一次性总付为促销设置贸易折让协议（适用于约定的服务）</span><span class="sxs-lookup"><span data-stu-id="945fc-108">Allocating discretionary funds to the selected accounts, and setting up trade allowance agreements for promotions, based on bill-backs and one-off lump sum payments (for an agreed service)</span></span>
- <span data-ttu-id="945fc-109">通过正在开展的销售运行协商促销合同和生成倒付索赔</span><span class="sxs-lookup"><span data-stu-id="945fc-109">Running the negotiated promotion contracts through ongoing sales and generating bill-back claims</span></span>
- <span data-ttu-id="945fc-110">计算，审核和处理生成的索赔，并将其作为付款的扣除传递给应收帐款 (A/R)</span><span class="sxs-lookup"><span data-stu-id="945fc-110">Calculating, approving, and processing the generated claims, and passing them on to Accounts receivable (A/R) as deductions for payment settlement</span></span>
- <span data-ttu-id="945fc-111">对帐扣除已到期的客户不足付款</span><span class="sxs-lookup"><span data-stu-id="945fc-111">Reconciling the customer’s short-pay with the deduction that is due</span></span>
- <span data-ttu-id="945fc-112">跟踪促销资金的使用，以及评估计划的收益率和效果</span><span class="sxs-lookup"><span data-stu-id="945fc-112">Tracking use of the promotional fund, and evaluating program profitability and effectiveness</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="945fc-113">受众和目的</span><span class="sxs-lookup"><span data-stu-id="945fc-113">Audience and purpose</span></span>

<span data-ttu-id="945fc-114">此文档中的信息面向在企业公司承担采购经理、首席财务官 (CFO) 和会计经理等职务，并承担以下职责的业务决策者：</span><span class="sxs-lookup"><span data-stu-id="945fc-114">The information in this document is intended for business decision makers in enterprise companies, in positions such as purchase manager, chief financial officer (CFO), and accounting manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="945fc-115">高级预算和资金分配</span><span class="sxs-lookup"><span data-stu-id="945fc-115">High-level budgets and fund allocation</span></span>
- <span data-ttu-id="945fc-116">规划和分析促销计划</span><span class="sxs-lookup"><span data-stu-id="945fc-116">Planning and analyzing sales promotions</span></span>
- <span data-ttu-id="945fc-117">管理处理倒付索赔，根据促销活动运行付款，以及结算不足付款和扣除的员工。</span><span class="sxs-lookup"><span data-stu-id="945fc-117">Managing staff that processes bill-back claims, runs payments based on merchandizing events, and settles short-pays and deductions</span></span>

<span data-ttu-id="945fc-118">担任这些角色的人正在寻找实现以下目标的途径：</span><span class="sxs-lookup"><span data-stu-id="945fc-118">People in these roles are looking for ways to achieve these goals:</span></span>

- <span data-ttu-id="945fc-119">改善营销促销资金的使用。</span><span class="sxs-lookup"><span data-stu-id="945fc-119">Better use marketing promotional funds.</span></span>
- <span data-ttu-id="945fc-120">灵活地满足不同类型的促销计划和折让。</span><span class="sxs-lookup"><span data-stu-id="945fc-120">Flexibly accommodate different types of promotion programs and allowances.</span></span>
- <span data-ttu-id="945fc-121">减少与监控促销计划和处理索赔有关的行政管理负担和错误。</span><span class="sxs-lookup"><span data-stu-id="945fc-121">Reduce the administrative burden and errors that are associated with monitoring promotion performance and processing claims.</span></span>
- <span data-ttu-id="945fc-122">通过应计未来负债改善现金流。</span><span class="sxs-lookup"><span data-stu-id="945fc-122">Improve cash flow forecasts by accruing for future liability.</span></span>
- <span data-ttu-id="945fc-123">具有针对与客户就促销进行的当前及未来的协商的量化依据。</span><span class="sxs-lookup"><span data-stu-id="945fc-123">Have a quantified basis for ongoing and future negotiations with customers about promotions.</span></span>

## <a name="promotional-fund-and-trade-allowance-agreement"></a><span data-ttu-id="945fc-124">促销资金和贸易折让协议</span><span class="sxs-lookup"><span data-stu-id="945fc-124">Promotional fund and Trade allowance agreement</span></span>

<span data-ttu-id="945fc-125">贸易折让协议是奖励计划，该计划为达到特定数量目标和/或绩效目标的客户提供绩效付薪体系货币奖励。</span><span class="sxs-lookup"><span data-stu-id="945fc-125">A trade allowance agreement is an incentive program where pay-for-performance monetary rewards are offered to customers that achieve specific volume targets and/or behavioral goals.</span></span> <span data-ttu-id="945fc-126">促销资金是预算性支出。</span><span class="sxs-lookup"><span data-stu-id="945fc-126">Promotional funds are budgeted expenditures.</span></span> <span data-ttu-id="945fc-127">因此，可以捕获促销市场活动。</span><span class="sxs-lookup"><span data-stu-id="945fc-127">In that way, the promotional campaigns can be captured.</span></span>

### <a name="promotional-fund"></a><span data-ttu-id="945fc-128">促销资金</span><span class="sxs-lookup"><span data-stu-id="945fc-128">Promotional fund</span></span>

<span data-ttu-id="945fc-129">**资金**页中记录了分配给贸易折让协议的资金。</span><span class="sxs-lookup"><span data-stu-id="945fc-129">Funds that are allocated to trade allowance agreements are recorded on the **Funds** page.</span></span> <span data-ttu-id="945fc-130">若要打开 **资金**页，请选择**销售和市场营销** \> **贸易折让** \> **资金** \> **资金**。</span><span class="sxs-lookup"><span data-stu-id="945fc-130">To open the **Funds** page, select **Sales and marketing** \> **Trade allowances** \> **Funds** \> **Funds**.</span></span>

<span data-ttu-id="945fc-131">![“资金”页面](./media/trade-allowance-management-funds-page.png "“资金”页面")</span><span class="sxs-lookup"><span data-stu-id="945fc-131">![Funds page](./media/trade-allowance-management-funds-page.png "Funds page")</span></span>

<span data-ttu-id="945fc-132">在**资金**页上，可查看促销资金的详细信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-132">On the **Funds** page, you can view the details of promotional funds.</span></span>

<span data-ttu-id="945fc-133">**常规**快速选项卡显示资金的有效期和预算金额。</span><span class="sxs-lookup"><span data-stu-id="945fc-133">The **General** FastTab shows the period that the fund is valid for and its budgeted amount.</span></span> <span data-ttu-id="945fc-134">若要为促销协议分配资金，**状态**字段的值必须为**已审核**。</span><span class="sxs-lookup"><span data-stu-id="945fc-134">In order for the fund to be allocated to the promotion agreement, the **Status** field must have a value of **Approved**.</span></span>

<span data-ttu-id="945fc-135">**客户**快速选项卡显示客户层次结构。</span><span class="sxs-lookup"><span data-stu-id="945fc-135">The **Customers** FastTab shows the customer hierarchy.</span></span> <span data-ttu-id="945fc-136">若要选择资金的目标客户，请将其拖到**资金客户**下。</span><span class="sxs-lookup"><span data-stu-id="945fc-136">To select the customers that the fund targets, drag them so that they are under **Fund customers**.</span></span> <span data-ttu-id="945fc-137">此快速选项卡还显示资金总金额的分配方式。</span><span class="sxs-lookup"><span data-stu-id="945fc-137">This FastTab also shows how the total amount of the fund is distributed.</span></span>

<span data-ttu-id="945fc-138">**物品**快速选项卡显示促销中包含的物品。</span><span class="sxs-lookup"><span data-stu-id="945fc-138">The **Items** FastTab shows the items that are included in the promotion.</span></span>

### <a name="trade-allowance-agreement"></a><span data-ttu-id="945fc-139">贸易折让协议</span><span class="sxs-lookup"><span data-stu-id="945fc-139">Trade allowance agreement</span></span>

<span data-ttu-id="945fc-140">准备好资金定义之后，促销规划的下一步是为每个促销活动登记促销合同（也称为贸易折让协议），分配资金和定义绩效目标。</span><span class="sxs-lookup"><span data-stu-id="945fc-140">After the fund definition is in place, the next step in promotion planning is to register promotion contracts (which are known as trade allowance agreements), allocate funds, and define performance goals for each merchandizing event.</span></span>

<span data-ttu-id="945fc-141">**贸易折让协议**页中记录了贸易折让协议。</span><span class="sxs-lookup"><span data-stu-id="945fc-141">Trade allowance agreements are recorded on the **Trade allowance agreements** page.</span></span> <span data-ttu-id="945fc-142">若要打开 **贸易折让协议**页，请选择 **销售和市场营销** \> **贸易折让** \> **贸易折让协议**。</span><span class="sxs-lookup"><span data-stu-id="945fc-142">To open the **Trade allowance agreements** page, select **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span>

<span data-ttu-id="945fc-143">![“贸易折让协议”页面](./media/trade-allowance-management-agreements-page.png "“贸易折让协议”页面")</span><span class="sxs-lookup"><span data-stu-id="945fc-143">![Trade allowance agreements page](./media/trade-allowance-management-agreements-page.png "Trade allowance agreements page")</span></span>

#### <a name="header"></a><span data-ttu-id="945fc-144">​页眉</span><span class="sxs-lookup"><span data-stu-id="945fc-144">Header</span></span>

<span data-ttu-id="945fc-145">选择**标题**切换到标题视图。</span><span class="sxs-lookup"><span data-stu-id="945fc-145">Select **Header** to switch to the Header view.</span></span>

<span data-ttu-id="945fc-146">在**常规**快速选项卡上，**订单结束日期**和**订单开始日期**字段定义协议的有效时间段。</span><span class="sxs-lookup"><span data-stu-id="945fc-146">On the **General** FastTab, the **Order to** and **Order from** fields define the period when the agreement is valid.</span></span> <span data-ttu-id="945fc-147">如果协议的审核状态为**已内部审核**，表示协议尚未生效，不能在销售订单处理期间应用。</span><span class="sxs-lookup"><span data-stu-id="945fc-147">An approval status of **Internal approved** for the agreement indicates that the agreement isn't yet valid and can't be applied during sales order processing.</span></span>

<span data-ttu-id="945fc-148">**常规**快速选项卡的**分析**部分中包含定义用于评估促销的数量和成本的重要字段：</span><span class="sxs-lookup"><span data-stu-id="945fc-148">The **Analysis** section of the **General** FastTab contains important fields that define the quantities and costs that are used for promotion evaluation:</span></span>

- <span data-ttu-id="945fc-149">**基础单位**字段指定应用促销之前必须销售给所选客户的产品数量。</span><span class="sxs-lookup"><span data-stu-id="945fc-149">The **Base units** field specifies the quantity of products that must be sold to the selected customers before the promotion is applied.</span></span>
- <span data-ttu-id="945fc-150">**计算的装运数量**值根据**提升百分比**值计算，后者是为该促销规划的目标增加。</span><span class="sxs-lookup"><span data-stu-id="945fc-150">The **Calculated ship quantity** value is calculated based on the **Lift percent** value, which is a planned target increase for this promotion.</span></span>
- <span data-ttu-id="945fc-151">**贸易折让成本**字段基于贸易折让协议中的各种活动的数量计算。</span><span class="sxs-lookup"><span data-stu-id="945fc-151">The **Trade allowance cost** field is calculated based on the quantities of the various events in the trade allowance agreement.</span></span>

<span data-ttu-id="945fc-152">在**客户**快速选项卡上左侧列表中，可选择并查看客户组，后者设置为预定义的层次结构。</span><span class="sxs-lookup"><span data-stu-id="945fc-152">On the **Customers** FastTab, in the list on the left, you can select and view customer groups, which are set up as predefined hierarchies.</span></span> <span data-ttu-id="945fc-153">然后可以选择整个层次结构或特定科目充当折让协议的目标。</span><span class="sxs-lookup"><span data-stu-id="945fc-153">You can then select the whole hierarchy or specific accounts as targets for the allowance agreement.</span></span>

<span data-ttu-id="945fc-154">在**物品**快速选项卡上，就像在**资金**页的**物品**快速选项卡上，将把产品添加到协议，以便将其销售与协商的折让关联。</span><span class="sxs-lookup"><span data-stu-id="945fc-154">On the **Items** FastTab, as on the **Items** FastTab of the **Funds** page, products are added to the agreement to associate its sales with the allowance that was agreed on.</span></span>

<span data-ttu-id="945fc-155">在**资金**快速选项卡上，可查看与该合同关联的促销资金。</span><span class="sxs-lookup"><span data-stu-id="945fc-155">On the **Funds** FastTab, you can view the promotion funds that are associated with this contract.</span></span> <span data-ttu-id="945fc-156">还可以查看合同的活动成本分摊。</span><span class="sxs-lookup"><span data-stu-id="945fc-156">You can also view the contract's event cost allocation.</span></span> <span data-ttu-id="945fc-157">如果活动成本分摊为 100%，表示此促销的资金属于同一个资金来源。</span><span class="sxs-lookup"><span data-stu-id="945fc-157">An event cost allocation of 100 percent means that this promotion will be financed exclusively from one fund.</span></span> <span data-ttu-id="945fc-158">促销协议也可以利用多项资金，并且可以使用相等或不同百分比分摊。</span><span class="sxs-lookup"><span data-stu-id="945fc-158">Alternatively, a promotion agreement can draw on several funds, and can use equal or differential percentage allocation.</span></span>

#### <a name="lines"></a><span data-ttu-id="945fc-159">路线</span><span class="sxs-lookup"><span data-stu-id="945fc-159">Lines</span></span>

<span data-ttu-id="945fc-160">接下来，选择**行**切换到行视图。</span><span class="sxs-lookup"><span data-stu-id="945fc-160">Next, select **Lines** to switch to the Lines view.</span></span>

<span data-ttu-id="945fc-161">**促销活动**选项卡显示协议包含的活动类型。</span><span class="sxs-lookup"><span data-stu-id="945fc-161">The **Merchandizing events** tab shows the types of events covered by an agreement.</span></span> <span data-ttu-id="945fc-162">类型有三种：倒付、总计和发票上直接折扣。</span><span class="sxs-lookup"><span data-stu-id="945fc-162">There are three types: bill back, lump sum and off-invoice.</span></span>

<span data-ttu-id="945fc-163">如果选择促销活动，然后选择**金额**选项卡，将显示活动的详细信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-163">When you select the merchandizing event and then select the **Amounts** tab, the details for the event are found.</span></span>

<span data-ttu-id="945fc-164">![贸易折让协议行](./media/trade-allowance-management-agreements-lines.png "贸易折让协议行")</span><span class="sxs-lookup"><span data-stu-id="945fc-164">![Trade allowance agreement lines](./media/trade-allowance-management-agreements-lines.png "Trade allowance agreement lines")</span></span>

<span data-ttu-id="945fc-165">在**贸易折让行**部分中，为定义指定要获得奖励，客户必须达到的数量或金额范围。</span><span class="sxs-lookup"><span data-stu-id="945fc-165">In the **Trade allowance lines** section, you specify the quantity or amount ranges that the customer must achieve for definitions to obtain the rewards.</span></span>

<span data-ttu-id="945fc-166">如果促销活动的类型为**倒付**，则**金额**选项卡的上部定义为倒付应用，生成和在支付时遵守的规则。</span><span class="sxs-lookup"><span data-stu-id="945fc-166">In the case of a merchandizing event of the **Bill back** type, the upper section the **Amounts** tab defines the rules that the bill back will be applied, generated, and paid under.</span></span> <span data-ttu-id="945fc-167">例如，这些规则可以为倒付索赔指定以下条件：</span><span class="sxs-lookup"><span data-stu-id="945fc-167">For example, the rules may specify the following conditions for the bill back claim:</span></span>

- <span data-ttu-id="945fc-168">基于销售订单的创建日期（**计算日期类型**值为**创建日期**）。</span><span class="sxs-lookup"><span data-stu-id="945fc-168">It’s based on the creation date of the sales order (the **Calculation date type** value is **Created**).</span></span>
- <span data-ttu-id="945fc-169">基于销售订单行的折扣前金额，而不是净额（其中包含折扣）进行计算（**取自**值为**总金额**）。</span><span class="sxs-lookup"><span data-stu-id="945fc-169">It’s calculated based on the sales order line’s amount before discounts, not the net amount, which includes discounts (the **Taken from** value is **Gross**).</span></span>
- <span data-ttu-id="945fc-170">基于所售产品量，而不是金额（**返点换行符类型**值为**数量**）。</span><span class="sxs-lookup"><span data-stu-id="945fc-170">It’s based on the volume of the sold products, not the amount (the **Rebate line break type** value is **Quantity**).</span></span>
- <span data-ttu-id="945fc-171">按月为周期计算（**累计销售期限**值为**月**）。</span><span class="sxs-lookup"><span data-stu-id="945fc-171">It’s calculated per period of a month (the **Cumulate sales by** value is **Month**).</span></span> 
- <span data-ttu-id="945fc-172">作为折扣，而不是通过使用 A/P 结算（**付款类型**值为**客户扣除额**）。</span><span class="sxs-lookup"><span data-stu-id="945fc-172">It’s settled as a deduction, not by using A/P (the **Payment type** value is **Customer deductions**).</span></span>

<span data-ttu-id="945fc-173">如果促销活动的类型为**总计**，则**金额**选项卡显示客户达到特定绩效时以扣除的形式付给客户的数量。</span><span class="sxs-lookup"><span data-stu-id="945fc-173">In the case of a merchandizing event of the **Lump sum** type, the **Amounts** tab shows the quantity that will be paid to the customer in the form of a deduction when the customer achieves specific performance.</span></span> <span data-ttu-id="945fc-174">如果审核状态为**未结**，则表示尚未支付总计。</span><span class="sxs-lookup"><span data-stu-id="945fc-174">An approval status of **Open** indicates that the lump sum hasn't yet been paid.</span></span>

<span data-ttu-id="945fc-175">若要将协议应用于满足协议条件的销售订单，则协议的状态必须为**已确认**。</span><span class="sxs-lookup"><span data-stu-id="945fc-175">To apply the agreement to sales orders that meet the agreement's conditions, the agreement's status must be **Confirmed**.</span></span> 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a><span data-ttu-id="945fc-176">通过规划的促销活动开展销售，并生成倒付索赔。</span><span class="sxs-lookup"><span data-stu-id="945fc-176">Perform sales under the planned merchandising event and generate bill-back claims</span></span>

<span data-ttu-id="945fc-177">创建包含用于履行协议要求的行的销售订单时，可通过选择**销售订单行** \> **视图** \> **价格详细信息**在**销售订单**页中查看相关信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-177">When you create a sales order that has lines that fulfill the requirements of the agreement, you can view the related information on the **Sales order** page by selecting **Sales order line** \> **View** \> **Price details**.</span></span>

<span data-ttu-id="945fc-178">在**价格详细信息**页上的**返利**快速选项卡中， 销售员可查看有效贸易折让协议中的倒付（显示返利计划 ID）和为行应用的中金额。</span><span class="sxs-lookup"><span data-stu-id="945fc-178">On the **Price details** page, on the **Rebates** FastTab, the sales clerk can see a bill back from the valid trade allowance agreement (the rebate program ID is shown) and the total amount that is applied to the line.</span></span> <span data-ttu-id="945fc-179">该金额也在**价格详细信息**页的**毛利估计**部分的**返利金额**字段中显示。</span><span class="sxs-lookup"><span data-stu-id="945fc-179">This amount is also shown in the **Rebate amount** field in the **Margin estimation** section of the **Price details** page.</span></span>

<span data-ttu-id="945fc-180">过帐销售发票时，将为每个发票行生成一项相应的倒付索赔。</span><span class="sxs-lookup"><span data-stu-id="945fc-180">When the sales invoice is posted, a corresponding bill-back claim is generated for each invoice line.</span></span>

> [!NOTE]
> <span data-ttu-id="945fc-181">若要查看**价格详细信息**页，请在**应收帐款参数**页上的**价格**选项卡上选中**允许价格明细**复选框。</span><span class="sxs-lookup"><span data-stu-id="945fc-181">To see the **Price details** page, on the **Accounts receivable parameters** page, on the **Prices** tab, select the **Enable price details** check box.</span></span> <span data-ttu-id="945fc-182">I</span><span class="sxs-lookup"><span data-stu-id="945fc-182">I</span></span>

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a><span data-ttu-id="945fc-183">处理索赔并作为扣除传递到 A/R</span><span class="sxs-lookup"><span data-stu-id="945fc-183">Process claims and pass them as deductions to A/R</span></span>

<span data-ttu-id="945fc-184">倒付处理流程中的后续步骤为检查，计算，审核索赔，然后将其转换为扣除。</span><span class="sxs-lookup"><span data-stu-id="945fc-184">The next steps in the process for handling bill-backs are to review, calculate, and approve claims, and then convert them into deductions.</span></span>

<span data-ttu-id="945fc-185">倒付工作台是促销协议负责人定期检查和处理生成的的索赔的位置。</span><span class="sxs-lookup"><span data-stu-id="945fc-185">The Bill back workbench is where the promotion agreement owner periodically reviews and processes the claims that are generated.</span></span> <span data-ttu-id="945fc-186">也是 A/R 管理员根据索赔的付款方式将审核的索赔转换为扣除或正常付款的位置。</span><span class="sxs-lookup"><span data-stu-id="945fc-186">It's also where the A/R administrator converts the approved claims into deductions or regular payments, depending on the payment method for the claim.</span></span>

<span data-ttu-id="945fc-187">可在**倒付工作台**页上查看索赔行。</span><span class="sxs-lookup"><span data-stu-id="945fc-187">On the **Bill back workbench** page, you can review the claim lines.</span></span> <span data-ttu-id="945fc-188">如果索赔的状态为**待重新计算**，则必须重新计算才能达到任何累计效果。</span><span class="sxs-lookup"><span data-stu-id="945fc-188">If the claims are in **To be recalculated** status, they must be recalculated for any cumulative effect.</span></span>

### <a name="recalculate-claims"></a><span data-ttu-id="945fc-189">重新计算索赔</span><span class="sxs-lookup"><span data-stu-id="945fc-189">Recalculate claims</span></span>

<span data-ttu-id="945fc-190">若要重新计算索赔，请在操作窗格上选择**累计**。</span><span class="sxs-lookup"><span data-stu-id="945fc-190">To recalculate the claims, on the Action Pane, select **Cumulate**.</span></span> <span data-ttu-id="945fc-191">然后在**累计返利** 对话框中选择客户。</span><span class="sxs-lookup"><span data-stu-id="945fc-191">Then, in the **Cumulate rebates** dialog box, select the customer.</span></span>

<span data-ttu-id="945fc-192">重新计算的结果是，程序为金额生成新的索赔，以便将原始索赔调整为符合单位金额的资格。</span><span class="sxs-lookup"><span data-stu-id="945fc-192">As a result of the recalculation, the program generates new claims for the amounts to adjust the original claims to the qualifying amount per unit.</span></span> <span data-ttu-id="945fc-193">将为客户、物品、币种、度量单位、库存维度、财务维度和增值税组的每种唯一组合创建一个调整索赔。</span><span class="sxs-lookup"><span data-stu-id="945fc-193">One adjustment claim is generated for each unique combination of a customer, an item, a currency, a unit of measure, inventory dimensions, financial dimensions, and a sales tax group.</span></span> <span data-ttu-id="945fc-194">这些调整索赔与政治被调整的索赔（即最初从销售单据创建的索赔）对销售订单和发票编号的引用相同。</span><span class="sxs-lookup"><span data-stu-id="945fc-194">These adjustment claims have the same reference to the sales order and invoice number as the claims that are being adjusted (that is, the claims that were originally created from the sales document).</span></span> <span data-ttu-id="945fc-195">与原始索赔不同，调整索赔的用于介绍原始销售订单行的金额和数量的字段中没有值。</span><span class="sxs-lookup"><span data-stu-id="945fc-195">Unlike the original claim, the adjustment claim doesn’t have values in the fields that describe the original sales order line’s amounts and quantity.</span></span>

<span data-ttu-id="945fc-196">重新计算完成后，索赔的状态更改为**已计算**。</span><span class="sxs-lookup"><span data-stu-id="945fc-196">After the recalculation is completed, the status of the claims is changed to **Calculated**.</span></span> <span data-ttu-id="945fc-197">若要审核计算索赔，请在操作窗格上选择**审核**。</span><span class="sxs-lookup"><span data-stu-id="945fc-197">To approve the claims, on the Action Pane, select **Approve**.</span></span>

### <a name="process-claims-and-pass-them-to-ar"></a><span data-ttu-id="945fc-198">处理索赔并传递到 A/R</span><span class="sxs-lookup"><span data-stu-id="945fc-198">Process claims and pass them to A/R</span></span>

<span data-ttu-id="945fc-199">索赔现在已准备就绪，可以执行 A/R 处理。</span><span class="sxs-lookup"><span data-stu-id="945fc-199">The claims are now ready for A/R processing.</span></span> <span data-ttu-id="945fc-200">若要处理，请在操作窗格上选择 **处理**。</span><span class="sxs-lookup"><span data-stu-id="945fc-200">To process them, on the Action Pane, select **Process**.</span></span> 

<span data-ttu-id="945fc-201">处理索赔后，状态已更改为**标记**，并指示日记帐过帐（过帐的日记帐为 A/R 参数中指定的应计返利日记帐）已导致发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="945fc-201">Upon processing the claims, the status has changed to **Mark** and indicates that a journal posting (the journal that is posted is the Rebate accrual journal, as specified in the A/R parameters) has caused the following events to occur:</span></span> 

- <span data-ttu-id="945fc-202">已将索赔作为扣除传输到临时客户余额。</span><span class="sxs-lookup"><span data-stu-id="945fc-202">The claims have been transferred to the temporary customer balance as deductions.</span></span>
- <span data-ttu-id="945fc-203">已贷记返利应计帐款，以表示客户的将来负债。</span><span class="sxs-lookup"><span data-stu-id="945fc-203">The rebate accrual account has been credited to represent the future liability for the customer.</span></span>
- <span data-ttu-id="945fc-204">已借记返利支出帐款，以识别销售产生的成本。</span><span class="sxs-lookup"><span data-stu-id="945fc-204">The rebate expense account has been debited to recognize the cost that was incurred in connection with the sales.</span></span>

<span data-ttu-id="945fc-205">若要完成处理，A/R 员现在必须处理应计扣除，方法是将其作为贷方通知单（负债）转到客户余额。</span><span class="sxs-lookup"><span data-stu-id="945fc-205">To complete the process, the A/R clerk must now handle the accrual deductions by transferring them to the customers balance as a credit note (liability).</span></span> 

<span data-ttu-id="945fc-206">若要开始执行任务，请在**客户** 页的操作窗格上选择**收集** \> **结算交易记录**。</span><span class="sxs-lookup"><span data-stu-id="945fc-206">To start the task, on the Action Pane of the **Customer** page, select **Collect** \> **Settle transactions**.</span></span> <span data-ttu-id="945fc-207">然后，在**结算交易记录**页上，选择 **功能** \> **倒付计划**。</span><span class="sxs-lookup"><span data-stu-id="945fc-207">Then, on the **Settle transactions** page, select **Functions** \> **Bill back program**.</span></span> <span data-ttu-id="945fc-208">此返利页显示以前处理的所有返利索赔。</span><span class="sxs-lookup"><span data-stu-id="945fc-208">This rebate page shows all the bill-back claims that were previously processed.</span></span>

<span data-ttu-id="945fc-209">如果要创建贷方通知单，请为所有行选中**标记**复选框，然后选择**功能** \> **创建贷方通知单**。</span><span class="sxs-lookup"><span data-stu-id="945fc-209">If you want to create a credit note, select the **Mark** check box for all lines, and then select **Functions** \> **Create credit note**.</span></span>

<span data-ttu-id="945fc-210">创建贷方通知单后，将过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="945fc-210">Upon credit note creation, a journal is posted.</span></span> <span data-ttu-id="945fc-211">（过帐的日记帐为 A/R 参数中指定的 AR 消耗日记帐）因此，真正负债（贷项）已移到客户余额中。</span><span class="sxs-lookup"><span data-stu-id="945fc-211">(The journal that is posted is the AR consumption journal, as specified in the A/R parameters.) As a result, the real liability (credit) amount has been moved to the customer balance.</span></span> <span data-ttu-id="945fc-212">从财务角度而言，这种情况说明发生了以下事件：</span><span class="sxs-lookup"><span data-stu-id="945fc-212">Financially, this situation implies that the following events have occurred:</span></span>

- <span data-ttu-id="945fc-213">已贷记客户的应收帐款。</span><span class="sxs-lookup"><span data-stu-id="945fc-213">The customer's receivable account has been credited.</span></span>
- <span data-ttu-id="945fc-214">已借记返利应计帐款。</span><span class="sxs-lookup"><span data-stu-id="945fc-214">The rebate accrual account has been debited.</span></span>

<span data-ttu-id="945fc-215">若要审核类型为**总计**的促销活动，请在**贸易折让协议**页中选择活动，然后在**金额**选项卡上选择**审核**。</span><span class="sxs-lookup"><span data-stu-id="945fc-215">To approve a merchandising event of the **Lump sum** type, select the event on the **Trade allowance agreements** page, and then, on the **Amount** tab, select **Approve**.</span></span>

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a><span data-ttu-id="945fc-216">通过使用扣除工作台结算已到期的扣除和客户的不足付款</span><span class="sxs-lookup"><span data-stu-id="945fc-216">Settle the deduction that is due and the customer short-pay by using the Deduction workbench</span></span>

<span data-ttu-id="945fc-217">参与倒付时，客户通常选择不足额支付所选发票。</span><span class="sxs-lookup"><span data-stu-id="945fc-217">Often, in anticipation of bill-backs, customers choose to short-pay selected invoices.</span></span> <span data-ttu-id="945fc-218">为了避免将来发生付款对帐问题，A/R 员在记录实际客户付款时将这些不足付款登记为扣除。</span><span class="sxs-lookup"><span data-stu-id="945fc-218">To prevent payment reconciliation issues in the future, the A/R clerk registers those short-pays as deductions when he or she records the actual customer payments.</span></span> <span data-ttu-id="945fc-219">然后，在扣除工作台上，可以针对公司中的已到期索赔金额轻松结算这些客户扣除。</span><span class="sxs-lookup"><span data-stu-id="945fc-219">Then, on the Deduction workbench, those customer deductions can easily be settled against the claim amounts that are due from the company.</span></span>

<span data-ttu-id="945fc-220">若要在付款日记帐中登记客户的不足付款，请选择**应收帐款** \> **付款** \> **付款日记帐**，然后创建新的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="945fc-220">To register a customer's short-pay in the Payment journal, select **Accounts receivable** \> **Payments** \> **Payment journal**, and create a new payment journal.</span></span> <span data-ttu-id="945fc-221">然后在操作窗格上，选择**扣除**。</span><span class="sxs-lookup"><span data-stu-id="945fc-221">Then, on the Action Pane, select **Deductions**.</span></span> <span data-ttu-id="945fc-222">在**扣除**页中，可以创建和跟踪不足付款金额。</span><span class="sxs-lookup"><span data-stu-id="945fc-222">On the **Deduction** page, you can create and track the amount that was short-paid.</span></span>

<span data-ttu-id="945fc-223">催款经理现在负责在扣除工作台中针对彼此结算未结贷方通知单交易记录和不足付款交易记录。</span><span class="sxs-lookup"><span data-stu-id="945fc-223">The collection manager is now responsible for settling the open credit note transaction and the short-pay transaction against each other in the Deduction workbench.</span></span>

<span data-ttu-id="945fc-224">若要管理扣除，请选择**销售和市场营销** \> **贸易折让**\> **扣除**\> **扣除工作台**。</span><span class="sxs-lookup"><span data-stu-id="945fc-224">To manage deductions, select **Sales and marketing** \> **Trade allowances** \> **Deductions** \> **Deduction workbench**.</span></span> <span data-ttu-id="945fc-225">此页的上半部分包含表示客户的不足付款的行。</span><span class="sxs-lookup"><span data-stu-id="945fc-225">The upper section of the page contains lines that represent the short-pays from the customer.</span></span> <span data-ttu-id="945fc-226">此页的下半部分包含客户的未结贷方交易记录。</span><span class="sxs-lookup"><span data-stu-id="945fc-226">The lower section of the page contains the customers open credit transactions.</span></span> 

<span data-ttu-id="945fc-227">若要结算未结交易记录的扣除，请标记扣除行，然后在“未结交易记录”选项卡上标记该行。</span><span class="sxs-lookup"><span data-stu-id="945fc-227">To settle the deduction against the open transaction, mark the deduction line, and then, on the Open transactions tab, mark the line.</span></span> <span data-ttu-id="945fc-228">在操作窗格上单击“维护 > 匹配”。</span><span class="sxs-lookup"><span data-stu-id="945fc-228">On the Action Pane, click Maintain > Match.</span></span>

<span data-ttu-id="945fc-229">原始索赔的状态现在设置为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="945fc-229">The status of the originating claims is now set to **Completed**.</span></span>

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a><span data-ttu-id="945fc-230">分析促销和所用资金的效果。</span><span class="sxs-lookup"><span data-stu-id="945fc-230">Analyze the effectiveness of the promotion and fund consumption</span></span>

<span data-ttu-id="945fc-231">若要获取计划的关键统计信息和资金使用情况的概览，可使用贸易折让管理中的几种报表和分析视图。</span><span class="sxs-lookup"><span data-stu-id="945fc-231">To get an overview of the program's key statistics and fund use, you can use several reports and analytical views that are available in Trade allowance management.</span></span>

<span data-ttu-id="945fc-232">在**贸易折让活动**页中，**概览**选项卡显示贸易折让协议的主要详细信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-232">On the **Trade allowance activity** page, the **Overview** tab shows the main details of the trade allowance agreement.</span></span> <span data-ttu-id="945fc-233">其他选项卡显示有关关联单据、付款和其他与计划有关的事件更具体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-233">The other tabs show more specific details about the associated documents, payments, and other events that are related to the program.</span></span>

<span data-ttu-id="945fc-234">**汇总**选项卡显示促销时已售出的产品总数、已开票的销售额，以及已支付的倒付和总计。</span><span class="sxs-lookup"><span data-stu-id="945fc-234">The **Summary** tab shows the total quantity of products that have been sold under the promotion, the sales amount that has been invoiced, and the bill-backs and lump sums that have been paid.</span></span>

<span data-ttu-id="945fc-235">**倒付贷记**选项卡包含已贷记给客户的单个倒付的详细信息。</span><span class="sxs-lookup"><span data-stu-id="945fc-235">The **Bill back credits** tab contains the details of individual bill-backs that have been credited to the customer.</span></span>

<span data-ttu-id="945fc-236">若要获取促销的各种性能度量的更多分析概览，可使用分析视图。</span><span class="sxs-lookup"><span data-stu-id="945fc-236">To get a more analytical overview of the various performance measures for the promotion, you can use the Analysis view.</span></span> <span data-ttu-id="945fc-237">若要转至分析视图，请单击**销售和市场营销** \> **贸易折让** \> **贸易折让管理**。</span><span class="sxs-lookup"><span data-stu-id="945fc-237">To go to the Analysis view, click **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span> <span data-ttu-id="945fc-238">在操作窗格上，单击**分析**。</span><span class="sxs-lookup"><span data-stu-id="945fc-238">On the Action Pane, click **Analysis**.</span></span>  

<span data-ttu-id="945fc-239">若要获取促销的各种性能度量的更多分析概览，可使用分析视图。</span><span class="sxs-lookup"><span data-stu-id="945fc-239">To get a more analytical overview of the various performance measures for the promotion, you can use the Analysis view.</span></span> <span data-ttu-id="945fc-240">若要转至分析视图，请单击**销售和市场营销** \> **贸易折让** \> **贸易折让管理**。</span><span class="sxs-lookup"><span data-stu-id="945fc-240">To go to the Analysis view, click **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span> <span data-ttu-id="945fc-241">在操作窗格上，单击**分析**。</span><span class="sxs-lookup"><span data-stu-id="945fc-241">On the Action Pane, click **Analysis**.</span></span> 

