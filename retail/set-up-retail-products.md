---
title: "设置零售产品"
description: "此文章在 Microsoft Dynamics 365 中描述如何设置零售零售的-产品的工序。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>设置零售产品

此文章在 Microsoft Dynamics 365 中描述如何设置零售零售的-产品的工序。

在您可以提供经销的产品在您的零售通道前，您必须创建并配置 Dynamics 中 365 的产品轴的-零售的工序。 Dynamics 中零售 365 使用产品功能。工序可以在基础产品创建组织的产品。 您可以创建产品，定义产品属性和特性和分配到零售类别层次结构。 若要使产品在零售通道中可用和添加到有效的分类，您必须发放到产品中可用的法人。 若要通过使用零售渠道销售产品，请完成以下任务。

1.  定义零售产品层次结构。 通过在 Dynamics 365 的类别层次结构功能，您可以定义工序的零售层次结构组类别和分类您分配到您的零售通道的产品。 用户定义和系统特性可以在类别级别定义。 然后，分配给类别的所有产品继承这些特性。 可以定义多个类别层次结构，并且每个产品可以分配给多个层次结构。 不过，在单个层次结构，每个产品只能分配到一个类别。
2.  添加产品和产品变型到基础产品。 产品添加到基础产品表示产品的全局列表。 您可以手动添加产品，一次一个，或可以从供应商导入产品数据。
3.  向法人发布产品。 已发放到的那些法人产品在您的零售渠道可用。 在您第一次定义产品时，您可以定义它在组织级别。 可以选择发放产品到一个或多个法人。 产品然后将可用于跨您的组织的多个零售渠道。 您可以使用此功能创建产品一次，在一个位置添加和更新产品特性和属性，然后跨组织将产品分发到可用的零售渠道。
4.  将产品添加到分类。 分类表示在零售渠道提供产品的集合。 您可以定义一个或多个分类，并且每个产品可以分配给一个或多个分类。 要分配产品到零售渠道，则分配分类到这些零售渠道。 创建分类时，您可以添加尚未发放到法人的产品。 但是，这些产品可以在零售渠道可用前，您必须发放到产品到法人。
5.  层次结构添加到所在的产品。 在将产品可以浏览的联机或{{关于：in_point_of}}销售点 (POS) 之前，某一零售层次结构中必须进行分类。
6.  该目录的添加产品。 虽然此步骤。POS 是可选的，网络商店要求至少位于一个产品目录中。



