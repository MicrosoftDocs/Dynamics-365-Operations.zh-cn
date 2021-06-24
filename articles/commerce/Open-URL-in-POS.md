---
title: 在 POS 中打开 URL
description: 此主题概述 Dynamics 365 Commerce 中的产品和客户搜索的增强功能。
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193195"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="4ab67-103">在 POS 中打开 URL</span><span class="sxs-lookup"><span data-stu-id="4ab67-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ab67-104">本主题介绍如何在 Dynamics 365 Commerce 销售点 (POS) 中配置打开 URL 的按钮。</span><span class="sxs-lookup"><span data-stu-id="4ab67-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="4ab67-105">此功能不需要代码自定义，可以由非开发人员角色的人员配置。</span><span class="sxs-lookup"><span data-stu-id="4ab67-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="4ab67-106">此功能允许在 POS 中配置按钮，进而使用按钮网格设计器打开 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="4ab67-107">目前，这在以下配置中不支持：</span><span class="sxs-lookup"><span data-stu-id="4ab67-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="4ab67-108">在新窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="4ab67-108">Open in new window.</span></span>
- <span data-ttu-id="4ab67-109">在 POS 内打开。</span><span class="sxs-lookup"><span data-stu-id="4ab67-109">Open within POS.</span></span>
- <span data-ttu-id="4ab67-110">在本地应用中打开。</span><span class="sxs-lookup"><span data-stu-id="4ab67-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="4ab67-111">在新窗口中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-111">Open in new window</span></span>

<span data-ttu-id="4ab67-112">此配置定义是否在新窗口或在应用内打开 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="4ab67-113">当配置为在应用内打开 Web URL 时，POS 的侧导航面板和顶部栏可见并可用于用户交互。</span><span class="sxs-lookup"><span data-stu-id="4ab67-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="4ab67-114">当配置为在新窗口中打开时，URL 将在 Windows 的现代 POS 上的新应用窗口，以及所有其他 POS 客户端的新浏览器标签页中打开。</span><span class="sxs-lookup"><span data-stu-id="4ab67-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="4ab67-115">为此，您必须使用所选的 **在新窗口中打开** 选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="4ab67-116">在 POS 内打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-116">Open within POS</span></span>

<span data-ttu-id="4ab67-117">当前仅 Windows 上的现代 POS 支持在 POS 内打开 Web URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="4ab67-118">在其他客户端，此功能正在开发，计划在将来的更新中发布。</span><span class="sxs-lookup"><span data-stu-id="4ab67-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="4ab67-119">为此，您必须使用未选择的 **在新窗口中打开** 选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="4ab67-120">打开本地应用</span><span class="sxs-lookup"><span data-stu-id="4ab67-120">Open a native app</span></span>

<span data-ttu-id="4ab67-121">此功能还允许您指定打开本地应用的非 Web URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="4ab67-122">例如，您可以指定 MailTo、SIP、IM 或 MSTEAMS 等 URL 协议，其然后由主机设备上各自的本地应用处理。</span><span class="sxs-lookup"><span data-stu-id="4ab67-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="4ab67-123">为此，您必须使用所选的 **在新窗口中打开** 选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="4ab67-124">如果您使用部署图像服务和管理 (DISM) 设置您的计算机，对于 Windows 计算机，请参阅[导出或导入默认应用程序关联](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)来设置默认的协议关联。</span><span class="sxs-lookup"><span data-stu-id="4ab67-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="4ab67-125">如果您使用 MDM（如 Intune）来管理您的 Windows 计算机，请参阅[策略 CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="4ab67-126">如果您是构建自定义网站的开发人员，请参阅[启动 URI 的默认应用](/windows/uwp/launch-resume/launch-default-app)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="4ab67-127">无缝打开本地应用</span><span class="sxs-lookup"><span data-stu-id="4ab67-127">Open a native app seamlessly</span></span>

<span data-ttu-id="4ab67-128">Windows、iOS 和 Android 还允许根据应用协议关联更加无缝地打开应用。</span><span class="sxs-lookup"><span data-stu-id="4ab67-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="4ab67-129">如果您的应用尚未配置为从 Web 浏览器处理打开，您可能需要开发人员进行此配置。</span><span class="sxs-lookup"><span data-stu-id="4ab67-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="4ab67-130">对于 Windows，请参阅[使用应用 URI 处理程序启用网站应用](/windows/uwp/launch-resume/web-to-app-linking)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="4ab67-131">对于 iOS，请参阅[通用的开发人员链接](https://developer.apple.com/ios/universal-links/)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="4ab67-132">对于 Android，请参阅[处理 Android 应用链接](https://developer.android.com/training/app-links/)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="4ab67-133">客户</span><span class="sxs-lookup"><span data-stu-id="4ab67-133">Client</span></span>                | <span data-ttu-id="4ab67-134">在新窗口中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-134">Open in new window</span></span> | <span data-ttu-id="4ab67-135">打开本地应用</span><span class="sxs-lookup"><span data-stu-id="4ab67-135">Open native app</span></span> | <span data-ttu-id="4ab67-136">在 POS 内打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-136">Open within POS</span></span> | <span data-ttu-id="4ab67-137">明细</span><span class="sxs-lookup"><span data-stu-id="4ab67-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="4ab67-138">Windows 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="4ab67-138">Modern POS on Windows</span></span> | <span data-ttu-id="4ab67-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ab67-139">✓\*</span></span>                | <span data-ttu-id="4ab67-140">✓</span><span class="sxs-lookup"><span data-stu-id="4ab67-140">✓</span></span>               | <span data-ttu-id="4ab67-141">✓</span><span class="sxs-lookup"><span data-stu-id="4ab67-141">✓</span></span>              | <span data-ttu-id="4ab67-142">\*在现代 POS 窗口中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="4ab67-143">云 POS</span><span class="sxs-lookup"><span data-stu-id="4ab67-143">Cloud POS</span></span>             | <span data-ttu-id="4ab67-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ab67-144">✓\*</span></span>                | <span data-ttu-id="4ab67-145">✓</span><span class="sxs-lookup"><span data-stu-id="4ab67-145">✓</span></span>               | <span data-ttu-id="4ab67-146">X</span><span class="sxs-lookup"><span data-stu-id="4ab67-146">X</span></span>              | <span data-ttu-id="4ab67-147">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4ab67-148">iOS 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="4ab67-148">Modern POS on iOS</span></span>     | <span data-ttu-id="4ab67-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ab67-149">✓\*</span></span>                | <span data-ttu-id="4ab67-150">✓</span><span class="sxs-lookup"><span data-stu-id="4ab67-150">✓</span></span>               | <span data-ttu-id="4ab67-151">X</span><span class="sxs-lookup"><span data-stu-id="4ab67-151">X</span></span>              | <span data-ttu-id="4ab67-152">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4ab67-153">Android 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="4ab67-153">Modern POS on Android</span></span> | <span data-ttu-id="4ab67-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ab67-154">✓\*</span></span>                | <span data-ttu-id="4ab67-155">✓</span><span class="sxs-lookup"><span data-stu-id="4ab67-155">✓</span></span>               | <span data-ttu-id="4ab67-156">X</span><span class="sxs-lookup"><span data-stu-id="4ab67-156">X</span></span>              | <span data-ttu-id="4ab67-157">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="4ab67-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="4ab67-158">开始之前</span><span class="sxs-lookup"><span data-stu-id="4ab67-158">Before you begin</span></span>

<span data-ttu-id="4ab67-159">在您开始前，请查看如何配置[销售点 (POS) 的屏幕布局](pos-screen-layouts.md)。</span><span class="sxs-lookup"><span data-stu-id="4ab67-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="4ab67-160">在 POS 中打开 URL</span><span class="sxs-lookup"><span data-stu-id="4ab67-160">Open URL in POS</span></span>

<span data-ttu-id="4ab67-161">若要将 URL 配置为在 POS 中打开，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4ab67-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="4ab67-162">在总部，转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="4ab67-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="4ab67-163">选择 **按钮网格 \> 设计器**。</span><span class="sxs-lookup"><span data-stu-id="4ab67-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="4ab67-164">创建新按钮。</span><span class="sxs-lookup"><span data-stu-id="4ab67-164">Create a new button.</span></span>
4. <span data-ttu-id="4ab67-165">选择 **按钮** 属性。</span><span class="sxs-lookup"><span data-stu-id="4ab67-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="4ab67-166">选择 **打开 URL** 作为操作。</span><span class="sxs-lookup"><span data-stu-id="4ab67-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="4ab67-167">输入要使用的 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="4ab67-168">配置是否在新窗口中打开 URL。</span><span class="sxs-lookup"><span data-stu-id="4ab67-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
