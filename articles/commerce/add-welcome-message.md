---
title: 添加欢迎消息
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980124"
---
# <a name="add-a-welcome-message"></a>添加欢迎消息


[!include [banner](includes/banner.md)]

此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。

## <a name="overview"></a>概览

电子商务网站中的欢迎消息可告知访问者正在开展的销售、站点新闻或是否提供应季商品。 欢迎消息使用预警模块设置。

应该将预警模块添加到页眉片段的 **错误/信息消息** 插槽中。 可使用预警模块指定显示的文本、文本元素和对齐方式。 还可以用于指定站点访问者是否可忽略消息。

欢迎消息添加到共享页眉片段之后，将在使用以下模板的每个页面中显示：使用这个共享页眉片段的模板。

若要向站点添加欢迎消息，请执行以下步骤。

1. 在 Commerce 站点构建器中，转到您的站点。
1. 选择 **片段**。
1. 选择要将消息添加到的页眉片段。
1. 在大纲树中，展开 **错误/信息消息**。
1. 选择预警模块，然后选择 **确定**。 如果还没有预警模块，首先选择 **错误/信息消息** 旁边的省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在右侧的属性窗格中 **数据** 选项卡上，选择 **添加数据源**，然后选择 **内容**。
1. 在 **输入文本** 字段中，输入欢迎消息的文本。
1. 选择 **保存**，选择 **完成编辑** 签入页眉片段，然后选择 **发布** 进行发布。 

现在将在使用所选页眉片段的每个站点页顶部显示欢迎消息。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加收藏夹图标](add-favicon.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]