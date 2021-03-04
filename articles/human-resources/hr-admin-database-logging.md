---
title: 配置和管理数据库日志记录
description: 您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417456"
---
# <a name="configure-and-manage-database-logging"></a>配置和管理数据库日志记录

您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。 本主题介绍如何：

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
2. 完成该向导。

## <a name="clean-up-database-logs"></a>清理数据库日志

您可以使用以下选项删除全部或部分数据库日志：

- 选择特定表的所有日志。
- 选择数据库日志的特定类型。
- 选择创建日志的日期和时间。

要设置数据库日志清理，请执行以下步骤： 

1. 转到 **系统管理 > 链接 > 数据库 > 数据库日志**。 选择 **清理日志**。

2. 通过输入以下选项之一，选择用于选择要删除的日志的方法：

   - 表 ID
   - 日志的类型
   - 创建日期和时间

3. 使用 **数据库日志清理** 选项卡确定何时运行日志清理任务。 默认情况下，数据库日志保留 30 天。


[!INCLUDE[footer-include](../includes/footer-banner.md)]