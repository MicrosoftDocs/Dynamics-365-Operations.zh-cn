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
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5684c710b8e167a4a39f106eb3c0fd77e3011dbd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841337"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="524a7-103">创建组织报告层次结构</span><span class="sxs-lookup"><span data-stu-id="524a7-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="524a7-104">此过程用于为组织报告创建报告层次结构。</span><span class="sxs-lookup"><span data-stu-id="524a7-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="524a7-105">此录制的目的是引导您熟悉维度层次结构，以便继续操作，直到创建整个组织报告结构。</span><span class="sxs-lookup"><span data-stu-id="524a7-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="524a7-106">此录制使用 USP2 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="524a7-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="524a7-107">转到“成本核算”>“维度”>“维度层次结构”。</span><span class="sxs-lookup"><span data-stu-id="524a7-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="524a7-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-108">Click New.</span></span>
3. <span data-ttu-id="524a7-109">在“层次结构类型组合框”字段中，选择“维度分类层次结构”。</span><span class="sxs-lookup"><span data-stu-id="524a7-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="524a7-110">选择“维度分类层次结构”。</span><span class="sxs-lookup"><span data-stu-id="524a7-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="524a7-111">维度分级层次结构类型用于定义规则和用于报告目的。</span><span class="sxs-lookup"><span data-stu-id="524a7-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="524a7-112">它支持所有维度，例如成本对象、成本元素和统计维度。</span><span class="sxs-lookup"><span data-stu-id="524a7-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="524a7-113">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-113">Click Create.</span></span>
5. <span data-ttu-id="524a7-114">在“维度层次结构名称”字段中，键入“组织 USP2”。</span><span class="sxs-lookup"><span data-stu-id="524a7-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="524a7-115">在“维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-116">选择“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="524a7-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-117">Click Save.</span></span>
8. <span data-ttu-id="524a7-118">单击“查看层次结构”。</span><span class="sxs-lookup"><span data-stu-id="524a7-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="524a7-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-119">Click New.</span></span>
10. <span data-ttu-id="524a7-120">在“节点名称”字段中，键入“CEO”。</span><span class="sxs-lookup"><span data-stu-id="524a7-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="524a7-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-121">Click Save.</span></span>
12. <span data-ttu-id="524a7-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-122">Click New.</span></span>
13. <span data-ttu-id="524a7-123">在“节点名称”字段中，键入“CEO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="524a7-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-124">Click Save.</span></span>
15. <span data-ttu-id="524a7-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-125">Click New.</span></span>
16. <span data-ttu-id="524a7-126">在“节点名称”字段中，键入“东部区域”。</span><span class="sxs-lookup"><span data-stu-id="524a7-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="524a7-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-127">Click Save.</span></span>
18. <span data-ttu-id="524a7-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-128">Click New.</span></span>
19. <span data-ttu-id="524a7-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="524a7-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="524a7-130">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-131">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="524a7-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="524a7-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-132">Click Save.</span></span>
22. <span data-ttu-id="524a7-133">在树中，选择“组织 USP2\CEO\CEO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="524a7-134">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-134">Click New.</span></span>
24. <span data-ttu-id="524a7-135">在“节点名称”字段中，键入“西部区域”。</span><span class="sxs-lookup"><span data-stu-id="524a7-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="524a7-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-136">Click Save.</span></span>
26. <span data-ttu-id="524a7-137">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-137">Click New.</span></span>
27. <span data-ttu-id="524a7-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="524a7-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="524a7-139">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-140">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="524a7-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="524a7-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-141">Click Save.</span></span>
30. <span data-ttu-id="524a7-142">在树中，选择“组织 USP2\CEO”。</span><span class="sxs-lookup"><span data-stu-id="524a7-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="524a7-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-143">Click New.</span></span>
32. <span data-ttu-id="524a7-144">在“节点名称”字段中，键入“CFO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="524a7-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-145">Click Save.</span></span>
34. <span data-ttu-id="524a7-146">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-146">Click New.</span></span>
35. <span data-ttu-id="524a7-147">在“节点名称”字段中，键入“营销市场活动”。</span><span class="sxs-lookup"><span data-stu-id="524a7-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="524a7-148">在“节点名称”字段中，键入“营销市场活动”。</span><span class="sxs-lookup"><span data-stu-id="524a7-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="524a7-149">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-149">Click Save.</span></span>
38. <span data-ttu-id="524a7-150">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-150">Click New.</span></span>
39. <span data-ttu-id="524a7-151">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="524a7-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="524a7-152">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-153">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="524a7-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="524a7-154">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-154">Click Save.</span></span>
42. <span data-ttu-id="524a7-155">在树中，选择“组织 USP2\CEO\CFO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="524a7-156">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-156">Click New.</span></span>
44. <span data-ttu-id="524a7-157">在“节点名称”字段中，键入“商业展览会”。</span><span class="sxs-lookup"><span data-stu-id="524a7-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="524a7-158">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-158">Click Save.</span></span>
46. <span data-ttu-id="524a7-159">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-159">Click New.</span></span>
47. <span data-ttu-id="524a7-160">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="524a7-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="524a7-161">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-162">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="524a7-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="524a7-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-163">Click Save.</span></span>
50. <span data-ttu-id="524a7-164">在树中，选择“组织 USP2\CEO”。</span><span class="sxs-lookup"><span data-stu-id="524a7-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="524a7-165">在“节点名称”字段中，键入“CIO 成本中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="524a7-166">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-166">Click Save.</span></span>
53. <span data-ttu-id="524a7-167">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-167">Click New.</span></span>
54. <span data-ttu-id="524a7-168">在“节点名称”字段中，键入“呼叫中心”。</span><span class="sxs-lookup"><span data-stu-id="524a7-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="524a7-169">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-169">Click Save.</span></span>
56. <span data-ttu-id="524a7-170">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="524a7-170">Click New.</span></span>
57. <span data-ttu-id="524a7-171">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="524a7-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="524a7-172">在“起始维度成员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="524a7-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="524a7-173">选中与节点对应的维度成员。</span><span class="sxs-lookup"><span data-stu-id="524a7-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="524a7-174">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="524a7-174">Click Save.</span></span>

