---
title: 根据发票的 TDS 计算
description: 本主题提供有关在发票级别计算从源扣缴税款的交易的参考。
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
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023062"
---
# <a name="tds-calculation-on-invoices"></a><span data-ttu-id="7c512-103">根据发票的 TDS 计算</span><span class="sxs-lookup"><span data-stu-id="7c512-103">TDS calculation on invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c512-104">本主题提供有关在发票级别计算从源扣缴税款的交易的参考。</span><span class="sxs-lookup"><span data-stu-id="7c512-104">This topic provides a reference for transactions where the Tax Deducted at Source (TDS) is calculated at the invoice level.</span></span>

| <span data-ttu-id="7c512-105">序列号</span><span class="sxs-lookup"><span data-stu-id="7c512-105">Serial number</span></span> | <span data-ttu-id="7c512-106">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="7c512-106">Transaction type</span></span>                                 | <span data-ttu-id="7c512-107">交易记录金额</span><span class="sxs-lookup"><span data-stu-id="7c512-107">Transaction amount</span></span> | <span data-ttu-id="7c512-108">页面名称和选择路径</span><span class="sxs-lookup"><span data-stu-id="7c512-108">Page name and selection path</span></span>                                 | <span data-ttu-id="7c512-109">帐户类型和抵销帐户类型</span><span class="sxs-lookup"><span data-stu-id="7c512-109">Account type and offset account type</span></span>                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <span data-ttu-id="7c512-110">1.</span><span class="sxs-lookup"><span data-stu-id="7c512-110">1.</span></span>            | <span data-ttu-id="7c512-111">从供应商进行的购买/记录支出</span><span class="sxs-lookup"><span data-stu-id="7c512-111">Purchase made from vendor / recording expenses</span></span>   | <span data-ttu-id="7c512-112">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7c512-112">Debit  Or  Credit</span></span>  | <span data-ttu-id="7c512-113">普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票审核日记帐页面（应付帐款 > 发票 > 发票审核）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐）</span><span class="sxs-lookup"><span data-stu-id="7c512-113">General journals page (General ledger >  Journal entries > General journals), Invoice approval journal page (Accounts payable > Invoices > Invoice approval), Invoice journal page (Accounts payable >  Invoices > Invoice journal)</span></span> | <span data-ttu-id="7c512-114">分类帐 (Dr.) 供应商 (Cr.).</span><span class="sxs-lookup"><span data-stu-id="7c512-114">Ledger (Dr.)  Vendor (Cr.).</span></span>  <span data-ttu-id="7c512-115">仅在分类帐帐户具有过帐类型 **采购** - **现金** 时，才为供应商-分类帐组合计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="7c512-115">Withholding tax is calculated for the Vendor-Ledger  combination only when the Ledger account has the posting type **Purchase**  **cash**.</span></span> |
| <span data-ttu-id="7c512-116">2.</span><span class="sxs-lookup"><span data-stu-id="7c512-116">2.</span></span>            | <span data-ttu-id="7c512-117">从客户进行的购买/记录支出</span><span class="sxs-lookup"><span data-stu-id="7c512-117">Purchase made from customer / recording expenses</span></span> | <span data-ttu-id="7c512-118">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7c512-118">Debit  Or  Credit</span></span>  | <span data-ttu-id="7c512-119">普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐）</span><span class="sxs-lookup"><span data-stu-id="7c512-119">General journals page (General ledger >  Journal entries > General journals), Invoice journal page (Accounts payable >  Invoices > Invoice journal)</span></span> | <span data-ttu-id="7c512-120">分类帐 (Dr.) 客户 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7c512-120">Ledger (Dr.)  Customer (Cr.)</span></span>                                 |
| <span data-ttu-id="7c512-121">3.</span><span class="sxs-lookup"><span data-stu-id="7c512-121">3.</span></span>            | <span data-ttu-id="7c512-122">从供应商的固定资产的购买</span><span class="sxs-lookup"><span data-stu-id="7c512-122">Purchase of fixed asset from vendor</span></span>              | <span data-ttu-id="7c512-123">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7c512-123">Debit  Or  Credit</span></span>  | <span data-ttu-id="7c512-124">普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票登记薄日记帐页面（应付帐款 > 发票 > 发票登记簿）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐）</span><span class="sxs-lookup"><span data-stu-id="7c512-124">General journals page (General ledger >  Journal entries > General journals), Invoice register journal page (Accounts payable > Invoices > Invoice register), Invoice journal page (Accounts payable >  Invoices > Invoice journal)</span></span> | <span data-ttu-id="7c512-125">固定资产 (Dr.) 供应商 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7c512-125">Fixed assets (Dr.)  Vendor (Cr.)</span></span>                             |
| <span data-ttu-id="7c512-126">4.</span><span class="sxs-lookup"><span data-stu-id="7c512-126">4.</span></span>            | <span data-ttu-id="7c512-127">从客户的固定资产的购买</span><span class="sxs-lookup"><span data-stu-id="7c512-127">Purchase of fixed asset from customer</span></span>            | <span data-ttu-id="7c512-128">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7c512-128">Debit  Or  Credit</span></span>  | <span data-ttu-id="7c512-129">普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐）</span><span class="sxs-lookup"><span data-stu-id="7c512-129">General journals page (General ledger >  Journal entries > General journals), Invoice journal page (Accounts payable >  Invoices > Invoice journal)</span></span> | <span data-ttu-id="7c512-130">固定资产 (Dr.) 客户 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7c512-130">Fixed assets (Dr.)  Customer (Cr.)</span></span>                           |
| <span data-ttu-id="7c512-131">5</span><span class="sxs-lookup"><span data-stu-id="7c512-131">5.</span></span>            | <span data-ttu-id="7c512-132">采购发票（应付 TDS）</span><span class="sxs-lookup"><span data-stu-id="7c512-132">Purchase invoice  (TDS payable)</span></span>                  |                    | <span data-ttu-id="7c512-133">采购订单页面（应付帐款 > 采购订单 > 所有采购订单）</span><span class="sxs-lookup"><span data-stu-id="7c512-133">Purchase order page (Accounts payable > Purchase orders > All purchase orders)</span></span> |                                                              |
| <span data-ttu-id="7c512-134">6</span><span class="sxs-lookup"><span data-stu-id="7c512-134">6.</span></span>            | <span data-ttu-id="7c512-135">销售发票（应收 TDS）</span><span class="sxs-lookup"><span data-stu-id="7c512-135">Sales invoice  (TDS receivable)</span></span>                  |                    | <span data-ttu-id="7c512-136">销售订单页面（应收帐款 > 订单 > 所有销售订单）、普通发票页面（应收帐款 > 发票 > 所有普通发票）</span><span class="sxs-lookup"><span data-stu-id="7c512-136">Sales order page (Accounts receivable > Orders > All sales orders), Free text invoice page (Accounts receivable > Invoices > All free text invoices)</span></span> |                                                              |
