---
title: 内容分发网络实施选项
description: 本主题回顾了可用于 Microsoft Dynamics 365 Commerce 环境的内容分发网络 (CDN) 实施的不同选项。 这些选项包括由 Commerce 提供的 Azure Front Door 本机实例，以及客户拥有的 Azure Front Door 实例。
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 73da1fff8f79b4fcde38f9da643b8a3479247959f763976d782279e4e2af7a33
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729906"
---
# <a name="content-delivery-network-implementation-options"></a>内容分发网络实施选项

[!include [banner](includes/banner.md)]

本主题回顾了可用于 Microsoft Dynamics 365 Commerce 环境的内容分发网络 (CDN) 实施的不同选项。 这些选项包括由 Commerce 提供的 Azure Front Door 本机实例，以及客户拥有的 Azure Front Door 实例。

当 Commerce 客户考虑在其 Commerce 环境中使用哪种 CDN 服务时，有若干种选择。 Commerce 随基本 Azure Front Door 支持一起发布，该支持可满足基本托管和自定义域要求。 对于需要加强控制和 Web 应用程序防火墙 (WAF) 等更具体的安全功能的公司，最佳选择可能是使用客户拥有的 Azure Front Door 实例或外部 CDN 服务。

以下三个 CDN 实施选项可用于 Commerce 环境：

- Commerce 提供的 Azure Front Door 实例
- 客户拥有的 Azure Front Door 实例（用于加强控制和其他安全功能）
- 外部 CDN 服务

所有这三个 CDN 实施选项都仅提供来自自定义域的动态 HTML 内容。 Commerce 会通过 Microsoft 托管的 CDN 自动处理所有 JavaScript、级联样式表 (CSS)、图像、视频和其他静态内容。 您选择的选项决定了可用的操作功能、控制功能和其他安全功能。

下图显示了 Commerce 体系结构的概览。

![Commerce 体系结构的概览。](media/Commerce_CDN-Option_ComparisonModels.png)

有关如何为您的 Commerce 站点设置 Azure Front Door 实例的更多信息，请参见[添加 CDN 支持](add-cdn-support.md)。

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>使用 Commerce 提供的 Azure Front Door 实例

下表列出了使用 Commerce 提供的 Azure Front Door 实例来管理内容终结点的利弊。

| 优点 | 缺点 |
|------|------|
| <ul><li>该实例已包含在 Commerce 成本中。</li><li>因为实例是由 Commerce 团队管理的，所以需要的维护较少，并且有共享的设置步骤。</li><li>Azure 托管的基础结构具有可伸缩性、安全性和可靠性。</li><li>安全套接字层 (SSL) 证书需要一次性设置并且会自动更新。</li><li>Commerce 团队将监视实例是否有错误和异常。</li></ul> | <ul><li>不支持 WAF。</li><li>没有特定的自定义或设置调整。</li><li>实例依靠 Commerce 团队进行更新或更改。</li><li>Apex 域需要一个单独的 Azure Front Door 实例，并且需要额外的工作才能将 apex 域与 Azure DNS 集成。</li><li>没有向客户提供有关每秒响应次数 (RPS) 或错误率的遥测。</li></ul> |

下图显示了由 Commerce 提供的 Azure Front Door 实例的体系结构。

![Commerce 提供的 Azure Front Door 实例。](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>使用客户拥有的 Azure Front Door 实例

下表列出了使用客户拥有的 Azure Front Door 实例来管理内容终结点的利弊。

| 优点 | 缺点 |
|------|------|
| <ul><li>设置既安全又易于管理。</li><li>Azure 托管的基础结构具有可伸缩性、安全性和可靠性。</li><li>该实例允许进行 WAF 集成和精细的规则控制，以实现针对您的站点专门调整的更高级别的安全性。</li><li>该实例允许更好地控制 SSL 证书（客户拥有的证书和由 Azure Front Door 托管的证书）和域链接。</li><li>如果该实例直接与 Azure DNS 配对，则该实例将提供一个 apex 域解决方案。</li><li>提供了遥测和警报。</li><li>SSL 证书需要一次性设置并且会自动更新。</li></ul> | <ul><li>此实例是自我托管型实例。</li><li>需要初步的知识提升。</li></ul> |

下图显示了一个包含客户拥有的 Azure Front Door 实例的 Commerce 基础结构。

![包含客户拥有的 Azure Front Door 实例的 Commerce 基础结构。](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>使用外部 CDN 服务

下表列出了使用外部 CDN 服务管理内容终结点的利弊。

| 优点 | 缺点 |
|------|------|
| <ul><li>当现有域已经托管在外部 CDN 上时，此选项很有用。</li><li>WAF：依赖外部提供程序。</li></ul> | <ul><li>需要单独的合同和额外的成本计算。</li><li>SSL 可能会产生额外费用。</li><li>由于该服务与 Azure 云结构是分开的，因此必须管理其他基础结构。</li><li>该服务可能需要在终结点和安全性设置上投入较多时间。</li><li>此服务是自我托管型服务。</li><li>此服务是自我监控型服务。</li></ul> |

下图显示了包含外部 CDN 服务的 Commerce 基础结构。

![包含外部 CDN 服务的 Commerce 基础结构。](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>其他资源

[添加对内容分发网络 (CDN) 的支持](add-cdn-support.md)
