---
title: 站点选取器模块
description: 本文介绍了站点选取器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: efd58206d88618aedb6b574afb47da1e9e578ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276740"
---
# <a name="site-picker-module"></a>站点选取器模块

[!include [banner](includes/banner.md)]

本文介绍了站点选取器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。

当企业跨市场、地区和区域具有不同的站点时，站点用户需要通过一种简单的方法在站点之间进行切换并选择他们喜欢的购物站点。 为了适应这种情况，站点选取器模块使用户能够跨多个站点浏览。 当您的电子商务站点实施了[地理检测和重定向](geo-detection-redirection.md)时，也建议使用站点选取器，让客户可以使用[国家/地区选取器](country-region-picker-module.md)模块替代他们指定的站点首选项。 

站点选取器模块必须配置有站点用户可以浏览的站点列表（市场、地区或区域）。 下图显示了站点页面标题中具有的站点选取器模块示例。

![站点页面标题中的站点选取器模块的示例。](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>站点选取器模块属性

| 属性名称 | 值                 | Description |
|---------------|-----------------------|-------------|
| 标题       | 文本                  | 模块的标题。 |
| 站点选项  | 名称、图像、URL      | 此属性指定名称、指向站点主页的链接以及为模块中包含的每个站点显示的可选图像。 该图像可以是旗帜，也可以是市场、地区或区域的某种表示形式。 |

## <a name="add-a-site-picker-module-to-a-page"></a>向页面添加站点选取器模块

站点选取器模块可以添加到 [标题模块](author-header-module.md)的 **站点选取器** 插槽中。 添加站点选取器模块后，您可以定义模块标题和站点选项。 通常，标题模块包含在可以跨站点的电子商务页面共享的标题片段中。 

要将站点选择器模块添加到标头模块，请执行以下步骤。

1. 在标题片段标题模块的 **站点选取器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，添加 **站点选取器** 模块，然后选择 **确定**。
1. 在 **站点选取器** 属性窗格中，选择 **添加站点选项** 列表。 此时会显示可编辑的 **站点选项列表** 选项。
1. 选择 **站点选项列表**。 此时会显示 **站点选项列表** 对话框。
1. 在 **站点名称** 下面，输入将在站点选取器下拉列表中显示的站点名称文本。
1. 在 **站点重定向 URL** 下，选择 **添加链接**。 将显示 **添加链接** 弹出窗格。
1. 在 **添加链接** 弹出窗格中，选择 **自定义页面**，然后选择 **下一步**。
1. 从站点 URL 列表中，选择在将渠道添加到站点（例如 `www.adventure-works.com/fr-ca`）时创建的路径的 URL，然后选择 **应用**。
1. 选择 **确定**。
1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布** 发布此页面。

在以下示例中，站点选取器模块已被添加到标题模块的 **站点选取器** 插槽中，该模块包含在名为 **HeaderContainer** 的标题片段中。

![标题片段中的站点选取器模块的示例。](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[标题模块](author-header-module.md)

[痕迹导航模块](add-breadcrumb.md)

[导航菜单模块](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
