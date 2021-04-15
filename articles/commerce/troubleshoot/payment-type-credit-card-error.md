---
title: 销售订单页面上的“付款类型必须是信用卡”错误
description: 本主题提供了故障排除指南，当订单同步后在销售订单页面上显示错误消息时，该指南可以提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801667"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="d828b-103">销售订单页面上的“付款类型必须是信用卡”错误</span><span class="sxs-lookup"><span data-stu-id="d828b-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d828b-104">本主题提供了故障排除指南，当订单同步后在销售订单页面上显示错误消息时，该指南可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="d828b-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="d828b-105">说明</span><span class="sxs-lookup"><span data-stu-id="d828b-105">Description</span></span>

<span data-ttu-id="d828b-106">同步订单后打开销售订单页面时，收到以下错误消息：“付款类型必须为信用卡，因为已指定了信用卡号。”</span><span class="sxs-lookup"><span data-stu-id="d828b-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![“付款类型必须是信用卡”错误](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="d828b-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="d828b-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="d828b-109">在 Commerce Headquarters 中设置付款类型</span><span class="sxs-lookup"><span data-stu-id="d828b-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="d828b-110">转到 **应收账款 \> 付款设置 \> 付款期限**。</span><span class="sxs-lookup"><span data-stu-id="d828b-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="d828b-111">在左侧导航栏中，选择您的付款方式。</span><span class="sxs-lookup"><span data-stu-id="d828b-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="d828b-112">在 **付款方式** 字段中，请确保选择了 **信用卡**。</span><span class="sxs-lookup"><span data-stu-id="d828b-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d828b-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="d828b-113">Additional resources</span></span>

[<span data-ttu-id="d828b-114">过帐在线销售和付款</span><span class="sxs-lookup"><span data-stu-id="d828b-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
