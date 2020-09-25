---
title: 导航菜单模块
description: 此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761370"
---
# <a name="navigation-menu-module"></a>导航菜单模块

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

导航菜单模块的主要用途是让站点用户可以根据 Dynamics 365 Commerce 总部中定义的渠道导航层次结构浏览产品和站点页面。 导航菜单模块中配置的项显示为站点标题导航。 导航菜单模块还支持链接到电子商务网站上其他页面的静态菜单项。

导航菜单模块可以添加到页面的标题模块。 默认情况下，Fabrikam 主题中的导航菜单显示两个级别。 默认情况下，Starter 主题中的导航菜单显示三个级别。 若要切换为级别数量，主题中需要视图扩展。

下图显示 Fabrikam 站点的导航菜单示例，以及两个类别层次结构级别和一些静态菜单项。
![导航菜单模块的示例](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>导航菜单模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 源                  | **零售**、**手动创作**、**零售和手动创作** | **零售**值允许在导航菜单中显示 Commerce 总部的渠道导航层次结构。 **手动创作**值允许策划静态菜单项。 **零售和手动创作**值允许混合使用两者。 |
| 显示类别图像 | **True** 或 **False**    | 启用后，此属性将在 Commerce 总部中为每个类别定义的导航菜单上显示类别图像。 Commerce 版本 10.0.14 中已添加。 |
| 静态菜单项| 值数组| 将菜单项名称与静态站点页的链接关联的静态菜单项。 可以在其他菜单项下创建菜单项。 默认情况下，静态菜单在根级别显示，并将追加到渠道导航层次结构（如果有）。 |

下图显示 Fabrikam 站点的导航菜单中显示的类别图像的示例。
![导航菜单模块和类别图像的示例](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>向标题模块添加导航菜单模块

有关如何向标题模块添加导航菜单模块的详细信息，请参阅[标题模块](author-header-module.md) 。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[Cookie 合规性](cookie-compliance.md)

[标题模块](author-header-module.md)
