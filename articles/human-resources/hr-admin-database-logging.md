---
title: 配置和管理数据库日志记录
description: 您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8faf0be5f094f18b75f2263fa622c9b7f3983274
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899754"
---
# <a name="configure-and-manage-database-logging"></a>配置和管理数据库日志记录


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。 本文介绍如何：

- 管理数据库日志记录的安全性和性能
- 设置数据库日志记录
- 清理数据库日志

## <a name="overview-of-database-logging"></a>数据库日志记录概述

数据库日志记录跟踪对 Microsoft Dynamics 365 Human Resources 表和字段的特定更改。 这些更改包括插入、更新或删除。 数据库日志记录在数据库日志表中存储对表或字段的更改的记录。

数据库日志记录的业务用途包括：

- 创建对包含敏感信息的特定表的更改的审核记录。
- 跟踪单个事务。 数据库日志记录不用于跟踪在批处理作业中运行的自动事务。

## <a name="security-for-database-logging"></a>数据库日志记录的安全性

数据库日志可能包含敏感数据。 将访问限制为仅包括需要访问日志数据的安全角色。

## <a name="database-logging-and-performance"></a>数据库日志记录和性能

尽管从业务角度来看很有价值，但是数据库日志记录在资源使用和管理方面可能会非常昂贵。 数据库日志记录的性能影响包括：

- 数据库日志表会快速增长，导致数据库大小增加。 增长取决于您决定保留的记录的数据量。 默认情况下，数据库日志表仅维护 30 天的日志数据。 

- 数据库日志记录可能会对长期运行的自动化流程产生不利影响，如长期运行的数据导入。

### <a name="best-practices"></a>最佳实践

为了提高性能，请通过选择要记录的特定字段而不是整个表来限制日志条目。 为了帮助保持整体性能，数据库日志记录限制为 20 个表。

> [!NOTE]
> 各个字段只能记录更新。

## <a name="set-up-database-logging"></a>设置数据库日志记录

您可以使用 **记录数据库更改** 向导来设置数据库日志记录。 此向导提供了一种灵活的方式来设置表或字段的日志记录。

1. 转到 **系统管理 > 链接 > 数据库 > 数据库日志设置**。 选择 **新** 启动 **记录数据库更改** 向导。
2. 选择 **下一步**。 
3. 在向导的 **表和字段** 页面上，选择要启用数据库日志记录的表和字段，然后选择 **下一步**。

   > [!Note]
   > 数据库日志记录不适用于 Human Resources 数据库中的所有表。 选择列表下面的 **显示所有表** 可展开表和字段的列表，以显示数据库日志记录可用的所有数据库表，但这将是数据库表的完整列表的子集。

4. 在向导的 **更改类型** 页面上，选择要跟踪每个表和字段的更改的数据操作，然后选择 **下一步**。 有关可用于日志记录的数据操作的描述，请参阅下面的表。
5. 在 **完成** 页面上，查看将要进行的更改，然后选择 **完成**。

| 操作​ | 说明 |
| -- | -- |
| 跟踪新交易记录 | 为在表中创建的新记录创建日志。 |
| 更新 | 为表记录的更新或表中单独选择的字段的更新创建日志。 如果选择表的日志更新，将在每次更新表上任何记录的任何字段时创建日志记录。 如果选择特定字段的日志更新，仅在更新表记录的这些字段时创建日志记录。 |
| Delete | 为从表中删除的记录创建日志。 |
| 重命名键 | 重命名表键后，创建日志记录。 |


## <a name="clean-up-database-logs"></a>清理数据库日志

您可以使用以下选项删除全部或部分数据库日志：

- 选择特定表的所有日志。
- 选择数据库日志的特定类型。
- 选择创建日志的日期和时间。

要设置数据库日志清理，请执行以下步骤： 

1. 转到 **系统管理 > 链接 > 数据库 > 数据库日志**。 选择 **清理日志**。
2. 在 **要包括的记录** 标题下，选择 **筛选器**。
3. 选择将用于选择要删除的日志的方法。 输入以下选项之一：

   - 表 ID
   - 日志的类型
   - 创建日期和时间

4. 使用 **数据库日志清理** 选项卡确定何时运行日志清理任务。 默认情况下，数据库日志保留 30 天。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
