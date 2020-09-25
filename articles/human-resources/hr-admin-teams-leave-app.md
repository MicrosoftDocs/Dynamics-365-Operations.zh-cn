---
title: Teams 中的 Human Resources 应用
description: 此主题介绍 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用。
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776300"
---
# <a name="human-resources-app-in-teams"></a>Teams 中的 Human Resources 应用

[!include [banner](includes/preview-feature.md)]

员工可通过 Microsoft Teams 中的 Microsoft Dynamics 365 Human Resources 应用在 Microsoft Teams 中快速请假和查看自己的请假余额信息。 员工可以与机器人交互以请求信息。 **休假**选项卡提供更详细信息。

![Human Resources Teams 休假应用机器人](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams 休假应用“休假”选项卡](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>安装和设置

可以在 Teams 商店中找到 Human Resources 应用。 有关安装 Teams 应用的信息，请参阅[在 Teams 中管理请假](hr-teams-leave-app.md)。

有关在 Teams 中管理应用权限的信息，请参阅[在 Microsoft Teams 中管理应用权限策略](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)。

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>在 Teams 中启用 Human Resources 应用通知

如果希望用户在 Teams 应用中接收请假通知，必须在 Human Resources 中启用通知。

>[!NOTE]
>只有已登录 Teams 且使用 Human Resources Teams 应用的用户才会收到通知。

1. 在 Human Resources 中，选择**系统管理**。

2. 选择**链接**。

3. 在**设置**下，选择**系统参数**。

4. 在**常规**选项卡中，将**启用 Teams 应用通知**设置为**是**。

   ![在系统参数中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. 若要为所有用户打开 Teams 通知，请在提示符处选择**是**。

   ![为所有用户启用 Teams 通知](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>为单个用户打开或关闭 Teams 通知

启用 Human Resources Teams 应用通知最后，可以为单个用户打开或关闭通知。

1. 在 Human Resources 中，选择**系统管理**。

2. 选择**链接**。

3. 在**用户**下，选择**用户选项**。

4. 选择**工作流**选项卡。

5. 将**启用 Teams 应用通知**设置为**是**为用户启用通知，或设置为**否**为用户禁用通知。

   ![在“用户选项工作流”选项卡中启用 Teams 应用通知](./media/hr-admin-teams-leave-app-notifications.png)

6. 选择**保存**。

## <a name="known-issues"></a>已知问题

| 签发 | 状态 |
| --- | --- |
| 水平滚动不适用于 Android 手机 | 水平滚动在 iOS 或台式机设备上不是问题。 我们正在解决 Android 上的问题。 |
| 错误：查找要连接的环境时出现问题。 | 即使您已确认用户可以访问一个或多个 Human Resources 环境，也可能会收到此错误。 此外，您可能看不到您预期的所有环境。 在我们修复此问题之前，请删除用户，然后再次将其导入以解决此问题。 |
| 提交将来日期的请假时，余额不正确。 | 预测尚不可用。 显示当前日期的余额。 |
| 不能取消**审查中**请求。 | 现在不支持此功能，将来的版本中将增加此功能。 |
| 将计算截止当天的余额信息。 | 系统现在不显示截止实际期间的余额，即使已在“休假和缺勤”参数中配置。 |

## <a name="privacy-notice"></a>隐私声明

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft 语言理解智能服务 (LUIS)

Microsoft Teams 中的 Dynamics 365 Human Resources 机器人用于分析用户的文本输入以了解底层的查询/意图。 “搜索帐户 Contoso”之类用户输入将传递到一个名称为语言理解智能服务 (LUIS) 的 Microsoft Cognitive Service。 请在 [此处](https://www.luis.ai/)详细了解 LUIS。 LUIS 服务用于厘清或了解用户输入的意图（此示例中的意图为查找信息）和目标实体（此示例中的意向实体为帐户 Contoso）。 然后将此信息继续传递到 Microsoft 的  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/)，后者与来自 Dynamics 365 Human Resources 的数据交互和检索用户查询所需信息。 

安装并允许访问使用机器人即表示您同意允许 LUIS 服务和 Azure 机器人框架处理输入背后的意图，从而增强对话用户体验。 与 Dynamics 365 Human Resources 相比，LUIS 服务和 Azure 机器人框架的合规性级别可能很多。 由于 LUIS 服务只能访问用户查询，不应连接到用户的 Dynamics 365 Human Resources 数据或帐户，所以 Dynamics 365 Human Resources 机器人的用户可以自愿输入其中包含客户数据、个人数据或其他数据的查询，并且可能将此类查询意图发送给 LUIS 服务和 Azure 机器人框架。 

用户的查询和消息的意图在 LUIS 系统中最多保留 30 天，静态加密，且不用于改进训练或服务。 请在 [此处](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)详细了解 Cognitive Services。 

若要管理 Microsoft Teams 中的应用的管理员设置，请转到 [Microsoft Teams 管理中心](https://admin.teams.microsoft.com/)。

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure 事件网格和 Microsoft Teams

使用 Teams 中的 Dynamics 365 Human Resources 应用的通知功能时，某些客户数据会流到租户的 Human Resources 服务的部署地理区域之外。 Dynamics 365 Human Resources 将员工的请假和工作流程任务详细信息传输到 Microsoft Azure 事件网格和 Microsoft Teams。 此数据可以存储最多 24 小时和在美国处理，在传输期间和静态时加密，并且不由 Microsoft 或其附属机构用于训练或服务改进。

## <a name="see-also"></a>请参阅 

[下载和安装 Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams 帮助中心](https://support.office.com/teams)</br>
[管理 Teams 中的休假申请](hr-teams-leave-app.md)

