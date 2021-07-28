---
title: 磁贴列表模块
description: 此主题介绍磁贴列表模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 2da3c0415e996cadb5261d90c6353aa28bff3abb
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479414"
---
# <a name="tile-list-module"></a>磁贴列表模块

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题介绍磁贴列表模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

磁贴列表模块是传送中的磁贴的集合。 它用于通过图像和文本营销产品类别或产品品牌。 例如，零售商可以在电子商务站点的主页上添加磁贴列表模块，以推广所有畅销类别。

磁贴列表模块由内容管理系统 (CMS) 的数据驱动。 它不依赖于来自 Commerce Headquarters 的任何其他模块或数据。 可将磁贴列表模块添加到零售商要进行营销或推广（如产品、类别或品牌）的任何站点页面中。

下图显示了 Adventure Works 主页上磁贴列表模块和磁贴模块的示例。

![Adventure Works 主页上磁贴列表模块和磁贴模块的示例](./media/Tile_list.PNG)

> [!IMPORTANT]
> 磁贴列表模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。
> 磁贴列表模块在 Adventure Works 主题中展示。

## <a name="tile-list-modules-and-themes"></a>磁贴列表模块和主题

磁贴列表模块可以基于主题支持各种布局和样式。 例如，在 Adventure Works 主题中，当站点用户将鼠标悬停在磁贴上时，磁贴会显示动画效果。 每个主题都可以包含磁贴列表和磁贴模块的附加属性。 主题开发人员还可以为磁贴列表和磁贴模块构建其他布局。

## <a name="tile-list-module-properties"></a>磁贴列表模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题       | 标题文本和标题标记 | 磁贴列表模块的文本标题。 |

## <a name="tile-module-properties"></a>磁贴模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 头像         | 图像文件 | 可使用图像来展示产品或类别。 可以将图像上传到 Commerce 站点构建器中的媒体库，也可以使用现有图像。 |
| 标题       | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 默认情况下，**H2** 标题标记用于标题，但是可以更改标记以满足辅助功能要求。 |
| 段落     | 段落文本 | 模块支持富文本格式的段落文本。 支持某些基本的富文本功能，如超链接、加粗，加下划线、斜体文本。 为模块应用的页面主题可替代这些功能中的一部分。 |
| 链接          | 链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和 **在新标签页中打开链接** | 模块支持一个或多个“调用操作”链接。 如果添加链接，则需要链接文本、URL 和 ARIA 标签。 ARIA 标签应该具有描述性，以满足辅助功能要求。 可将链接配置为在新标签页中打开。 |
| 磁贴链接     | 链接文本、链接 URL、ARIA 标签和 **在新选项卡中打开链接** 选择器 | 此属性用于定义“调用操作”链接。 如果添加链接，则需要链接文本、URL 和 ARIA 标签。 ARIA 标签应该具有描述性，以满足辅助功能要求。 可将链接配置为在新标签页中打开。|
| 图标          | 头像 | 除了产品或类别图像之外，还可以添加图标符号。 图标符号图像将出现在产品或类别图像上方。 |

## <a name="add-a-tile-list-module-to-a-new-page"></a>将磁贴列表模块添加到新页面

若要将磁贴列表模块添加到新页面和设置必需的属性，请按照以下步骤操作。

1. 转到 **模板**，打开站点主页的市场营销模板（或创建新的市场营销模板）。
1. 在默认页的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **磁贴列表** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，然后打开站点的主页（或使用市场营销模板创建新主页）。
1. 在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **磁贴列表** 模块，然后选择 **确定**。
1. 在磁贴列表模块的属性窗格中，添加标题。
1. 在 **磁贴列表** 插槽中，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **磁贴模块** 模块，然后选择 **确定**。
1. 在磁贴模块的属性窗格中，添加图像、标题和图标符号图像。
1. 根据需要添加和配置其他磁贴模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[Adventure Works 主题](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
