---
title: 辅助功能和功能
description: 本主题提供有关 Microsoft Dynamics 365 Commerce 中的辅助功能和功能的信息。
author: BrianShook
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 094ad8d34e13051ce7596be462070ead4cbc4f14
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206647"
---
# <a name="accessibility-features-and-capabilities"></a>辅助功能和功能


[!include [banner](includes/banner.md)]

本主题提供有关 Microsoft Dynamics 365 Commerce 中的辅助功能和功能的信息。

## <a name="overview"></a>概览

辅助功能和功能为所有用户提供访问和执行操作的功能性方法，以便他们可以实现自己的目标。 如此众多的用户可能需要辅助工具来改善听力、视力、移动性或神经多样性。

Dynamics 365 Commerce 中的各种功能可让您建立站点，使其包含辅助功能。 在设计站点时，您应该考虑 [Microsoft 辅助功能中心](https://www.microsoft.com/accessibility)中提到的辅助功能区域。 

本主题介绍使用 Dynamics 365 Commerce 时应考虑的辅助功能的其他一些区域。

## <a name="image-alt-text"></a>图片替代文本

Dynamics 365 Commerce 具有内置的数字资产管理系统，可以跟踪您站点上使用的图像和视频资产。 选择或上载图像时，可以在图像的属性窗格中添加图像字幕、说明和替代文本。

## <a name="video-accessibility"></a>视频辅助功能

Dynamics 365 Commerce 数字资产管理系统支持视频内容的多种辅助功能。 下表列出了一些示例。

| 视频功能               | 说明 |
|-----------------------------|-------------|
| 隐藏式字幕 (CC)      | 可以为视频的音频和音频描述元素显示的文本，以帮助失聪或有听力障碍的用户 |
| 字幕                   | 在屏幕上显示上下文线索或对话框文本的字幕文件 |
| 音频记录           | 从视频资产的音频生成的口头词句的文本记录 |
| 描述性音频           | 描述屏幕上正在发生的内容或上下文的非主要音频通道 |
| 最低年龄限制            | 可以存储观看者观看视频所必须达到的最小年龄的属性（仅元数据） |

### <a name="configure-video-accessibility-elements"></a>配置视频辅助功能元素

在站点的 Commerce **媒体库** 部分，您可以上载包含隐藏式字幕、常规音频和描述性音频的单独文件的视频资产。 上载视频资产时，还可以自动生成隐藏式字幕。

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>在视频资产上载过程中生成或上载隐藏式字幕文件

要在上载视频时自动生成隐藏式字幕文件，请按照以下步骤操作。

- 在 **资产上载** 对话框中，选择 **自动生成隐藏式字幕**。 如果您正在生成隐藏式字幕文件，隐藏式字幕文件的文件选择器在对话框中将不可用。

要在上载视频时手动上载隐藏式字幕文件，请按照以下步骤操作。

- 在 **资产上载** 对话框中，清除 **自动生成隐藏式字幕**。

要上载视频的常规音频或描述性音频文件，请使用 **资产上载** 对话框中的文件选择器。

> [!NOTE]
> 视频资产上载后，还可以添加隐藏式字幕、常规音频和描述性音频资产。 转到 **媒体库**，选择视频资产，然后选择 **编辑** 将其签出。然后，在视频资产的属性窗格中，上载其他资产。

#### <a name="edit-cc-and-audio-transcript-files"></a>编辑 CC 和音频记录文件

CC 和音频记录文件可以直接在创作工具中进行编辑。 可以在编辑过程中播放视频。

若要编辑 CC 和音频记录文件，请按照下列步骤操作。

1. 转到 **媒体库**，然后选择视频资产的文件名。 将出现隐藏式字幕和记录内容编辑器。
1. 选择 **编辑**。
1. 编辑隐藏式字幕或记录文本。
1. 完成后，选择 **保存**，然后选择 **完成编辑**。
1. 准备好发布时，选择 **发布**。

#### <a name="set-the-minimum-age-attribute"></a>设置“最低年龄”属性

**最低年龄** 元数据属性可以与视频资产相关联。

要为视频资产设置 **最低年龄** 属性，请按照以下步骤操作。

1. 转到 **媒体库**，然后选择视频资产。
1. 选择 **编辑**。
1. 在视频资产的属性窗格中，设置 **最低年龄** 属性。

> [!NOTE]
> 属性窗格仅用于设置和存储元数据属性值。 必须创建自定义模块才能使用此属性设置播放控制。

## <a name="additional-resources"></a>其他资源

[窗体、产品和控件中的辅助功能](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft 辅助功能中心](https://www.microsoft.com/accessibility)

[Dynamics 365 辅助功能中心](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[合规性概览](compliance-overview.md)

[Cookie 合规性](cookie-compliance.md)

[添加隐私政策页面](add-privacy-page.md)

[替换与所跟踪内容更改相关联的用户 ID](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]