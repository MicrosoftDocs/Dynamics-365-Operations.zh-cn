---
title: 采用双写入的库存可用性
description: 本主题提供有关如何以双写入方式检查库存可用性的信息。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4450171"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="8bd27-103">采用双写入的库存可用性</span><span class="sxs-lookup"><span data-stu-id="8bd27-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bd27-104">使用库存可用性，可以在 Microsoft Dynamics 365 Sales 中先检查库存，然后再将产品添加到 **报价单**、**订单** 或 **发票** 页面。</span><span class="sxs-lookup"><span data-stu-id="8bd27-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="8bd27-105">例如，检查库存并将履行日期确定为[目标客户到现金](dual-write-prospect-to-cash.md)流程的一个关键任务。</span><span class="sxs-lookup"><span data-stu-id="8bd27-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="8bd27-106">如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。</span><span class="sxs-lookup"><span data-stu-id="8bd27-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="8bd27-107">您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。</span><span class="sxs-lookup"><span data-stu-id="8bd27-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="8bd27-108">现有库存</span><span class="sxs-lookup"><span data-stu-id="8bd27-108">On-hand inventory</span></span>

<span data-ttu-id="8bd27-109">在 Dynamics 365 Sales 中，**报价单**、**订单** 和 **发票** 页面的标题中已经添加了一个新的 **现有库存量** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8bd27-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="8bd27-110">选择此按钮时，将出现一个对话框，您可以在其中指定要检查其现有库存量的公司和产品。</span><span class="sxs-lookup"><span data-stu-id="8bd27-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="8bd27-111">此对话框显示的信息与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同。</span><span class="sxs-lookup"><span data-stu-id="8bd27-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="8bd27-112">此对话框返回 Dynamics 365 Supply Chain Management 中的库存信息。</span><span class="sxs-lookup"><span data-stu-id="8bd27-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8bd27-113">此信息包括以下数量：</span><span class="sxs-lookup"><span data-stu-id="8bd27-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="8bd27-114">现有数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-114">On-hand quantity</span></span>
- <span data-ttu-id="8bd27-115">预留现有数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="8bd27-116">可用现有数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-116">Available on-hand quantity</span></span>
- <span data-ttu-id="8bd27-117">订购数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-117">Ordered quantity</span></span>
- <span data-ttu-id="8bd27-118">在单数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-118">On-order quantity</span></span>
- <span data-ttu-id="8bd27-119">预留的订购数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="8bd27-120">可用总数</span><span class="sxs-lookup"><span data-stu-id="8bd27-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="8bd27-121">ATP 信息</span><span class="sxs-lookup"><span data-stu-id="8bd27-121">ATP information</span></span>

<span data-ttu-id="8bd27-122">在 Sales 中，**报价单**、**订单** 和 **发票** 页面的行项中已经添加了新的 **ATP 信息** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8bd27-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="8bd27-123">选择此按钮时，将出现一个对话框，您可以在其中指定公司、产品、库存站点、库存仓库和订单数量。</span><span class="sxs-lookup"><span data-stu-id="8bd27-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="8bd27-124">此对话框具有与[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置相同的设置。</span><span class="sxs-lookup"><span data-stu-id="8bd27-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="8bd27-125">此对话框返回 Supply Chain Management 中的 ATP 信息。</span><span class="sxs-lookup"><span data-stu-id="8bd27-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="8bd27-126">此信息包括以下数量：</span><span class="sxs-lookup"><span data-stu-id="8bd27-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="8bd27-127">ATP 数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-127">ATP quantity</span></span>
- <span data-ttu-id="8bd27-128">收货数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-128">Receipt quantity</span></span>
- <span data-ttu-id="8bd27-129">发货数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-129">Issue quantity</span></span>
- <span data-ttu-id="8bd27-130">现有数量</span><span class="sxs-lookup"><span data-stu-id="8bd27-130">On-hand quantity</span></span>
