---
title: 导航菜单模块
description: 本文介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281500"
---
# <a name="navigation-menu-module"></a>导航菜单模块

[!include [banner](includes/banner.md)]

本文介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

导航菜单模块的主要用途是让站点用户可以根据 Dynamics 365 Commerce 总部中定义的渠道导航层次结构浏览产品和站点页面。 导航菜单模块中配置的项显示为站点标题导航。 导航菜单模块还支持链接到电子商务网站上其他页面的静态菜单项。

导航菜单模块可以添加到页面的标题模块。 默认情况下，Fabrikam 主题中的导航菜单显示两个级别。 默认情况下，Starter 主题中的导航菜单显示三个级别。 若要切换为级别数量，主题中需要视图扩展。

下图显示 Fabrikam 站点的导航菜单示例，以及两个类别层次结构级别和一些静态菜单项。
![导航菜单模块的示例。](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>导航菜单模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 源                  | **零售**、**手动创作**、**零售和手动创作** | **零售** 值允许在导航菜单中显示 Commerce 总部的渠道导航层次结构。 **手动创作** 值允许策划静态菜单项。 **零售和手动创作** 值允许混合使用两者。 |
| 显示类别图像 | **True** 或 **False**    | 启用后，此属性将在 Commerce 总部中为每个类别定义的导航菜单上显示类别图像。 Commerce 版本 10.0.14 中已添加。 |
| 显示促销图像 | **True** 或 **False** | 启用此属性后，可以使用图像、链接和文本配置促销。 此属性在 Commerce 版本 10.0.17 中添加。 |
|添加类别促销内容 | 文本、图像或链接 | **显示促销图像** 属性启用后，您可以在导航菜单上添加文本、图像或链接作为促销内容。 |
| 启用多级导航菜单 | **True** 或 **False** | 启用此属性后，导航菜单可以显示多级导航层次结构。 Commerce 版本 10.0.15 中提供此功能。 |
| 级别数 | 整数 | 如果 **启用多级导航菜单** 属性设置为 **True**，此属性将定义应该显示的级别数。 |
| 静态菜单项| 值数组| 将菜单项名称与静态站点页的链接关联的静态菜单项。 可以在其他菜单项下创建菜单项。 默认情况下，静态菜单在根级别显示，并将追加到渠道导航层次结构（如果有）。 |
| 显示根菜单 | **True** 或 **False** | 启用此属性后，可以在自定义根下定义导航菜单（例如，**立即购物**）。 Dynamics 365 Commerce 10.0.15 版本中提供此功能。 |
| 根菜单 | 字符串 | 如果 **显示根菜单** 属性设置为 **True**，此属性可用于为自定义根定义文本。 |

下图显示 Fabrikam 站点的导航菜单中显示的类别图像的示例。
![具有类别图像的导航菜单模块的示例。](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>向标题模块添加导航菜单模块

有关如何向标题模块添加导航菜单模块的详细信息，请参阅[标题模块](author-header-module.md) 。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[痕迹导航模块](add-breadcrumb.md)

[站点选取器模块](site-selector.md)

[购买框模块](add-buy-box.md)

[Cookie 合规性](cookie-compliance.md)

[标题模块](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
