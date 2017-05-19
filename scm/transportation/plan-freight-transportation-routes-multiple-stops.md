---
title: "计划具有多个停止点的货运运输路线"
description: "本文介绍用于在 Microsoft Dynamics AX 中计划运输路线的各种元素。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a59667014b7f6a8cfbd27463c33cefd5460ecfbc
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>计划具有多个停止点的货运运输路线

[!include[banner](../includes/banner.md)]


本文介绍用于在 Microsoft Dynamics AX 中计划运输路线的各种元素。

可以使用路线计划和路线指南计划具有多个停止点的复杂交通路线。 如果将定期使用同一个路线，您可以设置计划路线。

## <a name="route-plans"></a>路线计划
路线计划包含提供有关在路线中访问的停止点和用于每个段的运营商的信息。 必须在路线上将停止点定义为枢纽。 枢纽可以是供应商、仓库、客户或甚至只是一个再装货位置（您可在其中更改承运人）。 对于每个段，您可以定义各种费用的“即期费率”。 下面举了一些示例加以说明：

-   往返于给定段的费用
-   领取货物的费用
-   邮寄货物的费用

每个路线计划必须与路线指南关联。

## <a name="route-guides"></a>路线指南
路线指南定义将负荷与特定路线计划匹配的条件。 例如，您可以指定起始枢纽和目标枢纽，容器体积或重量限制，以及配送承运人、服务或组。 路线指南在**费率路线工作台**页面提供，在此页面上，负荷可以手动或自动与路线匹配。 如果路线指南针对计划路线，它也在**装载计划工作台**页提供。

## <a name="scheduled-routes"></a>计划的路线
计划路线是具有装运日期计划的预定义路线计划。 计划路线和非计划路线在负荷分配的方式方面不同。 如果通过使用费率路线工作台分配非计划路线，则仅负荷和路线指南进行验证。 如果分配计划路线，还考虑订单和枢纽的日期和地址，以及路线计划的日期。 您不必使用费率路线工作台页面手动将负荷分配到计划路线。 相反，可以使用装载计划工作台建议基于给定计划路线的销售订单的客户地址和交货日期构建。 对于计划路线，路线计划将具有固定的起始和目标枢纽。 通常情况下，装运承运人和服务对所有段将是相同的，但它们可以有区别。 目标枢纽使用在路线访问的客户的邮政编码创建。 可以为一个路线计划定义几种路线计划。 路线计划必须与路线指南关联。 不过，对于计划路线，计划可只与一个路线指南关联。 路线计划只能用于在**路线计划**页创建实际路线。 在装载计划工作台建议负荷时，可以使用默认的负荷模板。

## <a name="load-building-workbench"></a>装载计划工作台
装载计划工作台使用销售订单的客户地址和交货日期以及可用的计划路线建议负荷。 默认情况下，在工作台上输入路线的值。 但是，您可以选择早于路线上的“起始”日期的“起始”日期。 当建议负荷时，将检查所有未结销售订单的交货地址和交货日期。 如果交货地址的邮政编码与路线计划中的枢纽邮政编码匹配，且如果交货日期是在条件中选择的范围内，将为负荷建议销售订单。 此外还考虑负荷模板的产能。 一次只建议一个负荷。 如果您有不包含的销售订单，您可能必须使用不同的负荷模板（例如，更大的卡车或集装箱的负荷模板），或者计划额外交货。




