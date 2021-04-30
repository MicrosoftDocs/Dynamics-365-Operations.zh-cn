---
title: 优化 BYOD 计划批处理作业
description: 本主题说明在 Microsoft Dynamics 365 Human Resources 中使用“提供您自己的数据库 (BYOD)”功能时如何优化性能。
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: a63ff89a6fcbffc57eff14f310a080a35521ef34
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890068"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a><span data-ttu-id="326ca-103">优化 BYOD 计划批处理作业</span><span class="sxs-lookup"><span data-stu-id="326ca-103">Optimize BYOD scheduled batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="326ca-104">本主题说明在使用“提供您自己的数据库 (BYOD)”功能时如何优化性能。</span><span class="sxs-lookup"><span data-stu-id="326ca-104">This topic explains how to optimize performance when you're using the bring your own database (BYOD) feature.</span></span> <span data-ttu-id="326ca-105">有关 BYOD 的详细信息，请参阅[提供您自己的数据库 (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="326ca-105">For more information about BYOD, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

## <a name="performance-considerations-for-data-export"></a><span data-ttu-id="326ca-106">数据导出的性能注意事项</span><span class="sxs-lookup"><span data-stu-id="326ca-106">Performance considerations for data export</span></span>

<span data-ttu-id="326ca-107">实体发布到目标数据库后，可以使用 **数据管理** 工作区中的导出功能来移动数据。</span><span class="sxs-lookup"><span data-stu-id="326ca-107">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="326ca-108">导出功能使您可以定义包含一个或多个实体的数据移动作业。</span><span class="sxs-lookup"><span data-stu-id="326ca-108">The Export function lets you define a Data movement job that contains one or more entities.</span></span> <span data-ttu-id="326ca-109">有关数据导出的详细信息，请参阅[数据导入和导出作业概述](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="326ca-109">For more information about data export, see [Data import and export jobs overview](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="326ca-110">您可以使用 **导出** 页面将数据导出为不同的目标数据格式，如逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="326ca-110">You can use the **Export** page to export data into different target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="326ca-111">此页面还支持将 SQL 数据库作为另一个目标。</span><span class="sxs-lookup"><span data-stu-id="326ca-111">This page also supports SQL databases as another destination.</span></span>

<span data-ttu-id="326ca-112">您可以创建一个具有多个实体的数据项目，然后使用批处理作业来计划该数据项目的运行。</span><span class="sxs-lookup"><span data-stu-id="326ca-112">You can create a data project that has multiple entities and use a batch job to schedule that data project to run.</span></span> <span data-ttu-id="326ca-113">如果选择 **批量导出** 选项，您可以将数据导出作业计划为定期运行。</span><span class="sxs-lookup"><span data-stu-id="326ca-113">If you select the **Export in batch** option, you can schedule the data export job to run periodically.</span></span>

<span data-ttu-id="326ca-114">为了帮助保持 BYOD 导出的整体可靠性，在向导出项目添加多个实体时必须小心。</span><span class="sxs-lookup"><span data-stu-id="326ca-114">To help preserve the overall reliability of the BYOD export, you must be careful when you add multiple entities to an export project.</span></span> <span data-ttu-id="326ca-115">确定要添加到同一项目的实体数时，请考虑以下参数：</span><span class="sxs-lookup"><span data-stu-id="326ca-115">When you're determining the number of entities to add to the same project, consider the following parameters:</span></span>

- <span data-ttu-id="326ca-116">实体的复杂性</span><span class="sxs-lookup"><span data-stu-id="326ca-116">The complexity of the entities</span></span>
- <span data-ttu-id="326ca-117">每个实体的预期数据量</span><span class="sxs-lookup"><span data-stu-id="326ca-117">The expected data volume per entity</span></span>
- <span data-ttu-id="326ca-118">完成作业级别的导出所需的总时间</span><span class="sxs-lookup"><span data-stu-id="326ca-118">The overall time that will be required to complete the export at the job level</span></span>

<span data-ttu-id="326ca-119">为了获得最佳性能，请避免将数百个实体添加到一个项目中。</span><span class="sxs-lookup"><span data-stu-id="326ca-119">For the best performance, avoid adding hundreds of entities to a single project.</span></span> <span data-ttu-id="326ca-120">我们建议您创建多个作业，每个作业包含较少的实体。</span><span class="sxs-lookup"><span data-stu-id="326ca-120">We recommend that you create multiple jobs, each of which contains fewer entities.</span></span>

## <a name="scheduling-byod-batch-jobs"></a><span data-ttu-id="326ca-121">计划 BYOD 批处理作业</span><span class="sxs-lookup"><span data-stu-id="326ca-121">Scheduling BYOD batch jobs</span></span>

<span data-ttu-id="326ca-122">为帮助减少对 Microsoft Dynamics 365 Human Resources 用户的影响，请在晚上或下班后运行 BYOD 批处理作业。</span><span class="sxs-lookup"><span data-stu-id="326ca-122">To help reduce the impact on users of Microsoft Dynamics 365 Human Resources, run BYOD batch jobs at night or after hours.</span></span> <span data-ttu-id="326ca-123">务必检查定期批处理作业的时区。</span><span class="sxs-lookup"><span data-stu-id="326ca-123">Be sure to check the time zone for recurring batch jobs.</span></span> <span data-ttu-id="326ca-124">某些批处理作业可能使用太平洋标准时间 (PST)。</span><span class="sxs-lookup"><span data-stu-id="326ca-124">Some batch jobs might use Pacific Standard Time (PST).</span></span>

<span data-ttu-id="326ca-125">为帮助避免性能问题，在为 BYOD 批处理作业配置计划频率时，请考虑以下因素：</span><span class="sxs-lookup"><span data-stu-id="326ca-125">To help avoid performance issues, consider the following factors when you configure the scheduling frequency for BYOD batch jobs:</span></span>

- <span data-ttu-id="326ca-126">完成每个批处理作业所需的时间</span><span class="sxs-lookup"><span data-stu-id="326ca-126">The time that is required to complete each batch job</span></span>
- <span data-ttu-id="326ca-127">BYOD 中数据的业务需求</span><span class="sxs-lookup"><span data-stu-id="326ca-127">The business need for the data in BYOD</span></span>

<span data-ttu-id="326ca-128">将每个批处理作业的频率设置为一个可以确保该作业可以在下一个计划的运行时间之前正常完成的值。</span><span class="sxs-lookup"><span data-stu-id="326ca-128">Set the frequency for each batch job to a value that ensures that the job can be completed well before its next scheduled run time.</span></span> <span data-ttu-id="326ca-129">避免并行运行多个作业，因为这种方法会对 Human Resources 的性能产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="326ca-129">Avoid running multiple jobs in parallel, because this approach can negatively affect the performance of Human Resources.</span></span>

<span data-ttu-id="326ca-130">为了获得最佳性能，请始终使用 **导出** 页面上的 **批量导出** 选项来计划 BYOD 批处理作业。</span><span class="sxs-lookup"><span data-stu-id="326ca-130">For the best performance, always use the **Export in batch** option on the **Export** page to schedule BYOD batch jobs.</span></span> <span data-ttu-id="326ca-131">避免通过 **管理 \> 管理定期数据作业** 计划定期导出。</span><span class="sxs-lookup"><span data-stu-id="326ca-131">Avoid scheduling recurring exports at **Manage \> Manage recurring data jobs**.</span></span>

## <a name="incremental-export"></a><span data-ttu-id="326ca-132">增量导出</span><span class="sxs-lookup"><span data-stu-id="326ca-132">Incremental export</span></span>

<span data-ttu-id="326ca-133">添加要进行数据导出的实体时，可以执行增量推送（导出）或全面推送。</span><span class="sxs-lookup"><span data-stu-id="326ca-133">When you add an entity for data export, you can do either an incremental push (export) or a full push.</span></span> <span data-ttu-id="326ca-134">全面推送将从 BYOD 数据库中的实体中删除所有现有记录。</span><span class="sxs-lookup"><span data-stu-id="326ca-134">A full push deletes all existing records from an entity in the BYOD database.</span></span> <span data-ttu-id="326ca-135">然后，插入 Human Resources 实体中的当前记录集。</span><span class="sxs-lookup"><span data-stu-id="326ca-135">It then inserts the current set of records from the Human Resources entity.</span></span>

<span data-ttu-id="326ca-136">要执行增量推送，必须在 **实体** 页上为每个实体打开更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="326ca-136">To do an incremental push, you must turn on change tracking for each entity on the **Entities** page.</span></span> <span data-ttu-id="326ca-137">有关详细信息，请参阅[启用对实体的更改跟踪](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="326ca-137">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="326ca-138">如果选择增量推送，第一个推送始终是全面推送。</span><span class="sxs-lookup"><span data-stu-id="326ca-138">If you select an incremental push, the first push is always a full push.</span></span> <span data-ttu-id="326ca-139">SQL 将跟踪来自第一个全面推送的更改。</span><span class="sxs-lookup"><span data-stu-id="326ca-139">SQL tracks changes from this first full push.</span></span> <span data-ttu-id="326ca-140">插入新记录或更新或删除记录时，更改将反映在目标实体中。</span><span class="sxs-lookup"><span data-stu-id="326ca-140">When a new record is inserted, or when a record is updated or deleted, the change is reflected in the destination entity.</span></span>

## <a name="time-outs"></a><span data-ttu-id="326ca-141">超时</span><span class="sxs-lookup"><span data-stu-id="326ca-141">Time-outs</span></span>

<span data-ttu-id="326ca-142">以下是 BYOD 导出的默认超时：</span><span class="sxs-lookup"><span data-stu-id="326ca-142">Here are the default time-outs for BYOD exports:</span></span>

- <span data-ttu-id="326ca-143">截断操作十分钟</span><span class="sxs-lookup"><span data-stu-id="326ca-143">Ten minutes for truncation operations</span></span>
- <span data-ttu-id="326ca-144">批量插入操作一小时</span><span class="sxs-lookup"><span data-stu-id="326ca-144">One hour for bulk insert operations</span></span>

<span data-ttu-id="326ca-145">当量较大时，这些超时设置可能不够。</span><span class="sxs-lookup"><span data-stu-id="326ca-145">When volumes are high, these time-out settings might not be sufficient.</span></span> <span data-ttu-id="326ca-146">要更新设置，请转到 **数据管理 \> 框架参数 \> 提供您自己的数据库**。</span><span class="sxs-lookup"><span data-stu-id="326ca-146">To update them, go to **Data management \> Framework parameters \> Bring your own database**.</span></span> <span data-ttu-id="326ca-147">这些超时是公司特定的，必须为每个公司分别设置。</span><span class="sxs-lookup"><span data-stu-id="326ca-147">These time-outs are company-specific and must be set separately for each company.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="326ca-148">已知限制</span><span class="sxs-lookup"><span data-stu-id="326ca-148">Known limitations</span></span>

<span data-ttu-id="326ca-149">BYOD 功能具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="326ca-149">The BYOD feature has the following limitations:</span></span>

- <span data-ttu-id="326ca-150">同步期间，数据库上不应有活动锁定。</span><span class="sxs-lookup"><span data-stu-id="326ca-150">There should be no active locks on your database during synchronization.</span></span> <span data-ttu-id="326ca-151">活动锁可能导致写入缓慢，甚至无法将数据导出到 Azure SQL 数据库。</span><span class="sxs-lookup"><span data-stu-id="326ca-151">Active locks can cause slow writes or even failure to export data to your Azure SQL database.</span></span>
- <span data-ttu-id="326ca-152">您无法将组合实体导出到自己的数据库中。</span><span class="sxs-lookup"><span data-stu-id="326ca-152">You can't export composite entities into your own database.</span></span> <span data-ttu-id="326ca-153">当前，不支持组合实体。</span><span class="sxs-lookup"><span data-stu-id="326ca-153">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="326ca-154">您必须导出组成组合实体的单个实体。</span><span class="sxs-lookup"><span data-stu-id="326ca-154">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="326ca-155">不过，可以导出同一个数据项目中的两个实体。</span><span class="sxs-lookup"><span data-stu-id="326ca-155">However, you can export both entities in the same data project.</span></span>
- <span data-ttu-id="326ca-156">没有唯一键的实体无法使用增量推送来导出。</span><span class="sxs-lookup"><span data-stu-id="326ca-156">Entities that don't have unique keys can't be exported by using incremental push.</span></span> <span data-ttu-id="326ca-157">您可能会遇到此限制，尤其是当您尝试从一些现成的实体增量导出记录时。</span><span class="sxs-lookup"><span data-stu-id="326ca-157">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="326ca-158">因为设计这些实体是为了支持数据导入，所以它们没有唯一键。</span><span class="sxs-lookup"><span data-stu-id="326ca-158">Because these entities were designed to enable the import of data, they don't have a unique key.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="326ca-159">疑难解答</span><span class="sxs-lookup"><span data-stu-id="326ca-159">Troubleshooting</span></span>

### <a name="incremental-push-doesnt-work-correctly"></a><span data-ttu-id="326ca-160">增量推送无法正常工作</span><span class="sxs-lookup"><span data-stu-id="326ca-160">Incremental push doesn't work correctly</span></span>

<span data-ttu-id="326ca-161">**问题：** 当对实体进行全面推送时，如果使用 **select** 语句，您会在 BYOD 中看到大量记录。</span><span class="sxs-lookup"><span data-stu-id="326ca-161">**Issue:** When a full push occurs for an entity, you see a large set of records in BYOD when you use a **select** statement.</span></span> <span data-ttu-id="326ca-162">但是，当您执行增量推送时，您在 BYOD 中只会看到几条记录。</span><span class="sxs-lookup"><span data-stu-id="326ca-162">However, when you do an incremental push, you see only a few records in BYOD.</span></span> <span data-ttu-id="326ca-163">似乎增量推送删除了所有记录，然后仅在 BYOD 中添加了更改的记录。</span><span class="sxs-lookup"><span data-stu-id="326ca-163">It seems as though the incremental push deleted all the records and added only the changed records in BYOD.</span></span>

<span data-ttu-id="326ca-164">**解决方法：** SQL 更改跟踪表可能未处于预期状态。</span><span class="sxs-lookup"><span data-stu-id="326ca-164">**Solution:** The SQL change tracking tables might not be in the expected state.</span></span> <span data-ttu-id="326ca-165">在这种情况下，建议您关闭实体的变更跟踪，然后再将其重新打开。</span><span class="sxs-lookup"><span data-stu-id="326ca-165">In cases of this type, we recommend that you turn off change tracking for the entity and then turn it back on.</span></span> <span data-ttu-id="326ca-166">有关详细信息，请参阅[启用对实体的更改跟踪](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="326ca-166">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="326ca-167">请参阅</span><span class="sxs-lookup"><span data-stu-id="326ca-167">See also</span></span>

[<span data-ttu-id="326ca-168">数据管理概览</span><span class="sxs-lookup"><span data-stu-id="326ca-168">Data management overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="326ca-169">提供您自己的数据库 (BYOD)</span><span class="sxs-lookup"><span data-stu-id="326ca-169">Bring your own database (BYOD)</span></span>](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="326ca-170">数据导入和导出作业概览</span><span class="sxs-lookup"><span data-stu-id="326ca-170">Data import and export jobs overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="326ca-171">启用对实体的更改跟踪</span><span class="sxs-lookup"><span data-stu-id="326ca-171">Enable change tracking for entities</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]