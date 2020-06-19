---
title: 采用双写入的库存可用性
description: 本主题提供有关以双写入方式检查库存可用性的信息。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426974"
---
# <a name="inventory-availability"></a><span data-ttu-id="3f83e-103">库存可用性</span><span class="sxs-lookup"><span data-stu-id="3f83e-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3f83e-104">在 Dynamics 365 中的模型驱动应用中，使用库存可用性，您可以先检查库存，然后再将产品添加到**报价单**、**订单**或**发票**窗体。</span><span class="sxs-lookup"><span data-stu-id="3f83e-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="3f83e-105">例如，检查库存并确定履行日期是[目标客户到现金](dual-write-prospect-to-cash.md)流程的关键任务。</span><span class="sxs-lookup"><span data-stu-id="3f83e-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="3f83e-106">如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。</span><span class="sxs-lookup"><span data-stu-id="3f83e-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="3f83e-107">您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。</span><span class="sxs-lookup"><span data-stu-id="3f83e-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="3f83e-108">现有库存量</span><span class="sxs-lookup"><span data-stu-id="3f83e-108">On-hand Inventory</span></span> 

<span data-ttu-id="3f83e-109">在 Dynamics 365 Sales 中的**报价单**、**订单**或**发票**窗体的标题中，添加了一个新按钮**现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="3f83e-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="3f83e-110">单击此按钮时，将出现一个对话框，您可以指定要检查其现有库存量的公司和产品。</span><span class="sxs-lookup"><span data-stu-id="3f83e-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="3f83e-111">它返回 Dynamics 365 Supply Chain Management 中的库存信息，显示与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同的信息。</span><span class="sxs-lookup"><span data-stu-id="3f83e-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="3f83e-112">此信息包括以下数量：</span><span class="sxs-lookup"><span data-stu-id="3f83e-112">The information includes these quantities:</span></span>

- <span data-ttu-id="3f83e-113">**现有数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="3f83e-114">**预留现有数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="3f83e-115">**可用现有数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="3f83e-116">**订购数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="3f83e-117">**在单数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-117">**On-order Quantity**</span></span>
- <span data-ttu-id="3f83e-118">**预留订购数量**</span><span class="sxs-lookup"><span data-stu-id="3f83e-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="3f83e-119">**可用总数**</span><span class="sxs-lookup"><span data-stu-id="3f83e-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="3f83e-120">ATP 信息</span><span class="sxs-lookup"><span data-stu-id="3f83e-120">ATP information</span></span>

<span data-ttu-id="3f83e-121">在 Dynamics 365 Sales 中的**报价单**、**订单**或**发票**窗体的行项上，添加了一个新按钮 **ATP 信息**。</span><span class="sxs-lookup"><span data-stu-id="3f83e-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="3f83e-122">单击此按钮时，将出现一个对话框，您可以指定公司、产品、库存站点、库存仓库和订单数量。</span><span class="sxs-lookup"><span data-stu-id="3f83e-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="3f83e-123">它返回 Supply Chain Management 中的 **ATP 信息**，并显示[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置。</span><span class="sxs-lookup"><span data-stu-id="3f83e-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="3f83e-124">此信息包括 **ATP 数量**、**收货数量**、**发货数量**和**现有数量**。</span><span class="sxs-lookup"><span data-stu-id="3f83e-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
