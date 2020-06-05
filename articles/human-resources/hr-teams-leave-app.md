---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393000"
---
# <a name="manage-leave-requests-in-teams"></a>在 Teams 中管理请假

[!include [banner](includes/preview-feature.md)]

可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。 可以与机器人交互以请求信息。 **休假**选项卡提供更详细信息。

## <a name="install-the-app"></a>安装应用

可以在 Teams 商店中找到 Human Resources 应用。

1. 在 Microsoft Teams 中，选择省略号。

   ![Human Resources Teams 休假应用省略号](./media/hr-teams-leave-app-ellipses.png)
 
2. 搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。

   ![Human Resources Teams 休假应用 HR 磁贴](./media/hr-teams-leave-app-human-resources-tile.png)

3. 选择**添加**按钮安装应用。

   ![Human Resources Teams 休假应用安装](./media/hr-teams-leave-app-in-store.png)

如果应用不让您自动登录，请选择**设置**选项卡登录。

![Human Resources Teams 休假应用“设置”选项卡](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> 如果未看到登录对话框，请检查浏览器设置允许弹出窗口。 

如果可以访问多个 Human Resources 实例，可以在**设置**选项卡中选择要连接哪个环境。

> [!WARNING]
> 此应用现在支持系统管理员安全角色，并且在您使用系统管理员帐户时显示错误消息。 若要使用其他帐户登录，请在**设置**选项卡上选择**切换帐户**按钮，然后使用无系统管理员权限的用户帐户登录。
 
## <a name="use-the-bot"></a>使用机器人

安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。

![Human Resources Teams 休假应用机器人欢迎消息](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> 首次与机器人交互时，可能需要登录。 如果未看到登录对话框，请检查浏览器设置允许弹出窗口。

可以让机器人：

- 显示您等记的每个休假类型的休假余额信息。

   ![Human Resources Teams 休假应用显示余额](./media/hr-teams-leave-app-bot-balances.png)
 
- 显示有关特定休假类型的其他详细信息。

   ![Human Resources Teams 休假应用显示详细信息](./media/hr-teams-leave-app-bot-details.png)

- 为您启动休假请求。

   ![Human Resources Teams 休假应用请假](./media/hr-teams-leave-app-bot-request.png)
 
启动请假后，可以直接在卡中调整天数，也可以选择**编辑详细信息**向请求添加更多信息。

![Human Resources Teams 休假应用编辑请求](./media/hr-teams-leave-app-bot-edit.png)
 
输入完信息后，键入**提交**提交请求供批准。 也可以键入**另存为草稿**以后再回来。

![Human Resources Teams 休假应用提交请求](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>在 Teams 中管理休假

**休假**选项卡可用于查看：

- 您等记的每个休假类型的余额信息

- 近期请假

- 休假请求

- 草稿请假

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>创建新请求

1. 若要创建新休假请求，请选择**新请求**。

   ![Human Resources Teams 休假应用新请求](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. 输入请假天数，然后选择**添加**。

   ![Human Resources Teams 休假应用添加休假](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. 如果适用，输入原因代码。 并且输入任何注释和添加任何附件。

4. 输入完信息后，键入**提交**提交请求供批准。 也可以键入**另存为草稿**以后再回来。

### <a name="manage-draft-requests"></a>管理草稿请求

1. 选择**草稿**选项卡。

   ![Human Resources Teams 休假应用“草稿”选项卡](./media/hr-teams-leave-app-drafts-tab.png)

2. 选择铅笔编辑请求，或选择废纸篓删除请求。

3. 进行任何必要更改。 输入完信息后，键入**提交**提交请求供批准。 也可以选择**另存为草稿**以后再回来。

   ![Human Resources Teams 休假应用编辑草稿](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>隐私声明

Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。 “搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。 请在 [此处](https://www.luis.ai/)详细了解 LUIS。 LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。 然后将此信息继续传递到 Microsoft 的  [Azure 机器人框架](https://azure.microsoft.com/services/bot-service/) 后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。 

安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。 与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。 由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。 

用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。 请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。 

若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。 

## <a name="see-also"></a>请参阅

[下载和安装 Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams 帮助中心](https://support.office.com/teams)</br>
[Teams 中的 Human Resources 应用](hr-admin-teams-leave-app.md)
