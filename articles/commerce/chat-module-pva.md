---
title: Power Virtual Agents 商业聊天模块
description: 本文介绍了将 Microsoft Power Virtual Agents 与 Dynamics 365 Commerce 网站集成在一起的 Power Virtual Agents 商业聊天模块。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691050"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Power Virtual Agents 商业聊天模块

[!include [banner](includes/banner.md)]

本文介绍了将 Microsoft Power Virtual Agents 与 Dynamics 365 Commerce 网站集成在一起的 Power Virtual Agents 商业聊天模块。

Power Virtual Agents 商业聊天功能使 Dynamics 365 电子商务客户能够使用 Power Virtual Agents 聊天机器人功能来处理他们的查询。 从 Dynamics 365 Commerce 10.0.30 版本开始，此功能可以通过使用属于 Commerce 模块库一部分的 Power Virtual Agents 商业聊天模块并入电子商务网站。

Power Virtual Agents 商业聊天功能帮助企业实现以下目标：

- 增加与消费者的个性化互动，提高保留率。
- 通过集成自助聊天机器人增加客户服务。
- 提高整体客户满意度，从而增加销售额。

> [!NOTE]
> 要了解 Dynamics 365 Customer Service 全渠道与 Power Virtual Agents 应用程序之间的差异，请参阅[商业聊天模块概述](/commerce-chat-modules-overview.md)。

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>使用 Power Virtual Agents 的先决条件

要使用 Power Virtual Agents 商业聊天功能，您必须首先为您的电子商务网站创建一个 Power Virtual Agents 聊天机器人。 有关说明，请参阅[创建强大的虚拟代理机器人](/power-virtual-agents/authoring-first-bot)。

配置聊天机器人后，必须复制 **Bot ID** 和 **Tenant ID** 聊天机器人参数的值来配置商业聊天体验。 有关如何复制这些值的信息，请参阅[检索 Power Virtual Agents 机器人参数](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters)。

## <a name="configure-your-e-commerce-site"></a>配置电子商务站点 

为您的电子商务站点实现聊天体验的一种推荐方法是将 Power Virtual Agents 商业聊天模块添加到您的站点页面上使用的共享页眉片段中。

要在 Commerce 站点构建器中将聊天模块添加到站点的页眉片段，请执行以下步骤。

1. 在您站点的 Commerce 站点构建器中，转到 **片段**。
1. 选择 **新建**。
1. 在 **选择片段** 对话框中，选择 **Power Virtual Agents 商业聊天** 模块，为片段输入名称，然后选择 **确定**。
1. 在轮廓视图中，选择 **Msdyn365 pva 聊天连接器** 插槽。
1. 在右侧的属性窗格中，执行以下步骤：

    1. 在 **机器人参数** 下，在 **Bot Framework 网络聊天聊天 CDN URL** 字段中，保留默认值（例如，`https://cdn.botframework.com/botframework-webchat/latest/webchat.js`）。
    1. 在 **Bot Framework Direct Line 身份验证 URL** 字段，保留默认值（例如，`https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`）。
    1. 在 **机器人 ID** 字段中，输入您在 [使用 Power Virtual Agents 的先决条件](#prereq)一节中复制的 Power Virtual Agents **机器人 ID** 值。
    1. 在 **租户 ID** 字段中，输入您复制的 **租户 ID** 值。

1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。
1. 转到 **片段**，打开您的站点的页眉片段。
1. 在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择模块** 对话框中，选择您之前创建的聊天片段，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。

## <a name="proactive-chat-parameters"></a>主动聊天参数

要获取主动聊天配置参数的完整列表，请参阅[商业聊天模块主动聊天参数](chat-proactive-chat-parameters.md)。

> [!NOTE]
> 目前，Power Virtual Agents 不支持 Azure Active Directory B2C (Azure AD B2C) 身份验证。 它只支持使用匿名 Retail Cloud Scale Unit (RCSU) 调用来获取产品可用性或与其他匿名 API 交互。 通过 Power Virtual Agents 聊天机器人调用经过身份验证的 API 需要客户明确登录。

## <a name="additional-resources"></a>其他资源

[商业聊天功能概述](commerce-chat-overview.md)

[Customer Service 全渠道商业聊天模块](commerce-chat-module.md)

[商业聊天模块主动聊天参数](chat-proactive-chat-parameters.md)
