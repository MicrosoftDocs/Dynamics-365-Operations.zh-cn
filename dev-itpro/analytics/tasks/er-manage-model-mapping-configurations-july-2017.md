--- 
title: "针对电子申报 (ER) 管理模型映射配置"
description: "以下步骤说明了指派为“系统管理员”或者“电子电子报表开发人员”角色的用户如何管理单独 ER 配置中的电子申报 (ER) 模型映射。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 473cad588253b0eb42eb927834e186ccfa4c4f1e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a><span data-ttu-id="773b4-103">针对电子申报 (ER) 管理模型映射配置</span><span class="sxs-lookup"><span data-stu-id="773b4-103">Manage model mapping configurations for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="773b4-104">以下步骤说明了指派为“系统管理员”或者“电子电子报表开发人员”角色的用户如何管理单独 ER 配置中的电子申报 (ER) 模型映射。</span><span class="sxs-lookup"><span data-stu-id="773b4-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="773b4-105">在此任务指南中，将为示例公司 Litware 公司创建所需 ER 配置。若要完成此任务指南，您必须首先完成任务指南“ER 创建一个配置提供程序，并标记其为当前运行的”中的步骤。</span><span class="sxs-lookup"><span data-stu-id="773b4-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="773b4-106">由于 ER 配置在公司之间共享，所以您可以使用所选公司数据集完成此任务指南。</span><span class="sxs-lookup"><span data-stu-id="773b4-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="773b4-107">如果您已安装了以下修补程序之一，则可使用此任务指南的功能：针对 Dynamics AX 7.0 版本的 https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 或针对 Dynamics 365 for Operations 版本的 https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871。</span><span class="sxs-lookup"><span data-stu-id="773b4-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="773b4-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="773b4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="773b4-109">验证示例公司 Litware 公司的配置提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="773b4-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="773b4-110">如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一任务指南中的步骤。</span><span class="sxs-lookup"><span data-stu-id="773b4-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="773b4-111">添加新 ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="773b4-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="773b4-112">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="773b4-113">添加新模型配置。</span><span class="sxs-lookup"><span data-stu-id="773b4-113">Add a new model configuration.</span></span> <span data-ttu-id="773b4-114">名称在配置树中必须唯一。</span><span class="sxs-lookup"><span data-stu-id="773b4-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="773b4-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="773b4-116">在“名称”字段中，键入“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="773b4-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="773b4-117">示例数据模型</span><span class="sxs-lookup"><span data-stu-id="773b4-117">Sample data model</span></span>  
4. <span data-ttu-id="773b4-118">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-118">Click Create configuration.</span></span>
5. <span data-ttu-id="773b4-119">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-119">Click Designer.</span></span>
6. <span data-ttu-id="773b4-120">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="773b4-121">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="773b4-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="773b4-122">根</span><span class="sxs-lookup"><span data-stu-id="773b4-122">Root</span></span>  
8. <span data-ttu-id="773b4-123">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="773b4-123">Click Add.</span></span>
9. <span data-ttu-id="773b4-124">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="773b4-125">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="773b4-126">公司</span><span class="sxs-lookup"><span data-stu-id="773b4-126">Company</span></span>  
11. <span data-ttu-id="773b4-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="773b4-127">Click Add.</span></span>
12. <span data-ttu-id="773b4-128">在“描述”字段中，输入文本“用户在运行时登录的法人或公司的描述”。</span><span class="sxs-lookup"><span data-stu-id="773b4-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="773b4-129">用户在运行时登录的法人或公司的描述。</span><span class="sxs-lookup"><span data-stu-id="773b4-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="773b4-130">单击“根引用”。</span><span class="sxs-lookup"><span data-stu-id="773b4-130">Click Root reference.</span></span>
14. <span data-ttu-id="773b4-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-131">Click OK.</span></span>
15. <span data-ttu-id="773b4-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="773b4-132">Click Save.</span></span>
16. <span data-ttu-id="773b4-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-133">Close the page.</span></span>
17. <span data-ttu-id="773b4-134">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="773b4-134">Click Change status.</span></span>
18. <span data-ttu-id="773b4-135">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="773b4-135">Click Complete.</span></span>
19. <span data-ttu-id="773b4-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="773b4-137">添加新 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="773b4-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="773b4-138">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="773b4-139">在“新建”字段中，输入“模型映射基于数据模型‘示例数据模型’”。</span><span class="sxs-lookup"><span data-stu-id="773b4-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="773b4-140">在“名称”字段中，键入“示例映射”。</span><span class="sxs-lookup"><span data-stu-id="773b4-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="773b4-141">示例映射</span><span class="sxs-lookup"><span data-stu-id="773b4-141">Sample mapping</span></span>  
4. <span data-ttu-id="773b4-142">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-142">Click Create configuration.</span></span>
5. <span data-ttu-id="773b4-143">展开“先决条件”部分。</span><span class="sxs-lookup"><span data-stu-id="773b4-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="773b4-144">请注意，已自动添加了“实施”先决条件组。</span><span class="sxs-lookup"><span data-stu-id="773b4-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="773b4-145">此组中包含引用父数据模型配置的先决条件组件，并且标记为“实施”。</span><span class="sxs-lookup"><span data-stu-id="773b4-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="773b4-146">这意味着此“示例映射”模型映射配置被视为“示例数据模型”数据模型的实施。</span><span class="sxs-lookup"><span data-stu-id="773b4-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="773b4-147">因此，如果下载了“示例数据模型”模型配置，此组件将强制 ER 从 ER 存储库下载“示例映射”模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="773b4-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="773b4-148">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-148">Click Designer.</span></span>
    * <span data-ttu-id="773b4-149">请注意，创建的模型映射配置中包含一个与创建的配置同名的新空白映射。</span><span class="sxs-lookup"><span data-stu-id="773b4-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="773b4-150">请注意，如果所选父模型配置中包含模型映射，将把这些映射复制到新模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="773b4-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="773b4-151">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-151">Click Designer.</span></span>
8. <span data-ttu-id="773b4-152">在树结构中，选择“Dynamics 365 for Operations\表格”。</span><span class="sxs-lookup"><span data-stu-id="773b4-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="773b4-153">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="773b4-153">Click Add root.</span></span>
10. <span data-ttu-id="773b4-154">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="773b4-155">公司</span><span class="sxs-lookup"><span data-stu-id="773b4-155">Company</span></span>  
11. <span data-ttu-id="773b4-156">在“表格”字段中，键入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="773b4-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="773b4-157">公司信息</span><span class="sxs-lookup"><span data-stu-id="773b4-157">CompanyInfo</span></span>  
12. <span data-ttu-id="773b4-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-158">Click OK.</span></span>
13. <span data-ttu-id="773b4-159">在树中，展开“公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="773b4-160">在树中，展开“公司\find()”。</span><span class="sxs-lookup"><span data-stu-id="773b4-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="773b4-161">在树中，选择“公司\find()\名称”。</span><span class="sxs-lookup"><span data-stu-id="773b4-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="773b4-162">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-162">Click Bind.</span></span>
17. <span data-ttu-id="773b4-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="773b4-163">Click Save.</span></span>
18. <span data-ttu-id="773b4-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-164">Close the page.</span></span>
19. <span data-ttu-id="773b4-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-165">Close the page.</span></span>
20. <span data-ttu-id="773b4-166">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="773b4-167">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="773b4-167">Click User parameters.</span></span>
22. <span data-ttu-id="773b4-168">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="773b4-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="773b4-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-169">Click OK.</span></span>
24. <span data-ttu-id="773b4-170">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="773b4-170">Click Edit.</span></span>
25. <span data-ttu-id="773b4-171">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="773b4-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="773b4-172">添加新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="773b4-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="773b4-173">在树中，选择“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="773b4-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="773b4-174">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="773b4-175">在“新建”字段中，输入“格式基于数据模型‘示例数据模型’”。</span><span class="sxs-lookup"><span data-stu-id="773b4-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="773b4-176">在“名称”字段中，键入“示例格式”。</span><span class="sxs-lookup"><span data-stu-id="773b4-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="773b4-177">示例格式</span><span class="sxs-lookup"><span data-stu-id="773b4-177">Sample format</span></span>  
5. <span data-ttu-id="773b4-178">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-178">Click Create configuration.</span></span>
6. <span data-ttu-id="773b4-179">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-179">Click Designer.</span></span>
7. <span data-ttu-id="773b4-180">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="773b4-181">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="773b4-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="773b4-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-182">Click OK.</span></span>
10. <span data-ttu-id="773b4-183">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="773b4-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="773b4-184">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="773b4-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="773b4-185">在树中，选择“模型\公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="773b4-186">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-186">Click Bind.</span></span>
14. <span data-ttu-id="773b4-187">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="773b4-187">Click Save.</span></span>
15. <span data-ttu-id="773b4-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-188">Close the page.</span></span>
    * <span data-ttu-id="773b4-189">为测试目的运行所创建格式的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="773b4-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="773b4-190">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="773b4-190">Click Run.</span></span>
    * <span data-ttu-id="773b4-191">在“版本”快速选项卡上，单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="773b4-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="773b4-192">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-192">Click OK.</span></span>
    * <span data-ttu-id="773b4-193">查看其中包含运行此格式配置的用户所登录公司的名称的输出。</span><span class="sxs-lookup"><span data-stu-id="773b4-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="773b4-194">请注意，所创键模型映射配置由此格式配置使用，因为只有一个可用配置中包含所需模型映射。</span><span class="sxs-lookup"><span data-stu-id="773b4-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="773b4-195">添加备用 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="773b4-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="773b4-196">在树中，选择“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="773b4-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="773b4-197">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="773b4-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="773b4-198">在“新建”字段中，输入“模型映射基于数据模型‘示例数据模型’”。</span><span class="sxs-lookup"><span data-stu-id="773b4-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="773b4-199">在“名称”字段中，键入“示例映射(备用)”。</span><span class="sxs-lookup"><span data-stu-id="773b4-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="773b4-200">示例映射（备用）</span><span class="sxs-lookup"><span data-stu-id="773b4-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="773b4-201">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="773b4-201">Click Create configuration.</span></span>
6. <span data-ttu-id="773b4-202">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-202">Click Designer.</span></span>
7. <span data-ttu-id="773b4-203">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="773b4-203">Click Designer.</span></span>
8. <span data-ttu-id="773b4-204">在树结构中，选择“Dynamics 365 for Operations\表格”。</span><span class="sxs-lookup"><span data-stu-id="773b4-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="773b4-205">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="773b4-205">Click Add root.</span></span>
10. <span data-ttu-id="773b4-206">在“名称”字段中，键入“公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="773b4-207">公司</span><span class="sxs-lookup"><span data-stu-id="773b4-207">Company</span></span>  
11. <span data-ttu-id="773b4-208">在“表格”字段中，键入“公司信息”。</span><span class="sxs-lookup"><span data-stu-id="773b4-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="773b4-209">公司信息</span><span class="sxs-lookup"><span data-stu-id="773b4-209">CompanyInfo</span></span>  
12. <span data-ttu-id="773b4-210">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-210">Click OK.</span></span>
13. <span data-ttu-id="773b4-211">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="773b4-211">Click Edit.</span></span>
14. <span data-ttu-id="773b4-212">在树结构中，选择“字符串\连接”。</span><span class="sxs-lookup"><span data-stu-id="773b4-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="773b4-213">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="773b4-213">Click Add function.</span></span>
16. <span data-ttu-id="773b4-214">在树中，展开“公司”。</span><span class="sxs-lookup"><span data-stu-id="773b4-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="773b4-215">在树中，展开“公司\find()”。</span><span class="sxs-lookup"><span data-stu-id="773b4-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="773b4-216">在树中，选择“公司\find()\名称”。</span><span class="sxs-lookup"><span data-stu-id="773b4-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="773b4-217">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="773b4-217">Click Add data source.</span></span>
20. <span data-ttu-id="773b4-218">在“配方”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="773b4-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="773b4-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="773b4-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="773b4-220">在树中，选择“公司\find()\Company(DataArea)”。</span><span class="sxs-lookup"><span data-stu-id="773b4-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="773b4-221">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="773b4-221">Click Add data source.</span></span>
23. <span data-ttu-id="773b4-222">在“配方”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="773b4-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="773b4-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="773b4-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="773b4-224">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="773b4-224">Click Save.</span></span>
25. <span data-ttu-id="773b4-225">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-225">Close the page.</span></span>
26. <span data-ttu-id="773b4-226">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="773b4-226">Click Save.</span></span>
27. <span data-ttu-id="773b4-227">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-227">Close the page.</span></span>
28. <span data-ttu-id="773b4-228">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="773b4-228">Close the page.</span></span>
29. <span data-ttu-id="773b4-229">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="773b4-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="773b4-230">使用现有 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="773b4-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="773b4-231">在树中，选择“示例数据模型\示例格式“。</span><span class="sxs-lookup"><span data-stu-id="773b4-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="773b4-232">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="773b4-232">Click Run.</span></span>
    * <span data-ttu-id="773b4-233">请注意，不能执行所选 ER 格式配置草稿版本，因为有多个模型映射配置可用于已选择为运行 ER 格式的数据源的未定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="773b4-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="773b4-234">接下来，您将把备用模型映射配置定义为来自将用作运行 ER 格式的数据源的模型映射的模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="773b4-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="773b4-235">在树中，选择“示例数据模型\示例映射(备用)“。</span><span class="sxs-lookup"><span data-stu-id="773b4-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="773b4-236">在“模型映射的默认值”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="773b4-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="773b4-237">在树中，选择“示例数据模型\示例格式“。</span><span class="sxs-lookup"><span data-stu-id="773b4-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="773b4-238">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="773b4-238">Click Run.</span></span>
7. <span data-ttu-id="773b4-239">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="773b4-239">Click OK.</span></span>
    * <span data-ttu-id="773b4-240">请注意，默认模型映射配置供此格式配置用于生成电子单据（创建的输出中包含公司代码）。</span><span class="sxs-lookup"><span data-stu-id="773b4-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  


