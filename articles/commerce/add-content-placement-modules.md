---
title: 内容放置模块
description: 此主题介绍内容放置模块和内容放置项模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785291"
---
# <a name="content-placement-module"></a>内容放置模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍内容放置模块和内容放置项模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

内容放置模块是可以将其他模块按照特定布局放到其中的特殊容器。 内容放置模块支持将以下模块类型用作子模块：内容放置项、帐户欢迎项、帐户订单项、帐户愿望列表项和帐户个人资料项。

内容放置模块的数据派生自其支持的子模块。 因此，可以通过多种方法使用内容放置模块，具体取决于向其添加的模块。

内容放置模块使用图像和文本展示促销、政策和产品特色。 例如，可在主页中使用内容放置项模块显示商店政策或装运信息。 内容放置项模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。 但是，只能在内容放置模块中使用。

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>电子商务中的内容放置模块示例

* 可在主页或市场营销页中使用其中包含内容放置项模块的内容放置模块，以通过图像和文本展示产品特色、促销、商店政策、装运信息和其他信息。
* 可在产品详细信息页中使用其中包含内容放置项模块的内容放置模块，以展示产品特色。
* 可在帐户管理页中使用其中包含帐户欢迎项或帐户订单项模块的内容放置模块。

## <a name="content-placement-module-properties"></a>内容放置模块属性

| 属性名称 | 值 | 说明 |
|---------------|-------|-------------|
| 宽度         | **适合容器**或**充满屏幕** | 如果此值设置为**适合容器**，则内容放置模块内的项的宽度限制为内容放置模块的宽度。 如果此值设置为**充满屏幕**，则项不限制为内容放置模块宽度，而是可以进入全屏模式。 |

## <a name="content-placement-item-module-properties"></a>内容放置项模块属性

| 属性名称 | 值 | 说明 |
|---------------|-------|-------------|
| 标题       | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 每个内容放置项模块都可以有标题。 **标题**属性支持标题标记。 默认情况下使用 **H2** 标题，但是可以根据辅助功能需要更改标题标记。 |
| 段落     | 段落文本 | 内容放置项模块支持富文本格式的段落文本。 支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。 为模块应用的页面主题可替代这些功能中的一部分。 |
| 头像         | 图像文件 | 可以将图像与文本关联。 |
| 链接          | 链接 URL 和链接文本 | 可以向文本添加链接，以便将用户重定向到特定页。 |
| 磁贴大小     | 从 **1** 到 **12** 的数字 | 每个内容放置项的此属性定义项在内容放置模块中应该填充的插槽数量。 内容放置模块的最大大小为 12 个插槽。 如果内容放置模块中的前 *n* 个项的总磁贴大小超过 12 个插槽，则项换行到下一行。 |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>向页面添加一个其中包含一个内容放置项模块的内容放置模块

若要向新页面添加一个其中包含一个内容放置项模块的内容放置模块并设置必需的属性，请执行以下步骤。

1. 创建一个名称为**内容放置模块**的模板。
1. 在默认页的**主**插槽中，添加一个内容放置模块。
1. 在该内容放置模块中，添加一个内容放置项模块。
1. 签入模板，然后发布。
1. 使用您刚才创建的内容放置模板创建一个名称为**内容放置页**的页面。
1. 在新页的**主**插槽中，添加一个内容放置模块。
1. 在该内容放置模块中，添加一个内容放置项模块。
1. 在内容放置项模块的属性窗格中，选择一个图像，添加标题，添加段落，添加链接，设置链接 URL，然后将磁贴大小设置为 **6**。
1. 重复步骤 7 和 8 再添加一个采用相同磁贴大小的内容放置项模块。
1. 保存并预览页面。 应该会看到两个并排显示的内容放置项。 可调整每个内容放置项模块的**磁贴大小**属性，或添加更多模块以获得所需布局。
1. 签入页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[预警模块](add-alert.md)

[传送模块](add-carousel.md)

[内容丰富块模块](add-content-rich-block.md)

[特色模块](add-feature-module.md)

[主图模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)
