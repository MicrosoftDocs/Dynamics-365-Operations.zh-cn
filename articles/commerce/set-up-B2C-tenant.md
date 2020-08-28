---
title: 在 Commerce 中设置 B2C 租户
description: 此主题介绍如何在 Dynamics 365 Commerce 中设置 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以执行用户站点身份验证。
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f31f8898358626f2b008826aa69694dc16742aa0
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677896"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="03fdc-103">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="03fdc-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03fdc-104">此主题介绍如何在 Dynamics 365 Commerce 中设置 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以执行用户站点身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="03fdc-105">概览</span><span class="sxs-lookup"><span data-stu-id="03fdc-105">Overview</span></span>

<span data-ttu-id="03fdc-106">Dynamics 365 Commerce 使用 Azure AD B2C 为用户凭据和身份验证流提供支持。</span><span class="sxs-lookup"><span data-stu-id="03fdc-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="03fdc-107">用户可以通过这些流注册、登录和重置密码。</span><span class="sxs-lookup"><span data-stu-id="03fdc-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="03fdc-108">Azure AD B2C 中存储敏感的用户身份验证信息，如用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="03fdc-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="03fdc-109">B2C 租户中的用户记录中将存储 B2C 本地帐户记录或 B2C 社交标识提供程序记录。</span><span class="sxs-lookup"><span data-stu-id="03fdc-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="03fdc-110">这些 B2C 记录将链接回 Commerce 环境中的客户记录。</span><span class="sxs-lookup"><span data-stu-id="03fdc-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="03fdc-111">在 Azure 门户中创建或链接到现有的 AAD B2C 租户</span><span class="sxs-lookup"><span data-stu-id="03fdc-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="03fdc-112">登录 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="03fdc-113">在 Azure 门户菜单中选择**创建资源**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="03fdc-114">请务必使用将与您的 Commerce 环境连接的订阅和目录。</span><span class="sxs-lookup"><span data-stu-id="03fdc-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![在 Azure 门户中创建资源](./media/B2CImage_1.png)

1. <span data-ttu-id="03fdc-116">转到**标识 \> Azure Active Directory B2C**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="03fdc-117">进入**创建新的 B2C 租户或链接至现有租户**页之后，使用下面一个最适合贵公司需要的选项：</span><span class="sxs-lookup"><span data-stu-id="03fdc-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="03fdc-118">**创建新的 Azure AD B2C 租户**：此选项用于创建新的 AAD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="03fdc-119">选择**创建新的 Azure AD B2C 租户**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="03fdc-120">在**组织名称**下，输入组织名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="03fdc-121">在**初始域名**下，输入初始域名。</span><span class="sxs-lookup"><span data-stu-id="03fdc-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="03fdc-122">对于**国家或地区**，选择国家或地区。</span><span class="sxs-lookup"><span data-stu-id="03fdc-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="03fdc-123">选择**创建**创建租户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-123">Select **Create** to create the tenant.</span></span>

     ![创建新的 Azure AD 租户](./media/B2CImage_2.png)

     - <span data-ttu-id="03fdc-125">**将现有 Azure AD B2C 租户链接至我的 Azure 订阅**：如果您已经有需要链接至的 Azure AD B2C 租户，请使用此选项。</span><span class="sxs-lookup"><span data-stu-id="03fdc-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="03fdc-126">选择**将现有 Azure AD B2C 租户链接至我的 Azure 订阅**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="03fdc-127">对于 **Azure AD B2C 租户**，选择相应 B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="03fdc-128">如果选择框中显示消息“未发现符合要求的 B2C 租户”，说明您还没有符合要求的 B2C 租户，需要新建一个。</span><span class="sxs-lookup"><span data-stu-id="03fdc-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="03fdc-129">对于**资源组**，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="03fdc-130">输入将包含该租户的资源组的**名称**，选择**资源组位置**，然后选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![将现有 Azure AD B2C 租户链接至 Azure 订阅](./media/B2CImage_3.png)

1. <span data-ttu-id="03fdc-132">创建新的 Azure AD B2C 目录（可能需要一些时间）之后，仪表板中将显示这个新目录的链接。</span><span class="sxs-lookup"><span data-stu-id="03fdc-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="03fdc-133">这个链接将把您带到“欢迎使用 Azure Active Directory B2C”页面。</span><span class="sxs-lookup"><span data-stu-id="03fdc-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![链接到新的 AAD 目录](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="03fdc-135">如果您在您的 Azure 帐户中有多个订阅，或者如果您已经设置了 B2C 租户但未链接到有效订阅，**疑难解答**横幅将引导您把该租户链接到订阅。</span><span class="sxs-lookup"><span data-stu-id="03fdc-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="03fdc-136">选择疑难解答消息，然后按照指示解决订阅问题。</span><span class="sxs-lookup"><span data-stu-id="03fdc-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="03fdc-137">下图显示一个 Azure AD B2C **疑难解答** 横幅示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![其中显示目录无有效订阅的警告](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="03fdc-139">创建 B2C 应用程序</span><span class="sxs-lookup"><span data-stu-id="03fdc-139">Create the B2C application</span></span>

<span data-ttu-id="03fdc-140">创建 B2C 租户之后，您将在该租户中创建一个 B2C 应用程序来与 Commerce 操作交互。</span><span class="sxs-lookup"><span data-stu-id="03fdc-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="03fdc-141">若要创建 B2C 应用程序，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-142">在 Azure 门户中，选择**应用程序(旧版)**，然后选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-142">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="03fdc-143">在**名称**下，输入所需 AAD B2C 应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="03fdc-144">在 **Web 应用/Web API** 下，为**包含 Web 应用/Web API** 选择**是**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="03fdc-145">为**允许隐式流**选择**是**（默认值）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="03fdc-146">在**回复 URL** 下，输入您的专用回复 URL。</span><span class="sxs-lookup"><span data-stu-id="03fdc-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="03fdc-147">查看下面的[回复 URL](#reply-urls) 在此处了解有关回复 URL 的信息及其格式化方法。</span><span class="sxs-lookup"><span data-stu-id="03fdc-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="03fdc-148">为**包含本地客户端**选择**否**（默认值）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="03fdc-149">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="03fdc-150">回复 URL</span><span class="sxs-lookup"><span data-stu-id="03fdc-150">Reply URLs</span></span>

<span data-ttu-id="03fdc-151">回复 URL 非常重要，因为当您的站点调用 Azure AD B2C 以对用户进行身份验证时，它们会提供返回域的允许列表。</span><span class="sxs-lookup"><span data-stu-id="03fdc-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="03fdc-152">这将允许把已通过身份验证的用户返回到其用于登录的域（您的站点域）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="03fdc-153">在 **Azure AD B2c - 应用程序 \> 新应用程序**屏幕的**回复 URL** 框中，需要为您的站点域（预配环境之后）和 Commerce 生成的 URL 分别添加单独的行。</span><span class="sxs-lookup"><span data-stu-id="03fdc-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="03fdc-154">这些 URL 必须始终使用有效的 URL 格式，并且只能是基 URL（结尾没有斜杠或路径）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="03fdc-155">然后，需要将字符串 ``/_msdyn365/authresp`` 附加到基 URL，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="03fdc-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="03fdc-156">``https://www.fabrikam.com/_msdyn365/authresp``（该域应该与电子商务域完全匹配。</span><span class="sxs-lookup"><span data-stu-id="03fdc-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="03fdc-157">如果有多个域，则需要为每个域添加此 URL。）</span><span class="sxs-lookup"><span data-stu-id="03fdc-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="03fdc-158">创建用户流策略</span><span class="sxs-lookup"><span data-stu-id="03fdc-158">Create user flow policies</span></span>

<span data-ttu-id="03fdc-159">用户流是 Azure AD B2C 用于提供安全登录，安全注册，编辑配置文件和忘记密码用户体验的策略。</span><span class="sxs-lookup"><span data-stu-id="03fdc-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="03fdc-160">Dynamics 365 Commerce 使用这些流执行策略操作来与 Azure AD B2C 租户交互。</span><span class="sxs-lookup"><span data-stu-id="03fdc-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="03fdc-161">当用户与这些策略交互时，将被重定向到 Azure AD B2C 租户以执行操作。</span><span class="sxs-lookup"><span data-stu-id="03fdc-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="03fdc-162">Azure AD B2C 提供三种基本的用户流类型：</span><span class="sxs-lookup"><span data-stu-id="03fdc-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="03fdc-163">注册和登录</span><span class="sxs-lookup"><span data-stu-id="03fdc-163">Sign up and sign in</span></span>
- <span data-ttu-id="03fdc-164">配置文件编辑</span><span class="sxs-lookup"><span data-stu-id="03fdc-164">Profile editing</span></span>
- <span data-ttu-id="03fdc-165">密码重置</span><span class="sxs-lookup"><span data-stu-id="03fdc-165">Password reset</span></span>

<span data-ttu-id="03fdc-166">可选择使用 Azure AD 提供的默认用户流，这将显示 AAD B2C 托管的页面。</span><span class="sxs-lookup"><span data-stu-id="03fdc-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="03fdc-167">也可以创建 HTML 页面以控制这些用户流体验的外观。</span><span class="sxs-lookup"><span data-stu-id="03fdc-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="03fdc-168">若要自定义 Dynamics 365 Commerce 的用户策略页面，请参阅[设置用户登录自定义页面](custom-pages-user-logins.md)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="03fdc-169">有关更多信息，请参阅[定义 Azure Active Directory B2C 中的用户体验界面](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="03fdc-170">创建注册和登录用户流策略</span><span class="sxs-lookup"><span data-stu-id="03fdc-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="03fdc-171">若要创建注册和登录用户流策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-172">在 Azure 门户的左侧导航窗格中，选择**用户流（策略）**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="03fdc-173">在 **Azure AD B2C – 用户流（策略）** 页面中，选择**新建用户流**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="03fdc-174">在**推荐**选项卡中，选择**注册和登录**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="03fdc-175">在**名称**下面，输入策略名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="03fdc-176">此名称在门户分配的前缀后显示（例如，“B2C_1_”）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="03fdc-177">在**标识提供程序**下，选中相应复选框。</span><span class="sxs-lookup"><span data-stu-id="03fdc-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="03fdc-178">在**多重身份验证**下，选择适合贵公司的选项。</span><span class="sxs-lookup"><span data-stu-id="03fdc-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="03fdc-179">在**用户特性和声明**下，根据需要选择用于收集特性或返回声明的选项。</span><span class="sxs-lookup"><span data-stu-id="03fdc-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="03fdc-180">Commerce 需要以下默认选项：</span><span class="sxs-lookup"><span data-stu-id="03fdc-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="03fdc-181">**收集特性**</span><span class="sxs-lookup"><span data-stu-id="03fdc-181">**Collect  attribute**</span></span> | <span data-ttu-id="03fdc-182">**返回声明**</span><span class="sxs-lookup"><span data-stu-id="03fdc-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="03fdc-183">电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="03fdc-183">Email Address</span></span>          | <span data-ttu-id="03fdc-184">电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="03fdc-184">Email Addresses</span></span>   |
    | <span data-ttu-id="03fdc-185">给定名称</span><span class="sxs-lookup"><span data-stu-id="03fdc-185">Given Name</span></span>             | <span data-ttu-id="03fdc-186">给定名称</span><span class="sxs-lookup"><span data-stu-id="03fdc-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="03fdc-187">标识提供方</span><span class="sxs-lookup"><span data-stu-id="03fdc-187">Identity Provider</span></span> |
    | <span data-ttu-id="03fdc-188">姓</span><span class="sxs-lookup"><span data-stu-id="03fdc-188">Surname</span></span>                | <span data-ttu-id="03fdc-189">姓</span><span class="sxs-lookup"><span data-stu-id="03fdc-189">Surname</span></span>           |
    |                        | <span data-ttu-id="03fdc-190">用户的对象 ID</span><span class="sxs-lookup"><span data-stu-id="03fdc-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="03fdc-191">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-191">Select **Create**.</span></span>

<span data-ttu-id="03fdc-192">下图是 Azure AD B2C 注册和登录用户流的一个示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![注册和登录策略设置](./media/B2CImage_11.png)

<span data-ttu-id="03fdc-194">下图显示 Azure AD B2C 注册和登录用户流中的**运行用户流**选项。</span><span class="sxs-lookup"><span data-stu-id="03fdc-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![策略流中的“运行用户流”选项](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="03fdc-196">创建配置文件编辑用户流策略</span><span class="sxs-lookup"><span data-stu-id="03fdc-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="03fdc-197">若要创建配置文件编辑用户流策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-198">在 Azure 门户的左侧导航窗格中，选择**用户流（策略）**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="03fdc-199">在 **Azure AD B2C – 用户流（策略）** 页面中，选择**新建用户流**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="03fdc-200">在**推荐**选项卡中，选择**配置文件编辑**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="03fdc-201">在**名称**下，输入配置文件编辑用户流。</span><span class="sxs-lookup"><span data-stu-id="03fdc-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="03fdc-202">此名称在门户分配的前缀后显示（例如，“B2C_1_”）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="03fdc-203">在**标识提供程序**下，选择**本地帐户登录**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="03fdc-204">在**用户属性**下，选中以下复选框：</span><span class="sxs-lookup"><span data-stu-id="03fdc-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="03fdc-205">**电子邮件地址**（仅限**返回声明**）</span><span class="sxs-lookup"><span data-stu-id="03fdc-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="03fdc-206">**给定名称**（**收集特性**和**返回声明**）</span><span class="sxs-lookup"><span data-stu-id="03fdc-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="03fdc-207">**标识提供程序**（仅限**返回声明**）</span><span class="sxs-lookup"><span data-stu-id="03fdc-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="03fdc-208">**姓**（**收集特性**和**返回声明**）</span><span class="sxs-lookup"><span data-stu-id="03fdc-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="03fdc-209">**用户的对象 ID**（仅限**返回声明**）</span><span class="sxs-lookup"><span data-stu-id="03fdc-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="03fdc-210">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-210">Select **Create**.</span></span>

<span data-ttu-id="03fdc-211">下图显示 Azure AD B2C 配置文件编辑用户流的一个示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![创建配置文件编辑用户流](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="03fdc-213">创建密码重置用户流策略</span><span class="sxs-lookup"><span data-stu-id="03fdc-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="03fdc-214">若要创建密码重置用户流策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-215">在 Azure 门户的左侧导航窗格中，选择**用户流（策略）**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="03fdc-216">在 **Azure AD B2C – 用户流（策略）** 页面中，选择**新建用户流**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="03fdc-217">在**推荐**选项卡中，选择**密码重置**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="03fdc-218">在**名称**下，输入密码重置用户流的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="03fdc-219">在**标识提供程序**下，选择**使用电子邮件地址重置密码**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="03fdc-220">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-220">Select **Create**.</span></span>
1. <span data-ttu-id="03fdc-221">在**应用程序声明**下，选中以下复选框：</span><span class="sxs-lookup"><span data-stu-id="03fdc-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="03fdc-222">**电子邮件地址**</span><span class="sxs-lookup"><span data-stu-id="03fdc-222">**Email addresses**</span></span>
    - <span data-ttu-id="03fdc-223">**给定名称**</span><span class="sxs-lookup"><span data-stu-id="03fdc-223">**Given Name**</span></span>
    - <span data-ttu-id="03fdc-224">**姓**</span><span class="sxs-lookup"><span data-stu-id="03fdc-224">**Surname**</span></span>
    - <span data-ttu-id="03fdc-225">**用户的对象 ID**</span><span class="sxs-lookup"><span data-stu-id="03fdc-225">**User's Object ID**</span></span>
1. <span data-ttu-id="03fdc-226">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-226">Select **Create**.</span></span>

<span data-ttu-id="03fdc-227">下图显示在 Azure AD B2C 密码重置用户流中何处设置**使用邮件地址重置密码**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![在密码重置策略中设置“使用邮件地址重置密码”](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="03fdc-229">添加社交标识提供程序（可选）</span><span class="sxs-lookup"><span data-stu-id="03fdc-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="03fdc-230">社交标识提供程序让用户可以使用自己的社交帐户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="03fdc-231">添加社交标识提供程序身份验证在 Dynamics 365 Commerce 中为可选操作。</span><span class="sxs-lookup"><span data-stu-id="03fdc-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="03fdc-232">如果不添加社交标识提供程序身份验证，默认 Azure AD B2C 配置文件将充当您的用户群的主配置文件。</span><span class="sxs-lookup"><span data-stu-id="03fdc-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="03fdc-233">用户将选择自己的用户名（其首选电子邮件地址）并设置密码。</span><span class="sxs-lookup"><span data-stu-id="03fdc-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="03fdc-234">Azure AD B2C 将直接对用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="03fdc-235">如果已添加了社交标识提供程序身份验证，并且用户选择了提供的一个社交标识提供程序，将在 Azure AD B2C 租户中创建一个条目。</span><span class="sxs-lookup"><span data-stu-id="03fdc-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="03fdc-236">然后，Azure AD B2C 将使用该社交标识提供程序对用户的凭据进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="03fdc-237">标识提供程序登录将在 B2C 租户中创建一个记录，但是其格式与本地帐户的格式不同，因为其将调用外部社交标识提供程序引用来进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="03fdc-238">用户可以在多个社交标识提供程序中使用同一个电子邮件地址，这意味着用于身份验证的电子邮件用户名可能对租户不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="03fdc-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="03fdc-239">Azure AD B2C 将仅强制在本地 B2C 帐户中具有唯一电子邮件地址的用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="03fdc-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="03fdc-240">必须先转到标识提供程序的门户并按照 Azure AD B2C 文档中的指示设置标识提供程序应用程序，才能添加用于身份验证的社交标识提供程序。</span><span class="sxs-lookup"><span data-stu-id="03fdc-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="03fdc-241">下面提供了文档的链接列表。</span><span class="sxs-lookup"><span data-stu-id="03fdc-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="03fdc-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="03fdc-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="03fdc-243">Azure AD（单个租户）</span><span class="sxs-lookup"><span data-stu-id="03fdc-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="03fdc-244">Microsoft 帐户</span><span class="sxs-lookup"><span data-stu-id="03fdc-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="03fdc-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="03fdc-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="03fdc-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="03fdc-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="03fdc-247">Google</span><span class="sxs-lookup"><span data-stu-id="03fdc-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="03fdc-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="03fdc-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="03fdc-249">OpenID 连接</span><span class="sxs-lookup"><span data-stu-id="03fdc-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="03fdc-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="03fdc-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="03fdc-251">添加和设置社交标识提供程序</span><span class="sxs-lookup"><span data-stu-id="03fdc-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="03fdc-252">若要添加和设置社交标识提供程序，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="03fdc-253">在 Azure 门户中，导航到**标识提供程序**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="03fdc-254">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-254">Select **Add**.</span></span> <span data-ttu-id="03fdc-255">将显示**添加标识提供程序**屏幕。</span><span class="sxs-lookup"><span data-stu-id="03fdc-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="03fdc-256">在**名称**下，输入要在登录屏幕中对用户显示的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="03fdc-257">在**标识提供程序类型**下，从列表中选择标识提供程序。</span><span class="sxs-lookup"><span data-stu-id="03fdc-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="03fdc-258">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-258">Select **OK**.</span></span>
1. <span data-ttu-id="03fdc-259">选择**设置此标识提供程序**以访问**设置社交标识提供程序**屏幕。</span><span class="sxs-lookup"><span data-stu-id="03fdc-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="03fdc-260">在**客户端 ID** 下，输入从标识提供程序应用程序设置中获取的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="03fdc-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="03fdc-261">在**客户端密钥**下，输入从标识提供程序应用程序设置中获取的客户端密钥。</span><span class="sxs-lookup"><span data-stu-id="03fdc-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="03fdc-262">附加登录注册策略的用户流：</span><span class="sxs-lookup"><span data-stu-id="03fdc-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="03fdc-263">转到 **Azure AD B2C – 用户流（策略）\> {您的登录注册策略} \> 标识提供程序**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="03fdc-264">若要附加登录/注册用户流策略，请选择您已经为帐户设置的每个标识提供程序。</span><span class="sxs-lookup"><span data-stu-id="03fdc-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="03fdc-265">若要对其进行测试，请为每个标识提供程序选择**运行用户流**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="03fdc-266">一个新选项卡将显示登录页，其中显示新标识提供程序选择框。</span><span class="sxs-lookup"><span data-stu-id="03fdc-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="03fdc-267">下图显示 Azure AD B2C 中**添加标识提供程序**和**设置社交标识提供程序**屏幕的示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![向应用程序添加社交标识提供程序](./media/B2CImage_14.png)

<span data-ttu-id="03fdc-269">下图显示如何在 Azure AD B2C **标识提供程序**页中选择标识提供程序的示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![选择要为策略启用的每个社交标识提供程序](./media/B2CImage_16.png)

<span data-ttu-id="03fdc-271">下图显示默认登录屏幕的示例，该屏幕中显示了一个社交标识提供程序登录按钮。</span><span class="sxs-lookup"><span data-stu-id="03fdc-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![其中显示社交标识提供程序登录按钮的示例默认登录屏幕](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="03fdc-273">使用新的 Azure AD B2C 信息更新 Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="03fdc-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="03fdc-274">完成了上面的 Azure AD B2C 预配步骤之后，必须在 Dynamics 365 Commerce 环境中注册 Azure AD B2C 应用程序。</span><span class="sxs-lookup"><span data-stu-id="03fdc-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="03fdc-275">若要使用新的 Azure AD B2C 信息更新 Headquarters，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-276">在 Commerce 中，转到 **Commerce 共享参数**，然后选择左菜单中的**标识提供程序**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="03fdc-277">在**标识提供程序**下，执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="03fdc-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="03fdc-278">在**颁发者**框中，输入标识提供程序颁发者 URL。</span><span class="sxs-lookup"><span data-stu-id="03fdc-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="03fdc-279">若要查找颁发者 URL，请参阅下面的[获取颁发者 URL](#obtain-issuer-url)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="03fdc-280">在**名称**框中，输入颁发者记录的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="03fdc-281">在**类型**框中，输入 **Azure AD B2C (id_token)**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="03fdc-282">选择上面的 B2C 标识提供程序项之后，在**回复方**下执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="03fdc-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="03fdc-283">在**客户端 ID** 框中，输入您的 B2C 应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="03fdc-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="03fdc-284">可在您的 B2C 应用程序的属性页**应用程序 ID** 框中找到此信息。</span><span class="sxs-lookup"><span data-stu-id="03fdc-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="03fdc-285">在**类型**框中，输入**公开**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="03fdc-286">在**用户类型**框中，输入**客户**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="03fdc-287">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="03fdc-288">在 Commerce 搜索框中，搜索**配送计划**</span><span class="sxs-lookup"><span data-stu-id="03fdc-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="03fdc-289">在**配送计划**页的左导航菜单中，选择作业 **1110 全局配置**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="03fdc-290">在操作窗格上，选择**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="03fdc-291">获取颁发者 URL</span><span class="sxs-lookup"><span data-stu-id="03fdc-291">Obtain issuer URL</span></span>

<span data-ttu-id="03fdc-292">若要获取标识提供程序颁发者 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-293">使用您的 B2C 租户和策略创建以下格式的元数据地址 URL：``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="03fdc-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="03fdc-294">示例：``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``。</span><span class="sxs-lookup"><span data-stu-id="03fdc-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="03fdc-295">在浏览器地址栏中输入该元数据地址 URL。</span><span class="sxs-lookup"><span data-stu-id="03fdc-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="03fdc-296">在元数据中，复制标识提供程序颁发者 URL（**颁发者**的值）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="03fdc-297">示例：``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。</span><span class="sxs-lookup"><span data-stu-id="03fdc-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="03fdc-298">在 Commerce 站点构建器中配置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="03fdc-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="03fdc-299">Azure AD B2C 租户设置完毕之后，必须在 Commerce 站点构建器中配置该 B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="03fdc-300">配置步骤包括从 Azure 门户收集 B2C 应用程序信息，在站点构建器中输入 B2C 应用程序信息，然后将该 B2C 应用程序与您的站点和渠道关联。</span><span class="sxs-lookup"><span data-stu-id="03fdc-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="03fdc-301">收集所需的应用程序信息</span><span class="sxs-lookup"><span data-stu-id="03fdc-301">Collect the required application information</span></span>

<span data-ttu-id="03fdc-302">若要收集所需的应用程序信息，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-303">在 Azure 门户中，转到**主页\> Azure AD B2C - 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="03fdc-304">选择您的应用程序，然后在左侧导航窗格中选择**属性**获取应用程序详细信息。</span><span class="sxs-lookup"><span data-stu-id="03fdc-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="03fdc-305">从**应用程序 ID** 框收集在您的 B2C 租户中创建的 B2C 应用程序的应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="03fdc-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="03fdc-306">稍后将在站点构建器中把此信息作为**客户端 GUID** 输入。</span><span class="sxs-lookup"><span data-stu-id="03fdc-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="03fdc-307">在**回复 URL** 下，收集回复 URL。</span><span class="sxs-lookup"><span data-stu-id="03fdc-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="03fdc-308">转到**主页 \> Azure AD B2C – 用户流（策略）**，然后收集每个用户流策略的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="03fdc-309">下图显示 **Azure AD B2C - 应用程序**页的示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![在租户内导航到“B2C 应用程序”](./media/B2CImage_19.png)

<span data-ttu-id="03fdc-311">下图显示 Azure AD B2C 中一个应用程序**属性**页的示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![从 B2C 应用程序的属性复制应用程序 ID](./media/B2CImage_21.png)

<span data-ttu-id="03fdc-313">下图显示 **Azure AD B2C – 用户流（策略）** 页中用户流策略的一个示例。</span><span class="sxs-lookup"><span data-stu-id="03fdc-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![收集各 B2C 策略流的名称](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="03fdc-315">在 Commerce 中输入您的 AAD B2C 租户应用程序信息</span><span class="sxs-lookup"><span data-stu-id="03fdc-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="03fdc-316">必须在 Commerce 站点构建器中输入 Azure AD B2C 租户的详细信息，才能将 B2C 租户与站点关联。</span><span class="sxs-lookup"><span data-stu-id="03fdc-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="03fdc-317">若要将您的 AAD B2C 租户应用程序信息添加到 Commerce 中，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-318">以管理员身份登录您的环境的 Commerce 站点构建器。</span><span class="sxs-lookup"><span data-stu-id="03fdc-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="03fdc-319">在左侧导航窗格中，选择**租户设置**将其展开。</span><span class="sxs-lookup"><span data-stu-id="03fdc-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="03fdc-320">在**租户设置**下，选择 **B2C 设置**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="03fdc-321">在主窗口中 **B2C 应用程序**旁边，选择**管理**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="03fdc-322">（如果“B2C 应用程序”列表中显示您的租户，说明已经有管理员添加了此租户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="03fdc-323">请验证下面步骤 6 中的项是否与您的 B2C 应用程序匹配。）</span><span class="sxs-lookup"><span data-stu-id="03fdc-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="03fdc-324">选择**添加 B2C 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="03fdc-325">使用您的 B2c 租户和应用程序中的值在显示的窗体中输入下面的必需项。</span><span class="sxs-lookup"><span data-stu-id="03fdc-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="03fdc-326">可以将非必填字段（不带星号的字段）保留为空。</span><span class="sxs-lookup"><span data-stu-id="03fdc-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="03fdc-327">**应用程序名称**：您的 B2C 应用程序的名称，例如，“Fabrikam B2C”。</span><span class="sxs-lookup"><span data-stu-id="03fdc-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="03fdc-328">**租户名称**：您的 B2C 租户的名称（例如，如果 B2C 租户的域显示为“fabrikam.onmicrosoft.com”，则使用“fabrikam”）。</span><span class="sxs-lookup"><span data-stu-id="03fdc-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="03fdc-329">**忘记密码策略 ID**：忘记密码用户流策略 ID，例如“B2C_1_PasswordReset”。</span><span class="sxs-lookup"><span data-stu-id="03fdc-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="03fdc-330">**注册登录策略 ID**：注册和登录用户流策略 ID，例如“B2C_1_signup_signin”。</span><span class="sxs-lookup"><span data-stu-id="03fdc-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="03fdc-331">**客户端 GUID**：B2C 应用程序 ID，例如“22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”。</span><span class="sxs-lookup"><span data-stu-id="03fdc-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="03fdc-332">**编辑配置文件策略 ID**：概要文件编辑用户流策略 ID，例如“B2C_1A_ProfileEdit”。</span><span class="sxs-lookup"><span data-stu-id="03fdc-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="03fdc-333">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-333">Select **OK**.</span></span> <span data-ttu-id="03fdc-334">现在应该可以在列表中看到显示您的 B2C 应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="03fdc-335">选择**保存**以保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="03fdc-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="03fdc-336">将 B2C 应用程序关联到站点和渠道</span><span class="sxs-lookup"><span data-stu-id="03fdc-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="03fdc-337">如果您的站点已经与一个 B2C 应用程序关联，则切换到其他 B2C 应用程序将去除为已经登录该环境的用户建立的当前引用。</span><span class="sxs-lookup"><span data-stu-id="03fdc-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="03fdc-338">如果更改，与当前分配的 B2C 应用程序关联的所有凭据对用户均不可用。</span><span class="sxs-lookup"><span data-stu-id="03fdc-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="03fdc-339">仅当首次设置渠道的 B2C 应用程序时，或计划让用户使用此渠道的新凭据重新注册新 B2C 应用程序时，才更新此 B2C 应用程序。</span><span class="sxs-lookup"><span data-stu-id="03fdc-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="03fdc-340">将渠道关联到 B2C 应用程序时请小心谨慎，并为应用程序指定明确的名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="03fdc-341">如果不在下面的步骤中将渠道关联到 B2C 应用程序，将把登录您的站点的该渠道的用户输入到 B2C 应用程序中，并显示为 B2C 应用程序的**租户设置 \> B2C 设置**列表中的**默认值**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="03fdc-342">若要将 B2C 应用程序关联到站点和渠道，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="03fdc-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="03fdc-343">在 Commerce 网站构建器中导航到您的网站。</span><span class="sxs-lookup"><span data-stu-id="03fdc-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="03fdc-344">在左侧导航窗格中，选择**站点设置**将其展开。</span><span class="sxs-lookup"><span data-stu-id="03fdc-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="03fdc-345">在**站点设置**下，选择**渠道**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="03fdc-346">在主窗口中的**渠道**下，选择您的渠道。</span><span class="sxs-lookup"><span data-stu-id="03fdc-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="03fdc-347">在右侧渠道属性窗格中，从**选择 B2C 应用程序**下拉菜单中选择您的 B2C 应用程序名称。</span><span class="sxs-lookup"><span data-stu-id="03fdc-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="03fdc-348">选择**关闭**，然后选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="03fdc-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="03fdc-349">附加 B2C 信息</span><span class="sxs-lookup"><span data-stu-id="03fdc-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="03fdc-350">客户迁移</span><span class="sxs-lookup"><span data-stu-id="03fdc-350">Customer migration</span></span>

<span data-ttu-id="03fdc-351">如果考虑迁移早期标识提供程序平台中的客户记录，请与 Dynamics 365 Commerce 团队合作检查您的客户迁移需求。</span><span class="sxs-lookup"><span data-stu-id="03fdc-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="03fdc-352">有关客户迁移的更多 Azure AD B2C 文档，请参阅[将用户迁移到 Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="03fdc-353">自定义策略</span><span class="sxs-lookup"><span data-stu-id="03fdc-353">Custom policies</span></span>

<span data-ttu-id="03fdc-354">有关自定义非 B2C 标准策略提供的 Azure AD B2C 交互和策略流的更多信息，请参阅[在 Azure Active Directory B2C 中自定义策略](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom)。</span><span class="sxs-lookup"><span data-stu-id="03fdc-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="03fdc-355">第二管理员</span><span class="sxs-lookup"><span data-stu-id="03fdc-355">Secondary admin</span></span>

<span data-ttu-id="03fdc-356">可以在 B2C 租户的**用户**部分中添加可选的第二管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="03fdc-357">这可以是直接帐户或一般帐户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="03fdc-358">如果需要在团队资源之间共享某个帐户，也可以创建公共帐户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="03fdc-359">由于 Azure AD B2C 中存储的数据为敏感数据，所以应该按照贵公司的安全实践密切监控公共帐户。</span><span class="sxs-lookup"><span data-stu-id="03fdc-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03fdc-360">其他资源</span><span class="sxs-lookup"><span data-stu-id="03fdc-360">Additional resources</span></span>

[<span data-ttu-id="03fdc-361">配置域名</span><span class="sxs-lookup"><span data-stu-id="03fdc-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="03fdc-362">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="03fdc-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="03fdc-363">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="03fdc-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="03fdc-364">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="03fdc-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="03fdc-365">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="03fdc-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="03fdc-366">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="03fdc-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="03fdc-367">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="03fdc-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="03fdc-368">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="03fdc-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="03fdc-369">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="03fdc-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="03fdc-370">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="03fdc-370">Enable location-based store detection</span></span>](enable-store-detection.md)
