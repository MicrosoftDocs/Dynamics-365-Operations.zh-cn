---
title: 在结帐时信用卡录入页显示错误
description: 本主题提供了在“付款方式”部分未加载并显示错误消息时可能会有所帮助的故障排除指南。
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585208"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="041b6-103">在结帐时信用卡录入页显示错误</span><span class="sxs-lookup"><span data-stu-id="041b6-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="041b6-104">本主题提供了在 **付款方式** 部分未加载并显示错误消息时可能会有所帮助的故障排除指南。</span><span class="sxs-lookup"><span data-stu-id="041b6-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="041b6-105">说明</span><span class="sxs-lookup"><span data-stu-id="041b6-105">Description</span></span>

<span data-ttu-id="041b6-106">当您打开在线商店的结帐页面时，**付款方式** 部分未加载，并显示以下错误消息：“出了点问题。</span><span class="sxs-lookup"><span data-stu-id="041b6-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="041b6-107">请稍后重试。”</span><span class="sxs-lookup"><span data-stu-id="041b6-107">Please try again later."</span></span>

![付款模块错误](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="041b6-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="041b6-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="041b6-110">等待 Commerce Scale Unit 缓存过期</span><span class="sxs-lookup"><span data-stu-id="041b6-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="041b6-111">在线商店结帐页面上的付款服务设置缓存在 Commerce Scale Unit 上，最多可能需要 15 分钟才能显示在电子商务网站上。</span><span class="sxs-lookup"><span data-stu-id="041b6-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="041b6-112">这些付款服务设置包括对商家帐户 ID、云 API 密钥的更改，以及与付款方式相关的各种配置设置。</span><span class="sxs-lookup"><span data-stu-id="041b6-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="041b6-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="041b6-113">Additional resources</span></span>

[<span data-ttu-id="041b6-114">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="041b6-114">Set up an online channel</span></span>](../channel-setup-online.md)
