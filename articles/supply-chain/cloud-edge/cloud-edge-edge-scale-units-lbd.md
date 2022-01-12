---
title: 使用 LBD 在自定义硬件上部署边缘缩放单元
description: 本主题介绍如何使用基于本地业务数据 (LBD) 的自定义硬件和部署预配本地边缘缩放单元。
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2407d4e3c6adaf5df2e8f5440ee8336f86012caf
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920665"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>使用 LBD 在自定义硬件上部署边缘缩放单元

[!include [banner](../includes/banner.md)]

边缘缩放单元在 Supply Chain Management 的分布式混合拓扑中起着重要作用。 在混合拓扑中，您可以在 Supply Chain Management 云中心和云中或边缘的其他缩放单元之间分布工作负荷。

可以通过创建本地业务数据 (LBD) [本地环境](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md)来部署边缘缩放单元，然后将其配置为在分布式混合拓扑中充当 Supply Chain Management 的缩放单元。 这通过将本地 LBD 环境与云中的 Supply Chain Management 环境关联来实现，该环境已配置作为中心。  

本主题介绍如何将本地 LBD 环境设置为边缘缩放单元，然后将其与中心关联。

## <a name="deployment-overview"></a>部署概述

以下是部署步骤的概述。

1. **在 Microsoft Dynamics Lifecycle Services (LCS) 中的 LBD 项目中启用 LBD 时间。**

1. **使用 *空* 数据库设置和部署 LBD 环境。**

    使用 LCS 使用最新的拓扑和空数据库部署 LBD 环境。 有关详细信息，请参阅此主题后面的[使用空数据库设置和部署 LBD 环境](#set-up-deploy)一节。 您必须在中心和缩放单元环境中使用 Supply Chain Management 版本 10.0.21 或更高版本。

1. **将目标包上载到 LCS 中的 LBD 项目资产中。**

    准备跨中心和边缘缩放单元使用的应用程序、平台和自定义包。 有关详细信息，请参阅此主题后面的[将目标包上载到 LCS 中的 LBD 项目资产中](#upload-packages)一节。

1. **使用目标包为 LBD 环境提供服务。**

    此步骤可确保在中心和轮辐上部署相同的版本和自定义。 有关详细信息，请参阅此主题后面的[使用目标包为 LBD 环境提供服务](#service-target-packages)一节。

1. **完成缩放单元配置和工作负荷分配。**

    有关详细信息，请参阅此主题后面的[将 LBD 边缘缩放单元分配给中心](#assign-edge-to-hub)一节。

本主题的其余各节提供有关如何完成这些步骤的更多详细信息。

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>使用空数据库设置和部署 LBD 环境

此步骤创建功能 LBD 环境。 但是，环境不一定具有与中心环境相同的应用程序和平台版本。 而且，它仍然缺少自定义项，且尚未启用作为缩放单元。

1. 请按照[设置并部署本地环境（平台更新 41 及更高版本）](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md)中的说明进行操作。 您必须在中心和缩放单元环境中使用 Supply Chain Management 版本 10.0.21 或更高版本。 此外，您必须使用 2.12.0 或更高版本的基础结构脚本。 

    > [!IMPORTANT]
    > 请先阅读此节的其余部分，**然后** 再完成该主题中的步骤。

1. 在 infrastructure\\ConfigTemplate.xml 文件中描述您的配置之前，请运行以下脚本：

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > 此脚本将删除部署边缘缩放单元不需要的任何配置。

1. 设置包含空数据的数据库，如[配置数据库](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)中所述。 对此步骤使用空 data.bak 文件。
1. 完成[配置数据库](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)步骤后，运行以下脚本来配置缩放单元 Alm 业务流程协调程序数据库。

    > [!NOTE]
    > 在[配置数据库](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)步骤期间，不要配置 Financial Reporting 数据库。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Initialize-Database.ps1 脚本执行以下操作：

    1. 创建名为 **ScaleUnitAlmDb** 的空数据库。
    2. 根据下表将用户映射到数据库角色。

        | 用户            | 类型 | 数据库角色 |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. 继续按照[设置并部署本地环境（平台更新 41 及更高版本）](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md)中的说明进行操作。
1. 完成[配置 AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) 步骤后，执行以下步骤：

    1. 创建一个新的 Active Directory 联合身份验证服务 (AD FS) 应用程序，使 Alm 业务流程服务能够与您的应用程序对象服务器 (AOS) 通信。

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. 创建一个新的 Azure Active Directory (Azure AD) 应用程序，使 Alm 业务流程服务能够与缩放单元管理服务通信。

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. 继续按照[设置并部署本地环境（平台更新 41 及更高版本）](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md)中的说明进行操作。 当您必须输入本地代理的配置时，请确保启用 Edge Scale Unit 功能并提供所有所需的参数。

    ![启用 Edge Scale Unit 功能。](media/EnableEdgeScaleUnitFeatures.png "启用 Edge Scale Unit 功能。")

1. 在从 LCS 部署环境之前，请设置预部署脚本。 有关详细信息，请参阅[本地代理部署前和部署后脚本](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md)。

    1. 将 **基础结构** 脚本中 **ScaleUnit** 文件夹中的 Configure-CloudAndEdge.ps1 脚本复制到环境中设置的代理文件存储共享中的 **Scripts** 文件夹。 典型路径是 \\\\lbdiscsi01\\agent\\Scripts。
    2. 创建将使用所需的参数调用脚本的 **PreDeployment.ps1** 脚本。 预部署脚本必须放入代理文件存储共享中的 **Scripts** 文件夹。 否则无法运行。 典型路径为 \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1。

        PreDeployment.ps1 脚本的内容将类似于以下示例。

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
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
1. 部署环境后，请执行以下步骤：

    1. 在业务数据库 (AXDB) 上运行以下 SQL 命令。

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. 将并发最大批处理会话增加到大于 4 的值。

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. 验证是否已在业务数据库 (AXDB) 上启用更改跟踪。

        1. 打开 SQL Server Management Studio (SSMS)。
        1. 选择并按住（或右键单击）您的业务数据库 (AXDB)，然后选择 **属性**。
        1. 在出现的窗口中，选择 **更改跟踪**，然后设置以下值：

            - **更改跟踪**：*True*
            - **保留期**：*7*
            - **保留单位**：*天*
            - **自动清理**：*True*

    1. 将您之前创建（使用 Create-ADFSServerApplicationForEdgeScaleUnits.ps1 脚本）的 AD FS 应用程序 ID 添加到您的缩放单元中的 Azure AD 应用程序表中。 您可以通过用户界面 (UI) 手动完成此步骤。 或者，您可以使用以下脚本通过数据库完成。

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>设置 Azure 密钥保管库和 Azure AD 应用程序，以在缩放单元之间实现通信

1. 部署环境后，创建另外一个 Azure AD 应用程序，以在中心和缩放单元之间实现可信通信。

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. 创建应用程序后，您必须创建客户端密码，并将信息保存到 Azure 密钥保管库。 此外，您还必须向创建的 Azure AD 应用程序授予访问权限，以便它可以检索存储在密钥保管库中的密码。 为方便起见，以下脚本将自动执行所有所需的操作。

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > 如果不存在具有指定 **KeyVaultName** 值的密钥保管库，脚本会自动创建一个。

1. 将您刚才创建的 Azure AD 应用程序 ID（使用 Create-SpokeToHubAADApplication.ps1 脚本时）添加到中心的 Azure AD 应用程序表中。 您可以通过 UI 手动完成此步骤。

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>将目标包上载到 LCS 中的 LBD 项目资产中

此步骤准备将转移到 LBD 缩放单元环境的应用程序版本、平台版本和自定义项。

1. 将应用于中心环境的组合的相同应用程序/平台包上载到 LCS 本地项目的资产库中。
1. 获取应用于中心环境的自定义可部署包的副本，并将其上载到 LCS 本地项目的资产库中。

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>使用目标包为 LBD 环境提供服务

此步骤将 LBD 缩放单元环境中的应用程序版本、平台版本和自定义设置与中心保持一致。

1. 使用您在上一步中上载的组合应用程序/平台包为 LBD 环境提供服务。
1. 使用您在上一步中上载的自定义可部署包为 LBD 环境提供服务。

    ![在 LCS 中应用更新。](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "在 LCS 中应用更新")

    ![选择自定义包。](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "选择自定义包")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>将 LBD 边缘缩放单元分配给中心

您将通过缩放单元管理门户配置和管理边缘缩放单元。 有关详细信息，请参阅[使用缩放单元管理器门户管理缩放单元和工作负荷](./cloud-edge-landing-page.md#scale-unit-manager-portal)。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
