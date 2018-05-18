---
title: "安装和配置 Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing"
description: "此主题描述如何安装和配置 Microsoft Dynamics 365 for Finance and Operations - Warehousing。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: zh-cn
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>安装和配置 Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> 此主题介绍如何为云部署配置仓库。 如果您需要了解如何为本地部署配置仓库，请参阅[用于本地部署的仓库](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md)。


此主题描述如何安装和配置 Microsoft Dynamics 365 for Finance and Operations - Warehousing。

Finance and Operations - Warehousing 是 Google Play Store 和 Windows 应用商店中提供的一款应用程序。 对于当前版本的 Finance and Operations，此应用程序以独立组件的形式提供，也就是说，自行部署在用于仓库任务的设备上。 若要在 Finance and Operations 环境中使用此应用程序，必须将其下载到每台设备上并配置，以便连接到您的 Finance and Operations 环境。 此主题介绍如何在您的设备上安装此应用程序。 它还介绍如何配置此应用程序，以便连接到您的 Finance and Operations 环境。

## <a name="prerequisites"></a>必备项
此应用程序可在 Android 和 Windows 操作系统上使用。 若要使用此应用程序，设备上必须安装以下受支持操作系统之一。 还必须安装以下受支持的 Finance and Operations 版本之一。 请使用下表中的信息评估您的硬件和软件环境是否支持此项安装。

| 平台                    | 版本                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4、5.0、6.0、7.0、8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10（所有版本）                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations 版本 1611 <br>- 或者 - <br>Microsoft Dynamics AX 版本 7.0/7.0.1 和带修补程序 KB 3210014 的 Microsoft Dynamics AX 平台更新 2 |

## <a name="get-the-app"></a>获取应用
-   Windows (UWP)
     - [Windows 应用商店上的 Finance and Operations - Warehousing](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Google Play Store 上的 Finance and Operations - Warehousing](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Zebra App Gallery 上的 Finance and Operations - Warehousing](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>在 Azure Active Directory 中创建 Web 服务应用程序
若要使该应用程序与特定 Finance and Operations 服务器交互，必须在 Azure Active Directory 中注册一个 Web 服务应用程序，以便获得 Finance and Operations 租户。 出于安全原因，我们建议您为使用的每台设备创建一个 Web 服务应用程序。 若要在 Azure Active Directory (Azure AD) 中创建 Web 服务应用程序，请完成以下步骤：

1.  在 Web 浏览器中，转至 <https://portal.azure.com>。
2.  输入有权访问 Azure 订阅的用户的名称和密码。
3.  在 Azure Portal 中的左导航窗格内，单击 **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  确保 Finance and Operations 使用的是 Active Directory 实例。
5.  在列表中，单击**应用程序注册**。 [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  在顶部窗格中，单击 **新应用程序注册**。 将启动**添加应用程序**向导。
7.  输入应用程序的名称，然后选择 **Web 应用程序/Web API**。 输入登录 URL，这是您的 Web 应用 URL。 此 URL 与您的部署 URL 相同，但 Oauth 添加到末尾。 单击“**创建**”。 [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  在列表中选择新应用程序。 [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  记住**应用程序 ID**，后面需要它。 **应用程序 ID** 在后文称为**客户端 ID**。
10. 在**设置窗格**中，单击**密钥**。 通过在**密码**部分中输入密钥说明和持续时间创建密码。 
11. 单击**保存**，然后复制该密钥。 该密钥在后面将称为**客户端密码**。 [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>在 Finance and Operations 中创建和配置用户帐户
若要使 Finance and Operations 使用您的 Azure AD 应用程序，需要完成以下配置步骤：

1.  在 Azure Active Directory 中为 Finance and Operations 租户创建一个新用户帐户。 此用户帐户用于访问 Finance and Operations 服务器提供的 Warehousing 应用程序的特定自定义服务。 完成此步骤之后，您将拥有 WMDP 用户凭据，其中包含 WMDP 电子邮件地址和 WMDP 密码。 若要了解有关如何向 Azure AD 和 Finance and Operations 添加用户的基本步骤，请参阅以下教程：[注册 Finance and Operations 订阅](../../dev-itpro/dev-tools/sign-up-preview-subscription.md)。
2.  创建与 Warehousing 应用程序用户凭据对应的 Finance and Operations 用户。
    1.  在 Finance and Operations 中，转至**系统管理** &gt; **常用** &gt; **用户**。
    2.  创建新用户。
    3.  指定 Warehouse 移动设备用户，如以下屏幕截图所示。 [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  将您的 Azure Active Directory 应用程序与该 Warehousing 应用程序用户关联。
    1.  在 Finance and Operations 中，转至**系统管理** &gt; **设置** &gt; **Azure Active Directory 应用程序**。
    2.  创建新行。
    3.  输入（上一部分中获取的）**客户端 ID**，为其命名，然后选择以前创建的用户。 建议您标记自己的所有设备，这样就可以从该页面中轻松取消其对 Finance and Operations 的访问权限，以防这些设备丢失。 [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>配置应用程序
必须在设备上配置此应用程序，以便通过 Azure AD 应用程序连接到 Finance and Operations 服务器。 为此，请完成以下步骤。

1.  在应用程序中，转至**连接设置**。
2.  清除**演示模式**字段。 <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  输入以下信息： 
    + **Azure Active Directory 客户端 ID** - 步骤 9 中“在 Active Directory 中创建 Web 服务应用程序”内创建的客户端 ID。 
    + **Azure Active Directory 客户端密码** - 步骤 11 中“在 Active Directory 中创建 Web 服务应用程序”内创建的客户端密码。 
    + **Azure Active Directory 资源** - Azure AD Directory 资源描述 Finance and Operations 根 URL。 **注释**：此字段请勿使用正斜杠支付 (/) 结尾。 
    + **Azure Active Directory 租户** - 与 Finance and Operations 服务器一起使用的 Azure AD Directory 租户：`https://login.windows.net/your-AD-tenant-ID`。 例如：`https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**注释**：此字段请勿使用正斜杠支付 (/) 结尾。 
    + **公司** - 在希望应用程序连接到的 Finance and Operations 中输入法人。 <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  选择应用程序左上角中的**后退**按钮。 此应用程序现在将连接到您的 Finance and Operations 服务器，并将显示仓库工作人员的登录屏幕。 <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

有关如何设置 Dynamics 365 for Finance and Operations – Warehousing 以使用移动设备上的摄像头扫描条码的详细信息，请参阅[在 Dynamics 365 for Finance and Operations – Warehousing 中使用摄像头扫描条码](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>取消设备的访问权限
如果设备丢失或被入侵，您必须取消设备对 Finance and Operations 的访问权限。 以下步骤介绍推荐的访问权限取消流程。

1.  在 Finance and Operations 中，转至**系统管理** &gt; **设置** &gt; **Azure Active Directory 应用程序**。
2.  删除与要取消访问权限的设备对应的行。 记住已删除设备所用**客户端 ID**，后面需要它。
3.  登录 Azure 门户，地址为 <https://portal.azure.com>。
4.  单击左侧菜单中的 **Active Directory** 图标，然后确保位于正确的目录中。
5.  在列表中，单击**应用程序注册**，然后单击要配置的应用程序。 将显示**设置**页面，其中包含配置信息。
6.  确保应用程序的**客户端 ID** 与本部分步骤 2 中的相同。
7.  单击顶部窗格中的**删除**按钮。
8.  单击确认消息中的**是**。

