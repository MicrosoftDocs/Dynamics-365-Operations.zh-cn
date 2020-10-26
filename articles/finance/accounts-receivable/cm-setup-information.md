---
title: 信用管理设置
description: 本主题描述了信用管理所需的设置。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1d33dbbd37daaa75f4b64359194a2328728b27f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977879"
---
# <a name="credit-management-setup"></a><span data-ttu-id="5c846-103">信用管理设置</span><span class="sxs-lookup"><span data-stu-id="5c846-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="5c846-104">信用管理工作流</span><span class="sxs-lookup"><span data-stu-id="5c846-104">Credit management workflows</span></span>

<span data-ttu-id="5c846-105">转到**信用和收款 \> 设置 \> 信用管理工作流**以定义用于管理信用额度调整的工作流。</span><span class="sxs-lookup"><span data-stu-id="5c846-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="5c846-106">您可以创建一个工作流，以便能够通过一次批准来批准一批信用额度调整。</span><span class="sxs-lookup"><span data-stu-id="5c846-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="5c846-107">您可以在行级别添加工作流，以便可以分别批准信用额度调整。</span><span class="sxs-lookup"><span data-stu-id="5c846-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="5c846-108">您可以创建下达工作流以将暂停自动传送到工作流程。</span><span class="sxs-lookup"><span data-stu-id="5c846-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="5c846-109">锁定规则</span><span class="sxs-lookup"><span data-stu-id="5c846-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="5c846-110">对付款期限进行排名</span><span class="sxs-lookup"><span data-stu-id="5c846-110">Ranking payment terms</span></span>

<span data-ttu-id="5c846-111">如果订单上的付款期限与客户的默认付款期限不匹配，则可以暂停销售订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="5c846-112">但是，有时付款期限会有所不同，但又非常相似，以至于您不想暂停订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="5c846-113">您可以对付款期限进行排名，以使其中一些具有相同的排名，而另一些具有更高或更低的排名。</span><span class="sxs-lookup"><span data-stu-id="5c846-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="5c846-114">如果付款期限排名有效，且在订单上的付款期限排名高于客户的默认付款期限排名，销售订单将暂停。</span><span class="sxs-lookup"><span data-stu-id="5c846-114">If the rankings for payment terms are active, and if the payment terms on the order have a higher rank than the default payment terms for the customer, the sales order will be put on hold.</span></span>

<span data-ttu-id="5c846-115">要设置付款期限排名，请转到**信用和收款 \> 设置 \> 信用管理设置 \> 付款期限排名**</span><span class="sxs-lookup"><span data-stu-id="5c846-115">To set up the payment terms ranking go to **Credit and collections \> Setup \> Credit management setup \>Rank payment terms**</span></span>  

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="5c846-116">对结算折扣进行排名</span><span class="sxs-lookup"><span data-stu-id="5c846-116">Ranking settlement discounts</span></span>

<span data-ttu-id="5c846-117">如果订单上的现金折扣与客户的默认现金折扣不匹配，则可以暂停销售订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-117">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="5c846-118">但是，有时现金折扣会有所不同，但又非常相似，以至于您不想暂停订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-118">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="5c846-119">您可以对现金折扣进行排名，以使其中一些具有相同的排名，而另一些具有更高或更低的排名。</span><span class="sxs-lookup"><span data-stu-id="5c846-119">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="5c846-120">如果结算折扣排名有效，且在订单上的现金折扣排名高于客户的默认现金折扣排名，销售订单将暂停。</span><span class="sxs-lookup"><span data-stu-id="5c846-120">If rankings for settlement discounts are active, and if the cash discount on the order has a higher rank than the default cash discount for the customer, the sales order will be put on hold.</span></span>

<span data-ttu-id="5c846-121">要设置付款期限排名，请转到**信用和收款 \> 设置 \> 信用管理设置 \> 结算折扣排名**</span><span class="sxs-lookup"><span data-stu-id="5c846-121">To set up the payment terms ranking go to **Credit and collections \> Setup \> Credit management setup \>Rank settlement discounts**</span></span>  

## <a name="reasons"></a><span data-ttu-id="5c846-122">原因</span><span class="sxs-lookup"><span data-stu-id="5c846-122">Reasons</span></span>

<span data-ttu-id="5c846-123">信用管理中使用了一些类型的原因：</span><span class="sxs-lookup"><span data-stu-id="5c846-123">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="5c846-124">暂停原因表明为什么暂停销售订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-124">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="5c846-125">从暂停中下达订单后，会将下达原因分配给该订单。</span><span class="sxs-lookup"><span data-stu-id="5c846-125">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="5c846-126">状态原因表明为什么将帐户状态分配给客户。</span><span class="sxs-lookup"><span data-stu-id="5c846-126">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="5c846-127">您可以在**信用管理原因**页（**信用和收款 \> 设置 \> 信用管理设置 \> 信用管理原因**）上设置原因。</span><span class="sxs-lookup"><span data-stu-id="5c846-127">You can set up reasons on the **Credit management reasons** page (**Credit and collections \> Setup \> Credit management setup \> Credit management reasons**).</span></span>

1. <span data-ttu-id="5c846-128">在**原因类型**字段中，选择原因类型：**暂停**、**下达**或**状态**。</span><span class="sxs-lookup"><span data-stu-id="5c846-128">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="5c846-129">在**原因**字段中，输入原因的名称。</span><span class="sxs-lookup"><span data-stu-id="5c846-129">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="5c846-130">在**说明**字段中，输入原因代码的描述。</span><span class="sxs-lookup"><span data-stu-id="5c846-130">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="5c846-131">信用管理组</span><span class="sxs-lookup"><span data-stu-id="5c846-131">Credit management groups</span></span>

<span data-ttu-id="5c846-132">信用管理组用于标识具有相同信用管理属性的客户或客户组。</span><span class="sxs-lookup"><span data-stu-id="5c846-132">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="5c846-133">例如，信用管理组可用于为客户确定锁定和排除信用管理规则。</span><span class="sxs-lookup"><span data-stu-id="5c846-133">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="5c846-134">您可以在**信用管理组**页（**信用和收款 \> 设置 > 信用管理设置 \> 信用管理组**）上创建信用管理组。</span><span class="sxs-lookup"><span data-stu-id="5c846-134">You can create credit management groups on the **Credit management groups** page (**Credit and collections \> Setup> Credit management setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="5c846-135">选择**新建**创建行。</span><span class="sxs-lookup"><span data-stu-id="5c846-135">Select **New** to create a line.</span></span>
2. <span data-ttu-id="5c846-136">输入此组的 ID。</span><span class="sxs-lookup"><span data-stu-id="5c846-136">Enter an ID for the group.</span></span> <span data-ttu-id="5c846-137">该 ID 最多可包含 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="5c846-137">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="5c846-138">在**描述**字段中，输入组的名称。</span><span class="sxs-lookup"><span data-stu-id="5c846-138">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="5c846-139">该名称最多可包含 60 个字符。</span><span class="sxs-lookup"><span data-stu-id="5c846-139">The name can have up to 60 characters.</span></span>

<span data-ttu-id="5c846-140">信用管理组已分配给**所有客户**页（**应收帐款 \> 客户 \> 所有客户**）的**信用和收款**快速选项卡上的客户。</span><span class="sxs-lookup"><span data-stu-id="5c846-140">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="5c846-141">帐户状态</span><span class="sxs-lookup"><span data-stu-id="5c846-141">Account statuses</span></span>

<span data-ttu-id="5c846-142">您可以创建帐户状态以识别客户帐户的信用状况。</span><span class="sxs-lookup"><span data-stu-id="5c846-142">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="5c846-143">您可以定义状态及其对开票和交货暂停流程的影响。</span><span class="sxs-lookup"><span data-stu-id="5c846-143">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="5c846-144">帐户状态还可以用于确定客户的锁定规则。</span><span class="sxs-lookup"><span data-stu-id="5c846-144">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="5c846-145">您可以在**帐户状态**页（**信用和收款 \> 设置 > 信用管理设置 \> 帐户状态**）上创建帐户状态。</span><span class="sxs-lookup"><span data-stu-id="5c846-145">You can create account statuses on the **Account statuses** page (**Credit and collections \> Setup> Credit management setup \> Account statuses**).</span></span>

1. <span data-ttu-id="5c846-146">添加帐户状态，然后输入描述以表示客户的信用状况。</span><span class="sxs-lookup"><span data-stu-id="5c846-146">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="5c846-147">例如，使用**正常**表示客户信誉良好，未结订单会经过标准信用管理程序处理。</span><span class="sxs-lookup"><span data-stu-id="5c846-147">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="5c846-148">在**开票**和**交货暂停**字段中，选择具有此帐户状态的客户应存在的暂停类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-148">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="5c846-149">当应用信用额度规则后，您可以暂停所有处理，仅暂停发票处理或不暂停任何处理。</span><span class="sxs-lookup"><span data-stu-id="5c846-149">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="5c846-150">计分组</span><span class="sxs-lookup"><span data-stu-id="5c846-150">Scoring groups</span></span>

<span data-ttu-id="5c846-151">您可以设置计分组以定义风险因素以及用于衡量风险因素的标准。</span><span class="sxs-lookup"><span data-stu-id="5c846-151">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="5c846-152">将有关客户的信息应用于计分组后，会为每个风险因素计算一个分数，并用此分数将客户置于风险组中。</span><span class="sxs-lookup"><span data-stu-id="5c846-152">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="5c846-153">风险组可用于识别信用价值并计算自动信用额度。</span><span class="sxs-lookup"><span data-stu-id="5c846-153">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="5c846-154">您可以在**计分组**页（**信用和收款 \> 设置 \> 信用管理设置 \> 风险 \> 计分组**）上创建计分组。</span><span class="sxs-lookup"><span data-stu-id="5c846-154">You can create scoring groups on the **Scoring groups** page (**Credit and collections \> Setup \> Credit management setup \> Risk \> Scoring groups**).</span></span>

1. <span data-ttu-id="5c846-155">创建计分组并为其输入名称。</span><span class="sxs-lookup"><span data-stu-id="5c846-155">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="5c846-156">输入描述以进一步描述计分组。</span><span class="sxs-lookup"><span data-stu-id="5c846-156">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="5c846-157">选择组类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-157">Select a group type.</span></span> <span data-ttu-id="5c846-158">有八种预定义类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-158">There are eight predefined types.</span></span> <span data-ttu-id="5c846-159">您也可以选择**用户自定义**以定义更适合您的组织的组类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-159">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="5c846-160">选择分数类型以定义计分组如何计算风险分数。</span><span class="sxs-lookup"><span data-stu-id="5c846-160">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="5c846-161">选项如下：</span><span class="sxs-lookup"><span data-stu-id="5c846-161">The following options are available:</span></span>

    - <span data-ttu-id="5c846-162">**范围** – 使用此选项可以定义应该用于计算分数的值范围。</span><span class="sxs-lookup"><span data-stu-id="5c846-162">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="5c846-163">**用户自定义** – 使用此选项可手动定义应该用作分数的值列表。</span><span class="sxs-lookup"><span data-stu-id="5c846-163">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="5c846-164">如果选择了**范围**作为分数类型，请添加行以定义值的范围和相应的分数。</span><span class="sxs-lookup"><span data-stu-id="5c846-164">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="5c846-165">在**起始值**字段中，指定范围内的最小值。</span><span class="sxs-lookup"><span data-stu-id="5c846-165">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="5c846-166">在**结束值**字段中，指定范围内的最大值。</span><span class="sxs-lookup"><span data-stu-id="5c846-166">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="5c846-167">在**分数**字段中，输入提供的值在“从”/“到”范围内时应分配的分数。</span><span class="sxs-lookup"><span data-stu-id="5c846-167">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="5c846-168">如果选择了**用户自定义**作为分数类型，请添加行以定义用户自定义值和相应的分数。</span><span class="sxs-lookup"><span data-stu-id="5c846-168">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="5c846-169">在**值**字段中，输入应从客户信息中提供的用户定义值。</span><span class="sxs-lookup"><span data-stu-id="5c846-169">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="5c846-170">在**分数**字段中，输入提供的值在“从”/“到”范围内时应分配的分数。</span><span class="sxs-lookup"><span data-stu-id="5c846-170">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-classification"></a><span data-ttu-id="5c846-171">风险分类</span><span class="sxs-lookup"><span data-stu-id="5c846-171">Risk classification</span></span>

<span data-ttu-id="5c846-172">您可以根据客户的风险评分定义可以分配给客户的风险评估。</span><span class="sxs-lookup"><span data-stu-id="5c846-172">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="5c846-173">通过将客户信息与每个计分组进行比较来计算风险评分。</span><span class="sxs-lookup"><span data-stu-id="5c846-173">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="5c846-174">合计分数，然后将总分数与风险组设置中的值进行比较，以识别客户所属的风险组。</span><span class="sxs-lookup"><span data-stu-id="5c846-174">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="5c846-175">然后，使用风险组评分为客户定义信用管理锁定和排除规则。</span><span class="sxs-lookup"><span data-stu-id="5c846-175">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="5c846-176">您可以在**风险评估**页（**信用和收款 \> 设置 \> 信用管理设置 \> 风险 \> 风险分类**）上设置风险组。</span><span class="sxs-lookup"><span data-stu-id="5c846-176">You can set up risk groups on the **Risk assessments** page (**Credit and collections \> Setup \> Credit management setup \> Risk \> Risk classification**).</span></span>

1. <span data-ttu-id="5c846-177">输入风险组 ID。</span><span class="sxs-lookup"><span data-stu-id="5c846-177">Enter a risk group ID.</span></span>
2. <span data-ttu-id="5c846-178">输入描述以进一步说明风险组。</span><span class="sxs-lookup"><span data-stu-id="5c846-178">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="5c846-179">输入用于确定哪些客户属于风险组的分数范围。</span><span class="sxs-lookup"><span data-stu-id="5c846-179">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="5c846-180">选择风险组指标以指定代表风险组的符号。</span><span class="sxs-lookup"><span data-stu-id="5c846-180">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="5c846-181">担保/保险类型</span><span class="sxs-lookup"><span data-stu-id="5c846-181">Guarantee/insurance types</span></span>

<span data-ttu-id="5c846-182">您可以在**担保/保险类型**页（**信用和收款 \> 设置 \> 信用管理设置 \> 保险和担保 \> 保险和担保类型**）上设置担保/保险类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-182">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit and collections \> Setup \> Credit management setup \> Insurance and guarantees \> Insurance and guarantee types**).</span></span>

1. <span data-ttu-id="5c846-183">输入标识担保人或保险经纪人姓名的担保或保险类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-183">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="5c846-184">输入描述以描述担保人/保险经纪人。</span><span class="sxs-lookup"><span data-stu-id="5c846-184">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="5c846-185">覆盖范围类型</span><span class="sxs-lookup"><span data-stu-id="5c846-185">Coverage types</span></span>

<span data-ttu-id="5c846-186">覆盖范围类型可用于进一步对保险单进行分类。</span><span class="sxs-lookup"><span data-stu-id="5c846-186">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="5c846-187">它们不能与保证一起使用。</span><span class="sxs-lookup"><span data-stu-id="5c846-187">They can't be used with guarantees.</span></span>

<span data-ttu-id="5c846-188">您可以在**覆盖范围类型**页（**信用和收款 \> 设置 \> 信用管理设置 \> 保险和担保 \> 覆盖范围类型**）上添加覆盖范围类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-188">You can add coverage types on the **Coverage types** page (**Credit and collections \> Setup \> Credit management setup \> Insurance and guarantees \> Coverage types**).</span></span>

1. <span data-ttu-id="5c846-189">输入覆盖范围类型以标识应添加为保险或担保的覆盖范围的类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-189">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="5c846-190">输入描述以描述覆盖范围类型。</span><span class="sxs-lookup"><span data-stu-id="5c846-190">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="5c846-191">自动信用额度</span><span class="sxs-lookup"><span data-stu-id="5c846-191">Automatic credit limits</span></span>

<span data-ttu-id="5c846-192">您可以在**自动信用额度**页（**信用和收款 \> 设置 \> 信用管理设置 \> 风险 \> 自动信用额度**）上创建自动信用额度标准。</span><span class="sxs-lookup"><span data-stu-id="5c846-192">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit and collections \> Setup \> Credit management setup \> Risk \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="5c846-193">选择应将自动信用额度分配到的风险组。</span><span class="sxs-lookup"><span data-stu-id="5c846-193">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="5c846-194">选择自动信用额度的货币。</span><span class="sxs-lookup"><span data-stu-id="5c846-194">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="5c846-195">您可以为同一风险组创建多个以不同货币为单位的自动信用限额。</span><span class="sxs-lookup"><span data-stu-id="5c846-195">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="5c846-196">输入代表可用于此自动信用限额的最大公司收入的收入金额。</span><span class="sxs-lookup"><span data-stu-id="5c846-196">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="5c846-197">创建信用额度后，会将收入金额与在**金融**页（**应收帐款 \> 所有客户 \> 选择客户 \> 常规 \> 统计 \> 金融**）上找到的收入值进行比较。</span><span class="sxs-lookup"><span data-stu-id="5c846-197">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="5c846-198">系统使用**概览**部分中的最新值。</span><span class="sxs-lookup"><span data-stu-id="5c846-198">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="5c846-199">请按照以下步骤添加代表将基于所选标准生成的信用额度的行。</span><span class="sxs-lookup"><span data-stu-id="5c846-199">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="5c846-200">选择计分组以定义应该用于计算信用额度的客户信息。</span><span class="sxs-lookup"><span data-stu-id="5c846-200">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="5c846-201">选择比较运算符以定义应如何评估计分组信息。</span><span class="sxs-lookup"><span data-stu-id="5c846-201">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="5c846-202">输入应该与为计分组指定的值进行比较的值。</span><span class="sxs-lookup"><span data-stu-id="5c846-202">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="5c846-203">如果客户信息与为计分组指定的值匹配，请输入应分配的信用额度。</span><span class="sxs-lookup"><span data-stu-id="5c846-203">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="5c846-204">例如，您为**低**计分组创建自动信用额度。</span><span class="sxs-lookup"><span data-stu-id="5c846-204">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="5c846-205">如果营业年数是计分组之一，则可以定义一个行，以在客户已营业五年的情况下分配一个值为 100,000 的信用额度；可以定义另一个行，以在客户已营业 10 年的情况下分配一个值为 200,000 的信用额度。</span><span class="sxs-lookup"><span data-stu-id="5c846-205">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
