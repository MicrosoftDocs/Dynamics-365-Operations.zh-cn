---
title: 在 POS 中打开 URL
description: 此主题概述 Dynamics 365 Commerce 中的产品和客户搜索的增强功能。
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
ms.openlocfilehash: 137b699d5f60b9b62a5ce9501e3b2a262e60a88f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410393"
---
# <a name="open-url-in-pos"></a>在 POS 中打开 URL

[!include [banner](includes/banner.md)]

本主题介绍如何在 Retail 销售点 (POS) 中配置打开 URL 的按钮。 此功能不需要代码自定义，可以由非开发人员角色的人员配置。 

此功能允许在 POS 中配置按钮，进而使用按钮网格设计器打开 URL。 目前，这在以下配置中不支持：

- 在新窗口中打开。
- 在 POS 内打开。
- 在本地应用中打开。

## <a name="open-in-new-window"></a>在新窗口中打开

此配置定义是否在新窗口或在应用内打开 URL。 当配置为在应用内打开 Web URL 时，POS 的侧导航面板和顶部栏可见并可用于用户交互。 当配置为在新窗口中打开时，URL 将在 Windows 的现代 POS 上的新应用窗口，以及所有其他 POS 客户端的新浏览器标签页中打开。 为此，您必须使用所选的 **在新窗口中打开** 选项配置 URL。

## <a name="open-within-pos"></a>在 POS 内打开

当前仅 Windows 上的现代 POS 支持在 POS 内打开 Web URL。 在其他客户端，此功能正在开发，计划在将来的更新中发布。 为此，您必须使用未选择的 **在新窗口中打开** 选项配置 URL。

## <a name="open-a-native-app"></a>打开本地应用

此功能还允许您指定打开本地应用的非 Web URL。 例如，您可以指定 MailTo、SIP、IM 或 MSTEAMS 等 URL 协议，其然后由主机设备上各自的本地应用处理。 为此，您必须使用所选的 **在新窗口中打开** 选项配置 URL。

- 如果您使用部署图像服务和管理 (DISM) 设置您的计算机，对于 Windows 计算机，请参阅[导出或导入默认应用程序关联](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)来设置默认的协议关联。
- 如果您使用 MDM（如 Intune）来管理您的 Windows 计算机，请参阅[策略 CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults)。
- 如果您是构建自定义网站的开发人员，请参阅[启动 URI 的默认应用](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app)。

## <a name="open-a-native-app-seamlessly"></a>无缝打开本地应用

Windows、iOS 和 Android 还允许根据应用协议关联更加无缝地打开应用。 如果您的应用尚未配置为从 Web 浏览器处理打开，您可能需要开发人员进行此配置。

- 对于 Windows，请参阅[使用应用 URI 处理程序启用网站应用](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking)。
- 对于 iOS，请参阅[通用的开发人员链接](https://developer.apple.com/ios/universal-links/)。
- 对于 Android，请参阅[处理 Android 应用链接](https://developer.android.com/training/app-links/)。

| 客户                | 在新窗口中打开 | 打开本地应用 | 在 POS 内打开 | 明细                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Windows 上的现代 POS | ✓\*                | ✓               | ✓              | \*在现代 POS 窗口中打开 |
| 云 POS             | ✓\*                | ✓               | X              | \*在新浏览器标签页中打开        |
| iOS 上的现代 POS     | ✓\*                | ✓               | X              | \*在新浏览器标签页中打开        |
| Android 上的现代 POS | ✓\*                | ✓               | X              | \*在新浏览器标签页中打开        |

## <a name="before-you-begin"></a>开始之前

在您开始前，请查看如何配置[销售点 (POS) 的屏幕布局](pos-screen-layouts.md)。

## <a name="open-url-in-pos"></a>在 POS 中打开 URL

若要将 URL 配置为在 POS 中打开，请执行以下步骤。

1. 在总部，转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 屏幕布局**。
2. 选择 **按钮网格 \> 设计器**。
3. 创建新按钮。
4. 选择 **按钮** 属性。
5. 选择 **打开 URL** 作为操作。
6. 输入要使用的 URL。
7. 配置是否在新窗口中打开 URL。
