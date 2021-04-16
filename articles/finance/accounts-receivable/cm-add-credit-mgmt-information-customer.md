---
title: 为客户添加信用管理信息
description: 本主题说明如何为客户添加信用管理信息。
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dc734775e0ffe0388763d788a6eba90c1449ed1c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820585"
---
# <a name="add-credit-management-information-for-customers"></a><span data-ttu-id="66506-103">为客户添加信用管理信息</span><span class="sxs-lookup"><span data-stu-id="66506-103">Add credit management information for customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66506-104">设置控制信用管理的参数后，可以为每个客户添加更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="66506-104">After you've set up the parameters that control credit management, you can add more details for each customer.</span></span> <span data-ttu-id="66506-105">这些详细信息控制信贷管理流程，并且还提供其他信息，以帮助收款团队的成员管理客户。</span><span class="sxs-lookup"><span data-stu-id="66506-105">These details control the credit management processes, and they also provide additional information that helps members of the collections team manage customers.</span></span>

## <a name="customer-information"></a><span data-ttu-id="66506-106">客户信息</span><span class="sxs-lookup"><span data-stu-id="66506-106">Customer information</span></span>

<span data-ttu-id="66506-107">您可以在 **所有客户** 页面（**应收帐款 \> 客户\> 所有客户**）的 **信用和收款** 快速选项卡上添加客户详细信息。</span><span class="sxs-lookup"><span data-stu-id="66506-107">You can add the customer details on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

1. <span data-ttu-id="66506-108">如果客户不应受任何信用额度测试的限制，请将 **无限信用额度** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="66506-108">Set the **Unlimited credit limit** option to **Yes** if the customer should not be limited by any credit limit tests.</span></span>
2. <span data-ttu-id="66506-109">将 **从信用管理中排除** 选项设置为 **是**，以将客户排除在信用管理流程中通常发生的任何操作之外。</span><span class="sxs-lookup"><span data-stu-id="66506-109">Set the **Exclude from credit management** option to **Yes** to exclude the customer from any actions that usually occur during credit management processes.</span></span>
3. <span data-ttu-id="66506-110">为客户选择信用管理组。</span><span class="sxs-lookup"><span data-stu-id="66506-110">Select the credit management group for the customer.</span></span>
4. <span data-ttu-id="66506-111">要计算以客户货币为单位的信用额度，请在 **客户货币信用额度** 字段中输入客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-111">To calculate the credit limit in the customer's currency, in the **Credit limit in customer's currency** field, enter the customer's credit limit.</span></span> <span data-ttu-id="66506-112">将使用由在“信用管理参数”中选择的信用额度汇率类型所定义的汇率转换公司货币信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-112">The credit limit in the company currency will be converted by using the exchange rates that are defined by the credit limit exchange rate type that is selected in the Credit management parameters.</span></span>
5. <span data-ttu-id="66506-113">在 **上次审核日期** 字段中，输入信用经理上次审查客户信用额度的日期。</span><span class="sxs-lookup"><span data-stu-id="66506-113">In the **Last review date** field, enter the date when the customer's credit limit was last reviewed by a credit manager.</span></span>
6. <span data-ttu-id="66506-114">在 **已计划的下一次审查日期** 字段中，输入计划对客户进行信用审核和更新的日期。</span><span class="sxs-lookup"><span data-stu-id="66506-114">In the **Next scheduled review date** field, enter the date when the customer is scheduled for credit review and update.</span></span>
7. <span data-ttu-id="66506-115">在 **合格信用额度** 字段中，根据您对该客户的信用记录的审核，输入可以分配给该客户的最高信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-115">In the **Eligible credit limit** field, enter the highest credit limit that can be assigned to the customer, based on your review of that customer's credit history.</span></span> <span data-ttu-id="66506-116">合格信用额度可能与 **信用和收款** 快速选项卡上显示的信用额度不同。</span><span class="sxs-lookup"><span data-stu-id="66506-116">The eligible credit limit can differ from the credit limit that is shown on the **Credit and collections** FastTab.</span></span>
8. <span data-ttu-id="66506-117">在 **合格信用额度货币** 字段中，输入合格信用额度的货币。</span><span class="sxs-lookup"><span data-stu-id="66506-117">In the **Eligible credit limit currency** field, enter the currency of the eligible credit limit.</span></span>
9. <span data-ttu-id="66506-118">在 **合格信用额度日期** 字段中，输入合格信用额度的创建日期。</span><span class="sxs-lookup"><span data-stu-id="66506-118">In the **Eligible credit limit date** field, enter the date when the eligible credit limit was created.</span></span>
10. <span data-ttu-id="66506-119">在 **信用帐户状态** 字段中，输入客户的信用帐户状态。</span><span class="sxs-lookup"><span data-stu-id="66506-119">In the **Credit account status** field, enter the credit account status of the customer.</span></span>
11. <span data-ttu-id="66506-120">在 **状态原因** 字段中，输入与帐户状态相关联的原因。</span><span class="sxs-lookup"><span data-stu-id="66506-120">In the **Status reason** field, enter the reason that is associated the account status.</span></span>
12. <span data-ttu-id="66506-121">将 **与机构相关** 选项设置为 **是**，以指示当前已将客户分配给信贷机构。</span><span class="sxs-lookup"><span data-stu-id="66506-121">Set the **With agency** option to **Yes** to indicate that the customer is currently assigned to a credit agency.</span></span> <span data-ttu-id="66506-122">此值仅供参考。</span><span class="sxs-lookup"><span data-stu-id="66506-122">This value is for informational purposes only.</span></span> <span data-ttu-id="66506-123">在任何信用管理流程中都不会使用它。</span><span class="sxs-lookup"><span data-stu-id="66506-123">It isn't used in any credit management processes.</span></span>
13. <span data-ttu-id="66506-124">设置 **拥有所有权** 选项设置为 **是**，以指示该公司拥有所有权。</span><span class="sxs-lookup"><span data-stu-id="66506-124">Set the **Title held** option to **Yes** to indicate that a title is held for the company.</span></span> <span data-ttu-id="66506-125">此值仅供参考。</span><span class="sxs-lookup"><span data-stu-id="66506-125">This value is for informational purposes only.</span></span> <span data-ttu-id="66506-126">在任何信用管理流程中都不会使用它。</span><span class="sxs-lookup"><span data-stu-id="66506-126">It isn't used in any credit management process.</span></span>
14. <span data-ttu-id="66506-127">在 **营业开始日期** 字段中，输入客户首次开始营业的日期。</span><span class="sxs-lookup"><span data-stu-id="66506-127">In the **Business started date** field, enter the date when the customer first started to do business.</span></span> <span data-ttu-id="66506-128">此信息在创建风险评分时使用。</span><span class="sxs-lookup"><span data-stu-id="66506-128">This information is used when risk scores are created.</span></span>
15. <span data-ttu-id="66506-129">在 **自从以下时间以来的客户** 字段中，输入为客户处理第一笔交易的日期。</span><span class="sxs-lookup"><span data-stu-id="66506-129">In the **Customer since** field, enter the date when the first transactions were processed for the customer.</span></span> <span data-ttu-id="66506-130">此信息在创建风险评分时使用。</span><span class="sxs-lookup"><span data-stu-id="66506-130">This information is used when risk scores are created.</span></span>
16. <span data-ttu-id="66506-131">输入信贷团队可以用来进一步评估客户信贷价值的注释。</span><span class="sxs-lookup"><span data-stu-id="66506-131">Enter notes that the credit team can use to further evaluate the customer's credit worthiness.</span></span>

<span data-ttu-id="66506-132">请注意，**客户** 页面中显示的某些信息是由另一个流程创建的：</span><span class="sxs-lookup"><span data-stu-id="66506-132">Note that some of the information that is shown on the **Customer** page is created by another process:</span></span>

- <span data-ttu-id="66506-133">**信用额度到期日期** 字段显示了信用额度将到期的日期。</span><span class="sxs-lookup"><span data-stu-id="66506-133">The **Credit limit expiration date** field shows the date when the credit limit will expire.</span></span> <span data-ttu-id="66506-134">如果您未设置此字段，则客户的信用额度不会过期。</span><span class="sxs-lookup"><span data-stu-id="66506-134">If you don't set this field, the customer's credit limit won't expire.</span></span>
- <span data-ttu-id="66506-135">**信用额度日期** 字段显示了信用额度的创建日期。</span><span class="sxs-lookup"><span data-stu-id="66506-135">The **Credit limit date** field shows the date when the credit limit was created.</span></span> <span data-ttu-id="66506-136">每当调整信用额度时，此字段就会更新。</span><span class="sxs-lookup"><span data-stu-id="66506-136">This field is updated whenever the credit limit is adjusted.</span></span>
- <span data-ttu-id="66506-137">临时信用额度将在某个时间段内覆盖客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-137">Temporary credit limits override the customer credit limit for a period.</span></span> <span data-ttu-id="66506-138">用它们代替信用额度来计算总信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-138">They are used instead of the credit limit to calculate the total credit limit.</span></span> <span data-ttu-id="66506-139">仅当存在有效信用额度时才显示此信息。</span><span class="sxs-lookup"><span data-stu-id="66506-139">This information is shown only if there is an active credit limit.</span></span> <span data-ttu-id="66506-140">您可以通过信用额度调整来添加临时信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-140">You can add temporary credit limits through credit limit adjustments.</span></span>
- <span data-ttu-id="66506-141">**保险与担保** 字段显示了可以增加客户信用额度的保险和担保的总价值。</span><span class="sxs-lookup"><span data-stu-id="66506-141">The **Insurance and guarantees** field shows the total value of insurance and guarantees that can increase the credit limit for the customer.</span></span>
- <span data-ttu-id="66506-142">**总信用额度** 字段显示了客户的最终信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-142">The **Total credit limit** field shows the final credit limit for the customer.</span></span> <span data-ttu-id="66506-143">总信用额度包括保险和担保，以及临时信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-143">The total credit limit includes insurance and guarantees, and temporary credit limits.</span></span>

## <a name="temporary-credit-limits"></a><span data-ttu-id="66506-144">临时信用额度</span><span class="sxs-lookup"><span data-stu-id="66506-144">Temporary credit limits</span></span>

<span data-ttu-id="66506-145">临时信用额度将在所定义的时间段内覆盖客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-145">Temporary credit limits override customer credit limits for a defined period.</span></span> <span data-ttu-id="66506-146">您可以使用信用额度调整来添加临时信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-146">You can add temporary credit limits by using credit limit adjustments.</span></span> <span data-ttu-id="66506-147">信用额度调整使信用经理可以通过过帐流程来更新单个客户、一组客户或所有客户的信用额度和到期日期。</span><span class="sxs-lookup"><span data-stu-id="66506-147">Credit limit adjustments let credit managers update the credit limits and expiration dates of a single customer, a group of customers, or all customers through a posting process.</span></span>

<span data-ttu-id="66506-148">您可以在 **信用额度调整** 页面（**信用管理 \> 信用额度调整 \> 信用额度调整**）上创建信用额度调整条目。</span><span class="sxs-lookup"><span data-stu-id="66506-148">You can create credit limit adjustment entries on the **Credit limit adjustments** page (**Credit management \> Credit limit adjustments \> Credit limit adjustments**).</span></span>

## <a name="create-insurance-policies-and-guarantees"></a><span data-ttu-id="66506-149">创建保险单和担保</span><span class="sxs-lookup"><span data-stu-id="66506-149">Create insurance policies and guarantees</span></span>

<span data-ttu-id="66506-150">您可以为每个客户创建一个或多个保险单和担保。</span><span class="sxs-lookup"><span data-stu-id="66506-150">You can create one or more insurance policies and guarantees for each customer.</span></span> <span data-ttu-id="66506-151">然后，您可以使用它们来计算公司向客户提供信用时的风险。</span><span class="sxs-lookup"><span data-stu-id="66506-151">You can then use them to calculate the exposure that your company has when it offers credit to a customer.</span></span> <span data-ttu-id="66506-152">客户信用额度中也可以包括保险单和担保。</span><span class="sxs-lookup"><span data-stu-id="66506-152">Insurance policies and guarantees can also be included in the credit limit for a customer.</span></span>

<span data-ttu-id="66506-153">您可以在 **所有客户** 页面（**应收帐款 \> 客户 \> 所有客户**）上创建保险单和担保。</span><span class="sxs-lookup"><span data-stu-id="66506-153">You can create insurance policies and guarantees on the **All customers** page (**Accounts receivable \> Customers \> All customers**).</span></span> <span data-ttu-id="66506-154">选择客户，然后在操作窗格的 **信用管理** 选项卡上选择 **保险和担保**。</span><span class="sxs-lookup"><span data-stu-id="66506-154">Select a customer, and then, on the Action Pane, on the **Credit management** tab, select **Insurance and guarantees**.</span></span>

> [!NOTE]
> <span data-ttu-id="66506-155">在以下过程中，您将从全球通讯簿中选择保险人或担保人。</span><span class="sxs-lookup"><span data-stu-id="66506-155">In the following procedure, you select an insurer or guarantor from the global address book.</span></span> <span data-ttu-id="66506-156">因此，在开始此过程之前，必须确保已将保险人和担保人添加到全球通讯簿中。</span><span class="sxs-lookup"><span data-stu-id="66506-156">Therefore, before you begin this procedure, you must make sure that the insurers and guarantors have been added to the global address book.</span></span>

1. <span data-ttu-id="66506-157">在 **标识符** 字段中，输入 **担保** 或 **保险**。</span><span class="sxs-lookup"><span data-stu-id="66506-157">In the **Identifier** field, enter **Guarantee** or **Insurance**.</span></span>
2. <span data-ttu-id="66506-158">在 **担保/保险类型** 字段中，选择您先前设置的担保或保险类型之一。</span><span class="sxs-lookup"><span data-stu-id="66506-158">In the **Guarantee/Insurance type** field, select one of the guarantee or insurance types that you previously set up.</span></span>
3. <span data-ttu-id="66506-159">在 **保险人/担保人** 字段中，从全球通讯簿中选择保险人或担保人。</span><span class="sxs-lookup"><span data-stu-id="66506-159">In the **Insurer/Guarantor** field, select the insurer or guarantor from the global address book.</span></span> 
4. <span data-ttu-id="66506-160">如果在 **标识符** 字段中选择了 **保险**，请在 **保险单范围类型** 字段中选择您先前设置的一种范围类型。</span><span class="sxs-lookup"><span data-stu-id="66506-160">If you selected **Insurance** in the **Identifier** field, in the **Policy coverage type** field, select one of the coverage types that you previously set up.</span></span> <span data-ttu-id="66506-161">您不能为担保人选择保险单范围类型。</span><span class="sxs-lookup"><span data-stu-id="66506-161">You can't select a policy coverage type for a guarantee.</span></span>
5. <span data-ttu-id="66506-162">在 **身份证明** 字段中，输入保险单的 ID。</span><span class="sxs-lookup"><span data-stu-id="66506-162">In the **Identification** field, enter the ID of the policy.</span></span> <span data-ttu-id="66506-163">该 ID 通常是一个保险单编号。</span><span class="sxs-lookup"><span data-stu-id="66506-163">This ID is usually a policy number.</span></span>
6. <span data-ttu-id="66506-164">在 **有效** 字段中，输入保险单或担保人的开始日期。</span><span class="sxs-lookup"><span data-stu-id="66506-164">In the **Effective** field, enter the start date of the insurance policy or guarantee.</span></span>
7. <span data-ttu-id="66506-165">在 **到期** 字段中，输入保险单或担保人的到期。</span><span class="sxs-lookup"><span data-stu-id="66506-165">In the **Expiration** field, enter the date when the insurance policy or guarantee.</span></span> <span data-ttu-id="66506-166">日期。</span><span class="sxs-lookup"><span data-stu-id="66506-166">expires.</span></span>
8. <span data-ttu-id="66506-167">在 **价值** 字段中，输入保险单或担保人的价值。</span><span class="sxs-lookup"><span data-stu-id="66506-167">In the **Value** field, enter the value of the insurance policy or guarantee.</span></span> <span data-ttu-id="66506-168">该价值是保险单的全部价值。</span><span class="sxs-lookup"><span data-stu-id="66506-168">This value is the full value of the policy.</span></span>
9. <span data-ttu-id="66506-169">在 **货币** 字段中，选择保险单价值的对应货币。</span><span class="sxs-lookup"><span data-stu-id="66506-169">In the **Currency** field, select the currency for the policy value.</span></span> 
10. <span data-ttu-id="66506-170">在 **更新信用额度** 字段中，指定一个介于 **0** 和 **100** 之间的百分比。</span><span class="sxs-lookup"><span data-stu-id="66506-170">In the **Update credit limit** field, specify a percentage between **0** and **100**.</span></span> <span data-ttu-id="66506-171">该百分比将应用于保单价值，所得金额将用于增加信用额度计算中所使用的信用额度。</span><span class="sxs-lookup"><span data-stu-id="66506-171">This percentage will be applied to the policy value, and the resulting amount will be used to increase the credit limit that is used in credit limit calculations.</span></span> <span data-ttu-id="66506-172">计算的值显示在 **客户** 页面的 **信用和收款** 快速选项卡上的 **总信用额度、保险和担保** 下面。</span><span class="sxs-lookup"><span data-stu-id="66506-172">The calculated value is shown under **Total credit limit, Insurance and Guarantees** on the **Credit and collections** FastTab of the **Customers** page.</span></span>

    <span data-ttu-id="66506-173">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="66506-173">Here is an example:</span></span>

    - <span data-ttu-id="66506-174">信用额度 (A) 为 100,000。</span><span class="sxs-lookup"><span data-stu-id="66506-174">The credit limit (A) is 100,000.</span></span>
    - <span data-ttu-id="66506-175">保单价值 (B) 为 50,000。</span><span class="sxs-lookup"><span data-stu-id="66506-175">The policy value (B) is 50,000.</span></span>
    - <span data-ttu-id="66506-176">**更新信用额度** 百分比 (C) 为 50.00。</span><span class="sxs-lookup"><span data-stu-id="66506-176">The **Update credit limit** percentage (C) is 50.00.</span></span>
    
    <span data-ttu-id="66506-177">在此例中，有效信用额度为 125,000 (= A + \[B × C\])。</span><span class="sxs-lookup"><span data-stu-id="66506-177">In this case, the effective credit limit is 125,000 (= A + \[B × C\]).</span></span>

11. <span data-ttu-id="66506-178">选择 **包含在风险中** 复选框以从信用额度计算中使用的信用额度中扣除保险单的全部价值。</span><span class="sxs-lookup"><span data-stu-id="66506-178">Select the **Included in exposure** check box to reduce the credit limit that is used in credit limit calculations by the full value of the policy.</span></span> <span data-ttu-id="66506-179">如果选中此复选框，则指定 **更新信用额度** 百分比后计算的值不会用于信用额度计算。</span><span class="sxs-lookup"><span data-stu-id="66506-179">If this check box is selected, the value that is calculated when the **Update credit limit** percentage is specified won't be used in credit limit calculations.</span></span>

    <span data-ttu-id="66506-180">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="66506-180">Here is an example:</span></span>

    - <span data-ttu-id="66506-181">信用额度 (A) 为 100,000。</span><span class="sxs-lookup"><span data-stu-id="66506-181">The credit limit (A) is 100,000.</span></span>
    - <span data-ttu-id="66506-182">保单价值 (B) 为 50,000。</span><span class="sxs-lookup"><span data-stu-id="66506-182">The policy value (B) is 50,000.</span></span>
    - <span data-ttu-id="66506-183">**更新信用额度** 百分比 (C) 为 50.00。</span><span class="sxs-lookup"><span data-stu-id="66506-183">The **Update credit limit** percentage (C) is 50.00.</span></span>

    <span data-ttu-id="66506-184">在此例中，有效信用额度为 125,000 (= A + \[B × C\])。</span><span class="sxs-lookup"><span data-stu-id="66506-184">In this case, the effective credit limit is 125,000 (= A + \[B × C\]).</span></span>
    
    <span data-ttu-id="66506-185">但是，如果选中 **包含在风险中** 复选框，则会扣除 **更新信用额度** 值 50,000（= 100,000 的 50.00％），因此风险值为 75,000 (= A + \[B × C\] – B)。</span><span class="sxs-lookup"><span data-stu-id="66506-185">However, if you select the **Included in exposure** check box, the **Update credit limit** value of 50,000 (= 50.00 percent of 100,000) is removed, and the exposure value is 75,000 (= A + \[B × C\] – B).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]