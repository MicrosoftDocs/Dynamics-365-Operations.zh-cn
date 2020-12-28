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
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423383"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>仓库管理现有条目清除作业

用于计算现有库存量的查询的性能受所涉及表中的记录数的影响。 帮助提高性能的一种方法是减少数据库必须考虑的记录数。

本主题介绍现有条目清除作业，该作业将删除 InventSum 和 WHSInventReserve 表中不需要的记录。 这些表存储已启用仓库管理处理的项目的现有信息。 （这些项目称为 WHS 项。）删除这些记录可以显著提高现有计算的性能。

## <a name="what-the-cleanup-job-does"></a>清理作业做什么

现有条目清除作业将删除 WHSInventReserve 和 InventSum 表中所有字段值为 *0*（零）的记录。 这些记录可以删除，因为它们不会对现有信息有所帮助。 此作业仅删除 **库位** 级别以下的记录。

如果允许负实际库存，清除作业可能无法删除所有相关条目。 出现此限制的原因是，此作业必须允许一种特殊情况，即牌照具有多个序列号，而这些序列号之一已变为负数。 例如，当牌照的序列号 1 有 +1 件，序列号 2 有 –1 件时，系统将在牌照级别显示零。 对于这种特殊情况，此作业会先进行广度优先删除，尝试先从较低级别中删除。

## <a name="schedule-and-configure-the-cleanup-job"></a>计划和配置清除作业

现有条目清除作业可以在 **库存管理 \> 定期任务 \> 清除 \> 仓库管理现有条目清除** 处找到。 使用标准作业设置可以控制运行此作业的范围和计划。 此外，还提供了以下设置︰

- **如果这几天未更新则删除** – 输入作业删除已降为零数量的现有条目之前应等待的最小天数。 使用此设置有助于降低删除仍在使用的现有条目的风险。 如果您希望尽快进行清除，请输入 *0*（零）或将此字段留空。
- **最长执行时间（小时）**– 输入清除作业的最长执行时间，以小时为单位。 如果在此时间过去之前作业未完成，它将保存到目前为止已完成的工作，然后自行关闭。 此功能对于具有大库存使用量的实现尤其重要。 在这些情况下，您应该将此作业计划为在系统负荷尽可能轻时运行。 如果您希望批处理作业继续运行直到完成，请输入 *0*（零）或将此字段留空。 仅当相关功能已[在您的系统中打开](#max-execution-time)时，此设置才可用。

尽管您可以在正常营业时间运行此作业，但是我们建议您在工作时间以外运行。 这样，如果用户正在使用的记录也要清除，可以帮助防止发生冲突。

如果作业尝试删除另一个用户正在使用的某个项的记录，清除作业或用户将发生死锁错误。

此作业运行时，它的提交大小为 100。 换句话说，它将尝试每 100 次删除提交一次。 但是，由于某些删除是基于集的，因此在某些情况下可能会在同一事务中删除 100 个以上记录。 因此，锁升级有时仍会发生。

## <a name="possible-user-impact"></a>可能的用户影响

如果现有条目清除作业删除给定级别（如牌照级别）的所有记录，用户可能会受到影响。 在这种情况下，用于查看库存先前在牌照上是否是可用现有量的功能可能无法按预期工作，因为相关的现有条目不再可用。 （当用户查看现有信息时，该功能将检查 **维度显示** 设置中的条件 **数量 \<\> 0**。）但是，清除作业提供的性能改进应该会弥补这一功能上的小损失。

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>让“最长执行时间”可用

默认情况下，**最长执行时间** 设置不可用。 如果要使用它，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)在系统中打开相关功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*仓库管理现有条目清除作业的最长执行时间*
