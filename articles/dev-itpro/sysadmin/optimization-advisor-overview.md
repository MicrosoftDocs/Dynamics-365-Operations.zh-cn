---
title: 优化顾问概览
description: 此主题描述如何使用优化顾问来帮助保证 Microsoft Dynamics 365 Finance and Operations 的最佳配置。
author: roxanadiaconu
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a58990363003aec115e342925921f2171999b3b9
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864224"
---
# <a name="optimization-advisor-overview"></a><span data-ttu-id="52b7a-103">优化顾问概览</span><span class="sxs-lookup"><span data-stu-id="52b7a-103">Optimization advisor overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52b7a-104">此主题描述如何使用优化顾问来帮助保证 Microsoft Dynamics 365 Finance and Operations 的最佳配置。</span><span class="sxs-lookup"><span data-stu-id="52b7a-104">This topic describes how you can use Optimization advisor to help guarantee optimal configuration of Microsoft Dynamics 365 Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="52b7a-105">概览</span><span class="sxs-lookup"><span data-stu-id="52b7a-105">Overview</span></span>

<span data-ttu-id="52b7a-106">模块的不正确配置和设置可能对 Finance and Operations 功能的可用性、系统性能和业务流程的顺畅使用造成负面影响。</span><span class="sxs-lookup"><span data-stu-id="52b7a-106">Incorrect configuration and setup of a module can adversely affect the availability of features in Finance and Operations, system performance, and the smooth operation of business processes.</span></span> <span data-ttu-id="52b7a-107">业务数据的质量（例如，数据的正确性、完整性和清洁）还会影响系统性能，以及组织的决策制定能力和效率等。</span><span class="sxs-lookup"><span data-stu-id="52b7a-107">The quality of business data (for example, the correctness, completeness, and cleanliness of the data) also affects system performance, and an organization's decision-making capabilities, productivity, and so on.</span></span>

<span data-ttu-id="52b7a-108">**优化顾问**工作区是一个工具，让高级用户、业务分析师、功能顾问和 IT 支持职能部门发现模块配置和业务数据中的问题。</span><span class="sxs-lookup"><span data-stu-id="52b7a-108">The **Optimization advisor** workspace is a tool that lets power users, business analysts, functional consultants, and IT support functions identify issues in module configuration and business data.</span></span> <span data-ttu-id="52b7a-109">优化顾问建议模块配置的最佳实践并确定废弃或不正确的业务数据。</span><span class="sxs-lookup"><span data-stu-id="52b7a-109">Optimization advisor suggests best practices for module configuration and identifies business data that is obsolete or incorrect.</span></span>

<span data-ttu-id="52b7a-110">优化顾问会定期运行一组最佳实践规则。</span><span class="sxs-lookup"><span data-stu-id="52b7a-110">Optimization advisor periodically runs a set of best practice rules.</span></span> <span data-ttu-id="52b7a-111">有一组默认规则随 Microsoft Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）一起发布。</span><span class="sxs-lookup"><span data-stu-id="52b7a-111">A default set of rules is released together with Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="52b7a-112">但是，用户也可以创建特定于其自定义、来自独立软件供应商 (ISV) 的解决方案和业务数据的规则。</span><span class="sxs-lookup"><span data-stu-id="52b7a-112">However, users can also create rules that are specific to their customizations, solutions from independent software vendors (ISVs), and business data.</span></span> <span data-ttu-id="52b7a-113">有关如何创建规则的详细信息，请参阅[创建新规则](./create-rules-optimization-advisor.md)。</span><span class="sxs-lookup"><span data-stu-id="52b7a-113">For more information about how to create rules, see [Create new rules](./create-rules-optimization-advisor.md).</span></span>

<span data-ttu-id="52b7a-114">在检测到违反规则时，优化机会将生成并显示在**优化顾问**工作区中。</span><span class="sxs-lookup"><span data-stu-id="52b7a-114">When a violation of a rule is detected, an optimization opportunity is generated and appears in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="52b7a-115">用户可以直接从**优化顾问**工作区采取适当的纠正措施。</span><span class="sxs-lookup"><span data-stu-id="52b7a-115">A user can take appropriate corrective action directly from the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="52b7a-116">机会可以是公司特定或跨公司的，具体取决于所验证的设置和数据的类型。</span><span class="sxs-lookup"><span data-stu-id="52b7a-116">Opportunities can be company-specific or cross-company, depending on the type of setup and data that is being validated.</span></span> <span data-ttu-id="52b7a-117">跨公司机会可以从所有公司查看。</span><span class="sxs-lookup"><span data-stu-id="52b7a-117">Cross-company opportunities can be viewed from all companies.</span></span> <span data-ttu-id="52b7a-118">若要查看特定公司的机会，必须首先选择公司。</span><span class="sxs-lookup"><span data-stu-id="52b7a-118">To view the opportunities for a specific company, you must first select the company.</span></span>

<span data-ttu-id="52b7a-119">优化机会应用标准安全政策。</span><span class="sxs-lookup"><span data-stu-id="52b7a-119">Standard security policies apply to optimization opportunities.</span></span> <span data-ttu-id="52b7a-120">例如，与**仓库管理**模块的配置相关的优化机会仅对有权访问“仓库管理”且可以更改其设置的用户可见。</span><span class="sxs-lookup"><span data-stu-id="52b7a-120">For example, the optimization opportunities that are related to configuration of the **Warehouse management** module are visible only to users who have access to Warehouse management and can change its setup.</span></span>

<span data-ttu-id="52b7a-121">当您对一些优化机会采取行动时，系统将计算机会对业务流程运行时间减少的影响。</span><span class="sxs-lookup"><span data-stu-id="52b7a-121">When you take action on some optimization opportunities, the system calculates the impact of the opportunity in terms of the reduction in the runtime of business processes.</span></span> <span data-ttu-id="52b7a-122">很遗憾，此功能不能用于所有优化机会。</span><span class="sxs-lookup"><span data-stu-id="52b7a-122">Unfortunately, this feature isn't available for all optimization opportunities.</span></span>

<span data-ttu-id="52b7a-123">若要了解有关“优化顾问”的详细信息，请观看视频短片 [Dynamics 365 for Finance and Operations 中的优化顾问](https://www.youtube.com/watch?v=MRsAzgFCUSQ)。</span><span class="sxs-lookup"><span data-stu-id="52b7a-123">To learn more about Optimization advisor, watch the short [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ) video.</span></span>

## <a name="optimization-rules"></a><span data-ttu-id="52b7a-124">优化规则</span><span class="sxs-lookup"><span data-stu-id="52b7a-124">Optimization rules</span></span>

<span data-ttu-id="52b7a-125">要查看优化顾问规则的完整列表并了解规则的评估频率，请转到**系统管理** &gt; **定期任务** &gt; **维护诊断验证规则**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-125">To view the complete list of Optimization advisor rules and to see how often the rules are evaluated, go to **System administration** &gt; **Periodic tasks** &gt; **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="52b7a-126">仅对具有**活动**状态的规则进行评估。</span><span class="sxs-lookup"><span data-stu-id="52b7a-126">Only rules that have a status of **Active** are evaluated.</span></span> <span data-ttu-id="52b7a-127">评估频率可以设置为**每日**、**每周**、**每月**或**未计划**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-127">The evaluation frequency can be set to **Daily**, **Weekly**, **Monthly**, or **Unscheduled**.</span></span>

<span data-ttu-id="52b7a-128">若要触发对未计划规则的评估，或在预定义的计划外重新评估定期规则，转到**系统管理** &gt; **定期任务** &gt; **计划诊断验证规则**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-128">To trigger the evaluation of unscheduled rules, or to reevaluate periodic rules outside their predefined schedule, go to **System administration** &gt; **Periodic tasks** &gt; **Schedule diagnostics validation rule**.</span></span> <span data-ttu-id="52b7a-129">然后，在**诊断规则验证**对话框中，选择评估频率。</span><span class="sxs-lookup"><span data-stu-id="52b7a-129">Then, in the **Diagnostic rule validation** dialog box, select an evaluation frequency.</span></span> <span data-ttu-id="52b7a-130">具有指定频率的所有规则都将重新评估。</span><span class="sxs-lookup"><span data-stu-id="52b7a-130">All rules that have the specified frequency will be reevaluated.</span></span>

<span data-ttu-id="52b7a-131">当前的优化规则设置可划分为以下几个类别。</span><span class="sxs-lookup"><span data-stu-id="52b7a-131">The current set of optimization rules can be divided into the following categories.</span></span>

### <a name="module-configuration-and-setup"></a><span data-ttu-id="52b7a-132">模块配置和设置</span><span class="sxs-lookup"><span data-stu-id="52b7a-132">Module configuration and setup</span></span>

<span data-ttu-id="52b7a-133">仓库管理设置是一个复杂的过程。</span><span class="sxs-lookup"><span data-stu-id="52b7a-133">The setup of Warehouse management is a complicated process.</span></span> <span data-ttu-id="52b7a-134">为了让这个过程更简单，引入了某些规则来帮助验证设置的正确性。</span><span class="sxs-lookup"><span data-stu-id="52b7a-134">To make the process easier, some rules have been introduced to help validate the correctness of the setup.</span></span> <span data-ttu-id="52b7a-135">例如，有一个规则验证销售订单和转移单的固定产品变型位置的仓库库位指令的设置。</span><span class="sxs-lookup"><span data-stu-id="52b7a-135">For example, one rule validates the setup of warehouse location directives for fixed product variant locations for sales orders and transfer orders.</span></span>

<span data-ttu-id="52b7a-136">此外，某些规则检查是否实际使用了已启用的功能。</span><span class="sxs-lookup"><span data-stu-id="52b7a-136">Additionally, some rules check whether features that have been enabled are actually used.</span></span> <span data-ttu-id="52b7a-137">例如，有一个规则确定您是否在使用**主计划**模块。</span><span class="sxs-lookup"><span data-stu-id="52b7a-137">For example, one rule determines whether you're using the **Master planning** module.</span></span> <span data-ttu-id="52b7a-138">如果规则确定您未使用此模块，优化机会将生成以建议您关闭计划流程。</span><span class="sxs-lookup"><span data-stu-id="52b7a-138">If the rule determines that you aren't using the module, an optimization opportunity is generated to suggest that you turn off the planning processes.</span></span>

### <a name="system-configuration"></a><span data-ttu-id="52b7a-139">系统配置</span><span class="sxs-lookup"><span data-stu-id="52b7a-139">System configuration</span></span>

<span data-ttu-id="52b7a-140">如果未使用由 Configuration Key 控制的特定功能，优化机会将生成以建议您禁用 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="52b7a-140">If specific functionality that is controlled by a configuration key isn't used, an optimization opportunity is generated to suggest that you disable the configuration key.</span></span> <span data-ttu-id="52b7a-141">Configuration Key 的示例包括**实际称重**、**预算计划**、**项目**和**核准供应商列表**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-141">Examples of configuration keys include **Catch weight**, **Budget planning**, **Project**, and **Approved vendor list**.</span></span>

### <a name="business-data-consistency-and-cleanup"></a><span data-ttu-id="52b7a-142">业务数据的一致性和清理</span><span class="sxs-lookup"><span data-stu-id="52b7a-142">Business data consistency and cleanup</span></span>

<span data-ttu-id="52b7a-143">如果主数据不正确（例如，如果您有未定义单位的度量单位转换，或者您有除以 0 \[零\] 的度量单位转换），优化机会将生成以建议您更正数据。</span><span class="sxs-lookup"><span data-stu-id="52b7a-143">If master data isn't correct (for example, if you have unit of measure conversions for units that haven't been defined, or if you have unit of measure conversions that have a division by 0 \[zero\]), an optimization opportunity is generated to suggest that you correct the data.</span></span> 

<span data-ttu-id="52b7a-144">如果您的批处理作业历史记录条目、废弃项目、已启用仓库物料的关闭的现有条目等太多，或者如果这些条目和项目过旧，优化机会将生成以建议您清理数据。</span><span class="sxs-lookup"><span data-stu-id="52b7a-144">If you have too many batch job history entries, obsolete items, closed on-hand entries for warehouse enabled items, and so on, or if those entries and items are too old, optimization opportunities are generated to suggest that you clean up the data.</span></span> <span data-ttu-id="52b7a-145">通过保持数据的清洁，您可以帮助改善整个系统的性能。</span><span class="sxs-lookup"><span data-stu-id="52b7a-145">By keeping your data clean, you can help improve overall system performance.</span></span>

### <a name="best-practices"></a><span data-ttu-id="52b7a-146">最佳实践</span><span class="sxs-lookup"><span data-stu-id="52b7a-146">Best practices</span></span>

<span data-ttu-id="52b7a-147">如果您未根据最佳实践运行某些业务流程（例如，如果您在库存结转之前运行库存预结转，或者，如果您为子分类帐日记帐批处理转移使用计划的批处理），优化机会会通知您最佳实践并要求您照其执行。</span><span class="sxs-lookup"><span data-stu-id="52b7a-147">If you aren't running some business processes according to best practices (for example, if you run inventory pre-closing before the inventory is closed, or if you use the scheduled batch for subledger journal batch transfer), optimization opportunities inform you about the best practice and ask that you follow it.</span></span>

## <a name="optimization-opportunities"></a><span data-ttu-id="52b7a-148">优化机会</span><span class="sxs-lookup"><span data-stu-id="52b7a-148">Optimization opportunities</span></span>

<span data-ttu-id="52b7a-149">若要查看在优化规则评估时创建的优化机会，打开**优化顾问**工作区。</span><span class="sxs-lookup"><span data-stu-id="52b7a-149">To view the optimization opportunities that are generated during the evaluation of optimization rules, open the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="52b7a-150">在此工作区，您可以通过选择**更多信息**查看与机会有关的详细信息。</span><span class="sxs-lookup"><span data-stu-id="52b7a-150">In this workspace, you can view more information about an opportunity by selecting **More information**.</span></span> <span data-ttu-id="52b7a-151">如果您希望系统采取措施、更正设置、清洁数据等，以便您无需自己打开相应页面，选择**采取措施**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-151">If you want the system to take action and correct the setup, clean the data, and so on, so that you don't have to open the corresponding pages yourself, select **Take action**.</span></span>

<span data-ttu-id="52b7a-152">优化机会没有工作流。</span><span class="sxs-lookup"><span data-stu-id="52b7a-152">There is no workflow for optimization opportunities.</span></span> <span data-ttu-id="52b7a-153">在您选择**采取措施**或使用**更多信息**对话框中提供的导航路径后，优化机会将从列表中消失。</span><span class="sxs-lookup"><span data-stu-id="52b7a-153">After you select **Take action** or use a navigation path that is provided in the **More information** dialog box, the optimization opportunity disappears from the list.</span></span> <span data-ttu-id="52b7a-154">如果该更正操作未完全解决问题，机会将在下次评估规则时再次生成。</span><span class="sxs-lookup"><span data-stu-id="52b7a-154">If the corrective action doesn't completely resolve an issue, the opportunity will be generated again the next time that the rule is evaluated.</span></span>

<span data-ttu-id="52b7a-155">如果机会不适用于您的角色，您可以选择**从我的列表中隐藏**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-155">If an opportunity doesn't apply to your role, you can select **Hide from my list**.</span></span> <span data-ttu-id="52b7a-156">即使此机会背后的规则后以后再次触发，您也不会在您的列表中看到此机会。</span><span class="sxs-lookup"><span data-stu-id="52b7a-156">Even if the rule behind this opportunity is triggered again later, you won't see the opportunity in your list.</span></span>

<span data-ttu-id="52b7a-157">若要禁用特定规则的评估，选择由规则生成的机会，然后选择**禁用分析**。</span><span class="sxs-lookup"><span data-stu-id="52b7a-157">To deactivate the evaluation of specific rules, select the opportunity that was generated by the rule, and then select **Deactivate analysis**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52b7a-158">其他资源</span><span class="sxs-lookup"><span data-stu-id="52b7a-158">Additional resources</span></span>

[<span data-ttu-id="52b7a-159">创建新规则</span><span class="sxs-lookup"><span data-stu-id="52b7a-159">Create new rules</span></span>](./create-rules-optimization-advisor.md)

[<span data-ttu-id="52b7a-160">Dynamics 365 for Finance and Operations 中的优化顾问（视频）</span><span class="sxs-lookup"><span data-stu-id="52b7a-160">Optimization advisor in Dynamics 365 for Finance and Operations (Video)</span></span>](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
