---
title: 显示制造物料的费用
description: 制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235500"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="54954-103">显示制造物料的费用</span><span class="sxs-lookup"><span data-stu-id="54954-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54954-104">制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。</span><span class="sxs-lookup"><span data-stu-id="54954-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="54954-105">物料的费用的计算出的金额能和物料的单位成本一起显示。</span><span class="sxs-lookup"><span data-stu-id="54954-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="54954-106">然而，该费用有时候作为单独的字段显示，并且它们不包括在该物料的单位成本。</span><span class="sxs-lookup"><span data-stu-id="54954-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="54954-107">当费用作为单独的字段出现时，一个字段显示费用的总金额，另一个字段显示用于摊销该金额的成本计算批次规模。</span><span class="sxs-lookup"><span data-stu-id="54954-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="54954-108">例如，“物料价格”页显示作为两个单独的字段的费用。</span><span class="sxs-lookup"><span data-stu-id="54954-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="54954-109">然而，“完成”页显示物料的单位总成本，并且摊销的成本包括在单位成本中。</span><span class="sxs-lookup"><span data-stu-id="54954-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="54954-110">出于标准成本目的，某一制造物料的费用始终包括在该物料的单位成本中。</span><span class="sxs-lookup"><span data-stu-id="54954-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="54954-111">而出于计划成本目的，可以选择是否包括杂项费用。</span><span class="sxs-lookup"><span data-stu-id="54954-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="54954-112">成本计算版本内的策略强制包括在制造物料的成本中的费用。</span><span class="sxs-lookup"><span data-stu-id="54954-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="54954-113">在您启用某一物料的成本记录时，为该物料的基本成本信息更新费用，显示在“物料价格”页上。</span><span class="sxs-lookup"><span data-stu-id="54954-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="54954-114">该费用作为两个单独的字段显示，并且它们不包括在该物料的单位成本。</span><span class="sxs-lookup"><span data-stu-id="54954-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="54954-115">每次启用都将更新该物料的基本成本信息，即使该启用反映不同的站点。</span><span class="sxs-lookup"><span data-stu-id="54954-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="54954-116">因此，您应该查看作为参考信息的基本成本信息。</span><span class="sxs-lookup"><span data-stu-id="54954-116">Therefore, you should view the base cost information as reference information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]