---
title: 在 Commerce 环境中配置多个 B2C 租户
description: 本主题介绍何时和如何在专用的 Dynamics 365 Commerce 环境中设置多个按渠道 Microsoft Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以进行用户身份验证。
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027714"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="62d3a-103">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62d3a-104">本主题介绍何时和如何在专用的 Dynamics 365 Commerce 环境中按渠道设置多个 Microsoft Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以进行用户身份验证。</span><span class="sxs-lookup"><span data-stu-id="62d3a-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="62d3a-105">Dynamics 365 Commerce 使用 Azure AD B2C 云标识服务为用户凭据和身份验证流提供支持。</span><span class="sxs-lookup"><span data-stu-id="62d3a-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="62d3a-106">用户可以使用身份验证流注册，登录和重置密码。</span><span class="sxs-lookup"><span data-stu-id="62d3a-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="62d3a-107">Azure AD B2C 中存储用户的敏感身份验证信息，如用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="62d3a-107">Azure AD B2C stores a user's sensitive authentication information, such as the user name and password.</span></span> <span data-ttu-id="62d3a-108">用户记录对每个 B2C 租户都是唯一的，其使用用户名（电子邮件地址）凭据或社交标识提供程序凭据。</span><span class="sxs-lookup"><span data-stu-id="62d3a-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="62d3a-109">大多数情况下，一个 Commerce 环境中仅使用一个 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="62d3a-110">然后，Commerce 客户可以在同一个 Commerce 环境中创建和发布多个站点，而这些站点中将使用相同的客户凭据。</span><span class="sxs-lookup"><span data-stu-id="62d3a-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="62d3a-111">但是，如果应该将环境中的站点视为不同品牌，并作为不同企业向用户显示，则可以为渠道配置 B2C 租户来区分站点/品牌。</span><span class="sxs-lookup"><span data-stu-id="62d3a-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="62d3a-112">按渠道设置多个 B2C 租户时的注意事项</span><span class="sxs-lookup"><span data-stu-id="62d3a-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="62d3a-113">将每个渠道或站点视为一个单独的企业时，Commerce 中与用户身份验证流有关的最佳选项通常是使用单独的法人。</span><span class="sxs-lookup"><span data-stu-id="62d3a-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="62d3a-114">但是，如果要让每个渠道/站点保留在同一个环境和法人中，但是不希望为每个站点使用单独的用户身份验证，请务必在继续操作之前注意以下事项：</span><span class="sxs-lookup"><span data-stu-id="62d3a-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="62d3a-115">用户自己有每个渠道/站点的不同凭据。</span><span class="sxs-lookup"><span data-stu-id="62d3a-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="62d3a-116">同一人可以有每个渠道/站点的两个不同帐户，因为每个帐户在一个单独的 B2C 租户中是一个唯一条目。</span><span class="sxs-lookup"><span data-stu-id="62d3a-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="62d3a-117">在 Microsoft Dynamics 环境中，将为全局记录搜索返回单独的客户记录。</span><span class="sxs-lookup"><span data-stu-id="62d3a-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="62d3a-118">如果用户在多个渠道/站点中使用同一个电子邮件地址，全局客户搜索将返回每个渠道/站点的结果。</span><span class="sxs-lookup"><span data-stu-id="62d3a-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="62d3a-119">（将显示渠道指示器。）</span><span class="sxs-lookup"><span data-stu-id="62d3a-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="62d3a-120">可使用通讯簿帮助为用户分组，以便按渠道跟踪这些用户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="62d3a-121">每个渠道的客户记录数可能会增加，并且这种增加可能会影响全局客户搜索的性能。</span><span class="sxs-lookup"><span data-stu-id="62d3a-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="62d3a-122">必须将 B2C 租户仔细地映射到渠道，以便帮助避免客户注册错误的租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="62d3a-123">否则，可能会发生混淆或跟踪问题。</span><span class="sxs-lookup"><span data-stu-id="62d3a-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="62d3a-124">下图显示一个 Commerce 环境中的多个 B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![一个 Commerce 环境中的多个 B2C 租户](media/MultiB2C_In_Environment.png)

<span data-ttu-id="62d3a-126">如果认定您的企业在同一个 Commerce 环境中每个渠道需要不同 B2C 租户，请完成以下部分中的过程请求此功能。</span><span class="sxs-lookup"><span data-stu-id="62d3a-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="62d3a-127">在环境中配置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="62d3a-128">若要在环境中配置 B2C 租户，请完成此部分中的相关过程。</span><span class="sxs-lookup"><span data-stu-id="62d3a-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="62d3a-129">添加 Azure AD B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="62d3a-130">若要向环境添加 Azure AD B2C 租户，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="62d3a-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="62d3a-131">以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="62d3a-132">在左侧导航窗格中，选择 **租户设置** 将其展开。</span><span class="sxs-lookup"><span data-stu-id="62d3a-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="62d3a-133">选择 **B2C 设置**，然后选择 **管理**。</span><span class="sxs-lookup"><span data-stu-id="62d3a-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="62d3a-134">选择 **添加 B2C 应用程序**，然后输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="62d3a-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="62d3a-135">**应用程序名称**：输入应该在 Commerce 中的应用程序管理上下文内用于应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="62d3a-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="62d3a-136">建议使用您在 Azure 门户中设置 Azure AD B2C 应用程序时选择的应用程序名称。</span><span class="sxs-lookup"><span data-stu-id="62d3a-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="62d3a-137">这样就可以在 Commerce 中管理 B2C 租户时帮助降低混淆程度。</span><span class="sxs-lookup"><span data-stu-id="62d3a-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="62d3a-138">**租户名称**：输入要在 Azure 门户中显示的 B2C 租户名称。</span><span class="sxs-lookup"><span data-stu-id="62d3a-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="62d3a-139">**忘记密码策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。</span><span class="sxs-lookup"><span data-stu-id="62d3a-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="62d3a-140">**注册登录策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。</span><span class="sxs-lookup"><span data-stu-id="62d3a-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="62d3a-141">**客户端 GUID**：输入在 Azure 门户中显示的 Azure AD B2C 租户 ID（而不是 B2C 租户的应用程序 ID）。</span><span class="sxs-lookup"><span data-stu-id="62d3a-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="62d3a-142">**编辑配置文件策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。</span><span class="sxs-lookup"><span data-stu-id="62d3a-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="62d3a-143">输入完此信息之后，选择 **确定** 保存更改。</span><span class="sxs-lookup"><span data-stu-id="62d3a-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="62d3a-144">现在 **管理 B2C 应用程序** 下的列表中应该会显示您的新 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="62d3a-145">除非 Dynamics 365 Commerce 团队指示您设置 **范围**、**非交互式策略 ID**、**非交互式客户端 ID**、**登录自定义域** 和 **注册策略 ID** 等字段，否则请将这些字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="62d3a-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="62d3a-146">管理或删除 Azure AD B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="62d3a-147">以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="62d3a-148">在左侧导航窗格中，选择 **租户设置** 将其展开。</span><span class="sxs-lookup"><span data-stu-id="62d3a-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="62d3a-149">选择 **B2C 设置**，然后选择 **管理**。</span><span class="sxs-lookup"><span data-stu-id="62d3a-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="62d3a-150">若要编辑 B2C 租户，请选择其旁边的铅笔符号。</span><span class="sxs-lookup"><span data-stu-id="62d3a-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="62d3a-151">若要删除 B2C 租户，请选择其旁边的废纸篓符号。</span><span class="sxs-lookup"><span data-stu-id="62d3a-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="62d3a-152">选择 **保存**，然后选择 **发布** 激活您的更改。</span><span class="sxs-lookup"><span data-stu-id="62d3a-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="62d3a-153">为有效/已发布站点配置了 B2C 租户之后，用户可能已通过使用租户中的帐户进行了注册。</span><span class="sxs-lookup"><span data-stu-id="62d3a-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="62d3a-154">如果在 **租户设置 \> B2C 租户** 菜单中删除配置的租户，将解除该 B2C 租户和与该租户的任何渠道关联的站点之间的关联。</span><span class="sxs-lookup"><span data-stu-id="62d3a-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="62d3a-155">在此情况下，您的用户可能再也不能登录自己的帐户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="62d3a-156">因此，删除配置的租户时，请务必小心谨慎。</span><span class="sxs-lookup"><span data-stu-id="62d3a-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="62d3a-157">如果删除配置的租户，将继续保留 B2C 租户和记录，但是将更改或删除该租户的 Commerce 系统配置。</span><span class="sxs-lookup"><span data-stu-id="62d3a-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="62d3a-158">尝试注册或登录站点的用户将在为该站点的渠道配置的默认的或新关联的 B2C 租户中创建一个新的帐户记录。</span><span class="sxs-lookup"><span data-stu-id="62d3a-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="62d3a-159">为渠道配置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="62d3a-160">以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="62d3a-161">在左侧导航窗格中，选择 **站点设置** 将其展开。</span><span class="sxs-lookup"><span data-stu-id="62d3a-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="62d3a-162">选择 **渠道**，然后选择要配置的渠道。</span><span class="sxs-lookup"><span data-stu-id="62d3a-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="62d3a-163">在右侧的属性窗格中 **选择 B2C 应用程序** 字段内，选择为用于此渠道而配置的 Azure AD B2C 租户。</span><span class="sxs-lookup"><span data-stu-id="62d3a-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="62d3a-164">在命令栏中，选择 **保存并发布** 提交新的或更新后的配置。</span><span class="sxs-lookup"><span data-stu-id="62d3a-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="62d3a-165">如果更改分配给渠道的 B2C 应用程序，将删除已经为在环境中已注册的任何用户建立的当前首选项。</span><span class="sxs-lookup"><span data-stu-id="62d3a-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="62d3a-166">在此情况下，与当前分配的 B2C 应用程序关联的所有凭据对用户均不可用。</span><span class="sxs-lookup"><span data-stu-id="62d3a-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="62d3a-167">因此，仅当您首次设置渠道，并且任何用户均不可注册时，才更改渠道的 Azure AD B2C 配置。</span><span class="sxs-lookup"><span data-stu-id="62d3a-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="62d3a-168">否则，用户可能必须再次注册，才能在新的 Azure AD B2C 租户中建立记录。</span><span class="sxs-lookup"><span data-stu-id="62d3a-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="62d3a-169">其他资源</span><span class="sxs-lookup"><span data-stu-id="62d3a-169">Additional resources</span></span>

[<span data-ttu-id="62d3a-170">配置域名</span><span class="sxs-lookup"><span data-stu-id="62d3a-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="62d3a-171">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="62d3a-172">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="62d3a-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="62d3a-173">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="62d3a-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="62d3a-174">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="62d3a-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="62d3a-175">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="62d3a-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="62d3a-176">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="62d3a-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="62d3a-177">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="62d3a-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="62d3a-178">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="62d3a-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="62d3a-179">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="62d3a-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
