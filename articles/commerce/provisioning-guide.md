---
title: 配置 Dynamics 365 Commerce 沙盒环境
description: 本文介绍如何使用内置演示数据为演示或沙盒使用预配 Microsoft Dynamics 365 Commerce 沙盒环境。
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ada30fc9d86d236b71d018ef77f2ae8573f2285
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013126"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>配置 Dynamics 365 Commerce 沙盒环境

[!include [banner](includes/banner.md)]

本文介绍如何使用内置演示数据为演示使用预配 Microsoft Dynamics 365 Commerce 沙盒环境。 设置生产环境的过程类似，但更复杂，因为演示数据中已经提供了许多沙盒环境先决条件。

在开始之前，我们建议您快速浏览本文以了解该过程的要求。

要成功预配 Commerce 沙盒环境，您必须为稍后预配 Commerce 时将使用的环境和 Commerce Scale Unit (CSU) 指定一些参数。 本文中的说明介绍完成预配所需的所有步骤以及必须使用的参数。

成功预配 Commerce 环境后，还必须完成一些预配后步骤来为使用作准备。 其中一些步骤可选，具体取决于要使用系统的哪些方面。 您可以在以后随时完成可选步骤。

有关在预配后如何配置 Commerce 环境的信息，请参阅[配置 Commerce 沙盒环境](cpe-post-provisioning.md)。 有关为 Commerce 环境预配可选功能的信息，请参阅[为 Commerce 沙盒环境配置可选功能](cpe-optional-features.md)。

## <a name="prerequisites"></a>先决条件

必须先满足以下先决条件，才能预配 Commerce 环境：

- 您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。
- 您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并且已创建并可在 LCS 中使用实现项目。  
- 您已创建了可以用作 Commerce 系统管理员组的 Azure Active Directory (Azure AD) 安全组，并且您有它的可用 ID。
- 您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。 （此安全组可以与 Commerce 系统管理员组相同。）
- 您已在 LCS 中部署总部实例。 有关详细信息，请参阅[部署新环境](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)。

请注意，此列表并不详尽。 如果您遇到任何问题，请联系您的 Microsoft 合作伙伴联系人寻求帮助。

## <a name="provision-your-commerce-environment"></a>预配您的 Commerce 环境

以下过程说明如何预配 Commerce 环境。 成功完成这些步骤之后，Commerce 环境将可以进行配置。 下面介绍的所有步骤都在 LCS 门户中进行。

### <a name="initialize-the-commerce-scale-unit-cloud"></a>初始化 Commerce Scale Unit（云）

要初始化 CSU，请遵循以下步骤。

1. 在 LCS 中，从列表中选择您的环境。
1. 在右侧的 **环境** 视图中，选择 **完整详细信息**。 将显示环境详细信息视图。
1. 在 **管理环境** 部分中的 **环境特征** 下，选择 **管理**。
1. 在 **Commerce Scale Units** 选项卡上，选择 **初始化**。 **添加缩放单元** 视图将显示。
1. 在 **区域** 字段中，选择与您将环境部署到的区域相同或接近的区域。
1. 在 **版本** 下拉列表中，选择可用的最新版本。
1. 选择 **初始化**。
1. 在要求您确认 Commerce Scale Unit 初始化的警告对话框中，选择 **是**。 CSU 现在已进入队列等待配置。
1. 继续操作之前，确保 CSU 的状态为 **成功**。 初始化大约需要两到五个小时。

如果在环境详细信息视图中找不到 **管理** 链接，请联系您的 Microsoft 联系人寻求帮助。

### <a name="initialize-e-commerce"></a>初始化电子商务

要初始化 Commerce，请遵循以下步骤。

1. 在 **电子商务** 选项卡中，选择 **设置**。
1. 在 **电子商务环境名称** 字段中，输入名称。 请注意，某些指向您的电子商务实例的 URL 中将显示此名称。
1. 在 **Commerce Scale Unit 名称** 字段中，在列表中选择您的 CSU。 （此列表应该只有一个选项。）

    **电子商务地理位置** 字段是自动设置的。

1. 选择 **下一步** 继续。
1. 在 **支持的主机名** 字段中，输入任意有效域，例如 `www.fabrikam.com`。
1. 在 **系统管理员的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。 在列表中选择正确的安全组。
1.  在 **评级和审查仲裁者的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。 在列表中选择正确的安全组。
1. **启用评分和评价服务** 选项设置保留为 **是**。
1. 选择 **初始化**。 **商业管理** 视图再次显示，其中的 **电子商务** 选项卡被选中。 电子商务初始化已开始。
1. 请等待 Commerce 初始化的状态成为 **初始化成功**，再继续操作。
1. 在右下方的 **链接** 下，记下以下链接的 URL：

    * **电子商务站点** – 指向您的电子商务站点的根目录的链接。
    * **电子商务站点构建器** – 站点管理工具的链接。

## <a name="next-steps"></a>后续步骤

要继续 Commerce 环境的预配和配置过程，请参阅[配置 Commerce 沙盒环境](cpe-post-provisioning.md)。

## <a name="additional-resources"></a>其他资源

[配置 Dynamics 365 Commerce 沙盒环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 沙盒环境中配置 BOPIS](cpe-bopis.md)

[为 Dynamics 365 Commerce 沙盒环境配置可选功能](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit（云）](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
