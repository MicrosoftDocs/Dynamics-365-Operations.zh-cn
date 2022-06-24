---
title: 仓库管理现有条目清除作业
description: 本文介绍现有条目清除作业，该作业通过识别和删除相关但不需要的记录来帮助提高系统性能。
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 7f054f4f479affe8ca2e041c77bd6fd11d51378e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900497"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>仓库管理现有条目清除作业

[!include [banner](../includes/banner.md)]

用于计算现有库存量的查询的性能受所涉及表中的记录数的影响。 帮助提高性能的一种方法是减少数据库必须考虑的记录数。

本文介绍现有条目清除作业，该作业将删除 InventSum 和 WHSInventReserve 表中不需要的记录。 这些表存储已启用仓库管理处理的项目的现有信息。 （这些项目称为 WHS 项。）删除这些记录可以显著提高现有计算的性能。

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

如果现有条目清除作业删除给定级别（如牌照级别）的所有记录，用户可能会受到影响。 在这种情况下，用于查看库存先前在牌照上是否是可用现有量的功能可能无法按预期工作，因为相关的现有条目不再可用。 例如，在以下情况下可能会遇到这种情况：

- 在 **现有量列表** 上，当用户在 **维度显示** 设置中取消选择条件 **数量 \<\> 0** 或选择条件 **关闭的交易** 时。
- 在过去期间的 **按照库存维度统计的物理库存** 报表中，当用户设置 **截止日期** 参数时。

但是，清除作业提供的性能改进应会弥补功能上的这些小损失。

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>让“最长执行时间”可用

**最大执行时间** 设置仅在 *仓库管理现有条目清理作业的最长执行时间* 功能开启时可用。 从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。 管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *仓库管理现有条目清理作业的最长执行时间* 功能来打开或关闭此功能。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]