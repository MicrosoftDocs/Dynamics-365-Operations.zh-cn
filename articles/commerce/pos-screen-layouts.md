---
title: POS 用户界面视觉效果配置
description: 此主题提供有关 Dynamics 365 Commerce 销售点 (POS) 体验的屏幕布局的信息。
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2a6fdbc957a50adba38627bc37622c17ab4be419
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4410618"
---
# <a name="pos-user-interface-visual-configurations"></a><span data-ttu-id="3a1f7-103">POS 用户界面视觉效果配置</span><span class="sxs-lookup"><span data-stu-id="3a1f7-103">POS user interface visual configurations</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="3a1f7-104">可使用为商店、收银机和用户分配的视觉配置文件和屏幕布局，配置 Microsoft Dynamics 365 Commerce 销售点 (POS) 的用户界面 (UI)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-104">The user interface (UI) of the Microsoft Dynamics 365 Commerce point of sale (POS) can be configured by using a combination of visual profiles and screen layouts that are assigned to stores, registers, and users.</span></span> <span data-ttu-id="3a1f7-105">此主题介绍这些配置选项。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-105">This topic provides information about those configuration options.</span></span>

<span data-ttu-id="3a1f7-106">下图显示构成 POS UI 可配置项的各实体之间的关系。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-106">The following illustration shows the relationships among the various entities that make up the configurable aspects of the POS UI.</span></span>

![POS 屏幕布局实体](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a><span data-ttu-id="3a1f7-108">可视化配置文件</span><span class="sxs-lookup"><span data-stu-id="3a1f7-108">Visual profile</span></span>

<span data-ttu-id="3a1f7-109">视觉配置文件分配给收银机，用于指定收银机特定且在用户中共享的视觉元素。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-109">Visual profiles are assigned to registers, and they specify the visual elements that are register-specific and shared across users.</span></span> <span data-ttu-id="3a1f7-110">每位登录收银机的用户都将看到相同的主题、布局、颜色和图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-110">Every user who signs in to the register sees the same theme, layout, colors, and images.</span></span>

![采用浅色主题的 POS 欢迎使用屏幕](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![采用深色主题的 POS 交易记录屏幕](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- <span data-ttu-id="3a1f7-113">**配置文件编号** – 配置文件编号是可视化配置文件的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-113">**Profile number** – The profile number is the unique identifier of the visual profile.</span></span>
- <span data-ttu-id="3a1f7-114">**描述** - 您可以指定有意义的名称，帮助确定适合您的情况的配置文件。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-114">**Description** – You can specify a meaningful name that will help identify the correct profile for your situation.</span></span>
- <span data-ttu-id="3a1f7-115">**主题** – 您可以在 **浅色** 和 **深色** 两种应用程序主题之间选择。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-115">**Theme** – You can select between the **Light** and **Dark** application themes.</span></span> <span data-ttu-id="3a1f7-116">主题影响整个应用程序中的字体和背景色。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-116">The theme affects the font and background colors throughout the application.</span></span>
- <span data-ttu-id="3a1f7-117">**个性色** – 个性色在整个 POS 中用于区分或突出显示特定视觉元素，如标题、命令按钮和超链接。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-117">**Accent color** – The accent color is used throughout the POS to differentiate or highlight specific visual elements, such as tiles, command buttons, and hyperlinks.</span></span> <span data-ttu-id="3a1f7-118">这些元素通常可操作。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-118">Typically, these elements are actionable.</span></span>
- <span data-ttu-id="3a1f7-119">**标题颜色** – 您可以配置页标题的颜色，以便满足零售商的品牌需要。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-119">**Header color** – You can configure the color of the page header to meet the retailer's branding requirements.</span></span>
- <span data-ttu-id="3a1f7-120">**字体主题** – 可在 **标准** 和 **大** 字体方案之间选择。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-120">**Font scheme** – You can select between the **Standard** and **Large** font schemes.</span></span> <span data-ttu-id="3a1f7-121">字体方案影响整个应用程序的字体大小。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-121">The font scheme affects the font size throughout the application.</span></span> <span data-ttu-id="3a1f7-122">默认选择为 **标准**。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-122">The default selection is **Standard**.</span></span>
- <span data-ttu-id="3a1f7-123">**始终显示应用程序栏标签** – 如果开启了此选项，应用程序栏按钮下始终显示标签文本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-123">**Always show application bar labels** – When this option is turned on, the label text is always visible under the application bar buttons.</span></span>
- <span data-ttu-id="3a1f7-124">**布局** – 可在 **居中** 和 **靠右** 布局之间选择。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-124">**Layout** – You can select between the **Centered** and **Right** layouts.</span></span> <span data-ttu-id="3a1f7-125">布局影响登录屏幕中登录框的对齐。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-125">The layout affects the alignment of the sign-in box on the sign-in screen.</span></span> <span data-ttu-id="3a1f7-126">默认选择为 **居中**。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-126">The default selection is **Centered**.</span></span>
- <span data-ttu-id="3a1f7-127">**显示日期/时间** – 开启此选项之后，POS 标题和登录屏幕中将显示当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-127">**Show date/time** – When this option is turned on, the current date and time are shown in the POS header and on the sign-in screen.</span></span>
- <span data-ttu-id="3a1f7-128">**键盘** – 可在 **默认使用操作系统键盘** 和 **显示数字键盘** 之间选择以指定用于在登录屏幕中进行输入的默认键盘。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-128">**Keyboard** – You can select between **Default to OS keyboard** and **Show number pad** to specify the default keyboard that is used for input on the sign-in screen.</span></span> <span data-ttu-id="3a1f7-129">数字键盘是主要用于触控设备的虚拟键盘。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-129">The number pad is a virtual keyboard that is used primarily for touch-based devices.</span></span> <span data-ttu-id="3a1f7-130">默认选择为 **默认使用操作系统键盘**。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-130">The default selection is **Default to OS keyboard**.</span></span>
- <span data-ttu-id="3a1f7-131">**徽标图像** – 可指定登录屏幕中显示的徽标图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-131">**Logo image** – You can specify a logo image that is shown on the sign-in screen.</span></span> <span data-ttu-id="3a1f7-132">建议使用透明背景的图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-132">We recommend that you use an image that has a transparent background.</span></span> <span data-ttu-id="3a1f7-133">文件大小应尽量小，因为存储和加载大型文件可能影响应用程序的行为和性能。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-133">The file size should be kept as small as possible, because application behavior and performance can be affected when large files are stored and loaded.</span></span>
- <span data-ttu-id="3a1f7-134">**登录背景** – 您可以为登录屏幕指定背景图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-134">**Login background** – You can specify a background image for the sign-in screen.</span></span> <span data-ttu-id="3a1f7-135">背景图像的文件大小应尽量小。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-135">The file size of background images should be kept as small as possible.</span></span>
- <span data-ttu-id="3a1f7-136">**背景** – 您可以指定整个应用程序中使用的背景图像来代替纯色主题色。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-136">**Background** – You can specify a background image that is used instead of the solid theme color throughout the application.</span></span> <span data-ttu-id="3a1f7-137">对于登录屏幕的背景图像，文件大小应尽量小。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-137">As for background images for the sign-in screen, the file size should be kept as small as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="3a1f7-138">**靠右** 布局和日期/时间显示不适用于紧凑视图的登录屏幕。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-138">The **Right** layout and date/time display don't apply to the sign-in screen in compact view.</span></span>

<span data-ttu-id="3a1f7-139">您需要运行 **1090**（**收银机**）分发计划作业，来将最新的可视化配置文件配置同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-139">You need to run the **1090** (**Registers**) distribution schedule job to synchronize the latest visual profile configurations to the channel database.</span></span>

## <a name="screen-layouts"></a><span data-ttu-id="3a1f7-140">屏幕布局</span><span class="sxs-lookup"><span data-stu-id="3a1f7-140">Screen layouts</span></span>

<span data-ttu-id="3a1f7-141">屏幕布局配置决定 POS **欢迎** 屏幕和 **交易记录** 屏幕中的 UI 控件的操作、内容和位置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-141">Screen layout configurations determine the actions, content, and placement of UI controls on the POS **Welcome** screen and **Transaction** screen.</span></span>

![POS 屏幕布局视图](../commerce/media/POS-Screen-Layout-View.png)

- <span data-ttu-id="3a1f7-143">**欢迎屏幕** – 在大多数情况下，欢迎屏幕是用户首次登录 POS 时看到的页面。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-143">**Welcome screen** – In most cases, the welcome screen is the page that users see when they first sign in to the POS.</span></span> <span data-ttu-id="3a1f7-144">欢迎屏幕中可以包含品牌图像和用于访问 POS 操作的按钮网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-144">The welcome screen can consist of a branding image and button grids that provide access to POS operations.</span></span> <span data-ttu-id="3a1f7-145">此屏幕通常放置不特定于当前交易记录的操作。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-145">Typically, operations that aren't specific to the current transaction are put on this screen.</span></span>

    ![POS 欢迎屏幕](../commerce/media/POS-Welcome-Screen.png)

- <span data-ttu-id="3a1f7-147">**交易记录屏幕** – **交易记录** 屏幕是 POS 中用于处理销售交易记录和订单的主屏幕。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-147">**Transaction screen** – The **Transaction** screen is the main screen in the POS for processing sales transactions and orders.</span></span> <span data-ttu-id="3a1f7-148">内容和布局使用屏幕布局设计器配置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-148">The content and layout are configured by using the screen layout designer.</span></span>

    ![POS 交易记录屏幕](../commerce/media/POS-Transaction-Screen.png)

- <span data-ttu-id="3a1f7-150">**默认开始屏幕** – 有些零售商倾向于收银员在登录后直接进入 **交易记录** 屏幕。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-150">**Default start screen** – Some retailers prefer that cashiers go directly to the **Transaction** screen after sign-in.</span></span> <span data-ttu-id="3a1f7-151">**默认启动屏幕** 设置用于指定登录后每个屏幕布局显示的默认屏幕。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-151">The **Default start screen** setting lets you specify the default screen that appears after sign-in for each screen layout.</span></span>

### <a name="assignment"></a><span data-ttu-id="3a1f7-152">赋值</span><span class="sxs-lookup"><span data-stu-id="3a1f7-152">Assignment</span></span>

<span data-ttu-id="3a1f7-153">可在商店、收银机或用户级别分配屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-153">Screen layouts can be assigned at the store, register, or user level.</span></span> <span data-ttu-id="3a1f7-154">用户的分配将覆盖收银机和商店的分配，而收银机分配则覆盖商店分配。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-154">The user assignment overrides the register and store assignments, and the register assignment overrides the store assignment.</span></span> <span data-ttu-id="3a1f7-155">在简单方案中（即无论任何收银机或角色，所有用户都使用相同布局），只能在商店级别设计屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-155">In a simple scenario where all users use the same layout, regardless of register or role, the screen layout can be set only at the store level.</span></span> <span data-ttu-id="3a1f7-156">如果特定收银机或用户需要定制布局，可以为其分配这些布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-156">In scenarios where specific registers or users require specialized layouts, those layouts can be assigned.</span></span>

<span data-ttu-id="3a1f7-157">根据分配的屏幕布局级别，您需要运行 **1070**（**渠道配置**）、**1090**（**收银机**）和/或 **1060**（**人员**）分发计划作业，来将最新的屏幕布局配置同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-157">Depending on which level the screen layouts are assigned, you need to run the **1070** (**Channel configuration**), **1090** (**Registers**), and/or **1060** (**Staff**) distribution schedule jobs to synchronize the latest screen layout configurations to the channel database.</span></span>

### <a name="layout-sizes"></a><span data-ttu-id="3a1f7-158">布局大小</span><span class="sxs-lookup"><span data-stu-id="3a1f7-158">Layout sizes</span></span>

<span data-ttu-id="3a1f7-159">大多数 POS UI 可响应，而布局则会根据屏幕尺寸和方向自动调整大小和方向。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-159">Most aspects of the POS UI are responsive, and the layout is automatically resized and adjusted based on the screen size and orientation.</span></span> <span data-ttu-id="3a1f7-160">但是，必须为 POS **交易记录** 屏幕配置预期将使用的每种屏幕分辨率。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-160">However, the POS **Transaction** screen must be configured for every screen resolution that is expected.</span></span>

<span data-ttu-id="3a1f7-161">启动时，POS 应用程序将自动选择为设备配置的最接近的布局尺寸。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-161">At startup, the POS application automatically selects the closest layout size that is configured for the device.</span></span> <span data-ttu-id="3a1f7-162">屏幕布局中也可以包含横向和纵向模式的配置，以及全尺寸设备和精简型设备的配置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-162">A screen layout can also contain configurations for both landscape and portrait modes, and for both full-size and compact devices.</span></span> <span data-ttu-id="3a1f7-163">因此，可以为用户分配一个屏幕布局，而该屏幕布局支持商店内的多种尺寸和外形。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-163">Therefore, users can be assigned to a single screen layout that works across various sizes and form factors that are used in the store.</span></span>

![POS 布局尺寸](../commerce/media/POS-Screen-Layout-Sizes.png)

- <span data-ttu-id="3a1f7-165">**名称** – 您可以输入有意义的名称来标识屏幕大小。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-165">**Name** – You can enter a meaningful name to identify the screen size.</span></span>
- <span data-ttu-id="3a1f7-166">**布局类型** – POS 应用程序可以以各种模式显示其 UI，以便在给定设备上提供最佳用户体验。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-166">**Layout type** – The POS application can show its UI in various modes to provide the best user experience on a given device.</span></span>

    - <span data-ttu-id="3a1f7-167">**现代 POS – 完整型** – 完整型布局通常最适合较大显示器，如台式机显示器或平板电脑。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-167">**Modern POS – Full** – Full layouts are typically best for larger displays, such as desktop monitors and tablets.</span></span> <span data-ttu-id="3a1f7-168">您可以可以选择要包含的 UI 元素，指定这些元素的尺寸和位置，并配置它们的详细属性。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-168">You can select the UI elements to include, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="3a1f7-169">完整型布局同时支持垂直配置和水平配置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-169">Full layouts support both portrait and landscape configurations.</span></span>
    - <span data-ttu-id="3a1f7-170">**现代 POS – 紧凑型** – 紧凑型布局通常最适合手机和小平板电脑。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-170">**Modern POS – Compact** – Compact layouts are typically best for phones and small tablets.</span></span> <span data-ttu-id="3a1f7-171">对于紧凑型设备，设计功能受到限制。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-171">The design possibilities for compact devices are limited.</span></span> <span data-ttu-id="3a1f7-172">您可以为收据和总计窗格配置列和字段。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-172">You can configure the columns and fields for the receipt and totals panels.</span></span>

- <span data-ttu-id="3a1f7-173">**宽度/高度** –这些值以像素为单位表示布局应采用的有效屏幕尺寸。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-173">**Width/Height** – These values represent the effective screen size, in pixels, that is expected for the layout.</span></span> <span data-ttu-id="3a1f7-174">请注意，某些操作系统对高分辨率显示器使用缩放功能。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-174">Remember that some operating systems use scaling for high-resolution displays.</span></span>

> [!TIP]
> <span data-ttu-id="3a1f7-175">可以通过在应用程序中查看分辨率了解 POS 需要的布局尺寸。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-175">You can learn the layout size that is required for a POS screen by viewing the resolution in the app.</span></span> <span data-ttu-id="3a1f7-176">启动 POS，然后转至 **设置 \> 会话信息**。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-176">Start the POS, and go to **Settings \> Session information**.</span></span> <span data-ttu-id="3a1f7-177">POS 显示当前加载的屏幕布局，布局尺寸和应用程序窗口的分辨率。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-177">POS shows the screen layout that is currently loaded, the layout size, and the resolution of the app window.</span></span>

![POS 会话信息页显示当前加载的屏幕布局，布局尺寸和应用程序窗口的分辨率](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a><span data-ttu-id="3a1f7-179">按钮网格</span><span class="sxs-lookup"><span data-stu-id="3a1f7-179">Button grids</span></span>

<span data-ttu-id="3a1f7-180">对于屏幕布局的各布局尺寸，可以为 POS 欢迎屏幕和 **交易记录** 屏幕配置和分配按钮网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-180">For each layout size in a screen layout, you can configure and assign button grids for the POS welcome screen and **Transaction** screen.</span></span> <span data-ttu-id="3a1f7-181">欢迎屏幕的按钮网格自动从左到右，从最小编号（欢迎屏幕 1）到最大编号分布。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-181">Button grids for the welcome screen are automatically laid out from left to right, from the lowest number (Welcome screen 1) to the highest number.</span></span>

<span data-ttu-id="3a1f7-182">在完整型 POS 布局中，按钮网格的放置在屏幕布局设计器中指定。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-182">In Full POS layouts, the placement of button grids is specified in the screen layout designer.</span></span>

<span data-ttu-id="3a1f7-183">在精简型 POS 布局中，按钮网格自动从上到下，从最小编号（“交易记录”屏幕 1）到最大编号分布。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-183">In Compact POS layouts, the button grids are automatically laid out from top to bottom, from the lowest number (Transaction screen 1) to the highest number.</span></span> <span data-ttu-id="3a1f7-184">可以在 **操作** 菜单中访问这些按钮网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-184">They can be accessed on the **Actions** menu.</span></span>

![精简型布局按钮网格](../commerce/media/Compact-View-Button-Grids.png)

### <a name="images"></a><span data-ttu-id="3a1f7-186">图像</span><span class="sxs-lookup"><span data-stu-id="3a1f7-186">Images</span></span>

<span data-ttu-id="3a1f7-187">对于屏幕布局中的每种布局尺寸，您可以指定 POS UI 中要包含的图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-187">For each layout size in a screen layout, you can specify images to include in the POS UI.</span></span> <span data-ttu-id="3a1f7-188">对于完整型 POS 布局，只能为欢迎屏幕指定一个图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-188">For Full POS layouts, a single image can be specified for the welcome screen.</span></span> <span data-ttu-id="3a1f7-189">此图像显示为左侧的第一个 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-189">This image appears as the first UI element on the left.</span></span> <span data-ttu-id="3a1f7-190">在 **交易记录** 屏幕上，可以将图像用作标签图像或徽标。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-190">On the **Transaction** screen, images can be used as tab images or as a logo.</span></span> <span data-ttu-id="3a1f7-191">精简型 POS 布局不使用这些图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-191">Compact POS layouts don't use these images.</span></span>

### <a name="screen-layout-designer"></a><span data-ttu-id="3a1f7-192">屏幕布局设计器</span><span class="sxs-lookup"><span data-stu-id="3a1f7-192">Screen layout designer</span></span>

<span data-ttu-id="3a1f7-193">可使用屏幕布局设计器为纵向和横向模式下的各布局尺寸配置 POS **交易记录** 屏幕的各设置，也可以同时为完整型和精简型布局配置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-193">The screen layout designer lets you configure various aspects of the POS **Transaction** screen for each layout size, in both portrait and landscape modes, and for both Full and Compact layouts.</span></span> <span data-ttu-id="3a1f7-194">只要用户访问应用程序，屏幕布局设计器都将使用 ClickOnce 部署技术下载、安装和启动应用程序的最新版本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-194">The screen layout designer uses the ClickOnce deployment technology to download, install, and start the latest version of the application every time that users access it.</span></span> <span data-ttu-id="3a1f7-195">请确保检查 ClickOnce 的浏览器要求。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-195">Be sure to check the browser requirements for ClickOnce.</span></span> <span data-ttu-id="3a1f7-196">某些浏览器（如 Google Chrome）需要扩展。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-196">Some browsers, such as Google Chrome, require extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a1f7-197">必须为定义供 POS 使用的每个布局尺寸配置一个屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-197">You must configure a screen layout for each layout size that is defined and that is used by the POS.</span></span>

### <a name="full-layout-designer"></a><span data-ttu-id="3a1f7-198">完整型布局设计器</span><span class="sxs-lookup"><span data-stu-id="3a1f7-198">Full layout designer</span></span>

<span data-ttu-id="3a1f7-199">用户可使用完整型布局设计器将 UI 控件拖到 POS **交易记录** 屏幕上和配置这些控件的设置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-199">The Full layout designer lets users drag UI controls onto the POS **Transaction** screen and configure the settings of those controls.</span></span>

![POS 完整型布局设计器（横向）](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- <span data-ttu-id="3a1f7-201">**导入布局/导出布局** – 可将将 POS 屏幕布局设计作为 XML 文件导出和导入，以便轻松重复使用和在环境之间共享。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-201">**Import layout/Export layout** – You can export and import POS screen layout designs as XML files, so that you can easily reuse and share them across environments.</span></span> <span data-ttu-id="3a1f7-202">请务必导入正确布局尺寸的布局设计。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-202">It's important that you import layout designs for the correct layout sizes.</span></span> <span data-ttu-id="3a1f7-203">否则，UI 元素可能不能正确适应屏幕。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-203">Otherwise, UI elements might not fit correctly on the screen.</span></span>
- <span data-ttu-id="3a1f7-204">**横向/纵向** – 如果 POS 设备允许用户在横向和纵向模式之间切换，则您必须为各模式定义屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-204">**Landscape/Portrait** – If the POS device lets users switch between landscape and portrait modes, you must define a screen layout for each mode.</span></span> <span data-ttu-id="3a1f7-205">POS 将自动检测屏幕旋转方向并显示正确的布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-205">The POS automatically detects screen rotation and shows the correct layout.</span></span>
- <span data-ttu-id="3a1f7-206">**布局网格** – POS 布局设计器使用 4 像素网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-206">**Layout grid** – The POS layout designer uses a 4-pixel grid.</span></span> <span data-ttu-id="3a1f7-207">UI 控件“”与网格啮合，帮助您正确对齐内容。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-207">UI controls "snap" to the grid to help you correctly align the content.</span></span>
- <span data-ttu-id="3a1f7-208">**设计器缩放** – 可以缩放设计器视图，以便更好查看 POS 屏幕上的内容。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-208">**Designer zoom** – You can zoom the designer view in and out to better view the content on the POS screen.</span></span> <span data-ttu-id="3a1f7-209">POS 上的屏幕分辨率与设计器中使用的屏幕分辨率差别很大时，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-209">This feature is useful when the screen resolution on the POS differs greatly from the resolution of the screen that is used in the designer.</span></span>
- <span data-ttu-id="3a1f7-210">**显示/隐藏导航栏** – 对于完整型 POS 布局，您可以选择 **交易记录** 屏幕中是否显示左侧导航栏。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-210">**Show/hide navigation bar** – For Full POS layouts, you can select whether the left navigation bar is visible on the **Transaction** screen.</span></span> <span data-ttu-id="3a1f7-211">此功能对分辨率较低的显示器很有用。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-211">This feature is helpful for displays that have a lower resolution.</span></span> <span data-ttu-id="3a1f7-212">若要设置可见性，请在设计器中右键单击导航栏，然后选中或清除 **始终显示** 复选框。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-212">To set the visibility, right-click the navigation bar in the designer, and select or clear the **Always visible** check box.</span></span> <span data-ttu-id="3a1f7-213">如果导航栏已隐藏，POS 用户仍然可以使用左上角的菜单访问。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-213">If the navigation bar is hidden, POS users can still access it by using the menu in the upper left.</span></span>

    ![显示/隐藏导航栏](../commerce/media/Navigation-Bar.PNG)

- <span data-ttu-id="3a1f7-215">**POS 控件** – POS 布局设计器支持以下控件。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-215">**POS controls** – The POS layout designer supports the following controls.</span></span> <span data-ttu-id="3a1f7-216">可通过右键单击和使用快捷菜单配置大量控件。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-216">You can configure many controls by right-clicking and using the shortcut menu.</span></span>

    ![POS UI 控件](../commerce/media/POS-UI-Controls.png)

    - <span data-ttu-id="3a1f7-218">**数字键盘** - 数字键盘是 POS **交易记录** 屏幕中的主要用户输入机制。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-218">**Number pad** – The number pad is the main mechanism for user input on the POS **Transaction** screen.</span></span> <span data-ttu-id="3a1f7-219">您可以配置控件，以便显示完整型的数字键盘。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-219">You can configure the control so that the full number pad is shown.</span></span> <span data-ttu-id="3a1f7-220">此选项是触控屏设备的理想选择。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-220">This option is ideal for touchscreen devices.</span></span> <span data-ttu-id="3a1f7-221">您也可以将其配置为仅显示输入字段。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-221">Alternatively, you can configure it so that only the input field is shown.</span></span> <span data-ttu-id="3a1f7-222">在这种情况下，使用物理键盘进行输入。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-222">In this case, a physical keyboard is used for input.</span></span> <span data-ttu-id="3a1f7-223">只有完整型布局中才有数字键盘设置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-223">The number pad settings are available only for Full layouts.</span></span> <span data-ttu-id="3a1f7-224">对于精简型布局，**交易记录** 屏幕上始终显示完整型的数字键盘。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-224">For Compact layouts, the full number pad is always shown on the **Transaction** screen.</span></span>
    - <span data-ttu-id="3a1f7-225">**总计面板** - 您可以将总计面板配置为一列或两列，以显示值，如行计数、折扣金额、费用、小计和税。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-225">**Totals panel** – You can configure the totals panel in either one column or two columns, to show values such as the line count, discount amount, charges, subtotal, and tax.</span></span> <span data-ttu-id="3a1f7-226">精简型布局仅支持一列。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-226">Compact layouts support only a single column.</span></span>
    - <span data-ttu-id="3a1f7-227">**收据面板** – 收据面板中包含 POS 中处理的产品和服务的销售行、付款行和交货信息。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-227">**Receipt panel** – The receipt panel contains the sales lines, payment lines, and delivery information for the products and services that are processed in the POS.</span></span> <span data-ttu-id="3a1f7-228">您可以指定列、宽度和位置。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-228">You can specify columns, widths, and placement.</span></span> <span data-ttu-id="3a1f7-229">在精简型布局中，也可以配置在主行下的行中显示的更多信息。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-229">In Compact layouts, you can also configure additional information that appears in the row under the main line.</span></span>
    - <span data-ttu-id="3a1f7-230">**客户卡** – 客户卡显示有关与当前交易关联的客户的信息。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-230">**Customer card** – The customer card shows information about the customer who is associated with the current transaction.</span></span> <span data-ttu-id="3a1f7-231">您可以将客户卡配置为隐藏或显示更多信息。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-231">You can configure the customer card to hide or show additional information.</span></span>
    - <span data-ttu-id="3a1f7-232">**选项卡控件** – 您可以向屏幕布局添加选项卡控件，然后在其中放置其他控件（如数字键盘、客户卡或按钮窗格）。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-232">**Tab control** – You can add the tab control to a screen layout, and then put other controls, such as the number pad, customer card, or button grids, in it.</span></span> <span data-ttu-id="3a1f7-233">选项卡控件是帮助您在屏幕中放置更多内容的容器。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-233">The tab control is a container that helps you fit more content on the screen.</span></span> <span data-ttu-id="3a1f7-234">选项卡控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-234">The tab control is available only for Full layouts.</span></span>
    - <span data-ttu-id="3a1f7-235">**图像** -您可以使用 图像控件在 **交易记录** 屏幕中显示商店徽标或其他品牌图像。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-235">**Image** – You can use the image control to show the store's logo or another branding image on the **Transaction** screen.</span></span> <span data-ttu-id="3a1f7-236">图像控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-236">The image control is available only for Full layouts.</span></span>
    - <span data-ttu-id="3a1f7-237">**推荐产品** – 如果为环境配置了推荐产品控件，则将根据机器学习显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-237">**Recommended products** – If the recommended products control is configured for the environment, it shows product suggestions, based on machine learning.</span></span>
    - <span data-ttu-id="3a1f7-238">**自定义控件** – 自定义控件充当屏幕布局内的占位符，用于为自定义内容预留空间。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-238">**Custom control** – The custom control acts as a placeholder in the screen layout and lets you reserve space for custom content.</span></span> <span data-ttu-id="3a1f7-239">自定义控件仅可用于完整型布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-239">The custom control is available only for Full layouts.</span></span>

### <a name="compact-layout-designer"></a><span data-ttu-id="3a1f7-240">精简型布局设计器</span><span class="sxs-lookup"><span data-stu-id="3a1f7-240">Compact layout designer</span></span>

<span data-ttu-id="3a1f7-241">和完整型布局设计器一样，精简型布局设计器可用于针对手机和小型平板电脑配置 POS 屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-241">Like the Full layout designer, the Compact layout designer lets you configure the POS screen layout for phones and small tablets.</span></span> <span data-ttu-id="3a1f7-242">但是，在这种情况下，布局本身是固定的。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-242">However, in this case, the layout itself is fixed.</span></span> <span data-ttu-id="3a1f7-243">可通过右键单击和使用快捷菜单在布局中配置控件。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-243">You can configure the controls in the layout by right-clicking and using the shortcut menu.</span></span> <span data-ttu-id="3a1f7-244">但是，您不能为其他内容使用拖放操作。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-244">However, you can't use drag-and-drop operations for additional content.</span></span>

![精简型布局设计器](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a><span data-ttu-id="3a1f7-246">按钮网格设计器</span><span class="sxs-lookup"><span data-stu-id="3a1f7-246">Button grid designer</span></span>

<span data-ttu-id="3a1f7-247">可通过按钮网格设计器为完整型布局和精简型布局配置 POS 欢迎屏幕和 **交易记录** 屏幕上可使用的按钮网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-247">The button grid designer lets you configure button grids that can be used on the POS welcome screen and **Transaction** screen for both Full and Compact layouts.</span></span> <span data-ttu-id="3a1f7-248">可跨布局和布局类型使用同一个按钮网格。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-248">The same button grid can be used across layouts and layout types.</span></span> <span data-ttu-id="3a1f7-249">和屏幕布局设计器一样，只要用户访问应用程序，按钮网格设计器都将使用 ClickOnce 部署技术下载、安装和启动应用程序的最新版本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-249">Like the screen layout designer, the button grid designer uses the ClickOnce deployment technology to download, install, and start the latest version of the application every time that users access it.</span></span> <span data-ttu-id="3a1f7-250">请确保检查 ClickOnce 的浏览器要求。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-250">Be sure to check the browser requirements for ClickOnce.</span></span> <span data-ttu-id="3a1f7-251">某些浏览器（如 Google Chrome）需要扩展。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-251">Some browsers, such as Google Chrome, require extensions.</span></span>

![按钮网格设计器](../commerce/media/Button-Grid-Designer.png)

- <span data-ttu-id="3a1f7-253">**新按钮** – 单击以向按钮网格添加新按钮。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-253">**New button** – Click to add a new button to the button grid.</span></span> <span data-ttu-id="3a1f7-254">默认情况下，新按钮在网格左上角显示。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-254">By default, new buttons appear in the upper-left corner of the grid.</span></span> <span data-ttu-id="3a1f7-255">但是，您可以通过在布局中拖放来重新安排按钮。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-255">However, you can arrange buttons by dragging them in the layout.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3a1f7-256">按钮网格的内容可能重叠。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-256">The contents of the button grid can overlap.</span></span> <span data-ttu-id="3a1f7-257">安排按钮时，请确保按钮不会彼此遮挡。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-257">When you arrange buttons, make sure that they don't hide other buttons.</span></span>

- <span data-ttu-id="3a1f7-258">**新设计** – 单击以通过指定每行和每列的按钮数来自动设置按钮网格布局。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-258">**New design** – Click to automatically set up a button grid layout by specifying the number of buttons per row and column.</span></span>
- <span data-ttu-id="3a1f7-259">**按钮属性** – 您可以通过右键单击按钮和使用快捷菜单配置按钮属性。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-259">**Button properties** – You can configure button properties by right-clicking the button and using the shortcut menu.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3a1f7-260">某些按钮网格设置仅适用于 Enterprise POS，不适用于 Modern POS 或 Cloud POS。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-260">Some button grid settings apply only to Enterprise POS, not to Modern POS or Cloud POS.</span></span>

    ![按钮网格按钮属性](../commerce/media/Button-grid-button-properties.png)

    - <span data-ttu-id="3a1f7-262">**操作** – 在适用 POS 操作列表中，选择在 POS 中单击按钮时调用的操作。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-262">**Action** – In the list of applicable POS operations, select the operation that is invoked when the button is clicked in the POS.</span></span>

        <span data-ttu-id="3a1f7-263">有关支持的 POS 操作的列表，请参阅[销售点 (POS) 联机和脱机操作](pos-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-263">For the list of supported POS operations, see [Online and offline point of sale (POS) operations](pos-operations.md).</span></span>

    - <span data-ttu-id="3a1f7-264">**操作参数** – 某些 POS 操作在调用时使用更多参数。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-264">**Action parameters** – Some POS operations use additional parameters when they are invoked.</span></span> <span data-ttu-id="3a1f7-265">例如，对于“添加产品”操作，用户可以指定要添加的产品。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-265">For example, for the Add product operation, users can specify the product to add.</span></span>
    - <span data-ttu-id="3a1f7-266">**按钮稳步** – 指定 POS 中的按钮上显示的文本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-266">**Button text** – Specify the text that appears on the button in the POS.</span></span>
    - <span data-ttu-id="3a1f7-267">**隐藏按钮文本** – 此复选框用于隐藏或显示按钮文本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-267">**Hide button text** – Use this check box to hide or show the button text.</span></span> <span data-ttu-id="3a1f7-268">仅显示一个按钮的小型按钮通常会显示按钮文本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-268">Button text is often hidden for small buttons that show only an icon.</span></span>
    - <span data-ttu-id="3a1f7-269">**工具提示** – 指定用户将鼠标光标悬停在按钮上方时显示的更多帮助文本。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-269">**Tooltip** – Specify additional Help text that appears when users mouse over the button.</span></span>
    - <span data-ttu-id="3a1f7-270">**以列为单位的大小/以行为单位的大小** – 您可以指定按钮的高度和宽度。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-270">**Size in columns/Size in rows** – You can specify how tall and wide the button is.</span></span>

        ![以行和列为单位的 POS 按钮大小](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - <span data-ttu-id="3a1f7-272">**自定义字体** – 如果选中 **启用 POS 的自定义字体** 复选框，则可为 POS 指定非系统默认字体。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-272">**Custom font** – When you select the **Enable custom font for POS** check box, you can specify a font other than the default system font for the POS.</span></span>
    - <span data-ttu-id="3a1f7-273">**自定义主题** – 默认情况下，POS 按钮使用可视化配置文件中的主题颜色。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-273">**Custom theme** – By default, POS buttons use the accent color from the visual profile.</span></span> <span data-ttu-id="3a1f7-274">如果选中 **使用自定义主题** 复选框，则可指定更多颜色。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-274">When you select the **Use custom theme** check box, you can specify additional colors.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3a1f7-275">Modern POS 和 Cloud POS 仅适用于 **背景色** 和 **字体颜色** 值。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-275">Modern POS and Cloud POS use only the **Back color** and **Font color** values.</span></span>

    - <span data-ttu-id="3a1f7-276">–**按钮图像** – 按钮中可以包含图像或图标。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-276">**Button image** – Buttons can include images or icons.</span></span> <span data-ttu-id="3a1f7-277">可以在 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 图像** 中指定的可用图像内进行选择。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-277">Select among the available images that are specified at **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**.</span></span>

![POS 中的示例按钮网格](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a><span data-ttu-id="3a1f7-279">其他资源</span><span class="sxs-lookup"><span data-stu-id="3a1f7-279">Additional resources</span></span>

[<span data-ttu-id="3a1f7-280">安装 Retail 销售点 (POS) 布局设计器</span><span class="sxs-lookup"><span data-stu-id="3a1f7-280">Install the Retail point of sale (POS) layout designer</span></span>](install-pos-layout-designer.md)
