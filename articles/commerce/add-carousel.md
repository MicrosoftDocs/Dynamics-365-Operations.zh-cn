---
title: 传送模块
description: 本文介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275819"
---
# <a name="carousel-module"></a>传送模块

[!include [banner](includes/banner.md)]

本文介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

传送模块用于将多个促销项（包括大量图像）放到客户可浏览的旋转式传送横幅中。 例如，零售商可在主页中使用传送模块展示多个新产品或促销。

可以在传送模块中添加内容块模块。 然后，传送模块的属性定义如何显示这些模块。

## <a name="examples-of-carousel-modules-in-e-commerce"></a>电子商务中的传送模块示例

- 可在主页中使用内部有多个促销模块的传送。
- 可在产品详细信息页中使用内部有多个促销模块的传送。
- 可在任何市场营销页中使用传送来促销多个促销或产品。

下图显示了主页上使用的传送模块的示例。 此传送模块包含多个内容块项。

![传送模块的示例。](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>传送模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 自动播放                  | **True** 或 **False** | 如果此值设置为 **True**，将自动在传送内的项之间进行切换。 如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。 |
| 幻灯片切换间隔 | 以秒为单位的值    | 项之间的切换间隔。 |
| 转换类型           | **幻灯片** 或 **淡化** | 项目之间的过渡效果。 |
| 隐藏轮播翻转器     | **True** 或 **False** | 如果该值设置为 **True**，轮播翻转器和顺序指示器将被隐藏。 |
| 允许轮播消除    | **True** 或 **False** | 如果此值设置为 **True**，则用户可消除轮播。 |

## <a name="add-a-carousel-module-to-a-page"></a>向页面添加传送模块

若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **传送模板**，然后选择 **确定**。
1. 在 **正文** 插槽中，添加一个 **默认页面** 模块。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。  
1. 使用您刚才创建的传送模板创建一个名称为 **传送页** 的页面。
1. 在新页的 **主** 插槽中，添加一个容器模块。 
1. 在右侧窗格中，将 **宽度** 值设置为 **填充屏幕**。
1. 在 **页面大纲** 下面，将传送模块添加到容器模块中。
1. 向该传送模块添加一个内容块模块。 通过提供 **标题**、**链接**、**布局** 和其他属性来设置内容块模块的属性。
1. 添加并配置另一个内容块模块。
1. 根据需要为传送模块设置其他属性。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。 可以更改传送、主图和特色模块的其他属性以获得所需效果。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[促销横幅模块](add-alert.md)

[文本块模块](add-content-rich-block.md)

[内容块模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
