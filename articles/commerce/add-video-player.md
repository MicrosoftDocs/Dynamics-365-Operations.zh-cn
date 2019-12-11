---
title: 视频播放器模块
description: 此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785321"
---
# <a name="video-player-module"></a>视频播放器模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

视频播放器模块用于支持视频播放。 商店入门套件提供了两个视频播放器模块：氛围视频播放器模块和视频播放器模块。 这两个播放器都支持 .mp4 媒体类型。

## <a name="ambient-video-player-module"></a>氛围视频播放器模块

氛围视频播放器模块支持信息性短视频。 其应该用于不超过五秒钟的视频。 这种播放器支持有限视频播放功能，如播放和暂停。

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>电子商务中的氛围视频播放器模块示例

- 主页中重点介绍新产品的信息性短视频
- 产品详细信息页中重点介绍产品特色的信息性短视频

### <a name="ambient-video-player-module-properties"></a>氛围视频播放器模块属性

| 属性名称     | 值                 | 说明 |
|-------------------|-----------------------|-------------|
| 自动播放          | **True** 或 **False** | 如果此值设置为 **True**，将自动播放视频。 |
| 静音              | **True** 或 **False** | 如果此值设置为 **True**，将静音。 对于此播放器，默认值为 **True**。 在 Google Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。 |
| 循环              | **True** 或 **False** | 如果此值设置为 **True**，将循环重复播放视频。 |
| 媒体             |  视频文件路径和名称 | 视频播放器播放的视频文件。 |
| 播放控制 | **True** 或 **False** | 如果此值设置为 **True**，视频中将显示播放/暂停按钮。 如果此值设置为 **False**，将不显示播放/暂停按钮，当用户仍然可以使用键盘暂停和恢复播放视频。 |

## <a name="video-player-module"></a>视频播放器模块

可在电子商务站点中使用视频播放器模块展示视频。 它支持所有播放功能，如播放、暂停、全屏模式和隐藏式字幕。 视频播放器模块还支持自定义隐藏式字幕以满足 Microsoft 的辅助功能标准。 例如，可自定义字体大小和背景色。

### <a name="examples-of-video-player-modules-in-e-commerce"></a>电子商务中的视频播放器模块示例

- 产品详细信息页或市场营销页上的说明性视频
- 任何市场营销页上的促销视频或有关政策的视频
- 产品详细信息页或市场营销页上重点介绍产品特色的市场营销视频

### <a name="video-player-module-properties"></a>视频播放器模块属性

| 属性名称         | 值                               | 说明 |
|-----------------------|-------------------------------------|-------------|
| 自动播放             | **True** 或 **False**               | 如果此值设置为 **True**，将自动播放视频。 |
| 静音                  | **True** 或 **False**               | 如果此值设置为 **True**，将静音。 对于此播放器，默认值为 **False**。 在 Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。 |
| 循环                  | **True** 或 **False**               | 如果此值设置为 **True**，将循环重复播放视频。 |
| 媒体                 | 视频文件路径和名称 | 视频播放器中播放的视频文件。 |
| 播放控制     | **True** 或 **False**               | 如果此值设置为 **True**，视频中将显示播放/暂停按钮。 如果此值设置为 **False**，将不显示播放/暂停按钮，当用户仍然可以使用键盘暂停和恢复播放视频。 |
| 全屏播放       | **True** 或 **False**               | 如果此值设置为 **True**，将以全屏模式播放视频。 |
| 控件              | **True** 或 **False**               | 如果此值设置为 **True**，将显示所有控件。 这些控件包括播放和暂停按钮、进度指示器和隐藏式字幕。 |
| 隐藏海报框架     | **True** 或 **False**               | 视频可具有海报框架。 如果此属性的值设置为 **True**，将隐藏海报框架。 |
| 蒙板级别            | 从 **0** 到 **100** 的数字 | 为风格而向视频应用的蒙板。 |
| 全屏图标样式 | **正方形**或**箭头**             | 视频播放器中显示的全屏图标的样式。 |

## <a name="add-a-video-player-module-to-a-page"></a>向页面添加视频播放器模块

若要向新页面添加视频播放器模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**视频播放器模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个容器模块。
1. 在容器模块中，添加视频播放器模块和氛围视频播放器模块。
1. 签入模板，然后发布。
1. 使用您刚才创建的视频播放器模板创建一个名称为**视频播放器页**的页面。
1. 在新页的**主**插槽中，添加一个氛围视频播放器模块。
1. 在氛围视频播放器模块的设置中，转到**媒体**，然后上传一个视频文件。 可以根据需要更改**自动播放**、**循环**等属性。
1. 保存并预览页面。
1. 在新页的**主**插槽中，添加一个视频播放器模块。
1. 在视频播放器模块的设置中，转到**媒体**，然后上传一个视频文件。
1. 保存并预览页面。 应该可以在页面中看到这两个视频模块。 可以更改更多属性以自定义各模块的行为。
1. 签入页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[预警模块](add-alert.md)

[传送模块](add-carousel.md)

[内容丰富块模块](add-content-rich-block.md)

[内容放置模块](add-content-placement-modules.md)

[特色模块](add-feature-module.md)

[主图模块](add-hero-module.md)
