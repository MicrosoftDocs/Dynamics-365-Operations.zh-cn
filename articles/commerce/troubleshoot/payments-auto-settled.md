---
title: 付款会在订单开发票或装运之前自动结清
description: 本主题提供了故障排除指南，即使销售订单未开发票或未装运，也可以在下订单后立即在 Adyen 门户中结算付款时通过本指南获得帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018252"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="bbb51-103">付款会在订单开发票或装运之前自动结清</span><span class="sxs-lookup"><span data-stu-id="bbb51-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbb51-104">本主题提供了故障排除指南，即使销售订单未开发票或未装运，也可以在下订单后立即在 Adyen 门户中结算付款时通过本指南获得帮助。</span><span class="sxs-lookup"><span data-stu-id="bbb51-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="bbb51-105">说明</span><span class="sxs-lookup"><span data-stu-id="bbb51-105">Description</span></span>

<span data-ttu-id="bbb51-106">下订单后，即使销售订单未开发票或未装运，也可以立即在 Adyen 门户中结算付款。</span><span class="sxs-lookup"><span data-stu-id="bbb51-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="bbb51-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="bbb51-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="bbb51-108">配置手动捕获以在 Adyen 门户中进行电子商务付款</span><span class="sxs-lookup"><span data-stu-id="bbb51-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="bbb51-109">要配置手动捕获以在 Adyen 门户中进行电子商务付款，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="bbb51-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="bbb51-110">登录 Adyen 门户。</span><span class="sxs-lookup"><span data-stu-id="bbb51-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="bbb51-111">在右上角，为电子商务渠道选择您的商家帐户。</span><span class="sxs-lookup"><span data-stu-id="bbb51-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="bbb51-112">在顶部导航栏上，选择 **帐户**，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="bbb51-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="bbb51-113">在 **捕获延迟** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="bbb51-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Adyen 门户中的“捕获延迟”设置](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="bbb51-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="bbb51-115">Additional resources</span></span>

[<span data-ttu-id="bbb51-116">Adyen 付款捕获</span><span class="sxs-lookup"><span data-stu-id="bbb51-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="bbb51-117">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="bbb51-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="bbb51-118">设置适用于 Dynamics 365 的 Adyen 付款连接器</span><span class="sxs-lookup"><span data-stu-id="bbb51-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
