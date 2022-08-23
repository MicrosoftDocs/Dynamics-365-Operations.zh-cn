---
title: 解决 Store Commerce 设置和安装问题
description: 本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的设置和安装问题。
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3d115e84af1aaf5266eff6588ca6996a333e51a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286322"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>解决 Store Commerce 设置和安装问题

[!include [banner](../includes/banner.md)]

本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的设置和安装问题。

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>我无法激活应用，我收到连接错误消息

输入有效的云点销售点 (CPOS) URL 后，您可能会收到与以下示例相似的连接错误消息：

> 出现连接错误，您的设备无法连接到 CPOS。 键入的 CPOS URL 可能有一些问题。

在这种情况下，请查看 URL 是否存在拼写错误，或确定 CPOS 是否因为离线而无法访问。

此外，请验证 Cloud Scale Unit (CSU) 版本是否为 10.0.25 (9.35.\*.\*) 或更高版本。 需要 CPOS 版本 10.0.25 或更高版本才能使用 Store Commerce 应用。

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>我无法安装应用，因为已安装 Modern POS

在安装过程中，您可能会收到一条错误消息，如以下示例：

> 此产品 (Modern POS) 的版本 (9.\*.\*.\*) 之前已通过旧版安装程序安装。

要修复此错误，您必须卸载计算机上所有用户的现代销售点 (MPOS) 应用，然后重试。 您可以通过运行以下 PowerShell 命令来确认是否已删除所有用户的 MPOS。

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>由于 URL 无效或错误状态，我无法激活应用

如果您输入的 CPOS URL 无效，想要进行更改，或者如果 Store Commerce 应用在激活期间处于错误状态，您可以通过重置应用重新启动流程。 Store Commerce 应用将仅保存有效的 CPOS URL。

要重置 Store Commerce 应用，请按照以下步骤操作。

1. 在 Windows **开始** 菜单上，选择并按住（或右键单击）应用，然后选择 **更多 \> 应用设置**。
2. 向下滚动应用设置页面，直到找到 **重置** 按钮。
3. 选择 **重置**。 然后，当系统提示您时，确认您要重置应用。
