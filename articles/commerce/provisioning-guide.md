---
title: 配置电子商务评估环境
description: 此指南提供有关设置和配置 Microsoft Dynamics 365 Commerce 预览环境的分步说明。
author: v-chgri
manager: annbe
ms.date: 10/15/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771672"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>配置电子商务评估环境

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此指南提供有关设置和配置 Microsoft Dynamics 365 Commerce 预览环境的分步说明。 建议您首先至少快速浏览本文档以大致了解流程涉及的内容和指南包含的内容。

*注意：如果您尚未获得 Microsoft Dynamics 365 Commerce 预览的访问权限，可以从 [Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)申请预览访问权限。*

## <a name="summary"></a>摘要
若要成功配置环境，需要使用特定项目名称和类型创建项目。 环境和 Retail Cloud Scale Unit 页采用一些您需要用来以后启动电子商务配置的特定参数。 本指南中的说明包含您必须执行的所有步骤和需要使用的参数。

成功配置之后，需要执行一些配置后步骤来准备预览环境。 其中一些步骤可选，具体取决于要评估系统的哪些方面。 如果以后更改主意，以后始终可以运行可选步骤。

如果对配置步骤有任何疑问或遇到了任何问题，请通过 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)告知我们。 

## <a name="prerequisites"></a>先决条件
下面是配置 Dynamics 365 预览环境的先决条件：
* 您拥有 **Lifecycle Services 门户 (LCS)** 的访问权限
* 您已**获准加入 Dynamics 365 Commerce 预览计划**
* 您拥有足够权限，可以为**潜在售前支持**或**迁移，创建解决方案，了解**创建项目
* 您是我们将为其配置环境的项目的**环境管理员**或**项目负责人**角色的成员
* 您有 Azure 订阅的管理员访问权限，或您与可以代表您执行需要管理员权限的两步的订阅管理员联系
* 您有 **AAD 租户 ID**
* 您已创建了要用作**电子商务系统管理员组**的 **AAD 安全组**，并且您有其 ID
* 您已创建了要用作**评分和评价审查者组**的 **AAD 安全组**，并且您有其 ID（与上面的系统管理员组是同一个 SG）
## <a name="provisioning-preview-environment"></a>配置预览环境
这些说明介绍如何配置 Microsoft Dynamics 365 Commerce 预览环境。 成功完成这些步骤后，即准备好了要配置的预览环境。 此处介绍的所有活动都在 LCS 门户中进行。

*请注意，预览访问权限与您在预览应用程序中指定的 LCS 帐户和组织绑定。您需要使用同一个帐户来进行配置。如果必须对预览环境使用其他 LCS 帐户或租户，您需要向我们提供这些详细信息。有关联系信息，请参阅下面的“其他资源”。*
### <a name="before-starting"></a>准备工作
##### <a name="grant-access-to-e-commerce-applications"></a>授予电子商务应用程序的访问权限

*注意：**只有 AAD 租户管理员才能登录**。如果无法完成此步骤，其余配置步骤将失败。*

1. 需要 **AAD 租户 ID** 才能完成此步骤。您需要为电子商务应用程序授予您的 Azure 订阅的访问权限。 最简单的方法是创建如下 URL：

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **切勿直接单击此 URL**，而是将其复制粘贴到浏览器或文本编辑器中，然后将 **\{AAD_TENANT_ID\}** 替换为您的 **AAD 租户 ID**，之后再导航到此 URL。
3. 将显示 Microsoft AAD 登录对话框，您需要在这里确认要为“Dynamics 365 Commerce (预览)”授予您的订阅的访问权限。
4. 将把您带到一个页面，用于确定操作是否成功。

##### <a name="log-in-to-the-lcs"></a>登录到 LCS
1. 登录到 LCS 门户：https://lcs.dynamics.com
1. 确保使用用于申请预览访问权限的同一个 LCS 帐户登录。
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>确认预览功能可用且已启用
1. 在 LCS 标题页中，滚动到最右侧，然后单击**预览功能管理**磁贴。
1. 向下滚动到“专用预览功能”，并确保以下功能可用且已启用：
    1. **电子商务评估**
    1. **商务预览计划环境**
1. 如果在列表中看不到这些功能，请联系我们，并提供您的工作电子邮件、LCS 帐户和租户详细信息。 有关如何联系我们的信息，请参阅下面的**其他资源**。

![预览管理磁贴](./media/preview1.png)

![预览功能](./media/preview2.png)
### <a name="create-project"></a>创建项目
##### <a name="creating-new-project"></a>创建新项目
1. 单击 **+** 创建新项目。
1. 如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。
1. 如果您是客户，请选择**潜在售前支持**。
1. 输入您认为适合的名称、描述和行业。
1. **产品名称**选择 **Dynamics 365 Retail**。
1. **产品版本**选择 **Dynamics 365 Retail**。
1. **方法**选择 **Dynamics Retail 实施方法**。
1. 如果需要，可以从现有项目导入角色和用户。
1. 单击**创建**。
1. 将把您带到项目视图。
##### <a name="add-azure-connector"></a>添加 Azure 连接器
1. 如果您是合作伙伴，请单击最右侧工具磁贴中的**项目设置**。
1. 如果您是客户，请从顶部菜单选择**项目设置**。
1. 选择 **Azure 连接器**。
1. 单击 **+ 添加**添加 Azure 连接器。
1. 输入名称。
1. 输入您的 **Azure 订阅 ID**。
1. 启用**配置为使用 Azure 资源管理器(ARM)**。
1. 验证 **Azure 订阅 AAD 租户域(或 ID)** 是否正确。 如有必要，咨询 Azure 订阅管理员。
1. 单击**下一步**。
1. 按照屏幕中的说明为所需应用程序授予订阅的访问权限。 如有必要，咨询 Azure 订阅管理员：
    1. 登录到 Azure 门户：https://portal.azure.com/
    1. 确保已选择了正确的目录。
    1. 单击左侧菜单中的**订阅**。
    1. 在列表中找到正确的订阅并选择。 如果需要，使用搜索。
    1. 在菜单中选择**访问控制 (IAM)**。
    1. 单击右侧**添加角色分配**下的**添加**。 将打开**添加角色分配**窗格。
    1. **角色**选择**参与者**。
    1. 对于**将访问权限分配到**，保持为 **Azure AD 用户、组或服务主体**。
    1. 在**选择**下，输入 **b96b7e94-b82e-4e71-99a0-cf7fb188acea**。
    1. 从列表选择**动态部署服务 [已启用 wsfed]**。
    1. 单击**保存**。
1. 单击**下一步**。
1. 按照屏幕中的说明为所需应用程序授予订阅的访问权限。 如有必要，咨询 Azure 订阅管理员。
1. 单击**下一步**。
1. **Azure 区域**选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。
1. 单击**连接**。
1. 应该会在列表中显示您的 Azure 连接器。
### <a name="import-extension"></a>导入扩展
1. 通过单击顶部的项目名称回到项目标题页。
1. 如果您是合作伙伴，请单击最右侧工具磁贴中的**资产库**。
1. 如果您是客户，请从顶部菜单选择**资产库**。
1. 从左侧列表选择**软件可部署包**。
1. 单击操作窗格中的**导入**。
1. 在**共享资产库**下的资产列表中选择**商务预览演示库扩展**。
1. 单击**选择**。
1. 将回到资产库，应该可以在列表中看到此扩展。

![项目创建 - 版本](./media/import.png)
### <a name="deploy-environment"></a>部署环境

*注意：步骤 6、7 和/或 8 可能不显示，因为跳过了有一个选项的屏幕。在**环境参数**视图中，确定**环境名称**正上方有文本“Dynamics 365 Commerce(预览) - 演示(带平台更新 30 的 10.0.6)”。请参见下面的屏幕截图。*

1. 从顶级菜单，请选择 **管理云的环境**。
1. 单击 **+ 添加**添加环境。
1. **应用程序版本**选择 **10.0.6**。
1. **平台版本**选择**平台更新 30**。
1. 单击**下一步**。
1. 环境拓扑选择 **DEMO**。
1. 环境拓扑选择 **Dynamics 365 Commerce(预览) - 演示**。
1. 如果前面仅配置了一个 Azure 连接器，将把该连接器用于此环境。 如果配置了多个 Azure 连接器，则提供了选项用于选择要使用哪个连接器：**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**（针对最佳端到端性能推荐）
1. 输入一个**环境名称**。
1. 根据需要调整 VM 大小。 （建议使用 VM SKU **D13 v2**。）
1. **高级设置**保持原样。
1. 检查屏幕中的定价和许可条款后，选中框表示同意。
1. 单击**下一步**。
1. 在部署确认屏幕中，验证详细信息正确无误之后，单击**部署**。
1. 将回到**云托管的环境**视图，列表中应该会显示您的环境。
1. 您请求的环境将显示为已入队列，然后是正在部署。 需要一些时间才能完成所有环境工作流，收益请在几小时（大约 6 – 9 个小时）后回来检查。
1. 继续操作之前，确保环境状态为**已部署**。

![项目创建 - 版本](./media/project1.png)

![项目创建 - 拓扑 1](./media/project2.png)

![项目创建 - 拓扑 2](./media/project3.png)

![项目创建 - 环境参数](./media/project4.png)
### <a name="initialize-rcsu"></a>初始化 RCSU
1. 进入**云托管的环境**视图之后，从列表选择您的环境。
1. 在屏幕右侧的环境视图中，单击**完整详细信息**。 将显示环境详细信息视图。
1. 在**环境功能**下，单击**管理**。
1. 在 **Retail** 选项卡中，单击**初始化**。 将显示 RCSU 初始化参数视图。
1. **区域**选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。
1. 对于**版本**，先从下拉列表选择**指定版本**，然后在下面显示的文本字段中指定 **9.16.19262.5**。 *注意：请务必在此处**指定此处列出的精确版本**，以避免以后必须将 RCSU 更新为正确版本。*
1. 启用**应用扩展**。
1. 在扩展列表中，选择**商务预览演示库扩展**。
1. 单击**初始化**。
1. 在部署确认屏幕中，验证详细信息正确无误之后，单击**是**。
1. 将回到 **Retail 管理**视图，其中已激活了 **Retail** 选项卡。 您的 RCSU 现在已进入队列等待配置。
1. 等到 RCSU 状态成为**成功**，再继续操作（需要大约 2 - 5 小时）。
### <a name="initialize-e-commerce"></a>初始化电子商务
1. 切换到**电子商务(预览)** 选项卡。
1. 查看预览同意之后，单击**设置**。
1. 输入**电子商务租户名称**的名称。 但是，请注意，某些指向您的电子商务实例的 URL 中将显示该名称。
1. 对于 **Retail Cloud Scale Unit 名称**，从列表选择您的 RCSU（列表只有一个选项）。
1. 将自动填充**电子商务地理**且不可更改。
1. 单击**下一步**继续。
1. 对于**支持的主机名**，输入任何有效域（例如，www.fabrikam.com）。
1. 对于**系统管理员的 AAD 安全组**，输入要用作电子商务系统管理员组的 AAD SG ID。
1. 对于**评分和评价模块审查者的 AAD 安全组**，输入要用作评分和评价审查者组的 AAD SG ID。
1. 将 **B2C** 值保留为空（7 个以 B2C 开头的字段）。
1. 让**启用评分和评价服务**保持启用状态。
1. 单击**初始化**。
1. 将回到**零售管理**视图，其中已激活了**电子商务(预览)** 选项卡。 已开始初始化您的电子商务。
1. 等待电子商务初始化状态成为**初始化成功**，再继续操作。
1. 在右下部的**链接**下。
    * 记下**电子商务站点**链接。 这是您的 C2 站点的根的链接。
    * 记下**电子商务站点管理工具**链接。 这是站点管理工具（C1 创作工具）的链接。
## <a name="post-provisioning-steps"></a>配置后步骤
此阶段已端到端配置了环境，但是还需要执行配置步骤，才能开始评估环境。
### <a name="before-starting"></a>准备工作
1. 从顶级菜单，请选择 **管理云的环境**。
1. 从列表中选择您的环境。
1. 单击右侧环境信息中的**完整详细信息**。
1. 单击**登录**打开菜单，选择**登录到环境**。

确保选择 **USRT** 法人（右上角）。

### <a name="configure-pos"></a>配置 POS
##### <a name="associate-worker-with-your-identity"></a>将工作人员与您的标识关联
1. 使用左侧菜单转到**模块 > Retail > 员工 > 工作人员**。
1. 在列表中，找到并选择 **000713 - Andrew Collette**。
1. 在操作窗格上，单击 **Retail**。
1. 单击**关联现有标识**。
1. 在（**使用电子邮件搜索**右侧的）**电子邮件**字段中，键入您的电子邮件地址。
1. 单击**搜索**。
1. 选择包含您的姓名的记录。
1. 单击 **确定**。
1. 单击**保存**。
##### <a name="activate-cloud-pos"></a>激活 Cloud POS
1. 登录到 LCS 门户。
1. 导航到您的项目。
1. 从顶级菜单，请选择 **管理云的环境**。
1. 从列表中选择您的环境。
1. 单击右侧环境信息中的**完整详细信息**。
1. 单击**登录**打开菜单，选择**登录到云销售点**，应该将加载 POS。
1. 单击**下一步**。
1. 使用您的 AAD 帐户登录。
1. 在**商店名称**下，选择**旧金山**。
1. 单击**下一步**。
1. 在**收银机和设备**下，选择 **SANFRAN-1**。
1. 单击**启用**。
1. 应该会注销并进入 POS 登录屏幕中。
1. 现在可使用操作员 ID **000713** 和密码 **123** 登录到云 POS 体验。
### <a name="site-setup"></a>站点设置
1. 使用前面记下的 URL 登录到**站点管理工具**。
1. 单击 **Fabrikam** 站点打开站点设置对话框。
1. 对于域，选择之前初始化电子商务时输入的域。
1. 默认渠道选择 **Fabrikam 扩展的在线商店**。 *注意：务必选择**扩展的**在线商店*
1. 默认语言选择 **en-us**。
1. **路径**保持原样。
1. 单击 **确定**。
1. 将把您带到站点中的页面列表。
### <a name="enable-jobs"></a>启用作业
1. 登录到环境（总部）。
1. 使用左侧菜单转到 **Retail > 查询和报表 > 批处理作业**。
1. 对下面列表中的每个作业执行以下步骤：
    * **处理零售订单电子邮件通知**。
    * **产品可用性**。
    * **P-0001**。
    * **同步订单作业**。
1. 使用快速筛选器和（上面列出的）作业名称搜索作业。
1. 如果作业的状态为**预扣**，请执行以下步骤：
    1. 选择记录。
    1. 在操作窗格中，打开**批处理作业**功能区，然后单击**更改状态**。
    1. 选择**正在等待**，然后单击**确定**。
### <a name="run-full-data-sync"></a>运行完全数据同步
1. 使用左侧菜单转到 **模块 > Retail > 总部设置 > 零售调度 > 渠道数据库**。
1. 将从左侧列表选择**默认**渠道。 *选择另一个可用渠道（名称为 **scXXXXXXXXX**）*。
1. 单击操作窗格中的**完全数据同步**。
1. 输入 **9999** 作为配送计划。
1. 单击 **确定**。
1. 单击 **确定**。
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>执行这些步骤之后，即可开始评估您的预览环境！
使用**电子商务站点管理工具** URL 导航到 C1 创作体验，然后使用**电子商务站点** URL 导航到 C2 站点体验。

## <a name="additional-resources"></a>其他资源
### <a name="how-to-find-your-aad-tenant-id"></a>如何查找您的 AAD 租户 ID
AAD 租户 ID 是 GUID，如以下示例所示：**72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>从 Azure 门户
1. 登录到 Azure 门户：https://portal.azure.com/
1. 确保已选择了正确的目录。
1. 单击左侧菜单中的 **Azure Active Directory**。
1. 选择**管理**下的**属性**。
1. 将在**目录 ID** 下显示 AAD 租户 ID。
##### <a name="from-openid-connect-metadata"></a>从 OpenID 连接元数据
通过将 **\{YOUR_DOMAIN\}** 替换为您的域（如 microsoft.com）创建 **OpenID URL**：https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration 将成为 https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. 导航到其中包含您的域的 **OpenID URL**。
1. 可以在多个属性值中看到 AAD 租户 ID。
1. 找到 **authorization_endpoint**，并提取 **login.microsoftonline.com/** 后的 GUID。
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>如何查找您的 AAD 安全组的 ID
AAD 安全组 ID 是 GUID，如以下示例所示：**436ea7f5-ee6c-40c1-9f08-825c5811066a**

此步骤假设用户是其尝试查找的 ID 所属组的成员。
1. 导航到 Graph 资源管理器：https://developer.microsoft.com/en-us/graph/graph-explorer#
1. 单击**通过 Microsoft 登录**，然后使用您的凭据登录。
1. 登录后，单击左侧的**显示更多示例**。
1. 从右窗格启用**组**。
1. 关闭右窗格。
1. 单击**我属于的所有组**。
1. 从**响应预览**文本框找到您的组。
1. 记下属性 **id** 下的安全组 ID。
### <a name="test-credit-card-information-to-perform-test-purchases"></a>测试信用卡信息以执行测试性购买
若要在站点中执行测试交易，可使用此测试信用卡信息：

卡号：4111-1111-1111-1111；到期日期：10/20；CVV：737

*注意：任何情况下均不应在测试站点中尝试使用真正的信用卡信息！*
### <a name="useful-links"></a>有用链接
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure 门户](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)
* [Dynamics 365 Retail 的帮助资源](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Microsoft Dynamics 365 Commerce 预览支持
如果在执行配置步骤时遇到问题，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)获取帮助。 

如果在访问 Yammer 组时遇到问题，也可以通过电子邮件 **Dynamics365Commerce@microsoft.com** 联系我们。 不会主动监控此电子邮件地址，因此应该存在响应延迟。
***
## <a name="prerequisites-for-optional-features"></a>可选功能的先决条件
如果要评估交易电子邮件功能，必须满足以下先决条件：
* 您有可用的电子邮件服务器（SMTP 服务器），可从 Azure 订阅（在其中配置预览环境）使用该服务器。
* 您有该服务器的 FQDN/IP、SMTP 端口号和身份验证详细信息。

如果要评估数字资产管理功能，特别是要使用新的全渠道图像，则必须满足以下先决条件：
* 需要有您的 **CMS 租户名称**。 下面是有关查找此名称的说明。
### <a name="configure-image-backend-optional"></a>后端配置图像（可选）
##### <a name="finding-your-media-base-url"></a>编辑媒体基 URL
*注意：必须先完成**站点设置**，才能完成此步骤。*
1. 使用前面记下的 URL 登录到站点管理工具。
1. 打开 **Fabrikam** 站点。
1. 从左侧菜单中选择**资产**。
1. 选择任何单个图像资产。
1. 从右侧属性检查器找到**公共 URL**。 其中包含一个 URL。
    * 示例 URL：https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. 将 URL 中的最后一个标识符（上面的示例 URL 中为 MA1nQC）替换为以下字符串：**search?fileName=**
    * 替换后的示例 URL：https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * 这是您的**媒体基 URL** - 请记下。
##### <a name="updating-the-media-base-url"></a>更新媒体基 URL
1. 登录到环境（总部）。
1. 使用左侧菜单转到**模块 > Retail > 渠道设置 > 渠道配置文件**。
1. 单击**编辑**。
1. 在**配置文件属性**中，健康**媒体服务器基 URL** 的属性值替换为您前面创建的**媒体基 URL**。
1. 选择左侧列表中**默认**渠道下的另一个渠道。
1. 在**配置文件属性**下，单击 **+ 添加**。
1. 对于创建的属性，选择**媒体服务器基 URL** 作为属性键，为属性值输入您前面创建的**媒体基 URL**。
1. 单击**保存**。

### <a name="configure-email-server-optional"></a>配置电子邮件服务器（可选）
请注意，必须可从您用于环境的 Azure 订阅访问您在此处输入的 SMTP 服务器或电子邮件服务。
1. 登录到环境（总部）。
1. 使用左侧菜单转到**模块 > Retail > 总部设置 > 参数 > 电子邮件参数**。
1. 单击 **SMTP 设置**选项卡。
1. 在**出站邮件服务器**字段中，键入您的 SMTP 服务器或电子邮件服务的 FQDN 或 IP 地址。
1. 在 **SMTP 端口号**字段中，输入端口号（不使用 SSL 时，默认值为 25）。
1. 在**用户名**字段中，键入一个值（如果需要进行身份验证）。
1. 在**密码**字段中，键入一个值（如果需要进行身份验证）。
1. 单击**保存**。
1. 单击**刷新**。
1. 单击**测试电子邮件**选项卡。
1. 在电子邮件提供程序字段中，选择 **SMTP**。
1. 在**发送到**字段中，输入要将测试电子邮件发送到的电子邮件地址。
1. 单击**发送测试电子邮件**。
### <a name="configure-email-templates-optional"></a>配置电子邮件模板（可选）
需要使用有效的发件人电子邮件地址更新要为其发送电子邮件的每个交易事件的电子邮件模板。
1. 使用左侧菜单转到**模块 > 组织管理 > 设置 > 组织电子邮件模板**。
1. 单击**显示列表**。
1. 对于列表中的每个模板：
    1. 在**发件人电子邮件**字段中，键入此电子邮件模板的发件人电子邮件地址。
    1. （可选）在**发件人姓名**字段中，键入要用作此电子邮件模板的发件人的姓名。
1. 单击**保存**。
### <a name="customizing-email-templates-optional"></a>自定义电子邮件模板（可选）
您可能希望自定义电子邮件模板以使用其他图像，或更新模板中的链接以链接回您的预览环境。 下面的步骤介绍如何下载默认模板，自定义默认模板和更新系统中的模板。
1. 使用浏览器将 [Microsoft Dynamics 365 Commerce 预览默认电子邮件模板 .zip 文件](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)（其中包含以下 HTML 文档）下载到本地计算机。
    1. 订单确认模板
    1. 颁发礼品卡模板
    1. 新订单模板
    1. 打包订单模板
    1. 选择订单模板
1. 使用文本编辑器或 HTML 编辑器自定义模板。 请参阅下面的支持的令牌的列表。
1. 登录到环境（总部）。
1. 使用左侧菜单转到**模块 > Retail > 总部设置 > 参数 > 组织电子邮件模板**。
1. 展开左侧列表查看所有模板。
1. 为要自定义的每个模板执行以下步骤：
    1. 从列表中选择模板。
    1. 在**电子邮件内容**下，从列表选择相应语言版本（默认值为 **en-us**）。
    1. 在**电子邮件内容**下，单击**编辑**；您应该会看到打开了**上传电子邮件模板**窗格。
    1. 单击**浏览**，然后找到包含自定义的内容的 HTML 文件。
    1. 单击**上传**，将把您的模板上传到系统，并显示预览。
    1. 单击 **确定**。
    1. （可选）自定义模板的**主题**属性。
    1. 单击**保存**。

#### <a name="supported-tokens-in-the-email-template"></a>电子邮件模板中支持的令牌
将在显示电子邮件时把这些令牌替换为应用于客户及其订单的实际值。

**销售订单** - 以下令牌应用于整个销售订单。

|令牌的名称|标志|
|---|---|
|转移单编号|%salesid%|
|客户名称|%customername%|
|交货地址|%deliveryaddress%|
|帐单地址|%customeraddress%|
|订货日期|%shipdate%|
|传递模式|%modeofdelivery%|
|折扣|%discount%|
|销售税|%tax%|
|订单合计|%total%|

**销售行** - 将填写订单中每个产品的以下令牌。

*注意：将**产品列表 - 开始**和**产品列表 - 结束**令牌放到每个产品重复的 HTML 块的开始和结束处。*

|令牌的名称|标志|
|---|---|
|产品列表 - 开始|\<!--%tablebegin.salesline% -->|
|产品列表 - 结束|\<!--%tableend.salesline%-->|
|产品名称|%lineproductname%|
|说明|%lineproductdescription%|
|数量|%linequantity%|
|行单价|%lineprice%（验证）|
|行项总数|%linenetamount%|
|行折扣|%linediscount%|
|装运日期|%lineshipdate%|
|采购方法|%linedeliverymode%|
|delivery address / 交货地址|%linedeliveryaddress%|
|行的销售单位|%lineunit%|

