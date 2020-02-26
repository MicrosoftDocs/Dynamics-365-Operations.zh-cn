---
title: 将脚本代码添加到站点页面以支持遥测
description: 此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001269"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>将脚本代码添加到站点页面以支持遥测


[!include [banner](includes/banner.md)]

此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。

## <a name="overview"></a>概览

如果要了解客户如何与您的站点交互，并作出有助于优化最大转换体验的决策，Web 分析是至关重要的工具。 现在有大量 Web 分析包可帮助您实现这些目标，如 Google Analytics、Clicky、Moz Analytics 和 KISSMetrics。 大多数 Web 分析包都需要您在站点所有页面的 THML 的 **\<head\>** 元素中添加客户端脚本代码。

> [!NOTE]
> 此主题中的说明也适用于 Microsoft Dynamics 365 Commerce 本机不提供的其他自定义客户端功能。

## <a name="create-a-reusable-fragment-for-your-script-code"></a>为脚本代码创建可重复使用的片段

为脚本代码创建片段之后，可以在站点的所有页面中重复使用该片段。

1. 转到**片段 \> 新建页面片段**。
2. 选择**外部脚本**，输入片段的名称，然后选择**确定**。
3. 在片段层次结构中，选择刚才创建的片段的**脚本注入程序**模块子代。
4. 在右侧的属性窗格中，添加您的客户端脚本，然后根据需要设置其他配置选项。

## <a name="add-the-fragment-to-templates"></a>将片段添加到模板

1. 转到**模板**，然后打开要将脚本代码添加到的页面的模板。
2. 在左侧窗格中，展开层次结构以打开 **HTML 标头**插槽。
3. 选择 **HTML 标头**插槽的省略号按钮 (**...**)，然后选择**添加片段**。
4. 选择为脚本代码创建的片段。
5. 保存模板，然后签入。

> [!NOTE]
> 完成后，必须发布片段和主模板。 

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

