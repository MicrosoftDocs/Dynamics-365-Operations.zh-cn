---
title: 配置 Dynamics 365 Commerce 预览环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 预览环境。
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426457"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>配置 Dynamics 365 Commerce 预览环境


[!include [banner](includes/banner.md)]

本主题说明如何预配 Dynamics 365 Commerce 预览环境。

在开始之前，我们建议您快速浏览本主题以了解该过程的要求。

> [!NOTE]
> 如果您尚未获得 Dynamics 365 Commerce 预览的访问权限，可以从 [Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)申请预览访问权限。

## <a name="overview"></a>概览

要成功预配 Commerce 预览环境，您必须创建一个具有特定产品名称和类型的项目。 此环境和 Commerce Scale Unit (CSU) 还具有某些特定参数，以后在预配电子商务时必须使用这些参数。 本主题中的说明介绍完成预配所需的所有步骤以及必须使用的参数。

成功预配 Commerce 预览环境后，还必须完成一些预配后步骤来准备它。 其中一些步骤可选，具体取决于要评估系统的哪些方面。 您可以在以后随时完成可选步骤。

有关在预配后如何预配 Commerce 预览环境的信息，请参阅[预配 Commerce 预览环境](cpe-post-provisioning.md)。 有关为 Commerce 预览环境预配可选功能的信息，请参阅[为 Commerce 预览环境预配可选功能](cpe-optional-features.md)。

如果对预配步骤有任何疑问或遇到了任何问题，请通过 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)告知 Microsoft。

## <a name="prerequisites"></a>先决条件

必须先满足以下先决条件，才能预配 Commerce 预览环境：

- 您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。
- 您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并能够创建 Dynamics 365 Commerce 项目。
- 您已获准加入 Dynamics 365 Commerce 预览计划。
- 您拥有必需的权限，可以为**迁移、创建解决方案和了解**创建项目。
- 您是我们将为其预配环境的项目的**环境管理员**或**项目负责人**角色的成员。
- 您有 Microsoft Azure 订阅的管理员访问权限，或您与可以代表您完成需要管理员权限的两步的订阅管理员有联系。
- 您有可用的 Azure Active Directory (Azure AD) 租户 ID。
- 您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。
- 您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。 （此安全组可以与电子商务系统管理员组相同。）

## <a name="provision-your-commerce-preview-environment"></a>预配您的 Commerce 预览环境

这些过程说明如何预配 Commerce 预览环境。 成功完成这些过程之后，Commerce 预览环境将可以进行配置。 此处介绍的所有活动都在 LCS 门户中进行。

> [!IMPORTANT]
> 预览访问权限与您在 Commerce 预览应用程序中指定的 LCS 帐户和组织关联。 您必须使用相同的帐户来预配 Commerce 预览环境。 如果需要为 Commerce 预览环境使用其他 LCS 帐户或租户，则必须将这些详细信息提供给 Microsoft。 有关联系信息，请参阅本主题后面的 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>确认预览功能可用且已在 LCS 中打开

要确认预览功能可用且已在 LCS 中打开，请按照下列步骤操作。

1. 使用用于请求预览访问权限的相同 LCS 帐户登录到 [LCS 门户](https://lcs.dynamics.com)。
1. 在 LCS 主页上，滚动到最右侧，然后选择**预览功能管理**磁贴。

    ![预览管理磁贴](./media/preview1.png)

1. 向下滚动到**专用预览功能**，确认以下功能可用且已打开：

    - 电子商务评估
    - 商务预览计划环境

    ![专用预览功能](./media/preview2.png)

1. 如果这些功能没有出现在列表中，请与 Microsoft 联系，并提供您的工作电子邮件地址、LCS 帐户和租户详细信息。 有关联系信息，请参阅 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。

### <a name="create-a-new-project"></a>创建新项目

若要在 LCS 中创建新项目，请按以下步骤进行操作。

1. 在 LCS 主页上，选择加号 (**+**) 创建一个项目。
1. 在右窗格中，请按照下列步骤之一操作：

    - 如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。
    - 如果您是客户，请选择**潜在售前支持**。

1. 输入名称、描述和行业。
1. 在**产品名称**字段中，选择 **Dynamics 365 Retail**。
1. 在**产品版本**字段中，选择 **Dynamics 365 Retail**。
1. 在**方法**字段中，选择 **Dynamics Retail 实施方法**。
1. 可选：您可以从现有项目导入角色和用户。
1. 选择**创建**。 将出现项目视图。

### <a name="add-the-azure-connector"></a>添加 Azure 连接器

要将 Azure 连接器添加到您的 LCS 项目，请按照下列步骤操作。

1. 按以下步骤之一：

    - 如果您是合作伙伴，请选择最右边的**项目设置**磁贴。
    - 如果您是客户，请在顶部菜单中选择**项目设置**。

1. 选择 **Azure 连接器**。
1. 选择**添加**添加 Azure 连接器。
1. 输入名称。
1. 输入您的 Azure 订阅 ID。
1. 打开**配置为使用 Azure 资源管理器(ARM)** 选项。
1. 验证 **Azure 订阅 AAD 租户域(或 ID)** 值是否正确。 根据需要咨询 Azure 订阅管理员。
1. 选择**下一步**。
1. 按照页面上的说明为所需应用程序授予订阅的访问权限。 根据需要咨询 Azure 订阅管理员。

    1. 登录 [Azure 门户](https://portal.azure.com/)。
    1. 确保选择了正确的目录，然后在左侧菜单上选择**订阅**。
    1. 在列表中找到正确的订阅并选择它。 根据需要使用搜索功能。
    1. 在菜单上，选择**访问控制(IAM)**。
    1. 在右侧，在**添加角色分配**下，选择**添加**。 将显示**添加角色分配**窗格。
    1. 在**角色**字段中，选择**参与者**。
    1. 在**将访问权限分配到**字段中，保留默认值 **Azure AD 用户、组或服务主体**。
    1. 在**选择**下，输入 **b96b7e94-b82e-4e71-99a0-cf7fb188acea**。
    1. 在列表中选择**动态部署服务 \[wsfed-enabled\]**。
    1. 选择**保存**。

1. 选择**下一步**。
1. 按照页面上的说明为所需应用程序授予订阅的访问权限。 根据需要咨询 Azure 订阅管理员。
1. 选择**下一步**。
1. 在 **Azure 区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。
1. 选择**连接**。 应该会在列表中显示您的 Azure 连接器。

### <a name="import-the-commerce-preview-demo-base-extension"></a>导入 Commerce 预览演示库扩展

要将 Commerce 预览演示库扩展导入到您的项目中，请按照下列步骤操作。

1. 通过选择顶部的项目名称打开项目的主页。
1. 按以下步骤之一：

    - 如果您是合作伙伴，请选择最右边的**资产库**磁贴。
    - 如果您是客户，请在顶部菜单中选择**资产库**。

1. 在左侧列表中，选择**软件可部署包**。
1. 选择**导入**。
1. 在**共享资产库**下，在资产列表中选择 **Commerce 预览演示库扩展**。
1. 选择**选取**。 您已回到资产库，应该可以在列表中看到此扩展。

下图显示了必须在 LCS **资产库**页上执行的操作。

![导入 Commerce 预览演示库扩展](./media/import.png)

### <a name="deploy-the-environment"></a>部署环境

要部署环境，请按照下列步骤操作。

> [!NOTE]
> 您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。 在**环境参数**视图中时，请确认文本 **Dynamics 365 Commerce - 演示(具有平台更新 *xx* 的 10.0.* x*)**直接出现在**环境名称**字段上方。 有关详细信息，请参阅步骤 8 之后出现的图示。

1. 在顶级菜单上，选择**云托管的环境**。
1. 选择**添加**添加环境。
1. 在**应用程序版本**字段中，选择最新版本。 如果您明确需要选择除最新版本以外的其他应用程序版本，请不要选择 **10.0.8** 之前的版本。
1. 在**平台版本**字段中，使用为所选应用程序版本自动选择的平台版本。 

    ![选择应用程序和平台版本](./media/project1.png)

1. 选择**下一步**。
1. 选择**演示**作为环境拓扑。

    ![选择环境拓扑 1](./media/project2.png)

1. 选择 **Dynamics 365 Commerce - 演示**作为环境拓扑。 如果前面仅配置了一个 Azure 连接器，将把该连接器用于此环境。 如果配置了多个 Azure 连接器，则可以选择要使用的连接器：**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。 （为获得最佳的端到端性能，我们建议您选择**美国西部 2**。）

    ![选择环境拓扑 2](./media/project3.png)

1. 在**部署环境**页面上，输入环境名称。 高级设置保持原样。

    ![部署环境页面](./media/project4.png)

1. 根据需要调整 VM 大小。 （我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）
1. 查看定价和许可条款，然后选中指示您同意这些条款的复选框。
1. 选择**下一步**。
1. 在部署确认页面，验证详细信息是否正确，然后选择**部署**。 您已返回到**云托管的环境**视图，列表中应该会显示您的环境。

    您请求的环境将显示为已入队列，然后是正在部署。 环境工作流将需要一些时间完成。 因此，请在大约六到九小时后再次检查。

1. 继续操作之前，确保环境的状态为**已部署**。

### <a name="initialize-the-commerce-scale-unit-cloud"></a>初始化 Commerce Scale Unit（云）

要初始化您的 CSU，请遵循以下步骤。

1. 在**云托管的环境**视图中，在列表中选择您的环境。
1. 在右侧的环境视图中，选择**完整详细信息**。 将显示环境详细信息视图。
1. 在**环境功能**下，选择**管理**。
1. 在**商业**选项卡上，选择**初始化**。 将显示 CSU 初始化参数视图。
1. 在**区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。
1. 在**版本**字段中，在列表中选择**指定版本**，然后在出现的字段中指定 **9.18.20014.4**。 请确保指定此处指示的确切版本。 否则，您以后不得不将 RCSU 更新到正确的版本。
1. 打开**应用扩展**选项。
1. 在扩展列表中，选择 **Commerce 预览演示库扩展**。
1. 选择**初始化**。
1. 在部署确认页面，验证详细信息是否正确，然后选择**是**。 **商业管理**视图再次显示，其中的**商业**选项卡被选中。 您的 CSU 现在已进入队列等待配置。
1. 继续操作之前，确保 CSU 的状态为**成功**。 初始化大约需要两到五个小时。

### <a name="initialize-e-commerce"></a>初始化电子商务

要初始化电子商务，请遵循以下步骤。

1. 在**电子商务**选项卡上，查看预览同意内容，然后选择**设置**。
1. 在**电子商务租户名称**字段中，输入名称。 但是，请注意，某些指向您的电子商务实例的 URL 中将显示此名称。
1. 在 **Commerce Scale Unit 名称**字段中，在列表中选择您的 CSU。 （此列表应该只有一个选项。）

    **电子商务地理位置**字段是自动设置的，此值无法更改。

1. 选择**下一步**继续。
1. 在**支持的主机名**字段中，输入任意有效域，例如 `www.fabrikam.com`。
1.  在**系统管理员的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。 选择放大镜图标以显示搜索结果。 从列表中选择正确的安全组。
2.  在**评级和审查仲裁者的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。 选择放大镜图标以显示搜索结果。 从列表中选择正确的安全组。
1. 保留**启用评级和审查服务**选项为打开。
1. 选择**初始化**。 **商业管理**视图再次显示，其中的**电子商务**选项卡被选中。 电子商务初始化已开始。
1. 请等待电子商务初始化的状态成为**初始化成功**，再继续操作。
1. 在右下方的**链接**下，记下以下链接的 URL：

    * **电子商务站点** – 指向您的电子商务站点的根目录的链接。
    * **电子商务站点管理工具** – 站点管理工具的链接。

## <a name="commerce-preview-environment-support"></a>Commerce 预览环境支持

如果您在完成预配步骤时遇到问题，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)获取帮助。

## <a name="next-steps"></a>后续步骤

要继续 Commerce 预览环境的预配和配置过程，请参阅[配置 Commerce 预览环境](cpe-post-provisioning.md)。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 预览环境概览](cpe-overview.md)

[配置 Dynamics 365 Commerce 预览环境](cpe-post-provisioning.md)

[为 Dynamics 365 Commerce 预览环境配置可选功能](cpe-optional-features.md)

[Dynamics 365 Commerce 预览环境常见问题](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit（云）](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)

