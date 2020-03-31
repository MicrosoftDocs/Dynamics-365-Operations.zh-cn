---
title: 跨多个客户订单和账单的退回物料
description: 本主题介绍了 Dynamics 365 Commerce 中支持跨多个客户订单和账单进行退货的功能。
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004450"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="0ee2e-103">跨多个客户订单和账单的退回物料</span><span class="sxs-lookup"><span data-stu-id="0ee2e-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0ee2e-104">可以跨多个订单和账单处理退货。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="0ee2e-105">配置 Commerce 以支持跨多个客户订单和账单进行退货</span><span class="sxs-lookup"><span data-stu-id="0ee2e-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="0ee2e-106">转到**Commerce 参数 \> 客户订单**。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="0ee2e-107">启用**支持针对多个订单的退货**参数。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="0ee2e-108">处理退货</span><span class="sxs-lookup"><span data-stu-id="0ee2e-108">Process returns</span></span>

<span data-ttu-id="0ee2e-109">启用该参数并将更改同步到商店后，商店的出纳可以选择多个销售订单，以处理客户的退货。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="0ee2e-110">选中订单后，将显示所有订单发票上的所有可退产品的列表。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="0ee2e-111">然后，出纳可以选择要退回的产品。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="0ee2e-112">将为所有选定的产品创建单个退货单。</span><span class="sxs-lookup"><span data-stu-id="0ee2e-112">A single return order will be created for all the selected products.</span></span>