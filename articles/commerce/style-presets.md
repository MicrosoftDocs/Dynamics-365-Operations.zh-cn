---
title: 使用样式预设
description: 此主题描述如何在 Microsoft Dynamics 365 Commerce 站点构建器中使用站点样式预设。
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7279b52f801c2cb2f156d220d1a456b773d10f33
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791743"
---
# <a name="work-with-style-presets"></a><span data-ttu-id="0bef2-103">使用样式预设</span><span class="sxs-lookup"><span data-stu-id="0bef2-103">Work with style presets</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0bef2-104">此主题描述如何在 Microsoft Dynamics 365 Commerce 站点构建器中使用站点样式预设。</span><span class="sxs-lookup"><span data-stu-id="0bef2-104">This topic describes how to work with site style presets in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="0bef2-105">样式预设是站点主题中所有可创作样式值的存储集。</span><span class="sxs-lookup"><span data-stu-id="0bef2-105">A style preset is a stored set of all authorable style values across a site's theme.</span></span> <span data-ttu-id="0bef2-106">它可用于从站点构建器立即更改站点的外观。</span><span class="sxs-lookup"><span data-stu-id="0bef2-106">It can be used to immediately change the look of a site from site builder.</span></span> <span data-ttu-id="0bef2-107">样式预设使 Commerce 站点构建器作者可以快速更改、预览和激活整个站点中的一组样式值，而不必使用级联样式表 (CSS) 或部署主题。</span><span class="sxs-lookup"><span data-stu-id="0bef2-107">Style presets let Commerce site builder authors quickly change, preview, and activate a set of style values across their site, without having to use Cascading Style Sheets (CSS) or deploy themes.</span></span> <span data-ttu-id="0bef2-108">字体样式、按钮样式和站点颜色是可以通过样式预设管理的样式变量的典型示例。</span><span class="sxs-lookup"><span data-stu-id="0bef2-108">Font styles, button styles, and site colors are typical examples of style variables that can be managed through style presets.</span></span>

<span data-ttu-id="0bef2-109">站点中可用的样式变量集由部署到站点租户的主题和模块库确定。</span><span class="sxs-lookup"><span data-stu-id="0bef2-109">The set of style variables that is available in a site is determined by the theme and module library that is deployed to a site's tenant.</span></span> <span data-ttu-id="0bef2-110">Dynamics 365 Commerce 联机软件开发套件 (SDK) 使开发人员可以尽可能多（或少）地实现给定主题所需的可创作样式变量。</span><span class="sxs-lookup"><span data-stu-id="0bef2-110">The Dynamics 365 Commerce online software development kit (SDK) lets developers implement as many (or as few) authorable style variables as they require for a given theme.</span></span> <span data-ttu-id="0bef2-111">通过启用更多样式变量，主题开发人员可以将有关站点样式的最终选择权交给站点构建器作者。</span><span class="sxs-lookup"><span data-stu-id="0bef2-111">By enabling more style variables, a theme developer can put final choices about site styles into the hands of site builder authors.</span></span> <span data-ttu-id="0bef2-112">因此，非开发人员可以使用工具集更新和预览站点样式。</span><span class="sxs-lookup"><span data-stu-id="0bef2-112">Therefore, non-developers can update and preview site styles by using the toolset.</span></span> <span data-ttu-id="0bef2-113">对于直接更改主题或 CSS 会导致不必要开销的任何情况，此功能也很有用。</span><span class="sxs-lookup"><span data-stu-id="0bef2-113">The capability is also useful for any scenario where direct changes to themes or CSS will cause unnecessary overhead.</span></span>

<span data-ttu-id="0bef2-114">启用可创作样式变量的主题需要默认样式预设。</span><span class="sxs-lookup"><span data-stu-id="0bef2-114">Themes where authorable style variables are enabled require a default style preset.</span></span> <span data-ttu-id="0bef2-115">它们可以作为已部署主题包的一部分有选择地包含其他预设选项。</span><span class="sxs-lookup"><span data-stu-id="0bef2-115">They can optionally include additional preset options as part of a deployed theme package.</span></span> <span data-ttu-id="0bef2-116">例如，可以部署具有单个默认“现代浅色”样式预设的主题。</span><span class="sxs-lookup"><span data-stu-id="0bef2-116">For example, a theme can be deployed that has a single default "modern light" style preset.</span></span> <span data-ttu-id="0bef2-117">或者，除默认预设外，还可以包含其他样式预设选项，如“现代深色”、“复古浅色”或“复古深色”。</span><span class="sxs-lookup"><span data-stu-id="0bef2-117">Alternatively, it might include additional style preset options besides the default preset, such as "modern dark," "vintage light," or "vintage dark."</span></span> <span data-ttu-id="0bef2-118">这些内置主题预设由开发人员创建，可以用作新站点设计的起点。</span><span class="sxs-lookup"><span data-stu-id="0bef2-118">These built-in theme presets are created by developers and can be used as starting points for new site designs.</span></span>

<span data-ttu-id="0bef2-119">在站点构建器中，作者可以在主题的内置预设之间进行选择，或者可以使用启用的样式变量来创建自己的样式预设和自定义项。</span><span class="sxs-lookup"><span data-stu-id="0bef2-119">In site builder, authors can select among a theme's built-in presets, or they can create their own style presets and customizations by using the enabled style variables.</span></span> <span data-ttu-id="0bef2-120">样式预设在活动站点上激活之前可以在站点构建器中预览。</span><span class="sxs-lookup"><span data-stu-id="0bef2-120">A style preset can be previewed in site builder before it's activated on the live site.</span></span> <span data-ttu-id="0bef2-121">在审核作者的样式更改后，可以将活动站点的样式预设设置为“活动”。</span><span class="sxs-lookup"><span data-stu-id="0bef2-121">After an author's style changes are reviewed, the style preset can then be set to "active" for the live site.</span></span>

## <a name="preview-a-style-preset"></a><span data-ttu-id="0bef2-122">预览样式预设</span><span class="sxs-lookup"><span data-stu-id="0bef2-122">Preview a style preset</span></span>

<span data-ttu-id="0bef2-123">要在站点构建器中预览站点上的样式预设，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0bef2-123">To preview a style preset on your site in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0bef2-124">在站点的左侧导航窗格中，转到 **站点设置 \> 设计**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-124">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="0bef2-125">在设计编辑器顶部的 **样式预设** 选项卡上，在 **可用预设** 列表中，选择一个预设，然后选择 **查看** 转到预设编辑器。</span><span class="sxs-lookup"><span data-stu-id="0bef2-125">On the **Style presets** tab at the top of the design editor, in the **Available presets** list, select a preset, and then select **View** to go to the preset editor.</span></span>

    <span data-ttu-id="0bef2-126">如果 **可用预设** 列表中当前没有预设，请参阅[创建自定义样式预设](#create-a-custom-style-preset)了解有关如何创建自定义样式预设的信息。</span><span class="sxs-lookup"><span data-stu-id="0bef2-126">If there are currently no presets in the **Available presets** list, see [Create a custom style preset](#create-a-custom-style-preset) for information about how to create a custom style preset.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bef2-127">主题中包含的预设使用 **内置** 标记指示。</span><span class="sxs-lookup"><span data-stu-id="0bef2-127">Presets that were included with the theme are indicated by a **Built-in** badge.</span></span> <span data-ttu-id="0bef2-128">这些内置预设是只读的。</span><span class="sxs-lookup"><span data-stu-id="0bef2-128">These built-in presets are read-only.</span></span> <span data-ttu-id="0bef2-129">要作为新的可自定义预设复制内置预设，请选择预设对应的省略号按钮 (**...**)，然后选择 **另存为**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-129">To copy a built-in preset as a new customizable preset, select the ellipsis button (**...**) for the preset, and then select **Save as**.</span></span>

1. <span data-ttu-id="0bef2-130">在命令栏中，选择 **预览**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-130">On the command bar, select **Preview**.</span></span>
1. <span data-ttu-id="0bef2-131">从您的站点中选择一个 URL 来预览样式预设，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-131">Select a URL from your site to use to preview the style preset, and then select **OK**.</span></span>
1. <span data-ttu-id="0bef2-132">通过选择变型的名称来选择特定于渠道和特定于区域设置的 URL 变型来进行预览。</span><span class="sxs-lookup"><span data-stu-id="0bef2-132">Select the channel-specific and locale-specific URL variant to preview by selecting the variant's name.</span></span> <span data-ttu-id="0bef2-133">一个新的预览浏览器窗口将打开，其中所选样式预设已应用于指定页面。</span><span class="sxs-lookup"><span data-stu-id="0bef2-133">A new preview browser window is opened, where the selected style preset is applied to the specified page.</span></span>

> [!NOTE]
> <span data-ttu-id="0bef2-134">预览 URL 是永久性的，且已经过验证。</span><span class="sxs-lookup"><span data-stu-id="0bef2-134">The preview URL is persistent and authenticated.</span></span> <span data-ttu-id="0bef2-135">因此，您可以在活动站点上将其设置为“活动”之前，将其复制、粘贴并发送给其他经过身份验证的同事进行审核。</span><span class="sxs-lookup"><span data-stu-id="0bef2-135">Therefore, you can copy, paste, and send it to other authenticated co-workers for review before you set it to "active" on your live site.</span></span> <span data-ttu-id="0bef2-136">预览 URL 对于检查不同设备、不同浏览器和不同屏幕上的样式也很有用。</span><span class="sxs-lookup"><span data-stu-id="0bef2-136">The preview URL is also useful for checking styles on different devices, in different browsers, and on different screens.</span></span>

> [!TIP]
> <span data-ttu-id="0bef2-137">在编辑样式预设时，您可能会发现让预览浏览器窗口在单独的浏览器窗口中保持打开状态很有用，这样您可以快速验证所作的更改。</span><span class="sxs-lookup"><span data-stu-id="0bef2-137">While you edit a style preset, you might find it helpful to leave the preview browser window for it open in a separate browser window, so that you can quickly validate your changes.</span></span> <span data-ttu-id="0bef2-138">在将更改保存到预设后，刷新打开的预览浏览器窗口来验证用户体验。</span><span class="sxs-lookup"><span data-stu-id="0bef2-138">After you save your changes to a preset, refresh the open preview browser window to validate the user experience.</span></span>

## <a name="create-a-custom-style-preset"></a><span data-ttu-id="0bef2-139">创建自定义样式预设</span><span class="sxs-lookup"><span data-stu-id="0bef2-139">Create a custom style preset</span></span>

<span data-ttu-id="0bef2-140">要在站点构建器中创建自定义样式预设，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0bef2-140">To create a custom style preset in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0bef2-141">在站点的左侧导航窗格中，转到 **站点设置 \> 设计**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-141">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="0bef2-142">在设计编辑器顶部的 **样式预设** 选项卡上，在命令栏中，选择 **新建预设**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-142">On the **Style presets** tab at the top of the design editor, on the command bar, select **New preset**.</span></span>
1. <span data-ttu-id="0bef2-143">为新预设输入名称和描述，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-143">Enter a name and description for the new preset, and then select **Save**.</span></span> <span data-ttu-id="0bef2-144">一个新的可自定义预设将创建，该预设使用主题的默认值作为起点。</span><span class="sxs-lookup"><span data-stu-id="0bef2-144">A new customizable preset is created that uses the theme's default values as a starting point.</span></span>

> [!NOTE]
> <span data-ttu-id="0bef2-145">您还可以通过选择现有预设对应的省略号按钮 (**...**)，然后选择 **另存为**，从任何现有预设创建新的自定义样式预设。</span><span class="sxs-lookup"><span data-stu-id="0bef2-145">You can also create a new custom style preset from any existing preset by selecting the ellipsis button (**...**) for that preset and then selecting **Save as**.</span></span> <span data-ttu-id="0bef2-146">或者，在预设编辑器中的命令栏上选择 **另存为**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-146">Alternatively, select **Save as** on the command bar in the preset editor.</span></span>

## <a name="modify-global-and-module-type-style-values"></a><span data-ttu-id="0bef2-147">修改全局和模块类型样式值</span><span class="sxs-lookup"><span data-stu-id="0bef2-147">Modify global and module type style values</span></span>

<span data-ttu-id="0bef2-148">某些主题的样式变量在多个模块类型之间共享。</span><span class="sxs-lookup"><span data-stu-id="0bef2-148">Some of a theme's style variables are shared among multiple module types.</span></span> <span data-ttu-id="0bef2-149">这些样式变量称为 *全局* 样式变量。</span><span class="sxs-lookup"><span data-stu-id="0bef2-149">These style variables are referred to as *global* style variables.</span></span> <span data-ttu-id="0bef2-150">示例包括主要站点颜色、默认字体样式和按钮样式。</span><span class="sxs-lookup"><span data-stu-id="0bef2-150">Examples include primary site colors, default font styles, and button styles.</span></span> <span data-ttu-id="0bef2-151">通过设置全局变量，您可以更改许多不同模块类型的外观。</span><span class="sxs-lookup"><span data-stu-id="0bef2-151">By setting global variables, you might change the look across many different module types.</span></span>

<span data-ttu-id="0bef2-152">某些样式值对于模块类型可能是唯一的，或者可能必须有选择地覆盖默认的全局值。</span><span class="sxs-lookup"><span data-stu-id="0bef2-152">Some style values can be unique to a module type, or they might have to optionally override a default global value.</span></span> <span data-ttu-id="0bef2-153">如果站点的主题已实现模块类型样式变量，站点构建器作者则可以独立于全局设置自定义模块类型的样式。</span><span class="sxs-lookup"><span data-stu-id="0bef2-153">If a site's theme has implemented module type style variables, site builder authors can customize the style of a module type independently of the global settings.</span></span> <span data-ttu-id="0bef2-154">模块类型变量可以增加或覆盖主题中的全局样式变量。</span><span class="sxs-lookup"><span data-stu-id="0bef2-154">Module type variables can either augment or override the global style variables in a theme.</span></span>

> [!NOTE]
> <span data-ttu-id="0bef2-155">站点中样式值的层次结构的行为方式如下。</span><span class="sxs-lookup"><span data-stu-id="0bef2-155">The hierarchy of style values in a site behaves in the following manner.</span></span> <span data-ttu-id="0bef2-156">出现在更靠右的样式值将覆盖它们左侧的样式值。</span><span class="sxs-lookup"><span data-stu-id="0bef2-156">Style values that appear farther to the right override the style values to the left of them.</span></span>
>
> <span data-ttu-id="0bef2-157">主题默认值 \< 全局样式值 \< 模块类型样式值 \< CSS 覆盖</span><span class="sxs-lookup"><span data-stu-id="0bef2-157">Theme default values \< Global style values \< Module type style values \< CSS override</span></span>

<span data-ttu-id="0bef2-158">要在站点构建器中更改样式预设的全局或模块类型值，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0bef2-158">To change a style preset's global or module type values in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0bef2-159">在站点的左侧导航窗格中，转到 **站点设置 \> 设计**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-159">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="0bef2-160">在设计编辑器顶部的 **样式预设** 选项卡上，选择任一样式预设对应的 **查看** 转到预设编辑器。</span><span class="sxs-lookup"><span data-stu-id="0bef2-160">On the **Style presets** tab at the top of the design editor, select **View** for any style preset to go to the preset editor.</span></span>
1. <span data-ttu-id="0bef2-161">选择 **预览**，然后按照 URL 选择步骤打开您的预设的全浏览器窗口预览。</span><span class="sxs-lookup"><span data-stu-id="0bef2-161">Select **Preview**, and then follow the URL selection steps to open a full-browser-window preview for your preset.</span></span> <span data-ttu-id="0bef2-162">将此预览浏览器窗口保持打开状态。</span><span class="sxs-lookup"><span data-stu-id="0bef2-162">Leave this preview browser window open.</span></span>
1. <span data-ttu-id="0bef2-163">在预设编辑器中，选择右上方的 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-163">In the preset editor, select **Edit** in the upper right.</span></span>
1. <span data-ttu-id="0bef2-164">在编辑器中使用样式变量控件来更改某些全局样式值。</span><span class="sxs-lookup"><span data-stu-id="0bef2-164">Use the style variable controls in the editor to change some global style values.</span></span>
1. <span data-ttu-id="0bef2-165">在编辑器顶部，在 **全局** 选项卡右侧的 **模块** 选项卡上，选择必须设置样式的模块类型。</span><span class="sxs-lookup"><span data-stu-id="0bef2-165">At the top of the editor, on the **Modules** tab to the right of the **Global** tab, select a module type that must be styled.</span></span>
1. <span data-ttu-id="0bef2-166">使用样式控件更改模块类型的某些值。</span><span class="sxs-lookup"><span data-stu-id="0bef2-166">Use the style controls to change some values for the module type.</span></span>
1. <span data-ttu-id="0bef2-167">在准备好预览更改时，在命令栏上选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-167">When you're ready to preview your changes, select **Save** on the command bar.</span></span>
1. <span data-ttu-id="0bef2-168">返回到打开的预览浏览器窗口，然后刷新它。</span><span class="sxs-lookup"><span data-stu-id="0bef2-168">Return to the open preview browser window, and refresh it.</span></span> <span data-ttu-id="0bef2-169">全浏览器窗口预览对于检查不同视图断点、不同浏览器和不同设备平台上的样式更改很有用。</span><span class="sxs-lookup"><span data-stu-id="0bef2-169">The full-browser-window preview is useful for checking style changes at different view breakpoints, in different browsers, and on different device platforms.</span></span>
1. <span data-ttu-id="0bef2-170">在完成并验证所有更改后，在编辑器的右上方选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-170">When all changes have been completed and validated, select **Finish editing** in the upper right of the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="0bef2-171">如果您在编辑当前在站点上处于活动状态的样式预设，将会在编辑器中看到一个蓝色的 **活动** 标记。</span><span class="sxs-lookup"><span data-stu-id="0bef2-171">If you're editing the style preset that is currently active on your site, you will see a blue **Active** badge in the editor.</span></span> <span data-ttu-id="0bef2-172">此标记指示该预设当前在您的网站上处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="0bef2-172">This badge indicates that the preset is currently live on your website.</span></span> <span data-ttu-id="0bef2-173">如果更改活动预设，请选择 **发布** 将这些更改推送到您的活动站点。</span><span class="sxs-lookup"><span data-stu-id="0bef2-173">If you change the active preset, select **Publish** to push those changes to your live site.</span></span>

## <a name="make-a-new-style-preset-active-on-your-live-site"></a><span data-ttu-id="0bef2-174">在活动站点上让新样式预设进入活动状态</span><span class="sxs-lookup"><span data-stu-id="0bef2-174">Make a new style preset active on your live site</span></span>

<span data-ttu-id="0bef2-175">要在站点上将样式预设设置为新活动预设，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0bef2-175">To set a style preset as the new active preset on your site, follow these steps.</span></span>

- <span data-ttu-id="0bef2-176">在以下位置之一选择 **设置为活动按钮**：</span><span class="sxs-lookup"><span data-stu-id="0bef2-176">Select the **Set as active button** in one of these places:</span></span>

    - <span data-ttu-id="0bef2-177">样式预设编辑器中的命令栏</span><span class="sxs-lookup"><span data-stu-id="0bef2-177">The command bar in the style preset editor</span></span>
    - <span data-ttu-id="0bef2-178">**站点设置 \> 设计** 处 **样式预设** 选项卡上主视图中任一可用预设对应的省略号菜单 (**...**)</span><span class="sxs-lookup"><span data-stu-id="0bef2-178">The ellipsis menu (**...**) for any available preset in the main view on the **Style presets** tab at **Site Settings \> Design**</span></span>

<span data-ttu-id="0bef2-179">预设的样式值将在面向公众的整个网站上进入活动状态。</span><span class="sxs-lookup"><span data-stu-id="0bef2-179">The preset's style values are made active across your public-facing website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bef2-180">其他资源</span><span class="sxs-lookup"><span data-stu-id="0bef2-180">Additional resources</span></span>

[<span data-ttu-id="0bef2-181">添加徽标</span><span class="sxs-lookup"><span data-stu-id="0bef2-181">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0bef2-182">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="0bef2-182">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0bef2-183">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="0bef2-183">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0bef2-184">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="0bef2-184">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0bef2-185">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="0bef2-185">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0bef2-186">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="0bef2-186">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0bef2-187">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="0bef2-187">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0bef2-188">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="0bef2-188">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
