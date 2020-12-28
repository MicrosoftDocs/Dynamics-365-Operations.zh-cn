---
title: Finance Insights（预览）的配置
description: 本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664082"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="b120a-103">Finance Insights（预览）的配置</span><span class="sxs-lookup"><span data-stu-id="b120a-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b120a-104">Finance Insights 组合了 Microsoft Dynamics 365 Finance 的功能和 Common Data Service、Azure 和 AI Builder，以便为贵组织提供强大的预测功能。</span><span class="sxs-lookup"><span data-stu-id="b120a-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Common Data Service, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="b120a-105">本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。</span><span class="sxs-lookup"><span data-stu-id="b120a-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="b120a-106">部署 Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b120a-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="b120a-107">按照以下步骤部署环境。</span><span class="sxs-lookup"><span data-stu-id="b120a-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="b120a-108">在 Microsoft Dynamics Lifecycle Services (LCS) 中，创建或更新 Dynamics 365 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="b120a-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="b120a-109">此环境需要应用版本 10.0.11/平台更新 35 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="b120a-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="b120a-110">该环境必须是沙盒中的高可用性 (HA) 环境。</span><span class="sxs-lookup"><span data-stu-id="b120a-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="b120a-111">（这种类型的环境也称为二级环境。）有关详细信息，请参阅[环境规划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="b120a-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="b120a-112">如果您使用的是 Contoso 演示数据，则需要更多示例数据才能使用“客户付款预测”，“现金流预测”和“预算预测”功能。</span><span class="sxs-lookup"><span data-stu-id="b120a-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-common-data-service"></a><span data-ttu-id="b120a-113">配置 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b120a-113">Configure Common Data Service</span></span>

<span data-ttu-id="b120a-114">您可以完成后续的手动配置步骤，也可以使用提供的 Windows PowerShell 脚本来加快配置过程。</span><span class="sxs-lookup"><span data-stu-id="b120a-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="b120a-115">当 PowerShell 脚本运行完毕后，它将为您提供用于配置 Finance Insights 的值。</span><span class="sxs-lookup"><span data-stu-id="b120a-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="b120a-116">在 PC 上打开 PowerShell 以运行脚本。</span><span class="sxs-lookup"><span data-stu-id="b120a-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="b120a-117">您可能需要 PowerShell 版本 5。</span><span class="sxs-lookup"><span data-stu-id="b120a-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="b120a-118">Microsoft Azure CLI“试用”选项可能无效。</span><span class="sxs-lookup"><span data-stu-id="b120a-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="b120a-119">手动配置步骤</span><span class="sxs-lookup"><span data-stu-id="b120a-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="b120a-120">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/)，然后按照以下步骤在同一个 Active Directory 租户中创建一个新的 Common Data Service 环境：</span><span class="sxs-lookup"><span data-stu-id="b120a-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Common Data Service environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="b120a-121">打开 **环境** 页面。</span><span class="sxs-lookup"><span data-stu-id="b120a-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="b120a-122">[![环境页面](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="b120a-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="b120a-123">选择 **新建环境**。</span><span class="sxs-lookup"><span data-stu-id="b120a-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="b120a-124">在 **类型** 字段中，选择 **沙盒**。</span><span class="sxs-lookup"><span data-stu-id="b120a-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="b120a-125">将 **创建数据库** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b120a-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="b120a-126">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="b120a-126">Select **Next**.</span></span>
    6. <span data-ttu-id="b120a-127">选择组织的语言和货币。</span><span class="sxs-lookup"><span data-stu-id="b120a-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="b120a-128">接受其他字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b120a-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="b120a-129">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b120a-129">Select **Save**.</span></span>
    9. <span data-ttu-id="b120a-130">刷新 **环境** 页面。</span><span class="sxs-lookup"><span data-stu-id="b120a-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="b120a-131">等到 **状态** 字段的值更新为 **就绪**。</span><span class="sxs-lookup"><span data-stu-id="b120a-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="b120a-132">记录 Common Data Service 组织 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-132">Make a note of the Common Data Service organization ID.</span></span>
    12. <span data-ttu-id="b120a-133">选择环境，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="b120a-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="b120a-134">选择 **资源 \> 所有旧设置**。</span><span class="sxs-lookup"><span data-stu-id="b120a-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="b120a-135">在顶部导航栏上，选择 **设置**，然后选择 **自定义**。</span><span class="sxs-lookup"><span data-stu-id="b120a-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="b120a-136">选择 **开发人员资源**。</span><span class="sxs-lookup"><span data-stu-id="b120a-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="b120a-137">将 **实例参考信息 ID** 字段设置为您之前记下的 Common Data Service 组织 ID 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-137">Set the **Instance Reference Information ID** field to the Common Data Service organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="b120a-138">在浏览器的地址栏中，记下 Common Data Service 组织的 URL。</span><span class="sxs-lookup"><span data-stu-id="b120a-138">In the browser's address bar, make a note of the URL for the Common Data Service organization.</span></span> <span data-ttu-id="b120a-139">例如，URL 可能是 `https://org42b2b3d3.crm.dynamics.com`。</span><span class="sxs-lookup"><span data-stu-id="b120a-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="b120a-140">如果您打算使用现金流预测或预算预测功能，请按照以下步骤将组织的注释限制更新为至少 50 兆字节 (MB)：</span><span class="sxs-lookup"><span data-stu-id="b120a-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="b120a-141">打开 [Power Apps 门户](https://make.powerapps.com)。</span><span class="sxs-lookup"><span data-stu-id="b120a-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="b120a-142">选择您刚刚创建的环境，然后选择 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="b120a-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="b120a-143">选择 **设置 \> 电子邮件配置**。</span><span class="sxs-lookup"><span data-stu-id="b120a-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="b120a-144">将 **最大文件大小** 字段的值设置为 **51,200**。</span><span class="sxs-lookup"><span data-stu-id="b120a-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="b120a-145">（该值表示为千字节 \[KB\]。）</span><span class="sxs-lookup"><span data-stu-id="b120a-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="b120a-146">选择 **确定** 保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="b120a-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="b120a-147">Windows PowerShell 配置脚本</span><span class="sxs-lookup"><span data-stu-id="b120a-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="b120a-148">配置 Azure 设置</span><span class="sxs-lookup"><span data-stu-id="b120a-148">Configure the Azure setup</span></span>

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="b120a-149">输入 Common Data Service 目录 ID 和用户的 Azure AD 对象 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-149">Enter the Common Data Service directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="b120a-150">输入 Common Data Service 目录 ID：</span><span class="sxs-lookup"><span data-stu-id="b120a-150">Enter the Common Data Service directory ID:</span></span>

    1. <span data-ttu-id="b120a-151">打开 [Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="b120a-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="b120a-152">使用用于创建 Common Data Service 环境的用户 ID 登录。</span><span class="sxs-lookup"><span data-stu-id="b120a-152">Sign in by using the user ID that was used to create the Common Data Service environment.</span></span>
    3. <span data-ttu-id="b120a-153">转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="b120a-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="b120a-154">复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="b120a-155">输入用户的 Azure Active Directory (Azure AD) 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="b120a-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="b120a-156">在 [Azure 门户中](https://portal.azure.com)，转到 **用户**，然后按电子邮件地址搜索用户。</span><span class="sxs-lookup"><span data-stu-id="b120a-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="b120a-157">选择用户的名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-157">Select the user's name.</span></span>
    3. <span data-ttu-id="b120a-158">复制 **对象 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="b120a-159">使用 Azure Cloud Shell 设置 Finance insights Data Lake 资源</span><span class="sxs-lookup"><span data-stu-id="b120a-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="b120a-160">使用 Windows PowerShell 脚本</span><span class="sxs-lookup"><span data-stu-id="b120a-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="b120a-161">已提供了 Windows PowerShell 脚本，因此您可以轻松设置[配置导出到 Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake) 中介绍的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="b120a-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="b120a-162">如果您希望进行手动设置，请跳过此过程，然后继续执行[手动设置](#manual-setup)部分中的过程。</span><span class="sxs-lookup"><span data-stu-id="b120a-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="b120a-163">请按照以下步骤运行 PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="b120a-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="b120a-164">Azure CLI 的“尝试”选项，否则在 PC 上运行脚本可能无效。</span><span class="sxs-lookup"><span data-stu-id="b120a-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="b120a-165">请按照以下步骤使用 Windows PowerShell 脚本配置 Azure。</span><span class="sxs-lookup"><span data-stu-id="b120a-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="b120a-166">您必须有权创建 Azure 资源组、Azure 资源和 Azure AD 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b120a-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="b120a-167">有关所需权限的信息，请参阅[检查 Azure AD 权限](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)。</span><span class="sxs-lookup"><span data-stu-id="b120a-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="b120a-168">在 [Azure 门户](https://portal.azure.com)中，转到目标 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="b120a-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="b120a-169">选择 **搜索** 字段右侧的 **Cloud Shell** 按钮。</span><span class="sxs-lookup"><span data-stu-id="b120a-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="b120a-170">选择 **PowerShell**。</span><span class="sxs-lookup"><span data-stu-id="b120a-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="b120a-171">如果提示您创建存储，请创建。</span><span class="sxs-lookup"><span data-stu-id="b120a-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="b120a-172">然后将 Windows PowerShell 脚本上载到会话。</span><span class="sxs-lookup"><span data-stu-id="b120a-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="b120a-173">执行该脚本。</span><span class="sxs-lookup"><span data-stu-id="b120a-173">Run the script.</span></span>
5. <span data-ttu-id="b120a-174">按照提示运行脚本。</span><span class="sxs-lookup"><span data-stu-id="b120a-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="b120a-175">使用脚本输出中的信息在 LCS 中安装 **导出到 Data Lake** 加载项。</span><span class="sxs-lookup"><span data-stu-id="b120a-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="b120a-176">使用脚本输出中的信息在 Finance 中的 **数据连接** 页面（**系统管理 \> 系统参数 \> 数据连接**）上启用实体存储。</span><span class="sxs-lookup"><span data-stu-id="b120a-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="b120a-177">手动设置</span><span class="sxs-lookup"><span data-stu-id="b120a-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="b120a-178">向 Azure AD 租户添加应用程序</span><span class="sxs-lookup"><span data-stu-id="b120a-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="b120a-179">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="b120a-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="b120a-180">选择 **管理 \> Enterprise 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="b120a-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="b120a-181">通过应用 ID 搜索以下应用程序。</span><span class="sxs-lookup"><span data-stu-id="b120a-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="b120a-182">申请</span><span class="sxs-lookup"><span data-stu-id="b120a-182">Application</span></span>                              | <span data-ttu-id="b120a-183">应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="b120a-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="b120a-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="b120a-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="b120a-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="b120a-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="b120a-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="b120a-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="b120a-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="b120a-188">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="b120a-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="b120a-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="b120a-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="b120a-190">如果找不到上述任何应用程序，请尝试以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b120a-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="b120a-191">在本地计算机上，选择 **开始** 菜单，然后搜索 **powershell**。</span><span class="sxs-lookup"><span data-stu-id="b120a-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="b120a-192">选中并按住（或右键单击）**Windows PowerShell**，然后选择 **以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="b120a-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="b120a-193">运行以下命令以安装 **AzureAD** 模块。</span><span class="sxs-lookup"><span data-stu-id="b120a-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="b120a-194">如果需要 NuGet 提供商才能继续，请选择 **Y** 进行安装。</span><span class="sxs-lookup"><span data-stu-id="b120a-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="b120a-195">如果出现“不受信任的存储库”消息，请选择 **Y** 以继续操作。</span><span class="sxs-lookup"><span data-stu-id="b120a-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="b120a-196">对于必须添加的每个应用程序，运行以下命令以将该应用程序添加到 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="b120a-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="b120a-197">出现提示时，以 Azure AD 管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="b120a-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="b120a-198">创建 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="b120a-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="b120a-199">确保在与 Common Data Service 环境相同的 Azure AD 实例中创建以下资源。</span><span class="sxs-lookup"><span data-stu-id="b120a-199">Make sure that you create the following resources in the same Azure AD instance as the Common Data Service environment.</span></span> <span data-ttu-id="b120a-200">不能使用其他 Azure AD 实例的资源。</span><span class="sxs-lookup"><span data-stu-id="b120a-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="b120a-201">创建新的存储帐户：</span><span class="sxs-lookup"><span data-stu-id="b120a-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="b120a-202">在 [Azure 门户](https://portal.azure.com)中，创建一个存储帐户。</span><span class="sxs-lookup"><span data-stu-id="b120a-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="b120a-203">在 **创建存储帐户** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="b120a-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="b120a-204">**位置** – 选择环境所在的数据中心。</span><span class="sxs-lookup"><span data-stu-id="b120a-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="b120a-205">**性能** – 建议您选择 **标准**。</span><span class="sxs-lookup"><span data-stu-id="b120a-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="b120a-206">**帐户种类** – 必须选择 **StorageV2**。</span><span class="sxs-lookup"><span data-stu-id="b120a-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="b120a-207">在 **高级选项** 对话框中，在 **分层命名空间** 功能下为 **Data Lake 存储 Gen2** 选项选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="b120a-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="b120a-208">如果禁用此功能，则无法使用 Finance and Operations 应用使用 Power BI 数据流之类服务写入的数据。</span><span class="sxs-lookup"><span data-stu-id="b120a-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="b120a-209">选择 **查看并创建**。</span><span class="sxs-lookup"><span data-stu-id="b120a-209">Select **Review and create**.</span></span> <span data-ttu-id="b120a-210">部署完成后，新资源将显示在 Azure 门户中。</span><span class="sxs-lookup"><span data-stu-id="b120a-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="b120a-211">转到您创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="b120a-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="b120a-212">在左侧菜单中，选择 **访问密钥**。</span><span class="sxs-lookup"><span data-stu-id="b120a-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="b120a-213">复制并保存 **Key1** 或 **Key2** 的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="b120a-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="b120a-214">复制并保存存储帐户名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="b120a-215">创建新的密钥保管库：</span><span class="sxs-lookup"><span data-stu-id="b120a-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="b120a-216">在 [Azure 门户](https://portal.azure.com)中，创建一个密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="b120a-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="b120a-217">在 **创建密钥保管库** 对话框的 **位置** 字段中，选择您的环境所在数据中心。</span><span class="sxs-lookup"><span data-stu-id="b120a-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="b120a-218">创建密钥保管库之后，在列表中选择它，然后选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="b120a-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="b120a-219">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="b120a-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="b120a-220">在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="b120a-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="b120a-221">请输入密码的名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-221">Enter a name for the secret.</span></span> <span data-ttu-id="b120a-222">记下该名称，因为稍后将需要提供它。</span><span class="sxs-lookup"><span data-stu-id="b120a-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="b120a-223">在 **值** 字段中，输入您在上一过程中从存储帐户获得的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="b120a-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="b120a-224">选择 **启用**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="b120a-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b120a-225">将创建密码并添加到密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="b120a-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="b120a-226">转到 **密钥保管库概述**，并记下 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="b120a-227">创建并注册 Azure AD 应用程序：</span><span class="sxs-lookup"><span data-stu-id="b120a-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="b120a-228">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**，然后选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="b120a-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="b120a-229">选择 **新应用程序注册**，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="b120a-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="b120a-230">**名称** – 输入应用的名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="b120a-231">**应用程序类型** – 选择 **Web API**。</span><span class="sxs-lookup"><span data-stu-id="b120a-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="b120a-232">**重定向 URI 设置** – 输入您的 Dynamics 365 实例的 URL，例如 `https://yourdynamicsinstance.dynamics.com/auth`。</span><span class="sxs-lookup"><span data-stu-id="b120a-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="b120a-233">转到刚才创建的应用，然后复制并保存其 **应用程序（客户端）ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="b120a-234">之后在设置密钥保管库时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="b120a-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="b120a-235">转到 **API 权限**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="b120a-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="b120a-236">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="b120a-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="b120a-237">选择 **Azure 密钥保管库**。</span><span class="sxs-lookup"><span data-stu-id="b120a-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="b120a-238">选择委派权限后，选择 **用户\_模拟**。</span><span class="sxs-lookup"><span data-stu-id="b120a-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="b120a-239">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="b120a-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="b120a-240">在应用的菜单上，选择 **证书 \& 密码**，然后按照以下步骤创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="b120a-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="b120a-241">选择 **新客户端密码**。</span><span class="sxs-lookup"><span data-stu-id="b120a-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="b120a-242">在 **密钥描述** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="b120a-243">选择持续时间，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="b120a-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="b120a-244">将在 **值** 字段中生成一个密码。</span><span class="sxs-lookup"><span data-stu-id="b120a-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="b120a-245">复制并保存密码值。</span><span class="sxs-lookup"><span data-stu-id="b120a-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="b120a-246">创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="b120a-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="b120a-247">转到您先前创建的密钥保管库，然后选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="b120a-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="b120a-248">为下表中的每个密码名称执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="b120a-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b120a-249">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="b120a-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="b120a-250">在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="b120a-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="b120a-251">通过下表创建密码名称和值。</span><span class="sxs-lookup"><span data-stu-id="b120a-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="b120a-252">选择 **启用**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="b120a-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b120a-253">将创建密码并添加到密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="b120a-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="b120a-254">密钥名称</span><span class="sxs-lookup"><span data-stu-id="b120a-254">Secret name</span></span>                       | <span data-ttu-id="b120a-255">密码值</span><span class="sxs-lookup"><span data-stu-id="b120a-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="b120a-256">应用 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-256">app-id</span></span>                            | <span data-ttu-id="b120a-257">您先前创建的应用程序的应用 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="b120a-258">应用密码</span><span class="sxs-lookup"><span data-stu-id="b120a-258">app-secret</span></span>                        | <span data-ttu-id="b120a-259">您之前保存的客户端密码</span><span class="sxs-lookup"><span data-stu-id="b120a-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="b120a-260">存储帐户名称</span><span class="sxs-lookup"><span data-stu-id="b120a-260">storage-account-name</span></span>              | <span data-ttu-id="b120a-261">您之前创建的存储帐户的名称，例如 **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="b120a-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="b120a-262">存储帐户连接字符串</span><span class="sxs-lookup"><span data-stu-id="b120a-262">storage-account-connection-string</span></span> | <span data-ttu-id="b120a-263">您从 **访问密钥** 页面为存储帐户复制的连接字符串</span><span class="sxs-lookup"><span data-stu-id="b120a-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="b120a-264">为应用程序授予访问密钥保管库的权限：</span><span class="sxs-lookup"><span data-stu-id="b120a-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="b120a-265">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="b120a-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="b120a-266">选择访问策略。</span><span class="sxs-lookup"><span data-stu-id="b120a-266">Select the access policies.</span></span>
    3. <span data-ttu-id="b120a-267">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="b120a-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b120a-268">选择 **添加访问策略** 创建一个访问策略。</span><span class="sxs-lookup"><span data-stu-id="b120a-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="b120a-269">在 **密码权限** 字段中，从下表中选择权限。</span><span class="sxs-lookup"><span data-stu-id="b120a-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="b120a-270">在 **选择主体** 字段，搜索下表中的应用程序显示名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="b120a-271">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="b120a-271">Select **Select**.</span></span>
        5. <span data-ttu-id="b120a-272">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="b120a-272">Select **Add**.</span></span>
        6. <span data-ttu-id="b120a-273">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b120a-273">Select **Save**.</span></span>

        | <span data-ttu-id="b120a-274">申请</span><span class="sxs-lookup"><span data-stu-id="b120a-274">Application</span></span>                                              | <span data-ttu-id="b120a-275">权限</span><span class="sxs-lookup"><span data-stu-id="b120a-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="b120a-276">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="b120a-276">The display name of the new application that you created</span></span> | <span data-ttu-id="b120a-277">获取，列表</span><span class="sxs-lookup"><span data-stu-id="b120a-277">Get, List</span></span>   |
        | <span data-ttu-id="b120a-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="b120a-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="b120a-279">获取，列表</span><span class="sxs-lookup"><span data-stu-id="b120a-279">Get, List</span></span>   |

6. <span data-ttu-id="b120a-280">分配角色以访问存储帐户：</span><span class="sxs-lookup"><span data-stu-id="b120a-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="b120a-281">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="b120a-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="b120a-282">选择 **访问控制 (IAM)**，然后选择 **角色分配**。</span><span class="sxs-lookup"><span data-stu-id="b120a-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="b120a-283">选择 **添加，添加角色分配**。</span><span class="sxs-lookup"><span data-stu-id="b120a-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="b120a-284">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="b120a-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b120a-285">从列表中选择角色。</span><span class="sxs-lookup"><span data-stu-id="b120a-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="b120a-286">让 **将访问权限分配到** 字段保持设置为 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="b120a-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="b120a-287">在 **选择** 字段中，输入下表中的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b120a-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="b120a-288">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b120a-288">Select **Save**.</span></span>

        | <span data-ttu-id="b120a-289">申请</span><span class="sxs-lookup"><span data-stu-id="b120a-289">Application</span></span>                                              | <span data-ttu-id="b120a-290">角色</span><span class="sxs-lookup"><span data-stu-id="b120a-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="b120a-291">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="b120a-291">The display name of the new application that you created</span></span> | <span data-ttu-id="b120a-292">负责人</span><span class="sxs-lookup"><span data-stu-id="b120a-292">Owner</span></span>                       |
        | <span data-ttu-id="b120a-293">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="b120a-293">The display name of the new application that you created</span></span> | <span data-ttu-id="b120a-294">缴纳人</span><span class="sxs-lookup"><span data-stu-id="b120a-294">Contributor</span></span>                 |
        | <span data-ttu-id="b120a-295">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="b120a-295">The display name of the new application that you created</span></span> | <span data-ttu-id="b120a-296">存储帐户参与者</span><span class="sxs-lookup"><span data-stu-id="b120a-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="b120a-297">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="b120a-297">The display name of the new application that you created</span></span> | <span data-ttu-id="b120a-298">存储 Blob 数据负责人</span><span class="sxs-lookup"><span data-stu-id="b120a-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="b120a-299">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="b120a-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="b120a-300">存储 Blob 数据读者</span><span class="sxs-lookup"><span data-stu-id="b120a-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="b120a-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b120a-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message
  Write-Warning $_.Exception.StackTrace
  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}

```
---

## <a name="configure-the-entity-store"></a><span data-ttu-id="b120a-302">配置实体存储</span><span class="sxs-lookup"><span data-stu-id="b120a-302">Configure the entity store</span></span>

<span data-ttu-id="b120a-303">请按照以下步骤在您的 Finance 环境中设置实体存储。</span><span class="sxs-lookup"><span data-stu-id="b120a-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="b120a-304">转到 **系统管理 \> 设置 \> 系统参数 \> 数据连接**。</span><span class="sxs-lookup"><span data-stu-id="b120a-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="b120a-305">将 **启用 Data Lake 集成** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b120a-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="b120a-306">设置以下密钥保管库字段：</span><span class="sxs-lookup"><span data-stu-id="b120a-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="b120a-307">**应用程序（客户端）ID** – 输入您先前创建的应用程序客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="b120a-308">**应用程序密码** – 输入为先前创建的应用程序保存的密码。</span><span class="sxs-lookup"><span data-stu-id="b120a-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="b120a-309">**DNS 名称**–您可以在先前创建的应用程序的应用程序详细信息页面上找到域名系统 (DNS) 名称。</span><span class="sxs-lookup"><span data-stu-id="b120a-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="b120a-310">**密码名称** – 输入 **存储帐户连接字符串**。</span><span class="sxs-lookup"><span data-stu-id="b120a-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="b120a-311">配置数据湖</span><span class="sxs-lookup"><span data-stu-id="b120a-311">Configure the data lake</span></span>

<span data-ttu-id="b120a-312">请按照以下步骤使用 LCS 将 Azure Data Lake 加载项添加到环境中。</span><span class="sxs-lookup"><span data-stu-id="b120a-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="b120a-313">登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="b120a-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="b120a-314">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="b120a-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="b120a-315">选择 **导出到 Data Lake** 加载项。</span><span class="sxs-lookup"><span data-stu-id="b120a-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="b120a-316">输入以下值。</span><span class="sxs-lookup"><span data-stu-id="b120a-316">Enter the following values.</span></span>

    | <span data-ttu-id="b120a-317">值</span><span class="sxs-lookup"><span data-stu-id="b120a-317">Value</span></span>                                                              | <span data-ttu-id="b120a-318">说明</span><span class="sxs-lookup"><span data-stu-id="b120a-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="b120a-319">密钥保管库所在 Azure 订阅的租户 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="b120a-320">存储帐户，应用和密钥保管库所在的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="b120a-321">要找到此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory**，然后复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="b120a-322">提供密钥保管库的 DNS 名称</span><span class="sxs-lookup"><span data-stu-id="b120a-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="b120a-323">密钥保管库的 DNS 名称，例如 `https://customkeyvault.vault.azure.net/`。</span><span class="sxs-lookup"><span data-stu-id="b120a-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="b120a-324">（此值与实体存储中使用的 DNS 名称匹配。）</span><span class="sxs-lookup"><span data-stu-id="b120a-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="b120a-325">提供包含存储帐户名称的密钥</span><span class="sxs-lookup"><span data-stu-id="b120a-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="b120a-326">**存储帐户名称**</span><span class="sxs-lookup"><span data-stu-id="b120a-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="b120a-327">要用于访问 Data Lake 的应用 ID 的密码名称</span><span class="sxs-lookup"><span data-stu-id="b120a-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="b120a-328">**应用 ID**</span><span class="sxs-lookup"><span data-stu-id="b120a-328">**app-id**</span></span> |
    | <span data-ttu-id="b120a-329">与应用 ID 一起使用的密码名称</span><span class="sxs-lookup"><span data-stu-id="b120a-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="b120a-330">**应用密码**</span><span class="sxs-lookup"><span data-stu-id="b120a-330">**app-secret**</span></span> |

5. <span data-ttu-id="b120a-331">同意条款，然后选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="b120a-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="b120a-332">该加载项将在几分钟内安装。</span><span class="sxs-lookup"><span data-stu-id="b120a-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="b120a-333">配置 AI Builder</span><span class="sxs-lookup"><span data-stu-id="b120a-333">Configure AI Builder</span></span>

1. <span data-ttu-id="b120a-334">登录到 LCS，然后打开 **环境详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="b120a-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="b120a-335">滚动到 **环境加载项** 部分。</span><span class="sxs-lookup"><span data-stu-id="b120a-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="b120a-336">您应该看到此环境中已经安装的加载项。</span><span class="sxs-lookup"><span data-stu-id="b120a-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="b120a-337">如果其中不包含 **导出到 Data Lake** 加载项，请配置此加载项。</span><span class="sxs-lookup"><span data-stu-id="b120a-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="b120a-338">选择 **获取见解** 加载项。</span><span class="sxs-lookup"><span data-stu-id="b120a-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="b120a-339">在 **获取见解** 加载项的详细信息页面上，输入以下值。</span><span class="sxs-lookup"><span data-stu-id="b120a-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="b120a-340">值</span><span class="sxs-lookup"><span data-stu-id="b120a-340">Value</span></span>                                                    | <span data-ttu-id="b120a-341">说明</span><span class="sxs-lookup"><span data-stu-id="b120a-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="b120a-342">CDS 组织 URL</span><span class="sxs-lookup"><span data-stu-id="b120a-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="b120a-343">Common Data Service 实例的 Common Data Service 组织 URL。</span><span class="sxs-lookup"><span data-stu-id="b120a-343">The Common Data Service organization URL of the Common Data Service instance.</span></span> <span data-ttu-id="b120a-344">要找到此值，请打开 [Power Apps 门户](https://make.powerapps.com)，选择右上角的 **设置** 按钮（齿轮符号），选择 **高级设置**，然后复制 URL。</span><span class="sxs-lookup"><span data-stu-id="b120a-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="b120a-345">（此 URL 的结尾为“dynamics.com”。）</span><span class="sxs-lookup"><span data-stu-id="b120a-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="b120a-346">CDS 组织 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-346">CDS Org ID</span></span>                                               | <span data-ttu-id="b120a-347">Common Data Service 实例的环境 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-347">The environment ID of the Common Data Service instance.</span></span> <span data-ttu-id="b120a-348">要找到此值，请打开 [Power Apps 门户](https://make.powerapps.com)，选择右上角的 **设置** 按钮（齿轮符号），选择 **自定义 \> 开发人员资源 \> 实例参考信息**，然后复制 **ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="b120a-349">CDS 租户 ID（AAD 的目录 ID）</span><span class="sxs-lookup"><span data-stu-id="b120a-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="b120a-350">Common Data Service 实例的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-350">The tenant ID of the Common Data Service instance.</span></span> <span data-ttu-id="b120a-351">要找到此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory**，然后复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="b120a-352">提供具有系统管理员角色的用户对象 ID</span><span class="sxs-lookup"><span data-stu-id="b120a-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="b120a-353">用户在 Common Data Service 中的 Azure AD 用户对象 ID。</span><span class="sxs-lookup"><span data-stu-id="b120a-353">The Azure AD user object ID of the user in Common Data Service.</span></span> <span data-ttu-id="b120a-354">该用户必须是该 Common Data Service 实例的系统管理员。</span><span class="sxs-lookup"><span data-stu-id="b120a-354">This user must be a system administrator of the Common Data Service instance.</span></span> <span data-ttu-id="b120a-355">要找到此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory \> 用户**，选择用户，然后在 **身份** 部分中，复制 **对象 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="b120a-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="b120a-356">这是租户的默认 CDS 环境吗？</span><span class="sxs-lookup"><span data-stu-id="b120a-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="b120a-357">如果 Common Data Service 实例是创建的第一个生产实例，请选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="b120a-357">If the Common Data Service instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="b120a-358">如果 Common Data Service 实例是手动创建的，请清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="b120a-358">If the Common Data Service instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="b120a-359">反馈和支持</span><span class="sxs-lookup"><span data-stu-id="b120a-359">Feedback and support</span></span>

<span data-ttu-id="b120a-360">如果对提供反馈感兴趣或需要支持，请向 [客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b120a-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b120a-361">隐私声明</span><span class="sxs-lookup"><span data-stu-id="b120a-361">Privacy notice</span></span>

<span data-ttu-id="b120a-362">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="b120a-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
