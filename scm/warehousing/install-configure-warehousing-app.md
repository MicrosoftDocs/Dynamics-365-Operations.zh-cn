---
title: "安装和配置 Microsoft Dynamics 365 的工序&#8211;仓库"
description: "此主题描述如何设置和配置 Microsoft Dynamics 365 -工序的仓库。"
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>安装和配置 Microsoft Dynamics 365 的工序&#8211;仓库

此主题描述如何设置和配置 Microsoft Dynamics 365 -工序的仓库。

工序的 Dynamics 365 -仓库是应用程序可在谷歌播放商店和 Windows 商店。 对于当前版本工序的 Microsoft Dynamics 365，提供此应用为单独组件，也就是说在用于仓库任务的设备的自部署。 为了使用应用在您的环境，Dynamics 365。工序必须下载的设备在每个应用和配置它连接到您的环境的 Dynamics 365。工序 此主题介绍如何设置在您的设备上应用。 它还介绍了如何配置连接到您的应用工序环境的 Dynamics 365。

## <a name="prerequisites"></a>先决条件
应用可用的机器人和 Windows 操作系统。 若要使用此应用，您必须在您的设备上安装支持的操作系统的以下之一。 您还必须具有以下之一的版本支持工序的 Dynamics 365。 则您的硬件和软件环境支持准备安装，请使用下表中的信息在评估。

| 平台                    | 版本                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 机器人                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows 身份 (UWP)               | Windows 10 (所有版本)                                                                                                                                                   |
| 工序的 Dynamics 365 | 工序版本的 Microsoft Dynamics 365 - 1611 或 Microsoft Dynamics Dynamics AX 与 3210014 KB 修补程序的版本 7.0/7.0.1 和平台更新 Microsoft Dynamics AX 2 |

## <a name="get-the-app"></a>获取应用
-   Windows 身份 () - UWP [工序的 Dynamics 365 -仓库在 Windows https://www.microsoft.com/store/apps/9p1bffd5tstm)] (商店
-   [机器人-工序的 Dynamics 365 -在播放商店谷歌仓库] (https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>在 Active Directory 中创建一 Web 服务应用程序
要使应用与工序的特定服务器 Dynamics 365 进行交互，必须在一 Azure 的 Active Directory 的 Web 服务申请 Dynamics 365 的承租人。工序。 出于安全原因，我们建议您创建。您使用的设备的每个 Web 服务申请。 若要创建在 (Azure ML 的 Active Directory 的 AD) 的一 Web 服务应用程序，请完成以下步骤：

1.  在浏览器，请转到 https://manage.windowsazure.com>。
2.  输入名称和密码对 Azure 的预订的用户的。
3.  Azure 门户，左在的导航窗格中，单击** ** Active Directory。[] (。有效目录/media/wh /media/wh) example.png [![有效目录 wh 01] (示例。有效目录/media/wh /media/wh)] example.png(。/media/wh /media/wh 有效目录 example.png)
4.  在网格中，选择使用 Dynamics 365。工序的 Active Directory 实例。
5.  在工具栏上，依次单击顶部** **应用程序。 [![有效目录 wh![] (应用程序。有效目录/media/wh /media/wh 应用程序 1024x197.png)](。/media/wh /media/wh 有效目录 applications.png)
6.  在底部窗格中，单击** **添加。 ** **添加应用程序向导将启动。
7.  输入一个名称。应用程序并选择** Web 应用程序和网页/网站/web API **。 [![有效目录中添加 wh![] (应用程序。/media/wh /media/wh 有效目录中添加 application.png)](。/media/wh /media/wh 有效目录中添加 application.png)
8.  输入用于登录 URL，是在您的承租人的应用程序，则 URL 根目录工序 URL。 登录 URL 有效。当前不使用验证，应用，而是必填字段。 在应用 ID URI 相同字段中输入 URL。 [![wh![] (AD 添加属性。/media/wh /media/wh AD 添加 properties.png)](。/media/wh /media/wh AD 添加 properties.png)
9.  ** **到"配置"选项卡上的"转到。 [![wh![] (AD 配置应用。/media/wh /media/wh AD 配置 app.png)](。/media/wh /media/wh AD 配置 app.png)
10. 请下移，直到您看到**到其他应用程序的权限**部分。 单击** **添加应用程序。 [![wh![] (应用 AD 添加权限。/media/wh /media/wh 应用 AD 添加 permissions.png)](。/media/wh /media/wh 应用 AD 添加 permissions.png)
11. **选择 Microsoft Dynamics ERP **列表中。 **单击"完成检查**按在页面的右角。 ![wh [] (-![AD 权限。/media/wh AD - /media/wh)] permissions.png(。/media/wh /media/wh AD - permissions.png)
12. **在"委托权限**列出，则选择所有复选框。 Click **Save**. [![wh![] (AD 委托权限。/media/wh /media/wh AD 委托 permissions.png)](。/media/wh /media/wh AD 委托 permissions.png)
13. 记下以下信息：
    -   ** **客户 ID -，因为在滚动"页面中，您将看到一客户 ID ** **显示。
    -   ** **参数-在** **参数部分，通过选择持续时间为参数，并且参数复制。 此参数后将引用** **客户查询。

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>创建和配置 Dynamics 中 365 的用户帐户的工序
若要支持工序的 Dynamics 365 可以使用您 AD Azure 的应用程序，您需要完成以下步骤：配置

1.  Azure Active Directory 中创建的新的用户帐户 365 的承租人 Dynamics 的工序。 使用此用户帐户的目的将访问应用特定的仓库的客服，工序 365 的服务器 Dynamics 公开。 在完成此步骤后，将具有 WMDP 用户凭据，包括 WMDP 电子邮件地址和 WMDP 密码。 若要添加用户获悉的工序的基本步骤。Azure 的 AD 和 Dynamics 365，请参阅本指南：[工序为预订的/dynamics365/operations/dev] () itpro/sign 预览预订为 Microsoft Dynamics /dynamics365/operations/dev。
2.  创建对应于仓库的应用用户凭据的工序用户的 Dynamics 365。
    1.  在工序的 Dynamics 365，为**系统管理** &gt; **常见** &gt; ** **用户。
    2.  创建新用户。
    3.  如下屏幕截图中所示，分配仓库移动设备，用户。 [![wh 添加用户] (安全角色。/media/wh /media/wh 添加用户安全 role.png)](。/media/wh /media/wh 添加用户安全 role.png)

3.  Azure 您关联的 Active Directory 应用程序与仓库的应用用户。
    1.  在工序的 Dynamics 365，为**系统管理** &gt; **设置** &gt; ** Azure Active Directory **的应用程序。
    2.  创建新行。
    3.  **输入客户 ID ** (供在最后一部分)，请提供其一个名称，然后选择以前创建的用户。 我们建议您标记的所有设备，以便可以轻松地从该页面删除其到 Dynamics 365 的访问的工序，它们就丢失。 [![wh![AD 应用程序 (窗体)。/media/wh /media/wh AD 应用程序 form.png)](。/media/wh /media/wh AD 应用程序 form.png)

## <a name="configure-the-application"></a>配置应用程序
您必须配置对设备连接的应用到工序的 Dynamics 365 服务器通过 AD Azure 的应用程序。 为此，请完成以下步骤。

1.  在应用，请转到** **连接设置。
2.  **清除演示模式**字段。 [![连接设置应用 wh![] (演示模式。/media/wh /media/wh 应用连接设置演示模式 169x300.png)](。/media/wh /media/wh 应用连接设置 mode.png 演示)
3.  输入以下信息：** - Azure 的有效目录 ID **客户-客户 ID 在步骤 13 得到“在 Active Directory 中创建一 Web 服务应用程序”。 - ** Azure 的有效目录客户查询** -客户查询在第 13 步中获得“在 Active Directory 中创建一 Web 服务应用程序”。 - ** Azure 的有效目录- Azure **资源的目录 AD 资源工序表示 URL 的根目录 Dynamics 365。 **注释**:不要具有一结束"前进"字符此字段的反斜杠 (/)。 - ** Azure 的承租人**有效目录- Azure 的目录 AD 有关使用 Dynamics 365 用于工序服务器：https://login.windows.net/your-AD-tenant-ID&lt;&gt;。 例如：https://login.windows.net/contosooperations.onmicrosoft.com。 
**注释**:不要具有一结束"前进"字符此字段的反斜杠 (/)。 - ** **公司-输入 Dynamics 中 365 的法人您希望应用程序连接的操作。 [![wh![] (应用连接设置。应用/media/wh /media/wh)] 连接设置 169x300.png(。/media/wh /media/wh 应用 settings.png 连接)
4.  **选择恢复**按在应用程序的角落左上。 应用程序现在将与自己的操作服务器的 Dynamics 365，和仓库工人的登录画面将显示。 ![wh [] (![个日记帐在屏幕。/media/wh /media/wh 个日记帐在屏幕 180x300.png)](。{{/media/wh:/media/wh-13-log-in-screen.png}} /media/wh {{日志：/media/wh-13-log-in-screen.png}} {{在：/media/wh-13-log-in-screen.png}} {{screen.png:/media/wh-13-log-in-screen.png}})

## <a name="remove-access-for-a-device"></a>取消设备的访问
如遇丢失或一影响的设备的情况下，您必须首先取消对 Dynamics 365 的访问设备的操作。 以下步骤说明建议的流程删除访问权限。

1.  在工序的 Dynamics 365，为**系统管理** &gt; **设置** &gt; ** Azure Active Directory **的应用程序。
2.  设备删除对应于要删除访问权限的行。 用于中删除的{{在：down}}设备**的客户 ID **下的注释。
3.  Azure 登录的经典门户。<https://manage.windowsazure.com>。
4.  **菜单上单击左侧的 Active Directory **图标，然后单击所需的目录。
5.  在菜单中，单击顶部** **应用程序，然后单击要配置的应用程序。 **快速入门**页面将显示与单个登录和配置其他信息。
6.  **单击"配置"选项卡下移**，并确保**客户 ID **应用程序应相同取决于在{{在此：in}}一节中的第 2 步。
7.  **单击删除**栏按"订单。
8.  单击** **是在一条确认消息。



