---
title: 生产订单生命周期概览
description: 在创建生产订单时，将发起开始生产物料的请求。 生产订单包含与将生产的产品、生产数量和计划完工日期有关的信息。 它还包含要消耗的物料以及要用于生产物料的流程的信息。
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19741"
- intro-internal
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4c3632d644070f064ec70d3dd7c0d480927eafe
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982869"
---
# <a name="production-order-lifecycle-overview"></a>生产订单生命周期概览

[!include [banner](../includes/banner.md)]

在创建生产订单时，将发起开始生产物料的请求。 生产订单包含与将生产的产品、生产数量和计划完工日期有关的信息。 它还包含要消耗的物料以及要用于生产物料的流程的信息。

生产订单在生产生命周期的各个阶段中传递。 在创建一个订单后，会将状态 **已创建** 分配给该订单。 在完成一个订单后，会将状态 **已结束** 分配给该订单。 每个阶段中的参数设置允许用户配置每个步骤。 可以为单个用户或为所有用户指定该设置。

生产物料清单和生产工艺路线是生产订单的主要实体。 它们基于要生产的选定物料和数量复制到生产订单。 在启动生产订单之前，生产物料清单和工艺路线是可以编辑的。

在以下情况下可以创建生产订单：

-   由主规划执行基于物料需求创建。
-   从销售订单行直接创建，或在创建和估计更高级别的生产订单（限定供应）时创建。
-   手动创建。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]