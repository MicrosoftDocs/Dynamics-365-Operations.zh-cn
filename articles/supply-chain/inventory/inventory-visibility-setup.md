---
title: 安装库存可见性
description: 本主题介绍如何安装适用于 Microsoft Dynamics 365 Supply Chain Management 的库存可见性加载项。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343576"
---
# <a name="set-up-inventory-visibility"></a>安装库存可见性

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

本主题介绍如何安装适用于 Microsoft Dynamics 365 Supply Chain Management 的库存可见性加载项。

若要安装库存可见性加载项，必须使用 Microsoft Dynamics Lifecycle Services (LCS)。 LCS 是一个协作门户，可提供环境和一组定期更新的服务，以帮助您管理 Finance and Operations 应用的应用程序生命周期。

有关详细信息，请参阅 [Lifecycle Services 资源](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)。

## <a name="inventory-visibility-prerequisites"></a>库存可见性的先决条件

在安装库存可见性加载项之前，您必须完成以下任务：

- 获取至少部署了一个环境的 LCS 实施项目。
- 确保已满足安装加载项的先决条件。 有关这些先决条件的信息，请参见[加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。 库存可见性不需要双写入链接。
- 请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可见性产品团队联系，获取以下必需文件：

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip`（如果您运行的 Supply Chain Management 的版本早于版本 10.0.18）

> [!NOTE]
> 目前支持的国家和地区包括加拿大（CCA、ECA）、美国（WUS、EUS）、欧盟（NEU、WEU）、英国（SUK、WUK）和澳大利亚（EAU、SEAU）。

如果您对这些先决条件有任何疑问，请与库存可视性产品团队联系。

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>设置 Dataverse

若要安装 Dataverse，以使其与库存可见性配合使用，请使用 Package Deployer 工具部署库存可见性包。 以下小节介绍如何完成每个任务。

> [!NOTE]
> 目前仅支持使用 LCS 创建的 Dataverse 环境。 如果您的 Dataverse 环境是使用其他方法创建的（例如，使用 Power Apps 管理中心创建的），并且其已链接到您的 Supply Chain Management 环境，您必须首先联系库存可见性产品团队解决映射问题。 然后就可以安装库存可见性。

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>从旧版本 Dataverse 解决方案迁移

如果您已安装旧版本的库存可见性 Dataverse 解决方案，请按照以下说明更新您的版本。 分为两种情况：

- **情况 1：** 如果您的 Dataverse 是通过导入 `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` 解决方案手动安装的，请执行以下步骤：

    1. 下载下面的三个文件：

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. 按照以下步骤将 `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` 和 `InventoryServiceBase_managed.cab` 手动导入 Dataverse 中：

        1. 打开您的 Dataverse 环境的 URL。
        1. 打开 **解决方案** 页。
        1. 选择 **导入**。

    1. 使用 Package Deployer 工具部署 `InventoryServiceApplication.PackageDeployer.zip` 包。 有关说明，请参阅本主题后文的[使用 Package Deployer 工具部署包](#deploy-package)部分。

- **情况 2：** 如果您的 Dataverse 是您在安装旧版本 `.*PackageDeployer.zip` 包之前使用 Package Deployer 工具安装的，请下载 `InventoryServiceApplication.PackageDeployer.zip`，然后执行更新。 有关说明，请参阅[使用 Package Deployer 工具部署包](#deploy-package)部分。

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>使用 Package Deployer 工具部署包

1. 按照[从 NuGet 下载工具](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget)中所述安装开发人员工具。
1. 通过执行以下步骤取消阻止您从 Teams 组下载的 `InventoryServiceApplication.PackageDeployer.zip` 文件：

    1. 选择并按住（或右键单击）文件，然后选择 **属性**。
    1. 在 **属性** 对话框中的 **常规** 选项卡上，找到 **安全** 部分，选择 **取消阻止**，然后应用更改。 如果 **常规** 选项卡上没有 **安全** 部分，说明未阻止该文件。 在这种情况下，请继续到下一步。

    ![取消阻止下载的文件](media/unblock-file.png "取消阻止下载的文件")

1. 解压缩 `InventoryServiceApplication.PackageDeployer.zip` 以查找以下项：

    - `InventoryServiceApplication` 文件夹
    - `[Content_Types].xml` 文件
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` 文件

1. 将这些项目全部复制到 `.\Tools\PackageDeployment` 目录。 （此目录是您在安装开发人员工具时创建的。）
1. 运行 `.\Tools\PackageDeployment\PackageDeployer.exe`，然后按照屏幕上的说明导入解决方案。

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>安装库存可见性加载项

安装此加载项之前，请注册应用程序，然后在 Azure 订阅下向 Azure Active Directory (Azure AD) 添加一个客户端密钥。 有关说明，请参阅[注册应用程序](/azure/active-directory/develop/quickstart-register-app)和[添加客户端密钥](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)。 请务必记下 **应用程序（客户端）ID**、**客户端密钥** 和 **租户 ID** 值，因为后面需要这些值。

注册应用程序并向 Azure AD 添加客户端密钥后 ，按照以下步骤安装库存可见性加载项。

1. 登录 [LCS](https://lcs.dynamics.com/Logon/Index)。
1. 在主页上，选择在其中部署环境的项目。
1. 在项目页面上，选择要在其中安装加载项的环境。
1. 在环境页上向下滚动，直到在 **Power Platform 集成** 部分中找到 **环境加载项** 部分。 可以在这里找到 Dataverse 环境名称。
1. 在 **环境加载项** 部分中，选择 **安装新加载项**。

    ![LCS 中的环境页面](media/inventory-visibility-environment.png "LCS 中的环境页面")

1. 选择 **安装新加载项** 链接。 将显示可用加载项列表。
1. 在列表中选择 **库存可见性**。
1. 针对您的环境设置以下字段：

    - **AAD 应用程序（客户端）ID** – 输入之前创建并记下的 Azure AD 应用程序 ID。
    - **AAD 租户 ID** – 输入之前记下的租户 ID。

    ![设置加载项页面](media/inventory-visibility-setup.png "设置加载项页面")

1. 通过选中 **条款和条件** 复选框同意条款和条件。
1. 选择 **安装**。 加载项的状态将显示为 **正在安装**。 在安装完成时，刷新页面。 状态应更改为 **已安装**。

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>卸载库存可见性加载项

若要卸载库存可见性加载项，请在 LCS 页面上选择 **卸载**。 卸载流程终止库存可见性加载项，从 LCS 注销该加载项，并删除存储在库存可见性加载项数据缓存中的所有临时数据。 但是，不删除您的 Dataverse 订阅中存储的主库存数据。

若要卸载您的 Dataverse 订阅中存储的库存数据，请打开 [Power Apps](https://make.powerapps.com)，在导航栏中选择 **环境**，然后选择与您的 LCS 环境绑定的 Dataverse 环境。 然后转到 **解决方案**，并删除下面的五个解决方案：

- Dynamics 365 解决方案中适用于库存可见性应用程序的定位点解决方案
- Dynamics 365 FNO SCM 库存可见性应用程序解决方案
- 库存服务配置
- 库存可见性单机版
- Dynamics 365 FNO SCM 库存可见性基础解决方案

删除这些解决方案之后，也将删除表中存储的数据。

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>安装 Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>部署库存可见性集成包

如果您运行的是 Supply Chain Management 版本 10.0.17 或更早版本，请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可见性当班支持团队联系获取包文件。 然后在 LCS 中部署包。

> [!NOTE]
> 如果在部署过程中发生版本不匹配错误，则必须手动将 X++ 项目导入到您的开发环境。 然后在您的开发环境中创建可部署包，并在您的生产环境中部署。
>
> 此代码包含在 Supply Chain Management 版本 10.0.18 中。 如果您运行的是该版本或更高版本，则不需要进行部署。

确保在您的 Supply Chain Management 环境中启用了以下功能。 （默认情况下，它们是打开的。）

| 功能描述 | 代码版本 | 切换类 |
|---|---|---|
| 在 InventSum 表上启用或禁用使用库存维度      | 10.0.11 | InventUseDimOfInventSumToggle      |
| 在 InventSumDelta 表上启用或禁用使用库存维度 | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>设置库存可见性集成

1. 在 Supply Chain Management 中，打开 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区，然后打开 *库存可见性集成* 功能。
1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**，输入要运行“库存可见性”的环境的 URL。 有关详细信息，请参阅[查找服务终结点](inventory-visibility-power-platform.md#get-service-endpoint)。
1. 转到 **库存管理 \> 定期 \> 库存可见性集成**，启用作业。 现在，来自 Supply Chain Management 的所有库存更改事件都将发布到库存可见性。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
