---
title: 页脚模块
description: 此主题介绍页脚模块和如何在 Dynamics 365 Commerce 中制作页脚模块。
author: anupamar-ms
ms.date: 03/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81db5cf32f23b7ee1ca8325eeec2e6ceafda55e0
ms.sourcegitcommit: 90a553e271e7cd471fed2e4f006d753fdb67b47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2022
ms.locfileid: "8374823"
---
# <a name="footer-module"></a>页脚模块  

[!include [banner](includes/banner.md)]

此主题介绍页脚模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。

页脚模块是用于承载页脚中显示的模块的特殊容器。 例如，其中可包含站点中各页面（如 **联系我们** 和 **商店政策** 页面）的链接。

下图显示了站点页上的页脚模块的示例。

![页脚模块的示例。](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>页脚模块属性 

与大多数容器一样，页脚模块支持标题和宽度属性。 还支持添加多个页脚类别模块。 添加的每个页脚类别模块在页脚模块中显示为一列。

## <a name="modules-available-in-a-footer-module"></a>页脚模块中的可用模块

**页脚项** – 页脚项模块中可包含标题或链接。 标题通常用作页脚部分标题。  可配置页脚中的每个链接，使其仅包含文本（如“联系我们”和“隐私”链接），或使其同时包含文本和图像（例如，社交媒体链接）。 如果同时提供了标题和链接，标题属性优先于链接。 

**返回顶部** – 返回顶部模块提供用于快速导航到页面顶部的链接。 需要目标。 默认目标值为 \#，用于将用户带到页面顶部。

## <a name="create-a-footer-module"></a>创建页脚模块

1. 转到 **片段**，选择 **新建** 创建新片段。
1. 在 **新建片段** 对话框中，选择 **容器** 模块，输入片段的名称，然后选择 **确定**。
1. 在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **页脚类别** 模块，然后选择 **确定**。
1. 在 **页脚类别** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **页脚项** 模块，然后选择 **确定**。
1. 选择 **页脚项** 插槽，然后，在右侧属性窗格中，根据需要配置标题、链接和链接文本，以及图像。
1. 若要添加更多页脚项，请为每个页脚项重复执行步骤 5 到 7。
1. 若要向页脚添加“返回顶部”链接，请选择 **页脚类别** 插槽中的省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **返回顶部** 模块，然后选择 **确定**。
1. 选择 **返回顶部** 插槽，然后，在右侧属性窗格中，根据需要配置文本及其他模块属性。
1. 选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。

若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。

1. 在 **默认页** 模块的 **页脚** 插槽中，添加创建的页脚片段。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

通过向页面模板添加片段，可帮助确保在每个页面中显示页脚。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
