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
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443563"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="c3f22-103">配置和管理数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c3f22-103">Configure and manage database logging</span></span>

<span data-ttu-id="c3f22-104">您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。</span><span class="sxs-lookup"><span data-stu-id="c3f22-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="c3f22-105">本主题介绍如何：</span><span class="sxs-lookup"><span data-stu-id="c3f22-105">This topic describes how to:</span></span>

- <span data-ttu-id="c3f22-106">管理数据库日志记录的安全性和性能</span><span class="sxs-lookup"><span data-stu-id="c3f22-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="c3f22-107">设置数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c3f22-107">Set up database logging</span></span>
- <span data-ttu-id="c3f22-108">清理数据库日志</span><span class="sxs-lookup"><span data-stu-id="c3f22-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="c3f22-109">数据库日志记录概述</span><span class="sxs-lookup"><span data-stu-id="c3f22-109">Overview of database logging</span></span>

<span data-ttu-id="c3f22-110">数据库日志记录跟踪对 Microsoft Dynamics 365 Human Resources 表和字段的特定更改。</span><span class="sxs-lookup"><span data-stu-id="c3f22-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="c3f22-111">这些更改包括插入、更新或删除。</span><span class="sxs-lookup"><span data-stu-id="c3f22-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="c3f22-112">数据库日志记录在数据库日志表中存储对表或字段的更改的记录。</span><span class="sxs-lookup"><span data-stu-id="c3f22-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="c3f22-113">数据库日志记录的业务用途包括：</span><span class="sxs-lookup"><span data-stu-id="c3f22-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="c3f22-114">创建对包含敏感信息的特定表的更改的审核记录。</span><span class="sxs-lookup"><span data-stu-id="c3f22-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="c3f22-115">跟踪单个事务。</span><span class="sxs-lookup"><span data-stu-id="c3f22-115">Tracking single transactions.</span></span> <span data-ttu-id="c3f22-116">数据库日志记录不用于跟踪在批处理作业中运行的自动事务。</span><span class="sxs-lookup"><span data-stu-id="c3f22-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="c3f22-117">数据库日志记录的安全性</span><span class="sxs-lookup"><span data-stu-id="c3f22-117">Security for database logging</span></span>

<span data-ttu-id="c3f22-118">数据库日志可能包含敏感数据。</span><span class="sxs-lookup"><span data-stu-id="c3f22-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="c3f22-119">将访问限制为仅包括需要访问日志数据的安全角色。</span><span class="sxs-lookup"><span data-stu-id="c3f22-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="c3f22-120">数据库日志记录和性能</span><span class="sxs-lookup"><span data-stu-id="c3f22-120">Database logging and performance</span></span>

<span data-ttu-id="c3f22-121">尽管从业务角度来看很有价值，但是数据库日志记录在资源使用和管理方面可能会非常昂贵。</span><span class="sxs-lookup"><span data-stu-id="c3f22-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="c3f22-122">数据库日志记录的性能影响包括：</span><span class="sxs-lookup"><span data-stu-id="c3f22-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="c3f22-123">数据库日志表会快速增长，导致数据库大小增加。</span><span class="sxs-lookup"><span data-stu-id="c3f22-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="c3f22-124">增长取决于您决定保留的记录的数据量。</span><span class="sxs-lookup"><span data-stu-id="c3f22-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="c3f22-125">默认情况下，数据库日志表仅维护 30 天的日志数据。</span><span class="sxs-lookup"><span data-stu-id="c3f22-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="c3f22-126">数据库日志记录可能会对长期运行的自动化流程产生不利影响，如长期运行的数据导入。</span><span class="sxs-lookup"><span data-stu-id="c3f22-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="c3f22-127">最佳实践</span><span class="sxs-lookup"><span data-stu-id="c3f22-127">Best practices</span></span>

<span data-ttu-id="c3f22-128">为了提高性能，请通过选择要记录的特定字段而不是整个表来限制日志条目。</span><span class="sxs-lookup"><span data-stu-id="c3f22-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="c3f22-129">为了帮助保持整体性能，数据库日志记录限制为 20 个表。</span><span class="sxs-lookup"><span data-stu-id="c3f22-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="c3f22-130">各个字段只能记录更新。</span><span class="sxs-lookup"><span data-stu-id="c3f22-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="c3f22-131">设置数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c3f22-131">Set up database logging</span></span>

<span data-ttu-id="c3f22-132">您可以使用**记录数据库更改**向导来设置数据库日志记录。</span><span class="sxs-lookup"><span data-stu-id="c3f22-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="c3f22-133">此向导提供了一种灵活的方式来设置表或字段的日志记录。</span><span class="sxs-lookup"><span data-stu-id="c3f22-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="c3f22-134">转到**系统管理 > 链接 > 数据库 > 数据库日志设置**。</span><span class="sxs-lookup"><span data-stu-id="c3f22-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="c3f22-135">选择**新**启动**记录数据库更改**向导。</span><span class="sxs-lookup"><span data-stu-id="c3f22-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="c3f22-136">完成该向导。</span><span class="sxs-lookup"><span data-stu-id="c3f22-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="c3f22-137">清理数据库日志</span><span class="sxs-lookup"><span data-stu-id="c3f22-137">Clean up database logs</span></span>

<span data-ttu-id="c3f22-138">您可以使用以下选项删除全部或部分数据库日志：</span><span class="sxs-lookup"><span data-stu-id="c3f22-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="c3f22-139">选择特定表的所有日志。</span><span class="sxs-lookup"><span data-stu-id="c3f22-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="c3f22-140">选择数据库日志的特定类型。</span><span class="sxs-lookup"><span data-stu-id="c3f22-140">Select specific types of database log.</span></span>
- <span data-ttu-id="c3f22-141">选择创建日志的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c3f22-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="c3f22-142">要设置数据库日志清理，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c3f22-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="c3f22-143">转到**系统管理 > 链接 > 数据库 > 数据库日志**。</span><span class="sxs-lookup"><span data-stu-id="c3f22-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="c3f22-144">选择**清理日志**。</span><span class="sxs-lookup"><span data-stu-id="c3f22-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="c3f22-145">通过输入以下选项之一，选择用于选择要删除的日志的方法：</span><span class="sxs-lookup"><span data-stu-id="c3f22-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="c3f22-146">表 ID</span><span class="sxs-lookup"><span data-stu-id="c3f22-146">Table ID</span></span>
   - <span data-ttu-id="c3f22-147">日志的类型</span><span class="sxs-lookup"><span data-stu-id="c3f22-147">Type of log</span></span>
   - <span data-ttu-id="c3f22-148">创建日期和时间</span><span class="sxs-lookup"><span data-stu-id="c3f22-148">Created date and time</span></span>

3. <span data-ttu-id="c3f22-149">使用**数据库日志清理**选项卡确定何时运行日志清理任务。</span><span class="sxs-lookup"><span data-stu-id="c3f22-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="c3f22-150">默认情况下，数据库日志保留 30 天。</span><span class="sxs-lookup"><span data-stu-id="c3f22-150">By default, database logs are available for 30 days.</span></span>
