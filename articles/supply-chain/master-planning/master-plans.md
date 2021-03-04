---
title: 主计划概览
description: 使用各种主计划来支持公司的日常运营、模拟要监控的不同计划策略、实现公司策略，例如有关内部绩效或客户满意度的政策。
author: roxanadiaconu
manager: tfehr
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70a5b8f0c7e4857aa2904003b458bf6d02b72064
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423231"
---
# <a name="master-plans-overview"></a>主计划概览

[!include [banner](../includes/banner.md)]

使用各种主计划来支持公司的日常运营、模拟要监控的不同计划策略、实现公司策略，例如有关内部绩效或客户满意度的政策。 

您可以配置 **主计划** 页上的主计划。

有以下两种计划类型：
-   **静态计划** – 主计划计算使用当前数据来生成净需求计划。 在下次运行主计划或手动更改计划之前，此计划一直保持不变。 它是一个运营计划，公司的各类人员（例如采购人员或生产规划人员）可将其用作决策基础，也可使用它来执行日常活动。
-   **动态计划** – 此计划开始时具有主计划所生成的净需求计划。 但是，每当主数据更改时都可以更新该动态计划。 例如在创建新销售订单时。 这样您便可以监控更改的订单网络以及物料可用性，而无需中断其他人正在工作过程中使用的静态计划。

公司可以选择只使用静态计划，或可以同时使用动态计划和动态计划。 此外，还可以将任何主计划配置为反映特定策略或解决某一问题。 示例如下：
-   设置较高的库存水平，以防止缺货。
-   设置较长的安全宽限期，以防范不可靠的供应商。

还可以设置起始动态计划，以便每次运行主计划时都以新需求计划进行更新。 您可以在 **主计划参数** 页上指定这些设置。



<a name="additional-resources"></a>其他资源
--------

[覆盖范围设置](coverage-settings.md)

[主计划编制的分离策略和作业计划](https://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[主计划：使用静态和动态主计划或使用一个计划？](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]