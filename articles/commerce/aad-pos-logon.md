---
title: 为 POS 登录配置 Azure Active Directory 身份验证
description: 本主题说明如何将 Azure Active Directory 配置为 Microsoft Dynamics 365 Commerce 销售点中的身份验证方法。
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937450"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="ed223-103">为 POS 登录配置 Azure Active Directory 身份验证</span><span class="sxs-lookup"><span data-stu-id="ed223-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ed223-104">本主题说明如何将 Azure Active Directory (Azure AD) 配置为 Microsoft Dynamics 365 Commerce 销售点 (POS) 中的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="ed223-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="ed223-105">将 Dynamics 365 Commerce 与其他 Microsoft 云服务（如 Microsoft Azure、Microsoft 365 和 Microsoft Teams）一起使用的零售商通常希望使用 Azure AD 集中管理用户凭据，以跨各个应用程序实现安全、无缝的登录体验。</span><span class="sxs-lookup"><span data-stu-id="ed223-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="ed223-106">若要将 Azure AD 身份验证用于 Commerce POS，必须首先将 Azure AD 配置为 Commerce Headquarters 中的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="ed223-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="ed223-107">配置 POS 身份验证方法</span><span class="sxs-lookup"><span data-stu-id="ed223-107">Configure POS authentication method</span></span>

<span data-ttu-id="ed223-108">要在 Commerce headquarters 中配置 POS 身份验证方法，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ed223-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="ed223-109">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，选择要更改的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ed223-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="ed223-110">在 **功能** 快速选项卡的 **POS 人员登录** 部分，从 **登录身份验证方法** 下拉列表中选择所需的身份验证方法选项。</span><span class="sxs-lookup"><span data-stu-id="ed223-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="ed223-111">**登录身份验证方法** 有三个选项：</span><span class="sxs-lookup"><span data-stu-id="ed223-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="ed223-112">**个人 ID 和密码** - 此默认选项需要 POS 用户输入个人 ID 和密码来登录 POS 和访问经理替代功能。</span><span class="sxs-lookup"><span data-stu-id="ed223-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="ed223-113">**未采用单一登录的 Azure AD** - 此选项需要 POS 用户使用 Azure AD 凭据登录 POS 和访问经理替代功能。</span><span class="sxs-lookup"><span data-stu-id="ed223-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="ed223-114">刷新或重新打开 POS 客户端时，POS 用户必须提供 Azure AD 凭据才能再次登录。</span><span class="sxs-lookup"><span data-stu-id="ed223-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="ed223-115">**采用单一登录的 Azure AD** - 选择此选项后，POS 用户可以使用同一 Web 浏览器中其他 Web 应用程序正在使用的活动 Azure AD 凭据登录 Cloud POS (CPOS)，或使用登录到 Windows 的 Azure AD 凭据登录 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="ed223-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="ed223-116">使用这两种方法登录时都不需要在 POS 登录屏幕上输入 Azure AD 凭据。</span><span class="sxs-lookup"><span data-stu-id="ed223-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="ed223-117">但是，访问 POS 经理替代功能仍然需要使用 Azure AD 凭据登录。</span><span class="sxs-lookup"><span data-stu-id="ed223-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="ed223-118">转到 **Retail 和 Commerce > Retail 和 Commerce IT > 分配计划**，运行 **1070 (渠道配置)** 作业，将最新功能配置文件设置同步到 POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="ed223-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="ed223-119">**未采用单一登录的 Azure AD** 身份验证方法选项替换了 Commerce 版本 10.0.18 及更早版本中的 **Azure Active Directory** 选项。</span><span class="sxs-lookup"><span data-stu-id="ed223-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="ed223-120">Azure AD 身份验证需要有效的 Internet 连接，在 POS 处于离线状态时无法运行。</span><span class="sxs-lookup"><span data-stu-id="ed223-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="ed223-121">将 Azure AD 帐户与 POS 用户关联</span><span class="sxs-lookup"><span data-stu-id="ed223-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="ed223-122">要将 Azure AD 用作 POS 身份验证方法，必须将 Azure AD 帐户与 Commerce headquarters 中的 POS 用户关联。</span><span class="sxs-lookup"><span data-stu-id="ed223-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="ed223-123">要将 Azure AD 帐户与 Commerce headquarters 中的 POS 用户相关联，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ed223-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="ed223-124">转到 **Retail 和 Commerce > 员工 > 工作人员**，打开一个工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="ed223-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="ed223-125">在操作窗格上，选择 **Commerce** 选项卡，然后在 **外部标识** 下选择 **关联现有标识**。</span><span class="sxs-lookup"><span data-stu-id="ed223-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="ed223-126">在 **使用现有外部标识** 对话框中，选择 **使用电子邮件搜索**，输入 Azure AD 电子邮件地址，然后选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="ed223-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="ed223-127">选择返回的 Azure AD 帐户，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ed223-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="ed223-128">完成上述配置步骤后，将填写该工作人员详细信息页的 **Commerce** 选项卡中的 **别名**、**UPN** 和 **外部子标识** 字段。</span><span class="sxs-lookup"><span data-stu-id="ed223-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="ed223-129">您必须运行 **Retail 和 Commerce > Retail 和 Commerce IT > 分配计划** 中的 **1060 (人员)** 作业，来将最新的 POS 用户和 Azure AD 帐户数据同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="ed223-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="ed223-130">最佳做法是，在 Commerce headquarters 中更新工作人员信息（如密码、POS 权限、关联的 Azure AD 帐户或员工通讯簿）后，强烈建议运行 **1060 (人员)** 作业将最新的工作人员信息同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="ed223-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="ed223-131">然后，POS 客户端可以提取正确的数据来进行用户身份验证和授权检查。</span><span class="sxs-lookup"><span data-stu-id="ed223-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="ed223-132">使用 Azure AD 身份验证的 POS 锁定收银机和注销</span><span class="sxs-lookup"><span data-stu-id="ed223-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="ed223-133">将 POS 配置为使用 Azure AD 身份验证方法时，会发生以下情况：</span><span class="sxs-lookup"><span data-stu-id="ed223-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="ed223-134">**锁定收银机** 功能在 POS 应用程序中不可用。</span><span class="sxs-lookup"><span data-stu-id="ed223-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="ed223-135">**自动锁定** 功能与 **自动注销** 功能的行为相同。</span><span class="sxs-lookup"><span data-stu-id="ed223-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="ed223-136">如果 POS 用户选择 **注销**，下次 POS 启动时将要求该用户使用 Azure AD 凭据登录，无论是否启用了单一登录。</span><span class="sxs-lookup"><span data-stu-id="ed223-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="ed223-137">使用 Azure AD 身份验证的经理替代功能</span><span class="sxs-lookup"><span data-stu-id="ed223-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="ed223-138">当 POS 配置为使用 Azure AD 身份验证时，经理替代功能将打开一个对话框，提示输入经理用户的 Azure AD 凭据。</span><span class="sxs-lookup"><span data-stu-id="ed223-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="ed223-139">经理登录被批准后，将丢弃经理的 Azure AD 凭据，先前用户的 Azure AD 凭据将用于后续的 POS 操作。</span><span class="sxs-lookup"><span data-stu-id="ed223-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="ed223-140">在 Commerce 版本 10.0.18 和更早版本中，经理替代功能不支持 Azure AD。</span><span class="sxs-lookup"><span data-stu-id="ed223-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="ed223-141">即使将 POS 配置为使用 Azure AD 身份验证方法，也需要个人 ID 和密码。</span><span class="sxs-lookup"><span data-stu-id="ed223-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="ed223-142">在 Apple iOS 设备上通过 Safari Web 浏览器使用 CPOS 时，必须首先在 Safari 设置中关闭 **阻止弹出窗口**，这样经理替代功能才能使用 Azure AD 身份验证。</span><span class="sxs-lookup"><span data-stu-id="ed223-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="ed223-143">在共享设备上使用基于 Azure AD 的 POS 身份验证的最佳安全实践</span><span class="sxs-lookup"><span data-stu-id="ed223-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="ed223-144">很多零售商设置零售商店环境时采取的方式是多个用户需要从共享物理设备访问 POS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ed223-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="ed223-145">在这种情况下，虽然单一登录提供了方便、无缝的身份验证体验，但它也可能会造成安全漏洞：当前 POS 用户可能不会意识到另一个用户的凭据正被用于在 POS 中执行交易或操作。</span><span class="sxs-lookup"><span data-stu-id="ed223-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="ed223-146">在将 POS 配置为使用 Azure AD 身份验证方法之前，强烈建议查看您的安全策略和共享设备的登录设置，以确定最适合的选项。</span><span class="sxs-lookup"><span data-stu-id="ed223-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="ed223-147">如果您的零售环境使用共享帐户（例如，本地帐户）进行物理设备登录，则建议使用 **未采用单一登录的 Azure AD** 选项。</span><span class="sxs-lookup"><span data-stu-id="ed223-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="ed223-148">这样可以确保每个 POS 用户明确提供 Azure AD 凭据来登录 POS。</span><span class="sxs-lookup"><span data-stu-id="ed223-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="ed223-149">如果您的零售环境需要员工使用自己的 Azure AD 帐户登录 POS 及其托管物理设备，则建议使用 **采用单一登录的 Azure AD** 选项。</span><span class="sxs-lookup"><span data-stu-id="ed223-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed223-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="ed223-150">Additional resources</span></span>

[<span data-ttu-id="ed223-151">配置工作人员</span><span class="sxs-lookup"><span data-stu-id="ed223-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="ed223-152">创建零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="ed223-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="ed223-153">为 MPOS 和 Cloud POS 设置扩展登录功能</span><span class="sxs-lookup"><span data-stu-id="ed223-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="ed223-154">共享环境中 Cloud POS 的最佳安全实践</span><span class="sxs-lookup"><span data-stu-id="ed223-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
