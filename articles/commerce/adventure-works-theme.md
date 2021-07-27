---
title: Adventure Works 主题概述
description: 本主题概述了 Adventure Works 主题并介绍了如何在 Microsoft Dynamics 365 Commerce 中将其应用于站点页面。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479411"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works 主题概述

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题概述了 Adventure Works 主题并介绍了如何在 Microsoft Dynamics 365 Commerce 中将其应用于站点页面。

Dynamics 365 Commerce 有一个名为 Adventure Works 的电子商务主题。 Adventure Works 主题展示了体育和休闲产品，并针对丰富和增强的故事分享体验进行了优化。 它提供现代外观、新布局和动画效果，为电子商务客户创造身临其境、引人入胜的在线购物体验。

Adventure Works 主题提供了以下新工作流：

- 视频播放器模块现在支持标题、段落和链接功能以提供额外的故事分享。
- 添加到购物车操作调用迷你购物车，而不是提供通知。
- 快速查看模块是一个可以在桌面和移动视区中滑入的窗格。
- 空购物车现在可以展示促销活动。

Adventure Works 主题在 Commerce 模块库中包含以下故事分享模块：

- 磁贴列表模块
- 交互式功能模块
- 订阅模块
- 活动图像模块
- 图像列表模块

Adventure Works 主题完全可响应，并为桌面、移动和平板电脑视区提供优化的体验。

> [!IMPORTANT]
> Adventure Works 主题和新模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。

下图显示了使用 Adventure Works 主题的主页的示例。

![使用 Adventure Works 主题的主页的示例](./media/aw_b2c.PNG)

下图显示了使用 Adventure Works 主题的列表页面的示例。

![使用 Adventure Works 主题的列表页面的示例](./media/Aw_list.PNG)

下图显示了使用 Adventure Works 主题的产品详细信息页面 (PDP) 的示例。

![使用 Adventure Works 主题的产品详细信息页面 (PDP) 的示例](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>将 Adventure Works 主题用于 B2B 站点

Adventure Works 主题也是企业到企业 (B2B) 站点的参考主题。 Adventure Works 主题中展示了所有 B2B 模块和工作流。 有关如何设置 B2B 站点的信息，请参阅 [B2B 站点设置](./b2b/set-up-b2b-site.md)。

下图显示了使用 Adventure Works 主题的 B2B 主页的示例。

![使用 Adventure Works 主题的 B2B 主页的示例](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>主题扩展

Adventure Works 主题包括多个主题扩展，例如 **查看扩展** 和 **模块定义** 扩展。 Adventure Works 主题可用作参考主题来构建类似扩展。 例如，Adventure Works 主题中的列表页面作为具有水平优化器的视图扩展实现。 （相反，Fabrikam 主题中使用了左侧窗格优化器。）

同样，其他模块包括模块定义扩展。 例如，[购物车图标模块](cart-icon-module.md)包括两个通过使用模块定义扩展实现的额外 **空购物车** 和 **促销内容** 插槽。 此外，已向标题模块添加了新的 **移动徽标** 属性以在移动视区上支持徽标。 此属性作为标题模块定义扩展实现。

有关主题扩展的详细信息，请参阅[主题扩展](e-commerce-extensibility/theme-module-extensions.md)。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[磁贴列表模块](tile-list-module.md)

[交互式功能模块](interactive-feature-module.md)

[活动图像模块](active-image-module.md)

[订阅模块](subscribe-module.md)

[图像列表模块](image-list-module.md)

[主题扩展](e-commerce-extensibility/theme-module-extensions.md)

[购物车图标模块](cart-icon-module.md)

[建立 B2B 电子商务站点](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
