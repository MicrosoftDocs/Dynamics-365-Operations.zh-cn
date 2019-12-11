---
title: 为 4xx/5xx 状态代码错误生成自定义响应页面
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697098"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>为 4xx/5xx 状态代码错误生成自定义响应页面

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。

## <a name="overview"></a>概览

如果请求失败，服务器将发出 HTTP 状态代码错误响应。 如果未找到页面，将捕获并返回 404 状态代码，如果发生了服务器错误，将捕获并返回 500 状态代码。 在 Dynamics 365 Commerce 中，应用程序用户可为这些状态代码错误响应生成自定义状态代码错误响应页，对用户显示。

## <a name="build-a-status-code-error-response-page"></a>生成状态代码错误响应页

若要开始生成状态代码错误响应页，请执行以下步骤。

1. 在首选 Web 浏览器中，登录到 Dynamics 365 Commerce。 
1. 选择要为其生成 4xx/5xx 状态代码错误响应页的站点。

### <a name="build-the-template"></a>生成模板

若要生成状态代码错误响应页的模板，请执行以下步骤。

1. 转到**模板 \> 新建模板**。
1. 为新模板命名。
1. 基于希望状态代码错误响应页要采用的结构生成模板。
1. 签入模板，然后发布。

### <a name="build-the-status-code-error-response-page"></a>生成状态代码错误响应页

若要生成状态代码错误响应页，请执行以下步骤。

1. 转到**页面 \> 新建页面**。
1. 为状态代码错误响应页命名，但**不**设置 **URL** 字段。
1. 生成页面。
1. 签入页面，然后发布。

> [!NOTE]
> 可为 4xx 和 5xx 状态代码错误创建单独的状态代码错误响应页。 也可以将同一个通用状态代码错误响应页用于两个错误类别。

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>为状态代码错误响应页设置重定向。

若要为状态代码错误响应页设置重定向，请执行以下步骤。

1. 转到 **URL \> 新建 \> 新建别名**，然后选择之前生成的状态代码错误响应页。
1. 在**别名**字段中，输入 **default-4xx** 或 **default-5xx**，具体取决于要为其设置重定向的状态代码错误响应页。 必须发布这些别名。 否则，重定向无效。
1. 选择**确定**提交链接。

> [!NOTE]
> 如果要为两个错误类别设置一个状态代码错误响应页，请重复此过程将另一个错误类别的别名链接到同一页。

## <a name="additional-resources"></a>其他资源

[使用模板](work-with-templates.md)

[添加新的站点页面](add-new-page.md)

[创建页面 URL](create-page-url.md)
