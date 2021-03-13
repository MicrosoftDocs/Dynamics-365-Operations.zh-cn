---
title: 混合模式计划 - 合并不同的流程和精益采购
description: 文主题提供有关混合模式计划的信息。
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a074c35f64ce68fe24e501d7cb0e5e64f349c2a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011064"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>混合模式计划 - 合并不同的流程和精益采购

[!include [banner](../includes/banner.md)]

文主题提供有关混合模式计划的信息。 在混合模式计划中，您可以基于物料流来模拟供应链。 Dynamics 365 Supply Chain Management 确保物料流遵循您的模型，不论您选择的是哪种供应策略（看板、生产订单、采购订单、批次订单或转移单）。 

无论产品结构如何，您都可以选择产品供应的总体策略。  

例如，您可以在装配中实施看板控制，以便按生产订单、看板、转移、批次订单或适合供应链特性的任意组合来为装配区域采购物料，但您仍具有对多个供应的完全可见性。 此能力可实现优化的供应链流程并提高对供应链的可见性。  

主计划编制中使用的供应策略的粒度取决于作为覆盖范围维度启用的存储维度。 要启用主计划编制以控制不同类型的位置的补货和供应（例如，通过分离不同的生产单位的生产车间，或通过分离不同类型的物料和成品仓库），建议您将站点和仓库启用为覆盖范围维度。 或者，可以将仓库作为覆盖范围维度忽略。 在此情况下，当您使用高级仓库管理时，仓库内的所有转移将由仓库工作控制，而仓库间的所有转移可由取料看板控制。

## <a name="supply-policies"></a>供应策略
混合模式计划可控制产品的供应方式（基于供应）以及针对派生的需求（物料清单 \[BOM\] 中的物料消耗量）的发货方式。 系统将基于订单类型自动采购物料以满足需求。  

可在产品级别或以任何支持需求的粒度定义供应策略。 您在 **默认订单设置** 页面上定义供应策略的粒度。  

供应策略可按产品、物料维度（配置、颜色和大小）、站点和仓库控制。 在 **物料覆盖范围** 页面上进行此设置。  

默认订单类型控制主计划生成的订单。  

不管供应链的建模方式如何，Supply Chain Management 都支持供应策略的组合。 您可以具有从看板采购的生产订单。 或者，您可以具有需要按转移或看板供应的产品的批次订单。  

Supply Chain Management 确保物料流遵循该模型。  

在定义供应策略后，将在运行时动态分配物料领取仓库。  

通常，不会为将来日期创建看板，因为看板的生命周期短。 要保持对供应链的完全可见性，我们已引入“计划看板”这个新的计划概念，用于计算派生的需求并帮助确保基于在创建实际看板时使用的相同逻辑来满足需求。  

为所有其他供应策略类型提供了相同的逻辑。 因此，在批准生产和供应后，将基于应与实际订单一起运行的相同逻辑进行长期物料计划。

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>跨供应策略的物料分配 - 物料清单中的资源消耗量
资源消耗量是一项重要功能。 利用资源消耗量，可基于供应策略（订单类型）动态选择物料领取仓库，并可更轻松地维护基础数据。  

资源消耗量要求基于产品的供应方式分配物料领取仓库。 换句话说，在运行时，系统将查找应用于制造的资源。 随后，系统将基于这些资源查找领料仓库。  

对于与供应策略无关的工作，如果供应发生更改，您无需更改物料清单上的信息。 对于临时更改，Supply Chain Management 可确保从正确的仓库领取物料。

## <a name="process-manufacturing--the-production-type"></a>流程制造 – 生产类型
对于混合模式中的完整灵活性，建议您对所有产品使用生产类型 BOM。 随后，您可以使用生产订单、看板、转移单或采购订单来供应产品。 对于流程制造，您必须使用以下生产类型：**配方**、**联产品**、**副产品** 或 **计划物料**。 看板和生产订单不能用于这些生产类型。



