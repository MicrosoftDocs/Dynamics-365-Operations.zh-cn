---
title: Commerce 预览环境常见问题
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 预览环境的常见问题的解答。
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
ms.openlocfilehash: 53e593931850d6b8b22bb756d5828f742416aa4d
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906085"
---
# <a name="commerce-preview-environment-faq"></a>Commerce 预览环境常见问题

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

本主题提供对有关 Microsoft Dynamics 365 Commerce 预览环境的常见问题的解答。

**我可以将 Commerce 预览环境的邀请转移到另一个租户吗？**

是。 对于邀请转移，您可以使用 [Commerce 预览转移窗体](https://aka.ms/Dynamics365CommercePreviewTransferForm)。

**邀请转移需要多长时间？**

转移平均需要大约三到五个工作日。 但是，可能会有例外。

**Commerce 预览环境是否可以处理 Dynamics 365 Finance 或 Dynamics 365 Supply Chain 项目？**

编号 Commerce 预览环境只能处理 Dynamics 365 Retail 项目。

**我们是否可以将 Commerce 预览环境用作当前实现 Retail 的客户的电子商务店面？**

编号 Commerce 预览环境只是评估环境。 如果您需要针对实现 Retail 的客户的环境，请与 Microsoft 联系。

**可以使用 Commerce 预览环境在实现 Retail 的现有应用程序/环境基础上预配电子商务功能吗？**

编号 当前，只有在具有 10.0.6 版的演示数据的 Retail 库存单位 (SKU) 项目中部署的新环境中，才可以使用 Commerce 预览环境。

**通过 Microsoft Dynamics Lifecycle Services (LCS) 在 Microsoft Azure 上部署 Commerce 预览环境会产生哪些成本？**

Retail 是您的订阅中托管的唯一组件。 其他组件，例如 Retail Cloud Scale Unit (RCSU) 和电子商务将托管在 Microsoft 订阅中。 您可以使用 [Azure 定价计算器](https://azure.microsoft.com/pricing/calculator/)估算此成本。

**Commerce 预览环境当前支持哪些 Azure 地理位置？**

Commerce 预览环境只能在北美地区部署 。

**是否有具有完整的 OneBox 虚拟机 (VM) 选项的可下载虚拟硬盘 (VHD)？**

Dynamics 365 Retail Cloud Scale Unit (RCSU) 和电子商务完全是软件即服务 (SaaS) 形式的，必须托管在云中。

**Commerce 预览环境可以使用多长时间？**

自预配电子商务之日起，Commerce 预览环境的使用期限为 30 天。

**我可以延长我的 Commerce 预览环境的时间限制吗？**

是。 您可以使用 [Commerce 预览延长窗体](https://aka.ms/Dynamics365CommercePreviewExtensionForm)与支持团队联系。

**我们可以多次请求使用 Commerce 预览环境吗？**

每个被接受的请求有一个 Commerce 预览环境的配额。 如果您需要多个预览环境，请与 Microsoft 联系。 有关联系信息，请参阅下一节。

## <a name="dynamics-365-commerce-preview-environment-contact-information"></a>Dynamics 365 Commerce 预览环境联系信息

如果您有关 Commerce 预览环境的问题或要求，需要与 Microsoft 联系，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)寻求帮助。

如果您在尝试访问 Yammer 组时遇到问题，您可以通过电子邮件 <Dynamics365Commerce@microsoft.com> 与 Microsoft 联系。 此电子邮件地址的查看频率较低。 因此，回复会比较迟。

## <a name="additional-resources"></a>其他资源

[Commerce 预览环境概述](cpe-overview.md)

[预配 Commerce 预览环境](provisioning-guide.md)

[配置 Commerce 预览环境](cpe-post-provisioning.md)

[为 Commerce 预览环境配置可选功能](cpe-optional-features.md)
