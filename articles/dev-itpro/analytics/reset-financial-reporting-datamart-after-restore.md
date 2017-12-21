---
title: "重置财务报告数据市场"
description: "此主题描述如何重置财务报告数据市场。"
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: zh-cn
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>重置财务报告数据市场

[!include[banner](../includes/banner.md)]

本主题说明如何重置以下版本的财务报告数据市场：

- Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.2.6.0 及更高版本
- Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.0.10000.4 及更高版本
- Microsoft Dynamics 365 for Finance and Operations Enterprise edition（本地）

若要获取 Finance and Operations 财务报告版本 7.2.6.0，您可以从 <https://support.microsoft.com/en-us/help/4052514> 下载 KB 4052514。

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>重置 Finance and Operations 财务报告版本 7.2.6.0 及更高版本的财务报告数据市场

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>从报表设计器重置财务报告数据市场

> [!NOTE]
> 此流程中的步骤为 Finance and Operations 财务报告版本 7.2.6.0 及更高版本提供支持。 如果您有较早的版本，请与支持团队联系获取帮助。

在特定情况下，您可能必须重置财务报告的数据市场。 您可以在报表设计器客户端完成此任务。 以下是一些您可能必须重置数据市场的情况：

- Finance and Operations 数据库已还原，但数据市场数据库未还原。
- 您看到某个期间内有不正确的数据。
- 支持人员在故障排除步骤中指导您重置数据市场。

数据市场重置应仅在数据库的处理量较小时进行。 财务报告在重置流程中将不可用。

#### <a name="reset-the-data-mart"></a>重置数据市场

要重置数据市场，在报表设计器中，在**工具**菜单中，选择**重置数据市场**。 出现的对话框具有两部分：**统计**和**重置**。

[![“重置数据市场”对话框](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>集成尝试次数

**集成尝试次数**网格显示系统尝试集成交易的次数。 如果最开始的少数尝试不成功，系统将继续尝试在几天中集成数据。 如果尝试次数为 8 或更多，以及存在许多维度组合或交易记录，那么您就知道必须重置数据市场了。 在此情况下，数据将不报告。

##### <a name="data-status"></a>数据状态

**数据状态**网格在数据市场中提供交易、汇率和维度值的快照。 大量的过时记录指示记录已发生了许多更新。 此情况可能导致更长的报告生成时间。

##### <a name="misaligned-main-account-categories"></a>未对齐的主科目类别

如果您在使用 Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.2.1 以前的一个版本，且如果重命名科目并将科目在科目类别之间移动，您可能必须重置数据市场。 这些操作可能导致主科目类别不对齐。 **未对齐的主科目类别**字段显示您是否遇到此问题。

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>重置 Finance and Operations 财务报告版本 7.2.6.0 的数据市场

要重置 Finance and Operations 财务报告 7.2.6.0 及以前版本的数据市场，在**重置市场数据**对话框中，选择**重置数据市场**复选框，然后选择**确定**。 您应该只在计划停机期间重置数据市场。

[![“重置数据市场”复选框](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>在 Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.3.0 中重置数据市场并选择原因

如果您确定需要重置数据市场，则选择**重置数据市场**复选框，然后在**原因**字段中选择一个原因。 以下是可用的选项：

- **缺少数据或数据错误** – 根据统计，您确定可能缺少该数据。 在继续之前，我们建议您联系支持人员确定根本原因。
- **还原数据库** – Finance and Operations 数据库已还原，但财务报告数据市场的数据库未还原。
- **其他** – 您出于其他原因重置数据市场。 如果您担心存在问题，请联系支持人员加以确定。

> [!NOTE]
> 在完成步骤前先验证现有的所有任务已完成集成。 您可以通过选择**工具** &gt; **集成状态**来查看集成的状态。

#### <a name="clear-users-and-companies"></a>清除用户和公司

如果您还原了您的数据库，不过随后对用户或公司进行了更改，则选择**清除用户和公司**复选框。 您几乎不必选中此复选框。

当您准备好开始重置流程时，请选择**确定**。 系统将提示您确认已准备好开始流程。 请注意，在重置和之后发生的初始数据集成期间财务报告将不可用。

如果要查看集成的状态，请选择**工具** &gt; **集成状态**以查看集成运行的上次时间和状态。

[![查看集成的状态](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>重置 Finance and Operations 财务报告版本 7.0.10000.4 及更高版本的财务报告数据市场

如果您从备份还原 Finance and Operations 数据库或从其他环境复制该数据库，则必须执行本部分中的步骤，以帮助确保财务报告数据市场正确使用还原的 Finance and Operations 数据库。

> [!NOTE]
> 此流程中的步骤支持 Microsoft Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）（应用程序版本 7.0.1265.23014 和财务报告版本 7.0.10000.4）及更高版本。 如果您的 Finance and Operations 版本较低，请联系支持团队获取协助。

### <a name="export-report-definitions"></a>导出报表定义

首先，按照以下步骤从报表设计器导出报表设计。

1. 在报表设计器中，选择**公司** &gt; **构建基块组**。
2. 选择要导出的构建基块组，然后选择**导出**。

    > [!NOTE]
    > 对于 Finance and Operations，仅支持一个构建块组，即**默认**。

3. 选择要导出的报表定义：

    - 若要导出所有报表定义和关联的构建基块，请选择**全选**。
    - 要导出特定报表、行、列、树或维度集，请选择相应选项卡，然后选择要导出的项。 按住 Ctrl 键选择选项卡上的多个项目。当您选择要导出的报表时，系统将选择关联的行、列、树和维度集。

4. 选择**导出**。
5. 输入文件名，然后选择要用于保存所导出报表定义的安全位置。
6. 选择**保存**。

您可以将该文件复制或上传到安全位置。 通过此方法，文件以后可以导入到不同的环境。 有关如何使用 Microsoft Azure 存储帐户的信息，请参见[使用 AzCopy 命令行实用程序传输数据](/azure/storage/storage-use-azcopy)。

> [!NOTE]
> 根据您的 Finance and Operations 协议，Microsoft 不提供存储帐户。 您必须购买存储帐户，或使用单独 Azure 订阅的存储帐户。

> [!WARNING]
> 请注意 Azure 虚拟机 (VM) D 盘的行为。 请勿在 D 盘上永久储存导出的构建基块组。有关临时驱动器的详细信息，请参阅[了解 Windows Azure 虚拟机上的临时驱动器](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)。

### <a name="stop-services"></a>停止服务

以下 Microsoft Windows 服务具有到 Finance and Operations 数据库的开放连接。 因此，您必须使用 Microsoft 远程桌面连接到环境中的所有计算机，然后使用 services.msc 停止这些服务。

- 万维网 Web 发布服务（在所有应用程序对象服务器 [AOS] 计算机上）
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）
- Management Reporter 2012 Process Service（仅限于商业智能 [BI] 计算机上）

### <a name="reset"></a>重置

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>下载最新的 MinorVersionDataUpgrade.zip 程序包

下载最新的 MinorVersionDataUpgrade.zip 程序包。 有关如何查找并下载数据升级包的正确版本的说明，请参阅[下载最新的数据升级可部署程序包](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)。 无需下载 MinorVersionDataUpgrade.zip 程序包即可升级。 因此，您只需执行该主题的“下载最新的数据升级可部署程序包”部分中的步骤。 您可以跳过主题中的所有其他步骤。

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>对 Finance and Operations 数据库运行脚本

对 Finance and Operations 数据库（而非对财务报告数据库）运行以下脚本：

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

这些脚本帮助确保用户、角色和更改跟踪设置正确无误。

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>运行 Windows PowerShell 命令来重置数据库

在 AOS 计算机上，作为管理员启动 Microsoft Windows PowerShell 并运行以下命令以重置 Finance and Operations 与财务报告之间的集成。

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

以下是 **Reset-DatamartIntegration** 命令中参数的说明：

- **-Reason** 的有效值为 **SERVICING**、**BADDATA** 和 **OTHER**。
- **-ReasonDetail** 参数为自由文本。
- 原因和原因详细信息将记录到 telemetry/environment monitoring 中。

> [!NOTE]
> 在运行命令后，系统将要求您输入 **Y** 来确认您要重置数据库。

#### <a name="restart-services"></a>重新启动服务

使用 services.msc 重新启动您前面停止的服务：

- 万维网 Web 发布服务（在所有 AOS 计算机上）
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）
- Management Reporter 2012 Process Service（仅限于 BI 计算机上）

#### <a name="import-report-definitions"></a>导入报表定义

使用导出期间创建的文件从报表设计器导入您的报表设计。

1. 在报表设计器中，选择**公司** &gt; **构建基块组**。
2. 选择要导出的构建基块组，然后选择**导出**。

    > [!NOTE]
    > 对于 Finance and Operations，仅支持一个构建块组，即**默认**。

3. 选择**默认**构建块，然后选择**导入**。
4. 选择包含所导出报表定义的文件，然后选择**打开**。
5. 在“导入”对话框中，选择要导入的报表定义：

    - 若要导入所有报表定义和关联的构建基块，请选择**全选**。
    - 若要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。

6. 选择**导入**。

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>重置 Finance and Operations（本地）的财务报告数据市场

1. 指导所有用户退出报表设计器和 Finance and Operations 的财务报告区域。
2. 对财务报告数据库 (MRDB) 运行以下脚本。

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. 从 Finance and Operations 数据库 (AXDB) 的 FINANCIALREPORTS 表中截断或删除所有记录。
4. 如果 FINANCIALREPORTVERSION 表在 Finance and Operations 数据库中存在，则从此表中截断或删除所有记录。 如果此表不存在于 Finance and Operations 数据库中，则跳过此步骤。
5. 对财务报告数据库运行 **ResetDatamart.sql** 脚本。 此脚本禁用数据市场集成，删除所有数据市场数据，然后重新启用数据市场集成。

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. 重置后，可以通过对财务报告数据库运行以下查询来手动验证数据重新加载。

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    确认所有行均有 **LastRunTime** 值，且 **StateType** 被设置为 **5**。 **StateType** 值 **5** 表示数据已成功重载。 值 **7** 指示错误状态。 有时，组织层次结构映射在首次运行时具有此状态。 不过，错误状态应会自动解决。

