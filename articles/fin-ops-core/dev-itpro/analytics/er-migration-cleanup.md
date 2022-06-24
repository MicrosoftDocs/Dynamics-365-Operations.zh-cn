---
title: ER 迁移清理
description: 本文说明如何使用 ER 迁移清理功能解决 ER 模板问题。
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 0b81f2f83209807f0d095bb7114b2361f3ce6154
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892499"
---
# <a name="er-migration-cleanup"></a>ER 迁移清理 

[!include[banner](../includes/banner.md)]

在管理 Finance 实例时，您可能会决定将当前实例迁移到另一个位置。 例如，您可以将生产实例迁移到新的沙盒环境。 如果您将电子申报 (ER) 框架配置为将模板存储在 Microsoft Azure Blob 存储中，则新沙盒环境中的 **DocuValue** 表将在生产环境中引用 Blob 存储的实例。 但是，无法从沙盒环境访问此实例，因为迁移过程不支持迁移 Blob 存储中的项目。 相反，预计在新沙盒环境中，您会引用尚未获得 ER 模板的沙盒环境中的 Blob 存储实例。

如果尝试运行使用模板生成业务文档的 ER 格式，则会发生异常，并且会通知您缺少的模板。 系统还会指导您使用 ER 迁移清理选项删除包含模板的 ER 格式配置，然后重新导入该配置。

[![运行 ER 格式。](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

如果您导航到 **配置** 页面（**组织管理** \> **电子申报** \> **配置**）并位于配置树中，那么您将收到类似的错误，请尝试删除使用模板的 ER 格式配置。

[![删除 ER 格式。](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

完成以下步骤来解决您无法访问 ER 模板的问题。

1.  转到 **组织管理** \> **定期** \> **迁移清理** 页面。
2.  选择无法执行或删除的 ER 格式配置。
3.  选择 **删除**。
4.  确认删除所选的 ER 格式配置。
5.  将已删除的 ER 格式配置[导入](download-electronic-reporting-configuration-lcs.md)到当前的 Finance 实例中。

## <a name="applicability"></a>适用性

> [重要提示] **迁移清理** 选项仅适用于包含不可访问的 ER 模板的 ER 格式配置。 当您使用 **迁移清理** 选项删除 ER 格式配置时，ER 会删除与唯一应用程序数据库中的配置项目相关的模板。 未验证 Blob 存储中是否存在合适的物理文件。 相反，假定不存在这些文件。 因此，请勿使用 **迁移清理** 选项代替 **配置** 页面上的 ER 配置删除选项。 仅当 **配置** 页面上的 ER 配置删除选项失效时，才使用 **迁移清理** 选项。
>
> 在 Blob 存储中有可用的引用模板时，如果使用 **迁移清理** 选项删除 ER 格式配置，则将仅删除应用程序数据库中的相关配置项目。 Blob 存储中的模板物理文件仍然保留。 不再允许在 Blob 存储中覆盖文件。 有关详细信息，请参阅 [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217)。 此外，您将无法再重新导入在该环境中使用迁移清理删除的配置。 要解决此问题，您需要在 Blob 存储中找到相应的文件并手动将其删除。

[![导入 ER 格式。](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

如果将应用程序实例迁移到已多次用作迁移目标的另一个位置，并且 Blob 存储已经包含其 ER 模板文件，则可能会发生类似的问题。

因为您可以具有几种 ER 格式配置，所以此过程可能很耗时。 因此，最好使用 [ER 模板的备份存储](er-backup-storage-templates.md)功能自动恢复具有被破坏的引用的模板。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]