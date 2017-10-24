---
title: "批次属性"
description: "文本提供有关批属性的信息。 批次属性是构成库存批次的原材料和成品的特征。 本文还说明如何分配批属性，以及如何在预留批处理时对它们进行搜索。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="50a78-105">批次属性</span><span class="sxs-lookup"><span data-stu-id="50a78-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="50a78-106">文本提供有关批属性的信息。</span><span class="sxs-lookup"><span data-stu-id="50a78-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="50a78-107">批次属性是构成库存批次的原材料和成品的特征。</span><span class="sxs-lookup"><span data-stu-id="50a78-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="50a78-108">本文还说明如何分配批属性，以及如何在预留批处理时对它们进行搜索。</span><span class="sxs-lookup"><span data-stu-id="50a78-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="50a78-109">批次属性是构成库存批次的原材料和成品的特征。</span><span class="sxs-lookup"><span data-stu-id="50a78-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="50a78-110">受若干因素（如环境条件、用于生产该批次的原材料的质量或成品的结果）影响，批次属性会有所不同。</span><span class="sxs-lookup"><span data-stu-id="50a78-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="50a78-111">不同的行业所用的批次属性的数量和类型可能相差甚远。</span><span class="sxs-lookup"><span data-stu-id="50a78-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="50a78-112">这是两个显示如何使用批次属性的示例：</span><span class="sxs-lookup"><span data-stu-id="50a78-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="50a78-113">在奶酪行业，牛奶（用于生产奶酪的原材料之一）可能具有脂肪含量和百分比重量之类的属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="50a78-114">通过牛奶生产的奶酪可能具有类似湿度和期限之类的其他属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="50a78-115">在钢铁行业，所生产的铁可能具有镁含量、银含量和锌含量百分比之类的属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="50a78-116">为更好地管理属性的数量和类型，您可以使用批次属性组。</span><span class="sxs-lookup"><span data-stu-id="50a78-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="50a78-117">这样，就不必逐个添加各个属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="50a78-118">分配批次属性</span><span class="sxs-lookup"><span data-stu-id="50a78-118">Assign batch attributes</span></span>
<span data-ttu-id="50a78-119">您可以将批次属性分配到库存批次中包含的各个产品或者您可以将它们分配给与特定客户关联的产品。</span><span class="sxs-lookup"><span data-stu-id="50a78-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="50a78-120">在您可以将批次属性分配在客户水平前，必须先将其分配在产品级别。</span><span class="sxs-lookup"><span data-stu-id="50a78-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="50a78-121">产品必须具有批次维度在“跟踪维度组”中设置为**有效**。</span><span class="sxs-lookup"><span data-stu-id="50a78-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="50a78-122">若要将批次属性分配到单个产品，请使用“产品特定”页。</span><span class="sxs-lookup"><span data-stu-id="50a78-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="50a78-123">如果该属性特定于客户的产品，请使用“客户特定”页。</span><span class="sxs-lookup"><span data-stu-id="50a78-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="50a78-124">在您添加一个属性给产品时，还可以定义其他参数。</span><span class="sxs-lookup"><span data-stu-id="50a78-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="50a78-125">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="50a78-125">Here are some examples:</span></span>

-   <span data-ttu-id="50a78-126">**整数**或**分数**类型的属性的最小值和最大值范围。</span><span class="sxs-lookup"><span data-stu-id="50a78-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="50a78-127">**整数**或**分数**类型属性的容差操作。</span><span class="sxs-lookup"><span data-stu-id="50a78-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="50a78-128">如果该属性的值超出最小值和最大值范围，行动可以是警告消息或错误消息。</span><span class="sxs-lookup"><span data-stu-id="50a78-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="50a78-129">属性的目标值。</span><span class="sxs-lookup"><span data-stu-id="50a78-129">The target value for the attribute.</span></span> <span data-ttu-id="50a78-130">此值是最佳值属性，并且该规则将应用于所有属性类型。</span><span class="sxs-lookup"><span data-stu-id="50a78-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="50a78-131">您可以访问在“产品信息管理”的**发布产品**页中选择的产品的页面。</span><span class="sxs-lookup"><span data-stu-id="50a78-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="50a78-132">在向产品分配批次属性后，可以添加特定值到**库存批次属性**页的属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="50a78-133">预留批次</span><span class="sxs-lookup"><span data-stu-id="50a78-133">Reserve batches</span></span>
<span data-ttu-id="50a78-134">在为销售订单进行批次预留以履行客户订单时，或者当您为生产订单领取和预留批次时，您可以搜索批次属性。</span><span class="sxs-lookup"><span data-stu-id="50a78-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="50a78-135">搜索帮助找到包含具有所需批次属性的产品的库存批次。</span><span class="sxs-lookup"><span data-stu-id="50a78-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="50a78-136">找到该批次或这些批次后，然后可以预留产品到起源库存交易记录行。</span><span class="sxs-lookup"><span data-stu-id="50a78-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




