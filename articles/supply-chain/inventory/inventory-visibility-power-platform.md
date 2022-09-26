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
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520844"
---
# <a name="use-the-inventory-visibility-app"></a>使用 Inventory Visibility 应用

[!include [banner](../includes/banner.md)]

本文介绍如何使用库存可见性应用。

库存可见性提供模型驱动应用以进行可视化。 此应用中包含三个页面：**配置**、**操作可见性** 和 **库存汇总**。 它具有以下功能：

- 为现有库存配置和软预留配置提供用户接口 (UI)。
- 支持对各种维度组合执行实时现有库存查询。
- 提供用于发布预留请求的 UI。
- 提供产品的现有库存与所有维度的视图。
- 提供产品的现有库存量列表与预定义维度的视图。


## <a name="prerequisites"></a>先决条件

首先，按照[安装和设置库存可见性](inventory-visibility-setup.md)中的说明安装并设置库存可见性加载项。

## <a name="open-the-inventory-visibility-app"></a>打开库存可见性应用

若要打开库存可见性应用，请登录您的 Power Apps 环境，然后打开 **库存可见性**。

## <a name="configuration"></a><a name="configuration"></a>配置

库存可见性应用的 **配置** 页面可帮助您设置现有库存配置和软预留配置。 安装此加载项后，默认配置中将包含 Microsoft Dynamics 365 Supply Chain Management（`fno` 数据源）的默认设置。 可以查看默认设置。 此外，可根据您的业务要求和外部系统的库存过帐要求修改配置，以便标准化跨多个系统过帐，组织和查询库存更改的方法。

有关如何配置此解决方案的完整详细信息，请参阅[配置库存可见性](inventory-visibility-configuration.md)。

## <a name="operational-visibility"></a>操作可见性

**操作可见性** 页根据各种维度组合提供实时现有库存查询的结果。 如果开启了 *OnHandReservation* 功能，也可从 **操作可见性** 页发布预留请求。

### <a name="on-hand-query"></a>现有库存查询

**现场库存查询** 选项卡显示实时现有库存查询的结果。

打开 **运营可见性** 页面的 **现有库存查询** 选项卡时，系统将索取您的凭证，以便获取查询库存可见性服务所需持有者令牌。 只能将持有者令牌粘贴到 **BearerToken** 字段中，然后关闭对话框。 然后可以发布现有库存查询请求。

如果持有者令牌无效，或者其已过期，则必须将新令牌粘贴到 **BearerToken** 字段中。 输入正确的 **客户端 ID**、**租户 ID**、**客户端密钥** 值，然后选择 **刷新**。 系统将自动获取新的有效持有者令牌。

若要发布现有查询，请在请求正文中输入查询。 使用[使用发布方法查询](inventory-visibility-api.md#query-with-post-method)中介绍的模式。

![现有库存查询设置](media/inventory-visibility-query-settings.png "现有库存查询设置")

### <a name="reservation-posting"></a>预留发布

使用 **运营可见性** 页面的 **预留发布** 选项卡发布预留请求。 必须先开启 *OnHandReservation* 功能，才能发布预留请求。 有关此功能以及如何打开它的详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

若要发布预留请求，必须在请求正文中输入一个值。 请使用[创建一个预留事件](inventory-visibility-api.md#create-one-reservation-event)中介绍的模式。 然后选择 **发布**。 若要查看请求响应详细信息，请选择 **显示详细信息**。 也可以从相应详细信息获取 `reservationId` 值。

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

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>预加载简化的现有库存查询

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management 存储大量有关您当前的现有库存的信息，使其可用于各种用途。 但是，很多日常操作和第三方集成只需要这些详细信息的一小部分，而查询系统中的所有详细信息可能会导致出现需要花费时间来合并和传输的大型数据集。 因此，库存可见性服务可以定期提取和存储一组精简的现有库存数据，让优化的信息持续可用。 系统将根据可配置的业务条件筛选存储的现有库存详细信息，以确保仅包含最相关的信息。 由于筛选出的现有库存量列表本地存储在库存可见性服务中并定期更新，它们支持快速访问、按需数据导出以及与外部系统进行简化的整合。

> [!NOTE]
> 此功能的当前预览版只能提供包含站点和位置的预加载结果。 此功能的最终版本预期可以允许您选择要与结果一起预加载的其他维度。

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
