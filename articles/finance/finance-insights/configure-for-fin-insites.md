---
title: Finance Insights（预览）的配置
description: 本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941218"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="991a2-103">Finance Insights（预览）的配置</span><span class="sxs-lookup"><span data-stu-id="991a2-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="991a2-104">Finance Insights 组合了 Microsoft Dynamics 365 Finance 的功能和 Microsoft Dataverse、Azure 和 AI Builder，以便为贵组织提供强大的预测功能。</span><span class="sxs-lookup"><span data-stu-id="991a2-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="991a2-105">本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。</span><span class="sxs-lookup"><span data-stu-id="991a2-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="991a2-106">部署 Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="991a2-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="991a2-107">按照以下步骤部署环境。</span><span class="sxs-lookup"><span data-stu-id="991a2-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="991a2-108">在 Microsoft Dynamics Lifecycle Services (LCS) 中，创建或更新 Dynamics 365 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="991a2-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="991a2-109">此环境需要应用版本 10.0.11/平台更新 35 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="991a2-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="991a2-110">该环境必须是沙盒中的高可用性 (HA) 环境。</span><span class="sxs-lookup"><span data-stu-id="991a2-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="991a2-111">（这种类型的环境也称为二级环境。）有关详细信息，请参阅[环境规划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="991a2-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="991a2-112">如果您使用的是 Contoso 演示数据，则需要更多示例数据才能使用“客户付款预测”，“现金流预测”和“预算预测”功能。</span><span class="sxs-lookup"><span data-stu-id="991a2-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="991a2-113">配置 Dataverse</span><span class="sxs-lookup"><span data-stu-id="991a2-113">Configure Dataverse</span></span>

<span data-ttu-id="991a2-114">使用以下步骤为 Finance insights 配置 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="991a2-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="991a2-115">在 LCS 中打开环境页面，验证是否已设置 **Power Platform 集成** 部分。</span><span class="sxs-lookup"><span data-stu-id="991a2-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="991a2-116">如果已经设置，链接到 Dynamics 365 Finance 环境的 Dataverse 环境名称应该列出。</span><span class="sxs-lookup"><span data-stu-id="991a2-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="991a2-117">复制 Dataverse 环境名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="991a2-118">如果未设置，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="991a2-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="991a2-119">在“Power Platform 集成”部分选择 **设置** 按钮。</span><span class="sxs-lookup"><span data-stu-id="991a2-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="991a2-120">设置环境最多可能需要一个小时。</span><span class="sxs-lookup"><span data-stu-id="991a2-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="991a2-121">如果成功设置了 Dataverse 环境，链接到 Dynamics 365 Finance 环境的 Dataverse 环境名称应该列出。</span><span class="sxs-lookup"><span data-stu-id="991a2-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="991a2-122">复制 Dataverse 环境名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="991a2-123">完成环境设置后，**不要** 选择 **链接到面向应用程序的 CDS** 按钮。</span><span class="sxs-lookup"><span data-stu-id="991a2-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="991a2-124">Finance Insights 不需要此功能，它会禁用在 LCS 中完成所需的环境加载项的功能。</span><span class="sxs-lookup"><span data-stu-id="991a2-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="991a2-125">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/)，然后按照以下步骤在同一个 Active Directory 租户中创建一个新的 Dataverse 环境：</span><span class="sxs-lookup"><span data-stu-id="991a2-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="991a2-126">打开 **环境** 页面。</span><span class="sxs-lookup"><span data-stu-id="991a2-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="991a2-127">[![环境页面](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="991a2-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="991a2-128">选择上面创建的 Dataverse 环境，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="991a2-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="991a2-129">选择 **资源 \> 所有旧设置**。</span><span class="sxs-lookup"><span data-stu-id="991a2-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="991a2-130">在顶部导航栏上，选择 **设置**，然后选择 **自定义**。</span><span class="sxs-lookup"><span data-stu-id="991a2-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="991a2-131">选择 **开发人员资源**。</span><span class="sxs-lookup"><span data-stu-id="991a2-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="991a2-132">复制 **Dataverse 组织 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="991a2-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="991a2-133">在浏览器的地址栏中，记下 Dataverse 组织的 URL。</span><span class="sxs-lookup"><span data-stu-id="991a2-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="991a2-134">例如，URL 可能是 `https://org42b2b3d3.crm.dynamics.com`。</span><span class="sxs-lookup"><span data-stu-id="991a2-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="991a2-135">如果您打算使用现金流预测或预算预测功能，请按照以下步骤将组织的注释限制更新为至少 50 兆字节 (MB)：</span><span class="sxs-lookup"><span data-stu-id="991a2-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="991a2-136">打开 [Power Apps 门户](https://make.powerapps.com)。</span><span class="sxs-lookup"><span data-stu-id="991a2-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="991a2-137">选择您刚刚创建的环境，然后选择 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="991a2-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="991a2-138">选择 **设置 \> 电子邮件配置**。</span><span class="sxs-lookup"><span data-stu-id="991a2-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="991a2-139">将 **最大文件大小** 字段的值设置为 **51,200**。</span><span class="sxs-lookup"><span data-stu-id="991a2-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="991a2-140">（该值表示为千字节 \[KB\]。）</span><span class="sxs-lookup"><span data-stu-id="991a2-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="991a2-141">选择 **确定** 保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="991a2-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="991a2-142">配置 Azure 设置</span><span class="sxs-lookup"><span data-stu-id="991a2-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="991a2-143">输入 Dataverse 目录 ID 和用户的 Azure AD 对象 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="991a2-144">输入 Dataverse 目录 ID：</span><span class="sxs-lookup"><span data-stu-id="991a2-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="991a2-145">打开 [Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="991a2-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="991a2-146">使用用于创建 Dataverse 环境的用户 ID 登录。</span><span class="sxs-lookup"><span data-stu-id="991a2-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="991a2-147">转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="991a2-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="991a2-148">复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="991a2-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="991a2-149">输入用户的 Azure Active Directory (Azure AD) 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="991a2-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="991a2-150">在 [Azure 门户中](https://portal.azure.com)，转到 **用户**，然后按电子邮件地址搜索用户。</span><span class="sxs-lookup"><span data-stu-id="991a2-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="991a2-151">选择用户的名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-151">Select the user's name.</span></span>
    3. <span data-ttu-id="991a2-152">复制 **对象 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="991a2-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="991a2-153">使用 Azure Cloud Shell 设置 Finance insights Data Lake 资源</span><span class="sxs-lookup"><span data-stu-id="991a2-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="991a2-154">使用 Windows PowerShell 脚本</span><span class="sxs-lookup"><span data-stu-id="991a2-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="991a2-155">已提供了 Windows PowerShell 脚本，因此您可以轻松设置[配置导出到 Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) 中介绍的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="991a2-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="991a2-156">如果您希望进行手动设置，请跳过此过程，然后继续执行[手动设置](#manual-setup)部分中的过程。</span><span class="sxs-lookup"><span data-stu-id="991a2-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="991a2-157">请按照以下步骤运行 PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="991a2-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="991a2-158">Azure CLI 的“尝试”选项，否则在 PC 上运行脚本可能无效。</span><span class="sxs-lookup"><span data-stu-id="991a2-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="991a2-159">请按照以下步骤使用 Windows PowerShell 脚本配置 Azure。</span><span class="sxs-lookup"><span data-stu-id="991a2-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="991a2-160">您必须有权创建 Azure 资源组、Azure 资源和 Azure AD 应用程序。</span><span class="sxs-lookup"><span data-stu-id="991a2-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="991a2-161">有关所需权限的信息，请参阅[检查 Azure AD 权限](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)。</span><span class="sxs-lookup"><span data-stu-id="991a2-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="991a2-162">在 [Azure 门户](https://portal.azure.com)中，转到目标 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="991a2-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="991a2-163">选择 **搜索** 字段右侧的 **Cloud Shell** 按钮。</span><span class="sxs-lookup"><span data-stu-id="991a2-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="991a2-164">选择 **PowerShell**。</span><span class="sxs-lookup"><span data-stu-id="991a2-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="991a2-165">如果提示您创建存储，请创建。</span><span class="sxs-lookup"><span data-stu-id="991a2-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="991a2-166">转到 **Azure CLI** 选项卡，选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="991a2-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="991a2-167">打开记事本，粘贴 PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="991a2-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="991a2-168">将文件另存为 ConfigureDataLake.ps1。</span><span class="sxs-lookup"><span data-stu-id="991a2-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="991a2-169">使用菜单选项将 Windows PowerShell 脚本上载到会话，以在 Cloud Shell 中上载。</span><span class="sxs-lookup"><span data-stu-id="991a2-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="991a2-170">运行脚本 .\ConfigureDataLake.ps1。</span><span class="sxs-lookup"><span data-stu-id="991a2-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="991a2-171">按照提示运行脚本。</span><span class="sxs-lookup"><span data-stu-id="991a2-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="991a2-172">使用脚本输出中的信息在 LCS 中安装 **导出到 Data Lake** 加载项。</span><span class="sxs-lookup"><span data-stu-id="991a2-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="991a2-173">使用脚本输出中的信息在 Finance 中的 **数据连接** 页面（**系统管理 \> 系统参数 \> 数据连接**）上启用实体存储。</span><span class="sxs-lookup"><span data-stu-id="991a2-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="991a2-174">手动设置</span><span class="sxs-lookup"><span data-stu-id="991a2-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="991a2-175">向 Azure AD 租户添加应用程序</span><span class="sxs-lookup"><span data-stu-id="991a2-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="991a2-176">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="991a2-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="991a2-177">选择 **管理 \> Enterprise 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="991a2-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="991a2-178">通过应用 ID 搜索以下应用程序。</span><span class="sxs-lookup"><span data-stu-id="991a2-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="991a2-179">申请</span><span class="sxs-lookup"><span data-stu-id="991a2-179">Application</span></span>                              | <span data-ttu-id="991a2-180">应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="991a2-181">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="991a2-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="991a2-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="991a2-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="991a2-183">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="991a2-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="991a2-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="991a2-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="991a2-185">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="991a2-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="991a2-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="991a2-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="991a2-187">如果找不到上述任何应用程序，请尝试以下步骤。</span><span class="sxs-lookup"><span data-stu-id="991a2-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="991a2-188">在本地计算机上，选择 **开始** 菜单，然后搜索 **powershell**。</span><span class="sxs-lookup"><span data-stu-id="991a2-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="991a2-189">选中并按住（或右键单击）**Windows PowerShell**，然后选择 **以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="991a2-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="991a2-190">运行以下命令以安装 **AzureAD** 模块。</span><span class="sxs-lookup"><span data-stu-id="991a2-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="991a2-191">如果需要 NuGet 提供商才能继续，请选择 **Y** 进行安装。</span><span class="sxs-lookup"><span data-stu-id="991a2-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="991a2-192">如果出现“不受信任的存储库”消息，请选择 **Y** 以继续操作。</span><span class="sxs-lookup"><span data-stu-id="991a2-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="991a2-193">对于必须添加的每个应用程序，运行以下命令以将该应用程序添加到 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="991a2-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="991a2-194">出现提示时，以 Azure AD 管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="991a2-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="991a2-195">创建 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="991a2-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="991a2-196">确保在与 Dataverse 环境相同的 Azure AD 实例中创建以下资源。</span><span class="sxs-lookup"><span data-stu-id="991a2-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="991a2-197">不能使用其他 Azure AD 实例的资源。</span><span class="sxs-lookup"><span data-stu-id="991a2-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="991a2-198">创建新的存储帐户：</span><span class="sxs-lookup"><span data-stu-id="991a2-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="991a2-199">在 [Azure 门户](https://portal.azure.com)中，创建一个存储帐户。</span><span class="sxs-lookup"><span data-stu-id="991a2-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="991a2-200">在 **创建存储帐户** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="991a2-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="991a2-201">**位置** – 选择环境所在的数据中心。</span><span class="sxs-lookup"><span data-stu-id="991a2-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="991a2-202">**性能** – 建议您选择 **标准**。</span><span class="sxs-lookup"><span data-stu-id="991a2-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="991a2-203">**帐户种类** – 必须选择 **StorageV2**。</span><span class="sxs-lookup"><span data-stu-id="991a2-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="991a2-204">在 **高级选项** 对话框中，在 **分层命名空间** 功能下为 **Data Lake 存储 Gen2** 选项选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="991a2-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="991a2-205">如果禁用此功能，则无法使用 Finance and Operations 应用使用 Power BI 数据流之类服务写入的数据。</span><span class="sxs-lookup"><span data-stu-id="991a2-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="991a2-206">选择 **查看并创建**。</span><span class="sxs-lookup"><span data-stu-id="991a2-206">Select **Review and create**.</span></span> <span data-ttu-id="991a2-207">部署完成后，新资源将显示在 Azure 门户中。</span><span class="sxs-lookup"><span data-stu-id="991a2-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="991a2-208">转到您创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="991a2-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="991a2-209">在左侧菜单中，选择 **访问密钥**。</span><span class="sxs-lookup"><span data-stu-id="991a2-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="991a2-210">复制并保存 **Key1** 或 **Key2** 的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="991a2-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="991a2-211">复制并保存存储帐户名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="991a2-212">创建新的密钥保管库：</span><span class="sxs-lookup"><span data-stu-id="991a2-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="991a2-213">在 [Azure 门户](https://portal.azure.com)中，创建一个密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="991a2-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="991a2-214">在 **创建密钥保管库** 对话框的 **位置** 字段中，选择您的环境所在数据中心。</span><span class="sxs-lookup"><span data-stu-id="991a2-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="991a2-215">创建密钥保管库之后，在列表中选择它，然后选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="991a2-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="991a2-216">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="991a2-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="991a2-217">在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="991a2-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="991a2-218">请输入密码的名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-218">Enter a name for the secret.</span></span> <span data-ttu-id="991a2-219">记下该名称，因为稍后将需要提供它。</span><span class="sxs-lookup"><span data-stu-id="991a2-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="991a2-220">在 **值** 字段中，输入您在上一过程中从存储帐户获得的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="991a2-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="991a2-221">选择 **启用**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="991a2-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="991a2-222">将创建密码并添加到密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="991a2-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="991a2-223">转到 **密钥保管库概述**，并记下 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="991a2-224">创建并注册 Azure AD 应用程序：</span><span class="sxs-lookup"><span data-stu-id="991a2-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="991a2-225">在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory**，然后选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="991a2-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="991a2-226">选择 **新应用程序注册**，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="991a2-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="991a2-227">**名称** – 输入应用的名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="991a2-228">**应用程序类型** – 选择 **Web API**。</span><span class="sxs-lookup"><span data-stu-id="991a2-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="991a2-229">**重定向 URI 设置** – 输入您的 Dynamics 365 实例的 URL，例如 `https://yourdynamicsinstance.dynamics.com/auth`。</span><span class="sxs-lookup"><span data-stu-id="991a2-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="991a2-230">转到刚才创建的应用，然后复制并保存其 **应用程序（客户端）ID** 值。</span><span class="sxs-lookup"><span data-stu-id="991a2-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="991a2-231">之后在设置密钥保管库时必须提供此值。</span><span class="sxs-lookup"><span data-stu-id="991a2-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="991a2-232">转到 **API 权限**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="991a2-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="991a2-233">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="991a2-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="991a2-234">选择 **Azure 密钥保管库**。</span><span class="sxs-lookup"><span data-stu-id="991a2-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="991a2-235">选择委派权限后，选择 **用户\_模拟**。</span><span class="sxs-lookup"><span data-stu-id="991a2-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="991a2-236">选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="991a2-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="991a2-237">在应用的菜单上，选择 **证书 \& 密码**，然后按照以下步骤创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="991a2-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="991a2-238">选择 **新客户端密码**。</span><span class="sxs-lookup"><span data-stu-id="991a2-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="991a2-239">在 **密钥描述** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="991a2-240">选择持续时间，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="991a2-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="991a2-241">将在 **值** 字段中生成一个密码。</span><span class="sxs-lookup"><span data-stu-id="991a2-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="991a2-242">复制并保存密码值。</span><span class="sxs-lookup"><span data-stu-id="991a2-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="991a2-243">创建密钥保管库密码：</span><span class="sxs-lookup"><span data-stu-id="991a2-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="991a2-244">转到您先前创建的密钥保管库，然后选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="991a2-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="991a2-245">为下表中的每个密码名称执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="991a2-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="991a2-246">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="991a2-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="991a2-247">在 **创建密码** 对话框的 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="991a2-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="991a2-248">通过下表创建密码名称和值。</span><span class="sxs-lookup"><span data-stu-id="991a2-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="991a2-249">选择 **启用**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="991a2-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="991a2-250">将创建密码并添加到密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="991a2-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="991a2-251">密钥名称</span><span class="sxs-lookup"><span data-stu-id="991a2-251">Secret name</span></span>                       | <span data-ttu-id="991a2-252">密码值</span><span class="sxs-lookup"><span data-stu-id="991a2-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="991a2-253">应用 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-253">app-id</span></span>                            | <span data-ttu-id="991a2-254">您先前创建的应用程序的应用 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="991a2-255">应用密码</span><span class="sxs-lookup"><span data-stu-id="991a2-255">app-secret</span></span>                        | <span data-ttu-id="991a2-256">您之前保存的客户端密码</span><span class="sxs-lookup"><span data-stu-id="991a2-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="991a2-257">存储帐户名称</span><span class="sxs-lookup"><span data-stu-id="991a2-257">storage-account-name</span></span>              | <span data-ttu-id="991a2-258">您之前创建的存储帐户的名称，例如 **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="991a2-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="991a2-259">存储帐户连接字符串</span><span class="sxs-lookup"><span data-stu-id="991a2-259">storage-account-connection-string</span></span> | <span data-ttu-id="991a2-260">您从 **访问密钥** 页面为存储帐户复制的连接字符串</span><span class="sxs-lookup"><span data-stu-id="991a2-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="991a2-261">为应用程序授予访问密钥保管库的权限：</span><span class="sxs-lookup"><span data-stu-id="991a2-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="991a2-262">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="991a2-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="991a2-263">选择访问策略。</span><span class="sxs-lookup"><span data-stu-id="991a2-263">Select the access policies.</span></span>
    3. <span data-ttu-id="991a2-264">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="991a2-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="991a2-265">选择 **添加访问策略** 创建一个访问策略。</span><span class="sxs-lookup"><span data-stu-id="991a2-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="991a2-266">在 **密码权限** 字段中，从下表中选择权限。</span><span class="sxs-lookup"><span data-stu-id="991a2-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="991a2-267">在 **选择主体** 字段，搜索下表中的应用程序显示名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="991a2-268">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="991a2-268">Select **Select**.</span></span>
        5. <span data-ttu-id="991a2-269">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="991a2-269">Select **Add**.</span></span>
        6. <span data-ttu-id="991a2-270">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="991a2-270">Select **Save**.</span></span>

        | <span data-ttu-id="991a2-271">申请</span><span class="sxs-lookup"><span data-stu-id="991a2-271">Application</span></span>                                              | <span data-ttu-id="991a2-272">权限</span><span class="sxs-lookup"><span data-stu-id="991a2-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="991a2-273">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="991a2-273">The display name of the new application that you created</span></span> | <span data-ttu-id="991a2-274">获取，列表</span><span class="sxs-lookup"><span data-stu-id="991a2-274">Get, List</span></span>   |
        | <span data-ttu-id="991a2-275">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="991a2-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="991a2-276">获取，列表</span><span class="sxs-lookup"><span data-stu-id="991a2-276">Get, List</span></span>   |

6. <span data-ttu-id="991a2-277">分配角色以访问存储帐户：</span><span class="sxs-lookup"><span data-stu-id="991a2-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="991a2-278">在 [Azure 门户](https://portal.azure.com)中，打开您之前创建的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="991a2-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="991a2-279">选择 **访问控制 (IAM)**，然后选择 **角色分配**。</span><span class="sxs-lookup"><span data-stu-id="991a2-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="991a2-280">选择 **添加，添加角色分配**。</span><span class="sxs-lookup"><span data-stu-id="991a2-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="991a2-281">为下表中的每个应用程序执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="991a2-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="991a2-282">从列表中选择角色。</span><span class="sxs-lookup"><span data-stu-id="991a2-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="991a2-283">让 **将访问权限分配到** 字段保持设置为 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="991a2-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="991a2-284">在 **选择** 字段中，输入下表中的应用程序。</span><span class="sxs-lookup"><span data-stu-id="991a2-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="991a2-285">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="991a2-285">Select **Save**.</span></span>

        | <span data-ttu-id="991a2-286">申请</span><span class="sxs-lookup"><span data-stu-id="991a2-286">Application</span></span>                                              | <span data-ttu-id="991a2-287">角色</span><span class="sxs-lookup"><span data-stu-id="991a2-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="991a2-288">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="991a2-288">The display name of the new application that you created</span></span> | <span data-ttu-id="991a2-289">负责人</span><span class="sxs-lookup"><span data-stu-id="991a2-289">Owner</span></span>                       |
        | <span data-ttu-id="991a2-290">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="991a2-290">The display name of the new application that you created</span></span> | <span data-ttu-id="991a2-291">缴纳人</span><span class="sxs-lookup"><span data-stu-id="991a2-291">Contributor</span></span>                 |
        | <span data-ttu-id="991a2-292">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="991a2-292">The display name of the new application that you created</span></span> | <span data-ttu-id="991a2-293">存储帐户参与者</span><span class="sxs-lookup"><span data-stu-id="991a2-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="991a2-294">您创建的新应用程序的显示名称</span><span class="sxs-lookup"><span data-stu-id="991a2-294">The display name of the new application that you created</span></span> | <span data-ttu-id="991a2-295">存储 Blob 数据负责人</span><span class="sxs-lookup"><span data-stu-id="991a2-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="991a2-296">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="991a2-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="991a2-297">存储 Blob 数据读者</span><span class="sxs-lookup"><span data-stu-id="991a2-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="991a2-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="991a2-298">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="991a2-299">配置数据湖</span><span class="sxs-lookup"><span data-stu-id="991a2-299">Configure the data lake</span></span>

<span data-ttu-id="991a2-300">请按照以下步骤使用 LCS 将 Azure Data Lake 加载项添加到环境中。</span><span class="sxs-lookup"><span data-stu-id="991a2-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="991a2-301">登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="991a2-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="991a2-302">在 **环境加载项** 部分中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="991a2-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="991a2-303">选择 **导出到 Data Lake** 加载项。</span><span class="sxs-lookup"><span data-stu-id="991a2-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="991a2-304">输入以下值。</span><span class="sxs-lookup"><span data-stu-id="991a2-304">Enter the following values.</span></span>

    | <span data-ttu-id="991a2-305">值</span><span class="sxs-lookup"><span data-stu-id="991a2-305">Value</span></span>                                                              | <span data-ttu-id="991a2-306">说明</span><span class="sxs-lookup"><span data-stu-id="991a2-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="991a2-307">密钥保管库所在 Azure 订阅的租户 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="991a2-308">存储帐户，应用和密钥保管库所在的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="991a2-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="991a2-309">要找到此值，请打开 [Azure 门户](https://portal.azure.com)，转到 **Azure Active Directory**，然后复制 **租户 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="991a2-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="991a2-310">提供密钥保管库的 DNS 名称</span><span class="sxs-lookup"><span data-stu-id="991a2-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="991a2-311">密钥保管库的 DNS 名称，例如 `https://customkeyvault.vault.azure.net/`。</span><span class="sxs-lookup"><span data-stu-id="991a2-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="991a2-312">（此值与实体存储中使用的 DNS 名称匹配。）</span><span class="sxs-lookup"><span data-stu-id="991a2-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="991a2-313">提供包含存储帐户名称的密钥</span><span class="sxs-lookup"><span data-stu-id="991a2-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="991a2-314">**存储帐户名称**</span><span class="sxs-lookup"><span data-stu-id="991a2-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="991a2-315">要用于访问 Data Lake 的应用 ID 的密码名称</span><span class="sxs-lookup"><span data-stu-id="991a2-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="991a2-316">**应用 ID**</span><span class="sxs-lookup"><span data-stu-id="991a2-316">**app-id**</span></span> |
    | <span data-ttu-id="991a2-317">与应用 ID 一起使用的密码名称</span><span class="sxs-lookup"><span data-stu-id="991a2-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="991a2-318">**应用密码**</span><span class="sxs-lookup"><span data-stu-id="991a2-318">**app-secret**</span></span> |

5. <span data-ttu-id="991a2-319">同意条款，然后选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="991a2-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="991a2-320">该加载项将在几分钟内安装。</span><span class="sxs-lookup"><span data-stu-id="991a2-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="991a2-321">配置 AI Builder</span><span class="sxs-lookup"><span data-stu-id="991a2-321">Configure AI Builder</span></span>

1. <span data-ttu-id="991a2-322">登录到 LCS，然后打开 **环境详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="991a2-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="991a2-323">滚动到 **环境加载项** 部分。</span><span class="sxs-lookup"><span data-stu-id="991a2-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="991a2-324">您应该看到此环境中已经安装的加载项。</span><span class="sxs-lookup"><span data-stu-id="991a2-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="991a2-325">如果其中不包含 **导出到 Data Lake** 加载项，请配置此加载项。</span><span class="sxs-lookup"><span data-stu-id="991a2-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="991a2-326">选择 **获取见解** 加载项。</span><span class="sxs-lookup"><span data-stu-id="991a2-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="991a2-327">在 **获取见解** 加载项的详细信息页面上，输入以下值。</span><span class="sxs-lookup"><span data-stu-id="991a2-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="991a2-328">值</span><span class="sxs-lookup"><span data-stu-id="991a2-328">Value</span></span>                                                    | <span data-ttu-id="991a2-329">说明</span><span class="sxs-lookup"><span data-stu-id="991a2-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="991a2-330">CDS 组织 URL</span><span class="sxs-lookup"><span data-stu-id="991a2-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="991a2-331">从上面复制的 Dataverse 组织 URL。</span><span class="sxs-lookup"><span data-stu-id="991a2-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="991a2-332">CDS 组织 ID</span><span class="sxs-lookup"><span data-stu-id="991a2-332">CDS Org ID</span></span>                                               | <span data-ttu-id="991a2-333">从上面复制的 Dataverse 组织 ID。</span><span class="sxs-lookup"><span data-stu-id="991a2-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="991a2-334">启用 **是租户的默认环境**。</span><span class="sxs-lookup"><span data-stu-id="991a2-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="991a2-335">配置实体存储</span><span class="sxs-lookup"><span data-stu-id="991a2-335">Configure the entity store</span></span>

<span data-ttu-id="991a2-336">请按照以下步骤在您的 Finance 环境中设置实体存储。</span><span class="sxs-lookup"><span data-stu-id="991a2-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="991a2-337">转到 **系统管理 \> 设置 \> 系统参数 \> 数据连接**。</span><span class="sxs-lookup"><span data-stu-id="991a2-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="991a2-338">设置以下密钥保管库字段：</span><span class="sxs-lookup"><span data-stu-id="991a2-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="991a2-339">**应用程序（客户端）ID** – 输入您先前创建的应用程序客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="991a2-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="991a2-340">**应用程序密码** – 输入为先前创建的应用程序保存的密码。</span><span class="sxs-lookup"><span data-stu-id="991a2-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="991a2-341">**DNS 名称**–您可以在先前创建的应用程序的应用程序详细信息页面上找到域名系统 (DNS) 名称。</span><span class="sxs-lookup"><span data-stu-id="991a2-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="991a2-342">**密码名称** – 输入 **存储帐户连接字符串**。</span><span class="sxs-lookup"><span data-stu-id="991a2-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="991a2-343">启用 **启用 Data Lake 集成**。</span><span class="sxs-lookup"><span data-stu-id="991a2-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="991a2-344">选择 **测试 Azure 密钥保管库**，验证没有错误。</span><span class="sxs-lookup"><span data-stu-id="991a2-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="991a2-345">选择 **测试 Azure 存储**，验证没有错误。</span><span class="sxs-lookup"><span data-stu-id="991a2-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="991a2-346">反馈和支持</span><span class="sxs-lookup"><span data-stu-id="991a2-346">Feedback and support</span></span>

<span data-ttu-id="991a2-347">如果对提供反馈感兴趣或需要支持，请向 [客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="991a2-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="991a2-348">隐私声明</span><span class="sxs-lookup"><span data-stu-id="991a2-348">Privacy notice</span></span>

<span data-ttu-id="991a2-349">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="991a2-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
