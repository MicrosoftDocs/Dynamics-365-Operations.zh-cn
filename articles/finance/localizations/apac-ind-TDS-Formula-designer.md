---
title: TDS 计算的公式设计器
description: 本主题提供了如何基于为附加到交易的 TDS 组中每个 TDS 税码定义的公式计算从源扣缴税款 (TDS) 的示例。
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
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023049"
---
# <a name="formula-designer-for-tds-calculations"></a><span data-ttu-id="0f2ba-103">TDS 计算的公式设计器</span><span class="sxs-lookup"><span data-stu-id="0f2ba-103">Formula designer for TDS calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f2ba-104">本主题提供了如何基于为每个 TDS 税码定义的公式计算从源扣缴税款 (TDS) 的示例。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-104">This topic provides an example of how Tax Deducted at Source (TDS) is calculated based on the formula defined for each TDS tax code.</span></span> <span data-ttu-id="0f2ba-105">TDS 税码在附加到交易的 TDS 组中定义。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-105">TDS tax codes are defined in the TDS group that's attached to the transaction.</span></span> <span data-ttu-id="0f2ba-106">在设计 TDS 公式之前，请完成 TDS 所需的基本设置，如以下步骤所示。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-106">Before designing TDS formulas, complete the basic setup required for TDS as listed in the following steps.</span></span> 

- <span data-ttu-id="0f2ba-107">使用 **预缴税金组分组** 页面设置 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-107">Set up TDS component groups using the **Withholding tax component groups** page.</span></span> 
- <span data-ttu-id="0f2ba-108">使用 **预缴税金组分** 页面设置 TDS 组分，并将 TDS 组分组附加到 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-108">Set up TDS components and attach TDS component group to the TDS components using the **Withholding tax components** page.</span></span> 
- <span data-ttu-id="0f2ba-109">使用 **预缴税金代码** 页面设置 TDS 税码，并将 TDS 组分附加到 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-109">Set up TDS tax codes and attach TDS components to the tax codes using the **Withholding tax codes** page.</span></span> 
- <span data-ttu-id="0f2ba-110">使用 **预缴税金组** 页面设置 TDS 税组。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-110">Set up TDS tax groups using the **Withholding tax groups** page.</span></span> <span data-ttu-id="0f2ba-111">然后，使用 **公式设计器** 页面将 TDS 税码附加到税组，并定义公式。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-111">Then attach the TDS tax codes to the tax group, and define the formula, using the **Formula designer** page.</span></span> 

<span data-ttu-id="0f2ba-112">**公式示例**</span><span class="sxs-lookup"><span data-stu-id="0f2ba-112">**Example formula**</span></span>

<span data-ttu-id="0f2ba-113">在此示例中，TDS 组“租金”将附加到为供应商 A 创建的采购发票。发票金额为 $100,000。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-113">In this example, the TDS group, Rent, is attached to a purchase invoice that's created for vendor A. The invoice amount is $100,000.</span></span> <span data-ttu-id="0f2ba-114">请参考下表以查看发票的 TDS 计算。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-114">Refer to the following table to view the TDS calculation for the invoice.</span></span>

| <span data-ttu-id="0f2ba-115">TDS 组</span><span class="sxs-lookup"><span data-stu-id="0f2ba-115">TDS  group</span></span>                                                   | <span data-ttu-id="0f2ba-116">已附加到 TDS 组的 TDS 税码</span><span class="sxs-lookup"><span data-stu-id="0f2ba-116">TDS tax codes attached to the TDS group</span></span> | <span data-ttu-id="0f2ba-117">值</span><span class="sxs-lookup"><span data-stu-id="0f2ba-117">Value</span></span>              | <span data-ttu-id="0f2ba-118">应纳税基数（公式设计器）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-118">Taxable basis  (Formula designer)</span></span> | <span data-ttu-id="0f2ba-119">计算表达式（公式设计器）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-119">Calculation expression  (Formula designer)</span></span> | <span data-ttu-id="0f2ba-120">基准额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-120">Base amount</span></span> | <span data-ttu-id="0f2ba-121">计算的 TDS 金额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-121">Calculated TDS amount</span></span> |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| <span data-ttu-id="0f2ba-122">租金</span><span class="sxs-lookup"><span data-stu-id="0f2ba-122">Rent</span></span>                                                         | <span data-ttu-id="0f2ba-123">TDS（TDS 组分-TDS）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-123">TDS  (TDS component-TDS)</span></span>                | <span data-ttu-id="0f2ba-124">10%</span><span class="sxs-lookup"><span data-stu-id="0f2ba-124">10%</span></span>                | <span data-ttu-id="0f2ba-125">总额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-125">Gross amount</span></span>                      |                                            | <span data-ttu-id="0f2ba-126">100,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-126">100,000</span></span>      | <span data-ttu-id="0f2ba-127">10,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-127">10,000</span></span>                 |
| <span data-ttu-id="0f2ba-128">附加费（TDS 组分-附加费）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-128">Surcharge  (TDS component-Surcharge)</span></span>                         | <span data-ttu-id="0f2ba-129">10%</span><span class="sxs-lookup"><span data-stu-id="0f2ba-129">10%</span></span>                                     | <span data-ttu-id="0f2ba-130">不含总额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-130">Excl. gross amount</span></span> | <span data-ttu-id="0f2ba-131">+TDS</span><span class="sxs-lookup"><span data-stu-id="0f2ba-131">+TDS</span></span>                              |                   <span data-ttu-id="0f2ba-132">10000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-132">10000</span></span>                    | <span data-ttu-id="0f2ba-133">1,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-133">1,000</span></span>        |                       |
| <span data-ttu-id="0f2ba-134">PE-Cess（TDS 组分-PE-Cess）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-134">PE-Cess  (TDS component- PE-Cess)</span></span>                            | <span data-ttu-id="0f2ba-135">2%</span><span class="sxs-lookup"><span data-stu-id="0f2ba-135">2%</span></span>                                      | <span data-ttu-id="0f2ba-136">不含总额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-136">Excl. gross amount</span></span> | <span data-ttu-id="0f2ba-137">+TDS+附加费</span><span class="sxs-lookup"><span data-stu-id="0f2ba-137">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="0f2ba-138">11000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-138">11000</span></span>                    | <span data-ttu-id="0f2ba-139">220</span><span class="sxs-lookup"><span data-stu-id="0f2ba-139">220</span></span>         |                       |
| <span data-ttu-id="0f2ba-140">SHE Cess（TDS 组分-SHE Cess）</span><span class="sxs-lookup"><span data-stu-id="0f2ba-140">SHE Cess  (TDS component- SHE Cess)</span></span>                          | <span data-ttu-id="0f2ba-141">1%</span><span class="sxs-lookup"><span data-stu-id="0f2ba-141">1%</span></span>                                      | <span data-ttu-id="0f2ba-142">不含总额</span><span class="sxs-lookup"><span data-stu-id="0f2ba-142">Excl. gross amount</span></span> | <span data-ttu-id="0f2ba-143">+TDS+附加费</span><span class="sxs-lookup"><span data-stu-id="0f2ba-143">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="0f2ba-144">11000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-144">11000</span></span>                    | <span data-ttu-id="0f2ba-145">110</span><span class="sxs-lookup"><span data-stu-id="0f2ba-145">110</span></span>         |                       |
| <span data-ttu-id="0f2ba-146">**针对发票计算的总 TDS**</span><span class="sxs-lookup"><span data-stu-id="0f2ba-146">**Total** **TDS**  **calculated** **for** **the** **invoice**</span></span> | <span data-ttu-id="0f2ba-147">**11,330**</span><span class="sxs-lookup"><span data-stu-id="0f2ba-147">**11,330**</span></span>                               |                    |                                   |                                            |             |                       |

<span data-ttu-id="0f2ba-148">创建凭证条目，如下所示。</span><span class="sxs-lookup"><span data-stu-id="0f2ba-148">The voucher entries are created as follows.</span></span>

| <span data-ttu-id="0f2ba-149">科目</span><span class="sxs-lookup"><span data-stu-id="0f2ba-149">Account</span></span>           | <span data-ttu-id="0f2ba-150">借记</span><span class="sxs-lookup"><span data-stu-id="0f2ba-150">Debit</span></span>  | <span data-ttu-id="0f2ba-151">信用</span><span class="sxs-lookup"><span data-stu-id="0f2ba-151">Credit</span></span> |
| ----------------- | ------ | ------ |
| <span data-ttu-id="0f2ba-152">租金</span><span class="sxs-lookup"><span data-stu-id="0f2ba-152">Rent</span></span>              | <span data-ttu-id="0f2ba-153">100,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-153">100,000</span></span> |        |
| <span data-ttu-id="0f2ba-154">供应商 A</span><span class="sxs-lookup"><span data-stu-id="0f2ba-154">Vendor A</span></span>          |        | <span data-ttu-id="0f2ba-155">100,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-155">100,000</span></span> |
| <span data-ttu-id="0f2ba-156">供应商 A</span><span class="sxs-lookup"><span data-stu-id="0f2ba-156">Vendor A</span></span>          | <span data-ttu-id="0f2ba-157">11,330</span><span class="sxs-lookup"><span data-stu-id="0f2ba-157">11,330</span></span>  |        |
| <span data-ttu-id="0f2ba-158">应付 TDS</span><span class="sxs-lookup"><span data-stu-id="0f2ba-158">TDS payable</span></span>       |        | <span data-ttu-id="0f2ba-159">10,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-159">10,000</span></span>  |
| <span data-ttu-id="0f2ba-160">应付附加费</span><span class="sxs-lookup"><span data-stu-id="0f2ba-160">Surcharge payable</span></span> |        | <span data-ttu-id="0f2ba-161">1,000</span><span class="sxs-lookup"><span data-stu-id="0f2ba-161">1,000</span></span>   |
| <span data-ttu-id="0f2ba-162">应付 PE-Cess</span><span class="sxs-lookup"><span data-stu-id="0f2ba-162">PE-Cess payable</span></span>   |        | <span data-ttu-id="0f2ba-163">220</span><span class="sxs-lookup"><span data-stu-id="0f2ba-163">220</span></span>    |
| <span data-ttu-id="0f2ba-164">应付 SHE Cess</span><span class="sxs-lookup"><span data-stu-id="0f2ba-164">SHE Cess payable</span></span>  |        | <span data-ttu-id="0f2ba-165">110</span><span class="sxs-lookup"><span data-stu-id="0f2ba-165">110</span></span>    |
