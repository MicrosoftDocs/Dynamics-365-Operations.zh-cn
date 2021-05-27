---
title: “保存以用于下一次付款”选项未显示
description: 本主题提供了故障排除指南，当电子商务站点结帐页面上的“付款方式”下面未出现“保存以用于下一次付款”复选框时，该指南可以提供帮助。
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018426"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="a72fb-103">“保存以用于下一次付款”选项未显示</span><span class="sxs-lookup"><span data-stu-id="a72fb-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a72fb-104">本主题提供了故障排除指南，当电子商务站点结帐页面上的 **付款方式** 下面未出现 **保存以用于下一次付款** 复选框时，该指南可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="a72fb-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="a72fb-105">说明</span><span class="sxs-lookup"><span data-stu-id="a72fb-105">Description</span></span>

<span data-ttu-id="a72fb-106">此 **保存以用于下一次付款** 复选框没有出现在电子商务网站的结帐页面上的 **付款方式** 部分中。</span><span class="sxs-lookup"><span data-stu-id="a72fb-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="a72fb-107">下图显示了一个结帐页面的示例，其中包括 **保存以用于下一次付款** 复选框。</span><span class="sxs-lookup"><span data-stu-id="a72fb-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![“付款”模块中的“保存以用于下一次付款”复选框](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="a72fb-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="a72fb-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="a72fb-110">验证是否在 Commerce Headquarters 中正确配置了适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="a72fb-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="a72fb-111">若要验证是否在 Commerce Headquarters 中正确配置了适用于 Adyen 的 Dynamics 365 付款连接器，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a72fb-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a72fb-112">转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。</span><span class="sxs-lookup"><span data-stu-id="a72fb-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="a72fb-113">选择在线商店。</span><span class="sxs-lookup"><span data-stu-id="a72fb-113">Select the online store.</span></span>
1. <span data-ttu-id="a72fb-114">在 **付款帐户** 快速选项卡上，请确保 **允许在电子商务中保存付款信息** 字段设置为 **真**。</span><span class="sxs-lookup"><span data-stu-id="a72fb-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![允许在 Commerce Headquarters 的电子商务字段中保存付款信息](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="a72fb-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="a72fb-116">Additional resources</span></span>

[<span data-ttu-id="a72fb-117">付款模块</span><span class="sxs-lookup"><span data-stu-id="a72fb-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="a72fb-118">使用 Adyen 连接器保存在线付款方式</span><span class="sxs-lookup"><span data-stu-id="a72fb-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
