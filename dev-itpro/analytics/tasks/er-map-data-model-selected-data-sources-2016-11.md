--- 
title: "针对电子申报 (ER) 将数据模型映射到所选的数据源"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何映射电子报表 (ER) 数据模型到所选的 Dynamics 365 for Finance and Operations Enterprise Edition 数据源中。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96974d7c1597db4ac31168be40cecbc7e12d6edd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="4e004-103">针对电子申报 (ER) 将数据模型映射到所选的数据源</span><span class="sxs-lookup"><span data-stu-id="4e004-103">Map a data model to selected data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e004-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何映射电子报表 (ER) 数据模型到所选的 Dynamics 365 for Finance and Operations Enterprise Edition 数据源中。</span><span class="sxs-lookup"><span data-stu-id="4e004-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="4e004-105">此模型映射稍后将作为用于管理电子付款文件的格式配置中的数据源。</span><span class="sxs-lookup"><span data-stu-id="4e004-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="4e004-106">在此示例中，您将示例公司 Litware，Inc. 的数据模型映射到数据源。</span><span class="sxs-lookup"><span data-stu-id="4e004-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="4e004-107">为了完成这些步骤，您首先必须完成“为模型映射选择数据源”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="4e004-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="4e004-108">打开 ER 配置树</span><span class="sxs-lookup"><span data-stu-id="4e004-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="4e004-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="4e004-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4e004-110">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="4e004-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="4e004-111">选择已创建的模型映射</span><span class="sxs-lookup"><span data-stu-id="4e004-111">Select created model mapping</span></span>
1. <span data-ttu-id="4e004-112">在树结构中，选择“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="4e004-113">确保模型配置“付款（简化模型）”已提前创建。</span><span class="sxs-lookup"><span data-stu-id="4e004-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="4e004-114">否则，在完成任务指南“使用所选域的数据模型创建新配置”之后立即停止并返回。</span><span class="sxs-lookup"><span data-stu-id="4e004-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="4e004-115">单击“模型设计器”。</span><span class="sxs-lookup"><span data-stu-id="4e004-115">Click Model designer.</span></span>
3. <span data-ttu-id="4e004-116">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="4e004-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="4e004-117">选择“CT 映射”记录。</span><span class="sxs-lookup"><span data-stu-id="4e004-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="4e004-118">CT 映射</span><span class="sxs-lookup"><span data-stu-id="4e004-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="4e004-119">将创建的数据源与数据模型元素绑定。</span><span class="sxs-lookup"><span data-stu-id="4e004-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="4e004-120">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4e004-120">Click Designer.</span></span>
2. <span data-ttu-id="4e004-121">在树结构中，选择“处理日期和时间（处理日期时间）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="4e004-122">在树结构中，选择“处理日期（处理日期时间）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="4e004-123">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-123">Click Bind.</span></span>
5. <span data-ttu-id="4e004-124">在树结构中，选择“付款消息识别（消息识别）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="4e004-125">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4e004-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="4e004-126">在树结构中，选择“交易记录\日记帐批号（日记帐编号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="4e004-127">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-127">Click Bind.</span></span>
9. <span data-ttu-id="4e004-128">在树结构中，选择“付款”。</span><span class="sxs-lookup"><span data-stu-id="4e004-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="4e004-129">在树结构中，选择“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4e004-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="4e004-130">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-130">Click Bind.</span></span>
12. <span data-ttu-id="4e004-131">在树结构中，展开“付款=交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4e004-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="4e004-132">在树结构中，展开“付款=交易记录\贷方”。</span><span class="sxs-lookup"><span data-stu-id="4e004-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="4e004-133">在树结构中，展开“付款=交易记录\贷方\帐户”。</span><span class="sxs-lookup"><span data-stu-id="4e004-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="4e004-134">在树结构中，选择“付款=交易记录\贷方\帐户\币种代码（货币）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="4e004-135">在树结构中，展开“交易记录\出售银行帐户交易公司()”。</span><span class="sxs-lookup"><span data-stu-id="4e004-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="4e004-136">在树结构中，选择“交易记录\出售银行帐户交易公司\货币（币种代码）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="4e004-137">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-137">Click Bind.</span></span>
19. <span data-ttu-id="4e004-138">在树结构中，选择“付款=交易记录\贷方\帐户\IBAN 代码 (IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="4e004-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="4e004-139">在树结构中，选择“交易记录\出售银行帐户交易公司()\IBAN（银行 IBAN）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="4e004-140">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-140">Click Bind.</span></span>
22. <span data-ttu-id="4e004-141">在树结构中，选择“付款=交易记录\贷方\帐户\编号”。</span><span class="sxs-lookup"><span data-stu-id="4e004-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="4e004-142">在树结构中，选择“交易记录\出售银行帐户交易公司()\银行帐号（帐号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="4e004-143">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-143">Click Bind.</span></span>
25. <span data-ttu-id="4e004-144">在树结构中，展开“付款=交易记录\贷方\代理”。</span><span class="sxs-lookup"><span data-stu-id="4e004-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="4e004-145">在树结构中，选择“付款=交易记录\贷方\代理\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="4e004-146">在树结构中，选择“交易记录\出售银行帐户交易公司()\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="4e004-147">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-147">Click Bind.</span></span>
29. <span data-ttu-id="4e004-148">在树结构中，选择“付款=交易记录\贷方\代理\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="4e004-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="4e004-149">在树结构中，选择“交易记录\出售银行帐户交易公司()\银行代号（登记号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="4e004-150">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-150">Click Bind.</span></span>
32. <span data-ttu-id="4e004-151">在树结构中，选择“付款=交易记录\贷方\代理\SWIFT 代码 (SWIFT)”。</span><span class="sxs-lookup"><span data-stu-id="4e004-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="4e004-152">在树结构中，选择“交易记录\出售银行帐户交易公司()\SWIFT 代码（SWIFT 号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="4e004-153">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-153">Click Bind.</span></span>
35. <span data-ttu-id="4e004-154">在树结构中，选择“付款=交易记录\贷方\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="4e004-155">在树结构中，展开“交易记录\查找出售表格()”。</span><span class="sxs-lookup"><span data-stu-id="4e004-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="4e004-156">在树结构中，选择“Transactions\findVendTable()\name()”。</span><span class="sxs-lookup"><span data-stu-id="4e004-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="4e004-157">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-157">Click Bind.</span></span>
39. <span data-ttu-id="4e004-158">在树结构中，选择“付款=交易记录\币种代码（货币）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="4e004-159">在树结构中，展开“交易记录\>关系”。</span><span class="sxs-lookup"><span data-stu-id="4e004-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="4e004-160">在树结构中，展开“交易记录\>关系\货币表格（货币）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="4e004-161">在树结构中，选择“交易记录\>关系\货币表格（货币）\币种代码（币种代码 ISO）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="4e004-162">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-162">Click Bind.</span></span>
44. <span data-ttu-id="4e004-163">在树结构中，展开“付款=交易记录\借方”。</span><span class="sxs-lookup"><span data-stu-id="4e004-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="4e004-164">在树结构中，展开“付款=交易记录\借方\帐户”。</span><span class="sxs-lookup"><span data-stu-id="4e004-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="4e004-165">在树结构中，选择“付款=交易记录\借方\帐户\币种代码（货币）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="4e004-166">在树结构中，选择“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="4e004-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="4e004-167">在树结构中，展开“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="4e004-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="4e004-168">在树结构中，选择“银行帐户\货币（币种代码）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="4e004-169">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-169">Click Bind.</span></span>
51. <span data-ttu-id="4e004-170">在树结构中，选择“银行帐户\IBAN”。</span><span class="sxs-lookup"><span data-stu-id="4e004-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="4e004-171">在树结构中，选择“付款=交易记录\借方\帐户\IBAN 代码 (IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="4e004-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="4e004-172">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-172">Click Bind.</span></span>
54. <span data-ttu-id="4e004-173">在树结构中，选择“付款=交易记录\借方\帐户\编号”。</span><span class="sxs-lookup"><span data-stu-id="4e004-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="4e004-174">在树结构中，选择“银行帐户\银行帐号（帐号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="4e004-175">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-175">Click Bind.</span></span>
57. <span data-ttu-id="4e004-176">在树结构中，展开“付款=交易记录\借方\代理”。</span><span class="sxs-lookup"><span data-stu-id="4e004-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="4e004-177">在树结构中，选择“付款=交易记录\借方\代理\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="4e004-178">在树结构中，选择“银行帐户\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="4e004-179">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-179">Click Bind.</span></span>
61. <span data-ttu-id="4e004-180">在树结构中，选择“付款=交易记录\借方\代理\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="4e004-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="4e004-181">在树结构中，选择“银行帐户\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="4e004-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="4e004-182">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-182">Click Bind.</span></span>
64. <span data-ttu-id="4e004-183">在树结构中，选择“付款=交易记录\借方\代理\SWIFT 代码 (SWIFT)”。</span><span class="sxs-lookup"><span data-stu-id="4e004-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="4e004-184">在树结构中，选择“银行帐户\SWIFT 代码（SWIFT 号）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="4e004-185">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-185">Click Bind.</span></span>
67. <span data-ttu-id="4e004-186">在树结构中，选择“付款=交易记录\借方\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="4e004-187">在树结构中，选择“公司信息（公司）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="4e004-188">在树结构中，展开“公司信息（公司）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="4e004-189">在树结构中，选择“公司信息（公司）\名称”。</span><span class="sxs-lookup"><span data-stu-id="4e004-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="4e004-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-190">Click Bind.</span></span>
72. <span data-ttu-id="4e004-191">在树结构中，选择“付款=交易记录\描述”。</span><span class="sxs-lookup"><span data-stu-id="4e004-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="4e004-192">在树结构中，选择“交易记录\描述（文本）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="4e004-193">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-193">Click Bind.</span></span>
75. <span data-ttu-id="4e004-194">在树结构中，选择“付款=交易记录\端到端标识代码 (End2EndID)”。</span><span class="sxs-lookup"><span data-stu-id="4e004-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="4e004-195">在树结构中，选择“交易记录\$EndToEndID”。</span><span class="sxs-lookup"><span data-stu-id="4e004-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="4e004-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-196">Click Bind.</span></span>
78. <span data-ttu-id="4e004-197">在树结构中，选择“付款=交易记录\指示金额”。</span><span class="sxs-lookup"><span data-stu-id="4e004-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="4e004-198">在树结构中，选择“交易记录\$金额”。</span><span class="sxs-lookup"><span data-stu-id="4e004-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="4e004-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-199">Click Bind.</span></span>
81. <span data-ttu-id="4e004-200">在树结构中，选择“付款=交易记录\交易日期”。</span><span class="sxs-lookup"><span data-stu-id="4e004-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="4e004-201">在树结构中，选择“交易\日期（交易日期）”。</span><span class="sxs-lookup"><span data-stu-id="4e004-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="4e004-202">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="4e004-203">验证创建的映射</span><span class="sxs-lookup"><span data-stu-id="4e004-203">Validate created mapping</span></span>
1. <span data-ttu-id="4e004-204">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="4e004-204">Click Validate.</span></span>
    * <span data-ttu-id="4e004-205">验证新映射以确保所有绑定正常。</span><span class="sxs-lookup"><span data-stu-id="4e004-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="4e004-206">单击此箭头可展开或折叠“错误列表”部分。</span><span class="sxs-lookup"><span data-stu-id="4e004-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="4e004-207">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4e004-207">Click Save.</span></span>
4. <span data-ttu-id="4e004-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4e004-208">Close the page.</span></span>
5. <span data-ttu-id="4e004-209">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4e004-209">Close the page.</span></span>
6. <span data-ttu-id="4e004-210">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4e004-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="4e004-211">更改模型配置的当前版本状态</span><span class="sxs-lookup"><span data-stu-id="4e004-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="4e004-212">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="4e004-212">Click Change status.</span></span>
    * <span data-ttu-id="4e004-213">将设计的模型配置的状态 – 从“草稿”更改为“已完成”，以使其可用于设计付款格式。</span><span class="sxs-lookup"><span data-stu-id="4e004-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="4e004-214">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="4e004-214">Click Complete.</span></span>
    * <span data-ttu-id="4e004-215">选择“完成”。</span><span class="sxs-lookup"><span data-stu-id="4e004-215">Select Complete.</span></span>  
3. <span data-ttu-id="4e004-216">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4e004-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4e004-217">例如，“版本 1”。</span><span class="sxs-lookup"><span data-stu-id="4e004-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="4e004-218">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4e004-218">Click OK.</span></span>
5. <span data-ttu-id="4e004-219">选择当前配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="4e004-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="4e004-220">请注意已创建配置保存为已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="4e004-220">Note that the created configuration is saved as completed version 1.</span></span>  

