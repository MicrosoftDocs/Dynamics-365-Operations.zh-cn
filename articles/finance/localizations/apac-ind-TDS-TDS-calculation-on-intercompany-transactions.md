---
title: 根据内部公司交易的 TDS 计算
description: 本主题介绍了用于根据内部公司交易分阶段计算从源扣缴税款 (TDS) 的流程。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023061"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="95653-103">根据内部公司交易的 TDS 计算</span><span class="sxs-lookup"><span data-stu-id="95653-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95653-104">本主题介绍了用于根据内部公司交易分阶段计算从源扣缴税款 (TDS) 的流程。</span><span class="sxs-lookup"><span data-stu-id="95653-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="95653-105">创建内部公司采购订单或销售订单时，将使用为客户或供应商定义的默认 TDS 组计算 TDS 金额。</span><span class="sxs-lookup"><span data-stu-id="95653-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="95653-106">在过帐发票后，TDS 金额将过帐到可退税帐户或应付帐款。</span><span class="sxs-lookup"><span data-stu-id="95653-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="95653-107">将自动为原始采购订单或销售订单创建内部公司销售订单或采购订单。</span><span class="sxs-lookup"><span data-stu-id="95653-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="95653-108">默认 TDS 组显示在内部公司订单上，以便可以计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="95653-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="95653-109">您可以更改 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="95653-109">You can change the TDS group.</span></span> <span data-ttu-id="95653-110">仅在自动创建的内部公司订单上的净发票金额与原始订单上的净发票金额匹配时，才可以过帐发票。</span><span class="sxs-lookup"><span data-stu-id="95653-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="95653-111">（净额是扣除 TDS 之后的发票金额。）</span><span class="sxs-lookup"><span data-stu-id="95653-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="95653-112">例如，为 50,000 创建一个销售发票，并向其附加 **10%** TDS 组。</span><span class="sxs-lookup"><span data-stu-id="95653-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="95653-113">过帐的发票金额是 45,000，销售发票的过帐的 TDS 金额是 5,000。</span><span class="sxs-lookup"><span data-stu-id="95653-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="95653-114">将自动为内部公司销售订单创建采购订单，并向其附加 **10%** TDS 组。</span><span class="sxs-lookup"><span data-stu-id="95653-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="95653-115">如果将 TDS 组更改为 **15%**，则不能过帐发票，因为自动创建的内部公司销售订单的净发票金额与原始销售订单的净发票金额不匹配。</span><span class="sxs-lookup"><span data-stu-id="95653-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="95653-116">将自动过帐为内部公司发票创建的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="95653-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="95653-117">仅在付款日记帐上的净付款金额与原始付款日记帐上的净付款金额匹配时，才可以过帐该付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="95653-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
