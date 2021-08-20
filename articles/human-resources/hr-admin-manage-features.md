---
title: 管理 Human Resources 中的功能
description: 了解如何在 Dynamics 365 Human Resources 中打开或关闭新功能。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a9c459b2b34164a9be3ed609a99deb4c5b710d340ef560e6f991e760375d6146
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738359"
---
# <a name="manage-features-in-human-resources"></a>管理 Human Resources 中的功能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在持续推出适用于 Microsoft Dynamics 365 Human Resources 的新功能时，我们希望让客户尽快体验新功能。 我们提供预览功能，这些功能几乎已针对普通使用准备就绪，并经过了大量测试。 我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。

有关 Human Resources 中的新功能的详细信息，请参阅 [Human Resources 中的新增功能](hr-admin-whats-new.md)和 [Dynamics 365 和 Power Platform 版本计划](/dynamics365/release-plans/?panel=products1#pivot=products)。

**功能管理** 工作区提供了每个版本提供的功能列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。 有关功能管理的更多信息，请参阅[功能管理概述](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在 **功能管理** 工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。

某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理** 工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

## <a name="enable-or-disable-preview-features"></a>启用或禁用预览功能

若要访问预览功能，必须首先在您的环境中启用。 预览功能的启用或禁用特定于环境。

> [!IMPORTANT]
> 仅在 **沙盒** 环境中才能使用预览功能。 开启预览功能时，即对组织中该环境的所有用户启用了该预览功能。 关闭预览功能时，即禁用了该预览功能，并且您的用户不能访问该功能。 在 Human Resources 中，对预览功能的支持受限。 预览功能可以使用的隐私和安全措施更少，并且 Human Resources 服务级别协议 (SLA) 中不涵盖预览功能。 不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。

1. 在 Human Resources 中，选择 **系统管理**。

2. 选择 **功能管理** 磁贴。

3. 要启用预览功能，请从列表中选择它，然后选择 **启用**。 要禁用预览功能，请从列表中选择它，然后选择 **禁用**。

## <a name="enable-or-disable-benefits-management"></a>启用或禁用福利管理

若要启用福利管理，请使用[启用或禁用预览功能](hr-admin-manage-features.md?enable-or-disable-preview-features)中的相同过程。

> [!IMPORTANT]
> 不能在 **生产** 环境中禁用已启用的福利管理。 但是可以在 **沙盒** 环境中禁用福利管理。

有关福利管理配置和使用的详细信息，请参阅[福利管理概述](hr-benefits-management-overview.md)。

福利管理取代了 **福利** 工作区中的功能。 启用“福利管理”预览功能后，您将无法再访问 **福利** 工作区的以下窗体：

- **福利**
- **福利元素**
- **缴纳计算比率**
- **福利登记结果**
- **福利到期和延期结果**
- **福利资格策略规则类型**
- **福利资格政策**
- **资格事件**

您可以以只读模式查看这些窗体中的信息。 如果要编辑信息，必须先禁用“福利管理”（仅适用于 **沙盒** 环境）。

## <a name="enable-or-disable-leave-and-absence"></a>启用或禁用休假和缺勤

若要启用休假和缺勤，请使用[启用或禁用预览功能](hr-admin-manage-features.md?enable-or-disable-preview-features)中的相同过程。

> [!IMPORTANT]
> 不能在休假和缺勤中禁用已启用的 **多个休假类型** 功能。 这一条同时适用于 **沙盒** 和 **生产** 环境。

有关休假和缺勤中的预览功能的详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

## <a name="send-us-feedback"></a>向我们发送反馈

希望您提供有关预览功能的体验信息。 希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈：

- [社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。
- 告知我们您希望在产品中看到的功能，或您认为我们应对现有功能进行的任何更改。 提出有关 [Human Resources 想法](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)的产品观点。
    
请勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。 可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。 在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。

## <a name="see-also"></a>请参阅

- [Human Resources 中的新增功能](hr-admin-whats-new.md)
- [Dynamics 365 和 Power Platform 版本计划](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]