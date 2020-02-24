---
title: 文本块模块
description: 此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025589"
---
# <a name="text-block-module"></a>文本块模块


[!include [banner](includes/banner.md)]

此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

文本块模块是用于添加文本内容的模块。 此内容可以是参考内容或促销内容。

文本块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。 它们是不依赖于页面上下文或其他任何模块的独立模块。

## <a name="examples-of-text-block-modules-in-e-commerce"></a>电子商务中的文本块模块示例

可通过以下方式使用文本块模块：

* 在产品详细信息页中展示产品特色。
* 任何页面中起到参考作用。 例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。
* 在产品详细信息页中添加自定义消息。 （例如，“订单金额超过 50 美元免运费”）。
* 产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。

## <a name="text-block-module-properties"></a>文本块模块属性

| 属性名称     | Value                                            | 说明 |
|-------------------|--------------------------------------------------|-------------|
| 富文本         | 富文本                                        | 段落文本。 支持某些基本的富文本功能，如加粗，加下划线和斜体文本。 |
| 自定义类名称 | 级联样式表 (CSS) 类名称        | 开发人员提供的用于格式化此模块的自定义 CSS 类的名称。 类名称应在主题包中定义。 |
| 字号         | **小**、**中**、**大**或**特大** | 内容的字号。 |

## <a name="add-a-text-block-module-to-a-page"></a>向页面添加文本块模块

若要向新页面添加文本块模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**内容模板**的页面模板。 
1. 在**正文**插槽中，添加一个**默认页面**模块。
1. 编辑完模板，然后发布。
1. 使用您刚才创建的内容模板创建一个名称为**内容页**的页面。
1. 在新页的**主**插槽中，添加一个容器模块。
1. 在容器模块的属性窗格中，将**宽度**属性设置为**填充容器**。
1. 向该容器模块添加一个文本块模块。 
1. 在文本块模块的属性窗格中，将文本添加到**富文本**字段中。
1. 编辑完页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[促销横幅模块](add-alert.md)

[传送模块](add-carousel.md)

[内容块模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)

