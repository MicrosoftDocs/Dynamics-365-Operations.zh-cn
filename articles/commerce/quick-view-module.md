---
title: 快速查看模块
description: 本文介绍快速查看模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286856"
---
# <a name="quick-view-module"></a>快速查看模块

[!include [banner](includes/banner.md)]

本文介绍快速查看模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

快速查看模块让用户在浏览列表页上的产品时可以快速查看产品信息，并从列表页将一个或多个产品添加到购物车中，而不必转到产品详细信息页 (PDP)。 快速查看模块提供用户作出“添加到购物车”决定所需的产品信息的概览。 它还提供到 PDP 的链接，让用户可以查看其他产品详细信息和购买选项。

快速查看模块由[产品集合](product-collection-module-overview.md)和[搜索结果](search-result-module.md)模块支持。

> [!IMPORTANT]
> 快速查看模块自 Commerce 版本 10.0.17 开始提供。

下图显示了产品列表页上的快速查看模块的示例。

![产品列表页面上的快速查看模块的示例。](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>模块属性

快速查看模块支持与购买框模块相同的功能。 因此，快速查看模块的属性类似于购买框模块的属性。

| 属性 | 值 | 说明 |
|----------------|--------|-------------|
| 标题标记 | **H1**、**H2**、**H3**、**H4**、**H5** 或 **H6** | 此属性定义产品标题的标题标签。 如果快速查看模块位于页面顶部，此属性应设置为 **H1** 以达到可访问性标准。 |
| 允许自定义价格 | **True** 或 **False** | 如果将此属性设置为 **True**，用户可以输入自定义价格。 |
| 最低价格 | 整数 | 仅当 **允许自定义价格** 属性设置为 **True** 时，此属性才适用。 它定义用户可以输入的最低价格（例如，$1）。 |
| 最高价格 | 整数 | 仅当 **允许自定义价格** 属性设置为 **True** 时，此属性才适用。 它定义用户可以输入的最高价格（例如，$1,000）。 |

## <a name="commerce-site-builder-settings"></a>Commerce 站点构建器设置

与购买框模块一样，快速查看模块遵照 **站点设置 \> 扩展 \> 将产品添加到购物车** 的设置。 但是，**导航到购物车页面** 设置将被忽略，因为它与快速查看模块的目的不一致，后者的目的是让用户能够在列表页上浏览多个产品并将其添加到购物车，而无需离开列表页。

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>将快速查看模块添加到产品集合模块

可以将快速查看模块添加到产品集合和搜索结果模块。

要将快速查看模块添加到 Commerce 站点构建器中的产品集合模块，请按照下列步骤操作。

1. 转到 **页面**，然后选择 Fabrikam 站点的主页。
1. 转到主页上的任何 **产品集合** 模块，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **快速查看** 模块，然后选择 **确定**。
1. 在 **快速查看** 模块的属性窗格中，选择 **标题**。 在 **标题** 对话框中，将 **标题级别** 字段设置为 **H2**，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[产品集合模块](product-collection-module-overview.md)

[搜索结果模块](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
