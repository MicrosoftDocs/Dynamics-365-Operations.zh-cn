---
title: 客户付款预测(预览版)
description: 此主题介绍可帮助您更好理解客户的典型付款实践的付款预测功能。 此功能还可以帮助您确定应导致您开始执行本应提前进行的收款流程的情况。
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
ms.openlocfilehash: b321fdc185e175d9fe2673c9f1e16486efd8e798
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645665"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="95b5b-104">客户付款预测(预览版)</span><span class="sxs-lookup"><span data-stu-id="95b5b-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="95b5b-105">此主题介绍可帮助您更好理解客户的典型付款实践的付款预测功能。</span><span class="sxs-lookup"><span data-stu-id="95b5b-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="95b5b-106">此功能还可以帮助您确定应导致您开始执行本应提前进行的收款流程的情况。</span><span class="sxs-lookup"><span data-stu-id="95b5b-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="95b5b-107">概览</span><span class="sxs-lookup"><span data-stu-id="95b5b-107">Overview</span></span>

<span data-ttu-id="95b5b-108">组织通常发现很难预测客户何时为自己的发票付款。</span><span class="sxs-lookup"><span data-stu-id="95b5b-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="95b5b-109">缺乏此见识可能会导致以下问题：</span><span class="sxs-lookup"><span data-stu-id="95b5b-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="95b5b-110">现金流量预测不准确</span><span class="sxs-lookup"><span data-stu-id="95b5b-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="95b5b-111">开始得太晚的收款流程</span><span class="sxs-lookup"><span data-stu-id="95b5b-111">Collections processes that start too late</span></span>
- <span data-ttu-id="95b5b-112">下达给可能拖欠付款的客户的订单</span><span class="sxs-lookup"><span data-stu-id="95b5b-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="95b5b-113">客户付款预测（预览）可帮助组织预测客户何时为发票付款。</span><span class="sxs-lookup"><span data-stu-id="95b5b-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="95b5b-114">因此，他们可以创建收款策略，以帮助增加按时付款的可能性。</span><span class="sxs-lookup"><span data-stu-id="95b5b-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="95b5b-115">预测</span><span class="sxs-lookup"><span data-stu-id="95b5b-115">Predictions</span></span>

<span data-ttu-id="95b5b-116">付款预测使组织可以通过帮助组织识别可能逾期付款的发票来改善其业务流程。</span><span class="sxs-lookup"><span data-stu-id="95b5b-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="95b5b-117">组织可以使用该信息来采取行动，以提高按时付款的机会。</span><span class="sxs-lookup"><span data-stu-id="95b5b-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="95b5b-118">客户付款预测功能使用机器学习模型来更准确地预测客户何时支付未清发票。</span><span class="sxs-lookup"><span data-stu-id="95b5b-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="95b5b-119">该机器学习模型包括历史发票、付款和客户数据。</span><span class="sxs-lookup"><span data-stu-id="95b5b-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="95b5b-120">对于每张未结发票，此功能分配三项付款概率：</span><span class="sxs-lookup"><span data-stu-id="95b5b-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="95b5b-121">按时付款的概率</span><span class="sxs-lookup"><span data-stu-id="95b5b-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="95b5b-122">逾期付款的概率</span><span class="sxs-lookup"><span data-stu-id="95b5b-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="95b5b-123">严重逾期付款的概率</span><span class="sxs-lookup"><span data-stu-id="95b5b-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="95b5b-124">该功能还提供了预期付款的汇总视图。</span><span class="sxs-lookup"><span data-stu-id="95b5b-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="95b5b-125">[![付款预测的聚合视图](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="95b5b-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="95b5b-126">每个发票都指定了按时付款的概率。</span><span class="sxs-lookup"><span data-stu-id="95b5b-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="95b5b-127">按时付款概率小于 50% 的发票上会标有红色圆圈，以表示收款代理可能需要注意这些发票。</span><span class="sxs-lookup"><span data-stu-id="95b5b-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="95b5b-128">[![付款概率列表](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="95b5b-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="95b5b-129">客户付款预测功能还提供上下文信息以解释预测。</span><span class="sxs-lookup"><span data-stu-id="95b5b-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="95b5b-130">此信息包括影响预测的主要因素、与客户之间的业务的当前状态，以及有关客户的历史付款行为的详细信息。</span><span class="sxs-lookup"><span data-stu-id="95b5b-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="95b5b-131">在许多业务中，收款流程是一种被动活动。</span><span class="sxs-lookup"><span data-stu-id="95b5b-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="95b5b-132">换句话说，直到发票到期，才开始收款流程。</span><span class="sxs-lookup"><span data-stu-id="95b5b-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="95b5b-133">借助客户付款预测，组织可以更主动地进行收款。</span><span class="sxs-lookup"><span data-stu-id="95b5b-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="95b5b-134">他们不再需要等待交易到期才开始收款流程。</span><span class="sxs-lookup"><span data-stu-id="95b5b-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="95b5b-135">他们可以使用付款预测功能来确定主动收款是否会提高按时付款的概率。</span><span class="sxs-lookup"><span data-stu-id="95b5b-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="95b5b-136">方法</span><span class="sxs-lookup"><span data-stu-id="95b5b-136">Methodology</span></span>

<span data-ttu-id="95b5b-137">过去，通常很难开发和部署人工智能 (AI) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="95b5b-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="95b5b-138">此流程需要一支由数据科学家、主题专家 (SME) 和工程师组成的团队长时间工作，以制定、开发、部署和维护可用的 AI 解决方案。</span><span class="sxs-lookup"><span data-stu-id="95b5b-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="95b5b-139">客户付款预测有助于在 Microsoft Dynamics 365 Finance 中部署和使用 AI 解决方案。</span><span class="sxs-lookup"><span data-stu-id="95b5b-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="95b5b-140">Microsoft 正在预打包基于 Microsoft AI Builder 构建的 AI 解决方案。</span><span class="sxs-lookup"><span data-stu-id="95b5b-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="95b5b-141">因此，用户只需单击一下鼠标即可部署 AI 解决方案，以利用智能预测的优势。</span><span class="sxs-lookup"><span data-stu-id="95b5b-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="95b5b-142">如果您对预测的准确性不满意，那么高级用户可以（再次强调，只需单击一次鼠标）进入 AI Builder 扩展体验，然后选择或清除用于生成预测的字段。</span><span class="sxs-lookup"><span data-stu-id="95b5b-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="95b5b-143">准备就绪后，您可以“训练”模型并发布更改。</span><span class="sxs-lookup"><span data-stu-id="95b5b-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="95b5b-144">将在 Dynamics 365 Finance 中自动选取新训练的模型以生成预测。</span><span class="sxs-lookup"><span data-stu-id="95b5b-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="95b5b-145">发布详细信息</span><span class="sxs-lookup"><span data-stu-id="95b5b-145">Release details</span></span>

<span data-ttu-id="95b5b-146">Finance Insights 公开预览版可用于美国、欧洲和英国的试用部署。</span><span class="sxs-lookup"><span data-stu-id="95b5b-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="95b5b-147">Microsoft 将逐渐增加对更多地区的支持。</span><span class="sxs-lookup"><span data-stu-id="95b5b-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="95b5b-148">应该仅在第 2 层沙盒环境中启用公开预览版功能。</span><span class="sxs-lookup"><span data-stu-id="95b5b-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="95b5b-149">在沙盒环境中创建的设置和 AI 模型可能不能迁移到生产环境。</span><span class="sxs-lookup"><span data-stu-id="95b5b-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="95b5b-150">有关详细信息，请参阅 [Microsoft Dynamics 365 Previews 补充使用条款](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms)。</span><span class="sxs-lookup"><span data-stu-id="95b5b-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="95b5b-151">隐私声明</span><span class="sxs-lookup"><span data-stu-id="95b5b-151">Privacy notice</span></span>

<span data-ttu-id="95b5b-152">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="95b5b-152">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
