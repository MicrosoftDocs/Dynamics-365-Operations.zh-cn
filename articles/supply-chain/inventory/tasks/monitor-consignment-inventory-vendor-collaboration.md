---
title: 使用供应商协作监控托运库存
description: 此过程显示如何通过供应商协作查看有关您在客户托运中发放的物料的存货级别的信息。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c74f09ee2056ce88442bf8f8ccba3985638525a6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213927"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="48081-103">使用供应商协作监控托运库存</span><span class="sxs-lookup"><span data-stu-id="48081-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48081-104">此过程显示如何通过供应商协作查看有关您在客户托运中发放的物料的存货级别的信息。</span><span class="sxs-lookup"><span data-stu-id="48081-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="48081-105">也可以在客户接管库存的所有权时监控存货的消耗情况。</span><span class="sxs-lookup"><span data-stu-id="48081-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="48081-106">您可以在 USMF 演示数据公司中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="48081-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="48081-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="48081-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="48081-108">查看消耗的库存</span><span class="sxs-lookup"><span data-stu-id="48081-108">View consumed inventory</span></span>
1. <span data-ttu-id="48081-109">转到“供应商协作”>“托运库存”>“从托运库存接收的产品”。</span><span class="sxs-lookup"><span data-stu-id="48081-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="48081-110">此列表显示托运库存所有权从供应商更改为客户时生成的物料收货行。</span><span class="sxs-lookup"><span data-stu-id="48081-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="48081-111">可能必须向右滚动才能看到数量和其他信息。</span><span class="sxs-lookup"><span data-stu-id="48081-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="48081-112">可以使用此列表中的信息为客户生成发票。</span><span class="sxs-lookup"><span data-stu-id="48081-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="48081-113">您还可以将数据导出至 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="48081-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="48081-114">单击“查看采购订单”。</span><span class="sxs-lookup"><span data-stu-id="48081-114">Click View purchase order.</span></span>
3. <span data-ttu-id="48081-115">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="48081-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="48081-116">此行标记为“托运”，并且标题部分显示状态为“入库”的采购订单。</span><span class="sxs-lookup"><span data-stu-id="48081-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="48081-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="48081-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="48081-118">查看现有库存量</span><span class="sxs-lookup"><span data-stu-id="48081-118">View on-hand inventory</span></span>
1. <span data-ttu-id="48081-119">转到“供应商协作”>“托运库存”>“现有托运库存”。</span><span class="sxs-lookup"><span data-stu-id="48081-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="48081-120">“现有托运库存”页面显示您在客户的仓库中拥有的存货。</span><span class="sxs-lookup"><span data-stu-id="48081-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="48081-121">可以通过单击“显示维度”选项卡显示更多维度，如站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="48081-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

