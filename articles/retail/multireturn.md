---
title: 跨多个客户订单和发票的退回物料
description: 本主题介绍了 Microsoft Dynamics 365 for Retail 中支持跨多个客户订单和发票的退货的功能。
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2019
ms.locfileid: "373060"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="42c83-103">跨多个客户订单和发票的退回物料</span><span class="sxs-lookup"><span data-stu-id="42c83-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="42c83-104">在 Dynamics 365 for Finance and Operations 版本 10.0 中，可以跨多个订单和发票处理退货，而在低于 10.0 的版本中，一次只能通过单个发票处理退货。</span><span class="sxs-lookup"><span data-stu-id="42c83-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="42c83-105">配置 Retail 以支持跨多个客户订单和发票的退货</span><span class="sxs-lookup"><span data-stu-id="42c83-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="42c83-106">转到 **Retail 参数 \> 客户订单**。</span><span class="sxs-lookup"><span data-stu-id="42c83-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="42c83-107">启用**支持针对多个订单的退货**参数。</span><span class="sxs-lookup"><span data-stu-id="42c83-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="42c83-108">处理退货</span><span class="sxs-lookup"><span data-stu-id="42c83-108">Process returns</span></span>

<span data-ttu-id="42c83-109">启用该参数并将更改同步到商店后，商店的出纳可以选择多个销售订单，以处理客户的退货。</span><span class="sxs-lookup"><span data-stu-id="42c83-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="42c83-110">选中订单后，将显示所有订单发票上的所有可退产品的列表。</span><span class="sxs-lookup"><span data-stu-id="42c83-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="42c83-111">然后，出纳可以选择要退回的产品。</span><span class="sxs-lookup"><span data-stu-id="42c83-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="42c83-112">将为所有选定的产品创建单个退货单。</span><span class="sxs-lookup"><span data-stu-id="42c83-112">A single return order will be created for all the selected products.</span></span>
