---
title: 痕迹导航模块
description: 本主题介绍痕迹导航模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec9f5c72b03d9fd76055369e24491db5c7633cdf
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517152"
---
# <a name="breadcrumb-module"></a>痕迹导航模块

[!include [banner](includes/banner.md)]

本主题介绍痕迹导航模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

痕迹导航模块用于在站点页面上提供辅助导航。 它们通常显示在页面顶部的标题下方。 痕迹导航模块可以添加到任何页面，但它们最常用于产品详细信息页 (PDP)，来显示产品类别层次结构并提供在站点上快速四处移动的方法。 当用户从搜索或列表页打开 PDP 时，痕迹导航模块还可以用于显示“返回到结果”链接。 这样，用户可以快速返回到筛选后的列表页以继续购物。

在具有产品类别上下文的页面（如 PDP 和类别页面）上，痕迹导航模块显示类别层次结构。 在没有类别上下文的页面上，痕迹导航模块默认显示 **&lt;站点根&gt; / &lt;当前页面&gt;**。 痕迹导航模块还可以在其他类型的站点页面上手动配置，以显示指向站点上特定页面的链接。

> [!NOTE]
> 此痕迹导航模块在 Dynamics 365 Commerce 10.0.12 版本中提供。

下图显示了痕迹导航模块的示例，该模块显示 PDP 上的类别层次结构。

![痕迹导航模块的示例](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>痕迹导航模块设置

痕迹导航模块依赖于 **PDP 上的痕迹导航显示类型** 设置，此设置在站点构建器中的 **站点设置 \> 扩展** 中定义。 此设置有三个可能的值：

- **显示类别层次结构** – 选择此值时，痕迹导航模块将显示在 PDP 上查看的产品的完整类别层次结构。
- **显示返回到结果**– 选择此值时，如果用户从允许“返回到结果”链接的模块打开的 PDP，痕迹导航模块将在 PDP 上显示“返回到结果”链接。 当用户从类别、搜索、列表和建议列表页面导航时，此功能可用。 为了支持此功能，产品集合和搜索结果模块具有一个名为 **允许在 PDP 上返回到结果** 的属性。 此属性使您可以灵活地定义哪些模块应该在 PDP 上支持“返回到结果”链接功能。 例如，当为痕迹导航模块的 **PDP 上的痕迹导航显示类型** 设置选择了 **显示返回到结果**，并为搜索页面搜索结果模块选择了 **允许在 PDP 上返回到结果** 时，当用户从搜索页面导航到 PDP 时，将显示“返回到结果”链接。
- **显示类别层次结构和返回到结果**– 此值是前两个值的组合。 选择此值时，痕迹导航模块将在 PDP 上显示完整类别层次结构和“返回到结果”链接（如果已配置）。

> [!IMPORTANT]
> 这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

## <a name="breadcrumb-module-properties"></a>痕迹导航模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 根 | 文本或链接| 此可选属性为痕迹导航站点根指定链接文本和链接目标。 如果未配置此属性，将不会定义根。 |
| 痕迹导航链接 | 链接 | 此可选属性在需要链接时为手动配置的痕迹导航指定链接。 链接按列出的顺序显示。 |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>向新页面添加痕迹导航模块

若要向 PDP 添加痕迹导航模块和设置必需的属性，请执行以下步骤。

1. 转到 **站点设置 \> 扩展**，然后针对 **PDP 上的痕迹导航显示类型** 设置，选择 **显示类别层次结构**。
1. 转到 **模板**，选择 PDP 模板。
1. 在包含购买框模块的 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，打开使用 PDP 模板的 PDP。 如果 PDP 尚不存在，请创建一个。
1. 在包含购买框模块的 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。
1. 在 **痕迹导航** 插槽的属性窗格中，在 **根** 下，选择 **链接文本**。
1. 在 **链接文本** 对话框中，输入 **主页**，然后在 **链接目标** 下，选择 **添加链接**。
1. 在 **添加链接** 对话框中，选择痕迹导航根的链接，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[导航菜单模块](nav-menu-module.md)

[站点选择器模块](site-selector.md)

[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)

[产品集合模块](product-collection-module-overview.md)

[购买框模块](add-buy-box.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)
