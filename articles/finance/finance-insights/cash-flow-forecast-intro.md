---
title: 现金流预测(预览版)
description: 本主题描述现金流预测功能。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645240"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="4c069-103">现金流预测(预览版)</span><span class="sxs-lookup"><span data-stu-id="4c069-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4c069-104">现金流对任何业务都至关重要。</span><span class="sxs-lookup"><span data-stu-id="4c069-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="4c069-105">即使盈利的公司如果不保持现金流来满足眼前的需求，他们也可能面临破产。</span><span class="sxs-lookup"><span data-stu-id="4c069-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="4c069-106">Finance insights 中的现金流预测功能可帮助公司有效地监控和管理其现金余额。</span><span class="sxs-lookup"><span data-stu-id="4c069-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="4c069-107">此功能使用机器学习来帮助企业比以前更准确地预测现金流。</span><span class="sxs-lookup"><span data-stu-id="4c069-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="4c069-108">还可以帮助经理制定决策，以根据其当前的现金状况来优化商机。</span><span class="sxs-lookup"><span data-stu-id="4c069-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="4c069-109">对于大多数公司而言，管理现金流和进行现金流预测是一个繁琐、重复且手动的过程。</span><span class="sxs-lookup"><span data-stu-id="4c069-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="4c069-110">大多数公司依靠的 Microsoft Excel 解决方案的复杂程度各异。</span><span class="sxs-lookup"><span data-stu-id="4c069-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="4c069-111">准确预测现金流的挑战包括：</span><span class="sxs-lookup"><span data-stu-id="4c069-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="4c069-112">决策者无法使用数据，因为数据分散在多个地方，包括：</span><span class="sxs-lookup"><span data-stu-id="4c069-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="4c069-113">会计或企业资源计划系统</span><span class="sxs-lookup"><span data-stu-id="4c069-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="4c069-114">财务计划软件</span><span class="sxs-lookup"><span data-stu-id="4c069-114">Financial planning software</span></span>
  - <span data-ttu-id="4c069-115">Excel</span><span class="sxs-lookup"><span data-stu-id="4c069-115">Excel</span></span>
  - <span data-ttu-id="4c069-116">其他软件应用程序</span><span class="sxs-lookup"><span data-stu-id="4c069-116">Additional software applications</span></span> 
- <span data-ttu-id="4c069-117">预测基于每个领域或部门内“孤岛”中的内部知识。</span><span class="sxs-lookup"><span data-stu-id="4c069-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="4c069-118">财务实现后，衡量现金流预测的准确性不确定且困难。</span><span class="sxs-lookup"><span data-stu-id="4c069-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="4c069-119">现金流预测功能的详细信息</span><span class="sxs-lookup"><span data-stu-id="4c069-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="4c069-120">现金流预测功能包括以下功能。</span><span class="sxs-lookup"><span data-stu-id="4c069-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="4c069-121">轻松将来自外部系统的现金流数据集成到 Dynamics 365 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="4c069-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="4c069-122">现金流预测也可以使用数据导入-导出框架。</span><span class="sxs-lookup"><span data-stu-id="4c069-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="4c069-123">该框架使与 Excel OData 的集成变得容易。</span><span class="sxs-lookup"><span data-stu-id="4c069-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="4c069-124">您还可以合并来自多个来源的数据以创建全面的现金流解决方案。</span><span class="sxs-lookup"><span data-stu-id="4c069-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="4c069-125">介绍智能现金头寸。</span><span class="sxs-lookup"><span data-stu-id="4c069-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="4c069-126">根据客户的付款行为创建现金头寸，以预测公司何时可以期望现金进入其帐户。</span><span class="sxs-lookup"><span data-stu-id="4c069-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="4c069-127">它还分析了付款供应商的历史模式，以预测何时可能会支付将来的发票和订单。</span><span class="sxs-lookup"><span data-stu-id="4c069-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="4c069-128">通过与 AI Builder 的自动集成使用时间序列预测，引入了用于长期预测的智能现金流预测。</span><span class="sxs-lookup"><span data-stu-id="4c069-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="4c069-129">提供保存特定现金流头寸或预测，对其进行编辑，然后轻松地将其与实际财务状况进行比较和衡量预测性能的功能。</span><span class="sxs-lookup"><span data-stu-id="4c069-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="4c069-130">通过快照比较启用假设分析。</span><span class="sxs-lookup"><span data-stu-id="4c069-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="4c069-131">例如，您可以创建代表快照的最乐观、最悲观和最现实的快照，然后比较并查看差异。</span><span class="sxs-lookup"><span data-stu-id="4c069-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="4c069-132">提供查看法人中多种货币的现金流预测以及筛选和查看与银行帐户相关的现金流的功能。</span><span class="sxs-lookup"><span data-stu-id="4c069-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="4c069-133">使您可以筛选和查看与财务维度相关的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="4c069-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="4c069-134">Dynamics 365 Finance 中的现金流预测功能将使您的组织能够将繁琐、复杂但重复的现金流预测转换为简单的自动化流程。</span><span class="sxs-lookup"><span data-stu-id="4c069-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="4c069-135">自动化现金流预测的最繁琐的方面，使您可以专注于关键决策，以实现期望的业务成果。</span><span class="sxs-lookup"><span data-stu-id="4c069-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="4c069-136">设置现金流预测的维度</span><span class="sxs-lookup"><span data-stu-id="4c069-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="4c069-137">**现金流预测设置** 页上的一个新选项卡可让您控制使用财务维度在 **现金流预测** 工作区中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="4c069-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="4c069-138">仅当启用现金流预测功能后，此选项卡才会出现。</span><span class="sxs-lookup"><span data-stu-id="4c069-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="4c069-139">在 **维度** 选项卡上，从要用于筛选的维度列表中进行选择，然后使用箭头键将其移至右侧列。</span><span class="sxs-lookup"><span data-stu-id="4c069-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="4c069-140">只能选择两个维度来筛选现金流预测数据。</span><span class="sxs-lookup"><span data-stu-id="4c069-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="4c069-141">隐私声明</span><span class="sxs-lookup"><span data-stu-id="4c069-141">Privacy notice</span></span>
<span data-ttu-id="4c069-142">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="4c069-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
