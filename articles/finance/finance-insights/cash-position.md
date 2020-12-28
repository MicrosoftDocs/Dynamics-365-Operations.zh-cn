---
title: 现金头寸（预览）
description: 本主题描述现金流预测功能如何预测组织在特定时间的现金头寸。 还描述了可用于显示不同期间的预测的选项。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 64b8dcd43024e5c26d33bf12c5fe198711adde56
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645882"
---
# <a name="cash-position-preview"></a><span data-ttu-id="72a4b-104">现金头寸（预览）</span><span class="sxs-lookup"><span data-stu-id="72a4b-104">Cash position (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72a4b-105">现金头寸是对现金流的短期预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-105">Cash position is the projection of cash flow that is forecast for the near term.</span></span> <span data-ttu-id="72a4b-106">它基于对支付未付发票和订单的客户的现金收入的预测，还基于对购买发票和订单支付给供应商的现金支出的预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-106">It's based on the projection of cash receipts from customers that pay outstanding invoices and orders, and also on the projection cash disbursements that are paid to vendors for purchase invoices and orders.</span></span>

<span data-ttu-id="72a4b-107">当系统预测客户付款时，它将使用来自客户付款预测功能的付款预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-107">When the system predicts customer payments, it uses the payment predictions from the customer payment prediction feature.</span></span> <span data-ttu-id="72a4b-108">如果没有付款预测，则使用将每个客户的客户发票转换为付款所需的平均时间来计算付款日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-108">Without payment predictions, the average time that is required to convert a customer invoice to a payment for each customer is used to calculate a payment date.</span></span> <span data-ttu-id="72a4b-109">对于未结客户订单，系统通过使用要开票的每个客户的订单行的平均天数来计算发票日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-109">For open customer orders, the system calculates the invoice date by using the average number of days for order lines per customer to be invoiced.</span></span> <span data-ttu-id="72a4b-110">然后，它将发票日期用作付款预测功能的输入。</span><span class="sxs-lookup"><span data-stu-id="72a4b-110">It then uses the invoice date as an input for the payment prediction functionality.</span></span> <span data-ttu-id="72a4b-111">客户付款预测功能可计算每个订单行的付款日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-111">The customer payment prediction functionality calculates a payment date for each order line.</span></span> 

<span data-ttu-id="72a4b-112"><*需要来自 Jarek 或 Dave 的有关如何将付款预测转换为日期的文本*> 未付发票的付款日期通过付款预测推测 [*估计*]，方法是选取对应于从预测的时段概率获得的累积分布函数的百分之五十的日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-112"><*Need text from Jarek or Dave on how payment predictions are converted to a date*> The payment date for outstanding invoices is approximated [*estimated*] from the payment predictions by picking a date that corresponds to fiftieth percentile of the cumulative distribution function that's obtained from the predicted bucket's probabilities.</span></span>

<span data-ttu-id="72a4b-113">使用类似的方法来预测对供应商的付款。</span><span class="sxs-lookup"><span data-stu-id="72a4b-113">A similar approach is used to predict payments to vendors.</span></span> <span data-ttu-id="72a4b-114">对于每个供应商，系统都会计算将供应商发票转换为付款所需的平均时间。</span><span class="sxs-lookup"><span data-stu-id="72a4b-114">For each vendor, the system calculates the average time that is required to convert a vendor invoice to a payment.</span></span> <span data-ttu-id="72a4b-115">然后使用天数计算付款日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-115">That number of days is then used to calculate the payment date.</span></span> <span data-ttu-id="72a4b-116">对于未结供应商订单，系统通过考虑将每个供应商的订单行转换为发票所需的平均天数来计算发票日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-116">For open vendor orders, the system calculates the invoice date by considering the average number of days that is required to convert order lines to an invoice for each vendor.</span></span> <span data-ttu-id="72a4b-117">然后，系统使用将供应商发票转换为每位供应商的付款的平均时间计算付款日期。</span><span class="sxs-lookup"><span data-stu-id="72a4b-117">The system then calculates the payment date by using the average time to convert a vendor invoice to a payment for each vendor.</span></span>

<span data-ttu-id="72a4b-118">**现金头寸** 选项卡上部包含一个现金头寸图表。</span><span class="sxs-lookup"><span data-stu-id="72a4b-118">The upper section of the **Cash position** tab includes a cash position chart.</span></span> <span data-ttu-id="72a4b-119">该图表显示现金流入和流出，以及它们对总流动性余额的影响。</span><span class="sxs-lookup"><span data-stu-id="72a4b-119">This chart shows cash inflows and outflows, and their impact on the total liquidity balance.</span></span> <span data-ttu-id="72a4b-120">可以按天、周、月或季度期间查看现金头寸图表中的详细信息。</span><span class="sxs-lookup"><span data-stu-id="72a4b-120">The details in the cash position chart can be viewed in daily, weekly, monthly, or quarterly periods.</span></span> <span data-ttu-id="72a4b-121">当您选择 **每日**，则可以查看未来 21 天的预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-121">When you select **Daily**, you can view forecasts for the next 21 days.</span></span> <span data-ttu-id="72a4b-122">当您选择 **每周**，则可以查看未来 20 周的预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-122">When you select **Weekly**, you can view forecasts for the next 20 weeks.</span></span> <span data-ttu-id="72a4b-123">当您选择 **每月**，则可以查看未来 12 个月的预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-123">When you select **Monthly**, you can view forecasts for the next 12 months.</span></span> <span data-ttu-id="72a4b-124">当您选择 **每季度**，则可以查看未来 12 个季度的预测。</span><span class="sxs-lookup"><span data-stu-id="72a4b-124">When you select **Quarterly**, you can view forecasts for the next 12 quarters.</span></span> <span data-ttu-id="72a4b-125">如果您需要在屏幕上留出更多空间来查看 **现金头寸** 选项卡中的内容，可以隐藏图表。</span><span class="sxs-lookup"><span data-stu-id="72a4b-125">You can hide the chart if you require additional space on your screen to view content on the **Cash position** tab.</span></span>

<span data-ttu-id="72a4b-126">**现金头寸** 的下部显示头寸、现金流、预测付款和银行帐户的详细信息。</span><span class="sxs-lookup"><span data-stu-id="72a4b-126">The lower section of the **Cash position** tab shows details for the position, cash flow, projected payments, and bank account.</span></span>

- <span data-ttu-id="72a4b-127">**头寸详细信息** 网格的三个部分中提供了信息：流动性科目列表、构成现金流入的文档的列表，以及构成现金流出的文档的列表。</span><span class="sxs-lookup"><span data-stu-id="72a4b-127">Information in the **Position details** grid is presented in three sections: a list of liquidity accounts, a list of documents that make up cash inflows, and a list of documents that make up cash outflows.</span></span> <span data-ttu-id="72a4b-128">此网格还显示现金头寸余额。</span><span class="sxs-lookup"><span data-stu-id="72a4b-128">The grid also shows cash position balances.</span></span> <span data-ttu-id="72a4b-129">对于您正在查看的第一个期间，流动性科目的余额为期初余额。</span><span class="sxs-lookup"><span data-stu-id="72a4b-129">For the first period that you're viewing, the balance for the liquidity accounts is the opening balance.</span></span> <span data-ttu-id="72a4b-130">对于后续期间，流动性科目的余额根据现金流入的增加和从之前期间的现金流出扣除来计算。</span><span class="sxs-lookup"><span data-stu-id="72a4b-130">For subsequent periods, the balances for the liquidity accounts are calculated based on the addition of cash inflows and the subtraction of cash outflows from previous periods.</span></span> <span data-ttu-id="72a4b-131">要查看构成余额的交易的详细信息，请选择 **余额** 链接。</span><span class="sxs-lookup"><span data-stu-id="72a4b-131">To view details of the transactions that make up the balance, select the **Balance** link.</span></span>
- <span data-ttu-id="72a4b-132">**现金流** 网格显示现金流入、每个期间聚合的现金流出，及其对流动性科目余额的影响。</span><span class="sxs-lookup"><span data-stu-id="72a4b-132">The **Cash flow** grid shows cash inflows, cash outflows aggregated per period, and their impact on liquidity account balances.</span></span> <span data-ttu-id="72a4b-133">对于第一个期间，流动性科目的余额为期初余额。</span><span class="sxs-lookup"><span data-stu-id="72a4b-133">For the first period, the balance for the liquidity accounts is the opening balance.</span></span> <span data-ttu-id="72a4b-134">对于后续期间，流动性科目的余额根据现金流入的增加和从之前期间的现金流出扣除来计算。</span><span class="sxs-lookup"><span data-stu-id="72a4b-134">For subsequent periods, the balances for the liquidity accounts are calculated based on the addition of cash inflows and the subtraction of cash outflows from previous periods.</span></span>
- <span data-ttu-id="72a4b-135">**预测银行科目** 网格显示预期现金流出及其对流动性科目的影响。</span><span class="sxs-lookup"><span data-stu-id="72a4b-135">The **Projected bank balance** grid show expected cash outflows and their impact on liquidity accounts.</span></span>
- <span data-ttu-id="72a4b-136">**银行科目** 网格显示预期现金流入和流出对银行余额的影响。</span><span class="sxs-lookup"><span data-stu-id="72a4b-136">The **Bank account** grid shows the impact of expected cash inflows and outflows on the bank balance.</span></span>

<span data-ttu-id="72a4b-137">要保存和编辑现金头寸，请创建快照。</span><span class="sxs-lookup"><span data-stu-id="72a4b-137">To save and edit the cash position, create a snapshot.</span></span> <span data-ttu-id="72a4b-138">有关如何处理快照的详细信息，请参阅[快照概述](payment-snapshots.md)。</span><span class="sxs-lookup"><span data-stu-id="72a4b-138">For more information about how to work with snapshots, see [Snapshots overview](payment-snapshots.md).</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="72a4b-139">隐私声明</span><span class="sxs-lookup"><span data-stu-id="72a4b-139">Privacy notice</span></span>
<span data-ttu-id="72a4b-140">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="72a4b-140">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
