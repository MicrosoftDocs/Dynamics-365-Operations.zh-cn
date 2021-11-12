---
title: 使用 LBD 在自定义硬件上部署边缘缩放单元（预览）
description: 本主题介绍如何使用基于本地业务数据 (LBD) 的自定义硬件和部署预配本地边缘缩放单元。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678973"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>使用 LBD 在自定义硬件上部署边缘缩放单元（预览）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

边缘缩放单元在 Supply Chain Management 的分布式混合拓扑中起着重要作用。 在混合拓扑中，您可以在 Supply Chain Management 云中心和云中或边缘的其他缩放单元之间分布工作负荷。

可以通过创建本地业务数据 (LBD) [本地环境](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md)来部署边缘缩放单元，然后将其配置为在分布式混合拓扑中充当 Supply Chain Management 的缩放单元。 这通过将本地 LBD 环境与云中的 Supply Chain Management 环境关联来实现，该环境已配置作为中心。  

边缘缩放单元当前处于预览阶段。 因此，您只能根据[预览条款](https://aka.ms/scmcnepreviewterms)使用此类环境。

本主题介绍如何将本地 LBD 环境设置为边缘缩放单元，然后将其与中心关联。

## <a name="deployment-overview"></a>部署概述

以下是部署步骤的概述。

1. **在 Microsoft Dynamics Lifecycle Services (LCS) 中的 LBD 项目中启用 LBD 时间。**

    预览期间，LBD 边缘缩放单元针对现有 LBD 客户。 将仅在特定客户情况下提供额外的 60 天有限 LBD 沙盒时间。

1. **使用 *空* 数据库设置和部署 LBD 环境。**

    使用 LCS 使用最新的拓扑和空数据库部署 LBD 环境。 有关详细信息，请参阅此主题后面的[使用空数据库设置和部署 LBD 环境](#set-up-deploy)一节。 您必须使用 Supply Chain Management 版本 10.0.19 以及跨中心和缩放单元环境的平台更新 43 或更高版本。

1. **将目标包上载到 LCS 中的 LBD 项目资产中。**

    准备跨中心和边缘缩放单元使用的应用程序、平台和自定义包。 有关详细信息，请参阅此主题后面的[将目标包上载到 LCS 中的 LBD 项目资产中](#upload-packages)一节。

1. **使用目标包为 LBD 环境提供服务。**

    此步骤可确保在中心和轮辐上部署相同的版本和自定义。 有关详细信息，请参阅此主题后面的[使用目标包为 LBD 环境提供服务](#service-target-packages)一节。

1. **完成缩放单元配置和工作负荷分配。**

    有关详细信息，请参阅此主题后面的[将 LBD 边缘缩放单元分配给中心](#assign-edge-to-hub)一节。

本主题的其余各节提供有关如何完成这些步骤的更多详细信息。

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>使用空数据库设置和部署 LBD 环境

此步骤创建功能 LBD 环境。 但是，环境不一定具有与中心环境相同的应用程序和平台版本。 而且，它仍然缺少自定义项，且尚未启用作为缩放单元。

1. 请按照[设置并部署本地环境（平台更新 41 及更高版本）](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md)中的说明进行操作。 您必须使用 Supply Chain Management 版本 10.0.19 以及跨中心和缩放单元环境的平台更新 43 或更高版本

    > [!IMPORTANT]
    > 请先阅读此节的其余部分，**然后** 再完成该主题中的步骤。

1. 在 infrastructure\\ConfigTemplate.xml 文件中描述您的配置之前，请运行以下脚本：

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > 此脚本将删除部署边缘缩放单元不需要的任何配置。

1. 设置包含空数据的数据库，如[配置数据库](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)中所述。 对此步骤使用空 data.bak 文件。
1. 设置预部署脚本。 有关详细信息，请参阅[本地代理部署前和部署后脚本](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md)。

    1. 将 **基础结构** 脚本中 **ScaleUnit** 文件夹中的内容复制到环境中设置的代理文件存储共享中的 **Scripts** 文件夹。 典型路径是 \\\\lbdiscsi01\\agent\\Scripts。
    2. 创建将使用所需的参数调用脚本的 **PreDeployment.ps1** 脚本。 预部署脚本必须放入代理文件存储共享中的 **Scripts** 文件夹。 否则无法运行。 典型路径为 \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1。

        PreDeployment.ps1 脚本的内容将类似于以下示例。

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > InstanceId 参数应只有两个字符。 第一个字符是 @，第二个字符可以是英语字母中的任何大写字母。
        >
        > - 有效值：
        >   - @D
        >   - @X
        > - 无效值：
        >   - @a
        >   - @4
        >   - @#

1. 使用可用的最新基础拓扑部署环境。

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>将目标包上载到 LCS 中的 LBD 项目资产中

此步骤准备将转移到 LBD 缩放单元环境的应用程序版本、平台版本和自定义项。

1. 将应用于中心环境的组合的相同应用程序/平台包上载到 LCS 本地项目的资产库中。
1. 获取应用于中心环境的自定义可部署包的副本，并将其上载到 LCS 本地项目的资产库中。

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>使用目标包为 LBD 环境提供服务

此步骤将 LBD 缩放单元环境中的应用程序版本、平台版本和自定义设置与中心保持一致。

1. 使用您在上一步中上载的组合应用程序/平台包为 LBD 环境提供服务。
1. 使用您在上一步中上载的自定义可部署包为 LBD 环境提供服务。

    ![选择“维护 > 在 LCS 中应用更新”。](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "选择“维护 > 在 LCS 中应用更新”")

    ![选择自定义包。](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "选择自定义包")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>将 LBD 边缘缩放单元分配给中心

虽然边缘缩放单元仍在预览阶段，但您必须使用 GitHub 上提供的[缩放单元部署和配置工具](https://github.com/microsoft/SCMScaleUnitDevTools)才能将 LBD 边缘缩放单元分配给中心。 此过程使 LBD 配置能够充当边缘缩放单元并将其与中心关联。 此过程与配置一体框开发环境相似。

1. 下载 [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) 的最新版本并解压缩文件的内容。
1. 创建 `UserConfig.sample.xml` 文件的副本并将其命名为 `UserConfig.xml`。
1. 在您的 Azure AD 租户中创建 Microsoft Azure Active Directory (Azure AD) 应用程序，如[缩放单元和工作负荷的部署指南](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations)中所述。
    1. 创建后，导航到中心上的 Azure AD 应用程序窗体 (SysAADClientTable)。
    1. 创建新条目并将 **客户端 ID** 设置为您创建的应用程序的 ID。 将 **名称** 设置为 *ScaleUnits*，将 **用户 ID** 设置为 *管理员*。

1. 创建一个 Active Directory 联合身份验证服务 (AD FS) 应用程序，如[缩放单元和工作负荷的部署指南](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations)中所述。
    1. 创建后，导航到边缘缩放单元上的 Azure AD 应用程序窗体 (SysAADClientTable)。
    1. 创建新条目并将 **客户端 ID** 设置为您创建的应用程序的 ID。 将 **用户 ID** 设置为 *管理员*。

1. 修改 `UserConfig.xml` 文件。
    1. 在 `InterAOSAADConfiguration` 部分下，输入您之前创建的 Azure AD 应用程序的信息。
        - 在 `AppId` 元素中，输入 Azure 应用程序的应用程序 ID。
        - 在 `AppSecret` 元素中，输入 Azure 应用程序的应用程序密码。
        - `Authority` 元素必须包含指定租户安全机构的 URL。

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. 在 `ScaleUnitConfiguration` 部分下，对于第一个 `ScaleUnitInstance`，修改 `AuthConfiguration` 部分。
        - 在 `AppId` 元素中，输入 Azure 应用程序的应用程序 ID。
        - 在 `AppSecret` 元素中，输入 Azure 应用程序的应用程序密码。
        - `Authority` 元素必须包含指定租户安全机构的 URL。

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. 此外，对于同一个 `ScaleUnitInstance`，设置以下值：
        - 在 `Domain` 元素中，指定中心 URL。 例如：`https://cloudhub.sandbox.operations.dynamics.com/`
        - 在 `EnvironmentType` 元素中，确保设置值 `LCSHosted`。

    1. 在 `ScaleUnitConfiguration` 部分下，对于第二个 `ScaleUnitInstance`，修改 `AuthConfiguration` 部分。
        - 在 `AppId` 元素中，输入 AD FS 应用程序的应用程序 ID。
        - 在 `AppSecret` 元素中，输入 ADFS 应用程序的应用程序密码。
        - `Authority` 元素必须包含 AD FS 实例的 URL。

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. 此外，对于同一个 `ScaleUnitInstance`，设置以下值：
        - 在 `Domain` 元素中，指定边缘缩放单元的 URL。 例如：https://ax.contoso.com/
        - 在 `EnvironmentType` 元素中，确保设置值 LBD。
        - 在 `ScaleUnitId` 元素中，输入您配置 `Configure-CloudandEdge.ps1` 预部署脚本时为 `InstanceId` 指定的相同值。

        > [!NOTE]
        > 如果您未使用默认 Id (@A)，请确保更新“工作负荷”部分下每个 ConfiguredWorkload 的 ScaleUnitId。

1. 打开 PowerShell，导航到包含 `UserConfig.xml` 文件的文件夹。

1. 使用此命令运行工具。

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > 每次操作之后，都必须重新启动工具。

1. 在工具中，选择 **2. 为工作负荷安装准备环境**。 然后运行以下步骤：
    1. 选择 **1. 准备中心**。
    1. 选择 **2. 准备缩放单元**。

    > [!NOTE]
    > 如果您不是从洁净安装运行此命令并且命令失败，请执行以下操作：
    >
    > - 删除 `aos-storage` 文件夹中的所有文件夹（`GACAssemblies` 除外）。
    > - 在业务数据库 (AXDB) 上运行以下 SQL 命令：
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. 在业务数据库 (AXDB) 上运行以下 SQL 命令：

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. 验证是否已在业务数据库 (AXDB) 上启用更改跟踪
    1. 启动 SQL Server Management Studio (SSMS)。
    1. 右键单击业务数据库 (AXDB)，选择属性。
    1. 在打开的窗口中，选择 **更改跟踪** 并进行以下设置：

        - **更改跟踪**：*True*
        - **保留期**：*7*
        - **保留单位**：*天*
        - **自动清理**：*True*

1. 在工具中，选择 **3. 安装工作负荷**。 然后运行以下步骤：
    1. 选择 **1. 在中心上安装**。
    1. 选择 **2. 在缩放单元上安装**。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
