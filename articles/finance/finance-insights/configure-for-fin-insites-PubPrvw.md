---
title: 公开预览版（预览）的 Finance insights 的配置 - 版本 10.0.20 及更高版本
description: 本主题介绍如何配置系统以使用版本 10.0.20 及更高版本中公开预览版的 Finance Insights 中的可用功能。
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222604"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="f200e-103">公开预览版（预览）的 Finance insights 的配置 - 版本 10.0.20 及更高版本</span><span class="sxs-lookup"><span data-stu-id="f200e-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f200e-104">Finance Insights 组合了 Microsoft Dynamics 365 Finance 的功能和 Dataverse、Azure 和 AI Builder，以便为贵组织提供强大的预测功能。</span><span class="sxs-lookup"><span data-stu-id="f200e-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="f200e-105">本主题介绍如何配置 Dynamics 365 Finance 版本 10.0.20，以便系统可以使用 Finance insights 公开预览版中的可用功能。</span><span class="sxs-lookup"><span data-stu-id="f200e-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="f200e-106">本主题中描述的配置步骤仅适用于 Finance 版本 10.0.20 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="f200e-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="f200e-107">“若要在版本 10.0.19 及更早版本上设置 Finance Insights，请参阅 [Finance Insights 的配置 - 10.0.18 之前的版本](configure-for-fin-insites.md)。</span><span class="sxs-lookup"><span data-stu-id="f200e-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="f200e-108">部署 Finance</span><span class="sxs-lookup"><span data-stu-id="f200e-108">Deploy Finance</span></span>

<span data-ttu-id="f200e-109">按照以下步骤部署环境。</span><span class="sxs-lookup"><span data-stu-id="f200e-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="f200e-110">在 Microsoft Dynamics Lifecycle Services (LCS) 中，创建或更新 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="f200e-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="f200e-111">此环境需要 Finance and Operations 应用的应用版本 10.0.20 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="f200e-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="f200e-112">该环境必须是沙盒中的高可用性 (HA) 环境。</span><span class="sxs-lookup"><span data-stu-id="f200e-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="f200e-113">（这种类型的环境也称为二级环境。）有关详细信息，请参阅[环境规划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="f200e-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="f200e-114">如果您要在沙盒环境中配置 Finance Insights，可能需要将生产数据复制到该环境以进行工作预测。</span><span class="sxs-lookup"><span data-stu-id="f200e-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="f200e-115">预测模型使用多年的数据来生成预测。</span><span class="sxs-lookup"><span data-stu-id="f200e-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="f200e-116">Contoso 演示数据包含的历史数据不足以充分定型预测模型。</span><span class="sxs-lookup"><span data-stu-id="f200e-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="f200e-117">配置 Dataverse</span><span class="sxs-lookup"><span data-stu-id="f200e-117">Configure Dataverse</span></span>

<span data-ttu-id="f200e-118">按照以下步骤为 Finance Insights 配置 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="f200e-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="f200e-119">在 LCS 中，打开环境页面，验证是否已设置 **Power Platform 集成** 部分。</span><span class="sxs-lookup"><span data-stu-id="f200e-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="f200e-120">如果已经设置，链接到 Finance 环境的 Dataverse 环境名称应该列出。</span><span class="sxs-lookup"><span data-stu-id="f200e-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="f200e-121">如果尚未设置，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="f200e-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="f200e-122">在 **Power Platform 集成** 部分中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="f200e-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="f200e-123">环境设置最多可能需要一个小时。</span><span class="sxs-lookup"><span data-stu-id="f200e-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="f200e-124">如果成功设置了 Dataverse 环境，链接到 Finance 环境的 Dataverse 环境名称应该列出。</span><span class="sxs-lookup"><span data-stu-id="f200e-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f200e-125">完成环境设置后，**不要** 选择 **面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="f200e-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="f200e-126">Finance insights 不需要此按钮。</span><span class="sxs-lookup"><span data-stu-id="f200e-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="f200e-127">如果选择它，您将无法在 LCS 中配置所需的环境加载项。</span><span class="sxs-lookup"><span data-stu-id="f200e-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="f200e-128">配置 Azure</span><span class="sxs-lookup"><span data-stu-id="f200e-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="f200e-129">使用 Azure Cloud Shell 设置 Finance insights Data Lake 资源</span><span class="sxs-lookup"><span data-stu-id="f200e-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="f200e-130">使用 Windows PowerShell 脚本</span><span class="sxs-lookup"><span data-stu-id="f200e-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="f200e-131">已提供了 Windows PowerShell 脚本，因此您可以轻松设置[配置导出到 Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) 中介绍的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="f200e-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="f200e-132">如果您希望手动进行设置，请跳过此过程，然后改为完成[手动设置](#manual-setup)部分中的过程。</span><span class="sxs-lookup"><span data-stu-id="f200e-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="f200e-133">使用以下过程运行 Windows PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="f200e-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="f200e-134">如果您在 Azure CLI 中使用 **试用** 选项，或者如果您在计算机上运行脚本，设置可能不工作。</span><span class="sxs-lookup"><span data-stu-id="f200e-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="f200e-135">请按照以下步骤使用 Windows PowerShell 脚本来配置 Azure。</span><span class="sxs-lookup"><span data-stu-id="f200e-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="f200e-136">您必须有权创建 Azure 资源组、Azure 资源和 Azure AD 应用程序。</span><span class="sxs-lookup"><span data-stu-id="f200e-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="f200e-137">有关所需权限的信息，请参阅[检查 Azure AD 权限](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)。</span><span class="sxs-lookup"><span data-stu-id="f200e-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="f200e-138">在 [Azure 门户](https://portal.azure.com)中，转到目标 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="f200e-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="f200e-139">选择 **搜索** 字段右侧的 **Cloud Shell**。</span><span class="sxs-lookup"><span data-stu-id="f200e-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="f200e-140">选择 **PowerShell**。</span><span class="sxs-lookup"><span data-stu-id="f200e-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="f200e-141">如果系统提示您创建存储，请创建。</span><span class="sxs-lookup"><span data-stu-id="f200e-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="f200e-142">在 **Azure CLI** 选项卡上，选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="f200e-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="f200e-143">在记事本中，打开一个新文件，然后在 Windows PowerShell 脚本中进行粘贴。</span><span class="sxs-lookup"><span data-stu-id="f200e-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="f200e-144">将文件另存为 **ConfigureDataLake.ps1**。</span><span class="sxs-lookup"><span data-stu-id="f200e-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="f200e-145">使用菜单选项将 Windows PowerShell 脚本上传到会话，以在 Cloud Shell 中上传。</span><span class="sxs-lookup"><span data-stu-id="f200e-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="f200e-146">运行 **.\ConfigureDataLake.ps1** 脚本。</span><span class="sxs-lookup"><span data-stu-id="f200e-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="f200e-147">按照提示运行脚本。</span><span class="sxs-lookup"><span data-stu-id="f200e-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="f200e-148">使用脚本输出中的信息在 LCS 中安装导出到 Data Lake 加载项。</span><span class="sxs-lookup"><span data-stu-id="f200e-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="f200e-149">手动设置</span><span class="sxs-lookup"><span data-stu-id="f200e-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="f200e-150">向 Azure AD 租户添加应用程序</span><span class="sxs-lookup"><span data-stu-id="f200e-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="f200e-151">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="f200e-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="f200e-152">选择 **管理 \> Enterprise 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="f200e-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="f200e-153">通过应用 ID 搜索以下应用程序。</span><span class="sxs-lookup"><span data-stu-id="f200e-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="f200e-154">申请</span><span class="sxs-lookup"><span data-stu-id="f200e-154">Application</span></span>                              | <span data-ttu-id="f200e-155">应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="f200e-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f200e-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="f200e-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="f200e-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f200e-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="f200e-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="f200e-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="f200e-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="f200e-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="f200e-160">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="f200e-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="f200e-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="f200e-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="f200e-162">如果找不到上述任何应用程序，请尝试以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f200e-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="f200e-163">在本地计算机上，在 **开始** 菜单上，搜索 **powershell**。</span><span class="sxs-lookup"><span data-stu-id="f200e-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="f200e-164">选中并按住（或右键单击）**Windows PowerShell**，然后选择 **以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="f200e-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="f200e-165">运行以下命令以安装 **AzureAD** 模块。</span><span class="sxs-lookup"><span data-stu-id="f200e-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="f200e-166">如果需要 NuGet 提供商才能继续，请选择 **Y** 进行安装。</span><span class="sxs-lookup"><span data-stu-id="f200e-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="f200e-167">如果您收到“不受信任的存储库”消息，请选择 **Y** 以继续。</span><span class="sxs-lookup"><span data-stu-id="f200e-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="f200e-168">对于必须添加的每个应用程序，运行以下命令以将该应用程序添加到 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="f200e-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="f200e-169">出现提示时，以 Azure AD 管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="f200e-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="f200e-170">创建 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="f200e-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="f200e-171">确保在与 Dataverse 环境所在的相同 Azure AD 实例中创建以下资源。</span><span class="sxs-lookup"><span data-stu-id="f200e-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="f200e-172">不能使用其他 Azure AD 实例的资源。</span><span class="sxs-lookup"><span data-stu-id="f200e-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="f200e-173">创建存储帐户：</span><span class="sxs-lookup"><span data-stu-id="f200e-173">Create a storage account:</span></span>

    1. <span data-ttu-id="f200e-174">在 [Azure 门户](https://portal.azure.com)中，创建一个存储帐户。</span><span class="sxs-lookup"><span data-stu-id="f200e-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="f200e-175">在 **创建存储帐户** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f200e-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="f200e-176">**位置** – 选择环境所在的数据中心。</span><span class="sxs-lookup"><span data-stu-id="f200e-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="f200e-177">**性能** – 建议您选择 **标准**。</span><span class="sxs-lookup"><span data-stu-id="f200e-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="f200e-178">**帐户种类** – 必须选择 **StorageV2**。</span><span class="sxs-lookup"><span data-stu-id="f200e-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="f200e-179">在 **高级选项** 对话框中，在 **分层命名空间** 功能下为 **Data Lake 存储 Gen2** 选项选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="f200e-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="f200e-180">如果不启用此功能，则无法使用 Finance and Operations 应用通过诸如 Power BI 数据流的服务写入的数据。</span><span class="sxs-lookup"><span data-stu-id="f200e-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="f200e-181">选择 **查看并创建**。</span><span class="sxs-lookup"><span data-stu-id="f200e-181">Select **Review and create**.</span></span> <span data-ttu-id="f200e-182">部署完成后，新资源将显示在 Azure 门户中。</span><span class="sxs-lookup"><span data-stu-id="f200e-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="f200e-183">转到您创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="f200e-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="f200e-184">在左侧菜单中，选择 **访问密钥**。</span><span class="sxs-lookup"><span data-stu-id="f200e-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="f200e-185">复制并保存存储帐户的名称。</span><span class="sxs-lookup"><span data-stu-id="f200e-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="f200e-186">之后在设置密钥保管库密码时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="f200e-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="f200e-187">创建密钥保管库：</span><span class="sxs-lookup"><span data-stu-id="f200e-187">Create a key vault:</span></span>

    1. <span data-ttu-id="f200e-188">在 [Azure 门户](https://portal.azure.com)中，创建一个密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="f200e-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="f200e-189">在 **创建密钥保管库** 对话框的 **位置** 字段中，选择您的环境所在数据中心。</span><span class="sxs-lookup"><span data-stu-id="f200e-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="f200e-190">创建密钥保管库后，转到 **密钥保管库概述**，然后复制并保存 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="f200e-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="f200e-191">之后在 Data Lake 加载项时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="f200e-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="f200e-192">创建并注册 Azure AD 应用程序：</span><span class="sxs-lookup"><span data-stu-id="f200e-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="f200e-193">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**，然后选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="f200e-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="f200e-194">选择 **新应用程序注册**，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f200e-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="f200e-195">**名称** – 输入应用的名称。</span><span class="sxs-lookup"><span data-stu-id="f200e-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="f200e-196">**应用程序类型** – 选择 **Web API**。</span><span class="sxs-lookup"><span data-stu-id="f200e-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="f200e-197">**重定向 URI 设置** – 输入您的 Dynamics 365 实例的 URL，例如 `https://yourdynamicsinstance.dynamics.com/auth`。</span><span class="sxs-lookup"><span data-stu-id="f200e-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="f200e-198">转到刚才创建的应用，然后复制并保存其 **应用程序（客户端）ID** 值。</span><span class="sxs-lookup"><span data-stu-id="f200e-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="f200e-199">之后在设置密钥保管库密码时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="f200e-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="f200e-200">转到 **API 权限**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="f200e-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="f200e-201">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="f200e-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="f200e-202">选择 **Azure 密钥保管库**。</span><span class="sxs-lookup"><span data-stu-id="f200e-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="f200e-203">选择委派权限后，选择 **用户\_模拟**。</span><span class="sxs-lookup"><span data-stu-id="f200e-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="f200e-204">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="f200e-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="f200e-205">在应用的菜单上，选择 **证书 \& 密码**，然后按照以下步骤创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="f200e-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="f200e-206">选择 **新客户端密码**。</span><span class="sxs-lookup"><span data-stu-id="f200e-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="f200e-207">在 **密钥描述** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="f200e-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="f200e-208">选择持续时间，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f200e-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="f200e-209">将在 **值** 字段中生成一个密码。</span><span class="sxs-lookup"><span data-stu-id="f200e-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="f200e-210">复制并保存客户端密码值。</span><span class="sxs-lookup"><span data-stu-id="f200e-210">Copy and save the client secret value.</span></span> <span data-ttu-id="f200e-211">之后在设置密钥保管库密码时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="f200e-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="f200e-212">创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="f200e-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="f200e-213">转到您先前创建的密钥保管库，然后选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="f200e-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="f200e-214">为下表中的每个密码名称执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="f200e-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f200e-215">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="f200e-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="f200e-216">在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="f200e-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="f200e-217">从表中创建密码名称和值。</span><span class="sxs-lookup"><span data-stu-id="f200e-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="f200e-218">选择 **启用**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="f200e-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f200e-219">将创建密码并添加到密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="f200e-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="f200e-220">密钥名称</span><span class="sxs-lookup"><span data-stu-id="f200e-220">Secret name</span></span>                       | <span data-ttu-id="f200e-221">密码值</span><span class="sxs-lookup"><span data-stu-id="f200e-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="f200e-222">应用 ID</span><span class="sxs-lookup"><span data-stu-id="f200e-222">app-id</span></span>                            | <span data-ttu-id="f200e-223">您先前创建的应用程序的应用 ID。</span><span class="sxs-lookup"><span data-stu-id="f200e-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="f200e-224">应用密码</span><span class="sxs-lookup"><span data-stu-id="f200e-224">app-secret</span></span>                        | <span data-ttu-id="f200e-225">您之前保存的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="f200e-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="f200e-226">存储帐户名称</span><span class="sxs-lookup"><span data-stu-id="f200e-226">storage-account-name</span></span>              | <span data-ttu-id="f200e-227">您之前创建的存储帐户的名称，例如 **storageaccount1**。</span><span class="sxs-lookup"><span data-stu-id="f200e-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="f200e-228">为应用程序授予访问密钥保管库的权限：</span><span class="sxs-lookup"><span data-stu-id="f200e-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="f200e-229">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="f200e-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="f200e-230">选择访问策略。</span><span class="sxs-lookup"><span data-stu-id="f200e-230">Select the access policies.</span></span>
    3. <span data-ttu-id="f200e-231">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="f200e-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f200e-232">选择 **添加访问策略** 创建一个访问策略。</span><span class="sxs-lookup"><span data-stu-id="f200e-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="f200e-233">在 **密码权限** 字段中，从表中选择权限。</span><span class="sxs-lookup"><span data-stu-id="f200e-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="f200e-234">在 **选择主体** 字段中，从表中搜索应用程序显示名称。</span><span class="sxs-lookup"><span data-stu-id="f200e-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="f200e-235">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="f200e-235">Select **Select**.</span></span>
        5. <span data-ttu-id="f200e-236">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f200e-236">Select **Add**.</span></span>
        6. <span data-ttu-id="f200e-237">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f200e-237">Select **Save**.</span></span>

        | <span data-ttu-id="f200e-238">申请</span><span class="sxs-lookup"><span data-stu-id="f200e-238">Application</span></span>                                              | <span data-ttu-id="f200e-239">权限</span><span class="sxs-lookup"><span data-stu-id="f200e-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="f200e-240">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="f200e-240">The display name of the new application that you created</span></span> | <span data-ttu-id="f200e-241">获取，列表</span><span class="sxs-lookup"><span data-stu-id="f200e-241">Get, List</span></span>   |
        | <span data-ttu-id="f200e-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="f200e-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="f200e-243">获取，列表</span><span class="sxs-lookup"><span data-stu-id="f200e-243">Get, List</span></span>   |

6. <span data-ttu-id="f200e-244">分配角色以访问存储帐户：</span><span class="sxs-lookup"><span data-stu-id="f200e-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="f200e-245">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="f200e-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="f200e-246">选择 **访问控制 (IAM)**，然后选择 **角色分配**。</span><span class="sxs-lookup"><span data-stu-id="f200e-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="f200e-247">选择 **添加，添加角色分配**。</span><span class="sxs-lookup"><span data-stu-id="f200e-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="f200e-248">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="f200e-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f200e-249">从表中选择角色。</span><span class="sxs-lookup"><span data-stu-id="f200e-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="f200e-250">让 **将访问权限分配到** 字段保持设置为 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="f200e-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="f200e-251">在 **选择** 字段中，从表中输入应用程序。</span><span class="sxs-lookup"><span data-stu-id="f200e-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="f200e-252">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f200e-252">Select **Save**.</span></span>

        | <span data-ttu-id="f200e-253">申请</span><span class="sxs-lookup"><span data-stu-id="f200e-253">Application</span></span>                                              | <span data-ttu-id="f200e-254">角色</span><span class="sxs-lookup"><span data-stu-id="f200e-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="f200e-255">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="f200e-255">The display name of the new application that you created</span></span> | <span data-ttu-id="f200e-256">负责人</span><span class="sxs-lookup"><span data-stu-id="f200e-256">Owner</span></span>                       |
        | <span data-ttu-id="f200e-257">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="f200e-257">The display name of the new application that you created</span></span> | <span data-ttu-id="f200e-258">缴纳人</span><span class="sxs-lookup"><span data-stu-id="f200e-258">Contributor</span></span>                 |
        | <span data-ttu-id="f200e-259">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="f200e-259">The display name of the new application that you created</span></span> | <span data-ttu-id="f200e-260">存储帐户参与者</span><span class="sxs-lookup"><span data-stu-id="f200e-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="f200e-261">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="f200e-261">The display name of the new application that you created</span></span> | <span data-ttu-id="f200e-262">存储 Blob 数据负责人</span><span class="sxs-lookup"><span data-stu-id="f200e-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="f200e-263">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="f200e-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="f200e-264">存储 Blob 数据读者</span><span class="sxs-lookup"><span data-stu-id="f200e-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="f200e-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f200e-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="f200e-266">配置“导出到 Data Lake”加载项</span><span class="sxs-lookup"><span data-stu-id="f200e-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="f200e-267">请按照以下步骤使用 LCS 将“导出到 Data Lake”加载项添加到环境。</span><span class="sxs-lookup"><span data-stu-id="f200e-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="f200e-268">登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="f200e-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f200e-269">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="f200e-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f200e-270">选择 **导出到 Data Lake** 加载项。</span><span class="sxs-lookup"><span data-stu-id="f200e-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="f200e-271">输入以下值。</span><span class="sxs-lookup"><span data-stu-id="f200e-271">Enter the following values.</span></span>

    | <span data-ttu-id="f200e-272">值</span><span class="sxs-lookup"><span data-stu-id="f200e-272">Value</span></span>                                                              | <span data-ttu-id="f200e-273">说明</span><span class="sxs-lookup"><span data-stu-id="f200e-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="f200e-274">密钥保管库所在 Azure 订阅的租户 ID</span><span class="sxs-lookup"><span data-stu-id="f200e-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="f200e-275">存储帐户，应用和密钥保管库所在的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="f200e-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="f200e-276">若要获取此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory**，然后复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="f200e-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f200e-277">提供密钥保管库的 DNS 名称</span><span class="sxs-lookup"><span data-stu-id="f200e-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="f200e-278">密钥保管库的 DNS 名称，例如 `https://customkeyvault.vault.azure.net/`。</span><span class="sxs-lookup"><span data-stu-id="f200e-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="f200e-279">提供包含存储帐户名称的密钥</span><span class="sxs-lookup"><span data-stu-id="f200e-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="f200e-280">**存储帐户名称**</span><span class="sxs-lookup"><span data-stu-id="f200e-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="f200e-281">要用于访问 Data Lake 的应用 ID 的密码名称</span><span class="sxs-lookup"><span data-stu-id="f200e-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="f200e-282">**应用 ID**</span><span class="sxs-lookup"><span data-stu-id="f200e-282">**app-id**</span></span> |
    | <span data-ttu-id="f200e-283">应用客户端密码的密码名称</span><span class="sxs-lookup"><span data-stu-id="f200e-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="f200e-284">**应用密码**</span><span class="sxs-lookup"><span data-stu-id="f200e-284">**app-secret**</span></span> |

5. <span data-ttu-id="f200e-285">同意条款，然后选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="f200e-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="f200e-286">该加载项将在几分钟内安装。</span><span class="sxs-lookup"><span data-stu-id="f200e-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="f200e-287">配置 Finance Insights 加载项</span><span class="sxs-lookup"><span data-stu-id="f200e-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="f200e-288">如果之前安装了“获取见解”加载项，请先卸载，然后再完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="f200e-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="f200e-289">按照以下步骤安装 Finance Insights 加载项。</span><span class="sxs-lookup"><span data-stu-id="f200e-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="f200e-290">登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="f200e-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f200e-291">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="f200e-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f200e-292">选择 **Finance Insights** 加载项。</span><span class="sxs-lookup"><span data-stu-id="f200e-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="f200e-293">同意条款，然后选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="f200e-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="f200e-294">反馈和支持</span><span class="sxs-lookup"><span data-stu-id="f200e-294">Feedback and support</span></span>

<span data-ttu-id="f200e-295">如果您对提供反馈感兴趣，或者如果您需要支持，请向 [Finance Insights（预览）](mailto:fiap@microsoft.com)发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f200e-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
