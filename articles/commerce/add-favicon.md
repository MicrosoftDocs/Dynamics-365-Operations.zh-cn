---
title: 添加收藏夹图标
description: 此主题介绍如何向站点添加收藏夹图标。
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797711"
---
# <a name="add-a-favicon"></a>添加收藏夹图标

[!include [banner](includes/banner.md)]

此主题介绍如何向站点添加收藏夹图标。

收藏夹图标是在 Web 浏览器标签页上、地址栏中、浏览历史记录中和书签或收藏夹中及其他位置内显示的小图形文件。 建议向站点添加收藏夹图标，因为这样可以展示和强化您的品牌形象，帮助您的站点从客户访问的其他站点中脱颖而出。

虽然可以向站点添加各种大小和文件类型的多个收藏夹图标，此主题介绍如何添加一个收藏夹图标。 但是，可使用相同流程和位置添加更多收藏夹图标。

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>将收藏夹图标上传到站点的资产集中

若要将收藏夹图标上传到站点的资产集中，请执行以下步骤。

1. 在左侧导航窗格中，选择 **媒体库**。
1. 在命令栏上，选择 **上传 \> 上传媒体项**。
1. 在“文件资源管理器”窗口中，浏览到要上传的收藏夹图标图像文件，选择它，然后选择 **打开**。
1. 在 **上传媒体项** 对话框中，输入必需的标题和替代文本。
1. 如果要在上传后立即发布图像，请选中 **在上传后发布媒体项目** 复选框。

    > [!NOTE]
    > 如果您未选中 **在上传后发布媒体项目** 复选框，则必须返回到 **媒体项目** 页面并稍后手动发布收藏夹图标。

1. 选择 **确定**。
1. 在右侧的属性窗格中，复制收藏夹图标的公共 URL。 您稍后将使用此 URL。

## <a name="create-the-html-for-your-favicon"></a>为您的收藏夹图标创建 HTML

要为收藏夹图标创建 HTML，请使用以下 HTML 字符串。 对于 **href** 属性，请将 **您的\_收藏夹\_图标\_的\_公共 URL** 替换为您先前复制的公共 URL。

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>创建一个包含收藏夹图标元标记的片段

要创建一个包含收藏夹图标元标记的片段，请执行以下步骤。

1. 转到 **片段**，然后选择 **新建**.
1. 在 **新建片段** 对话框中，选择 **元标记** 作为片段所基于的模块。
1. 输入片段名称，然后选择 **确定**。
1. 在片段层次结构树中，选择 **默认元标记** 子项。
1. 在右窗格中的 **元标记** 下，选择 **添加**，然后输入您先前为该收藏夹图标创建的 HTML 字符串。 
1. 选择 **完成编辑**，然后选择 **发布** 以发布片段。

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>将元标记片段添加到页面的 HTML 标头部分

要将元标记片段添加到页面的 HTML **标头** 部分，请执行以下步骤。

1. 转到 **模板**，打开要向其中添加收藏夹图标的页面的模板，然后选择 **编辑**。
1. 在模板层次结构树中，选择 **HTML 标头** 容器右侧的省略号 (**...**) 按钮，然后选择 **添加片段**。
1. 在 **选择片段** 对话框中，选择您之前创建的元标记片段，然后选择 **确定**。
1. 选择 **完成编辑**，然后选择 **发布** 以发布模板。

> [!NOTE]
> 如果您的站点使用多个模板，则必须将元标记片段添加到所有项中。

当您预览的页面基于元标记片段所添加到的模板时，您现在应该会在浏览器选项卡上看到收藏夹图标。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
