---
title: 在 POS 中打开 URL
description: 此主题概述 Microsoft Dynamics 365 for Retail 中的产品和客户搜索的增强功能。
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 729caf9fad9097a3ecbf7d546c8f8a96f67aec92
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845672"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="cc443-103">在 POS 中打开 URL</span><span class="sxs-lookup"><span data-stu-id="cc443-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc443-104">本主题介绍如何在 Retail 销售点 (POS) 中配置打开 URL 的按钮。</span><span class="sxs-lookup"><span data-stu-id="cc443-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="cc443-105">此功能不需要代码自定义，可以由非开发人员角色的人员配置。</span><span class="sxs-lookup"><span data-stu-id="cc443-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="cc443-106">此功能作为 Dynamics 365 for Finance and Operations 版本 8.1.3（内部版本 8.1.227.10014）以及更高版本的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="cc443-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="cc443-107">此功能允许在 POS 中配置按钮，进而使用按钮网格设计器打开 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="cc443-108">目前，这在以下配置中不支持：</span><span class="sxs-lookup"><span data-stu-id="cc443-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="cc443-109">在新窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="cc443-109">Open in new window.</span></span>
- <span data-ttu-id="cc443-110">在 POS 内打开。</span><span class="sxs-lookup"><span data-stu-id="cc443-110">Open within POS.</span></span>
- <span data-ttu-id="cc443-111">在本地应用中打开。</span><span class="sxs-lookup"><span data-stu-id="cc443-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="cc443-112">在新窗口中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-112">Open in new window</span></span>

<span data-ttu-id="cc443-113">此配置定义是否在新窗口或在应用内打开 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="cc443-114">当配置为在应用内打开 Web URL 时，POS 的侧导航面板和顶部栏可见并可用于用户交互。</span><span class="sxs-lookup"><span data-stu-id="cc443-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="cc443-115">当配置为在新窗口中打开时，URL 将在 Windows 的现代 POS 上的新应用窗口，以及所有其他 POS 客户端的新浏览器标签页中打开。</span><span class="sxs-lookup"><span data-stu-id="cc443-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="cc443-116">为此，您必须使用所选的**在新窗口中打开**选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="cc443-117">在 POS 内打开</span><span class="sxs-lookup"><span data-stu-id="cc443-117">Open within POS</span></span>

<span data-ttu-id="cc443-118">当前仅 Windows 上的现代 POS 支持在 POS 内打开 Web URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="cc443-119">在其他客户端，此功能正在开发，计划在将来的更新中发布。</span><span class="sxs-lookup"><span data-stu-id="cc443-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="cc443-120">为此，您必须使用未选择的**在新窗口中打开**选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="cc443-121">打开本地应用</span><span class="sxs-lookup"><span data-stu-id="cc443-121">Open a native app</span></span>

<span data-ttu-id="cc443-122">此功能还允许您指定打开本地应用的非 Web URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="cc443-123">例如，您可以指定 MailTo、SIP、IM 或 MSTEAMS 等 URL 协议，其然后由主机设备上各自的本地应用处理。</span><span class="sxs-lookup"><span data-stu-id="cc443-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="cc443-124">为此，您必须使用所选的**在新窗口中打开**选项配置 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="cc443-125">如果您使用部署图像服务和管理 (DISM) 设置您的计算机，对于 Windows 计算机，请参阅[导出或导入默认应用程序关联](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)来设置默认的协议关联。</span><span class="sxs-lookup"><span data-stu-id="cc443-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="cc443-126">如果您使用 MDM（如 Intune）来管理您的 Windows 计算机，请参阅[策略 CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults)。</span><span class="sxs-lookup"><span data-stu-id="cc443-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="cc443-127">如果您是构建自定义网站的开发人员，请参阅[启动 URI 的默认应用](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app)。</span><span class="sxs-lookup"><span data-stu-id="cc443-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="cc443-128">无缝打开本地应用</span><span class="sxs-lookup"><span data-stu-id="cc443-128">Open a native app seamlessly</span></span>

<span data-ttu-id="cc443-129">Windows、iOS 和 Android 还允许根据应用协议关联更加无缝地打开应用。</span><span class="sxs-lookup"><span data-stu-id="cc443-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="cc443-130">如果您的应用尚未配置为从 Web 浏览器处理打开，您可能需要开发人员进行此配置。</span><span class="sxs-lookup"><span data-stu-id="cc443-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="cc443-131">对于 Windows，请参阅[使用应用 URI 处理程序启用网站应用](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking)。</span><span class="sxs-lookup"><span data-stu-id="cc443-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="cc443-132">对于 iOS，请参阅[通用的开发人员链接](https://developer.apple.com/ios/universal-links/)。</span><span class="sxs-lookup"><span data-stu-id="cc443-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="cc443-133">对于 Android，请参阅[处理 Android 应用链接](https://developer.android.com/training/app-links/)。</span><span class="sxs-lookup"><span data-stu-id="cc443-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="cc443-134">客户</span><span class="sxs-lookup"><span data-stu-id="cc443-134">Client</span></span>                | <span data-ttu-id="cc443-135">在新窗口中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-135">Open in new window</span></span> | <span data-ttu-id="cc443-136">打开本地应用</span><span class="sxs-lookup"><span data-stu-id="cc443-136">Open native app</span></span> | <span data-ttu-id="cc443-137">在 POS 内打开</span><span class="sxs-lookup"><span data-stu-id="cc443-137">Open within POS</span></span> | <span data-ttu-id="cc443-138">明细</span><span class="sxs-lookup"><span data-stu-id="cc443-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="cc443-139">Windows 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="cc443-139">Modern POS on Windows</span></span> | <span data-ttu-id="cc443-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc443-140">✓\*</span></span>                | <span data-ttu-id="cc443-141">✓</span><span class="sxs-lookup"><span data-stu-id="cc443-141">✓</span></span>               | <span data-ttu-id="cc443-142">✓</span><span class="sxs-lookup"><span data-stu-id="cc443-142">✓</span></span>              | <span data-ttu-id="cc443-143">\*在现代 POS 窗口中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="cc443-144">云 POS</span><span class="sxs-lookup"><span data-stu-id="cc443-144">Cloud POS</span></span>             | <span data-ttu-id="cc443-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc443-145">✓\*</span></span>                | <span data-ttu-id="cc443-146">✓</span><span class="sxs-lookup"><span data-stu-id="cc443-146">✓</span></span>               | <span data-ttu-id="cc443-147">X</span><span class="sxs-lookup"><span data-stu-id="cc443-147">X</span></span>              | <span data-ttu-id="cc443-148">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cc443-149">iOS 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="cc443-149">Modern POS on iOS</span></span>     | <span data-ttu-id="cc443-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc443-150">✓\*</span></span>                | <span data-ttu-id="cc443-151">✓</span><span class="sxs-lookup"><span data-stu-id="cc443-151">✓</span></span>               | <span data-ttu-id="cc443-152">X</span><span class="sxs-lookup"><span data-stu-id="cc443-152">X</span></span>              | <span data-ttu-id="cc443-153">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cc443-154">Android 上的现代 POS</span><span class="sxs-lookup"><span data-stu-id="cc443-154">Modern POS on Android</span></span> | <span data-ttu-id="cc443-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc443-155">✓\*</span></span>                | <span data-ttu-id="cc443-156">✓</span><span class="sxs-lookup"><span data-stu-id="cc443-156">✓</span></span>               | <span data-ttu-id="cc443-157">X</span><span class="sxs-lookup"><span data-stu-id="cc443-157">X</span></span>              | <span data-ttu-id="cc443-158">\*在新浏览器标签页中打开</span><span class="sxs-lookup"><span data-stu-id="cc443-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="cc443-159">开始之前</span><span class="sxs-lookup"><span data-stu-id="cc443-159">Before you begin</span></span>

<span data-ttu-id="cc443-160">在您开始前，请查看如何配置[销售点 (POS) 的屏幕布局](pos-screen-layouts.md)。</span><span class="sxs-lookup"><span data-stu-id="cc443-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="cc443-161">在 POS 中打开 URL</span><span class="sxs-lookup"><span data-stu-id="cc443-161">Open URL in POS</span></span>

<span data-ttu-id="cc443-162">若要将 URL 配置为在 POS 中打开，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cc443-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="cc443-163">在总部，转至**零售 \> 渠道设置 \> POS 设置 \> POS \> 屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="cc443-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="cc443-164">选择**按钮网格 \> 设计器**。</span><span class="sxs-lookup"><span data-stu-id="cc443-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="cc443-165">创建新按钮。</span><span class="sxs-lookup"><span data-stu-id="cc443-165">Create a new button.</span></span>
4. <span data-ttu-id="cc443-166">选择**按钮**属性。</span><span class="sxs-lookup"><span data-stu-id="cc443-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="cc443-167">选择**打开 URL** 作为操作。</span><span class="sxs-lookup"><span data-stu-id="cc443-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="cc443-168">输入要使用的 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="cc443-169">配置是否在新窗口中打开 URL。</span><span class="sxs-lookup"><span data-stu-id="cc443-169">Configure whether to open the URL in a new window.</span></span>
