---
title: 上载和提供静态文件
description: 此主题介绍如何将静态文件上载到 Microsoft Dynamics 365 Commerce 站点构建器，以及如何创建可用于请求该文件的自定义 URL 和文件名。
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594946"
---
# <a name="upload-and-serve-static-files"></a>上载和提供静态文件

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题介绍如何将静态文件上载到 Microsoft Dynamics 365 Commerce 站点构建器，以及如何创建可用于请求该文件的自定义 URL 和文件名。

有些第三方连接器需要文件从电子商务站点托管和提供。 这些连接器预期文件将由对特定回叫 URL 路径和文件名的请求返回。 因此，此主题说明如何在 Dynamics 365 Commerce 电子商务站点上载和提供具有用户可定义 URL 和文件名的静态文件。

## <a name="create-a-site-url-that-returns-a-static-file"></a>创建返回静态文件的站点 URL

若要在 Commerce 站点构建器中创建返回静态文件的站点 URL，请按照下列步骤操作。

1. 转到您的站点的媒体库，上载应由对您定义的 URL 的请求提供的文件。 如果您已经上载文件，则可以跳过此步骤。
1. 转到您的站点的 **URL**。
1. 选择 **新建 \> 新建 URL**。
1. 在 **新建 URL** 对话框中，选择 **媒体库资产**。
1. 在 **URL 路径** 字段中，输入 URL 路径。 在路径中包括文件名。
1. 选择 **下一步**。 媒体库将打开，显示所有已上载的 **文档** 类型的媒体资产。
1. 选择应为对您在步骤 5 中定义的 URL 的请求提供的文件。
1. 选择 **保存**。

此时，您创建的 URL 处于草稿状态。 在您发布 URL 之前，URL 指向的文件不会返回。 在发布 URL 之前，您可以验证它是否返回正确的数据。

## <a name="validate-and-publish-a-url"></a>验证和发布 URL

要在发布之前验证 URL，请按照下列步骤操作。

1. 转到您的站点的 **URL**，选择要预览的 URL。
2. 在右侧的属性窗格中，在 **编辑** 按钮下，选择正确的 URL 链接。 一个新浏览器窗口将打开，您应会收到 404 错误。
3. 将 **?preview=inprogress** 查询字符串追加到 URL（例如，`https://yoursite.com/callback.html?preview=inprogress`），然后重新加载页面。 您上载到媒体库的文件应在响应中返回。

验证 URL 后，可以将其发布。

1. 转到您的站点的 **URL**，选择 URL。
2. 在命令栏上选择 **发布**。

## <a name="update-the-file-that-a-url-points-to"></a>更新 URL 指向的文件

URL 发布后，您可以对它进行更新，让它指向另一个文件。 或者，您可以更新 URL，让它指向不同的资源类型，如下一节中所述。 例如，您可以将 URL 指向内部页面或重定向。

要更新 URL 指向的文件，请按照下列步骤操作。

1. 转到您的站点的 **URL**，选择要更新的 URL。
1. 在右侧的属性窗格中，选择 **编辑**。
1. 在 **URL 分配** 下，选择 **步骤 2** 框，然后从媒体库中选择一个新文档。
1. 选择 **应用**。

## <a name="update-the-asset-type-that-a-url-points-to"></a>更新 URL 指向的资产类型

您还可以更新 URL，让它指向其他类型的资产（资源），如内部页面或重定向。

要更新 URL 指向的资产类型，请按照下列步骤操作。

1. 转到您的站点的 **URL**，选择要更新的 URL。
1. 在右侧的属性窗格中，选择 **编辑**。
1. 在 **URL 分配** 下，在 **步骤 1** 下，选择其他资产类型。
1. 选择 **步骤 2** 框，然后选择新资产。
1. 选择 **应用**。

## <a name="change-the-url-path"></a>更改 URL 路径

创建 URL 后，它的路径无法更改。 如果必须更改用于提供文件或任何其他类型资源的 URL 路径，必须创建一个新 URL，将其映射到现有文件或其他资源，然后取消发布并删除旧 URL。

若要更改 URL 路径，请执行以下步骤。

1. 要创建新的 URL 并将其映射到现有文件或另一个资源，请按照此主题前面的[创建返回静态文件的站点 URL](#create-a-site-url-that-returns-a-static-file) 一节中的说明操作。
1. 选择新 URL，然后在命令栏上选择 **发布**。 新 URL 将发布。
1. 要取消发布旧 URL，选择它，然后在命令栏上选择 **取消发布**。 现在，您可以根据需要删除旧 URL 了。

## <a name="additional-resources"></a>其他资源

[数字资产管理概览](dam-overview.md)

[上传图像](dam-upload-images.md)

[上传视频](dam-upload-video.md)

[上传图像和视频以外的文件](dam-upload-files.md)

[裁剪图像](dam-crop-images.md)

[自定义图像焦点](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]