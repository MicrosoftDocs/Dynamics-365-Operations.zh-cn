---
title: 站点选择器模块
description: 本主题介绍了站点选择器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665215"
---
# <a name="site-selector-module"></a>站点选择器模块

[!include [banner](includes/banner.md)]

本主题介绍了站点选择器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

## <a name="overview"></a>概览

当企业跨市场、地区和区域具有不同的站点时，站点用户需要通过一种简单的方法在站点之间进行切换并选择他们喜欢的购物站点。 为了适应这种情况，站点选择器模块使用户能够跨多个站点浏览。

站点选择器模块必须配置有站点用户可以浏览的站点列表（市场、地区或区域）。

> [!NOTE]
> Dynamics 365 Commerce 10.0.14 版本中提供了站点选择器模块。

下图显示了站点页面标题中具有的站点选择器模块示例。

![站点页面标题中的站点选择器模块示例](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>站点选择器模块属性

| 属性名称 | 值                 | 说明 |
|---------------|-----------------------|-------------|
| 标题       | 文本                  | 模块的标题。 |
| 站点选项  | 名称、图像、URL      | 此属性指定名称、指向站点主页的链接以及为模块中包含的每个站点显示的可选图像。 该图像可以是旗帜，也可以是市场、地区或区域的某种表示形式。 |

## <a name="add-a-site-selector-module-to-a-page"></a>向页面添加站点选择器模块

站点选择器模块可以添加到站点选择器插槽下的[标题模块](author-header-module.md)。 添加后，您可以定义模块标题和站点选项。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[标题模块](author-header-module.md)

[痕迹导航模块](add-breadcrumb.md)

[导航菜单模块](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]