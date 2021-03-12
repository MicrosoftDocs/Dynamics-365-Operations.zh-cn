---
title: 选择站点主题
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中设置或更改站点的主题。
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982386"
---
# <a name="select-a-site-theme"></a>选择站点主题

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中设置或更改站点的主题。

## <a name="overview"></a>概览

站点的布局和样式（如字体、大小和颜色）由主题定义，并应用于站点。 主题由公司的开发人员创建和部署。 有关主题概述，请参阅[主题概述](e-commerce-extensibility/theming.md)。 有关如何创建和部署主题的详细信息，请参阅[创建新主题](e-commerce-extensibility/create-theme.md)。

默认情况下，首次创建站点时，使用名称为 **Fabrikam** 的主题。 Commerce 模块库中提供此默认主题。 为站点开发了更多主题之后，可以配置站点，使其改用其中之一。

## <a name="select-the-site-theme"></a>选择站点主题

若要选择应用于站点的主题，请执行以下步骤。

1. 在站点创作环境中，转到您的站点。
1. 转到 **站点管理** \> **扩展性**。
1. 在 **主题** 下，选择下拉菜单中的一个主题。
1. 若要将所选主题应用于您的站点，请选择 **保存并发布**。

> [!NOTE]
> 您在 **扩展性** 页面中选择 **保存并发布** 之后，将立即把您选择的主题发布到您的站点。 若要在应用主题之前在站点中预览该主题，可使用您的开发环境或沙盒环境。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

[主题概览](e-commerce-extensibility/theming.md)

[创建新主题](e-commerce-extensibility/create-theme.md)

