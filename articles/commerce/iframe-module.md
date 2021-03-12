---
title: iframe 模块
description: 此主题介绍 iframe 模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993361"
---
# <a name="iframe-module"></a>iframe 模块

[!include [banner](includes/banner.md)]

此主题介绍 iframe 模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

iframe 模块提供在站点上托管外部内容的 iframe（内联框架）。 例如，它可以用于在任何站点页面上托管 YouTube 视频或 PDF 文件查看器。 

iframe 模块需要目标 URL。 然后，它将目标页面的内容托管在 HTML **iframe** 元素内。 根据站点的内容安全策略 (CSP) 指令，外部 URL 必须在允许列表上。 对于 iframe 内容，应使用 **frame-ancestor** 指令允许 URL。 有关详细信息，请参阅[管理内容安全策略 (CSP)](manage-csp.md)。

> [!NOTE]
> 此 iFrame 模块在 Dynamics 365 Commerce 10.0.13 版本中提供。

下图显示了 iframe 模块的示例，这些模块在站点页面上展示外部视频。

![展示外部视频的 iframe 模块示例](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>iframe 模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 标题 | 文本 | 模块的标题。 |
| 目标 URL | URL | 在模块中托管的 URL。 |
| 高度 | 数字或百分比 | 模块的高度，以像素或百分比表示。 例如，值 **100** 将被视为像素数，值 **100%** 将被视为百分比。 |
| Aria 标签 | 文本 | 可以出于可访问性目的定义可访问丰富 Internet 应用程序 (ARIA) 标签。 |

## <a name="add-an-iframe-module-to-a-page"></a>向页面添加 iframe 模块

要将 iframe 模块添加到页面上以显示外部视频，请按照以下步骤操作。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **市场营销模板**，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择 **市场营销模板** 模板。 在 **页面名称** 下，输入 **市场营销页面**，然后选择 **确定**。
1. 在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在模块的属性窗格中，将 **宽度** 值设置为 **填充容器**。
1. 在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **iframe** 模块，然后选择 **确定**。
1. 在模块的属性窗格中，将 **目标 URL** 值设置为视频的外部 URL。
1. 根据您的要求设置其他属性，如 **标题** 和 **高度**。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。
1. 转到您的站点上的市场营销页面。 您应该会看到视频已在 iframe 模块中呈现。
 
## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[管理内容安全策略 (CSP)](manage-csp.md)
