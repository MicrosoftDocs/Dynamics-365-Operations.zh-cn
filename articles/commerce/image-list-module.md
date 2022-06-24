---
title: 图像列表模块
description: 本文介绍图像列表模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
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
ms.openlocfilehash: 8e47c9806c21de24f0e519d0132374d2e1ff2bbf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892792"
---
# <a name="image-list-module"></a>图像列表模块

[!include [banner](includes/banner.md)]

本文介绍图像列表模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

图像列表模块可用于轻松地将图像集合（阵列）添加到站点页面。 可以使用段落文本和链接 URL 配置阵列中的每个图像。 图像列表模块最适合显示品牌徽标或包含徽标的列表。

> [!IMPORTANT]
> - 图像列表模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始在 Commerce 模块库中提供。
> - 图像列表模块在 Adventure Works 主题中展示。

下图显示了一个示例，其中图像列表模块在 Adventure Works 企业对消费者 (B2C) 站点页面上显示包含徽标的文本列表。

![显示包含徽标的文本列表的图像列表模块的示例](./media/Image_list.PNG)

下图显示了一个示例，其中图像列表模块在 Adventure Works 企业对企业 (B2B) 站点页面上显示品牌徽标。

![显示品牌徽标的图像列表模块的示例](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>图像列表模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题       | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 图像列表模块的文本标题。 |
| 图像列表    | 图像、文本和 URL | 阵列中的每个项目都是带有段落文本和 URL 的图像。 |

## <a name="add-an-image-list-module-to-a-new-page"></a>将图像列表模块添加到新页面

若要将图像列表模块添加到新页面并在 Commerce 站点构建器中设置必需的属性，请按照以下步骤操作。

1. 转到 **模板**，打开站点主页的市场营销模板（或创建新的市场营销模板）。
1. 在默认页的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **图像列表** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，然后打开站点的主页（或使用市场营销模板创建新主页）。
1. 在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **图像列表**，然后选择 **确定**。
1. 在图像列表模块的属性窗格中，添加一个标题（例如，**我们的品牌**）。
1. 添加图像列表项，并指定图像、一些段落文本和重定向 URL。
1. 根据需要添加和配置其他图像列表项模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[Adventure Works 主题](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
