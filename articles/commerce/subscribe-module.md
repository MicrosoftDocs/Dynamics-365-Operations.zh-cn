---
title: 订阅模块
description: 本文介绍订阅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 23b74f5853ffb7f191ea7ee3da0d3238db339d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852685"
---
# <a name="subscribe-module"></a>订阅模块

[!include [banner](includes/banner.md)]

本文介绍订阅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

订阅模块可用于站点页面以捕获有关新闻稿或促销的客户信息。

下图显示了 Adventure Works 站点页面的页脚中订阅模块的示例。

![Adventure Works 站点页面的页脚中订阅模块的示例](./media/Subscribe.PNG)

> [!IMPORTANT]
> - 订阅模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始在 Commerce 模块库中提供。
> - 订阅模块在 Adventure Works 主题中展示。
> - 订阅模块需要数据操作扩展来使用一些市场营销电子邮件提供商，以便可以在捕获客户信息后发送新闻稿或促销电子邮件。

## <a name="subscribe-module-properties"></a>订阅模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题       | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 订阅模块的文本标题，例如 **订阅新闻稿** 或 **注册享受 10% 的折扣**。 |
| 段落     | 段落文本 | 订阅模块支持富文本格式的段落文本，以为标题中的调用操作提供额外的详细信息。 |

## <a name="add-a-subscribe-module-to-a-new-page"></a>将订阅模块添加到新页面

若要将订阅列表模块添加到新页面并在 Commerce 站点构建器中设置必需的属性，请按照以下步骤操作。

1. 转到 **模板**，打开站点主页的市场营销模板（或创建新的市场营销模板）。
1. 在默认页的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **订阅** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，然后打开站点的主页（或使用市场营销模板创建新主页）。
1. 在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **订阅** 模块，然后选择 **确定**。
1. 在订阅模块的属性面板中，添加一个标题，如 **订阅**。
1. 添加段落文本，例如 **最新趋势、样式和促销活动。您在名单上吗？订阅并获得最新的热卖！**
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[Adventure Works 主题](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
