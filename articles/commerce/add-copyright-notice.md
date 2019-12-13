---
title: 添加版权声明
description: 此主题介绍如何向电子商务网站添加版权声明。
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696937"
---
# <a name="add-a-copyright-notice"></a>添加版权声明

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何向电子商务网站添加版权声明。

## <a name="prerequisites"></a>先决条件

必须准备好以下项，才能向站点添加版权声明：

- 一个包含共享页脚片段的模板。
- 一个使用该模板的页面。

## <a name="add-a-copyright-notice"></a>添加版权声明

若要向使用特定模板的每个页面的底部添加版权声明，请执行以下步骤。

1. 转到**片段**，然后选择**新建页面片段**。
1. 在对话框中，选择**页脚**模块，然后为片段命名。 例如，输入 **Footer-Copyright**。
1. 选择**确定**。
1. 在导航窗格中，选择**页脚**旁边的省略号按钮 (**...**)，然后选择**添加模块**。
1. 在对话框中，选择**页脚类别**，然后选择**确定**。
1. 在导航窗格中，选择**页类别脚**旁边的省略号按钮，然后选择**添加模块**。
1. 在对话框中，选择**内容丰富块项**，然后选择**确定**。
1. 在导航窗格中，选择**内容丰富块项**。
1. 在右侧的属性窗格中**段落**字段内，添加版权消息。 例如，输入 **(C) Fabrikam 2019**。
1. 选择**保存**，选择**签入**，然后选择**发布**。
1. 转到**模板**，选择模板，然后选择**签出**。
1. 在**页面大纲**下，展开**正文**，然后展开**默认页面**。
1. 选择**页脚**插槽旁边的省略号按钮，然后选择**添加片段**。
1. 选择前面创建的片段，然后选择**选择**。
1. 签入模板，然后发布。

将在使用所选模板的所有页面的底部自动显示其中包含版权声明的页脚。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

