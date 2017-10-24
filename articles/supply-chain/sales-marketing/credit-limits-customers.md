---
title: "客户的信用额度"
description: "本文对 Microsoft Dynamics 365 for Finance and Operations 中的信用额度如何运作进行概述。"
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Unified operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 333a99d483415ee024e1ec67f27d02698463ae4f
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="credit-limits-for-customers"></a><span data-ttu-id="362cc-103">客户的信用额度</span><span class="sxs-lookup"><span data-stu-id="362cc-103">Credit limits for customers</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="362cc-104">设置信用额度可以指定要为您的客户扩展的最大信用金额。</span><span class="sxs-lookup"><span data-stu-id="362cc-104">Setting a credit limit lets you specify the maximum amount of credit to extend to your customers.</span></span> <span data-ttu-id="362cc-105">如果指定了信用额度，系统将自动检查用户何时尝试更新单据。</span><span class="sxs-lookup"><span data-stu-id="362cc-105">If a credit limit is specified, it is checked automatically when a user attempts to update a document.</span></span> <span data-ttu-id="362cc-106">如果超出信用额度，将向用户显示消息。</span><span class="sxs-lookup"><span data-stu-id="362cc-106">If the credit limit is exceeded, a message is displayed to the user.</span></span> <span data-ttu-id="362cc-107">本文提供信用额度如何运作的概述，并回答以下问题：</span><span class="sxs-lookup"><span data-stu-id="362cc-107">This article provides an overview of how credit limits work  and answers the following questions:</span></span>

-   <span data-ttu-id="362cc-108">我可以为哪些单据和流程检查信用额度？</span><span class="sxs-lookup"><span data-stu-id="362cc-108">What documents and processes can I check credit limits for?</span></span>

-   <span data-ttu-id="362cc-109">我要在哪里配置计算客户剩余信用的方式？</span><span class="sxs-lookup"><span data-stu-id="362cc-109">Where do I configure the way that the customer’s remaining credit is calculated?</span></span>

-   <span data-ttu-id="362cc-110">哪里有关于客户所用的剩余信用的信息？</span><span class="sxs-lookup"><span data-stu-id="362cc-110">Where is information about a customer’s remaining credit used?</span></span>

-   <span data-ttu-id="362cc-111">我要在哪里指定要为客户扩展的信用是否需要身份证明，以及信用额度金额是否需要身份证明？</span><span class="sxs-lookup"><span data-stu-id="362cc-111">Where do I specify whether identification is required for credit to be extended to a customer, and also the credit limit amount that requires identification?</span></span>

-   <span data-ttu-id="362cc-112">我要在哪里指定如果超过信用额度是否显示警告或错误？</span><span class="sxs-lookup"><span data-stu-id="362cc-112">Where do I specify whether to display a warning or error if the credit limit is exceeded?</span></span>

-   <span data-ttu-id="362cc-113">如何为特定客户指定信用额度？</span><span class="sxs-lookup"><span data-stu-id="362cc-113">How do I specify the credit limit for a specific customer?</span></span>

-   <span data-ttu-id="362cc-114">如何手动检查销售订单上的信用额度？</span><span class="sxs-lookup"><span data-stu-id="362cc-114">How do I check credit limits manually on sales orders?</span></span>

<span data-ttu-id="362cc-115">**我可以为哪些单据和流程检查信用额度？**</span><span class="sxs-lookup"><span data-stu-id="362cc-115">**What documents and processes can I check credit limits for?**</span></span>

<span data-ttu-id="362cc-116">使用**应收账款参数**窗体指定要检查信用额度的单据。</span><span class="sxs-lookup"><span data-stu-id="362cc-116">Use the **Accounts receivable parameters** form to specify which documents to check credit limits for.</span></span> <span data-ttu-id="362cc-117">必须是“系统管理员 (-SYSADMIN-)”安全角色才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-117">You must be a member of the System administrator (-SYSADMIN-) security role to make changes in this form.</span></span> <span data-ttu-id="362cc-118">可以检查以下单据和流程的信用额度：</span><span class="sxs-lookup"><span data-stu-id="362cc-118">You can check credit limits for the following documents and processes:</span></span>

-   <span data-ttu-id="362cc-119">销售订单的发票，过帐发票时</span><span class="sxs-lookup"><span data-stu-id="362cc-119">Invoices for sales orders, when you post the invoices</span></span>

-   <span data-ttu-id="362cc-120">销售订单的装箱单，更新装箱单时</span><span class="sxs-lookup"><span data-stu-id="362cc-120">Packing slips for sales orders, when you update packing slips</span></span>

-   <span data-ttu-id="362cc-121">销售订单，将行添加到**销售订单**窗体中时</span><span class="sxs-lookup"><span data-stu-id="362cc-121">Sales orders, when you add lines in the **Sales order** form</span></span>

-   <span data-ttu-id="362cc-122">销售订单，通过服务创建销售订单时</span><span class="sxs-lookup"><span data-stu-id="362cc-122">Sales orders, when they are created through a service</span></span>

-   <span data-ttu-id="362cc-123">普通发票，过帐发票时</span><span class="sxs-lookup"><span data-stu-id="362cc-123">Free text invoices, when you post the invoices</span></span>

<span data-ttu-id="362cc-124">如果设置了以下选项之一，系统将自动检测信用额度：</span><span class="sxs-lookup"><span data-stu-id="362cc-124">Credit limits are automatically checked if either of the following options is set:</span></span>

-   <span data-ttu-id="362cc-125">在**应收账款参数**窗体中，**信用额度类型**字段设置为除**无**以外的任何内容。</span><span class="sxs-lookup"><span data-stu-id="362cc-125">In the **Accounts receivable parameters** form, the **Credit limit type** field is set to anything other than **None**.</span></span> <span data-ttu-id="362cc-126">将为所有客户检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-126">Credit limits are checked for all customers.</span></span>

-   <span data-ttu-id="362cc-127">在**应收账款参数**窗体中，**信用额度类型**字段设置为**无**，但在**客户**窗体中为客户选择**强制信用额度**。</span><span class="sxs-lookup"><span data-stu-id="362cc-127">In the **Accounts receivable parameters** form, the **Credit limit type** field is set to **None** but **Mandatory credit limit** is selected for a customer in the **Customers** form.</span></span> <span data-ttu-id="362cc-128">只为特定客户检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-128">Credit limits are checked only for specific customers.</span></span>

<span data-ttu-id="362cc-129">若要检查以下单据的信用额度，必须指定其他设置。</span><span class="sxs-lookup"><span data-stu-id="362cc-129">To check credit limits for the following documents, you must specify additional settings.</span></span>

|    <span data-ttu-id="362cc-130">原始凭证</span><span class="sxs-lookup"><span data-stu-id="362cc-130">Document</span></span>                                    |    <span data-ttu-id="362cc-131">其他设置</span><span class="sxs-lookup"><span data-stu-id="362cc-131">Additional setting</span></span>                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    <span data-ttu-id="362cc-132">普通发票</span><span class="sxs-lookup"><span data-stu-id="362cc-132">Free text   invoice</span></span>                         |    <span data-ttu-id="362cc-133">在“应收账款参数”窗体的“信用等级”区域选择“在普通发票上检查信用额度”。</span><span class="sxs-lookup"><span data-stu-id="362cc-133">In the Accounts receivable parameters   form, in the Credit rating area, select Check credit limit on free   text invoice.</span></span>     |
|    <span data-ttu-id="362cc-134">销售订单（手动输入）</span><span class="sxs-lookup"><span data-stu-id="362cc-134">Sales   order (manually entered)</span></span>            |    <span data-ttu-id="362cc-135">在“应收账款参数”窗体的“信用等级”区域选择“在销售订单上检查信用额度”。</span><span class="sxs-lookup"><span data-stu-id="362cc-135">In the Accounts receivable parameters   form, in the Credit rating area, select Check credit limit on sales   order.</span></span>           |
|    <span data-ttu-id="362cc-136">销售订单（以电子方式收到）</span><span class="sxs-lookup"><span data-stu-id="362cc-136">Sales   order (electronically received)</span></span>     |    <span data-ttu-id="362cc-137">在“应收账款参数”窗体的 AIF 区域选择“检查销售订单的信用额度”。</span><span class="sxs-lookup"><span data-stu-id="362cc-137">In the Accounts receivable parameters   form, in the AIF area, select Check credit limit for sales orders.</span></span>                     |

<span data-ttu-id="362cc-138">**我要在哪里配置计算客户剩余信用的方式？**</span><span class="sxs-lookup"><span data-stu-id="362cc-138">**Where do I configure the way that a customer’s remaining credit is calculated?**</span></span>

<span data-ttu-id="362cc-139">可以用以下任一方式配置 Dynamics 365 以计算客户的剩余信用：</span><span class="sxs-lookup"><span data-stu-id="362cc-139">You can configure Dynamics 365 to calculate a customer’s remaining credit in any of the following ways:</span></span>

-   <span data-ttu-id="362cc-140">将信用额度与客户余额作比较。</span><span class="sxs-lookup"><span data-stu-id="362cc-140">Compare the credit limit against the customer balance.</span></span>

-   <span data-ttu-id="362cc-141">将信用额度与客户余额和装箱单金额作比较。</span><span class="sxs-lookup"><span data-stu-id="362cc-141">Compare the credit limit against the customer balance and packing slip amounts.</span></span>

-   <span data-ttu-id="362cc-142">将信用额度与客户余额和所有未结交易活动作比较。</span><span class="sxs-lookup"><span data-stu-id="362cc-142">Compare the credit limit against the customer balance and all open transaction activity.</span></span> <span data-ttu-id="362cc-143">这包括装箱单金额和销售订单金额。</span><span class="sxs-lookup"><span data-stu-id="362cc-143">This includes packing slip amounts and sales order amounts.</span></span>

<span data-ttu-id="362cc-144">使用**应收账款参数**窗体指定要比较的信息。</span><span class="sxs-lookup"><span data-stu-id="362cc-144">Use the **Accounts receivable parameters** form to specify the information to compare to.</span></span> <span data-ttu-id="362cc-145">必须是“系统管理员 (-SYSADMIN-)”安全角色才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-145">You must be a member of the System administrator (-SYSADMIN-) security role to make changes in this form.</span></span> <span data-ttu-id="362cc-146">在**信用额度类型**字段中，选择是否执行信用额度检查以及如果检查信用额度要包括哪些交易记录信息。</span><span class="sxs-lookup"><span data-stu-id="362cc-146">In the **Credit limit type** field, select whether to perform credit limit checks and what transaction information to include when the credit limit is checked.</span></span> <span data-ttu-id="362cc-147">从以下选项中进行选择：</span><span class="sxs-lookup"><span data-stu-id="362cc-147">Select from the following options:</span></span>

-   <span data-ttu-id="362cc-148">**无** – 不检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-148">**None** – Do not check credit limits.</span></span> <span data-ttu-id="362cc-149">可以通过选择**客户**窗体中的**强制信用额度**复选框为特定客户覆盖此选项。</span><span class="sxs-lookup"><span data-stu-id="362cc-149">You can override this option for a specific customer by selecting the **Mandatory credit limit** check box in the **Customers** form.</span></span> <span data-ttu-id="362cc-150">如果执行此操作，将检查信用额度和客户余额。</span><span class="sxs-lookup"><span data-stu-id="362cc-150">If you do this, the credit limit is checked against the customer balance.</span></span>

-   <span data-ttu-id="362cc-151">**余额** - 对客户余额检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-151">**Balance** – The credit limit is checked against the customer balance.</span></span>

-   <span data-ttu-id="362cc-152">**余额+装箱单或产品收据** – 通过客户余额和交货情况检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-152">**Balance + packing slip or product receipt** – The credit limit is checked against the customer balance and deliveries.</span></span>

-   <span data-ttu-id="362cc-153">**余额+所有** - 对客户余额、交货和未结订单检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-153">**Balance+All** – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span>

<span data-ttu-id="362cc-154">**哪里有关于客户所用的剩余信用的信息？**</span><span class="sxs-lookup"><span data-stu-id="362cc-154">**Where is information about a customer’s remaining credit used?**</span></span>

<span data-ttu-id="362cc-155">有关客户的余额和剩余信用金额的信息在创建帐龄快照时计算和存储，并显示在**收款**窗体中。</span><span class="sxs-lookup"><span data-stu-id="362cc-155">Information about a customer’s balance and remaining credit amount is calculated and stored when you create an aging snapshot, and is displayed in the **Collections** form.</span></span> <span data-ttu-id="362cc-156">显示在**收款**窗体中的金额可能不包括所有交易记录活动，直到创建了新的帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="362cc-156">The amounts that are displayed in the **Collections** form might not include all transaction activity until a new aging snapshot is created.</span></span> <span data-ttu-id="362cc-157">有关详细信息，请参阅[在应收账款中的收款和信用](https://technet.microsoft.com/en-us/library/hh209221.aspx)。</span><span class="sxs-lookup"><span data-stu-id="362cc-157">For more information, see [Collections and credit in Accounts receivable](https://technet.microsoft.com/en-us/library/hh209221.aspx).</span></span>

<span data-ttu-id="362cc-158">根据所选单据，将在更新销售订单、装箱单和客户发票时计算有关客户的余额和剩余信用金额的信息。</span><span class="sxs-lookup"><span data-stu-id="362cc-158">Depending on the documents that are selected, information about a customer’s balance and remaining credit amount is calculated when sales orders, packing slips, and customer invoices are updated.</span></span> <span data-ttu-id="362cc-159">如果您处理的单据的金额将超过信用额度，则会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="362cc-159">If the amount of the document that you are working with would cause the credit limit to be exceeded, a message is displayed.</span></span>

<span data-ttu-id="362cc-160">**我要在哪里指定要为客户扩展的信用是否需要身份证明，以及信用额度是否需要身份证明？**</span><span class="sxs-lookup"><span data-stu-id="362cc-160">**Where do I specify whether identification is required for credit to be extended to a customer, and also the credit limit that requires identification?**</span></span>

<span data-ttu-id="362cc-161">使用**应收账款参数**窗体可以指定是否需要身份证明以及信用额度金额限制是否需要身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-161">Use the **Accounts receivable parameters** form to specify whether to require identification and the credit limit amount limit that requires identification.</span></span>
<span data-ttu-id="362cc-162">必须是“系统管理员 (-SYSADMIN-)”安全角色才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-162">You must be a member of the System administrator (-SYSADMIN-) security role to make changes in this form.</span></span>

|    <span data-ttu-id="362cc-163">字段</span><span class="sxs-lookup"><span data-stu-id="362cc-163">Field</span></span>                                    |    <span data-ttu-id="362cc-164">说明</span><span class="sxs-lookup"><span data-stu-id="362cc-164">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    <span data-ttu-id="362cc-165">要求对贷款显示标识号</span><span class="sxs-lookup"><span data-stu-id="362cc-165">Require   identification with credit</span></span>     |    <span data-ttu-id="362cc-166">选择必须为您的法人要向其扩展信用的客户输入的身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="362cc-166">Select the type of identification that must be   entered for customers to whom your legal entity extends credit.</span></span> <span data-ttu-id="362cc-167">您在此字段中选择的选项决定了要求在“客户”窗体中的“政府标识”字段中填写信息的时间和类型：无 - 无论客户的信用额度是多少，都无需使用政府签发的身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-167">The option   that you select in this field determines when and what type of information is   required in the Government identification fields in the Customers   form:        No – No government-issued        identification is required, regardless of the customer's credit limit.</span></span>     <span data-ttu-id="362cc-168">是 – 如果客户的信用额度大于或等于零，则需要政府签发的许可证编号或其他身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-168">Yes – A        government-issued license number or other government-issued        identification is required if the customer's credit limit is higher than        or equal to zero.</span></span>     <span data-ttu-id="362cc-169">下限 – 如果客户的信用额度大于或等于您在此窗体的“限值”字段中输入的限值，则需要政府签发的许可证编号或其他身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-169">Minimum limit – A        government-issued license number or other government-issued        identification is required if the customer's credit limit is higher than        or equal to the limit that you enter in the Limit field in this        form.</span></span>        |
|    <span data-ttu-id="362cc-170">限额</span><span class="sxs-lookup"><span data-stu-id="362cc-170">Limit</span></span>                                    |    <span data-ttu-id="362cc-171">输入某个信用额度，客户达到该信用额度时需要政府签发的许可证编号或其他身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-171">Enter the credit limit at which a   government-issued license number or other identification is required for   customers.</span></span>    <span data-ttu-id="362cc-172">例如，键入 2000 以要求必须为信用额度在 2,000 或 2,000 以上的客户输入身份证明编号，如司机的驾照号。</span><span class="sxs-lookup"><span data-stu-id="362cc-172">For example, type 2000 to require that an   identification number, such as a driver's license number, must be entered for   customers who have a credit limit of 2,000 or higher.</span></span>    <span data-ttu-id="362cc-173">仅当在“要求对贷款显示标识号”字段中选择了“下限”时，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="362cc-173">This field is available if you selected Minimum   limit in the Require identification with credit field.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |

<span data-ttu-id="362cc-174">**我要在哪里指定如果超过信用额度是否显示警告或错误？**</span><span class="sxs-lookup"><span data-stu-id="362cc-174">**Where do I specify whether to display a warning or error if the credit limit is exceeded?**</span></span>

<span data-ttu-id="362cc-175">使用**应收账款参数**窗体可以指定如果超出信用额度是否显示警告或错误。</span><span class="sxs-lookup"><span data-stu-id="362cc-175">Use the **Accounts receivable parameters** form to specify whether to display a warning or error if the credit limit is exceeded.</span></span> <span data-ttu-id="362cc-176">此警告或此外在用户输入或过帐信息时显示，或者如果单据通过电子服务处理，则包括在日志中。</span><span class="sxs-lookup"><span data-stu-id="362cc-176">This warning or error is displayed when a user is entering or posting information, or it is included in a log if the documents are being processed by an electronic service.</span></span> <span data-ttu-id="362cc-177">必须是“系统管理员 (-SYSADMIN-)”安全角色才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-177">You must be a member of the System administrator (-SYSADMIN-) security role to make changes in this form.</span></span>

|    <span data-ttu-id="362cc-178">字段</span><span class="sxs-lookup"><span data-stu-id="362cc-178">Field</span></span>                                                               |    <span data-ttu-id="362cc-179">说明</span><span class="sxs-lookup"><span data-stu-id="362cc-179">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    <span data-ttu-id="362cc-180">在超出信用额度时显示的消息（在信用等级区域）</span><span class="sxs-lookup"><span data-stu-id="362cc-180">Message when exceeding credit limit (in the Credit rating area)</span></span>     |    <span data-ttu-id="362cc-181">选择如何向用户显示关于超出信用额度的消息。</span><span class="sxs-lookup"><span data-stu-id="362cc-181">Select how messages about credit limits being   exceeded are displayed to users.</span></span> <span data-ttu-id="362cc-182">从以下选项中进行选择：错误 - 将显示一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="362cc-182">Select from the following options:        Error – An        error message is displayed.</span></span> <span data-ttu-id="362cc-183">这通常会停止当前操作，并且必须解决了冲突，之后才能继续处理。</span><span class="sxs-lookup"><span data-stu-id="362cc-183">This usually stops the current operation and        the conflict must be resolved before the process can continue.</span></span>     <span data-ttu-id="362cc-184">警告 – 显示警告消息，但可以继续操作。</span><span class="sxs-lookup"><span data-stu-id="362cc-184">Warning – A        warning message is displayed, but the process can continue.</span></span>                     |
|    <span data-ttu-id="362cc-185">在超出信用额度时显示的消息（在 AIF 区域）</span><span class="sxs-lookup"><span data-stu-id="362cc-185">Message when exceeding credit limit (in the AIF area)</span></span>               |    <span data-ttu-id="362cc-186">选择如何在日志中传递关于超出信用额度的消息。</span><span class="sxs-lookup"><span data-stu-id="362cc-186">Select how messages about credit limits being   exceeded are delivered in a log.</span></span> <span data-ttu-id="362cc-187">从以下选项中进行选择 – 将在“异常”窗体中显示错误消息，并且不会处理单据，直到解决了错误。</span><span class="sxs-lookup"><span data-stu-id="362cc-187">Select from the following options:        Error – An        error message is displayed in the Exceptions form, and the        document will not be processed until the error is resolved.</span></span>     <span data-ttu-id="362cc-188">警告 – 将在“异常”窗体中显示警告消息，但是可以继续处理。</span><span class="sxs-lookup"><span data-stu-id="362cc-188">Warning – A        warning message is displayed in the Exceptions form, but the        process can continue.</span></span>        |

<span data-ttu-id="362cc-189">**如何为特定客户指定信用额度金额？**</span><span class="sxs-lookup"><span data-stu-id="362cc-189">**How do I specify the credit limit amount for a specific customer?**</span></span>

<span data-ttu-id="362cc-190">使用**客户**窗体可以为特定客户指定信用额度金额。</span><span class="sxs-lookup"><span data-stu-id="362cc-190">Use the **Customers** form to specify the credit limit amount for a specific customer.</span></span> <span data-ttu-id="362cc-191">必须是获分配“维护客户主数据 (CustCustomersMaintain)”职责的安全角色的成员才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-191">You must be a member of a security role that has the Maintain customer master (CustCustomersMaintain) duty assigned to it to make changes in this form.</span></span>

1.  <span data-ttu-id="362cc-192">单击**应收账款** \> **通用** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="362cc-192">Click **Accounts receivable** \> **Common** \> **Customers** \> **All customers**.</span></span> <span data-ttu-id="362cc-193">双击客户帐户。</span><span class="sxs-lookup"><span data-stu-id="362cc-193">Double-click a customer account.</span></span>

2.  <span data-ttu-id="362cc-194">在**客户**窗体的操作窗格上单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="362cc-194">In the **Customers** form, on the Action Pane, click **Edit**.</span></span>

3.  <span data-ttu-id="362cc-195">在**信用额度**字段中输入货币金额。</span><span class="sxs-lookup"><span data-stu-id="362cc-195">Enter a currency amount in the **Credit limit** field.</span></span> <span data-ttu-id="362cc-196">此值必须大于零（0）并且将用作信用额度金额。</span><span class="sxs-lookup"><span data-stu-id="362cc-196">This value must be higher than zero (0), and will be used as the credit limit amount.</span></span>

4.  <span data-ttu-id="362cc-197">如果要求，请在**政府标识**字段中输入许可证编号或政府签发的其他身份证明。</span><span class="sxs-lookup"><span data-stu-id="362cc-197">If it is required, enter a license number or other government-issued identification in the **Government identification** field.</span></span>

> [!NOTE]
> <span data-ttu-id="362cc-198">在**应收账款参数**窗体中，通常选择信用额度类型。</span><span class="sxs-lookup"><span data-stu-id="362cc-198">In the **Accounts receivable parameters** form, a credit limit type is typically selected.</span></span> <span data-ttu-id="362cc-199">但是，如果信用额度类型设置为**无**，则您还必须选择**客户**窗体中的**强制信用额度**复选框以便对照客户的余额检查客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-199">However, if the credit limit type is set to **None**, you must also select the **Mandatory credit limit** check box in the **Customers** form in order to check the customer’s credit limit against the customer’s balance.</span></span> <span data-ttu-id="362cc-200">有关信用额度类型的详细信息，请参见本主题中的“可以为哪些单据和流程检查信用额度？”</span><span class="sxs-lookup"><span data-stu-id="362cc-200">For more information about credit limit types, see “What documents and processes can I check credit limits for?”</span></span> <span data-ttu-id="362cc-201">。</span><span class="sxs-lookup"><span data-stu-id="362cc-201">in this topic.</span></span> 

<span data-ttu-id="362cc-202">**如何手动检查销售订单上的信用额度？**</span><span class="sxs-lookup"><span data-stu-id="362cc-202">**How do I manually check credit limits on sales orders?**</span></span>

<span data-ttu-id="362cc-203">有时，您可能必须手动检查客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-203">Sometimes, you might have to manually check a customer’s credit limit.</span></span> <span data-ttu-id="362cc-204">例如，在开始输入销售订单前，您可以手动检查客户的信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-204">For example, you might manually check a customer’s credit limit before you start entering a sales order.</span></span> <span data-ttu-id="362cc-205">可以使用**销售订单**窗体手动检查信用额度。</span><span class="sxs-lookup"><span data-stu-id="362cc-205">You can use the **Sales order** form to manually check credit limits.</span></span> <span data-ttu-id="362cc-206">必须是获分配“维护销售订单 (SalesOrderMaintain)”职责的安全角色的成员才可更改此窗体。</span><span class="sxs-lookup"><span data-stu-id="362cc-206">You must be a member of a security role that has the Maintain sales order (SalesOrderMaintain) duty assigned to it to make changes in this form.</span></span>

1.  <span data-ttu-id="362cc-207">单击**销售和市场营销** \> **通用** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="362cc-207">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span> <span data-ttu-id="362cc-208">双击销售订单。</span><span class="sxs-lookup"><span data-stu-id="362cc-208">Double-click a sales order.</span></span>

2.  <span data-ttu-id="362cc-209">在**销售订单**窗体的操作窗格中，在**管理**选项卡上单击**检查信用额度**。</span><span class="sxs-lookup"><span data-stu-id="362cc-209">In the **Sales order** form, on the Action Pane, on the **Manage** tab, click **Check credit limit**.</span></span>
