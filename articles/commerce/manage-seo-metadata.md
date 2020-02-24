---
title: 管理 SEO 元数据
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003456"
---
# <a name="manage-seo-metadata"></a>管理 SEO 元数据


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。

## <a name="overview"></a>概览

可以使用站点地图和页面元数据管理站点的 SEO 元数据。
    
## <a name="site-maps"></a>站点地图

站点地图是网站中所有页面的 XML 格式机器可识别列表。 其供搜索引擎使用，所以可以改善站点的搜索结果。 站点地图可以由搜索引擎手动消化，也可以通过 robots.txt 文件发布。

Dynamics 365 Commerce 支持自动生成站点地图。 发布和取消发布页面时，将自动更新站点地图。

### <a name="turn-on-site-map-generation"></a>开启站点地图生成

1. 登录创作工具。
1. 在**站点**下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择**站点管理**。
1. 确保已开启**启用站点地图**选项。

## <a name="page-metadata"></a>页面元数据

Dynamics 365 Commerce 允许您管理单个页面的 SEO 元数据。 可在页面容器的 **SEO 属性**部分中查看和修改这些信息。 支持以下 SEO 元数据属性：

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

1. 在**站点**下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择**页面**。
1. 选择主页在页面编辑器中将其打开。
1. 在操作窗格上，选择**签出**。
1. 在右侧的属性窗格中，展开**默认元数据**。
1. 若要添加新的元标记，请选择**添加**，然后在字段中输入标记。

    若要删除现有元标记，请选择其右侧的废纸篓符合。

1. 选择**保存**，然后选择**签入**。
1. 在**注释**字段中，输入**更新的元标记**，然后选择**确定**。
1. 选择**预览**预览您的页面。 完成后，关闭预览标签页回到创作工具。
1. 选择**发布**。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容可访问性](verify-accessibility.md)
