---
title: 将脚本代码添加到站点页面以支持遥测
description: 此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。
author: bicyclingfool
ms.date: 09/29/2020
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
ms.openlocfilehash: e3916b18c797222c300957fb25cabad78c4fcb9744a29d611a81b0bda3e9834d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724596"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>将脚本代码添加到站点页面以支持遥测

[!include [banner](includes/banner.md)]

此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。

如果要了解客户如何与您的站点交互，并作出有助于优化最大转换体验的决策，Web 分析是至关重要的工具。 现在有大量 Web 分析包可帮助您实现这些目标，如 Google Analytics、Clicky、Moz Analytics 和 KISSMetrics。 大多数 Web 分析包都需要您在站点所有页面的 THML 的 **\<head\>** 元素中添加客户端脚本代码。

> [!NOTE]
> 此主题中的说明也适用于 Microsoft Dynamics 365 Commerce 本机不提供的其他自定义客户端功能。

## <a name="create-a-reusable-fragment-for-your-script-code"></a>为脚本代码创建可重复使用的片段

片段使您可以在站点上的所有页面上重复使用内联或外部脚本代码，不管它们使用的模板是什么。

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>为内联脚本代码创建可重复使用的片段

要在站点构建器中为内联脚本代码创建可重复使用的片段，请按照下列步骤操作。

1. 转到 **片段**，然后选择 **新建**.
1. 在 **新建片段** 对话框中，选择 **内联脚本**。
1. 在 **片段名称** 下，输入片段的名称，然后选择 **确定**。
1. 在您创建的片段下，选择 **默认内联脚本** 模块。
1. 在右侧的属性窗格中，在 **内联脚本** 下，输入您的客户端脚本。 然后根据需要配置其他选项。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布**。

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>为外部脚本代码创建可重复使用的片段

要在站点构建器中为外部脚本代码创建可重复使用的片段，请按照下列步骤操作。

1. 转到 **片段**，然后选择 **新建**.
1. 在 **新建片段** 对话框中，选择 **外部脚本**。
1. 在 **片段名称** 下，输入片段的名称，然后选择 **确定**。
1. 在您创建的片段下，选择 **默认外部脚本** 模块。
1. 在右侧的属性窗格中，在 **脚本源** 下，为外部脚本源添加一个外部或相对 URL。 然后根据需要配置其他选项。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布**。

> [!NOTE]
> 如果为您的站点启用了内容安全策略 (CSP)，请确保将所有外部 URL 添加到 Commerce 站点构建器中的 **script-src** CSP 指令。 有关详细信息，请参阅[管理内容安全策略 (CSP)](manage-csp.md)。

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>将包含脚本代码的片段添加到模板

要将包含脚本代码的片段添加到站点构建器中的模板，请按照下列步骤操作。

1. 转到 **模板**，然后打开要将脚本代码添加到的页面的模板。
1. 在左侧窗格中，展开层次结构以打开 **HTML 标头** 插槽。
1. 在 **HTML 标头** 插槽中，选择省略号按钮 (**...**)，然后选择 **添加片段**。
1. 选择为脚本代码创建的片段。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布**。

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>将外部脚本或内联脚本直接添加到模板

如果要将内联脚本或外部脚本直接插入由单个模板控制的一组页面中，则不必先创建片段。

### <a name="add-an-inline-script-directly-to-a-template"></a>将内联脚本直接添加到模板

要将内联脚本直接添加到站点构建器中的模板，请按照下列步骤操作。

1. 转到 **模板**，然后打开要将脚本代码添加到的页面的模板。
1. 在左侧窗格中，展开层次结构以打开 **HTML 标头** 插槽。
1. 在 **HTML 标头** 插槽中，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **内联脚本**。
1. 在右侧的属性窗格中，在 **内联脚本** 下，输入您的客户端脚本。 然后根据需要配置其他选项。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布**。

### <a name="add-an-external-script-directly-to-a-template"></a>将外部脚本直接添加到模板

要将外部脚本直接添加到站点构建器中的模板，请按照下列步骤操作。

1. 转到 **模板**，然后打开要将脚本代码添加到的页面的模板。
1. 在左侧窗格中，展开层次结构以打开 **HTML 标头** 插槽。
1. 在 **HTML 标头** 插槽中，选择省略号按钮 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **外部脚本**。
1. 在右侧的属性窗格中，在 **脚本源** 下，为外部脚本源添加一个外部或相对 URL。 然后根据需要配置其他选项。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布**。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
