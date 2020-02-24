---
title: Dynamics 365 Commerce 预览环境概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 预览环境。
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024675"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Dynamics 365 Commerce 预览环境概览


[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 预览环境。

## <a name="overview"></a>概览

Commerce 预览环境是 Dynamics 365 Commerce 的一个可选的端到端预览环境，让潜在客户可以在 Commerce 产品向公众发布之前试用该产品。

除了一些不影响特性或功能的小限制外，Commerce 预览环境提供了完整的 Commerce 体验，客户和实现合作伙伴可以使用它来评估产品、提供反馈以及进行适应/差距分析。

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce 预览环境的限制

虽然 Commerce 预览环境提供了完整的 Commerce 特性和功能集，但仍存在一些小的限制：

- 尽管 Commerce 预览环境本身没有地理限制，但是环境的组件（例如 Retail Cloud Scale Unit (RCSU) 和电子商务应用程序）只能在美国预配。
- Commerce 预览环境的使用限制在从预配电子商务之日起 30 天。
- Commerce 预览环境只能在使用演示拓扑的环境中成功部署和初始化，环境的所有组件都部署在一个虚拟机 (VM) 中。 这种 OneBox VM 拓扑的主要限制是对于预览环境可以支持的并发用户数。
- Commerce 预览环境只能在 Commerce 产品公开发布 (GA) 之前评估。 GA 之后将提供新的演示环境。

## <a name="get-started"></a>入门

要预配 Commerce 预览环境，请参阅[预配 Commerce 预览环境](provisioning-guide.md)。

## <a name="additional-resources"></a>其他资源

[配置 Dynamics 365 Commerce 预览环境](provisioning-guide.md)

[配置 Dynamics 365 Commerce 预览环境](cpe-post-provisioning.md)

[为 Dynamics 365 Commerce 预览环境配置可选功能](cpe-optional-features.md)

[Dynamics 365 Commerce 预览环境常见问题](cpe-faq.md)
