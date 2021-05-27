---
title: 使用采购订单窗体和销售订单窗体计算 TDS 发票
description: 本主题列出了用于计算各种类型的发票的从源扣缴税款 (TDS) 的步骤。
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023048"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="176bd-103">使用采购订单窗体和销售订单窗体计算 TDS 发票</span><span class="sxs-lookup"><span data-stu-id="176bd-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="176bd-104">本主题列出了使用 **采购订单**、**采购日记帐**、**总订单** 和 **销售订单** 页面计算各种类型的发票的从源扣缴税款 (TDS) 的步骤。</span><span class="sxs-lookup"><span data-stu-id="176bd-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="176bd-105">使用列出的页面创建采购订单、采购日记帐、采购总订单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="176bd-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="176bd-106">输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="176bd-106">Enter the required details.</span></span>

2. <span data-ttu-id="176bd-107">选择 **设置** 选项卡以查看供应商或客户的评估对象的性质。</span><span class="sxs-lookup"><span data-stu-id="176bd-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="176bd-108">此信息在 **预缴税金组** 字段组下的 **评估对象的性质** 字段中列出。</span><span class="sxs-lookup"><span data-stu-id="176bd-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="176bd-109">在 **TDS 组** 字段中，查看或修改为供应商或客户定义的默认 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="176bd-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="176bd-110">在 **TDS 组** 字段中选择 TDS 组时，**TCS 组** 字段不可用。</span><span class="sxs-lookup"><span data-stu-id="176bd-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="176bd-111">如果为 **所有供应商** 或 **所有客户** 页面上的供应商或客户选中 **计算预缴税金** 复选框，将仅计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="176bd-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="176bd-112">在 **行** 选项卡上创建明细项，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="176bd-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="176bd-113">选择 **设置** 选项卡（行级别）以查看或更改在标头级别定义的 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="176bd-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="176bd-114">TDS 组显示在位于 **预缴税金组** 字段组下的 **TDS 组** 字段中。</span><span class="sxs-lookup"><span data-stu-id="176bd-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="176bd-115">选择 **税务信息** 选项卡，然后选择为此字段中显示的公司名称设置的备用地址。</span><span class="sxs-lookup"><span data-stu-id="176bd-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="176bd-116">公司名称显示在位于 **公司信息** 字段组下的 **名称** 字段中。</span><span class="sxs-lookup"><span data-stu-id="176bd-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="176bd-117">选定公司名称的 TAN 显示在 **预缴税金** 字段组下的 **税务帐号** (**TAN**) 字段中。</span><span class="sxs-lookup"><span data-stu-id="176bd-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="176bd-118">选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="176bd-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="176bd-119">查看 **临时预缴税金交易** 页面上方的窗格上的以下字段。</span><span class="sxs-lookup"><span data-stu-id="176bd-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="176bd-120">**预缴税金总金额** - 为 TDS 组的交易计算的总 TDS。</span><span class="sxs-lookup"><span data-stu-id="176bd-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="176bd-121">**值** - 用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="176bd-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="176bd-122">总百分比基于为附加到 TDS 组的 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="176bd-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="176bd-123">**调整后预缴税金总金额** - TDS 组中所有税码的调整后 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="176bd-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="176bd-124">**TDS** - 如果选择，TDS 组将附加到交易。</span><span class="sxs-lookup"><span data-stu-id="176bd-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="176bd-125">**临时预缴税金交易** 页面上的 **概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。</span><span class="sxs-lookup"><span data-stu-id="176bd-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="176bd-126">选择 **阈值** 以打开 **阈值** 页面。</span><span class="sxs-lookup"><span data-stu-id="176bd-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="176bd-127">在此页面上查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制。</span><span class="sxs-lookup"><span data-stu-id="176bd-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="176bd-128">选择 **公式设计器** 以打开 **公式设计器** 页面。</span><span class="sxs-lookup"><span data-stu-id="176bd-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="176bd-129">在此页面上查看为特定 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="176bd-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="176bd-130">过帐发票。</span><span class="sxs-lookup"><span data-stu-id="176bd-130">Post the invoice.</span></span> <span data-ttu-id="176bd-131">根据采购发票计算的 TDS 金额将过帐到应付帐款，根据销售发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。</span><span class="sxs-lookup"><span data-stu-id="176bd-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="176bd-132">TDS 税码的应付帐款或应收帐款在 **预缴税金代码** 页面上定义。</span><span class="sxs-lookup"><span data-stu-id="176bd-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="176bd-133">选择 **查询** 按钮 **> 发票 > 过帐的预缴税金** 按钮以打开 **预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="176bd-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="176bd-134">您可以在 **值** 字段中查看用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="176bd-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="176bd-135">**预缴税金交易** 页面上的 **概述**、**常规** 和 **金额** 选项卡上的字段显示为交易计算的 TDS 的信息。</span><span class="sxs-lookup"><span data-stu-id="176bd-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="176bd-136">查看附加到 TDS 组的每个 TDS 税码的 TDS 计算信息。</span><span class="sxs-lookup"><span data-stu-id="176bd-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
