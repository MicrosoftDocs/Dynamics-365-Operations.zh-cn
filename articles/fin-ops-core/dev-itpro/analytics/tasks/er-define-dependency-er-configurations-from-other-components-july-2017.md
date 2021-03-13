---
title: 定义其他组件上的电子报告配置的依赖关系
description: 本主题介绍如何设计电子报告 (ER) 配置并指定其与其他软件组件的依赖关系。
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9516ac68c46649ebc50711357b97179bfc1b2c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092142"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a><span data-ttu-id="dd021-103">定义其他组件上的电子报告配置的依赖关系</span><span class="sxs-lookup"><span data-stu-id="dd021-103">Define the dependency of ER configurations on other components</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd021-104">若要完成这些步骤，首先必须完成任务指南“ER 管理模型映射配置”中的步骤，还必须可以访问 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="dd021-104">To complete these steps, you must first complete the steps in the task guide, ER Manage model mapping configurations, and you must have access to Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="dd021-105">此过程显示如何设计电子申报 (ER) 配置和指定其与其他软件组件之间的依赖关系，以便帮助确保将配置正确下载到特定 Finance and Operations 版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-105">This procedure shows how to design an Electronic reporting (ER) configuration and specify its dependency from other software components, so that you can help guarantee that the configuration is correctly downloaded to a specific version of Finance and Operations.</span></span> <span data-ttu-id="dd021-106">在此示例中，将为示例公司 Litware 公司创建所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="dd021-106">In this example, you will create required ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="dd021-107">此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。</span><span class="sxs-lookup"><span data-stu-id="dd021-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="dd021-108">这些步骤适用于所有公司，因为这些公司共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="dd021-108">The steps can be performed in any company, because ER configurations are shared among companies.</span></span> 

1. <span data-ttu-id="dd021-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="dd021-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
    * <span data-ttu-id="dd021-110">确保配置树中包含“示例数据模型”配置和附属项。</span><span class="sxs-lookup"><span data-stu-id="dd021-110">Make sure that the configurations tree contains the 'Sample data model' configuration and subordinate items.</span></span> <span data-ttu-id="dd021-111">否则，完成“ER 管理模型映射配置”这一任务指南中的步骤，然后再次启动此指南。</span><span class="sxs-lookup"><span data-stu-id="dd021-111">Otherwise, complete the steps in the task guide, ER Manage model mapping configurations, and then start this guide again.</span></span>   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a><span data-ttu-id="dd021-112">定义 ER 配置与其他组件之间的依赖关系</span><span class="sxs-lookup"><span data-stu-id="dd021-112">Define the dependency of ER configurations from other components</span></span>
1. <span data-ttu-id="dd021-113">在树中，展开“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-113">In the tree, expand 'Sample data model'.</span></span>
2. <span data-ttu-id="dd021-114">在树中，选择“示例数据模型\示例映射“。</span><span class="sxs-lookup"><span data-stu-id="dd021-114">In the tree, select 'Sample data model\Sample mapping'.</span></span>
    * <span data-ttu-id="dd021-115">我们选择了“示例映射”模型映射配置的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-115">We selected the draft version of the 'Sample mapping' model mapping configuration.</span></span> <span data-ttu-id="dd021-116">我们现在将定义其与其他软件组件之间的依赖关系。</span><span class="sxs-lookup"><span data-stu-id="dd021-116">We will now define its dependency from other software components.</span></span> <span data-ttu-id="dd021-117">此步骤被视为控制从 ER 存储库下载此配置的版本和进一步使用此版本的先决条件。</span><span class="sxs-lookup"><span data-stu-id="dd021-117">This step is considered a prerequisite for controlling the download of this configuration's version from an ER repository and any further use of this version.</span></span>   
3. <span data-ttu-id="dd021-118">展开“先决条件”部分。</span><span class="sxs-lookup"><span data-stu-id="dd021-118">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="dd021-119">请注意，此阶段已自动添加了“实施”先决条件组。</span><span class="sxs-lookup"><span data-stu-id="dd021-119">Note that the 'Implementations' prerequisites group has been added automatically at this stage.</span></span> <span data-ttu-id="dd021-120">此组中包含引用数据模型配置的先决条件组件，并且已开启了实施标记。</span><span class="sxs-lookup"><span data-stu-id="dd021-120">This group contains the prerequisite component that refers to the data model configuration and has the Implementation flag turned on.</span></span> <span data-ttu-id="dd021-121">此标记指示“示例映射”映射配置被视为“示例数据模型”数据模型的实施。</span><span class="sxs-lookup"><span data-stu-id="dd021-121">This flag indicates that the 'Sample mapping' mapping configuration is considered the implementation of the 'Sample data model' data model.</span></span> <span data-ttu-id="dd021-122">只要下载了“示例数据模型”模型配置，此组件都将强制 ER 从 ER 存储库下载“示例映射”映射配置。</span><span class="sxs-lookup"><span data-stu-id="dd021-122">This component will force ER to download the 'Sample mapping' mapping configuration from an ER repository whenever the 'Sample data model' model configuration is downloaded.</span></span>   
4. <span data-ttu-id="dd021-123">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="dd021-123">Click Edit.</span></span>
    * <span data-ttu-id="dd021-124">可以通过使用软件组件的类型，以及组件版本或组件版本范围，定义配置的当前版本与该软件组件之间的单个依赖关系。</span><span class="sxs-lookup"><span data-stu-id="dd021-124">A single dependency of the current version of a configuration from a software component can be specified by using the definition of the component's type, and either the component version or a range of component versions.</span></span>  
    * <span data-ttu-id="dd021-125">可以将所需依赖关系组合在一起。</span><span class="sxs-lookup"><span data-stu-id="dd021-125">Desired dependencies can be grouped together.</span></span> <span data-ttu-id="dd021-126">如果选择了“所有”组类型，并且满足了此组和附属组的每个依赖关系条件，将视为满足了此组的依赖关系条件。</span><span class="sxs-lookup"><span data-stu-id="dd021-126">When the 'All of' grouping type is selected, the dependency condition of this group is considered satisfied when each dependency condition from this group and subordinate group is satisfied.</span></span> <span data-ttu-id="dd021-127">如果选择了“一个”组类型，并且满足了此组的至少一个依赖关系条件，将视为满足了此组的依赖关系条件。</span><span class="sxs-lookup"><span data-stu-id="dd021-127">When the 'One of' grouping type is selected, the dependency condition of this group is considered satisfied when at least one dependency condition from this group is satisfied.</span></span>   
5. <span data-ttu-id="dd021-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dd021-128">Click New.</span></span>
6. <span data-ttu-id="dd021-129">选择”产品必备项组件“。</span><span class="sxs-lookup"><span data-stu-id="dd021-129">Select Product prerequisite component.</span></span>
7. <span data-ttu-id="dd021-130">选择 Microsoft Dynamics 365 for Operations (1611)。</span><span class="sxs-lookup"><span data-stu-id="dd021-130">Select Microsoft Dynamics 365 for Operations (1611).</span></span>
8. <span data-ttu-id="dd021-131">在”版本“字段中，键入”[7.1.1541.3036,8)“。</span><span class="sxs-lookup"><span data-stu-id="dd021-131">In the Version field, type '[7.1.1541.3036,8)'.</span></span>
    * <span data-ttu-id="dd021-132">[7.1.1541.3036,8)</span><span class="sxs-lookup"><span data-stu-id="dd021-132">[7.1.1541.3036,8)</span></span>  
    * <span data-ttu-id="dd021-133">如果从任何 ER 存储库下载了此配置，将评估您输入的依赖关系。</span><span class="sxs-lookup"><span data-stu-id="dd021-133">Dependencies that you enter will be evaluated when this configuration is downloaded from any ER repository.</span></span> <span data-ttu-id="dd021-134">如果“示例数据模型”配置的版本 1 已提前准备就绪或下载，将从 ER 存储库下载此配置版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-134">This configuration version will be downloaded from the ER repository when version 1 of the 'Sample data model' configuration is either already in place or downloaded in advance.</span></span> <span data-ttu-id="dd021-135">如果提前下载，则必须在 Finance and Operations 版本 7.1.1541.3036 或更高版本中完成，但是不得超过主要版本 8。</span><span class="sxs-lookup"><span data-stu-id="dd021-135">If it's downloaded in advance, it must be completed in Finance and Operations version 7.1.1541.3036 or later, but must not exceed major version 8.</span></span>   
9. <span data-ttu-id="dd021-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="dd021-136">Click Save.</span></span>
10. <span data-ttu-id="dd021-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-137">Close the page.</span></span>
11. <span data-ttu-id="dd021-138">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="dd021-138">Click Change status.</span></span>
12. <span data-ttu-id="dd021-139">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="dd021-139">Click Complete.</span></span>
13. <span data-ttu-id="dd021-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-140">Click OK.</span></span>
14. <span data-ttu-id="dd021-141">在树中，选择“示例数据模型\示例映射(备用)“。</span><span class="sxs-lookup"><span data-stu-id="dd021-141">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
15. <span data-ttu-id="dd021-142">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="dd021-142">Click Edit.</span></span>
16. <span data-ttu-id="dd021-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dd021-143">Click New.</span></span>
17. <span data-ttu-id="dd021-144">选择”产品必备项组件“。</span><span class="sxs-lookup"><span data-stu-id="dd021-144">Select Product prerequisite component.</span></span>
18. <span data-ttu-id="dd021-145">选择 Microsoft Dynamics AX 7.0 RTW。</span><span class="sxs-lookup"><span data-stu-id="dd021-145">Select Microsoft Dynamics AX 7.0 RTW.</span></span>
19. <span data-ttu-id="dd021-146">在”版本“字段中，键入”[7.0.1265.3015,7.1)“。</span><span class="sxs-lookup"><span data-stu-id="dd021-146">In the Version field, type '[7.0.1265.3015,7.1)'.</span></span>
    * <span data-ttu-id="dd021-147">[7.0.1265.3015,7.1)</span><span class="sxs-lookup"><span data-stu-id="dd021-147">[7.0.1265.3015,7.1)</span></span>  
    * <span data-ttu-id="dd021-148">如果从任何 ER 存储库下载了此配置，将评估依赖关系。</span><span class="sxs-lookup"><span data-stu-id="dd021-148">Dependencies will be evaluated when the configuration is downloaded from any ER repository.</span></span> <span data-ttu-id="dd021-149">如果“示例数据模型”配置的版本 1 已提前准备就绪或下载，将从 ER 存储库下载此配置版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-149">This configuration version will be downloaded from the ER repository when version 1 of the 'Sample data model' configuration is either already in place or downloaded in advance.</span></span> <span data-ttu-id="dd021-150">如果提前下载，则必须在 Microsoft Dynamics 365 for Finance and Operations Enterprise edition 中完成，其版本必须为 7.0.1265.3015 或更高，但是不得超过次要版本 1。</span><span class="sxs-lookup"><span data-stu-id="dd021-150">If it's downloaded in advance, it must be completed in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, the version of which must be 7.0.1265.3015 or later, but must not exceed minor version 1.</span></span>   
20. <span data-ttu-id="dd021-151">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="dd021-151">Click Save.</span></span>
21. <span data-ttu-id="dd021-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-152">Close the page.</span></span>
22. <span data-ttu-id="dd021-153">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="dd021-153">Click Change status.</span></span>
23. <span data-ttu-id="dd021-154">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="dd021-154">Click Complete.</span></span>
24. <span data-ttu-id="dd021-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-155">Click OK.</span></span>

## <a name="configure-the-er-repository"></a><span data-ttu-id="dd021-156">配置 ER 存储库</span><span class="sxs-lookup"><span data-stu-id="dd021-156">Configure the ER repository</span></span>
1. <span data-ttu-id="dd021-157">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-157">Close the page.</span></span>
2. <span data-ttu-id="dd021-158">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="dd021-158">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="dd021-159">打开当前 ER 提供商 Litware 公司的 ER 存储库列表。</span><span class="sxs-lookup"><span data-stu-id="dd021-159">Open the list of ER repositories for the current ER provider, Litware, Inc.</span></span>  
3. <span data-ttu-id="dd021-160">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="dd021-160">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dd021-161">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="dd021-161">Click Repositories.</span></span>
5. <span data-ttu-id="dd021-162">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="dd021-162">Click Show filters.</span></span>
6. <span data-ttu-id="dd021-163">使用”包含“筛选器运算符在”类型名称“字段中输入筛选器值”LCS“。</span><span class="sxs-lookup"><span data-stu-id="dd021-163">Enter a filter value of "LCS" on the "Type name" field using the "contains" filter operator.</span></span>
    * <span data-ttu-id="dd021-164">如果已经为当前 ER 提供商注册了 LCS 存储库，则可跳过此子任务中的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="dd021-164">If the LCS repository is already registered for the current ER provider, you can skip the remaining steps in this sub-task.</span></span> <span data-ttu-id="dd021-165">如果尚未注册 LCS 存储库，请完成其余步骤。</span><span class="sxs-lookup"><span data-stu-id="dd021-165">If the LCS repository isn't already registered, complete the remaining steps.</span></span>   
7. <span data-ttu-id="dd021-166">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="dd021-166">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="dd021-167">在“配置存储库类型”字段中，输入”LCS“。</span><span class="sxs-lookup"><span data-stu-id="dd021-167">In the Configuration repository type field, enter 'LCS'.</span></span>
9. <span data-ttu-id="dd021-168">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="dd021-168">Click Create repository.</span></span>
10. <span data-ttu-id="dd021-169">在“项目”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dd021-169">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="dd021-170">从“项目”字段的查找中选择所需 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="dd021-170">Select the desired LCS project from the lookup of the 'Project' field.</span></span>  
11. <span data-ttu-id="dd021-171">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-171">Click OK.</span></span>
12. <span data-ttu-id="dd021-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-172">Close the page.</span></span>

## <a name="upload-configurations-to-lcs"></a><span data-ttu-id="dd021-173">将配置上传到 LCS</span><span class="sxs-lookup"><span data-stu-id="dd021-173">Upload configurations to LCS</span></span>
1. <span data-ttu-id="dd021-174">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="dd021-174">Click Reporting configurations.</span></span>
2. <span data-ttu-id="dd021-175">在树中，选择“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-175">In the tree, select 'Sample data model'.</span></span>
3. <span data-ttu-id="dd021-176">选择此配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-176">Select the completed version of this configuration.</span></span>
4. <span data-ttu-id="dd021-177">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="dd021-177">Click Change status.</span></span>
5. <span data-ttu-id="dd021-178">单击“共享”。</span><span class="sxs-lookup"><span data-stu-id="dd021-178">Click Share.</span></span>
6. <span data-ttu-id="dd021-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-179">Click OK.</span></span>
    * <span data-ttu-id="dd021-180">已通过使用以前配置的 ER 存储库的 LCS 项目，将此模型配置的版本 1 上传到该 LCS。</span><span class="sxs-lookup"><span data-stu-id="dd021-180">Version 1 of this model configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   
7. <span data-ttu-id="dd021-181">在树中，展开“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-181">In the tree, expand 'Sample data model'.</span></span>
8. <span data-ttu-id="dd021-182">在树中，选择“示例数据模型\示例映射“。</span><span class="sxs-lookup"><span data-stu-id="dd021-182">In the tree, select 'Sample data model\Sample mapping'.</span></span>
9. <span data-ttu-id="dd021-183">选择此配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-183">Select the completed version of this configuration.</span></span>
10. <span data-ttu-id="dd021-184">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="dd021-184">Click Change status.</span></span>
11. <span data-ttu-id="dd021-185">单击“共享”。</span><span class="sxs-lookup"><span data-stu-id="dd021-185">Click Share.</span></span>
12. <span data-ttu-id="dd021-186">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-186">Click OK.</span></span>
    * <span data-ttu-id="dd021-187">已通过使用以前配置的 ER 存储库的 LCS 项目，将此模型映射配置的版本 1.1 上传到该 LCS。</span><span class="sxs-lookup"><span data-stu-id="dd021-187">Version 1.1 of this model mapping configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   
13. <span data-ttu-id="dd021-188">在树中，选择“示例数据模型\示例映射(备用)“。</span><span class="sxs-lookup"><span data-stu-id="dd021-188">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
14. <span data-ttu-id="dd021-189">选择此配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="dd021-189">Select the completed version of this configuration.</span></span>
15. <span data-ttu-id="dd021-190">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="dd021-190">Click Change status.</span></span>
16. <span data-ttu-id="dd021-191">单击“共享”。</span><span class="sxs-lookup"><span data-stu-id="dd021-191">Click Share.</span></span>
17. <span data-ttu-id="dd021-192">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dd021-192">Click OK.</span></span>
    * <span data-ttu-id="dd021-193">已通过使用以前配置的 ER 存储库的 LCS 项目，将此模型映射配置的版本 1.1 上传到该 LCS。</span><span class="sxs-lookup"><span data-stu-id="dd021-193">Version 1.1 of this model mapping configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   

## <a name="evaluate-er-configuration-dependencies"></a><span data-ttu-id="dd021-194">评估 ER 配置依赖关系</span><span class="sxs-lookup"><span data-stu-id="dd021-194">Evaluate ER configuration dependencies</span></span>
<span data-ttu-id="dd021-195">我们将从系统中删除创建的配置，然后将其从 LCS 存储库下载回来。</span><span class="sxs-lookup"><span data-stu-id="dd021-195">We will delete created configurations from the system and download them back from the LCS repository.</span></span>  
1. <span data-ttu-id="dd021-196">在树中，选择“示例数据模型\示例映射“。</span><span class="sxs-lookup"><span data-stu-id="dd021-196">In the tree, select 'Sample data model\Sample mapping'.</span></span>
2. <span data-ttu-id="dd021-197">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="dd021-197">Click Delete.</span></span>
3. <span data-ttu-id="dd021-198">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="dd021-198">Click Yes.</span></span>
4. <span data-ttu-id="dd021-199">在树中，选择“示例数据模型\示例映射(备用)“。</span><span class="sxs-lookup"><span data-stu-id="dd021-199">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
5. <span data-ttu-id="dd021-200">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="dd021-200">Click Delete.</span></span>
6. <span data-ttu-id="dd021-201">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="dd021-201">Click Yes.</span></span>
7. <span data-ttu-id="dd021-202">在树中，选择“示例数据模型\示例格式“。</span><span class="sxs-lookup"><span data-stu-id="dd021-202">In the tree, select 'Sample data model\Sample format'.</span></span>
8. <span data-ttu-id="dd021-203">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="dd021-203">Click Delete.</span></span>
9. <span data-ttu-id="dd021-204">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="dd021-204">Click Yes.</span></span>
10. <span data-ttu-id="dd021-205">在树中，选择“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-205">In the tree, select 'Sample data model'.</span></span>
11. <span data-ttu-id="dd021-206">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="dd021-206">Click Delete.</span></span>
12. <span data-ttu-id="dd021-207">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="dd021-207">Click Yes.</span></span>
13. <span data-ttu-id="dd021-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-208">Close the page.</span></span>
    * <span data-ttu-id="dd021-209">打开当前 ER 提供商 Litware 公司的 ER 存储库列表。</span><span class="sxs-lookup"><span data-stu-id="dd021-209">Open the list of ER repositories for the current ER provider, Litware, Inc.</span></span>  
14. <span data-ttu-id="dd021-210">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="dd021-210">Click Repositories.</span></span>
15. <span data-ttu-id="dd021-211">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="dd021-211">Click Show filters.</span></span>
16. <span data-ttu-id="dd021-212">使用”包含“筛选器运算符在”类型名称“字段中输入筛选器值”LCS“。</span><span class="sxs-lookup"><span data-stu-id="dd021-212">Enter a filter value of "LCS" on the "Type name" field using the "contains" filter operator.</span></span>
17. <span data-ttu-id="dd021-213">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="dd021-213">Click Open.</span></span>
18. <span data-ttu-id="dd021-214">在树中，选择“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-214">In the tree, select 'Sample data model'.</span></span>
    * <span data-ttu-id="dd021-215">请注意，您可以查看对是否已满足了当前存储库的 ER 配置各版本必备项的评估。</span><span class="sxs-lookup"><span data-stu-id="dd021-215">Note that you can view an evaluation of whether prerequisite conditions have been satisfied for each version of the ER configurations for the current repository.</span></span> <span data-ttu-id="dd021-216">若要查看此评估，请单击“检查必备项”。</span><span class="sxs-lookup"><span data-stu-id="dd021-216">To view this evaluation, click Check prerequisites.</span></span>   
19. <span data-ttu-id="dd021-217">单击”检查必备项“。</span><span class="sxs-lookup"><span data-stu-id="dd021-217">Click Check prerequisites.</span></span>
20. <span data-ttu-id="dd021-218">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="dd021-218">Click Import.</span></span>
21. <span data-ttu-id="dd021-219">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="dd021-219">Click Yes.</span></span>
22. <span data-ttu-id="dd021-220">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-220">Close the page.</span></span>
23. <span data-ttu-id="dd021-221">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-221">Close the page.</span></span>
24. <span data-ttu-id="dd021-222">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dd021-222">Close the page.</span></span>
25. <span data-ttu-id="dd021-223">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="dd021-223">Go to Organization administration > Electronic reporting > Configurations.</span></span>
26. <span data-ttu-id="dd021-224">在树中，展开“示例数据模型”。</span><span class="sxs-lookup"><span data-stu-id="dd021-224">In the tree, expand 'Sample data model'.</span></span>
    * <span data-ttu-id="dd021-225">请注意，已下载了模型“示例映射”映射配置和所选数据模型配置。</span><span class="sxs-lookup"><span data-stu-id="dd021-225">Note that the model 'Sample mapping' mapping configuration has been downloaded together with the selected data model configuration.</span></span> <span data-ttu-id="dd021-226">一起下载这两个文件是因为已将“示例映射”定义为实施所选数据模型，并且其适用于此应用程序。</span><span class="sxs-lookup"><span data-stu-id="dd021-226">The two files are downloaded together because 'Sample mapping' has been defined as implementing the selected data model, and because it's applicable for the application.</span></span> <span data-ttu-id="dd021-227">尚未下载“示例映射（备用）”配置，因为未满足所需应用程序版本的条件。</span><span class="sxs-lookup"><span data-stu-id="dd021-227">The 'Sample mapping (alternative)' configuration hasn't been downloaded because the condition for the required application version isn't satisfied.</span></span>   
    * <span data-ttu-id="dd021-228">如果登录 Finance and Operations，注册相同提供程序，访问相同 LCS 项目，然后下载相同数据模型配置，将下载“示例映射（备用）”配置，但将跳过“示例映射”配置。</span><span class="sxs-lookup"><span data-stu-id="dd021-228">If you sign in to Finance and Operations, register the same provider, access the same LCS project, and download the same data model configuration, the 'Sample mapping (alternative)' configuration will download, whereas the 'Sample mapping' configuration will be skipped.</span></span>  
