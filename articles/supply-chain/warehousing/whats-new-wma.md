---
title: Warehouse Management 移动应用中的新增功能或更改的功能
description: 本主题列出了 Microsoft Dynamics 365 Supply Chain Management 的 Warehouse Management 移动应用的每个已发布版本的新增功能和更改的功能。
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261764"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="8424b-103">Warehouse Management 移动应用中的新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="8424b-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8424b-104">本主题列出了 Microsoft Dynamics 365 Supply Chain Management 的 Warehouse Management 移动应用的每个已发布版本的新增功能、修复、改进和已知问题。</span><span class="sxs-lookup"><span data-stu-id="8424b-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="8424b-105">版本 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="8424b-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="8424b-106">版本 2.0.6.0 中的新增功能、修复和改进</span><span class="sxs-lookup"><span data-stu-id="8424b-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="8424b-107">此版本引入了以下新增功能、修复和改进：</span><span class="sxs-lookup"><span data-stu-id="8424b-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="8424b-108">演示模式现在以设备语言显示所有标签。</span><span class="sxs-lookup"><span data-stu-id="8424b-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="8424b-109">您不太可能收到以下错误消息：“找不到适合指定大小的视图。”</span><span class="sxs-lookup"><span data-stu-id="8424b-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="8424b-110">工作卡的最小高度已增加（对于配置三个或更少字段以显示在工作列表中的情况）。</span><span class="sxs-lookup"><span data-stu-id="8424b-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="8424b-111">详细信息卡底部的边距（淡出）已改进。</span><span class="sxs-lookup"><span data-stu-id="8424b-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="8424b-112">现在可以正常处理与服务器交换的 XML 文件中的无效符号。</span><span class="sxs-lookup"><span data-stu-id="8424b-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="8424b-113">（例如，非打印字符现在可以正常处理，并且不再导致应用停止响应。）</span><span class="sxs-lookup"><span data-stu-id="8424b-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="8424b-114">提交服务器请求时的 HTTP 错误（例如“错误 503”）现在可以正常处理。</span><span class="sxs-lookup"><span data-stu-id="8424b-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="8424b-115">显示错误时，组合框控件不再自动显示选项列表。</span><span class="sxs-lookup"><span data-stu-id="8424b-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="8424b-116">应用不再因用户设置中选择的显示方向而停止响应。</span><span class="sxs-lookup"><span data-stu-id="8424b-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="8424b-117">产品图像现在显示在自助服务环境中。</span><span class="sxs-lookup"><span data-stu-id="8424b-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="8424b-118">（此更改仅适用于低分辨率版本。</span><span class="sxs-lookup"><span data-stu-id="8424b-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="8424b-119">文件管理服务不支持自助服务环境中的全尺寸图像。）</span><span class="sxs-lookup"><span data-stu-id="8424b-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="8424b-120">涉及零数量短缺领料的问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="8424b-121">当详细信息卡显示多个相同的字段时，应用不再停止响应。</span><span class="sxs-lookup"><span data-stu-id="8424b-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="8424b-122">版本 2.0.6.0 中的已知问题</span><span class="sxs-lookup"><span data-stu-id="8424b-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="8424b-123">此版本中存在以下已知问题：</span><span class="sxs-lookup"><span data-stu-id="8424b-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="8424b-124">随着时间的推移，应用（尤其是工作列表）会变慢。</span><span class="sxs-lookup"><span data-stu-id="8424b-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="8424b-125">**Windows 版本：** 在 Windows 上使用 USB 扫描枪进行扫描时，不一致的结果会导致扫描的符号混淆。</span><span class="sxs-lookup"><span data-stu-id="8424b-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="8424b-126">版本 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="8424b-126">Version 2.0.5.0</span></span>

<span data-ttu-id="8424b-127">此版本引入了以下新增功能、修复和改进：</span><span class="sxs-lookup"><span data-stu-id="8424b-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="8424b-128">客户端密码不再隐藏在连接设置的设置中。</span><span class="sxs-lookup"><span data-stu-id="8424b-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="8424b-129">您现在可以长按任何文本以使其完全显示。</span><span class="sxs-lookup"><span data-stu-id="8424b-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="8424b-130">缺少存储权限时的错误消息已改进。</span><span class="sxs-lookup"><span data-stu-id="8424b-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="8424b-131">为某些流添加了新的控制序列。</span><span class="sxs-lookup"><span data-stu-id="8424b-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="8424b-132">由于窗口大小，提交按钮不再错误地可用。</span><span class="sxs-lookup"><span data-stu-id="8424b-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="8424b-133">当使用较大的按钮大小时，滑块现在可以在较小的屏幕上进行。</span><span class="sxs-lookup"><span data-stu-id="8424b-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="8424b-134">四个按钮的覆盖不再被切断。</span><span class="sxs-lookup"><span data-stu-id="8424b-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="8424b-135">键盘现在支持删除按钮。</span><span class="sxs-lookup"><span data-stu-id="8424b-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="8424b-136">按下键盘时可能出现的亮度问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="8424b-137">各种演示数据问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="8424b-138">影响详细信息页面上的数字字段的问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="8424b-139">屏幕键盘不再偶尔在某些设备上消失。</span><span class="sxs-lookup"><span data-stu-id="8424b-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="8424b-140">各种用户界面 (UI) bug 已修复，例如影响背景颜色和定位的 bug。</span><span class="sxs-lookup"><span data-stu-id="8424b-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="8424b-141">俄语 UI 已改进。</span><span class="sxs-lookup"><span data-stu-id="8424b-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="8424b-142">导致系统停止响应的各种问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="8424b-143">与重新打开计算器相关的问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="8424b-144">**Android 版本：** 导致 Android 4.4 在启动时停止响应的问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="8424b-145">**Android 版本：** 最小缩放比例已降至 50%。</span><span class="sxs-lookup"><span data-stu-id="8424b-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="8424b-146">版本 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="8424b-146">Version 2.0.4.0</span></span>

<span data-ttu-id="8424b-147">版本 2.0.4.0 是 Warehouse Management 移动应用的第一个公开发布的版本。</span><span class="sxs-lookup"><span data-stu-id="8424b-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="8424b-148">版本 2.0.4.0 中的新增功能、修复和改进</span><span class="sxs-lookup"><span data-stu-id="8424b-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="8424b-149">此版本引入了预览版中未提供的以下新增功能、修复和改进：</span><span class="sxs-lookup"><span data-stu-id="8424b-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="8424b-150">如果详细信息卡包含两个具有相同数据的标签，则其中一个标签将隐藏。</span><span class="sxs-lookup"><span data-stu-id="8424b-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="8424b-151">现在默认显示特殊字符，隐藏它们的选项已从用户设置中删除。</span><span class="sxs-lookup"><span data-stu-id="8424b-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="8424b-152">禁用的提交按钮现在在紧凑的臂上视图中显示为不可用。</span><span class="sxs-lookup"><span data-stu-id="8424b-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="8424b-153">对控件排序逻辑的更改可确保跨设备更顺利地缩放。</span><span class="sxs-lookup"><span data-stu-id="8424b-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="8424b-154">因此，不需要调整字体或按钮的缩放比例。</span><span class="sxs-lookup"><span data-stu-id="8424b-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="8424b-155">默认颜色主题已更改为 *深色*。</span><span class="sxs-lookup"><span data-stu-id="8424b-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="8424b-156">已在功能区视图中添加了已禁用提交按钮的缺失图标。</span><span class="sxs-lookup"><span data-stu-id="8424b-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="8424b-157">超时异常现在会将您转到连接页面，而不是显示内联错误。</span><span class="sxs-lookup"><span data-stu-id="8424b-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="8424b-158">如果没有可用的提交操作（例如 **确定**、**是**、**接受**、**完毕** 或 **完成**），提交按钮将禁用。</span><span class="sxs-lookup"><span data-stu-id="8424b-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="8424b-159">应用稳定性已改进。</span><span class="sxs-lookup"><span data-stu-id="8424b-159">App stability has been improved.</span></span>
- <span data-ttu-id="8424b-160">有一个针对安全漏洞 [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701) 的修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="8424b-161">**Windows 版本：** 在 Windows 上，调整窗口大小后菜单无响应的问题已修复。</span><span class="sxs-lookup"><span data-stu-id="8424b-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="8424b-162">版本 2.0.4.0 中的已知问题</span><span class="sxs-lookup"><span data-stu-id="8424b-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="8424b-163">此版本中存在以下已知问题：</span><span class="sxs-lookup"><span data-stu-id="8424b-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="8424b-164">此版本中使用 Android 4.4 的设备有问题。</span><span class="sxs-lookup"><span data-stu-id="8424b-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="8424b-165">在此 Android 版本上使用应用时，可能会遇到问题。</span><span class="sxs-lookup"><span data-stu-id="8424b-165">You might experience issues when you use the app on this Android version.</span></span>
