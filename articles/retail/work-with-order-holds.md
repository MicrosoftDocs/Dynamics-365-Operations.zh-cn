---
title: "订单保留"
description: "本主题描述使用 Dynamics 365 for Retail 将订单置于暂停状态。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 106ce40f93704e67e53db2e62ae481d271aed755
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="order-holds"></a><span data-ttu-id="a4b60-103">订单保留</span><span class="sxs-lookup"><span data-stu-id="a4b60-103">Order holds</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4b60-104">本主题描述使用 Dynamics 365 for Retail 将订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a4b60-105">出于各种原因，可将订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="a4b60-106">例如，在可以验证客户地址或付款方式之前，或在经理可以查看客户的信用额度之前，您可以将订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="a4b60-107">在销售流程中，有时必须将销售订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="a4b60-108">例如，由于客户付款出现问题、可疑欺诈或经理必须审核销售订单，可能将销售订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="a4b60-109">在销售订单置于暂停状态时，一个订单保留代码被分配给销售订单来表明保留的原因。</span><span class="sxs-lookup"><span data-stu-id="a4b60-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="a4b60-110">在**销售和市场营销** &gt; **设置** &gt; **销售订单** &gt; **订单保留代码**中配置销售订单保留代码。</span><span class="sxs-lookup"><span data-stu-id="a4b60-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="a4b60-111">可在创建订单时或稍后手动将销售订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="a4b60-112">此外，可以根据欺诈规则自动将订单置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="a4b60-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="a4b60-113">在将销售订单置于暂停状态时，可能需要使用更多信息更新该订单。</span><span class="sxs-lookup"><span data-stu-id="a4b60-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="a4b60-114">或者，在继续使用销售订单时，可能需要签出该订单。</span><span class="sxs-lookup"><span data-stu-id="a4b60-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="a4b60-115">您可使用订单保留工作台来签出销售订单，将其签回甚至覆盖另一个用户的签出（**零售** &gt; **客户** &gt; **订单保留**）。</span><span class="sxs-lookup"><span data-stu-id="a4b60-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="a4b60-116">在订单即将完成时，您需在完成订单流程之前删除保留。</span><span class="sxs-lookup"><span data-stu-id="a4b60-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




