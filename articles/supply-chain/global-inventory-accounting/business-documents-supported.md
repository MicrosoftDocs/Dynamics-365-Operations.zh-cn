---
title: 全球库存核算支持的业务单据
description: 本主题列出了全球库存核算支持的业务单据。 它还提供了采购订单单据的详细示例。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 311c894d709985d0d053b0ec3a317142aa582c39
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273121"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a><span data-ttu-id="5c698-104">全球库存核算支持的业务单据</span><span class="sxs-lookup"><span data-stu-id="5c698-104">Business documents supported by Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="5c698-105">完全设置全球库存核算加载项后，即可处理在 Microsoft Dynamics 365 Supply Chain Management 中输入的与库存相关的单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-105">After the Global Inventory Accounting Add-in is fully set up, it's ready to process inventory-related documents that are entered in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="supported-business-documents"></a><span data-ttu-id="5c698-106">支持的业务单据</span><span class="sxs-lookup"><span data-stu-id="5c698-106">Supported business documents</span></span>

<span data-ttu-id="5c698-107">有两种类型的业务单据：</span><span class="sxs-lookup"><span data-stu-id="5c698-107">There are two types of business documents:</span></span>

- <span data-ttu-id="5c698-108">**具有日记帐的单据** – 这些单据包括产品收货、采购发票、装箱单和销售发票单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-108">**Documents that have a journal** – These documents include product receipt, purchase invoice, packing slip, and sales invoice documents.</span></span>
- <span data-ttu-id="5c698-109">**没有日记帐的单据** – 这些单据包括盘点、移动和库存调整单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-109">**Documents that don't have a journal** – These documents include counting, movement, and inventory adjustment documents.</span></span>

<span data-ttu-id="5c698-110">在本主题的后面，将使用采购订单作为示例来说明该流程。</span><span class="sxs-lookup"><span data-stu-id="5c698-110">Later in this topic, purchase orders will be used as an example to illustrate the process.</span></span>

<span data-ttu-id="5c698-111">下表列出了当前版本支持的单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-111">The following table lists the documents that the current release supports.</span></span>

| <span data-ttu-id="5c698-112">文件类型</span><span class="sxs-lookup"><span data-stu-id="5c698-112">Document type</span></span>      | <span data-ttu-id="5c698-113">单据</span><span class="sxs-lookup"><span data-stu-id="5c698-113">Document</span></span>        |
|--------------------|-----------------|
| <span data-ttu-id="5c698-114">采购订单</span><span class="sxs-lookup"><span data-stu-id="5c698-114">Purchase Order</span></span>     | <span data-ttu-id="5c698-115">物料收货</span><span class="sxs-lookup"><span data-stu-id="5c698-115">Product Receipt</span></span> |
| <span data-ttu-id="5c698-116">采购订单</span><span class="sxs-lookup"><span data-stu-id="5c698-116">Purchase Order</span></span>     | <span data-ttu-id="5c698-117">发票</span><span class="sxs-lookup"><span data-stu-id="5c698-117">Invoice</span></span>         |
| <span data-ttu-id="5c698-118">销售订单</span><span class="sxs-lookup"><span data-stu-id="5c698-118">Sales Order</span></span>        | <span data-ttu-id="5c698-119">装箱单</span><span class="sxs-lookup"><span data-stu-id="5c698-119">Packing slip</span></span>    |
| <span data-ttu-id="5c698-120">销售订单</span><span class="sxs-lookup"><span data-stu-id="5c698-120">Sales Order</span></span>        | <span data-ttu-id="5c698-121">发票</span><span class="sxs-lookup"><span data-stu-id="5c698-121">Invoice</span></span>         |
| <span data-ttu-id="5c698-122">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="5c698-122">Inventory Journals</span></span> | <span data-ttu-id="5c698-123">变动</span><span class="sxs-lookup"><span data-stu-id="5c698-123">Movement</span></span>        |
| <span data-ttu-id="5c698-124">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="5c698-124">Inventory Journals</span></span> | <span data-ttu-id="5c698-125">调整</span><span class="sxs-lookup"><span data-stu-id="5c698-125">Adjustment</span></span>      |
| <span data-ttu-id="5c698-126">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="5c698-126">Inventory Journals</span></span> | <span data-ttu-id="5c698-127">盘点</span><span class="sxs-lookup"><span data-stu-id="5c698-127">Counting</span></span>        |
| <span data-ttu-id="5c698-128">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="5c698-128">Inventory Journals</span></span> | <span data-ttu-id="5c698-129">转让</span><span class="sxs-lookup"><span data-stu-id="5c698-129">Transfer</span></span>        |
| <span data-ttu-id="5c698-130">转移单</span><span class="sxs-lookup"><span data-stu-id="5c698-130">Transfer Order</span></span>     | <span data-ttu-id="5c698-131">装运</span><span class="sxs-lookup"><span data-stu-id="5c698-131">Shipment</span></span>        |
| <span data-ttu-id="5c698-132">转移单</span><span class="sxs-lookup"><span data-stu-id="5c698-132">Transfer Order</span></span>     | <span data-ttu-id="5c698-133">收货</span><span class="sxs-lookup"><span data-stu-id="5c698-133">Receive</span></span>         |

> [!IMPORTANT]
> <span data-ttu-id="5c698-134">全球库存核算异步处理在 Supply Chain Management 中输入的单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-134">Global Inventory Accounting asynchronously processes the documents that are entered in Supply Chain Management.</span></span> <span data-ttu-id="5c698-135">对于有问题的单据，不会显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="5c698-135">No error messages will be shown for problematic documents.</span></span>

## <a name="example-purchase-order"></a><span data-ttu-id="5c698-136">示例：采购订单</span><span class="sxs-lookup"><span data-stu-id="5c698-136">Example: Purchase order</span></span>

### <a name="product-receipt"></a><span data-ttu-id="5c698-137">产品收货</span><span class="sxs-lookup"><span data-stu-id="5c698-137">Product receipt</span></span>

<span data-ttu-id="5c698-138">按常规方式过帐产品收货。</span><span class="sxs-lookup"><span data-stu-id="5c698-138">Post product receipts in the usual way.</span></span> <span data-ttu-id="5c698-139">在 **所有采购订单** 页面上，选择采购订单，然后在操作窗格的 **接收** 选项卡上，选择 **产品收货** 以打开 **产品收货日记帐** 页面。</span><span class="sxs-lookup"><span data-stu-id="5c698-139">On the **All purchase orders** page, select a purchase order, and then, on the Action Pane, on the **Receive** tab, select **Product receipt** to open the **Product receipt journal** page.</span></span> <span data-ttu-id="5c698-140">为每一行生成操作事件和全球库存核算事件。</span><span class="sxs-lookup"><span data-stu-id="5c698-140">An operation event and a Global Invntroy Accounting event are generated for each line.</span></span> <span data-ttu-id="5c698-141">因此，选择 **行** 选项卡，然后选择 **库存 \> 事件和度量** 以打开 **事件和度量** 页面。</span><span class="sxs-lookup"><span data-stu-id="5c698-141">Therefore, select the **Lines** tab, and then select **Inventory \> Events and measurements** to open the **Events and measurements** page.</span></span>

<span data-ttu-id="5c698-142">全球库存核算是基于事件和度量的核算系统。</span><span class="sxs-lookup"><span data-stu-id="5c698-142">Global Inventory Accounting is an accounting system that is based on events and measurements.</span></span> <span data-ttu-id="5c698-143">**事件和度量** 页面上的度量行网格显示度量的列表。</span><span class="sxs-lookup"><span data-stu-id="5c698-143">The measurement line grid on the **Events and measurements** page shows a list of measurements.</span></span> <span data-ttu-id="5c698-144">每个度量都有一个维度列表。</span><span class="sxs-lookup"><span data-stu-id="5c698-144">Each measurement has a list of dimensions.</span></span>

<span data-ttu-id="5c698-145">对于每个操作事件，有两种类型的度量：</span><span class="sxs-lookup"><span data-stu-id="5c698-145">For each operation event, there are two types of measurement:</span></span>

- <span data-ttu-id="5c698-146">**操作度量** – 这些度量以通用术语描述业务单据。</span><span class="sxs-lookup"><span data-stu-id="5c698-146">**Operations measurements** – These measurements describe business documents in generic terms.</span></span> <span data-ttu-id="5c698-147">一种度量是使用在单据中使用的度量单位的产品数量。</span><span class="sxs-lookup"><span data-stu-id="5c698-147">One measurement is the product quantity using the unit of measure that is used in the document.</span></span> <span data-ttu-id="5c698-148">还有一些影响库存价值的度量，例如延伸价格、折扣、折扣百分比和行费用。</span><span class="sxs-lookup"><span data-stu-id="5c698-148">There are also measurements that affect the inventory value, such as extended price, discount, discount percent, and line charge.</span></span>
- <span data-ttu-id="5c698-149">**资源核算度量** – 这些度量源自库存登记的角度。</span><span class="sxs-lookup"><span data-stu-id="5c698-149">**Resource accounting measurements** – These measurements are from the inventory register perspective.</span></span> <span data-ttu-id="5c698-150">它们以库存度量单位描述单据对库存的影响。</span><span class="sxs-lookup"><span data-stu-id="5c698-150">They describe the document's impact on the inventory in the inventory unit of measure.</span></span> <span data-ttu-id="5c698-151">如果存在多个库存登记，则存在多行资源核算度量。</span><span class="sxs-lookup"><span data-stu-id="5c698-151">If there are multiple inventory registrations, there are multiple lines of resource accounting measurements.</span></span>

<span data-ttu-id="5c698-152">维度按以下方式组织：</span><span class="sxs-lookup"><span data-stu-id="5c698-152">The dimensions are organized in the following way:</span></span>

- <span data-ttu-id="5c698-153">**二元性** – 二元性描述参与经济事件的代理。</span><span class="sxs-lookup"><span data-stu-id="5c698-153">**Duality** – Duality describes the agents who participate in the economic events.</span></span> <span data-ttu-id="5c698-154">对于外部业务单据，原始维度描述输入单据的法人，而双重维度描述供应商、客户等。</span><span class="sxs-lookup"><span data-stu-id="5c698-154">For external business documents, the primal dimensions describe the legal entity where the document is entered, whereas the dual dimensions describe the vendor, customer, and so on.</span></span> <span data-ttu-id="5c698-155">对于内部业务单据（例如，转移单），双重维度描述对应仓库。</span><span class="sxs-lookup"><span data-stu-id="5c698-155">For internal business documents (for example, transfer orders), the dual dimensions describe the counterpart warehouse.</span></span>
- <span data-ttu-id="5c698-156">**维度类型** – 维度类型对维度进行分类。</span><span class="sxs-lookup"><span data-stu-id="5c698-156">**Dimension type** – Dimension types categorize the dimensions.</span></span>
- <span data-ttu-id="5c698-157">**维度** – 维度的名称。</span><span class="sxs-lookup"><span data-stu-id="5c698-157">**Dimension** – The name of the dimension.</span></span>
- <span data-ttu-id="5c698-158">**维度值** – 维度的值。</span><span class="sxs-lookup"><span data-stu-id="5c698-158">**Dimension value** – The value of the dimension.</span></span>

### <a name="global-inventory-accounting-event"></a><span data-ttu-id="5c698-159">全球库存核算事件</span><span class="sxs-lookup"><span data-stu-id="5c698-159">Global Inventory Accounting event</span></span>

<span data-ttu-id="5c698-160">全球库存核算将操作事件和度量作为输入。</span><span class="sxs-lookup"><span data-stu-id="5c698-160">Global Inventory Accounting takes the operational events and measurements as input.</span></span> <span data-ttu-id="5c698-161">然后，它基于附加的货币和惯例对每个相关分类帐进行适当的核算。</span><span class="sxs-lookup"><span data-stu-id="5c698-161">It then does the appropriate accounting for each related ledger, based on the attached currency and convention.</span></span> <span data-ttu-id="5c698-162">您可以选择 **全球库存核算事件和度量** 以查看全球库存核算事件。</span><span class="sxs-lookup"><span data-stu-id="5c698-162">You can select **Global inventory accounting events and measurements** to view the Global Inventory Accounting event.</span></span> <span data-ttu-id="5c698-163">全球库存核算事件遵循与操作事件相同的方法，但它使用不同的度量。</span><span class="sxs-lookup"><span data-stu-id="5c698-163">The Global Inventory Accounting event follows the same methodology as operation events, but it uses different measurements.</span></span> <span data-ttu-id="5c698-164">有三种主要度量类型：产品成本数量、产品成本和差异。</span><span class="sxs-lookup"><span data-stu-id="5c698-164">There are three major measurement types: product cost quantity, product cost, and variance.</span></span>

<span data-ttu-id="5c698-165">子分类帐科目用于进一步对度量进行分类。</span><span class="sxs-lookup"><span data-stu-id="5c698-165">Subledger accounts are used to further classify the measurements.</span></span> <span data-ttu-id="5c698-166">可能有多个分类帐。</span><span class="sxs-lookup"><span data-stu-id="5c698-166">There might be multiple ledgers.</span></span> <span data-ttu-id="5c698-167">这些分类帐与输入单据的法人相关联。</span><span class="sxs-lookup"><span data-stu-id="5c698-167">These ledgers are linked to the legal entity where the document is entered.</span></span> <span data-ttu-id="5c698-168">您可以通过更改 **分类帐** 字段的值，查看每个分类帐的事件和度量。</span><span class="sxs-lookup"><span data-stu-id="5c698-168">You can view the events and measurements for each ledger by changing the value of the **Ledger** field.</span></span>

### <a name="cost-element"></a><span data-ttu-id="5c698-169">成本元素</span><span class="sxs-lookup"><span data-stu-id="5c698-169">Cost element</span></span>

<span data-ttu-id="5c698-170">基于附加到分类帐的成本元素策略，系统将成本元素分派给每个影响库存成本的已核算操作事件度量。</span><span class="sxs-lookup"><span data-stu-id="5c698-170">Based on the cost element policy that is attached to the ledger, the system assigns a cost element to each accounted operation event measurement that affects the inventory cost.</span></span> <span data-ttu-id="5c698-171">这些度量包括延伸价格、折扣、折扣百分比和行费用。</span><span class="sxs-lookup"><span data-stu-id="5c698-171">These measurements include extended price, discount, discount percent, and line charge.</span></span>

### <a name="measurement-line-details"></a><span data-ttu-id="5c698-172">度量行详细信息</span><span class="sxs-lookup"><span data-stu-id="5c698-172">Measurement line details</span></span>

<span data-ttu-id="5c698-173">**概述** 选项卡显示附加策略的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5c698-173">The **Overview** tab shows the details of the attached policies.</span></span> <span data-ttu-id="5c698-174">成本对象维度基于成本对象策略显示成本对象。</span><span class="sxs-lookup"><span data-stu-id="5c698-174">The cost object dimensions show the cost object, based on the cost object policy.</span></span> <span data-ttu-id="5c698-175">如果成本流假设为 *特定 – 批次*，特定的标识维度显示批号。</span><span class="sxs-lookup"><span data-stu-id="5c698-175">Specific identification dimensions show the batch number if the cost flow assumption is *Specific – Batch*.</span></span>

### <a name="purchase-invoice"></a><span data-ttu-id="5c698-176">采购发票</span><span class="sxs-lookup"><span data-stu-id="5c698-176">Purchase invoice</span></span>

<span data-ttu-id="5c698-177">按常规方式过帐发票。</span><span class="sxs-lookup"><span data-stu-id="5c698-177">Post the invoice in the usual way.</span></span> <span data-ttu-id="5c698-178">然后，在操作窗格的 **发票** 选项卡上，在 **日记帐** 组中，选择 **发票** 以打开发票日记帐。</span><span class="sxs-lookup"><span data-stu-id="5c698-178">Then, on the Action Pane, on the **Invoice** tab, in the **Journals** group, select **Invoice** to open the invoice journal.</span></span> <span data-ttu-id="5c698-179">为每一行生成操作事件和全球库存核算事件。</span><span class="sxs-lookup"><span data-stu-id="5c698-179">An operation event and a Global Inventory Accounting event are generated for each line.</span></span> <span data-ttu-id="5c698-180">因此，选择 **行** 选项卡，然后选择 **库存 \> 事件和度量** 以打开 **事件和度量** 页面。</span><span class="sxs-lookup"><span data-stu-id="5c698-180">Therefore, select the **Lines** tab, and then select **Inventory \> Events and measurements** to open the **Events and measurements** page.</span></span> <span data-ttu-id="5c698-181">**事件和度量** 页面显示相同的度量类型。</span><span class="sxs-lookup"><span data-stu-id="5c698-181">The **Events and measurements** page shows the same measure type.</span></span> <span data-ttu-id="5c698-182">但是，由于页面显示不同的度量角色和度量修饰符，因此对代理（法人）的影响不同。</span><span class="sxs-lookup"><span data-stu-id="5c698-182">However, because the page shows a different measure role and measure modifier, the impact on the agent (legal entity) differs.</span></span>

<span data-ttu-id="5c698-183">选择 **全球库存核算事件和度量** 以查看全球库存核算事件。</span><span class="sxs-lookup"><span data-stu-id="5c698-183">Select **Global inventory accounting events and measurements** to view the Global Inventory Accounting event.</span></span> <span data-ttu-id="5c698-184">库存数量和成本现在从 *收到的货物未开具库存发票* 分类帐科目中流出，并流入到 *所采购货物的成本* 分类帐科目中。</span><span class="sxs-lookup"><span data-stu-id="5c698-184">The inventory quantity and cost now flow out from the *Goods received not invoiced inventory* subledger account and into the *Cost of goods purchased* subledger account.</span></span>
