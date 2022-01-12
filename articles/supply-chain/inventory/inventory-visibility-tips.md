---
title: 库存可见性提示
description: 本主题提供了您在设置和使用库存可见性加载项时应考虑的一些提示。
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
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920792"
---
# <a name="inventory-visibility-tips"></a>库存可见性提示

[!include [banner](../includes/banner.md)]

以下是您在设置和使用库存可见性加载项时应考虑的一些提示：

- 当前，库存可见性加载项仅支持使用 Microsoft Dynamics Lifecycle Services (LCS) 创建的 Microsoft Dataverse 环境。 如果您的 Dataverse 环境是使用某种其他方法创建的（例如，使用 Power Apps 管理中心创建的），并且其已链接到您的 Dynamics 365 Supply Chain Management 环境，您必须首先请求库存可见性产品团队解决映射问题。 您可以通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与团队联系。 当您的环境准备好安装库存可见性时，团队会通知您。
- 如果您有多个 LCS 环境，请为每个环境创建一个不同的 Azure Active Directory (Azure AD) 应用程序。 如果使用相同的应用程序 ID 和租户 ID 为不同环境安装库存可见性加载项，较低版本环境将发生令牌问题。 只有安装的库存可见性加载项的最后一个实例才有效。
- 云托管的环境当前不支持库存可见性。 它仅支持第 2 层以上的环境。
- 应用编程接口 (API) 当前最多支持按 `ProductID` 值查询 100 个单个项。 也可以在每个查询中指定多个 `SiteID` 值和 `LocationID` 值。 最大限制定义为 `NumOf(SiteID) * NumOf(LocationID) <= 100`。
- `fno` 数据源是为 Supply Chain Management 预留的。 如果您的库存可见性加载项与 Supply Chain Management 环境集成，我们建议您不要删除[数据源](inventory-visibility-configuration.md#data-source-configuration)中与 `fno` 相关的配置。
- 当前，[分区配置](inventory-visibility-configuration.md#partition-configuration)由两个基本维度（`SiteId` 和 `LocationId`）组成，这两个维度指示数据的分配方式。 同一分区下的操作可以以更低的成本提供更高的性能。 默认情况下，该解决方案包括此分区配置。 因此，*您不必亲自定义它*。 不自定义默认分区配置。 如果删除或更改它，则可能会导致意外错误。
- 不应在[产品索引层次结构配置](inventory-visibility-configuration.md#index-configuration)中定义在分区配置中定义的基础维度。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
