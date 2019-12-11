---
title: 预警模块
description: 此主题介绍预警模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785344"
---
# <a name="alert-module"></a>预警模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍预警模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

预警模块用于在页面中显示内联参考消息。 预警模块支持文本消息和链接。 可用于显示电子商务站点所有页面中显示的站点范围促销。 

预警模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。

## <a name="examples-of-alert-modules-in-e-commerce"></a>电子商务中的预警模块示例

可在站点标题中使用预警模块指示站点范围的促销或消息。 下面举了一些示例加以说明：

“年度促销 10 天后结束”

“返校季大促销。 快来买啦。”

## <a name="alert-module-properties"></a>预警模块属性

| 属性名称  | 值                              | 说明 |
|----------------|------------------------------------|-------------|
| 文本           | 文本                               | 预警模块中显示的文本消息。 |
| 文本对齐 | **向右对齐**、**向左对齐**或**居中对齐** | 用于定义预警模块中的文本如何对齐的值。 |
| 消除预警  | **True** 或 **False**              | 如果此值设置为 **True**，则客户可忽略预警。 |
| 链接           | URL                                | 可选链接的 URL。 |

## <a name="add-an-alert-module-to-a-page"></a>向页面添加预警模块 

若要向新页面添加预警模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**预警模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个预警模块。
1. 签入模板，然后发布。 
1. 使用您刚才创建的预警模板创建一个名称为**预警页**的页面。 
1. 在新页的**主**插槽中，添加一个预警模块。
1. 在预警模块的设置中，输入预警文本。 如果要进一步自定义预警模块，可以编辑其他属性。
1. 保存并预览页面。 在页面顶部，应该会看到包含您添加的文本的预警。
1. 签入页面，然后发布。 

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[传送模块](add-carousel.md)

[内容丰富块模块](add-content-rich-block.md)

[内容放置模块](add-content-placement-modules.md)

[特色模块](add-feature-module.md)

[主图模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)
