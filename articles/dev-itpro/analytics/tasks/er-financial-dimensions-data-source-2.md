--- 
title: "针对电子申报 (ER) 映射模型以将财务维度用作数据源"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。"
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: a5fa6fb07fb2ba08812826acba748b38738bb468
ms.contentlocale: zh-cn
ms.lasthandoff: 03/09/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="e3e95-103">针对电子申报 (ER) 映射模型以将财务维度用作数据源</span><span class="sxs-lookup"><span data-stu-id="e3e95-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3e95-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="e3e95-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e3e95-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="e3e95-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e3e95-106">若要完成这些步骤，则必须首先完成“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e3e95-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="e3e95-107">向模型映射添加所需数据源</span><span class="sxs-lookup"><span data-stu-id="e3e95-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="e3e95-108">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e3e95-109">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e3e95-110">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-110">Click Designer.</span></span>
4. <span data-ttu-id="e3e95-111">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="e3e95-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-112">Click New.</span></span>
6. <span data-ttu-id="e3e95-113">在“定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="e3e95-114">在“名称”字段中，键入“维度数据映射”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="e3e95-115">在“描述”字段中，键入“维度数据映射”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="e3e95-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-116">Click Save.</span></span>
10. <span data-ttu-id="e3e95-117">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-117">Click Designer.</span></span>
11. <span data-ttu-id="e3e95-118">在树结构中，选择“Dynamics 365 for Operations\表格”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="e3e95-119">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-119">Click Add root.</span></span>
13. <span data-ttu-id="e3e95-120">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="e3e95-121">在“表格”字段中，键入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="e3e95-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-122">Click OK.</span></span>
16. <span data-ttu-id="e3e95-123">在树中，选择“功能\财务维度细节”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="e3e95-124">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-124">Click Add root.</span></span>
    * <span data-ttu-id="e3e95-125">此数据源指定如何为将把该模型用作数据源的任何报表定义财务维度的范围。</span><span class="sxs-lookup"><span data-stu-id="e3e95-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="e3e95-126">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e3e95-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="e3e95-127">在“要求维度”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="e3e95-128">选择“是”将允许用户在“用户”对话框窗体中运行时选择维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="e3e95-129">如果设置为“否”，默认将使用当前实例的所有财务维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="e3e95-130">在“财务维度选择”字段中，选择“法人”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="e3e95-131">选择“所有”将允许用户在“查询”字段中选择当前实例的所需维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="e3e95-132">选择“法人”将允许用户在“查询”字段中选择公司的维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="e3e95-133">选择“维度”将允许用户选择使用单个纬度集的维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="e3e95-134">在“要求主科目”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="e3e95-135">将“请求主科目”设置为“是”将允许用户把主科目作为维度列表的一部分选择。</span><span class="sxs-lookup"><span data-stu-id="e3e95-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="e3e95-136">如果设置为“否”，将不会在维度列表中包含主科目，并且启用“主科目是否必填”选项。</span><span class="sxs-lookup"><span data-stu-id="e3e95-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="e3e95-137">如果“主科目是否必填”设置为“是”，无论用户如何选择，都应该在维度列表中包含主科目。</span><span class="sxs-lookup"><span data-stu-id="e3e95-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="e3e95-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-138">Click OK.</span></span>
23. <span data-ttu-id="e3e95-139">在树结构中，选择“Dynamics 365 for Operations\表格记录”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="e3e95-140">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-140">Click Add root.</span></span>
25. <span data-ttu-id="e3e95-141">在“名称”字段中，键入“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="e3e95-142">在“要求查询”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="e3e95-143">在“表格”字段中，键入“分类日记帐表”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="e3e95-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="e3e95-145">将数据模型元素映射到添加的数据源</span><span class="sxs-lookup"><span data-stu-id="e3e95-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="e3e95-146">在树中，展开“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="e3e95-147">在树中，展开“日记帐\交易”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="e3e95-148">在树中，展开“日记帐\交易\维度数据”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="e3e95-149">在树中，展开“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="e3e95-150">在树中，展开“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="e3e95-151">在树中，展开“分类日记帐\<关系”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="e3e95-152">在树中，展开“分类日记帐\<关系\分类日记帐交易”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="e3e95-153">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\凭证”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="e3e95-154">在树中，选择“日记帐\交易\凭证”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="e3e95-155">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-155">Click Bind.</span></span>
11. <span data-ttu-id="e3e95-156">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="e3e95-157">请注意，对于对财务维度设置为的任何引用（如 LedgerDimension），都有一个相应数据源项 (LedgerDimension.Dimension) 可用。</span><span class="sxs-lookup"><span data-stu-id="e3e95-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="e3e95-158">此数据源项提供设置为记录的列表的维度的财务维度。</span><span class="sxs-lookup"><span data-stu-id="e3e95-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="e3e95-159">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="e3e95-160">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="e3e95-161">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="e3e95-162">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="e3e95-163">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义\名称”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="e3e95-164">在树中，选择“日记帐\交易\维度数据\名称”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="e3e95-165">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-165">Click Bind.</span></span>
19. <span data-ttu-id="e3e95-166">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\描述”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="e3e95-167">在树中，选择“日记帐\交易\维度数据\描述”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="e3e95-168">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-168">Click Bind.</span></span>
22. <span data-ttu-id="e3e95-169">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\代码”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="e3e95-170">在树中，选择“日记帐\交易\维度数据\代码”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="e3e95-171">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-171">Click Bind.</span></span>
25. <span data-ttu-id="e3e95-172">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="e3e95-173">在树中，选择“日记帐\交易\维度数据”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="e3e95-174">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-174">Click Bind.</span></span>
28. <span data-ttu-id="e3e95-175">在树中，选择“分类日记帐\<关系\分类日记帐交易\Debit(AmountCurDebit)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="e3e95-176">在树中，选择“日记帐\交易\借方”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="e3e95-177">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-177">Click Bind.</span></span>
31. <span data-ttu-id="e3e95-178">在树中，选择“分类日记帐\<关系\分类日记帐交易\Date(TransDate)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="e3e95-179">在树中，选择“日记帐\交易\日期”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="e3e95-180">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-180">Click Bind.</span></span>
34. <span data-ttu-id="e3e95-181">在树中，选择“分类日记帐\<关系\分类日记帐交易\Currency(CurrencyCode)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="e3e95-182">在树中，选择“日记帐\交易\币种”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="e3e95-183">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-183">Click Bind.</span></span>
37. <span data-ttu-id="e3e95-184">在树中，选择“分类日记帐\<关系\分类日记帐交易\Credit(AmountCurCredit)”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="e3e95-185">在树中，选择“日记帐\交易\贷方”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="e3e95-186">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-186">Click Bind.</span></span>
40. <span data-ttu-id="e3e95-187">在树中，选择“分类日记帐\<关系\分类日记帐交易”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="e3e95-188">在树中，选择“日记帐\交易”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="e3e95-189">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-189">Click Bind.</span></span>
43. <span data-ttu-id="e3e95-190">在树中，选择“分类日记帐\日记帐批号（日记帐编号）”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="e3e95-191">在树中，选择“日记帐\批次”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="e3e95-192">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-192">Click Bind.</span></span>
46. <span data-ttu-id="e3e95-193">在树中，选择“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="e3e95-194">在树中，选择“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="e3e95-195">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-195">Click Bind.</span></span>
49. <span data-ttu-id="e3e95-196">在树中，展开“维度”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="e3e95-197">在树中，展开“维度\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="e3e95-198">在树中，展开“维度\主科目和维度\定义”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="e3e95-199">在树中，选择“维度\主科目和维度\定义\名称”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="e3e95-200">在树中，选择“维度设置\代码”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="e3e95-201">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-201">Click Bind.</span></span>
55. <span data-ttu-id="e3e95-202">在树中，选择“维度\主科目和维度\定义\报表列名”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="e3e95-203">在树中，选择“维度设置\名称”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="e3e95-204">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-204">Click Bind.</span></span>
58. <span data-ttu-id="e3e95-205">在树中，选择“维度\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="e3e95-206">在树中，选择“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="e3e95-207">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-207">Click Bind.</span></span>
61. <span data-ttu-id="e3e95-208">在树中，选择“公司”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="e3e95-209">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-209">Click Edit.</span></span>
63. <span data-ttu-id="e3e95-210">在“expressionAsStringText”字段中，输入“Company.'find()'.'name()'”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="e3e95-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="e3e95-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="e3e95-212">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-212">Click Save.</span></span>
65. <span data-ttu-id="e3e95-213">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3e95-213">Close the page.</span></span>
66. <span data-ttu-id="e3e95-214">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-214">Click Save.</span></span>
67. <span data-ttu-id="e3e95-215">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3e95-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="e3e95-216">完成此草稿模型的版本</span><span class="sxs-lookup"><span data-stu-id="e3e95-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="e3e95-217">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3e95-217">Close the page.</span></span>
2. <span data-ttu-id="e3e95-218">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e3e95-218">Close the page.</span></span>
3. <span data-ttu-id="e3e95-219">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-219">Click Change status.</span></span>
4. <span data-ttu-id="e3e95-220">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-220">Click Complete.</span></span>
5. <span data-ttu-id="e3e95-221">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e3e95-221">Click OK.</span></span>


