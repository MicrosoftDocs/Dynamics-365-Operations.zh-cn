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
ms.openlocfilehash: f21e9b94b5aa30b2cdb18692e8cc9c8d00f758d6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805026"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>优化 BYOD 计划批处理作业

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题说明在使用“提供您自己的数据库 (BYOD)”功能时如何优化性能。 有关 BYOD 的详细信息，请参阅[提供您自己的数据库 (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)。

## <a name="performance-considerations-for-data-export"></a>数据导出的性能注意事项

实体发布到目标数据库后，可以使用 **数据管理** 工作区中的导出功能来移动数据。 导出功能使您可以定义包含一个或多个实体的数据移动作业。 有关数据导出的详细信息，请参阅[数据导入和导出作业概述](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)。

您可以使用 **导出** 页面将数据导出为不同的目标数据格式，如逗号分隔值 (CSV) 文件。 此页面还支持将 SQL 数据库作为另一个目标。

您可以创建一个具有多个实体的数据项目，然后使用批处理作业来计划该数据项目的运行。 如果选择 **批量导出** 选项，您可以将数据导出作业计划为定期运行。

为了帮助保持 BYOD 导出的整体可靠性，在向导出项目添加多个实体时必须小心。 确定要添加到同一项目的实体数时，请考虑以下参数：

- 实体的复杂性
- 每个实体的预期数据量
- 完成作业级别的导出所需的总时间

为了获得最佳性能，请避免将数百个实体添加到一个项目中。 我们建议您创建多个作业，每个作业包含较少的实体。

## <a name="scheduling-byod-batch-jobs"></a>计划 BYOD 批处理作业

为帮助减少对 Microsoft Dynamics 365 Human Resources 用户的影响，请在晚上或下班后运行 BYOD 批处理作业。 务必检查定期批处理作业的时区。 某些批处理作业可能使用太平洋标准时间 (PST)。

为帮助避免性能问题，在为 BYOD 批处理作业配置计划频率时，请考虑以下因素：

- 完成每个批处理作业所需的时间
- BYOD 中数据的业务需求

将每个批处理作业的频率设置为一个可以确保该作业可以在下一个计划的运行时间之前正常完成的值。 避免并行运行多个作业，因为这种方法会对 Human Resources 的性能产生负面影响。

为了获得最佳性能，请始终使用 **导出** 页面上的 **批量导出** 选项来计划 BYOD 批处理作业。 避免通过 **管理 \> 管理定期数据作业** 计划定期导出。

## <a name="incremental-export"></a>增量导出

添加要进行数据导出的实体时，可以执行增量推送（导出）或全面推送。 全面推送将从 BYOD 数据库中的实体中删除所有现有记录。 然后，插入 Human Resources 实体中的当前记录集。

要执行增量推送，必须在 **实体** 页上为每个实体打开更改跟踪。 有关详细信息，请参阅[启用对实体的更改跟踪](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)。

如果选择增量推送，第一个推送始终是全面推送。 SQL 将跟踪来自第一个全面推送的更改。 插入新记录或更新或删除记录时，更改将反映在目标实体中。

## <a name="time-outs"></a>超时

以下是 BYOD 导出的默认超时：

- 截断操作十分钟
- 批量插入操作一小时

当量较大时，这些超时设置可能不够。 要更新设置，请转到 **数据管理 \> 框架参数 \> 提供您自己的数据库**。 这些超时是公司特定的，必须为每个公司分别设置。

## <a name="known-limitations"></a>已知限制

BYOD 功能具有下列限制：

- 同步期间，数据库上不应有活动锁定。 活动锁可能导致写入缓慢，甚至无法将数据导出到 Azure SQL 数据库。
- 您无法将组合实体导出到自己的数据库中。 当前，不支持组合实体。 您必须导出组成组合实体的单个实体。 不过，可以导出同一个数据项目中的两个实体。
- 没有唯一键的实体无法使用增量推送来导出。 您可能会遇到此限制，尤其是当您尝试从一些现成的实体增量导出记录时。 因为设计这些实体是为了支持数据导入，所以它们没有唯一键。

## <a name="troubleshooting"></a>疑难解答

### <a name="incremental-push-doesnt-work-correctly"></a>增量推送无法正常工作

**问题：** 当对实体进行全面推送时，如果使用 **select** 语句，您会在 BYOD 中看到大量记录。 但是，当您执行增量推送时，您在 BYOD 中只会看到几条记录。 似乎增量推送删除了所有记录，然后仅在 BYOD 中添加了更改的记录。

**解决方法：** SQL 更改跟踪表可能未处于预期状态。 在这种情况下，建议您关闭实体的变更跟踪，然后再将其重新打开。 有关详细信息，请参阅[启用对实体的更改跟踪](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)。

## <a name="see-also"></a>请参阅

[数据管理概览](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[提供您自己的数据库 (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[数据导入和导出作业概览](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[启用对实体的更改跟踪](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]