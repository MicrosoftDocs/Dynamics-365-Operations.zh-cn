---
title: "升级转换测试"
description: "此主题说明如何测试在您关闭 AX 2012 之后但打开 Dynamics 365 for Finance and Operations Enterprise Edition 之前发生的任务。"
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
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
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: zh-cn
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>升级转换测试

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*转换*是我们对实施新系统最终流程使用的术语。 该转换流程包括在关闭 Microsoft Dynamics AX 2012 后但打开 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 之前发生的任务。 升级转换测试的目的是实践转换流程，以帮助保证参与实际转换到实施的每个人都将获得一个平稳的体验。

转换期间有两个主要工作流：

- **技术工作流** –此工作流包括数据升级执行流程。 您的公司将对允许的停机时间量执行限制。 在此停机时间期间，AX 2012 和 Finance and Operations 都不可用。 此工作流可能必须优化数据升级过程以满足企业的停机时间限制。
- **功能工作流** - 此工作流包括在完成数据升级后执行的配置任务。 必须记录和量化所有这些任务，并对它们分配资源，因为功能工作流和技术工作流都必须在企业的停机时间限制内。

下图显示在生产环境中发生的转换到实施的总体流程。

![转换流程](./media/cutover_1.png)

此转换流程与沙盒环境中的基本数据升级在以下方面存在差异：

- AX 2012 数据库不进行复制，仅备份，然后再修改原始数据库。 此方法更加快速，且当需要回滚时，备份提供回滚。
- 因为 Finance and Operations 的生产环境具有受限制的访问权限，因此之前对应用程序对象服务器 (AOS) 的沙盒实例执行的任务现在由 Microsoft DSE 团队执行。 这些任务包括下载和导入 bacpac 文件，以及运行 MajorversionDataUpgrade.zip 包。
- 我们增加了以下任务：

    - 执行烟雾测试。
    - 完成应用程序设置任务。 此步骤可能较大，具体取决于使用的功能。 在此步骤期间，功能团队配置新应用程序功能，以便随时准备在升级的系统中使用。
    - 允许用户返回。 通知您的用户群升级已完成，他们可以再次使用系统。

## <a name="technical-workstream"></a>技术工作流

技术工作流涉及各种技术团队成员：数据库管理员 (DBA)、AX 2012 系统管理员、服务器管理员以及熟悉 AX 2012 和 Finance and Operations 的开发人员。 此主题将阐释哪些任务涉及哪些角色。

在转换测试期间，技术团队主要关注数据升级流程的性能和可靠性测试，以确保满足企业的停机时间限制。 此流程涉及硬件和软件的许多元素。 其中一些为本地元素，另一些为 Microsoft 云中的元素。 此外还涉及自定义应用程序代码和标准代码的许多元素。 此测试的结果应对您的环境的转换流程有信心。

### <a name="turn-off-the-ax-2012-aos-instances"></a>关闭 AX 2012 AOS 实例

此任务涉及 AX 2012 系统管理员和服务器管理员。

应验证以下区域：

- **在转换时运行的批处理作业** –长时间运行已经开始运行的批处理作业将防止系统停止。 提前计划，以便您可以在预期的时刻停止 AOS 实例。 您可能必须安排批次，以便在您关闭 AX 2012 前提前一段时间完成这些批次。
- **集成系统** - 您可能具有其他与 AX 2012 环境集成的系统。 您在计划关闭 AX 2012 时必须考虑这些系统。 例如，您可能必须在关闭 AX 2012 前提前一段时间关闭集成系统，以便可以完成剩余的飞行中交易。 对集成系统的要求在企业与企业之间有很大的差异。 因此，您的专家团队必须单独计划此方案。

### <a name="create-a-backup-of-the-ax-2012-database"></a>创建 AX 2012 数据库的备份

此任务涉及 DBA。 如果需要回滚，将使用该备份。 它还将用作参考点保留一段时间并显示转换时刻的系统状态。

应验证以下区域：

- 获取备份流程的具体时间。
- 调整使用的备份选项（如压缩与非压缩）以帮助保证尽可能最快速的备份。

### <a name="export-the-database-to-bacpac"></a>将数据库导出到 bacpac

此任务涉及 DBA。 此任务的输出是导出文件，该文件将被上载到 Microsoft Azure 用于新系统。

应验证以下区域：

- 获取备份流程的具体时间。
- 优化导出流程以帮助保证尽可能最快速的体验。 优化可能需要以下任务：

    - 测量导出期间的系统资源，如 CPU、磁盘 I/O 和内存。
    - 如果找到资源瓶颈，请创建缓解计划。 通常，您将通过分配更多的必需资源缓解这些瓶颈。

### <a name="upload-the-bacpac-file-to-azure-storage"></a>将 bacpac 文件上载到 Azure 存储

此任务涉及 DBA 或服务器管理员。 在此任务期间，bacpac 文件被移动到 Azure。

应验证以下区域：

- 选择将要用于上载的计算机，并确保 Azure 存储资源管理器工具已配置并立即可用。
- 通过多次测量获取上载流程的时间。 上载时间将根据您的互联网连接速度和 Azure 数据中心相对于您所在位置的地理位置而有差异。

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>下载 bacpac 文件并导入到 Azure SQL 数据库

在实施时发生此任务时，将由 Microsoft DSE 团队执行。 但是，在转换测试期间，它涉及您的 DBA。 此任务的输出是导出文件，该文件将被上载到 Azure 用于新系统。

应验证以下区域：

- 获取导入流程的具体时间。
- 优化导出流程以帮助保证尽可能最快速的体验。 优化可能需要以下任务：

    - 在导出期间测量系统资源。 下面举了一些示例加以说明：

        - **在 AOS 计算机上：**CPU、磁盘 I/O 和内存
        - **在 Azure SQL 数据库实例上：**SQL 数据库吞吐量 (DTU)。 您可以通过查看 sys.dm 资源统计系统视图监控来自 AOS 计算机上的 Microsoft SQL Server Management Studio 的 Azure SQL DTU。

    - 如果找到资源瓶颈，请创建缓解计划。 通常，您将通过分配更多的必需资源缓解这些瓶颈。 由于此计算机由 Microsoft 托管，如果您确定是瓶颈，您必须提交请求到 Microsoft 以增加资源。

### <a name="run-the-majorversiondataupgradezip-package"></a>运行 MajorVersiondataUpgrade.zip 包

在实施时发生此任务时，将由 Microsoft DSE 团队执行。 但是，在转换测试期间，它涉及开发人员。 在此任务期间，旧数据库结构转换为新系统的结构。

数据库同步流程作为此任务的一部分运行。 数据库同步在某些情况下可能需要较长的时间，例如当表上的聚集索引更改时，因为此操作是 SQL 中的一个昂贵的操作。

我们强烈建议您第一次在开发环境中执行您的分析和调试流程。 在沙盒环境中，调试和分析选项受到更大的限制。 其目的是在您执行转换测试时必须解决的问题很少或没有。

应验证以下区域：

- 获取导入流程的具体时间。
- 优化该流程以帮助保证获得最快速的体验。 优化可能需要以下任务：

    - 通过 ReleaseUpdateScriptsExecution 表监控单个升级脚本的性能。
    - 调整脚本以优化性能。 此任务可能要求您自定义脚本的 X++ 代码以针对您的数据集进行优化。
    - 通过使用 Microsoft Dynamics Lifecycle Services (LCS) 监控或 Management Studio 中的 sys.dm_resources_stats 系统视图监控 Azure SQL DTU。 如果资源已达到最高极限，您可能必须从 Microsoft DSE 团队申请更高的数据库级别。

### <a name="roll-back-to-ax-2012"></a>回滚到 AX 2012

此任务的目标是通过使用在关闭 AX 2012 时进行备份还原数据库，然后再重新打开 AX 2012。 可能还必须还原集成系统的状态。 但是，由于集成系统因不同企业而异，您必须根据自己的特定情况单独计划此方案。 尽管您必须回滚的可能性不大，但具有一个经测试的流程以备您所需非常重要。

## <a name="functional-workstream"></a>功能工作流

在数据升级后，需要在新环境中执行若干配置任务。 此工作流的目标是对所有配置任务进行记录和量化，并对每个任务分配资源，以帮助保证在停机时间窗口期间可以与技术工作流一同完成这些任务。

通常，功能任务涉及到更改特定系统参数的值或其他配置数据。 这些任务通过完整功能测试传递进行确定，完整功能测试传递是与转换测试单独分开的活动。 确定此类型的任务后，应与功能资源和您的开发人员一同进行审核。

更大的更改可能要求编写新的自定义数据升级脚本以在数据升级流程中更新数据。 但是，功能资源可以通过数据升级后的新系统手动运行较小的更改。

必须对具有新数据升级脚本的较大更改进行测试。 因此，必须运行 MajorVersionDataUpgrade.zip 包的一个或多个额外迭代。 再次权衡运行包的成本与手动录入数据的成本十分重要。

对于每次手动更改，必须将任务添加到转换计划文档。 此任务必须显示以下详细信息：

-   任务是什么，必须执行什么？
-   谁必须执行！
-   需要多长时间？

