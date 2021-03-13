---
title: 丰富产品页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。
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
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097330"
---
# <a name="enrich-a-product-page"></a>丰富产品页面


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。

## <a name="overview"></a>概览

默认情况下，站点使用通用页面显示产品数据。 这种页面中包含有关产品和销售产品需要的控件的基本信息。 但是，可以使用特定产品的更多图像或文本补充来自 Commerce Scale Unit 的信息。 此过程称为扩充产品页。

许多情况下，希望使用产品的更多具体内容。 在创作工具中转到 **Retail 和 Commerce** 时，将看到来自分配给站点的渠道的产品的列表。 在此列表中，**已扩充** 列指示是否已扩充了某个产品的产品页。 如果列中显示复选标记，说明产品有已扩充产品页。 如果不显示复选标记，说明对产品使用的是默认产品页和内容。 可通过在列表中选择产品名称预览已扩充产品页和未扩充产品页。

## <a name="enrich-a-product-page"></a>丰富产品页面

若要扩充产品页，请执行以下步骤。

1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择 **产品**。
1. 选择没有已扩充产品页的任何产品。
1. 在操作窗格上，选择 **扩充产品页**。
1. 选择 **PDP-template**，然后选择 **确定**。
1. 在左侧的页面大纲树中，展开 **主** 插槽。
1. 选择 **主** 插槽的省略号按钮 (**...**)，然后选择 **添加模块**。
1. 选择 **容器 2**，然后选择 **确定**。
1. 选择 **容器 2** 的省略号按钮，然后选择 **添加模块**。
1. 选择 **功能**，然后选择 **确定**。
1. 在右侧的属性窗格中 **富文本** 字段内，输入更新后的产品描述。
1. 在 **标题** 字段中，输入标题文本，然后选择 **确定**。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 在 **注释** 字段中，输入 **已扩充产品**，然后选择 **确定**。
1. 选择 **预览** 预览扩充后的产品页。 完成后，关闭预览标签页回到创作工具。
1. 选择 **发布**。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容的可访问性](verify-accessibility.md)

[基于 URL 参数创建动态电子商务页面](create-dynamic-pages.md)
