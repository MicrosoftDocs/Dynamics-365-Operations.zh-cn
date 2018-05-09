---
title: "序列化产品中的 POS 改进"
description: "此主题列出了为了帮助您节省时间和提高生产效率而对序列化产品做出的改进。"
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 24f8fab744a186ef9070814a738a93bc99a479de
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="pos-improvements-for-serialized-products"></a><span data-ttu-id="615e7-103">序列化产品中的 POS 改进</span><span class="sxs-lookup"><span data-stu-id="615e7-103">POS improvements for serialized products</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="615e7-104">概览</span><span class="sxs-lookup"><span data-stu-id="615e7-104">Overview</span></span> 
<span data-ttu-id="615e7-105">基于零售总部中的设置，产品可归类为序列化或非序列化。</span><span class="sxs-lookup"><span data-stu-id="615e7-105">Based on the settings in Retail headquarters, products can be classified as either serialized or non-serialized.</span></span> <span data-ttu-id="615e7-106">产品序列化时，可以为每个物料分配一个唯一编号，以便跟踪保修、跟踪物料和确认所有权。</span><span class="sxs-lookup"><span data-stu-id="615e7-106">When products are serialized, each item can be assigned a unique number that helps track warranties, trace items, and confirm ownership.</span></span> <span data-ttu-id="615e7-107">尽管在我们的现代/云销售点 (POS) 中存在为序列化产品提供序列号的能力，我们仍然增加了一些改进，以帮助出纳节省时间和提高生产效率。</span><span class="sxs-lookup"><span data-stu-id="615e7-107">Although, the ability to provide serial numbers for serialized products existed in our Modern/Cloud Point of Sale (POS), some improvements have been added to help cashiers save time and be more productive.</span></span>  

## <a name="pos-improvements"></a><span data-ttu-id="615e7-108">POS 改进</span><span class="sxs-lookup"><span data-stu-id="615e7-108">POS improvements</span></span>

- <span data-ttu-id="615e7-109">**在结帐时才需要使用序列号** - 以前，出纳向交易记录添加序列化产品时必须提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-109">**Serial numbers aren't required until checkout** – Previously, a cashier who added a serialized product to the transaction was required to provide a serial number.</span></span> <span data-ttu-id="615e7-110">在客户服务解决方案中，如果出纳和销售内勤有机会向上销售产品，该要求就成为了一个问题。</span><span class="sxs-lookup"><span data-stu-id="615e7-110">This requirement became an issue in clienteling scenarios, if cashiers and sales associates had an opportunity to up-sell products.</span></span> <span data-ttu-id="615e7-111">在付款步骤之前，经常要在购物车中更新产品。</span><span class="sxs-lookup"><span data-stu-id="615e7-111">Until the payment step, the products were often updated in the cart.</span></span> <span data-ttu-id="615e7-112">因此，出纳每次添加新产品时，系统就会提示出纳提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-112">Therefore, every time that a cashier added a new product, the system prompted him or her for the serial number.</span></span> <span data-ttu-id="615e7-113">序列号对话框现在包括一个**稍后添加**按钮。</span><span class="sxs-lookup"><span data-stu-id="615e7-113">The serial number dialog box now includes an **Add later** button.</span></span> <span data-ttu-id="615e7-114">因此，销售内勤可以将物料添加到交易记录中，但可以稍后提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-114">Therefore, the sales associates can add the item to the transaction but can provide the serial number later.</span></span> <span data-ttu-id="615e7-115">销售内勤可以迅速添加和替换购物车中的序列化物料，然后在要结帐时提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-115">Sales associates can quickly add and replace serialized items in the cart, and then provide the serial number just before checkout.</span></span> <span data-ttu-id="615e7-116">如果未提供任何序列化产品的序列号，出纳在尝试完成交易时会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="615e7-116">If the serial number isn't provided for any serialized product, a cashier who tries to complete the transaction receives an error message.</span></span> <span data-ttu-id="615e7-117">该消息指出出纳必须提供缺失的序列号后才能继续。</span><span class="sxs-lookup"><span data-stu-id="615e7-117">This messages that states that the cashier must provide the missing serial numbers before he or she can continue.</span></span>

    <span data-ttu-id="615e7-118">对于跳过序列号的每个序列化物料，交易记录行下都会显示一条注释。</span><span class="sxs-lookup"><span data-stu-id="615e7-118">For each serialized item where the serial number was skipped, a comment appears under the transaction line.</span></span> <span data-ttu-id="615e7-119">该注释指出未提供该物料的序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-119">This comment states that the serial number hasn't been provided for the item.</span></span> <span data-ttu-id="615e7-120">因此，出纳可以快速找到缺少序列号的物料。</span><span class="sxs-lookup"><span data-stu-id="615e7-120">Therefore, the cashier can quickly find items that are missing a serial number.</span></span>

    <span data-ttu-id="615e7-121">新的**添加序列号**操作也为缺少序列号的物料提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-121">A new **Add serial number** operation also provides the serial number for items that are missing a serial number.</span></span> <span data-ttu-id="615e7-122">提供序列号后，无法编辑该序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-122">After the serial number is provided, it can't be edited.</span></span> <span data-ttu-id="615e7-123">出纳必须使该行失效并重新添加产品。</span><span class="sxs-lookup"><span data-stu-id="615e7-123">The cashier must void the line and add the product again.</span></span> 
    
- <span data-ttu-id="615e7-124">**下达客户订单不需要提供序列号** - 可以在一个商店下达客户订单，并从另一个商店完成该订单。</span><span class="sxs-lookup"><span data-stu-id="615e7-124">**Serial numbers aren't required in order to place customer orders** – Customer orders can be placed in one store and fulfilled from another.</span></span> <span data-ttu-id="615e7-125">下达客户订单的出纳不必提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-125">A cashier who places a customer order doesn't have to provide the serial number.</span></span> <span data-ttu-id="615e7-126">在领料或装货步骤中将提供该序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-126">The serial number will be provided during the picking or pickup step.</span></span> <span data-ttu-id="615e7-127">但是，选择了**自提**交货类型的所有行项都必须提供序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-127">However, a serial number must be provided for all line items that the **Carry out** delivery type is selected for.</span></span> <span data-ttu-id="615e7-128">否则无法完成交易记录。</span><span class="sxs-lookup"><span data-stu-id="615e7-128">Otherwise, the transaction can't be completed.</span></span>    
- <span data-ttu-id="615e7-129">**序列化产品没有在交易记录屏幕上聚合** - 使用**功能配置文件**页的**终端**字段组中的**聚合产品**设置可以在交易记录屏幕上聚合相同的非序列化产品。</span><span class="sxs-lookup"><span data-stu-id="615e7-129">**Serialized products aren't aggregated on the transaction screen** – The **Aggregate products** setting in the **Terminal** field group on the **Functionality profile** page lets you aggregate the same non-serialized products on the transaction screen.</span></span> <span data-ttu-id="615e7-130">聚合相同产品时，更容易在交易记录网格中进行查看。</span><span class="sxs-lookup"><span data-stu-id="615e7-130">When the same products are aggregated, they are easier to see in the transaction grid.</span></span> <span data-ttu-id="615e7-131">但是，由于序列号通常是唯一的，且销售内勤在结帐前无需输入序列号，因此**聚合产品**设置不适用于序列化产品。</span><span class="sxs-lookup"><span data-stu-id="615e7-131">However, because serial numbers are generally unique, and sales associates don't have to enter serial numbers until checkout, the **Aggregate products** setting doesn't apply to serialized products.</span></span> <span data-ttu-id="615e7-132">因此，如果选择了**聚合产品**设置，则不会在交易记录屏幕上聚合序列化产品。</span><span class="sxs-lookup"><span data-stu-id="615e7-132">Therefore, serialized products won't be aggregated on the transaction screen if the **Aggregate products** setting is selected.</span></span>
- <span data-ttu-id="615e7-133">**按序列号搜索日记帐的功能** - 现在可以额外按序列号搜索日记帐。</span><span class="sxs-lookup"><span data-stu-id="615e7-133">**Ability to search the journals by serial number** - The journals can now be additionally searched by serial numbers.</span></span> <span data-ttu-id="615e7-134">若要执行此操作，请打开“日记帐”操作，并按下应用栏上的“高级搜索”按钮。</span><span class="sxs-lookup"><span data-stu-id="615e7-134">To do so, open the "Journals" operation and press the "Advanced search" button in the app bar.</span></span> <span data-ttu-id="615e7-135">使用“添加筛选器”按钮，也可以应用筛选器来搜索序列号。</span><span class="sxs-lookup"><span data-stu-id="615e7-135">Using the "Add filter" button, a filter can be applied to search for the serial numbers as well.</span></span>

