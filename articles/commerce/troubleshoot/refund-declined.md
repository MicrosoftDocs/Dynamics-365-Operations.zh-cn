---
title: 退货单上的退款被拒绝
description: 本主题提供了故障排除指南，当由于用于开票的信用卡与原始付款授权期间使用的信用卡不同而导致退货单上的退款被拒绝时，该指南可提供帮助。
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801547"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="06f49-103">退货单上的退款被拒绝</span><span class="sxs-lookup"><span data-stu-id="06f49-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06f49-104">本主题提供了故障排除指南，当由于用于开票的信用卡与原始付款授权期间使用的信用卡不同而导致退货单上的退款被拒绝时，该指南可提供帮助。</span><span class="sxs-lookup"><span data-stu-id="06f49-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="06f49-105">说明</span><span class="sxs-lookup"><span data-stu-id="06f49-105">Description</span></span>

<span data-ttu-id="06f49-106">当用于对退货单开具发票的信用卡与原始付款授权期间使用的信用卡不同时，退款将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="06f49-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="06f49-107">您收到以下错误信息：“某些付款的状态不正确，因此无法过帐。</span><span class="sxs-lookup"><span data-stu-id="06f49-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="06f49-108">请在开具发票之前重新验证所有付款的状态。”</span><span class="sxs-lookup"><span data-stu-id="06f49-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="06f49-109">付款授权详细信息将包括以下错误消息：“Adyen 网关 SendRequest() 失败，状态为 'InternalServerError'.22144；从 Adyen 返回了空响应。(22001)；”</span><span class="sxs-lookup"><span data-stu-id="06f49-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![退货单上的拒绝退款错误](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="06f49-111">解决方法</span><span class="sxs-lookup"><span data-stu-id="06f49-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="06f49-112">在 Adyen 中启用盲目退款</span><span class="sxs-lookup"><span data-stu-id="06f49-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="06f49-113">要启用盲目退款，请执行[解决适用于 Adyen 的 Dynamics 365 付款连接器问题](adyen-support.md)中的步骤，与 Adyen 支持团队联系，并要求在您的 Adyen 商户帐户上启用盲目退款。</span><span class="sxs-lookup"><span data-stu-id="06f49-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06f49-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="06f49-114">Additional resources</span></span>

[<span data-ttu-id="06f49-115">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="06f49-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="06f49-116">设置适用于 Dynamics 365 的 Adyen 付款连接器</span><span class="sxs-lookup"><span data-stu-id="06f49-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
