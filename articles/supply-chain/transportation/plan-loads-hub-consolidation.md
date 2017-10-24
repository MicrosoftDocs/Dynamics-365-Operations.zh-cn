---
title: "使用中心合并计划装载量"
description: "本文介绍当您从其他仓库将货物交付给同一客户，或将多个供应商的货物接收到同一个仓库时，在枢纽合并装运的功能。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="plan-loads-using-hub-consolidation"></a>使用中心合并计划装载量

[!include[banner](../includes/banner.md)]


本文介绍当您从其他仓库将货物交付给同一客户，或将多个供应商的货物接收到同一个仓库时，在枢纽合并装运的功能。

当您从其他仓库将货物交付给同一客户，或货物从多个供应商交货到同一个仓库时，它对于合并枢纽的装运非常有用。

## <a name="building-loads"></a>构建负荷
您必须先启用**运输管理参数**页的**在途计划**选项，才能够使用枢纽合并。 您还必须创建将发生合并的枢纽。 下图显示枢纽合并的示例。 在这种情况下，不同仓库的销售订单前往同一个客户。 基本负荷基于销售订单以通常的方式创建，通过使用**装载计划工作台**页。 若要在将负荷交付给客户前合并枢纽的两个负荷，在**装载计划工作台**页，在**运输**字段中，选择**枢纽合并**。 在选择每个负荷的正确枢纽时，负荷将枢纽作为“邮寄”目的地。 您还将在**装载计划工作台**页的**供应和需求**部分有两个“运输请求行”。 然后可以为新的负荷添加这两个行。 此新的负荷将具有两个销售订单行，并且还将枢纽作为“取件”地址，以及将客户 A 作为“邮寄”目的地。 然后三个负荷准备好进行评价和路由，像任何其他负荷一样。 您可以选择系统为每个负荷建议的任何装运承运人。 [![集中整合](./media/hubconsol.jpg)](./media/hubconsol.jpg) 您还可以使用相同的方法来合并多个转移单的负荷。 在这种情况下，上图中的客户 A 是一仓库。 或者，您可以合并多个采购订单的负荷，其中将不同供应商的负荷交付到同一仓库。 可以有多个合并枢纽，并可以在多个枢纽合并更多来自不同仓库的负荷。 构建基本负荷并使用枢纽合并选项后，您使用合并的运输请求行构建新的负荷。 然后评价并路由负荷。




