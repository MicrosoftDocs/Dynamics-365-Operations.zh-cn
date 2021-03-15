---
title: 配置 Dataverse 集成
description: 您可以打开或关闭 Microsoft Dataverse 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步表，以帮助解决两个环境之间的数据问题。
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111678"
---
# <a name="configure-dataverse-integration"></a>配置 Dataverse 集成

您可以打开或关闭 Microsoft Dataverse 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步表，以帮助解决两个环境之间的数据问题。

> [!NOTE]
> 有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

关闭集成后，用户可以在 Human Resources 或 Dataverse 中进行更改，但是这些更改在两个环境之间不同步。

默认情况下，已关闭 Human Resources 和 Dataverse 之间的集成。

在以下情况下，您可能需要关闭集成：

- 您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。

- Human Resources 或 Dataverse 中的数据存在问题。 如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。 重新打开集成后，未删除记录的环境中的记录将同步到已删除记录的环境。 同步将在下一次运行 **Dataverse 集成错过的请求同步** 批处理作业时开始。

> [!WARNING]
> 关闭数据集成时，请确保不要在两个环境中编辑同一个记录。 当您重新打开集成时，上次编辑的记录将被同步。 因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。

## <a name="access-the-dataverse-integration-page"></a>访问 Dataverse 集成页面

1. 在要查看或配置与 Dataverse 集成的设置的 Human Resources 实例中，选择 **系统管理** 磁贴。

    [![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. 选择 **链接** 选项卡。

    [![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. 在 **集成** 下，选择 **Dataverse 配置**。

    [![Dataverse 配置链接](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>打开或关闭 Human Resources 和 Dataverse 之间的数据集成

- 要打开集成，在 **Microsoft Dataverse 集成** 页上将 **启用 Dataverse 集成** 选项设置为 **是**。

    > [!NOTE]
    > 当您打开集成时，下次运行 **Dataverse 集成错过的请求同步** 批处理作业时，将同步数据。 批处理作业完成后，所有数据都应该可用。

- 要关闭集成，请将此选项设置为 **否**。

[![打开或关闭 Dataverse 集成](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> 强烈建议在执行数据迁移任务时关闭 Dataverse 集成。 上载大量数据会严重影响性能。 例如，启用集成后，上载 2000 个工作人员可能要花费几个小时，禁用后则不到一小时。 本示例中提供的数字仅用于演示目的。 导入记录所需的确切时间由于很多因素可能出现很大差异。

## <a name="view-data-integration-details"></a>查看数据集成详细信息

在 **Microsoft Dataverse 集成** 页面的 **管理** 快速选项卡上，您可以看到行在 Human Resources 和 Dataverse 之间如何链接在一起。

- 要查看表的行，在 **Dataverse 表** 字段中选择该表。 网格将显示链接到所选表的所有行。

> [!NOTE]
> 当前不会列出所有 Dataverse 表。 只有支持使用自定义字段的表会显示在网格中。 新表将在陆续发布的 Human Resources 中提供。

网格包括以下字段：

- **Dataverse 表** – Dataverse 中的表的名称。
- **Dataverse 表引用** – Dataverse 用于标识记录的标识符。 此值等效于 Human Resources **RecId** 值。 在 Microsoft Excel 中打开 Dataverse 表时，您可以找到此标识符。
- **Human Resources 实体名称** – 上次将数据同步到 Dataverse 的 Human Resources 实体。 此实体可以具有 Dataverse 前缀或另一个前缀。
- **Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。
- **已从 Dataverse 中删除** – 指示行是否已从 Dataverse 中删除的值。

> [!NOTE]
> Human Resources 中的记录与 Dataverse 中的行对应。

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>从 Dataverse 行中删除 Human Resources 记录的关联

如果您在 Human Resources 和 Dataverse 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。 如果您删除关联，然后更改或删除 Dataverse 中的行，更改将不会同步到 Human Resources。 如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Dataverse 中更新该行。

- 要删除 Human Resources 记录和 Dataverse 行之间的记录的关联，请在 **Dataverse 表** 字段中选择表，然后选择 **清除跟踪信息**。

[![清除跟踪信息](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

要在清除跟踪后在表上运行完全同步，请参见下一个过程。

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>在 Human Resources 和 Dataverse 之间同步表

在以下情况下使用此过程：

- 从 Dataverse 进行的更改需要很长时间才会在 Human Resources 中显示。

- 必须在清除跟踪后刷新跟踪表。

若要在 Human Resources 与 Dataverse 之间对表运行完全同步：

1. 在 **Dataverse 表** 字段中选择表。

2. 选择 **立即同步**。

[![运行完全同步](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>请参阅

[Dataverse 表](hr-developer-entities.md)<br>
[配置 Dataverse 虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources 虚拟表常见问题解答](hr-admin-virtual-entity-faq.md)<br>
[什么是 Microsoft Dataverse？](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[术语更新](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]