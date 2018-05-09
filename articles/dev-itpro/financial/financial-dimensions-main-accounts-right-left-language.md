---
title: "从右到左语言的财务维度和主科目"
description: "本主题介绍当您使用从右到左的语言时应考虑的一些实施决策以及您必须设置财务维度和主科目。"
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 857f2c7ea948717695c3c741a20f6b3e922b33e1
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a><span data-ttu-id="82e31-103">从右到左语言的财务维度和主科目</span><span class="sxs-lookup"><span data-stu-id="82e31-103">Financial dimensions and main accounts in a right-to-left language</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82e31-104">本主题介绍当您使用从右到左的语言时应考虑的一些实施决策以及您必须设置财务维度和主科目。</span><span class="sxs-lookup"><span data-stu-id="82e31-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="82e31-105">财务维度和主科目是实施的计划阶段的关键组件。</span><span class="sxs-lookup"><span data-stu-id="82e31-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="82e31-106">在系统中创建财务维度和主科目后，它们在“**配置科目结构**”、“**高级规则结构**”和“**用于集成应用程序的财务维度配置**”页使用。</span><span class="sxs-lookup"><span data-stu-id="82e31-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="82e31-107">在这些页面上定义的顺序在系统中针对数据输入和消耗量使用。</span><span class="sxs-lookup"><span data-stu-id="82e31-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="82e31-108">在系统中的某些位置，财务维度和主科目在单独的字段中显示。</span><span class="sxs-lookup"><span data-stu-id="82e31-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="82e31-109">但是在其他位置，例如日记帐，财务维度和主科目作为一个字符串显示。</span><span class="sxs-lookup"><span data-stu-id="82e31-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="82e31-110">在从右到左系统中设置财务维度和主科目设置财务维度和主科目的最佳实践</span><span class="sxs-lookup"><span data-stu-id="82e31-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="82e31-111">在您选择会计科目表的分隔符时，请选择其中一个双分隔符选项：双连字符 (--)、双竖线 (||) 或双句点 (..) 或双下划线 (\_\_)。</span><span class="sxs-lookup"><span data-stu-id="82e31-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="82e31-112">在您创建财务维度和主科目值时，仅使用数字和从右到左的语言字符。</span><span class="sxs-lookup"><span data-stu-id="82e31-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="82e31-113">避免在财务维度和主科目值中使用选定的会计科目分隔符。</span><span class="sxs-lookup"><span data-stu-id="82e31-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="82e31-114">通过以下最佳实践，您将帮助保障在整个系统中一致地显示用户定义的顺序。</span><span class="sxs-lookup"><span data-stu-id="82e31-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




