---
title: 上传视频
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dd9e710f9a6ea593a0673e7902fadf84ca05cff
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594300"
---
# <a name="upload-videos"></a>上传视频

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。

## <a name="overview"></a>概览

Commerce 站点构建器的媒体库允许上传视频。 应始终上传比特率和分辨率最高的视频版本，因为将把视频自动转换为适合不同视区及其断点的视频。

### <a name="video-information-specified-during-upload"></a>上传期间指定的视频信息

上载视频时，可以指定以下信息。

- **标题、描述、关键字**：视频的元数据。
- **自动生成隐藏式字幕**：指定应该为视频自动生成隐藏式字幕。
- **隐藏式字幕**：指定要使用的隐藏式字幕。
- **常规音频**：指定要使用的常规音轨。
- **缩略图**：指定视频的缩略图。 如果不指定，将自动生成。
- **描述性音频**：指定要使用的描述性音轨。

## <a name="upload-a-video"></a>上传视频

若要在站点构建器中上传视频，请执行以下步骤。

1. 在左侧导航窗格中，选择 **媒体库**。
1. 在命令栏上，选择 **上传 \> 上传媒体项**。
1. 在文件资源管理器中，浏览到要上传的一个或多个视频文件并选中，然后选择 **打开**。
1. 在 **上传媒体项** 对话框中，输入必需的标题和替代文本。
1. 如果需要，输入可选描述和关键字，然后选择类别。 
1. 如果要在上传后立即发布视频，请选中 **上传后发布媒体项** 复选框
1. 选择 **确定**。

如果要同时上传多种资产（例如，图像和视频），则在 **上传媒体项** 对话框中只能指定关键字，是否应该在上传后立即发布文件，以及是否应该为视频自动生成隐藏式字幕。 所有资产将共享相同的关键字。

## <a name="additional-resources"></a>其他资源

[数字资产管理概览](dam-overview.md)

[上传图像](dam-upload-images.md)

[上传文件](dam-upload-files.md)

[裁剪图像](dam-crop-images.md)

[自定义图像焦点](dam-custom-focal-point.md)

[上传和提供静态文件](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]