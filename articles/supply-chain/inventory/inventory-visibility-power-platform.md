---
title: 库存可见性应用
description: 本主题介绍如何使用库存可见性应用。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 359f89f98ca6954a0bbafd63fffa1d505a43f0c8
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060964"
---
# <a name="use-the-inventory-visibility-app"></a>使用库存可见性应用

[!include [banner](../includes/banner.md)]


本主题介绍如何使用库存可见性应用。

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

**库存汇总** 是 *现有库存总和* 实体的自定义视图。 其提供产品的库存汇总以及所有维度。 将定期从库存可见性同步库存汇总数据。 必须先在 **功能管理** 选项卡上开启 *OnHandMostSpecificBackgroundService* 功能，才能在 **库存汇总** 选项卡上看到数据。

可以通过使用 Dataverse 提供的 **高级筛选器**，创建个人视图以显示对您至关重要的行。 可使用高级筛选器选项创建从简单到复杂的大量视图。 还可用于向筛选器添加组合嵌套条件。 若要了解有关如何使用 **高级筛选器** 的详细信息，请参阅[使用高级网格筛选器编辑或创建个人视图](/powerapps/user/grid-filters-advanced)。

这个自定义视图的顶部显示三个字段：**默认维度**、**自定义维度** 和 **度量**。 可以使用这些字段控制哪些列可见。

可以选择列标题，以便筛选当前结果或为当前结果排序。

这个自定义视图的底部显示信息，如“50 条记录（29 条已选）”或“50 条记录”。 此信息指的是当前从 **高级筛选器** 结果加载的记录。 文本“29 条已选”指的是通过对加载的记录使用列标题选择的记录的数量。

视图底部是可用于从 Dataverse 加载更多记录的 **加载更多** 按钮。 加载的默认记录的数量为 50。 选择 **加载更多** 时，将在视图中加载下 1,000 条可用记录。 **加载更多** 按钮上的数字指示当前加载的记录数和 **高级筛选器** 结果的记录总数。

![库存汇总](media/inventory-visibility-onhand-list.png "库存汇总")
