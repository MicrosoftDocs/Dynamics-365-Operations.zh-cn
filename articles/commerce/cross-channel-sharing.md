---
title: 启用和使用跨渠道共享
description: 本文介绍了如何启用和使用 Microsoft Dynamics 365 Commerce 站点构建器的跨渠道共享功能。
author: josaw1
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: c05da17327e61d6f61883ab97a403bf2cf8a68f1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270065"
---
# <a name="enable-and-use-cross-channel-sharing"></a>启用和使用跨渠道共享

[!include [banner](includes/banner.md)]

本文介绍了如何启用和使用 Microsoft Dynamics 365 Commerce 站点构建器的跨渠道共享功能。

通过跨渠道共享，零售商可以在站点的多个渠道中重复使用和共享内容。 当站点渠道具有兼容的基本语言时，或者当它们具有多个共同的内容项时，此功能很有用。

跨渠道共享的工作原理是在找不到所请求内容的渠道特定版本时，启用将搜索可用内容的默认渠道。 打算在渠道之间共享的内容将在默认渠道中创建。 可以针对任何站点渠道上使用的任何区域设置对该内容进行本地化。

## <a name="when-to-use-cross-channel-sharing"></a>何时使用跨渠道共享

当单个站点上的多个渠道可以共享内容时，跨渠道共享非常有用。 例如，具有在一个站点下分组的多个品牌和店面的零售商可以在一些或所有店面之间共享某些内容。 此共享的内容可以包括有关条款和条件、付款期、运输方式和常见问题 (FAQ) 的页面。

跨渠道共享也支持片段。 因此，可以将包含渠道特定片段的内容页面创建为跨渠道内容。 在这种情况下，尽管大多数内容将在渠道之间共享，但是仅当从相应的店面渠道请求它们时，才会呈现跨渠道页面上的渠道特定片段。

只有一个渠道的站点或具有多个无法共享内容的渠道的站点将无法从跨渠道共享中受益。

## <a name="enable-cross-channel-sharing"></a>启用跨渠道共享

在站点级别上启用跨渠道共享。 此操作是单向的。 换句话说，启用跨渠道共享后，便无法将其禁用。

若要在 Commerce 站点构建器中启用跨渠道共享，请按照下列步骤操作。

1. 转到 **站点设置 \> 功能**。
1. 将 **跨渠道** 功能的选项设置为 **开**。

    ![在 Commerce 站点构建器中，将“跨渠道”选项设置为“开”。](./media/enabling-cross-channel-sharing.png)

启用跨渠道共享后，跨渠道信息将显示在 **站点设置 \> 功能** 的 **渠道** 部分中，如下图示例所示。

![渠道信息在启用跨渠道共享后可见。](./media/channels-cross-channel.png)

此外，启用跨渠道共享后，Commerce 站点构建器右上角的 **渠道** 字段将包含一个 **跨渠道在线商店** 选项，可用于管理跨渠道内容，如下图所示。

![启用跨渠道共享后，“渠道”字段中的“跨渠道在线商店”选项。](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>创建和使用跨渠道内容

您可以通过多种方式创建和使用跨渠道内容。 例如，您可以创建跨渠道片段，创建使用跨渠道和渠道特定内容的跨渠道页面，并使用渠道特定版本的片段替代跨渠道片段。

### <a name="create-a-cross-channel-fragment"></a>创建跨渠道片段

若要在 Commerce 站点构建器中创建跨渠道片段，请按照下列步骤操作。

1. 转到 **片段**，选择 **新建** 创建新片段。
1. 在 **新建片段** 对话框中，选择 **促销横幅** 模块，然后在 **片段名称** 下，输入名称（例如，**跨渠道横幅**）。 然后选择 **确定**。
1. 在 **促销横幅** 模块的属性窗格中，选择 **添加消息**，然后选择 **消息**。
1. 在 **消息** 对话框中，在 **文本** 下，输入 **跨渠道**，然后选择 **确定**。 
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

此跨渠道片段可用于在任何站点渠道上创建的跨渠道页面或渠道特定页面。

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>创建使用跨渠道内容的跨渠道页面

跨渠道页面可用于您的站点的任何渠道。 因此，您可以一次创建一个共享内容页面，并在单个位置进行任何后续更新。 例如，具有 URL `/toc` 的跨渠道 **条款和条件** 页面可以在站点的所有渠道之间共享。 如果站点渠道的基本 URL 是 `www.fabrikam.com/brand1` 和 `www.fabrikam.com/brand2`，相同的跨渠道共享的 **条款和条件** 页面将分别在 `www.fabrikam.com/brand1/toc` 和 `www.fabrikam.com/brand2/toc` 的站点渠道 URL 上提供。 如果 **条款和条件** 页面必须稍后更新，您只需更新单个共享页面。

若要在 Commerce 站点构建器中创建使用跨渠道内容的跨渠道页面，请按照下列步骤操作。

1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择一个模板，例如 **市场营销**。
1. 在 **页面名称** 下，输入页面名称（例如，**跨渠道页面**）。
1. 在 **页面 URL** 下，输入页面 URL（例如，**examplepage**），然后选择 **确定**。
1. 在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **添加片段** 对话框中，选择您先前创建的具有促销横幅的跨渠道片段，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 您应该看到显示“跨渠道”的促销横幅。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>创建使用跨渠道内容的渠道特定页面

通过在渠道特定页面上使用跨渠道内容，您可以一次创建一个共享内容片段，然后在渠道特定页面上使用它。 此“单一来源”可用于共享内容，例如条款和条件、付款期或联系人信息。

若要在 Commerce 站点构建器中创建使用跨渠道内容的渠道特定页面，请按照下列步骤操作。

1. 从特定渠道（例如 **Fabrikam 扩展的在线商店**）中，转到 **页面**，然后选择 **新建** 来创建一个新页面。
1. 在 **选择模板** 对话框中，选择一个模板，例如 **市场营销**。
1. 在 **页面名称** 下，输入页面名称（例如，**渠道特定页面**）。
1. 在 **页面 URL** 下，输入页面 URL（例如，**channelspecificpage**），然后选择 **确定**。
1. 在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **添加片段** 对话框中，在 **渠道** 下，选择 **跨渠道在线商店**。 您之前创建的跨渠道片段应显示在列表中。 选择它，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 您应该看到显示“跨渠道”的促销横幅。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>创建渠道特定版本的跨渠道页面

跨渠道共享支持替代跨渠道内容。 例如，您的站点渠道中除一个渠道之外的所有渠道都共享相同的内容。 该站点渠道需要不同的内容。 若要为其实现不同的内容，您可以通过创建渠道特定版本的跨渠道页面来使用渠道特定内容替代跨渠道内容。

若要在 Commerce 站点构建器中创建渠道特定版本的跨渠道页面，请按照下列步骤操作。

1. 在右上角的 **渠道** 字段中，选择 **跨渠道在线商店**。
1. 打开您之前创建的跨渠道页面。
1. 在右上角的 **渠道** 字段中，选择应具有特定内容的渠道。 页面编辑器显示一条消息，提示您创建新的页面变体。
1. 选择 **创建页面变体**。
1. 在页面变体的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **促销横幅** 模块，然后选择 **确定**。
1. 在 **促销横幅** 模块的属性窗格中，选择 **添加消息**，然后选择 **消息**。
1. 在 **消息** 对话框中，在 **文本** 下，输入 **渠道特定**，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 您应该看到显示“渠道特定”的促销横幅。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

现在，如果您使用渠道的基本 URL 并转到该站点上的跨渠道页面的 URL，您将看到渠道特定内容，而不是跨渠道内容。

## <a name="additional-resources"></a>其他资源

[添加内容的方法](add-manage-content.md)

[页面模型词汇表](page-elements-overview.md)

[文档状态和生命周期](document-states-overview.md)

[使用发布组](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
