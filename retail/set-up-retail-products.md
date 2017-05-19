---
title: "设置零售产品"
description: "本文介绍了如何在 Microsoft Dynamics 365 for Operations - Retail 中设置零售产品。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4f565bd5563cbcf9079f3220dd855f41889f1d5e
ms.contentlocale: zh-cn
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-retail-products"></a>设置零售产品

[!include[banner](includes/banner.md)]


本文介绍了如何在 Microsoft Dynamics 365 for Operations - Retail 中设置零售产品。

在您可以在您的零售渠道前提供经销产品前，您必须在 Dynamics 365 for Operations AX - Retail 的“零售和商务”中创建并配置产品。 零售在 Dynamics 365 for Operations 中使用产品功能来创建基础产品中的组织产品。 您可以创建产品，定义产品属性和特性和分配到零售类别层次结构。 若要使产品在零售通道中可用和添加到有效的分类，您必须发放到产品中可用的法人。 若要通过使用零售渠道销售产品，请完成以下任务。

1.  定义零售产品层次结构。 通过使用在 Dynamics 365 for Operations 中的类别层次结构功能，您可以定义零售类别层次结构分组和分类您分配给零售渠道的产品。 用户定义和系统特性可以在类别级别定义。 然后，分配给类别的所有产品继承这些特性。 可以定义多个类别层次结构，并且每个产品可以分配给多个层次结构。 不过，在单个层次结构，每个产品只能分配到一个类别。
2.  添加产品和产品变型到基础产品。 产品添加到基础产品表示产品的全局列表。 您可以手动添加产品，一次一个，或可以从供应商导入产品数据。
3.  向法人发布产品。 已发放到的那些法人产品在您的零售渠道可用。 在您第一次定义产品时，您可以定义它在组织级别。 可以选择发放产品到一个或多个法人。 产品然后将可用于跨您的组织的多个零售渠道。 您可以使用此功能创建产品一次，在一个位置添加和更新产品特性和属性，然后跨组织将产品分发到可用的零售渠道。
4.  将产品添加到分类。 分类表示在零售渠道提供产品的集合。 您可以定义一个或多个分类，并且每个产品可以分配给一个或多个分类。 要分配产品到零售渠道，则分配分类到这些零售渠道。 创建分类时，您可以添加尚未发放到法人的产品。 但是，这些产品可以在零售渠道可用前，您必须发放到产品到法人。
5.  将产品添加到导航层次结构。 在产品可在线或在销售点 (POS) 浏览之前，它们必须在零售导航层次结构中进行分类。
6.  将产品添加到目录。 尽管此步骤对 POS 是可选的，在线商店需要产品至少包含在一个目录中。





