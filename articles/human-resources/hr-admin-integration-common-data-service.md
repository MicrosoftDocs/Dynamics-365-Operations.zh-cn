---
title: 配置 Common Data Service 集成
description: 您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04280aa0908ed6dab86ef87b6c1843e4b4348e08
ms.sourcegitcommit: c9657b44adb9c1a77c7c2f6ab63a58cc848974ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198414"
---
# <a name="configure-common-data-service-integration"></a>配置 Common Data Service 集成

您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。

关闭集成后，用户可以在 Human Resources 或 Common Data Service 中进行更改，但是这些更改在两个环境之间不同步。

默认情况下，已关闭 Human Resources 和 Common Data Service 之间的集成。

在以下情况下，您可能需要关闭集成：

- 您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。

- Human Resources 或 Common Data Service 中的数据存在问题。 如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。 重新打开集成后，未删除记录的环境中的记录将同步到已删除记录的环境。 同步将在下一次运行 **Common Data Service 集成错过的请求同步**批处理作业时开始。

> [!WARNING]
> 关闭数据集成时，请确保不要在两个环境中编辑同一个记录。 当您重新打开集成时，上次编辑的记录将被同步。 因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。

## <a name="access-the-common-data-service-integration-page"></a>访问 Common Data Service 集成页面

1. 在要查看或配置与 Common Data Service 集成的设置的 Human Resources 实例中，选择**系统管理**磁贴。

    [![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. 选择**链接**选项卡。

    [![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. 在**集成**下，选择 **Common Data Service 配置**。

    [![Common Data Service 配置链接](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>打开或关闭 Human Resources 和 Common Data Service 之间的数据集成

- 要打开集成，请将**启用对 Common Data Service 的集成**选项设置为**是**。

    > [!NOTE]
    > 当您打开集成时，下次运行 **Common Data Service 集成错过的请求同步**批处理作业时，将同步数据。 批处理作业完成后，所有数据都应该可用。

- 要关闭集成，请将此选项设置为**否**。

[![打开或关闭 Common Data Service 集成](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>查看数据集成详细信息

在 **Common Data Service 集成**页面的**管理**快速选项卡上，您可以看到记录在 Human Resources 和 Common Data Service 之间如何链接在一起。

- 要查看实体的记录，请在 **CDS 实体名称**字段中选择实体。 网格显示链接到所选实体的所有记录。

[![查看实体的记录](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> 当前不会列出所有 Common Data Service 实体。 只有支持使用自定义字段的实体会显示在网格中。 新实体将在陆续发布的 Human Resources 中提供。

网格包括以下字段：

- **CDS 实体名称** – Common Data Service 中实体的名称。
- **CDS 实体引用** – Common Data Service 用于标识记录的标识符。 此值等效于 Human Resources **RecId** 值。 在 Microsoft Excel 中打开 Common Data Service 实体时，您可以找到此标识符。
- **Human Resources 实体名称** – 上次将数据同步到 Common Data Service 的实体。 此实体可以具有 Common Data Service 前缀或另一个前缀。
- **Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。
- **已从 CDS 中删除** – 指示记录是否已从 Common Data Service 中删除的值。

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>从 Common Data Service 中删除 Human Resources 中的记录的关联

如果您在 Human Resources 和 Common Data Service 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。 如果您删除关联，然后更改或删除 Common Data Service 中的记录，更改将不会同步到 Human Resources。 如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Common Data Service 中更新该记录。

- 要删除 Human Resources 和 Common Data Service 之间的记录的关联，请在 **CDS 实体名称**字段中选择实体，然后选择**清除跟踪信息**。

[![清除跟踪信息](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

要在清除跟踪后在实体上运行完全同步，请参见下一个过程。

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>在 Human Resources 和 Common Data Service 之间同步实体

在以下情况下使用此过程：

- 从 Common Data Service 进行的更改需要很长时间才会在 Human Resources 中显示。

- 必须在清除跟踪后刷新跟踪表。

若要在 Human Resources 与 Common Data Service 之间对实体运行网站同步：

1. 在 **CDS 实体名称**字段中选择实体。

2. 选择**立即同步**。

[![运行完全同步](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


