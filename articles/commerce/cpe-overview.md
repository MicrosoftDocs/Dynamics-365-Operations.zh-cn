---
title: Dynamics 365 Commerce 评估环境概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 评估环境。
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f225db13fba91ce78287adfda9c6d084dea20af33e62287f517e51cc5a296352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752504"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Dynamics 365 Commerce 评估环境概览

[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 评估环境。

> [!NOTE]
> Commerce 评估环境不是公开发布的服务，它根据请求授予合作伙伴和客户使用权。 有关详细信息，请联系您的 Microsoft 合作伙伴联系人。

Commerce 评估环境是 Dynamics 365 Commerce 的一个可选的端到端环境，让合作伙伴和潜在客户可以试用 Commerce 产品。

评估环境已部分预配置，以减少所需的预配后步骤。

除了一些不影响特性或功能的小限制外，Commerce 评估环境提供了完整的 Commerce 体验，客户和实现合作伙伴可以使用它来评估产品、提供反馈以及进行适应/差距分析。

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Commerce 评估环境的限制

虽然 Commerce 评估环境提供了完整的 Commerce 特性和功能集，但仍存在一些小的限制：

- 尽管 Commerce 评估环境本身没有地理限制，但是环境的组件（例如 Retail Cloud Scale Unit (RCSU) 和电子商务应用程序）应只在美国预配。
- Commerce 评估环境的使用限制在从预配电子商务之日起 30 天。
- Commerce 评估环境只能在使用演示拓扑的环境中成功部署和初始化，环境的所有组件都部署在一个云托管的虚拟机 (VM) 中。 这种拓扑的主要限制是对于环境可以支持的并发用户数。

## <a name="get-started"></a>开始

要预配 Commerce 评估环境，请参阅[预配 Commerce 评估环境](provisioning-guide.md)。

## <a name="additional-resources"></a>其他资源

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)

[Dynamics 365 Commerce 评估环境常见问题](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
