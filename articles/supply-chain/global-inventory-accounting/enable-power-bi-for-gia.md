---
title: 为全球库存核算启用 Power BI
description: 本主题介绍了如何为全球库存核算启用 Microsoft Power BI。
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8be486409d60cc4927599816e30e1e4ab21a312a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669760"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>为全球库存核算启用 Power BI

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

您可以将磁贴、仪表板和报表从 [PowerBI.com](https://powerbi.com/) 帐户固定到 Microsoft Dynamics 365 应用程序工作区。

## <a name="prerequisites"></a>先决条件

必须具备以下先决条件才能启用 Power BI 报告：

- 您必须是 Dynamics 365 应用程序中的系统管理员。
- 您必须具有 [PowerBI.com](https://powerbi.com/) 帐户。
- 您在 Power BI 帐户中必须至少有一个仪表板和一个报表。
- 您必须是 Azure Active Directory (Azure AD) 帐户的管理员。
- Azure AD 域必须与您用于 [PowerBI.com](https://powerbi.com/) 帐户的域相同。

## <a name="setup"></a>设置

若要设置 Power BI 集成，请按照以下步骤操作。

1. 登录到 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)。
1. 转到 **共用资产库**，选择 **Power BI 报表模型** 作为资产类型，然后下载 **全球库存核算** 包。 
1. 登录到 [PowerBI.com](https://app.powerbi.com/)，，然后通过执行以下步骤上传 **全球库存核算** Power BI 报表文件：

    1. 选择 **新建**。
    1. 选择 **上传文件**。
    1. 选择 **全球库存核算** Power BI 报表文件。

1. 通过执行以下步骤配置 **全球库存核算** Power BI 报表：

    1. 转到 **我的工作区**，查找全球库存核算的数据集，然后在 **选项** 菜单上，选择 **设置**。
    1. 在 **全球库存核算的设置** 中，展开 **参数**，并根据需要更新所有参数。 特别是，请务必检查以下设置：
        1. 使用在 LCS 中的 **Power Platform 环境信息** 页面上找到的值（在 **Power Platform 集成** 部分）覆盖默认的 **Dataverse URL** 值。
        1. 使用在 LCS 中 **环境详细信息** 页面上找到的值（在 **管理环境** 部分）覆盖默认的 **环境 ID** 值。
        1. 选择 **数据源凭据** 部分中 **CDS** 标签旁边的 **编辑凭据** 链接。 然后使用 **OAuth2** 身份验证方法登录到您的 Dataverse 帐户。
    1. 验证在 **我的工作区 \> 报表 \> 全球库存核算** 中找到的 Power BI 报表现在是否正常工作，并且是否显示系统中的内容。

1. 如[配置 PowerBI.com 集成](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process)中所述注册应用程序。
1. 通过执行以下步骤将 **全球库存核算** Power BI 报表文件集成到 Dynamics 365 Supply Chain Management 中：

    1. 转到 **系统管理 \> 设置 \> PowerBI.com 配置**。
    1. 选择 **编辑**。
    1. 选择 **启用 PowerBI.Com 集成**。
    1. 在 **应用程序 ID** 字段中，输入应用程序 ID。
    1. 在 **应用程序密钥** 字段中，输入应用程序密钥。
    1. 选择 **保存**。

1. 刷新页面，以便显示 Power BI 登录对话框。
1. 在 **选项** 选项卡上，选择 **打开报表目录**，然后选择您之前上传的 **全球库存核算** Power BI 报表文件。
1. 刷新该页面。 您应该会看到您的报表已添加。
1. 在 **Power BI 报表** 下，选择 **全球库存核算** 链接。

有关详细信息，请参阅[配置 PowerBI.com 集成](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md)。
