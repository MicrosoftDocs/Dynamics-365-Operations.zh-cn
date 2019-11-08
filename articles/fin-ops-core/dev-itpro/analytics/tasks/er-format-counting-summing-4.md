---
title: ER 配置格式以执行盘点和合计（第 4 部分 - 运行格式）
description: 以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a80e5b1a79c874ce0a8d24c85be71d0dc5c9c8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550548"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="3f916-103">ER 配置格式以执行盘点和合计（第 4 部分 - 运行格式）</span><span class="sxs-lookup"><span data-stu-id="3f916-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f916-104">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="3f916-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3f916-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="3f916-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="3f916-106">必须首先完成“ER 配置格式以执行盘点和合计（第 3 部分：使用计算创建输出）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="3f916-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="3f916-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="3f916-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="3f916-108">为生成内部统计报表测试此配置</span><span class="sxs-lookup"><span data-stu-id="3f916-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="3f916-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="3f916-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3f916-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="3f916-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3f916-111">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="3f916-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="3f916-112">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="3f916-113">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="3f916-114">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="3f916-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="3f916-115">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="3f916-115">Click User parameters.</span></span>
8. <span data-ttu-id="3f916-116">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3f916-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="3f916-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3f916-117">Click OK.</span></span>
10. <span data-ttu-id="3f916-118">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="3f916-118">Click Edit.</span></span>
11. <span data-ttu-id="3f916-119">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3f916-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="3f916-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3f916-120">Click Save.</span></span>
13. <span data-ttu-id="3f916-121">转到缴税>设置 >外贸>外贸参数。</span><span class="sxs-lookup"><span data-stu-id="3f916-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="3f916-122">展开“电子报表”部分。</span><span class="sxs-lookup"><span data-stu-id="3f916-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="3f916-123">选择“带盘点和合计的内部统计 (DE)”配置。</span><span class="sxs-lookup"><span data-stu-id="3f916-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="3f916-124">选择“带盘点和合计的内部统计 (DE)”配置。</span><span class="sxs-lookup"><span data-stu-id="3f916-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="3f916-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3f916-125">Click Save.</span></span>
18. <span data-ttu-id="3f916-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3f916-126">Close the page.</span></span>
19. <span data-ttu-id="3f916-127">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="3f916-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="3f916-128">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="3f916-128">Click Output.</span></span>
21. <span data-ttu-id="3f916-129">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="3f916-129">Click Report.</span></span>
    * <span data-ttu-id="3f916-130">运行内部统计报表生成过程。</span><span class="sxs-lookup"><span data-stu-id="3f916-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="3f916-131">在“开始日期”字段中，将日期设置为“2000-01-01”。</span><span class="sxs-lookup"><span data-stu-id="3f916-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="3f916-132">为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。</span><span class="sxs-lookup"><span data-stu-id="3f916-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="3f916-133">在“结束日期”字段中，将日期设置为“2022-12-31”。</span><span class="sxs-lookup"><span data-stu-id="3f916-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="3f916-134">为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。</span><span class="sxs-lookup"><span data-stu-id="3f916-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="3f916-135">在“方向”字段中，选择“到货”。</span><span class="sxs-lookup"><span data-stu-id="3f916-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="3f916-136">在“生成文档”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3f916-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="3f916-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3f916-137">Click OK.</span></span>
    * <span data-ttu-id="3f916-138">查看创建的输出，该输出的结尾包含汇总行。</span><span class="sxs-lookup"><span data-stu-id="3f916-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="3f916-139">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3f916-139">Click New.</span></span>
28. <span data-ttu-id="3f916-140">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3f916-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="3f916-141">在“方向”字段中，选择“发货”。</span><span class="sxs-lookup"><span data-stu-id="3f916-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="3f916-142">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3f916-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="3f916-143">在“商品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3f916-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="3f916-144">将“重量”设置为“10”。</span><span class="sxs-lookup"><span data-stu-id="3f916-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="3f916-145">将“发票金额”设置为“10000”。</span><span class="sxs-lookup"><span data-stu-id="3f916-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="3f916-146">将“统计金额”设置为“10000”。</span><span class="sxs-lookup"><span data-stu-id="3f916-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="3f916-147">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="3f916-147">Click Output.</span></span>
36. <span data-ttu-id="3f916-148">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="3f916-148">Click Report.</span></span>
37. <span data-ttu-id="3f916-149">在“方向”字段中，选择“发货”。</span><span class="sxs-lookup"><span data-stu-id="3f916-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="3f916-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3f916-150">Click OK.</span></span>
    * <span data-ttu-id="3f916-151">查看创建的输出，该输出的结尾包含汇总行。</span><span class="sxs-lookup"><span data-stu-id="3f916-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="3f916-152">请注意，已经在与首次运行的比较中更改了它。</span><span class="sxs-lookup"><span data-stu-id="3f916-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="3f916-153">以调试模式运行此配置以查看收集的盘点和合计数据</span><span class="sxs-lookup"><span data-stu-id="3f916-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="3f916-154">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="3f916-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3f916-155">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="3f916-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="3f916-156">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="3f916-157">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="3f916-158">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="3f916-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="3f916-159">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="3f916-159">Click User parameters.</span></span>
7. <span data-ttu-id="3f916-160">在“在调试模式下运行”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3f916-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="3f916-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3f916-161">Click OK.</span></span>
9. <span data-ttu-id="3f916-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3f916-162">Close the page.</span></span>
10. <span data-ttu-id="3f916-163">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="3f916-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="3f916-164">单击“输出”。</span><span class="sxs-lookup"><span data-stu-id="3f916-164">Click Output.</span></span>
12. <span data-ttu-id="3f916-165">单击“报表”。</span><span class="sxs-lookup"><span data-stu-id="3f916-165">Click Report.</span></span>
13. <span data-ttu-id="3f916-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3f916-166">Click OK.</span></span>
14. <span data-ttu-id="3f916-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3f916-167">Close the page.</span></span>
15. <span data-ttu-id="3f916-168">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="3f916-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="3f916-169">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="3f916-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="3f916-170">在树中，展开“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="3f916-171">在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="3f916-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="3f916-172">单击“调试日志”。</span><span class="sxs-lookup"><span data-stu-id="3f916-172">Click Debug logs.</span></span>
    * <span data-ttu-id="3f916-173">请注意，已经为所选配置的执行过程创建了调试日志记录。</span><span class="sxs-lookup"><span data-stu-id="3f916-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="3f916-174">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="3f916-174">Click Attach.</span></span>
21. <span data-ttu-id="3f916-175">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="3f916-175">Click Open.</span></span>
    * <span data-ttu-id="3f916-176">查看创建的 XML 文件，其中包含执行所选配置期间收集的盘点和合计详细信息。</span><span class="sxs-lookup"><span data-stu-id="3f916-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

