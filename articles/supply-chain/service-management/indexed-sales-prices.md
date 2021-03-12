---
title: 指数化销售价
description: 您在创建预订费用时为预订销售价设置指数。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2103bc79e2a9671a059657838245e2d60455e168
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965872"
---
# <a name="indexed-sales-prices"></a><span data-ttu-id="b0216-103">指数化销售价</span><span class="sxs-lookup"><span data-stu-id="b0216-103">Indexed sales prices</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b0216-104">您在创建预订费用时为预订销售价设置指数。</span><span class="sxs-lookup"><span data-stu-id="b0216-104">You set up the index for a subscription sales price when you create a subscription fee.</span></span>

<span data-ttu-id="b0216-105">在 **创建预订费用** 窗体中，将 **定价来自** 字段设置为 **已建立指数的基价**，然后将基价乘以 **价格变更百分比** 字段中的百分比，以便获取预订交易记录的销售价。</span><span class="sxs-lookup"><span data-stu-id="b0216-105">In the **Create subscription fee** form, set the **Get pricing from** field to **Indexed base price**, and then multiply the base price by the percentage in the **Percent price change** field to get the sales price of the subscription transaction.</span></span>

<span data-ttu-id="b0216-106">如果基价是 EUR 1,000，并且指数是 110，则销售价是 EUR 1,100。</span><span class="sxs-lookup"><span data-stu-id="b0216-106">For example, if the base price is EUR 1,000, and the index is 110, the sales price is EUR 1,100.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0216-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="b0216-107">See also</span></span>

[<span data-ttu-id="b0216-108">创建预订费用交易记录</span><span class="sxs-lookup"><span data-stu-id="b0216-108">Create subscription fee transactions</span></span>](create-subscription-fee-transactions.md)

  


