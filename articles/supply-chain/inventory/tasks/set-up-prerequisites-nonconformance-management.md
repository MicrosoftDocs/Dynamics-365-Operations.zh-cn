---
title: 设置不符合项管理的先决条件
description: 使用此主题可以启用未达标管理流程。
author: perlynne
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8ce4ae69585a93d679ae614ae81efc9723d9397
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818173"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="48e74-103">设置不符合项管理的先决条件</span><span class="sxs-lookup"><span data-stu-id="48e74-103">Set up prerequisites for nonconformance management</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48e74-104">使用此主题可以启用未达标管理流程。</span><span class="sxs-lookup"><span data-stu-id="48e74-104">Use this topic to enable nonconformance management processes.</span></span> <span data-ttu-id="48e74-105">未达标描述存在质量问题的过程或物料，有关的描述性信息将包括问题的来源和类型。</span><span class="sxs-lookup"><span data-stu-id="48e74-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="48e74-106">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="48e74-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="48e74-107">此过程通常由质量经理执行。</span><span class="sxs-lookup"><span data-stu-id="48e74-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="48e74-108">在公司内启用质量管理流程</span><span class="sxs-lookup"><span data-stu-id="48e74-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="48e74-109">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="48e74-109">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="48e74-110">选择 **质量管理** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="48e74-110">Select the **Quality management** tab.</span></span>
3. <span data-ttu-id="48e74-111">在 **使用质量管理** 字段中选择 **是** 以便为公司启用质量管理流程。</span><span class="sxs-lookup"><span data-stu-id="48e74-111">Select **Yes** in the **Use quality management** field to enable quality management processes for the company.</span></span>
4. <span data-ttu-id="48e74-112">在 **小时工资率** 字段中用本币输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="48e74-112">In the **Hourly rate** field, enter a number in the local currency.</span></span> <span data-ttu-id="48e74-113">小时工资率用于计算与未达标相关的工序的成本。</span><span class="sxs-lookup"><span data-stu-id="48e74-113">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="48e74-114">小时工资率和计算的成本为未达标提供了参考信息，并且它们不与其他功能交互。</span><span class="sxs-lookup"><span data-stu-id="48e74-114">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="48e74-115">萱蕚 **报表设置** 以定义将在不同类型的质量管理报表上使用的质量报表注释类型。</span><span class="sxs-lookup"><span data-stu-id="48e74-115">Select **Report setup** to define the quality report note types that will be used on different kinds of quality management reports.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="48e74-116">支持用户进行未达标处理</span><span class="sxs-lookup"><span data-stu-id="48e74-116">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-117">在导航窗格中，转到 **模块 > 系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="48e74-117">In the navigation pane, go to **Modules > System administration > Users > Users**.</span></span> 
2. <span data-ttu-id="48e74-118">使用快速筛选器查找将审核或拒绝未达标记录的用户。</span><span class="sxs-lookup"><span data-stu-id="48e74-118">Use the Quick Filter to find the user who will be approving or rejecting the nonconformance records.</span></span> <span data-ttu-id="48e74-119">例如，使用值 `Ricardo` 在 **名称** 字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="48e74-119">For example, filter on the **Name** field with a value of `Ricardo`.</span></span> <span data-ttu-id="48e74-120">若要处理未达标的审核，审核或拒绝未达标的用户必须有在 **用户** 页分配的“名称”值。</span><span class="sxs-lookup"><span data-stu-id="48e74-120">To process the approval of a nonconformance, the user who approves or rejects nonconformances must have a "Name" value assigned on the **Users** page.</span></span> <span data-ttu-id="48e74-121">若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。</span><span class="sxs-lookup"><span data-stu-id="48e74-121">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
3. <span data-ttu-id="48e74-122">标记所需记录的行。</span><span class="sxs-lookup"><span data-stu-id="48e74-122">Mark the row of the desired record.</span></span>
4. <span data-ttu-id="48e74-123">选择 **用户选项**。</span><span class="sxs-lookup"><span data-stu-id="48e74-123">Select **User options**.</span></span>
5. <span data-ttu-id="48e74-124">选择 **首选项** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="48e74-124">Select the **Preferences** tab.</span></span>
6. <span data-ttu-id="48e74-125">在 **启用文档处理** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="48e74-125">Select **Yes** in the **Enable document handling** field.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="48e74-126">定义未达标处理的诊断类型</span><span class="sxs-lookup"><span data-stu-id="48e74-126">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-127">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 诊断类型**。</span><span class="sxs-lookup"><span data-stu-id="48e74-127">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Diagnostic types**.</span></span> <span data-ttu-id="48e74-128">使用 **诊断类型** 页定义诊断操作的分类。</span><span class="sxs-lookup"><span data-stu-id="48e74-128">Use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="48e74-129">更正标识应对已审核的未达标采取的诊断操作类型、应该执行更改的用户，以及请求和计划的完成日期。</span><span class="sxs-lookup"><span data-stu-id="48e74-129">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="48e74-130">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-130">Select **New**.</span></span>
3. <span data-ttu-id="48e74-131">在 **诊断** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-131">In the **Diagnostic** field, type a value.</span></span>
4. <span data-ttu-id="48e74-132">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-132">In the **Description** field, type a value.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="48e74-133">定义未达标处理的质量费用</span><span class="sxs-lookup"><span data-stu-id="48e74-133">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-134">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 质量费用**。</span><span class="sxs-lookup"><span data-stu-id="48e74-134">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Quality charges**.</span></span> <span data-ttu-id="48e74-135">使用 **质量费用** 页定义将在未达标相关工序中使用的费用的分类。</span><span class="sxs-lookup"><span data-stu-id="48e74-135">Use the **Quality charges** page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="48e74-136">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-136">Select **New**.</span></span>
3. <span data-ttu-id="48e74-137">在 **费用代码** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-137">In the **Charges code** field, type a value.</span></span>
4. <span data-ttu-id="48e74-138">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-138">In the **Description** field, type a value.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="48e74-139">定义未达标处理的工序</span><span class="sxs-lookup"><span data-stu-id="48e74-139">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-140">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 工序**。</span><span class="sxs-lookup"><span data-stu-id="48e74-140">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Operations**.</span></span> <span data-ttu-id="48e74-141">使用 **工序** 页定义可以对已审核的未达标执行的工作的分类。</span><span class="sxs-lookup"><span data-stu-id="48e74-141">Use the **Operations** page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="48e74-142">在将工序与未达标关联时，您可以定义有关执行该工序所需的关联物料、工时和杂项费用的信息。</span><span class="sxs-lookup"><span data-stu-id="48e74-142">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="48e74-143">这些信息为计算执行该工序所需的预估成本奠定了基础。</span><span class="sxs-lookup"><span data-stu-id="48e74-143">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="48e74-144">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-144">Select **New**.</span></span>
3. <span data-ttu-id="48e74-145">在 **工序** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-145">In the **Operation** field, type a value.</span></span>
4. <span data-ttu-id="48e74-146">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-146">In the **Description** field, type a value.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="48e74-147">定义未达标处理的问题类型</span><span class="sxs-lookup"><span data-stu-id="48e74-147">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-148">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 问题类型**。</span><span class="sxs-lookup"><span data-stu-id="48e74-148">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Problem types**.</span></span> <span data-ttu-id="48e74-149">使用 **问题类型** 页定义各类未达标类型遇到的质量问题分类。</span><span class="sxs-lookup"><span data-stu-id="48e74-149">Use the **Problem types** page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="48e74-150">未达标类型包括 **内部**、**客户**、**供应商**、**服务请求**、**生产** 和 **联产品生产**。</span><span class="sxs-lookup"><span data-stu-id="48e74-150">The nonconformance types include **Internal**, **Customer**, **Vendor**, **Service request**, **Production**, and **Co-product production**.</span></span> <span data-ttu-id="48e74-151">一个问题类型可与多个未达标类型关联。</span><span class="sxs-lookup"><span data-stu-id="48e74-151">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="48e74-152">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-152">Select **New**.</span></span>
3. <span data-ttu-id="48e74-153">在 **问题类型** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-153">In the **Problem type** field, type a value.</span></span>
4. <span data-ttu-id="48e74-154">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-154">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="48e74-155">选择 **不符合项类型**。</span><span class="sxs-lookup"><span data-stu-id="48e74-155">Select **Non conformance types**.</span></span> <span data-ttu-id="48e74-156">使用 **不符合项类型** 页来授权一个或多个不符合项类型的问题类型的使用。</span><span class="sxs-lookup"><span data-stu-id="48e74-156">Use the **Non conformance types** page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="48e74-157">例如，有关缺陷代码的问题类型可适用于所有未达标类型，而有关客户投诉的问题类型只能适用于客户和服务请求未达标类型。</span><span class="sxs-lookup"><span data-stu-id="48e74-157">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="48e74-158">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-158">Select **New**.</span></span>
7. <span data-ttu-id="48e74-159">在新行的 **不符合项类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="48e74-159">In the **Non conformance type** field of the new row, select an option.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="48e74-160">定义未达标处理的检验区域</span><span class="sxs-lookup"><span data-stu-id="48e74-160">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="48e74-161">在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 检验区域**。</span><span class="sxs-lookup"><span data-stu-id="48e74-161">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Quarantine zones**.</span></span>
2. <span data-ttu-id="48e74-162">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48e74-162">Select **New**.</span></span>
3. <span data-ttu-id="48e74-163">在 **检验区域** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-163">In the **Quarantine zone** field, type a value.</span></span>
4. <span data-ttu-id="48e74-164">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="48e74-164">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="48e74-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="48e74-165">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]