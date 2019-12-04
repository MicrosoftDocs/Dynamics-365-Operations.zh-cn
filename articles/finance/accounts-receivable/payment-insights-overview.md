---
title: 客户付款见解(预览)
description: 本主题介绍付款见解功能，该功能可帮助您更好地理解单个客户的典型付款习惯，并可以识别出可以调整发起收款流程以将此流程提前的情况。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
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
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773906"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="aaefa-103">客户付款见解(预览)</span><span class="sxs-lookup"><span data-stu-id="aaefa-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="aaefa-104">本主题介绍付款见解功能，该功能可帮助您更好地理解单个客户的典型付款习惯，并可以识别出可以调整发起收款流程以提前于您可能发起的情况。</span><span class="sxs-lookup"><span data-stu-id="aaefa-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="aaefa-105">概览</span><span class="sxs-lookup"><span data-stu-id="aaefa-105">Overview</span></span>

<span data-ttu-id="aaefa-106">组织通常发现很难预测客户何时为自己的发票付款。</span><span class="sxs-lookup"><span data-stu-id="aaefa-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="aaefa-107">缺乏见解会导致现金流量预测不准确，收款流程开始得太迟，或者订单被下达到可能拖欠付款的客户。</span><span class="sxs-lookup"><span data-stu-id="aaefa-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="aaefa-108">客户付款见解（预览）可帮助组织预测何时将支付客户发票，从而帮助组织制定收款策略，以提高按时付款的可能性。</span><span class="sxs-lookup"><span data-stu-id="aaefa-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="aaefa-109">预测</span><span class="sxs-lookup"><span data-stu-id="aaefa-109">Predictions</span></span>

<span data-ttu-id="aaefa-110">付款预测将使组织能够轻松地识别可能延迟付款的发票，并采取适当的措施来提高其按时付款的机会，从而改善他们的业务流程。</span><span class="sxs-lookup"><span data-stu-id="aaefa-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="aaefa-111">使用利用历史发票、付款和客户数据的机器学习模型，客户付款见解（预览）可以更准确地预测客户会何时支付未清发票。</span><span class="sxs-lookup"><span data-stu-id="aaefa-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="aaefa-112">对于每个未结发票，客户付款见解（预览）预测三种付款概率：</span><span class="sxs-lookup"><span data-stu-id="aaefa-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="aaefa-113">准时付款概率</span><span class="sxs-lookup"><span data-stu-id="aaefa-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="aaefa-114">延迟付款概率</span><span class="sxs-lookup"><span data-stu-id="aaefa-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="aaefa-115">长时间延迟付款概率</span><span class="sxs-lookup"><span data-stu-id="aaefa-115">Probability of payment being made very late</span></span>

<span data-ttu-id="aaefa-116">为了帮助组织了解他们可以期望客户会在三个时段（准时、延迟和长时间延迟）的哪一个收到付款总金额，客户付款见解（预览）还提供了预期付款的聚合视图。</span><span class="sxs-lookup"><span data-stu-id="aaefa-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="aaefa-117">[![付款预测的聚合视图](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="aaefa-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="aaefa-118">而且，每个发票都指定了按时付款的概率。</span><span class="sxs-lookup"><span data-stu-id="aaefa-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="aaefa-119">如果按时付款的概率小于 50%，发票上会标有红色圆圈，以表示这些发票可能需要注意收款问题。</span><span class="sxs-lookup"><span data-stu-id="aaefa-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="aaefa-120">[![付款概率列表](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="aaefa-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="aaefa-121">客户付款见解（预览）还提供上下文信息以解释预测，例如影响预测的主要因素，客户的业务现状以及有关客户历史付款行为的详细信息。</span><span class="sxs-lookup"><span data-stu-id="aaefa-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="aaefa-122">在许多企业中，收款流程是一种被动活动；在发票到期之前，收款流程不会开始。</span><span class="sxs-lookup"><span data-stu-id="aaefa-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="aaefa-123">借助客户付款见解（预览），组织可以更主动地进行收款。</span><span class="sxs-lookup"><span data-stu-id="aaefa-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="aaefa-124">他们不再需要等待交易到期才开始收款流程。</span><span class="sxs-lookup"><span data-stu-id="aaefa-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="aaefa-125">他们可以使用付款预测功能来确定主动收款是否会提高按时付款的概率。</span><span class="sxs-lookup"><span data-stu-id="aaefa-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="aaefa-126">付款预测还为企业提供了证明有必要提前开始收款流程所需的信息。</span><span class="sxs-lookup"><span data-stu-id="aaefa-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="aaefa-127">方法</span><span class="sxs-lookup"><span data-stu-id="aaefa-127">Methodology</span></span>

<span data-ttu-id="aaefa-128">开发和部署 AI 解决方案非常困难。</span><span class="sxs-lookup"><span data-stu-id="aaefa-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="aaefa-129">需要一支由数据科学家、主题专家和工程师组成的团队长时间工作，以制定、开发、部署和维护可用的 AI 解决方案。</span><span class="sxs-lookup"><span data-stu-id="aaefa-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="aaefa-130">我们使在 Finance 中轻松部署和使用 AI 解决方案变得容易。</span><span class="sxs-lookup"><span data-stu-id="aaefa-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="aaefa-131">我们正在预打包基于 Microsoft AI Builder 构建的 Finance 中的 AI 解决方案。</span><span class="sxs-lookup"><span data-stu-id="aaefa-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="aaefa-132">最终用户只需单击一下按钮，即可部署 AI 解决方案并开始利用智能预测的好处。</span><span class="sxs-lookup"><span data-stu-id="aaefa-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="aaefa-133">如果组织对预测的准确性不满意，那么高级用户可以再次单击以输入 AI Builder 扩展体验，然后选择或取消选择用于生成预测的字段。</span><span class="sxs-lookup"><span data-stu-id="aaefa-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="aaefa-134">一旦准备好，他们就可以培养和发布更改，新培养的模型将在 Finance 中被自动选择用于预测。</span><span class="sxs-lookup"><span data-stu-id="aaefa-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="aaefa-135">如何获取客户付款见解（预览）</span><span class="sxs-lookup"><span data-stu-id="aaefa-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="aaefa-136">如果您有兴趣试用客户付款见解（预览），请向[客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="aaefa-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="aaefa-137">隐私声明</span><span class="sxs-lookup"><span data-stu-id="aaefa-137">Privacy Notice</span></span>

<span data-ttu-id="aaefa-138">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="aaefa-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


