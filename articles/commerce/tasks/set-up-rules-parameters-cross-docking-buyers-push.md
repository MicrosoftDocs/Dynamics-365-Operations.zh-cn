---
title: 设置越库配送和集中采购配送的规则和参数
description: 此程序会演示补货规则的创建步骤。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410516"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="d0584-103">设置越库配送和集中采购配送的规则和参数</span><span class="sxs-lookup"><span data-stu-id="d0584-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0584-104">此程序会演示补货规则的创建步骤。</span><span class="sxs-lookup"><span data-stu-id="d0584-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="d0584-105">在使用越库配送和集中采购配送时，补货规则可用于控制如何将产品配送到商店。</span><span class="sxs-lookup"><span data-stu-id="d0584-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="d0584-106">可以为商店或商店组设置补货规则。</span><span class="sxs-lookup"><span data-stu-id="d0584-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="d0584-107">在使用补货规则作为越库配送或集中采购配送的配送方法时，规则内为每一行定义的权重将控制如何在商店之间分配产品的数量。</span><span class="sxs-lookup"><span data-stu-id="d0584-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="d0584-108">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="d0584-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d0584-109">转至“补货规则”。</span><span class="sxs-lookup"><span data-stu-id="d0584-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="d0584-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d0584-110">Click New.</span></span>
3. <span data-ttu-id="d0584-111">在“补货规则”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0584-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="d0584-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0584-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d0584-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d0584-113">Click Save.</span></span>
6. <span data-ttu-id="d0584-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d0584-114">Click Add.</span></span>
7. <span data-ttu-id="d0584-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d0584-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d0584-116">您可以选择“补货层次结构”或“渠道”类型。</span><span class="sxs-lookup"><span data-stu-id="d0584-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="d0584-117">该值可以控制“名称”中的选择是渠道层次结构还是特定渠道。</span><span class="sxs-lookup"><span data-stu-id="d0584-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="d0584-118">对于本示例，将它设置为“补货层次结构”。</span><span class="sxs-lookup"><span data-stu-id="d0584-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="d0584-119">在“名称”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d0584-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="d0584-120">默认权重值使用仓库定义的权重进行填充。</span><span class="sxs-lookup"><span data-stu-id="d0584-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="d0584-121">此权重可用于补货规则，或者您可以在“权重”字段中输入一个新的权重。</span><span class="sxs-lookup"><span data-stu-id="d0584-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="d0584-122">在“权重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d0584-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="d0584-123">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d0584-123">Click Add.</span></span>
11. <span data-ttu-id="d0584-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d0584-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="d0584-125">在“类型”字段中，选择“渠道”。</span><span class="sxs-lookup"><span data-stu-id="d0584-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="d0584-126">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d0584-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="d0584-127">在“权重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d0584-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="d0584-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d0584-128">Click Save.</span></span>

