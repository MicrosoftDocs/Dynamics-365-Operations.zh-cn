---
title: Lifecycle Services 的双写入设置
description: 本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103561"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services 的双写入设置

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 启用双写入。

## <a name="prerequisites"></a>先决条件

您必须按照以下主题中所述完成 Power Platform 集成：

+ [Power Platform 集成 - 在环境部署期间启用](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform 集成 - 在环境部署后设置](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>为新 Dataverse 环境设置双写入

按照以下步骤从 LCS **环境详细信息** 页设置双写入：

1. 在 **环境详细信息** 页上，展开 **Power Platform 集成** 部分。

2. 选择 **双写入应用程序** 按钮。

    ![Power Platform 集成](media/powerplat_integration_step2.png)

3. 查看条款和条件，然后选择 **配置**。

4. 选择 **确定** 继续。

5. 您可以通过定期刷新环境详细信息页来监视进度。 设置通常需要 30 分钟或更短时间。  

6. 设置完成后，一条消息将通知您过程是成功还是失败。 如果设置失败，会显示相关的错误消息。 您必须解决所有错误，然后再进行下一步。

7. 选择 **链接到 Power Platform 环境** 在 Dataverse 和当前环境的数据库之间创建链接。 这通常需要不到 5 分钟时间。

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="链接到 Power Platform 环境":::

8. 链接完成后，将显示一个超链接。 使用此链接登录到 Finance and Operations 环境中的双写入管理区域。 从那里，您可以设置实体映射。

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>为现有 Dataverse 环境设置双写入

要为现有 Dataverse 环境设置双写入，必须创建 Microsoft [支持票证](../../lifecycle-services/lcs-support.md)。 票证必须包括：

+ 您的 Finance and Operations 环境 ID。
+ Lifecycle Services 中的环境名称。
+ 来自 Power Platform 管理中心的 Dataverse 组织 ID 或 Power Platform 环境 ID。 在您的票证中，要求 ID 是用于 Power Platform 集成的实例。

> [!NOTE]
> 不能使用 LCS 取消链接环境。 若要取消链接环境，请在 Finance and Operations 环境中打开 **数据集成** 工作区，然后选择 **取消链接**。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
