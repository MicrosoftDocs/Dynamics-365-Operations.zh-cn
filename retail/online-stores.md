---
title: "在线商店概述"
description: "本文提供有关 Retail 在线商店以及如何在 Microsoft Dynamics 365 for Retail 中设置它们的信息。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 28ab301dc3aede6b23fb5d87fcb179916e0296e4
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017



---

# <a name="online-store-overview"></a>在线商店概览

[!include[banner](includes/banner.md)]


本文提供有关 Retail 在线商店以及如何在 Microsoft Dynamics 365 for Retail 中设置它们的信息。

Dynamics 365 for Retail 支持多个零售渠道。 这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。 在线商店为零售商提供在线形式，使其客户除零售商店外可从零售商的在线商店采购产品。 如果顾客在在线商店采购产品，产品可以邮寄给他们，或者客户可以在当地零售商店领取产品。 可在 Dynamics 365 for Retail 客户端创建在线商店。 此在线商店随后将发布到与 Dynamics 365 for Retail 集成的第三方在线商店。 第三方在线商店用作在线商店的店面 (UI)，并向您提供客户管理系统 (CMS) 和 UI 功能的选择。 此类型的多个集成可用于 Dynamics 365 for Retail。 您为在线商店定义的属性将控制在线商店的行为。 例如，您在 Dynamics 365 for Retail 中定义导航类别层次结构，并将其分配给在线商店。 将在线商店发布到第三方在线商店后，导航类别层次结构会显示在商店的在线版本中。 购物者然后将导航类别层次结构用于浏览在线商店和搜索产品。 若要创建在线商店，您必须设置允许为商店处理交易记录的组件。 例如，您必须添加分类、应用属性和设置付款方式和装运方法。 还可以定义价格、促销、折扣、贸易协议和特定于在线商店的装运条件。 将在线商店发布到第三方在线商店后，您可以为在线商店创建零售产品目录。 目录中的产品就是在线商店中的产品清单。 顾客从在线商店采购产品时，系统会在客户端更新和同步可用库存。 此外，还会为采购生成销售订单并发送到客户端，以便执行和处理订单。

## <a name="set-up-an-online-store"></a>设置在线商店
若要设置在线商店，必须完成以下任务。

1.  创建在线商店。
2.  将在线商店添加到相应组织层次结构。
3.  添加包括在线商店中可用的产品的分类。
4.  为在线商店分配或创建价格组。
5.  设置在线商店可用的交货方式。
6.  分配在线商店接受的付款方式。
7.  如果您允许顾客在线订购产品，然后在当地商店领取，则将商店定位符组分配给在线商店。
8.  将渠道、产品和销售订单的属性分配给在线商店。 渠道属性适用于整个在线商店，产品属性适用于在线商店中提供的产品，而销售订单属性适用于从在线商店生成的销售订单。
9.  映射特性以定义决定这些特性在在线商店中的行为方式的属性。 例如，属性可以定义为必需或可搜索。
10. 发布在线商店以在您选择的第三方在线商店中生成商店结构。 **重要提示：**在发布在线商店之前，必须为在线商店设置配送地。

## <a name="retail-channel-navigation-hierarchies"></a>零售渠道导航层次结构
必须先定义您用于在线商店的零售渠道导航层次结构，然后才能创建在线商店。 零售渠道导航层次结构表示发布商店后显示在在线商店中的类别导航。 将零售产品目录发布到在线商店时，目录中的产品会映射到零售渠道导航层次结构中的目录。 顾客然后使用该层次结构在在线商店中进行导航。

## <a name="organization-hierarchies"></a>组织层次结构
组织层次结构用于构造零售渠道。 组织层次结构表示构成贵企业组织之间的关系。 设置在线商店时，您可以将这些商店添加到组织层次结构。 然后，商店共享用于分类、补货和报告的数据。 在您创建某一组织层次结构时，将目标分配给它。 目标指示层次结构如何在业务结构中使用。 您可以为商店运营创建一个组织层次结构，并使用层次结构为您的商店分类、补货和报告。 或者，您可以为每个目标创建单独的组织层次结构。 您还可以创建具有相同目标的多个层次结构，然后将单独渠道分配给每个层次结构。 如果您计划将零售产品目录发布到在线商店，则您应该至少将在线商店添加到组织层次结构中以便进行分类。 目录中的产品是从分配给在线商店的分类中选择的。 发布目录时，发布流程会将分配给在线商店的分类的有效日期与目录中包括的产品作比较，以便确定要使哪些产品在在线商店中可用。




