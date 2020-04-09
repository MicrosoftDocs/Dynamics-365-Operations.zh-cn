---
title: 页眉模块
description: 此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025643"
---
# <a name="header-module"></a>标题模块


[!include [banner](includes/banner.md)]

此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。

## <a name="overview"></a>概览

在 Dynamics 365 Commerce 中，页面标题包含多个模块，例如标题、导航菜单、搜索、促销横幅和 cookie 同意模块。 

标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车符号、愿望列表符号、登录选项和搜索栏。 针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。 例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。

## <a name="properties-of-a-header-module"></a>标题模块的属性

标题模块支持**徽标图像**、**徽标链接**和**我的帐户连结**属性。 

**徽标图像**和**徽标链接**属性用于在页面上定义徽标。 有关详细信息，请参阅[添加徽标](add-logo.md)。 

**我的帐户链接**属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。

## <a name="modules-that-are-available-in-a-header-module"></a>页眉模块中的可用模块

页眉模块中可使用以下模块：

- **导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。 可以在 Dynamics 365 Commerce 中配置渠道导航层次结构。 导航菜单有一个**导航来源**属性，用于指定零售服务器导航菜单项和静态菜单项作为来源。 如果将静态菜单项指定为来源，则可以提供指向站点上其他页面的相对链接。 配置的项然后显示为页眉导航。 
- **搜索** – 用户可使用搜索模块输入搜索词以搜索产品。 必须在**站点设置 \> 扩展**中提供默认搜索页面的 URL 和搜索查询参数。 搜索模块的属性可让您根据需要隐藏搜索按钮或标签。 搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。

## <a name="create-a-header-module-for-a-page"></a>创建页面的标题模块

若要创建页眉模块，请执行以下步骤。

1. 创建一个名称为**标题片段**的片段，然后向其添加一个容器模块。
1. 在容器模块的属性窗格中，将**宽度**属性设置为**填充容器**。
1. 将促销横幅和 Cookie 同意模块添加到容器模块。
1. 向片段添加另一个容器模块，将**宽度**属性设置为**填充容器**。
1. 向第二个容器模块添加一个标题模块。
1. 在标题模块的**导航菜单**插槽中，添加导航菜单模块。 
1. 在导航菜单模块的属性窗格中，配置导航菜单模块的属性。
1. 在标题模块的**搜索**插槽中，添加搜索模块。 
1. 在搜索模块的属性窗格中，配置搜索模块的属性。 
1. 保存页面片段，完成编辑，然后发布。 

若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。

1. 在默认页面的**主**插槽中，向标题添加其中包含标题模块的标题页面片段。
1. 保存模板，完成编辑，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
