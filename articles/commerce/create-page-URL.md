---
title: 创建页面 URL
description: 此主题介绍有关在站点中创建页面 URL 的基本概念和过程。
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 062a49df93e442dbe402ac9a78244c966958aaa2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965245"
---
# <a name="create-a-page-url"></a>创建页面 URL


[!include [banner](includes/banner.md)]

此主题介绍有关在站点中创建页面 URL 的基本概念和过程。

## <a name="overview"></a>概览

指向站点中的页面的完全或绝对 URL 包含以下独有部分。 例如，URL `https://www.contoso.com/en-us/contactus` 具有以下部分：

- `https://www.contoso.com` – HTTP 协议和站点的域。
- `/en-us` – 站点的语言路径。
- `/contactus` – **联系我们** 页面的相对 URL。 相对 URL 也称为 URL *数据域*。

设置站点时，将建立站点的域和可选语言路径。 可通过站点的设置中的在线商店页面向站点添加更多域和语言路径。

页面的 URL 数据域在站点创作环境中以独立实体的形式存在。 页面 URL 中包含两个部分：表示 URL 数据域的名称，和站点或外部站点上的页面的指针。 也可以将页面 URL 配置为到充当站点或外部站点上另一个页面的重定向。

## <a name="create-a-page-url"></a>创建页面 URL

可通过两种方法创建页面 URL：

- 自动，在创建页面时
- 手动，从 **URL** 页面

### <a name="create-a-page-url-when-you-create-a-page"></a>创建页面时创建页面 URL

如果在创建新页面时在 **URL** 字段中提供名称，将在 **URL** 页面中自动创建指向该页面的页面 URL。 发布 URL 及其指向的页面后，站点用户（即您的客户）可访问与该 URL 关联的页面。

> [!NOTE]
> 如果发布 URL 但不发布其指向的页面，则站点用户在尝试访问该页面时，将遇到 404 错误。 如果发布页面但不发布指向该页面的 URL，则不能使用 URL 访问该页面。

### <a name="manually-create-a-page-url"></a>手动创建页面 URL

创建新页面时，无需指定页面 URL。 如果让 URL 字段保持为空，将在未链接状态下创建页面。 在此情况下，客户不能访问页面，即使已发布了该页面。 若要使该页面可访问，必须手动创建 URL 并将其链接到该页面。

若要为页面手动创建页面 URL，请执行以下步骤。

1. 在 **URL** 页面上，选择 **新建**。
1. 选择要与 URL 关联的站点页面。
1. 输入 URL 数据域，然后选择 **确定**。

此时，URL 处于草稿状态。 必须先发布它，站点用户才能访问关联的页面。

## <a name="update-a-page-url"></a>更新页面 URL

若要更新页面 URL 的目标页，请执行以下步骤。

1. 在 **URL** 页中，选择要更新的 URL。
1. 在右侧的属性窗格中，选择目标页字段旁边的省略号按钮 (**...**)。
1. 在对话框中，选择其他页，然后选择 **确定**。
1. 保存并发布 URL。

## <a name="redirect-a-page-url"></a>重定向页面 URL

有时，您可能希望客户在请求特定 URL 时查看其他页。 在这些情况下，最好，最简单的方法通常是更改页面 URL 指向的页面。 但是，您可能有正当理由使用 HTTP 301 或 3023 重定向将 URL 的请求重定向到其他 URL。

若要将 URL 重定向到其他 URL，请执行以下步骤。

1. 在 **URL** 页中，选择要更新的 URL。
1. 在右侧属性窗格中，选择 **重定向**。
1. 选择重定向的目标：

    - 若要执行站点中的其他页面，请选择 **内部 URL**，选择省略号按钮 (**...**)，然后选择要重定向到的 URL。
    - 若要指向外部站点中的页面，请选择 **外部 URL**，然后输入该页面的完整 URL。 务必包含协议。 例如，输入 `https://domain.com/new/page`。 如果 URL 已经重定向到内部 URL，必须在输入外部 URL 前选择 **清除选择**。

1. 选择重定向类型：

    - **永久重定向 (301)** – 如果知道内容将永久移动，不会恢复为之前的 URL，请选择此选项。 搜索引擎将把重定向 URL 的搜索引擎优化 (SEO) 值分配给将重定向到的 URL，并更新其记录以显示新 URL。 
    - **临时重定向 (302)** – 选择此选项以重定向流量，但不更新搜索引擎。 如果内容很快将恢复为之前的 URL，通常使用此方法。

1. 准备好实施重定向时，保存并发布 URL。

## <a name="additional-resources"></a>其他资源

[自定义站点导航](customize-site-navigation.md)

[添加新的站点页面](add-new-page.md)

[配置域名](configure-your-domain-name.md)

[向站点添加语言](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]