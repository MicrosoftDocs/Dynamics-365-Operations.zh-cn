---
title: 库存可见性应用
description: 本文介绍如何使用库存可见性应用。
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762692"
---
# <a name="use-the-inventory-visibility-app"></a>使用 Inventory Visibility 应用

[!include [banner](../includes/banner.md)]

本文介绍如何使用库存可见性应用。

库存可见性提供模型驱动应用以进行可视化。 此应用中包含三个页面：**配置**、**操作可见性** 和 **库存汇总**。 它具有以下功能：

- 为现有库存配置和软预留配置提供用户接口 (UI)。
- 支持对各种维度组合执行实时现有库存查询。
- 提供用于发布预留请求的 UI。
- 提供产品的现有库存与所有维度的视图。
- 提供产品的现有库存量列表与预定义维度的视图。 现有量列表视图可以是完整的摘要，也可以是现有量查询的预加载结果。

## <a name="prerequisites"></a>先决条件

首先，按照[安装和设置库存可见性](inventory-visibility-setup.md)中的说明安装并设置库存可见性加载项。

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>打开库存可见性应用并进行身份验证

要打开库存可见性应用并进行身份验证，请执行以下步骤。

1. 登录您的 Power Apps 环境。
1. 打开 **库存可见性** 应用。
1. 从左侧窗格打开 **运营可见性** 页面。
1. 选择页面顶部的 **设置** 按钮（齿轮符号）。
1. 在 **设置** 对话框中，输入 [安装和设置库存可见性](inventory-visibility-setup.md)时记下的 **客户端 ID**、**租户 ID** 和 **客户端密码** 值。
1. 选择 **持有者令牌** 字段旁边的 **刷新** 按钮。 系统会根据您输入的信息生成一个新的持有者令牌。

    ![现有量查询设置。](media/inventory-visibility-query-settings.png "现有库存查询设置")

1. 当您收到有效的持有者令牌时，关闭对话框。 持有者令牌将在一段时间后过期。 因此，当您必须更新配置、发布数据或查询数据时，必须间或地进行刷新。

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>配置库存可见性应用

库存可见性应用的 **配置** 页面可帮助您设置设置一般数据管理配置和功能配置。 安装此加载项后，默认配置中将包含 Microsoft Dynamics 365 Supply Chain Management（`fno` 数据源）的默认设置。 可以查看默认设置。 之后，可根据您的业务要求和外部系统的库存过帐要求修改配置，以便标准化跨多个系统过帐，组织和查询库存更改的方法。

有关如何配置此解决方案的完整详细信息，请参阅[配置库存可见性](inventory-visibility-configuration.md)。

## <a name="operational-visibility"></a>操作可见性

**操作可见性** 页根据各种维度组合提供实时现有库存查询、预留发布和分配的结果。 如果 [开启](inventory-visibility-configuration.md)了 *OnHandReservation* 功能，也可从 **运营可见性** 页发布预留请求。

### <a name="on-hand-query"></a>现有库存查询

**运营可见性** 页面的 **现有量查询** 选项卡允许您查询实时现有库存。 按照以下步骤设置和运行查询。

1. 打开 **库存可见性** 应用。
1. 从左侧窗格打开 **运营可见性** 页面。
1. 在 **现有量查询** 选项卡上，输入要查询的 **组织 ID**、**站点 ID** 和 **位置 ID** 值。
1. 在 **产品 ID** 字段中，输入一个或多个产品 ID 可获得精确的查询匹配结果。 如果将 **产品 ID** 字段留空，结果将包括指定站点和位置的所有产品。
1. 要获得更精细的结果（例如，按维度值(如颜色和大小)显示的视图），在 **结果分组依据** 字段中选择分组依据维度。
1. 要查找具有特定维度值（如颜色 = 红色）的项，在 **筛选维度** 字段中选择维度，然后输入维度值。
1. 选择 **查询**。 您将收到成功（绿色）消息或失败（红色）消息。 如果查询失败，检查您的查询条件，确保您的[持有者令牌](#open-authenticate)尚未过期。

进行现有量查询的另一种方法是发起直接 API 请求。 您可以使用 `/api/environment/{environmentId}/onhand/indexquery` 或 `/api/environment/{environmentId}/onhand`。 有关详细信息，请参阅[库存可见性公共 API](inventory-visibility-api.md)。

### <a name="reservation-posting"></a>预留发布

使用 **运营可见性** 页面的 **预留发布** 选项卡发布预留请求。 必须先开启 *OnHandReservation* 功能，才能发布预留请求。 有关此功能以及如何打开它的详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

> [!NOTE]
> 通过用户界面进行软预留的功能用于支持您对功能进行测试。 每个软预留请求都应与交易订单行更改（创建、修改、删除等）相关联。 因此，我们建议您仅进行链接到后端订单的软预留。 有关详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

按照以下步骤使用用户界面发布软预留请求。

1. 打开 **库存可见性** 应用。
1. 从左侧窗格打开 **运营可见性** 页面。
1. 在 **预留发布** 选项卡上，在 **数量** 字段中，指定您要软预留的数量。
1. 清除 **启用负库存以支持超额销售** 复选框，以防止库存超额销售或超额预留。
1. 在 **运算符** 字段中，选择适用于软预留数量的数据源和实际度量。
1. 输入要查询的 **组织 ID**、**站点 ID**、**位置 ID** 和 **产品 ID** 值。
1. 要获得更精细的结果，选择数据源、维度和维度值。

发布软预留的另一种方法是直接发起 API 请求。 请使用[创建一个预留事件](inventory-visibility-api.md#create-one-reservation-event)中介绍的模式。 然后选择 **发布**。 若要查看请求响应详细信息，请选择 **显示详细信息**。 也可以从相应详细信息获取 `reservationId` 值。

### <a name="allocation"></a>分配

有关如何从用户界面和 API 管理分配的信息，请参阅[库存可见性库存分配](inventory-visibility-allocation.md)。

## <a name="inventory-summary"></a><a name="inventory-summary"></a>库存汇总

**库存摘要** 页面提供产品的库存汇总以及所有维度。 它是 *现有库存总和* 实体的自定义视图。 将定期从库存可见性同步库存摘要数据。

要启用 **库存摘要** 页面并设置同步频率，请按以下步骤操作：

1. 打开 **管理** 页面。
1. 打开 **功能管理和设置** 选项卡。
1. 将 **OnHandMostSpecificBackgroundService** 功能的切换开关设置为 *是*。
1. 启用此功能后，**服务配置** 部分将可用，其中包含用于配置 **OnHandMostSpecificBackgroundService** 功能的行。 此设置允许您选择同步库存摘要数据的频率。 使用 **值** 列中的 **向上** 和 **向下** 按钮更改同步之间间隔的时间（最低可设置为 5 分钟）。 然后选择 **保存**。

    ![OnHandMostSpecificBackgroundService 设置](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService 设置")

1. 选择 **更新配置** 保存所有更改。

> [!NOTE]
> *OnHandMostSpecificBackgroundService* 功能仅跟踪启用该功能后发生的现有库存更改。 自启用此功能后未更改的产品的数据不会从库存服务缓存同步到 Dataverse 环境。 如果您的 **库存汇总** 页面未显示您所预期的所有现有信息，打开 Supply Chain Management，转到 **库存管理 > 定期任务 > 库存可见性集成**，禁用批处理作业，然后重新启用。 这将执行初始推送，所有数据将在接下来的 15 分钟内同步到 *现有库存量总计* 实体。 如果您想要使用 *OnHandMostSpecificBackgroundService* 功能，我们建议您在创建任何现有更改和启用 **库存可见性集成** 批处理作业之前先启用它。

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>预加载简化的现有库存查询

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management 存储大量有关您当前的现有库存的信息，使其可用于各种用途。 但是，很多日常操作和第三方集成只需要这些详细信息的一小部分，而查询系统中的所有详细信息可能会导致出现需要花费时间来合并和传输的大型数据集。 因此，库存可见性服务可以定期提取和存储一组精简的现有库存数据，让优化的信息持续可用。 系统将根据可配置的业务条件筛选存储的现有库存详细信息，以确保仅包含最相关的信息。 由于筛选出的现有库存量列表本地存储在库存可见性服务中并定期更新，它们支持快速访问、按需数据导出以及与外部系统进行简化的整合。

**预加载库存可见性摘要** 页面提供了 *现有库存索引查询预加载结果* 实体的视图。 与 *库存摘要* 实体不同，*现有库存索引查询预加载结果* 实体提供产品的现有库存量列表以及选定的维度。 库存可见性每 15 分钟同步一次预加载的摘要数据。

要在 **预加载库存可见性摘要** 选项卡上查看数据，您必须在 **配置** 页面的 **功能管理** 选项卡上打开 *OnHandIndexQueryPreloadBackgroundService* 功能，然后选择 **更新配置**（另请参阅[配置库存可见性](inventory-visibility-configuration.md)）。

> [!NOTE]
> 与 *OnhandMostSpecificBackgroudService* 功能一样，*OnHandIndexQueryPreloadBackgroundService* 功能仅跟踪您打开该功能后发生的现有库存量变化。 自启用此功能后未更改的产品的数据不会从库存服务缓存同步到 Dataverse 环境。 如果您的 **库存汇总** 页面未显示您所预期的所有现有信息，请转到 **库存管理 > 定期任务 > 库存可见性集成**，禁用批处理作业，然后重新启用。 这将执行初始推送，所有数据将在接下来的 15 分钟内同步到 *现有库存索引查询预加载结果* 实体。 如果您想要使用此功能，我们建议您在创建任何现有更改和启用 **库存可见性集成** 批处理作业之前先启用它。

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>筛选和浏览库存摘要

可以通过使用 Dataverse 提供的 **高级筛选器**，创建个人视图以显示对您至关重要的行。 可使用高级筛选器选项创建从简单到复杂的大量视图。 还可用于向筛选器添加组合嵌套条件。 若要了解有关如何使用高级筛选器的详细信息，请参阅[使用高级网格筛选器编辑或创建个人视图](/powerapps/user/grid-filters-advanced)。

**库存摘要** 页面在网格上方提供三个字段（**默认维度**、**自定义维度** 和 **度量**），您可以用来控制哪些列可见。 您还可以选择任何列标题来按该列筛选当前结果或为结果排序。 以下屏幕截图突出显示了 **库存摘要** 页面提供的维度、筛选、结果计数和“加载更多”字段。

![库存摘要页面。](media/inventory-visibility-onhand-list.png "库存摘要页面")

由于您已经预定义了用于加载摘要数据的维度，**预加载库存可见性摘要** 页面会显示与维度相关的列。 *维度不能自定义&mdash;系统仅支持预先加载现有库存列表的站点和位置维度。* **预加载库存可见性摘要** 页面提供的筛选器与 **库存摘要** 页面上的筛选器类似，但已选择维度。 以下屏幕截图突出显示了 **预加载库存可见性摘要** 页面提供的筛选字段。

![预加载库存可见性摘要页面。](media/inventory-visibility-preload-onhand-list.png "预加载库存可见性摘要页面")

在 **预加载库存可见性摘要** 和 **库存摘要** 页面的底部，您会找到诸如“50 个记录（29 个已选择）”或“50 个记录”等信息。 此信息指的是当前从 **高级筛选器** 结果加载的记录。 文本“29 条已选”指的是通过对加载的记录使用列标题选择的记录的数量。 还有一个 **加载更多** 按钮，您可以使用该按钮从 Dataverse 加载更多记录。 默认加载的记录数为 50。 选择 **加载更多** 时，将在视图中加载下 1,000 个可用记录。 **加载更多** 按钮上的数字指示当前加载的记录数和 **高级筛选器** 结果的记录总数。
