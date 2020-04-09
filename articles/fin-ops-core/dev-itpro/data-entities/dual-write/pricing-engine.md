---
title: 按需与 Dynamics 365 Supply Chain Management 定价引擎同步
description: 本主题介绍如何在 Dynamics 365 Sales 的 Microsoft Dynamics 365 Supply Chain Management 中使用定价引擎。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173169"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="c0495-103">按需与 Dynamics 365 Supply Chain Management 定价引擎同步</span><span class="sxs-lookup"><span data-stu-id="c0495-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c0495-104">Microsoft Dynamics 365 Supply Chain Management 包括处理贸易协议、价目表、客户会员计划、促销和折扣的定价引擎。</span><span class="sxs-lookup"><span data-stu-id="c0495-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="c0495-105">定价引擎使用复杂的规则来确定给定报价单或订单的最佳价格。</span><span class="sxs-lookup"><span data-stu-id="c0495-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="c0495-106">使用双向写入时，您可以在 Dynamics 365 Sales 中的“报价单”和“订单”页面上使用 Dynamics 365 Supply Chain Management 中的静态定价或定价引擎。</span><span class="sxs-lookup"><span data-stu-id="c0495-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="c0495-107">使用 Sales 中的 Supply Chain Management 中的定价引擎</span><span class="sxs-lookup"><span data-stu-id="c0495-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="c0495-108">在 Sales 中，转到**销售 \> 订单**。</span><span class="sxs-lookup"><span data-stu-id="c0495-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="c0495-109">选择**新建**创建新订单，或在**我的订单**列表中选择现有订单。</span><span class="sxs-lookup"><span data-stu-id="c0495-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="c0495-110">添加新订单行。</span><span class="sxs-lookup"><span data-stu-id="c0495-110">Add a new order line.</span></span>
4. <span data-ttu-id="c0495-111">如果您要创建新订单，请选择在操作窗格上**价格订单**。</span><span class="sxs-lookup"><span data-stu-id="c0495-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="c0495-112">如果您要更新现有订单，请选择在操作窗格上**重新计算**。</span><span class="sxs-lookup"><span data-stu-id="c0495-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="c0495-113">下列字段将自动填写：</span><span class="sxs-lookup"><span data-stu-id="c0495-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="c0495-114">详细信息金额</span><span class="sxs-lookup"><span data-stu-id="c0495-114">Detail Amount</span></span>
    + <span data-ttu-id="c0495-115">折扣百分比</span><span class="sxs-lookup"><span data-stu-id="c0495-115">Discount %</span></span>
    + <span data-ttu-id="c0495-116">折扣</span><span class="sxs-lookup"><span data-stu-id="c0495-116">Discount</span></span>
    + <span data-ttu-id="c0495-117">不计运费金额</span><span class="sxs-lookup"><span data-stu-id="c0495-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="c0495-118">运费金额</span><span class="sxs-lookup"><span data-stu-id="c0495-118">Freight Amount</span></span>
    + <span data-ttu-id="c0495-119">税金总计</span><span class="sxs-lookup"><span data-stu-id="c0495-119">Total Tax</span></span>
    + <span data-ttu-id="c0495-120">总金额</span><span class="sxs-lookup"><span data-stu-id="c0495-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="c0495-121">工作原理</span><span class="sxs-lookup"><span data-stu-id="c0495-121">How it works</span></span>

<span data-ttu-id="c0495-122">当您在 Sales 中选择**价格订单**时，将为关联销售订单调用 Supply Chain Management 中**销售订单 \> 视图**选项卡上的**总计**函数。</span><span class="sxs-lookup"><span data-stu-id="c0495-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="c0495-123">Sales 中订单总计中的值用于填写 Supply Chain Management 中的对应字段。</span><span class="sxs-lookup"><span data-stu-id="c0495-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="c0495-124">在 Supply Chain Management 中计算销售订单总计时，计算将评估客户的现有贸易协议和销售协议以及销售订单中列出的产品。</span><span class="sxs-lookup"><span data-stu-id="c0495-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="c0495-125">此信息用于计算总计。</span><span class="sxs-lookup"><span data-stu-id="c0495-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="c0495-126">选择**价格订单**时，Sales 会自动反映 Supply Chain Management 中已经完成的所有设置。</span><span class="sxs-lookup"><span data-stu-id="c0495-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="c0495-127">限制</span><span class="sxs-lookup"><span data-stu-id="c0495-127">Limitations</span></span>

<span data-ttu-id="c0495-128">填写 Sales 中的字段后，将应用以下限制：</span><span class="sxs-lookup"><span data-stu-id="c0495-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="c0495-129">Supply Chain Management 中的费用设置和费用分配不会在 Sales 中复制。</span><span class="sxs-lookup"><span data-stu-id="c0495-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="c0495-130">定价不考虑在 Supply Chain Management 中销售订单行页面上的**零售渠道**字段中指定的特殊零售定价。</span><span class="sxs-lookup"><span data-stu-id="c0495-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="c0495-131">不考虑 Supply Chain Management 的**贸易折让管理**部分定义的折扣。</span><span class="sxs-lookup"><span data-stu-id="c0495-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
