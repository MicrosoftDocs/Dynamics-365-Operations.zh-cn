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
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: d58bab48c65bb891155af95c79738b019e5760bf
ms.contentlocale: zh-cn
ms.lasthandoff: 05/22/2018

---

# <a name="data-import-and-export-jobs"></a><span data-ttu-id="ade4d-103">数据导入和导出作业</span><span class="sxs-lookup"><span data-stu-id="ade4d-103">Data import and export jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ade4d-104">要在 Microsoft Dynamics 365 for Finance and Operations 中创建和管理数据导入和导出作业，请使用**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="ade4d-104">To create and manage data import and export jobs in Microsoft Dynamics 365 for Finance and Operations, you use the **Data management** workspace.</span></span> <span data-ttu-id="ade4d-105">默认情况下，数据导入和导出流程为目标数据库中的每个实体创建一个暂存表。</span><span class="sxs-lookup"><span data-stu-id="ade4d-105">By default, the data import and export process creates a staging table for each entity in the target database.</span></span> <span data-ttu-id="ade4d-106">通过暂存表可以在移动数据之前验证、清理或转换数据。</span><span class="sxs-lookup"><span data-stu-id="ade4d-106">Staging tables let you verify, clean up, or convert data before you move it.</span></span>

> [!NOTE]
> <span data-ttu-id="ade4d-107">此主题假定您熟悉[数据实体](data-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="ade4d-107">This topic assumes that you are familiar with [data entities](data-entities.md).</span></span>

## <a name="data-importexport-process"></a><span data-ttu-id="ade4d-108">数据导入/导出流程</span><span class="sxs-lookup"><span data-stu-id="ade4d-108">Data import/export process</span></span>
<span data-ttu-id="ade4d-109">以下是导入或导出数据的步骤。</span><span class="sxs-lookup"><span data-stu-id="ade4d-109">Here are the steps to import or export data.</span></span>

1. <span data-ttu-id="ade4d-110">在完成以下任务后创建导入或导出作业：</span><span class="sxs-lookup"><span data-stu-id="ade4d-110">Create an import or export job where you complete the following tasks:</span></span>

    - <span data-ttu-id="ade4d-111">定义项目类别。</span><span class="sxs-lookup"><span data-stu-id="ade4d-111">Define the project category.</span></span>
    - <span data-ttu-id="ade4d-112">确定要导入或导出的实体。</span><span class="sxs-lookup"><span data-stu-id="ade4d-112">Identify the entities to import or export.</span></span>
    - <span data-ttu-id="ade4d-113">设置作业的数据格式。</span><span class="sxs-lookup"><span data-stu-id="ade4d-113">Set the data format for the job.</span></span>
    - <span data-ttu-id="ade4d-114">给实体排序，以便以合理的顺序在逻辑组中处理这些实体。</span><span class="sxs-lookup"><span data-stu-id="ade4d-114">Sequence the entities, so that they are processed in logical groups and in an order that makes sense.</span></span>
    - <span data-ttu-id="ade4d-115">确定是否使用暂存表。</span><span class="sxs-lookup"><span data-stu-id="ade4d-115">Determine whether to use staging tables.</span></span>

2. <span data-ttu-id="ade4d-116">验证源数据和目标数据是否正确映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-116">Validate that the source data and target data are mapped correctly.</span></span>
3. <span data-ttu-id="ade4d-117">验证您的导入或导出作业的安全性。</span><span class="sxs-lookup"><span data-stu-id="ade4d-117">Verify the security for your import or export job.</span></span>
4. <span data-ttu-id="ade4d-118">运行导入或导出作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-118">Run the import or export job.</span></span>
5. <span data-ttu-id="ade4d-119">查看作业历史纪录，验证作业是否按预期运行。</span><span class="sxs-lookup"><span data-stu-id="ade4d-119">Validate that the job ran as expected by reviewing the job history.</span></span>
6. <span data-ttu-id="ade4d-120">清除暂存表。</span><span class="sxs-lookup"><span data-stu-id="ade4d-120">Clean up the staging tables.</span></span>

<span data-ttu-id="ade4d-121">本主题的其余部分提供有关流程的每个步骤的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ade4d-121">The remaining sections of this topic provide more details about each step of the process.</span></span>

> [!NOTE]
> <span data-ttu-id="ade4d-122">要刷新“数据导入/导出”窗体以查看最新进度，请使用窗体刷新图标。</span><span class="sxs-lookup"><span data-stu-id="ade4d-122">In order to refresh the Data import/export form to see the latest progress, use the form refresh icon.</span></span> <span data-ttu-id="ade4d-123">不建议执行浏览器级刷新，因为这将中断所有未批量运行的导入/导出作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-123">Browser level refresh is not recommended because it will interrupt any import/export jobs that are not run in batch.</span></span>

## <a name="create-an-import-or-export-job"></a><span data-ttu-id="ade4d-124">创建导入或导出作业</span><span class="sxs-lookup"><span data-stu-id="ade4d-124">Create an import or export job</span></span>
<span data-ttu-id="ade4d-125">可以一次性运行或分多次运行数据导入或导出作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-125">A data import or export job can be run one time or many times.</span></span>

### <a name="define-the-project-category"></a><span data-ttu-id="ade4d-126">定义项目类别</span><span class="sxs-lookup"><span data-stu-id="ade4d-126">Define the project category</span></span>
<span data-ttu-id="ade4d-127">我们建议您花时间为导入或导出作业选择合适的项目类别。</span><span class="sxs-lookup"><span data-stu-id="ade4d-127">We recommend that you take the time to select an appropriate project category for your import or export job.</span></span> <span data-ttu-id="ade4d-128">项目类别有助于管理相关作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-128">Project categories can help you manage related jobs.</span></span>

### <a name="identify-the-entities-to-import-or-export"></a><span data-ttu-id="ade4d-129">确定要导入或导出的实体</span><span class="sxs-lookup"><span data-stu-id="ade4d-129">Identify the entities to import or export</span></span>
<span data-ttu-id="ade4d-130">您可以将特定实体添加到导入或导出作业或选择一个要应用的模板。</span><span class="sxs-lookup"><span data-stu-id="ade4d-130">You can add specific entities to an import or export job or select a template to apply.</span></span> <span data-ttu-id="ade4d-131">模板使用一个实体列表填充一个作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-131">Templates fill a job with a list of entities.</span></span> <span data-ttu-id="ade4d-132">给作业命名并保存作业后，**应用模板**选项可用。</span><span class="sxs-lookup"><span data-stu-id="ade4d-132">The **Apply template** option is available after you give the job a name and save the job.</span></span>

### <a name="set-the-data-format-for-the-job"></a><span data-ttu-id="ade4d-133">设置作业的数据格式</span><span class="sxs-lookup"><span data-stu-id="ade4d-133">Set the data format for the job</span></span>
<span data-ttu-id="ade4d-134">选择一个实体后，必须选择要导出或导入的数据的格式。</span><span class="sxs-lookup"><span data-stu-id="ade4d-134">When you select an entity, you must select the format of the data that will be exported or imported.</span></span> <span data-ttu-id="ade4d-135">使用**数据源设置**磁贴定义格式。</span><span class="sxs-lookup"><span data-stu-id="ade4d-135">You define formats by using the **Data sources setup** tile.</span></span> <span data-ttu-id="ade4d-136">源数据格式是**类型**、**文件格式**、**行分隔符**和**列分隔符**的组合。</span><span class="sxs-lookup"><span data-stu-id="ade4d-136">A source data format is a combination of **Type**, **File format**, **Row delimiter** and **Column delimiter**.</span></span> <span data-ttu-id="ade4d-137">还有其他属性，但以上属性则是需要了解的关键属性。</span><span class="sxs-lookup"><span data-stu-id="ade4d-137">There are also other attributes, but these are the key ones to understand.</span></span> <span data-ttu-id="ade4d-138">下表列出了有效组合。</span><span class="sxs-lookup"><span data-stu-id="ade4d-138">The following table lists the valid combinations.</span></span>

| <span data-ttu-id="ade4d-139">**文件格式**</span><span class="sxs-lookup"><span data-stu-id="ade4d-139">**File Format**</span></span>        | <span data-ttu-id="ade4d-140">**行/列分隔符**</span><span class="sxs-lookup"><span data-stu-id="ade4d-140">**Row/Column delimiter**</span></span>                   | <span data-ttu-id="ade4d-141">**XML 样式**</span><span class="sxs-lookup"><span data-stu-id="ade4d-141">**XML Style**</span></span>             |
|------------------------|--------------------------------------------|---------------------------|
| <span data-ttu-id="ade4d-142">Excel</span><span class="sxs-lookup"><span data-stu-id="ade4d-142">Excel</span></span>                  | <span data-ttu-id="ade4d-143">Excel</span><span class="sxs-lookup"><span data-stu-id="ade4d-143">Excel</span></span>                                      | <span data-ttu-id="ade4d-144">\-NA-</span><span class="sxs-lookup"><span data-stu-id="ade4d-144">\-NA-</span></span>                     |
| <span data-ttu-id="ade4d-145">XML</span><span class="sxs-lookup"><span data-stu-id="ade4d-145">XML</span></span>                    | <span data-ttu-id="ade4d-146">\-NA-</span><span class="sxs-lookup"><span data-stu-id="ade4d-146">\-NA-</span></span>                                      | <span data-ttu-id="ade4d-147">XML 元素 XML 属性</span><span class="sxs-lookup"><span data-stu-id="ade4d-147">XML-Element XML-Attribute</span></span> |
| <span data-ttu-id="ade4d-148">分隔，固定宽度</span><span class="sxs-lookup"><span data-stu-id="ade4d-148">Delimited, fixed width</span></span> | <span data-ttu-id="ade4d-149">逗号、分号、制表符、竖线、冒号</span><span class="sxs-lookup"><span data-stu-id="ade4d-149">Comma, semicolon, tab, vertical bar, colon</span></span> | <span data-ttu-id="ade4d-150">\-NA-</span><span class="sxs-lookup"><span data-stu-id="ade4d-150">\-NA-</span></span>                     |



### <a name="sequence-the-entities"></a><span data-ttu-id="ade4d-151">给实体排序</span><span class="sxs-lookup"><span data-stu-id="ade4d-151">Sequence the entities</span></span>
<span data-ttu-id="ade4d-152">实体可以在数据模板或导入和导出作业中排序。</span><span class="sxs-lookup"><span data-stu-id="ade4d-152">Entities can be sequenced in a data template, or in import and export jobs.</span></span> <span data-ttu-id="ade4d-153">运行的作业包含多个数据实体时，必须确保数据实体的序列正确。</span><span class="sxs-lookup"><span data-stu-id="ade4d-153">When you run a job that contains more than one data entity, you must make sure that the data entities are correctly sequenced.</span></span> <span data-ttu-id="ade4d-154">给实体排序的主要目的是为了解决实体中的任何功能依赖项。</span><span class="sxs-lookup"><span data-stu-id="ade4d-154">You sequence entities primarily so that you can address any functional dependencies among entities.</span></span> <span data-ttu-id="ade4d-155">如果实体不具有任何功能依赖项，可以计划并行导入或导出。</span><span class="sxs-lookup"><span data-stu-id="ade4d-155">If entities don’t have any functional dependencies, they can be scheduled for parallel import or export.</span></span>

#### <a name="execution-units-levels-and-sequences"></a><span data-ttu-id="ade4d-156">执行单元、级别和序列</span><span class="sxs-lookup"><span data-stu-id="ade4d-156">Execution units, levels, and sequences</span></span>
<span data-ttu-id="ade4d-157">执行单元、执行单元中的级别以及实体序列有助于控制导出或导入数据的顺序。</span><span class="sxs-lookup"><span data-stu-id="ade4d-157">The execution unit, level in the execution unit, and sequence of an entity help control the order that the data is exported or imported in.</span></span>

- <span data-ttu-id="ade4d-158">不同执行单元中的实体并行处理。</span><span class="sxs-lookup"><span data-stu-id="ade4d-158">Entities in different execution units are processed in parallel.</span></span>
- <span data-ttu-id="ade4d-159">在每个执行单元中，具有相同级别的实体并行处理。</span><span class="sxs-lookup"><span data-stu-id="ade4d-159">In each execution unit, entities are processed in parallel if they have the same level.</span></span>
- <span data-ttu-id="ade4d-160">在每个级别中，根据实体在该级别中的序列号处理实体。</span><span class="sxs-lookup"><span data-stu-id="ade4d-160">In each level, entities are processed according to their sequence number in that level.</span></span>
- <span data-ttu-id="ade4d-161">处理完一个级别后，再处理下一个级别。</span><span class="sxs-lookup"><span data-stu-id="ade4d-161">After one level has been processed, the next level is processed.</span></span>

#### <a name="resequencing"></a><span data-ttu-id="ade4d-162">重新排序</span><span class="sxs-lookup"><span data-stu-id="ade4d-162">Resequencing</span></span>
<span data-ttu-id="ade4d-163">在以下情形中，您可能想要对实体重新排序：</span><span class="sxs-lookup"><span data-stu-id="ade4d-163">You might want to resequence your entities in the following situations:</span></span>

- <span data-ttu-id="ade4d-164">如果只有一个数据作业用于您的所有更改，可以使用重新排序选项来优化整个作业的执行时间。</span><span class="sxs-lookup"><span data-stu-id="ade4d-164">If only one data job is used for all your changes, you can use resequencing options to optimize the execution time for the full job.</span></span> <span data-ttu-id="ade4d-165">在这些情况下，您可以使用执行单元表示模块，用级别表示模块中的功能区域，用序列表示实体。</span><span class="sxs-lookup"><span data-stu-id="ade4d-165">In these cases, you can use the execution unit to represent the module, the level to represent the feature area in the module, and the sequence to represent the entity.</span></span> <span data-ttu-id="ade4d-166">使用此方法可以并行处理不同模块，但也仍然能在一个模块中按顺序处理。</span><span class="sxs-lookup"><span data-stu-id="ade4d-166">By using this approach, you can work across modules in parallel, but you can still work in sequence in a module.</span></span> <span data-ttu-id="ade4d-167">为了帮助保证成功完成并行操作，必须考虑所有依赖项。</span><span class="sxs-lookup"><span data-stu-id="ade4d-167">To help guarantee that parallel operations succeed, you must consider all dependencies.</span></span>
- <span data-ttu-id="ade4d-168">如果使用多个数据作业（例如，一个模块使用一个作业），可以使用排序来影响实体的级别和顺序，以获得最佳执行。</span><span class="sxs-lookup"><span data-stu-id="ade4d-168">If multiple data jobs are used (for example, one job for each module), you can use sequencing to affect the level and sequence of entities for optimal execution.</span></span>
- <span data-ttu-id="ade4d-169">如果没有任何依赖项，可以在不同执行单元对实体排序，以最大程度地进行优化。</span><span class="sxs-lookup"><span data-stu-id="ade4d-169">If there are no dependencies at all, you can sequence entities at different execution units for maximum optimization.</span></span>

<span data-ttu-id="ade4d-170">选择多个实体时，**重新排序**菜单可用。</span><span class="sxs-lookup"><span data-stu-id="ade4d-170">The **Resequencing** menu is available when multiple entities are selected.</span></span> <span data-ttu-id="ade4d-171">可以基于执行单元、级别或顺序选项重新排序。</span><span class="sxs-lookup"><span data-stu-id="ade4d-171">You can resequence based on execution unit, level, or sequence options.</span></span> <span data-ttu-id="ade4d-172">可以设定增量，以对选定的实体重新排序。</span><span class="sxs-lookup"><span data-stu-id="ade4d-172">You can set an increment to resequence the entities that have been selected.</span></span> <span data-ttu-id="ade4d-173">为每个实体选择的单元、级别和/或序列号按指定增量进行更新。</span><span class="sxs-lookup"><span data-stu-id="ade4d-173">The unit, level, and/or sequence number that is selected for each entity is updated by the specified increment.</span></span>

#### <a name="sorting"></a><span data-ttu-id="ade4d-174">排序</span><span class="sxs-lookup"><span data-stu-id="ade4d-174">Sorting</span></span>
<span data-ttu-id="ade4d-175">用户可以使用**排序依据**选项按顺序查看实体列表。</span><span class="sxs-lookup"><span data-stu-id="ade4d-175">Use can use the **Sort by** option to view the entity list in sequential order.</span></span>

### <a name="truncating"></a><span data-ttu-id="ade4d-176">截断</span><span class="sxs-lookup"><span data-stu-id="ade4d-176">Truncating</span></span>
<span data-ttu-id="ade4d-177">对于导入项目，可在导入前选择截断实体中的记录。</span><span class="sxs-lookup"><span data-stu-id="ade4d-177">For import projects, you can choose to truncate records in the entities prior to import.</span></span> <span data-ttu-id="ade4d-178">如果必须将记录导入一套干净的表中，这很有用。</span><span class="sxs-lookup"><span data-stu-id="ade4d-178">This is useful if your records must be imported into a clean set of tables.</span></span> <span data-ttu-id="ade4d-179">默认情况下，此设置已关闭。</span><span class="sxs-lookup"><span data-stu-id="ade4d-179">This setting is off by default.</span></span>

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a><span data-ttu-id="ade4d-180">验证源数据和目标数据是否正确映射</span><span class="sxs-lookup"><span data-stu-id="ade4d-180">Validate that the source data and target data are mapped correctly</span></span>
<span data-ttu-id="ade4d-181">映射是同时适用于导入和导出作业的一项功能。</span><span class="sxs-lookup"><span data-stu-id="ade4d-181">Mapping is a function that applies to both import and export jobs.</span></span>

- <span data-ttu-id="ade4d-182">在导入作业情况下，映射描述源文件中的哪些列成为暂存表中的列。</span><span class="sxs-lookup"><span data-stu-id="ade4d-182">In the context of an import job, mapping describes which columns in the source file become the columns in the staging table.</span></span> <span data-ttu-id="ade4d-183">因此，系统可以确定源文件中的哪些列数据必须复制到暂存表中的哪一列。</span><span class="sxs-lookup"><span data-stu-id="ade4d-183">Therefore, the system can determine which column data in the source file must be copied into which column of the staging table.</span></span>
- <span data-ttu-id="ade4d-184">在导出作业情况下，映射描述暂存表（即源）中的哪些列成为目标文件中的列。</span><span class="sxs-lookup"><span data-stu-id="ade4d-184">In the context of an export job, mapping describes which columns of the staging table (that is, the source) become the columns in the target file.</span></span>

<span data-ttu-id="ade4d-185">如果暂存表和文件中的列名称匹配，则系统自动基于名称建立映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-185">If the column names in the staging table and the file match, the system automatically establishes the mapping, based on the names.</span></span> <span data-ttu-id="ade4d-186">但是，如果名称有差异，则不会自动映射列。</span><span class="sxs-lookup"><span data-stu-id="ade4d-186">However, if the names differ, columns aren’t mapped automatically.</span></span> <span data-ttu-id="ade4d-187">在这些情况下，必须在数据作业中的实体上选择**查看映射**选项，以完成映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-187">In these cases, you must complete the mapping by selecting the **View map** option on the entity in the data job.</span></span>

<span data-ttu-id="ade4d-188">有两个映射视图：**映射可视化**，即默认视图，以及**映射详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ade4d-188">There are two mapping views: **Mapping visualization**, which is the default view, and **Mapping details**.</span></span> <span data-ttu-id="ade4d-189">红色星号 (\*) 标识实体中的任何必填字段。</span><span class="sxs-lookup"><span data-stu-id="ade4d-189">A red asterisk (\*) identifies any required fields in the entity.</span></span> <span data-ttu-id="ade4d-190">必须映射这些字段后才能处理实体。</span><span class="sxs-lookup"><span data-stu-id="ade4d-190">These fields must be mapped before you can work with the entity.</span></span> <span data-ttu-id="ade4d-191">处理实体时，可以按需要取消其他字段的映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-191">You can unmap other fields as you require when you work with the entity.</span></span> <span data-ttu-id="ade4d-192">要取消字段映射，选择**实体**列或**源**列中的字段，然后选择**删除选择**。</span><span class="sxs-lookup"><span data-stu-id="ade4d-192">To unmap a field, select the field in either the **Entity** column or the **Source** column, and then select **Delete selection**.</span></span> <span data-ttu-id="ade4d-193">选择**保存**以保存更改，然后关闭页面以返回项目。</span><span class="sxs-lookup"><span data-stu-id="ade4d-193">Select **Save** to save your changes, and then close the page to return to the project.</span></span> <span data-ttu-id="ade4d-194">在导入后，您可以使用相同流程编辑来自源的字段映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-194">You can use the same process to edit the field mapping from source to staging after you import.</span></span>

<span data-ttu-id="ade4d-195">通过选择**生成源映射**可以在页面上生成映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-195">You can generate a mapping on the page by selecting **Generate source mapping**.</span></span> <span data-ttu-id="ade4d-196">生成的映射表现地类似于自动映射。</span><span class="sxs-lookup"><span data-stu-id="ade4d-196">A generated mapping behaves like an automatic mapping.</span></span> <span data-ttu-id="ade4d-197">因此，您必须手动映射所有未映射的字段。</span><span class="sxs-lookup"><span data-stu-id="ade4d-197">Therefore, you must manually map any unmapped fields.</span></span>

![数据映射](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a><span data-ttu-id="ade4d-199">验证您的导入或导出作业的安全性</span><span class="sxs-lookup"><span data-stu-id="ade4d-199">Verify the security for your import or export job</span></span>
<span data-ttu-id="ade4d-200">**数据管理**工作区的访问权限可能受到限制，因此非管理员用户可能仅可访问特定的数据作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-200">Access to the **Data management** workspace can be restricted, so that non-administrator users can access only specific data jobs.</span></span> <span data-ttu-id="ade4d-201">对数据作业的访问权限暗示着对该作业的执行历史记录的完全访问权限和对暂存表的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ade4d-201">Access to a data job implies full access to the execution history of that job and access to the staging tables.</span></span> <span data-ttu-id="ade4d-202">因此，您必须确保在创建数据作业时采取适当的访问权限控制。</span><span class="sxs-lookup"><span data-stu-id="ade4d-202">Therefore, you must make sure that appropriate access controls are in place when you create a data job.</span></span>

### <a name="secure-a-job-by-roles-and-users"></a><span data-ttu-id="ade4d-203">按角色和用户保护作业安全</span><span class="sxs-lookup"><span data-stu-id="ade4d-203">Secure a job by roles and users</span></span>
<span data-ttu-id="ade4d-204">使用**适用的角色**菜单将作业限制到一个或多个安全角色。</span><span class="sxs-lookup"><span data-stu-id="ade4d-204">Use the **Applicable roles** menu to restrict the job to one or more security roles.</span></span> <span data-ttu-id="ade4d-205">仅这些角色的用户具有该作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ade4d-205">Only users in those roles will have access to the job.</span></span>

<span data-ttu-id="ade4d-206">您还可以将该作业限制到特定用户。</span><span class="sxs-lookup"><span data-stu-id="ade4d-206">You can also restrict a job to specific users.</span></span> <span data-ttu-id="ade4d-207">当您按用户而不是角色保护作业安全时，如果有多个用户分配到角色，则具有更多的控制性。</span><span class="sxs-lookup"><span data-stu-id="ade4d-207">When you secure a job by users instead of roles, there is more control if multiple users are assigned to a role.</span></span>

### <a name="secure-a-job-by-legal-entity"></a><span data-ttu-id="ade4d-208">通过法人保护作业安全</span><span class="sxs-lookup"><span data-stu-id="ade4d-208">Secure a job by legal entity</span></span>
<span data-ttu-id="ade4d-209">数据作业在性质上是全局的。</span><span class="sxs-lookup"><span data-stu-id="ade4d-209">Data jobs are global in nature.</span></span> <span data-ttu-id="ade4d-210">因此，如果在法人中创建和使用数据作业，该作业将在系统中的其他法人中可见。</span><span class="sxs-lookup"><span data-stu-id="ade4d-210">Therefore, if a data job was created and used in a legal entity, the job will be visible in other legal entities in the system.</span></span> <span data-ttu-id="ade4d-211">此默认行为可能在有些应用方案中优先。</span><span class="sxs-lookup"><span data-stu-id="ade4d-211">This default behavior might be preferred in some application scenarios.</span></span> <span data-ttu-id="ade4d-212">例如，使用数据实体导入发票的组织可能提供一个集中发票处理团队负责管理组织中的所有部门的发票错误。</span><span class="sxs-lookup"><span data-stu-id="ade4d-212">For example, an organization that imports invoices by using data entities might provide a centralized invoice processing team that is responsible for managing invoice errors for all divisions in the organization.</span></span> <span data-ttu-id="ade4d-213">在此方案中，它有助于集中发票处理团队获得所有法人的发票导入作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ade4d-213">In this scenario, it’s useful for the centralized invoice processing team to have access to invoice import jobs from all legal entities.</span></span> <span data-ttu-id="ade4d-214">因此，从一个法人的角度看，默认行为满足要求。</span><span class="sxs-lookup"><span data-stu-id="ade4d-214">Therefore, the default behavior meets the requirement from a legal entity perspective.</span></span>

<span data-ttu-id="ade4d-215">但是，组织可能希望每个法人各有一个发票处理团队。</span><span class="sxs-lookup"><span data-stu-id="ade4d-215">However, an organization might want to have invoice processing teams per legal entity.</span></span> <span data-ttu-id="ade4d-216">在这种情况下，一个法人中的团队应仅具有它自己的法人的发票导入作业的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ade4d-216">In this case, a team in a legal entity should have access only to the invoice import job in its own legal entity.</span></span> <span data-ttu-id="ade4d-217">为了满足此要求，您可以使用数据作业内的**适用的法人**菜单在数据作业上配置基于法人的访问权限控制。</span><span class="sxs-lookup"><span data-stu-id="ade4d-217">To meet this requirement, you can configure legal entity–based access control on the data jobs by using the **Applicable legal entities** menu inside the data job.</span></span> <span data-ttu-id="ade4d-218">配置完成后，用户仅可以看到他们当前分配的法人中可用的作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-218">After the configuration is done, users can see only jobs that are available in the legal entity that they are currently signed in to.</span></span> <span data-ttu-id="ade4d-219">若要查看其他法人的作业，用户必须切换到该法人。</span><span class="sxs-lookup"><span data-stu-id="ade4d-219">To see jobs from another legal entity, users must switch to that legal entity.</span></span>

<span data-ttu-id="ade4d-220">可同时按角色、用户和法人保护作业安全。</span><span class="sxs-lookup"><span data-stu-id="ade4d-220">A job can be secured by roles, users, and legal entity at the same time.</span></span>

## <a name="run-the-import-or-export-job"></a><span data-ttu-id="ade4d-221">运行导入或导出作业</span><span class="sxs-lookup"><span data-stu-id="ade4d-221">Run the import or export job</span></span>
<span data-ttu-id="ade4d-222">在定义作业后，您可以选择**导入**或**导出**按钮运行一次作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-222">You can run a job one time by selecting the **Import** or **Export** button after you define the job.</span></span> <span data-ttu-id="ade4d-223">若要设置重复执行的作业，请选择**创建重复性数据作业**。</span><span class="sxs-lookup"><span data-stu-id="ade4d-223">To set up a recurring job, select **Create recurring data job**.</span></span>

## <a name="validate-that-the-job-ran-as-expected"></a><span data-ttu-id="ade4d-224">验证该作业按预期运行</span><span class="sxs-lookup"><span data-stu-id="ade4d-224">Validate that the job ran as expected</span></span>
<span data-ttu-id="ade4d-225">作业历史记录可用于导入和导出作业的故障排除和调查。</span><span class="sxs-lookup"><span data-stu-id="ade4d-225">The job history is available for troubleshooting and investigation on both import and export jobs.</span></span> <span data-ttu-id="ade4d-226">历史作业运行按时间范围进行组织。</span><span class="sxs-lookup"><span data-stu-id="ade4d-226">Historical job runs are organized by time ranges.</span></span>

![作业历史记录范围](./media/dixf-job-history.md.png)

<span data-ttu-id="ade4d-228">每次作业运行提供以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="ade4d-228">Each job run provides the following details:</span></span>

- <span data-ttu-id="ade4d-229">执行详细信息</span><span class="sxs-lookup"><span data-stu-id="ade4d-229">Execution details</span></span>
- <span data-ttu-id="ade4d-230">执行日志</span><span class="sxs-lookup"><span data-stu-id="ade4d-230">Execution log</span></span>

<span data-ttu-id="ade4d-231">执行详细信息显示作业处理的每个数据实体的状态。</span><span class="sxs-lookup"><span data-stu-id="ade4d-231">Execution details show the state of each data entity that the job processed.</span></span> <span data-ttu-id="ade4d-232">因此，您可以迅速找到以下信息：</span><span class="sxs-lookup"><span data-stu-id="ade4d-232">Therefore, you can quickly find the following information:</span></span>

- <span data-ttu-id="ade4d-233">处理了哪些实体</span><span class="sxs-lookup"><span data-stu-id="ade4d-233">Which entities were processed</span></span>
- <span data-ttu-id="ade4d-234">对于实体，处理成功的记录数量和处理失败的记录数量</span><span class="sxs-lookup"><span data-stu-id="ade4d-234">For an entity, how many records were successfully processed, and how many failed</span></span>
- <span data-ttu-id="ade4d-235">每个实体的暂存记录</span><span class="sxs-lookup"><span data-stu-id="ade4d-235">The staging records for each entity</span></span>

<span data-ttu-id="ade4d-236">您可以将暂存数据下载到一个文件用于导出作业，或将其下载为包用于导入和导出作业。</span><span class="sxs-lookup"><span data-stu-id="ade4d-236">You can download the staging data in a file for export jobs, or you can download it as a package for import and export jobs.</span></span>

<span data-ttu-id="ade4d-237">您还可以从执行详细信息打开执行日志。</span><span class="sxs-lookup"><span data-stu-id="ade4d-237">From the execution details, you can also open the execution log.</span></span>

## <a name="clean-up-the-staging-tables"></a><span data-ttu-id="ade4d-238">清除暂存表</span><span class="sxs-lookup"><span data-stu-id="ade4d-238">Clean up the staging tables</span></span>
<span data-ttu-id="ade4d-239">您可以使用**数据管理**工作区中的**暂存清除**功能清除暂存表。</span><span class="sxs-lookup"><span data-stu-id="ade4d-239">You can clean up staging tables by using the **Staging clean up** feature in the **Data management** workspace.</span></span> <span data-ttu-id="ade4d-240">您可以使用以下选项选择从哪个暂存表删除哪些记录：</span><span class="sxs-lookup"><span data-stu-id="ade4d-240">You can use the following options to select which records should be deleted from which staging table:</span></span>

- <span data-ttu-id="ade4d-241">**实体** - 如果仅提供一个实体，则删除来自该实体暂存表的所有记录。</span><span class="sxs-lookup"><span data-stu-id="ade4d-241">**Entity** – If only an entity is provided, all records from that entity’s staging table are deleted.</span></span> <span data-ttu-id="ade4d-242">选择此选项以清除跨所有数据项目和所有作业的实体的所有数据。</span><span class="sxs-lookup"><span data-stu-id="ade4d-242">Select this option to clean up all the data for the entity across all data projects and all jobs.</span></span>
- <span data-ttu-id="ade4d-243">**作业 ID** - 如果仅提供一个作业 ID，则从相应的暂存表中删除选定作业中的所有实体的所有记录。</span><span class="sxs-lookup"><span data-stu-id="ade4d-243">**Job ID** – If only a job ID is provided, all records for all entities in the selected job are deleted from the appropriate staging tables.</span></span>
- <span data-ttu-id="ade4d-244">**数据项目** - 如果仅选择一个数据项目，则删除选定数据项目的所有实体和跨所有作业的所有记录。</span><span class="sxs-lookup"><span data-stu-id="ade4d-244">**Data projects** – If only a data project is selected, all records for all entities and across all jobs for the selected data project are deleted.</span></span>

<span data-ttu-id="ade4d-245">您还可以合并这些选项以进一步限制被删除的记录集。</span><span class="sxs-lookup"><span data-stu-id="ade4d-245">You can also combine the options to further restrict the record set that is deleted.</span></span>

