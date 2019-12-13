---
title: 页脚模块
description: 此主题介绍页脚模块和如何在 Dynamics 365 Commerce 中制作页脚模块。
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697305"
---
# <a name="footer-module"></a>页脚模块  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍页脚模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。

## <a name="overview"></a>概览

页脚模块是用于承载页脚中显示的模块的特殊容器。 例如，其中可包含站点中各页面（如**联系我们**和**商店政策**页面）的链接。

## <a name="footer-module-properties"></a>页脚模块属性 

与大多数容器一样，页脚模块支持标题和宽度属性。 还支持添加多个页脚类别模块。 添加的每个页脚类别模块在页脚模块中显示为一列。

## <a name="modules-available-in-a-footer-module"></a>页脚模块中的可用模块

**页脚项** – 页脚项模块中可包含标题、图像和链接。 标题可以单独使用，也可以与图像和链接组合使用。 可配置页脚中的每个链接，使其仅包含文本（如“联系我们”和“隐私”链接），或使其同时包含文本和图像（例如，社交媒体链接）。

**返回顶部** – 返回顶部模块提供用于快速导航到页面顶部的链接。 需要目标。 默认目标值为 #，用于将用户带到页面顶部。

## <a name="author-a-footer-module"></a>制作页脚模块

1. 在导航窗格中，选择**片段**，然后选择**新建页面片段**。
1. 在**新页面片段**对话框中，选择页脚模块，输入页面片段的名称，然后选择**确定**。
1. 在左侧大纲树中，选择页脚模块的省略号按钮 (**...**)，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择页脚类别模块，然后选择**确定**。
1. 在大纲树中，选择页脚类别模块的省略号按钮，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择页脚项模块，然后选择**确定**。
1. 在大纲树中，选择页脚项模块。 然后，在右侧属性窗格中，根据需要配置标题、链接和链接文本，以及图像。
1. 若要添加更多页脚项，请重复执行第 5 步到第 7 步。
1. 若要向页脚添加“返回顶部”链接，请选择页脚类别模块的省略号按钮，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择返回顶部模块，然后选择**确定**。
1. 在大纲树中，选择返回顶部模块。 然后，在右侧的属性窗格中，根据需要配置返回顶部模块。
1. 保存页面片段，签入，然后发布。

在已经为站点创建的每个页面模板中，执行以下步骤。

1. 在默认页的**主**插槽中页脚模块内，添加创建的页脚片段。
1. 保存模板，签入，然后发布。

通过向页面模板添加页面片段，可帮助确保在每个页面中显示页脚。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
