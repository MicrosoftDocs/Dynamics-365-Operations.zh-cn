---
title: 添加新的站点页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加新的站点页面。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d96f173c68bd6a7d9c7a559ed7f18329c3508af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208031"
---
# <a name="add-a-new-site-page"></a>添加新的站点页面


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加新的站点页面。

## <a name="overview"></a>概览

为站点创建模板和片段之后，下一步是开始创建使用这些模板和片段的页面。 首先，必须选择模板或布局，页面名称和页面 URL。

## <a name="template-or-layout"></a>模板或布局

可为新页面使用模板或布局。 有关详细信息，请参阅[模板和布局概述](templates-layouts-overview.md)。

## <a name="page-name"></a>页面名称

页面名称对于页面必须唯一。 应该具有描述性，以便您轻松找到，其他人可以知道页面的用途。 请仔细选择页面名称，因为以后不能更改。

## <a name="page-url"></a>页面 URL

提供了用于为新页面输入 URL 的选项。 创建页面时，可输入将用于构成完整 URL 的字符串。 此字符串称为相对 URL 或 URL 数据域。 然后基于 URL 数据域生成完整 URL，并将新页面分配给它。 可在以后发布页面前更改 URL 数据域。 有关详细信息，请参阅[创建页面 URL](create-page-URL.md)。

> [!NOTE]
> Dynamics 365 Commerce 分离 URL 和内容。 换句话说，可以创建不与 URL 关联的页面，也可以创建不与页面关联的 URL。 因此，可以为 URL 执行内容交还，并且不需要停机时间，而重定向更容易管理。

## <a name="add-a-new-page"></a>添加新页面

若要向站点添加新站点页面，请执行以下步骤。

1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 选择 **新建页面**。
1. 在 **新页面** 对话框中，选择一个模板，然后选择 **确定**。
1. 在 **页面名称** 字段中，输入页面名称（例如，**我的新页面**）。
1. 在 **URL** 字段中，输入一个字符串（URL 数据域）完成该 URL（例如，**mynewpage**）。
1. 选择 **确定**。 将显示页面编辑器。 请注意，将根据您选择的模板自动向页面添加页眉和页脚。
1. 在页面大纲中，选择 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 选择 **容器**，然后选择 **确定**
1. 选择 **流体容器**，选择省略号按钮，然后选择 **添加模块**。
1. 选择 **内容丰富块**，然后选择 **确定**。
1. 选择 **内容丰富块**，选择省略号按钮，然后选择 **添加模块**。
1. 选择 **内容丰富块项**，然后选择 **确定**。
1. 在右侧属性窗格中，选择 **段落**，然后在字段中，输入 **我的测试文本**。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 在 **注释** 字段中，输入 **添加的新页面**，然后选择 **确定**。
1. 选择 **预览** 预览您的页面。 完成后，关闭预览标签页回到创作工具。
1. 选择 **发布**。
1. 在导航路径（面包屑导航）中，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择 **URL**。
1. 在列表中找到并选择您的 URL (**mynewpage**)。
1. 选择 **发布**。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容的可访问性](verify-accessibility.md)

[基于 URL 参数创建动态电子商务页面](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]