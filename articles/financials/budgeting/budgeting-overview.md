---
title: "预算编制主页"
description: "此主题概要介绍了 Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 中的预算编制功能组件、预算编制工具和申报功能。"
author: twheeloc
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 953c79b134b82ce2a3e0adc05dc3bdf3ce583482
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="budgeting-home-page"></a><span data-ttu-id="85e40-103">预算编制主页</span><span class="sxs-lookup"><span data-stu-id="85e40-103">Budgeting home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85e40-104">此主题概要介绍了 Finance and Operations 中的预算编制功能组件、预算编制工具和申报功能。</span><span class="sxs-lookup"><span data-stu-id="85e40-104">This topic provides an overview of the budgeting functionality components, budgeting tools, and reporting capabilities in Finance and Operations.</span></span> 

<a name="components-of-budgeting-functionality"></a><span data-ttu-id="85e40-105">预算功能组件</span><span class="sxs-lookup"><span data-stu-id="85e40-105">Components of budgeting functionality</span></span>
-------------------------------------

<span data-ttu-id="85e40-106">公司的资源计划周期通常包含计划、预算和预测活动。</span><span class="sxs-lookup"><span data-stu-id="85e40-106">The resource planning cycle for a company typically consists of planning, budgeting, and forecasting activities.</span></span>

<span data-ttu-id="85e40-107">[![预算功能组件](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)</span><span class="sxs-lookup"><span data-stu-id="85e40-107">[![Budgeting functionality components](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)</span></span>

<span data-ttu-id="85e40-108">长期战略计划和年度预算计划的流程均通过预算计划文档来获得支持。</span><span class="sxs-lookup"><span data-stu-id="85e40-108">The processes for both long-term strategic planning and annual budget planning are supported through a budget plan document.</span></span> <span data-ttu-id="85e40-109">预算计划文档与 Microsoft Excel 紧密集成在一起。</span><span class="sxs-lookup"><span data-stu-id="85e40-109">Budget plan documents are tightly integrated with Microsoft Excel.</span></span> <span data-ttu-id="85e40-110">用户可配置无数个货币和数量方案，也可以定义一个预算组织层次结构以支持自上而下和自下而上的预算方法。</span><span class="sxs-lookup"><span data-stu-id="85e40-110">Users can configure unlimited monetary and quantitative scenarios, and can also define a budgeting organizational hierarchy to both support top-down and bottom-up budgeting methods.</span></span> <span data-ttu-id="85e40-111">在 Finance and Operations 中建立和审核预算之后，将预算计划转换为预算登记分录。</span><span class="sxs-lookup"><span data-stu-id="85e40-111">After a budget is established and approved in Finance and Operations, you convert the budget plan to a budget register entry.</span></span> <span data-ttu-id="85e40-112">预算登记分录提供了用于维护预算以及通过预算代码保持金额的可追溯性的工具。</span><span class="sxs-lookup"><span data-stu-id="85e40-112">Budget register entries provide tools for maintaining the budget and for keeping amounts traceable through budget codes.</span></span> <span data-ttu-id="85e40-113">预算登记分录可让您修订原始预算、执行转移和从上一年结转预算金额。</span><span class="sxs-lookup"><span data-stu-id="85e40-113">Budget register entries let you revise original budgets, perform transfers, and carry forward budget amounts from the previous year.</span></span> <span data-ttu-id="85e40-114">根据建立的预算，公司可启用预算控制。</span><span class="sxs-lookup"><span data-stu-id="85e40-114">Based on the established budget, a company can enable budget control.</span></span> <span data-ttu-id="85e40-115">控制的级别取决于组织文化和组织的成熟度级别。</span><span class="sxs-lookup"><span data-stu-id="85e40-115">The level of control depends on the organizational culture and the organization's level of maturity.</span></span> <span data-ttu-id="85e40-116">成熟度较低的组织可能将预算保留“原样”，当预算未达到预期时，它们可能更多的是被动地响应，而不是主动采取措施。</span><span class="sxs-lookup"><span data-stu-id="85e40-116">Organizations that have low maturity might leave the budget “as is” and might be more reactive than proactive if a budget doesn't meet expectations.</span></span> <span data-ttu-id="85e40-117">其他组织可能会启用预算控制策略以防止用户在没有预算资金时进行采购。</span><span class="sxs-lookup"><span data-stu-id="85e40-117">Other organizations might enable budget control policies that prevent users from purchasing if budget funds aren't available.</span></span>

<span data-ttu-id="85e40-118">最后，非常成熟的组织可能会建立一种组织文化，在这种文化中，员工将获得有关组织目标的培训，并通过“考虑在线会议而不是出差”之类的策略实现这些目标。</span><span class="sxs-lookup"><span data-stu-id="85e40-118">Finally, very mature organizations might establish an organizational culture where employees are educated about organizational targets and follow those targets through policies such as “Consider online meeting instead of a travel.”</span></span> <span data-ttu-id="85e40-119">Finance and Operations 包含让公司的管理层选择硬控制（防止超过预算的过帐）或软控制（用户将收到超过可用预算资金的警告，但用户可以自行决定如何继续）的预算控制框架。</span><span class="sxs-lookup"><span data-stu-id="85e40-119">Finance and Operations includes a budget control framework that lets the company's management select either hard control (which prevents postings that would go over the budget) or soft control (where users are warned that they will exceed the available budget funds but can decide for themselves how to proceed).</span></span> <span data-ttu-id="85e40-120">最后，您可使用滚动预测。</span><span class="sxs-lookup"><span data-stu-id="85e40-120">Finally, you can use rolling forecasts.</span></span> <span data-ttu-id="85e40-121">滚动预测是预算与实际支出的定期比较，用于确定公司的预算执行状况。</span><span class="sxs-lookup"><span data-stu-id="85e40-121">A rolling forecast is a regular comparison of budget to actuals and is used to define how well the company operates against the budget.</span></span> <span data-ttu-id="85e40-122">滚动预测还用于确定趋势。</span><span class="sxs-lookup"><span data-stu-id="85e40-122">A rolling forecast is also used to identify trends.</span></span> <span data-ttu-id="85e40-123">在 Finance and Operations 中，滚动预测通过在初始规划活动中制定的预算计划文档来获得支持。</span><span class="sxs-lookup"><span data-stu-id="85e40-123">In Finance and Operations, rolling forecasts are supported, through a budget plan document, as initial planning activities.</span></span> <span data-ttu-id="85e40-124">滚动预测可以与针对即将到来的预算周期的规划并行执行。</span><span class="sxs-lookup"><span data-stu-id="85e40-124">Rolling forecasts can be done in parallel with the planning for the upcoming budget cycle.</span></span>

-   [<span data-ttu-id="85e40-125">基本预算编制：概述和配置</span><span class="sxs-lookup"><span data-stu-id="85e40-125">Basic budgeting: Overview and configuration</span></span>](basic-budgeting-overview-configuration.md)
-   [<span data-ttu-id="85e40-126">预算控制：概述和配置</span><span class="sxs-lookup"><span data-stu-id="85e40-126">Budget control: Overview and configuration</span></span>](budget-control-overview-configuration.md)
-   [<span data-ttu-id="85e40-127">预算计划：概述和配置</span><span class="sxs-lookup"><span data-stu-id="85e40-127">Budget planning: Overview and configuration</span></span>](budget-planning-overview-configuration.md)
-   [<span data-ttu-id="85e40-128">职位预测</span><span class="sxs-lookup"><span data-stu-id="85e40-128">Position forecasting</span></span>](position-forecasting.md)
-   [<span data-ttu-id="85e40-129">预算计划证明文档</span><span class="sxs-lookup"><span data-stu-id="85e40-129">Budget planning justification documents</span></span>](budget-planning-justification-docs.md)
-   [<span data-ttu-id="85e40-130">适用于预算计划的 Microsoft Excel 模板</span><span class="sxs-lookup"><span data-stu-id="85e40-130">Microsoft Excel templates for budget planning</span></span>](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-finance-and-operations"></a><span data-ttu-id="85e40-131">Finance and Operations 中的预算工具</span><span class="sxs-lookup"><span data-stu-id="85e40-131">Budgeting tools in Finance and Operations</span></span>
<span data-ttu-id="85e40-132">[![预算工具](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg)</span><span class="sxs-lookup"><span data-stu-id="85e40-132">[![Budgeting tools](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg)</span></span> 

<span data-ttu-id="85e40-133">其他计划和预算功能跨 Finance and Operations 提供，并且与分类帐预算集成在一起。</span><span class="sxs-lookup"><span data-stu-id="85e40-133">Additional planning and budgeting capabilities are available across Finance and Operations and are integrated with ledger budgets.</span></span>

-   <span data-ttu-id="85e40-134">**劳动力预算** - 劳动力预算包括针对职位、薪酬组等方面的详细的预算成本构成计划。</span><span class="sxs-lookup"><span data-stu-id="85e40-134">**Workforce budgets** – Workforce budgeting includes detailed budget cost component planning for positions, compensation groups, and so on.</span></span>
-   <span data-ttu-id="85e40-135">**固定资产预算** - 基于固定资产信息，您可以计算计划的折旧并记录其他与固定资产相关的计划交易记录。</span><span class="sxs-lookup"><span data-stu-id="85e40-135">**Fixed assets budgets** – Based on fixed asset information, you can calculate planned depreciation and record other planned transactions that are related to fixed assets.</span></span>
-   <span data-ttu-id="85e40-136">**项目预算** – 在项目模块中，可以创建详细的项目预测。</span><span class="sxs-lookup"><span data-stu-id="85e40-136">**Project budgets** – In the projects module, you can create detailed project forecasts.</span></span> <span data-ttu-id="85e40-137">项目预测将包括有关计划的工时、支出、费用和物料的详细信息。</span><span class="sxs-lookup"><span data-stu-id="85e40-137">The projects forecasts will include details about the planned hours, expenses, fees, and items.</span></span>
-   <span data-ttu-id="85e40-138">**需求预测** - 基于历史交易记录数据，您可以预估未来库存需求并创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="85e40-138">**Demand forecasting **– Based on historical transaction data, you can estimate future inventory demand and create demand forecasts.</span></span>

<span data-ttu-id="85e40-139">有关如何将计划数据从其他模板放入预算计划的信息，请参阅[预算计划与其他模块的集成](budget-planning-integration-other-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="85e40-139">For information about how to bring planning data from other modules into budget plans, see [Budget planning integration with other modules](budget-planning-integration-other-modules.md).</span></span>

## <a name="user-interface-and-reporting-capabilities"></a><span data-ttu-id="85e40-140">用户界面和报告功能</span><span class="sxs-lookup"><span data-stu-id="85e40-140">User interface and reporting capabilities</span></span>
<span data-ttu-id="85e40-141">在 Finance and Operations 中，用户可以直接在 Finance and Operations 客户端中创建预算计划（通过使用可配置预算计划文档页），也可以通过 Excel 创建预算计划。</span><span class="sxs-lookup"><span data-stu-id="85e40-141">In Finance and Operations, users can create budget plans either directly in the Finance and Operations client (by using a configurable budget plan document page) or through Excel.</span></span> <span data-ttu-id="85e40-142">Excel 提供了几个额外功能。</span><span class="sxs-lookup"><span data-stu-id="85e40-142">Excel provides several additional capabilities.</span></span> <span data-ttu-id="85e40-143">例如，您可以使用外部数据作为预算计划的来源，执行自定义计算，并使用 Microsoft 数据透视表和图表。</span><span class="sxs-lookup"><span data-stu-id="85e40-143">For example, you can use external data as a source for a budget plan, do custom calculations, and use Microsoft PivotTable and charts.</span></span> <span data-ttu-id="85e40-144">预算计划流程中的大多数变量都可配置。</span><span class="sxs-lookup"><span data-stu-id="85e40-144">Most of the variables in the budget planning process can be configured.</span></span> 

<span data-ttu-id="85e40-145">例如，您可以定义执行预算的人员、预算的对象以及具体流程。</span><span class="sxs-lookup"><span data-stu-id="85e40-145">For example, you can define who does budgeting, what is budgeted, and what the process looks like.</span></span> <span data-ttu-id="85e40-146">尽管您可以使用 Excel 进行预算计划，但 Finance and Operations 仍将作为唯一的数据来源，帮助防止预算控制问题。</span><span class="sxs-lookup"><span data-stu-id="85e40-146">Although you can use Excel for budget planning, Finance and Operations is kept as a single source of truth and helps prevent budget control issues.</span></span> <span data-ttu-id="85e40-147">周期性流程可用于将预算的初始数据纳入预算计划。</span><span class="sxs-lookup"><span data-stu-id="85e40-147">Periodic processes can be used to bring initial data for budgeting into the budget plan.</span></span> <span data-ttu-id="85e40-148">对于报告，Finance and Operations 提供了一系列标准查询页，供您查看和分析预算数据。</span><span class="sxs-lookup"><span data-stu-id="85e40-148">For reporting, Finance and Operations offers a set of standard inquiry pages that let you view and analyze budgeting data.</span></span> <span data-ttu-id="85e40-149">预算计划数据可通过 Management Reporter 访问，单独的预算计划方案可在 Management Reporter 报告中显示为列。</span><span class="sxs-lookup"><span data-stu-id="85e40-149">Budget plan data can be accessed through Management Reporter, and separate budget plan scenarios can be displayed as columns on the Management Reporter report.</span></span>







