---
title: 安装缩放单元仓库工作负荷后出现处理问题
description: 本主题介绍安装缩放单元仓库工作负荷后可能很快出现的问题，并提供修复建议。
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071623"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>安装缩放单元仓库工作负荷后出现处理问题

本主题介绍安装缩放单元仓库工作负荷后可能很快出现的问题，并提供修复建议。

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>问题 1：从负荷计划工作台发放负荷后出错

### <a name="symptoms-of-issue-1"></a>问题 1 特征

当您从 **负荷计划工作台** 或 **出站负荷计划工作台** 页面发放负荷时，您会收到以下形式的错误消息：

> 过帐负荷 %1 时捕获到异常，无法发放负荷。
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> 无法编辑装运中的记录 (WHSShipmentTable)。 装运 ID：...

以下是包含示例数据的实际示例：

> 过帐负荷 USMF-000033 时捕获到异常，无法发放负荷。
会话 5133（管理员）
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]缩放单元 @@ 尝试更新缩放单元 @A 负责的记录。  
> 对象服务器 Azure：
>
> 无法编辑装运中的记录 (WHSShipmentTable)。 装运 ID：USMF-000031、USMF-000033。 SQL 数据库已发布一个错误。

### <a name="cause-of-issue-1"></a>问题 1 原因

如果安装缩放单元仓库工作负荷时存在以下条件组合，可能会出现此问题：

- 系统包含未发放的负荷，其中有多个行与不同的订单关联，有一些负荷行未与装运关联。
- 系统被设置为使用装运合并。

在分布式混合拓扑部署中，每个负荷和装运记录都标记为由特定缩放单元或中心负责。 当您从 **负荷计划工作台** 页面发放负荷时，系统会更改分配的所有权。 但是，由于以前列出的条件，系统可能无法解析数据所有权。 因此，它无法将负荷发放到仓库。

### <a name="resolution-of-issue-1"></a>解决问题 1

将负荷拆分为两个较小的负荷，然后再将其发放到仓库。

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>问题 2：在缩放单元中处理波次时出错

### <a name="symptoms-of-issue-2"></a>问题 2 特征

在缩放单元上处理波次时，您收到以下形式的错误消息：

> 您无法修改 RecId = %1、负荷 ID= %2 的负荷行，因为它仍由企业中心负责。 请确保相应的出站负荷已被发放到缩放单元，并因此已创建仓库订单行。

以下是包含示例数据的实际示例：

> 作业执行波次 USMF-000000012 (9223377668365210) 的信息日志  
> 任务执行波次 USMF-000000012 (9223377668370462) 的信息日志  
> 您无法修改 RecId = 68719478242、负荷 ID= USMF-000034 的负荷行，因为它仍由企业中心负责。 请确保相应的出站负荷已被发放到缩放单元，并因此已创建仓库订单行。

### <a name="cause-of-issue-2"></a>问题 2 原因

在分布式混合拓扑部署中，负荷和装运数据的所有权被分配给特定缩放单元或中心。 作为波次处理的一部分，数据的所有权会被分配给缩放单元。

安装缩放单元仓库工作负荷时，如果未结装运与负荷和波次关联，系统将无法控制数据所有权。 因此，波次处理在缩放单元上失败。

### <a name="resolution-of-issue-2"></a>解决问题 2

将负荷从中心发放到仓库。

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>通过查看记录的所有权和目标来解决问题

在分布式混合拓扑部署中，很多记录类型标记为由特定缩放单元或中心负责。 切换到分布式混合拓扑并/或设置新的缩放单元仓库工作负荷后，系统会将所有权分配给每个相关记录。 此过程有时会导致错误或意外结果。 因此，有关记录所有权和转移目标的信息可以帮助您解决在进行这些类型的更改后出现的问题。

请按照以下步骤查看记录的所有权和转移目标。

1. 打开相关记录。
1. 在操作窗格上，在 **选项** 选项卡，在 **记录信息** 组中，选择 **显示所有字段**。
1. 出现的页面显示可用于所选记录的所有字段的值。 查看以下字段：

    - **SYSSCALEUNITID** – 此字段显示记录的当前负责人。
    - **SYSTARGETSCALEUNITID** – 此字段显示当前负责人完成处理后记录将转移到的中心或缩放单元的缩放单元 ID。 此字段的值由管理此类流程的批处理作业使用。 虽然此字段不与所有权直接相关，但转移记录时所有权可能会发生变化。 在某些情况下，此字段将为空白。
