---
title: Dynamics 365 Commerce 评估环境常见问题
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410384"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce 评估环境常见问题

[!include [banner](includes/banner.md)]

本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。

**我们是否可以将 Commerce 评估环境用作当前实现 Retail 的客户的电子商务店面？**

编号 Commerce 评估环境仅用于评估。 如果您需要针对实现 Retail 的客户的环境，请与 Microsoft 联系。

**可以使用 Commerce 评估环境在实现 Retail 的现有应用程序/环境基础上预配电子商务功能吗？**

不可以（通常）。 Commerce 评估组件仅可用于与先决条件和预配指南中指定的配置匹配的环境。 此外，所需的基本演示数据在使用 10.0.8 之前的初始版本部署的环境中不可用。 

**通过 Microsoft Dynamics Lifecycle Services (LCS) 在 Microsoft Azure 上部署 Commerce 评估环境会产生哪些成本？**

传统 Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce 总部演示环境（虚拟机 \[VM\]）将托管在 Azure 订阅中。 您可以使用 [Azure 定价计算器](https://azure.microsoft.com/pricing/calculator/)估算此成本。

其他组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）将作为服务型软件 (SaaS) 提供，由 Microsoft 托管。

**Commerce 评估环境当前支持哪些 Azure 地理位置？**

Commerce 评估环境只能在北美地区部署 。

**是否有具有完整的 OneBox 虚拟机 (VM) 选项的可下载虚拟硬盘 (VHD)？**

Dynamics 365 Commerce 和 Commerce Scale Unit 完全是服务型软件 (SaaS)，必须托管在云中。

**Commerce 评估环境可以使用多长时间？**

从 SaaS 组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）预配之日起，Commerce 评估环境的期限为 30 天。

**我可以延长我的 Commerce 评估环境的时间限制吗？**

延长时限是标准之外的一个例外，会根据具体情况加以考虑。 您应该与 Microsoft 合作伙伴联系寻求帮助。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)
