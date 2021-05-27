---
title: 阈值限制和异常阈值限制
description: 本主题介绍了从源扣缴税款 (TDS) 的阈值和异常限制。
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
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023052"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a><span data-ttu-id="5c556-103">阈值限制和异常阈值限制</span><span class="sxs-lookup"><span data-stu-id="5c556-103">Threshold limit and exception threshold limit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c556-104">本主题介绍了从源扣缴税款 (TDS) 的阈值和异常限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-104">This topic describes the threshold and exception limits for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="5c556-105">在针对发票和付款计算 TDS 时，始终考虑在 **预缴税金组分** 页面上为 TDS 税种组分定义的阈值限制和异常阈值限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-105">The TDS on invoices and payments is always calculated considering the threshold limit and exception threshold limit defined for the TDS tax components on the **Withholding tax components** page.</span></span> <span data-ttu-id="5c556-106">TDS 税种组分附加到包括在 TDS 税组中的 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="5c556-106">The TDS tax components are attached to TDS tax codes, which are included in the TDS tax groups.</span></span> <span data-ttu-id="5c556-107">TDS 税组附加到供应商和客户，以在发票级别或付款级别计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-107">The TDS tax groups are attached to vendors and customers to calculate TDS at the invoice-level or payment-level.</span></span>

<span data-ttu-id="5c556-108">如果通过供应商的特定 TDS 组过帐的交易或累计交易的金额超过在 **预缴税金组分** 页面上指定的阈值限制，将计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-108">TDS is calculated if the amount for a transaction or the cumulative transactions posted with a specific TDS group for a vendor exceeds the threshold limit specified on the **Withholding tax components** page.</span></span> <span data-ttu-id="5c556-109">在累计交易金额超过指定的阈值限制之前，不会计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-109">TDS will not be calculated until the cumulative transaction amount exceeds the specified threshold limit.</span></span>

<span data-ttu-id="5c556-110">如果同时指定了异常阈值限制和 TDS 组分的阈值限制，当特定交易金额超过异常阈值限制时，即使累计交易金额未超过指定的阈值限制，也会计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-110">If an exception threshold limit is specified along with the threshold limit for a TDS component, TDS is calculated when a specific transaction amount exceeds the exception threshold limit even if the cumulative transaction amount does not exceed the specified threshold limit.</span></span>

### <a name="example"></a><span data-ttu-id="5c556-111">示例</span><span class="sxs-lookup"><span data-stu-id="5c556-111">Example</span></span>
<span data-ttu-id="5c556-112">称为 TDS 的税种组分将设置并附加到称为合同工的 TDS 税组。</span><span class="sxs-lookup"><span data-stu-id="5c556-112">A tax component called TDS is set up and attached to the TDS tax group called Contractor.</span></span> <span data-ttu-id="5c556-113">对于 TDS 税种组分，阈值已定义为 50,000，异常阈值已定义为 20,000。</span><span class="sxs-lookup"><span data-stu-id="5c556-113">The threshold has been defined as 50,000 and exception threshold has been defined as 20,000 for TDS tax component.</span></span> <span data-ttu-id="5c556-114">对于供应商 1，TDS 组合同工将定义为默认的 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="5c556-114">The TDS group contractor is defined as the default TDS group for vendor 1.</span></span>

<span data-ttu-id="5c556-115">对于供应商 1，将为 10000 过帐采购发票 001。</span><span class="sxs-lookup"><span data-stu-id="5c556-115">A purchase invoice 001 is posted for vendor 1 for 10000.</span></span> <span data-ttu-id="5c556-116">不计算发票的 TDS，因为发票金额未超过阈值限制或异常阈值限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-116">TDS is not calculated for the invoice because the invoice amount has not crossed the threshold limit or exception threshold limit.</span></span> <span data-ttu-id="5c556-117">对于供应商 1，将为 25,000 过帐采购发票 002。</span><span class="sxs-lookup"><span data-stu-id="5c556-117">A purchase invoice 002 is posted for vendor 1 for 25,000.</span></span> <span data-ttu-id="5c556-118">计算发票的 TDS，因为发票金额已超过异常阈值限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-118">TDS is calculated for the invoice because the invoice amount has crossed the exception threshold limit.</span></span> <span data-ttu-id="5c556-119">对于供应商 1，将为 20,000 过帐采购发票 003。</span><span class="sxs-lookup"><span data-stu-id="5c556-119">A purchase invoice 003 is posted for Vendor 1 for 20,000.</span></span> <span data-ttu-id="5c556-120">计算发票的 TDS，因为为供应商签发的三个发票的发票总金额已超过阈值限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-120">TDS is calculated for the invoice because the total invoice amount of the three invoices that are issued for the vendor has crossed the threshold limit.</span></span> <span data-ttu-id="5c556-121">根据为供应商签发的之前尚未计算 TDS 的所有发票计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-121">TDS is calculated on all invoices that are issued for the vendor on which the TDS has not been calculated earlier.</span></span> <span data-ttu-id="5c556-122">因此，根据 30,000 计算 TDS，这是发票 001 和 003 的发票总金额。</span><span class="sxs-lookup"><span data-stu-id="5c556-122">Therefore, TDS is calculated on 30,000, which is the total invoice amount of invoice 001 and 003.</span></span>

<span data-ttu-id="5c556-123">如果对于附加到交易的 TDS 组中的 TDS 税码选中 **忽略阈值** 复选框，则在计算 TDS 时不考虑阈值限制和异常阈值限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-123">The threshold limit and exception threshold limit are not considered for the TDS calculation if the **Overlook threshold** check box is selected for TDS tax codes in the TDS group that is attached to the transaction.</span></span> <span data-ttu-id="5c556-124">将不在选中了 **忽略阈值** 复选框的 TDS 组的 TDS 税码中使用异常限制。</span><span class="sxs-lookup"><span data-stu-id="5c556-124">The threshold limit won't be used in the TDS tax codes in the TDS group that the **Overlook threshold** check box is for.</span></span>

<span data-ttu-id="5c556-125">如果针对某些发票的特定 TDS 组，但不针对已为特定供应商/客户创建的其他发票选中 **忽略阈值** 复选框，考虑到之前尚未计算 TDS 的所有发票的累计金额，可能会在不忽略少数发票的阈值限制的情况下计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-125">If the **Overlook threshold** check box is selected for a specific TDS group for some invoices, but not selected for other invoices that were created for a specific vendor/customer, the calculation of TDS without overlooking the threshold limit for few invoices may take place considering the cumulative amount on all invoices on which TDS hasn't been calculated earlier.</span></span>

<span data-ttu-id="5c556-126">例如，阈值限制为 25000。</span><span class="sxs-lookup"><span data-stu-id="5c556-126">For example, the threshold limit is 25000.</span></span> <span data-ttu-id="5c556-127">为供应商 A 创建以下发票。</span><span class="sxs-lookup"><span data-stu-id="5c556-127">The following invoices are created for Vendor A.</span></span>

- <span data-ttu-id="5c556-128">发票 1 – 2,0000 –（未选中 **忽略阈值** 复选框）：不计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-128">Invoice 1 – 2,0000 – (**Overlook threshold** check box is not selected): TDS is not calculated.</span></span>

- <span data-ttu-id="5c556-129">发票 2 – 4,000 –（选中 **忽略阈值** 复选框）：根据 4,000 计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-129">Invoice 2 – 4,000 – (**Overlook threshold** check box is selected): TDS is calculated on 4,000.</span></span>

- <span data-ttu-id="5c556-130">发票 2 – 3,000 –（未选中 **忽略阈值**）：当累计发票金额 27,000 (20000+4000+3000) 超过阈值限制时计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-130">Invoice 2 – 3,000 – (**Overlook threshold** check box is not selected): TDS is calculated as the cumulative invoice amount, that is, 27,000 (20000+4000+3000) exceeded the threshold limit.</span></span> <span data-ttu-id="5c556-131">针对之前尚未计算 TDS 的累计发票金额 23,000 (20000+3000) 计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="5c556-131">TDS is calculated on the cumulative amount of invoices on which the TDS has not been calculated earlier, that is, 23,000 (20000+3000).</span></span>
