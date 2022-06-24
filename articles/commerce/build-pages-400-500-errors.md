---
title: 为 4xx/5xx 状态代码错误生成自定义响应页面
description: 本文介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b56d7a58659205ce4483480fd85d1c91ae52a0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882251"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>为 4xx/5xx 状态代码错误生成自定义响应页面

[!include [banner](includes/banner.md)]

本文介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。

如果请求失败，服务器将发出 HTTP 状态代码错误响应。 如果未找到页面，将捕获并返回 404 状态代码，如果发生了服务器错误，将捕获并返回 500 状态代码。 在 Dynamics 365 Commerce 中，应用程序用户可为这些状态代码错误响应生成自定义状态代码错误响应页，对用户显示。

## <a name="build-a-status-code-error-response-page"></a>生成状态代码错误响应页

若要开始生成状态代码错误响应页，请执行以下步骤。

1. 在首选 Web 浏览器中，登录到 Dynamics 365 Commerce。 
1. 选择要为其生成 4xx/5xx 状态代码错误响应页的站点。

### <a name="build-the-template"></a>生成模板

若要生成状态代码错误响应页的模板，请执行以下步骤。

1. 转到 **模板**。
1. 选择 **新建** 以创建页面模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，为新模板输入名称，然后选择 **确定**。
1. 基于希望状态代码错误响应页要采用的结构生成模板。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。 

### <a name="build-the-status-code-error-response-page"></a>生成状态代码错误响应页

若要生成状态代码错误响应页，请执行以下步骤。

1. 转到 **页面**。
1. 选择 **新建** 创建页面。
1. 在 **选择模板** 对话框中，选择一个模板，然后在 **页面名称** 下，输入状态代码错误响应页面的名称。 保持 **页面 URL** 字段为空。
1. 生成页面。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

> [!NOTE]
> 可为 4xx 和 5xx 状态代码错误创建单独的状态代码错误响应页。 也可以将同一个通用状态代码错误响应页用于两个错误类别。

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>为状态代码错误响应页设置重定向。

若要为状态代码错误响应页设置重定向，请执行以下步骤。

1. 转到 **URL \> 新建 \> 新建别名**，然后选择之前生成的状态代码错误响应页。
1. 在 **别名** 字段中，输入 **default-4xx** 或 **default-5xx**，具体取决于要为其设置重定向的状态代码错误响应页。 必须发布这些别名。 否则，重定向无效。
1. 选择 **确定** 提交链接。

> [!NOTE]
> 如果要为两个错误类别设置一个状态代码错误响应页，请重复此过程将另一个错误类别的别名链接到同一页。

## <a name="additional-resources"></a>其他资源

[使用模板](work-with-templates.md)

[添加新的站点页面](add-new-page.md)

[创建页面 URL](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
