---
title: 传送模块
description: 此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785229"
---
# <a name="carousel-module"></a>传送模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

传送模块用于将多个促销项放到客户可浏览的传送中。 这是用于承载其他模块的特殊容器模块。 例如，零售商可在主页中使用传送模块展示多个新产品或促销。

可以在传送模块中添加主图模块和特色模块。 然后，传送模块的属性定义如何显示这些模块。

## <a name="examples-of-carousel-modules-in-e-commerce"></a>电子商务中的传送模块示例

- 可在主页中使用内部有多个促销模块的传送。
- 可在产品详细信息页中使用内部有多个促销模块的传送。
- 可在任何市场营销页中使用传送来促销多个促销或产品。

## <a name="carousel-module-properties"></a>传送模块属性

| 属性名称             | 值                                | 说明 |
|---------------------------|--------------------------------------|-------------|
| 自动播放                  | **True** 或 **False**                | 如果此值设置为 **True**，将自动在传送内的项之间进行切换。 如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。 |
| 幻灯片切换间隔 | 以秒为单位的值                   | 项之间的切换间隔。 |
| 切换动画      | **幻灯片**或**淡化**                | 切换效果。 |
| 宽度                     | **适合容器**或**充满屏幕** | 如果此值设置为**适合容器**，则传送内的项的宽度限制为传送的宽度。 如果此值设置为**充满屏幕**，则项不限制为传送宽度，而是可以进入全屏模式。 可以更改此值以获得所需布局。 |

## <a name="add-a-carousel-module-to-a-page"></a>向页面添加传送模块

若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**传送模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个传送模块。
1. 向该传送模块添加一个主图模块。
1. 向该传送模块添加一个特色模块。
1. 签入模板，然后发布。 
1. 使用您刚才创建的传送模板创建一个名称为**传送页**的页面。
1. 在新页的**主**插槽中，添加一个传送模块。
1. 将该传送模块的**宽度**属性设置为**充满屏幕**。 
1. 将**切换动画**属性设置为**幻灯片**。
1. 向该传送模块添加一个主图模块。
1. 在主图模块汇总，添加图像和标题，然后选择**保存**。
1. 向该传送模块添加一个特色模块。
1. 在特色模块中，添加图像、标题和一段文本。
1. 保存并预览页面。 此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。 可以更改传送、主图和特色模块的其他属性以获得所需效果。
1. 签入页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[预警模块](add-alert.md)

[内容丰富块模块](add-content-rich-block.md)

[内容放置模块](add-content-placement-modules.md)

[特色模块](add-feature-module.md)

[主图模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)
