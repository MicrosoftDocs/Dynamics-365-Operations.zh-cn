---
title: 嵌入第三方应用
description: 本主题说明如何嵌入第三方应用以扩展产品的功能。
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b0471fd2ea9a5e8b07b9e8bc279da53f6a1539ca
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345402"
---
# <a name="embed-third-party-apps"></a>嵌入第三方应用

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

很多客户使用各种应用程序来开展业务。 这些应用程序中有一些是与 Finance and Operations 应用结合使用的第三方 Web 应用。 要提供更无缝的用户体验，您可以使用 **整页应用** 功能将那些第三方应用直接嵌入到您的 Finance and Operations 应用中（前提是第三方应用允许被嵌入）。 这样，用户可以访问所需的网站和应用，而无需切换选项卡或窗口。

您必须先在“功能管理”中打开 **整页应用** 功能，然后才能够将第三方应用嵌入产品。 然后，您可以使用以下方法之一嵌入第三方应用或网站。 这些方法类似于将 Microsoft Power Apps 中的画布应用嵌入到 Finance and Operations 应用的方法。

- 将应用或网站作为新的选项卡（数据透视选项卡、快速选项卡、边栏选项卡或工作区部分）嵌入到现有页面。
- 从仪表板为应用或网站创建新的整页体验。

## <a name="embed-a-website-on-an-existing-page"></a>在现有页面上嵌入网站

如果要使用嵌入式应用补充系统中的现有页面，请使用此过程。

1. 打开要在其中嵌入应用的页面。
2. 打开 **添加应用** 窗格：

    1. 选择 **设置**，然后选择 **个性化** 打开 **个性化** 工具栏。
    2. 选择 **更多 \> 添加应用**。

3. 选择页面上要添加应用的区域。 此区域必须是数据透视选项卡、快速选项卡、边栏选项卡或工作区部分的 *选项卡容器*。
4. 选择 **网站**。
5. 配置嵌入的应用：

    - **名称** – 输入应为包含嵌入式应用的选项卡显示的文本。 通常，您会希望此文本成为应用的名称。
    - **URL** – 指定应用的位置。

    > [!IMPORTANT]
    > - 出于安全原因，URL 必须使用安全超文本传输协议 (HTTPS)。
    > - 必须将应用或网站配置为允许被嵌入。

6. 选择 **保存** 将应用嵌入页面。 应用将被添加为组中的最后一个选项卡或部分。
7. 确认应用按预期显示。 如果应用未呈现，请参阅本主题后面的[故障排除](#troubleshooting)一节。
8. 打开视图选择器，选择 **保存**（如果应用应与当前视图关联）或 **另存为**（将应用保存到其他视图）。

    如果页面没有视图选择器（例如，如果页面是对话框或工作区），可以跳过此步骤。

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>从仪表板将网站嵌入为整页体验

如果您要嵌入的应用与现有页面不相关，或者您只想在 Finance and Operations 应用中获得该应用的整页体验，请使用此过程。

1. 打开仪表板。
2. 选择并按住（或右键单击）此仪表反，选择 **个性化**，然后选择 **添加页面**。
3. 在 **添加页面** 窗格中，选择 **网站**。
4. 配置嵌入的应用：

    - **名称** – 在仪表板上输入为嵌入的应用添加的磁贴上应显示的文本。 通常，您会希望此文本成为应用的名称。
    - **URL** – 指定应用的位置。

    > [!IMPORTANT]
    > - 出于安全原因，URL 必须使用 HTTPS。
    > - 必须将应用或网站配置为允许被嵌入。

5. 选择 **保存** 将应用作为新磁贴添加到仪表板。
6. 选择仪表板上的新磁贴，确认应用按预期显示。 如果应用未呈现，请参阅本主题后面的[故障排除](#troubleshooting)一节。

## <a name="sharing-embedded-apps"></a>共享嵌入的应用

使用上一节中介绍的方法之一嵌入应用后，您可能希望与系统中的其他用户共享视图。 要共享嵌入的应用，请使用以下方法之一：

- **发布视图（推荐）：** 如果嵌入的应用已保存到视图，共享应用的推荐的首选方法是将视图发布给在目标法人中具有适当安全角色的用户。 在这种情况下，只有所需的用户才会在该页面上看到嵌入式应用。 有关如何发布视图的详细信息，请参阅[发布视图](saved-views.md#publishing-views)。

    您还可以从仪表板发布已嵌入为整页体验的应用。 在仪表板上，选择并按住（或右键单击）与应用关联的磁贴，选择 **个性化**，然后选择 **发布页面**。 系统显示了与 *发布视图* 体验相似的体验，您可以选择要发布到的安全角色。 在更新 10.0.21 或更高版本中，如果打开了 **改进了对已保存视图的法人支持** 功能，您还可以将应用发布到所需的法人。

- **复制个性化：** 对于不支持视图的页面（例如，对话框或工作区），或者对于整页应用体验，您可以将个性化设置复制给适当的用户。 有关详细信息，请参阅[共享个性化](personalize-user-experience.md#sharing-personalizations)。

## <a name="viewing-embedded-apps"></a>查看嵌入的应用

要在 Finance and Operations 应用中的页面上查看嵌入的应用，打开包含嵌入的应用的页面。 请记住，在有些页面上，可以使用标准操作窗格上的 **Power Apps** 按钮访问嵌入的应用。 或者，它们可以作为新选项卡、快速选项卡或边栏选项卡，或者工作区中的新部分直接显示在页面上。

## <a name="editing-or-removing-embedded-apps"></a>编辑或删除嵌入的应用

将应用嵌入页面后，您可能必须编辑其配置（例如，更改部分标签或 URL）。 或者，您可能必须将其从页面中删除。 使用以下过程之一来编辑嵌入的应用的配置或将其完全删除。

### <a name="apps-that-are-embedded-on-existing-pages"></a>嵌入到现有页面的应用

1. 打开嵌入了应用的页面。
2. 选择 **设置**，然后选择 **个性化** 打开 **个性化** 工具栏。
3. 选择 **选择** 工具，然后选择嵌入的应用。
4. 要编辑应用，对其配置进行所需的更改，然后选择 **保存**。

    或者，要删除应用，选择 **删除**。

5. 重新保存或重新发布视图。 请注意，如果您离开页面时未明确保存视图，将不会保留您在 **编辑网站** 窗格中执行的任何操作。

### <a name="apps-that-are-embedded-from-the-dashboard"></a>从仪表板嵌入的应用

1. 打开仪表板。
2. 选择并按住（或右键单击）与嵌入的应用关联的磁贴，然后选择 **个性化**。
3. 要编辑应用，选择 **编辑页面**。 在 **编辑网站** 窗格中，对应用配置进行所需的更改，然后选择 **保存**。

    或者，要删除应用，选择 **删除页面**。

## <a name="appendix"></a>附录

### <a name="troubleshooting"></a>疑难解答

如果将网站嵌入到 Finance and Operation 应用中后网站未正确呈现，或者如果您收到错误消息，指出 URL 被拒绝连接，说明该网站可能已配置为阻止被嵌入到 iframe 中。 请按照以下步骤确定网站是否可以嵌入。

1. 打开您使用的浏览器的开发人员工具。
2. 在 **网络** 选项卡上，从嵌入的站点中找到并选择响应。
3. 在 **标头** 选项卡上的 **响应标头** 下，查找 **x-frame-options**。 如果响应标头中存在 **x-frame-options**，并且其值为 **DENY** 或 **SAMEORIGIN**，网站当前无法嵌入。 您必须与应用的所有者合作来将它安全地嵌入。

### <a name="developer-modeling-a-website-on-a-form"></a>[开发人员] 在窗体上为网站建模

本主题的重点是通过个性化嵌入第三方应用或网站，但开发人员也可以使用 Visual Studio 开发体验将它们嵌入到窗体中。 只需将 **WebsiteHostControl** 控件添加到窗体中。 控件可用的元数据属性提供与个性化体验相同的功能。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
