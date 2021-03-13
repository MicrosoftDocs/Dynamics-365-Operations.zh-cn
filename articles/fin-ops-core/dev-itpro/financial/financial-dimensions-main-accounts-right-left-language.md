---
title: 从右到左的语言中的财务维度和主科目
description: 本主题介绍使用从右到左语言并且必须设置财务维度和主科目时需要作出的决定。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2bdf1b99ae7be6c9d9c43c91c9273e18ce9b1093
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127639"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>从右到左的语言中的财务维度和主科目

[!include [banner](../includes/banner.md)]

本主题介绍当您使用从右到左的语言时应考虑的一些实施决策以及您必须设置财务维度和主科目。

财务维度和主科目是实施的计划阶段的关键组件。 在系统中创建财务维度和主科目后，它们在 **配置科目结构**、**高级规则结构** 和 **用于集成应用程序的财务维度配置** 页使用。 在这些页面上定义的顺序在系统中针对数据输入和消耗量使用。 在系统中的某些位置，财务维度和主科目在单独的字段中显示。 在其他位置，例如日记帐，财务维度和主科目作为一个字符串显示。

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>在从右到左系统中设置财务维度和主科目设置财务维度和主科目的最佳实践

- 在您选择会计科目表的分隔符时，请选择其中一个双分隔符选项：双连字符 (`--`)、双竖线 (`||`) 或双句点 (`..`) 或双下划线 (`\\`)。
- 在您创建财务维度和主科目值时，仅使用数字和从右到左的语言字符。
- 避免在财务维度和主科目值中使用选定的会计科目分隔符。

通过以下最佳实践，您将帮助保障在整个系统中一致地显示用户定义的顺序。
