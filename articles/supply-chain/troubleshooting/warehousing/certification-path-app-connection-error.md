---
title: 设置应用连接时出现认证路径错误
description: 如果 Warehouse Management 应用显示错误“未找到认证路径的信任锚”，请使用此页面解决问题。
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475691"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>设置应用连接时找不到认证路径的信任锚

## <a name="symptoms"></a>故障特征

尝试连接到 Supply Chain Management 时，Warehouse Management 应用可能会显示以下错误消息：

> “java.security.cert.certPathValidatorException：找到不认证路径的信任锚。

此问题可能会影响具有以下属性的设备：

- **操作系统版本**：Android 4.4.x（如 Zebra TC55）。 在最新 Android 版本中，这不属于问题。
- **Supply Chain Management 位置**：云
- **连接模式**：客户端密码或证书

## <a name="possible-cause"></a>可能原因

Microsoft 可能已更新了 Supply Chain Management 使用的服务器 SSL 证书。 因此，根证书和/或其中一个中间证书可能已更改，因此移动设备的可信系统证书列表中不包含这个新证书。 吸版本的 Android 将自动更新可信证书列表，但 Android 4.4.x 不会更新。

## <a name="resolution"></a>解决方法

请执行以下操作之一解决此问题。

- 请使用下一节中描述的解决方法更新每个相关设备。
- *可能* 可以联系 Zebra 或 Google 获取系统可信认证机构 (CA) 证书的更新。 但是，我们尚未确认这一点。
- 如果可能，请考虑将较旧的设备替换为正在运行较高版本 Android 的设备（其中将自动更新可信 CA 证书）。

### <a name="workaround"></a>解决方法

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>步骤 1：从 Supply Chain Management 导出新的根证书

使用 Internet 浏览器执行以下步骤手动下载新的根证书：

1. 登录 Dynamics Supply Chain Management，然后打开标题页。

1. 在浏览器的地址栏中，选择锁图标打开 **位置安全** 对话框。
1. 在对话框中，选择 **证书（有效）** 以打开该证书的 **证书** 窗口。
1. 打开 **证书** 窗口的 **认证路径** 选项卡。
1. 选择层次结构中显示的顶级证书。 （这是根证书）。
1. 打开 **证书** 窗口的 **详细信息** 选项卡。
1. 选择 **详细信息** 选项卡底部的 **复制到文件** 按钮。
1. 将打开 **证书导出向导**。 选择 **下一步** 继续。
1. 将打开 **导出文件格式** 页面。 选择 **DER 编码二进制 X.509 (.CER)**。 然后选择 **下一步** 继续。
1. 将打开 **要导出的文件** 页面；请指定文件名和位置。 然后选择 **下一步** 继续。
1. 将打开 **完成证书导出向导** 页面，其中显示导出结果。 选择 **完成**。

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>步骤 2：将下载的证书安装到受影响的设备上

通过执行以下操作安装下载的证书：

1. 将上一步中下载的证书传输到要更新的设备上。 例如，可以使用 SD 卡或网络连接将文件传输到设备上。
1. 打开设备的安全设置，然后选择有关从文件中安装证书的菜单选项。 （此操作的确切步骤因设备和操作系统版本而异。）
1. 现在可信证书的 **用户** 选项卡中应显示新证书。
1. 为每个受影响设备重复此过程。
