---
title: 添加收藏夹图标
description: 此主题介绍如何向站点添加收藏夹图标。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914558"
---
# <a name="add-a-favicon"></a>添加收藏夹图标

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何向站点添加收藏夹图标。

## <a name="overview"></a>概览

收藏夹图标是在 Web 浏览器标签页上、地址栏中、浏览历史记录中和书签或收藏夹中及其他位置内显示的小图形文件。 建议向站点添加收藏夹图标，因为这样可以展示和强化您的品牌形象，帮助您的站点从客户访问的其他站点中脱颖而出。

虽然可以向站点添加各种大小和文件类型的多个收藏夹图标，此主题介绍如何添加一个收藏夹图标。 但是，可使用相同流程和位置添加更多收藏夹图标。

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>将收藏夹图标上传到站点的资产集中

若要将收藏夹图标上传到站点的资产集中，请执行以下步骤。

1. 转到**资产 \> 上传 \> 上传资产**。
1. 在本地文件系统中找到并选择收藏夹图标。
1. 输入标题，然后选择**确定**。 
1. 在右侧的属性窗格中，复制收藏夹图标的公共 URL。

> [!NOTE]
> 如果不选择**上传后发布资产**选项，必须回到**资产**页，以后再发布该收藏夹图标。

## <a name="create-the-html-for-the-favicon"></a>为收藏夹图标创建 HTML

若要为收藏夹图标创建 HTML，请使用以下 HTML 片段。 对于 **href** 属性，将 **"Public\_URL\_for\_your\_favicon"** 替换为您前面复制的公共 URL。

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>将收藏夹图标的 HTML 添加到页面的 \<head\> 元素中。

若要向站点添加收藏夹图标，请使用向站点页的 **\<head\>** 元素添加任何类型的 HTML 或脚本所用相同过程。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

