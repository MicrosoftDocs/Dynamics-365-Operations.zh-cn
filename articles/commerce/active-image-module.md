---
title: 活动图像模块
description: 此主题介绍活动图像模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 06b9162029de3f5f3fede9583fa8a4a96fefb2f3
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780277"
---
# <a name="active-image-module"></a>活动图像模块

[!include [banner](includes/banner.md)]

此主题介绍活动图像模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

活动图像模块可用于在图像中嵌入产品标记。 然后，电子商务站点用户可以将鼠标悬停在标记上以预览图像中显示的产品。 预览显示在弹出窗口中。 通过选择预览弹出窗口，用户可以直接转到相应产品的产品详细信息页面 (PDP)。

使用图像上的 X 和 Y 坐标定义标记。 应该使用图像中显示的产品的产品 ID 配置每个标记的点。

下图显示了 Adventure Works 主页上主图上的预览弹出窗口示例。

![活动图像模块中的预览弹出窗口示例](./media/Active_image.PNG)

> [!IMPORTANT]
> - 活动图像模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。
> - 活动图像模块在 Adventure Works 主题中展示。

## <a name="active-image-module-properties"></a>活动图像模块属性

| 属性名称      | 值 | 说明 |
|--------------------|--------|-------------|
| 头像              | 图像文件 | 图像可用于展示一个或多个产品。 可以将图像上传到 Commerce 站点构建器中的媒体库，也可以使用现有图像。 |
| 宽度              | 像素数 | 此属性定义图像的宽度。 基于图像的宽度计算活动坐标。|
| 有效坐标 | X 和 Y 坐标，以及产品 ID 编号 | 每个活动图像阵列由 X 和 Y 坐标以及产品 ID 编号组成。|
| 标题            | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 默认情况下，**H2** 标题标记用于标题，但是可以更改标记以满足辅助功能要求。 |
| 段落          | 段落文本 | 模块支持富文本格式的段落文本。 支持某些基本的富文本功能，如超链接、加粗，加下划线、斜体文本。 为模块应用的页面主题可替代这些功能中的一部分。 |
| 链接               | 链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和 **在新选项卡中打开链接** 选择器 | 该模块支持一个或多个“调用操作”链接。 如果添加链接，则需要链接文本、URL 和 ARIA 标签。 ARIA 标签应该具有描述性，以满足辅助功能要求。 可将链接配置为在新标签页中打开。 |
| 子文本           | 标题、文本和链接 | 可以添加图像的其他上下文，例如作者或设计者姓名，或指向个人博客的链接。|
| 文本主题         | **浅** 或 **深** | 此属性允许用户基于背景图像将文本设置为浅色或深色。 它作为 Adventure Works 主题中的主题扩展提供。 |

## <a name="add-an-active-image-module-to-a-new-page"></a>将活动图像模块添加到新页面

若要将活动图像模块添加到新页面并设置必需的属性，请按照以下步骤操作。

1. 转到 **模板**，打开站点主页的市场营销模板（或创建新的市场营销模板）。
1. 在默认页的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **活动图像** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，然后打开站点的主页（或使用市场营销模板创建新主页）。
1. 在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **活动图像** 模块，然后选择 **确定**。
1. 在活动图像模块的属性窗格中，添加图像，并将画布宽度设置为图像的大小。
1. 设置 X 和 Y 坐标，并添加相应的产品 ID 编号。
1. 根据需要添加和配置其他活动图像模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[Adventure Works 主题](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
