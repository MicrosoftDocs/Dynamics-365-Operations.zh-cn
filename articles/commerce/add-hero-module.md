---
title: 内容块模块
description: 本文介绍内容块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: dc6d728f49befd0c156340379dba05f592ca7919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276992"
---
# <a name="content-block-module"></a>内容块模块

[!include [banner](includes/banner.md)]

本文介绍内容块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

内容块模块用于通过图像和文本的组合营销产品或促销。 例如，零售商可向电子商务站点的主页添加一个内容块模块来促销新产品和吸引客户的注意。

内容块模块由内容管理系统 (CMS) 的数据驱动。 它是不依赖于页面上的其他任何模块的独立模块。 可将内容块模块放到零售商要进行营销或推广（如产品、销售或特色）的任何站点页中。

## <a name="examples-of-content-block-module-in-e-commerce"></a>电子商务中的内容块模块示例

- 可在电子商务站点的主页中使用内容块模块来重点展示促销和新产品。
- 可在产品详细信息页上使用内容块模块来展示产品信息。
- 可在一个传送模块中放置多个内容块模块来重点展示多个产品或促销。

## <a name="content-block-modules-and-themes"></a>内容块模块和主题

内容块模块可以支持基于主题的各种布局和样式。 例如，Fabrikam 主题支持内容块模块的三种布局变体：主图、特色和磁贴。 主图布局在背景上显示带有文字叠加层的图像。 功能布局并排显示图像和文本。 磁贴布局允许以磁贴格式显示多个内容块。

此外，主题可以为每个布局公开不同的属性。 主题开发人员可以使用内容块模块构建具有更多样式的更多布局。

下图显示了具有主图布局的内容块模块的示例。

![主图模块的示例。](./media/Hero.PNG)

下图显示了具有特色布局的内容块模块的示例。

![功能模块的示例。](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>内容块模块属性

| 属性名称  | 值 | 说明 |
|----------------|--------|-------------|
| 头像          | 图像文件 | 可使用图像来展示产品或促销。 可将图像上传到图像库，也可以使用现有图像。 |
| 标题        | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 每个主图模块都有标题。 默认情况下，将 **H2** 标题标记用于标题。 但是，可更改此标记以满足辅助功能要求。 |
| 段落      | 段落文本 | 主图模块支持富文本格式的段落文本。 支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。 为模块应用的页面主题可替代这些功能中的一部分。 |
| 链接           | 链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和 **在新标签页中打开链接** | 主图模块支持一个或多个“调用操作”链接。 如果添加链接，则需要链接文本、URL 和 ARIA 标签。 ARIA 标签应该具有描述性，以满足辅助功能要求。 可将链接配置为在新标签页中打开。 |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Fabrikam 主题公开的内容块模块属性 

| 属性名称  | 值 | 说明 |
|----------------|--------|-------------|
| 文本放置 | **向左对齐**、**向右对齐**、**居中对齐** | 此属性定义文本在图像上的位置。 它仅适用于主图布局。 |
| 文本主题     | **浅** 或 **深** | 可以基于背景图像为文本定义颜色主题。 例如，如果图像采用了深色背景，则可应用浅色主题来凸显文本和加强颜色对比度，以达到辅助功能目的。 它仅适用于主图布局。|
| 图像放置       | **向左对齐**、**向右对齐** | 此属性指定图像应位于文本的左侧还是右侧。 它仅适用于特色布局。  |

## <a name="add-a-content-block-module-to-a-new-page"></a>向新页面添加内容块模块

若要向新页面添加主图模块和设置必需的属性，请执行以下步骤。

1. 转到 **模板**，然后创建一个名称为 **内容块模板** 的页面模板。
1. 在默认页的 **主** 插槽中，添加一个主图模块。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 使用您刚才创建的主图模板创建一个名称为 **内容块页** 的页面。
1. 在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择主图模块，然后选择 **确定**。
1. 在左侧的大纲树中，选择该内容块模块。
1. 在右侧的属性窗格中，选择 **添加图像**。 然后选择现有图像或上传新图像。
1. 选择 **标题**。
1. 在 **标题** 对话框中，添加标题文本，选择标题级别，然后选择 **确定**。
1. 在 **富文本** 下，根据需要添加文本。
1. 选择 **添加链接**。
1. 在 **链接** 对话框中，添加链接的链接文本、链接 URL 和 ARIA 标签，然后选择 **确定**。
1. 选择 **主图** 布局。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。 

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[促销横幅模块](add-alert.md)

[传送模块](add-carousel.md)

[文本块模块](add-content-rich-block.md)

[视频播放器模块](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
