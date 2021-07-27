---
title: 开始使用全球库存核算
description: 本主题介绍了如何开始使用全球库存核算。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 07d3222680d9d9bff639f34eca5fea64d753ffd1
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336971"
---
# <a name="get-started-with-global-inventory-accounting"></a>开始使用全球库存核算

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

全球库存核算使您可以在已设置的全球库存核算分类帐中执行多个库存核算。 您必须将每个全球库存核算分类帐与一个 *惯例* 关联。 惯例是以下几种会计政策的集合：

- 成本对象
- 输入度量依据
- 成本流假设
- 成本元素

> [!NOTE]
> 即使在打开全球库存核算后，仍然可以按常规方式在 Microsoft Dynamics 365 Supply Chain Management 中执行库存核算。

全球库存核算是一个加载项。 若要使其功能可用，必须从 Microsoft Dynamics Lifecycle Services (LCS) 进行安装。 您可以选择在测试环境中对其进行评估，然后再将其打开以用于生产环境。

全球库存核算目前不支持 Supply Chain Management 中内置的所有成本管理功能。 因此，重要的是要评估当前可用的功能集是否满足您的要求。

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>如何获得全球库存核算公开预览版

> [!IMPORTANT]
> 若要使用全球库存核算，您必须具有启用了 LCS 的高可用性环境（而不是 OneBox 环境）。 此外，您必须运行 Supply Chain Management 版本 10.0.19 或更高版本。

若要注册全球库存核算公开预览版，请将您的 LCS 环境 ID 通过电子邮件发送至[全球库存核算团队](mailto:GlobalInventoryAccounting@service.microsoft.com)。 在您获得该计划的批准后，团队将向您发送一封跟进电子邮件，其中包含全球库存核算测试密钥和您的服务终结点。 收到测试密钥后，您可以[安装加载项](#install)。

## <a name="licensing"></a>许可授权

全球库存核算与可用于 Supply Chain Management 的库存核算的标准功能一起获得许可。 您无需购买其他许可证即可使用全球库存核算。

## <a name="prerequisites"></a>先决条件

### <a name="set-up-microsoft-power-platform-integration"></a>设置 Microsoft Power Platform 集成

您必须先通过执行以下步骤与 Microsoft Power Platform 集成，才能启用加载项功能。

1. 打开要在其中添加服务的 LCS 环境。
1. 转到 **完整详细信息**。
1. 在 **Power Platform 集成** 部分中，选择 **设置**。
1. 在 **Power Platform 环境设置** 对话框中，选中该复选框，然后选择 **设置**。 通常，设置需要 60 到 90 分钟。
1. 在完成 Microsoft Power Platform 环境的设置后，页面将显示您的环境的名称。 此外，**Power Platform 集成** 部分显示声明，“Power Platform 环境设置完成。” 全球库存核算不需要双写入应用程序。

有关详细信息，请参阅[在环境部署后设置](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment)。

### <a name="set-up-dataverse"></a>设置 Dataverse

在设置 Dataverse 之前，通过执行以下步骤将全球库存核算服务原则添加到您的租户。

1. 如[安装 Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2) 中所述安装 Windows PowerShell v2 的 Azure AD 模块。
1. 运行以下 PowerShell 命令。

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

接下来，通过执行以下步骤在 Dataverse 中为全球库存核算创建应用程序用户。

1. 打开您的 Dataverse 环境的 URL。
1. 转到 **高级设置 \> 系统 \> 安全 \> 用户**，创建应用程序用户。 使用 **视图** 字段将页面视图更改为 *应用程序用户*。
1. 选择 **新建**。
1. 将 **申请 ID** 字段设置为 *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*。
1. 选择 **分配角色**，然后选择 *系统管理员*。 如果有一个名为 *Common Data Service 用户* 的角色，也选择它。
1. 重复前面的步骤，但将 **应用程序 ID** 字段设置为 *5f58fc56-0202-49a8-ac9e-0946b049718b*。

有关详细信息，请参阅[创建应用程序用户](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)。

如果您的 Dataverse 安装的默认语言不是英语，请按照以下步骤操作。

1. 转到 **高级设置 \> 管理 \> 语言**。
1. 选择 *英语* (*LanguageCode=1033*)，然后选择 **应用**。

## <a name="install-the-add-in"></a><a name="install"></a>安装加载项

按照以下步骤安装加载项，以便您可以使用全球库存核算。

1. [注册](#sign-up)全球库存核算公开预览版。
1. 登录 [LCS](https://lcs.dynamics.com/Logon/Index)。
1. 转到 **预览功能管理**。
1. 选择加号 (**+**)。
1. 在 **代码** 字段中，输入您的全球库存核算的加载项测试密钥。 （您应该已在注册时通过电子邮件收到您的测试密钥。）
1. 选择 **解锁**。
1. 打开要在其中添加服务的 LCS 环境。
1. 转到 **完整详细信息**。
1. 转到 **Power Platform 集成**，然后选择 **设置**。
1. 在 **Power Platform 环境设置** 对话框中，选中该复选框，然后选择 **设置**。 通常，设置需要 60 到 90 分钟。
1. 完成 Microsoft Power Platform 环境的设置后，在 **环境加载项** 快速选项卡上，选择 **安装新加载项**。
1. 选择 **全球库存核算**。
1. 按照安装指南操作，并同意条款和条件。
1. 选择 **安装**。
1. 在 **环境加载项** 快速选项卡上，您应该会看到正在安装全球库存核算。 几分钟后，状态应从 *正在安装* 变为 *已安装*。 （您可能必须刷新页面才能看到此更改。）此时，全球库存核算可以使用了。

## <a name="set-up-the-integration"></a>设置集成

按照以下步骤设置全球库存核算和 Supply Chain Management 之间的集成。

1. 登录 Supply Chain Management。
1. 转到 **系统管理 \> 功能管理**。
1. 选择 **检查更新**。
1. 在 **全部** 选项卡上，搜索名为 *全球库存核算* 的功能。
1. 选择 **立即启用**。
1. 转到 **全球库存核算 \> 设置 \> 全球库存核算参数 \> 集成参数**。
1. 在 **数据服务终结点** 和 **全球库存核算终结点** 字段中，输入全球库存核算团队在您注册预览版时发送的电子邮件中的 URL。

全球库存核算现在可以使用了。
