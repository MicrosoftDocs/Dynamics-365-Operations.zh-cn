---
title: 促销横幅模块
description: 此主题介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025612"
---
# <a name="promo-banner-module"></a>促销横幅模块


[!include [banner](includes/banner.md)]

此主题介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

促销横幅模块用于在页面中显示内联参考消息。 可用于显示电子商务站点所有页面中显示的站点范围促销。 

促销横幅模块支持文本消息和链接。 如果将多个消息添加到促销横幅模块，它将变成旋转的轮播横幅，使客户可以循环浏览所有消息。 

促销横幅模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>电子商务中促销横幅的用法示例

可以在网站标题中使用促销横幅，以显示网站范围内的促销或消息，如以下示例所示。

“年度促销 10 天后结束”

“返校季大促销。 快来买啦。”

## <a name="promo-banner-module-properties"></a>促销横幅模块属性

| 属性名称             | Value                              | 说明 |
|---------------------------|------------------------------------|-------------|
| 横幅消息           | 文本和链接                     | 文本和链接的数组。 |
| 自动播放                  | **True** 或 **False**              | 一个值，指示如果配置了多个消息，则是否自动循环显示消息。 |
| 幻灯片切换间隔 | 毫秒数      | 用于循环浏览消息的时间间隔。 |
| 允许消除             | **True** 或 **False**              | 如果此值设置为 **True**，则客户可忽略预警。 |
| 显示轮播翻转器     | **True** 或 **False**              | 一个值，该值指示是否应显示轮播翻转器，以便客户可以手动循环浏览多个横幅项目。 |
| 文本对齐            | **向右对齐**、**向左对齐**或**居中对齐** | 促销横幅模块中的文本对齐。 |
| 链接                      | URL                              | 可选链接的 URL。 |

## <a name="add-a-promo-banner-module-to-a-page"></a>向页面添加促销横幅模块 

若要向页面添加促销横幅模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**促销横幅模板**的页面模板。
1. 在**页面大纲**下面，将**默认页面**模块添加到**正文**插槽中。 
1. 签入模板，然后发布。 
1. 使用您刚才创建的模板创建一个名称为**促销横幅页**的页面。 
1. 在新页的**主**插槽中，添加一个容器模块。 
1. 在右侧窗格中，将**宽度**值设置为**填充容器**。
1. 在**页面大纲**下面，将促销横幅模块添加到容器模块中。
1. 在横幅模块的设置中，添加一个或多个横幅消息。 每条消息都可以具有带有链接的文本。 可以编辑其他属性以进一步自定义模块。
1. 保存并预览页面。 在页面顶部，应该会看到显示您添加的文本的预警。
1. 编辑完页面，然后发布。 

> [!NOTE]
> 通常在页面标题槽或子标题槽中使用促销横幅。


## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[传送模块](add-carousel.md)

[文本块模块](add-content-rich-block.md)

[内容块模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)
