---
title: ER 将财务维度用作数据源（第 2 部分 - 模型映射）
description: 本主题介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 2 部分）
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570160"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="2733c-104">ER 将财务维度用作数据源（第 2 部分 - 模型映射）</span><span class="sxs-lookup"><span data-stu-id="2733c-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2733c-105">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="2733c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2733c-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="2733c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="2733c-107">为了完成这些步骤，您必须首先完成“ER 将财务维度用作数据源（第 1 部分：设计数据模型）”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="2733c-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="2733c-108">向模型映射添加所需数据源</span><span class="sxs-lookup"><span data-stu-id="2733c-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="2733c-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="2733c-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2733c-110">在树中，选择“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="2733c-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2733c-111">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="2733c-111">Click Designer.</span></span>
4. <span data-ttu-id="2733c-112">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="2733c-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="2733c-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2733c-113">Click New.</span></span>
6. <span data-ttu-id="2733c-114">在“定义”字段中，选择“条目”。</span><span class="sxs-lookup"><span data-stu-id="2733c-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="2733c-115">在“名称”字段中，键入“维度数据映射”。</span><span class="sxs-lookup"><span data-stu-id="2733c-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="2733c-116">在“描述”字段中，键入“维度数据映射”。</span><span class="sxs-lookup"><span data-stu-id="2733c-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="2733c-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2733c-117">Click Save.</span></span>
10. <span data-ttu-id="2733c-118">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="2733c-118">Click Designer.</span></span>
11. <span data-ttu-id="2733c-119">在树中，选择“Dynamics 365 for Operations\表”'。</span><span class="sxs-lookup"><span data-stu-id="2733c-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="2733c-120">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="2733c-120">Click Add root.</span></span>
13. <span data-ttu-id="2733c-121">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="2733c-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="2733c-122">在“表格”字段中，键入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="2733c-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="2733c-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-123">Click OK.</span></span>
16. <span data-ttu-id="2733c-124">在树中，选择“功能\财务维度细节”。</span><span class="sxs-lookup"><span data-stu-id="2733c-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="2733c-125">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="2733c-125">Click Add root.</span></span>
    * <span data-ttu-id="2733c-126">此数据源指定如何为将把该模型用作数据源的任何报表定义财务维度的范围。</span><span class="sxs-lookup"><span data-stu-id="2733c-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="2733c-127">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2733c-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="2733c-128">在“要求维度”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="2733c-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="2733c-129">选择“是”将允许用户在“用户”对话框窗体中运行时选择维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="2733c-130">如果设置为“否”，默认将使用当前实例的所有财务维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="2733c-131">在“财务维度选择”字段中，选择“法人”。</span><span class="sxs-lookup"><span data-stu-id="2733c-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="2733c-132">选择“所有”将允许用户在“查询”字段中选择当前实例的所需维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="2733c-133">选择“法人”将允许用户在“查询”字段中选择公司的维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="2733c-134">选择“维度”将允许用户选择使用单个纬度集的维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="2733c-135">在“要求主科目”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="2733c-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="2733c-136">将“请求主科目”设置为“是”将允许用户把主科目作为维度列表的一部分选择。</span><span class="sxs-lookup"><span data-stu-id="2733c-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="2733c-137">如果设置为“否”，将不会在维度列表中包含主科目，并且启用“主科目是否必填”选项。</span><span class="sxs-lookup"><span data-stu-id="2733c-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="2733c-138">如果“主科目是否必填”设置为“是”，无论用户如何选择，都应该在维度列表中包含主科目。</span><span class="sxs-lookup"><span data-stu-id="2733c-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="2733c-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-139">Click OK.</span></span>
<span data-ttu-id="2733c-140">![ER 模型映射设计器页面](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="2733c-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="2733c-141">在树中，选择“Dynamics 365 for Operations\表记录”'。</span><span class="sxs-lookup"><span data-stu-id="2733c-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="2733c-142">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="2733c-142">Click Add root.</span></span>
25. <span data-ttu-id="2733c-143">在“名称”字段中，键入“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2733c-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="2733c-144">在“要求查询”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="2733c-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="2733c-145">在“表格”字段中，键入“分类日记帐表”。</span><span class="sxs-lookup"><span data-stu-id="2733c-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="2733c-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-146">Click OK.</span></span>
<span data-ttu-id="2733c-147">![ER 模型映射设计器页面](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="2733c-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="2733c-148">将数据模型元素映射到添加的数据源</span><span class="sxs-lookup"><span data-stu-id="2733c-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="2733c-149">在树中，展开“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2733c-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="2733c-150">在树中，展开“日记帐\交易”。</span><span class="sxs-lookup"><span data-stu-id="2733c-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="2733c-151">在树中，展开“日记帐\交易\维度数据”。</span><span class="sxs-lookup"><span data-stu-id="2733c-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="2733c-152">在树中，展开“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="2733c-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="2733c-153">在树中，展开“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2733c-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="2733c-154">在树中，展开“分类日记帐\<关系”。</span><span class="sxs-lookup"><span data-stu-id="2733c-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="2733c-155">在树中，展开“分类日记帐\<关系\分类日记帐交易”。</span><span class="sxs-lookup"><span data-stu-id="2733c-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="2733c-156">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\凭证”。</span><span class="sxs-lookup"><span data-stu-id="2733c-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="2733c-157">在树中，选择“日记帐\交易\凭证”。</span><span class="sxs-lookup"><span data-stu-id="2733c-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="2733c-158">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-158">Click Bind.</span></span>
11. <span data-ttu-id="2733c-159">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="2733c-160">请注意，对于对财务维度设置为的任何引用（如 LedgerDimension），都有一个相应数据源项 (LedgerDimension.Dimension) 可用。</span><span class="sxs-lookup"><span data-stu-id="2733c-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="2733c-161">此数据源项提供设置为记录的列表的维度的财务维度。</span><span class="sxs-lookup"><span data-stu-id="2733c-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="2733c-162">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="2733c-163">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="2733c-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="2733c-164">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值”。</span><span class="sxs-lookup"><span data-stu-id="2733c-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="2733c-165">在树中，展开“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义”。</span><span class="sxs-lookup"><span data-stu-id="2733c-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="2733c-166">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\定义\名称”。</span><span class="sxs-lookup"><span data-stu-id="2733c-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="2733c-167">在树中，选择“日记帐\交易\维度数据\名称”。</span><span class="sxs-lookup"><span data-stu-id="2733c-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="2733c-168">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-168">Click Bind.</span></span>
19. <span data-ttu-id="2733c-169">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\描述”。</span><span class="sxs-lookup"><span data-stu-id="2733c-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="2733c-170">在树中，选择“日记帐\交易\维度数据\描述”。</span><span class="sxs-lookup"><span data-stu-id="2733c-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="2733c-171">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-171">Click Bind.</span></span>
22. <span data-ttu-id="2733c-172">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度\值\代码”。</span><span class="sxs-lookup"><span data-stu-id="2733c-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="2733c-173">在树中，选择“日记帐\交易\维度数据\代码”。</span><span class="sxs-lookup"><span data-stu-id="2733c-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="2733c-174">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-174">Click Bind.</span></span>
25. <span data-ttu-id="2733c-175">在树中，选择“分类日记帐\<关系\分类日记帐交易记录\Account.Dimension(LedgerDimension.Dimension)\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="2733c-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="2733c-176">在树中，选择“日记帐\交易\维度数据”。</span><span class="sxs-lookup"><span data-stu-id="2733c-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="2733c-177">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-177">Click Bind.</span></span>
<span data-ttu-id="2733c-178">![ER 模型映射设计器页面](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="2733c-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="2733c-179">在树中，选择“分类日记帐\<关系\分类日记帐交易\Debit(AmountCurDebit)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="2733c-180">在树中，选择“日记帐\交易\借方”。</span><span class="sxs-lookup"><span data-stu-id="2733c-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="2733c-181">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-181">Click Bind.</span></span>
31. <span data-ttu-id="2733c-182">在树中，选择“分类日记帐\<关系\分类日记帐交易\Date(TransDate)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="2733c-183">在树中，选择“日记帐\交易\日期”。</span><span class="sxs-lookup"><span data-stu-id="2733c-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="2733c-184">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-184">Click Bind.</span></span>
34. <span data-ttu-id="2733c-185">在树中，选择“分类日记帐\<关系\分类日记帐交易\Currency(CurrencyCode)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="2733c-186">在树中，选择“日记帐\交易\币种”。</span><span class="sxs-lookup"><span data-stu-id="2733c-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="2733c-187">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-187">Click Bind.</span></span>
37. <span data-ttu-id="2733c-188">在树中，选择“分类日记帐\<关系\分类日记帐交易\Credit(AmountCurCredit)”。</span><span class="sxs-lookup"><span data-stu-id="2733c-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="2733c-189">在树中，选择“日记帐\交易\贷方”。</span><span class="sxs-lookup"><span data-stu-id="2733c-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="2733c-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-190">Click Bind.</span></span>
40. <span data-ttu-id="2733c-191">在树中，选择“分类日记帐\<关系\分类日记帐交易”。</span><span class="sxs-lookup"><span data-stu-id="2733c-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="2733c-192">在树中，选择“日记帐\交易”。</span><span class="sxs-lookup"><span data-stu-id="2733c-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="2733c-193">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-193">Click Bind.</span></span>
43. <span data-ttu-id="2733c-194">在树中，选择“分类日记帐\日记帐批号（日记帐编号）”。</span><span class="sxs-lookup"><span data-stu-id="2733c-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="2733c-195">在树中，选择“日记帐\批次”。</span><span class="sxs-lookup"><span data-stu-id="2733c-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="2733c-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-196">Click Bind.</span></span>
46. <span data-ttu-id="2733c-197">在树中，选择“分类日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2733c-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="2733c-198">在树中，选择“日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2733c-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="2733c-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-199">Click Bind.</span></span>
49. <span data-ttu-id="2733c-200">在树中，展开“维度”。</span><span class="sxs-lookup"><span data-stu-id="2733c-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="2733c-201">在树中，展开“维度\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="2733c-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="2733c-202">在树中，展开“维度\主科目和维度\定义”。</span><span class="sxs-lookup"><span data-stu-id="2733c-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="2733c-203">在树中，选择“维度\主科目和维度\定义\名称”。</span><span class="sxs-lookup"><span data-stu-id="2733c-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="2733c-204">在树中，选择“维度设置\代码”。</span><span class="sxs-lookup"><span data-stu-id="2733c-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="2733c-205">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-205">Click Bind.</span></span>
55. <span data-ttu-id="2733c-206">在树中，选择“维度\主科目和维度\定义\报表列名”。</span><span class="sxs-lookup"><span data-stu-id="2733c-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="2733c-207">在树中，选择“维度设置\名称”。</span><span class="sxs-lookup"><span data-stu-id="2733c-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="2733c-208">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-208">Click Bind.</span></span>
58. <span data-ttu-id="2733c-209">在树中，选择“维度\主科目和维度”。</span><span class="sxs-lookup"><span data-stu-id="2733c-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="2733c-210">在树中，选择“维度设置”。</span><span class="sxs-lookup"><span data-stu-id="2733c-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="2733c-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-211">Click Bind.</span></span>
61. <span data-ttu-id="2733c-212">在树中，选择“公司”。</span><span class="sxs-lookup"><span data-stu-id="2733c-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="2733c-213">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="2733c-213">Click Edit.</span></span>
63. <span data-ttu-id="2733c-214">在“expressionAsStringText”字段中，输入“Company.'find()'.'name()'”。</span><span class="sxs-lookup"><span data-stu-id="2733c-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="2733c-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="2733c-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="2733c-216">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2733c-216">Click Save.</span></span>
<span data-ttu-id="2733c-217">![ER 模型映射设计器页面](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="2733c-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="2733c-218">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2733c-218">Close the page.</span></span>
66. <span data-ttu-id="2733c-219">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2733c-219">Click Save.</span></span>
67. <span data-ttu-id="2733c-220">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2733c-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="2733c-221">完成此草稿模型的版本</span><span class="sxs-lookup"><span data-stu-id="2733c-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="2733c-222">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2733c-222">Close the page.</span></span>
2. <span data-ttu-id="2733c-223">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2733c-223">Close the page.</span></span>
3. <span data-ttu-id="2733c-224">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="2733c-224">Click Change status.</span></span>
4. <span data-ttu-id="2733c-225">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="2733c-225">Click Complete.</span></span>
5. <span data-ttu-id="2733c-226">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2733c-226">Click OK.</span></span>
<span data-ttu-id="2733c-227">![ER 模型映射设计器页面](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="2733c-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]