---
title: 仓库管理现有条目清除作业
description: 本主题介绍现有条目清除作业，该作业通过识别和删除相关但不需要的记录来帮助提高系统性能。
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 9d01c577fc33564d3517d242e9b01f73cc8e079c
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015933"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a><span data-ttu-id="da68f-103">仓库管理现有条目清除作业</span><span class="sxs-lookup"><span data-stu-id="da68f-103">Warehouse management on-hand entries cleanup job</span></span>

<span data-ttu-id="da68f-104">用于计算现有库存量的查询的性能受所涉及表中的记录数的影响。</span><span class="sxs-lookup"><span data-stu-id="da68f-104">The performance of queries that are used to calculate on-hand inventory is affected by the number of records in the tables that are involved.</span></span> <span data-ttu-id="da68f-105">帮助提高性能的一种方法是减少数据库必须考虑的记录数。</span><span class="sxs-lookup"><span data-stu-id="da68f-105">One way to help improve the performance is to reduce the number of records that the database must consider.</span></span>

<span data-ttu-id="da68f-106">本主题介绍现有条目清除作业，该作业将删除 InventSum 和 WHSInventReserve 表中不需要的记录。</span><span class="sxs-lookup"><span data-stu-id="da68f-106">This topic describes the on-hand entries cleanup job, which deletes unneeded records in the InventSum and WHSInventReserve tables.</span></span> <span data-ttu-id="da68f-107">这些表存储已启用仓库管理处理的项目的现有信息。</span><span class="sxs-lookup"><span data-stu-id="da68f-107">These tables store on-hand information for items that are enabled for warehouse management processing.</span></span> <span data-ttu-id="da68f-108">（这些项目称为 WHS 项。）删除这些记录可以显著提高现有计算的性能。</span><span class="sxs-lookup"><span data-stu-id="da68f-108">(These items are referred to as WHS items.) Deletion of these records can significantly improve the performance of on-hand calculations.</span></span>

## <a name="what-the-cleanup-job-does"></a><span data-ttu-id="da68f-109">清理作业做什么</span><span class="sxs-lookup"><span data-stu-id="da68f-109">What the cleanup job does</span></span>

<span data-ttu-id="da68f-110">现有条目清除作业将删除 WHSInventReserve 和 InventSum 表中所有字段值为 *0* （零）的记录。</span><span class="sxs-lookup"><span data-stu-id="da68f-110">The on-hand entries cleanup job deletes any records in the WHSInventReserve and InventSum tables where all the field values are *0* (zero).</span></span> <span data-ttu-id="da68f-111">这些记录可以删除，因为它们不会对现有信息有所帮助。</span><span class="sxs-lookup"><span data-stu-id="da68f-111">These records can be deleted because they don't contribute to the on-hand information.</span></span> <span data-ttu-id="da68f-112">此作业仅删除 **库位** 级别以下的记录。</span><span class="sxs-lookup"><span data-stu-id="da68f-112">The job deletes only records that are below the **Location** level.</span></span>

<span data-ttu-id="da68f-113">如果允许负实际库存，清除作业可能无法删除所有相关条目。</span><span class="sxs-lookup"><span data-stu-id="da68f-113">If negative physical inventory is allowed, the cleanup job might not be able to delete all the relevant entries.</span></span> <span data-ttu-id="da68f-114">出现此限制的原因是，此作业必须允许一种特殊情况，即牌照具有多个序列号，而这些序列号之一已变为负数。</span><span class="sxs-lookup"><span data-stu-id="da68f-114">The reason for this limitation is that the job must allow for a special scenario where a license plate has multiple serial numbers, and one of those serial numbers has become negative.</span></span> <span data-ttu-id="da68f-115">例如，当牌照的序列号 1 有 +1 件，序列号 2 有 –1 件时，系统将在牌照级别显示零。</span><span class="sxs-lookup"><span data-stu-id="da68f-115">For example, the system will have zero on hand at the license plate level when a license plate has +1 pcs of serial number 1 and –1 pcs of serial number 2.</span></span> <span data-ttu-id="da68f-116">对于这种特殊情况，此作业会先进行广度优先删除，尝试先从较低级别中删除。</span><span class="sxs-lookup"><span data-stu-id="da68f-116">For this special scenario, the job does a breadth-first deletion, where it tries to delete from lower levels first.</span></span>

## <a name="schedule-and-configure-the-cleanup-job"></a><span data-ttu-id="da68f-117">计划和配置清除作业</span><span class="sxs-lookup"><span data-stu-id="da68f-117">Schedule and configure the cleanup job</span></span>

<span data-ttu-id="da68f-118">现有条目清除作业可以在 **库存管理 \> 定期任务 \> 清除 \> 仓库管理现有条目清除** 处找到。</span><span class="sxs-lookup"><span data-stu-id="da68f-118">The on-hand entries cleanup job is available at **Inventory management \> Periodic tasks \> Clean up \> Warehouse management on-hand entries cleanup**.</span></span> <span data-ttu-id="da68f-119">使用标准作业设置可以控制运行此作业的范围和计划。</span><span class="sxs-lookup"><span data-stu-id="da68f-119">Use the standard job settings to control the scope and schedule for running the job.</span></span> <span data-ttu-id="da68f-120">此外，还提供了以下设置︰</span><span class="sxs-lookup"><span data-stu-id="da68f-120">In addition, the following settings are provided:</span></span>

- <span data-ttu-id="da68f-121">**如果这几天未更新则删除** – 输入作业删除已降为零数量的现有条目之前应等待的最小天数。</span><span class="sxs-lookup"><span data-stu-id="da68f-121">**Delete if not updated for this many days** – Enter the minimum number of days that the job should wait before it deletes an on-hand entry that has dropped to zero quantity.</span></span> <span data-ttu-id="da68f-122">使用此设置有助于降低删除仍在使用的现有条目的风险。</span><span class="sxs-lookup"><span data-stu-id="da68f-122">Use this setting to help reduce the risk of deleting on-hand entries that are still being used.</span></span> <span data-ttu-id="da68f-123">如果您希望尽快进行清除，请输入 *0* （零）或将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="da68f-123">If you want cleanup to occur as soon as possible, either enter *0* (zero) or leave the field blank.</span></span>
- <span data-ttu-id="da68f-124">**最长执行时间（小时）** – 输入清除作业的最长执行时间，以小时为单位。</span><span class="sxs-lookup"><span data-stu-id="da68f-124">**Maximum execution time (hours)** – Enter the maximum execution time of the cleanup job, in hours.</span></span> <span data-ttu-id="da68f-125">如果在此时间过去之前作业未完成，它将保存到目前为止已完成的工作，然后自行关闭。</span><span class="sxs-lookup"><span data-stu-id="da68f-125">If the job isn't completed before this time passes, it will save the work that it has completed so far and then close itself.</span></span> <span data-ttu-id="da68f-126">此功能对于具有大库存使用量的实现尤其重要。</span><span class="sxs-lookup"><span data-stu-id="da68f-126">This capability is especially relevant for implementations that have high inventory use.</span></span> <span data-ttu-id="da68f-127">在这些情况下，您应该将此作业计划为在系统负荷尽可能轻时运行。</span><span class="sxs-lookup"><span data-stu-id="da68f-127">In these cases, you should schedule the job to run at times when the system load is as light as possible.</span></span> <span data-ttu-id="da68f-128">如果您希望批处理作业继续运行直到完成，请输入 *0* （零）或将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="da68f-128">If you want the batch job to continue to run until it's completed, either enter *0* (zero) or leave the field blank.</span></span> <span data-ttu-id="da68f-129">仅当相关功能已[在您的系统中打开](#max-execution-time)时，此设置才可用。</span><span class="sxs-lookup"><span data-stu-id="da68f-129">This setting is available only if the related feature has been [turned on in your system](#max-execution-time).</span></span>

<span data-ttu-id="da68f-130">尽管您可以在正常营业时间运行此作业，但是我们建议您在工作时间以外运行。</span><span class="sxs-lookup"><span data-stu-id="da68f-130">Although you can run the job during regular business hours, we recommend that you run it outside working hours.</span></span> <span data-ttu-id="da68f-131">这样，如果用户正在使用的记录也要清除，可以帮助防止发生冲突。</span><span class="sxs-lookup"><span data-stu-id="da68f-131">In this way, you help prevent conflicts that can occur if a user is working with a record that is also being cleaned up.</span></span>

<span data-ttu-id="da68f-132">如果作业尝试删除另一个用户正在使用的某个项的记录，清除作业或用户将发生死锁错误。</span><span class="sxs-lookup"><span data-stu-id="da68f-132">If the job tries to delete a record for an item while that record is being used by another user, a deadlock error occurs for either the cleanup job or the user.</span></span>

<span data-ttu-id="da68f-133">此作业运行时，它的提交大小为 100。</span><span class="sxs-lookup"><span data-stu-id="da68f-133">When the job runs, it has a commit size of 100.</span></span> <span data-ttu-id="da68f-134">换句话说，它将尝试每 100 次删除提交一次。</span><span class="sxs-lookup"><span data-stu-id="da68f-134">In other words, it will try to commit one time for every 100 deletions.</span></span> <span data-ttu-id="da68f-135">但是，由于某些删除是基于集的，因此在某些情况下可能会在同一事务中删除 100 个以上记录。</span><span class="sxs-lookup"><span data-stu-id="da68f-135">However, because some deletions are set-based, there might be scenarios where more than 100 records can be deleted in the same transaction.</span></span> <span data-ttu-id="da68f-136">因此，锁升级有时仍会发生。</span><span class="sxs-lookup"><span data-stu-id="da68f-136">Therefore, lock escalations can still sometimes occur.</span></span>

## <a name="possible-user-impact"></a><span data-ttu-id="da68f-137">可能的用户影响</span><span class="sxs-lookup"><span data-stu-id="da68f-137">Possible user impact</span></span>

<span data-ttu-id="da68f-138">如果现有条目清除作业删除给定级别（如牌照级别）的所有记录，用户可能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="da68f-138">Users might be affected if the on-hand entries cleanup job deletes all the records for a given level (such as the license plate level).</span></span> <span data-ttu-id="da68f-139">在这种情况下，用于查看库存先前在牌照上是否是可用现有量的功能可能无法按预期工作，因为相关的现有条目不再可用。</span><span class="sxs-lookup"><span data-stu-id="da68f-139">In this case, the functionality for seeing that inventory was previously available on hand at a license plate might not work as expected, because the relevant on-hand entries are no longer available.</span></span> <span data-ttu-id="da68f-140">（当用户查看现有信息时，该功能将检查 **维度显示** 设置中的条件 **数量 \<\> 0** 。）但是，清除作业提供的性能改进应该会弥补这一功能上的小损失。</span><span class="sxs-lookup"><span data-stu-id="da68f-140">(That functionality checks the condition **Quantity \<\> 0** in the **Dimension display** settings when users view on-hand information.) However, the performance improvement that the cleanup job provides should make up for this small loss in functionality.</span></span>

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a><span data-ttu-id="da68f-141">让“最长执行时间”可用</span><span class="sxs-lookup"><span data-stu-id="da68f-141">Make the Maximum execution time setting available</span></span>

<span data-ttu-id="da68f-142">默认情况下， **最长执行时间** 设置不可用。</span><span class="sxs-lookup"><span data-stu-id="da68f-142">By default, the **Maximum execution time** setting isn't available.</span></span> <span data-ttu-id="da68f-143">如果要使用它，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)在系统中打开相关功能。</span><span class="sxs-lookup"><span data-stu-id="da68f-143">If you want to use it, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the related feature in your system.</span></span> <span data-ttu-id="da68f-144">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="da68f-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="da68f-145">**模块** ： *仓库管理*</span><span class="sxs-lookup"><span data-stu-id="da68f-145">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="da68f-146">**功能名称** ： *仓库管理现有条目清除作业的最长执行时间*</span><span class="sxs-lookup"><span data-stu-id="da68f-146">**Feature name:** *Maximum execution time for the warehouse management on-hand entries cleanup job*</span></span>
