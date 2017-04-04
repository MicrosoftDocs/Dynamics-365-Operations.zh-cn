---
title: "系统定义和用户定义的表约束"
description: "文章说明此表约束的两个种类型组件的资本-用户定义和系统中定义配置的产品模型。 表约束表示允许的属性组合的矩阵，在其中每行定义一组可能的属性值。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 510ee819e6bc69b72df767f6cfd284230baba729
ms.lasthandoff: 03/31/2017


---

# <a name="system-defined-and-user-defined-table-constraints"></a>系统定义和用户定义的表约束

文章说明此表约束的两个种类型组件的资本-用户定义和系统中定义配置的产品模型。 表约束表示允许的属性组合的矩阵，在其中每行定义一组可能的属性值。

表约束表示产品配置模型中的组件允许的属性组合的矩阵。 表中的每行定义一组可能的属性值。 可在产品配置模型中声明两种类型的约束：

-   **表达式约束** – 创建一个表达式，用以定义属性之间的关系，以确保配置产品时仅可选择兼容值。
-   **表约束** – 创建定义指定的属性集允许的所有组合的表。 两种类型的表约束可用：用户定义的表约束和系统定义的表约束。

本文描述用户定义和系统定义的用于产品配置模型中的组件的表约束。

## <a name="user-defined-table-constraints"></a>用户定义的表约束
用户定义的表约束是一种可于描述属性类型定义的属性值组合的矩阵。 例如，如果生产扬声器，您可以在用户定义的表约束中包括用于机柜表面处理和前格栅的列。 机柜表面处理的属性类型有四个值，前格栅的属性类型有三个值。 因此，如果不使用约束，有 4 × 3 = 12 个可能组合。 但是，在本示例中，只允许六个组合，如下表中所示。 此信息显示在**“编辑表约束”**页上的**“允许的组合”**选项卡上。

| 机柜表面处理 | 前格栅 |
|----------------|-------------|
| 黑          | 黑       |
| 黑          | 金属       |
| 橡木            | 黑       |
| 红木       | 白色       |
| 白色          | 黑       |
| 白色          | 白色       |

用户定义的表约束由工作方式与表达式约束系统的静态表输入定义。 使用用户定义的表约束时，该表的优点是通常比长表达式约束更易于创建、了解和维护。

## <a name="system-defined-table-constraints"></a>系统定义的表约束
系统定义的表约束在表中的属性类型与字段之间创建动态映射。 当系统定义的表约束包括在产品配置模型中时，映射可确保显示表中的数据，而不是属性类型的值。 结果是动态约束，因为表内容可被修改（例如，由其他模块）。  

创建系统定义的表约束时，选择一个表，（可选）定义要使用的查询，然后将这些属性类型与所选表中的字段关联。 字段的类型必须与属性类型的类型匹配。  

在表约束生效可以对产品模型配置的，在前之一的一个约束条件必须包括表约束模型的组件。 过程是创建新约束，选择表约束类型，然后选择表约束定义使用。 最后，表中的所有字段都必须映射到产品配置模型中的属性。

<a name="see-also"></a>请参阅
--------

[产品配置模型中的重要概念](product-configuration-models.md)


