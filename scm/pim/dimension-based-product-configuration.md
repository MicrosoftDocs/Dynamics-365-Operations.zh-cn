---
title: "基于维度的产品配置"
description: "基于维度的产品配置表示从单个基础产品和物料清单创建多个产品变型的简单解决方案。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7fbf69dc217a2f61ec3aeda952ff221491e9385a
ms.lasthandoff: 03/31/2017


---

# <a name="dimension-based-product-configuration"></a>基于维度的产品配置

基于维度的产品配置表示从单个基础产品和物料清单创建多个产品变型的简单解决方案。

基于维度的产品配置有三内置产品配置技术之一。 其他两项技术是预定义的变型和基于约束的配置。 全部三项技术使用基础产品作为起点，并允许用户为一个基础产品创建许多产品变型。

## <a name="key-concepts"></a>重要概念
基于维度的产品配置基于以下重要概念：

-   基础产品
-   配置产品维度
-   配置组
-   物料清单 (BOM)
-   配置流程
-   配置规则

### <a name="product-masters"></a>基础产品

基础产品是所有产品配置流程的起点。 对于基于维度的产品配置，您需要具有此特定配置技术的基础产品和包括配置产品维度的产品维度组。

### <a name="configuration-product-dimension"></a>配置产品维度

配置产品维度用于确定具有基于维度的配置技术的基础产品的产品变型。 配置维度值由用户输入，应帮助确定各个产品变型。

### <a name="configuration-groups"></a>配置组

配置组在中央存储库定义，并且可以用于所有基于维度的产品配置模型。 配置组与各个物料清单行关联，并包含一组相互排斥的行。 这意味着只能为单个产品变型选择组中的一个行。

### <a name="bill-of-materials-bom"></a>物料清单 (BOM)

物料清单表示基于维度的产品配置的构建基块。 它必须包括可用于所有产品变型的所有不同的产品。 物料清单中的每一行均可以引用配置组。 如果行不引用配置组，它将包括在所有产品变型中。

### <a name="configuration-route"></a>配置流程

因为配置组将在产品配置流程中显示给用户，配置流程确定配置组的顺序。

### <a name="configuration-rules"></a>配置规则

配置规则表示，确保包括在物料清单的一个配置组中的产品在同一物料清单的不同配置组中强制包含或排除某一产品的机制。

## <a name="product-modeling-process"></a>产品建模流程
为基于维度的产品构建产品模型的自然顺序从定义相关配置组开始。 请务必确保物料清单中使用的所有产品已发布到已为其构建产品模型的公司。 对于到位这些构建基块，用户可以创建和分配物料清单配置组分配给所有相关物料清单行。 当物料清完成后配置流程，可以用于对相应配置组的序列中定义。 \[标题 id= "附件\_\["align= "”alignnone width= "\_"\][基于维度的![] (产品建模过程。/media/dimension 基于产品建模过程 v1.png)](。/media/dimension 基于产品建模过程 v1.png) 基于维度的\[产品建模过程/caption\]，则必须具有来自或不可以。使用的不同配置组的特定产品，可以创建将实行这些产品关系的配置规则。 在物料清单通过物料清单版本与基于维度的基础产品关联，并且二者均已审核和激活后，您可以创建产品配置并为每个配置输入一个名称。 配置可以在所有交易记录生成前定义，或者可以在某些配置需求发生前进行。

### <a name="suggested-use"></a>建议的使用

基于维度配置的技术最适合用于具有有限可变性的产品，标准产品维度尺寸、颜色、样式和配置的组合不适合确定特定的产品变型。 示例可以是具有框架高度、车轮大小、闸类型和不同齿轮的自行车。


