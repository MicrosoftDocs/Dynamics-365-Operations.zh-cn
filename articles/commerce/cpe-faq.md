---
title: Dynamics 365 Commerce 评估环境常见问题
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343550"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce 评估环境常见问题

[!include [banner](includes/banner.md)]

本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>我们是否可以将 Commerce 评估环境用作当前实现 Retail 的客户的电子商务店面？

编号 Commerce 评估环境仅用于评估。 如果您需要针对实现 Retail 的客户的环境，请与 Microsoft 联系。

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>可以使用 Commerce 评估环境在实现 Retail 的现有应用程序/环境基础上预配电子商务功能吗？

不可以（通常）。 Commerce 评估组件仅可用于与先决条件和预配指南中指定的配置匹配的环境。 此外，所需的基本演示数据在使用 10.0.8 之前的初始版本部署的环境中不可用。 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>通过 Microsoft Dynamics Lifecycle Services (LCS) 在 Microsoft Azure 上部署 Commerce 评估环境会产生哪些成本？

传统 Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce 总部演示环境（虚拟机 \[VM\]）将托管在 Azure 订阅中。 您可以使用 [Azure 定价计算器](https://azure.microsoft.com/pricing/calculator/)估算此成本。

其他组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）将作为服务型软件 (SaaS) 提供，由 Microsoft 托管。

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Commerce 评估环境当前支持哪些 Azure 地理位置？

Commerce 评估环境只能在北美地区部署 。

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>是否有具有完整的 OneBox 虚拟机 (VM) 选项的可下载虚拟硬盘 (VHD)？

Dynamics 365 Commerce 和 Commerce Scale Unit 完全是服务型软件 (SaaS)，必须托管在云中。

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Commerce 评估环境可以使用多长时间？

从 SaaS 组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）预配之日起，Commerce 评估环境的期限为 30 天。

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>我可以延长我的 Commerce 评估环境的时间限制吗？

延长时限是标准之外的一个例外，会根据具体情况加以考虑。 您应该与 Microsoft 合作伙伴联系寻求帮助。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
