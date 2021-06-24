---
title: Finance Insights 的配置 - 10.0.19 之前的版本
description: 本主题介绍的配置步骤用于让系统使用 10.0.19 之前的版本的 Finance Insights 中的可用功能。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186412"
---
# <a name="configuration-for-finance-insights-preview"></a>Finance Insights（预览）的配置

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> 以下设置 Finance Insights 的过程对 10.0.19 之前的 Microsoft Dynamics 365 Finance 版本有效。 若要在 10.0.20 版本及更高版本上设置 Finance Insights，请参阅 [Finance Insights（预览）的配置 - 版本 10.0.20 及更高版本](configure-for-fin-insites-PubPrvw.md)。

Finance Insights 组合了 Microsoft Dynamics 365 Finance 的功能和 Microsoft Dataverse、Azure 和 AI Builder，以便为贵组织提供强大的预测功能。 本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。

## <a name="deploy-dynamics-365-finance"></a>部署 Dynamics 365 Finance

按照以下步骤部署环境。

1. 在 Microsoft Dynamics Lifecycle Services (LCS) 中，创建或更新 Dynamics 365 Finance 环境。 此环境需要应用版本 10.0.11/平台更新 35 或更高版本。
2. 该环境必须是沙盒中的高可用性 (HA) 环境。 （这种类型的环境也称为二级环境。）有关详细信息，请参阅[环境规划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。
3. 如果您要在沙盒环境中配置 Finance Insights，可能需要将生产数据复制到该环境以进行工作预测。 预测模型使用多年的数据来生成预测。 Contoso 演示数据包含的历史数据不足以充分定型预测模型。 

## <a name="configure-dataverse"></a>配置 Dataverse

使用以下步骤为 Finance insights 配置 Dataverse。

1. 在 LCS 中打开环境页面，验证是否已设置 **Power Platform 集成** 部分。
    1. 如果已经设置，链接到 Dynamics 365 Finance 环境的 Dataverse 环境名称应该列出。 复制 Dataverse 环境名称。
    2. 如果未设置，请按照下列步骤操作：
        1. 在“Power Platform 集成”部分选择 **设置** 按钮。 设置环境最多可能需要一个小时。
        2. 如果成功设置了 Dataverse 环境，链接到 Dynamics 365 Finance 环境的 Dataverse 环境名称应该列出。 复制 Dataverse 环境名称。
> [!NOTE]
> 完成环境设置后，**不要** 选择 **链接到面向应用程序的 CDS** 按钮。 Finance Insights 不需要此功能，它会禁用在 LCS 中完成所需的环境加载项的功能。

2. 打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/)，然后按照以下步骤在同一个 Active Directory 租户中创建一个新的 Dataverse 环境：

    1. 打开 **环境** 页面。

        [![环境页面](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. 选择上面创建的 Dataverse 环境，然后选择 **设置**。
    3. 选择 **资源 \> 所有旧设置**。
    4. 在顶部导航栏上，选择 **设置**，然后选择 **自定义**。
    5. 选择 **开发人员资源**。
    6. 复制 **Dataverse 组织 ID** 值。
    7. 在浏览器的地址栏中，记下 Dataverse 组织的 URL。 例如，URL 可能是 `https://org42b2b3d3.crm.dynamics.com`。

3. 如果您打算使用现金流预测或预算预测功能，请按照以下步骤将组织的注释限制更新为至少 50 兆字节 (MB)：

    1. 打开 [Power Apps 门户](https://make.powerapps.com)。
    2. 选择您刚刚创建的环境，然后选择 **高级设置**。
    3. 选择 **设置 \> 电子邮件配置**。
    4. 将 **最大文件大小** 字段的值设置为 **51,200**。 （该值表示为千字节 \[KB\]。）
    5. 选择 **确定** 保存您的更改。

## <a name="configure-the-azure-setup"></a>配置 Azure 设置

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>输入 Dataverse 目录 ID 和用户的 Azure AD 对象 ID

1. 输入 Dataverse 目录 ID：

    1. 打开 [Azure 门户](https://portal.azure.com)。
    2. 使用用于创建 Dataverse 环境的用户 ID 登录。
    3. 转到 **Azure Active Directory**。
    4. 复制 **租户 ID** 值。

2. 输入用户的 Azure Active Directory (Azure AD) 对象 ID：

    1. 在 [Azure 门户中](https://portal.azure.com)，转到 **用户**，然后按电子邮件地址搜索用户。
    2. 选择用户的名称。
    3. 复制 **对象 ID** 值。

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>使用 Azure Cloud Shell 设置 Finance insights Data Lake 资源

# <a name="use-a-windows-powershell-script"></a>[使用 Windows PowerShell 脚本](#tab/use-a-powershell-script)

已提供了 Windows PowerShell 脚本，因此您可以轻松设置[配置导出到 Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) 中介绍的 Azure 资源。 如果您希望进行手动设置，请跳过此过程，然后继续执行[手动设置](#manual-setup)部分中的过程。

> [!NOTE]
> 请按照以下步骤运行 PowerShell 脚本。 Azure CLI 的“尝试”选项，否则在 PC 上运行脚本可能无效。

请按照以下步骤使用 Windows PowerShell 脚本配置 Azure。 您必须有权创建 Azure 资源组、Azure 资源和 Azure AD 应用程序。 有关所需权限的信息，请参阅[检查 Azure AD 权限](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)。

1. 在 [Azure 门户](https://portal.azure.com)中，转到目标 Azure 订阅。 选择 **搜索** 字段右侧的 **Cloud Shell** 按钮。
2. 选择 **PowerShell**。
3. 如果提示您创建存储，请创建。
4. 转到 **Azure CLI** 选项卡，选择 **复制**。  
5. 打开记事本，粘贴 PowerShell 脚本。 将文件另存为 ConfigureDataLake.ps1。
6. 使用菜单选项将 Windows PowerShell 脚本上载到会话，以在 Cloud Shell 中上载。
7. 运行脚本 .\ConfigureDataLake.ps1。
8. 按照提示运行脚本。
9. 使用脚本输出中的信息在 LCS 中安装 **导出到 Data Lake** 加载项。
10. 使用脚本输出中的信息在 Finance 中的 **数据连接** 页面（**系统管理 \> 系统参数 \> 数据连接**）上启用实体存储。

### <a name="manual-setup"></a>手动设置

#### <a name="add-applications-to-the-azure-ad-tenant"></a>向 Azure AD 租户添加应用程序

1. 在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**。
2. 选择 **管理 \> Enterprise 应用程序**。
3. 通过应用 ID 搜索以下应用程序。

    | 申请                              | 应用程序 ID                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder Authorization Service         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

如果找不到上述任何应用程序，请尝试以下步骤。

1. 在本地计算机上，选择 **开始** 菜单，然后搜索 **powershell**。
2. 选中并按住（或右键单击）**Windows PowerShell**，然后选择 **以管理员身份运行**。
3. 运行以下命令以安装 **AzureAD** 模块。

    `Install-Module -Name AzureAD`

4. 如果需要 NuGet 提供商才能继续，请选择 **Y** 进行安装。
5. 如果出现“不受信任的存储库”消息，请选择 **Y** 以继续操作。
6. 对于必须添加的每个应用程序，运行以下命令以将该应用程序添加到 Azure AD。 出现提示时，以 Azure AD 管理员身份登录。

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>创建 Azure 资源

> [!NOTE]
> 确保在与 Dataverse 环境相同的 Azure AD 实例中创建以下资源。 不能使用其他 Azure AD 实例的资源。

1. 创建新的存储帐户：

    1. 在 [Azure 门户](https://portal.azure.com)中，创建一个存储帐户。
    2. 在 **创建存储帐户** 对话框中，设置以下字段：

        - **位置** – 选择环境所在的数据中心。
        - **性能** – 建议您选择 **标准**。
        - **帐户种类** – 必须选择 **StorageV2**。

    3. 在 **高级选项** 对话框中，在 **分层命名空间** 功能下为 **Data Lake 存储 Gen2** 选项选择 **启用**。 如果禁用此功能，则无法使用 Finance and Operations 应用使用 Power BI 数据流之类服务写入的数据。
    4. 选择 **查看并创建**。 部署完成后，新资源将显示在 Azure 门户中。
    5. 转到您创建的存储帐户。
    6. 在左侧菜单中，选择 **访问密钥**。
    7. 复制并保存 **Key1** 或 **Key2** 的连接字符串。
    8. 复制并保存存储帐户名称。

2. 创建新的密钥保管库：

    1. 在 [Azure 门户](https://portal.azure.com)中，创建一个密钥保管库。
    2. 在 **创建密钥保管库** 对话框的 **位置** 字段中，选择您的环境所在数据中心。
    3. 创建密钥保管库之后，在列表中选择它，然后选择 **密码**。
    4. 选择 **生成/导入**。
    5. 在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。
    6. 请输入密码的名称。 记下该名称，因为稍后将需要提供它。
    7. 在 **值** 字段中，输入您在上一过程中从存储帐户获得的连接字符串。
    8. 选择 **启用**，然后选择 **创建**。 将创建密码并添加到密钥保管库中。
    9. 转到 **密钥保管库概述**，并记下 DNS 名称。

3. 创建并注册 Azure AD 应用程序：

    1. 在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**，然后选择 **应用注册**。
    2. 选择 **新应用程序注册**，然后设置以下字段：

        - **名称** – 输入应用的名称。
        - **应用程序类型** – 选择 **Web API**。
        - **重定向 URI 设置** – 输入您的 Dynamics 365 实例的 URL，例如 `https://yourdynamicsinstance.dynamics.com/auth`。

    3. 转到刚才创建的应用，然后复制并保存其 **应用程序（客户端）ID** 值。 之后在设置密钥保管库时必须提供此值。
    4. 转到 **API 权限**，然后按照以下步骤操作：

        1. 选择 **添加权限**。
        2. 选择 **Azure 密钥保管库**。
        3. 选择委派权限后，选择 **用户\_模拟**。
        4. 选择 **添加权限**。

    5. 在应用的菜单上，选择 **证书 \& 密码**，然后按照以下步骤创建密钥保管库密码：

        1. 选择 **新客户端密码**。
        2. 在 **密钥描述** 字段中，输入名称。
        3. 选择持续时间，然后选择 **添加**。 将在 **值** 字段中生成一个密码。
        4. 复制并保存密码值。

4. 创建密钥保管库密码：

    1. 转到您先前创建的密钥保管库，然后选择 **密码**。
    2. 为下表中的每个密码名称执行下列步骤：

        1. 选择 **生成/导入**。
        2. 在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。
        3. 通过下表创建密码名称和值。
        4. 选择 **启用**，然后选择 **创建**。 将创建密码并添加到密钥保管库中。

        | 密钥名称                       | 密码值                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | 应用 ID                            | 您先前创建的应用程序的应用 ID                                      |
        | 应用密码                        | 您之前保存的客户端密码                                                    |
        | 存储帐户名称              | 您之前创建的存储帐户的名称，例如 **storageaccount1**       |
        | 存储帐户连接字符串 | 您从 **访问密钥** 页面为存储帐户复制的连接字符串 |

5. 为应用程序授予访问密钥保管库的权限：

    1. 在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的密钥保管库。
    2. 选择访问策略。
    3. 为下表中的每个应用程序执行下列步骤：

        1. 选择 **添加访问策略** 创建一个访问策略。
        2. 在 **密码权限** 字段中，从下表中选择权限。
        3. 在 **选择主体** 字段，搜索下表中的应用程序显示名称。
        4. 选择 **选择**。
        5. 选择 **添加**。
        6. 选择 **保存**。

        | 申请                                              | 权限 |
        |----------------------------------------------------------|-------------|
        | 您创建的新应用程序的显示名称 | 获取，列表   |
        | **Microsoft Dynamics ERP Microservices**                 | 获取，列表   |

6. 分配角色以访问存储帐户：

    1. 在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的存储帐户。
    2. 选择 **访问控制 (IAM)**，然后选择 **角色分配**。
    3. 选择 **添加，添加角色分配**。
    4. 为下表中的每个应用程序执行下列步骤：

        1. 从列表中选择角色。
        2. 让 **将访问权限分配到** 字段保持设置为 **Azure AD 用户、组或服务主体**。
        3. 在 **选择** 字段中，输入下表中的应用程序。
        4. 选择 **保存**。

        | 申请                                              | 角色                        |
        |----------------------------------------------------------|-----------------------------|
        | 您创建的新应用程序的显示名称 | 负责人                       |
        | 您创建的新应用程序的显示名称 | 缴纳人                 |
        | 您创建的新应用程序的显示名称 | 存储帐户参与者 |
        | 您创建的新应用程序的显示名称 | 存储 Blob 数据负责人     |
        | **AI Builder Authorization Service**                     | 存储 Blob 数据读者    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a>配置数据湖

请按照以下步骤使用 LCS 将 Azure Data Lake 加载项添加到环境中。

1. 登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。
2. 在 **环境加载项** 部分中，选择 **安装新加载项**。
3. 选择 **导出到 Data Lake** 加载项。
4. 输入以下值。

    | 值                                                              | 说明 |
    |--------------------------------------------------------------------|-------------|
    | 密钥保管库所在 Azure 订阅的租户 ID | 存储帐户，应用和密钥保管库所在的租户 ID。 要找到此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory**，然后复制 **租户 ID** 值。 |
    | 提供密钥保管库的 DNS 名称                             | 密钥保管库的 DNS 名称，例如 `https://customkeyvault.vault.azure.net/`。 （此值与实体存储中使用的 DNS 名称匹配。） |
    | 提供包含存储帐户名称的密钥   | **存储帐户名称** |
    | 要用于访问 Data Lake 的应用 ID 的密码名称          | **应用 ID** |
    | 与应用 ID 一起使用的密码名称                                 | **应用密码** |

5. 同意条款，然后选择 **安装**。

该加载项将在几分钟内安装。

## <a name="configure-ai-builder"></a>配置 AI Builder

1. 登录到 LCS，然后打开 **环境详细信息** 页面。
2. 滚动到 **环境加载项** 部分。 您应该看到此环境中已经安装的加载项。 如果其中不包含 **导出到 Data Lake** 加载项，请配置此加载项。
3. 选择 **获取见解** 加载项。
4. 在 **获取见解** 加载项的详细信息页面上，输入以下值。

    | 值                                                    | 说明 |
    |----------------------------------------------------------|-------------|
    | CDS 组织 URL                                     | 从上面复制的 Dataverse 组织 URL。 |
    | CDS 组织 ID                                               | 从上面复制的 Dataverse 组织 ID。 |
5. 启用 **是租户的默认环境**。
    
## <a name="configure-the-entity-store"></a>配置实体存储

请按照以下步骤在您的 Finance 环境中设置实体存储。

1. 转到 **系统管理 \> 设置 \> 系统参数 \> 数据连接**。
2. 设置以下密钥保管库字段：

    - **应用程序（客户端）ID** – 输入您先前创建的应用程序客户端 ID。
    - **应用程序密码** – 输入为先前创建的应用程序保存的密码。
    - **DNS 名称**–您可以在先前创建的应用程序的应用程序详细信息页面上找到域名系统 (DNS) 名称。
    - **密码名称** – 输入 **存储帐户连接字符串**。
3. 启用 **启用 Data Lake 集成**。
4. 选择 **测试 Azure 密钥保管库**，验证没有错误。
5. 选择 **测试 Azure 存储**，验证没有错误。

## <a name="feedback-and-support"></a>反馈和支持

如果对提供反馈感兴趣或需要支持，请向 [客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。

## <a name="privacy-notice"></a>隐私声明

预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
