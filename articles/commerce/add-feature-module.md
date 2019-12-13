---
title: 特色模块
description: 此主题介绍特色模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785275"
---
# <a name="feature-module"></a>特色模块 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍特色模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

特色模块用于通过图像和文本的组合营销产品或促销。 例如，零售商可以向产品详细信息页添加特色模块以重点介绍产品的特色。

特色模块由内容管理系统 (CMS) 的数据驱动。 它是不依赖于页面上的其他任何模块的独立模块。 可将特色模块放到零售商要进行营销或推广（如产品、销售或特色）的任何站点页中。

## <a name="examples-of-feature-modules-in-e-commerce"></a>电子商务中的特色模块示例

可在以下页中使用特色模块：

- 产品详细信息页，用于展示产品特色
- 主页，用于促销产品
- 类别页，用于重点展示一类产品

## <a name="feature-module-properties"></a>特色模块属性

| 属性名称     | 值 | 说明 |
|-------------------|--------|-------------|
| 头像             | 图像文件 | 可使用图像来营销产品或促销。 可将图像上传到图像库，也可以使用现有图像。 |
| 标题           | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 每个特色模块都有标题。 默认情况下，将 **H2** 标题标记用于标题。 但是，可更改此标记以满足辅助功能要求。 |
| 段落         | 段落文本 | 特色模块支持富文本格式的段落文本。 支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。 为模块应用的页面主题可替代这些功能中的一部分。 |
| 链接              | 链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和**在新标签页中打开链接** | 特色模块支持一个或多个“调用操作”链接。 如果添加链接，则需要链接文本、URL 和 ARIA 标签。 ARIA 标签应该具有描述性，以满足辅助功能要求。 可将链接配置为在新标签页中打开。 |
| 图像放置   | **靠右**、**靠左**、**靠上**或**靠下** | 此属性定义图像相对文本的位置。 例如，如果选择**靠右**，则图像在文本右侧显示。 |
| 图像列大小 | 从 **1** 到 **12** 的值 | 此属性定义图像相对文本的大小。 大小表示为页面中的列数。 页面中有 12 列。 默认情况下，图像和文本的大小相等（分别六列）。 但是，可以根据需要调整大小。 |

## <a name="add-a-feature-module-to-a-new-page"></a>向新页添加特色模块 

若要向新页面添加特色模块和设置必需的属性，请执行以下步骤。

1. 转到**模板**，然后创建一个名称为**特色模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个特色模块。
1. 签入模板，然后发布。
1. 使用您刚才创建的特色模板创建一个名称为**特色页**的页面。
1. 在默认页的**主**插槽，选择省略号按钮 (**...**)，然后选择**添加模块**。
1. 在**添加模块**对话框中**选择模块**下，选择一个特色模块，然后选择**确定**。
1. 在左侧的大纲树中，选择该特色模块。
1. 在右侧的属性窗格中，选择**添加图像**。 然后选择现有图像或上传新图像。
1. 选择**标题**。
1. 在**标题**对话框中，添加标题文本，选择标题级别，然后选择**确定**。
1. 在**富文本**下，根据需要添加文本。
1. 选择**添加操作链接**。
1. 在**操作链接**对话框中，添加链接的链接文本、链接 URL 和 ARIA 标签，然后选择**确定**。
1. 保存页面，然后预览更改。
1. 签入页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[预警模块](add-alert.md)

[传送模块](add-carousel.md)

[内容丰富块模块](add-content-rich-block.md)

[内容放置模块](add-content-placement-modules.md)

[主图模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)
