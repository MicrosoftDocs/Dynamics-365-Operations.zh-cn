---
title: "配置费用管理"
description: "本文介绍您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中配置费用管理前在计划流程中的考虑事项和必须做的决定。 在“费用管理”区域中，除其他信息外，您可以存储有关付款方式、出差申请、支出报表和政策的信息。"
author: KimANelson
manager: AnnBe
ms.date: 06/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 83cfd2ef15ae3a02eba21bb31f3311e8f5e15b90
ms.contentlocale: zh-cn
ms.lasthandoff: 06/30/2017


---

# <a name="configure-expense-management"></a><span data-ttu-id="5ce34-104">配置费用管理</span><span class="sxs-lookup"><span data-stu-id="5ce34-104">Configure expense management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5ce34-105">本文介绍您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中配置费用管理前在计划流程中的考虑事项和必须做的决定。</span><span class="sxs-lookup"><span data-stu-id="5ce34-105">This article describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="5ce34-106">在“费用管理”区域中，除其他信息外，您可以存储有关付款方式、出差申请、支出报表和政策的信息。</span><span class="sxs-lookup"><span data-stu-id="5ce34-106">In the Expense management area, you can store information about payment methods, travel requisitions, expense reports, and policies, among other things.</span></span> 

<span data-ttu-id="5ce34-107">由于您在计划费用管理的配置时所做的许多决策基于您的组织的层次结构和财务结构，因此您必须是引用这些领域的计划文档。</span><span class="sxs-lookup"><span data-stu-id="5ce34-107">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="5ce34-108">内部公司支出</span><span class="sxs-lookup"><span data-stu-id="5ce34-108">Intercompany expenses</span></span>
<span data-ttu-id="5ce34-109">在您启用内部公司费用时，您允许和法人和员工代表您组织中的其他法人产生费用，从您组织中的其他法人那里收取付款。</span><span class="sxs-lookup"><span data-stu-id="5ce34-109">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of, and collect payment from, another legal entity within your organization.</span></span> <span data-ttu-id="5ce34-110">例如，法人 A 中的某员工完成法人 B 的一个项目。如果启用内部公司费用，员工可以将时间表存档到法人 B 并由法人 B 付款。如果您的组织不具有多个法人，您就不需要启用内部公司费用。</span><span class="sxs-lookup"><span data-stu-id="5ce34-110">For example, an employee in legal entity A completes a project for legal entity B. If intercompany expenses are enabled, the employee can then file a timesheet to, and be paid by, legal entity B. If your organization doesn’t have multiple legal entities, you won’t need to enable intercompany expenses.</span></span> <span data-ttu-id="5ce34-111">**决策：**是否要启用内部公司费用？</span><span class="sxs-lookup"><span data-stu-id="5ce34-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="5ce34-112">财务管理</span><span class="sxs-lookup"><span data-stu-id="5ce34-112">Financial management</span></span>
<span data-ttu-id="5ce34-113">费用管理与您的组织的财务管理紧密集成。</span><span class="sxs-lookup"><span data-stu-id="5ce34-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="5ce34-114">费用管理的许多配置都将基于您关于您的组织的财务作出的决策。</span><span class="sxs-lookup"><span data-stu-id="5ce34-114">A lot of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="5ce34-115">以下各节介绍需要基于您的领导团队给出的您组织的财务决策和指导计划和决策的不同领域。</span><span class="sxs-lookup"><span data-stu-id="5ce34-115">The following sections describe the different areas that require planning and decisions based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="5ce34-116">出差津贴</span><span class="sxs-lookup"><span data-stu-id="5ce34-116">Per diems</span></span>

<span data-ttu-id="5ce34-117">您必须定义您的组织提供的员工出差津贴。</span><span class="sxs-lookup"><span data-stu-id="5ce34-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="5ce34-118">由于出差津贴通常用于覆盖费用（如津贴、住所和其他附加费用），因此您可以创建您的组织提供的出差津贴补助的规则。</span><span class="sxs-lookup"><span data-stu-id="5ce34-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="5ce34-119">出差津贴比率可以基于出差时间和/或出差地点。</span><span class="sxs-lookup"><span data-stu-id="5ce34-119">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5ce34-120">在定义某一出差津贴规则时，您可以指定将预扣的出差津贴费用百分比（如果工作人员获得了免费提供的餐饮或服务）。</span><span class="sxs-lookup"><span data-stu-id="5ce34-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5ce34-121">您还可以定义出差津贴费率层，以设置可以对工作人员差旅应用出差津贴费率的最低和最高小时数。</span><span class="sxs-lookup"><span data-stu-id="5ce34-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span> <span data-ttu-id="5ce34-122">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-122">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-123">第一天和最后一天的默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="5ce34-123">Default per diem rules for the first and last days:</span></span>
    -   <span data-ttu-id="5ce34-124">员工可以要求一天下班打卡并仍领取出差津贴的最低小时数是多少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    -   <span data-ttu-id="5ce34-125">为第一天和最后一天的餐饮提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-125">Is there a reduction in the amount that is offered for meals for the first and last day?</span></span> <span data-ttu-id="5ce34-126">如果是，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-126">If so, what is the percentage of the reduction?</span></span>
    -   <span data-ttu-id="5ce34-127">为第一天和最后一天的酒店提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-127">Is there a reduction in the amount that is offered for a hotel for the first and last day?</span></span> <span data-ttu-id="5ce34-128">如果是，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-128">If so, what is the percentage of the reduction?</span></span>
    -   <span data-ttu-id="5ce34-129">为第一天和最后一天发生的其他费用提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-129">Is there a reduction in the amount that is offered for other expenses incurred on the first and last day?</span></span> <span data-ttu-id="5ce34-130">如果是，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-130">If so, what is the percentage of the reduction?</span></span>
-   <span data-ttu-id="5ce34-131">默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="5ce34-131">Default per diem rules:</span></span>
    -   <span data-ttu-id="5ce34-132">如果（例如）就餐是免费的，那么每次就餐的出差津贴补助是否存在百分比减少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="5ce34-133">如果是，那么每次就餐的减少百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="5ce34-133">If so, what is the reduction percentage for each meal?</span></span>
    -   <span data-ttu-id="5ce34-134">餐费减少是按天、按行程计算的，还是按每天的就餐次数计算的？</span><span class="sxs-lookup"><span data-stu-id="5ce34-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    -   <span data-ttu-id="5ce34-135">出差津贴应正常四舍五入还是向上舍入？</span><span class="sxs-lookup"><span data-stu-id="5ce34-135">Should per diem amounts be rounded normally or rounded up?</span></span>
    -   <span data-ttu-id="5ce34-136">出差津贴是按 24 小时期间计算的还是按一个日历天计算的？</span><span class="sxs-lookup"><span data-stu-id="5ce34-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>
-   <span data-ttu-id="5ce34-137">基于位置的出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="5ce34-137">Per diem rules based on location:</span></span>
    -   <span data-ttu-id="5ce34-138">出差津贴费率是否基于位置而变，而且都包括什么位置？</span><span class="sxs-lookup"><span data-stu-id="5ce34-138">Do per diem rates vary based on location and what locations are included?</span></span>
    -   <span data-ttu-id="5ce34-139">如果出差津贴费率基于位置而变，那么对于每个位置，提供什么样的百分比金额：</span><span class="sxs-lookup"><span data-stu-id="5ce34-139">If per diem rate do vary based on location, for each location, what percentage amount is provided for:</span></span>
        -   <span data-ttu-id="5ce34-140">就餐</span><span class="sxs-lookup"><span data-stu-id="5ce34-140">meals</span></span>
        -   <span data-ttu-id="5ce34-141">酒店</span><span class="sxs-lookup"><span data-stu-id="5ce34-141">hotel</span></span>
        -   <span data-ttu-id="5ce34-142">其他费用</span><span class="sxs-lookup"><span data-stu-id="5ce34-142">other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="5ce34-143">费用管理日记帐和帐户</span><span class="sxs-lookup"><span data-stu-id="5ce34-143">Expense management journals and accounts</span></span>

<span data-ttu-id="5ce34-144">费用管理要求您使用多个日记帐和帐户。</span><span class="sxs-lookup"><span data-stu-id="5ce34-144">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="5ce34-145">例如，您必须确定同一帐户是否用于预付现金和信用卡争议。</span><span class="sxs-lookup"><span data-stu-id="5ce34-145">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span> <span data-ttu-id="5ce34-146">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-146">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-147">已审核的费用报表过帐到哪个分类帐日记帐？</span><span class="sxs-lookup"><span data-stu-id="5ce34-147">Which ledger journal are approved expense reports posted to?</span></span>
-   <span data-ttu-id="5ce34-148">哪个帐户用于预付现金？</span><span class="sxs-lookup"><span data-stu-id="5ce34-148">Which account is used for cash advances?</span></span>
-   <span data-ttu-id="5ce34-149">是否应立即过帐预付现金？</span><span class="sxs-lookup"><span data-stu-id="5ce34-149">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="5ce34-150">付款方式</span><span class="sxs-lookup"><span data-stu-id="5ce34-150">Payment methods</span></span>

<span data-ttu-id="5ce34-151">当您允许员工代表您的企业产生支出时，您必须定义允许员工使用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="5ce34-151">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="5ce34-152">例如，您可能允许员工使用现金或公司信用卡。</span><span class="sxs-lookup"><span data-stu-id="5ce34-152">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="5ce34-153">您可能还允许员工使用个人信用卡，然后偿还员工。</span><span class="sxs-lookup"><span data-stu-id="5ce34-153">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="5ce34-154">您必须为允许您的每个付款方式做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="5ce34-154">You must make the following decisions for each payment method that you allow.</span></span> <span data-ttu-id="5ce34-155">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-155">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-156">允许什么付款方式？</span><span class="sxs-lookup"><span data-stu-id="5ce34-156">What payment methods are allowed?</span></span>
-   <span data-ttu-id="5ce34-157">谁拥有付款方式费用？</span><span class="sxs-lookup"><span data-stu-id="5ce34-157">Who owns the payment method expenses?</span></span>
-   <span data-ttu-id="5ce34-158">是否有对方科目类型？</span><span class="sxs-lookup"><span data-stu-id="5ce34-158">Is there an offset account type?</span></span> <span data-ttu-id="5ce34-159">如果有，它是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-159">If so, what is it?</span></span>
-   <span data-ttu-id="5ce34-160">如果存在一个对方科目，该科目是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-160">If there is an offset account, what is the account?</span></span>
-   <span data-ttu-id="5ce34-161">如果付款方式是信用卡，那么是否付款方式仅用于导入的交易记录？</span><span class="sxs-lookup"><span data-stu-id="5ce34-161">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="5ce34-162">费用类别和共享类别</span><span class="sxs-lookup"><span data-stu-id="5ce34-162">Expense categories and shared categories</span></span>

<span data-ttu-id="5ce34-163">当员工创建费用报表时，他们记录的每个费用都必须与支出类别关联。</span><span class="sxs-lookup"><span data-stu-id="5ce34-163">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="5ce34-164">费用类别是从共享类别派生的，共享类别可以在您的组织中的法人间共享。</span><span class="sxs-lookup"><span data-stu-id="5ce34-164">Expense categories are derived from Shared categories that can be shared across the legal entities within your organization.</span></span> <span data-ttu-id="5ce34-165">这些类别还可以在项目管理和会计中共享，具体取决于您的组织是如何定义的。</span><span class="sxs-lookup"><span data-stu-id="5ce34-165">These categories can also be shared in Project management and accounting, depending on how your organization is defined.</span></span> <span data-ttu-id="5ce34-166">根据您组织的定义和实施团队的指导，确定在费用管理中使用的类别是否要仅在费用中使用，或者它们是否应在项目和费用之间共享。</span><span class="sxs-lookup"><span data-stu-id="5ce34-166">Based on the definition of your organization and guidance from the implementation team, determine whether the categories used in expense management are to be used in only expense or if they should be shared between Project and Expense.</span></span> <span data-ttu-id="5ce34-167">请注意，这些类别可以在项目和费用或项目和生产之间共享，不过，不在费用和生产之间共享。</span><span class="sxs-lookup"><span data-stu-id="5ce34-167">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="5ce34-168">您必须为每个费用类别做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="5ce34-168">You must make the following decisions for each expense category.</span></span> <span data-ttu-id="5ce34-169">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-169">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-170">费用类别是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-170">What is the expense category?</span></span> <span data-ttu-id="5ce34-171">例如，飞行、酒店或里程。</span><span class="sxs-lookup"><span data-stu-id="5ce34-171">For example, flights, hotel, or mileage.</span></span>
-   <span data-ttu-id="5ce34-172">此费用类别是否还可以在项目管理和会计中使用？</span><span class="sxs-lookup"><span data-stu-id="5ce34-172">Can this expense category also be used in Project management and accounting?</span></span>
-   <span data-ttu-id="5ce34-173">费用类型是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-173">What is the expense type?</span></span>
-   <span data-ttu-id="5ce34-174">费用类别的默认付款方式是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-174">What is the default payment method for the expense category?</span></span>
-   <span data-ttu-id="5ce34-175">此类别中的费用是否必须明细化？</span><span class="sxs-lookup"><span data-stu-id="5ce34-175">Are expenses in this category required to be itemized?</span></span>
-   <span data-ttu-id="5ce34-176">费用类别的主要默认帐户是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-176">What is the main default account for the expense category?</span></span>
-   <span data-ttu-id="5ce34-177">费用类别的默认物料销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-177">What is the default item sales tax group for the expense category?</span></span>
-   <span data-ttu-id="5ce34-178">此支出类别是否允许其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="5ce34-178">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="5ce34-179">如果是，它们是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-179">If so, what are they?</span></span>
-   <span data-ttu-id="5ce34-180">此费用类别中是否有子类别？</span><span class="sxs-lookup"><span data-stu-id="5ce34-180">Are there subcategories within this expense category?</span></span> <span data-ttu-id="5ce34-181">如果是：</span><span class="sxs-lookup"><span data-stu-id="5ce34-181">If so:</span></span>
    -   <span data-ttu-id="5ce34-182">是否任何子类别都排除在退税之外？</span><span class="sxs-lookup"><span data-stu-id="5ce34-182">Are any of the subcategories excluded from tax recovery?</span></span>
    -   <span data-ttu-id="5ce34-183">子类别的物料销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-183">What is the item sales tax group of the subcategories?</span></span>

    <span data-ttu-id="5ce34-184">如果此费用类别还用于项目管理和会计，则回答剩余的问题。</span><span class="sxs-lookup"><span data-stu-id="5ce34-184">If this expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="5ce34-185">否则，此部分即完成。</span><span class="sxs-lookup"><span data-stu-id="5ce34-185">Otherwise, you are finished with this section.</span></span>
-   <span data-ttu-id="5ce34-186">哪些成本科目用于以下各项？</span><span class="sxs-lookup"><span data-stu-id="5ce34-186">Which cost accounts will be used for the following?</span></span>
    -   <span data-ttu-id="5ce34-187">成本</span><span class="sxs-lookup"><span data-stu-id="5ce34-187">Cost</span></span>
    -   <span data-ttu-id="5ce34-188">工资分配</span><span class="sxs-lookup"><span data-stu-id="5ce34-188">Payroll allocation</span></span>
    -   <span data-ttu-id="5ce34-189">WIP - 成本价值</span><span class="sxs-lookup"><span data-stu-id="5ce34-189">WIP-cost value</span></span>
    -   <span data-ttu-id="5ce34-190">成本 - 物料</span><span class="sxs-lookup"><span data-stu-id="5ce34-190">Cost-item</span></span>
    -   <span data-ttu-id="5ce34-191">WIP - 成本价值 - 物料</span><span class="sxs-lookup"><span data-stu-id="5ce34-191">WIP-cost value-item</span></span>
    -   <span data-ttu-id="5ce34-192">应计损失</span><span class="sxs-lookup"><span data-stu-id="5ce34-192">Accrued loss</span></span>
    -   <span data-ttu-id="5ce34-193">WIP - 应计损失</span><span class="sxs-lookup"><span data-stu-id="5ce34-193">WIP-accrued loss</span></span>
-   <span data-ttu-id="5ce34-194">哪些收入科目用于以下各项？</span><span class="sxs-lookup"><span data-stu-id="5ce34-194">Which revenue accounts will be used for the following?</span></span>
    -   <span data-ttu-id="5ce34-195">开票收入</span><span class="sxs-lookup"><span data-stu-id="5ce34-195">Invoiced revenue</span></span>
    -   <span data-ttu-id="5ce34-196">应计收入 - 销售价值</span><span class="sxs-lookup"><span data-stu-id="5ce34-196">Accrued revenue-sales value</span></span>
    -   <span data-ttu-id="5ce34-197">WIP - 销售价值</span><span class="sxs-lookup"><span data-stu-id="5ce34-197">WIP-sales value</span></span>
    -   <span data-ttu-id="5ce34-198">应计收入 - 生产</span><span class="sxs-lookup"><span data-stu-id="5ce34-198">Accrued revenue-production</span></span>
    -   <span data-ttu-id="5ce34-199">WIP - 生产</span><span class="sxs-lookup"><span data-stu-id="5ce34-199">WIP-production</span></span>
    -   <span data-ttu-id="5ce34-200">应计收入 - 利润</span><span class="sxs-lookup"><span data-stu-id="5ce34-200">Accrued revenue-profit</span></span>
    -   <span data-ttu-id="5ce34-201">WIP - 利润</span><span class="sxs-lookup"><span data-stu-id="5ce34-201">WIP-profit</span></span>
    -   <span data-ttu-id="5ce34-202">应计收入 - 预订</span><span class="sxs-lookup"><span data-stu-id="5ce34-202">Accrued revenue-subscription</span></span>
    -   <span data-ttu-id="5ce34-203">WIP - 预订</span><span class="sxs-lookup"><span data-stu-id="5ce34-203">WIP-subscription</span></span>

 

### <a name="taxes"></a><span data-ttu-id="5ce34-204">税金</span><span class="sxs-lookup"><span data-stu-id="5ce34-204">Taxes</span></span>

<span data-ttu-id="5ce34-205">对于支出相关的税，必须确定费用报表上包括或启用什么。</span><span class="sxs-lookup"><span data-stu-id="5ce34-205">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span> <span data-ttu-id="5ce34-206">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-206">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-207">销售税是否包括在费用金额中？</span><span class="sxs-lookup"><span data-stu-id="5ce34-207">Is sales tax included in the expense amounts?</span></span>
-   <span data-ttu-id="5ce34-208">是否在费用上启用退税？</span><span class="sxs-lookup"><span data-stu-id="5ce34-208">Should tax recovery be enabled on expenses?</span></span>

<span data-ttu-id="5ce34-209">请注意，如果在您计划总帐期间，您决定应用美国销售税并且使用销项税规则（通过将**“应用销售税税务规则”**字段切换为“是”），则无法在费用上启用退税。</span><span class="sxs-lookup"><span data-stu-id="5ce34-209">Note that if, during your planning of the general ledger, you have decided to apply U.S. sales tax and use tax rules, which is done by toggling the **Apply sales tax taxations rules** field to Yes, you can’t enable tax recovery on expenses.</span></span>

## <a name="policies"></a><span data-ttu-id="5ce34-210">政策</span><span class="sxs-lookup"><span data-stu-id="5ce34-210">Policies</span></span>
<span data-ttu-id="5ce34-211">您可以创建费用报表策略，以便您的组织可以在员工产生代表自己产生费用时节省时间和金钱。</span><span class="sxs-lookup"><span data-stu-id="5ce34-211">You can create expense report policies so that your organization can save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="5ce34-212">策略可确保员工保持在预算中，提供所有必需的信息，并且只在需要时花钱。</span><span class="sxs-lookup"><span data-stu-id="5ce34-212">Policies ensure that employees stay within budget, provide all required information, and spend money only as necessary.</span></span> <span data-ttu-id="5ce34-213">您必须为您创建的每个费用报表策略和每个费用报表审核策略做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="5ce34-213">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span> <span data-ttu-id="5ce34-214">**决策：**</span><span class="sxs-lookup"><span data-stu-id="5ce34-214">**Decisions:**</span></span>

-   <span data-ttu-id="5ce34-215">策略的名称是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-215">What is the name of the policy?</span></span>
-   <span data-ttu-id="5ce34-216">费用策略的目的是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-216">What is the expense policy for?</span></span>
-   <span data-ttu-id="5ce34-217">如果您已经决定启用内部公司费用，则此策略将应用于您组织中的哪个公司？</span><span class="sxs-lookup"><span data-stu-id="5ce34-217">If you previously decided to enable intercompany expenses, to which companies in your organization will this policy apply?</span></span>
-   <span data-ttu-id="5ce34-218">策略什么时候生效？</span><span class="sxs-lookup"><span data-stu-id="5ce34-218">When does the policy become effective?</span></span>
-   <span data-ttu-id="5ce34-219">策略什么时候到期？</span><span class="sxs-lookup"><span data-stu-id="5ce34-219">When does the policy expire?</span></span>
-   <span data-ttu-id="5ce34-220">策略规则是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-220">What is the policy rule?</span></span>
-   <span data-ttu-id="5ce34-221">策略规则的结果是什么？</span><span class="sxs-lookup"><span data-stu-id="5ce34-221">What is the outcome of the policy rule?</span></span>





