---
title: 预配 Commerce 预览环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 预览环境。
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934740"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="206d7-103">预配 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="206d7-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="206d7-104">本主题说明如何预配 Microsoft Dynamics 365 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="206d7-105">建议您首先至少快速浏览整个主题，以大致了解流程涉及的内容和本主题包含的内容。</span><span class="sxs-lookup"><span data-stu-id="206d7-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="206d7-106">如果您尚未获得 Dynamics 365 Commerce 预览的访问权限，可以从 [Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)申请预览访问权限。</span><span class="sxs-lookup"><span data-stu-id="206d7-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="206d7-107">概览</span><span class="sxs-lookup"><span data-stu-id="206d7-107">Overview</span></span>

<span data-ttu-id="206d7-108">要成功预配 Commerce 预览环境，您必须创建一个具有特定产品名称和类型的项目。</span><span class="sxs-lookup"><span data-stu-id="206d7-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="206d7-109">此环境和 Retail Cloud Scale Unit (RCSU) 还具有某些特定参数，以后在预配电子商务时必须使用这些参数。</span><span class="sxs-lookup"><span data-stu-id="206d7-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="206d7-110">本主题中的说明介绍必须完成的所有必需步骤以及必须使用的参数。</span><span class="sxs-lookup"><span data-stu-id="206d7-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="206d7-111">成功预配 Commerce 预览环境后，还必须完成一些预配后步骤来准备它。</span><span class="sxs-lookup"><span data-stu-id="206d7-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="206d7-112">其中一些步骤可选，具体取决于要评估系统的哪些方面。</span><span class="sxs-lookup"><span data-stu-id="206d7-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="206d7-113">您可以在以后随时完成可选步骤。</span><span class="sxs-lookup"><span data-stu-id="206d7-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="206d7-114">有关在预配后如何预配 Commerce 预览环境的信息，请参阅[预配 Commerce 预览环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="206d7-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="206d7-115">有关为 Commerce 预览环境预配可选功能的信息，请参阅[为 Commerce 预览环境预配可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="206d7-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="206d7-116">如果对预配步骤有任何疑问或遇到了任何问题，请通过 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)告知 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="206d7-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="206d7-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="206d7-117">Prerequisites</span></span>

<span data-ttu-id="206d7-118">必须先满足以下先决条件，才能预配 Commerce 预览环境：</span><span class="sxs-lookup"><span data-stu-id="206d7-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="206d7-119">您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。</span><span class="sxs-lookup"><span data-stu-id="206d7-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="206d7-120">您已获准加入 Dynamics 365 Commerce 预览计划。</span><span class="sxs-lookup"><span data-stu-id="206d7-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="206d7-121">您拥有足够权限，可以为**潜在售前支持**或**迁移，创建解决方案，了解**创建项目。</span><span class="sxs-lookup"><span data-stu-id="206d7-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="206d7-122">您是我们将为其预配环境的项目的**环境管理员**或**项目负责人**角色的成员。</span><span class="sxs-lookup"><span data-stu-id="206d7-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="206d7-123">您有 Microsoft Azure 订阅的管理员访问权限，或您与可以代表您完成需要管理员权限的两步的订阅管理员有联系。</span><span class="sxs-lookup"><span data-stu-id="206d7-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="206d7-124">您有可用的 Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="206d7-125">您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="206d7-126">您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="206d7-127">（此安全组可以与电子商务系统管理员组相同。）</span><span class="sxs-lookup"><span data-stu-id="206d7-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="206d7-128">查找您的 Azure AD 租户 ID</span><span class="sxs-lookup"><span data-stu-id="206d7-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="206d7-129">您的 Azure AD 租户 ID 是一个类似于以下示例的全局唯一标识符 (GUID)：**72f988bf-86f1-41af-91ab-2d7cd011db47**。</span><span class="sxs-lookup"><span data-stu-id="206d7-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="206d7-130">使用 Azure 门户找到您的 Azure AD 租户 ID</span><span class="sxs-lookup"><span data-stu-id="206d7-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="206d7-131">登录 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="206d7-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="206d7-132">确保选择了正确的目录。</span><span class="sxs-lookup"><span data-stu-id="206d7-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="206d7-133">在左侧菜单中，选择 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="206d7-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="206d7-134">在**管理**下，选择**属性**。</span><span class="sxs-lookup"><span data-stu-id="206d7-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="206d7-135">您的 Azure AD 租户 ID 将出现在**目录 ID** 下。</span><span class="sxs-lookup"><span data-stu-id="206d7-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="206d7-136">使用 OpenID Connect 元数据查找您的 Azure AD 租户 ID</span><span class="sxs-lookup"><span data-stu-id="206d7-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="206d7-137">通过将 **\{YOUR\_DOMAIN\}** 替换为您的域（例如 `microsoft.com`）创建 OpenID URL。</span><span class="sxs-lookup"><span data-stu-id="206d7-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="206d7-138">例如，`https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` 会变成 `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`。</span><span class="sxs-lookup"><span data-stu-id="206d7-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="206d7-139">转到包含您的域的 OpenID URL。</span><span class="sxs-lookup"><span data-stu-id="206d7-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="206d7-140">您可以在多个属性值中找到您的 Azure AD 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="206d7-141">找到 **authorization\_endpoint**，并提取紧跟 `login.microsoftonline.com/` 出现的 GUID。</span><span class="sxs-lookup"><span data-stu-id="206d7-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="206d7-142">查找您的 Azure AD 安全组 ID</span><span class="sxs-lookup"><span data-stu-id="206d7-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="206d7-143">您的 Azure AD安全组的 ID 是一个类似于以下示例的 GUID：**436ea7f5-ee6c-40c1-9f08-825c5811066a**。</span><span class="sxs-lookup"><span data-stu-id="206d7-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="206d7-144">此过程假定您是尝试查找其 ID 的组的成员。</span><span class="sxs-lookup"><span data-stu-id="206d7-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="206d7-145">打开 [Graph 资源管理器](https://developer.microsoft.com/graph/graph-explorer#)。</span><span class="sxs-lookup"><span data-stu-id="206d7-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="206d7-146">选择**通过 Microsoft 登录**，然后使用您的凭据登录。</span><span class="sxs-lookup"><span data-stu-id="206d7-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="206d7-147">在左侧，选择**显示更多示例**。</span><span class="sxs-lookup"><span data-stu-id="206d7-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="206d7-148">从右窗格中，启用**组**。</span><span class="sxs-lookup"><span data-stu-id="206d7-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="206d7-149">关闭右窗格。</span><span class="sxs-lookup"><span data-stu-id="206d7-149">Close the right pane.</span></span>
1. <span data-ttu-id="206d7-150">选择**我属于的所有组**。</span><span class="sxs-lookup"><span data-stu-id="206d7-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="206d7-151">在**响应预览**字段中，找到您的组。</span><span class="sxs-lookup"><span data-stu-id="206d7-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="206d7-152">安全组 ID 将出现在 **ID** 属性下。</span><span class="sxs-lookup"><span data-stu-id="206d7-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="206d7-153">预配您的 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="206d7-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="206d7-154">这些过程说明如何预配 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="206d7-155">成功完成这些过程之后，Commerce 预览环境将可以进行配置。</span><span class="sxs-lookup"><span data-stu-id="206d7-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="206d7-156">此处介绍的所有活动都在 LCS 门户中进行。</span><span class="sxs-lookup"><span data-stu-id="206d7-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="206d7-157">预览访问权限与您在预览应用程序中指定的 LCS 帐户和组织关联。</span><span class="sxs-lookup"><span data-stu-id="206d7-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="206d7-158">您必须使用相同的帐户来预配 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="206d7-159">如果必须为 Commerce 预览环境使用其他 LCS 帐户或租户，则必须将这些详细信息提供给 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="206d7-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="206d7-160">有关联系信息，请参阅本主题后面的 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。</span><span class="sxs-lookup"><span data-stu-id="206d7-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="206d7-161">授予电子商务应用程序的访问权限</span><span class="sxs-lookup"><span data-stu-id="206d7-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="206d7-162">登录的人员必须是拥有 Azure AD 租户 ID 的 Azure AD 租户管理员。</span><span class="sxs-lookup"><span data-stu-id="206d7-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="206d7-163">如果此步骤未成功完成，其余的预配步骤将失败。</span><span class="sxs-lookup"><span data-stu-id="206d7-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="206d7-164">若要授权电子商务应用程序访问您的 Azure 订阅，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="206d7-165">组合以下格式的 URL：</span><span class="sxs-lookup"><span data-stu-id="206d7-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="206d7-166">将 URL 复制并粘贴到浏览器或文本编辑器中，然后将 **\{AAD\_TENANT\_ID\}** 替换为您的 Azure AD 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="206d7-167">然后打开 URL。</span><span class="sxs-lookup"><span data-stu-id="206d7-167">Then open the URL.</span></span>
1. <span data-ttu-id="206d7-168">在 Azure AD 登录对话框中，登录并确认您要授予 **Dynamics 365 Commerce（预览）** 访问您的订阅的权限。</span><span class="sxs-lookup"><span data-stu-id="206d7-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="206d7-169">您将被重定向到一个页面，其指示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="206d7-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="206d7-170">确认预览功能可用且已在 LCS 中打开</span><span class="sxs-lookup"><span data-stu-id="206d7-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="206d7-171">要确认预览功能可用且已在 LCS 中打开，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="206d7-172">使用用于请求预览访问权限的相同 LCS 帐户登录到 [LCS 门户](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="206d7-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="206d7-173">在 LCS 主页上，滚动到最右侧，然后选择**预览功能管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="206d7-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![预览管理磁贴](./media/preview1.png)

1. <span data-ttu-id="206d7-175">向下滚动到**专用预览功能**，确认以下功能可用且已打开：</span><span class="sxs-lookup"><span data-stu-id="206d7-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="206d7-176">电子商务评估</span><span class="sxs-lookup"><span data-stu-id="206d7-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="206d7-177">商务预览计划环境</span><span class="sxs-lookup"><span data-stu-id="206d7-177">Commerce Preview Program Environments</span></span>

    ![专用预览功能](./media/preview2.png)

1. <span data-ttu-id="206d7-179">如果这些功能没有出现在列表中，请与 Microsoft 联系，并提供您的工作电子邮件地址、LCS 帐户和租户详细信息。</span><span class="sxs-lookup"><span data-stu-id="206d7-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="206d7-180">有关联系信息，请参阅 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。</span><span class="sxs-lookup"><span data-stu-id="206d7-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="206d7-181">创建新项目</span><span class="sxs-lookup"><span data-stu-id="206d7-181">Create a new project</span></span>

<span data-ttu-id="206d7-182">若要在 LCS 中创建新项目，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="206d7-183">在 LCS 主页上，选择加号 (**+**) 创建一个项目。</span><span class="sxs-lookup"><span data-stu-id="206d7-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="206d7-184">在右窗格中，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="206d7-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="206d7-185">如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。</span><span class="sxs-lookup"><span data-stu-id="206d7-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="206d7-186">如果您是客户，请选择**潜在售前支持**。</span><span class="sxs-lookup"><span data-stu-id="206d7-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="206d7-187">输入名称、描述和行业。</span><span class="sxs-lookup"><span data-stu-id="206d7-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="206d7-188">在**产品名称**字段中，选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="206d7-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="206d7-189">在**产品版本**字段中，选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="206d7-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="206d7-190">在**方法**字段中，选择 **Dynamics Retail 实施方法**。</span><span class="sxs-lookup"><span data-stu-id="206d7-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="206d7-191">可选：您可以从现有项目导入角色和用户。</span><span class="sxs-lookup"><span data-stu-id="206d7-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="206d7-192">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="206d7-192">Select **Create**.</span></span> <span data-ttu-id="206d7-193">将出现项目视图。</span><span class="sxs-lookup"><span data-stu-id="206d7-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="206d7-194">添加 Azure 连接器</span><span class="sxs-lookup"><span data-stu-id="206d7-194">Add the Azure Connector</span></span>

<span data-ttu-id="206d7-195">要将 Azure 连接器添加到您的 LCS 项目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="206d7-196">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="206d7-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="206d7-197">如果您是合作伙伴，请选择最右边的**项目设置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="206d7-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="206d7-198">如果您是客户，请在顶部菜单中选择**项目设置**。</span><span class="sxs-lookup"><span data-stu-id="206d7-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="206d7-199">选择 **Azure 连接器**。</span><span class="sxs-lookup"><span data-stu-id="206d7-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="206d7-200">选择**添加**添加 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="206d7-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="206d7-201">输入名称。</span><span class="sxs-lookup"><span data-stu-id="206d7-201">Enter a name.</span></span>
1. <span data-ttu-id="206d7-202">输入您的 Azure 订阅 ID。</span><span class="sxs-lookup"><span data-stu-id="206d7-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="206d7-203">打开**配置为使用 Azure 资源管理器(ARM)** 选项。</span><span class="sxs-lookup"><span data-stu-id="206d7-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="206d7-204">验证 **Azure 订阅 AAD 租户域(或 ID)** 值是否正确。</span><span class="sxs-lookup"><span data-stu-id="206d7-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="206d7-205">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="206d7-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="206d7-206">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="206d7-206">Select **Next**.</span></span>
1. <span data-ttu-id="206d7-207">按照页面上的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="206d7-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="206d7-208">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="206d7-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="206d7-209">登录 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="206d7-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="206d7-210">确保选择了正确的目录，然后在左侧菜单上选择**订阅**。</span><span class="sxs-lookup"><span data-stu-id="206d7-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="206d7-211">在列表中找到正确的订阅并选择它。</span><span class="sxs-lookup"><span data-stu-id="206d7-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="206d7-212">根据需要使用搜索功能。</span><span class="sxs-lookup"><span data-stu-id="206d7-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="206d7-213">在菜单上，选择**访问控制(IAM)**。</span><span class="sxs-lookup"><span data-stu-id="206d7-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="206d7-214">在右侧，在**添加角色分配**下，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="206d7-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="206d7-215">将显示**添加角色分配**窗格。</span><span class="sxs-lookup"><span data-stu-id="206d7-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="206d7-216">在**角色**字段中，选择**参与者**。</span><span class="sxs-lookup"><span data-stu-id="206d7-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="206d7-217">在**将访问权限分配到**字段中，保留默认值 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="206d7-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="206d7-218">在**选择**下，输入 **b96b7e94-b82e-4e71-99a0-cf7fb188acea**。</span><span class="sxs-lookup"><span data-stu-id="206d7-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="206d7-219">在列表中选择**动态部署服务 \[wsfed-enabled\]**。</span><span class="sxs-lookup"><span data-stu-id="206d7-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="206d7-220">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="206d7-220">Select **Save**.</span></span>

1. <span data-ttu-id="206d7-221">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="206d7-221">Select **Next**.</span></span>
1. <span data-ttu-id="206d7-222">按照页面上的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="206d7-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="206d7-223">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="206d7-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="206d7-224">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="206d7-224">Select **Next**.</span></span>
1. <span data-ttu-id="206d7-225">在 **Azure 区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="206d7-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="206d7-226">选择**连接**。</span><span class="sxs-lookup"><span data-stu-id="206d7-226">Select **Connect**.</span></span> <span data-ttu-id="206d7-227">应该会在列表中显示您的 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="206d7-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="206d7-228">导入 Commerce 预览演示库扩展</span><span class="sxs-lookup"><span data-stu-id="206d7-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="206d7-229">要将 Commerce 预览演示库扩展导入到您的项目中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="206d7-230">通过选择顶部的项目名称打开项目的主页。</span><span class="sxs-lookup"><span data-stu-id="206d7-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="206d7-231">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="206d7-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="206d7-232">如果您是合作伙伴，请选择最右边的**资产库**磁贴。</span><span class="sxs-lookup"><span data-stu-id="206d7-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="206d7-233">如果您是客户，请在顶部菜单中选择**资产库**。</span><span class="sxs-lookup"><span data-stu-id="206d7-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="206d7-234">在左侧列表中，选择**软件可部署包**。</span><span class="sxs-lookup"><span data-stu-id="206d7-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="206d7-235">选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="206d7-235">Select **Import**.</span></span>
1. <span data-ttu-id="206d7-236">在**共享资产库**下，在资产列表中选择 **Commerce 预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="206d7-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="206d7-237">选择**选取**。</span><span class="sxs-lookup"><span data-stu-id="206d7-237">Select **Pick**.</span></span> <span data-ttu-id="206d7-238">您已回到资产库，应该可以在列表中看到此扩展。</span><span class="sxs-lookup"><span data-stu-id="206d7-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="206d7-239">下图显示了必须在 LCS **资产库**页上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![导入 Commerce 预览演示库扩展](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="206d7-241">部署环境</span><span class="sxs-lookup"><span data-stu-id="206d7-241">Deploy the environment</span></span>

<span data-ttu-id="206d7-242">要部署环境，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="206d7-243">您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。</span><span class="sxs-lookup"><span data-stu-id="206d7-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="206d7-244">在**环境参数**视图中时，请确认文本 **Dynamics 365 Commerce (预览) - 演示(具有平台更新 30 的 10.0.6)** 直接出现在**环境名称**字段上方。</span><span class="sxs-lookup"><span data-stu-id="206d7-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="206d7-245">请参阅步骤 8 之后出现的图示。</span><span class="sxs-lookup"><span data-stu-id="206d7-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="206d7-246">在顶级菜单上，选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="206d7-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="206d7-247">选择**添加**添加环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="206d7-248">在**应用程序版本**字段中，选择 **10.0.6**。</span><span class="sxs-lookup"><span data-stu-id="206d7-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="206d7-249">在**平台版本**字段中，选择**平台更新 30**。</span><span class="sxs-lookup"><span data-stu-id="206d7-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![选择应用程序和平台版本](./media/project1.png)

1. <span data-ttu-id="206d7-251">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="206d7-251">Select **Next**.</span></span>
1. <span data-ttu-id="206d7-252">选择**演示**作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="206d7-252">Select **Demo** as the environment topology.</span></span>

    ![选择环境拓扑 1](./media/project2.png)

1. <span data-ttu-id="206d7-254">选择 **Dynamics 365 Commerce (预览) - 演示**作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="206d7-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="206d7-255">如果前面仅配置了一个 Azure 连接器，将把该连接器用于此环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="206d7-256">如果配置了多个 Azure 连接器，则可以选择要使用的连接器：**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="206d7-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="206d7-257">（为获得最佳的端到端性能，我们建议您选择**美国西部 2**。）</span><span class="sxs-lookup"><span data-stu-id="206d7-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![选择环境拓扑 2](./media/project3.png)

1. <span data-ttu-id="206d7-259">在**部署环境**页面上，输入环境名称。</span><span class="sxs-lookup"><span data-stu-id="206d7-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="206d7-260">高级设置保持原样。</span><span class="sxs-lookup"><span data-stu-id="206d7-260">Leave the advanced settings as they are.</span></span>

    ![部署环境页面](./media/project4.png)

1. <span data-ttu-id="206d7-262">根据需要调整 VM 大小。</span><span class="sxs-lookup"><span data-stu-id="206d7-262">Adjust the VM size as required.</span></span> <span data-ttu-id="206d7-263">（我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）</span><span class="sxs-lookup"><span data-stu-id="206d7-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="206d7-264">查看定价和许可条款，然后选中指示您同意这些条款的复选框。</span><span class="sxs-lookup"><span data-stu-id="206d7-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="206d7-265">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="206d7-265">Select **Next**.</span></span>
1. <span data-ttu-id="206d7-266">在部署确认页面，验证详细信息是否正确，然后选择**部署**。</span><span class="sxs-lookup"><span data-stu-id="206d7-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="206d7-267">您已返回到**云托管的环境**视图，列表中应该会显示您的环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="206d7-268">您请求的环境将显示为已入队列，然后是正在部署。</span><span class="sxs-lookup"><span data-stu-id="206d7-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="206d7-269">环境工作流将需要一些时间完成。</span><span class="sxs-lookup"><span data-stu-id="206d7-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="206d7-270">因此，请在大约六到九小时后再次检查。</span><span class="sxs-lookup"><span data-stu-id="206d7-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="206d7-271">继续操作之前，确保环境的状态为**已部署**。</span><span class="sxs-lookup"><span data-stu-id="206d7-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="206d7-272">初始化 RCSU</span><span class="sxs-lookup"><span data-stu-id="206d7-272">Initialize RCSU</span></span>

<span data-ttu-id="206d7-273">要初始化您的 RCSU，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="206d7-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="206d7-274">在**云托管的环境**视图中，在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="206d7-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="206d7-275">在右侧的环境视图中，选择**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="206d7-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="206d7-276">将显示环境详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="206d7-276">The environment details view appears.</span></span>
1. <span data-ttu-id="206d7-277">在**环境功能**下，选择**管理**。</span><span class="sxs-lookup"><span data-stu-id="206d7-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="206d7-278">在**零售**选项卡上，选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="206d7-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="206d7-279">将显示 RCSU 初始化参数视图。</span><span class="sxs-lookup"><span data-stu-id="206d7-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="206d7-280">在**区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="206d7-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="206d7-281">在**版本**字段中，在列表中选择**指定版本**，然后在出现的字段中指定 **9.16.19262.5**。</span><span class="sxs-lookup"><span data-stu-id="206d7-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="206d7-282">请确保指定此处指示的确切版本。</span><span class="sxs-lookup"><span data-stu-id="206d7-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="206d7-283">否则，您以后不得不将 RCSU 更新到正确的版本。</span><span class="sxs-lookup"><span data-stu-id="206d7-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="206d7-284">打开**应用扩展**选项。</span><span class="sxs-lookup"><span data-stu-id="206d7-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="206d7-285">在扩展列表中，选择 **Commerce 预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="206d7-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="206d7-286">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="206d7-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="206d7-287">在部署确认页面，验证详细信息是否正确，然后选择**是**。</span><span class="sxs-lookup"><span data-stu-id="206d7-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="206d7-288">您已回到**零售管理**视图，其中已选择了**零售**选项卡。</span><span class="sxs-lookup"><span data-stu-id="206d7-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="206d7-289">您的 RCSU 现在已进入队列等待配置。</span><span class="sxs-lookup"><span data-stu-id="206d7-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="206d7-290">继续操作之前，确保 RCSU 的状态为**成功**。</span><span class="sxs-lookup"><span data-stu-id="206d7-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="206d7-291">初始化大约需要两到五个小时。</span><span class="sxs-lookup"><span data-stu-id="206d7-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="206d7-292">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="206d7-292">Initialize e-Commerce</span></span>

<span data-ttu-id="206d7-293">要初始化电子商务，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="206d7-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="206d7-294">在**电子商务(预览)** 选项卡上，查看预览同意内容，然后选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="206d7-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="206d7-295">在**电子商务租户名称**字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="206d7-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="206d7-296">但是，请注意，某些指向您的电子商务实例的 URL 中将显示此名称。</span><span class="sxs-lookup"><span data-stu-id="206d7-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="206d7-297">在 **Retail cloud scale unit 名称**字段中，在列表中选择您的 RCSU。</span><span class="sxs-lookup"><span data-stu-id="206d7-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="206d7-298">（此列表应该只有一个选项。）</span><span class="sxs-lookup"><span data-stu-id="206d7-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="206d7-299">**电子商务地理位置**字段是自动设置的，此值无法更改。</span><span class="sxs-lookup"><span data-stu-id="206d7-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="206d7-300">选择**下一步**继续。</span><span class="sxs-lookup"><span data-stu-id="206d7-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="206d7-301">在**支持的主机名**字段中，输入任意有效域，例如 `www.fabrikam.com`。</span><span class="sxs-lookup"><span data-stu-id="206d7-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="206d7-302">在**系统管理员的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。</span><span class="sxs-lookup"><span data-stu-id="206d7-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="206d7-303">选择放大镜图标以显示搜索结果。</span><span class="sxs-lookup"><span data-stu-id="206d7-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="206d7-304">从列表中选择安全组。</span><span class="sxs-lookup"><span data-stu-id="206d7-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="206d7-305">在**评级和审查仲裁者的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。</span><span class="sxs-lookup"><span data-stu-id="206d7-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="206d7-306">选择放大镜图标以显示搜索结果。</span><span class="sxs-lookup"><span data-stu-id="206d7-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="206d7-307">从列表中选择安全组。</span><span class="sxs-lookup"><span data-stu-id="206d7-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="206d7-308">保留**启用评级和审查服务**选项为打开。</span><span class="sxs-lookup"><span data-stu-id="206d7-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="206d7-309">如果您已经按“授予电子商务应用程序的访问权限”一节所述完成了 Microsoft Azure Active Directory (Azure AD) 同意步骤，请选中确认您同意的复选框。</span><span class="sxs-lookup"><span data-stu-id="206d7-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="206d7-310">如果尚未完成此步骤，您需要先完成，然后再继续初始化。</span><span class="sxs-lookup"><span data-stu-id="206d7-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="206d7-311">选择复选框旁边文本内的链接打开同意对话框并完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="206d7-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="206d7-312">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="206d7-312">Select **Initialize**.</span></span> <span data-ttu-id="206d7-313">您已回到**零售管理**视图，其中已选择了**电子商务(预览)** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="206d7-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="206d7-314">电子商务初始化已开始。</span><span class="sxs-lookup"><span data-stu-id="206d7-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="206d7-315">请等待电子商务初始化的状态成为**初始化成功**，再继续操作。</span><span class="sxs-lookup"><span data-stu-id="206d7-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="206d7-316">在右下方的**链接**下，记下以下链接的 URL：</span><span class="sxs-lookup"><span data-stu-id="206d7-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="206d7-317">**电子商务站点** – 指向您的电子商务站点的根目录的链接。</span><span class="sxs-lookup"><span data-stu-id="206d7-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="206d7-318">**电子商务站点管理工具** – 站点管理工具的链接。</span><span class="sxs-lookup"><span data-stu-id="206d7-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="206d7-319">Commerce 预览环境支持</span><span class="sxs-lookup"><span data-stu-id="206d7-319">Commerce preview environment support</span></span>

<span data-ttu-id="206d7-320">如果您在完成预配步骤时遇到问题，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)获取帮助。</span><span class="sxs-lookup"><span data-stu-id="206d7-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="206d7-321">如果您在尝试访问 Yammer 组时遇到问题，您可以通过电子邮件 <Dynamics365Commerce@microsoft.com> 与 Microsoft 联系。</span><span class="sxs-lookup"><span data-stu-id="206d7-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="206d7-322">此电子邮件地址的查看频率较低。</span><span class="sxs-lookup"><span data-stu-id="206d7-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="206d7-323">因此，回复会比较迟。</span><span class="sxs-lookup"><span data-stu-id="206d7-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="206d7-324">后续步骤</span><span class="sxs-lookup"><span data-stu-id="206d7-324">Next steps</span></span>

<span data-ttu-id="206d7-325">要继续 Commerce 预览环境的预配和配置过程，请参阅[配置 Commerce 预览环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="206d7-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="206d7-326">其他资源</span><span class="sxs-lookup"><span data-stu-id="206d7-326">Additional resources</span></span>

[<span data-ttu-id="206d7-327">Commerce 预览环境概述</span><span class="sxs-lookup"><span data-stu-id="206d7-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="206d7-328">配置 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="206d7-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="206d7-329">为 Commerce 预览环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="206d7-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="206d7-330">Commerce 预览环境常见问题</span><span class="sxs-lookup"><span data-stu-id="206d7-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="206d7-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="206d7-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="206d7-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="206d7-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="206d7-333">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="206d7-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="206d7-334">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="206d7-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="206d7-335">Dynamics 365 Retail 的帮助资源</span><span class="sxs-lookup"><span data-stu-id="206d7-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
