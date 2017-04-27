---
title: "零售层次结构"
description: "本文介绍 Microsoft Dynamics AX 中的零售层次结构。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5fed76e09ef2a64bc2aad2cf6ad7dcfa290acab1
ms.lasthandoff: 03/31/2017


---

# <a name="retail-hierarchies"></a>零售层次结构

[!include[banner](includes/banner.md)]


本文介绍 Microsoft Dynamics AX 中的零售层次结构。

您可以创建零售类别层次结构组织通过零售渠道销售的产品。 您可以使用零售产品层次结构来分类或组产品。 然后，可以使用这些产品来创建产品分类和客户会员计划。 您还可以分配产品特性和属性，分配定价结构，将产品包括在产品促销中，以及将产品用于报告。 您可以在您的组织中创建一个零售类别层次结构表示所有产品和类别，然后为多个目的使用该类别层次结构。 或者，您可以为特殊用途创建多个零售类别层次结构，例如产品促销。 在创建零售产品层次结构时，必须分配类别层次结构类型标识类别层次结构的用途。 例如，当您按在线类别或在销售点 (POS) 浏览产品时，只有分配了**“零售导航层次结构”**类型的产品层次结构会被引用。

## <a name="retail-hierarchy-types"></a>零售层次结构类型
下表列出了可用的零售类别层次结构的类型以及每个类型的一般用途。

| 类别层次结构类型       | 用途                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 零售产品层次结构      | 使用此层次结构类型定义您的组织的整个产品层次结构。 您可以为促销活动，定价和促销、报告和分类计划使用此层次结构类型。 只有一个零售产品层次结构可以分配此层次结构类型。                                       |
| 补充零售层次结构 | 为您要创建的任何附加的零售类别层次结构使用此层次结构类型。 例如，在春天，有游泳衣的促销。 因此，您可以在单独的类别层次结构包括您的游泳衣产品并应用促销价到不同产品类别。 |
| 零售导航层次结构   | 使用此层次结构类型可将产品分组并组织到类别，以便在线或在 POS 中浏览产品。                                                                                                                                                                                       |

可以通过使用零售类别层次结构构成产品，设置和维护产品属性和在类别级别的属性。 这些特性和属性包括产品维度和 POS 设置。 自动分配给类别的所有产品继承您定义的属性和属性。 您可以在所选类别的多个产品中同时复制所有产品的属性设置。




