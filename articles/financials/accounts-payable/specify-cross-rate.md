---
title: 指定交叉汇率
description: 此主题提供有关 Microsoft Dynamics 365 for Finance and Operations 中交叉汇率的一般信息。
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c2cba3ed655e2b4b1ada75bdbb5f01c300b25a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834527"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="04087-103">指定交叉汇率</span><span class="sxs-lookup"><span data-stu-id="04087-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04087-104">本主题说明了交叉汇率的目的，以及当您使用发票结算付款时如何指定交叉汇率。</span><span class="sxs-lookup"><span data-stu-id="04087-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="04087-105">在适用以下所有条件时使用交叉汇率：</span><span class="sxs-lookup"><span data-stu-id="04087-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="04087-106">您正在使用发票结算付款。</span><span class="sxs-lookup"><span data-stu-id="04087-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="04087-107">付款行和发票行使用不同币种。</span><span class="sxs-lookup"><span data-stu-id="04087-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="04087-108">两种货币均不是记帐币种。</span><span class="sxs-lookup"><span data-stu-id="04087-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="04087-109">交叉汇率不用于计算付款交易记录币种与付款记帐币种之间的转换。</span><span class="sxs-lookup"><span data-stu-id="04087-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="04087-110">而是检索汇率表中的汇率以计算付款交易记录币种金额和付款记帐币种金额的值。</span><span class="sxs-lookup"><span data-stu-id="04087-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="04087-111">例如，记帐币种是 USD，发票币种是 CAD，而付款币种是 EUR。</span><span class="sxs-lookup"><span data-stu-id="04087-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="04087-112">交叉汇率使得您可以输入汇率直接在 CAD 和 EUR 之间换算而不需要通过 USD 为单位来转换。</span><span class="sxs-lookup"><span data-stu-id="04087-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="04087-113">在您选择某一发票和主付款时，可为该发票行输入交叉汇率。</span><span class="sxs-lookup"><span data-stu-id="04087-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="04087-114">交叉汇率是截止到结算日期时这些交易记录的币种之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="04087-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="04087-115">访问以下页面之一：</span><span class="sxs-lookup"><span data-stu-id="04087-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="04087-116">**应收帐款 > 通用 > 客户 > 所有客户**</span><span class="sxs-lookup"><span data-stu-id="04087-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="04087-117">**应付帐款 > 通用 > 供应商 > 所有供应商**</span><span class="sxs-lookup"><span data-stu-id="04087-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="04087-118">**采购 > 通用 > 供应商 > 所有供应商**</span><span class="sxs-lookup"><span data-stu-id="04087-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="04087-119">选择您要结算其未结交易记录的客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="04087-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="04087-120">对于客户，在**所有客户**列表页上，转至**催款 > 结算未结交易记录**。</span><span class="sxs-lookup"><span data-stu-id="04087-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="04087-121">对于供应商，则在**所有供应商**列表页上，转至**发票 > 结算未结交易记录**。</span><span class="sxs-lookup"><span data-stu-id="04087-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="04087-122">选择作为主付款的交易记录，然后单击**标记付款**。</span><span class="sxs-lookup"><span data-stu-id="04087-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="04087-123">**标记**列中的复选框被选中，并且在**主付款**列中将出现信息图标。</span><span class="sxs-lookup"><span data-stu-id="04087-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="04087-124">在**交叉汇率**字段中，输入截止到结算日期时发票币种和付款币种之间的汇率倍数。</span><span class="sxs-lookup"><span data-stu-id="04087-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
