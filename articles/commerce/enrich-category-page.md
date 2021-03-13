---
title: 丰富类别登陆页面
description: 此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。
author: v-chgri
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 96fbd7c2ddfcd43e38e9572a60873d5f5930c94c
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097221"
---
# <a name="enrich-a-category-landing-page"></a>丰富类别登陆页面


[!include [banner](includes/banner.md)]

此主题介绍如何在 Dynamics 365 Commerce 中扩充类别页。

## <a name="overview"></a>概览

Commerce 提供显示类别数据时使用的默认类别登陆页。 默认类别页中包含必需的元素，如优化器、已分类的产品放置、排序选项、选项汇总和分页控件。 

但是，不应使用默认类别页，而是使用包含更多内容和更多特定元素的“扩充的”类别登陆页。 典型的扩充包括向类别页添加类别特定的市场营销内容。 此内容可能包括交叉销售用途的交叉类别产品放置、编辑列表、图像、视频和其他文本。 可以修改默认类别页或为特定类别定义其他类别页。

![扩充的类别登陆页面](./media/CategoryLandingPages.png)

在 Commerce 站点构建器中，**产品** 页包含渠道中分配给站点的类别的列表。 如果为类别页选择 **扩充** 状态，则说明该类别页已扩充。 否则，对类别使用默认类别页和内容。 可通过选择类别名称预览类别的扩充类别页和未扩充类别页。

若要扩充类别页，请执行以下操作。

1. 在 **产品** 页中，选择要扩充其类别页的类别的名称。 将在页面编辑器中打开所选类别的默认类别页。
2. 选择 **扩充类别页**。
3. 选择已扩充类别页的模板。 如果仅进行微小更改，可选择默认类别页。 也可以选择特定类别页模板。 选择模板后，将打开页面编辑器，并使用所选模板为所选类别创建新的类别页。 将把此页签出给您，而您现在可进行更改。

> [!NOTE]
> 使用类别规范数据的模块使用所选类别的数据。 您选择的模板的设置决定您可以进行的更改。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[验证页面内容的可访问性](verify-accessibility.md)

[基于 URL 参数创建动态电子商务页面](create-dynamic-pages.md)
