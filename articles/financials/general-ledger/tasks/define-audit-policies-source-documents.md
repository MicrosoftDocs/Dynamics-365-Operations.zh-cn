--- 
title: "定义原始凭证的审计策略"
description: "此过程显示如何设置和运行审计政策规则。"
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="57aa4-103">定义原始凭证的审计策略</span><span class="sxs-lookup"><span data-stu-id="57aa4-103">Define audit policies for source documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57aa4-104">此过程显示如何设置和运行审计政策规则。</span><span class="sxs-lookup"><span data-stu-id="57aa4-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="57aa4-105">本例使用含酒店费用类型的费用报表。</span><span class="sxs-lookup"><span data-stu-id="57aa4-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="57aa4-106">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="57aa4-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="57aa4-107">审计角色包含执行这些任务的正确权限。</span><span class="sxs-lookup"><span data-stu-id="57aa4-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="57aa4-108">转至“审计工作台”>“设置”>“政策规则类型”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="57aa4-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-109">Click New.</span></span>
3. <span data-ttu-id="57aa4-110">在“规则名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="57aa4-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="57aa4-112">在“查询名称”字段中，选择“费用报表”行</span><span class="sxs-lookup"><span data-stu-id="57aa4-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="57aa4-113">在“查询类型”字段中，选择“汇总”</span><span class="sxs-lookup"><span data-stu-id="57aa4-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="57aa4-114">在“法人实体”字段中，选择“法人实体”</span><span class="sxs-lookup"><span data-stu-id="57aa4-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="57aa4-115">在“文档日期引用”字段中，选择“已修改的日期和时间”</span><span class="sxs-lookup"><span data-stu-id="57aa4-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="57aa4-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-116">Click Save.</span></span>
10. <span data-ttu-id="57aa4-117">转至“审计工作台”>“设置”>“审计政策”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="57aa4-118">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-118">Click New.</span></span>
12. <span data-ttu-id="57aa4-119">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="57aa4-120">展开“政策组织”部分。</span><span class="sxs-lookup"><span data-stu-id="57aa4-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="57aa4-121">在树结构中，选择“美国 Contoso 娱乐系统”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="57aa4-122">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-122">Click Add.</span></span>
16. <span data-ttu-id="57aa4-123">在树结构中，选择“美国 Contoso 咨询”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="57aa4-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-124">Click Add.</span></span>
18. <span data-ttu-id="57aa4-125">在树结构中，选择“美国 Contoso 零售”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="57aa4-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-126">Click Add.</span></span>
20. <span data-ttu-id="57aa4-127">展开“政策组织”部分。</span><span class="sxs-lookup"><span data-stu-id="57aa4-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="57aa4-128">展开“政策规则”部分。</span><span class="sxs-lookup"><span data-stu-id="57aa4-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="57aa4-129">在列表中，查找并选择以前创建的政策规则。</span><span class="sxs-lookup"><span data-stu-id="57aa4-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="57aa4-130">单击“创建政策规则”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="57aa4-131">在“有效日期”字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="57aa4-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="57aa4-132">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-132">Click Filter.</span></span>
26. <span data-ttu-id="57aa4-133">在列表中，选择“费用类别”行，然后设置酒店详细信息</span><span class="sxs-lookup"><span data-stu-id="57aa4-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="57aa4-134">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="57aa4-135">单击“汇总”选项卡。</span><span class="sxs-lookup"><span data-stu-id="57aa4-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="57aa4-136">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-136">Click Add.</span></span>
30. <span data-ttu-id="57aa4-137">在列表中，选择“交易金额”上的字段值</span><span class="sxs-lookup"><span data-stu-id="57aa4-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="57aa4-138">在名为“字段”的字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="57aa4-139">在“汇总功能”字段中，选择“合计”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="57aa4-140">单击选项卡上的“组别”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="57aa4-141">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-141">Click Add.</span></span>
35. <span data-ttu-id="57aa4-142">在列表中，选择员工值</span><span class="sxs-lookup"><span data-stu-id="57aa4-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="57aa4-143">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-143">Click Add.</span></span>
37. <span data-ttu-id="57aa4-144">在列表中，选择“费用类别”的值</span><span class="sxs-lookup"><span data-stu-id="57aa4-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="57aa4-145">在名为“字段”的字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="57aa4-146">单击“持有”选项卡。</span><span class="sxs-lookup"><span data-stu-id="57aa4-146">Click the Having tab.</span></span>
40. <span data-ttu-id="57aa4-147">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-147">Click Add.</span></span>
41. <span data-ttu-id="57aa4-148">选择“交易金额”</span><span class="sxs-lookup"><span data-stu-id="57aa4-148">Select Transaction amount</span></span>
42. <span data-ttu-id="57aa4-149">在名为“字段”的字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57aa4-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="57aa4-150">在“汇总功能”字段中，选择“合计”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="57aa4-151">在“条件”字段中，键入“>2000”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="57aa4-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-152">Click OK.</span></span>
46. <span data-ttu-id="57aa4-153">单击“测试”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-153">Click Test.</span></span>
47. <span data-ttu-id="57aa4-154">在“文档选择开始日期”字段，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="57aa4-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="57aa4-155">在“文档选择结束日期”字段，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="57aa4-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="57aa4-156">单击“运行测试”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-156">Click Run test.</span></span>
50. <span data-ttu-id="57aa4-157">在操作窗格上，单击“审计政策”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="57aa4-158">单击“附加选项”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-158">Click Additional options.</span></span>
52. <span data-ttu-id="57aa4-159">在“开始日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="57aa4-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="57aa4-160">在“结束日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="57aa4-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="57aa4-161">单击“批处理”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-161">Click Batch.</span></span>
55. <span data-ttu-id="57aa4-162">展开“后台运行”部分。</span><span class="sxs-lookup"><span data-stu-id="57aa4-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="57aa4-163">在“批处理”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="57aa4-164">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-164">Click OK.</span></span>
58. <span data-ttu-id="57aa4-165">转至“审计工作台”>“审计案例”。</span><span class="sxs-lookup"><span data-stu-id="57aa4-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="57aa4-166">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="57aa4-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="57aa4-167">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="57aa4-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="57aa4-168">展开“关联”部分。</span><span class="sxs-lookup"><span data-stu-id="57aa4-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="57aa4-169">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="57aa4-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="57aa4-170">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="57aa4-170">In the list, click the link in the selected row.</span></span>


