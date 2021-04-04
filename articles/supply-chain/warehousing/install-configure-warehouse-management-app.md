---
title: 安装和连接仓库管理移动应用
description: 本主题说明如何在每个移动设备上安装仓库管理移动应用，以及如何进行配置以将其连接到 Microsoft Dynamics 365 Supply Chain Management 环境。
author: MarkusFogelberg
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e1e8c8b1464a38a0145cbdcdcb4882db00d3c4c1
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487017"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>安装和连接仓库管理移动应用

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> 本主题介绍如何配置新的仓库管理移动应用。 如果要查找有关如何配置旧仓库应用的信息，请参阅[安装和连接仓库应用](../../supply-chain/warehousing/install-configure-warehousing-app.md)。

本主题说明如何在每个移动设备上下载和安装仓库管理移动应用，以及如何配置应用来将其连接到 Supply Chain Management 环境。 可以手动配置每个设备，也可以通过文件或使用 QR 代码导入连接字符串。

## <a name="system-requirements"></a>系统要求

Windows 和 Google Android 操作系统均支持仓库管理移动应用。 若要使用此应用，您的移动设备上必须安装以下操作系统之一：

- Windows 10（通用 Windows 平台 \[UWP\]）2018 年 10 月更新 1809（内部版本 10.0.17763）或更高版本
- Android 4.4 或更高版本

## <a name="turn-on-the-feature"></a>开启功能

您必须先在系统中打开相关功能，然后才能使用此应用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：

- **模块**：*仓库管理*
- **功能名称**：*新仓库应用的用户设置、图标和步骤标题*

## <a name="get-the-warehouse-management-mobile-app"></a>获取仓库管理移动应用

对于较小部署，通常可能在每个设备上从相关商店安装此应用，然后手动配置与您在使用的环境之间的连接。

对于较大部署，您可以自动化应用部署和/或配置，如果您管理很多设备，这样会更加方便。 例如，您可能使用移动设备管理和移动应用程序管理解决方案，如 [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune)。 有关如何使用 Intune 添加应用程序的信息，请参阅[向 Microsoft Intune 添加应用](https://docs.microsoft.com/mem/intune/apps/apps-add)。

### <a name="install-the-app-from-an-app-store"></a>从应用商店安装应用

在单个设备上安装应用的最简单方法是从应用商店安装，应用商店始终会提供最新的正式发布版本。 Microsoft Intune 也可以从应用商店获取应用。 使用以下链接之一从应用商店安装应用：

- **Windows (UWP)**：[Microsoft Store 中的仓库管理](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android**：[Google Play 商店中的仓库管理](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>从 Microsoft App Center 下载应用

作为从应用商店安装的替代方法，您可以从 Microsoft App Center 下载应用。 App Center 提供可以旁加载的可安装包。 除了当前版本外，App Center 还允许您下载以前的版本，而且可以提供包含您可以试用的即将发布功能的预览版本。要从 Microsoft App Center 下载仓库管理移动应用的当前、先前或预览版本，请使用以下链接之一：

- **Windows (UWP)**：[仓库管理 (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    有关如何在 Windows 设备上安装下载的包然后设置所需证书的说明，请参阅[从 App Center 安装版本](https://docs.microsoft.com/appcenter/distribution/installation)。

- **Android**：[仓库管理 (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    如果您下载预览版，需要执行一些额外的步骤进行安装。 有关详细信息，请参阅[测试 Android 应用](https://docs.microsoft.com/appcenter/distribution/testers/testing-android)。

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>在 Azure Active Directory 中创建 Web 服务应用程序

若要使仓库管理移动应用与特定 Supply Chain Management 服务器交互，必须在 Azure Active Directory (Azure AD) 中注册一个 Web 服务应用程序，以便获得 Supply Chain Management 租户。 以下过程显示了一种完成此任务的方法。 有关详细信息和备用方法，请参阅此过程后的链接。

1. 在 Web 浏览器中，转至 [https://portal.azure.com](https://portal.azure.com/)。
1. 输入有权访问 Azure 订阅的用户的名称和密码。
1. 在 Azure 门户的左侧导航窗格中，选择 **Azure Active Directory**。

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. 确保使用 Supply Chain Management 所用 Azure AD 实例。
1. 在 **管理** 列表中，选择 **应用注册**。

    ![应用注册](media/app-connect-azure-register.png "应用注册")

1. 在工具栏中，选择 **新注册** 打开 **注册应用程序** 向导。
1. 输入应用程序的名称，选择 **仅此组织目录中的帐户** 选项，然后选择 **注册**。

    ![注册应用程序向导](media/app-connect-azure-register-wizard.png "注册应用程序向导")

1. 将打开您的新应用注册。 记下 **应用程序（客户端）ID** 值，因为后面需要该值。 本主题后文将此 ID 称为 *客户端 ID*。

    ![应用程序（客户端）ID](media/app-connect-azure-app-id.png "应用程序（客户端）ID")

1. 在 **管理** 列表中，选择 **证书和密码**。 然后选择下面的一个按钮，具体取决于要如何针对身份验证配置应用。 （有关详细信息，请参阅本主题后文的[使用证书或客户端密码](#authenticate)部分。）

    - **上传证书** – 上传证书充当密码。 建议使用此方法，因为更安全，也可以更完整地自动执行。 如果要在 Windows 设备上运行仓库管理移动应用，请记下上传证书后显示的 **指纹** 值。 在 Windows 设备上配置证书时需要此值。
    - **新客户端密码** – 通过在 **密码** 部分中输入密钥说明和持续时间创建密钥，然后选择 **添加**。 创建密钥备份，然后安全存储。

    ![证书和密码](media/app-connect-azure-authentication.png "证书和密码")

有关如何在 Azure AD 中设置 Web 服务应用程序的详细信息，请参阅以下资源：

- 有关如何使用 Windows PowerShell 在 Azure AD 中设置 Web 服务应用程序的说明，请参阅[方法：使用 Azure PowerShell 和证书创建服务主体](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell)。
- 有关如何在 Azure AD 中手动创建 Web 服务应用程序的完整详细信息，请参阅以下主题：

    - [快速入门：向 Microsoft 身份平台注册应用程序](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [方法：使用门户创建可访问资源的 Azure AD 应用程序和服务主体](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>在 Supply Chain Management 中创建和配置用户帐户

若要让 Supply Chain Management 使用您的 Azure AD 应用程序，请执行以下步骤。

1. 创建与仓库管理移动应用的用户凭据对应的用户：

    1. 在 Supply Chain Management 中，转到 **系统管理 \> 用户 \> 用户**。
    1. 创建一个用户。
    1. 分配仓库移动设备用户。

    ![分配仓库移动设备用户](media/app-connect-app-users.png "分配仓库移动设备用户")

1. 将您的 Azure AD 应用程序与仓库管理移动应用用户关联：

    1. 转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。
    1. 创建一行。
    1. 输入在上一部分中记下的客户端 ID，为其命名，然后选择刚才创建的用户。 建议标记所有设备。 然后，如果设备丢失，可以轻松从此页解除其对 Supply Chain Management 的访问权限。

    ![Azure Active Directory 应用程序](media/app-connect-aad-apps.png "Azure Active Directory 应用程序")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>使用证书或客户端密码进行身份验证

使用 Azure AD 进行身份验证可以安全地将移动设备连接到 Supply Chain Management。 可以通过使用客户端密码或证书进行身份验证。 如果将导入连接设置，建议使用证书，不使用客户端密码。 因为客户端密码始终安全存储，所以不能从连接设置文件或 QR 代码导入，如本主题后文所述。

请求令牌时，可以将证书用作密码来证明应用程序的身份。 将把证书的公开部分上传到 Azure 门户中的应用注册，虽然必须将完整证书部署到安装仓库管理移动应用的每个设备上。 您的组织负责以轮换等方式管理证书。 可使用自签名证书，但是始终应该使用不可导出证书。

必须在运行仓库管理移动应用的每个设备本地提供证书。 有关如何在使用 Intune 时管理 Intune 控制的设备的证书的信息，请参阅[在 Microsoft Intune 中将证书用于身份验证](https://docs.microsoft.com/mem/intune/protect/certificates-configure)。

## <a name="configure-the-application-by-importing-connection-settings"></a>通过导入连接设置配置应用程序

若要更轻松地在大量移动设备上维护和部署此应用程序，可以导入连接设置，而不是在每个设备上手动输入。 此部分介绍如何创建和导入设置。

### <a name="create-a-connection-settings-file-or-qr-code"></a>创建连接设置文件或 QR 代码

可以从文件或 QR 代码导入连接设置。 对于这两种方法，首先必须创建使用 JavaScript Object Notation (JSON) 格式和语法的设置文件。 此文件中包含一个连接列表，该列表中包含必须添加的单个连接。 下表汇总了必须在连接设置文件中指定的参数。

| 参数 | 说明 |
|---|---|
| ConnectionName | 指定连接设置的名称。 最大长度为 20 个字符。 因为此值是连接设置的唯一标识符，因此请确保其在列表中唯一。 如果设备中已有同名连接，所导入文件中的设置将覆盖该连接。 |
| ActiveDirectoryClientAppId | 指定[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。 |
| ActiveDirectoryResource | 指定 Supply Chain Management 的根 URL。 |
| ActiveDirectoryTenant | 指定要用于 Supply Chain Management 服务器的 Azure AD 租户。 此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。 下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。 |
| 公司 | 在 Supply Chain Management 中指定希望应用程序连接到的法人。 |
| ConnectionType | （可选）指定连接设置应使用证书还是客户端密码连接到环境。 有效值为 *certificate* 和 *clientsecret*。 默认值为 *certificate*。<p>**注意：** 不能导入客户端密码。</p> |
| IsEditable | （可选）指定应用用户是否应该可以编辑连接设置。 有效值为 *true* 和 *false*。 默认值为 *true*。 |
| IsDefault | （可选）指定连接是否为默认连接。 打开应用时，将提前选中设置为默认连接的连接。 只能将一个连接设置为默认连接。 有效值为 *true* 和 *false*。 默认值为 *false*。 |
| CertificateThumbprint | （可选）对于 Windows 设备，您可以为连接指定证书指纹。 对于 Android 设备，则应用用户必须在首次使用连接时选择证书。 |

以下示例显示一个有效连接设置文件，该文件中包含两个连接。 如您所见，连接列表（文件中的名称为 *ConnectionList*）是一个对象，该对象有一个将每个连接作为对象存储的阵列。 每个对象必须使用括号 ({}) 括起来并使用逗号分隔，而阵列则必须使用方括号 (\[\]) 括起来。

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

可以将信息保存为 JSON 文件，或生成具有相同内容的 QR 代码。 如果将信息保存为文件，建议使用默认名称 *connections.json* 保存，尤其是将把其存储在每个移动设备上的默认位置中时。

### <a name="save-the-connection-settings-file-on-each-device"></a>将连接设置文件保存到每个设备上

您通常使用设备管理工具或脚本将连接设置文件发放到您管理的每个设备上。 如果在每个设备上保存连接设置文件时使用默认名称和位置，仓库管理移动应用将自动导入该文件，即使是在安装该应用后首次运行期间。 如果为该文件使用自定义名称或位置，应用用户必须在首次运行期间指定值。 但是，以后此应用将继续使用指定的名称和位置。

每次启动此应用时，都将从连接设置的之前位置重新导入连接设置，以确定是否进行了任何更改。 此应用将仅更新与连接设置文件中的连接同名的连接。 将不更新用户创建且使用其他名称的连接。

不能使用连接设置文件删除连接。

如前所述，默认文件名为 *connections.json*。 默认文件位置取决于使用的是 Windows 设备还是 Android 设备：

- **Windows：**`C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android**：`Android\data\com.Microsoft.WarehouseManagement\files`

通常在首次运行此应用后自动创建这些路径。 但是，如果必须在安装前将连接设置文件传输到设备，可以手动创建这些路径。

> [!NOTE]
> 如果卸载了此应用，将删除默认路径及其内容。

### <a name="import-the-connection-settings"></a>导入连接设置

执行以下步骤从文件或 QR 代码导入连接设置。

1. 在您的移动设备上启动仓库管理移动应用。 首次启动该应用时，会显示一条欢迎消息。 选择 **选择连接**。

    ![欢迎消息](media/app-configure-welcome-screen.png "欢迎消息")

1. 如果要从文件导入连接设置，并且保存该文件时使用的是默认名称和默认位置，应用可能已经找到了该文件。 在这种情况下，直接跳到步骤 4。 否则，选择 **设置连接**，然后继续执行步骤 3。

    ![设置连接](media/app-configure-set-up-connection.png "设置连接")

1. 在 **连接设置** 对话框中，选择 **从文件添加** 或 **从 QR 码添加**，具体取决于您要导入设置的方式：

    - 如果要从文件导入连接设置，则选择 **从文件添加**，浏览到本地设备上的文件，然后选择它。 如果选择自定义位置，应用将存储该文件，并在下次自动使用。
    - 如果要通过扫描 QR 码导入连接设置，则选择 **从 QR 码添加**。 应用将提示您提供使用设备摄像头所需权限。 提供权限后，将启动摄像头，以便您将其用于扫描。 您可能发现很难获得正确扫描，具体取决于设备摄像头的质量和 QR 代码的复杂程度。 在这种情况下，请尝试通过为每个 QR 码仅生成一个连接来降低 QR 代码的复杂程度。 （现在，只能使用设备摄像头扫描 QR 代码。）

    ![连接设置菜单](media/app-configure-connection-setup-flyout.png "连接设置菜单")

1. 成功加载连接设置后，将显示所选的连接。

    ![已加载连接设置](media/app-configure-select-connection.png "已加载连接设置")

1. 如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。

    ![Android 设备上的选择证书提示](media/app-configure-select-certificate.png "Android 设备上的选择证书提示")

1. 此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。

    ![登录页](media/app-configure-sign-in-page.png "登录页")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>手动配置应用程序

如果您没有文件或 QR 码，可以在设备上手动配置此应用，以便通过 Azure AD 应用程序连接到 Supply Chain Management 服务器。

1. 在您的移动设备上启动仓库管理移动应用。
1. 如果应用以 **演示模式** 启动，选择 **连接设置**。 如果应用启动时出现 **登录** 页，选择 **更改连接**。
1. 选择 **设置连接**。

    ![设置连接](media/app-configure-set-up-connection.png "设置连接")

1. 选择 **手动输入**。

    ![连接设置菜单](media/app-configure-connection-setup-flyout.png "连接设置菜单")

    **新建连接** 页将出现，显示手动输入连接详细信息所需的设置。

    ![手动连接字段](media/app-configure-input-manually.png "手动连接字段")

1. 输入以下信息：

    - **使用客户端密码** – 将此选项设置为 _是_ 以使用客户端密码和 Supply Chain Management 进行身份验证。 若要使用证书进行身份验证，请将其设置为 _否_。 （有关详细信息，请参阅本主题前面的[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)一节。）
    - **连接名称** – 输入新连接的名称。 下次打开连接设置时，将在 **选择连接** 字段中显示此名称。 您输入的名称必须唯一。 （换句话说，如果在设备上存储了其他任何连接名称，该名称必须与这些名称不同。）
    - **Active Directory 客户端 ID** – 输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端 ID。
    - **Active Directory 客户端密码** – 仅当 **使用客户端密码** 选项设置为 _是_，此字段才可用。 输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的客户端密码。
    - **Active Directory 证书指纹** – 此字段仅可用于 Windows 设备，且仅在 **使用客户端密码** 选项设置为 _否_ 时可用。 输入[在 Azure Active Directory 中创建 Web 服务应用程序](#create-service)部分中设置 Azure AD 时记下的证书指纹。
    - **Active Directory 资源** – 指定 Supply Chain Management 的根 URL。

        > [!IMPORTANT]
        > 请勿为此值使用反斜杠 (/)。

    - **Active Directory 租户** – 输入与 Supply Chain Management 服务器一起使用的 Azure AD 租户。 此值的格式为 `https://login.windows.net/<your-Azure-AD-tenant-ID>`。 下面是一个示例：`https://login.windows.net/contosooperations.onmicrosoft.com`。

        > [!IMPORTANT]
        > 请勿为此值使用反斜杠 (/)。

    - **公司** – 在希望应用程序连接到的 Supply Chain Management 中输入法人（公司）。

1. 选择页面右上角的 **保存** 按钮。
1. 如果在使用 Android 设备，并使用证书进行身份验证，设备将提示您选择证书。
1. 此应用将连接到您的 Supply Chain Management 服务器，并显示登录页。

## <a name="remove-access-for-a-device"></a>取消设备的访问权限

如果设备丢失或被入侵，您必须取消设备对 Supply Chain Management 的访问权限。 以下步骤介绍推荐的访问权限取消流程。

1. 转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。
1. 删除与要取消访问权限的设备对应的行。 记下用于该设备的客户端 ID，因为后面需要它。

    如果仅注册了一个客户端 ID，并且多个设备使用同一个客户端 ID，则必须将新连接设置推送到这些设备。 否则，它们将失去访问权限。

1. 登录 Azure 门户，地址为 [https://portal.azure.com](https://portal.azure.com/)。
1. 在左侧导航窗格中，选择 **Active Directory**，然后确保位于正确目录中。
1. 在 **管理** 列表中，选择 **应用程序注册**，然后选择要配置的应用程序。 将显示 **设置** 页面，其中包含配置信息。
1. 确保应用程序的客户端 ID 与您在步骤 2 中记下的客户端 ID 匹配。
1. 在工具栏上，选择 **删除**。
1. 在出现的确认消息中选择 **是**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]