---
title: 配置和管理数据库日志记录
description: 您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801327"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="c560e-103">配置和管理数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c560e-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c560e-104">您可以使用数据库日志记录跟踪 Dynamics 365 Human Resources 中对表和字段的更改。</span><span class="sxs-lookup"><span data-stu-id="c560e-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="c560e-105">本主题介绍如何：</span><span class="sxs-lookup"><span data-stu-id="c560e-105">This topic describes how to:</span></span>

- <span data-ttu-id="c560e-106">管理数据库日志记录的安全性和性能</span><span class="sxs-lookup"><span data-stu-id="c560e-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="c560e-107">设置数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c560e-107">Set up database logging</span></span>
- <span data-ttu-id="c560e-108">清理数据库日志</span><span class="sxs-lookup"><span data-stu-id="c560e-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="c560e-109">数据库日志记录概述</span><span class="sxs-lookup"><span data-stu-id="c560e-109">Overview of database logging</span></span>

<span data-ttu-id="c560e-110">数据库日志记录跟踪对 Microsoft Dynamics 365 Human Resources 表和字段的特定更改。</span><span class="sxs-lookup"><span data-stu-id="c560e-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="c560e-111">这些更改包括插入、更新或删除。</span><span class="sxs-lookup"><span data-stu-id="c560e-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="c560e-112">数据库日志记录在数据库日志表中存储对表或字段的更改的记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="c560e-113">数据库日志记录的业务用途包括：</span><span class="sxs-lookup"><span data-stu-id="c560e-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="c560e-114">创建对包含敏感信息的特定表的更改的审核记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="c560e-115">跟踪单个事务。</span><span class="sxs-lookup"><span data-stu-id="c560e-115">Tracking single transactions.</span></span> <span data-ttu-id="c560e-116">数据库日志记录不用于跟踪在批处理作业中运行的自动事务。</span><span class="sxs-lookup"><span data-stu-id="c560e-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="c560e-117">数据库日志记录的安全性</span><span class="sxs-lookup"><span data-stu-id="c560e-117">Security for database logging</span></span>

<span data-ttu-id="c560e-118">数据库日志可能包含敏感数据。</span><span class="sxs-lookup"><span data-stu-id="c560e-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="c560e-119">将访问限制为仅包括需要访问日志数据的安全角色。</span><span class="sxs-lookup"><span data-stu-id="c560e-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="c560e-120">数据库日志记录和性能</span><span class="sxs-lookup"><span data-stu-id="c560e-120">Database logging and performance</span></span>

<span data-ttu-id="c560e-121">尽管从业务角度来看很有价值，但是数据库日志记录在资源使用和管理方面可能会非常昂贵。</span><span class="sxs-lookup"><span data-stu-id="c560e-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="c560e-122">数据库日志记录的性能影响包括：</span><span class="sxs-lookup"><span data-stu-id="c560e-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="c560e-123">数据库日志表会快速增长，导致数据库大小增加。</span><span class="sxs-lookup"><span data-stu-id="c560e-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="c560e-124">增长取决于您决定保留的记录的数据量。</span><span class="sxs-lookup"><span data-stu-id="c560e-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="c560e-125">默认情况下，数据库日志表仅维护 30 天的日志数据。</span><span class="sxs-lookup"><span data-stu-id="c560e-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="c560e-126">数据库日志记录可能会对长期运行的自动化流程产生不利影响，如长期运行的数据导入。</span><span class="sxs-lookup"><span data-stu-id="c560e-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="c560e-127">最佳实践</span><span class="sxs-lookup"><span data-stu-id="c560e-127">Best practices</span></span>

<span data-ttu-id="c560e-128">为了提高性能，请通过选择要记录的特定字段而不是整个表来限制日志条目。</span><span class="sxs-lookup"><span data-stu-id="c560e-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="c560e-129">为了帮助保持整体性能，数据库日志记录限制为 20 个表。</span><span class="sxs-lookup"><span data-stu-id="c560e-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="c560e-130">各个字段只能记录更新。</span><span class="sxs-lookup"><span data-stu-id="c560e-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="c560e-131">设置数据库日志记录</span><span class="sxs-lookup"><span data-stu-id="c560e-131">Set up database logging</span></span>

<span data-ttu-id="c560e-132">您可以使用 **记录数据库更改** 向导来设置数据库日志记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="c560e-133">此向导提供了一种灵活的方式来设置表或字段的日志记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="c560e-134">转到 **系统管理 > 链接 > 数据库 > 数据库日志设置**。</span><span class="sxs-lookup"><span data-stu-id="c560e-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="c560e-135">选择 **新** 启动 **记录数据库更改** 向导。</span><span class="sxs-lookup"><span data-stu-id="c560e-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="c560e-136">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c560e-136">Select **Next**.</span></span> 
3. <span data-ttu-id="c560e-137">在向导的 **表和字段** 页面上，选择要启用数据库日志记录的表和字段，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c560e-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="c560e-138">数据库日志记录不适用于 Human Resources 数据库中的所有表。</span><span class="sxs-lookup"><span data-stu-id="c560e-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="c560e-139">选择列表下面的 **显示所有表** 可展开表和字段的列表，以显示数据库日志记录可用的所有数据库表，但这将是数据库表的完整列表的子集。</span><span class="sxs-lookup"><span data-stu-id="c560e-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="c560e-140">在向导的 **更改类型** 页面上，选择要跟踪每个表和字段的更改的数据操作，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c560e-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="c560e-141">有关可用于日志记录的数据操作的描述，请参阅下面的表。</span><span class="sxs-lookup"><span data-stu-id="c560e-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="c560e-142">在 **完成** 页面上，查看将要进行的更改，然后选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="c560e-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="c560e-143">操作​</span><span class="sxs-lookup"><span data-stu-id="c560e-143">Operation</span></span> | <span data-ttu-id="c560e-144">说明</span><span class="sxs-lookup"><span data-stu-id="c560e-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="c560e-145">跟踪新交易记录</span><span class="sxs-lookup"><span data-stu-id="c560e-145">Track new transactions</span></span> | <span data-ttu-id="c560e-146">为在表中创建的新记录创建日志。</span><span class="sxs-lookup"><span data-stu-id="c560e-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="c560e-147">更新</span><span class="sxs-lookup"><span data-stu-id="c560e-147">Update</span></span> | <span data-ttu-id="c560e-148">为表记录的更新或表中单独选择的字段的更新创建日志。</span><span class="sxs-lookup"><span data-stu-id="c560e-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="c560e-149">如果选择表的日志更新，将在每次更新表上任何记录的任何字段时创建日志记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="c560e-150">如果选择特定字段的日志更新，仅在更新表记录的这些字段时创建日志记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="c560e-151">Delete</span><span class="sxs-lookup"><span data-stu-id="c560e-151">Delete</span></span> | <span data-ttu-id="c560e-152">为从表中删除的记录创建日志。</span><span class="sxs-lookup"><span data-stu-id="c560e-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="c560e-153">重命名键</span><span class="sxs-lookup"><span data-stu-id="c560e-153">Rename key</span></span> | <span data-ttu-id="c560e-154">重命名表键后，创建日志记录。</span><span class="sxs-lookup"><span data-stu-id="c560e-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="c560e-155">清理数据库日志</span><span class="sxs-lookup"><span data-stu-id="c560e-155">Clean up database logs</span></span>

<span data-ttu-id="c560e-156">您可以使用以下选项删除全部或部分数据库日志：</span><span class="sxs-lookup"><span data-stu-id="c560e-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="c560e-157">选择特定表的所有日志。</span><span class="sxs-lookup"><span data-stu-id="c560e-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="c560e-158">选择数据库日志的特定类型。</span><span class="sxs-lookup"><span data-stu-id="c560e-158">Select specific types of database log.</span></span>
- <span data-ttu-id="c560e-159">选择创建日志的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c560e-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="c560e-160">要设置数据库日志清理，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c560e-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="c560e-161">转到 **系统管理 > 链接 > 数据库 > 数据库日志**。</span><span class="sxs-lookup"><span data-stu-id="c560e-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="c560e-162">选择 **清理日志**。</span><span class="sxs-lookup"><span data-stu-id="c560e-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="c560e-163">通过输入以下选项之一，选择用于选择要删除的日志的方法：</span><span class="sxs-lookup"><span data-stu-id="c560e-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="c560e-164">表 ID</span><span class="sxs-lookup"><span data-stu-id="c560e-164">Table ID</span></span>
   - <span data-ttu-id="c560e-165">日志的类型</span><span class="sxs-lookup"><span data-stu-id="c560e-165">Type of log</span></span>
   - <span data-ttu-id="c560e-166">创建日期和时间</span><span class="sxs-lookup"><span data-stu-id="c560e-166">Created date and time</span></span>

3. <span data-ttu-id="c560e-167">使用 **数据库日志清理** 选项卡确定何时运行日志清理任务。</span><span class="sxs-lookup"><span data-stu-id="c560e-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="c560e-168">默认情况下，数据库日志保留 30 天。</span><span class="sxs-lookup"><span data-stu-id="c560e-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
