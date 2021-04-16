---
title: 通过复制现有看板规则创建新看板规则
description: 该过程的重点是创建现有看板规则的副本。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d80bf0318234f858e51fb461894238894e01717c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829058"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="6f33b-103">通过复制现有看板规则创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="6f33b-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f33b-104">该过程的重点是创建现有看板规则的副本。</span><span class="sxs-lookup"><span data-stu-id="6f33b-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="6f33b-105">如果您想要根据现有看板规则创建新的看板规则，这很有用。</span><span class="sxs-lookup"><span data-stu-id="6f33b-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="6f33b-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="6f33b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6f33b-107">该过程面向工艺工程师和价值流经理，因为他们负责改进的生产流或新补货规则的制定。</span><span class="sxs-lookup"><span data-stu-id="6f33b-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="6f33b-108">选择一个看板规则</span><span class="sxs-lookup"><span data-stu-id="6f33b-108">Select a kanban rule</span></span>
1. <span data-ttu-id="6f33b-109">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="6f33b-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6f33b-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6f33b-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f33b-111">为产品 M0006 选择看板规则 000017。</span><span class="sxs-lookup"><span data-stu-id="6f33b-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="6f33b-112">复制一个看板规则</span><span class="sxs-lookup"><span data-stu-id="6f33b-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="6f33b-113">单击“复制看板规则”。</span><span class="sxs-lookup"><span data-stu-id="6f33b-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="6f33b-114">在复制看板规则时，可以更改类型、日期、活动和产品选择。</span><span class="sxs-lookup"><span data-stu-id="6f33b-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="6f33b-115">在下一步更改该过程的产品。</span><span class="sxs-lookup"><span data-stu-id="6f33b-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="6f33b-116">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6f33b-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="6f33b-117">选择“M0007”。</span><span class="sxs-lookup"><span data-stu-id="6f33b-117">Select M0007.</span></span>  
3. <span data-ttu-id="6f33b-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6f33b-118">Click OK.</span></span>
    * <span data-ttu-id="6f33b-119">请注意，已创建看板规则 000017 的副本。</span><span class="sxs-lookup"><span data-stu-id="6f33b-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]