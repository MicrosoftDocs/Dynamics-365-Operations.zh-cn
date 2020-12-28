---
title: 定义原始凭证的审计策略
description: 此主题介绍如何设置和运行审计政策规则。
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440835"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="34320-103">定义原始凭证的审计策略</span><span class="sxs-lookup"><span data-stu-id="34320-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34320-104">此主题介绍如何设置和运行审计政策规则。</span><span class="sxs-lookup"><span data-stu-id="34320-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="34320-105">本例使用含酒店费用类型的费用报表。</span><span class="sxs-lookup"><span data-stu-id="34320-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="34320-106">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="34320-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="34320-107">审计角色包含执行这些任务的正确权限。</span><span class="sxs-lookup"><span data-stu-id="34320-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="34320-108">在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 策略规则类型**。</span><span class="sxs-lookup"><span data-stu-id="34320-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="34320-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="34320-109">Select **New**.</span></span>
3. <span data-ttu-id="34320-110">在 **规则名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="34320-111">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="34320-112">在 **查询名称** 字段中，选择 **支出报表行**</span><span class="sxs-lookup"><span data-stu-id="34320-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="34320-113">在 **查询类型** 字段中，选择 **汇总**</span><span class="sxs-lookup"><span data-stu-id="34320-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="34320-114">在 **法人** 字段中，选择 **法人**</span><span class="sxs-lookup"><span data-stu-id="34320-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="34320-115">在 **文档日期引用** 字段中，选择 **已修改的日期和时间**</span><span class="sxs-lookup"><span data-stu-id="34320-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="34320-116">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="34320-116">Select **Save**.</span></span>
10. <span data-ttu-id="34320-117">在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 审计策略**。</span><span class="sxs-lookup"><span data-stu-id="34320-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="34320-118">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="34320-118">Select **New**.</span></span>
12. <span data-ttu-id="34320-119">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="34320-120">展开 **策略组织** 部分。</span><span class="sxs-lookup"><span data-stu-id="34320-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="34320-121">在树结构中，选择 **美国 Contoso 娱乐系统**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="34320-122">在树结构中，选择 **美国 Contoso 咨询**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="34320-123">在树结构中，选择 **美国 Contoso 零售**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="34320-124">展开 **策略组织** 部分。</span><span class="sxs-lookup"><span data-stu-id="34320-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="34320-125">展开 **策略规则** 部分。</span><span class="sxs-lookup"><span data-stu-id="34320-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="34320-126">在列表中，查找并选择以前创建的政策规则。</span><span class="sxs-lookup"><span data-stu-id="34320-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="34320-127">选择 **创建策略规则**。</span><span class="sxs-lookup"><span data-stu-id="34320-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="34320-128">在 **生效日期** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="34320-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="34320-129">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="34320-129">Select **Filter**.</span></span>
23. <span data-ttu-id="34320-130">在列表中，选择 **支出类别** 行，然后将详细信息设置为 **酒店**。</span><span class="sxs-lookup"><span data-stu-id="34320-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="34320-131">在 **标准** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="34320-132">选择 **汇总** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="34320-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="34320-133">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-133">Select **Add**.</span></span>
27. <span data-ttu-id="34320-134">在列表中，选择 **交易金额** 的字段值。</span><span class="sxs-lookup"><span data-stu-id="34320-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="34320-135">在 **字段** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="34320-136">在 **汇总功能** 字段中，选择 **合计**。</span><span class="sxs-lookup"><span data-stu-id="34320-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="34320-137">选择 **分组依据** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="34320-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="34320-138">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-138">Select **Add**.</span></span>
32. <span data-ttu-id="34320-139">在列表中，选择 **员工** 值。</span><span class="sxs-lookup"><span data-stu-id="34320-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="34320-140">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-140">Select **Add**.</span></span>
34. <span data-ttu-id="34320-141">在列表中，选择 **支出类别** 的值。</span><span class="sxs-lookup"><span data-stu-id="34320-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="34320-142">在 **字段** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="34320-143">选择 **具有** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="34320-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="34320-144">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="34320-144">Select **Add**.</span></span>
38. <span data-ttu-id="34320-145">选择 **交易金额**。</span><span class="sxs-lookup"><span data-stu-id="34320-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="34320-146">在 **字段** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="34320-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="34320-147">在 **汇总功能** 字段中，选择 **合计**。</span><span class="sxs-lookup"><span data-stu-id="34320-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="34320-148">在 **标准** 字段中，输入 `>2000`。</span><span class="sxs-lookup"><span data-stu-id="34320-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="34320-149">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="34320-149">Select **OK**.</span></span>
43. <span data-ttu-id="34320-150">选择 **测试**。</span><span class="sxs-lookup"><span data-stu-id="34320-150">Select **Test**.</span></span>
44. <span data-ttu-id="34320-151">在 **文档选择开始日期** 字段，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="34320-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="34320-152">在 **文档选择结束日期** 字段，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="34320-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="34320-153">选择 **运行测试**。</span><span class="sxs-lookup"><span data-stu-id="34320-153">Select **Run test**.</span></span>
47. <span data-ttu-id="34320-154">在操作窗格上，选择 **审计策略**。</span><span class="sxs-lookup"><span data-stu-id="34320-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="34320-155">选择 **其他选项**。</span><span class="sxs-lookup"><span data-stu-id="34320-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="34320-156">在 **开始日期** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="34320-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="34320-157">在 **结束日期** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="34320-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="34320-158">选择 **批处理**。</span><span class="sxs-lookup"><span data-stu-id="34320-158">Select **Batch**.</span></span>
52. <span data-ttu-id="34320-159">展开 **后台运行** 部分。</span><span class="sxs-lookup"><span data-stu-id="34320-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="34320-160">在 **批处理** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="34320-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="34320-161">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="34320-161">Select **OK**.</span></span>
55. <span data-ttu-id="34320-162">在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 审计案例**。</span><span class="sxs-lookup"><span data-stu-id="34320-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="34320-163">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34320-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="34320-164">展开 **关联** 部分。</span><span class="sxs-lookup"><span data-stu-id="34320-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="34320-165">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="34320-165">In the list, find and select the desired record.</span></span>

