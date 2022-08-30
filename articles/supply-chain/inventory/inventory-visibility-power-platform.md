---
title: 库存可见性应用
description: 本文介绍如何使用库存可见性应用。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306164"
---
# <a name="use-the-inventory-visibility-app"></a>使用 Inventory Visibility 应用

[!include [banner](../includes/banner.md)]


本文介绍如何使用库存可见性应用。

库存可见性提供模型驱动应用以进行可视化。 此应用中包含三个页面：**配置**、**操作可见性** 和 **库存汇总**。 它具有以下功能：

- 为现有库存配置和软预留配置提供用户接口 (UI)。
- 支持对各种维度组合执行实时现有库存查询。
- 提供用于发布预留请求的 UI。
- 提供产品的现有库存与所有维度的自定义视图。

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

选择 **现有库存查询** 选项卡时，系统将索取您的凭证，以便获取查询库存可见性服务所需持有者令牌。 只能将持有者令牌粘贴到 **BearerToken** 字段中，然后关闭对话框。 然后可以发布现有库存查询请求。

如果持有者令牌无效，或者其已过期，则必须将新令牌粘贴到 **BearerToken** 字段中。 输入正确的 **客户端 ID**、**租户 ID**、**客户端密钥** 值，然后选择 **刷新**。 系统将自动获取新的有效持有者令牌。

若要发布现有查询，请在请求正文中输入查询。 使用[使用发布方法查询](inventory-visibility-api.md#query-with-post-method)中介绍的模式。

![现有库存查询设置](media/inventory-visibility-query-settings.png "现有库存查询设置")

### <a name="reservation-posting"></a>预留发布

可使用 **预留发布** 选项卡发布预留请求。 必须先开启 *OnHandReservation* 功能，才能发布预留请求。 有关此功能的详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

若要发布预留请求，必须在请求正文中输入一个值。 请使用[创建一个预留事件](inventory-visibility-api.md#create-one-reservation-event)中介绍的模式。 然后选择 **发布**。 若要查看请求响应详细信息，请选择 **显示详细信息**。 也可以从相应详细信息获取 `reservationId` 值。

## <a name="inventory-summary"></a><a name="inventory-summary"></a>库存汇总

**库存摘要** 页面提供产品的库存汇总以及所有维度。 它是 *现有库存总和* 实体的自定义视图。 将定期从库存可见性同步库存摘要数据。

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>启用库存摘要并设置同步频率

要启用 **库存摘要** 页面并设置同步频率，请按以下步骤操作：

1. 打开 **管理** 页面。
1. 打开 **功能管理和设置** 选项卡。
1. 将 **OnHandMostSpecificBackgroundService** 功能的切换开关设置为 *是*。
1. 启用此功能后，**服务配置** 部分将可用，其中包含用于配置 **OnHandMostSpecificBackgroundService** 功能的行。 此设置允许您选择同步库存摘要数据的频率。 使用 **值** 列中的 **向上** 和 **向下** 按钮更改同步之间间隔的时间（最低可设置为 5 分钟）。 然后选择 **保存**。
1. 选择 **更新配置** 保存所有更改。

![OnHandMostSpecificBackgroundService 设置](media/inventory-visibility-ohms-freq.PNG "OnHandMostSpecificBackgroundService 设置")

> [!NOTE]
> *OnHandMostSpecificBackgroundService* 功能仅跟踪启用该功能后发生的现有产品更改。 自启用此功能后未更改的产品的数据不会从库存服务缓存同步到 Dataverse 环境。 如果您的 **库存汇总** 页面未显示您所预期的所有现有信息，请转到 **库存管理 > 定期任务 > 库存可见性集成**，禁用批处理作业，然后重新启用。 这将执行初始推送，所有数据将在接下来的 15 分钟内同步到 *现有库存量总计* 实体。 如果您想要使用此功能，我们建议您在创建任何现有更改和启用 **库存可见性集成** 批处理作业之前先启用它。

### <a name="work-with-the-inventory-summary"></a>使用库存摘要

可以通过使用 Dataverse 提供的 **高级筛选器**，创建个人视图以显示对您至关重要的行。 可使用高级筛选器选项创建从简单到复杂的大量视图。 还可用于向筛选器添加组合嵌套条件。 若要了解有关如何使用 **高级筛选器** 的详细信息，请参阅[使用高级网格筛选器编辑或创建个人视图](/powerapps/user/grid-filters-advanced)。

这个自定义视图的顶部显示三个字段：**默认维度**、**自定义维度** 和 **度量**。 可以使用这些字段控制哪些列可见。

可以选择列标题，以便筛选当前结果或为当前结果排序。

这个自定义视图的底部显示信息，如“50 条记录（29 条已选）”或“50 条记录”。 此信息指的是当前从 **高级筛选器** 结果加载的记录。 文本“29 条已选”指的是通过对加载的记录使用列标题选择的记录的数量。

视图底部是可用于从 Dataverse 加载更多记录的 **加载更多** 按钮。 加载的默认记录的数量为 50。 选择 **加载更多** 时，将在视图中加载下 1,000 条可用记录。 **加载更多** 按钮上的数字指示当前加载的记录数和 **高级筛选器** 结果的记录总数。

![库存汇总](media/inventory-visibility-onhand-list.png "库存摘要")
