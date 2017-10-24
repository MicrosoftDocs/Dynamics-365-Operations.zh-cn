--- 
title: "设置中国式凭证"
description: "此过程逐步演示如何使用特定演示数据设置中国式凭证。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 139940ac89c6886577d466f7e5a5190944907b38
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-chinese-vouchers"></a><span data-ttu-id="b8402-103">设置中国式凭证</span><span class="sxs-lookup"><span data-stu-id="b8402-103">Set up Chinese vouchers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8402-104">此过程逐步演示如何使用特定演示数据设置中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="b8402-104">This procedure walks you through setting up Chinese vouchers with specific demo data.</span></span>
<span data-ttu-id="b8402-105">中国式凭证编号是中国式财务报表的基础。</span><span class="sxs-lookup"><span data-stu-id="b8402-105">Chinese voucher numbers are the foundation for Chinese financial reporting.</span></span> <span data-ttu-id="b8402-106">必须先设置此类编号，才能执行任何财务交易过帐。</span><span class="sxs-lookup"><span data-stu-id="b8402-106">You must set them up before you do any financial transaction posting.</span></span> <span data-ttu-id="b8402-107">只能按照此过程的演示一次一个设置凭证，也可以使用凭证类型设置向导设置。</span><span class="sxs-lookup"><span data-stu-id="b8402-107">You can set up the vouchers one at a time as this procedure demonstrates or you can use the Voucher type setup wizard to set them up.</span></span>
<span data-ttu-id="b8402-108">本流程是用演示公司 CNMF 数据生成的。</span><span class="sxs-lookup"><span data-stu-id="b8402-108">This procedure was created using the demo data company CNMF.</span></span> <span data-ttu-id="b8402-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="b8402-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-chinese-voucher-type"></a><span data-ttu-id="b8402-110">设置中国式凭证类型</span><span class="sxs-lookup"><span data-stu-id="b8402-110">Set up Chinese Voucher Type</span></span>
1. <span data-ttu-id="b8402-111">转到“总帐”>“日记帐设置”>“中国式凭证类型”>“凭证类型”。</span><span class="sxs-lookup"><span data-stu-id="b8402-111">Go to General ledger > Journal setup > Chinese voucher type > Voucher type.</span></span>
2. <span data-ttu-id="b8402-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8402-112">Click New.</span></span>
3. <span data-ttu-id="b8402-113">在“凭证类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-113">In the Voucher type field, type a value.</span></span>
4. <span data-ttu-id="b8402-114">在“凭证类型编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-114">In the Voucher type number field, type a value.</span></span>
    * <span data-ttu-id="b8402-115">此值用作 GB/T24589 导出文件中的类型 ID。</span><span class="sxs-lookup"><span data-stu-id="b8402-115">This value is used as the Type ID in the GB/T24589 export file.</span></span>  
5. <span data-ttu-id="b8402-116">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-116">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b8402-117">在“优先”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b8402-117">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="b8402-118">对于从原始凭证生成的财务凭证（如过帐销售发票），如果根据凭证类型规则有多个凭证类型匹配，将分配第一优先级凭证类型。</span><span class="sxs-lookup"><span data-stu-id="b8402-118">For financial vouchers that are generated from source documents, such as posting sales invoices, if more than one voucher type is matched according the voucher type rule, the first priority voucher type will be assigned.</span></span>  <span data-ttu-id="b8402-119">也可以将某个凭证类型设置为“缺省”，用作缺省凭证类型。</span><span class="sxs-lookup"><span data-stu-id="b8402-119">You also can set a voucher type as Default, which will be used as the default voucher type.</span></span>  
7. <span data-ttu-id="b8402-120">在数序码字段，输入或选一哥值。</span><span class="sxs-lookup"><span data-stu-id="b8402-120">In the Number sequence code field, enter or select a value.</span></span>
8. <span data-ttu-id="b8402-121">在“打印布局组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-121">In the Print layout group field, enter or select a value.</span></span>
9. <span data-ttu-id="b8402-122">输入负责创建这种类型的配置的人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="b8402-122">Enter the name of the person who is responsible for making this type of voucher.</span></span>
    * <span data-ttu-id="b8402-123">此名称将在 GB/T24589 导出文件中使用。</span><span class="sxs-lookup"><span data-stu-id="b8402-123">This name will be used in the GB/T24589 export file.</span></span> <span data-ttu-id="b8402-124">此人应该不是审核此凭证类型的人。</span><span class="sxs-lookup"><span data-stu-id="b8402-124">This should be a different person than the person who can approve this type of voucher.</span></span>  
10. <span data-ttu-id="b8402-125">输入可审核这种类型的凭证的人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="b8402-125">Enter the name of the person who can approve this type of voucher.</span></span>
    * <span data-ttu-id="b8402-126">此名称将在 GB/T24589 导出文件中使用。</span><span class="sxs-lookup"><span data-stu-id="b8402-126">This name will be used in the GB/T24589 export file.</span></span> <span data-ttu-id="b8402-127">此人应该不是创建此凭证类型的人。</span><span class="sxs-lookup"><span data-stu-id="b8402-127">This should be a different person than the person who can create this type of voucher.</span></span>  
11. <span data-ttu-id="b8402-128">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-128">Click Add.</span></span>
    * <span data-ttu-id="b8402-129">凭证类型规则定义凭证的条件。</span><span class="sxs-lookup"><span data-stu-id="b8402-129">Voucher type rules define the criteria for vouchers.</span></span> <span data-ttu-id="b8402-130">只能将凭证中满足这些条件的交易分配给此凭证类型和过帐这些交易。</span><span class="sxs-lookup"><span data-stu-id="b8402-130">Only transactions in a voucher that meet these criteria can be assigned to this voucher type and can be posted.</span></span> <span data-ttu-id="b8402-131">在此示例中，只有此现金类型凭证中的借贷双方中才允许银行帐户和现金帐户。</span><span class="sxs-lookup"><span data-stu-id="b8402-131">In this example, only bank accounts and cash accounts are allowed in debit and credit sides for this Cash type voucher.</span></span>  
12. <span data-ttu-id="b8402-132">在“限制”字段中，选择“借方只有”。</span><span class="sxs-lookup"><span data-stu-id="b8402-132">In the Restriction field, select 'All debits must include (one of the selected accounts)'.</span></span>
13. <span data-ttu-id="b8402-133">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-133">Click Add.</span></span>
14. <span data-ttu-id="b8402-134">在“主科目”字段中，指定值“100101”。</span><span class="sxs-lookup"><span data-stu-id="b8402-134">In the Main account field, specify the values '100101'.</span></span>
15. <span data-ttu-id="b8402-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-135">Click Add.</span></span>
16. <span data-ttu-id="b8402-136">在“主科目”字段中，指定值“100102”。</span><span class="sxs-lookup"><span data-stu-id="b8402-136">In the Main account field, specify the values '100102'.</span></span>
17. <span data-ttu-id="b8402-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-137">Click Add.</span></span>
18. <span data-ttu-id="b8402-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b8402-138">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="b8402-139">在“主科目”字段中，指定值“100103”。</span><span class="sxs-lookup"><span data-stu-id="b8402-139">In the Main account field, specify the values '100103'.</span></span>
20. <span data-ttu-id="b8402-140">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-140">Click Add.</span></span>
21. <span data-ttu-id="b8402-141">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-141">In the Account type field, select 'Bank'.</span></span>
22. <span data-ttu-id="b8402-142">在“主科目”字段中，指定值“CNYBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-142">In the Main account field, specify the values 'CNYBANK'.</span></span>
23. <span data-ttu-id="b8402-143">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-143">Click Add.</span></span>
24. <span data-ttu-id="b8402-144">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-144">In the Account type field, select 'Bank'.</span></span>
25. <span data-ttu-id="b8402-145">在“主科目”字段中，指定值“USDBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-145">In the Main account field, specify the values 'USDBANK'.</span></span>
26. <span data-ttu-id="b8402-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-146">Click Add.</span></span>
27. <span data-ttu-id="b8402-147">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-147">In the Account type field, select 'Bank'.</span></span>
28. <span data-ttu-id="b8402-148">在“主科目”字段中，指定值“HKDBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-148">In the Main account field, specify the values 'HKDBANK'.</span></span>
29. <span data-ttu-id="b8402-149">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-149">Click Add.</span></span>
30. <span data-ttu-id="b8402-150">在“限制”字段中，选择“贷方只有”。</span><span class="sxs-lookup"><span data-stu-id="b8402-150">In the Restriction field, select 'All credits must include (one of the selected accounts)'.</span></span>
31. <span data-ttu-id="b8402-151">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-151">Click Add.</span></span>
32. <span data-ttu-id="b8402-152">在“主科目”字段中，指定值“100101”。</span><span class="sxs-lookup"><span data-stu-id="b8402-152">In the Main account field, specify the values '100101'.</span></span>
33. <span data-ttu-id="b8402-153">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-153">Click Add.</span></span>
34. <span data-ttu-id="b8402-154">在“主科目”字段中，指定值“100102”。</span><span class="sxs-lookup"><span data-stu-id="b8402-154">In the Main account field, specify the values '100102'.</span></span>
35. <span data-ttu-id="b8402-155">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-155">Click Add.</span></span>
36. <span data-ttu-id="b8402-156">在“主科目”字段中，指定值“100103”。</span><span class="sxs-lookup"><span data-stu-id="b8402-156">In the Main account field, specify the values '100103'.</span></span>
37. <span data-ttu-id="b8402-157">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-157">Click Add.</span></span>
38. <span data-ttu-id="b8402-158">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-158">In the Account type field, select 'Bank'.</span></span>
39. <span data-ttu-id="b8402-159">在“主科目”字段中，指定值“CNYBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-159">In the Main account field, specify the values 'CNYBANK'.</span></span>
40. <span data-ttu-id="b8402-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-160">Click Add.</span></span>
41. <span data-ttu-id="b8402-161">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-161">In the Account type field, select 'Bank'.</span></span>
42. <span data-ttu-id="b8402-162">在“主科目”字段中，指定值“USDBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-162">In the Main account field, specify the values 'USDBANK'.</span></span>
43. <span data-ttu-id="b8402-163">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-163">Click Add.</span></span>
44. <span data-ttu-id="b8402-164">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="b8402-164">In the Account type field, select 'Bank'.</span></span>
45. <span data-ttu-id="b8402-165">在“主科目”字段中，指定值“HKDBANK”。</span><span class="sxs-lookup"><span data-stu-id="b8402-165">In the Main account field, specify the values 'HKDBANK'.</span></span>
46. <span data-ttu-id="b8402-166">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8402-166">Click Save.</span></span>

## <a name="setup-additional-parameters"></a><span data-ttu-id="b8402-167">设置更多参数</span><span class="sxs-lookup"><span data-stu-id="b8402-167">Setup additional parameters</span></span>
1. <span data-ttu-id="b8402-168">转到总分类记账>分类记账设置 >总分类记账参数。</span><span class="sxs-lookup"><span data-stu-id="b8402-168">Go to General ledger > Ledger setup > General ledger parameters.</span></span>
    * <span data-ttu-id="b8402-169">在"总帐参数"页面中，必须首先启用中国式凭证，然后选择允许会计年度中包含重复凭证。</span><span class="sxs-lookup"><span data-stu-id="b8402-169">In the General ledger parameter page, you must first enable Chinese Voucher, then select to allow Duplicate vouchers in fiscal year.</span></span> <span data-ttu-id="b8402-170">需要为每个会计期间从 1 开始为中国式凭证编号。</span><span class="sxs-lookup"><span data-stu-id="b8402-170">Chinse vouchers need to be renumbered from 1 for each fiscal period.</span></span>  
2. <span data-ttu-id="b8402-171">然后在“有效凭证检验”字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="b8402-171">In the Check for voucher used field, select an option.</span></span>

## <a name="set-up-the-print-layout"></a><span data-ttu-id="b8402-172">设置打印布局</span><span class="sxs-lookup"><span data-stu-id="b8402-172">Set up the print layout</span></span>
1. <span data-ttu-id="b8402-173">转到“总帐”>“日记帐设置”>“中国式凭证类型”>“打印布局”。</span><span class="sxs-lookup"><span data-stu-id="b8402-173">Go to General ledger > Journal setup > Chinese voucher type > Print layout.</span></span>
2. <span data-ttu-id="b8402-174">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8402-174">Click New.</span></span>
3. <span data-ttu-id="b8402-175">在“打印布局组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-175">In the Print layout group field, type a value.</span></span>
4. <span data-ttu-id="b8402-176">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b8402-176">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b8402-177">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-177">Click Add.</span></span>
6. <span data-ttu-id="b8402-178">在“打印布局代码”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b8402-178">In the Print layout code field, select an option.</span></span>
7. <span data-ttu-id="b8402-179">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b8402-179">Click Add.</span></span>
8. <span data-ttu-id="b8402-180">在“打印布局代码”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b8402-180">In the Print layout code field, select an option.</span></span>
9. <span data-ttu-id="b8402-181">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8402-181">Click Save.</span></span>

