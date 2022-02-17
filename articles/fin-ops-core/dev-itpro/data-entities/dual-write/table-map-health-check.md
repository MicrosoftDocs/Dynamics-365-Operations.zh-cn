---
title: 表映射运行状况检查的错误代码
description: 本主题介绍表映射运行状况检查的错误代码。
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061270"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>表映射运行状况检查的错误代码

[!include [banner](../../includes/banner.md)]



本主题介绍表映射运行状况检查的错误代码。

## <a name="error-100"></a>错误 100

错误消息是“最低需要财务和运营平台版本 PU 43 才能运行财务和运营建议。”

此功能需要版本 10.0.19 或更高版本财务和运营应用的平台更新。

## <a name="error-400"></a>错误 400

错误消息是“未找到实体\{财务和运营 UniqueEntityName\} 的业务事件注册数据，这意味着映射未运行或所有字段映射都是单向的。”

## <a name="error-500"></a>错误 500

错误消息是“未找到项目 \{项目名称\} 的项目配置。 可能由于项目未启用，或从客户互动到财务和运营的所有字段映射都是单向的。”

请检查表映射的映射。 如果它们是从客户互动应用到财务和运营应用的单向映射，则不会为从财务和运营应用到 Dataverse 应用的实时同步生成流量。

## <a name="error-900"></a>错误 900

错误消息是“实体\{财务和运营 UniqueEntityName\} 的源筛选器 \{sourceFilter\} 格式无效。”

在表映射上为财务和运营应用指定的源筛选器在语法上不正确。 要验证筛选条件，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps)。

## <a name="error-1000"></a>错误 1000

错误消息是“用于双写入实时同步的实体\{财务和运营 UniqueEntityName\} 查询是\{财务和运营 EntityFilterQueryString\}。 符合查询条件的记录将被选出进行实时同步。”

返回的实体查询是实体的后备 SQL 查询。 请检查查询上确定选出要进行实时同步的业务数据的内部联接或筛选器。 内部联接和筛选器是要选出以进行双写入实时同步的每个记录必须满足的强制性条件。

## <a name="error-1300"></a>错误 1300

错误消息是“可能无法跟踪实体\{财务和运营 EntityMetadata.EntityProperties.LogicalEntityName\} 的虚拟字段 \{s.EntityFieldName\} 的双写入。”

财务和运营表中的虚拟字段未启用跟踪。 实时同步可以同步数据，但无法选出对列所作的更改。

## <a name="error-1500"></a>错误 1500

错误消息是“应该至少有一个字段映射到 Customer Engagement 上的非查找字段，以对数据源 \{datasource.DataSourceName\} 启用跟踪。”

实体中的数据源没有任何映射要进行双重写入的字段。 对基础表的更改不会被双写入跟踪。

## <a name="error-1600"></a>错误 1600

错误消息是“实体\{财务和运营 EntityMetadata.EntityProperties.LogicalEntityName\} 的数据源 \{datasource.DataSourceName\} 有一个范围。 只有满足此范围条件的记录会被选出作为出站记录。”

财务和运营应用中的实体可以具有启用了筛选器范围的数据源。 这些范围定义作为实时同步的一部分选出的记录。 如果某些记录从财务和运营应用跳过到 Dataverse，请检查这些记录是否符合实体上的范围条件。 执行此检查的简单方法是运行类似于以下示例的 SQL 查询。

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>错误 1700

错误消息是“实体 \{datasourceTable.Key.entityName\} 的表 \{datasourceTable.Key.subscribedTableName\} 是为实体 \{origTableToEntityMaps.EntityName\} 跟踪。 为多个实体跟踪的相同表可能会影响实时同步事务的系统性能。”

如果同一个表被多个实体跟踪，对表的任何更改都会触发链接实体的双写入评估。 虽然筛选器子句仅发送有效记录，但如果存在长时间运行的查询或未优化的查询计划，评估可能会导致性能问题。 从业务角度来看，此问题可能不可避免。 但是，如果跨多个实体存在很多相交表，您应考虑简化实体或检查实体查询的优化。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
