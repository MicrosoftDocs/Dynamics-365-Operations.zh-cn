---
title: ER 模板的备份存储
description: 此主题介绍如何使用电子申报 (ER) 备份存储来恢复模板。
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b4e783f79b02c77a27fc59c2f4be8a192f2f476
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248692"
---
# <a name="backup-storage-of-er-templates"></a>ER 模板的备份存储

[!include [banner](../includes/banner.md)]

业务用户可使用[电子申报 (ER) 框架](general-electronic-reporting.md)根据各个国家和地区的法律要求配置传出文档的格式。 配置的 ER 格式可使用预定义的模板生成各种格式（如 Microsoft Excel 工作簿、Microsoft Word 文档或 PDF 文档）的传出文档。 已经使用为生成的文档配置的数据流所需数据填充了模板。

可以在 ER 解决方案中发布配置的每种格式。 可以将每种 ER 解决方案从一个 Finance and Operations 实例导出，然后导入到另一个实例中。

ER 框架使用[文档管理框架](../../fin-and-ops/organization-administration/configure-document-management.md)保留当前 Finance and Operations 实例所需模板。 可以根据 ER 框架的设置，将 Microsoft Azure Blob 存储或 Microsoft SharePoint 文件夹选作模板的物理主存储位置。 （有关详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。）DocuValue 表中是每个模板的单个记录。 在每个记录中，**AccessInformation** 字段中存储模板文件在配置的存储位置内的路径。

管理 Finance and Operations 实例时，可以决定将当前实例迁移到其他位置。 例如，您可以将生产实例迁移到新的沙盒环境。 如果将 ER 框架配置为把模板存储到 Blob 存储中，则新沙盒环境中的 DocuValue 表引用生产环境中的 Blob 存储实例。 但是，不能从沙盒环境访问此实例，因为迁移过程不支持迁移 Blob 存储中的项目。 因此，如果尝试运行使用模板的 ER 格式来生成业务文档，将发生异常，并通知您缺少模板。 还将引导您使用 ER 清理工具删除再重新导入其中包含此模板的 ER 格式配置。 因为您可能有多个 ER 格式配置，所以此过程可能需要很长时间。

ER 模板的备份存储功能可帮助您创建模板，这样始终可以使用这些模板来生成业务文档。

> [!NOTE]
> 仅当已选择 Blob 存储作为 ER 模板的物理存储位置，才能使用此功能。

对于此功能，如果发生以下事件，将把当前环境中新 ER 格式配置的每个模板自动保存到模板的备份存储位置（ERDocuDatabaseStorage 数据库表）：

- 导入其中包含模板的新 ER 格式配置。
- 完成其中包含模板的 ER 格式配置的草稿版本。

将模板的备份副本作为应用程序数据库的一部分迁移到 Finance and Operations 的新实例。

如果需要 ER 格式的模板才能生成传出文档（例如，为了处理其中包含付款通知和控制报告的供应商付款），但是未在主存储位置中找到所需模板，则会发生以下事件：

- 如果备份存储位置中有此模板，则会从备份存储位置自动提取该模板，还原到主存储位置，用于当前执行。
- 将通过操作中心向为其分配了**电子申报开发人员**或**系统管理员**角色的每位用户通知发生了缺少模板问题。 显示的消息取决于**自动运行受损附件批量还原**参数的值：

    - 如果此参数设置为**关**，则此消息将建议您开始执行批处理流程以自动修复其他 ER 格式配置模板的相似问题。 此消息中有一个链接，可用于启动批处理流程。
    - 如果此参数设置为**开**，此消息将通知您，说明已发现了缺少模板问题，并且已自动安排了新的批处理流程**通过内部数据库备份还原受损模板**。 此批处理流程将自动修复其他模板的相似问题。

若要设置**自动运行受损附件批量还原**参数，请完成以下步骤：

1. 在 Finance and Operations 中，打开**组织管理 \> 电子申报 \> 配置**页。
2. 在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。
3. 在**用户参数**对话框中，设置**自动运行受损附件批量还原**参数所需值。

> [!NOTE]
> 此参数定义为应用程序用户，并特定于记录的公司。

![ER 配置页](./media/GER-BackupTemplates-1.png)

下图显示当**自动运行受损附件批量还原**参数设置为**开**时显示的消息的示例。

![供应商付款日记帐页](./media/GER-BackupTemplates-2.png)

下图显示**批处理作业**页上的**通过内部数据库备份还原受损模板**批处理流程。

![批处理作业页](./media/GER-BackupTemplates-3.png)

已完成的**通过内部数据库备份还原受损模板**批处理流程的执行日志中包含有关已从备份存储位置还原到主存储位置的模板的信息。

![批处理作业历史记录页](./media/GER-BackupTemplates-4.png)

命若琴弦看，已开启 ER 格式配置中的模板的自动创建备份副本流程。 若要停止创建模板的备份副本，请将**电子申报参数**页**附件**选项卡上的**停止制作模板的备份副本**选项设置为**是**。 可从**电子申报**工作区打开此页。

如果将**停止制作模板的备份副本**选项设置为**是**，但是不希望保留以前创建的模板备份副本，请选择**电子申报参数**页上的**清理备份存储**。

如果已将您的环境升级到 Finance and Operations 版本 10.0.5（2019 年 10 月），并希望迁移到其中包含可运行的 ER 格式配置的新环境，请在迁移前选择**电子申报参数**页上的**填充备份存储**。 此按钮用于开始创建所有可用模板的备份副本，所以可将其存储到模板的 ER 备份存储位置中。

![“电子申报参数”页面](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>支持的部署

在 Finance and Operations 版本 10.0.5 中，只有云部署中才支持 ER 模板备份存储功能。

## <a name="additional-resources"></a>其他资源

[电子报告概览](general-electronic-reporting.md)

[配置电子报告框架](electronic-reporting-er-configure-parameters.md)
