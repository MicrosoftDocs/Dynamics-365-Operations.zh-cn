--- 
title: "针对电子申报 (ER) 定义模型映射并选择数据源"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何为电子报表 (ER) 数据模型选择数据源。"
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
ms.openlocfilehash: 512e24b5d0e20f00890e2a9abfe45b660a913913
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="cf408-103">针对电子申报 (ER) 定义模型映射并选择数据源</span><span class="sxs-lookup"><span data-stu-id="cf408-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf408-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何为电子报表 (ER) 数据模型选择数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="cf408-105">数据源将绑定到设计时所选数据模型的各个部分中，并在运行时间生成该数据模型的业务数据。</span><span class="sxs-lookup"><span data-stu-id="cf408-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="cf408-106">在此示例中，您将为给示例公司 Litware，Inc. 创建的现有数据模型选择数据源。为了完成这些步骤，您首先必须完成“创建新数据模型”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="cf408-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="cf408-107">打开“电子申报配置”树结构</span><span class="sxs-lookup"><span data-stu-id="cf408-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="cf408-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="cf408-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cf408-109">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="cf408-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="cf408-110">插入新的模型映射</span><span class="sxs-lookup"><span data-stu-id="cf408-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="cf408-111">在树结构中，选择“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="cf408-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="cf408-112">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="cf408-112">Click Designer.</span></span>
3. <span data-ttu-id="cf408-113">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="cf408-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="cf408-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cf408-114">Click New.</span></span>
    * <span data-ttu-id="cf408-115">这将创建映射数据模型到数据源的新记录。</span><span class="sxs-lookup"><span data-stu-id="cf408-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="cf408-116">在此示例中，您将映射数据模型到所需付款类型 — 贷方转帐的数据源中。</span><span class="sxs-lookup"><span data-stu-id="cf408-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="cf408-117">可以为特定数据模型设计多个映射。</span><span class="sxs-lookup"><span data-stu-id="cf408-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="cf408-118">例如，您可以为不同类型的付款创建一个映射，如直接借记或贷方转帐。</span><span class="sxs-lookup"><span data-stu-id="cf408-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="cf408-119">在此示例中，您将创建贷方转帐的映射。</span><span class="sxs-lookup"><span data-stu-id="cf408-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="cf408-120">在“名称”字段中，键入“CT 映射”。</span><span class="sxs-lookup"><span data-stu-id="cf408-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="cf408-121">CT 映射</span><span class="sxs-lookup"><span data-stu-id="cf408-121">CT mapping</span></span>  
6. <span data-ttu-id="cf408-122">在“描述”字段，键入“付款模型映射 CT”。</span><span class="sxs-lookup"><span data-stu-id="cf408-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="cf408-123">付款模型映射 CT</span><span class="sxs-lookup"><span data-stu-id="cf408-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="cf408-124">在“定义”字段中，键入“客户贷方转帐发起”。</span><span class="sxs-lookup"><span data-stu-id="cf408-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="cf408-125">客户贷方转帐发起</span><span class="sxs-lookup"><span data-stu-id="cf408-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="cf408-126">改变定义。</span><span class="sxs-lookup"><span data-stu-id="cf408-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="cf408-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cf408-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="cf408-128">定义当前模型映射所需的数据源</span><span class="sxs-lookup"><span data-stu-id="cf408-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="cf408-129">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="cf408-129">Click Designer.</span></span>
2. <span data-ttu-id="cf408-130">在树结构中，选择“Dynamics 365 for Operations\表格记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="cf408-131">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="cf408-131">Click Add root.</span></span>
    * <span data-ttu-id="cf408-132">输入此数据源以访问付款交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf408-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="cf408-133">在“名称”字段中，键入“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="cf408-134">交易</span><span class="sxs-lookup"><span data-stu-id="cf408-134">Transactions</span></span>  
5. <span data-ttu-id="cf408-135">在“标签”字段中，输入“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="cf408-136">交易</span><span class="sxs-lookup"><span data-stu-id="cf408-136">Transactions</span></span>  
6. <span data-ttu-id="cf408-137">在“帮助”字段中，输入“分类日记帐行”。</span><span class="sxs-lookup"><span data-stu-id="cf408-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="cf408-138">分类日记帐行</span><span class="sxs-lookup"><span data-stu-id="cf408-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="cf408-139">在“要求查询”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="cf408-140">选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-140">Select Yes.</span></span>  
8. <span data-ttu-id="cf408-141">在“表格”字段中，键入“分类日记帐交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="cf408-142">分类日记帐交易记录</span><span class="sxs-lookup"><span data-stu-id="cf408-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="cf408-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-143">Click OK.</span></span>
    * <span data-ttu-id="cf408-144">为当前数据模型选择“分类日记帐交易记录”表作为数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="cf408-145">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="cf408-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="cf408-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cf408-146">Click Add.</span></span>
    * <span data-ttu-id="cf408-147">单击“添加”以添加新的计算字段。</span><span class="sxs-lookup"><span data-stu-id="cf408-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="cf408-148">在“名称”字段中，键入“$EndToEndID”。</span><span class="sxs-lookup"><span data-stu-id="cf408-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="cf408-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="cf408-149">$EndToEndID</span></span>  
13. <span data-ttu-id="cf408-150">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="cf408-150">Click Edit formula.</span></span>
14. <span data-ttu-id="cf408-151">在树结构中，选择“字符串\连接”。</span><span class="sxs-lookup"><span data-stu-id="cf408-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="cf408-152">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="cf408-152">Click Add function.</span></span>
16. <span data-ttu-id="cf408-153">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="cf408-154">在树结构中，选择“交易记录\凭证”。</span><span class="sxs-lookup"><span data-stu-id="cf408-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="cf408-155">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="cf408-155">Click Add data source.</span></span>
19. <span data-ttu-id="cf408-156">在“公式”字段中，输入“CONCATENATE(Transactions.Voucher, "-",”。</span><span class="sxs-lookup"><span data-stu-id="cf408-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="cf408-157">在公式结尾键入[ , “-“, ]。</span><span class="sxs-lookup"><span data-stu-id="cf408-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="cf408-158">在树结构中，选择“字符串\文本”。</span><span class="sxs-lookup"><span data-stu-id="cf408-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="cf408-159">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="cf408-159">Click Add function.</span></span>
22. <span data-ttu-id="cf408-160">在树结构中，选择“交易记录\记录 ID”。</span><span class="sxs-lookup"><span data-stu-id="cf408-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="cf408-161">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="cf408-161">Click Add data source.</span></span>
24. <span data-ttu-id="cf408-162">在“公式”字段中，输入“CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”。</span><span class="sxs-lookup"><span data-stu-id="cf408-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="cf408-163">在公式结尾键入[))]。</span><span class="sxs-lookup"><span data-stu-id="cf408-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="cf408-164">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cf408-164">Click Save.</span></span>
    * <span data-ttu-id="cf408-165">确保创建的公式没有发现错误。</span><span class="sxs-lookup"><span data-stu-id="cf408-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="cf408-166">查看公式编辑器控制项下的“错误”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cf408-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="cf408-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-167">Close the page.</span></span>
27. <span data-ttu-id="cf408-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-168">Click OK.</span></span>
    * <span data-ttu-id="cf408-169">添加计算字段到此数据源中。</span><span class="sxs-lookup"><span data-stu-id="cf408-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="cf408-170">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cf408-170">Click Add.</span></span>
    * <span data-ttu-id="cf408-171">单击“添加”以添加新的计算字段。</span><span class="sxs-lookup"><span data-stu-id="cf408-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="cf408-172">在“名称”字段中，键入“$金额”。</span><span class="sxs-lookup"><span data-stu-id="cf408-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="cf408-173">$金额</span><span class="sxs-lookup"><span data-stu-id="cf408-173">$Amount</span></span>  
30. <span data-ttu-id="cf408-174">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="cf408-174">Click Edit formula.</span></span>
31. <span data-ttu-id="cf408-175">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="cf408-176">在树结构中，选择“交易记录\借方（借方币种金额）”。</span><span class="sxs-lookup"><span data-stu-id="cf408-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="cf408-177">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="cf408-177">Click Add data source.</span></span>
34. <span data-ttu-id="cf408-178">在“公式”字段中，输入“Transactions.AmountCurDebit -”。</span><span class="sxs-lookup"><span data-stu-id="cf408-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="cf408-179">在公式结尾键入[ - ]。</span><span class="sxs-lookup"><span data-stu-id="cf408-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="cf408-180">在树结构中，选择“交易记录\贷方（贷方币种金额）”。</span><span class="sxs-lookup"><span data-stu-id="cf408-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="cf408-181">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="cf408-181">Click Add data source.</span></span>
37. <span data-ttu-id="cf408-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cf408-182">Click Save.</span></span>
38. <span data-ttu-id="cf408-183">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-183">Close the page.</span></span>
39. <span data-ttu-id="cf408-184">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-184">Click OK.</span></span>
    * <span data-ttu-id="cf408-185">这将添加“$计算金额”字段到当前数据模型的所选数据源中。</span><span class="sxs-lookup"><span data-stu-id="cf408-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="cf408-186">在树结构中，选择“交易记录\$金额”。</span><span class="sxs-lookup"><span data-stu-id="cf408-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="cf408-187">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="cf408-188">在树结构中，展开或折叠“交易记录\$金额”。</span><span class="sxs-lookup"><span data-stu-id="cf408-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="cf408-189">在树中，展开或折叠“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="cf408-190">在树结构中，选择“Dynamics 365 for Operations\表格记录”。</span><span class="sxs-lookup"><span data-stu-id="cf408-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="cf408-191">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="cf408-191">Click Add root.</span></span>
    * <span data-ttu-id="cf408-192">输入此数据源以访问公司的银行帐户详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf408-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="cf408-193">在“名称”字段中，键入“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cf408-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="cf408-194">银行帐户</span><span class="sxs-lookup"><span data-stu-id="cf408-194">BankAccount</span></span>  
47. <span data-ttu-id="cf408-195">在“标签”字段中，输入“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cf408-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="cf408-196">银行帐户</span><span class="sxs-lookup"><span data-stu-id="cf408-196">Bank Account</span></span>  
48. <span data-ttu-id="cf408-197">在“帮助”字段中，输入“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cf408-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="cf408-198">银行帐户</span><span class="sxs-lookup"><span data-stu-id="cf408-198">Bank Account</span></span>  
49. <span data-ttu-id="cf408-199">在“要求查询”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="cf408-200">选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-200">Select Yes.</span></span>  
50. <span data-ttu-id="cf408-201">在“表格”字段中，键入“银行帐户表”。</span><span class="sxs-lookup"><span data-stu-id="cf408-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="cf408-202">银行帐户表</span><span class="sxs-lookup"><span data-stu-id="cf408-202">BankAccountTable</span></span>  
51. <span data-ttu-id="cf408-203">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-203">Click OK.</span></span>
    * <span data-ttu-id="cf408-204">为当前数据模型选择“银行帐户表”作为数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="cf408-205">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="cf408-205">Click Add root.</span></span>
    * <span data-ttu-id="cf408-206">输入此数据源以访问公司的基本信息。</span><span class="sxs-lookup"><span data-stu-id="cf408-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="cf408-207">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="cf408-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="cf408-208">公司</span><span class="sxs-lookup"><span data-stu-id="cf408-208">Company</span></span>  
54. <span data-ttu-id="cf408-209">在“标签”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cf408-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="cf408-210">公司信息</span><span class="sxs-lookup"><span data-stu-id="cf408-210">Company information</span></span>  
55. <span data-ttu-id="cf408-211">在“帮助”字段中，输入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="cf408-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="cf408-212">公司信息</span><span class="sxs-lookup"><span data-stu-id="cf408-212">Company information</span></span>  
56. <span data-ttu-id="cf408-213">在“要求查询”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="cf408-214">选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cf408-214">Select Yes.</span></span>  
57. <span data-ttu-id="cf408-215">在“表格”字段中，键入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="cf408-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="cf408-216">公司信息</span><span class="sxs-lookup"><span data-stu-id="cf408-216">CompanyInfo</span></span>  
58. <span data-ttu-id="cf408-217">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-217">Click OK.</span></span>
    * <span data-ttu-id="cf408-218">为当前数据模型选择“公司信息”表作为数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="cf408-219">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="cf408-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="cf408-220">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="cf408-220">Click Add root.</span></span>
    * <span data-ttu-id="cf408-221">插入“计算”字段作为新数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="cf408-222">在“名称”字段中，键入“处理日期时间”“。</span><span class="sxs-lookup"><span data-stu-id="cf408-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="cf408-223">处理日期时间</span><span class="sxs-lookup"><span data-stu-id="cf408-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="cf408-224">在“标签”字段中，输入“处理日期和时间”。</span><span class="sxs-lookup"><span data-stu-id="cf408-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="cf408-225">处理日期和时间</span><span class="sxs-lookup"><span data-stu-id="cf408-225">Processing date & time</span></span>  
63. <span data-ttu-id="cf408-226">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="cf408-226">Click Edit formula.</span></span>
64. <span data-ttu-id="cf408-227">在树结构中，选择“日期/时间\SESSIONNOW”。</span><span class="sxs-lookup"><span data-stu-id="cf408-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="cf408-228">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="cf408-228">Click Add function.</span></span>
66. <span data-ttu-id="cf408-229">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cf408-229">Click Save.</span></span>
67. <span data-ttu-id="cf408-230">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-230">Close the page.</span></span>
68. <span data-ttu-id="cf408-231">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cf408-231">Click OK.</span></span>
    * <span data-ttu-id="cf408-232">为当前数据模型添加“处理日期时间”计算字段作为数据源。</span><span class="sxs-lookup"><span data-stu-id="cf408-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="cf408-233">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cf408-233">Click Save.</span></span>
70. <span data-ttu-id="cf408-234">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-234">Close the page.</span></span>
71. <span data-ttu-id="cf408-235">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-235">Close the page.</span></span>
72. <span data-ttu-id="cf408-236">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf408-236">Close the page.</span></span>

