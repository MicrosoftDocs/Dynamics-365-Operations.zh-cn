---
title: 使用日记帐计算发票的 TDS
description: 本主题列出了使用日记帐计算从源扣缴税款 (TDS) 的步骤。
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023072"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="1b280-103">使用日记帐计算发票的 TDS</span><span class="sxs-lookup"><span data-stu-id="1b280-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b280-104">本主题列出了使用日记帐计算从源扣缴税款 (TDS) 的步骤。</span><span class="sxs-lookup"><span data-stu-id="1b280-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="1b280-105">首先，打开 **普通日记帐** 页面（**总帐 > 日记帐条目 > 总帐**）。</span><span class="sxs-lookup"><span data-stu-id="1b280-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="1b280-106">[![普通日记帐](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="1b280-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="1b280-107">使用表中列出的日记帐表单创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="1b280-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="1b280-108">选择帐户类型和抵销帐户类型，然后输入交易金额。</span><span class="sxs-lookup"><span data-stu-id="1b280-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="1b280-109">在 **发票审核日记帐** 页面上，选择 **查找凭证**，然后选择要计算 TDS 的发票。</span><span class="sxs-lookup"><span data-stu-id="1b280-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="1b280-110">查看在 **发票登记簿** 页面或 **查找凭证** 页面中创建的发票。</span><span class="sxs-lookup"><span data-stu-id="1b280-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="1b280-111">在 **日记帐凭证** 页面的 **常规** 选项卡上，在 **TDS 组** 字段中查看或修改为供应商或客户定义的默认 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="1b280-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="1b280-112">在日记帐行上计算的 TDS 金额基于为在 **TDS 组** 字段中列出的 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="1b280-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="1b280-113">当在 **TDS 组** 字段中选择 TDS 组时，**预缴税金组** 字段和 **TCS 组** 字段变得不可用。</span><span class="sxs-lookup"><span data-stu-id="1b280-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="1b280-114">**预缴税金组** 字段仅在 **普通日记帐** 页面上可用。</span><span class="sxs-lookup"><span data-stu-id="1b280-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="1b280-115">如果为 **所有供应商** 或 **所有客户** 页面上的供应商或客户选中 **计算预缴税金** 复选框，将仅计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="1b280-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="1b280-116">选择 **税务信息** 选项卡。根据需要选择为此字段中的公司设置的公司备用地址。</span><span class="sxs-lookup"><span data-stu-id="1b280-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="1b280-117">您可以在位于 **公司信息** 字段组下的 **名称** 字段中查看公司名称。</span><span class="sxs-lookup"><span data-stu-id="1b280-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="1b280-118">在位于 **预缴税金** 字段组下的 **评估对象的性质** 字段中查看供应商或客户的评估对象类别的性质。</span><span class="sxs-lookup"><span data-stu-id="1b280-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="1b280-119">在 **税务帐号** (**TAN**) 字段中，查看显示的选定公司名称的 TAN。</span><span class="sxs-lookup"><span data-stu-id="1b280-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="1b280-120">在 **预缴税金** 菜单中选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b280-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="1b280-121">以下字段显示在 **临时预缴税金交易** 页面上方的窗格上。</span><span class="sxs-lookup"><span data-stu-id="1b280-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="1b280-122">**预缴税金总金额** - 为 TDS 组的交易计算的总 TDS。</span><span class="sxs-lookup"><span data-stu-id="1b280-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="1b280-123">**值** - 用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="1b280-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="1b280-124">总百分比基于为附加到 TDS 组的 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="1b280-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="1b280-125">**调整后预缴税金总金额** - TDS 组中所有税码的调整后 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="1b280-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="1b280-126">**TDS** - 如果选择，TDS 组将附加到交易。</span><span class="sxs-lookup"><span data-stu-id="1b280-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="1b280-127">**临时预缴税金交易** 页面上的 **概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。</span><span class="sxs-lookup"><span data-stu-id="1b280-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="1b280-128">选择 **阈值** 以打开 **阈值** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b280-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="1b280-129">在此页面上查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制和异常阈值限制。</span><span class="sxs-lookup"><span data-stu-id="1b280-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="1b280-130">选择 **公式设计器** 以打开 **公式设计器** 窗体。</span><span class="sxs-lookup"><span data-stu-id="1b280-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="1b280-131">在此页面中查看为特定 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="1b280-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="1b280-132">关闭 **公式设计器** 和 **临时预缴税金交易** 页面以返回到 **日记帐凭证** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b280-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="1b280-133">输入其他所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1b280-133">Enter the other required details.</span></span> <span data-ttu-id="1b280-134">验证和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="1b280-134">Validate and post the journal.</span></span> <span data-ttu-id="1b280-135">根据采购发票计算的 TDS 金额将过帐到应付帐款。</span><span class="sxs-lookup"><span data-stu-id="1b280-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="1b280-136">根据销售发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。</span><span class="sxs-lookup"><span data-stu-id="1b280-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="1b280-137">TDS 税码的应付帐款或应收帐款在 **预缴税金代码** 页面上定义。</span><span class="sxs-lookup"><span data-stu-id="1b280-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="1b280-138">选择 **过帐的预缴税金** 以打开 **预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b280-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="1b280-139">在 **值** 字段中，显示用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="1b280-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="1b280-140">预缴税金交易页面中的 **概述**、**常规** 和 **金额** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。</span><span class="sxs-lookup"><span data-stu-id="1b280-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
