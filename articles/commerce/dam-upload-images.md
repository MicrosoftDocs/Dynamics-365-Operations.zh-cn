---
title: 上传图像
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传图像。
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
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096977"
---
# <a name="upload-images"></a>上传图像

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传图像。

## <a name="overview"></a>概览

Commerce 站点构建器的媒体库允许您上传单个图像或使用文件夹批量上传图像。 应始终上传分辨率和质量最高的图像版本，因为图像大小调整组件将针对不同视区及其断点自动优化图像。

### <a name="image-information-specified-during-upload"></a>上传期间指定的图像信息

上载图像时，可以指定以下信息。

- **标题、替代文本、描述、关键字**：图像的元数据。 标题和替代文本是必需值。
- **选择类别**：
    - **无**：用于电子商务故事分享图像。
    - **产品、类别、客户、员工、目录**：用于 Dynamics 365 Commerce 全渠道图像。
- **上传后发布资产**：如果选中此复选框，图像在上传后将立即发布。

> [!NOTE]
> 还将对已分配了类别的图像资产使用该类别作为关键字进行标记，以便帮助搜索特定类别的资产。

### <a name="naming-conventions-for-omni-channel-images"></a>全渠道图像的命名约定 

如果已将媒体库配置为全渠道图像后端，则可使用图像类别指示上传的图像属于哪个类别。 还应遵守一个命名约定以确保其他渠道（如销售点 (POS)）可以正确检索图像。

默认命名约定取决于类别：
- 目录图像应该命名为 **/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**
- 类别图像应该命名为 **/Categories/\{CategoryName\}.png**
- 客户图像应该命名为 **/Customers/\{CustomerNumber\}.jpg**
- 员工图像应该命名为 **/Workers/\{WorkerNumber\}.jpg**
- 产品图像应该命名为 **/Products/\{ProductNumber\}_000_001.png**
    - 001 是图像的序号，可以是 001、002、003、004 或 005
- 产品变型图像应该命名为 **/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**

## <a name="upload-an-image"></a>上传图片

若要在站点构建器中上传图像，请执行以下步骤。

1. 在左侧导航窗格中，选择**媒体库**。
1. 在命令栏上，选择**上传 \> 上传媒体项**。
1. 在文件资源管理器中，浏览到要上传的一个或多个图像文件并选中，然后选择**打开**。
1. 在**上传媒体项**对话框中，输入必需的标题和替代文本。
1. 如果需要，输入可选描述和关键字，然后选择类别。 
1. 如果要在上传后立即发布图像，请选中**上传后发布媒体项**复选框。
1. 选择**确定**。

## <a name="upload-a-folder-of-images"></a>上传图像文件夹

若要在站点构建器中上传图像文件夹，请执行以下步骤。

1. 在左侧导航窗格中，选择**媒体库**。
1. 在命令栏上，选择**上传 \> 上传文件夹**。
1. 在文件资源管理器中，浏览到要上传的文件夹并选中，然后选择**打开**。
1. 如果需要，在**上传媒体项**对话框中，输入可选关键字，然后选择类别。 
1. 如果要在上传后立即发布文件夹中的图像，请选中**上传后发布媒体项**复选框。
1. 选择**确定**。

## <a name="additional-resources"></a>其他资源

[数字资产管理概览](dam-overview.md)

[上传视频](dam-upload-video.md)

[上传文件](dam-upload-files.md)

[裁剪图像](dam-crop-images.md)

[自定义图像焦点](dam-custom-focal-point.md)
