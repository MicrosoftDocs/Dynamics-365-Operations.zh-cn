---
title: 限制没有收据的退货的付款方式
description: 此主题描述如果在没有收据的情况下退货，如何为退款限制某些付款类型。
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564334"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="1de63-103">限制没有收据的退货的付款方式</span><span class="sxs-lookup"><span data-stu-id="1de63-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1de63-104">设置系统时，必须配置零售商接受的每种付款类型。</span><span class="sxs-lookup"><span data-stu-id="1de63-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="1de63-105">此主题描述如果在没有收据的情况下退货，如何为退款限制某些付款类型。</span><span class="sxs-lookup"><span data-stu-id="1de63-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="1de63-106">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="1de63-106">Set up payment methods</span></span>

<span data-ttu-id="1de63-107">若要设置付款方式，必须完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="1de63-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="1de63-108">创建的整个组织收到的付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="1de63-109">创建组织范围的卡类型和卡号。</span><span class="sxs-lookup"><span data-stu-id="1de63-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="1de63-110">如果接受信用卡或借记卡，则必须创建一种卡支付方式，然后创建组织范围的卡类型和卡号。</span><span class="sxs-lookup"><span data-stu-id="1de63-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="1de63-111">设置商店付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-111">Set up store payment methods.</span></span> <span data-ttu-id="1de63-112">将付款方式与每个商店，然后输入每个特定于商店设置的付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="1de63-113">为存储设置卡付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="1de63-114">对于商店接收的所有卡支付方式，请完成卡设置。</span><span class="sxs-lookup"><span data-stu-id="1de63-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="1de63-115">![零售商店设置](media/NoReceiptReturns1.png "零售商店设置")</span><span class="sxs-lookup"><span data-stu-id="1de63-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="1de63-116">限制没有收据的退货的付款方式</span><span class="sxs-lookup"><span data-stu-id="1de63-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="1de63-117">对于每个商店付款方式，在**零售商店管理**页上，在**非收据退货**下，将**对没有收据的退货限制**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="1de63-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="1de63-118">切换的默认值为**否**，这确保退款允许该付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="1de63-119">在**对没有收据的退货限制**设置为**是**时，退款将不允许所选付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="1de63-120">![零售商店付款方式](media/NoReceiptReturns3.png "零售商店付款方式")</span><span class="sxs-lookup"><span data-stu-id="1de63-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="1de63-121">在出纳选择为没有收据的退货限制的付款方式时，将显示一条消息来验证可接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="1de63-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="1de63-122">![可接受的付款方式](media/NoReceiptReturns4.png "可接受的付款方式")</span><span class="sxs-lookup"><span data-stu-id="1de63-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="1de63-123">如果某一交易既有有收据的退货，也有没有收据的退货，由于这类交易将是有收据的退货工作流，因此不强制使用限制条件。</span><span class="sxs-lookup"><span data-stu-id="1de63-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

