---
title: 选项卡模块
description: 本主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7d2cd7b7ce9446d77eff66433739c8ea6b1f309
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348288"
---
# <a name="tab-module"></a>标签模块

[!include [banner](includes/banner.md)]

本主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

选项卡模块是类似于容器的模块，用于组织选项卡的站点页面上的信息。 此类模块可以在必须在选项卡上呈现信息的任何页面上使用。

在每个选项卡模块中，可以添加一个或多个选项卡项模块。 每个选项卡项模块代表一个选项卡。在每个选项卡项模块中，可以添加一个或多个模块。 可添加到选项卡项模块的模块类型没有限制。

下图显示了站点页上的选项卡模块的示例。 在此示例中，已选择 **装运** 选项卡。

![选项卡模块的示例。](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>选项卡模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题 | 文本 | 此属性为选项卡模块指定可选的文本标题。 |
| 活动选项卡索引 | 数值 | 此属性指定在加载页面时默认应处于活动状态的选项卡。 如果未提供任何值，默认第一个选项卡项处于活动状态。 |

## <a name="tab-item-module-properties"></a>选项卡项模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 职称 | 文本 | 此属性为选项卡项模块指定标题文本。 |

## <a name="add-a-tab-module-to-a-page"></a>向页面添加选项卡模块

若要向页面添加选项卡模块和设置属性，请执行以下步骤。

1. 使用 Fabrikam 市场营销模板（或任何没有限制的模板）创建一个名为 **商店政策页面** 的新页面。
1. 在 **默认页** 的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **选项卡** 模块，然后选择 **确定**。
1. 在选项卡模块的属性窗格中，选择铅笔符号旁边的 **标题**。
1. 在 **标题** 对话框中，在 **标题文本** 下，输入标题文本（例如，**政策**）。 然后选择 **确定**。
1. 在 **选项卡** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **选项卡项** 模块，然后选择 **确定**。
1. 在选项卡项模块的属性窗格中，在 **标题** 下，输入标题文本（例如，**交货**）。
1. 在 **选项卡项** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **文本块** 模块，然后选择 **确定**。
1. 在文本块模块的属性窗格中，在 **富文本** 下，输入一段文本。
1. 在 **选项卡** 插槽中，再添加几个带有标题的选项卡项模块。 在每个选项卡项模块中，添加一个有内容的文本块模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 页面将显示一个选项卡模块，其中包含具有您添加的内容的选项卡项模块。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[容器模块](add-container-module.md)

[可折叠模块](add-accordion.md)

[文本块模块](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]