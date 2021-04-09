---
title: 设置付款发票方案
description: 本主题将介绍如何配置 Dynamics 365 Commerce 以支持与发票付款相关的各种方案。
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804545"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="0032b-103">设置付款发票方案</span><span class="sxs-lookup"><span data-stu-id="0032b-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0032b-104">Dynamics 365 Commerce 中的“付款发票”功能已扩展为支持：</span><span class="sxs-lookup"><span data-stu-id="0032b-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="0032b-105">单一 POS 交易中多个销售订单发票的结算。</span><span class="sxs-lookup"><span data-stu-id="0032b-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="0032b-106">各种客户发票类型的支付，包括普通发票、基于项目的发票和贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="0032b-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="0032b-107">要启用这些方案，必须按如下所述配置商店的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="0032b-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="0032b-108">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，然后选择与您要更改的商店关联的配置文件。</span><span class="sxs-lookup"><span data-stu-id="0032b-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="0032b-109">在 **功能** 选项卡上，根据需要配置以下参数。</span><span class="sxs-lookup"><span data-stu-id="0032b-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="0032b-110">**销售订单发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个基于销售订单的发票。</span><span class="sxs-lookup"><span data-stu-id="0032b-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0032b-111">**普通发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个普通发票。</span><span class="sxs-lookup"><span data-stu-id="0032b-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0032b-112">**项目发票** - 选择 **是** 以允许用户在单一 POS 交易中支付一个或多个基于项目的发票。</span><span class="sxs-lookup"><span data-stu-id="0032b-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0032b-113">**销售订单贷方通知单** - 选择 **是** 以允许用户针对未结发票结算多个基于销售订单的贷方通知单，或者向未结贷方通知单的客户处理退款。</span><span class="sxs-lookup"><span data-stu-id="0032b-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="0032b-114">尚不支持对部分金额进行支付或结算。</span><span class="sxs-lookup"><span data-stu-id="0032b-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]