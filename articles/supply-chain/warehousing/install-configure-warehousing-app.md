---
title: 安装和连接仓库应用
description: 此主题说明如何在每个移动设备上安装仓库应用，以及如何进行配置以将其连接到 Microsoft Dynamics 365 Supply Chain Management 环境。 可以手动配置每个设备，也可以通过文件或使用 QR 代码导入连接字符串。
author: MarkusFogelberg
ms.date: 05/25/2020
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
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aeb9675477e728c28c38b1ef43fa6055acd23360
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909371"
---
# <a name="install-and-connect-the-warehouse-app"></a><span data-ttu-id="fb9d1-104">安装和连接仓库应用</span><span class="sxs-lookup"><span data-stu-id="fb9d1-104">Install and connect the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fb9d1-105">本主题介绍了如何配置旧仓库应用（现在已弃用）。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-105">This topic describes how to configure the old warehouse app (which is now deprecated).</span></span> <span data-ttu-id="fb9d1-106">如果您要查找有关如何配置新仓库管理移动应用的信息，请参阅[安装和连接仓库管理移动应用](install-configure-warehouse-management-app.md)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-106">If you're looking for information about how to configure the new Warehouse Management mobile app, see [Install and connect the Warehouse Management mobile app](install-configure-warehouse-management-app.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fb9d1-107">本主题介绍如何为云部署配置仓库应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-107">This topic describes how to configure the warehouse app for cloud deployments.</span></span> <span data-ttu-id="fb9d1-108">如果您需要了解有关如何为本地部署配置仓库应用的信息，请参阅[用于本地部署的仓库](../../fin-ops-core/dev-itpro/deployment/warehousing-for-on-premise-deployments.md)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-108">If you're looking for information about how to configure the warehouse app for on-premises deployments, see [Warehousing for on-premises deployments](../../fin-ops-core/dev-itpro/deployment/warehousing-for-on-premise-deployments.md).</span></span>

<span data-ttu-id="fb9d1-109">可从 Google Play Store 和 Microsoft Store 获取仓库应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-109">The warehouse app is available from Google Play Store and Microsoft Store.</span></span> <span data-ttu-id="fb9d1-110">其以独立组件的形式提供。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-110">It's provided as a standalone component.</span></span> <span data-ttu-id="fb9d1-111">因此，必须将其下载到每个设备，然后进行配置以连接到 Microsoft Dynamics 365 Supply Chain Management 环境。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-111">Therefore, you must download it on each device and then configure it to connect to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>

<span data-ttu-id="fb9d1-112">此主题说明如何在每个移动设备上安装仓库应用，以及如何进行配置以将其连接到 Supply Chain Management 环境。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-112">This topic explains how to install the warehouse app on each of your mobile devices and configure it to connect to your Supply Chain Management environment.</span></span> <span data-ttu-id="fb9d1-113">可以手动配置每个设备，也可以通过文件或使用 QR 代码导入连接字符串。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-113">You can configure each device manually, or you can import connection settings through a file or by scanning a QR code.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="fb9d1-114">系统要求</span><span class="sxs-lookup"><span data-stu-id="fb9d1-114">System requirements</span></span>

<span data-ttu-id="fb9d1-115">Windows 和 Android 操作系统均支持此仓库应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-115">The warehouse app is available for both Windows and Android operating systems.</span></span> <span data-ttu-id="fb9d1-116">若要使用此应用的最新版本，移动设备上必须安装以下操作系统之一：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-116">To use the latest version of the app, you must have one of the following operating systems installed on your mobile devices:</span></span>

- <span data-ttu-id="fb9d1-117">Windows 10（通用 Windows 平台 \[UWP\]）秋季创建者更新 1709（构建版本 10.0.16299）或更高版本</span><span class="sxs-lookup"><span data-stu-id="fb9d1-117">Windows 10 (Universal Windows Platform \[UWP\]) Fall creators update 1709 (build 10.0.16299) or later</span></span>
- <span data-ttu-id="fb9d1-118">Android 4.4 或更高版本</span><span class="sxs-lookup"><span data-stu-id="fb9d1-118">Android 4.4 or later</span></span>

> [!NOTE]
> <span data-ttu-id="fb9d1-119">如果必须支持不能运行最新 Windows 版本的较低版本 Windows 设备，仍然可以从 Microsoft Store 下载仓库应用的版本 1.6.3.0。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-119">If you must support older Windows devices that can't run the latest version of Windows, you can still download version 1.6.3.0 of the warehouse app from Microsoft Store.</span></span> <span data-ttu-id="fb9d1-120">此版本将在 Windows 10 (UWP) 11 月更新 1511（固件版本 10.0.10586）或更高版本上运行。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-120">That version will run on Windows 10 (UWP) November Update 1511 (build 10.0.10586) or later.</span></span> <span data-ttu-id="fb9d1-121">但是，请注意，此版本的仓库应用不支持批量部署连接设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-121">However, be aware that this version of the warehouse app doesn't support mass deployment of connection settings.</span></span> <span data-ttu-id="fb9d1-122">因此，必须在运行此版本应用的每个设备上[手动配置连接](#config-manually)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-122">Therefore, you must [manually configure the connection](#config-manually) on each device that runs this version of the app.</span></span>

## <a name="get-the-warehouse-app"></a><span data-ttu-id="fb9d1-123">获取仓库应用</span><span class="sxs-lookup"><span data-stu-id="fb9d1-123">Get the warehouse app</span></span>

<span data-ttu-id="fb9d1-124">使用以下链接之一下载该应用：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-124">Use one of the following links to download the app:</span></span>

- <span data-ttu-id="fb9d1-125">**Windows (UWP)**：[Microsoft Store 中的 Dynamics 365 for Finance and Operations - Warehousing](https://www.microsoft.com/store/apps/9p1bffd5tstm)</span><span class="sxs-lookup"><span data-stu-id="fb9d1-125">**Windows (UWP):** [Dynamics 365 for Finance and Operations - Warehousing on Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)</span></span>
- <span data-ttu-id="fb9d1-126">**Android**：[Google Play Store 中的 Warehousing - Dynamics 365](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)</span><span class="sxs-lookup"><span data-stu-id="fb9d1-126">**Android:** [Warehousing - Dynamics 365 on Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)</span></span>

<span data-ttu-id="fb9d1-127">对于较小部署，可能需要在每个设备上从相关商店安装此应用，然后手动配置与您在使用的环境之间的连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-127">For smaller deployments, you might want to install the app from the relevant store on each device and then manually configure the connection to the environments that you're using.</span></span> <span data-ttu-id="fb9d1-128">但是，在仓库应用的版本 1.7.0.0 及更高版本中，也可以自动执行应用部署和/或配置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-128">However, in version 1.7.0.0 and later of the warehouse app, you can also automate app deployment and/or configuration.</span></span> <span data-ttu-id="fb9d1-129">如果管理大量设备，并且在使用移动设备管理和移动应用程序管理解决方案（如 [Microsoft Intune](/mem/intune/fundamentals/what-is-intune)），可能会发现这种方法非常方便。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-129">You might find this approach convenient if you manage many devices, and you're using a mobile device management and mobile application management solution such as [Microsoft Intune](/mem/intune/fundamentals/what-is-intune).</span></span> <span data-ttu-id="fb9d1-130">有关如何使用 Intune 添加应用程序的信息，请参阅[向 Microsoft Intune 添加应用](/mem/intune/apps/apps-add)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-130">For information about how to use Intune to add applications, see [Add apps to Microsoft Intune](/mem/intune/apps/apps-add).</span></span>

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a><span data-ttu-id="fb9d1-131">在 Azure Active Directory 中创建 Web 服务应用程序</span><span class="sxs-lookup"><span data-stu-id="fb9d1-131">Create a web service application in Azure Active Directory</span></span>

<span data-ttu-id="fb9d1-132">若要使仓库应用与特定 Supply Chain Management 服务器交互，必须在 Azure Active Directory (Azure AD) 中注册一个 Web 服务应用程序，以便获得 Supply Chain Management 租户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-132">To enable the warehouse app to interact with a specific Supply Chain Management server, you must register a web service application for the Supply Chain Management tenant in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="fb9d1-133">以下过程显示了一种完成此任务的方法。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-133">The following procedure shows one way to complete this task.</span></span> <span data-ttu-id="fb9d1-134">有关详细信息和备用方法，请参阅此过程后的链接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-134">For detailed information and alternatives, see the links after the procedure.</span></span>

1. <span data-ttu-id="fb9d1-135">在 Web 浏览器中，转至 [https://portal.azure.com](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-135">In a web browser, go to [https://portal.azure.com](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="fb9d1-136">输入有权访问 Azure 订阅的用户的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-136">Enter the name and password of the user who has access to the Azure subscription.</span></span>
1. <span data-ttu-id="fb9d1-137">在 Azure 门户的左侧导航窗格中，选择 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-137">In the Azure portal, in the left navigation pane, select **Azure Active Directory**.</span></span>

    <span data-ttu-id="fb9d1-138">![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-138">![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")</span></span>

1. <span data-ttu-id="fb9d1-139">确保使用 Supply Chain Management 所用 Azure AD 实例。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-139">Make sure that you're working with the instance of Azure AD that is used by Supply Chain Management.</span></span>
1. <span data-ttu-id="fb9d1-140">在 **管理** 列表中，选择 **应用注册**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-140">In the **Manage** list, select **App registrations**.</span></span>

    <span data-ttu-id="fb9d1-141">![应用注册](media/app-connect-azure-register.png "应用注册")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-141">![App registrations](media/app-connect-azure-register.png "App registrations")</span></span>

1. <span data-ttu-id="fb9d1-142">在工具栏中，选择 **新注册** 打开 **注册应用程序** 向导。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-142">On the toolbar, select **New registration** to open the **Register an application** wizard.</span></span>
1. <span data-ttu-id="fb9d1-143">输入应用程序的名称，选择 **仅此组织目录中的帐户** 选项，然后选择 **注册**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-143">Enter a name for the application, select the **Accounts in this organizational directory only** option, and then select **Register**.</span></span>

    <span data-ttu-id="fb9d1-144">![注册应用程序向导](media/app-connect-azure-register-wizard.png "注册应用程序向导")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-144">![Register an application wizard](media/app-connect-azure-register-wizard.png "Register an application wizard")</span></span>

1. <span data-ttu-id="fb9d1-145">将打开您的新应用注册。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-145">Your new app registration is opened.</span></span> <span data-ttu-id="fb9d1-146">记下 **应用程序（客户端）ID** 值，因为后面需要该值。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-146">Make a note of the **Application (client) ID** value, because you will need it later.</span></span> <span data-ttu-id="fb9d1-147">本主题后文将此 ID 称为 *客户端 ID*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-147">This ID will be referred to later in this topic as the *client ID*.</span></span>

    <span data-ttu-id="fb9d1-148">![应用程序（客户端）ID](media/app-connect-azure-app-id.png "应用程序（客户端）ID")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-148">![Application (client) ID](media/app-connect-azure-app-id.png "Application (client) ID")</span></span>

1. <span data-ttu-id="fb9d1-149">在 **管理** 列表中，选择 **证书和密码**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-149">In the **Manage** list, select **Certificate & secrets**.</span></span> <span data-ttu-id="fb9d1-150">然后选择下面的一个按钮，具体取决于要如何针对身份验证配置应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-150">Then select one of the following buttons, depending on how you want to configure the app for authentication.</span></span> <span data-ttu-id="fb9d1-151">（有关详细信息，请参阅本主题后文的[使用证书或客户端密码](#authenticate)部分。）</span><span class="sxs-lookup"><span data-stu-id="fb9d1-151">(For more information, see the [Authenticate by using a certificate or client secret](#authenticate) section later in this topic.)</span></span>

    - <span data-ttu-id="fb9d1-152">**上传证书** – 上传证书充当密码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-152">**Upload certificate** – Upload a certificate to use as a secret.</span></span> <span data-ttu-id="fb9d1-153">建议使用此方法，因为更安全，也可以更完整地自动执行。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-153">We recommend this approach, because it's more secure and can also be automated more completely.</span></span> <span data-ttu-id="fb9d1-154">如果要在 Windows 设备上运行仓库应用，请记下上传证书后显示的 **指纹** 值。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-154">If you're running the warehouse app on Windows devices, make a note of the **Thumbprint** value that is shown after you upload the certificate.</span></span> <span data-ttu-id="fb9d1-155">在 Windows 设备上配置证书时需要此值。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-155">You will need this value when you configure the certificate on Windows devices.</span></span>
    - <span data-ttu-id="fb9d1-156">**新客户端密码** – 通过在 **密码** 部分中输入密钥说明和持续时间创建密钥，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-156">**New client secret** – Create a key by entering a key description and a duration in the **Passwords** section, and then select **Add**.</span></span> <span data-ttu-id="fb9d1-157">创建密钥备份，然后安全存储。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-157">Make a copy of the key, and store it securely.</span></span>

    <span data-ttu-id="fb9d1-158">![证书和密码](media/app-connect-azure-authentication.png "证书和密码")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-158">![Certificate & secrets](media/app-connect-azure-authentication.png "Certificate & secrets")</span></span>

<span data-ttu-id="fb9d1-159">有关如何在 Azure AD 中设置 Web 服务应用程序的详细信息，请参阅以下资源：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-159">For more information about how to set up web service applications in Azure AD, see the following resources:</span></span>

- <span data-ttu-id="fb9d1-160">有关如何使用 Windows PowerShell 在 Azure AD 中设置 Web 服务应用程序的说明，请参阅[方法：使用 Azure PowerShell 和证书创建服务主体](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-160">For instructions that show how to use Windows PowerShell to set up web service applications in Azure AD, see [How to: Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).</span></span>
- <span data-ttu-id="fb9d1-161">有关如何在 Azure AD 中手动创建 Web 服务应用程序的完整详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-161">For complete details about how to manually create a web service application in Azure AD, see the following topics:</span></span>

    - [<span data-ttu-id="fb9d1-162">快速入门：向 Microsoft 身份平台注册应用程序</span><span class="sxs-lookup"><span data-stu-id="fb9d1-162">Quickstart: Register an application with the Microsoft identity platform</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="fb9d1-163">方法：使用门户创建可访问资源的 Azure AD 应用程序和服务主体</span><span class="sxs-lookup"><span data-stu-id="fb9d1-163">How to: Use the portal to create an Azure AD application and service principal that can access resources</span></span>](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><span data-ttu-id="fb9d1-164">在 Supply Chain Management 中创建和配置用户帐户</span><span class="sxs-lookup"><span data-stu-id="fb9d1-164">Create and configure a user account in Supply Chain Management</span></span>

<span data-ttu-id="fb9d1-165">若要让 Supply Chain Management 使用您的 Azure AD 应用程序，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-165">To enable Supply Chain Management to use your Azure AD application, follow these steps.</span></span>

1. <span data-ttu-id="fb9d1-166">创建与仓库应用的用户凭据对应的用户：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-166">Create a user that corresponds to the user credentials for the warehouse app:</span></span>

    1. <span data-ttu-id="fb9d1-167">在 Supply Chain Management 中，转到 **系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-167">In Supply Chain Management, go to **System administration \> Users \> Users**.</span></span>
    1. <span data-ttu-id="fb9d1-168">创建一个用户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-168">Create a user.</span></span>
    1. <span data-ttu-id="fb9d1-169">分配仓库移动设备用户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-169">Assign the warehousing mobile device user.</span></span>

    <span data-ttu-id="fb9d1-170">![分配仓库移动设备用户](media/app-connect-app-users.png "分配仓库移动设备用户")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-170">![Assign the warehousing mobile device user](media/app-connect-app-users.png "Assign the warehousing mobile device user")</span></span>

1. <span data-ttu-id="fb9d1-171">将您的 Azure AD 应用程序与该仓库应用用户关联：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-171">Associate your Azure AD application with the warehouse app user:</span></span>

    1. <span data-ttu-id="fb9d1-172">转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-172">Go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
    1. <span data-ttu-id="fb9d1-173">创建一行。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-173">Create a line.</span></span>
    1. <span data-ttu-id="fb9d1-174">输入在上一部分中记下的客户端 ID，为其命名，然后选择刚才创建的用户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-174">Enter the client ID that you made a note of in the previous section, give it a name, and select the user that you just created.</span></span> <span data-ttu-id="fb9d1-175">建议标记所有设备。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-175">We recommend that you tag all your devices.</span></span> <span data-ttu-id="fb9d1-176">然后，如果已丢失，可以轻松从此页解除其对 Supply Chain Management 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-176">Then, if they are lost, you can easily remove their access to Supply Chain Management from this page.</span></span>

    <span data-ttu-id="fb9d1-177">![Azure Active Directory 应用程序](media/app-connect-aad-apps.png "Azure Active Directory 应用程序")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-177">![Azure Active Directory applications](media/app-connect-aad-apps.png "Azure Active Directory applications")</span></span>

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a><span data-ttu-id="fb9d1-178">使用证书或客户端密码进行身份验证</span><span class="sxs-lookup"><span data-stu-id="fb9d1-178">Authenticate by using a certificate or client secret</span></span>

<span data-ttu-id="fb9d1-179">使用 Azure AD 进行身份验证可以安全地将移动设备连接到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-179">Authentication with Azure AD provides a secure way of connecting a mobile device to Supply Chain Management.</span></span> <span data-ttu-id="fb9d1-180">可以通过使用客户端密码或证书进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-180">You can authenticate by using either a client secret or a certificate.</span></span> <span data-ttu-id="fb9d1-181">如果将导入连接设置，建议使用证书，不使用客户端密码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-181">If you will import connection settings, we recommend that you use a certificate instead of a client secret.</span></span> <span data-ttu-id="fb9d1-182">因为客户端密码始终安全存储，所以不能从连接设置文件或 QR 代码导入，如本主题后文所述。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-182">Because the client secret must always be stored securely, you can't import it from a connection settings file or a QR code, as described later in this topic.</span></span>

<span data-ttu-id="fb9d1-183">请求令牌时，可以将证书用作密码来证明应用程序的身份。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-183">Certificates can be used as secrets to prove the application's identity when a token is requested.</span></span> <span data-ttu-id="fb9d1-184">将把证书的公开部分上传到 Azure 门户中的应用注册，虽然必须将完整证书部署到安装仓库应用的每个设备上。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-184">The public part of the certificate is uploaded to the app registration in the Azure portal, whereas the full certificate must be deployed on each device where the warehouse app is installed.</span></span> <span data-ttu-id="fb9d1-185">您的组织负责以轮换等方式管理证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-185">Your organization is responsible for managing the certificate in terms of rotation and so on.</span></span> <span data-ttu-id="fb9d1-186">可使用自签名证书，但是始终应该使用不可导出证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-186">You can use self-signed certificates, but you should always use non-exportable certificates.</span></span>

<span data-ttu-id="fb9d1-187">必须在运行仓库应用的每个设备本地提供证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-187">You must make the certificate available locally on each device where you run the warehouse app.</span></span> <span data-ttu-id="fb9d1-188">有关如何在使用 Intune 时管理 Intune 控制的设备的证书的信息，请参阅[在 Microsoft Intune 中将证书用于身份验证](/mem/intune/protect/certificates-configure)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-188">For information about how to manage certificates for Intune-controlled devices if you're using Intune, see [Use certificates for authentication in Microsoft Intune](/mem/intune/protect/certificates-configure).</span></span>

## <a name="configure-the-application-by-importing-connection-settings"></a><span data-ttu-id="fb9d1-189">通过导入连接设置配置应用程序</span><span class="sxs-lookup"><span data-stu-id="fb9d1-189">Configure the application by importing connection settings</span></span>

<span data-ttu-id="fb9d1-190">若要更轻松地在大量移动设备上维护和部署此应用程序，可以导入连接设置，而不是在每个设备上手动输入。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-190">To make it easier to maintain and deploy the application on many mobile devices, you can import the connection settings instead of manually entering them on each device.</span></span> <span data-ttu-id="fb9d1-191">此部分介绍如何创建和导入设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-191">This section explains how to create and import the settings.</span></span>

### <a name="create-a-connection-settings-file-or-qr-code"></a><span data-ttu-id="fb9d1-192">创建连接设置文件或 QR 代码</span><span class="sxs-lookup"><span data-stu-id="fb9d1-192">Create a connection settings file or QR code</span></span>

<span data-ttu-id="fb9d1-193">可以从文件或 QR 代码导入连接设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-193">You can import connection settings from either a file or a QR code.</span></span> <span data-ttu-id="fb9d1-194">对于这两种方法，首先必须创建使用 JavaScript Object Notation (JSON) 格式和语法的设置文件。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-194">For both approaches, you must first create a settings file that uses JavaScript Object Notation (JSON) format and syntax.</span></span> <span data-ttu-id="fb9d1-195">此文件中包含一个连接列表，该列表中包含必须添加的单个连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-195">The file must include a connection list that contains the individual connections that have to be added.</span></span> <span data-ttu-id="fb9d1-196">下表汇总了必须在连接设置文件中指定的参数。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-196">The following table summarizes the parameters that you must specify in the connection settings file.</span></span>

| <span data-ttu-id="fb9d1-197">参数</span><span class="sxs-lookup"><span data-stu-id="fb9d1-197">Parameter</span></span> | <span data-ttu-id="fb9d1-198">说明</span><span class="sxs-lookup"><span data-stu-id="fb9d1-198">Description</span></span> |
| --- | --- |
| <span data-ttu-id="fb9d1-199">ConnectionName</span><span class="sxs-lookup"><span data-stu-id="fb9d1-199">ConnectionName</span></span> | <span data-ttu-id="fb9d1-200">指定连接设置的名称。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-200">Specify the name of the connection setting.</span></span> <span data-ttu-id="fb9d1-201">最大长度为 20 个字符。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-201">The maximum length is 20 characters.</span></span> <span data-ttu-id="fb9d1-202">因为此值是连接设置的唯一标识符，因此请确保其在列表中唯一。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-202">Because this value is the unique identifier for a connection setting, make sure that it's unique in the list.</span></span> <span data-ttu-id="fb9d1-203">如果设备中已有同名连接，所导入文件中的设置将覆盖该连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-203">If a connection that has the same name already exists on the device, it will be overridden by the settings from the imported file.</span></span> |
| <span data-ttu-id="fb9d1-204">ActiveDirectoryClientAppId</span><span class="sxs-lookup"><span data-stu-id="fb9d1-204">ActiveDirectoryClientAppId</span></span> | <span data-ttu-id="fb9d1-205">指定[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-205">Specify the client ID that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span> |
| <span data-ttu-id="fb9d1-206">ActiveDirectoryResource</span><span class="sxs-lookup"><span data-stu-id="fb9d1-206">ActiveDirectoryResource</span></span> | <span data-ttu-id="fb9d1-207">指定 Supply Chain Management 的根 URL。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-207">Specify the root URL of Supply Chain Management.</span></span> |
| <span data-ttu-id="fb9d1-208">ActiveDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="fb9d1-208">ActiveDirectoryTenant</span></span> | <span data-ttu-id="fb9d1-209">指定要用于 Supply Chain Management 服务器的 Azure AD 租户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-209">Specify the Azure AD tenant that you're using with the Supply Chain Management server.</span></span> <span data-ttu-id="fb9d1-210">此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-210">This value has the form `https://login.windows.net/<your-Azure-AD-tenant-ID>`.</span></span> <span data-ttu-id="fb9d1-211">下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-211">Here is an example: `https://login.windows.net/contosooperations.onmicrosoft.com`.</span></span> |
| <span data-ttu-id="fb9d1-212">公司</span><span class="sxs-lookup"><span data-stu-id="fb9d1-212">Company</span></span> | <span data-ttu-id="fb9d1-213">在 Supply Chain Management 中指定希望应用程序连接到的法人。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-213">Specify the legal entity in Supply Chain Management that you want the application to connect to.</span></span> |
| <span data-ttu-id="fb9d1-214">ConnectionType</span><span class="sxs-lookup"><span data-stu-id="fb9d1-214">ConnectionType</span></span> | <span data-ttu-id="fb9d1-215">（可选）指定连接设置应使用证书还是客户端密码连接到环境。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-215">(Optional) Specify whether the connection setting should use a certificate or a client secret to connect to an environment.</span></span> <span data-ttu-id="fb9d1-216">有效值为 *certificate* 和 *clientsecret*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-216">Valid values are *"certificate"* and *"clientsecret"*.</span></span> <span data-ttu-id="fb9d1-217">默认值为 *certificate*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-217">The default value is *"certificate"*.</span></span><p><span data-ttu-id="fb9d1-218">**注意：** 不能导入客户端密码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-218">**Note:** Client secrets can't be imported.</span></span></p> |
| <span data-ttu-id="fb9d1-219">IsEditable</span><span class="sxs-lookup"><span data-stu-id="fb9d1-219">IsEditable</span></span> | <span data-ttu-id="fb9d1-220">（可选）指定应用用户是否应该可以编辑连接设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-220">(Optional) Specify whether the app user should be able to edit the connection setting.</span></span> <span data-ttu-id="fb9d1-221">有效值为 *true* 和 *false*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-221">Valid values are *"true"* and *"false"*.</span></span> <span data-ttu-id="fb9d1-222">默认值为 *true*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-222">The default value is *"true"*.</span></span> |
| <span data-ttu-id="fb9d1-223">IsDefault</span><span class="sxs-lookup"><span data-stu-id="fb9d1-223">IsDefault</span></span> | <span data-ttu-id="fb9d1-224">（可选）指定连接是否为默认连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-224">(Optional) Specify whether the connection is the default connection.</span></span> <span data-ttu-id="fb9d1-225">打开应用时，将提前选中设置为默认连接的连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-225">A connection that is set as the default connection will automatically be preselected when the app is opened.</span></span> <span data-ttu-id="fb9d1-226">只能将一个连接设置为默认连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-226">Only one connection can be set as the default connection.</span></span> <span data-ttu-id="fb9d1-227">有效值为 *true* 和 *false*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-227">Valid values are *"true"* and *"false"*.</span></span> <span data-ttu-id="fb9d1-228">默认值为 *false*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-228">The default value is *"false"*.</span></span> |
| <span data-ttu-id="fb9d1-229">CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fb9d1-229">CertificateThumbprint</span></span> | <span data-ttu-id="fb9d1-230">（可选）对于 Windows 设备，您可以为连接指定证书指纹。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-230">(Optional) For Windows devices, you can specify the certificate thumbprint for the connection.</span></span> <span data-ttu-id="fb9d1-231">对于 Android 设备，则应用用户必须在首次使用连接时选择证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-231">For Android devices, the app user must select the certificate the first time that a connection is used.</span></span> |

<span data-ttu-id="fb9d1-232">以下示例显示一个有效连接设置文件，该文件中包含两个连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-232">The following example shows a valid connection settings file that contains two connections.</span></span> <span data-ttu-id="fb9d1-233">如您所见，连接列表（文件中的名称为 *ConnectionList*）是一个对象，该对象有一个将每个连接作为对象存储的阵列。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-233">As you can see, the connection list (named *"ConnectionList"* in the file) is an object that has an array that stores each connection as an object.</span></span> <span data-ttu-id="fb9d1-234">每个对象必须使用括号 ({}) 括起来并使用逗号分隔，而阵列则必须使用方括号 (\[\]) 括起来。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-234">Each object must be enclosed in braces ({}) and separated by commas, and the array must be enclosed in brackets (\[\]).</span></span>

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

<span data-ttu-id="fb9d1-235">可以将信息保存为 JSON 文件，或生成具有相同内容的 QR 代码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-235">You can either save the information as a JSON file or generate a QR code that has the same content.</span></span> <span data-ttu-id="fb9d1-236">如果将信息保存为文件，建议使用默认名称 *connections.json* 保存，尤其是将把其存储在每个移动设备上的默认位置中时。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-236">If you save the information as a file, we recommend that you save it by using the default name, *connections.json*, especially if you will store it in the default location on each mobile device.</span></span>

### <a name="save-the-connection-settings-file-on-each-device"></a><span data-ttu-id="fb9d1-237">将连接设置文件保存到每个设备上</span><span class="sxs-lookup"><span data-stu-id="fb9d1-237">Save the connection settings file on each device</span></span>

<span data-ttu-id="fb9d1-238">您通常使用设备管理工具或脚本将连接设置文件发放到您管理的每个设备上。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-238">Typically, you will use a device management tool or script to distribute the connection settings files to each device that you're managing.</span></span> <span data-ttu-id="fb9d1-239">如果在每个设备上保存连接设置文件时使用默认名称和位置，仓库应用将自动导入该文件，即使是在安装该应用后首次运行期间。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-239">If you use the default name and location when you save the connection settings file on each device, the warehouse app will automatically import it, even during the first run after the app is installed.</span></span> <span data-ttu-id="fb9d1-240">如果为该文件使用自定义名称或位置，应用用户必须在首次运行期间指定值。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-240">If you use a custom name or location for the file, the app user must specify the values during the first run.</span></span> <span data-ttu-id="fb9d1-241">但是，以后此应用将继续使用指定的名称和位置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-241">However, the app will continue to use the specified name and location afterward.</span></span>

<span data-ttu-id="fb9d1-242">每次启动此应用时，都将从连接设置的之前位置重新导入连接设置，以确定是否进行了任何更改。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-242">Every time that the app is started, it reimports the connection settings from their previous location to determine whether there have been any changes.</span></span> <span data-ttu-id="fb9d1-243">此应用将仅更新与连接设置文件中的连接同名的连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-243">The app will update only connections that have the same names as the connections in the connection settings file.</span></span> <span data-ttu-id="fb9d1-244">将不更新用户创建且使用其他名称的连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-244">User-created connections that use other names won't be updated.</span></span>

<span data-ttu-id="fb9d1-245">不能使用连接设置文件删除连接。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-245">You can't remove a connection by using the connection settings file.</span></span>

<span data-ttu-id="fb9d1-246">如前所述，默认文件名为 *connections.json*。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-246">As has been mentioned, the default file name is *connections.json*.</span></span> <span data-ttu-id="fb9d1-247">默认文件位置取决于使用的是 Windows 设备还是 Android 设备：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-247">The default file location depends on whether you're using a Windows device or an Android device:</span></span>

- <span data-ttu-id="fb9d1-248">**Windows：**`C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`</span><span class="sxs-lookup"><span data-stu-id="fb9d1-248">**Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`</span></span>
- <span data-ttu-id="fb9d1-249">**Android：**`Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`</span><span class="sxs-lookup"><span data-stu-id="fb9d1-249">**Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`</span></span>

<span data-ttu-id="fb9d1-250">通常在首次运行此应用后自动创建这些路径。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-250">Usually, the paths are automatically created after the first run of the app.</span></span> <span data-ttu-id="fb9d1-251">但是，如果必须在安装前将连接设置文件传输到设备，可以手动创建这些路径。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-251">However, you can manually create them if you must transfer the connection settings file to the device before installation.</span></span>

> [!NOTE]
> <span data-ttu-id="fb9d1-252">如果卸载了此应用，将删除默认路径及其内容。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-252">If the app is uninstalled, the default path and its contents are removed.</span></span>

### <a name="import-the-connection-settings"></a><span data-ttu-id="fb9d1-253">导入连接设置</span><span class="sxs-lookup"><span data-stu-id="fb9d1-253">Import the connection settings</span></span>

<span data-ttu-id="fb9d1-254">执行以下步骤从文件或 QR 代码导入连接设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-254">Follow these steps to import connection settings from a file or a QR code.</span></span>

1. <span data-ttu-id="fb9d1-255">在移动设备上打开仓库应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-255">Open the warehouse app on your mobile device.</span></span>
1. <span data-ttu-id="fb9d1-256">转至 **连接设置**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-256">Go to **Connection settings**.</span></span>
1. <span data-ttu-id="fb9d1-257">将 **使用演示模式** 选项设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-257">Set the **Use demo mode** option to _No_.</span></span>

    <span data-ttu-id="fb9d1-258">![使用演示模式选项](media/app-connect-app-demo-mode.png "使用演示模式选项")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-258">![Use demo mode option](media/app-connect-app-demo-mode.png "Use demo mode option")</span></span>

1. <span data-ttu-id="fb9d1-259">选择 **选择文件** 或 **扫描 QR 代码**，具体取决于要如何导入设置：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-259">Select **Select file** or **Scan QR code**, depending on how you want to import the settings:</span></span>

    - <span data-ttu-id="fb9d1-260">如果要从文件导入连接设置，并且保存该文件时使用的是默认名称和默认位置，应用可能已经找到了该文件。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-260">If you're importing the connection settings from a file, the app might already have found the file if the default name and the default location were used when it was saved.</span></span> <span data-ttu-id="fb9d1-261">否则，选择 **选择文件**，在本地设备上浏览找到该文件，然后选择该文件。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-261">Otherwise, select **Select file**, browse to the file on your local device, and select it.</span></span> <span data-ttu-id="fb9d1-262">如果选择自定义位置，应用将存储该文件，并在下次自动使用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-262">If you select a custom location, the app will store it and automatically use it the next time.</span></span>
    - <span data-ttu-id="fb9d1-263">如果要通过扫描 QR 代码导入连接设置，请选择 **扫描 QR 代码**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-263">If you're importing the connection settings by scanning a QR code, select **Scan QR code**.</span></span> <span data-ttu-id="fb9d1-264">应用将提示您提供使用设备摄像头所需权限。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-264">The app prompts you for permission to use the device's camera.</span></span> <span data-ttu-id="fb9d1-265">提供权限后，将启动摄像头，以便您将其用于扫描。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-265">After you give permission, the camera is started, so that you can use it for scanning.</span></span> <span data-ttu-id="fb9d1-266">您可能发现很难获得正确扫描，具体取决于设备摄像头的质量和 QR 代码的复杂程度。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-266">Depending on the quality of the device's camera and the complexity of the QR code, you might find it difficult to get a correct scan.</span></span> <span data-ttu-id="fb9d1-267">在这种情况下，请尝试通过为每个 QR 码仅生成一个连接来降低 QR 代码的复杂程度。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-267">In that case, try to reduce the complexity of the QR code by generating only one connection per QR code.</span></span> <span data-ttu-id="fb9d1-268">（现在，只能使用设备摄像头扫描 QR 代码。）</span><span class="sxs-lookup"><span data-stu-id="fb9d1-268">(Currently, you can use only the device's camera to scan the QR code.)</span></span>

    <span data-ttu-id="fb9d1-269">![导入连接设置](media/app-connect-app-select-file.png "导入连接设置")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-269">![Import connection settings](media/app-connect-app-select-file.png "Import connection settings")</span></span>

1. <span data-ttu-id="fb9d1-270">成功加载连接设置后，选择页面右上角的 **后退**（向左箭头）按钮。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-270">When the connection settings are successfully loaded, select the **Back** (left arrow) button in the upper-left corner of the page.</span></span>

    <span data-ttu-id="fb9d1-271">![已加载连接设置](media/app-connect-app-settings-loaded.png "已加载连接设置")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-271">![Connection settings loaded](media/app-connect-app-settings-loaded.png "Connection settings loaded")</span></span>

1. <span data-ttu-id="fb9d1-272">如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-272">If you're using an Android device and are using a certificate for authentication, the device prompts you to select the certificate.</span></span>

    <span data-ttu-id="fb9d1-273">![Android 设备上的选择证书提示](media/app-connect-app-choose-cert.png "Android 设备上的选择证书提示")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-273">![Choose certificate prompt on an Android device](media/app-connect-app-choose-cert.png "Choose certificate prompt on an Android device")</span></span>

1. <span data-ttu-id="fb9d1-274">此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-274">The app connects to your Supply Chain Management server and shows the sign-in page.</span></span>

    <span data-ttu-id="fb9d1-275">![登录页](media/app-connect-sign-in.png "登录页")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-275">![Sign-in page](media/app-connect-sign-in.png "Sign-in page")</span></span>

## <a name="manually-configure-the-application"></a><a name="config-manually"></a><span data-ttu-id="fb9d1-276">手动配置应用程序</span><span class="sxs-lookup"><span data-stu-id="fb9d1-276">Manually configure the application</span></span>

<span data-ttu-id="fb9d1-277">可以在设备上手动配置此应用，以便通过 Azure AD 应用程序连接到 Supply Chain Management 服务器。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-277">You can manually configure the app on the device so that it connects to the Supply Chain Management server through the Azure AD application.</span></span>

1. <span data-ttu-id="fb9d1-278">在移动设备上打开仓库应用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-278">Open the warehouse app on your mobile device.</span></span>
1. <span data-ttu-id="fb9d1-279">转至 **连接设置**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-279">Go to **Connection settings**.</span></span>
1. <span data-ttu-id="fb9d1-280">将 **使用演示模式** 选项设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-280">Set the **Use demo mode** option to _No_.</span></span>

    <span data-ttu-id="fb9d1-281">![演示模式已关闭](media/app-connect-app-select-file.png "演示模式已关闭")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-281">![Demo mode turned off](media/app-connect-app-select-file.png "Demo mode turned off")</span></span>

1. <span data-ttu-id="fb9d1-282">在 **选择连接** 字段中点击展开手动输入连接详细信息所需设置。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-282">Tap in the **Select connection** field to expand the settings that are required to manually enter the connection details.</span></span>

    <span data-ttu-id="fb9d1-283">![手动连接字段](media/app-connect-manual-connect.png "手动连接字段")</span><span class="sxs-lookup"><span data-stu-id="fb9d1-283">![Manual connection fields](media/app-connect-manual-connect.png "Manual connection fields")</span></span>

1. <span data-ttu-id="fb9d1-284">输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="fb9d1-284">Enter the following information:</span></span>

    - <span data-ttu-id="fb9d1-285">**使用客户端密码** – 将此选项设置为 _是_ 以使用客户端密码和 Supply Chain Management 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-285">**Use client secret** – Set this option to _Yes_ to use a client secret to authenticate with Supply Chain Management.</span></span> <span data-ttu-id="fb9d1-286">若要使用证书进行身份验证，请将其设置为 _否_。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-286">Set it to _No_ to use a certificate for authentication.</span></span> <span data-ttu-id="fb9d1-287">（有关详细信息，请参阅[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)。）</span><span class="sxs-lookup"><span data-stu-id="fb9d1-287">(For more information, see [Create a web service application in Azure Active Directory](#create-service).)</span></span>
    - <span data-ttu-id="fb9d1-288">**连接名称** – 输入新连接的名称。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-288">**Connection name** – Enter a name for the new connection.</span></span> <span data-ttu-id="fb9d1-289">下次打开连接设置时，将在 **选择连接** 字段中显示此名称。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-289">This name will appear in the **Select connection** field the next time that you open the connection settings.</span></span> <span data-ttu-id="fb9d1-290">您输入的名称必须唯一。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-290">The name that you enter must be unique.</span></span> <span data-ttu-id="fb9d1-291">（换句话说，如果在设备上存储了其他任何连接名称，该名称必须与这些名称不同。）</span><span class="sxs-lookup"><span data-stu-id="fb9d1-291">(In other words, it must differ from all other connection names that are stored on your device, if any other connection names are stored there.).</span></span>
    - <span data-ttu-id="fb9d1-292">**Active Directory 客户端 ID** – 输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-292">**Active directory client ID** – Enter the client ID that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="fb9d1-293">**Active Directory 客户端密码** – 仅当 **使用客户端密码** 选项设置为 _是_，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-293">**Active directory client secret** – This field is available only when the **Use client secret** option is set to _Yes_.</span></span> <span data-ttu-id="fb9d1-294">输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端密码。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-294">Enter the client secret that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="fb9d1-295">**Active Directory 证书指纹** – 仅当 **使用客户端密码** 选项设置为 _否_，此字段对 Windows 设备才可用。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-295">**Active directory certificate thumbprint** – This field is available for Windows devices only when the **Use client secret** option is set to _No_.</span></span> <span data-ttu-id="fb9d1-296">输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的证书指纹。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-296">Enter the certificate thumbprint that you made a note of while you were setting up Azure AD in the [Create a web service application in Azure Active Directory](#create-service) section.</span></span>
    - <span data-ttu-id="fb9d1-297">**Active Directory 资源** – 指定 Supply Chain Management 的根 URL。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-297">**Active directory resource** – Specify the root URL of Supply Chain Management.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fb9d1-298">请勿为此值使用反斜杠 (/)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-298">Don't end this value with a slash (/).</span></span>

    - <span data-ttu-id="fb9d1-299">**Active Directory 租户** – 输入与 Supply Chain Management 服务器一起使用的 Azure AD 租户。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-299">**Active directory tenant** – Enter the Azure AD tenant that you're using with the Supply Chain Management server.</span></span> <span data-ttu-id="fb9d1-300">此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-300">This value has the form `https://login.windows.net/<your-Azure-AD-tenant-ID>`.</span></span> <span data-ttu-id="fb9d1-301">下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-301">Here is an example: `https://login.windows.net/contosooperations.onmicrosoft.com`.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fb9d1-302">请勿为此值使用反斜杠 (/)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-302">Don't end this value with a slash (/).</span></span>

    - <span data-ttu-id="fb9d1-303">**公司** – 在希望应用程序连接到的 Supply Chain Management 中输入法人。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-303">**Company** – Enter the legal entity in Supply Chain Management that you want the application to connect to.</span></span>

1. <span data-ttu-id="fb9d1-304">选择页面右上角的 **保存** 按钮。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-304">Select the **Save** button in the upper-right corner of the page.</span></span>
1. <span data-ttu-id="fb9d1-305">如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-305">If you're using an Android device and are using a certificate for authentication, the device prompts you to select the certificate.</span></span>
1. <span data-ttu-id="fb9d1-306">此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-306">The app connects to your Supply Chain Management server and shows the sign-in page.</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="fb9d1-307">取消设备的访问权限</span><span class="sxs-lookup"><span data-stu-id="fb9d1-307">Remove access for a device</span></span>

<span data-ttu-id="fb9d1-308">如果设备丢失或被入侵，您必须取消设备对 Supply Chain Management 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-308">In the event of a lost or compromised device, you must remove access to Supply Chain Management for the device.</span></span> <span data-ttu-id="fb9d1-309">以下步骤介绍推荐的访问权限取消流程。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-309">The following steps describe the recommended process for removing access.</span></span>

1. <span data-ttu-id="fb9d1-310">转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-310">Go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="fb9d1-311">删除与要取消访问权限的设备对应的行。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-311">Delete the line that corresponds to the device that you want to remove access for.</span></span> <span data-ttu-id="fb9d1-312">记下用于所删除设备的客户端 ID，因为后面需要它。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-312">Make a note of the client ID that is used for the removed device, because you will need it later.</span></span>

    <span data-ttu-id="fb9d1-313">如果仅注册了一个客户端 ID，并且多个设备使用同一个客户端 ID，则必须将新连接设置推送到这些设备。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-313">If you've registered only one client ID, and multiple devices use the same client ID, you must push out new connection settings to those devices.</span></span> <span data-ttu-id="fb9d1-314">否则，它们将失去访问权限。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-314">Otherwise, they will lose access.</span></span>

1. <span data-ttu-id="fb9d1-315">登录 Azure 门户，地址为 [https://portal.azure.com](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-315">Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="fb9d1-316">在左侧导航窗格中，选择 **Active Directory**，然后确保位于正确目录中。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-316">In the left navigation pane, select **Active Directory**, and make sure that you're in the correct directory.</span></span>
1. <span data-ttu-id="fb9d1-317">在 **管理** 列表中，选择 **应用程序注册**，然后选择要配置的应用程序。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-317">In the **Manage** list, select **App registrations**, and then select the application to configure.</span></span> <span data-ttu-id="fb9d1-318">将显示 **设置** 页面，其中包含配置信息。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-318">The **Settings** page appears and shows configuration information.</span></span>
1. <span data-ttu-id="fb9d1-319">确保应用程序的客户端 ID 与您在步骤 2 中记下的客户端 ID 匹配。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-319">Make sure that the client ID of the application matches the client ID that you made a note of in step 2.</span></span>
1. <span data-ttu-id="fb9d1-320">在工具栏上，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-320">On the toolbar, select **Delete**.</span></span>
1. <span data-ttu-id="fb9d1-321">在出现的确认消息中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="fb9d1-321">In the confirmation message that appears, select **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]