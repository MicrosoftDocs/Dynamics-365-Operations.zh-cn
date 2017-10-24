---
title: "数据导入和导出作业"
description: "使用数据管理工作区创建和管理数据导入和导出作业。"
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c788b018f621144755cc0b4ee4b55cb633cd81be
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="data-import-and-export-jobs"></a><span data-ttu-id="a3467-103">数据导入和导出作业</span><span class="sxs-lookup"><span data-stu-id="a3467-103">Data import and export jobs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3467-104">要在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中创建和管理数据导入和导出作业，请使用**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="a3467-104">To create and manage data import and export jobs in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you use the **Data management** workspace.</span></span> <span data-ttu-id="a3467-105">默认情况下，数据导入和导出流程为目标数据库中的每个实体创建一个暂存表。</span><span class="sxs-lookup"><span data-stu-id="a3467-105">By default, the data import and export process creates a staging table for each entity in the target database.</span></span> <span data-ttu-id="a3467-106">通过暂存表可以在移动数据之前验证、清理或转换数据。</span><span class="sxs-lookup"><span data-stu-id="a3467-106">Staging tables let you verify, clean up, or convert data before you move it.</span></span>

## <a name="data-importexport-process"></a><span data-ttu-id="a3467-107">数据导入/导出流程</span><span class="sxs-lookup"><span data-stu-id="a3467-107">Data import/export process</span></span>
<span data-ttu-id="a3467-108">以下是导入或导出数据的步骤。</span><span class="sxs-lookup"><span data-stu-id="a3467-108">Here are the steps to import or export data.</span></span>

1. <span data-ttu-id="a3467-109">在完成以下任务后创建导入或导出作业：</span><span class="sxs-lookup"><span data-stu-id="a3467-109">Create an import or export job where you complete the following tasks:</span></span>

    - <span data-ttu-id="a3467-110">定义项目类别。</span><span class="sxs-lookup"><span data-stu-id="a3467-110">Define the project category.</span></span>
    - <span data-ttu-id="a3467-111">确定要导入或导出的实体。</span><span class="sxs-lookup"><span data-stu-id="a3467-111">Identify the entities to import or export.</span></span>
    - <span data-ttu-id="a3467-112">设置作业的数据格式。</span><span class="sxs-lookup"><span data-stu-id="a3467-112">Set the data format for the job.</span></span>
    - <span data-ttu-id="a3467-113">给实体排序，以便以合理的顺序在逻辑组中处理这些实体。</span><span class="sxs-lookup"><span data-stu-id="a3467-113">Sequence the entities, so that they are processed in logical groups and in an order that makes sense.</span></span>
    - <span data-ttu-id="a3467-114">确定是否使用暂存表。</span><span class="sxs-lookup"><span data-stu-id="a3467-114">Determine whether to use staging tables.</span></span>

2. <span data-ttu-id="a3467-115">验证源数据和目标数据是否正确映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-115">Validate that the source data and target data are mapped correctly.</span></span>
3. <span data-ttu-id="a3467-116">验证您的导入或导出作业的安全性。</span><span class="sxs-lookup"><span data-stu-id="a3467-116">Verify the security for your import or export job.</span></span>
4. <span data-ttu-id="a3467-117">运行导入或导出作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-117">Run the import or export job.</span></span>
5. <span data-ttu-id="a3467-118">查看作业历史纪录，验证作业是否按预期运行。</span><span class="sxs-lookup"><span data-stu-id="a3467-118">Validate that the job ran as expected by reviewing the job history.</span></span>
6. <span data-ttu-id="a3467-119">清除暂存表。</span><span class="sxs-lookup"><span data-stu-id="a3467-119">Clean up the staging tables.</span></span>

<span data-ttu-id="a3467-120">本主题的其余部分提供有关流程的每个步骤的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a3467-120">The remaining sections of this topic provide more details about each step of the process.</span></span>

## <a name="create-an-import-or-export-job"></a><span data-ttu-id="a3467-121">创建导入或导出作业</span><span class="sxs-lookup"><span data-stu-id="a3467-121">Create an import or export job</span></span>
<span data-ttu-id="a3467-122">可以一次性运行或分多次运行数据导入或导出作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-122">A data import or export job can be run one time or many times.</span></span>

### <a name="define-the-project-category"></a><span data-ttu-id="a3467-123">定义项目类别</span><span class="sxs-lookup"><span data-stu-id="a3467-123">Define the project category</span></span>
<span data-ttu-id="a3467-124">我们建议您花时间为导入或导出作业选择合适的项目类别。</span><span class="sxs-lookup"><span data-stu-id="a3467-124">We recommend that you take the time to select an appropriate project category for your import or export job.</span></span> <span data-ttu-id="a3467-125">项目类别有助于管理相关作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-125">Project categories can help you manage related jobs.</span></span>

### <a name="identify-the-entities-to-import-or-export"></a><span data-ttu-id="a3467-126">确定要导入或导出的实体</span><span class="sxs-lookup"><span data-stu-id="a3467-126">Identify the entities to import or export</span></span>
<span data-ttu-id="a3467-127">您可以将特定实体添加到导入或导出作业或选择一个要应用的模板。</span><span class="sxs-lookup"><span data-stu-id="a3467-127">You can add specific entities to an import or export job or select a template to apply.</span></span> <span data-ttu-id="a3467-128">模板使用一个实体列表填充一个作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-128">Templates fill a job with a list of entities.</span></span> <span data-ttu-id="a3467-129">给作业命名并保存作业后，**应用模板**选项可用。</span><span class="sxs-lookup"><span data-stu-id="a3467-129">The **Apply template** option is available after you give the job a name and save the job.</span></span>

### <a name="set-the-data-format-for-the-job"></a><span data-ttu-id="a3467-130">设置作业的数据格式</span><span class="sxs-lookup"><span data-stu-id="a3467-130">Set the data format for the job</span></span>
<span data-ttu-id="a3467-131">选择一个实体后，必须选择要导出或导入的数据的格式。</span><span class="sxs-lookup"><span data-stu-id="a3467-131">When you select an entity, you must select the format of the data that will be exported or imported.</span></span> <span data-ttu-id="a3467-132">使用**数据源设置**磁贴定义格式。</span><span class="sxs-lookup"><span data-stu-id="a3467-132">You define formats by using the **Data sources setup** tile.</span></span> <span data-ttu-id="a3467-133">许多组织从演示数据集中默认包括的格式开始。</span><span class="sxs-lookup"><span data-stu-id="a3467-133">Many organizations start from the formats that are included by default in the demo data set.</span></span> <span data-ttu-id="a3467-134">以下是其中一些格式的列表：</span><span class="sxs-lookup"><span data-stu-id="a3467-134">Here is a list of some of these formats:</span></span>

- <span data-ttu-id="a3467-135">AX（导入或导出数据的格式必须与 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 所使用的格式相同）</span><span class="sxs-lookup"><span data-stu-id="a3467-135">AX (for data that must be imported or exported in the same format that is used for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition)</span></span>
- <span data-ttu-id="a3467-136">ColonSeparated</span><span class="sxs-lookup"><span data-stu-id="a3467-136">ColonSeparated</span></span>
- <span data-ttu-id="a3467-137">CSV</span><span class="sxs-lookup"><span data-stu-id="a3467-137">CSV</span></span>
- <span data-ttu-id="a3467-138">Excel</span><span class="sxs-lookup"><span data-stu-id="a3467-138">Excel</span></span>
- <span data-ttu-id="a3467-139">套装</span><span class="sxs-lookup"><span data-stu-id="a3467-139">Package</span></span>

### <a name="sequence-the-entities"></a><span data-ttu-id="a3467-140">给实体排序</span><span class="sxs-lookup"><span data-stu-id="a3467-140">Sequence the entities</span></span>
<span data-ttu-id="a3467-141">实体可以在数据模板或导入和导出作业中排序。</span><span class="sxs-lookup"><span data-stu-id="a3467-141">Entities can be sequenced in a data template, or in import and export jobs.</span></span> <span data-ttu-id="a3467-142">运行的作业包含多个数据实体时，必须确保数据实体的序列正确。</span><span class="sxs-lookup"><span data-stu-id="a3467-142">When you run a job that contains more than one data entity, you must make sure that the data entities are correctly sequenced.</span></span> <span data-ttu-id="a3467-143">给实体排序的主要目的是为了解决实体中的任何功能依赖项。</span><span class="sxs-lookup"><span data-stu-id="a3467-143">You sequence entities primarily so that you can address any functional dependencies among entities.</span></span> <span data-ttu-id="a3467-144">如果实体不具有任何功能依赖项，可以计划并行导入或导出。</span><span class="sxs-lookup"><span data-stu-id="a3467-144">If entities don’t have any functional dependencies, they can be scheduled for parallel import or export.</span></span>

#### <a name="execution-units-levels-and-sequences"></a><span data-ttu-id="a3467-145">执行单元、级别和序列</span><span class="sxs-lookup"><span data-stu-id="a3467-145">Execution units, levels, and sequences</span></span>
<span data-ttu-id="a3467-146">执行单元、执行单元中的级别以及实体序列有助于控制导出或导入数据的顺序。</span><span class="sxs-lookup"><span data-stu-id="a3467-146">The execution unit, level in the execution unit, and sequence of an entity help control the order that the data is exported or imported in.</span></span>

- <span data-ttu-id="a3467-147">不同执行单元中的实体并行处理。</span><span class="sxs-lookup"><span data-stu-id="a3467-147">Entities in different execution units are processed in parallel.</span></span>
- <span data-ttu-id="a3467-148">在每个执行单元中，具有相同级别的实体并行处理。</span><span class="sxs-lookup"><span data-stu-id="a3467-148">In each execution unit, entities are processed in parallel if they have the same level.</span></span>
- <span data-ttu-id="a3467-149">在每个级别中，根据实体在该级别中的序列号处理实体。</span><span class="sxs-lookup"><span data-stu-id="a3467-149">In each level, entities are processed according to their sequence number in that level.</span></span>
- <span data-ttu-id="a3467-150">处理完一个级别后，再处理下一个级别。</span><span class="sxs-lookup"><span data-stu-id="a3467-150">After one level has been processed, the next level is processed.</span></span>

#### <a name="resequencing"></a><span data-ttu-id="a3467-151">重新排序</span><span class="sxs-lookup"><span data-stu-id="a3467-151">Resequencing</span></span>
<span data-ttu-id="a3467-152">在以下情形中，您可能想要对实体重新排序：</span><span class="sxs-lookup"><span data-stu-id="a3467-152">You might want to resequence your entities in the following situations:</span></span>

- <span data-ttu-id="a3467-153">如果只有一个数据作业用于您的所有更改，可以使用重新排序选项来优化整个作业的执行时间。</span><span class="sxs-lookup"><span data-stu-id="a3467-153">If only one data job is used for all your changes, you can use resequencing options to optimize the execution time for the full job.</span></span> <span data-ttu-id="a3467-154">在这些情况下，您可以使用执行单元表示模块，用级别表示模块中的功能区域，用序列表示实体。</span><span class="sxs-lookup"><span data-stu-id="a3467-154">In these cases, you can use the execution unit to represent the module, the level to represent the feature area in the module, and the sequence to represent the entity.</span></span> <span data-ttu-id="a3467-155">使用此方法可以并行处理不同模块，但也仍然能在一个模块中按顺序处理。</span><span class="sxs-lookup"><span data-stu-id="a3467-155">By using this approach, you can work across modules in parallel, but you can still work in sequence in a module.</span></span> <span data-ttu-id="a3467-156">为了帮助保证成功完成并行操作，必须考虑所有依赖项。</span><span class="sxs-lookup"><span data-stu-id="a3467-156">To help guarantee that parallel operations succeed, you must consider all dependencies.</span></span>
- <span data-ttu-id="a3467-157">如果使用多个数据作业（例如，一个模块使用一个作业），可以使用排序来影响实体的级别和顺序，以获得最佳执行。</span><span class="sxs-lookup"><span data-stu-id="a3467-157">If multiple data jobs are used (for example, one job for each module), you can use sequencing to affect the level and sequence of entities for optimal execution.</span></span>
- <span data-ttu-id="a3467-158">如果没有任何依赖项，可以在不同执行单元对实体排序，以最大程度地进行优化。</span><span class="sxs-lookup"><span data-stu-id="a3467-158">If there are no dependencies at all, you can sequence entities at different execution units for maximum optimization.</span></span>

<span data-ttu-id="a3467-159">选择多个实体时，**重新排序**菜单可用。</span><span class="sxs-lookup"><span data-stu-id="a3467-159">The **Resequencing** menu is available when multiple entities are selected.</span></span> <span data-ttu-id="a3467-160">可以基于执行单元、级别或顺序选项重新排序。</span><span class="sxs-lookup"><span data-stu-id="a3467-160">You can resequence based on execution unit, level, or sequence options.</span></span> <span data-ttu-id="a3467-161">可以设定增量，以对选定的实体重新排序。</span><span class="sxs-lookup"><span data-stu-id="a3467-161">You can set an increment to resequence the entities that have been selected.</span></span> <span data-ttu-id="a3467-162">为每个实体选择的单元、级别和/或序列号按指定增量进行更新。</span><span class="sxs-lookup"><span data-stu-id="a3467-162">The unit, level, and/or sequence number that is selected for each entity is updated by the specified increment.</span></span>

#### <a name="sorting"></a><span data-ttu-id="a3467-163">排序</span><span class="sxs-lookup"><span data-stu-id="a3467-163">Sorting</span></span>
<span data-ttu-id="a3467-164">用户可以使用**排序依据**选项按顺序查看实体列表。</span><span class="sxs-lookup"><span data-stu-id="a3467-164">Use can use the **Sort by** option to view the entity list in sequential order.</span></span>

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a><span data-ttu-id="a3467-165">验证源数据和目标数据是否正确映射</span><span class="sxs-lookup"><span data-stu-id="a3467-165">Validate that the source data and target data are mapped correctly</span></span>
<span data-ttu-id="a3467-166">映射是同时适用于导入和导出作业的一项功能。</span><span class="sxs-lookup"><span data-stu-id="a3467-166">Mapping is a function that applies to both import and export jobs.</span></span>

- <span data-ttu-id="a3467-167">在导入作业情况下，映射描述源文件中的哪些列成为暂存表中的列。</span><span class="sxs-lookup"><span data-stu-id="a3467-167">In the context of an import job, mapping describes which columns in the source file become the columns in the staging table.</span></span> <span data-ttu-id="a3467-168">因此，系统可以确定源文件中的哪些列数据必须复制到暂存表中的哪一列。</span><span class="sxs-lookup"><span data-stu-id="a3467-168">Therefore, the system can determine which column data in the source file must be copied into which column of the staging table.</span></span>
- <span data-ttu-id="a3467-169">在导出作业情况下，映射描述暂存表（即源）中的哪些列成为目标文件中的列。</span><span class="sxs-lookup"><span data-stu-id="a3467-169">In the context of an export job, mapping describes which columns of the staging table (that is, the source) become the columns in the target file.</span></span>

<span data-ttu-id="a3467-170">如果暂存表和文件中的列名称匹配，则系统自动基于名称建立映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-170">If the column names in the staging table and the file match, the system automatically establishes the mapping, based on the names.</span></span> <span data-ttu-id="a3467-171">但是，如果名称有差异，则不会自动映射列。</span><span class="sxs-lookup"><span data-stu-id="a3467-171">However, if the names differ, columns aren’t mapped automatically.</span></span> <span data-ttu-id="a3467-172">在这些情况下，必须在数据作业中的实体上选择**查看映射**选项，以完成映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-172">In these cases, you must complete the mapping by selecting the **View map** option on the entity in the data job.</span></span>

<span data-ttu-id="a3467-173">有两个映射视图：**映射可视化**，即默认视图，以及**映射详细信息**。</span><span class="sxs-lookup"><span data-stu-id="a3467-173">There are two mapping views: **Mapping visualization**, which is the default view, and **Mapping details**.</span></span> <span data-ttu-id="a3467-174">红色星号 (\*) 标识实体中的任何必填字段。</span><span class="sxs-lookup"><span data-stu-id="a3467-174">A red asterisk (\*) identifies any required fields in the entity.</span></span> <span data-ttu-id="a3467-175">必须映射这些字段后才能处理实体。</span><span class="sxs-lookup"><span data-stu-id="a3467-175">These fields must be mapped before you can work with the entity.</span></span> <span data-ttu-id="a3467-176">处理实体时，可以按需要取消其他字段的映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-176">You can unmap other fields as you require when you work with the entity.</span></span> <span data-ttu-id="a3467-177">要取消字段映射，选择**实体**列或**源**列中的字段，然后选择**删除选择**。</span><span class="sxs-lookup"><span data-stu-id="a3467-177">To unmap a field, select the field in either the **Entity** column or the **Source** column, and then select **Delete selection**.</span></span> <span data-ttu-id="a3467-178">选择**保存**以保存更改，然后关闭页面以返回项目。</span><span class="sxs-lookup"><span data-stu-id="a3467-178">Select **Save** to save your changes, and then close the page to return to the project.</span></span> <span data-ttu-id="a3467-179">在导入后，您可以使用相同流程编辑来自源的字段映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-179">You can use the same process to edit the field mapping from source to staging after you import.</span></span>

<span data-ttu-id="a3467-180">通过选择**生成源映射**可以在页面上生成映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-180">You can generate a mapping on the page by selecting **Generate source mapping**.</span></span> <span data-ttu-id="a3467-181">生成的映射表现地类似于自动映射。</span><span class="sxs-lookup"><span data-stu-id="a3467-181">A generated mapping behaves like an automatic mapping.</span></span> <span data-ttu-id="a3467-182">因此，您必须手动映射所有未映射的字段。</span><span class="sxs-lookup"><span data-stu-id="a3467-182">Therefore, you must manually map any unmapped fields.</span></span>

![数据映射](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a><span data-ttu-id="a3467-184">验证您的导入或导出作业的安全性</span><span class="sxs-lookup"><span data-stu-id="a3467-184">Verify the security for your import or export job</span></span>
<span data-ttu-id="a3467-185">**数据管理**工作区的访问权限可能受到限制，因此非管理员用户可能仅可访问特定的数据作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-185">Access to the **Data management** workspace can be restricted, so that non-administrator users can access only specific data jobs.</span></span> <span data-ttu-id="a3467-186">对数据作业的访问权限暗示着对该作业的执行历史记录的完全访问权限和对暂存表的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a3467-186">Access to a data job implies full access to the execution history of that job and access to the staging tables.</span></span> <span data-ttu-id="a3467-187">因此，您必须确保在创建数据作业时采取适当的访问权限控制。</span><span class="sxs-lookup"><span data-stu-id="a3467-187">Therefore, you must make sure that appropriate access controls are in place when you create a data job.</span></span>

### <a name="secure-a-job-by-roles-and-users"></a><span data-ttu-id="a3467-188">按角色和用户保护作业安全</span><span class="sxs-lookup"><span data-stu-id="a3467-188">Secure a job by roles and users</span></span>
<span data-ttu-id="a3467-189">使用**适用的角色**菜单将作业限制到一个或多个安全角色。</span><span class="sxs-lookup"><span data-stu-id="a3467-189">Use the **Applicable roles** menu to restrict the job to one or more security roles.</span></span> <span data-ttu-id="a3467-190">仅这些角色的用户具有该作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a3467-190">Only users in those roles will have access to the job.</span></span>

<span data-ttu-id="a3467-191">您还可以将该作业限制到特定用户。</span><span class="sxs-lookup"><span data-stu-id="a3467-191">You can also restrict a job to specific users.</span></span> <span data-ttu-id="a3467-192">当您按用户而不是角色保护作业安全时，如果有多个用户分配到角色，则具有更多的控制性。</span><span class="sxs-lookup"><span data-stu-id="a3467-192">When you secure a job by users instead of roles, there is more control if multiple users are assigned to a role.</span></span>

### <a name="secure-a-job-by-legal-entity"></a><span data-ttu-id="a3467-193">通过法人保护作业安全</span><span class="sxs-lookup"><span data-stu-id="a3467-193">Secure a job by legal entity</span></span>
<span data-ttu-id="a3467-194">数据作业在性质上是全局的。</span><span class="sxs-lookup"><span data-stu-id="a3467-194">Data jobs are global in nature.</span></span> <span data-ttu-id="a3467-195">因此，如果在法人中创建和使用数据作业，该作业将在系统中的其他法人中可见。</span><span class="sxs-lookup"><span data-stu-id="a3467-195">Therefore, if a data job was created and used in a legal entity, the job will be visible in other legal entities in the system.</span></span> <span data-ttu-id="a3467-196">此默认行为可能在有些应用方案中优先。</span><span class="sxs-lookup"><span data-stu-id="a3467-196">This default behavior might be preferred in some application scenarios.</span></span> <span data-ttu-id="a3467-197">例如，使用数据实体导入发票的组织可能提供一个集中发票处理团队负责管理组织中的所有部门的发票错误。</span><span class="sxs-lookup"><span data-stu-id="a3467-197">For example, an organization that imports invoices by using data entities might provide a centralized invoice processing team that is responsible for managing invoice errors for all divisions in the organization.</span></span> <span data-ttu-id="a3467-198">在此方案中，它有助于集中发票处理团队获得所有法人的发票导入作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a3467-198">In this scenario, it’s useful for the centralized invoice processing team to have access to invoice import jobs from all legal entities.</span></span> <span data-ttu-id="a3467-199">因此，从一个法人的角度看，默认行为满足要求。</span><span class="sxs-lookup"><span data-stu-id="a3467-199">Therefore, the default behavior meets the requirement from a legal entity perspective.</span></span>

<span data-ttu-id="a3467-200">但是，组织可能希望每个法人各有一个发票处理团队。</span><span class="sxs-lookup"><span data-stu-id="a3467-200">However, an organization might want to have invoice processing teams per legal entity.</span></span> <span data-ttu-id="a3467-201">在这种情况下，一个法人中的团队应仅具有它自己的法人的发票导入作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a3467-201">In this case, a team in a legal entity should have access only to the invoice import job in its own legal entity.</span></span> <span data-ttu-id="a3467-202">为了满足此要求，您可以使用数据作业内的**适用的法人**菜单在数据作业上配置基于法人的访问权限控制。</span><span class="sxs-lookup"><span data-stu-id="a3467-202">To meet this requirement, you can configure legal entity–based access control on the data jobs by using the **Applicable legal entities** menu inside the data job.</span></span> <span data-ttu-id="a3467-203">配置完成后，用户仅可以看到他们当前分配的法人中可用的作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-203">After the configuration is done, users can see only jobs that are available in the legal entity that they are currently signed in to.</span></span> <span data-ttu-id="a3467-204">若要查看其他法人的作业，用户必须切换到该法人。</span><span class="sxs-lookup"><span data-stu-id="a3467-204">To see jobs from another legal entity, users must switch to that legal entity.</span></span>

<span data-ttu-id="a3467-205">可同时按角色、用户和法人保护作业安全。</span><span class="sxs-lookup"><span data-stu-id="a3467-205">A job can be secured by roles, users, and legal entity at the same time.</span></span>

## <a name="run-the-import-or-export-job"></a><span data-ttu-id="a3467-206">运行导入或导出作业</span><span class="sxs-lookup"><span data-stu-id="a3467-206">Run the import or export job</span></span>
<span data-ttu-id="a3467-207">在定义作业后，您可以选择**导入**或**导出**按钮运行一次作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-207">You can run a job one time by selecting the **Import** or **Export** button after you define the job.</span></span> <span data-ttu-id="a3467-208">若要设置重复执行的作业，请选择**创建重复性数据作业**。</span><span class="sxs-lookup"><span data-stu-id="a3467-208">To set up a recurring job, select **Create recurring data job**.</span></span>

## <a name="validate-that-the-job-ran-as-expected"></a><span data-ttu-id="a3467-209">验证该作业按预期运行</span><span class="sxs-lookup"><span data-stu-id="a3467-209">Validate that the job ran as expected</span></span>
<span data-ttu-id="a3467-210">作业历史记录可用于导入和导出作业的故障排除和调查。</span><span class="sxs-lookup"><span data-stu-id="a3467-210">The job history is available for troubleshooting and investigation on both import and export jobs.</span></span> <span data-ttu-id="a3467-211">历史作业运行按时间范围进行组织。</span><span class="sxs-lookup"><span data-stu-id="a3467-211">Historical job runs are organized by time ranges.</span></span>

![作业历史记录范围](./media/dixf-job-history.md.png)

<span data-ttu-id="a3467-213">每次作业运行提供以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="a3467-213">Each job run provides the following details:</span></span>

- <span data-ttu-id="a3467-214">执行详细信息</span><span class="sxs-lookup"><span data-stu-id="a3467-214">Execution details</span></span>
- <span data-ttu-id="a3467-215">执行日志</span><span class="sxs-lookup"><span data-stu-id="a3467-215">Execution log</span></span>

<span data-ttu-id="a3467-216">执行详细信息显示作业处理的每个数据实体的状态。</span><span class="sxs-lookup"><span data-stu-id="a3467-216">Execution details show the state of each data entity that the job processed.</span></span> <span data-ttu-id="a3467-217">因此，您可以迅速找到以下信息：</span><span class="sxs-lookup"><span data-stu-id="a3467-217">Therefore, you can quickly find the following information:</span></span>

- <span data-ttu-id="a3467-218">处理了哪些实体</span><span class="sxs-lookup"><span data-stu-id="a3467-218">Which entities were processed</span></span>
- <span data-ttu-id="a3467-219">对于实体，处理成功的记录数量和处理失败的记录数量</span><span class="sxs-lookup"><span data-stu-id="a3467-219">For an entity, how many records were successfully processed, and how many failed</span></span>
- <span data-ttu-id="a3467-220">每个实体的暂存记录</span><span class="sxs-lookup"><span data-stu-id="a3467-220">The staging records for each entity</span></span>

<span data-ttu-id="a3467-221">您可以将暂存数据下载到一个文件用于导出作业，或将其下载为包用于导入和导出作业。</span><span class="sxs-lookup"><span data-stu-id="a3467-221">You can download the staging data in a file for export jobs, or you can download it as a package for import and export jobs.</span></span>

<span data-ttu-id="a3467-222">您还可以从执行详细信息打开执行日志。</span><span class="sxs-lookup"><span data-stu-id="a3467-222">From the execution details, you can also open the execution log.</span></span>

## <a name="clean-up-the-staging-tables"></a><span data-ttu-id="a3467-223">清除暂存表</span><span class="sxs-lookup"><span data-stu-id="a3467-223">Clean up the staging tables</span></span>
<span data-ttu-id="a3467-224">您可以使用**数据管理**工作区中的**暂存清除**功能清除暂存表。</span><span class="sxs-lookup"><span data-stu-id="a3467-224">You can clean up staging tables by using the **Staging clean up** feature in the **Data management** workspace.</span></span> <span data-ttu-id="a3467-225">您可以使用以下选项选择从哪个暂存表删除哪些记录：</span><span class="sxs-lookup"><span data-stu-id="a3467-225">You can use the following options to select which records should be deleted from which staging table:</span></span>

- <span data-ttu-id="a3467-226">**实体** - 如果仅提供一个实体，则删除来自该实体暂存表的所有记录。</span><span class="sxs-lookup"><span data-stu-id="a3467-226">**Entity** – If only an entity is provided, all records from that entity’s staging table are deleted.</span></span> <span data-ttu-id="a3467-227">选择此选项以清除跨所有数据项目和所有作业的实体的所有数据。</span><span class="sxs-lookup"><span data-stu-id="a3467-227">Select this option to clean up all the data for the entity across all data projects and all jobs.</span></span>
- <span data-ttu-id="a3467-228">**作业 ID** - 如果仅提供一个作业 ID，则从相应的暂存表中删除选定作业中的所有实体的所有记录。</span><span class="sxs-lookup"><span data-stu-id="a3467-228">**Job ID** – If only a job ID is provided, all records for all entities in the selected job are deleted from the appropriate staging tables.</span></span>
- <span data-ttu-id="a3467-229">**数据项目** - 如果仅选择一个数据项目，则删除选定数据项目的所有实体和跨所有作业的所有记录。</span><span class="sxs-lookup"><span data-stu-id="a3467-229">**Data projects** – If only a data project is selected, all records for all entities and across all jobs for the selected data project are deleted.</span></span>

<span data-ttu-id="a3467-230">您还可以合并这些选项以进一步限制被删除的记录集。</span><span class="sxs-lookup"><span data-stu-id="a3467-230">You can also combine the options to further restrict the record set that is deleted.</span></span>

