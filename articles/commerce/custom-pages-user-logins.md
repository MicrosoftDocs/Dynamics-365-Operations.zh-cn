---
title: 设置用户登录自定义页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970070"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="2db29-103">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="2db29-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2db29-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="2db29-105">概览</span><span class="sxs-lookup"><span data-stu-id="2db29-105">Overview</span></span>

<span data-ttu-id="2db29-106">若要使用在 Dynamics 365 Commerce 中创作的自定义页面来处理用户登录流，必须设置 Commerce 环境中将引用的Azure AD 策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="2db29-107">可以使用 Azure AD B2C 应用程序配置“注册和登录”、“个人资料编辑”和“密码重置”Azure AD B2C 策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="2db29-108">然后可以在使用 Microsoft Dynamics Lifecycle Services (LCS) 对 Commerce 环境进行预配流程期间引用 Azure AD B2C 租户和策略名称。</span><span class="sxs-lookup"><span data-stu-id="2db29-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="2db29-109">可以使用登录、注册、帐户个人资料编辑或密码重置模块生成自定义 Commerce 页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="2db29-110">然后，应该在 Azure 门户中的 Azure AD B2C 策略配置内引用为这些自定义页面发布的页面 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="2db29-111">设置 B2C 策略</span><span class="sxs-lookup"><span data-stu-id="2db29-111">Set up B2C policies</span></span>

<span data-ttu-id="2db29-112">设置 Azure AD B2C 租户并将其与 Commerce 环境关联之后，在 Azure 门户中转到 **Azure AD B2C** 页面，在菜单中 **策略** 下选择 **用户流(策略)**。</span><span class="sxs-lookup"><span data-stu-id="2db29-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![菜单中的“用户流(策略)”命令](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="2db29-114">现在可使用“注册和登录”、“个人资料编辑”和“密码重置”用户登录流。</span><span class="sxs-lookup"><span data-stu-id="2db29-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="2db29-115">配置“注册和登录”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="2db29-116">若要配置“注册和登录”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="2db29-117">选择 **新建用户流**，然后在 **建议** 选项卡中选择 **注册和登录** 策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="2db29-118">输入策略的名称（如 **B2C\_1\_SignInSignUp**）。</span><span class="sxs-lookup"><span data-stu-id="2db29-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="2db29-119">在 **身份提供程序** 部分中，选择要用于策略的身份提供程序。</span><span class="sxs-lookup"><span data-stu-id="2db29-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="2db29-120">至少必须选择 **电子邮件注册**。</span><span class="sxs-lookup"><span data-stu-id="2db29-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="2db29-121">在 **收集属性** 列中，选中 **电子邮件地址**、**给定名称** 和 **姓** 复选框。</span><span class="sxs-lookup"><span data-stu-id="2db29-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="2db29-122">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**身份提供程序**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="2db29-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![已选中属性和声明](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="2db29-124">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2db29-125">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="2db29-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2db29-126">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="2db29-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![新策略的属性页](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="2db29-128">将在 Commerce 环境中完全引用策略名称。</span><span class="sxs-lookup"><span data-stu-id="2db29-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="2db29-129">（引用中将包括前缀 **B2C\_1\_**。）策略在创建后不能重命名。</span><span class="sxs-lookup"><span data-stu-id="2db29-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="2db29-130">如果要更换 Commerce 环境的现有策略，可删除原始策略，然后生成一个同名新策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="2db29-131">此外，如果已预配了环境，可以通过服务请求提交新策略名称。</span><span class="sxs-lookup"><span data-stu-id="2db29-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="2db29-132">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="2db29-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2db29-133">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="2db29-134">配置“个人资料编辑”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="2db29-135">若要配置“个人资料编辑”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="2db29-136">选择 **新建用户流**，然后在 **建议** 选项卡中选择 **个人资料编辑** 策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="2db29-137">输入策略的名称（如 **B2C\_1\_EditProfile**）。</span><span class="sxs-lookup"><span data-stu-id="2db29-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="2db29-138">在 **身份提供程序** 部分中，选择要用于策略的身份提供程序。</span><span class="sxs-lookup"><span data-stu-id="2db29-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="2db29-139">至少必须选择 **本地帐户登录**。</span><span class="sxs-lookup"><span data-stu-id="2db29-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="2db29-140">在 **收集属性** 列中，选中 **电子邮件地址** 和 **姓** 复选框。</span><span class="sxs-lookup"><span data-stu-id="2db29-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="2db29-141">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**身份提供程序**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="2db29-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="2db29-142">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2db29-143">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="2db29-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2db29-144">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="2db29-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="2db29-145">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="2db29-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2db29-146">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="2db29-147">配置“密码重置”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="2db29-148">若要配置“密码重置”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="2db29-149">选择 **新建用户流**，然后在 **预览** 选项卡中选择 **密码重置 v1.1** 策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![“预览”选项卡中已选择“密码重置 v1.1”策略](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="2db29-151">输入策略的名称（如 **B2C\_1\_ForgetPassword**）。</span><span class="sxs-lookup"><span data-stu-id="2db29-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="2db29-152">在 **身份提供程序** 部分中，选择 **使用电子邮件地址重置密码**。</span><span class="sxs-lookup"><span data-stu-id="2db29-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="2db29-153">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="2db29-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![已选择声明](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="2db29-155">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="2db29-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2db29-156">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="2db29-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2db29-157">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="2db29-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="2db29-158">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="2db29-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2db29-159">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="2db29-160">生成自定义页面</span><span class="sxs-lookup"><span data-stu-id="2db29-160">Build the custom pages</span></span>

<span data-ttu-id="2db29-161">若要声明自定义页面以处理用户登录，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="2db29-162">在 Commerce 创作工具中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="2db29-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="2db29-163">生成下面的五个模板和五个页面：</span><span class="sxs-lookup"><span data-stu-id="2db29-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="2db29-164">使用登录模块的 **登录** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="2db29-165">使用注册模块的 **注册** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="2db29-166">使用密码重置模块的 **密码重置** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="2db29-167">使用密码重置验证模块的 **密码重置验证** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="2db29-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="2db29-168">使用帐户个人资料编辑模块的 **个人资料编辑** 模板和页面</span><span class="sxs-lookup"><span data-stu-id="2db29-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="2db29-169">生成页面时，请遵守以下说明：</span><span class="sxs-lookup"><span data-stu-id="2db29-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="2db29-170">对每个页面或模块使用最适合您的业务要求的布局和样式。</span><span class="sxs-lookup"><span data-stu-id="2db29-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="2db29-171">发布 Azure AD B2C 设置中必须使用的所有页面和 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="2db29-172">发布页面和 URL 之后，收集必须用于 Azure AD B2C 策略配置的 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="2db29-173">将在使用每个 URL 时向其添加 **?preloadscripts=true** 后缀。</span><span class="sxs-lookup"><span data-stu-id="2db29-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2db29-174">请勿使用具有相对链接的通用页眉和页脚。</span><span class="sxs-lookup"><span data-stu-id="2db29-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="2db29-175">因为这些页面在使用时托管在 Azure AD B2C 域中，所以仅应对所有链接使用绝对 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="2db29-176">为 Azure AD B2C 策略配置自定义页面信息</span><span class="sxs-lookup"><span data-stu-id="2db29-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="2db29-177">在 Azure 门户中，回到 **Azure AD B2C** 页面，然后在菜单中 **策略** 下，选择 **用户流(策略)**。</span><span class="sxs-lookup"><span data-stu-id="2db29-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="2db29-178">使用自定义页面信息更新“注册和登录”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="2db29-179">若要使用自定义页面信息更新“注册和登录”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2db29-180">在前面配置的 **登录和注册** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="2db29-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2db29-181">选择 **统一注册或登录页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="2db29-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="2db29-182">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2db29-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2db29-183">在 **自定义页面 URI** 字段中，输入完整的登录 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="2db29-184">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="2db29-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2db29-185">例如，输入 ``www.<my domain>.com/sign-in?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="2db29-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2db29-186">在 **页面布局版本(预览)** 字段中，选择 **1.2.0**。</span><span class="sxs-lookup"><span data-stu-id="2db29-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2db29-187">选择 **本地帐户注册页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="2db29-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="2db29-188">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2db29-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2db29-189">在 **自定义页面 URI** 字段中，输入完整的注册 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="2db29-190">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="2db29-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2db29-191">例如，输入 ``www.<my domain>.com/sign-up?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="2db29-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2db29-192">在 **页面布局版本(预览)** 字段中，选择 **1.2.0**。</span><span class="sxs-lookup"><span data-stu-id="2db29-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2db29-193">在 **用户属性** 部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="2db29-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="2db29-194">在 **需要验证** 字段中对 **电子邮件地址**、**给定名称** 和 **姓** 属性选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="2db29-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="2db29-195">在 **可选** 字段中对 **给定名称** 和 **姓** 属性选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="2db29-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![“本地帐户注册页面”策略的配置](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="2db29-197">使用自定义页面信息更新“个人资料编辑”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="2db29-198">若要使用自定义页面信息更新“个人资料编辑”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2db29-199">在前面配置的 **个人资料编辑** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="2db29-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2db29-200">选择 **个人资料编辑页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="2db29-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="2db29-201">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2db29-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2db29-202">在 **自定义页面 URI** 字段中，输入完整的个人资料编辑 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="2db29-203">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="2db29-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2db29-204">例如，输入 ``www.<my domain>.com/profile-edit?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="2db29-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2db29-205">在 **页面布局版本(预览)** 字段中，选择 **1.2.0**。</span><span class="sxs-lookup"><span data-stu-id="2db29-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2db29-206">在 **用户属性** 部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="2db29-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="2db29-207">在 **需要验证** 字段中对 **电子邮件地址** 和 **给定名称** 属性选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="2db29-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="2db29-208">在 **可选** 字段中对 **给定名称** 和 **姓** 属性选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="2db29-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="2db29-209">使用自定义页面信息更新“密码重置”策略</span><span class="sxs-lookup"><span data-stu-id="2db29-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="2db29-210">若要使用自定义页面信息更新“密码重置”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2db29-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2db29-211">在前面配置的 **密码重置** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="2db29-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2db29-212">选择 **新建密码页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="2db29-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="2db29-213">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2db29-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2db29-214">在 **自定义页面 URI** 字段中，输入完整的密码重置 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="2db29-215">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="2db29-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2db29-216">例如，输入 ``www.<my domain>.com/passwordreset?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="2db29-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2db29-217">在 **页面布局版本(预览)** 字段中，选择 **1.2.0**。</span><span class="sxs-lookup"><span data-stu-id="2db29-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2db29-218">选择 **帐户验证页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="2db29-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="2db29-219">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2db29-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2db29-220">在 **自定义页面 URI** 字段中，输入完整的密码重置验证 URL。</span><span class="sxs-lookup"><span data-stu-id="2db29-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="2db29-221">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="2db29-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2db29-222">例如，输入 ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="2db29-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2db29-223">在 **页面布局版本(预览)** 字段中，选择 **1.2.0**。</span><span class="sxs-lookup"><span data-stu-id="2db29-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="2db29-224">自定义标签和描述的默认文本字符串</span><span class="sxs-lookup"><span data-stu-id="2db29-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="2db29-225">在模块库中，已经为登录模块预填充了标签和描述的默认文本字符串。</span><span class="sxs-lookup"><span data-stu-id="2db29-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="2db29-226">可通过更新登录模块的 global.json 文件来自定义软件开发工具包 (SDK) 中的这些字符串。</span><span class="sxs-lookup"><span data-stu-id="2db29-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="2db29-227">例如，遗忘密码链接的默认文本为 **忘记密码了?**。</span><span class="sxs-lookup"><span data-stu-id="2db29-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="2db29-228">下面显示登录页面中的默认文本。</span><span class="sxs-lookup"><span data-stu-id="2db29-228">The following shows this default text on the sign-in page.</span></span>

![登录页面中忘记密码了链接的默认文本](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="2db29-230">但是，在模块库登录模块的 global.json 文件中，可将文本编辑为 **忘记了密码?**，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="2db29-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![登录模块的 global.json 文件中更新后的链接文本](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="2db29-232">更新 global.json 文件并发布更改之后，将在 Commerce 中和活动的登录页面内登录模块中显示新链接文本。</span><span class="sxs-lookup"><span data-stu-id="2db29-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2db29-233">其他资源</span><span class="sxs-lookup"><span data-stu-id="2db29-233">Additional resources</span></span>

[<span data-ttu-id="2db29-234">配置域名</span><span class="sxs-lookup"><span data-stu-id="2db29-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2db29-235">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="2db29-235">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2db29-236">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="2db29-236">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2db29-237">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="2db29-237">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2db29-238">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="2db29-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="2db29-239">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="2db29-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="2db29-240">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="2db29-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="2db29-241">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="2db29-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="2db29-242">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="2db29-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="2db29-243">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="2db29-243">Enable location-based store detection</span></span>](enable-store-detection.md)
