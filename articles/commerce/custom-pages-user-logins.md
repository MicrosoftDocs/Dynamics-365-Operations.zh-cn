---
title: 设置用户登录自定义页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0318814f421ab862559965bb4b003308d6279812
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799437"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="60a4e-103">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="60a4e-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60a4e-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="60a4e-105">若要使用在 Dynamics 365 Commerce 中创作的自定义页面来处理用户登录流，必须设置 Commerce 环境中将引用的Azure AD 策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="60a4e-106">可以使用 Azure AD B2C 应用程序配置“注册和登录”、“个人资料编辑”和“密码重置”Azure AD B2C 策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="60a4e-107">然后可以在使用 Microsoft Dynamics Lifecycle Services (LCS) 对 Commerce 环境进行预配流程期间引用 Azure AD B2C 租户和策略名称。</span><span class="sxs-lookup"><span data-stu-id="60a4e-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="60a4e-108">可以使用登录、注册、帐户个人资料编辑、密码重置或通用 AAD 模块生成自定义 Commerce 页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, password reset, or generic AAD modules.</span></span> <span data-ttu-id="60a4e-109">然后，应该在 Azure 门户中的 Azure AD B2C 策略配置内引用为这些自定义页面发布的页面 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

> [!WARNING] 
> <span data-ttu-id="60a4e-110">Azure AD B2C 将于 2021 年 8 月 1 日停用旧（旧版）用户流。</span><span class="sxs-lookup"><span data-stu-id="60a4e-110">Azure AD B2C will retire old (legacy) user flows by August 1, 2021.</span></span> <span data-ttu-id="60a4e-111">因此，您应该计划将用户流迁移到新的推荐版本。</span><span class="sxs-lookup"><span data-stu-id="60a4e-111">Therefore, you should plan to migrate your user flows to the new recommended version.</span></span> <span data-ttu-id="60a4e-112">新版本提供功能奇偶一致性和新功能。</span><span class="sxs-lookup"><span data-stu-id="60a4e-112">The new version provides feature parity and new features.</span></span> <span data-ttu-id="60a4e-113">有关详细信息，请参阅 [Azure Active Directory B2C 中的用户流](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview)。</span><span class="sxs-lookup"><span data-stu-id="60a4e-113">For more information, see [User flows in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview).</span></span>

><span data-ttu-id="60a4e-114">Commerce 版本 10.0.15 或更高版本的模块库应与推荐的 B2C 用户流一起使用。</span><span class="sxs-lookup"><span data-stu-id="60a4e-114">The module library for Commerce version 10.0.15 or higher should be used with the recommended B2C user flows.</span></span> <span data-ttu-id="60a4e-115">在 Azure AD B2C 中提供的默认用户策略页面也可以使用，并且允许添加与公司品牌相关的背景图像、徽标和背景颜色更改。</span><span class="sxs-lookup"><span data-stu-id="60a4e-115">The default user policy pages offered in Azure AD B2C can also be used, and allow for added background image, logo, and background color changes related to company branding.</span></span> <span data-ttu-id="60a4e-116">尽管设计功能受到更多限制，但是默认用户策略页面提供 Azure AD B2C 策略功能，而无需创建和配置专用的自定义页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-116">Though more limited in design capabilities, the default user policy pages provide Azure AD B2C policy functionality without creating and configuring dedicated custom pages.</span></span> 

## <a name="set-up-b2c-policies"></a><span data-ttu-id="60a4e-117">设置 B2C 策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-117">Set up B2C policies</span></span>

<span data-ttu-id="60a4e-118">设置 Azure AD B2C 租户并将其与 Commerce 环境关联之后，在 Azure 门户中转到 **Azure AD B2C** 页面，在菜单中 **策略** 下选择 **用户流(策略)**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-118">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![菜单中的“用户流(策略)”命令](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="60a4e-120">现在可使用“注册和登录”、“个人资料编辑”和“密码重置”用户登录流。</span><span class="sxs-lookup"><span data-stu-id="60a4e-120">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="60a4e-121">配置“注册和登录”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-121">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="60a4e-122">若要配置“注册和登录”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-122">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-123">选择 **新建用户流**，选择 **注册和登录**，选择 **建议** 选项卡，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-123">Select **New user flow**, select **Sign up and sign in**, select the **Recommended** tab,  and then select **Create**.</span></span>
1. <span data-ttu-id="60a4e-124">输入策略的名称（如 **B2C\_1\_SignInSignUp**）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-124">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="60a4e-125">在 **身份提供程序** 部分中，选择要用于策略的身份提供程序。</span><span class="sxs-lookup"><span data-stu-id="60a4e-125">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="60a4e-126">至少必须选择 **电子邮件注册**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-126">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="60a4e-127">在 **收集属性** 列中，选中 **电子邮件地址**、**给定名称** 和 **姓** 复选框。</span><span class="sxs-lookup"><span data-stu-id="60a4e-127">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="60a4e-128">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**身份提供程序**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="60a4e-128">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![已选中属性和声明](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="60a4e-130">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-130">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="60a4e-131">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-131">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="60a4e-132">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-132">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![新策略的属性页](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="60a4e-134">将在 Commerce 环境中完全引用策略名称。</span><span class="sxs-lookup"><span data-stu-id="60a4e-134">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="60a4e-135">（引用中将包括前缀 **B2C\_1\_**。）策略在创建后不能重命名。</span><span class="sxs-lookup"><span data-stu-id="60a4e-135">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="60a4e-136">如果要更换 Commerce 环境的现有策略，可删除原始策略，然后生成一个同名新策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-136">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="60a4e-137">此外，如果已预配了环境，可以通过服务请求提交新策略名称。</span><span class="sxs-lookup"><span data-stu-id="60a4e-137">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="60a4e-138">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="60a4e-138">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="60a4e-139">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-139">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="60a4e-140">配置“个人资料编辑”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-140">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="60a4e-141">若要配置“个人资料编辑”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-141">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-142">选择 **新建用户流**，选择 **个人资料编辑**，选择 **建议** 选项卡，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-142">Select **New user flow**, select **Profile editing**, select the **Recommended** tab, and then select **Create**.</span></span>
1. <span data-ttu-id="60a4e-143">输入策略的名称（如 **B2C\_1\_EditProfile**）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-143">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="60a4e-144">在 **身份提供程序** 部分中，选择要用于策略的身份提供程序。</span><span class="sxs-lookup"><span data-stu-id="60a4e-144">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="60a4e-145">至少必须选择 **本地帐户登录**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-145">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="60a4e-146">在 **收集属性** 列中，选中 **给定名称** 和 **姓** 复选框。</span><span class="sxs-lookup"><span data-stu-id="60a4e-146">In the **Collect attribute** column, select the check boxes for **Given Name** and **Surname**.</span></span>
1. <span data-ttu-id="60a4e-147">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**身份提供程序**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="60a4e-147">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="60a4e-148">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-148">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="60a4e-149">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-149">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="60a4e-150">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-150">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="60a4e-151">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="60a4e-151">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="60a4e-152">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-152">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="60a4e-153">配置“密码重置”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-153">Configure the "Password reset" policy</span></span>

<span data-ttu-id="60a4e-154">若要配置“密码重置”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-154">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-155">选择 **新建用户流**，选择 **密码重置** 选项，选择 **建议** 选项卡，然后单击 **创建**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-155">Select **New user flow**, and then select the **Password reset** option, and choose the **Recommended** tab, and click **Create**.</span></span>
1. <span data-ttu-id="60a4e-156">输入策略的名称（如 **B2C\_1\_ForgetPassword**）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-156">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="60a4e-157">在 **身份提供程序** 部分中，选择 **使用电子邮件地址重置密码**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-157">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="60a4e-158">在 **返回声明** 列中，选中 **电子邮件地址**、**给定名称**、**姓** 和 **用户的对象 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="60a4e-158">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="60a4e-159">选择 **确定** 创建策略。</span><span class="sxs-lookup"><span data-stu-id="60a4e-159">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="60a4e-160">双击新策略名称，然后在导航窗格中选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-160">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="60a4e-161">将 **启用 JavaScript 执行页面布局(预览)** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-161">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="60a4e-162">生成自定义页面之后，您将回到此策略以完成设置。</span><span class="sxs-lookup"><span data-stu-id="60a4e-162">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="60a4e-163">现在，关闭策略以回到 Azure 门户中的 **用户流(策略)** 页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-163">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="60a4e-164">生成自定义页面</span><span class="sxs-lookup"><span data-stu-id="60a4e-164">Build the custom pages</span></span>

<span data-ttu-id="60a4e-165">Commerce 中包括专用 Azure AD 模块以为 Azure AD B2C 用户策略生成自定义页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-165">Dedicated Azure AD modules are included in Commerce to build custom pages for Azure AD B2C user policies.</span></span> <span data-ttu-id="60a4e-166">可以使用下面详细描述的主 Azure AD B2C 模块专门为每个用户策略页面的布局生成页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-166">Pages can be built specifically for each user policy page's layout using the main Azure AD B2C modules detailed below.</span></span> <span data-ttu-id="60a4e-167">或者，可以针对 Azure AD B2C 中的所有页面布局和策略（甚至是下面未列出的策略中的页面布局选项）使用 **AAD 通用** 模块。</span><span class="sxs-lookup"><span data-stu-id="60a4e-167">Alternatively, the **AAD Generic** module can be used for all page layouts and policies in Azure AD B2C (even for page layout options within policies not listed below).</span></span> 

- <span data-ttu-id="60a4e-168">特定于页面的 Azure AD 模块将绑定到由 Azure AD B2C 呈现的数据输入项目。</span><span class="sxs-lookup"><span data-stu-id="60a4e-168">Page-specific Azure AD modules are bound to data input items rendered by Azure AD B2C.</span></span> <span data-ttu-id="60a4e-169">这些模块使您可以更好地控制页面中元素的位置。</span><span class="sxs-lookup"><span data-stu-id="60a4e-169">These modules give you more control over the positioning of the elements in your pages.</span></span> <span data-ttu-id="60a4e-170">但是，可能需要生成更多页面和模块扩展，以解决如下所述的默认设置之外的差异。</span><span class="sxs-lookup"><span data-stu-id="60a4e-170">However, more pages and module extensions may need to be built to account for variances beyond the default settings described below.</span></span>
- <span data-ttu-id="60a4e-171">**AAD 通用** 模块为 Azure AD B2C 创建“div”元素以在用户策略页面布局中呈现所有元素，从而为 B2C 提供更大的灵活性，但对位置和样式的控制减少（虽然 CSS 可用于匹配站点的外观和风格）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-171">The **AAD Generic** module creates the "div" element for Azure AD B2C to render all elements in the user policy page layout, giving more flexibility to the B2C functions of the page, but less control of the positioning and styling (though CSS can be used to match the look and feel of your site).</span></span>

<span data-ttu-id="60a4e-172">您可以使用 **AAD 通用** 模块创建单个页面并将其用于所有用户策略页面，或者您可以使用单独的 Azure AD 模块生成用于登录、注册、个人资料编辑、密码重置和密码重置验证的特定页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-172">You can create a single page with the **AAD Generic** module and use it for all of your user policy pages, or you can build out specific pages using the individual Azure AD modules for sign-in, sign-up, profile edit, password reset, and password reset verification.</span></span> <span data-ttu-id="60a4e-173">您也可以将两者混合使用，将特定的 Azure AD 页面用于如下所述的页面布局，将通用 AAD 模块页面用于这些页面或其他用户策略页面内的其余页面布局。</span><span class="sxs-lookup"><span data-stu-id="60a4e-173">You may also use a mix of both, using the specific Azure AD pages for the page layouts noted below, and the generic AAD module page for remaining page layouts within these or other user policies pages.</span></span>

<span data-ttu-id="60a4e-174">若要了解有关模块库附带的 Azure AD 模块的详细信息，请详细阅读[身份管理页面和模块](identity-mgmt-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="60a4e-174">To learn more about the Azure AD Modules that ship with the module library, read more at [Identity management pages and modules](identity-mgmt-modules.md).</span></span>

<span data-ttu-id="60a4e-175">若要使用特定身份模块生成自定义页面以处理用户登录，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-175">To build the custom pages with specific identity modules to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-176">在 Commerce 站点构建器中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="60a4e-176">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="60a4e-177">生成以下五个模板和页面（如果您的站点中尚不存在）：</span><span class="sxs-lookup"><span data-stu-id="60a4e-177">Build the following five templates and pages (if not already present in your site):</span></span>
    - <span data-ttu-id="60a4e-178">使用登录模块的 **登录** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-178">A **Sign In** template and page that use the sign-in module.</span></span>
    - <span data-ttu-id="60a4e-179">使用注册模块的 **注册** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-179">A **Sign Up** template and page that use the sign-up module.</span></span>
    - <span data-ttu-id="60a4e-180">使用密码重置模块的 **密码重置** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-180">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="60a4e-181">使用密码重置验证模块的 **密码重置验证** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-181">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="60a4e-182">使用帐户个人资料编辑模块的 **个人资料编辑** 模板和页面。</span><span class="sxs-lookup"><span data-stu-id="60a4e-182">A **Profile Edit** template and page that use the account profile edit module.</span></span>

<span data-ttu-id="60a4e-183">生成页面时，请遵守以下说明：</span><span class="sxs-lookup"><span data-stu-id="60a4e-183">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="60a4e-184">对每个页面或模块使用最适合您的业务要求的布局和样式。</span><span class="sxs-lookup"><span data-stu-id="60a4e-184">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="60a4e-185">发布 Azure AD B2C 设置中必须使用的所有页面和 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-185">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="60a4e-186">发布页面和 URL 之后，收集必须用于 Azure AD B2C 策略配置的 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-186">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="60a4e-187">将在使用每个 URL 时向其添加 **?preloadscripts=true** 后缀。</span><span class="sxs-lookup"><span data-stu-id="60a4e-187">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60a4e-188">生成以供在 Azure AD B2C 中引用的页面直接通过 Azure AD B2C 租户的域提供服务。</span><span class="sxs-lookup"><span data-stu-id="60a4e-188">Pages built to be referenced in Azure AD B2C are served directly from the Azure AD B2C tenant's domain.</span></span> <span data-ttu-id="60a4e-189">请勿使用具有相对链接的通用页眉和页脚。</span><span class="sxs-lookup"><span data-stu-id="60a4e-189">Do not reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="60a4e-190">因为这些页面在使用时托管在 Azure AD B2C 域中，所以仅应对所有链接使用绝对 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-190">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span> <span data-ttu-id="60a4e-191">建议使用需要删除 Retail Server 连接的任何 Commerce 特定模块，创建具有 Azure AD 相关的自定义页面的绝对 URL 的特定页面和页脚。</span><span class="sxs-lookup"><span data-stu-id="60a4e-191">It is recommended to create a specific header and footer with absolute URLs for your Azure AD-related custom pages, with any Commerce-specific modules that require connection to Retail Server removed.</span></span> <span data-ttu-id="60a4e-192">例如，收藏夹、搜索栏、登录链接和购物车模块不应包括在将用于 Azure AD B2C 用户流的任何页面中。</span><span class="sxs-lookup"><span data-stu-id="60a4e-192">For example, the favorites, search bar, sign-in link, and cart modules should not be included in any pages which will be used in Azure AD B2C user flows.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="60a4e-193">为 Azure AD B2C 策略配置自定义页面信息</span><span class="sxs-lookup"><span data-stu-id="60a4e-193">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="60a4e-194">在 Azure 门户中，回到 **Azure AD B2C** 页面，然后在菜单中 **策略** 下，选择 **用户流(策略)**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-194">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="60a4e-195">使用自定义页面信息更新“注册和登录”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-195">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="60a4e-196">若要使用自定义页面信息更新“注册和登录”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-196">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-197">在前面配置的 **登录和注册** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-197">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="60a4e-198">选择 **统一注册或登录页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="60a4e-198">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="60a4e-199">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-199">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="60a4e-200">在 **自定义页面 URI** 字段中，输入完整的登录 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-200">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="60a4e-201">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-201">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="60a4e-202">例如，输入 ``www.<my domain>.com/sign-in?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="60a4e-202">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="60a4e-203">在 **页面布局版本** 字段中，选择版本 **2.1.0** 或更高版本（需要 Commerce 版本 10.0.15 或更高版本的模块库）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-203">In the **Page Layout Version** field, select version **2.1.0** or later (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="60a4e-204">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-204">Select **Save**.</span></span>
1. <span data-ttu-id="60a4e-205">选择 **本地帐户注册页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="60a4e-205">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="60a4e-206">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-206">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="60a4e-207">在 **自定义页面 URI** 字段中，输入完整的注册 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-207">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="60a4e-208">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-208">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="60a4e-209">例如，输入 ``www.<my domain>.com/sign-up?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="60a4e-209">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="60a4e-210">在 **页面布局版本** 字段中，选择版本 **2.1.0** 或更高版本（需要 Commerce 版本 10.0.15 或更高版本的模块库）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-210">In the **Page Layout Version** field, select version **2.1.0** or later (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="60a4e-211">在 **用户属性** 部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="60a4e-211">In the **User attributes** section, follow these steps:</span></span>
    1. <span data-ttu-id="60a4e-212">对于 **给定名称** 和 **姓** 属性，在 **需要验证** 列中选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-212">For the **Given Name** and **Surname** attributes, select **No** in the **Requires Verification** column.</span></span>
    1. <span data-ttu-id="60a4e-213">对于 **电子邮件地址** 属性，建议在 **需要验证** 列中保留选择的默认值 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-213">For **Email Address** attribute, it is recommended to leave the default value **Yes** selected in the **Requires Verification** column.</span></span> <span data-ttu-id="60a4e-214">此选项可确保使用给定电子邮件地址注册的用户验证自己是否拥有该电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="60a4e-214">This option ensures that users signing up with a given email address verify that they own the email address.</span></span>
    1. <span data-ttu-id="60a4e-215">对于 **电子邮件地址**、**给定名称** 和 **姓** 属性，在 **可选** 列中选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-215">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Optional** column.</span></span>
1. <span data-ttu-id="60a4e-216">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-216">Select **Save**.</span></span>

    ![本地帐户注册页面策略的配置](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="60a4e-218">使用自定义页面信息更新“个人资料编辑”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-218">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="60a4e-219">若要使用自定义页面信息更新“个人资料编辑”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-219">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-220">在前面配置的 **个人资料编辑** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-220">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="60a4e-221">选择 **个人资料编辑页面** 布局（可能需要向下滚动到其他布局选项，具体取决于您的屏幕）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-221">Select the **Profile edit page** layout (may require scrolling down past other layout options, depending on your screen).</span></span>
1. <span data-ttu-id="60a4e-222">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-222">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="60a4e-223">在 **自定义页面 URI** 字段中，输入完整的个人资料编辑 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-223">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="60a4e-224">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-224">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="60a4e-225">例如，输入 ``www.<my domain>.com/profile-edit?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="60a4e-225">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="60a4e-226">对于 **页面布局版本**，选择版本 **2.1.0** 或更高版本（需要 Commerce 版本 10.0.15 或更高版本的模块库）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-226">For **Page Layout Version**, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
1. <span data-ttu-id="60a4e-227">在 **用户属性** 部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="60a4e-227">In the **User attributes** section, follow these steps:</span></span>
    1. <span data-ttu-id="60a4e-228">对于 **给定名称** 和 **姓** 属性，在 **可选** 列中选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-228">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** column.</span></span>
    1. <span data-ttu-id="60a4e-229">对于 **给定名称** 和 **姓** 属性，在 **需要验证** 列中选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-229">For the **Given Name** and **Surname** attributes, select **No** in the **Requires verification** column.</span></span>
1. <span data-ttu-id="60a4e-230">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-230">Select **Save**.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="60a4e-231">使用自定义页面信息更新“密码重置”策略</span><span class="sxs-lookup"><span data-stu-id="60a4e-231">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="60a4e-232">若要使用自定义页面信息更新“密码重置”策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="60a4e-232">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="60a4e-233">在前面配置的 **密码重置** 策略中导航窗格内，选择 **页面布局**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-233">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="60a4e-234">选择 **忘记密码页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="60a4e-234">Select the **Forgot password page** layout.</span></span>
1. <span data-ttu-id="60a4e-235">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-235">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="60a4e-236">在 **自定义页面 URI** 字段中，输入完整的密码重置验证 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-236">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="60a4e-237">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-237">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="60a4e-238">例如，输入 ``www.<my domain>.com/password-reset-verification?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="60a4e-238">For example, enter ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="60a4e-239">在 **页面布局版本** 字段中，选择版本 **2.1.0** 或更高版本（需要 Commerce 版本 10.0.15 或更高版本的模块库）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-239">In the **Page Layout Version** field, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
2. <span data-ttu-id="60a4e-240">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-240">Select **Save**.</span></span>
3. <span data-ttu-id="60a4e-241">选择 **更改密码页面** 布局。</span><span class="sxs-lookup"><span data-stu-id="60a4e-241">Select the **Change password page** layout.</span></span>
4. <span data-ttu-id="60a4e-242">将 **使用自定义页面内容** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-242">Set the **Use custom page content** option to **Yes**.</span></span>
5. <span data-ttu-id="60a4e-243">在 **自定义页面 URI** 字段中，输入完整的密码重置 URL。</span><span class="sxs-lookup"><span data-stu-id="60a4e-243">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="60a4e-244">包括后缀 **?preloadscripts=true**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-244">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="60a4e-245">例如，输入 ``www.<my domain>.com/password-reset?preloadscripts=true``。</span><span class="sxs-lookup"><span data-stu-id="60a4e-245">For example, enter ``www.<my domain>.com/password-reset?preloadscripts=true``.</span></span>
6. <span data-ttu-id="60a4e-246">在 **页面布局版本** 字段中，选择版本 **2.1.0** 或更高版本（需要 Commerce 版本 10.0.15 或更高版本的模块库）。</span><span class="sxs-lookup"><span data-stu-id="60a4e-246">In the **Page Layout Version** field, select version **2.1.0** or higher (requires module library for Commerce version 10.0.15 or higher).</span></span>
7. <span data-ttu-id="60a4e-247">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-247">Select **Save**.</span></span>

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="60a4e-248">自定义标签和描述的默认文本字符串</span><span class="sxs-lookup"><span data-stu-id="60a4e-248">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="60a4e-249">在模块库中，已经为登录模块预填充了标签和描述的默认文本字符串。</span><span class="sxs-lookup"><span data-stu-id="60a4e-249">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="60a4e-250">您可以在正在使用的模块的属性窗格中自定义字符串。</span><span class="sxs-lookup"><span data-stu-id="60a4e-250">You can customize the strings in the properties pane of the module you are working on.</span></span> <span data-ttu-id="60a4e-251">页面上的其他字符串（例如 **忘记密码？** 链接文本或 **创建帐户** 操作文本）将需要使用 Commerce 软件开发工具包 (SDK) 并为登录模块更新 global.json 文件中的值。</span><span class="sxs-lookup"><span data-stu-id="60a4e-251">Additional strings on the page (such as the **Forgotten password?** link text or the **Create an account** call to action text) will require using the Commerce software development kit (SDK) and updating the values in the global.json file for the sign-in module.</span></span>

<span data-ttu-id="60a4e-252">例如，遗忘密码链接的默认文本为 **忘记密码了?**。</span><span class="sxs-lookup"><span data-stu-id="60a4e-252">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="60a4e-253">下面显示登录页面中的默认文本。</span><span class="sxs-lookup"><span data-stu-id="60a4e-253">The following shows this default text on the sign-in page.</span></span>

![登录页面中忘记密码了链接的默认文本](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="60a4e-255">但是，在模块库登录模块的 global.json 文件中，可将文本编辑为 **忘记了密码?**，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="60a4e-255">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![登录模块的 global.json 文件中更新后的链接文本](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="60a4e-257">更新 global.json 文件并发布更改之后，将在 Commerce 中和活动的登录页面内登录模块中显示新链接文本。</span><span class="sxs-lookup"><span data-stu-id="60a4e-257">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60a4e-258">其他资源</span><span class="sxs-lookup"><span data-stu-id="60a4e-258">Additional resources</span></span>

[<span data-ttu-id="60a4e-259">配置域名</span><span class="sxs-lookup"><span data-stu-id="60a4e-259">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="60a4e-260">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="60a4e-260">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="60a4e-261">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="60a4e-261">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="60a4e-262">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="60a4e-262">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="60a4e-263">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="60a4e-263">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="60a4e-264">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="60a4e-264">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="60a4e-265">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="60a4e-265">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="60a4e-266">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="60a4e-266">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="60a4e-267">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="60a4e-267">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="60a4e-268">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="60a4e-268">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
