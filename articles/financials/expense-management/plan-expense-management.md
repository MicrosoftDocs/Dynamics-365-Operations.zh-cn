---
title: "配置费用管理"
description: "本文介绍您在 Microsoft Dynamics 365 for Finance and Operations 中配置费用管理前在计划流程中的考虑事项和必须做的决定。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7c7bfaf4301904e1b7ae242efaf8b660fb076a
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="6946d-103">配置费用管理</span><span class="sxs-lookup"><span data-stu-id="6946d-103">Configure expense management</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6946d-104">本主题介绍您在 Microsoft Dynamics 365 for Finance and Operations 中配置费用管理前在计划流程中的考虑事项和必须做的决定。</span><span class="sxs-lookup"><span data-stu-id="6946d-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6946d-105">在费用管理中，您可以存储有关付款方式、出差申请、费用报表和政策等的信息。</span><span class="sxs-lookup"><span data-stu-id="6946d-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="6946d-106">由于您在计划费用管理的配置时所做的许多决策基于您的组织的层次结构和财务结构，因此您必须是引用这些领域的计划文档。</span><span class="sxs-lookup"><span data-stu-id="6946d-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="6946d-107">内部公司支出</span><span class="sxs-lookup"><span data-stu-id="6946d-107">Intercompany expenses</span></span>

<span data-ttu-id="6946d-108">在您启用内部公司费用时，您允许和法人和员工代表您组织中的其他法人产生费用，从您组织中的雇佣法人那里收取付款。</span><span class="sxs-lookup"><span data-stu-id="6946d-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="6946d-109">例如，法人 A 中的一名员工完成法人 B 的一个项目，且该项目产生出差费用。</span><span class="sxs-lookup"><span data-stu-id="6946d-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="6946d-110">如果启用内部公司费用，则该员工可以提交费用报表，将费用过帐到法人 B，且该费用必须由法人 A 支付。如果您的组织不具有多个法人，您就不需要启用内部公司费用。</span><span class="sxs-lookup"><span data-stu-id="6946d-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="6946d-111">**决策：**是否要启用内部公司费用？</span><span class="sxs-lookup"><span data-stu-id="6946d-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="6946d-112">财务管理</span><span class="sxs-lookup"><span data-stu-id="6946d-112">Financial management</span></span>

<span data-ttu-id="6946d-113">费用管理与您的组织的财务管理紧密集成。</span><span class="sxs-lookup"><span data-stu-id="6946d-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="6946d-114">费用管理的许多配置都将基于您作出的关于您的组织的财务决策。</span><span class="sxs-lookup"><span data-stu-id="6946d-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="6946d-115">以下各节介绍需要基于您的领导团队给出的您组织的财务决策和指导计划和决策的不同领域。</span><span class="sxs-lookup"><span data-stu-id="6946d-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="6946d-116">出差津贴</span><span class="sxs-lookup"><span data-stu-id="6946d-116">Per diems</span></span>

<span data-ttu-id="6946d-117">您必须定义您的组织提供的员工出差津贴。</span><span class="sxs-lookup"><span data-stu-id="6946d-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="6946d-118">由于出差津贴通常用于覆盖费用（如津贴、住所和其他附加费用），因此您可以创建您的组织提供的出差津贴补助的规则。</span><span class="sxs-lookup"><span data-stu-id="6946d-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="6946d-119">出差津贴比率可以基于出差时间和/或出差地点。</span><span class="sxs-lookup"><span data-stu-id="6946d-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="6946d-120">在定义某一出差津贴规则时，您可以指定将预扣的出差津贴费用百分比（如果工作人员获得了免费提供的餐饮或服务）。</span><span class="sxs-lookup"><span data-stu-id="6946d-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="6946d-121">您还可以定义出差津贴费率层，以设置可以对工作人员差旅应用出差津贴费率的最低和最高小时数。</span><span class="sxs-lookup"><span data-stu-id="6946d-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="6946d-122">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-122">**Decisions:**</span></span>

- <span data-ttu-id="6946d-123">第一天和最后一天的默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="6946d-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="6946d-124">员工可以要求一天下班打卡并仍领取出差津贴的最低小时数是多少？</span><span class="sxs-lookup"><span data-stu-id="6946d-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="6946d-125">为第一天和最后一天的餐饮提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="6946d-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="6946d-126">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="6946d-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="6946d-127">为第一天和最后一天的酒店提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="6946d-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="6946d-128">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="6946d-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="6946d-129">为第一天和最后一天发生的其他费用提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="6946d-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="6946d-130">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="6946d-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="6946d-131">默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="6946d-131">Default per diem rules:</span></span>

    - <span data-ttu-id="6946d-132">如果（例如）就餐是免费的，那么每次就餐的出差津贴补助是否存在百分比减少？</span><span class="sxs-lookup"><span data-stu-id="6946d-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="6946d-133">如果减少，那么每餐减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="6946d-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="6946d-134">餐费减少是按天、按行程计算的，还是按每天的就餐次数计算的？</span><span class="sxs-lookup"><span data-stu-id="6946d-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="6946d-135">出差津贴金额是否应按常规方式四舍五入或向上舍入？</span><span class="sxs-lookup"><span data-stu-id="6946d-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="6946d-136">出差津贴是按 24 小时期间计算的还是按一个日历天计算的？</span><span class="sxs-lookup"><span data-stu-id="6946d-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="6946d-137">基于位置的出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="6946d-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="6946d-138">出差津贴比率根据位置而存在差异？</span><span class="sxs-lookup"><span data-stu-id="6946d-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="6946d-139">哪些位置包括在内？</span><span class="sxs-lookup"><span data-stu-id="6946d-139">What locations are included?</span></span>
    - <span data-ttu-id="6946d-140">如果出差津贴比率根据位置而存在差异，那么对于每个位置，为以下费用类型提供的金额百分比是多少：</span><span class="sxs-lookup"><span data-stu-id="6946d-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="6946d-141">餐费</span><span class="sxs-lookup"><span data-stu-id="6946d-141">Meals</span></span>
        - <span data-ttu-id="6946d-142">酒店</span><span class="sxs-lookup"><span data-stu-id="6946d-142">Hotel</span></span>
        - <span data-ttu-id="6946d-143">其他支出</span><span class="sxs-lookup"><span data-stu-id="6946d-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="6946d-144">费用管理日记帐和帐户</span><span class="sxs-lookup"><span data-stu-id="6946d-144">Expense management journals and accounts</span></span>

<span data-ttu-id="6946d-145">费用管理要求您使用多个日记帐和帐户。</span><span class="sxs-lookup"><span data-stu-id="6946d-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="6946d-146">例如，您必须确定同一帐户是否用于预付现金和信用卡争议。</span><span class="sxs-lookup"><span data-stu-id="6946d-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="6946d-147">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-147">**Decisions:**</span></span>

- <span data-ttu-id="6946d-148">已审核的费用报表过帐到哪个分类帐日记帐？</span><span class="sxs-lookup"><span data-stu-id="6946d-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="6946d-149">哪个帐户用于预付现金？</span><span class="sxs-lookup"><span data-stu-id="6946d-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="6946d-150">是否应立即过帐预付现金？</span><span class="sxs-lookup"><span data-stu-id="6946d-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="6946d-151">付款方式</span><span class="sxs-lookup"><span data-stu-id="6946d-151">Payment methods</span></span>

<span data-ttu-id="6946d-152">当您允许员工代表您的企业产生支出时，您必须定义允许员工使用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="6946d-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="6946d-153">例如，您可能允许员工使用现金或公司信用卡。</span><span class="sxs-lookup"><span data-stu-id="6946d-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="6946d-154">您可能还允许员工使用个人信用卡，然后偿还员工。</span><span class="sxs-lookup"><span data-stu-id="6946d-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="6946d-155">您必须为允许您的每个付款方式做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="6946d-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="6946d-156">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-156">**Decisions:**</span></span>

- <span data-ttu-id="6946d-157">允许什么付款方式？</span><span class="sxs-lookup"><span data-stu-id="6946d-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="6946d-158">谁拥有付款方式费用？</span><span class="sxs-lookup"><span data-stu-id="6946d-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="6946d-159">是否有对方科目类型？</span><span class="sxs-lookup"><span data-stu-id="6946d-159">Is there an offset account type?</span></span> <span data-ttu-id="6946d-160">如果存在一个对方科目类型，该类型是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="6946d-161">如果存在一个对方科目，该科目是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="6946d-162">如果付款方式是信用卡，那么是否付款方式仅用于导入的交易记录？</span><span class="sxs-lookup"><span data-stu-id="6946d-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="6946d-163">费用类别和共享类别</span><span class="sxs-lookup"><span data-stu-id="6946d-163">Expense categories and shared categories</span></span>

<span data-ttu-id="6946d-164">当员工创建费用报表时，他们记录的每个费用都必须与支出类别关联。</span><span class="sxs-lookup"><span data-stu-id="6946d-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="6946d-165">费用类别是从共享类别派生的，共享类别可以在您的组织中的法人间共享。</span><span class="sxs-lookup"><span data-stu-id="6946d-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="6946d-166">这些类别还可以在项目管理和会计中共享，具体取决于您的组织的定义方式。</span><span class="sxs-lookup"><span data-stu-id="6946d-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="6946d-167">根据您组织的定义和实施团队的指导，确定在费用管理中使用的类别是否要仅在费用管理中使用，或者它们是否应在项目管理与核算和费用管理之间共享。</span><span class="sxs-lookup"><span data-stu-id="6946d-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="6946d-168">请注意，这些类别可以在项目和费用或项目和生产之间共享，不过，不在费用和生产之间共享。</span><span class="sxs-lookup"><span data-stu-id="6946d-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="6946d-169">您必须为每个费用类别做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="6946d-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="6946d-170">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-170">**Decisions:**</span></span>

- <span data-ttu-id="6946d-171">费用类别是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-171">What is the expense category?</span></span> <span data-ttu-id="6946d-172">示例包括用于飞行、酒店或里程的类别。</span><span class="sxs-lookup"><span data-stu-id="6946d-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="6946d-173">此费用类别是否还可以在项目管理与核算中使用？</span><span class="sxs-lookup"><span data-stu-id="6946d-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="6946d-174">费用类型是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-174">What is the expense type?</span></span>
- <span data-ttu-id="6946d-175">费用类别的默认付款方式是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="6946d-176">是否必须逐项列出费用类别中的费用？</span><span class="sxs-lookup"><span data-stu-id="6946d-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="6946d-177">费用类别的主要默认帐户是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="6946d-178">费用类别的默认物料销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="6946d-179">此支出类别是否允许其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="6946d-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="6946d-180">如果允许其他付款方式，有哪些付款方式？</span><span class="sxs-lookup"><span data-stu-id="6946d-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="6946d-181">此费用类别中是否有子类别？</span><span class="sxs-lookup"><span data-stu-id="6946d-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="6946d-182">如果存在子类别，还必须做出以下决策：</span><span class="sxs-lookup"><span data-stu-id="6946d-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6946d-183">是否任何子类别都排除在退税之外？</span><span class="sxs-lookup"><span data-stu-id="6946d-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="6946d-184">子类别的物料销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="6946d-185">如果此费用类别还用于项目管理与核算，则回答剩余的问题。</span><span class="sxs-lookup"><span data-stu-id="6946d-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="6946d-186">否则，移至下一部分。</span><span class="sxs-lookup"><span data-stu-id="6946d-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="6946d-187">哪些成本科目用于以下费用？</span><span class="sxs-lookup"><span data-stu-id="6946d-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="6946d-188">成本</span><span class="sxs-lookup"><span data-stu-id="6946d-188">Cost</span></span>
    - <span data-ttu-id="6946d-189">工资分配</span><span class="sxs-lookup"><span data-stu-id="6946d-189">Payroll allocation</span></span>
    - <span data-ttu-id="6946d-190">WIP - 成本价值</span><span class="sxs-lookup"><span data-stu-id="6946d-190">WIP-cost value</span></span>
    - <span data-ttu-id="6946d-191">成本 - 物料</span><span class="sxs-lookup"><span data-stu-id="6946d-191">Cost-item</span></span>
    - <span data-ttu-id="6946d-192">WIP  - 成本价值 - 物料</span><span class="sxs-lookup"><span data-stu-id="6946d-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="6946d-193">应计损失</span><span class="sxs-lookup"><span data-stu-id="6946d-193">Accrued loss</span></span>
    - <span data-ttu-id="6946d-194">WIP - 应计损失</span><span class="sxs-lookup"><span data-stu-id="6946d-194">WIP-accrued loss</span></span>

- <span data-ttu-id="6946d-195">哪些收入科目用于以下各项？</span><span class="sxs-lookup"><span data-stu-id="6946d-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="6946d-196">开票收入</span><span class="sxs-lookup"><span data-stu-id="6946d-196">Invoiced revenue</span></span>
    - <span data-ttu-id="6946d-197">应计收入 - 销售价值</span><span class="sxs-lookup"><span data-stu-id="6946d-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="6946d-198">WIP - 销售价值</span><span class="sxs-lookup"><span data-stu-id="6946d-198">WIP-sales value</span></span>
    - <span data-ttu-id="6946d-199">应计收入 - 生产</span><span class="sxs-lookup"><span data-stu-id="6946d-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="6946d-200">WIP - 生产</span><span class="sxs-lookup"><span data-stu-id="6946d-200">WIP-production</span></span>
    - <span data-ttu-id="6946d-201">应计收入 - 利润</span><span class="sxs-lookup"><span data-stu-id="6946d-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="6946d-202">WIP - 利润</span><span class="sxs-lookup"><span data-stu-id="6946d-202">WIP-profit</span></span>
    - <span data-ttu-id="6946d-203">应计收入 - 预订</span><span class="sxs-lookup"><span data-stu-id="6946d-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="6946d-204">WIP - 预订</span><span class="sxs-lookup"><span data-stu-id="6946d-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="6946d-205">税金</span><span class="sxs-lookup"><span data-stu-id="6946d-205">Taxes</span></span>

<span data-ttu-id="6946d-206">对于支出相关的税，必须确定费用报表上包括或启用什么。</span><span class="sxs-lookup"><span data-stu-id="6946d-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="6946d-207">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-207">**Decisions:**</span></span>

- <span data-ttu-id="6946d-208">销售税是否包括在费用金额中？</span><span class="sxs-lookup"><span data-stu-id="6946d-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="6946d-209">是否在费用上启用退税？</span><span class="sxs-lookup"><span data-stu-id="6946d-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="6946d-210">计划总帐时，如果决定应用美国销售税和销项税规则，则无法启用支出退税。</span><span class="sxs-lookup"><span data-stu-id="6946d-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="6946d-211">（若要应用美国销售税和采用销项税规则，则将**应用销售税税务规则**选项设置为**是**。）</span><span class="sxs-lookup"><span data-stu-id="6946d-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="6946d-212">策略</span><span class="sxs-lookup"><span data-stu-id="6946d-212">Policies</span></span>

<span data-ttu-id="6946d-213">通过创建费用报表策略，当员工代表您的组织产生费用时，您可以帮助您的组织节省时间和金钱。</span><span class="sxs-lookup"><span data-stu-id="6946d-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="6946d-214">策略有助于保证员工保持在预算中，提供所有必需的信息，并且只在需要时花钱。</span><span class="sxs-lookup"><span data-stu-id="6946d-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="6946d-215">您必须为您创建的每个费用报表策略和每个费用报表审核策略做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="6946d-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="6946d-216">**决策：**</span><span class="sxs-lookup"><span data-stu-id="6946d-216">**Decisions:**</span></span>

- <span data-ttu-id="6946d-217">策略的名称是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-217">What is the name of the policy?</span></span>
- <span data-ttu-id="6946d-218">费用策略的目的是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-218">What is the expense policy for?</span></span>
- <span data-ttu-id="6946d-219">如果您已经决定启用内部公司费用，则此策略将应用于您组织中的哪个公司？</span><span class="sxs-lookup"><span data-stu-id="6946d-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="6946d-220">策略什么时候生效？</span><span class="sxs-lookup"><span data-stu-id="6946d-220">When does the policy become effective?</span></span>
- <span data-ttu-id="6946d-221">策略什么时候到期？</span><span class="sxs-lookup"><span data-stu-id="6946d-221">When does the policy expire?</span></span>
- <span data-ttu-id="6946d-222">策略规则是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-222">What is the policy rule?</span></span>
- <span data-ttu-id="6946d-223">策略规则的结果是什么？</span><span class="sxs-lookup"><span data-stu-id="6946d-223">What is the outcome of the policy rule?</span></span>

