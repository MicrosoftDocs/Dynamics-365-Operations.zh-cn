---
title: 信用额度调整
description: 本主题说明了如何设置和添加信用额度调整。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 31d83e2083806a518928dc2079c31fab6f95872c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254505"
---
# <a name="credit-limit-adjustments"></a><span data-ttu-id="23d67-103">信用额度调整</span><span class="sxs-lookup"><span data-stu-id="23d67-103">Credit limit adjustments</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23d67-104">信用额度调整使信用经理可以通过过帐流程来更新单个客户、一组客户或所有客户的信用额度和到期日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-104">Credit limit adjustments let credit managers update the credit limits and expiration dates of a single customer, a group of customers, or all customers through a posting process.</span></span> <span data-ttu-id="23d67-105">您可以添加信用额度调整条目来更新客户和客户信用组，也可以使用它们来计算自动信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-105">You can add credit limit adjustment entries to update customers and customer credit groups, or you can use them to calculate automatic credit limits.</span></span> <span data-ttu-id="23d67-106">然后可以检查条目，通过工作流发送以供批准，并过帐到客户帐户。</span><span class="sxs-lookup"><span data-stu-id="23d67-106">The entries can then be reviewed, sent for approval through a workflow, and posted to customer accounts.</span></span>

## <a name="set-up-credit-limit-adjustments"></a><span data-ttu-id="23d67-107">设置信用额度调整</span><span class="sxs-lookup"><span data-stu-id="23d67-107">Set up credit limit adjustments</span></span>

<span data-ttu-id="23d67-108">您可以在 **信用额度调整** 页面（**信用管理 \> 信用额度调整 \> 信用额度调整**）上的信用额度调整日记帐中创建条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-108">You can create entries in the Credit limit adjustment journal on the **Credit limit adjustment** page (**Credit management \> Credit limit adjustments \> Credit limit adjustments**).</span></span>

1. <span data-ttu-id="23d67-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="23d67-109">Select **New**.</span></span> <span data-ttu-id="23d67-110">此时会创建具有信用额度调整编号的新条目组。</span><span class="sxs-lookup"><span data-stu-id="23d67-110">A new group of entries is created that has a credit limit adjustment number.</span></span>
2. <span data-ttu-id="23d67-111">选择信用额度调整类型：</span><span class="sxs-lookup"><span data-stu-id="23d67-111">Select the credit limit adjustment type:</span></span>

    - <span data-ttu-id="23d67-112">选择 **信用额度** 以更改客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-112">Select **Credit limit** to change the customer's credit limit.</span></span>
    - <span data-ttu-id="23d67-113">选择 **临时信用额度** 以创建临时信用额度，而不是更改客户的当前信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-113">Select **Temporary credit limit** to create a temporary credit limit instead of changing the customer's current credit limit.</span></span> <span data-ttu-id="23d67-114">临时信用额度将在所定义的时间段内覆盖客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-114">Temporary credit limits override a customer's credit limit for a defined period.</span></span> <span data-ttu-id="23d67-115">该时间段结束后，将再次使用客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-115">After that period ends, the customer's credit limit is used again.</span></span>
3. <span data-ttu-id="23d67-116">输入描述。</span><span class="sxs-lookup"><span data-stu-id="23d67-116">Enter a description.</span></span> 

<span data-ttu-id="23d67-117">如果选中 **已过帐** 复选框，则已应用了信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-117">If the **Posted** check box is selected, the credit limits have been applied.</span></span> <span data-ttu-id="23d67-118">**审批状态** 字段指示日记帐的工作流状态。</span><span class="sxs-lookup"><span data-stu-id="23d67-118">The **Approval status** field indicates the workflow status of the journal.</span></span> <span data-ttu-id="23d67-119">工作流是可选的。</span><span class="sxs-lookup"><span data-stu-id="23d67-119">A workflow is optional.</span></span>

### <a name="add-credit-limit-adjustments"></a><span data-ttu-id="23d67-120">添加信用额度调整</span><span class="sxs-lookup"><span data-stu-id="23d67-120">Add credit limit adjustments</span></span>

<span data-ttu-id="23d67-121">要手动添加信用额度调整，请选择 **行**，然后执行下列步骤。</span><span class="sxs-lookup"><span data-stu-id="23d67-121">To manually add credit limit adjustments, select **Lines**, and then follow these steps.</span></span>

1. <span data-ttu-id="23d67-122">要为客户添加信用额度调整，请使用 **客户调整** 菜单。</span><span class="sxs-lookup"><span data-stu-id="23d67-122">To add a credit limit adjustment for a customer, use the **Customer adjustments** menu.</span></span> <span data-ttu-id="23d67-123">要为客户信用组添加信用额度，请选择 **客户信用组调整**。</span><span class="sxs-lookup"><span data-stu-id="23d67-123">To add a credit limit for a customer credit group, select **Customer credit group adjustments**.</span></span>
2. <span data-ttu-id="23d67-124">输入客户帐户作为应使用新信用额度进行更新的发票客户帐户。</span><span class="sxs-lookup"><span data-stu-id="23d67-124">Enter a customer account for the invoice customer account that should be updated with the new credit limit.</span></span> <span data-ttu-id="23d67-125">如果在步骤 1 中选择了 **客户信用组调整**，请输入客户信用组。</span><span class="sxs-lookup"><span data-stu-id="23d67-125">If you selected **Customer credit group adjustments** in step 1, enter the customer credit group.</span></span> <span data-ttu-id="23d67-126">您不能在同一日记帐行上同时输入客户帐户和客户信用组 ID。</span><span class="sxs-lookup"><span data-stu-id="23d67-126">You can't enter both a customer account and a customer credit group ID on the same journal line.</span></span>

    <span data-ttu-id="23d67-127">此时会显示当前的信用额度，并自动显示名称。</span><span class="sxs-lookup"><span data-stu-id="23d67-127">The current credit limit is shown, and the name automatically appears.</span></span>

3. <span data-ttu-id="23d67-128">输入新的信用额度，该额度将在信用额度条目过帐后替换当前信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-128">Enter the new credit limit that should replace the current credit limit when the credit limit entry is posted.</span></span>
4. <span data-ttu-id="23d67-129">输入日期以定义客户信用额度的新到期日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-129">Enter a date to define the new expiration date for the customer credit limit.</span></span> <span data-ttu-id="23d67-130">创建信用额度调整时，您必须输入信用额度到期日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-130">You must enter a credit limit expiration date when you create a credit limit adjustment.</span></span>

<span data-ttu-id="23d67-131">**审批状态** 字段指示日记帐行的工作流状态。</span><span class="sxs-lookup"><span data-stu-id="23d67-131">The **Approval status** field indicates the workflow status of the journal line.</span></span>

<span data-ttu-id="23d67-132">如果您想自动生成信用额度调整，可以使用操作窗格上的 **生成** 菜单。</span><span class="sxs-lookup"><span data-stu-id="23d67-132">If you want the credit limit adjustments to be automatically generated, you can use the **Generate** menu on the Action Pane.</span></span>
 
### <a name="add-temporary-credit-limit-adjustments"></a><span data-ttu-id="23d67-133">添加临时信用额度调整</span><span class="sxs-lookup"><span data-stu-id="23d67-133">Add temporary credit limit adjustments</span></span>

<span data-ttu-id="23d67-134">要手动添加临时信用额度调整，请针对日记帐行执行下列步骤。</span><span class="sxs-lookup"><span data-stu-id="23d67-134">To manually add temporary credit limit adjustments, follow these steps for the journal lines.</span></span>

1. <span data-ttu-id="23d67-135">要为客户添加信用额度调整，请使用 **客户调整** 菜单。</span><span class="sxs-lookup"><span data-stu-id="23d67-135">To add a credit limit adjustment for a customer, use the **Customer adjustments** menu.</span></span> <span data-ttu-id="23d67-136">要为客户信用组添加信用额度，请选择 **客户信用组调整**。</span><span class="sxs-lookup"><span data-stu-id="23d67-136">To add a credit limit for a customer credit group, select **Customer credit group adjustments**.</span></span>
2. <span data-ttu-id="23d67-137">输入客户帐户作为应使用新信用额度进行更新的发票客户帐户。</span><span class="sxs-lookup"><span data-stu-id="23d67-137">Enter a customer account for the invoice customer account that should be updated with the new credit limit.</span></span> <span data-ttu-id="23d67-138">如果在步骤 1 中选择了 **客户信用组调整**，请输入客户信用组。</span><span class="sxs-lookup"><span data-stu-id="23d67-138">If you selected **Customer credit group adjustments** in step 1, enter the customer credit group.</span></span> <span data-ttu-id="23d67-139">您不能在同一日记帐行上同时输入客户帐户和客户信用组 ID。</span><span class="sxs-lookup"><span data-stu-id="23d67-139">You can't enter both a customer account and a customer credit group ID on the same journal line.</span></span>

    <span data-ttu-id="23d67-140">如果已经存在有效或将来的临时信用额度，则将为每个临时信用额度显示当前临时信用额度和日期范围。</span><span class="sxs-lookup"><span data-stu-id="23d67-140">If an active or future temporary credit limit already exists, the current temporary credit limit and date ranges appear for each temporary credit limit.</span></span> <span data-ttu-id="23d67-141">名称会自动出现。</span><span class="sxs-lookup"><span data-stu-id="23d67-141">The name automatically appears.</span></span>

3. <span data-ttu-id="23d67-142">输入应该替换当前信用额度的新信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-142">Enter the new credit limit that should replace the current credit limit.</span></span>
4. <span data-ttu-id="23d67-143">在 **新开始日期** 和 **新结束日期** 字段中，定义高级信用额度的有效期限。</span><span class="sxs-lookup"><span data-stu-id="23d67-143">In the **New from date** and **New to date** fields, define the period when the advanced credit limit is valid.</span></span> <span data-ttu-id="23d67-144">创建信用额度调整日记帐时，您必须输入信用额度到期日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-144">You must enter credit limit expiration dates when you create a credit limit adjustment journal.</span></span>

<span data-ttu-id="23d67-145">**审批状态** 字段指示日记帐行的工作流状态。</span><span class="sxs-lookup"><span data-stu-id="23d67-145">The **Approval status** field indicates the workflow status of the journal line.</span></span>

## <a name="generate-credit-limit-adjustments"></a><span data-ttu-id="23d67-146">生成信用额度调整</span><span class="sxs-lookup"><span data-stu-id="23d67-146">Generate credit limit adjustments</span></span>

<span data-ttu-id="23d67-147">您还可以自动调整信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-147">You can also have credit limits automatically adjusted.</span></span> <span data-ttu-id="23d67-148">在操作窗格上，选择 **生成**，然后选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="23d67-148">On the Action Pane, select **Generate**, and then select one of the following options:</span></span>

- <span data-ttu-id="23d67-149">从现有客户</span><span class="sxs-lookup"><span data-stu-id="23d67-149">From existing customer</span></span>
- <span data-ttu-id="23d67-150">从现有客户信用组</span><span class="sxs-lookup"><span data-stu-id="23d67-150">From existing customer credit group</span></span>
- <span data-ttu-id="23d67-151">自动信用额度</span><span class="sxs-lookup"><span data-stu-id="23d67-151">Automatic credit limits</span></span>

### <a name="from-existing-customer"></a><span data-ttu-id="23d67-152">从现有客户</span><span class="sxs-lookup"><span data-stu-id="23d67-152">From existing customer</span></span>

<span data-ttu-id="23d67-153">您可以从现有客户创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="23d67-153">You can create journal lines from existing customers.</span></span> <span data-ttu-id="23d67-154">当您选择 **生成 \> 从现有客户** 时，将出现一个对话框，您可以在其中提供用于选择客户和计算新限额的标准。</span><span class="sxs-lookup"><span data-stu-id="23d67-154">When you select **Generate \> From existing customer**, a dialog box appears where you can provide criteria for selecting customers and calculating the new limits.</span></span>

1. <span data-ttu-id="23d67-155">输入一个调整值以对信用额度加减金额。</span><span class="sxs-lookup"><span data-stu-id="23d67-155">Enter an adjustment value to add or subtract an amount from the credit limit.</span></span> <span data-ttu-id="23d67-156">输入负值可以减小当前信用额度，输入正值可以增大当前信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-156">Enter a negative value to decrease the current credit limit or a positive value to increase it.</span></span>
2. <span data-ttu-id="23d67-157">在 **值类型** 字段中，选择应如何使用在步骤 1 中输入的值来计算新信用额度：</span><span class="sxs-lookup"><span data-stu-id="23d67-157">In the **Value type** field, select how the value that you entered in step 1 should be used to calculate the new credit limit:</span></span>

    - <span data-ttu-id="23d67-158">选择 **固定值** 以按金额更改信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-158">Select **Fixed value** to change the credit limit by an amount.</span></span>
    - <span data-ttu-id="23d67-159">选择 **百分比** 以按百分比更改信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-159">Select **Percentage** to change the credit limit by a percentage.</span></span>

3. <span data-ttu-id="23d67-160">输入用于舍入计算出的信用额度的值。</span><span class="sxs-lookup"><span data-stu-id="23d67-160">Enter a value that is used to round the calculated credit limit.</span></span> <span data-ttu-id="23d67-161">例如，输入 **10.00** 会将信用额度四舍五入成最接近的 10.00 货币单位。</span><span class="sxs-lookup"><span data-stu-id="23d67-161">For example, enter **10.00** to round the credit limit to the nearest 10.00 currency units.</span></span>
4. <span data-ttu-id="23d67-162">设置 **舍入形式** 字段以指定余数应向上还是向下舍入。</span><span class="sxs-lookup"><span data-stu-id="23d67-162">Set the **Rounding form** field to specify whether the remainder should be rounded up or down.</span></span>
5. <span data-ttu-id="23d67-163">选择用于调整日期的方法。</span><span class="sxs-lookup"><span data-stu-id="23d67-163">Select the method that is used to adjust dates.</span></span>

    - <span data-ttu-id="23d67-164">如果选择 **绝对**，您可以输入定义信用额度日期范围的日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-164">If you select **Absolute**, you can enter dates that define the date range for the credit limits.</span></span>
    - <span data-ttu-id="23d67-165">如果选择 **相对**，则可以输入范围的偏移日期。</span><span class="sxs-lookup"><span data-stu-id="23d67-165">If you select **Relative**, you can enter offset dates for the range.</span></span> <span data-ttu-id="23d67-166">信用额度的当前日期范围将通过偏移得到调整。</span><span class="sxs-lookup"><span data-stu-id="23d67-166">The current date range for the credit limit will be adjusted by the offset.</span></span>

6. <span data-ttu-id="23d67-167">使用 **要包括的记录** 快速选项卡筛选包含的客户列表。</span><span class="sxs-lookup"><span data-stu-id="23d67-167">Use the **Records to include** FastTab to filter the list of customers that are included.</span></span> <span data-ttu-id="23d67-168">如果您不包括筛选器，则将为所有客户生成信用额度条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-168">If you don't include filters, credit limit entries will be generated for all customers.</span></span>
7. <span data-ttu-id="23d67-169">选择 **确定** 以创建信用额度调整条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-169">Select **OK** to create the credit limit adjustment entries.</span></span>

### <a name="from-existing-customer-credit-group"></a><span data-ttu-id="23d67-170">从现有客户信用组</span><span class="sxs-lookup"><span data-stu-id="23d67-170">From existing customer credit group</span></span>

<span data-ttu-id="23d67-171">您可以从现有客户信用组创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="23d67-171">You can create journal lines from existing customer credit groups.</span></span> <span data-ttu-id="23d67-172">当您选择 **生成 \> 从现有客户信用组** 时，将出现一个对话框，您可以在其中提供用于选择客户信用组和计算新额度的标准。</span><span class="sxs-lookup"><span data-stu-id="23d67-172">When you select **Generate \> From existing customer credit group**, a dialog appears where you can provide criteria for selecting customer credit groups and calculating the new limits.</span></span> <span data-ttu-id="23d67-173">这些标准与从现有客户创建日记帐行所使用的标准相同。</span><span class="sxs-lookup"><span data-stu-id="23d67-173">The criteria are the same criteria that are used to create journal lines from existing customers.</span></span> <span data-ttu-id="23d67-174">请参见上一部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="23d67-174">See the steps in the previous section.</span></span>

### <a name="automatic-credit-limits"></a><span data-ttu-id="23d67-175">自动信用额度</span><span class="sxs-lookup"><span data-stu-id="23d67-175">Automatic credit limits</span></span>

<span data-ttu-id="23d67-176">您可以创建自动信用额度来定义和更新客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-176">You can create automatic credit limits to define and update customer credit limits.</span></span> <span data-ttu-id="23d67-177">自动信用额度是为风险组创建的，它们基于评分组中使用的特定值。</span><span class="sxs-lookup"><span data-stu-id="23d67-177">The automatic credit limits are created for a risk group, and they are based on specific values that are used in the scoring groups.</span></span> <span data-ttu-id="23d67-178">您可以使用这些自动信用额度生成信用额度条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-178">You can use these automatic credit limits to generate credit limit entries.</span></span> <span data-ttu-id="23d67-179">如果已将客户分配给特定的风险组，并且客户的信用信息与自动信用额度标准匹配，则会创建一个信用额度调整条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-179">If a customer has been assigned to a specific risk group, and the customer's credit information matches the criteria for an automatic credit limit, a credit limit adjustment entry is created.</span></span>

#### <a name="create-automatic-credit-limits"></a><span data-ttu-id="23d67-180">创建自动信用额度</span><span class="sxs-lookup"><span data-stu-id="23d67-180">Create automatic credit limits</span></span>

<span data-ttu-id="23d67-181">您可以使用信用额度调整来创建自动信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-181">You create automatic credit limits by using credit limit adjustments.</span></span> <span data-ttu-id="23d67-182">当您选择 **生成 \> 自动信用额度** 时，将出现一个对话框，您可以在其中设置新信用额度的到期日期，新信用额度将根据分配给客户的风险组来创建。</span><span class="sxs-lookup"><span data-stu-id="23d67-182">When you select **Generate \> Automatic credit limits**, a dialog appears where you can set an expiration date for the new credit limits that will be created based on the risk groups that customers are assigned to.</span></span> <span data-ttu-id="23d67-183">完成后，选择 **确定** 以创建信用额度调整行。</span><span class="sxs-lookup"><span data-stu-id="23d67-183">When you've finished, select **OK** to create the credit limit adjustment lines.</span></span>

### <a name="post-adjustments"></a><span data-ttu-id="23d67-184">过帐调整</span><span class="sxs-lookup"><span data-stu-id="23d67-184">Post adjustments</span></span>

<span data-ttu-id="23d67-185">创建信用额度调整行后，您可以使用操作窗格上的 **过帐** 按钮过帐条目并更新客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="23d67-185">After you've created credit limit adjustment lines, you can use the **Post** button on the Action Pane to post the entries and update the customer credit limits.</span></span> <span data-ttu-id="23d67-186">但是，如果您已设置工作流，则必须选择操作窗格上的 **工作流 \> 提交**，以提交审批日记帐。</span><span class="sxs-lookup"><span data-stu-id="23d67-186">However, if you've set up a workflow, you must select **Workflow \> Submit** on the Action Pane to submit the journal for approval.</span></span>

### <a name="credit-limit-adjustments-workflows"></a><span data-ttu-id="23d67-187">信用额度调整工作流</span><span class="sxs-lookup"><span data-stu-id="23d67-187">Credit limit adjustments workflows</span></span>

<span data-ttu-id="23d67-188">**信用额度调整** 工作流可用于通过工作流批准流程发送信用额度调整。</span><span class="sxs-lookup"><span data-stu-id="23d67-188">The **Credit limit adjustments** workflows can be used to send credit limit adjustments through a workflow approval process.</span></span> <span data-ttu-id="23d67-189">您可以在 **信用管理工作流** 页（**信用管理 \> 设置 \> 信用管理工作流**）上创建两个工作流：</span><span class="sxs-lookup"><span data-stu-id="23d67-189">You can create two workflows on the **Credit management worfklow** page (**Credit management \> Setup \> Credit management worfklow**):</span></span>

- <span data-ttu-id="23d67-190">**信用额度调整** – 此工作流可用于在标题级别批准条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-190">**Credit limit adjustments** – This workflow can be used to approve entries at the header level.</span></span>
- <span data-ttu-id="23d67-191">**信用额度调整行** – 此工作流可用于批准调整条目，以便可以根据工作流中的标准由不同人员批准这些条目。</span><span class="sxs-lookup"><span data-stu-id="23d67-191">**Credit limit adjustments line** – This workflow can be used to approve the adjustment entries so that the entries can be approved by different people, based on the criteria in the workflow.</span></span>

> [!NOTE]
> <span data-ttu-id="23d67-192">当您创建 **信用额度调整** 工作流时，您可以对其进行设置，以便在批准行之后自动过帐调整。</span><span class="sxs-lookup"><span data-stu-id="23d67-192">When you create the **Credit limit adjustments** workflow, you can set it up so that the adjustments are automatically posted after the lines are approved.</span></span> <span data-ttu-id="23d67-193">只需在工作流中包括 **自动过帐日记帐** 任务即可。</span><span class="sxs-lookup"><span data-stu-id="23d67-193">Just include the **Post Journal automatically** task in the workflow.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]