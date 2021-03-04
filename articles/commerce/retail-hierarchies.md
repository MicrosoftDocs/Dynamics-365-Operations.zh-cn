---
title: Commerce 层次结构
description: 本文介绍 Dynamics 365 Commerce 中的层次结构。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410579"
---
# <a name="commerce-hierarchies"></a>Commerce 层次结构

[!include [banner](includes/banner.md)]

本文介绍 Dynamics 365 Commerce 中的层次结构。

您可以创建类别层次结构来组织通过渠道销售的产品。 您可以使用产品层次结构来对产品进行分类或分组。 然后，可以使用这些产品来创建产品分类和客户会员计划。 您还可以分配产品特性和属性，分配定价结构，将产品包括在产品促销中，以及将产品用于报告。 您可以创建一个类别层次结构以表示组织中的所有产品和类别，然后为多个目的使用该类别层次结构。 或者，您可以为特殊用途创建多个类别层次结构，例如产品促销。 在创建产品层次结构时，必须分配类别层次结构类型以标识类别层次结构的用途。 例如，仅当您在线或在销售点 (POS) 按类别浏览产品时，分配了 **商业导航层次结构** 类型的产品层次结构才会被引用。

## <a name="hierarchy-types"></a>层次结构类型

下表列出了可用的类别层次结构的类型以及每个类型的一般用途。

| 类别层次结构类型       | 目的 |
|-------------------------------|---------|
| 产品层次结构      | 使用此层次结构类型定义您的组织的整个产品层次结构。 您可以为促销活动，定价和促销、报告和分类计划使用此层次结构类型。 只有一个产品层次结构可以分配此层次结构类型。 |
| 补充层次结构 | 为您要创建的任何附加类别层次结构使用此层次结构类型。 例如，在春天，有游泳衣的促销。 因此，您可以在单独的类别层次结构包括您的游泳衣产品并应用促销价到不同产品类别。 |
| 导航层次结构   | 使用此层次结构类型可将产品分组并组织到类别，以便在线或在 POS 中浏览产品。 |

通过使用类别层次结构组织产品，可以在类别级别设置和维护产品属性和特性。 这些特性和属性包括产品维度和 POS 设置。 自动分配给类别的所有产品继承您定义的属性和属性。 您可以在所选类别的多个产品中同时复制所有产品的属性设置。


[!INCLUDE[footer-include](../includes/footer-banner.md)]