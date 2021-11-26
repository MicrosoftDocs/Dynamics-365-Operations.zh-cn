---
title: Lifecycle Services 的双写入设置
description: 本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781384"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services 的双写入设置

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 启用双写入。

## <a name="prerequisites"></a>先决条件

您必须按照以下主题中所述完成 Power Platform 集成：

+ [Power Platform 集成 - 在环境部署期间启用](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform 集成 - 在环境部署后启用](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>为新 Dataverse 环境设置双写入

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

8. 链接完成后，将显示一个超链接。 使用此链接登录到 Finance and Operations 环境中的双写入管理区域。 从那里，您可以设置实体映射。

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>为现有 Dataverse 环境设置双写入

要为现有 Dataverse 环境设置双写入，必须创建 Microsoft [支持票证](../../lifecycle-services/lcs-support.md)。 票证必须包括：

+ 您的 Finance and Operations 环境 ID。
+ Lifecycle Services 中的环境名称。
+ 来自 Power Platform 管理中心的 Dataverse 组织 ID 或 Power Platform 环境 ID。 在您的票证中，要求 ID 是用于 Power Platform 集成的实例。

> [!NOTE]
> 不能使用 LCS 取消链接环境。 若要取消链接环境，请在 Finance and Operations 环境中打开 **数据集成** 工作区，然后选择 **取消链接**。

## <a name="linking-mismatch"></a>链接不匹配

您的 LCS 环境可能会链接到一个 Dataverse 实例，而您的双重写入环境则链接到另一个 Dataverse 实例。 此链接不匹配可能导致意外行为，最终可能会将数据发送到错误的环境。 建议用于双重写入的环境是作为 Power Platform 集成的一部分而创建的环境，长期而言，这将是在环境之间建立链接的唯一方法。

如果您的环境存在链接不匹配，则 LCS 会在环境详细信息页上显示类似于“Microsoft 检测到您的环境通过双重写入功能链接到非 Power Platform 集成中指定的目标（不建议）”的警告：

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform集成链接不匹配。":::

如果您遇到此错误，则会根据您的需要提供两个选项：

+ [取消链接并重新链接 LCS 环境详细信息页上指定的双重写入环境（重置或更改链接）](relink-environments.md#scenario-reset-or-change-linking)。 这是理想的选择，因为您可以在没有 Microsoft 支持的情况下运行它。  
+ 如果想要在双重写入中保持链接，您可以向 Microsoft 支持部门寻求帮助，以更改 Power Platform 集成，以使用您现有的 Dataverse 环境，如上一节所述。  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
