---
title: 安装库存可见性加载项
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
ms.openlocfilehash: d6f58eab38d1aee97a5d39704255bf06a168b36c
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581857"
---
# <a name="install-and-set-up-inventory-visibility"></a>安装和设置库存可见性

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

本主题介绍如何安装适用于 Microsoft Dynamics 365 Supply Chain Management 的库存可见性加载项。

若要安装库存可见性加载项，必须使用 Microsoft Dynamics Lifecycle Services (LCS)。 LCS 是一个协作门户，可提供环境和一组定期更新的服务，以帮助您管理 Finance and Operations 应用的应用程序生命周期。

有关详细信息，请参阅 [Lifecycle Services 资源](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)。

## <a name="inventory-visibility-prerequisites"></a>库存可见性的先决条件

在安装库存可见性加载项之前，您必须完成以下任务：

- 获取至少部署了一个环境的 LCS 实施项目。
- 确保已满足安装加载项的先决条件。 有关这些先决条件的信息，请参见[加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。 库存可见性不需要双写入链接。

> [!NOTE]
> 目前支持的国家和地区包括加拿大（CCA、ECA）、美国（WUS、EUS）、欧盟（NEU、WEU）、英国（SUK、WUK）、澳大利亚（EAU、SEAU）、日本（EJP、WJP）和巴西（SBR、SCUS）。

如果您对这些先决条件有任何疑问，请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可视性产品团队联系。

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>安装库存可见性加载项

安装此加载项之前，请注册应用程序，然后在 Azure 订阅下向 Azure Active Directory (Azure AD) 添加一个客户端密钥。 有关说明，请参阅[注册应用程序](/azure/active-directory/develop/quickstart-register-app)和[添加客户端密钥](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)。 请务必记下 **应用程序（客户端）ID**、**客户端密钥** 和 **租户 ID** 值，因为后面需要这些值。

注册应用程序并向 Azure AD 添加客户端密钥后 ，按照以下步骤安装库存可见性加载项。

1. 登录 [LCS](https://lcs.dynamics.com/Logon/Index)。
1. 在主页上，选择在其中部署环境的项目。
1. 在项目页面上，选择要在其中安装加载项的环境。
1. 在环境页上向下滚动，直到在 **Power Platform 集成** 部分中找到 **环境加载项** 部分。 可以在这里找到 Dataverse 环境名称。 确认 Dataverse 环境名称是您要用于库存可见性的名称。

    > [!NOTE]
    > 目前仅支持使用 LCS 创建的 Dataverse 环境。 如果您的 Dataverse 环境是使用其他方法创建的（例如，使用 Power Apps 管理中心创建的），并且其已链接到您的 Supply Chain Management 环境，您必须首先通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 联系库存可见性产品团队解决映射问题。 然后就可以安装库存可见性。

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
1. 在 Dataverse 中，在左侧导航中选择 **应用** 部分，并验证是否已成功安装 **库存可见性** Power Apps。 如果 **应用** 部分不存在，请通过 [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) 与库存可见性产品团队联系。

> [!IMPORTANT]
> 如果您有多个 LCS 环境，请为每个环境创建一个不同的 Azure AD 应用程序。 如果使用相同的应用程序 ID 和租户 ID 为不同环境安装库存可见性加载项，较低版本环境将发生令牌问题。 只有最后安装的才有效。

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>卸载库存可见性加载项

若要卸载库存可见性加载项，请在 LCS 页面上选择 **卸载**。 卸载流程终止库存可见性加载项，从 LCS 注销该加载项，并删除存储在库存可见性加载项数据缓存中的所有临时数据。 但是，不删除您的 Dataverse 订阅中存储的主库存数据。

若要卸载您的 Dataverse 订阅中存储的库存数据，请打开 [Power Apps](https://make.powerapps.com)，在导航栏中选择 **环境**，然后选择与您的 LCS 环境绑定的 Dataverse 环境。 然后转到 **解决方案**，并按以下顺序删除下面的五个解决方案：

1. Dynamics 365 解决方案中适用于库存可见性应用程序的定位点解决方案
1. Dynamics 365 FNO SCM 库存可见性应用程序解决方案
1. 库存服务配置
1. 库存可见性单机版
1. Dynamics 365 FNO SCM 库存可见性基础解决方案

删除这些解决方案之后，也将删除表中存储的数据。

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>在 Supply Chain Management 中设置库存可见性

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

安装此加载项之后，请执行以下步骤准备 Supply Chain Management 系统以使用此加载项。

1. 在 Supply Chain Management 中，打开 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区，然后打开以下功能：
    - *库存可见性集成* – 必需。
    - *带预留抵销的库存可见性集成* – 推荐但可选。 需要版本 10.0.22 或更高版本。 有关详细信息，请参阅[库存可见性预留](inventory-visibility-reservations.md)。

1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**。
1. 打开 **常规** 选项卡，然后设置以下设置：
    - **库存可见性终结点** – 输入运行库存可见性的环境的 URL。 有关详细信息，请参阅[查找服务终结点](inventory-visibility-configuration.md#get-service-endpoint)。
    - **单个请求中的最大记录数** – 设置为单个请求中要包含的最大记录数。 必须输入小于或等于 1000 的正整数。 默认值为 512。 强烈建议您保留默认值，除非您已收到 Microsoft 支持部门的建议或您确信需要更改该值。

1. 如果启用了可选的 *带预留抵销的库存可见性集成* 功能，请打开 **预留抵销** 选项卡，然后进行以下设置：
    - **启用预留抵销** – 设置为 *是* 以启用此功能。
    - **预留抵销修饰符** – 选择将抵销在库存可见性中所做预留的库存交易记录状态。 此设置决定触发抵销的订单处理阶段。 此阶段通过订单的库存交易记录状态跟踪。 选择以下各项之一：
        - *在单* – 对于 *在交易记录* 状态，创建订单时间发送抵销请求。 抵销数量将为所创建订单的数量。
        - *预留* – 对于 *预留订购的交易记录* 状态，对订单进行预留，拣货，过帐装箱单或开票时，订单将发送抵销请求。 此请求仅在上述流程发生时为第一个步骤触发一次。 抵销数量将为其中的相应订单行上库存交易记录状态已从 *在单* 更改为 *订购预留*（或更晚状态）的数量。

1. 转到 **库存管理 \> 定期 \> 库存可见性集成**，启用作业。 现在，来自 Supply Chain Management 的所有库存更改事件都将发布到库存可见性。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
