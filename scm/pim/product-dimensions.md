---
title: "产品维度"
description: "有四产品维度 - 颜色、配置、大小和样式。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>产品维度

[!include[banner](../includes/banner.md)]


有四产品维度 - 颜色、配置、大小和样式。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。

产品维度是用于标识产品变型的特性。 您可以使用产品维度的组合来定义产品变型。 必须至少为基础产品定义一个产品维度，以便创建产品变型。
产品变型
----------------

产品变型也称作物料。 该物料是与服务不同的有形产品。 还可以用服务类型定义基础产品。 通过使用“服务”类型，可以指定包括服务的产品变型。 例如，您可以为咨询工作指定基础产品，为高级顾问和初级顾问执行的工作指定产品变型。

## <a name="product-dimensions"></a>产品维度
以下产品维度可用：配置、颜色、尺寸和样式。 产品变型可以基于产品维度值生成。

产品维度值（例如尺寸、颜色和样式）可以在**尺寸**、**颜色**和**样式**页创建，可以从以下位置访问这些页：**产品信息管理** &gt; **设置** &gt; **维度和变型组** &gt; **尺寸/颜色/样式**。 配置维度的产品维度值通常使用产品配置器或基于维度的配置器创建。 产品维度还可以在**产品维度**页中创建和维护，可从以下位置访问该页：
-   单击**产品信息管理** &gt; **产品** &gt; **基础产品**。 在**操作窗格**上单击**产品维度**。
-   单击**产品信息管理** &gt; **产品** &gt; **所有产品和基础产品**。 选择基础产品。 在**操作窗格**上单击**产品维度**。
-   单击**产品信息管理** &gt; **已发布产品**。 选择基础产品。 在**操作窗格**上，单击**产品**。 在**基础产品**组，单击**产品维度**。

为物料可创建的变型数受限于可能的产品维度组合数。
| **提示**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 例如，当您在订单行上使用一个产品时，选择产品维度以确定您要使用的产品变型。 |

## <a name="example"></a>示例
一家公司销售牛仔裤。 物料（即牛仔裤）使用颜色和尺寸产品维度。 销售的牛仔裤有三种不同的颜色和六种不同的尺寸。 颜色：蓝色、黑色、棕色 尺寸：XS、S、M、L、XL、XXL 不是全部三种颜色都提供所有尺寸。 如果所有组合均可用，将得到 18 种不同类型的牛仔裤。 在此示例中，只生产了以下九个产品变型组合。

| 颜色 | 大小 |
|-------|------|
| 蓝色  | XS   |
| 蓝色  | 六    |
| 蓝色  | 一    |
| 黑 | 一    |
| 黑 | L    |
| 黑 | XL   |
| 棕 | L    |
| 棕 | XL   |
| 棕 | XXL  |






