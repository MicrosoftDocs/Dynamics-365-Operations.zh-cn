---
title: 与默认付款服务有关的订单同步错误
description: 本主题提供了故障排除指南，可以帮助解决同步在线订单时可能发生的错误。
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585207"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="23b92-103">与默认付款服务有关的订单同步错误</span><span class="sxs-lookup"><span data-stu-id="23b92-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23b92-104">本主题提供了故障排除指南，可以帮助解决同步在线订单时可能发生的错误。</span><span class="sxs-lookup"><span data-stu-id="23b92-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="23b92-105">说明</span><span class="sxs-lookup"><span data-stu-id="23b92-105">Description</span></span>

<span data-ttu-id="23b92-106">同步在线订单时，您会收到以下错误消息：“必须有默认的付款服务才能处理信用卡交易。”</span><span class="sxs-lookup"><span data-stu-id="23b92-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![缺少默认付款服务错误](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="23b92-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="23b92-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="23b92-109">在 Commerce Headquarters 中确认或设置默认付款服务</span><span class="sxs-lookup"><span data-stu-id="23b92-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="23b92-110">要在 Commerce Headquarters 中确认或设置默认付款服务，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="23b92-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="23b92-111">转至 **应收帐款 \> 付款设置 \> 付款服务**。</span><span class="sxs-lookup"><span data-stu-id="23b92-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="23b92-112">确保对一项付款服务将 **新信用卡的默认处理程序** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="23b92-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23b92-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="23b92-113">Additional resources</span></span>

[<span data-ttu-id="23b92-114">信用卡设置、授权和获取</span><span class="sxs-lookup"><span data-stu-id="23b92-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
