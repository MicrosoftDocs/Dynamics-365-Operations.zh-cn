---
title: "混合客户订单"
description: "混合客户订单是一份订单，其中包含客户可以从店内自提的产品，以及以后将拣货或装运的产品。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 88d12641fa05953f7082158303237b7ba40c3fe2
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="hybrid-customer-orders"></a><span data-ttu-id="35ff5-103">混合客户订单</span><span class="sxs-lookup"><span data-stu-id="35ff5-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35ff5-104">混合客户订单是一份订单，其中包含客户可以从店内自提的产品，以及以后将拣货或装运的产品。</span><span class="sxs-lookup"><span data-stu-id="35ff5-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="35ff5-105">在 Microsoft Dynamics 365 for Retail 中，可以为客户订单选择自提所有产品，或自提选定产品。</span><span class="sxs-lookup"><span data-stu-id="35ff5-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="35ff5-106">创建订单后，自动为标记为自提的产品行开票，同样，创建订单后也会为待拣货的订单自动开票。</span><span class="sxs-lookup"><span data-stu-id="35ff5-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="35ff5-107">混合订单中的应付款金额通过添加带自提行金额的拣货和装运产品行中的保证金百分比确定。</span><span class="sxs-lookup"><span data-stu-id="35ff5-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="35ff5-108">对于混合订单，系统按照以下方式在客户订单模式与现金提货模式之间切换：</span><span class="sxs-lookup"><span data-stu-id="35ff5-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

-   <span data-ttu-id="35ff5-109">如果购物车中的所有产品设置为**自提交货**，将把订单作为现金提货交易记录处理。</span><span class="sxs-lookup"><span data-stu-id="35ff5-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
-   <span data-ttu-id="35ff5-110">如果购物车中的任何或所有行设置为**拣货**或**装运交货**，订单将作为客户订单交易记录处理。</span><span class="sxs-lookup"><span data-stu-id="35ff5-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="35ff5-111">如果某个购物车行已选中并选中了**领取所选项**、**装运所选产品**或**完成所选产品**，则仅使用该交货方法设置这个特定购物车行。</span><span class="sxs-lookup"><span data-stu-id="35ff5-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="35ff5-112">在这种情况下，工序的下游流程照常继续。</span><span class="sxs-lookup"><span data-stu-id="35ff5-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="35ff5-113">但是，如果选中了**领取所选项**、**装运所选产品**或**完成所选产品**但未选中购物车行，将打开一个新页面，其中列举所有购物车行。</span><span class="sxs-lookup"><span data-stu-id="35ff5-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="35ff5-114">在该屏幕上，可以一次选择多行以设置交货方法。</span><span class="sxs-lookup"><span data-stu-id="35ff5-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="35ff5-115">使用该方法选择行时，将覆盖已分配给该行的上述任何交货方法。</span><span class="sxs-lookup"><span data-stu-id="35ff5-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

<a name="additional-resources"></a><span data-ttu-id="35ff5-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="35ff5-116">Additional resources</span></span>
--------

[<span data-ttu-id="35ff5-117">客户订单概览</span><span class="sxs-lookup"><span data-stu-id="35ff5-117">Customer orders overview</span></span>](customer-orders-overview.md)




