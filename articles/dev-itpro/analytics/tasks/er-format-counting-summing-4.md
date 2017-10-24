--- 
title: "针对电子申报 (ER) 运行执行盘点和合计的格式"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="8ad40-103">针对电子申报 (ER) 运行执行盘点和合计的格式</span><span class="sxs-lookup"><span data-stu-id="8ad40-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ad40-104">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="8ad40-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8ad40-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="8ad40-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="8ad40-106">必须首先完成“ER 配置格式以执行盘点和合计（第 3 部分：使用计算创建输出）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="8ad40-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="8ad40-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="8ad40-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="8ad40-108">为生成内部统计报表测试此配置</span><span class="sxs-lookup"><span data-stu-id="8ad40-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="8ad40-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8ad40-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8ad40-111">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="8ad40-112">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="8ad40-113">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="8ad40-114">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="8ad40-115">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-115">Click User parameters.</span></span>
8. <span data-ttu-id="8ad40-116">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="8ad40-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-117">Click OK.</span></span>
10. <span data-ttu-id="8ad40-118">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-118">Click Edit.</span></span>
11. <span data-ttu-id="8ad40-119">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="8ad40-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-120">Click Save.</span></span>
13. <span data-ttu-id="8ad40-121">转到缴税>设置 >外贸>外贸参数。</span><span class="sxs-lookup"><span data-stu-id="8ad40-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="8ad40-122">展开“电子报表”部分。</span><span class="sxs-lookup"><span data-stu-id="8ad40-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="8ad40-123">选择“带盘点和合计的内部统计 (DE)”配置。</span><span class="sxs-lookup"><span data-stu-id="8ad40-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="8ad40-124">选择“带盘点和合计的内部统计 (DE)”配置。</span><span class="sxs-lookup"><span data-stu-id="8ad40-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="8ad40-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-125">Click Save.</span></span>
18. <span data-ttu-id="8ad40-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8ad40-126">Close the page.</span></span>
19. <span data-ttu-id="8ad40-127">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="8ad40-128">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-128">Click Output.</span></span>
21. <span data-ttu-id="8ad40-129">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-129">Click Report.</span></span>
    * <span data-ttu-id="8ad40-130">运行内部统计报表生成过程。</span><span class="sxs-lookup"><span data-stu-id="8ad40-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="8ad40-131">在“开始日期”字段中，将日期设置为“2000-01-01”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="8ad40-132">为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。</span><span class="sxs-lookup"><span data-stu-id="8ad40-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="8ad40-133">在“结束日期”字段中，将日期设置为“2022-12-31”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="8ad40-134">为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。</span><span class="sxs-lookup"><span data-stu-id="8ad40-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="8ad40-135">在“方向”字段中，选择“到货”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="8ad40-136">在“生成文档”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="8ad40-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-137">Click OK.</span></span>
    * <span data-ttu-id="8ad40-138">查看创建的输出，该输出的结尾包含汇总行。</span><span class="sxs-lookup"><span data-stu-id="8ad40-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="8ad40-139">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-139">Click New.</span></span>
28. <span data-ttu-id="8ad40-140">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8ad40-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="8ad40-141">在“方向”字段中，选择“发货”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="8ad40-142">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8ad40-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="8ad40-143">在“商品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8ad40-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="8ad40-144">将“重量”设置为“10”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="8ad40-145">将“发票金额”设置为“10000”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="8ad40-146">将“统计金额”设置为“10000”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="8ad40-147">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-147">Click Output.</span></span>
36. <span data-ttu-id="8ad40-148">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-148">Click Report.</span></span>
37. <span data-ttu-id="8ad40-149">在“方向”字段中，选择“发货”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="8ad40-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-150">Click OK.</span></span>
    * <span data-ttu-id="8ad40-151">查看创建的输出，该输出的结尾包含汇总行。</span><span class="sxs-lookup"><span data-stu-id="8ad40-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="8ad40-152">请注意，已经在与首次运行的比较中更改了它。</span><span class="sxs-lookup"><span data-stu-id="8ad40-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="8ad40-153">以调试模式运行此配置以查看收集的盘点和合计数据</span><span class="sxs-lookup"><span data-stu-id="8ad40-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="8ad40-154">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8ad40-155">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="8ad40-156">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="8ad40-157">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="8ad40-158">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="8ad40-159">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-159">Click User parameters.</span></span>
7. <span data-ttu-id="8ad40-160">在“在调试模式下运行”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="8ad40-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-161">Click OK.</span></span>
9. <span data-ttu-id="8ad40-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8ad40-162">Close the page.</span></span>
10. <span data-ttu-id="8ad40-163">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="8ad40-164">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-164">Click Output.</span></span>
12. <span data-ttu-id="8ad40-165">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-165">Click Report.</span></span>
13. <span data-ttu-id="8ad40-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-166">Click OK.</span></span>
14. <span data-ttu-id="8ad40-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8ad40-167">Close the page.</span></span>
15. <span data-ttu-id="8ad40-168">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="8ad40-169">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="8ad40-170">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="8ad40-171">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="8ad40-172">单击“调试日志”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-172">Click Debug logs.</span></span>
    * <span data-ttu-id="8ad40-173">请注意，已经为所选配置的执行过程创建了调试日志记录。</span><span class="sxs-lookup"><span data-stu-id="8ad40-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="8ad40-174">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-174">Click Attach.</span></span>
21. <span data-ttu-id="8ad40-175">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="8ad40-175">Click Open.</span></span>
    * <span data-ttu-id="8ad40-176">查看创建的 XML 文件，其中包含执行所选配置期间收集的盘点和合计详细信息。</span><span class="sxs-lookup"><span data-stu-id="8ad40-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

