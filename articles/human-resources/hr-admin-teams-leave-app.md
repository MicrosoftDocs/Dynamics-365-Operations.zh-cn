---
title: Teams 中的 Human Resources 应用
description: 此主题介绍 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用。
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9cc15c33c7efdd515121db67331477baa4bdacaf
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953380"
---
# <a name="human-resources-app-in-teams"></a>Teams 中的 Human Resources 应用

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

员工可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用在 Microsoft Teams 中快速请假和查看自己的请假余额信息。 员工可以与机器人交互以请求信息。 **休假** 选项卡提供更详细信息。 此外，他们可以在 Human Resources 应用之外在团队和聊天中发送有关近期休假的人员信息。

![Human Resources Teams 休假应用机器人](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources 休假请求卡](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>安装和设置

可以在 Teams 商店中找到 Dynamics 365 Human Resources 应用。 有关安装 Teams 应用的信息，请参阅[在 Teams 中管理请假](hr-teams-leave-app.md)。

有关在 Teams 中管理应用权限的信息，请参阅[在 Microsoft Teams 中管理应用权限策略](/MicrosoftTeams/teams-app-permission-policies)。

如果要让用户在应用中查看休假和缺勤日历，您需要在“功能管理”中启用 **Teams 中的休假和缺勤日历**。 有关启用功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>在 Teams 中启用 Human Resources 应用通知

如果希望用户在 Teams 应用中接收请假通知，必须在 Dynamics 365 Human Resources 中启用通知。

>[!NOTE]
>只有已登录 Teams 且使用 Dynamics 365 Human Resources Teams 应用的用户才会收到通知。

1. 在 Human Resources 中，选择 **系统管理**。

2. 选择 **链接**。

3. 在 **设置** 下，选择 **系统参数**。

4. 在 **常规** 选项卡中，将 **启用 Teams 应用通知** 设置为 **是**。

   ![在系统参数中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. 若要为所有用户打开 Teams 通知，请在提示符处选择 **是**。

   ![为所有用户启用 Teams 通知](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>为单个用户打开或关闭 Teams 通知

启用 Dynamics 365 Human Resources Teams 应用通知最后，可以为单个用户打开或关闭通知。

1. 在 Human Resources 中，选择 **系统管理**。

2. 选择 **链接**。

3. 在 **用户** 下，选择 **用户选项**。

4. 选择 **工作流** 选项卡。

5. 将 **启用 Teams 应用通知** 设置为 **是** 为用户启用通知，或设置为 **否** 为用户禁用通知。

   ![在“用户选项工作流”选项卡中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-notifications.png)

6. 选择 **保存**。

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

## <a name="notes"></a>说明

以下工作项计划用于将来版本：

| 工作项 | 状态 |
| --- | --- |
| 提交将来日期的请假时，余额不正确。 | 预测尚不可用。 显示当前日期的余额。 |
| 不能取消 **审查中** 请求。 | 现在不支持此功能，将来的版本中将增加此功能。 |
| 将计算截止当天的余额信息。 | 系统现在不显示截止实际期间的余额，即使已在“休假和缺勤”参数中配置。 |

## <a name="troubleshooting"></a>疑难解答

如果用户在登录或使用 Human Resources Teams 应用时遇到问题，请尝试按照以下疑难解答说明进行操作。 如果在进行疑难解答后仍有问题，请联系支持人员。 有关详细信息，请参阅[获取支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>无法登录到 Teams 中的 Human Resources 应用

如果用户由于无法登录应用而与您联系，请确认他们在 Human Resources 中具有关联的员工记录。

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>在 Teams 中的 Human Resources 应用中审批请假请求时出错

如果用户在尝试批准 Teams 应用中的请假请求时收到错误，请尝试以下疑难解答步骤：

1. 验证其 Teams 帐户与用于访问 Human Resources 的帐户相同。

2. 通过检查请假审批的工作流设置，验证他们是否是该请求的有效审批者。 有关请假请求工作流的详细信息，请参阅[创建请假请求工作流](hr-leave-and-absence-workflow.md)。

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>休假审批者收不到审批休假申请的 Teams 聊天消息

1. 请确保为环境和用户启用了通知。 有关详细信息，请参阅[在 Teams 中启用 Human Resources 应用通知](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)和[为单个用户打开或关闭 Teams 通知](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)。

2. 确保用户使用与用于审批休假申请相同的凭据登录到 **聊天** 选项卡。 使用消息“注销”，然后使用“登录”以正确的凭据登录。

3. 如果问题仍然存在，请以系统管理员身份检查业务事件系统批处理作业的状态。 如果是处于等待或执行阶段，请过几分钟再次检查。 如果状态保持不变，请记录支持票证，以便我们的团队可以帮助解决问题。

## <a name="privacy-notice"></a>隐私声明

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft 语言理解智能服务 (LUIS)

Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。 “搜索帐户 Contoso”之类的用户输入将传递到一个名为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。 请在 [此处](https://www.luis.ai/)详细了解 LUIS。 LUIS 服务用于理清或了解用户输入的意图（在此示例中，意图为查找信息）和目标实体（在此示例中，意图实体为帐户 Contoso）。 然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。

安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。 与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。 由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。 

用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。 请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。 

若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams、Azure Event Grid 和 Azure Cosmos DB

使用 Microsoft Teams 中的 Dynamics 365 Human Resources 应用时，某些客户数据可能会流到租户的 Human Resources 服务的部署地理区域之外。

Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。 此数据可以在 Microsoft Azure 事件网格中最多存储 24 小时，将在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。 要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。

与 Human Resources 应用中的聊天机器人进行对话时，对话内容可以存储在 Azure Cosmos DB 中并传输到 Microsoft Teams。 此数据最多可以在 Azure Cosmos DB 中存储 24 小时，可以在您的租户的 Human Resources 服务所部署的地理区域之外进行处理，在传输过程中和静态时进行加密，不会被 Microsoft 或其子处理器用于培训或服务改进。 要了解您的数据在 Teams 中的存储位置，请参阅：[Microsoft Teams 数据的位置](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)。
 
要对您的组织或组织内的用户限制对 Microsoft Teams 中的 Human Resources 应用的访问，请参阅[在 Microsoft Teams 中管理应用权限策略](/MicrosoftTeams/teams-app-permission-policies)。

## <a name="see-also"></a>请参阅 

[下载和安装 Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams 帮助中心](https://support.office.com/teams)</br>
[管理 Teams 中的休假申请](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]