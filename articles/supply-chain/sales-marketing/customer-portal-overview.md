---
title: Dynamics 365 Supply Chain Management 客户门户概览（包含视频）
description: 本文介绍客户门户，并说明谁应该使用它及其如何工作。
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ff074e62489fe74f0c2de6dae0e02d1da7e7f6ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901899"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Dynamics 365 Supply Chain Management 客户门户概述

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>什么是客户门户？

现代供应链系统依赖于集成。 他们需要库存、客户需求和销售部门集成在一起，而不是各自位于单独的孤岛。 客户门户可帮助运行 Microsoft Dynamics 365 Supply Chain Management 的组织增强这种集成，并更有效地让客户了解情况。

客户门户是一个 [Power Apps 门户](/powerapps/maker/portals/overview)模板，让公司可以为与销售订单处理相关的场景创建一个面向外部的企业到企业 (B2B) 网站。 此模板使用[双写入](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)、Supply Chain Management 和 Power Apps 门户支持外部企业客户从公司的 Dynamics 365 环境中查看和创建数据。

客户门户模板具有 Power Apps 的门户功能提供的所有自定义功能。 此模板可以轻松修改来表示公司的品牌、添加更多功能，以及更改用户体验。 此模板现在提供的所有功能都可以根据需要修改。

> [!IMPORTANT]
> 单是模板本身，不能提供完整功能。 对于希望创建面向外部的网站，以便企业客户可以与 Supply Chain Management 中的数据进行交互的客户，它只是充当一个使能者。

> [!NOTE]
> 客户门户文档面向将为 Supply Chain Management 安装设置客户门户的管理员、定制员和系统集成商。 它使用术语 _客户_ 和 _用户_ 描述属于运行 Supply Chain Management 的组织的客户，以及将使用最终门户的人员。

## <a name="video"></a>视频

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Dynamics 365 Supply Chain Management 中的客户门户模板概述](https://youtu.be/nPrqoLuHfV8)视频（上方所示）包含在 YouTube 上的可用 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="who-should-use-it"></a>谁应该使用它？

客户门户是为运行 Supply Chain Management 并具有以下特征的公司设计的：

- 他们希望构建一个面向外部的网站，该网站将订单处理信息（如订单状态或帐户信息）直接从其 Supply Chain Management 系统传达到其企业客户。
- 他们正在从 Dynamics AX 2012 转移到 Supply Chain Management，以前使用 [AX 2012 客户自助服务门户](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal)。

以下类型的组织 **不** 是实施客户门户的理想候选人：

- 希望为非企业客户构建网站的公司。 这些公司应该考虑创建 [Dynamics 365 Commerce 电子商务网站](../../commerce/create-ecommerce-site.md)。
- 已经将现有 Power Apps 门户网站用于类似目的的公司。 这些公司不会从客户门户获得任何其他好处。 客户门户作为模板提供，它充当希望在双写入、Supply Chain Management 和 Power Apps 门户之间“连接点”的客户的指南和起点。 如果您已经设置了一个用于此目的的网站，使用客户门户模板重新预配该网站可能不会获得太多价值。

## <a name="how-does-it-work"></a>工作原理

客户门户作为 Power Apps 门户模板提供。 依赖 Power Apps 门户和双写入。

[Power Apps 门户](/powerapps/maker/portals/overview)是一项功能，让用户可以创建面向外部的网站，组织外部的人员可以登录到该网站。 创建门户几乎不需要编码。 客户门户是众多 [Dynamics 365 门户模板](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365)之一，可以从 Microsoft 获得。

[双写入](/powerapps/maker/portals/overview)是一种现成基础结构产品，其提供 Customer Engagement 应用与 Finance and Operations 应用之间的近实时交互。 双写入提供 Finance and Operations 应用与 Microsoft Dataverse 之间的双向集成。 因此，它可以提供应用之间的集成用户体验。 客户门户依赖于与双写入同步的表。 必须先对所有适当的表启用双写入，才能在客户门户中显示来自 Supply Chain Management 的数据。

![客户门户依赖关系。](media/customer-portal-elements.png "客户门户依赖关系")

对于想要使用 Power Apps 门户构建面向外部的使用其 Supply Chain Management 安装中数据的网站的组织，客户门户充当一个起点。 它帮助组织连接双写入、Supply Chain Management 和 Power Apps 门户。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]