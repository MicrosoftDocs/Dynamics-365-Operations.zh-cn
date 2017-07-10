---
title: "沙盒环境中的数据升级"
description: "此主题说明如何在沙盒环境中将数据从 AX 2012 升级到 Dynamics 365 for Finance and Operations。"
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: zh-cn
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>沙盒环境中的数据升级

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

此任务的输出是可以在沙盒环境中使用的升级的数据库。 沙盒环境是业务用户和职能团队成员可以在其中验证应用程序功能的环境。 此功能包括从 Microsoft Dynamics AX 2012 提供的自定义项和数据。

我们强烈建议在共享的沙盒环境中允许数据升级流程前先在开发环境中运行该流程，因为此方法将有助于减少成功升级数据所需的总时间。 有关详细信息，请参阅 [开发环境中的数据升级](prepare-data-upgrade.md)。

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>沙盒数据升级流程概览

开始在沙盒环境中升级数据之前，您将已经按照 [开发环境中的数据升级](prepare-data-upgrade.md) 中的说明在开发环境中升级数据。 这两个流程非常相似。 主要差异在于沙盒环境使用 Microsoft Azure SQL 数据库进行数据存储，而开发环境使用 Microsoft SQL Server。 数据库层中的此技术差异要求您稍微修改沙盒环境中的数据升级过程，因为来自 AX 2012 数据库的备份实例不能存储到 SQL 数据库。

![沙盒数据数据升级流程](./media/data-upgrade-sandbox.png)

以下是升级流程中的概括步骤。

1. 创建 AX 2012 数据库的副本。 我们强烈建议您使用副本，因为您必须删除将要导出的副本中的一些对象。
2. 使用名称为 SQLPackage.exe 的免费 SQL Server 工具将复制的数据库导出到 bacpac 文件。 此工具提供可导入到 SQL 数据库的特殊类型的数据库备份。
3. 将 bacpac 文件上载到 Azure 存储。
4. 在沙盒环境中将 bacpac 文件下载到应用程序对象服务器 (AOS) 计算机，然后使用 SQLPackage.exe 导入。 随后必须对导入的数据库运行脚本以重置 SQL 数据库用户。
5. 运行 MajorVersionDataUpgrade.zip 包以对导入的数据库执行数据升级。

## <a name="create-a-copy-of-the-ax-2012-database"></a>创建 AX 2012 数据库的副本

您必须创建正在升级的 AX 2012 数据库的副本，因为您必须从数据库删除一些对象。 这些对象包括任何 Microsoft Windows 身份验证用户。 这些更改使修订的数据库对 AX 2012 不可用。 在此步骤期间，您将创建数据库的一份副本并删除这些对象。

必须由数据库管理员 (DBA) 或者具有类似的知识和经验的人士完成此步骤。

要创建数据库副本，请创建原始数据库的备份，并还原在新的名称下。 确保有足够的空间可用于两个数据库。 您可以在不同的服务器上创建副本。 运行数据库的 SQL Server 实例的版本并不重要。

这是创建数据库副本的代码示例。 必须修改此示例以反映您的特定数据库名称。

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

创建副本后，对其运行以下 Transact-SQL (T-SQL) 脚本。
任务 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>将复制的数据库导出到 bacpac 文件

使用 SQLPackage.exe 工具将复制的数据库导出到 bacpac 文件。 应由 DBA 或具有同等知识的团队成员完成此步骤。

在开始此步骤前安装最新版本的 SQL Server Management Studio 非常重要。 尽管在较早版本的 Management Studio 中存在 SQLPackage，但它在此步骤无法正确运行，除非您先安装最新版本。

此步骤很重要，因为在实施前的停机时间期间必须再次执行导出。 以下是一些提示：

- bacpac 流程占用大量的 I/O 和 CPU。 因此，请在大功率计算机上运行导出。
- 应在托管数据库的计算机上本地运行 SQLPackage。 不要在连接到数据库计算机的本地计算机上运行 SQLPackage，因为此流程对网络的要求也很高。

接下来，以管理员的身份打开**命令提示符**窗口，并运行以下命令。

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

以下是对参数的说明：

- **ssn**（源服务器名称）- 从中导出的 SQL Server 的名称。 在我们的流程中，此参数应始终设置为 **localhost**。
- **sdn**（源数据库名称）- 要导出的数据库的名称。
- **tf**（目标文件）- 要导出到的路径和文件名。 文件夹应已存在，但文件将由流程创建。
- **/p:CommandTimeout** – 每次查询的超时值。 此参数便于导出更大的表而不会超时。

### <a name="upload-the-bacpac-file-to-azure-storage"></a>将 bacpac 文件上载到 Azure 存储

将您的 bacpac 文件上载到 Azure 存储。 参阅 UsingStorageExplorer.docx 任务

### <a name="import-the-bacpac-file-into-sql-database"></a>将 bacpac 文件导入到 SQL 数据库

在此步骤期间，您将导出的 bacpac 文件导入到您的沙盒环境使用的 SQL 数据库实例。 您必须先在您的沙盒 AOS 计算机上安装最新版本的 Management Studio。 然后再使用 SQLPackage.exe 工具导入文件。

您将直接在 AOS 计算机的沙盒环境中执行这些任务，因为具有限制对 SQL 数据库实例访问权限的防火墙规则。 但使用 AOS 计算机可以获取访问权限。

对于导出步骤，在开始导入前必须具有最新版本的 Management Studio。 如果您使用的是旧版本，此步骤将无法运行。

由于性能的原因，我们建议您将 bacpac 文件放在 AOS 计算机的 D 盘。 在 Azure 虚拟机 (VM) 上，D 盘是物理磁盘，性能通常比其他可以磁盘高。

以管理员的身份打开**命令提示符**窗口，并运行以下命令。

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

以下是对参数的说明：

- **tsn**（目标服务器名称）– 要导入到的 SQL Azure 服务器的名称。 在 LCS 中可以找到名称。 添加后缀 **.database.windows.net**。
- **tdn**（目标数据库名称）- 要导入到的数据库的名称。 数据库不应已经存在。 导入流程将创建数据库。
- **sf**（源文件）- 要从其导入的路径和文件名。
- **tp**（目标密码）- 目标 SQL 数据库实例的 SQL 密码。
- **tu**（目标用户）- 目标 SQL 数据库实例的 SQL 用户名。 我们建议您使用 **sqladmin**。 您可以从 LCS 项目检索此用户的密码。
- **/p:CommandTimeout** – 每次查询的超时值。 此参数便于导出更大的表而不会超时。
- **/p:DatabaseServiceObjective** – 创建的数据库的服务层级别。 您可以使用 Management Studio 检查现有数据库的值。 右键单击数据库，然后选择**属性**。

在运行命令后，您将收到以下警告。 您可以放心地忽略它。

![沙盒错误](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>运行 MajorVersionDataUpgrade.zip 包

按照 [在开发、演示或沙盒环境中升级数据](upgrade-data-to-latest-update.md) 中的说明运行数据升级可部署包。

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>在开发环境中升级数据库的副本

在开发环境中升级相同数据库十分有用。 如果您有可用于开发环境的数据库的副本，将更容易调查在升级的沙盒环境中找到的漏洞。

