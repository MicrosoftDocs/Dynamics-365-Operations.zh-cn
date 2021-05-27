---
title: 从普通发票页面中根据发票的 TDS 计算
description: 本主题说明如何使用普通发票页面根据发票计算从源扣缴税款 (TDS)。
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023064"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="98e17-103">从普通发票页面中根据发票的 TDS 计算</span><span class="sxs-lookup"><span data-stu-id="98e17-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98e17-104">本主题说明如何使用 **普通发票** 页面根据发票计算从源扣缴税款 (TDS)。</span><span class="sxs-lookup"><span data-stu-id="98e17-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="98e17-105">转到 **应收帐款 \> 发票 \> 所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="98e17-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="98e17-106">[![普通发票页面](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="98e17-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="98e17-107">选择 **新建** 以创建普通发票，并输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="98e17-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="98e17-108">选择 **发票** 选项卡。在 **预缴税金组** 部分中，**评估对象的性质** 字段显示客户的评估对象类别的性质。</span><span class="sxs-lookup"><span data-stu-id="98e17-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="98e17-109">在 **TDS 组** 字段中，查看或更改为客户定义的默认 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="98e17-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="98e17-110">当在 **TDS 组** 字段中选择值时，**TCS 组** 字段变得不可用。</span><span class="sxs-lookup"><span data-stu-id="98e17-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="98e17-111">仅在 **所有客户** 页面上为客户将 **计算预缴税金** 选项设置为 **是** 时，才计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="98e17-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="98e17-112">在 **税务信息** 选项卡的 **公司信息** 部分中，在 **名称** 字段中，针对已为公司设置的备用地址选择公司名称。</span><span class="sxs-lookup"><span data-stu-id="98e17-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="98e17-113">在 **预缴税金** 部分中，**税务帐号 (TAN)** 字段显示选定公司的税务帐号 (TAN)。</span><span class="sxs-lookup"><span data-stu-id="98e17-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="98e17-114">在 **发票行** 选项卡上，创建发票行，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="98e17-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="98e17-115">在 **预缴税金组** 部分中，**税务帐号 (TAN)** 字段显示 TAN，**TDS 组** 字段显示 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="98e17-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="98e17-116">选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="98e17-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="98e17-117">此页面的上部具有以下字段：</span><span class="sxs-lookup"><span data-stu-id="98e17-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="98e17-118">**预缴税金总金额** – 已为 TDS 组的交易计算的总 TDS。</span><span class="sxs-lookup"><span data-stu-id="98e17-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="98e17-119">**值** – 已用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="98e17-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="98e17-120">总百分比基于为 TDS 税码定义和附加到 TDS 组的公式。</span><span class="sxs-lookup"><span data-stu-id="98e17-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="98e17-121">**调整后预缴税金总金额** – TDS 组中所有税码的调整后 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="98e17-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="98e17-122">**TDS** – 选中的复选框指示 TDS 组已附加到交易。</span><span class="sxs-lookup"><span data-stu-id="98e17-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="98e17-123">**概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。</span><span class="sxs-lookup"><span data-stu-id="98e17-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="98e17-124">选择 **阈值** 以打开 **阈值** 页面，您可以在该页面中查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制。</span><span class="sxs-lookup"><span data-stu-id="98e17-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="98e17-125">选择 **公式设计器** 以打开 **公式设计器** 页面，您可以在该页面中查看为特定 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="98e17-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="98e17-126">过帐普通发票。</span><span class="sxs-lookup"><span data-stu-id="98e17-126">Post the free text invoice.</span></span> <span data-ttu-id="98e17-127">为普通发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。</span><span class="sxs-lookup"><span data-stu-id="98e17-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="98e17-128">TDS 税码的应收帐款在 **预缴税金代码** 页面上定义。</span><span class="sxs-lookup"><span data-stu-id="98e17-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="98e17-129">选择 **过帐的预缴税金** 以打开 **预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="98e17-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="98e17-130">**值** 字段显示用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="98e17-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="98e17-131">**概述**、**常规** 和 **金额** 选项卡上的字段显示已针对发票行计算的 TDS 金额。</span><span class="sxs-lookup"><span data-stu-id="98e17-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="98e17-132">查看附加到 TDS 组的每个 TDS 税码的 TDS 计算信息。</span><span class="sxs-lookup"><span data-stu-id="98e17-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
