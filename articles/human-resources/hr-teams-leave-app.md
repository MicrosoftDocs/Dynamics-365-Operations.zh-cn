---
title: 在 Teams 中管理请假
description: 此主题显示如何在 Microsoft Teams 中的 Dynamics 365 Human Resources 应用内请假。
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72fa3309b77717d0291b8b6828ed5bc4c65e95ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790564"
---
# <a name="manage-leave-requests-in-teams"></a>管理 Teams 中的休假申请

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

可通过 Microsoft Teams 中的 Dynamics 365 Human Resources 应用直接在 Microsoft Teams 中快速请假和查看自己的请假余额信息。 您可以与机器人交互来请求信息和开始请假请求。 **休假** 选项卡提供更详细信息。 您还可以在 Human Resources 应用之外在 Teams 和聊天中发送有关您的近期休假的人员信息。

## <a name="install-the-app"></a>安装应用

可以在 Teams 商店中找到 Dynamics 365 Human Resources 应用。

1. 在 Microsoft Teams 中，选择省略号。

   ![Human Resources Teams 休假应用省略号](./media/hr-teams-leave-app-ellipses.png)
 
2. 搜索 Dynamics 365 Human Resources，然后选择 **Human Resources** 磁贴。

   ![Human Resources Teams 休假应用 HR 磁贴](./media/hr-teams-leave-app-human-resources-tile.png)

3. 选择 **添加** 按钮安装应用。

   ![Human Resources Teams 休假应用安装](./media/hr-teams-leave-app-in-store.png)

如果应用不让您自动登录，请选择 **设置** 选项卡登录。

![Human Resources Teams 休假应用“设置”选项卡](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> 如果未看到登录对话框，请检查浏览器设置允许弹出窗口。 

如果可以访问多个 Human Resources 实例，可以在 **设置** 选项卡中选择要连接哪个环境。

> [!NOTE]
> 此应用现在支持系统管理员安全角色。
 
## <a name="use-the-bot"></a>使用机器人

安装应用后，将显示欢迎消息，告知您机器人可代表您执行的操作类型。

![Human Resources Teams 休假应用机器人欢迎消息](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> 首次与机器人交互时，可能需要登录。 如果未看到登录对话框，请检查浏览器设置允许弹出窗口。

可以让机器人：

- 为您启动休假请求。

  ![在 Teams 聊天中发起休假请求](./media/hr-teams-leave-app-initiate.png)

- 聊天机器人将为您填充休假请求。 选择 **请求休假**，然后编辑您的请求的详细信息。

  ![编辑休假请求详细信息](./media/hr-teams-leave-app-details.png)

- 完成休假请求详细信息的编辑后，选择 **提交** 提交请求进行审批。

  ![提交休假请求](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>在 Teams 中管理休假

**休假** 选项卡可用于查看： 

- 您等记的每个休假类型的余额信息

- 近期请假

- 休假请求

- 草稿请假

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>创建新请求

1. 若要创建新休假请求，请选择 **新请求**。

   ![Human Resources Teams 休假应用新请求](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. 输入请假天数，然后选择 **添加**。

   ![Human Resources Teams 休假应用添加休假](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. 如果适用，输入原因代码。 并且输入任何注释和添加任何附件。

4. 输入完信息后，键入 **提交** 提交请求供批准。 也可以键入 **另存为草稿** 以后再回来。

### <a name="manage-draft-requests"></a>管理草稿请求

1. 选择 **草稿** 选项卡。

   ![Human Resources Teams 休假应用“草稿”选项卡](./media/hr-teams-leave-app-drafts-tab.png)

2. 选择铅笔编辑请求，或选择废纸篓删除请求。

3. 进行任何必要更改。 输入完信息后，键入 **提交** 提交请求供批准。 也可以选择 **另存为草稿** 以后再回来。

   ![Human Resources Teams 休假应用编辑草稿](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>响应 Teams 通知

当您或作为审批者的您的下属工作人员提交请假时，您将在 Teams 中的 Human Resources 应用内收到通知。 您可以选择通知进行查看。 也会在 **聊天** 区域中显示通知。

如果您是审批者，您可以在通知中选择 **批准** 或 **拒绝**。 还可以提供可选消息。

![Human Resources Teams 中的请假通知](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>向您的同事发送近期休假信息

安装 Teams 的 Human Resources 应用后，您可以轻松地在团队或聊天中向同事发送您的近期休假的信息。

1. 在 Teams 中的团队或聊天中，选择聊天窗口下方的 Human Resources 按钮。

   ![聊天窗口下的 Human Resources 按钮](./media/hr-teams-leave-app-chat-button.png)

2. 选择您要共享的休假请求。 如果要共享休假请求草稿，请先选择 **草稿**。

   ![选择要共享的近期休假请求](./media/hr-teams-leave-app-chat-search.png)

您的休假请求将显示在聊天中。

![Human Resources 休假请求卡](./media/hr-teams-leave-app-chat-card.png)

如果您共享了请求草稿，它将显示为草稿：

![Human Resources 休假请求草稿卡](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>查看您的休假日历

如果您是具有直接下属的的经理，则可以查看团队的批准和待定请假。

1. 在 Teams 中的 Human Resources 应用内，选择 **请假**。

2. 选择 **Team 日历**。 日历显示直接下属的已批准和待定请假。

   ![在 Human Resources Teams 应用中查看日历](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > 如果您看不到团队日历，请让管理员启用它。 有关详细信息，请参阅[安装和设置](hr-admin-teams-leave-app.md#install-and-setup)。

## <a name="supported-languages"></a>支持的语言

Teams 中的 Dynamics 365 Human Resources 应用支持以下语言：

| 区域设置 ID | 语言 |
| --- | --- |
| de-DE | 德语(德国) |
| es-ES | 西班牙语(西班牙) |
| es-MX | 西班牙语(墨西哥) |
| fr-CA | 法语(加拿大) |
| fr-FR | 法语(法国) |
| it-IT | 意大利语(意大利) |
| nl-NL | 荷兰语(荷兰) |
| pt-BR | 葡萄牙语(巴西) |
| tr-TR | 土耳其语(土耳其) |
| zh-CN | 中文(简体) |

## <a name="troubleshooting"></a>疑难解答

如果您在登录或使用 Dynamics 365 Human Resources Teams 应用时遇到问题，请尝试按照以下疑难解答说明进行操作。 如果在进行疑难解答后仍有问题，请联系支持人员。 有关详细信息，请参阅[获取支持](hr-admin-troubleshooting-support.md)。

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>无法登录到 Teams 中的 Human Resources 应用

如果您无法登录该应用，则可能是您用来登录 Microsoft Teams 的帐户与 Dynamics 365 Human Resources 中的员工记录无关。 请与系统管理员联系，以确保您的员工记录已正确关联。

### <a name="translations-dont-display-correctly"></a>翻译未正确显示

如果翻译未按预期显示，请确保您在 Teams 中选择的语言与在 Human Resources **用户选项** 中选择的语言匹配。

在 Teams 中，查看 **设置** 中的 **应用语言**。

![Teams 设置](./media/hr-teams-leave-app-settings.png)

在 Human Resources 中，选择 **设置**，然后选择 **用户选项**。 验证 Teams 中的 **语言** 字段是否与 **应用语言** 字段匹配。

![Human Resources 用户选项](./media/hr-teams-leave-app-user-options.png)

如果您仍然遇到翻译问题，请告诉我们。 有关信息，请参阅[获取对 Finance and Operations 应用或 Lifecycle Services (LCS) 的支持](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json)。

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>在 Teams 中的 Human Resources 应用中审批请假请求时出错

如果您在尝试在 Teams 应用中审核休假请求时收到错误，请尝试以下疑难解答步骤：

1. 验证您用于登录 Microsoft Teams 的帐户是否与用于访问 Dynamics 365 Human Resources 的帐户相同。

2. 通过检查请假审批的工作流设置，验证您是否是该请求的有效审批者。 有关请假请求工作流的详细信息，请参阅[创建请假请求工作流](hr-leave-and-absence-workflow.md)。

## <a name="known-accessibility-issues"></a>已知的可访问性问题

Teams 中的 Human Resources 应用具有以下可访问性问题，我们正在努力在将来的版本中修复这些问题。

| 签发 | 解决方法或说明 |
| --- | --- |
| 在桌面上放大到 400％ 时，将看不见某些操作按钮。 | 建议您改用放大镜，直到我们可以支持此缩放级别为止。 |
| 在 **休假** 选项卡上，在读出休假网格的标题时，VoiceOver 将宣布一个按钮操作。 | 网格中的标题和元素按年份分组，并且可以折叠。 VoiceOver 将此解释为可操作的项目，但并非如此。 |
| 在 **休假** 选项卡上，当在新请求中导航到 **原因代码** 时，有一个额外的轻扫手势。 | 没有轻扫导航要尝试获取的隐藏控件。 |
| 在 **休假** 选项卡上，如果您在打开日历时进行轻扫，您最终位于控件之外，而不是在新请求中或编辑请求时位于顶部。 | 当您到达 **立即前往** 时，将其视为控件的结束，然后以相反方向轻扫以返回到顶部。 |
| 在 **聊天** 选项卡上，在使用辅助工具或键盘导航的同时输入日期时，焦点会跳回到顶部。 | 按 Tab 键，直到再次到达输入区域。 |

## <a name="privacy-notice"></a>隐私声明

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft 语言理解智能服务 (LUIS)

Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。 “搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。 请在 [此处](https://www.luis.ai/)详细了解 LUIS。 LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。 然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。 

安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。 与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。 由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。 

用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。 请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。 

若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB

使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。

Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。 此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。 要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。

与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。 此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。 要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)。
 
要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。

## <a name="see-also"></a>请参阅

[下载和安装 Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams 帮助中心](https://support.office.com/teams)</br>
[Teams 中的 Human Resources 应用](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]