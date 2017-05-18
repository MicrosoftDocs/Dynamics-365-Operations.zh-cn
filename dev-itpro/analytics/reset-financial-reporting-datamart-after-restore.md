---
title: "还原数据库后重置财务申报数据市场"
description: "此主题介绍如何在还原 Microsoft Dynamics 365 for Operations 数据库之后重置财务申报数据市场。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d4ce390c62cbfb1f693410b004aa296c0ed75eb2
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>还原数据库后重置财务申报数据市场

[!include[banner](../includes/banner.md)]


此主题介绍如何在还原 Microsoft Dynamics 365 for Operations 数据库之后重置财务申报数据市场。 

有几种方案您可能需要从备份还原 Dynamics 365 for Operations 数据库或从另一环境复制数据库。 发生这种情况时，可能还需要执行相应步骤以确保财务申报数据市场正确使用还原的 Dynamics 365 for Operations 数据库。 如果对除还原 Dynamics 365 for Operations 数据库之外的原因导致重置财务申报数据市场有疑问，请参阅[重置 Management Reporter 数据市场](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/)获取详细信息。 请注意，此流程中的步骤支持 Dynamics 365 for Operation May 2016 版本（应用程序版本 7.0.1265.23014 和财务申报版本 7.0.10000.4）及更高版本。 如果您的 Dynamics 365 for Operations 版本较低，请联系我们的支持团队获取协助。

## <a name="export-report-definitions"></a>导出报表定义
首先，使用以下步骤导出报表设计器中的报表设计：

1.  在报表设计器中，转至**公司** &gt; **构建基块组**。
2.  选择要导出的构建基块组，然后单击**导出**。 **注释：**对于 Dynamics 365 for Operations，仅支持一个构建块组（即**默认**）。
3.  选择要导出的报表定义：
    -   要导出您的所有报表定义和关联的构建基块，请单击**“全选”**。
    -   要导出特定报表、行、列、树或维度集，请单击相应选项卡，然后选择要导出的项。 按住 Ctrl 键选择选项卡中的多个项。 当选择要导出的报表时，将选择关联的行、列、树和维度集。

4.  单击**导出**。
5.  输入文件名，然后选择要用于保存所导出报表定义的安全位置。
6.  单击**保存**。

可将文件复制或上传到安全位置，使其可在其他时间导入到其他环境中。 可在[使用 AzCopy 命令行实用程序传输数据](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy)中找到有关使用 Microsoft Azure 存储帐户的信息。 
> [!NOTE]
> 根据您的 Dynamics 365 for Operations 协议，Microsoft 不提供存储帐户。 您必须购买存储帐户，或使用单独 Azure 订阅的存储帐户。 
> [!WARNING]
> 请注意 Azure 虚拟机 D 盘的行为。 请勿将导出的构建块永久保留在此处。 有关临时驱动器的详细信息，请参阅[了解 Windows Azure 虚拟机上的临时驱动器](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)。

## <a name="stop-services"></a>停止服务
使用远程桌面连接到环境中的所有计算机，并通过使用 services.msc 停止以下 Windows 服务：

-   万维网 Web 发布服务（在所有 AOS 计算机上）
-   Microsoft Dynamics 365 for Operations Batch Management Service（仅限非私有 AOS 计算机上）
-   Management Reporter 2012 Process Service（仅限于 BI 计算机上）

这些服务具有到 Dynamics 365 for Operations 数据库的开放连接。

## <a name="reset"></a>重置
#### <a name="locate-the-latest-dataupgradezip-package"></a>找到最新的 DataUpgrade.zip 包

使用[下载 DataUpgrade.zip 脚本](..\migration-upgrade\upgrade-data-to-latest-update.md) 中的说明下载 DataUpgrade.zip 包。 这些说明介绍如何找到您的环境的正确数据升级包版本。

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>对 Dynamics 365 for Operations 数据库执行脚本

对 Dynamics 365 for Operations 数据库（而非对财务申报数据库）运行以下脚本。

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

这些脚本确保用户、角色和更改跟踪设置正确无误。

#### <a name="execute-powershell-command-to-reset-database"></a>执行 PowerShell 命令重置数据库

直接在 AOS 计算机上执行以下命令，以便重置 Dynamics 365 for Operations 与财务申报之间的集成：

1.  以管理员身份打开 Windows PowerShell。
2.  执行：F:
3.  执行：cd F:\\MRApplicationService\\MRInstallDirectory
4.  执行：Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  执行：Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   将请您输入“Y”予以确认。

参数的说明：

-   -Reason 的有效值为：SERVICING、BADDATA、OTHER。
-   -ReasonDetail 参数为自由文本。
-   原因和 reasonDetail 将记录到 telemetry/environment monitoring 中。

## <a name="start-services"></a>启动服务
使用 services.msc 重新启动您前面停止的服务：

-   万维网 Web 发布服务（在所有 AOS 计算机上）
-   Microsoft Dynamics 365 for Operations Batch Management Service（仅限非私有 AOS 计算机上）
-   Management Reporter 2012 Process Service（仅限于 BI 计算机上）

## <a name="import-report-definitions"></a>导入报表定义
使用导出期间创建的文件从报表设计器导入您的报表设计：

1.  在报表设计器中，转至**公司** &gt; **构建基块组**。
2.  选择要导出的构建基块组，然后单击**导出**。 
    > [!NOTE]
    > 对于 Dynamics 365 for Operations，仅支持一个构建块组（即**默认**）。
3.  选择**默认**构建块，然后单击**导入**。
4.  选择包含所导出报表定义的文件，然后单击**打开**。
5.  在“导入”对话框中，选择要导入的报表定义：
    -   要导入所有报表定义和支持构建基块，请单击**全选**。
    -   要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。

6.  单击**导入**。





