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
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Warehouse Management 移动应用中的新增功能或更改的功能

[!include [banner](../includes/banner.md)]

本主题列出了 Microsoft Dynamics 365 Supply Chain Management 的 Warehouse Management 移动应用的每个已发布版本的新增功能、修复、改进和已知问题。

## <a name="version-2060"></a>版本 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>版本 2.0.6.0 中的新增功能、修复和改进

此版本引入了以下新增功能、修复和改进：

- 演示模式现在以设备语言显示所有标签。
- 您不太可能收到以下错误消息：“找不到适合指定大小的视图。”
- 工作卡的最小高度已增加（对于配置三个或更少字段以显示在工作列表中的情况）。
- 详细信息卡底部的边距（淡出）已改进。
- 现在可以正常处理与服务器交换的 XML 文件中的无效符号。 （例如，非打印字符现在可以正常处理，并且不再导致应用停止响应。）
- 提交服务器请求时的 HTTP 错误（例如“错误 503”）现在可以正常处理。
- 显示错误时，组合框控件不再自动显示选项列表。
- 应用不再因用户设置中选择的显示方向而停止响应。
- 产品图像现在显示在自助服务环境中。 （此更改仅适用于低分辨率版本。 文件管理服务不支持自助服务环境中的全尺寸图像。）
- 涉及零数量短缺领料的问题已修复。
- 当详细信息卡显示多个相同的字段时，应用不再停止响应。

### <a name="known-issues-in-version-2060"></a>版本 2.0.6.0 中的已知问题

此版本中存在以下已知问题：

- 随着时间的推移，应用（尤其是工作列表）会变慢。
- **Windows 版本：** 在 Windows 上使用 USB 扫描枪进行扫描时，不一致的结果会导致扫描的符号混淆。

## <a name="version-2050"></a>版本 2.0.5.0

此版本引入了以下新增功能、修复和改进：

- 客户端密码不再隐藏在连接设置的设置中。
- 您现在可以长按任何文本以使其完全显示。
- 缺少存储权限时的错误消息已改进。
- 为某些流添加了新的控制序列。
- 由于窗口大小，提交按钮不再错误地可用。
- 当使用较大的按钮大小时，滑块现在可以在较小的屏幕上进行。
- 四个按钮的覆盖不再被切断。
- 键盘现在支持删除按钮。
- 按下键盘时可能出现的亮度问题已修复。
- 各种演示数据问题已修复。
- 影响详细信息页面上的数字字段的问题已修复。
- 屏幕键盘不再偶尔在某些设备上消失。
- 各种用户界面 (UI) bug 已修复，例如影响背景颜色和定位的 bug。
- 俄语 UI 已改进。
- 导致系统停止响应的各种问题已修复。
- 与重新打开计算器相关的问题已修复。
- **Android 版本：** 导致 Android 4.4 在启动时停止响应的问题已修复。
- **Android 版本：** 最小缩放比例已降至 50%。

## <a name="version-2040"></a>版本 2.0.4.0

版本 2.0.4.0 是 Warehouse Management 移动应用的第一个公开发布的版本。

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>版本 2.0.4.0 中的新增功能、修复和改进

此版本引入了预览版中未提供的以下新增功能、修复和改进：

- 如果详细信息卡包含两个具有相同数据的标签，则其中一个标签将隐藏。
- 现在默认显示特殊字符，隐藏它们的选项已从用户设置中删除。
- 禁用的提交按钮现在在紧凑的臂上视图中显示为不可用。
- 对控件排序逻辑的更改可确保跨设备更顺利地缩放。 因此，不需要调整字体或按钮的缩放比例。
- 默认颜色主题已更改为 *深色*。
- 已在功能区视图中添加了已禁用提交按钮的缺失图标。
- 超时异常现在会将您转到连接页面，而不是显示内联错误。
- 如果没有可用的提交操作（例如 **确定**、**是**、**接受**、**完毕** 或 **完成**），提交按钮将禁用。
- 应用稳定性已改进。
- 有一个针对安全漏洞 [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701) 的修复。
- **Windows 版本：** 在 Windows 上，调整窗口大小后菜单无响应的问题已修复。

### <a name="known-issue-in-version-2040"></a>版本 2.0.4.0 中的已知问题

此版本中存在以下已知问题：

- 此版本中使用 Android 4.4 的设备有问题。 在此 Android 版本上使用应用时，可能会遇到问题。
