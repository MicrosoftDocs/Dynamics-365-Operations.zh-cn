---
title: 预配 Dynamics 365 Commerce 评估环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4410641"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>预配 Dynamics 365 Commerce 评估环境

[!include [banner](includes/banner.md)]

本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。

在开始之前，我们建议您快速浏览本主题以了解该过程的要求。

> [!NOTE]
> Commerce 评估环境不是公开发布的服务，它根据请求授予合作伙伴和客户使用权。 有关详细信息，请联系您的 Microsoft 合作伙伴联系人。

## <a name="overview"></a>概览

要成功预配 Commerce 评估环境，您必须创建一个具有特定产品名称和类型的项目。 此环境和 Commerce Scale Unit (CSU) 还具有一些特定的参数，当您以后希望预配电子商务时必须使用这些参数。 本主题中的说明介绍完成预配所需的所有步骤以及必须使用的参数。

成功预配 Commerce 评估环境后，还必须完成一些预配后步骤来为使用作准备。 其中一些步骤可选，具体取决于要评估系统的哪些方面。 您可以在以后随时完成可选步骤。

有关在预配后如何预配 Commerce 评估环境的信息，请参阅[预配 Commerce 评估环境](cpe-post-provisioning.md)。 有关为 Commerce 评估环境预配可选功能的信息，请参阅[为 Commerce 评估环境预配可选功能](cpe-optional-features.md)。

## <a name="prerequisites"></a>先决条件

必须先满足以下先决条件，才能预配 Commerce 评估环境：

- 您已加入评估计划，并获得了评估环境的能力。
- 您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。
- 您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并能够创建 Dynamics 365 Commerce 项目。
- 您具有对 Microsoft Azure 订阅的管理员访问权限，或者在需要时与可以帮助您的订阅管理员联系。
- 您有可用的 Azure Active Directory (Azure AD) 租户 ID。
- 您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。
- 您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。 （此安全组可以与电子商务系统管理员组相同。）

请注意，此列表并不详尽。 如果您遇到任何问题，请联系您的 Microsoft 合作伙伴联系人寻求帮助。

## <a name="provision-your-commerce-evaluation-environment"></a>预配您的 Commerce 评估环境

这些过程说明如何预配 Commerce 评估环境。 成功完成这些过程之后，Commerce 评估环境将可以进行配置。 此处介绍的所有活动都在 LCS 门户中进行。

### <a name="create-a-new-project"></a>创建新项目

若要在 LCS 中创建新项目，请按以下步骤进行操作。

1. 在 LCS 主页上，选择加号 (**+**) 创建一个项目。
1. 在右窗格中，请按照下列步骤之一操作：

    - 如果您是合作伙伴，请选择 **迁移，创建解决方案，了解**。
    - 如果您是客户，请选择 **潜在售前支持**。

1. 输入名称、描述和行业。
1. 在 **产品名称** 字段中，选择 **Dynamics 365 Commerce**。
1. 在 **产品版本** 字段中，选择 **Dynamics 365 Commerce**。
1. 在 **方法** 字段中，选择 **Dynamics Retail 实施方法**。
1. 可选：您可以从现有项目导入角色和用户。
1. 选择 **创建**。 将出现项目视图。

### <a name="add-the-azure-connector"></a>添加 Azure 连接器

要将 Azure 连接器添加到您的 LCS 项目，请按照[完成 Azure 资源管理器 (ARM) 加入流程](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding)中的步骤操作。

### <a name="deploy-the-environment"></a>部署环境

要部署环境，请按照下列步骤操作。

> [!NOTE]
> 您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。 在 **环境参数** 视图中时，请确认文本 **Dynamics 365 Commerce - 演示(具有平台更新 *xx* 的 10.0.* x*)**直接出现在 **环境名称** 字段上方。 有关详细信息，请参阅步骤 8 之后出现的图示。

1. 在顶级菜单上，选择 **云托管的环境**。
1. 选择 **添加** 添加环境。
1. 在 **应用程序版本** 字段中，选择最新版本。 如果您明确需要选择除最新版本以外的其他应用程序版本，请不要选择 **10.0.14** 之前的版本。
1. 在 **平台版本** 字段中，使用为所选应用程序版本自动选择的平台版本。 

    ![选择应用程序和平台版本](./media/project1.png)

1. 选择 **下一步**。
1. 选择 **演示** 作为环境拓扑。

    ![选择环境拓扑 1](./media/project2.png)

1. 在 **部署环境** 页面上，输入环境名称。 高级设置保持原样。

    ![部署环境页面](./media/project4.png)

1. 根据需要调整 VM 大小。 （我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）
1. 查看定价和许可条款，然后选中指示您同意这些条款的复选框。
1. 选择 **下一步**。
1. 在部署确认页面，验证详细信息是否正确，然后选择 **部署**。 您已返回到 **云托管的环境** 视图，列表中应该会显示您的环境。

    您请求的环境将显示为已入队列，然后是正在部署。 环境工作流将需要一些时间完成。 因此，请在大约六到九小时后再次检查。

1. 继续操作之前，确保环境的状态为 **已部署**。

### <a name="initialize-the-commerce-scale-unit-cloud"></a>初始化 Commerce Scale Unit（云）

要初始化您的 CSU，请遵循以下步骤。

1. 在 **云托管的环境** 视图中，在列表中选择您的环境。
1. 在右侧的环境视图中，选择 **完整详细信息**。 将显示环境详细信息视图。
1. 在 **环境功能** 下，选择 **管理**。
1. 在 **商业** 选项卡上，选择 **初始化**。 将显示 CSU 初始化参数视图。
1. 在 **区域** 字段中，选择与您将环境部署到的区域相同或接近的区域。
1. 保留 **版本** 字段不变。
1. 选择 **初始化**。
1. 在部署确认页面，验证详细信息是否正确，然后选择 **是**。 **商业管理** 视图再次显示，其中的 **商业** 选项卡被选中。 您的 CSU 现在已进入队列等待配置。
1. 继续操作之前，确保 CSU 的状态为 **成功**。 初始化大约需要两到五个小时。

如果在环境详细信息视图中找不到 **管理** 链接，请联系您的 Microsoft 联系人寻求帮助。

### <a name="initialize-e-commerce"></a>初始化电子商务

要初始化电子商务，请遵循以下步骤。

1. 在 **电子商务** 选项卡上，查看评估同意内容，然后选择 **设置**。
1. 在 **电子商务环境名称** 字段中，输入名称。 请注意，某些指向您的电子商务实例的 URL 中将显示此名称。
1. 在 **Commerce Scale Unit 名称** 字段中，在列表中选择您的 CSU。 （此列表应该只有一个选项。）

    **电子商务地理位置** 字段是自动设置的。

1. 选择 **下一步** 继续。
1. 在 **支持的主机名** 字段中，输入任意有效域，例如 `www.fabrikam.com`。
1. 在 **系统管理员的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。 在列表中选择正确的安全组。
1.  在 **评级和审查仲裁者的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。 在列表中选择正确的安全组。
1. **启用评分和评价服务** 选项设置保留为 **是**。
1. 选择 **初始化**。 **商业管理** 视图再次显示，其中的 **电子商务** 选项卡被选中。 电子商务初始化已开始。
1. 请等待电子商务初始化的状态成为 **初始化成功**，再继续操作。
1. 在右下方的 **链接** 下，记下以下链接的 URL：

    * **电子商务站点** – 指向您的电子商务站点的根目录的链接。
    * **电子商务站点构建器** – 站点管理工具的链接。

## <a name="next-steps"></a>后续步骤

要继续 Commerce 评估环境的预配和配置过程，请参阅[配置 Commerce 评估环境](cpe-post-provisioning.md)。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)

[Dynamics 365 Commerce 评估环境常见问题](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit（云）](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)
