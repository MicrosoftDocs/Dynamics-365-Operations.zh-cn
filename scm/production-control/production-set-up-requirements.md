---
title: "生产设置需求"
description: "本文提供您需要先满足才可以使用生产控制的设置要求的相关信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f34def96ea3b8fd6a8bd015cd120adf87d443285
ms.lasthandoff: 03/31/2017


---

# <a name="production-setup-requirements"></a>生产设置需求

[!include[banner](../includes/banner.md)]


本文提供您需要先满足才可以使用生产控制的设置要求的相关信息。 

生产控制与其他模块中的功能集成。 通过这一相互关联，您可以更改生产订单并确保它们在系统中的所有其他相关流程和计算中自动更新。 以下设置过程按照应完成的顺序列出。

## <a name="required-baseline-setup-in-other-modules"></a>其他模块中要求的基准设置
在使用生产控制前，必须设置其他模块中的信息。 本安装包含以下任务：

-   设置一般公司信息。
-   设置总帐。
-   定义物料组。
-   为物料组设置会计科目。
-   在库存管理中设置库存物料表。
-   在库存管理中创建物料清单 (BOM) 和物料清单版本。

## <a name="required-calendar-and-resource-setup"></a>要求的日历和资源设置
在您使用生产控制前，请打开组织管理，并按以下顺序创建和定义日历和运营资源：

1.  **工作时间模板** – 设置工作时间模板，以便定义可用于生产排产的时间。
2.  **日历** – 设置工作时间日历，以便定义该年度的哪些天可供生产排产。
3.  **资源组** – 在运行计划编制时，设置资源组以分组工序资源，从而让您能够概览所有可用产能。 在设置运营资源前，不必设置资源组。 但是，在您设置生产控制时，我们建议您确定如何对资源分组。
4.  **资源** – 设置运营资源，以便定义用于完成生产流程和计划产能的不同资源。

## <a name="required-production-parameters-setup"></a>要求的生产参数设置
**生产控制参数** – 设置基本生产参数，以便定义该系统如何处理生产订单。 定义如何创建、评估、计划和使用生产订单。 您还可以选择所需反馈类型以及执行成本核算的方式。

## <a name="required-journal-name-identification"></a>所需的日志名称标识
**生产日记帐名称** – 指定用于记录和过帐交易记录的生产日记帐名称。

## <a name="setup-if-you-use-operations"></a>使用工序情况下的设置
工序表示为生产成品而完成的特定活动。 **注意：**您必须知道为生产物料而需要的活动的类型，以及这些活动的顺序和优先级。 您还必须知道涉及哪些资源，以及涉及多少资源。

1.  **工序** – 设置工序以表示生产成品而必须完成的任务。
2.  **关系** – 设置用于确立详细属性的工序关系。 若要定义工序关系，请单击“操作”****页上的“关系”****。

## <a name="setup-if-you-use-routes"></a>使用工艺路线情况下的设置
如果您在使用工艺路线，则必须为您设置的每个生产工艺路线定义工序。 工艺路线表示物料在各工序间流动的路线，从生产流程开始直到结束。

1.  **成本类别** – 设置成本类别，以便定义指定流程和设置时间的每工时成本。
2.  **成本组** – 设置用于创建和维护不同类型的成本计算的成本组。
3.  **工艺路线组** – 设置工艺路线组，以便定义与工艺路线组有关的参数。 您必须首先设置工艺路线组，然后才能创建生产工艺路线。
4.  **工艺路线** – 设置生产工艺路线，并定义默认设置，用于控制排产、成本计算和工艺路线工序价格以及控制进度报告。
5.  **工艺路线** – 设置工艺路线版本，以便实现生产中的物料变化。

## <a name="optional-advanced-settings"></a>可选的高级设置
1.  **生产组** – 设置生产组，以便在生产订单和会计科目之间建立关系。 会计科目用于对订单进行过帐或分组，以便报告。
2.  **生产池** – 创建生产池，以便对生产订单进行分组，使您能够处理紧急的生产订单，或者删除和过帐订单组。
3.  **属性** – 定义属性可以创建可分配到您的资源控制生产订单的特殊特性。 这些属性将与工作时间模板相关联。





