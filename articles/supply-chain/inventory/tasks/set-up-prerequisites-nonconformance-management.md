--- 
title: "设置不符合项管理的先决条件"
description: "使用此过程可以启用未达标管理流程。"
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="786f6-103">设置不符合项管理的先决条件</span><span class="sxs-lookup"><span data-stu-id="786f6-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="786f6-104">使用此过程可以启用未达标管理流程。</span><span class="sxs-lookup"><span data-stu-id="786f6-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="786f6-105">未达标描述存在质量问题的过程或物料，有关的描述性信息将包括问题的来源和类型。</span><span class="sxs-lookup"><span data-stu-id="786f6-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="786f6-106">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="786f6-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="786f6-107">此过程通常由质量经理执行。</span><span class="sxs-lookup"><span data-stu-id="786f6-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="786f6-108">在公司内启用质量管理流程</span><span class="sxs-lookup"><span data-stu-id="786f6-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="786f6-109">转到“库存管理”>“设置”>“库存和仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="786f6-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="786f6-110">单击“质量管理”选项卡。</span><span class="sxs-lookup"><span data-stu-id="786f6-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="786f6-111">在“使用质量管理”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="786f6-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="786f6-112">选择此参数以启用公司的质量管理流程。</span><span class="sxs-lookup"><span data-stu-id="786f6-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="786f6-113">在“小时工资率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="786f6-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="786f6-114">使用“小时工资率”字段用本币输入人工小时工资率。</span><span class="sxs-lookup"><span data-stu-id="786f6-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="786f6-115">小时工资率用于计算与未达标相关的工序的成本。</span><span class="sxs-lookup"><span data-stu-id="786f6-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="786f6-116">小时工资率和计算的成本为未达标提供了参考信息，并且它们不与其他功能交互。</span><span class="sxs-lookup"><span data-stu-id="786f6-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="786f6-117">单击“报表设置”。</span><span class="sxs-lookup"><span data-stu-id="786f6-117">Click Report setup.</span></span>
    * <span data-ttu-id="786f6-118">此页面允许您定义将在不同类型的质量管理报表上使用的质量报表注释类型。</span><span class="sxs-lookup"><span data-stu-id="786f6-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="786f6-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-119">Close the page.</span></span>
7. <span data-ttu-id="786f6-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="786f6-121">支持用户进行未达标处理</span><span class="sxs-lookup"><span data-stu-id="786f6-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-122">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="786f6-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="786f6-123">若要处理未达标的审核，审核或拒绝未达标的用户必须有在用户页分配的“名称”值。</span><span class="sxs-lookup"><span data-stu-id="786f6-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="786f6-124">若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。</span><span class="sxs-lookup"><span data-stu-id="786f6-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="786f6-125">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="786f6-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="786f6-126">例如，在“姓名”字段中筛选值 'Ricardo'。</span><span class="sxs-lookup"><span data-stu-id="786f6-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="786f6-127">使用筛选器查找将审核或拒绝未达标记录的用户。</span><span class="sxs-lookup"><span data-stu-id="786f6-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="786f6-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="786f6-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="786f6-129">若要处理未达标的审核，确保审核或拒绝未达标的用户具有在用户页分配的“名称”值。</span><span class="sxs-lookup"><span data-stu-id="786f6-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="786f6-130">单击“用户选项”。</span><span class="sxs-lookup"><span data-stu-id="786f6-130">Click User options.</span></span>
5. <span data-ttu-id="786f6-131">单击“首选项”选项卡。</span><span class="sxs-lookup"><span data-stu-id="786f6-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="786f6-132">在“启用文档处理”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="786f6-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="786f6-133">若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。</span><span class="sxs-lookup"><span data-stu-id="786f6-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="786f6-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-134">Close the page.</span></span>
8. <span data-ttu-id="786f6-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-135">Close the page.</span></span>
9. <span data-ttu-id="786f6-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="786f6-137">定义未达标处理的诊断类型</span><span class="sxs-lookup"><span data-stu-id="786f6-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-138">转到“库存管理”>“设置”>“质量管理”>“诊断类型”。</span><span class="sxs-lookup"><span data-stu-id="786f6-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="786f6-139">使用诊断类型页定义诊断操作的分类。</span><span class="sxs-lookup"><span data-stu-id="786f6-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="786f6-140">更正标识应对已审核的未达标采取的诊断操作类型、应该执行更改的用户，以及请求和计划的完成日期。</span><span class="sxs-lookup"><span data-stu-id="786f6-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="786f6-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-141">Click New.</span></span>
3. <span data-ttu-id="786f6-142">在“诊断”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="786f6-143">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="786f6-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="786f6-145">定义未达标处理的质量费用</span><span class="sxs-lookup"><span data-stu-id="786f6-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-146">转到“库存管理“>”设置“>”质量管理“>”质量费用”。</span><span class="sxs-lookup"><span data-stu-id="786f6-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="786f6-147">使用质量费用页定义将在未达标相关工序中使用的费用的分类。</span><span class="sxs-lookup"><span data-stu-id="786f6-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="786f6-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-148">Click New.</span></span>
3. <span data-ttu-id="786f6-149">在“费用代码”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="786f6-150">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="786f6-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="786f6-152">定义未达标处理的工序</span><span class="sxs-lookup"><span data-stu-id="786f6-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-153">转到“库存管理”>“设置”>“质量管理”>“工序”。</span><span class="sxs-lookup"><span data-stu-id="786f6-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="786f6-154">使用工序页定义可以对已审核的未达标执行的工作的分类。</span><span class="sxs-lookup"><span data-stu-id="786f6-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="786f6-155">在将工序与未达标关联时，您可以定义有关执行该工序所需的关联物料、工时和杂项费用的信息。</span><span class="sxs-lookup"><span data-stu-id="786f6-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="786f6-156">这些信息为计算执行该工序所需的预估成本奠定了基础。</span><span class="sxs-lookup"><span data-stu-id="786f6-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="786f6-157">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-157">Click New.</span></span>
3. <span data-ttu-id="786f6-158">在“工序”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="786f6-159">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="786f6-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="786f6-161">定义未达标处理的问题类型</span><span class="sxs-lookup"><span data-stu-id="786f6-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-162">转到“库存管理”>“设置”>“质量管理”>“问题类型”。</span><span class="sxs-lookup"><span data-stu-id="786f6-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="786f6-163">使用问题类型页定义各类未达标类型遇到的质量问题分类。</span><span class="sxs-lookup"><span data-stu-id="786f6-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="786f6-164">未达标类型包括内部、客户、供应商、服务请求、生产和联产品生产。</span><span class="sxs-lookup"><span data-stu-id="786f6-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="786f6-165">一个问题类型可与多个未达标类型关联。</span><span class="sxs-lookup"><span data-stu-id="786f6-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="786f6-166">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-166">Click New.</span></span>
3. <span data-ttu-id="786f6-167">在“问题类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="786f6-168">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="786f6-169">单击“未达标类型”。</span><span class="sxs-lookup"><span data-stu-id="786f6-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="786f6-170">使用未达标类型页来授权一个或多个未达标类型的问题类型的使用。</span><span class="sxs-lookup"><span data-stu-id="786f6-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="786f6-171">例如，有关缺陷代码的问题类型可适用于所有未达标类型，而有关客户投诉的问题类型只能适用于客户和服务请求未达标类型。</span><span class="sxs-lookup"><span data-stu-id="786f6-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="786f6-172">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-172">Click New.</span></span>
7. <span data-ttu-id="786f6-173">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="786f6-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="786f6-174">在“未达标类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="786f6-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="786f6-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-175">Close the page.</span></span>
10. <span data-ttu-id="786f6-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="786f6-177">定义未达标处理的检验区域</span><span class="sxs-lookup"><span data-stu-id="786f6-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="786f6-178">转到“库存管理“>”设置“>”质量管理“>”检验区域”。</span><span class="sxs-lookup"><span data-stu-id="786f6-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="786f6-179">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="786f6-179">Click New.</span></span>
3. <span data-ttu-id="786f6-180">在“检验区域”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="786f6-181">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="786f6-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="786f6-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="786f6-182">Close the page.</span></span>


