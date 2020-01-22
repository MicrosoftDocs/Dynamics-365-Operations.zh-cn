---
title: 处理 CSS 覆盖文件
description: 本主题介绍为什么、何时以及如何在 Microsoft Dynamics 365 Commerce 中使用级联样式表 (CSS) 覆盖文件。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915431"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="b1f8b-103">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-103">Work with CSS override files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b1f8b-104">本主题介绍为什么、何时以及如何在 Microsoft Dynamics 365 Commerce 中使用级联样式表 (CSS) 覆盖文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1f8b-105">概览</span><span class="sxs-lookup"><span data-stu-id="b1f8b-105">Overview</span></span>

<span data-ttu-id="b1f8b-106">永久站点样式通常应该通过站点主题进行处理。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="b1f8b-107">主题为站点的任何一个页面上的模块提供基本 CSS 和样式设置。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="b1f8b-108">主题是使用 Dynamics 365 Commerce 联机软件开发套件 (SDK) 创建的，可以通过 Microsoft Dynamics Lifecycle Services (LCS) 部署到您的网站。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b1f8b-109">SDK 中的主题调试功能和模块接口配置可帮助站点开发人员创建可自定义且紧密结合的站点设计包。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="b1f8b-110">将这些设计包部署到站点时，站点作者可以专注于创建、编辑和发布内容，而不是站点开发。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="b1f8b-111">考虑到主题的一般生命周期，在某些情况下，依赖开发人员通过 SDK 和 LCS 部署管道进行样式更改可能会被禁止。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="b1f8b-112">如果未配置 SDK，或者您没有时间等待 LCS 部署完成，站点原型或修补程序似乎会很难处理。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="b1f8b-113">在这些情况下，CSS 覆盖文件可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="b1f8b-114">在 Commerce 创作工具中，经过身份验证的用户可以上载 CSS 文件，对其进行预览，然后将其激活来覆盖站点的主题。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="b1f8b-115">SDK 或 LCS 部署不需要开销。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="b1f8b-116">CSS 覆盖文件中指定的覆盖可以小至对一个文本样式的更改，也可以广到完整的品牌调整。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="b1f8b-117">使用 CSS 覆盖文件之前，请注意以下限制：</span><span class="sxs-lookup"><span data-stu-id="b1f8b-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="b1f8b-118">站点上一次只能有一个 CSS 覆盖文件处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="b1f8b-119">因此，所有活动覆盖都必须在一个覆盖文件中。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="b1f8b-120">尽管您可以在 Commerce 创作工具中预览覆盖，但是并没有专用的调试功能来帮助发现覆盖所引起的错误。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="b1f8b-121">换句话说，当您使用 CSS 覆盖文件时，您没有与 SDK 为模块和创作验证提供的相同的工具集。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="b1f8b-122">不过，CSS 覆盖文件提供了一种在开发和部署完整主题更新之前快速设计原型或实现修补程序的方法。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="b1f8b-123">新建 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-123">Create a CSS override file</span></span>

<span data-ttu-id="b1f8b-124">创建 CSS 覆盖文件，您可以使用任何一个集成开发环境 (IDE)、文本编辑器或源代码编辑器。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="b1f8b-125">一种典型的方法是在浏览器中使用标准 Web 调试器，来在现有站点上确定样式选择器、属性和值。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="b1f8b-126">大多数浏览器允许您在调试器中更改值并预览它们。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="b1f8b-127">确定要进行的更改后，可以将其保存到您自己的 CSS 文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="b1f8b-128">上载 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-128">Upload a CSS override file</span></span>

<span data-ttu-id="b1f8b-129">要将 CSS 文件上载到 Commerce 中的站点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b1f8b-130">在创作工具中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="b1f8b-131">在左侧的导航窗格中，选择**设计**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1f8b-132">根据您使用的 Commerce 的创作工具的版本，您可能需要在导航窗格中展开**设置**，然后才能选择**设计**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="b1f8b-133">在主设计窗格的顶部，选择 **CSS 覆盖**选项卡（如果尚未选择）。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="b1f8b-134">在**可用 CSS 覆盖**下，选择**上载 CSS 文件**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="b1f8b-135">将出现一个“文件资源管理器”窗口。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="b1f8b-136">在“文件资源管理器”中，浏览并选择一个 CSS 文件，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="b1f8b-137">上载的 CSS 文件现在显示在**可用 CSS 覆盖**下。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="b1f8b-138">预览 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-138">Preview a CSS override file</span></span>

<span data-ttu-id="b1f8b-139">若要预览 CSS 覆盖文件，然后在活动站点上将其激活，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="b1f8b-140">在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要预览的 CSS 文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="b1f8b-141">在 CSS 文件名旁边，选择**预览站点**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="b1f8b-142">在**选择 URL** 对话框中，选择应用了覆盖的站点的 URL，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="b1f8b-143">如果所选 URL 有多个变型，请在出现的**预览变型**对话框中选择所需的变型。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="b1f8b-144">将打开一个新的浏览器选项卡或窗口，您可以在其中验证针对您的网站的样式覆盖。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="b1f8b-145">然后，您可以与其他经过身份验证的 Commerce 用户共享该 URL，以进行查看和反馈。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="b1f8b-146">在您的活动站点上激活 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="b1f8b-147">预览并批准后 CSS 覆盖文件，您可以在活动站点上激活它。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="b1f8b-148">您的站点上一次只能有一个 CSS 覆盖文件处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="b1f8b-149">如果激活新的覆盖文件，先前的覆盖文件将被禁用。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="b1f8b-150">因此，请确保所有必需的覆盖都存在于一个 CSS 覆盖文件中。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="b1f8b-151">若要激活 CSS 覆盖文件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="b1f8b-152">在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要激活的 CSS 文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="b1f8b-153">在 CSS 文件名下，选择**激活**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="b1f8b-154">覆盖文件将立即在您的活动站点上变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="b1f8b-155">在您的活动站点上禁用 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="b1f8b-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="b1f8b-156">要在您的站点上禁用 CSS 覆盖文件，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="b1f8b-157">在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要禁用的 CSS 文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="b1f8b-158">在 CSS 文件名下，选择**禁用**。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="b1f8b-159">覆盖文件将立即在您的活动站点上变为停用状态。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="b1f8b-160">要访问 CSS 覆盖文件的其他选项，请选择 CSS 文件名旁边的省略号 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="b1f8b-161">**下载**、**重命名**和**替换**选项可用于快速更改现有的 CSS 覆盖文件。</span><span class="sxs-lookup"><span data-stu-id="b1f8b-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1f8b-162">其他资源</span><span class="sxs-lookup"><span data-stu-id="b1f8b-162">Additional resources</span></span>

[<span data-ttu-id="b1f8b-163">添加徽标</span><span class="sxs-lookup"><span data-stu-id="b1f8b-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b1f8b-164">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="b1f8b-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b1f8b-165">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="b1f8b-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b1f8b-166">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="b1f8b-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b1f8b-167">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="b1f8b-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b1f8b-168">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="b1f8b-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b1f8b-169">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="b1f8b-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
