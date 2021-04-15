---
title: 设置零售产品
description: 本文介绍如何在 Dynamics 365 Commerce 中设置产品。
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5c8ae2f385e2e3a4d08412d9da4ab68d50496211
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795493"
---
# <a name="set-up-retail-products"></a>设置零售产品

[!include [banner](includes/banner.md)]

本文介绍如何在 Dynamics 365 Commerce 中设置产品。

您必须创建和配置产品，然后才能将产品投入商业渠道中转售。 Commerce 在基础产品中创建组织级产品。 您可以创建产品，定义产品属性和特性并将产品分配到商业类别层次结构。 要使产品进入渠道并将其添加到有效的分类，您必须将产品发放给合适的法人。 若要通过使用渠道销售产品，请完成以下任务。

1. **定义产品层次结构。** 通过使用 Commerce 中的类别层次结构功能，您可以定义零售类别层次结构以对您分配给渠道的产品进行分组和分类。 用户定义和系统特性可以在类别级别定义。 然后，分配给类别的所有产品继承这些特性。 可以定义多个类别层次结构，并且每个产品可以分配给多个层次结构。 不过，在单个层次结构，每个产品只能分配到一个类别。
2. **添加产品和产品变型到基础产品。** 产品添加到基础产品表示产品的全局列表。 您可以手动添加产品，一次一个，或可以从供应商导入产品数据。
3. **向法人发布产品。** 只有已发放给法人的产品才能提供给您的渠道。 在您第一次定义产品时，您可以定义它在组织级别。 可以选择发放产品到一个或多个法人。 产品然后将可用于跨您的组织的多个渠道。 您可以使用此功能创建产品一次，在一个位置添加和更新产品特性和属性，然后跨组织将产品分发到可用的渠道。
4. **将产品添加到分类。** 分类表示在渠道提供产品的集合。 您可以定义一个或多个分类，并且每个产品可以分配给一个或多个分类。 要分配产品到渠道，则将分类分配到这些渠道。 创建分类时，您可以添加尚未发放到法人的产品。 但是，这些产品可以在渠道中可用前，您必须发放到产品到法人。
5. **将产品添加到导航层次结构。** 在产品可在线或在销售点 (POS) 浏览之前，它们必须在 Commerce 导航层次结构中进行分类。
6. **将产品添加到目录。** 尽管此步骤对 POS 是可选的，在线商店需要产品至少包含在一个目录中。


[!INCLUDE[footer-include](../includes/footer-banner.md)]