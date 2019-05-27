---
title: 创建组织报告层次结构
description: 此过程用于为组织报告创建报告层次结构。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543925"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="ea5d6-103">创建组织报告层次结构</span><span class="sxs-lookup"><span data-stu-id="ea5d6-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea5d6-104">此过程用于为组织报告创建报告层次结构。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="ea5d6-105">此录制的目的是引导您熟悉维度层次结构，以便继续操作，直到创建整个组织报告结构。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="ea5d6-106">此录制使用 USP2 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="ea5d6-107">转到“成本核算”>“维度”>“维度层次结构”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="ea5d6-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-108">Click New.</span></span>
3. <span data-ttu-id="ea5d6-109">在“层次结构类型组合框”字段中，选择“维度分类层次结构”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="ea5d6-110">选择“维度分类层次结构”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="ea5d6-111">维度分级层次结构类型用于定义规则和用于报告目的。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="ea5d6-112">它支持所有维度，例如成本对象、成本元素和统计维度。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="ea5d6-113">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-113">Click Create.</span></span>
5. <span data-ttu-id="ea5d6-114">在“维度层次结构名称”字段中，键入“组织 USP2”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="ea5d6-115">在“维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-116">选择“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="ea5d6-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-117">Click Save.</span></span>
8. <span data-ttu-id="ea5d6-118">单击“查看层次结构”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="ea5d6-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-119">Click New.</span></span>
10. <span data-ttu-id="ea5d6-120">在“节点名称”字段中，键入“CEO”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="ea5d6-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-121">Click Save.</span></span>
12. <span data-ttu-id="ea5d6-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-122">Click New.</span></span>
13. <span data-ttu-id="ea5d6-123">在“节点名称”字段中，键入“CEO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="ea5d6-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-124">Click Save.</span></span>
15. <span data-ttu-id="ea5d6-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-125">Click New.</span></span>
16. <span data-ttu-id="ea5d6-126">在“节点名称”字段中，键入“东部区域”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="ea5d6-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-127">Click Save.</span></span>
18. <span data-ttu-id="ea5d6-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-128">Click New.</span></span>
19. <span data-ttu-id="ea5d6-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="ea5d6-130">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-131">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="ea5d6-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-132">Click Save.</span></span>
22. <span data-ttu-id="ea5d6-133">在树中，选择“组织 USP2\CEO\CEO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="ea5d6-134">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-134">Click New.</span></span>
24. <span data-ttu-id="ea5d6-135">在“节点名称”字段中，键入“西部区域”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="ea5d6-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-136">Click Save.</span></span>
26. <span data-ttu-id="ea5d6-137">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-137">Click New.</span></span>
27. <span data-ttu-id="ea5d6-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="ea5d6-139">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-140">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="ea5d6-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-141">Click Save.</span></span>
30. <span data-ttu-id="ea5d6-142">在树中，选择“组织 USP2\CEO”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="ea5d6-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-143">Click New.</span></span>
32. <span data-ttu-id="ea5d6-144">在“节点名称”字段中，键入“CFO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="ea5d6-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-145">Click Save.</span></span>
34. <span data-ttu-id="ea5d6-146">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-146">Click New.</span></span>
35. <span data-ttu-id="ea5d6-147">在“节点名称”字段中，键入“营销市场活动”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="ea5d6-148">在“节点名称”字段中，键入“营销市场活动”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="ea5d6-149">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-149">Click Save.</span></span>
38. <span data-ttu-id="ea5d6-150">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-150">Click New.</span></span>
39. <span data-ttu-id="ea5d6-151">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="ea5d6-152">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-153">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="ea5d6-154">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-154">Click Save.</span></span>
42. <span data-ttu-id="ea5d6-155">在树中，选择“组织 USP2\CEO\CFO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="ea5d6-156">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-156">Click New.</span></span>
44. <span data-ttu-id="ea5d6-157">在“节点名称”字段中，键入“商业展览会”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="ea5d6-158">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-158">Click Save.</span></span>
46. <span data-ttu-id="ea5d6-159">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-159">Click New.</span></span>
47. <span data-ttu-id="ea5d6-160">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="ea5d6-161">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-162">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="ea5d6-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-163">Click Save.</span></span>
50. <span data-ttu-id="ea5d6-164">在树中，选择“组织 USP2\CEO”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="ea5d6-165">在“节点名称”字段中，键入“CIO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="ea5d6-166">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-166">Click Save.</span></span>
53. <span data-ttu-id="ea5d6-167">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-167">Click New.</span></span>
54. <span data-ttu-id="ea5d6-168">在“节点名称”字段中，键入“呼叫中心”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="ea5d6-169">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-169">Click Save.</span></span>
56. <span data-ttu-id="ea5d6-170">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-170">Click New.</span></span>
57. <span data-ttu-id="ea5d6-171">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="ea5d6-172">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ea5d6-173">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="ea5d6-174">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea5d6-174">Click Save.</span></span>

