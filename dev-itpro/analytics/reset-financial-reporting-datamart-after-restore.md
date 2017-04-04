---
title: "在还原数据库后重置财务报表数据市场"
description: "此主题描述如何在还原工序数据库的 Microsoft Dynamics 后重置财务报表数据市场 365。"
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
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
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>在还原数据库后重置财务报表数据市场

此主题描述如何在还原工序数据库的 Microsoft Dynamics 后重置财务报表数据市场 365。 

存在一些您可能需要工序还原您的数据库的 Dynamics 365 从备份或复制来自其他环境的数据库的若干情况。 在发生此情况时，还需要执行步骤确保相应的财务报表数据工序为市场数据库正确使用被还原的 Dynamics 365。 如果您具有的与市场重置财务报表数据的问题在还原 Dynamics 365 之外的原因的操作的数据库，请参阅 Management Reporter 数据市场重置 [] (https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) 以索取更多信息。 请注意{{在此：in}}流程中的步骤操作为 5 月 2016 年 (应用版本 7.0.1265.23014 和财务报告版本 7.0.10000.4) 和更高 365 Dynamics 的支持。 如果您具有较早发行本工序的 Dynamics 365，请与我们的帮助的支持团队可用。

## <a name="export-report-definitions"></a>导出报表定义
首先，则导出在报表设计器的导航报表设计，使用以下步骤：

1.  在报表设计器中，转到**公司** &gt; ** **构建基块组。
2.  选择导出的构建基块组，然后单击** **导出。 **注释：**有关工序的 Dynamics 365，只有一个构建基块组支持，礼品**默认**。
3.  选择要导出的报表定义：
    -   要导出您的所有报表定义和关联的构建基块，请单击**“全选”**。
    -   要导出特定报表、行、列、树或维度集，请单击相应选项卡，然后选择要导出的项。 按住 Ctrl 键选择选项卡中的多个项。 在您选择要导出的报表时，关联的行、列、树和维度集选择。

4.  单击** **导出。
5.  输入文件名和选择要导出的报表定义保存的安全位置。
6.  Click **Save**.

文件可以复制或上载存放在安全位置，它允许导入到不同的环境。其他时间。 有关使用 Microsoft Azure 存储帐户的信息可以查找在 [使用命令行 AzCopy 实用程序] (https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) 的转移数据。 **注释：** Microsoft 不提供一存储帐户作为您的 Dynamics 365 协议的工序的一部分。 您必须将采购帐户或使用从单独 Azure 的预订中的单元帐户。 **重要：**请注意 D 驱动器的行为。Azure 的虚拟机的。 不要收留您的导出的构建基块组将永久。 有关临时驱动器的详细信息，请参阅 Windows Azure 虚拟机了解在 [] (https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) 临时的驱动器。

## <a name="stop-services"></a>停止服务
通过使用 services.msc，桌面使用远程连接到环境中正在的任何计算机和停止以下 Windows 服务：

-   万维网发行服务 (在所有 AOS 计算机)
-   工序批次管理业务的 Microsoft Dynamics 365 (在非专用只有 AOS 计算机)
-   Management Reporter 2012 提供进程服务 (仅在 BI 计算机)

这些服务将到 Dynamics 365 打开的可用操作的数据库。

## <a name="reset"></a>重置
#### <a name="locate-the-latest-dataupgradezip-package"></a>找到最新的 DataUpgrade.zip 包装

找到最新的 DataUpgrade.zip 使用包装方向查找在 [] (请下载 DataUpgrade.zip 脚本。\ \ {{升级：upgrade-data-to-latest-update.md}}迁移升级{{数据：upgrade-data-to-latest-update.md}} {{对：upgrade-data-to-latest-update.md}} {{后：upgrade-data-to-latest-update.md}} {{update.md:upgrade-data-to-latest-update.md}})。 方向说明如何查找数据升级包装的正确的版本您的环境中的。

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>脚本工序执行数据库的 Dynamics 365

执行以下脚本工序数据库的 Dynamics 365 (尚未进行财务报告数据库)。

-   DataUpgrade.zip\\AosService\\写电影脚本\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\写电影脚本\\GrantAzViewChangeTracking.sql

这些角色脚本确保用户、更改和跟踪设置正确。

#### <a name="execute-powershell-command-to-reset-database"></a>执行 PowerShell 订单重置数据库

执行以下命令，直接在 AOS 计算机。重置，Dynamics 365 之间的集成工序和财务报告的：

1.  Windows PowerShell 以管理员身份打开。
2.  执行的操作：F:
3.  执行的操作：F 的方法：\\MRApplicationService\\MRInstallDirectory
4.  执行的操作：模块导入。\\服务器\\MRDeploy\\MRDeploy.psd1
5.  执行的操作：重置 DatamartIntegration 的原因-其他- ReasonDetail“&lt;我的”重置的原因&gt;
    -   您将请求输入“Y”为"已确认"。

参数的说明：

-   有效值为-原因是：服务，BADDATA，其他。
-   - ReasonDetail 参数是普通。
-   原因和 reasonDetail 在遥测/环境监控中记录。

## <a name="start-services"></a>启动该服务
使用 services.msc 重新启动您可以及早停止服务：

-   万维网发行服务 (在所有 AOS 计算机)
-   工序批次管理业务的 Microsoft Dynamics 365 (在非专用只有 AOS 计算机)
-   Management Reporter 2012 提供进程服务 (仅在 BI 计算机)

## <a name="import-report-definitions"></a>导入定义报表
您的导入从报表设计器的报表设计，在导入期间使用创建的文件：

1.  在报表设计器中，转到**公司** &gt; ** **构建基块组。
2.  选择导出的构建基块组，然后单击** **导出。 **注释：**有关工序的 Dynamics 365，只有一个构建基块组支持，礼品**默认**。
3.  **选择默认**构建基块并单击** **导入。
4.  选择包含导出的报表定义的文件单击** **并打开。
5.  在“导入”对话框中，选择要导入的报表定义：
    -   要导入所有报表定义和支持构建基块，请单击**全选**。
    -   要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。

6.  Click **Import**.



