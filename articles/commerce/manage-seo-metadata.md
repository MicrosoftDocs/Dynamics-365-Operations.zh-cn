---
title: 管理 SEO 元数据
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 78ed94ced246157daafbc482ce674cda6579f930
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881289"
---
# <a name="manage-seo-metadata"></a>管理 SEO 元数据

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。

可以使用站点地图和页面元数据管理站点的 SEO 元数据。
    
## <a name="site-maps"></a>站点地图

站点地图是网站中所有页面的 XML 格式机器可识别列表。 其供搜索引擎使用，所以可以改善站点的搜索结果。 站点地图可以由搜索引擎手动消化，也可以通过 robots.txt 文件发布。

Dynamics 365 Commerce 支持自动生成站点地图。 发布和取消发布页面时，将自动更新站点地图。

### <a name="turn-on-site-map-generation"></a>开启站点地图生成

1. 登录创作工具。
1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择 **站点管理**。
1. 确保已开启 **启用站点地图** 选项。

## <a name="page-metadata"></a>页面元数据

Dynamics 365 Commerce 允许您管理单个页面的 SEO 元数据。 可在页面容器的 **SEO 属性** 部分中查看和修改这些信息。 支持以下 SEO 元数据属性：

- 称谓
- 说明
- SEO 关键字
- Aria 标签
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>修改页面元数据

若要修改页面元数据，请执行以下步骤。
1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择 **页面**。
1. 选择主页在页面编辑器中将其打开。
1. 在命令栏中，选择 **编辑**。
1. 在页面编辑器中左侧页面大纲控件的顶部，选择 **大纲模式选项**（齿轮符号），然后选择 **高级大纲视图**。
1. 在大纲视图中，展开树控件以显示 **HTML 标头** 插槽的内容。
1. 在 **HTML 标头** 插槽中，选择所需的 SEO 模块（例如，**页面摘要**、**产品页面摘要**、**类别页面摘要** 或 **元标记**）。
1. 在右侧的属性窗格中，编辑所选 SEO 模块（例如 **标题**、**描述** 或 **共享图像**）所需的 SEO 数据。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 在 **注释** 字段中，输入 **更新的 SEO 数据**，然后选择 **确定**。
1. 选择 **预览** 预览您的页面。 完成后，关闭预览标签页回到创作工具。
1. 选择 **发布**。

> [!TIP]
> 作者可以在页面编辑器的左侧大纲控件顶部使用 **大纲模式选项**（齿轮符号），以在 **基本大纲视图** 和 **高级大纲视图** 之间切换。 **基本大纲视图** 是默认设置并将筛选大纲，以便它仅在页面的 **正文** HTML 插槽中显示模块。 **高级大纲视图** 显示整个页面模块，包括 **HTML 标头**、**正文开头** 和 **正文结尾** 插槽。 当作者必须编辑页面的特定 SEO 或脚本模块设置时，此视图很有用。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容的可访问性](verify-accessibility.md)

[基于 URL 参数创建动态电子商务页面](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
