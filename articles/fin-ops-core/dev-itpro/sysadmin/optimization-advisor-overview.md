---
title: 优化顾问概览
description: 此主题描述了如何使用优化顾问来帮助确保 Finance and Operations 的最佳配置。
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
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 25ca62466c00b038e0d7e1758fd4f13f776cb2f0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982544"
---
# <a name="optimization-advisor-overview"></a><span data-ttu-id="51be1-103">优化顾问概览</span><span class="sxs-lookup"><span data-stu-id="51be1-103">Optimization advisor overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51be1-104">此主题描述了如何使用优化顾问来帮助确保 Finance and Operations 的最佳配置。</span><span class="sxs-lookup"><span data-stu-id="51be1-104">This topic describes how you can use Optimization advisor to help ensure optimal configuration of Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="51be1-105">概览</span><span class="sxs-lookup"><span data-stu-id="51be1-105">Overview</span></span>

<span data-ttu-id="51be1-106">模块的不正确配置和设置可能对应用程序功能的可用性、系统性能和业务流程的顺畅使用造成负面影响。</span><span class="sxs-lookup"><span data-stu-id="51be1-106">Incorrect configuration and setup of a module can adversely affect the availability of application features, system performance, and the smooth operation of business processes.</span></span> <span data-ttu-id="51be1-107">业务数据的质量（例如，数据的正确性、完整性和清洁）还会影响系统性能，以及组织的决策制定能力和效率等。</span><span class="sxs-lookup"><span data-stu-id="51be1-107">The quality of business data (for example, the correctness, completeness, and cleanliness of the data) also affects system performance, and an organization's decision-making capabilities, productivity, and so on.</span></span>

<span data-ttu-id="51be1-108">**优化顾问**工作区是一个工具，让高级用户、业务分析师、功能顾问和 IT 支持职能部门发现模块配置和业务数据中的问题。</span><span class="sxs-lookup"><span data-stu-id="51be1-108">The **Optimization advisor** workspace is a tool that lets power users, business analysts, functional consultants, and IT support functions identify issues in module configuration and business data.</span></span> <span data-ttu-id="51be1-109">优化顾问建议模块配置的最佳实践并确定废弃或不正确的业务数据。</span><span class="sxs-lookup"><span data-stu-id="51be1-109">Optimization advisor suggests best practices for module configuration and identifies business data that is obsolete or incorrect.</span></span>

<span data-ttu-id="51be1-110">优化顾问会定期运行一组最佳实践规则。</span><span class="sxs-lookup"><span data-stu-id="51be1-110">Optimization advisor periodically runs a set of best practice rules.</span></span> <span data-ttu-id="51be1-111">提供了一组默认规则，但是，用户也可以创建特定于其自定义、来自独立软件供应商 (ISV) 的解决方案和业务数据的规则。</span><span class="sxs-lookup"><span data-stu-id="51be1-111">A default set of rules is available, however users can also create rules that are specific to their customizations, solutions from independent software vendors (ISVs), and business data.</span></span> <span data-ttu-id="51be1-112">有关如何创建规则的详细信息，请参阅[创建优化顾问规则](./create-rules-optimization-advisor.md)。</span><span class="sxs-lookup"><span data-stu-id="51be1-112">For more information about how to create rules, see [Create rules for Optimization advisor](./create-rules-optimization-advisor.md).</span></span>

<span data-ttu-id="51be1-113">在检测到违反规则时，优化机会将生成并显示在**优化顾问**工作区中。</span><span class="sxs-lookup"><span data-stu-id="51be1-113">When a violation of a rule is detected, an optimization opportunity is generated and appears in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="51be1-114">用户可以直接从**优化顾问**工作区采取适当的纠正措施。</span><span class="sxs-lookup"><span data-stu-id="51be1-114">A user can take appropriate corrective action directly from the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="51be1-115">机会可以是公司特定或跨公司的，具体取决于所验证的设置和数据的类型。</span><span class="sxs-lookup"><span data-stu-id="51be1-115">Opportunities can be company-specific or cross-company, depending on the type of setup and data that is being validated.</span></span> <span data-ttu-id="51be1-116">跨公司机会可以从所有公司查看。</span><span class="sxs-lookup"><span data-stu-id="51be1-116">Cross-company opportunities can be viewed from all companies.</span></span> <span data-ttu-id="51be1-117">若要查看特定公司的机会，必须首先选择公司。</span><span class="sxs-lookup"><span data-stu-id="51be1-117">To view the opportunities for a specific company, you must first select the company.</span></span>

<span data-ttu-id="51be1-118">优化机会应用标准安全政策。</span><span class="sxs-lookup"><span data-stu-id="51be1-118">Standard security policies apply to optimization opportunities.</span></span> <span data-ttu-id="51be1-119">例如，与**仓库管理**模块的配置相关的优化机会仅对有权访问“仓库管理”且可以更改其设置的用户可见。</span><span class="sxs-lookup"><span data-stu-id="51be1-119">For example, the optimization opportunities that are related to configuration of the **Warehouse management** module are visible only to users who have access to Warehouse management and can change its setup.</span></span>

<span data-ttu-id="51be1-120">当您对一些优化机会采取行动时，系统将计算机会对业务流程运行时间减少的影响。</span><span class="sxs-lookup"><span data-stu-id="51be1-120">When you take action on some optimization opportunities, the system calculates the impact of the opportunity in terms of the reduction in the runtime of business processes.</span></span> <span data-ttu-id="51be1-121">很遗憾，此功能不能用于所有优化机会。</span><span class="sxs-lookup"><span data-stu-id="51be1-121">Unfortunately, this feature isn't available for all optimization opportunities.</span></span>

<span data-ttu-id="51be1-122">若要了解有关“优化顾问”的详细信息，请观看视频短片 [Dynamics 365 for Finance and Operations 中的优化顾问](https://www.youtube.com/watch?v=MRsAzgFCUSQ)。</span><span class="sxs-lookup"><span data-stu-id="51be1-122">To learn more about Optimization advisor, watch the short [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ) video.</span></span>

## <a name="optimization-rules"></a><span data-ttu-id="51be1-123">优化规则</span><span class="sxs-lookup"><span data-stu-id="51be1-123">Optimization rules</span></span>

<span data-ttu-id="51be1-124">要查看优化顾问规则的完整列表并了解规则的评估频率，请转到**系统管理** &gt; **定期任务** &gt; **维护诊断验证规则**。</span><span class="sxs-lookup"><span data-stu-id="51be1-124">To view the complete list of Optimization advisor rules and to see how often the rules are evaluated, go to **System administration** &gt; **Periodic tasks** &gt; **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="51be1-125">仅对具有**活动**状态的规则进行评估。</span><span class="sxs-lookup"><span data-stu-id="51be1-125">Only rules that have a status of **Active** are evaluated.</span></span> <span data-ttu-id="51be1-126">评估频率可以设置为**每日**、**每周**、**每月**或**未计划**。</span><span class="sxs-lookup"><span data-stu-id="51be1-126">The evaluation frequency can be set to **Daily**, **Weekly**, **Monthly**, or **Unscheduled**.</span></span>

<span data-ttu-id="51be1-127">若要触发对未计划规则的评估，或在预定义的计划外重新评估定期规则，转到**系统管理** &gt; **定期任务** &gt; **计划诊断验证规则**。</span><span class="sxs-lookup"><span data-stu-id="51be1-127">To trigger the evaluation of unscheduled rules, or to reevaluate periodic rules outside their predefined schedule, go to **System administration** &gt; **Periodic tasks** &gt; **Schedule diagnostics validation rule**.</span></span> <span data-ttu-id="51be1-128">然后，在**诊断规则验证**对话框中，选择评估频率。</span><span class="sxs-lookup"><span data-stu-id="51be1-128">Then, in the **Diagnostic rule validation** dialog box, select an evaluation frequency.</span></span> <span data-ttu-id="51be1-129">具有指定频率的所有规则都将重新评估。</span><span class="sxs-lookup"><span data-stu-id="51be1-129">All rules that have the specified frequency will be reevaluated.</span></span>

<span data-ttu-id="51be1-130">当前的优化规则设置可划分为以下几个类别。</span><span class="sxs-lookup"><span data-stu-id="51be1-130">The current set of optimization rules can be divided into the following categories.</span></span>

### <a name="module-configuration-and-setup"></a><span data-ttu-id="51be1-131">模块配置和设置</span><span class="sxs-lookup"><span data-stu-id="51be1-131">Module configuration and setup</span></span>

<span data-ttu-id="51be1-132">仓库管理设置是一个复杂的过程。</span><span class="sxs-lookup"><span data-stu-id="51be1-132">The setup of Warehouse management is a complicated process.</span></span> <span data-ttu-id="51be1-133">为了让这个过程更简单，引入了某些规则来帮助验证设置的正确性。</span><span class="sxs-lookup"><span data-stu-id="51be1-133">To make the process easier, some rules have been introduced to help validate the correctness of the setup.</span></span> <span data-ttu-id="51be1-134">例如，有一个规则验证销售订单和转移单的固定产品变型位置的仓库库位指令的设置。</span><span class="sxs-lookup"><span data-stu-id="51be1-134">For example, one rule validates the setup of warehouse location directives for fixed product variant locations for sales orders and transfer orders.</span></span>

<span data-ttu-id="51be1-135">此外，某些规则检查是否实际使用了已启用的功能。</span><span class="sxs-lookup"><span data-stu-id="51be1-135">Additionally, some rules check whether features that have been enabled are actually used.</span></span> <span data-ttu-id="51be1-136">例如，有一个规则确定您是否在使用**主计划**模块。</span><span class="sxs-lookup"><span data-stu-id="51be1-136">For example, one rule determines whether you're using the **Master planning** module.</span></span> <span data-ttu-id="51be1-137">如果规则确定您未使用此模块，优化机会将生成以建议您关闭计划流程。</span><span class="sxs-lookup"><span data-stu-id="51be1-137">If the rule determines that you aren't using the module, an optimization opportunity is generated to suggest that you turn off the planning processes.</span></span>

### <a name="system-configuration"></a><span data-ttu-id="51be1-138">系统配置</span><span class="sxs-lookup"><span data-stu-id="51be1-138">System configuration</span></span>

<span data-ttu-id="51be1-139">如果未使用由 Configuration Key 控制的特定功能，优化机会将生成以建议您禁用 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="51be1-139">If specific functionality that is controlled by a configuration key isn't used, an optimization opportunity is generated to suggest that you disable the configuration key.</span></span> <span data-ttu-id="51be1-140">Configuration Key 的示例包括**实际称重**、**预算计划**、**项目**和**核准供应商列表**。</span><span class="sxs-lookup"><span data-stu-id="51be1-140">Examples of configuration keys include **Catch weight**, **Budget planning**, **Project**, and **Approved vendor list**.</span></span>

### <a name="business-data-consistency-and-cleanup"></a><span data-ttu-id="51be1-141">业务数据的一致性和清理</span><span class="sxs-lookup"><span data-stu-id="51be1-141">Business data consistency and cleanup</span></span>

<span data-ttu-id="51be1-142">如果主数据不正确（例如，如果您有未定义单位的度量单位转换，或者您有除以 0 \[零\] 的度量单位转换），优化机会将生成以建议您更正数据。</span><span class="sxs-lookup"><span data-stu-id="51be1-142">If master data isn't correct (for example, if you have unit of measure conversions for units that haven't been defined, or if you have unit of measure conversions that have a division by 0 \[zero\]), an optimization opportunity is generated to suggest that you correct the data.</span></span> 

<span data-ttu-id="51be1-143">如果您的批处理作业历史记录条目、废弃项目、已启用仓库物料的关闭的现有条目等太多，或者如果这些条目和项目过旧，优化机会将生成以建议您清理数据。</span><span class="sxs-lookup"><span data-stu-id="51be1-143">If you have too many batch job history entries, obsolete items, closed on-hand entries for warehouse enabled items, and so on, or if those entries and items are too old, optimization opportunities are generated to suggest that you clean up the data.</span></span> <span data-ttu-id="51be1-144">通过保持数据的清洁，您可以帮助改善整个系统的性能。</span><span class="sxs-lookup"><span data-stu-id="51be1-144">By keeping your data clean, you can help improve overall system performance.</span></span>

### <a name="best-practices"></a><span data-ttu-id="51be1-145">最佳实践</span><span class="sxs-lookup"><span data-stu-id="51be1-145">Best practices</span></span>

<span data-ttu-id="51be1-146">如果您未根据最佳实践运行某些业务流程（例如，如果您在库存结转之前运行库存预结转，或者，如果您为子分类帐日记帐批处理转移使用计划的批处理），优化机会会通知您最佳实践并要求您照其执行。</span><span class="sxs-lookup"><span data-stu-id="51be1-146">If you aren't running some business processes according to best practices (for example, if you run inventory pre-closing before the inventory is closed, or if you use the scheduled batch for subledger journal batch transfer), optimization opportunities inform you about the best practice and ask that you follow it.</span></span>

## <a name="optimization-opportunities"></a><span data-ttu-id="51be1-147">优化机会</span><span class="sxs-lookup"><span data-stu-id="51be1-147">Optimization opportunities</span></span>

<span data-ttu-id="51be1-148">若要查看在优化规则评估时创建的优化机会，打开**优化顾问**工作区。</span><span class="sxs-lookup"><span data-stu-id="51be1-148">To view the optimization opportunities that are generated during the evaluation of optimization rules, open the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="51be1-149">在此工作区，您可以通过选择**更多信息**查看与机会有关的详细信息。</span><span class="sxs-lookup"><span data-stu-id="51be1-149">In this workspace, you can view more information about an opportunity by selecting **More information**.</span></span> <span data-ttu-id="51be1-150">如果您希望系统采取措施、更正设置、清洁数据等，以便您无需自己打开相应页面，选择**采取措施**。</span><span class="sxs-lookup"><span data-stu-id="51be1-150">If you want the system to take action and correct the setup, clean the data, and so on, so that you don't have to open the corresponding pages yourself, select **Take action**.</span></span>

<span data-ttu-id="51be1-151">优化机会没有工作流。</span><span class="sxs-lookup"><span data-stu-id="51be1-151">There is no workflow for optimization opportunities.</span></span> <span data-ttu-id="51be1-152">在您选择**采取措施**或使用**更多信息**对话框中提供的导航路径后，优化机会将从列表中消失。</span><span class="sxs-lookup"><span data-stu-id="51be1-152">After you select **Take action** or use a navigation path that is provided in the **More information** dialog box, the optimization opportunity disappears from the list.</span></span> <span data-ttu-id="51be1-153">如果该更正操作未完全解决问题，机会将在下次评估规则时再次生成。</span><span class="sxs-lookup"><span data-stu-id="51be1-153">If the corrective action doesn't completely resolve an issue, the opportunity will be generated again the next time that the rule is evaluated.</span></span>

<span data-ttu-id="51be1-154">如果机会不适用于您的角色，您可以选择**从我的列表中隐藏**。</span><span class="sxs-lookup"><span data-stu-id="51be1-154">If an opportunity doesn't apply to your role, you can select **Hide from my list**.</span></span> <span data-ttu-id="51be1-155">即使此机会背后的规则后以后再次触发，您也不会在您的列表中看到此机会。</span><span class="sxs-lookup"><span data-stu-id="51be1-155">Even if the rule behind this opportunity is triggered again later, you won't see the opportunity in your list.</span></span>

<span data-ttu-id="51be1-156">若要禁用特定规则的评估，选择由规则生成的机会，然后选择**禁用分析**。</span><span class="sxs-lookup"><span data-stu-id="51be1-156">To deactivate the evaluation of specific rules, select the opportunity that was generated by the rule, and then select **Deactivate analysis**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51be1-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="51be1-157">Additional resources</span></span>

[<span data-ttu-id="51be1-158">创建优化顾问规则</span><span class="sxs-lookup"><span data-stu-id="51be1-158">Create rules for Optimization advisor</span></span>](./create-rules-optimization-advisor.md)

[<span data-ttu-id="51be1-159">Dynamics 365 for Finance and Operations 中的优化顾问（视频）</span><span class="sxs-lookup"><span data-stu-id="51be1-159">Optimization advisor in Dynamics 365 for Finance and Operations (Video)</span></span>](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
