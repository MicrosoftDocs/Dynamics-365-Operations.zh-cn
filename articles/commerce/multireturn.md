---
title: 跨多个客户订单和账单的退回物料
description: 本主题介绍了 Dynamics 365 Commerce 中支持跨多个客户订单和账单进行退货的功能。
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796876"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="82945-103">跨多个客户订单和账单的退回物料</span><span class="sxs-lookup"><span data-stu-id="82945-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="82945-104">本文介绍了两项功能，这些功能可对多个账单的客户订单退货进行优化。</span><span class="sxs-lookup"><span data-stu-id="82945-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="82945-105">启用针对多个捕获的退款</span><span class="sxs-lookup"><span data-stu-id="82945-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="82945-106">此功能可针对同一客户订单进行多次关联退款。</span><span class="sxs-lookup"><span data-stu-id="82945-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="82945-107">转到 **功能管理** 工作区并搜索 **启用针对多个捕获的退款**。</span><span class="sxs-lookup"><span data-stu-id="82945-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="82945-108">选择 **启用针对多个订单的退款**，然后单击 **启用**。</span><span class="sxs-lookup"><span data-stu-id="82945-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="82945-109">对具有部分数量的退货启用正确的税金计算</span><span class="sxs-lookup"><span data-stu-id="82945-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="82945-110">此功能可确保在使用多个账单进行订单退货时，最终的税金等于最初收取的税额。</span><span class="sxs-lookup"><span data-stu-id="82945-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="82945-111">转到 **功能管理** 工作区并搜索 **对具有部分数量的退货启用正确的税金计算**。</span><span class="sxs-lookup"><span data-stu-id="82945-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="82945-112">选择 **对具有部分数量的退货启用正确的税金计算**，然后单击 **启用**。</span><span class="sxs-lookup"><span data-stu-id="82945-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="82945-113">处理退货</span><span class="sxs-lookup"><span data-stu-id="82945-113">Process returns</span></span>

<span data-ttu-id="82945-114">启用这些功能并将更改同步到商店后，商店的出纳可以选择多个销售订单，以处理客户的退货。</span><span class="sxs-lookup"><span data-stu-id="82945-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="82945-115">选中订单后，将显示所有订单发票上的所有可退产品的列表。</span><span class="sxs-lookup"><span data-stu-id="82945-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="82945-116">然后，出纳可以选择要退回的产品。</span><span class="sxs-lookup"><span data-stu-id="82945-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="82945-117">将为所有选定的产品创建单个退货单。</span><span class="sxs-lookup"><span data-stu-id="82945-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="82945-118">如果订单已全部退货，那么退还给客户的税额等于最初收取的税额。</span><span class="sxs-lookup"><span data-stu-id="82945-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]