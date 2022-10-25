---
title: Customer Service 全渠道商业聊天模块
description: 本文介绍了 Microsoft Dynamics 365 Commerce 中的 Customer Service 全渠道商业聊天模块。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: 99e8b9d66a04390ab70fd1deff9f95fe28bdfae3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690308"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Customer Service 全渠道商业聊天模块

[!include [banner](includes/banner.md)]

本文介绍了 Microsoft Dynamics 365 Commerce 中的 *Customer Service 全渠道商业聊天* 模块。

在 Commerce 版本 10.0.29 中，一个新的 Customer Service 全渠道商业聊天模块已添加到 Commerce 模块库中。 商业聊天功能为电子商务客户提供 Dynamics 365 Customer Service 全渠道的聊天功能，包括人工代理支持，帮助解决客户查询、提供客户服务以及促进对 Commerce 客户的销售。

商业聊天功能使零售商能够实现以下目标：

- 增加与客户的个性化互动，以帮助提高客户保留率。
- 通过集成人工代理和自助聊天机器人来改善客户服务。
- 帮助代理通过实时客户资料、订单和购买数据获得经验，从而推动运营改进和参与度。
- 提高整体客户满意度，以帮助增加销售额。

以下功能作为商业聊天功能的一部分提供：

- Customer Service 全渠道商业聊天
- 在 Dynamics 365 Customer Service 全渠道的代理体验中添加了 **Commerce 呼叫中心** 作为应用程序选项卡

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Customer Service 全渠道的先决条件

作为先决条件，您必须在 Customer Service 全渠道管理小组件中配置聊天并获取一些参数来配置 Commerce 聊天体验。 有关说明，请参阅[配置聊天渠道](/dynamics365/customer-service/set-up-chat-widget)。

在 Customer Service 全渠道管理小组件中配置聊天后，您将获得类似于以下示例的脚本。

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

复制此脚本，因为您需要其中的值来配置聊天模块。

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Customer Service 全渠道商业聊天必需字段

下表显示了来自 Customer Service 全渠道管理小组件的脚本值，这些值是配置 Customer Service 全渠道商业聊天模块所必需的。

| 小组件属性 | Description |
| ------------- |--------------|
| 脚本源 | 聊天小组件脚本中的 **src** 值。 |
| 数据应用程序 ID | 聊天小组件脚本中的 **data-app-id** 值。 |
| 数据组织 ID | 聊天小组件脚本中的 **data-org-id** 值。 |
| 数据组织 URL | 聊天小组件脚本中的 **data-org-url** 值。 |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>为您的电子商务站点配置商业聊天体验

为您的电子商务站点实现聊天体验的一种推荐方法是将 Customer Service 全渠道商业聊天模块添加到您的电子商务站点页面上使用的共享页眉片段中。

要在 Commerce 站点构建器中将聊天模块添加到站点的页眉片段，请执行以下步骤。

1. 在您站点的站点构建器中，转到 **片段**。
1. 选择 **新建**。
1. 在 **选择片段** 对话框中，选择 **Customer Service 全渠道商业聊天** 模块，为片段输入名称，然后选择 **确定**。
1. 在轮廓视图中，选择 **Msdyn365 cs 聊天连接器** 插槽。
1. 在右侧的 **聊天属性** 窗格中，执行以下步骤：

    1. 在 **脚本源** 字段中，输入您从 Customer Service 全渠道脚本获取的 **src** 值。
    1. 在 **数据应用程序 ID** 字段中，输入您从 Customer Service 全渠道脚本获取的 **data-app-id** 值。
    1. 在 **数据组织 ID** 字段中，输入您从 Customer Service 全渠道脚本获取的 **data-org-id** 值。
    1. 在 **数据组织 URL** 字段中，输入您从 Customer Service 全渠道脚本获取的 **data-org-url** 值。

    ![在 Commerce 站点构建器中创建商业聊天模块片段。](media/Commerce-chat-creating-new-fragment.png)

1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。
1. 转到 **片段**，打开您的站点的页眉片段。
1. 在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择模块** 对话框中，选择您之前创建的聊天片段，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。

> [!NOTE]
> 要获取配置参数的完整列表，请参阅[商业聊天模块主动聊天参数](chat-proactive-chat-parameters.md)。

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>将 Commerce headquarters 添加为 Customer Service 全渠道的应用程序选项卡

您可以在 Customer Service 全渠道中为 Commerce headquarters 添加应用程序选项卡。 然后，人工代理可以使用 Customer Service 全渠道代理体验的用户界面，轻松访问 Dynamics 365 Commerce 客户服务模块，该模块包含客户的上下文信息及其销售订单信息。 此外，客户服务代理可以下新订单、发起退货和验证订单状态信息。

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>创建一个新的应用程序选项卡，在 iFrame 模块中加载 Commerce headquarters 

要创建一个在 iFrame 模块中加载 Commerce headquarters 的新应用程序选项卡，请执行以下步骤。

1. 打开 [Power Apps Maker portal](https://make.powerapps.com)。
1. 在左侧的导航窗格中，选择 **应用**。
1. 选择 **Customer Service 管理中心**。
1. 转到 **代理体验**。
1. 对于 **应用程序选项卡模板**，选择 **管理**。
1. 新建一个 **第三方网站** 类型的应用程序选项卡。 有关说明，请参阅[管理应用程序选项卡模板](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter)。
1. 在 **参数** 下，在 **url** 参数的 **值** 字段中，输入以下 URL，其中 `<YourOrganizationHeadquartersURL>` 和 `<LegalEntityname>` 将替换为适当的值。 全渠道客户服务将从聊天上下文中读取 **{AccountNumber}**。 因此，保留 **{AccountNumber}** 不变。

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. 将 **数据** 参数的 **值** 字段留空。

![在 Dynamics 365 全渠道客户服务中创建应用程序选项卡。](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>在 Dynamics 365 Customer Service 全渠道中为客户代理启用新的应用程序选项卡

要在 Dynamics 365 Customer Service 全渠道中为客户代理启用新的应用程序选项卡，请按照下列步骤操作。
    
1. 打开 [Power Apps Maker portal](https://make.powerapps.com)。
1. 在左侧的导航窗格中，选择 **应用**。
1. 选择 **Customer Service 管理中心**。
1. 转到 **客户支持 \> 工作流**。
1. 打开您为代理创建的工作流，然后在 **高级设置** 下选择 **默认会话**。
1. 在 **应用程序选项卡** 下，选择 **添加现有应用程序选项卡**，然后添加您之前创建的新应用程序选项卡。 此步骤可确保当代理收到来自您的电子商务网站的传入聊天呼叫时，将出现一个在 iFrame 模块中加载 Commerce headquarters 的应用程序选项卡。

> [!NOTE]
> 您无法修改工作流中的默认聊天会话模板。 因此，您可能需要创建新模板或复制现有模板来进行更新。 有关详细信息，请参阅[将模板与工作流关联](/dynamics365/app-profile-manager/associate-templates)。

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>在 Dynamics 365 Customer Service 全渠道中添加上下文变量

要在 Dynamics 365 Customer Service 全渠道中添加上下文变量，请按照下列步骤操作。

1. 打开 [Power Apps Maker portal](https://make.powerapps.com)。
1. 在左侧的导航窗格中，选择 **应用**。
1. 选择 **Customer Service 管理中心**。
1. 转到 **客户支持 \> 工作流**。
1. 打开您为代理创建的工作流，然后在 **高级设置** 下，转到 **上下文变量** 部分。
1. 选择 **编辑**，然后添加 **AccountNumber** 作为 **文本** 类型的上下文变量。 此变量将帮助 Commerce headquarters 加载具有匹配帐号的客户信息。

> [!NOTE]
> 如果您想要从电子商务渠道读取登录用户的电子邮件地址和姓名，您可以添加 **电子邮件** 和 **姓名** 作为 **文本** 类型的上下文变量，并添加 **AccountNumber** 上下文变量。

## <a name="additional-resources"></a>其他资源

[商业聊天功能概述](commerce-chat-overview.md)

[Power Virtual Agents 商业聊天模块](chat-module-pva.md)

[商业聊天模块主动聊天参数](chat-proactive-chat-parameters.md)
