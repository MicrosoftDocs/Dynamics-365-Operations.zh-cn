---
title: "配置 POS 的屏幕布局"
description: "此主题提供有关 Microsoft Dynamics 365 for Retail 销售点 (POS) 体验的屏幕布局的信息。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: d1ee1b873839697eaee83effb3ca4f95dcf7b9a7
ms.contentlocale: zh-cn
ms.lasthandoff: 06/29/2017


---

# <a name="configure-screen-layouts-for-pos"></a><span data-ttu-id="f0ad5-103">配置 POS 的屏幕布局</span><span class="sxs-lookup"><span data-stu-id="f0ad5-103">Configure screen layouts for POS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f0ad5-104">此主题提供有关 Microsoft Dynamics 365 for Retail 销售点 (POS) 体验的屏幕布局的信息。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-104">This topic provides information about screen layouts for the Microsoft Dynamics 365 for Retail point of sale (POS) experiences.</span></span>

<span data-ttu-id="f0ad5-105">可使用为商店、收银机和/或用户分配的视觉配置文件和屏幕布局，配置 Microsoft Dynamics 365 for Retail 销售点 (POS) 用户界面。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-105">The Microsoft Dynamics 365 for Retail point of sale (POS) user interface can be configured using a combination of visual profiles and screen layouts, assigned to stores, registers, and/or users.</span></span>

## <a name="visual-profile"></a><span data-ttu-id="f0ad5-106">可视化配置文件</span><span class="sxs-lookup"><span data-stu-id="f0ad5-106">Visual profile</span></span>
<span data-ttu-id="f0ad5-107">视觉配置文件分配给收银机，用于指定收银机特定且在用户中共享的视觉元素。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-107">Visual profiles are assigned to registers and are used to specify the visual elements that are register-specific and shared across users.</span></span> <span data-ttu-id="f0ad5-108">任何登录收银机的用户都将看到相同的主题、颜色和图像。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-108">Any user who logs into the register will have the same theme, colors, and images.</span></span> 

<span data-ttu-id="f0ad5-109">**配置文件编号** - 配置文件编号是可视化配置文件的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-109">**Profile number** - The profile number is the unique identifier for the Visual profile.</span></span> 

<span data-ttu-id="f0ad5-110">**描述** - 可通过描述指定有意义的名称，帮助确定适合您的情况的配置文件。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-110">**Description** - The description allows you to specify a meaningful name that will help to identify the correct profile for your situation.</span></span>

<span data-ttu-id="f0ad5-111">**主题** - 用户可在“浅色”或“深色”两种应用程序主题之间选择。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-111">**Theme** - Users can choose between the Light or Dark application themes.</span></span> <span data-ttu-id="f0ad5-112">这些设置应用整个应用程序中的自提和背景颜色。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-112">These settings impact the font and background colors throughout the app.</span></span>

<span data-ttu-id="f0ad5-113">**个性色** - 个性色在整个 POS 中用于区分或突出显示特定视觉元素，如标题、命令按钮或超链接。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-113">**Accent color** - The accent color is used throughout the POS to differentiate or highlight certain visual elements such as tiles, command buttons, or hyperlinks.</span></span> <span data-ttu-id="f0ad5-114">这些元素通常可操作。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-114">These elements are typically actionable.</span></span>

<span data-ttu-id="f0ad5-115">**标题颜色** - 用户可通过标题颜色配置页标题的颜色，以便满足零售商的品牌需求。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-115">**Header color** - The header color allows the user to configure the color of the page header to meet the branding needs of the retailer.</span></span> <span data-ttu-id="f0ad5-116">只有 Dynamics 365 for Retail 版本 1611 中才有此功能。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-116">This feature is only available in Dynamics 365 for Retail version 1611.</span></span>

<span data-ttu-id="f0ad5-117">**登录背景** - 用户可为登录屏幕指定背景图像。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-117">**Login backgrounds** - Users can specify a background image for the login screen.</span></span> <span data-ttu-id="f0ad5-118">背景图像的文件大小应尽量小，因为存储和加载大型文件可能影响应用程序的行为和性能。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-118">The file size of background images should be kept as small as possible, as storing and loading large files can have an impact on the application behavior and performance.</span></span>

<span data-ttu-id="f0ad5-119">**应用程序背景** - POS 也可以将图像用作整个应用程序中的背景，以代替纯色主题色。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-119">**Application background** - The POS can also use an image as a background throughout the application in place of the solid theme color.</span></span> <span data-ttu-id="f0ad5-120">就像登录背景，建议文件大小尽量小。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-120">As with the login backgrounds, it is advised to keep the file size as minimal as possible.</span></span>

## <a name="screen-layouts"></a><span data-ttu-id="f0ad5-121">屏幕布局</span><span class="sxs-lookup"><span data-stu-id="f0ad5-121">Screen layouts</span></span>
<span data-ttu-id="f0ad5-122">屏幕布局配置决定 POS“欢迎”屏幕和“交易记录”屏幕中的 UI 控件的操作、内容和位置。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-122">Screen layout configuration determines the actions, content, and placement of UI controls in the POS Welcome screen and Transaction screen.</span></span> 

<span data-ttu-id="f0ad5-123">**欢迎屏幕**- 在大多数情况下，“欢迎”屏幕是用户首次登录 POS 时看到的页面。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-123">**Welcome screen**- In most cases, the Welcome screen is the page that users will see when they first log into POS.</span></span> <span data-ttu-id="f0ad5-124">“欢迎”屏幕中可以包含品牌图像和用于访问 POS 操作的按钮网格。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-124">The Welcome screen can consist of a branding image and button grids that provide access to POS operations.</span></span> <span data-ttu-id="f0ad5-125">此处通常放置不特定于当前交易记录的操作。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-125">Typically, operations that are not specific to the current transaction are placed here.</span></span> 

<span data-ttu-id="f0ad5-126">**交易记录屏幕** -“交易记录”屏幕是 POS 中用于处理销售交易记录和订单的主屏幕。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-126">**Transaction screen** - The Transaction screen is the main screen in POS for processing sales transactions and orders.</span></span> <span data-ttu-id="f0ad5-127">可以使用屏幕布局设计器配置“交易记录”屏幕。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-127">The Transaction screen can be configured using the Screen layout designer.</span></span> 

<span data-ttu-id="f0ad5-128">**默认开始屏幕** - 有些零售商倾向于收银员在登录后直接进入“交易记录”屏幕。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-128">**Default start screen** - Some retailers prefer that the cashier navigate directly to the Transaction screen after logging in.</span></span> <span data-ttu-id="f0ad5-129">用户可通过默认开始屏幕设置为每种屏幕布局设置此项。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-129">The default start screen setting allows users to set this for each screen layout.</span></span>

### <a name="assignment"></a><span data-ttu-id="f0ad5-130">赋值</span><span class="sxs-lookup"><span data-stu-id="f0ad5-130">Assignment</span></span>

<span data-ttu-id="f0ad5-131">可在商店、收银机或用户级别分配屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-131">Screen layouts can be assigned at the store, register, or user level.</span></span> <span data-ttu-id="f0ad5-132">用户的分配将覆盖收银机和商店的分配，而收银机分配则覆盖商店分配。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-132">The user assignment overrides the register and store assignment, and the register assignment overrides the store assignment.</span></span> <span data-ttu-id="f0ad5-133">在简单方案中（即无论任何收银机或角色，所有用户都使用相同布局），只能在商店设计屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-133">In a simple scenario where all users use the same layout regardless of register or role, the screen layout can be set only at the store.</span></span> <span data-ttu-id="f0ad5-134">如果特定收银机或用户需要定制布局，可以相应地为其分配。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-134">In cases where certain registers or users require specialized layouts, they can be assigned appropriately.</span></span>

### <a name="layout-sizes"></a><span data-ttu-id="f0ad5-135">布局大小</span><span class="sxs-lookup"><span data-stu-id="f0ad5-135">Layout sizes</span></span>

<span data-ttu-id="f0ad5-136">此功能仅适用于 Dynamics 365 for Retail 版本 1611。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-136">This feature only applies to Dynamics 365 for Retail version 1611.</span></span> <span data-ttu-id="f0ad5-137">由于许多情况下屏幕布局可以跨多种屏幕大小和分辨率下使用，所以用户可以为每种配置自己的布局和内容。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-137">Because in many cases screen layouts can be used across multiple screen sizes and resolutions, users can configure their layout and content for each.</span></span> <span data-ttu-id="f0ad5-138">POS 应用程序将在启动时自动为设备选择最接近的布局大小。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-138">The POS application will automatically choose the closest layout size for the device at the time of startup.</span></span> <span data-ttu-id="f0ad5-139">屏幕布局中还可以同时包含完整和紧凑设备的配置。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-139">A screen layout can also contain configurations for both full and compact devices.</span></span> <span data-ttu-id="f0ad5-140">此配置允许为用户分配一个屏幕布局，而该屏幕布局支持商店内的多种尺寸和外形。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-140">This configuration allows a user to be assigned to a single screen layout that will work across various sizes and form factors within the store.</span></span> 

<span data-ttu-id="f0ad5-141">**现代 POS - 完整型** - 完整型布局通常最适合较大显示器，如 PC 显示器或平板电脑。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-141">**Modern POS - Full** - Full layouts are typically best used for larger displays such as PC monitors or tablets.</span></span> <span data-ttu-id="f0ad5-142">用户可以选择包含哪些 UI 元素，决定其大小和位置，以及配置其详细属性。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-142">Users can choose which UI elements to include, determine their size and placement, and configure their detailed properties.</span></span> <span data-ttu-id="f0ad5-143">完整型布局同时支持垂直配置和水平配置。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-143">Full layouts support both portrait and landscape configurations.</span></span> 

<span data-ttu-id="f0ad5-144">**现代 POS - 紧凑型** - 紧凑型布局通常最适合手机或小平板电脑。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-144">**Modern POS - Compact** - Compact layouts are typically best used for phones or small tablets.</span></span> <span data-ttu-id="f0ad5-145">对于紧凑型设备，设计功能受到限制。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-145">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="f0ad5-146">用户可以为收据和总计窗格配置列和字段。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-146">Users can configure the columns and fields for the receipt and totals panes.</span></span>

### <a name="screen-layout-designer"></a><span data-ttu-id="f0ad5-147">屏幕布局设计器</span><span class="sxs-lookup"><span data-stu-id="f0ad5-147">Screen layout designer</span></span>

<span data-ttu-id="f0ad5-148">必须使用屏幕布局设计器配置屏幕布局中的每种布局大小。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-148">Each layout size within a screen layout must be configured using the Screen layout designer.</span></span> <span data-ttu-id="f0ad5-149">此设计器允许用户指定和配置“交易记录”屏幕的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-149">The designer allows users to specify and configure the UI elements of the Transaction screen.</span></span> <span data-ttu-id="f0ad5-150">只要用户访问应用程序，屏幕布局设计器都将使用 ClickOnce 下载、安装和启动应用程序的最新版本。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-150">The Screen layout designer uses ClickOnce to download, install, and launch the latest version of the application each time the user accesses it.</span></span> <span data-ttu-id="f0ad5-151">请务必检查使用 ClickOnce 的浏览器要求 — 某些浏览器（如 Chrome）需要扩展。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-151">Be sure to check browser requirements for using ClickOnce—some browsers, such as Chrome, require extensions.</span></span> 

<span data-ttu-id="f0ad5-152">**数字键盘** - 数字键盘是 POS“交易记录”屏幕中的主要用户输入。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-152">**Number pad** - The number pad is the main user input in the POS Transaction screen.</span></span> <span data-ttu-id="f0ad5-153">可将其配置为显示完整的屏幕键盘，这是触控屏的理想选择，也可以配置为仅显示输入字段，可在使用物理键盘时使用。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-153">It can be configured to show the entire on-screen pad, which is ideal for touchscreens, or only the input field, which can be used with a physical keyboard.</span></span> <span data-ttu-id="f0ad5-154">只有完整型布局中才有数字键盘设置。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-154">The number pad settings are available in the full layout only.</span></span> <span data-ttu-id="f0ad5-155">在 Dynamics 365 for Retail 版本 1611 中，紧凑型布局始终从“交易记录”屏幕中提供完整的数字键盘。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-155">In Dynamics 365 for Retail version 1611, compact layouts always have the full number pad available from the Transaction screen.</span></span>

<span data-ttu-id="f0ad5-156">**总计面板** - 可可将总计面板配置为一列或两列，以显示字段，如行计数、折扣金额、费用、小计和税。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-156">**Totals panel** - The totals panel can be configured in either one or two columns to show fields such as line count, discount amount, charges, subtotal, and tax.</span></span> <span data-ttu-id="f0ad5-157">在 Dynamics 365 for Retail 版本 1611 中，紧凑型布局仅支持单个总计列。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-157">In Dynamics 365 for Retail version 1611, compact layouts only support a single totals column.</span></span> 

<span data-ttu-id="f0ad5-158">**收据** - 收据面板中包含 POS 中处理的产品和服务的销售行、付款行和交货信息。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-158">**Receipt** - The receipt panel contains the sales lines, payment lines, and delivery information for the products and services processed in the POS.</span></span> <span data-ttu-id="f0ad5-159">用户可以指定列、宽度和位置。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-159">Users can specify columns, widths, and placement.</span></span> <span data-ttu-id="f0ad5-160">在 Dynamics 365 for Retail 版本 1611 中的紧凑型布局内，还可以配置更多在主行下的行中显示的信息。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-160">In compact layouts in Dynamics 365 for Retail version 1611, you can also configure additional information which will appear in the row under the main line.</span></span> 

<span data-ttu-id="f0ad5-161">**客户卡** - 客户卡显示有关当前与交易关联的客户的信息。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-161">**Customer card** - The customer card shows information pertaining to the customer currently associated with the transaction.</span></span> <span data-ttu-id="f0ad5-162">可以将客户卡配置为隐藏或显示更多信息。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-162">The customer card can be configured to hide or show additional information.</span></span> 

<span data-ttu-id="f0ad5-163">**选项卡控件** - 可将选项卡控件放到屏幕布局中，也可以将其他控件（如数字键盘、客户卡或按钮窗格）放到选项卡内。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-163">**Tab control** - The tab control can be placed onto the screen layout, and other controls such as the number pad, customer card, or button grids can be placed inside the tab.</span></span> <span data-ttu-id="f0ad5-164">选项卡控件是帮助用户在屏幕中放置更多内容的容器。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-164">The tab control is a container that helps users fit more content in the screen.</span></span> <span data-ttu-id="f0ad5-165">选项卡控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-165">The tab control is only available for full layouts.</span></span> 

<span data-ttu-id="f0ad5-166">**图像** - 图像控件可用于在交易记录屏幕中显示商店徽标或其他品牌图像。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-166">**Image** - The image control can be used to show the store logo or other branding image on the transaction screen.</span></span> <span data-ttu-id="f0ad5-167">图像控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-167">The image control is only available for full layouts.</span></span> 

<span data-ttu-id="f0ad5-168">**推荐产品** - 如果为环境配置了推荐产品控件，则将根据机器学习显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-168">**Recommended products** - If configured for the environment, the recommended products control will show product suggestions based on machine learning.</span></span> <span data-ttu-id="f0ad5-169">推荐产品控件仅可用于 Dynamics 365 for Retail 版本 1611 中的完整型布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-169">The recommended products control is only available for full layouts in Dynamics 365 for Retail version 1611.</span></span> <span data-ttu-id="f0ad5-170">**自定义控件**- 自定义控件充当屏幕布局内的占位符，供用户为自定义内容预留空间。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-170">**Custom control **- The custom control acts as a placeholder within the screen layout to allows users to reserve space for custom content.</span></span> <span data-ttu-id="f0ad5-171">自定义控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="f0ad5-171">The custom control is only available for full layouts.</span></span>

<a name="see-also"></a><span data-ttu-id="f0ad5-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0ad5-172">See also</span></span>
--------

[<span data-ttu-id="f0ad5-173">安装 Retail POS 布局设计器</span><span class="sxs-lookup"><span data-stu-id="f0ad5-173">Install the Retail POS Layout designer</span></span>](install-pos-layout-designer.md)




