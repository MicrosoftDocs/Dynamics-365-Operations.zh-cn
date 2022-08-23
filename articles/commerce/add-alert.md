---
title: 促销横幅模块
description: 本文介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fbde146923d1448e382cbf2458880f7e300f605c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279727"
---
# <a name="promo-banner-module"></a>促销横幅模块

[!include [banner](includes/banner.md)]

本文介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

促销横幅模块用于在页面中显示内联参考消息。 可用于显示电子商务站点所有页面中显示的站点范围促销。 

促销横幅模块支持文本消息和链接。 如果将多个消息添加到促销横幅模块，它将变成旋转的轮播横幅，使客户可以循环浏览所有消息。 

促销横幅模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>电子商务中促销横幅的使用情况示例

可以在网站标题中使用促销横幅，以显示网站范围内的促销或消息，如以下示例所示。

“年度促销 10 天后结束”

“返校季大促销。 快来买啦。”

“感恩节大减价！” 

下图显示了一个促销横幅示例。

![促销横幅模块的示例。](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>促销横幅模块属性

| 属性名称             | 值                              | 说明 |
|---------------------------|------------------------------------|-------------|
| 横幅消息           | 文本和链接                     | 文本和链接的数组。 |
| 自动播放                  | **True** 或 **False**              | 一个值，指示如果配置了多个消息，则是否自动循环显示消息。 |
| 幻灯片切换间隔 | 毫秒数      | 用于循环浏览消息的时间间隔。 |
| 允许消除             | **True** 或 **False**              | 如果此值设置为 **True**，则客户可忽略预警。 |
| 显示轮播翻转器     | **True** 或 **False**              | 一个值，该值指示是否应显示轮播翻转器，以便客户可以手动循环浏览多个横幅项目。 |
| 文本对齐            | **向右对齐**、**向左对齐** 或 **居中对齐** | 促销横幅模块中的文本对齐。 |
| 链接                      | URL                              | 可选链接的 URL。 |
|文本对齐方式             | **向右对齐**、**向左对齐** 或 **居中对齐** | 此属性作为 Adventure Works 主题中的主题扩展提供。 它允许用户在促销横幅中设置文本对齐方式。 |

> [!IMPORTANT]
> Adventure Works 主题从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。

## <a name="add-a-promo-banner-module-to-a-page"></a>向页面添加促销横幅模块 

若要向页面添加促销横幅模块和设置必需的属性，请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **促销横幅模板**，然后选择 **确定**。
1. 在 **页面大纲** 下面，将 **默认页面** 模块添加到 **正文** 插槽中。 
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。 
1. 使用您刚才创建的模板创建一个名称为 **促销横幅页** 的页面。 
1. 在新页的 **主** 插槽中，添加一个容器模块。 
1. 在右侧窗格中，将 **宽度** 值设置为 **填充容器**。
1. 在 **页面大纲** 下面，将促销横幅模块添加到容器模块中。
1. 在横幅模块的设置中，添加一个或多个横幅消息。 每条消息都可以具有带有链接的文本。 可以编辑其他属性以进一步自定义模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 在页面顶部，应该会看到显示您添加的文本的预警。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

> [!NOTE]
> 通常在页面标题槽或子标题槽中使用促销横幅。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[传送模块](add-carousel.md)

[文本块模块](add-content-rich-block.md)

[内容块模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
