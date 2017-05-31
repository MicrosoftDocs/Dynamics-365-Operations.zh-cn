---
title: "安装和配置 Microsoft Dynamics 365 for Operations - Warehousing。"
description: "此主题描述如何安装和配置 Microsoft Dynamics 365 for Operations - Warehousing。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>安装和配置 Microsoft Dynamics 365 for Operations - Warehousing。

[!include[banner](../includes/banner.md)]


此主题描述如何安装和配置 Microsoft Dynamics 365 for Operations - Warehousing。

Dynamics 365 for Operations - Warehousing 是 Google Play Store 和 Windows 应用商店中提供的一款应用程序。 对于当前版本的 Microsoft Dynamics 365 for Operations，此应用程序以独立组件的形式提供，也就是说，自行部署在用于仓库任务的设备上。 要在 Dynamics 365 for Operations 环境中使用此应用程序，必须将其下载到每台设备上并配置，以便连接到您的 Dynamics 365 for Operations 环境。 此主题介绍如何在您的设备上安装此应用程序。 还介绍如何配置此应用程序，以便连接到您的 Dynamics 365 for Operations 环境。

## <a name="prerequisites"></a>先决条件
此应用程序可在 Android 和 Windows 操作系统上使用。 若要使用此应用程序，设备上必须安装以下受支持操作系统之一。 还必须安装以下受支持的 Dynamics 365 for Operations 版本之一。 请使用下表中的信息评估您的硬件和软件环境是否支持此项安装。

| 平台                    | 版本                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4、5.0、6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10（所有版本）                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations 版本 1611 或 Microsoft Dynamics Dynamics AX 版本 7.0/7.0.1，以及带修补程序 KB 3210014 的 Microsoft Dynamics AX 平台更新 2 |

## <a name="get-the-app"></a>获取应用
-   Windows (UWP) - [Windows 应用商城中的 Dynamics 365 for Operations - Warehousing](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Google Play Store 中的 Dynamics 365 for Operations - Warehousing](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>在 Active Directory 中创建 Web 服务应用程序
要使该应用程序与特定 Dynamics 365 for Operations 服务器交互，必须在 Azure Active Directory 中注册一个 Web 服务应用程序，以便获得 Dynamics 365 for Operations 租户。 出于安全原因，我们建议您为使用的每台设备创建一个 Web 服务应用程序。 若要在 Azure Active Directory (Azure AD) 中创建 Web 服务应用程序，请完成以下步骤：

1.  在 Web 浏览器中，转至 <https://manage.windowsazure.com>。
2.  输入有权访问 Azure 订阅的用户的名称和密码。
3.  在 Azure Portal 中的左导航窗格内，单击 **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  在网格中，选择 Dynamics 365 for Operations 使用的 Active Directory 实例。
5.  在顶部工具栏中，单击**应用程序**。 [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  在底部窗格中，单击**添加**。 将启动**添加应用程序**向导。
7.  输入应用程序的名称，然后选择 **Web 应用程序和/或 Web API**。 [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  输入登录 URL，这是您的租户中的应用程序 URL，即根 Operations URL。 此登录 URL 目前尚未积极用于为应用程序执行身份验证，但是这是必填字段。 在“应用程序 ID URI”字段中输入同一 URL。 [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  转至**配置**选项卡。 [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. 向下滚动，直到显示**其他应用程序的权限**部分。 单击**添加应用程序**。 [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. 选择列表中的 **Microsoft Dynamics ERP**。 单击该页面右上角中的**完成检查**按钮。 [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. 在**委托权限**列表中，选中所有复选框。 单击**保存**。 [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. 记下以下信息：
    -   **客户端 ID** - 向上滚动页面时，将显示**客户端 ID**。
    -   **密钥** - 在**密钥**部分中，通过选择持续时间创建密钥，然后复制该密钥。 该密钥在后面将称为**客户端密码**。

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>在 Dynamics 365 for Operations 中创建和配置用户帐户
要使 Dynamics 365 for Operations 使用您的 Azure AD 应用程序，需要完成以下配置步骤：

1.  在 Azure Active Directory 中为 Dynamics 365 for Operations 租户创建一个新用户帐户。 此用户帐户用于访问 Dynamics 365 for Operations 服务器提供的 Warehousing 应用程序的特定自定义服务。 完成此步骤之后，您将拥有 WMDP 用户凭据，其中包含 WMDP 电子邮件地址和 WMDP 密码。 若要了解有关如何向 Azure AD 和 Dynamics 365 for Operations 添加用户的基本步骤，请参阅以下教程：[注册 Microsoft Dynamics 365 for Operations 订阅](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription)。
2.  创建与 Warehousing 应用程序用户凭据对应的 Dynamics 365 for Operations 用户
    1.  在 Dynamics 365 for Operations 中，转至**系统管理** &gt; **常用** &gt; **用户**。
    2.  创建新用户。
    3.  指定 Warehouse 移动设备用户，如以下屏幕截图所示。 [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  将您的 Azure Active Directory 应用程序与该 Warehousing 应用程序用户关联。
    1.  在 Dynamics 365 for Operations 中，转至**系统管理** &gt; **设置** &gt; **Azure Active Directory 应用程序**。
    2.  创建新行。
    3.  输入（上一部分中获取的）**客户端 ID**，为其命名，然后选择以前创建的用户。 建议您标记自己的所有设备，这样就可以从该页面中轻松取消其对 Dynamics 365 for Operations 的访问权限，以防这些设备丢失。 [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>配置应用程序
必须在设备上配置此应用程序，以便通过 Azure AD 应用程序连接到 Dynamics 365 for Operations 服务器。 为此，请完成以下步骤。

1.  在应用程序中，转至**连接设置**。
2.  清除**演示模式**字段。 [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  输入以下信息：- **Azure Active Directory 客户端 ID** - 步骤 13 中“在 Active Directory 中创建 Web 服务应用程序”内创建的客户端 ID。 - **Azure Active Directory 客户端密码** - 步骤 13 中“在 Active Directory 中创建 Web 服务应用程序”内创建的客户端密码。 - **Azure Active Directory 资源** - Azure AD Directory 资源描述 Dynamics 365 for Operations 根 URL。 **注释**：此字段请勿使用正斜杠支付 (/) 结尾。 - **Azure Active Directory 租户** - Dynamics 365 for Operations 服务器使用的 Azure AD Directory 租户：https://login.windows.net/&lt;your-AD-tenant-ID&gt;。 例如：https://login.windows.net/contosooperations.onmicrosoft.com。 
**注释**：此字段请勿使用正斜杠支付 (/) 结尾。 - **公司** - 在希望应用程序连接到的 Dynamics 365 for Operations 中输入法人。 [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  选择应用程序左上角中的**后退**按钮。 此应用程序现在将连接到您的 Dynamics 365 for Operations 服务器，并将显示仓库工作人员的登录屏幕。 [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>取消设备的访问权限
如果设备丢失或被入侵，您必须取消设备对 Dynamics 365 for Operations 的访问权限。 以下步骤介绍推荐的访问权限取消流程。

1.  在 Dynamics 365 for Operations 中，转至**系统管理** &gt; **设置** &gt; **Azure Active Directory 应用程序**。
2.  删除与要取消访问权限的设备对应的行。 记下用于所删除设备的**客户端 ID**。
3.  登录 Azure 经典门户，地址为 <https://manage.windowsazure.com>。
4.  单击左侧菜单中的 **Active Directory** 图标，然后单击所需目录。
5.  在顶部菜单中，单击**应用程序**，然后单击要配置的应用程序。 将显示**快速入门**页面，其中包含单一登录信息和其他配置信息。
6.  单击**配置**选项卡，向下滚动并确保应用程序的**客户端 ID** 与此部分的步骤 2 中的相同。
7.  单击命令栏中的**删除**按钮。
8.  单击确认消息中的**是**。





