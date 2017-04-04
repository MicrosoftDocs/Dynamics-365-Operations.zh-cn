---
title: "混合模式的计划-合并不同，流程和精瘦的来源添加"
description: "文本提供有关混合模式计划的信息。 在混合模式计划中，您可以基于物料流来模拟供应链。 工序的 Microsoft Dynamics 365 确保物料过程应遵循您的模型，而与所选供应策略 (看板、采购订单、生产订单、批次订单或转移单)。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>混合模式的计划-合并不同，流程和精瘦的来源添加

文本提供有关混合模式计划的信息。 在混合模式计划中，您可以基于物料流来模拟供应链。 工序的 Microsoft Dynamics 365 确保物料过程应遵循您的模型，而与所选供应策略 (看板、采购订单、生产订单、批次订单或转移单)。 

无论产品结构如何，您都可以选择产品供应的总体策略。  

例如，您可以在装配中实施看板控制，以便按生产订单、看板、转移、批次订单或适合供应链特性的任意组合来为装配区域采购物料，但您仍具有对多个供应的完全可见性。 此能力可实现优化的供应链流程并提高对供应链的可见性。  

主计划编制中使用的供应策略的粒度取决于作为覆盖范围维度启用的存储维度。 要启用主计划编制以控制不同类型的位置的补货和供应（例如，通过分离不同的生产单位的生产车间，或通过分离不同类型的物料和成品仓库），建议您将站点和仓库启用为覆盖范围维度。 或者，可以将仓库作为覆盖范围维度忽略。 在此情况下，当您使用高级仓库管理时，仓库内的所有转移将由仓库工作控制，而仓库间的所有转移可由取料看板控制。

## <a name="supply-policies"></a>供应策略
混合模式工序的计划控制如何的 Dynamics 365 供应和产品，按供应，派生的需求的物料消耗量 (根据物料清单 \[物料清单\]如何) 的发货。 系统将基于订单类型自动采购物料以满足需求。  

可在产品级别或以任何支持需求的粒度定义供应策略。 您在**“默认订单设置”**页面上定义供应策略的粒度。  

供应策略可按产品、物料维度（配置、颜色和大小）、站点和仓库控制。 在**“物料覆盖范围”**页面上进行此设置。  

默认订单类型控制主计划生成的订单。  

无论如何将供应链建模，工序 365 Dynamics 的支持您的供应策略的混用。 您可以具有从看板采购的生产订单。 或者，您可以具有需要按转移或看板供应的产品的批次订单。  

工序的 Dynamics 365 确保物料过程应遵循模型。  

在定义供应策略后，将在运行时动态分配物料领取仓库。  

通常，不会为将来日期创建看板，因为看板的生命周期短。 要保持对供应链的完全可见性，我们已引入“计划看板”这个新的计划概念，用于计算派生的需求并帮助确保基于在创建实际看板时使用的相同逻辑来满足需求。  

为所有其他供应策略类型提供了相同的逻辑。 因此，在批准生产和供应后，将基于应与实际订单一起运行的相同逻辑进行长期物料计划。

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>物料分配 crosssupply 策略–物料清单上的消耗量资源
资源消耗量是一个重要功能。 利用资源消耗量，可基于供应策略（订单类型）动态选择物料领取仓库，并可更轻松地维护基础数据。  

资源消耗量要求基于产品的供应方式分配物料领取仓库。 换句话说，在运行时，系统将查找应用于制造的资源。 随后，系统将基于这些资源查找领料仓库。  

对于与供应策略无关的工作，如果供应发生更改，您无需更改物料清单上的信息。 对于临时更改，工序 365 的材料从 Dynamics 确保正确的仓库与来源。

## <a name="process-manufacturing--the-production-type"></a>流程制造 – 生产类型
对于中混合模式的完整的灵活性，我们建议您为所有产品使用生产物料清单类型。 您可以使用看板、生产订单、转移单或采购订单供应产品。 对于流程制造，您必须使用以下生产类型：**“配方”**、**“联产品”**、**“副产品”**或**“计划物料”**。 看板和生产订单不能用于这些生产类型。


