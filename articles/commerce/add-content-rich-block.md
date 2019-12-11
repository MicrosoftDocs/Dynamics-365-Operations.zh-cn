---
title: 内容丰富块模块
description: 此主题介绍内容丰富块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785413"
---
# <a name="content-rich-block-module"></a>内容丰富块模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍内容丰富块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

内容丰富块模块是可在其中放入一个或多个内容丰富块项的特殊容器。 内容丰富块模块用于页面中的文本内容。 此内容可以是参考内容或促销内容。

内容丰富块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。 它们是不依赖于页面上下文或其他任何模块的独立模块。

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>电子商务中的内容丰富块模块示例

可通过以下方式使用内容丰富块模块：

* 在产品详细信息页中展示产品特色。
* 任何页面中起到参考作用。 例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。
* 在产品详细信息页中添加自定义消息。 （例如，“订单金额超过 50 美元免运费”）。
* 产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。

## <a name="content-rich-block-module-properties"></a>内容丰富块模块属性

| 属性名称     | 值                                 | 属性 |
|-------------------|---------------------------------------|----------|
| 列数 | 从 **1** 到 **4** 的数字     | 内容丰富块中的列数。 最多四列。 |
| 宽度             | **充满容器**或**充满屏幕** | 如果此值设置为**充满容器**，则容器内的项的宽度限制为容器的宽度。 如果此值设置为**充满屏幕**，则商品不限制为容器宽度，而是可以进入全屏模式。 可以更改此值以获得所需布局。 |

## <a name="content-rich-block-item-module-properties"></a>内容丰富块项模块属性

| 属性名称 | 值          | 说明 |
|---------------|----------------|-------------|
| 段落     | 段落文本 | 每个内容丰富块项随附的文本。 支持某些基本的富文本功能，如加粗，加下划线和斜体文本。 |

## <a name="add-a-content-rich-block-module-to-a-page"></a>向页面添加内容丰富块模块

若要向新页面添加内容丰富块模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**内容模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个内容丰富块模块。
1. 签入模板，然后发布。
1. 使用您刚才创建的内容模板创建一个名称为**内容页**的页面。
1. 在新页的**主**插槽中，添加一个内容丰富块模块。
1. 在内容丰富块模块的属性中，将列数设置为 **2**。
1. 在内容丰富块模块中，选择**添加模块**，然后添加一个内容丰富块项（例如，**item1**）。
1. 在新内容丰富块项中，添加段落文本。
1. 在内容丰富块模块中，选择**添加模块**，然后添加一个内容丰富块项（例如，**item2**）。
1. 在新内容丰富块项中，添加段落文本。
1. 保存页面，然后预览更改。 应该可以在两列视图中看到两个富文本块。
1. 签入页面，然后发布。

> [!NOTE]
> 如果添加第三个内容丰富块项，将把该项堆叠在之前添加的两个项的下方。 可通过更改容器中的列和项的数量为文本内容获得不同布局。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[预警模块](add-alert.md)

[传送模块](add-carousel.md)

[内容放置模块](add-content-placement-modules.md)

[特色模块](add-feature-module.md)

[主图模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)

