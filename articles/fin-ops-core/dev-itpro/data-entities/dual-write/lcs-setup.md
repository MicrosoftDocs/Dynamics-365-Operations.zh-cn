---
title: Lifecycle Services 的双重写入设置
description: 本文说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 5cccba580d23c3a0e9aed62f76a305926a58585f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879795"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services 的双重写入设置

[!include [banner](../../includes/banner.md)]



本文说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 启用双写入。

## <a name="prerequisites"></a>先决条件

客户必须按照以下主题中所述完成 Power Platform 集成：

- 如果您尚未使用 Microsoft Power Platform，并且要通过添加平台功能来扩展财务和运营环境，请参阅 [Power Platform 集成 - 在环境部署期间启用](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)。
- 如果您已拥有 Dataverse 和 Power Platform 环境，并且要将它们连接到财务和运营环境，请参阅 [Power Platform 集成 - 在环境部署后启用](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)。

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>为新的和现有的 Dataverse 环境设置双重写入

按照以下步骤从 LCS **环境详细信息** 页设置双写入：

1. 在 **环境详细信息** 页上，展开 **Power Platform 集成** 部分。

2. 选择 **双写入应用程序** 按钮。

    ![Power Platform 集成。](media/powerplat_integration_step2.png)

3. 查看条款和条件，然后选择 **配置**。

4. 选择 **确定** 继续。

5. 您可以通过定期刷新环境详细信息页来监视进度。 设置通常需要 30 分钟或更短时间。  

6. 设置完成后，一条消息将通知您过程是成功还是失败。 如果设置失败，会显示相关的错误消息。 您必须解决所有错误，然后再进行下一步。

7. 选择 **链接到 Power Platform 环境** 在 Dataverse 和当前环境的数据库之间创建链接。 这通常需要不到 5 分钟时间。

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="链接到 Power Platform 环境。":::

8. 链接完成后，将显示一个超链接。 使用此链接登录到财务和运营环境中的双写入管理区域。 从那里，您可以设置实体映射。

## <a name="linking-mismatch"></a>链接不匹配

在没有为 Power Platform 集成设置 LCS 时，您的双重写入环境可以链接到 Dataverse 实例。 此链接不匹配可能会导致意外行为。 建议 LCS 环境详细信息与您在双重写入中连接到的内容匹配，以便业务事件、虚拟表和加载项可以使用相同的连接。

如果您的环境存在链接不匹配，则 LCS 会在环境详细信息页上显示如下警告：“Microsoft 检测到您的环境通过双重写入功能链接到非 Power Platform 集成中指定的目标（不建议）”。

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform集成链接不匹配。":::

如果您收到此警告，请尝试以下解决方案之一：

- 如果从未为 Power Platform 集成设置您的 LCS 环境，则您可以按照本文中的说明连接到在双重写入中配置的 Dataverse 实例。
- 如果已为 Power Platform 集成设置了您的 LCS 环境，则您应取消链接双重写入，并使用[方案：重置或更改链接](relink-environments.md#scenario-reset-or-change-linking)将其重新连接到 LCS 指定的环境。

在过去，手动支持票证选项可用，但那是在上述选项 1 存在之前的情况。  Microsoft 不再支持通过支持票证手动重新链接请求。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
