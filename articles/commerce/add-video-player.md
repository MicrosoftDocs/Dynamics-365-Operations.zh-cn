---
title: 视频播放器模块
description: 此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025635"
---
# <a name="video-player-module"></a>视频播放器模块


[!include [banner](includes/banner.md)]

此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

视频播放器模块用于支持视频播放。 只要视频内容已上传到内容管理系统 (CMS) 并在其中可用，就可以将它添加到任何页面。 视频播放器模块支持 .mp4 媒体类型。

## <a name="video-player-module"></a>视频播放器模块

可在电子商务站点中使用视频播放器模块展示视频。 它支持所有播放功能，如播放、暂停、全屏模式、音频描述和隐藏式字幕。 视频播放器模块还支持自定义隐藏式字幕以满足 Microsoft 的辅助功能标准。 例如，可自定义字体大小和背景色。

视频播放器模块还支持辅助音轨。 将视频上载到 CMS 后，还可以上载辅助音轨。 然后，如果用户选择了视频播放器模块，它则可以播放辅助音轨。

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
| 全屏播放       | **True** 或 **False**               | 如果此值设置为 **True**，将以全屏模式播放视频。 |
| 播放暂停触发器    | **True** 或 **False**               | 如果此值设置为 **True**，视频中将显示播放/暂停按钮。 |
| 视频播放器控件 | **True** 或 **False**               | 如果此值设置为 **True**，将显示所有视频播放器控件。 这些控件包括播放和暂停按钮、进度指示器和隐藏式字幕选项。 |
| 隐藏海报图像     | **True** 或 **False**               | 视频可具有海报框架。 如果此属性的值设置为 **True**，将隐藏海报框架。 |
| 蒙板级别            | 从 **0** 到 **100** 的数字 | 为风格而向视频应用的蒙板。 |

## <a name="add-a-video-player-module-to-a-page"></a>向页面添加视频播放器模块

> [!NOTE] 
> 在创建视频播放器模块之前，必须首先将视频上传到媒体库。

若要向新页面添加视频播放器模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**视频播放器模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个容器模块。
1. 在容器模块中，添加视频播放器模块和氛围视频播放器模块。
1. 编辑完模板，然后发布。
1. 使用您创建的视频播放器模板创建一个名称为**视频播放器页**的页面。
1. 在新页的**主**插槽中，添加一个视频播放器模块。
1. 在视频播放器模块的属性窗格中，选择**添加视频**。
1. 在**媒体选择器**对话框中，选择一个视频，然后选择**上载新媒体项目**。
1. 保存并预览页面。 应该可以在页面中看到此视频模块。 可以更改更多属性以自定义模块的行为。
1. 编辑完页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[促销横幅模块](add-alert.md)

[传送模块](add-carousel.md)

[文本块模块](add-content-rich-block.md)

[内容块模块](add-hero-module.md)
