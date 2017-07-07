---
title: "从右到左语言的财务维度和主科目"
description: "本主题介绍当您使用从右到左的语言时应考虑的一些实施决策以及您必须设置财务维度和主科目。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: e28d3b318c2efa0b9d0da1154692f8e64c553e64
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>从右到左语言的财务维度和主科目

[!include[banner](../includes/banner.md)]


本主题介绍当您使用从右到左的语言时应考虑的一些实施决策以及您必须设置财务维度和主科目。

财务维度和主科目是实施的计划阶段的关键组件。 在系统中创建财务维度和主科目后，它们在“**配置科目结构**”、“**高级规则结构**”和“**用于集成应用程序的财务维度配置**”页使用。 在这些页面上定义的顺序在系统中针对数据输入和消耗量使用。 在系统中的某些位置，财务维度和主科目在单独的字段中显示。 但是在其他位置，例如日记帐，财务维度和主科目作为一个字符串显示。

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>在从右到左系统中设置财务维度和主科目设置财务维度和主科目的最佳实践

-   在您选择会计科目表的分隔符时，请选择其中一个双分隔符选项：双连字符 (--)、双竖线 (||) 或双句点 (..) 或双下划线 (\_\_)。
-   在您创建财务维度和主科目值时，仅使用数字和从右到左的语言字符。
-   避免在财务维度和主科目值中使用选定的会计科目分隔符。

通过以下最佳实践，您将帮助保障在整个系统中一致地显示用户定义的顺序。




