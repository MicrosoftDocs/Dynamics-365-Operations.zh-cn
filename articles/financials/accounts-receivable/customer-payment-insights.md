---
title: "客户付款见解（预览版）"
description: "此主题介绍客户付款见解如何帮助预测何时为发票付款，以及帮助组织创建优化策略以提高按时付款概率。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="customer-payment-insights-preview"></a><span data-ttu-id="2e261-103">客户付款见解（预览版）</span><span class="sxs-lookup"><span data-stu-id="2e261-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2e261-104">此功能是目标版本的一部分，仅适用于已选择加入专用预览的用户。</span><span class="sxs-lookup"><span data-stu-id="2e261-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="2e261-105">此功能还将在即将推出的一个一般可用性版本中提供。</span><span class="sxs-lookup"><span data-stu-id="2e261-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="2e261-106">概览</span><span class="sxs-lookup"><span data-stu-id="2e261-106">Overview</span></span>

<span data-ttu-id="2e261-107">组织通常发现很难预测客户何时为自己的发票付款。</span><span class="sxs-lookup"><span data-stu-id="2e261-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="2e261-108">缺少此项见解可能导致现金流量预测不精确，催款过程效率低下，以及可能将订单下达给可能有信用风险的客户。</span><span class="sxs-lookup"><span data-stu-id="2e261-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="2e261-109">客户付款见解（预览版）使用机器学习预测何时为发票付款。</span><span class="sxs-lookup"><span data-stu-id="2e261-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="2e261-110">还提供可调整的优化策略以将客户按时付款概率发挥到极致。</span><span class="sxs-lookup"><span data-stu-id="2e261-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="2e261-111">预测</span><span class="sxs-lookup"><span data-stu-id="2e261-111">Predictions</span></span>

<span data-ttu-id="2e261-112">组织可通过付款预测改进其业务流程，方法是帮助：</span><span class="sxs-lookup"><span data-stu-id="2e261-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="2e261-113">轻松识别据预测可能晚付款的发票。</span><span class="sxs-lookup"><span data-stu-id="2e261-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="2e261-114">采取相应措施提高按时付款的几率。</span><span class="sxs-lookup"><span data-stu-id="2e261-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="2e261-115">客户付款见解（预览版）使用机器学习预测何时为发票付款。</span><span class="sxs-lookup"><span data-stu-id="2e261-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="2e261-116">使用历史发票、付款和客户数据创建用于预测何时为发票付款的机器学习模型。</span><span class="sxs-lookup"><span data-stu-id="2e261-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="2e261-117">对于每个未结发票，客户付款见解（预览版）预测三种付款概率：</span><span class="sxs-lookup"><span data-stu-id="2e261-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="2e261-118">可能按时付款（在发票的到期日期内）。</span><span class="sxs-lookup"><span data-stu-id="2e261-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="2e261-119">可能在发票的到期日期 30 天内付款。</span><span class="sxs-lookup"><span data-stu-id="2e261-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="2e261-120">可能在发票的到期日期前 30 天内付款。</span><span class="sxs-lookup"><span data-stu-id="2e261-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="2e261-121">可以在预测部分中查看付款概率。</span><span class="sxs-lookup"><span data-stu-id="2e261-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="2e261-122">[![付款预测](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="2e261-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="2e261-123">还将使用上面定义的三种预测的付款概率之一为每个发票分配获胜的付款概率。</span><span class="sxs-lookup"><span data-stu-id="2e261-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="2e261-124">付款概率最高的方案为获胜方案。</span><span class="sxs-lookup"><span data-stu-id="2e261-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="2e261-125">例如，假设一个发票的预测显示其按时付款概率为 71%，到期日期 30 天内付款概率为 13%，到期日期 30 天前付款概率为 16%。</span><span class="sxs-lookup"><span data-stu-id="2e261-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="2e261-126">最高概率显示发票为准时方案，所以将使用准时付款概率标记发票。</span><span class="sxs-lookup"><span data-stu-id="2e261-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="2e261-127">[![付款预测](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="2e261-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="2e261-128">优化策略</span><span class="sxs-lookup"><span data-stu-id="2e261-128">Optimization strategies</span></span>

<span data-ttu-id="2e261-129">除了付款预测，客户付款见解（预览版）还可以使用优化策略提高准时付款的几率。</span><span class="sxs-lookup"><span data-stu-id="2e261-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="2e261-130">这样组织就可以通过让用户调整发票和客户参数执行“假设”分析，然后比较对发票准时收款概率的相应影响。</span><span class="sxs-lookup"><span data-stu-id="2e261-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="2e261-131">例如，组织可能希望估计更新发票中的现金折扣对准时收款概率的影响。</span><span class="sxs-lookup"><span data-stu-id="2e261-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="2e261-132">发票优化后使用新折扣时，用户可以查看应用折扣对发票准时收款概率的影响。</span><span class="sxs-lookup"><span data-stu-id="2e261-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="2e261-133">如果与准时催款的优点相比，应用折扣的成本最低，组织可能选择对将来的所有未结订单应用所选折扣。</span><span class="sxs-lookup"><span data-stu-id="2e261-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="2e261-134">现在，只有折扣才可以成为客户付款见解（预览版）的优化策略。</span><span class="sxs-lookup"><span data-stu-id="2e261-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="2e261-135">[![优化后的预测](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="2e261-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="2e261-136">如何获取客户付款见解（预览版）</span><span class="sxs-lookup"><span data-stu-id="2e261-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="2e261-137">如果您有兴趣试用客户付款见解（预览版），请向[财务见解预览团队](mailto:fiap@microsoft.com)发电子邮件。</span><span class="sxs-lookup"><span data-stu-id="2e261-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="2e261-138">隐私声明</span><span class="sxs-lookup"><span data-stu-id="2e261-138">Privacy Statement</span></span>

<span data-ttu-id="2e261-139">预览版将客户数据存储在美国。</span><span class="sxs-lookup"><span data-stu-id="2e261-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="2e261-140">此外，预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 for Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="2e261-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>

