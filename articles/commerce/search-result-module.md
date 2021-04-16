---
title: 搜索结果模块
description: 此主题介绍搜索结果模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 01/28/2021
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
ms.openlocfilehash: 3409e9e99329def55b173eb78cf03db4a6764c92
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794107"
---
# <a name="search-results-module"></a>搜索结果模块

[!include [banner](includes/banner.md)]

此主题介绍搜索结果模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

搜索结果模块返回产品搜索结果和产品的适用优化器列表。 Dynamics 365 Commerce 站点上的搜索结果模块可用于呈现以下场景的页面：

- 由用户搜索发起的搜索结果
- 显示一组特定产品的搜索结果，如“购买外观相似的商品”
- 属于某个类别的产品的列表

有关类别和搜索结果页面的详细信息，请参阅[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)。

下图显示了 Fabrikam 站点上某个类别的搜索结果页面的示例。

![Fabrikam 站点上的搜索结果页面的示例](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>搜索结果模块属性

下表列出了搜索结果模块的属性，以及它们的值和描述。

| 属性 | 值 | 说明 |
|----------|--------|-------------|
| 每页的项数 | 整数 | 每页上应显示的项目数。 |
| 允许在 PDP 上后退 | **True** 或 **False** | 如果将此属性设置为 **True**，当用户在搜索结果页面上选择产品时，打开的产品详细信息页 (PDP) 上的痕迹导航将显示“返回到结果”链接。 |
| 扩展精简项 | **所有**、**1**、**2**、**3** 或 **4** | 加载页面时应该展开的排在前面的优化器的数量。 例如，如果此属性设置为 **3**，页面上的前三个优化器将展开。 |
| 隐藏类别层次结构显示 | **True** 或 **False** | 如果将此属性设置为 **True**，页面上显示的类别层次结构将被隐藏。 如果您使用 [痕迹导航模块](add-breadcrumb.md)显示类别层次结构，此属性应设置为 **True**。|
| 在搜索结果中包括产品属性 | **True** 或 **False** | 如果将此属性设置为 **True**，将在搜索结果中返回产品的属性。 虽然这些属性可以在 Commerce 站点上显示，但需要扩展。|
| 显示隶属关系价格 | **True** 或 **False** | 如果将此属性设置为 **True**，登录用户浏览页面时，产品的从属价格将显示在搜索结果中。 |

> [!IMPORTANT]
> 在 Dynamics 365 Commerce 10.0.16 版及更高版本，**显示从属价格** 配置可用于在页面上显示从属价格。

## <a name="supported-modules"></a>支持的模块

搜索结果模块支持[快速查看模块](quick-view-module.md)，让用户可以查看产品信息并将产品从搜索结果页面添加到购物车。

## <a name="add-a-search-results-module-to-a-category-page"></a>将搜索结果模块添加到类别页面

要将搜索结果模块添加到类别页面，请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框中，输入名称 **搜索结果**，然后选择 **确定**。
1. 在 **正文** 插槽中，选择省略号 (...)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。
1. 在 **默认页** 模块的 **主** 插槽中，选择省略号 (...)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在 **容器** 插槽中，选择省略号 (...)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **痕迹导航** 模块，然后选择 **确定**。
1. 在 **痕迹导航** 属性窗格中，为 **最小发生次数** 输入值 **1**。
1. 在 **容器** 插槽中，选择省略号 (...)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **搜索结果** 模块，然后选择 **确定**。
1. 在 **搜索结果** 属性窗格中，为 **最小发生次数** 输入值 **1**，然后为搜索结果模块设置任何其他必需的属性。 通过在模板中设置这些属性，可以确保对特定类别页面进行的任何自定义都会自动包括这些设置。
1. 选择 **完成编辑**，然后选择 **发布** 以发布模板。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择您创建的 **搜索结果** 模板，为 **页面名称** 输入 **类别页**，然后选择 **确定**。 由于所有值都在模板中设置，因此页面已准备好发布。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)

[模块库概览](starter-kit-overview.md)

[快速查看模块](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
