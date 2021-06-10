---
title: 安装和连接仓库管理移动应用
description: 本主题说明如何在每个移动设备上安装仓库管理移动应用，以及如何进行配置以将其连接到 Microsoft Dynamics 365 Supply Chain Management 环境。
author: MarkusFogelberg
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 810592bcbe11b03753c12ab7bfe6160d3e9233ee
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049308"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a><span data-ttu-id="f9e17-103">安装和连接仓库管理移动应用</span><span class="sxs-lookup"><span data-stu-id="f9e17-103">Install and connect the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f9e17-104">本主题介绍如何配置新的仓库管理移动应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-104">This topic describes how to configure the new Warehouse Management mobile app.</span></span> <span data-ttu-id="f9e17-105">如果要查找有关如何配置旧仓库应用（现在已弃用）的信息，请参阅[安装和连接仓库应用](../../supply-chain/warehousing/install-configure-warehousing-app.md)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-105">If you're looking for information about how to configure the old warehouse app (now deprecated), see [Install and connect the warehouse app](../../supply-chain/warehousing/install-configure-warehousing-app.md).</span></span>

<span data-ttu-id="f9e17-106">本主题说明如何在每个移动设备上下载和安装仓库管理移动应用，以及如何配置应用来将其连接到 Supply Chain Management 环境。</span><span class="sxs-lookup"><span data-stu-id="f9e17-106">This topic explains how to download and install the Warehouse Management mobile app on each of your mobile devices, and how configure the app to connect to your Supply Chain Management environment.</span></span> <span data-ttu-id="f9e17-107">可以手动配置每个设备，也可以通过文件或使用 QR 代码导入连接字符串。</span><span class="sxs-lookup"><span data-stu-id="f9e17-107">You can configure each device manually, or you can import connection settings through a file or by scanning a QR code.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="f9e17-108">系统要求</span><span class="sxs-lookup"><span data-stu-id="f9e17-108">System requirements</span></span>

<span data-ttu-id="f9e17-109">Windows 和 Google Android 操作系统均支持仓库管理移动应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-109">The Warehouse Management mobile app is available for both Windows and Google Android operating systems.</span></span> <span data-ttu-id="f9e17-110">若要使用此应用，您的移动设备上必须安装以下操作系统之一：</span><span class="sxs-lookup"><span data-stu-id="f9e17-110">To use the app, one of the following operating systems must be installed on your mobile devices:</span></span>

- <span data-ttu-id="f9e17-111">Windows 10（通用 Windows 平台 \[UWP\]）2018 年 10 月更新 1809（内部版本 10.0.17763）或更高版本</span><span class="sxs-lookup"><span data-stu-id="f9e17-111">Windows 10 (Universal Windows Platform \[UWP\]) October 2018 update 1809 (build 10.0.17763) or later</span></span>
- <span data-ttu-id="f9e17-112">Android 4.4 或更高版本</span><span class="sxs-lookup"><span data-stu-id="f9e17-112">Android 4.4 or later</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="f9e17-113">开启功能</span><span class="sxs-lookup"><span data-stu-id="f9e17-113">Turn on the feature</span></span>

<span data-ttu-id="f9e17-114">您必须先在系统中打开相关功能，然后才能使用此应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-114">Before you can use the app, a related feature must be turned on in your system.</span></span> <span data-ttu-id="f9e17-115">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="f9e17-115">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f9e17-116">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="f9e17-116">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f9e17-117">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="f9e17-117">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f9e17-118">**功能名称**：*新仓库应用的用户设置、图标和步骤标题*</span><span class="sxs-lookup"><span data-stu-id="f9e17-118">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="get-the-warehouse-management-mobile-app"></a><span data-ttu-id="f9e17-119">获取仓库管理移动应用</span><span class="sxs-lookup"><span data-stu-id="f9e17-119">Get the Warehouse Management mobile app</span></span>

<span data-ttu-id="f9e17-120">对于较小部署，通常可能在每个设备上从相关商店安装此应用，然后手动配置与您在使用的环境之间的连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-120">For smaller deployments, you might typically install the app on each device from the relevant store and then manually configure the connection to the environments that you're using.</span></span>

<span data-ttu-id="f9e17-121">对于较大部署，您可以自动化应用部署和/或配置，如果您管理很多设备，这样会更加方便。</span><span class="sxs-lookup"><span data-stu-id="f9e17-121">For larger deployments, you can automate app deployment and/or configuration, which can be more convenient if you manage many devices.</span></span> <span data-ttu-id="f9e17-122">例如，您可能使用移动设备管理和移动应用程序管理解决方案，如 [Microsoft Intune](/mem/intune/fundamentals/what-is-intune)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-122">For example, you might use a mobile device management and mobile application management solution such as [Microsoft Intune](/mem/intune/fundamentals/what-is-intune).</span></span> <span data-ttu-id="f9e17-123">有关如何使用 Intune 添加应用程序的信息，请参阅[向 Microsoft Intune 添加应用](/mem/intune/apps/apps-add)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-123">For information about how to use Intune to add applications, see [Add apps to Microsoft Intune](/mem/intune/apps/apps-add).</span></span>

### <a name="install-the-app-from-an-app-store"></a><span data-ttu-id="f9e17-124">从应用商店安装应用</span><span class="sxs-lookup"><span data-stu-id="f9e17-124">Install the app from an app store</span></span>

<span data-ttu-id="f9e17-125">在单个设备上安装应用的最简单方法是从应用商店安装，应用商店始终会提供最新的正式发布版本。</span><span class="sxs-lookup"><span data-stu-id="f9e17-125">The easiest way to install the app on single device is to install it from an app store, which always provides the latest generally available version.</span></span> <span data-ttu-id="f9e17-126">Microsoft Intune 也可以从应用商店获取应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-126">Microsoft Intune can also fetch apps from the app stores.</span></span> <span data-ttu-id="f9e17-127">使用以下链接之一从应用商店安装应用：</span><span class="sxs-lookup"><span data-stu-id="f9e17-127">Use one of the following links to install the app from an app store:</span></span>

- <span data-ttu-id="f9e17-128">**Windows (UWP)**：[Microsoft Store 中的仓库管理](https://www.microsoft.com/store/apps/9pd35cdqcmg3)</span><span class="sxs-lookup"><span data-stu-id="f9e17-128">**Windows (UWP):** [Warehouse Management on Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)</span></span>

- <span data-ttu-id="f9e17-129">**Android**：[Google Play 商店中的仓库管理](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)</span><span class="sxs-lookup"><span data-stu-id="f9e17-129">**Android:** [Warehouse Management on Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)</span></span>

### <a name="download-the-app-from-microsoft-app-center"></a><span data-ttu-id="f9e17-130">从 Microsoft App Center 下载应用</span><span class="sxs-lookup"><span data-stu-id="f9e17-130">Download the app from Microsoft App Center</span></span>

<span data-ttu-id="f9e17-131">作为从应用商店安装的替代方法，您可以从 Microsoft App Center 下载应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-131">As an alternative to installing from an app store, you can instead download the app from the Microsoft App Center.</span></span> <span data-ttu-id="f9e17-132">App Center 提供可以旁加载的可安装包。</span><span class="sxs-lookup"><span data-stu-id="f9e17-132">The App Center provides installable packages that you can sideload.</span></span> <span data-ttu-id="f9e17-133">除了当前版本外，App Center 还允许您下载以前的版本，而且可以提供包含您可以试用的即将发布功能的预览版本。要从 Microsoft App Center 下载仓库管理移动应用的当前、先前或预览版本，请使用以下链接之一：</span><span class="sxs-lookup"><span data-stu-id="f9e17-133">In addition to the current version, the App Center also lets you download previous versions and may provide preview versions with upcoming features that you can try out. To download current, previous, or preview versions of the Warehouse Management mobile app from Microsoft App Center, use one of the following links:</span></span>

- <span data-ttu-id="f9e17-134">**Windows (UWP)**：[仓库管理 (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)</span><span class="sxs-lookup"><span data-stu-id="f9e17-134">**Windows (UWP):** [Warehouse Management (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)</span></span>  
    <span data-ttu-id="f9e17-135">有关如何在 Windows 设备上安装下载的包然后设置所需证书的说明，请参阅[从 App Center 安装版本](/appcenter/distribution/installation)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-135">For instructions about how to install a downloaded package on a Windows device and then set up the required certificates, see [Install a Build from App Center](/appcenter/distribution/installation).</span></span>

- <span data-ttu-id="f9e17-136">**Android**：[仓库管理 (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)</span><span class="sxs-lookup"><span data-stu-id="f9e17-136">**Android:** [Warehouse Management (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)</span></span>  
    <span data-ttu-id="f9e17-137">如果您下载预览版，需要执行一些额外的步骤进行安装。</span><span class="sxs-lookup"><span data-stu-id="f9e17-137">If you download a preview version, a few extra steps are required to install it.</span></span> <span data-ttu-id="f9e17-138">有关详细信息，请参阅[测试 Android 应用](/appcenter/distribution/testers/testing-android)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-138">For details, see [Testing Android Apps](/appcenter/distribution/testers/testing-android).</span></span>

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a><span data-ttu-id="f9e17-139">在 Azure Active Directory 中创建 Web 服务应用程序</span><span class="sxs-lookup"><span data-stu-id="f9e17-139">Create a web service application in Azure Active Directory</span></span>

<span data-ttu-id="f9e17-140">若要使仓库管理移动应用与特定 Supply Chain Management 服务器交互，必须在 Azure Active Directory (Azure AD) 中注册一个 Web 服务应用程序，以便获得 Supply Chain Management 租户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-140">To enable the Warehouse Management mobile app to interact with a specific Supply Chain Management server, you must register a web service application for the Supply Chain Management tenant in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="f9e17-141">以下过程显示了一种完成此任务的方法。</span><span class="sxs-lookup"><span data-stu-id="f9e17-141">The following procedure shows one way to complete this task.</span></span> <span data-ttu-id="f9e17-142">有关详细信息和备用方法，请参阅此过程后的链接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-142">For detailed information and alternatives, see the links after the procedure.</span></span>

1. <span data-ttu-id="f9e17-143">在 Web 浏览器中，转至 [https://portal.azure.com](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-143">In a web browser, go to [https://portal.azure.com](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="f9e17-144">输入有权访问 Azure 订阅的用户的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-144">Enter the name and password of the user who has access to the Azure subscription.</span></span>
1. <span data-ttu-id="f9e17-145">在 Azure 门户的左侧导航窗格中，选择 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-145">In the Azure portal, in the left navigation pane, select **Azure Active Directory**.</span></span>

    <span data-ttu-id="f9e17-146">![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")</span><span class="sxs-lookup"><span data-stu-id="f9e17-146">![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")</span></span>

1. <span data-ttu-id="f9e17-147">确保使用 Supply Chain Management 所用 Azure AD 实例。</span><span class="sxs-lookup"><span data-stu-id="f9e17-147">Make sure that you're working with the instance of Azure AD that is used by Supply Chain Management.</span></span>
1. <span data-ttu-id="f9e17-148">在 **管理** 列表中，选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-148">In the **Manage** list, select **App registrations**.</span></span>

    <span data-ttu-id="f9e17-149">![应用注册](media/app-connect-azure-register.png "应用注册")</span><span class="sxs-lookup"><span data-stu-id="f9e17-149">![App registrations](media/app-connect-azure-register.png "App registrations")</span></span>

1. <span data-ttu-id="f9e17-150">在工具栏中，选择 **新注册** 打开 **注册应用程序** 向导。</span><span class="sxs-lookup"><span data-stu-id="f9e17-150">On the toolbar, select **New registration** to open the **Register an application** wizard.</span></span>
1. <span data-ttu-id="f9e17-151">输入应用程序的名称，选择 **仅此组织目录中的帐户** 选项，然后选择 **注册**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-151">Enter a name for the application, select the **Accounts in this organizational directory only** option, and then select **Register**.</span></span>

    <span data-ttu-id="f9e17-152">![注册应用程序向导](media/app-connect-azure-register-wizard.png "注册应用程序向导")</span><span class="sxs-lookup"><span data-stu-id="f9e17-152">![Register an application wizard](media/app-connect-azure-register-wizard.png "Register an application wizard")</span></span>

1. <span data-ttu-id="f9e17-153">将打开您的新应用注册。</span><span class="sxs-lookup"><span data-stu-id="f9e17-153">Your new app registration is opened.</span></span> <span data-ttu-id="f9e17-154">记下 **应用程序（客户端）ID** 值，因为后面需要该值。</span><span class="sxs-lookup"><span data-stu-id="f9e17-154">Make a note of the **Application (client) ID** value, because you will need it later.</span></span> <span data-ttu-id="f9e17-155">本主题后文将此 ID 称为 *客户端 ID*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-155">This ID will be referred to later in this topic as the *client ID*.</span></span>

    <span data-ttu-id="f9e17-156">![应用程序（客户端）ID](media/app-connect-azure-app-id.png "应用程序（客户端）ID")</span><span class="sxs-lookup"><span data-stu-id="f9e17-156">![Application (client) ID](media/app-connect-azure-app-id.png "Application (client) ID")</span></span>

1. <span data-ttu-id="f9e17-157">在 **管理** 列表中，选择 **证书和密码**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-157">In the **Manage** list, select **Certificate & secrets**.</span></span> <span data-ttu-id="f9e17-158">然后选择下面的一个按钮，具体取决于要如何针对身份验证配置应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-158">Then select one of the following buttons, depending on how you want to configure the app for authentication.</span></span> <span data-ttu-id="f9e17-159">（有关详细信息，请参阅本主题后文的[使用证书或客户端密码](#authenticate)部分。）</span><span class="sxs-lookup"><span data-stu-id="f9e17-159">(For more information, see the [Authenticate by using a certificate or client secret](#authenticate) section later in this topic.)</span></span>

    - <span data-ttu-id="f9e17-160">**上传证书** – 上传证书充当密码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-160">**Upload certificate** – Upload a certificate to use as a secret.</span></span> <span data-ttu-id="f9e17-161">建议使用此方法，因为更安全，也可以更完整地自动执行。</span><span class="sxs-lookup"><span data-stu-id="f9e17-161">We recommend this approach, because it's more secure and can also be automated more completely.</span></span> <span data-ttu-id="f9e17-162">如果要在 Windows 设备上运行仓库管理移动应用，请记下上传证书后显示的 **指纹** 值。</span><span class="sxs-lookup"><span data-stu-id="f9e17-162">If you're running the Warehouse Management mobile app on Windows devices, make a note of the **Thumbprint** value that is shown after you upload the certificate.</span></span> <span data-ttu-id="f9e17-163">在 Windows 设备上配置证书时需要此值。</span><span class="sxs-lookup"><span data-stu-id="f9e17-163">You will need this value when you configure the certificate on Windows devices.</span></span>
    - <span data-ttu-id="f9e17-164">**新客户端密码** – 通过在 **密码** 部分中输入密钥说明和持续时间创建密钥，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-164">**New client secret** – Create a key by entering a key description and a duration in the **Passwords** section, and then select **Add**.</span></span> <span data-ttu-id="f9e17-165">创建密钥备份，然后安全存储。</span><span class="sxs-lookup"><span data-stu-id="f9e17-165">Make a copy of the key, and store it securely.</span></span>

    <span data-ttu-id="f9e17-166">![证书和密码](media/app-connect-azure-authentication.png "证书和密码")</span><span class="sxs-lookup"><span data-stu-id="f9e17-166">![Certificate & secrets](media/app-connect-azure-authentication.png "Certificate & secrets")</span></span>

<span data-ttu-id="f9e17-167">有关如何在 Azure AD 中设置 Web 服务应用程序的详细信息，请参阅以下资源：</span><span class="sxs-lookup"><span data-stu-id="f9e17-167">For more information about how to set up web service applications in Azure AD, see the following resources:</span></span>

- <span data-ttu-id="f9e17-168">有关如何使用 Windows PowerShell 在 Azure AD 中设置 Web 服务应用程序的说明，请参阅[方法：使用 Azure PowerShell 和证书创建服务主体](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-168">For instructions that show how to use Windows PowerShell to set up web service applications in Azure AD, see [How to: Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).</span></span>
- <span data-ttu-id="f9e17-169">有关如何在 Azure AD 中手动创建 Web 服务应用程序的完整详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="f9e17-169">For complete details about how to manually create a web service application in Azure AD, see the following topics:</span></span>

    - [<span data-ttu-id="f9e17-170">快速入门：向 Microsoft 身份平台注册应用程序</span><span class="sxs-lookup"><span data-stu-id="f9e17-170">Quickstart: Register an application with the Microsoft identity platform</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="f9e17-171">方法：使用门户创建可访问资源的 Azure AD 应用程序和服务主体</span><span class="sxs-lookup"><span data-stu-id="f9e17-171">How to: Use the portal to create an Azure AD application and service principal that can access resources</span></span>](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><span data-ttu-id="f9e17-172">在 Supply Chain Management 中创建和配置用户帐户</span><span class="sxs-lookup"><span data-stu-id="f9e17-172">Create and configure a user account in Supply Chain Management</span></span>

<span data-ttu-id="f9e17-173">若要让 Supply Chain Management 使用您的 Azure AD 应用程序，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f9e17-173">To enable Supply Chain Management to use your Azure AD application, follow these steps.</span></span>

1. <span data-ttu-id="f9e17-174">创建与仓库管理移动应用的用户凭据对应的用户：</span><span class="sxs-lookup"><span data-stu-id="f9e17-174">Create a user that corresponds to the user credentials for the Warehouse Management mobile app:</span></span>

    1. <span data-ttu-id="f9e17-175">在 Supply Chain Management 中，转到 **系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-175">In Supply Chain Management, go to **System administration \> Users \> Users**.</span></span>
    1. <span data-ttu-id="f9e17-176">创建一个用户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-176">Create a user.</span></span>
    1. <span data-ttu-id="f9e17-177">分配仓库移动设备用户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-177">Assign the warehousing mobile device user.</span></span>

    <span data-ttu-id="f9e17-178">![分配仓库移动设备用户](media/app-connect-app-users.png "分配仓库移动设备用户")</span><span class="sxs-lookup"><span data-stu-id="f9e17-178">![Assign the warehousing mobile device user](media/app-connect-app-users.png "Assign the warehousing mobile device user")</span></span>

1. <span data-ttu-id="f9e17-179">将您的 Azure AD 应用程序与仓库管理移动应用用户关联：</span><span class="sxs-lookup"><span data-stu-id="f9e17-179">Associate your Azure AD application with the Warehouse Management mobile app user:</span></span>

    1. <span data-ttu-id="f9e17-180">转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-180">Go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
    1. <span data-ttu-id="f9e17-181">创建一行。</span><span class="sxs-lookup"><span data-stu-id="f9e17-181">Create a line.</span></span>
    1. <span data-ttu-id="f9e17-182">输入在上一部分中记下的客户端 ID，为其命名，然后选择刚才创建的用户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-182">Enter the client ID that you made a note of in the previous section, give it a name, and select the user that you just created.</span></span> <span data-ttu-id="f9e17-183">建议标记所有设备。</span><span class="sxs-lookup"><span data-stu-id="f9e17-183">We recommend that you tag all your devices.</span></span> <span data-ttu-id="f9e17-184">然后，如果设备丢失，可以轻松从此页解除其对 Supply Chain Management 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f9e17-184">Then, if a device is lost, you can easily remove its access to Supply Chain Management from this page.</span></span>

    <span data-ttu-id="f9e17-185">![Azure Active Directory 应用程序](media/app-connect-aad-apps.png "Azure Active Directory 应用程序")</span><span class="sxs-lookup"><span data-stu-id="f9e17-185">![Azure Active Directory applications](media/app-connect-aad-apps.png "Azure Active Directory applications")</span></span>

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a><span data-ttu-id="f9e17-186">使用证书或客户端密码进行身份验证</span><span class="sxs-lookup"><span data-stu-id="f9e17-186">Authenticate by using a certificate or client secret</span></span>

<span data-ttu-id="f9e17-187">使用 Azure AD 进行身份验证可以安全地将移动设备连接到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="f9e17-187">Authentication with Azure AD provides a secure way of connecting a mobile device to Supply Chain Management.</span></span> <span data-ttu-id="f9e17-188">可以通过使用客户端密码或证书进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="f9e17-188">You can authenticate by using either a client secret or a certificate.</span></span> <span data-ttu-id="f9e17-189">如果将导入连接设置，建议使用证书，不使用客户端密码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-189">If you will import connection settings, we recommend that you use a certificate instead of a client secret.</span></span> <span data-ttu-id="f9e17-190">因为客户端密码始终安全存储，所以不能从连接设置文件或 QR 代码导入，如本主题后文所述。</span><span class="sxs-lookup"><span data-stu-id="f9e17-190">Because the client secret must always be stored securely, you can't import it from a connection settings file or a QR code, as described later in this topic.</span></span>

<span data-ttu-id="f9e17-191">请求令牌时，可以将证书用作密码来证明应用程序的身份。</span><span class="sxs-lookup"><span data-stu-id="f9e17-191">Certificates can be used as secrets to prove the application's identity when a token is requested.</span></span> <span data-ttu-id="f9e17-192">将把证书的公开部分上传到 Azure 门户中的应用注册，虽然必须将完整证书部署到安装仓库管理移动应用的每个设备上。</span><span class="sxs-lookup"><span data-stu-id="f9e17-192">The public part of the certificate is uploaded to the app registration in the Azure portal, whereas the full certificate must be deployed on each device where the Warehouse Management mobile app is installed.</span></span> <span data-ttu-id="f9e17-193">您的组织负责以轮换等方式管理证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-193">Your organization is responsible for managing the certificate in terms of rotation and so on.</span></span> <span data-ttu-id="f9e17-194">可使用自签名证书，但是始终应该使用不可导出证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-194">You can use self-signed certificates, but you should always use non-exportable certificates.</span></span>

<span data-ttu-id="f9e17-195">必须在运行仓库管理移动应用的每个设备本地提供证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-195">You must make the certificate available locally on each device where you run the Warehouse Management mobile app.</span></span> <span data-ttu-id="f9e17-196">有关如何在使用 Intune 时管理 Intune 控制的设备的证书的信息，请参阅[在 Microsoft Intune 中将证书用于身份验证](/mem/intune/protect/certificates-configure)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-196">For information about how to manage certificates for Intune-controlled devices if you're using Intune, see [Use certificates for authentication in Microsoft Intune](/mem/intune/protect/certificates-configure).</span></span>

## <a name="configure-the-application-by-importing-connection-settings"></a><span data-ttu-id="f9e17-197">通过导入连接设置配置应用程序</span><span class="sxs-lookup"><span data-stu-id="f9e17-197">Configure the application by importing connection settings</span></span>

<span data-ttu-id="f9e17-198">若要更轻松地在大量移动设备上维护和部署此应用程序，可以导入连接设置，而不是在每个设备上手动输入。</span><span class="sxs-lookup"><span data-stu-id="f9e17-198">To make it easier to maintain and deploy the application on many mobile devices, you can import the connection settings instead of manually entering them on each device.</span></span> <span data-ttu-id="f9e17-199">此部分介绍如何创建和导入设置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-199">This section explains how to create and import the settings.</span></span>

### <a name="create-a-connection-settings-file-or-qr-code"></a><span data-ttu-id="f9e17-200">创建连接设置文件或 QR 代码</span><span class="sxs-lookup"><span data-stu-id="f9e17-200">Create a connection settings file or QR code</span></span>

<span data-ttu-id="f9e17-201">可以从文件或 QR 代码导入连接设置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-201">You can import connection settings from either a file or a QR code.</span></span> <span data-ttu-id="f9e17-202">对于这两种方法，首先必须创建使用 JavaScript Object Notation (JSON) 格式和语法的设置文件。</span><span class="sxs-lookup"><span data-stu-id="f9e17-202">For both approaches, you must first create a settings file that uses JavaScript Object Notation (JSON) format and syntax.</span></span> <span data-ttu-id="f9e17-203">此文件中包含一个连接列表，该列表中包含必须添加的单个连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-203">The file must include a connection list that contains the individual connections that have to be added.</span></span> <span data-ttu-id="f9e17-204">下表汇总了必须在连接设置文件中指定的参数。</span><span class="sxs-lookup"><span data-stu-id="f9e17-204">The following table summarizes the parameters that you must specify in the connection settings file.</span></span>

| <span data-ttu-id="f9e17-205">参数</span><span class="sxs-lookup"><span data-stu-id="f9e17-205">Parameter</span></span> | <span data-ttu-id="f9e17-206">说明</span><span class="sxs-lookup"><span data-stu-id="f9e17-206">Description</span></span> |
|---|---|
| <span data-ttu-id="f9e17-207">ConnectionName</span><span class="sxs-lookup"><span data-stu-id="f9e17-207">ConnectionName</span></span> | <span data-ttu-id="f9e17-208">指定连接设置的名称。</span><span class="sxs-lookup"><span data-stu-id="f9e17-208">Specify the name of the connection setting.</span></span> <span data-ttu-id="f9e17-209">最大长度为 20 个字符。</span><span class="sxs-lookup"><span data-stu-id="f9e17-209">The maximum length is 20 characters.</span></span> <span data-ttu-id="f9e17-210">因为此值是连接设置的唯一标识符，因此请确保其在列表中唯一。</span><span class="sxs-lookup"><span data-stu-id="f9e17-210">Because this value is the unique identifier for a connection setting, make sure that it's unique in the list.</span></span> <span data-ttu-id="f9e17-211">如果设备中已有同名连接，所导入文件中的设置将覆盖该连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-211">If a connection that has the same name already exists on the device, it will be overridden by the settings from the imported file.</span></span> |
| <span data-ttu-id="f9e17-212">ActiveDirectoryClientAppId</span><span class="sxs-lookup"><span data-stu-id="f9e17-212">ActiveDirectoryClientAppId</span></span> | <span data-ttu-id="f9e17-213">指定[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="f9e17-213">Specify the client ID that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span> |
| <span data-ttu-id="f9e17-214">ActiveDirectoryResource</span><span class="sxs-lookup"><span data-stu-id="f9e17-214">ActiveDirectoryResource</span></span> | <span data-ttu-id="f9e17-215">指定 Supply Chain Management 的根 URL。</span><span class="sxs-lookup"><span data-stu-id="f9e17-215">Specify the root URL of Supply Chain Management.</span></span> |
| <span data-ttu-id="f9e17-216">ActiveDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="f9e17-216">ActiveDirectoryTenant</span></span> | <span data-ttu-id="f9e17-217">指定要用于 Supply Chain Management 服务器的 Azure AD 租户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-217">Specify the Azure AD tenant that you're using with the Supply Chain Management server.</span></span> <span data-ttu-id="f9e17-218">此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。</span><span class="sxs-lookup"><span data-stu-id="f9e17-218">This value has the form `https://login.windows.net/<your-Azure-AD-tenant-ID>`.</span></span> <span data-ttu-id="f9e17-219">下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。</span><span class="sxs-lookup"><span data-stu-id="f9e17-219">Here is an example: `https://login.windows.net/contosooperations.onmicrosoft.com`.</span></span> |
| <span data-ttu-id="f9e17-220">公司</span><span class="sxs-lookup"><span data-stu-id="f9e17-220">Company</span></span> | <span data-ttu-id="f9e17-221">在 Supply Chain Management 中指定希望应用程序连接到的法人。</span><span class="sxs-lookup"><span data-stu-id="f9e17-221">Specify the legal entity in Supply Chain Management that you want the application to connect to.</span></span> |
| <span data-ttu-id="f9e17-222">ConnectionType</span><span class="sxs-lookup"><span data-stu-id="f9e17-222">ConnectionType</span></span> | <span data-ttu-id="f9e17-223">（可选）指定连接设置应使用证书还是客户端密码连接到环境。</span><span class="sxs-lookup"><span data-stu-id="f9e17-223">(Optional) Specify whether the connection setting should use a certificate or a client secret to connect to an environment.</span></span> <span data-ttu-id="f9e17-224">有效值为 *certificate* 和 *clientsecret*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-224">Valid values are *"certificate"* and *"clientsecret"*.</span></span> <span data-ttu-id="f9e17-225">默认值为 *certificate*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-225">The default value is *"certificate"*.</span></span><p><span data-ttu-id="f9e17-226">**注意：** 不能导入客户端密码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-226">**Note:** Client secrets can't be imported.</span></span></p> |
| <span data-ttu-id="f9e17-227">IsEditable</span><span class="sxs-lookup"><span data-stu-id="f9e17-227">IsEditable</span></span> | <span data-ttu-id="f9e17-228">（可选）指定应用用户是否应该可以编辑连接设置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-228">(Optional) Specify whether the app user should be able to edit the connection setting.</span></span> <span data-ttu-id="f9e17-229">有效值为 *true* 和 *false*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-229">Valid values are *"true"* and *"false"*.</span></span> <span data-ttu-id="f9e17-230">默认值为 *true*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-230">The default value is *"true"*.</span></span> |
| <span data-ttu-id="f9e17-231">IsDefault</span><span class="sxs-lookup"><span data-stu-id="f9e17-231">IsDefault</span></span> | <span data-ttu-id="f9e17-232">（可选）指定连接是否为默认连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-232">(Optional) Specify whether the connection is the default connection.</span></span> <span data-ttu-id="f9e17-233">打开应用时，将提前选中设置为默认连接的连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-233">A connection that is set as the default connection will automatically be preselected when the app is opened.</span></span> <span data-ttu-id="f9e17-234">只能将一个连接设置为默认连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-234">Only one connection can be set as the default connection.</span></span> <span data-ttu-id="f9e17-235">有效值为 *true* 和 *false*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-235">Valid values are *"true"* and *"false"*.</span></span> <span data-ttu-id="f9e17-236">默认值为 *false*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-236">The default value is *"false"*.</span></span> |
| <span data-ttu-id="f9e17-237">CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f9e17-237">CertificateThumbprint</span></span> | <span data-ttu-id="f9e17-238">（可选）对于 Windows 设备，您可以为连接指定证书指纹。</span><span class="sxs-lookup"><span data-stu-id="f9e17-238">(Optional) For Windows devices, you can specify the certificate thumbprint for the connection.</span></span> <span data-ttu-id="f9e17-239">对于 Android 设备，则应用用户必须在首次使用连接时选择证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-239">For Android devices, the app user must select the certificate the first time that a connection is used.</span></span> |

<span data-ttu-id="f9e17-240">以下示例显示一个有效连接设置文件，该文件中包含两个连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-240">The following example shows a valid connection settings file that contains two connections.</span></span> <span data-ttu-id="f9e17-241">如您所见，连接列表（文件中的名称为 *ConnectionList*）是一个对象，该对象有一个将每个连接作为对象存储的阵列。</span><span class="sxs-lookup"><span data-stu-id="f9e17-241">As you can see, the connection list (named *"ConnectionList"* in the file) is an object that has an array that stores each connection as an object.</span></span> <span data-ttu-id="f9e17-242">每个对象必须使用括号 ({}) 括起来并使用逗号分隔，而阵列则必须使用方括号 (\[\]) 括起来。</span><span class="sxs-lookup"><span data-stu-id="f9e17-242">Each object must be enclosed in braces ({}) and separated by commas, and the array must be enclosed in brackets (\[\]).</span></span>

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

<span data-ttu-id="f9e17-243">可以将信息保存为 JSON 文件，或生成具有相同内容的 QR 代码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-243">You can either save the information as a JSON file or generate a QR code that has the same content.</span></span> <span data-ttu-id="f9e17-244">如果将信息保存为文件，建议使用默认名称 *connections.json* 保存，尤其是将把其存储在每个移动设备上的默认位置中时。</span><span class="sxs-lookup"><span data-stu-id="f9e17-244">If you save the information as a file, we recommend that you save it by using the default name, *connections.json*, especially if you will store it in the default location on each mobile device.</span></span>

### <a name="save-the-connection-settings-file-on-each-device"></a><span data-ttu-id="f9e17-245">将连接设置文件保存到每个设备上</span><span class="sxs-lookup"><span data-stu-id="f9e17-245">Save the connection settings file on each device</span></span>

<span data-ttu-id="f9e17-246">您通常使用设备管理工具或脚本将连接设置文件发放到您管理的每个设备上。</span><span class="sxs-lookup"><span data-stu-id="f9e17-246">Typically, you will use a device management tool or script to distribute the connection settings files to each device that you're managing.</span></span> <span data-ttu-id="f9e17-247">如果在每个设备上保存连接设置文件时使用默认名称和位置，仓库管理移动应用将自动导入该文件，即使是在安装该应用后首次运行期间。</span><span class="sxs-lookup"><span data-stu-id="f9e17-247">If you use the default name and location when you save the connection settings file on each device, the Warehouse Management mobile app will automatically import it, even during the first run after the app is installed.</span></span> <span data-ttu-id="f9e17-248">如果为该文件使用自定义名称或位置，应用用户必须在首次运行期间指定值。</span><span class="sxs-lookup"><span data-stu-id="f9e17-248">If you use a custom name or location for the file, the app user must specify the values during the first run.</span></span> <span data-ttu-id="f9e17-249">但是，以后此应用将继续使用指定的名称和位置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-249">However, the app will continue to use the specified name and location afterward.</span></span>

<span data-ttu-id="f9e17-250">每次启动此应用时，都将从连接设置的之前位置重新导入连接设置，以确定是否进行了任何更改。</span><span class="sxs-lookup"><span data-stu-id="f9e17-250">Every time that the app is started, it reimports the connection settings from their previous location to determine whether there have been any changes.</span></span> <span data-ttu-id="f9e17-251">此应用将仅更新与连接设置文件中的连接同名的连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-251">The app will update only connections that have the same names as the connections in the connection settings file.</span></span> <span data-ttu-id="f9e17-252">将不更新用户创建且使用其他名称的连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-252">User-created connections that use other names won't be updated.</span></span>

<span data-ttu-id="f9e17-253">不能使用连接设置文件删除连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-253">You can't remove a connection by using the connection settings file.</span></span>

<span data-ttu-id="f9e17-254">如前所述，默认文件名为 *connections.json*。</span><span class="sxs-lookup"><span data-stu-id="f9e17-254">As has been mentioned, the default file name is *connections.json*.</span></span> <span data-ttu-id="f9e17-255">默认文件位置取决于使用的是 Windows 设备还是 Android 设备：</span><span class="sxs-lookup"><span data-stu-id="f9e17-255">The default file location depends on whether you're using a Windows device or an Android device:</span></span>

- <span data-ttu-id="f9e17-256">**Windows：**`C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`</span><span class="sxs-lookup"><span data-stu-id="f9e17-256">**Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`</span></span>
- <span data-ttu-id="f9e17-257">**Android**：`Android\data\com.Microsoft.WarehouseManagement\files`</span><span class="sxs-lookup"><span data-stu-id="f9e17-257">**Android:** `Android\data\com.Microsoft.WarehouseManagement\files`</span></span>

<span data-ttu-id="f9e17-258">通常在首次运行此应用后自动创建这些路径。</span><span class="sxs-lookup"><span data-stu-id="f9e17-258">Usually, the paths are automatically created after the first run of the app.</span></span> <span data-ttu-id="f9e17-259">但是，如果必须在安装前将连接设置文件传输到设备，可以手动创建这些路径。</span><span class="sxs-lookup"><span data-stu-id="f9e17-259">However, you can manually create them if you must transfer the connection settings file to the device before installation.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e17-260">如果卸载了此应用，将删除默认路径及其内容。</span><span class="sxs-lookup"><span data-stu-id="f9e17-260">If the app is uninstalled, the default path and its contents are removed.</span></span>

### <a name="import-the-connection-settings"></a><span data-ttu-id="f9e17-261">导入连接设置</span><span class="sxs-lookup"><span data-stu-id="f9e17-261">Import the connection settings</span></span>

<span data-ttu-id="f9e17-262">执行以下步骤从文件或 QR 代码导入连接设置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-262">Follow these steps to import connection settings from a file or a QR code.</span></span>

1. <span data-ttu-id="f9e17-263">在您的移动设备上启动仓库管理移动应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-263">Start the Warehouse Management mobile app on your mobile device.</span></span> <span data-ttu-id="f9e17-264">首次启动该应用时，会显示一条欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="f9e17-264">The first time that you start the app, a welcome message is shown.</span></span> <span data-ttu-id="f9e17-265">选择 **选择连接**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-265">Select **Select a connection**.</span></span>

    <span data-ttu-id="f9e17-266">![欢迎消息](media/app-configure-welcome-screen.png "欢迎消息")</span><span class="sxs-lookup"><span data-stu-id="f9e17-266">![Welcome message](media/app-configure-welcome-screen.png "Welcome message")</span></span>

1. <span data-ttu-id="f9e17-267">如果要从文件导入连接设置，并且保存该文件时使用的是默认名称和默认位置，应用可能已经找到了该文件。</span><span class="sxs-lookup"><span data-stu-id="f9e17-267">If you're importing the connection settings from a file, and the default name and location were used when the file was saved, the app might already have found the file.</span></span> <span data-ttu-id="f9e17-268">在这种情况下，直接跳到步骤 4。</span><span class="sxs-lookup"><span data-stu-id="f9e17-268">In this case, skip ahead to step 4.</span></span> <span data-ttu-id="f9e17-269">否则，选择 **设置连接**，然后继续执行步骤 3。</span><span class="sxs-lookup"><span data-stu-id="f9e17-269">Otherwise, select **Set up connection**, and then continue to step 3.</span></span>

    <span data-ttu-id="f9e17-270">![设置连接](media/app-configure-set-up-connection.png "设置连接")</span><span class="sxs-lookup"><span data-stu-id="f9e17-270">![Set up connection](media/app-configure-set-up-connection.png "Set up connection")</span></span>

1. <span data-ttu-id="f9e17-271">在 **连接设置** 对话框中，选择 **从文件添加** 或 **从 QR 码添加**，具体取决于您要导入设置的方式：</span><span class="sxs-lookup"><span data-stu-id="f9e17-271">In the **Connection setup** dialog box, select **Add from file** or **Add from QR code**, depending on how you want to import the settings:</span></span>

    - <span data-ttu-id="f9e17-272">如果要从文件导入连接设置，则选择 **从文件添加**，浏览到本地设备上的文件，然后选择它。</span><span class="sxs-lookup"><span data-stu-id="f9e17-272">If you're importing the connection settings from a file, select **Add from file**, browse to the file on your local device, and select it.</span></span> <span data-ttu-id="f9e17-273">如果选择自定义位置，应用将存储该文件，并在下次自动使用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-273">If you select a custom location, the app will store it and automatically use it the next time.</span></span>
    - <span data-ttu-id="f9e17-274">如果要通过扫描 QR 码导入连接设置，则选择 **从 QR 码添加**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-274">If you're importing the connection settings by scanning a QR code, select **Add from QR code**.</span></span> <span data-ttu-id="f9e17-275">应用将提示您提供使用设备摄像头所需权限。</span><span class="sxs-lookup"><span data-stu-id="f9e17-275">The app prompts you for permission to use the device's camera.</span></span> <span data-ttu-id="f9e17-276">提供权限后，将启动摄像头，以便您将其用于扫描。</span><span class="sxs-lookup"><span data-stu-id="f9e17-276">After you give permission, the camera is started, so that you can use it for scanning.</span></span> <span data-ttu-id="f9e17-277">您可能发现很难获得正确扫描，具体取决于设备摄像头的质量和 QR 代码的复杂程度。</span><span class="sxs-lookup"><span data-stu-id="f9e17-277">Depending on the quality of the device's camera and the complexity of the QR code, you might find it difficult to get a correct scan.</span></span> <span data-ttu-id="f9e17-278">在这种情况下，请尝试通过为每个 QR 码仅生成一个连接来降低 QR 代码的复杂程度。</span><span class="sxs-lookup"><span data-stu-id="f9e17-278">In that case, try to reduce the complexity of the QR code by generating only one connection per QR code.</span></span> <span data-ttu-id="f9e17-279">（现在，只能使用设备摄像头扫描 QR 代码。）</span><span class="sxs-lookup"><span data-stu-id="f9e17-279">(Currently, you can use only the device's camera to scan the QR code.)</span></span>

    <span data-ttu-id="f9e17-280">![连接设置菜单](media/app-configure-connection-setup-flyout.png "连接设置菜单")</span><span class="sxs-lookup"><span data-stu-id="f9e17-280">![Connection setup menu](media/app-configure-connection-setup-flyout.png "Connection setup menu")</span></span>

1. <span data-ttu-id="f9e17-281">成功加载连接设置后，将显示所选的连接。</span><span class="sxs-lookup"><span data-stu-id="f9e17-281">When the connection settings are successfully loaded, the selected connection is shown.</span></span>

    <span data-ttu-id="f9e17-282">![已加载连接设置](media/app-configure-select-connection.png "已加载连接设置")</span><span class="sxs-lookup"><span data-stu-id="f9e17-282">![Connection settings loaded](media/app-configure-select-connection.png "Connection settings loaded")</span></span>

1. <span data-ttu-id="f9e17-283">如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-283">If you're using an Android device and are using a certificate for authentication, the device prompts you to select the certificate.</span></span>

    <span data-ttu-id="f9e17-284">![Android 设备上的选择证书提示](media/app-configure-select-certificate.png "Android 设备上的选择证书提示")</span><span class="sxs-lookup"><span data-stu-id="f9e17-284">![Select certificate prompt on an Android device](media/app-configure-select-certificate.png "Select certificate prompt on an Android device")</span></span>

1. <span data-ttu-id="f9e17-285">此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。</span><span class="sxs-lookup"><span data-stu-id="f9e17-285">The app connects to your Supply Chain Management server and shows the sign-in page.</span></span>

    <span data-ttu-id="f9e17-286">![登录页](media/app-configure-sign-in-page.png "登录页")</span><span class="sxs-lookup"><span data-stu-id="f9e17-286">![Sign-in page](media/app-configure-sign-in-page.png "Sign-in page")</span></span>

## <a name="manually-configure-the-application"></a><a name="config-manually"></a><span data-ttu-id="f9e17-287">手动配置应用程序</span><span class="sxs-lookup"><span data-stu-id="f9e17-287">Manually configure the application</span></span>

<span data-ttu-id="f9e17-288">如果您没有文件或 QR 码，可以在设备上手动配置此应用，以便通过 Azure AD 应用程序连接到 Supply Chain Management 服务器。</span><span class="sxs-lookup"><span data-stu-id="f9e17-288">If you don't have a file or QR code, you can manually configure the app on the device so that it connects to the Supply Chain Management server through the Azure AD application.</span></span>

1. <span data-ttu-id="f9e17-289">在您的移动设备上启动仓库管理移动应用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-289">Start the Warehouse Management mobile app on your mobile device.</span></span>
1. <span data-ttu-id="f9e17-290">如果应用以 **演示模式** 启动，选择 **连接设置**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-290">If the app is started in **Demo mode**, select **Connection settings**.</span></span> <span data-ttu-id="f9e17-291">如果应用启动时出现 **登录** 页，选择 **更改连接**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-291">If the **Sign-in** page appears when the app is started, select **Change connection**.</span></span>
1. <span data-ttu-id="f9e17-292">选择 **设置连接**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-292">Select **Set up connection**.</span></span>

    <span data-ttu-id="f9e17-293">![设置连接](media/app-configure-set-up-connection.png "设置连接")</span><span class="sxs-lookup"><span data-stu-id="f9e17-293">![Set up connection](media/app-configure-set-up-connection.png "Set up connection")</span></span>

1. <span data-ttu-id="f9e17-294">选择 **手动输入**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-294">Select **Input manually**.</span></span>

    <span data-ttu-id="f9e17-295">![连接设置菜单](media/app-configure-connection-setup-flyout.png "连接设置菜单")</span><span class="sxs-lookup"><span data-stu-id="f9e17-295">![Connection setup menu](media/app-configure-connection-setup-flyout.png "Connection setup menu")</span></span>

    <span data-ttu-id="f9e17-296">**新建连接** 页将出现，显示手动输入连接详细信息所需的设置。</span><span class="sxs-lookup"><span data-stu-id="f9e17-296">The **New Connection** page appears and shows the settings that are required to manually enter the connection details.</span></span>

    <span data-ttu-id="f9e17-297">![手动连接字段](media/app-configure-input-manually.png "手动连接字段")</span><span class="sxs-lookup"><span data-stu-id="f9e17-297">![Manual connection fields](media/app-configure-input-manually.png "Manual connection fields")</span></span>

1. <span data-ttu-id="f9e17-298">输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="f9e17-298">Enter the following information:</span></span>

    - <span data-ttu-id="f9e17-299">**使用客户端密码** – 将此选项设置为 _是_ 以使用客户端密码和 Supply Chain Management 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="f9e17-299">**Use client secret** – Set this option to _Yes_ to use a client secret to authenticate with Supply Chain Management.</span></span> <span data-ttu-id="f9e17-300">若要使用证书进行身份验证，请将其设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="f9e17-300">Set it to _No_ to use a certificate for authentication.</span></span> <span data-ttu-id="f9e17-301">（有关详细信息，请参阅本主题前面的[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)一节。）</span><span class="sxs-lookup"><span data-stu-id="f9e17-301">(For more information, see the [Create a web service application in Azure Active Directory](#create-service) section earlier in this topic.)</span></span>
    - <span data-ttu-id="f9e17-302">**连接名称** – 输入新连接的名称。</span><span class="sxs-lookup"><span data-stu-id="f9e17-302">**Connection name** – Enter a name for the new connection.</span></span> <span data-ttu-id="f9e17-303">下次打开连接设置时，将在 **选择连接** 字段中显示此名称。</span><span class="sxs-lookup"><span data-stu-id="f9e17-303">This name will appear in the **Select connection** field the next time that you open the connection settings.</span></span> <span data-ttu-id="f9e17-304">您输入的名称必须唯一。</span><span class="sxs-lookup"><span data-stu-id="f9e17-304">The name that you enter must be unique.</span></span> <span data-ttu-id="f9e17-305">（换句话说，如果在设备上存储了其他任何连接名称，该名称必须与这些名称不同。）</span><span class="sxs-lookup"><span data-stu-id="f9e17-305">(In other words, it must differ from all other connection names that are stored on your device, if any other connection names are stored there.)</span></span>
    - <span data-ttu-id="f9e17-306">**Active Directory 客户端 ID** – 输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="f9e17-306">**Active directory client ID** – Enter the client ID that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="f9e17-307">**Active Directory 客户端密码** – 仅当 **使用客户端密码** 选项设置为 _是_，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-307">**Active directory client secret** – This field is available only when the **Use client secret** option is set to _Yes_.</span></span> <span data-ttu-id="f9e17-308">输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="f9e17-308">Enter the client secret that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="f9e17-309">**Active Directory 证书指纹** – 此字段仅可用于 Windows 设备，且仅在 **使用客户端密码** 选项设置为 _否_ 时可用。</span><span class="sxs-lookup"><span data-stu-id="f9e17-309">**Active directory certificate thumbprint** – This field is available only for Windows devices and only when the **Use client secret** option is set to _No_.</span></span> <span data-ttu-id="f9e17-310">输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的证书指纹。</span><span class="sxs-lookup"><span data-stu-id="f9e17-310">Enter the certificate thumbprint that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="f9e17-311">**Active Directory 资源** – 指定 Supply Chain Management 的根 URL。</span><span class="sxs-lookup"><span data-stu-id="f9e17-311">**Active directory resource** – Specify the root URL of Supply Chain Management.</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="f9e17-312">请勿为此值使用反斜杠 (/)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-312">Don't end this value with a slash (/).</span></span>

    - <span data-ttu-id="f9e17-313">**Active Directory 租户** – 输入与 Supply Chain Management 服务器一起使用的 Azure AD 租户。</span><span class="sxs-lookup"><span data-stu-id="f9e17-313">**Active directory tenant** – Enter the Azure AD tenant that you're using with the Supply Chain Management server.</span></span> <span data-ttu-id="f9e17-314">此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。</span><span class="sxs-lookup"><span data-stu-id="f9e17-314">This value has the form `https://login.windows.net/<your-Azure-AD-tenant-ID>`.</span></span> <span data-ttu-id="f9e17-315">下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。</span><span class="sxs-lookup"><span data-stu-id="f9e17-315">Here is an example: `https://login.windows.net/contosooperations.onmicrosoft.com`.</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="f9e17-316">请勿为此值使用反斜杠 (/)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-316">Don't end this value with a slash (/).</span></span>

    - <span data-ttu-id="f9e17-317">**公司** – 在希望应用程序连接到的 Supply Chain Management 中输入法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="f9e17-317">**Company** – Enter the legal entity (company) in Supply Chain Management that you want the application to connect to.</span></span>

1. <span data-ttu-id="f9e17-318">选择页面右上角的 **保存** 按钮。</span><span class="sxs-lookup"><span data-stu-id="f9e17-318">Select the **Save** button in the upper-right corner of the page.</span></span>
1. <span data-ttu-id="f9e17-319">如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。</span><span class="sxs-lookup"><span data-stu-id="f9e17-319">If you're using an Android device and are using a certificate for authentication, the device prompts you to select the certificate.</span></span>
1. <span data-ttu-id="f9e17-320">此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。</span><span class="sxs-lookup"><span data-stu-id="f9e17-320">The app connects to your Supply Chain Management server and shows the sign-in page.</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="f9e17-321">取消设备的访问权限</span><span class="sxs-lookup"><span data-stu-id="f9e17-321">Remove access for a device</span></span>

<span data-ttu-id="f9e17-322">如果设备丢失或被入侵，您必须取消设备对 Supply Chain Management 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f9e17-322">If a device is lost or compromised, you must remove access to Supply Chain Management for it.</span></span> <span data-ttu-id="f9e17-323">以下步骤介绍推荐的访问权限取消流程。</span><span class="sxs-lookup"><span data-stu-id="f9e17-323">The following steps describe the recommended process for removing access.</span></span>

1. <span data-ttu-id="f9e17-324">转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-324">Go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="f9e17-325">删除与要取消访问权限的设备对应的行。</span><span class="sxs-lookup"><span data-stu-id="f9e17-325">Delete the line that corresponds to the device that you want to remove access for.</span></span> <span data-ttu-id="f9e17-326">记下用于该设备的客户端 ID，因为后面需要它。</span><span class="sxs-lookup"><span data-stu-id="f9e17-326">Make a note of the client ID that is used for the device, because you will need it later.</span></span>

    <span data-ttu-id="f9e17-327">如果仅注册了一个客户端 ID，并且多个设备使用同一个客户端 ID，则必须将新连接设置推送到这些设备。</span><span class="sxs-lookup"><span data-stu-id="f9e17-327">If you've registered only one client ID, and multiple devices use the same client ID, you must push out new connection settings to those devices.</span></span> <span data-ttu-id="f9e17-328">否则，它们将失去访问权限。</span><span class="sxs-lookup"><span data-stu-id="f9e17-328">Otherwise, they will lose access.</span></span>

1. <span data-ttu-id="f9e17-329">登录 Azure 门户，地址为 [https://portal.azure.com](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="f9e17-329">Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="f9e17-330">在左侧导航窗格中，选择 **Active Directory**，然后确保位于正确目录中。</span><span class="sxs-lookup"><span data-stu-id="f9e17-330">In the left navigation pane, select **Active Directory**, and make sure that you're in the correct directory.</span></span>
1. <span data-ttu-id="f9e17-331">在 **管理** 列表中，选择 **应用程序注册**，然后选择要配置的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f9e17-331">In the **Manage** list, select **App registrations**, and then select the application to configure.</span></span> <span data-ttu-id="f9e17-332">将显示 **设置** 页面，其中包含配置信息。</span><span class="sxs-lookup"><span data-stu-id="f9e17-332">The **Settings** page appears and shows configuration information.</span></span>
1. <span data-ttu-id="f9e17-333">确保应用程序的客户端 ID 与您在步骤 2 中记下的客户端 ID 匹配。</span><span class="sxs-lookup"><span data-stu-id="f9e17-333">Make sure that the client ID of the application matches the client ID that you made a note of in step 2.</span></span>
1. <span data-ttu-id="f9e17-334">在工具栏上，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-334">On the toolbar, select **Delete**.</span></span>
1. <span data-ttu-id="f9e17-335">在出现的确认消息中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="f9e17-335">In the confirmation message that appears, select **Yes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9e17-336">其他资源</span><span class="sxs-lookup"><span data-stu-id="f9e17-336">Additional resources</span></span>

- [<span data-ttu-id="f9e17-337">移动设备用户设置</span><span class="sxs-lookup"><span data-stu-id="f9e17-337">Mobile device user settings</span></span>](mobile-device-user-settings.md)
- [<span data-ttu-id="f9e17-338">为 Warehouse Management 移动应用分配步骤图标和标题</span><span class="sxs-lookup"><span data-stu-id="f9e17-338">Assign step icons and titles for the Warehouse Management mobile app</span></span>](step-icons-titles.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]