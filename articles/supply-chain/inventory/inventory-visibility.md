---
title: 库存可见性加载项概述
description: 本主题介绍库存可见性的定义及其功能。
author: yufeihuang
ms.date: 10/26/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8871d10dac9103f17780989bc547b6c20ba79b76
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985537"
---
# <a name="inventory-visibility-add-in-overview"></a>库存可见性加载项概述

[!include [banner](../includes/banner.md)]

库存可见性加载项（也称为 *库存可见性*）是一项独立且高度可扩展的微服务，可实现实时现有库存跟踪。 从而提供库存的全局视图。

外部系统通过 RESTful API 访问该服务。 这样就可以查询有关给定维度集的现有信息，或对不同自定义数据源中的库存进行更改。

库存可见性是一种基于 Microsoft Dataverse 的微服务，用于提供可扩展性。 可以使用 Power Apps 生成应用。 还可以应用 Power BI 以提供自定义功能来满足业务要求。

可以通过为标准化库存维度设置配置选项和设置交易记录类型，将库存可见性与多个第三方系统集成。 库存可见性还支持通过可配置的计算数量进行自定义扩展。

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>库存可见性与 Dynamics 365 Supply Chain Management 的集成

这款集成解决方案从 Dynamics 365 Supply Chain Management 提取库存数据，并持续跟踪库存更改。 有关详细信息，请参阅 [安装和设置库存可见性](inventory-visibility-setup.md)和[配置库存可见性](inventory-visibility-configuration.md)。

## <a name="get-a-global-view-of-inventory"></a>获取库存的全局视图

这款集成解决方案可用于定义自己的数据源和集中库存数据。 有关详细信息，请参阅[配置库存可见性](inventory-visibility-configuration.md)。

查看库存的方法有两种：

- 通过高性能 API 提交查询。 此 API 可以直接从缓存实例返回近实时库存数据。 您可以在[库存可见性公共 API](inventory-visibility-api.md) 中找到合同和示例 。
- 查看原始现有库存列表。 此列表定期从缓存实例同步，并在 Dataverse 中显示。 有关详细信息，请参阅[库存可见性应用](inventory-visibility-power-platform.md)。

## <a name="soft-reservations"></a>软预留

当企业必须预留特定数量的产品来为履行订单提供支持，以免超兽之类时，适合采用软预留。 在 Supply Chain Management 或其他订单管理系统中创建并确认订单之后，将向库存可见性发送有关预留该数量的请求。 可使用库存可见性预留具有维度详细信息和特定库存交易类型的产品。 （有关详细信息，请参阅[库存可见性应用](inventory-visibility-power-platform.md) 。）在成功预留数量后，将返回预留 ID。 可以在 Supply Chain Management 或其他订单管理系统中使用此预留 ID 重新链接到原始订单。

此功能旨在使库存可见性中的预留不会更改总数量。 而是仅标记预留数量。 （因此称为 *软预留*。）如果 Supply Chain Management 或第三方系统中使用了产品，可以通过再次调用 API 进行数量扣减并在库存可见性中更新总数量来抵销软预留数量。 有关详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
