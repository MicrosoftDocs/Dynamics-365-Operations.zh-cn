---
title: 增值税客户发票的中国税务集成修改常见问题
description: 您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。 接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。
author: mrolecki
manager: AnnBe
ms.date: 05/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VATInvoiceDescTable_CN, TaxProfileTable_CN
audience: Application User
ms.reviewer: kfend
ms.custom: 264894
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0ff45209fe29e0f0a4b74b4c5bfa3ceb9d7f5c0b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975414"
---
# <a name="chinese-tax-integration-modification-for-vat-customer-invoices-faq"></a><span data-ttu-id="4534e-104">增值税客户发票的中国税务集成修改常见问题</span><span class="sxs-lookup"><span data-stu-id="4534e-104">Chinese tax integration modification for VAT customer invoices FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4534e-105">您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。</span><span class="sxs-lookup"><span data-stu-id="4534e-105">You can generate value-added tax (VAT) customer invoices, and then export them as text files.</span></span> <span data-ttu-id="4534e-106">接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。</span><span class="sxs-lookup"><span data-stu-id="4534e-106">You can then import reference numbers for the VAT customer invoices that can be linked to the original invoices.</span></span>

<span data-ttu-id="4534e-107">在导出增值税客户发票前，您可以拆分增值税客户发票以创建多个发票单据。</span><span class="sxs-lookup"><span data-stu-id="4534e-107">Before you export a VAT customer invoice, you can split the VAT customer invoice to create multiple invoice documents.</span></span> <span data-ttu-id="4534e-108">您还可以合并多个增值税客户发票，以创建一个包含原始发票行明细的发票导出单据。</span><span class="sxs-lookup"><span data-stu-id="4534e-108">You can also combine multiple VAT customer invoices to create one invoice export document that contains the line details of the original invoices.</span></span>

## <a name="what-is-a-vat-customer-invoice"></a><span data-ttu-id="4534e-109">增值税客户发票是什么？</span><span class="sxs-lookup"><span data-stu-id="4534e-109">What is a VAT customer invoice?</span></span>
<span data-ttu-id="4534e-110">当您过帐使用了增值税的销售税组和物料销售税组的客户交易时，则需要生成增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-110">A VAT customer invoice is generated when you post a customer transaction that uses the sales tax group for VAT and the item sales tax group for VAT.</span></span> <span data-ttu-id="4534e-111">您可以通过销售订单、退货销售订单、普通发票、贷方通知单或项目销售发票创建增值税款客户发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-111">You can generate a VAT customer invoice from a sales order, return sales order, credit note, free text invoice, or project sales invoice.</span></span>

## <a name="can-i-create-one-tax-integration-profile-for-multiple-types-of-documents"></a><span data-ttu-id="4534e-112">我是否可以创建一个用于多种类型单据的纳税集成模板？</span><span class="sxs-lookup"><span data-stu-id="4534e-112">Can I create one tax integration profile for multiple types of documents?</span></span>

<span data-ttu-id="4534e-113">是。</span><span class="sxs-lookup"><span data-stu-id="4534e-113">Yes.</span></span> <span data-ttu-id="4534e-114">您可以创建一个用于多种类型单据的纳税集成模板。</span><span class="sxs-lookup"><span data-stu-id="4534e-114">You can create one tax integration profile for multiple types of documents.</span></span>

## <a name="can-i-create-an-invoice-that-has-different-sales-tax-codes-and-sales-tax-rates-in-lines"></a><span data-ttu-id="4534e-115">我可以在行中创建具有不同销售税代码和销售税率的发票吗？</span><span class="sxs-lookup"><span data-stu-id="4534e-115">Can I create an invoice that has different sales tax codes and sales tax rates in lines?</span></span>

<span data-ttu-id="4534e-116">是。</span><span class="sxs-lookup"><span data-stu-id="4534e-116">Yes.</span></span> <span data-ttu-id="4534e-117">如果您开启 **允许在增值税客户发票行中使用多个税码进行中国金税集成** 功能（请参阅 [功能管理概述](../../fin-and-ops/get-started/feature-management/feature-management-overview.md)），并且存在一个税务集成配置文件，其 **税务集成配置文件** 页上的 **销售税代码** 字段为空（**应收帐款 \> 设置 \> 税务集成**），您可以创建和过帐具有不同销售税代码和销售税率的发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-117">If you turn on the **Allow multiple tax codes in VAT customer invoices lines for Chinese Golden tax integration** feature (see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md)), and if there is a tax integration profile where the **Sales tax code** field is blank on **Tax integration profile** page (**Accounts receivable \> Setup \> Tax integration**), you can create and post invoices that have different sales tax codes and sales tax rates.</span></span> <span data-ttu-id="4534e-118">您还可以将发票导出到文件中。</span><span class="sxs-lookup"><span data-stu-id="4534e-118">You can also export the invoices to the file.</span></span>   

## <a name="when-should-i-split-a-vat-customer-invoice"></a><span data-ttu-id="4534e-119">我该何时拆分增值税客户发票？</span><span class="sxs-lookup"><span data-stu-id="4534e-119">When should I split a VAT customer invoice?</span></span>
<span data-ttu-id="4534e-120">如果在 **增值税发票集成** 页中选中了 **超过最大发票金额** 复选框，则您应该拆分增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-120">You should split a VAT customer invoice if the **Over amount limit** check box is selected on the **VAT invoice integration** page.</span></span> <span data-ttu-id="4534e-121">**超过最大发票金额** 选项是为了发票总金额超过您在 **最大发票金额** 字段（位于 **税务集成模板** 页中）中指定的金额限制的发票选择的。</span><span class="sxs-lookup"><span data-stu-id="4534e-121">The **Over amount limit** option is selected for the invoices that have a total invoice amount that exceeds the amount limit that you specify in the **Maximum invoice amount** field on the **Tax integration profiles** page.</span></span>

## <a name="which-vat-customer-invoices-can-i-combine"></a><span data-ttu-id="4534e-122">我可以合并哪些增值税客户发票？</span><span class="sxs-lookup"><span data-stu-id="4534e-122">Which VAT customer invoices can I combine?</span></span>
<span data-ttu-id="4534e-123">您可以合并使用相同发票帐户和销售税代码的增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-123">You can combine VAT customer invoices that use the same invoice account number and sales tax code.</span></span>

## <a name="how-many-times-can-i-export-an-invoice"></a><span data-ttu-id="4534e-124">我可以导出发票多少次？</span><span class="sxs-lookup"><span data-stu-id="4534e-124">How many times can I export an invoice?</span></span>
<span data-ttu-id="4534e-125">一次只能导出一张发票。</span><span class="sxs-lookup"><span data-stu-id="4534e-125">You can only export an invoice one time.</span></span>

## <a name="can-i-export-summarized-invoice-lines-including-miscellaneous-charge-amounts-if-charges-are-applied-for-the-invoice-line"></a><span data-ttu-id="4534e-126">如果对发票行应用费用，我可以导出包含杂项费用金额的汇总发票行吗？</span><span class="sxs-lookup"><span data-stu-id="4534e-126">Can I export summarized invoice lines including miscellaneous charge amounts if charges are applied for the invoice line?</span></span>
<span data-ttu-id="4534e-127">如果在 **税务集成模板** 页上选中 **将行费用添加到发票行** 复选框，则您可以导出发票以及汇总发票行金额包含杂项费用的发票行。</span><span class="sxs-lookup"><span data-stu-id="4534e-127">You can export an invoice and its lines with summarized invoice line amounts including miscellaneous charges if **Add line charges into invoice line** check box is selected on the **Tax integration profile** page.</span></span>

## <a name="can-i-customize-or-add-new-information-on-vat-customer-invoices"></a><span data-ttu-id="4534e-128">我是否可以在增值税客户发票中自定义或添加新信息？</span><span class="sxs-lookup"><span data-stu-id="4534e-128">Can I customize or add new information on VAT customer invoices?</span></span>
<span data-ttu-id="4534e-129">是。</span><span class="sxs-lookup"><span data-stu-id="4534e-129">Yes.</span></span> <span data-ttu-id="4534e-130">您可以通过添加其他字段对增值税客户发票自定义，然后将增值税客户发票导出为文本文件。</span><span class="sxs-lookup"><span data-stu-id="4534e-130">You can customize VAT customer invoices by adding other fields, and then you can export the VAT customer invoices as text files.</span></span>

<span data-ttu-id="4534e-131">若要自定义增值税客户发票，使其包括其他详细信息，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="4534e-131">To customize VAT customer invoices to include other details, follow these steps:</span></span>

1. <span data-ttu-id="4534e-132">在 **电子申报** 页中，选择 **申报配置** 以打开 **配置**。</span><span class="sxs-lookup"><span data-stu-id="4534e-132">On the **Electronic reporting** page, select **Reporting configurations** to open **Configurations**.</span></span>
2. <span data-ttu-id="4534e-133">在树结构中，选择 **金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="4534e-133">In the tree, select **Golden Tax(CN)**.</span></span>
3. <span data-ttu-id="4534e-134">单击 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="4534e-134">Click **Designer**.</span></span> <span data-ttu-id="4534e-135">在树结构中的 **导出的发票** &gt; **发票** 下添加其他字段，然后保存 GER 模型。</span><span class="sxs-lookup"><span data-stu-id="4534e-135">Add other fields on the tree under **Exported Invoices** &gt; **Invoices**, and save the GER model.</span></span>
4. <span data-ttu-id="4534e-136">单击 **将模型映射到数据源**，然后选择 **金税** &gt; **设计器**。</span><span class="sxs-lookup"><span data-stu-id="4534e-136">Click **Map model to data source** and select **Golden Tax** &gt; **Designer**.</span></span>
5. <span data-ttu-id="4534e-137">单击 **保存** 并返回到 **配置**。</span><span class="sxs-lookup"><span data-stu-id="4534e-137">Click **Save** and return to **Configurations**.</span></span>
6. <span data-ttu-id="4534e-138">将添加的字段映射到表。</span><span class="sxs-lookup"><span data-stu-id="4534e-138">Map the added fields to a table.</span></span> 
    1. <span data-ttu-id="4534e-139">在树结构中，选择 **金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="4534e-139">Select **GoldenTax(CN)** in the tree.</span></span>
    2. <span data-ttu-id="4534e-140">单击 **更改状态** &gt; **完成** 以获取模型的新版本。</span><span class="sxs-lookup"><span data-stu-id="4534e-140">Click **Change status** &gt; **Complete** to get a new version of the model.</span></span>
    3. <span data-ttu-id="4534e-141">在树结构中，展开 **金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="4534e-141">Expand **GoldenTax(CN)** in the tree.</span></span>
    4. <span data-ttu-id="4534e-142">在树结构中，选择 **金税(CN)** 格式。</span><span class="sxs-lookup"><span data-stu-id="4534e-142">Select the **GoldenTax(CN)** format in the tree.</span></span>
    5. <span data-ttu-id="4534e-143">单击 **重定基本值**。</span><span class="sxs-lookup"><span data-stu-id="4534e-143">Click **Rebase**.</span></span> <span data-ttu-id="4534e-144">确认目标版本是新完成的版本。</span><span class="sxs-lookup"><span data-stu-id="4534e-144">Confirm that the target version is the new completed version.</span></span>
    6. <span data-ttu-id="4534e-145">单击 **确定** 完成重定基本值过程。</span><span class="sxs-lookup"><span data-stu-id="4534e-145">Click **OK** to finish the rebase process.</span></span>
    7. <span data-ttu-id="4534e-146">单击 **设计器** 打开格式设计器。</span><span class="sxs-lookup"><span data-stu-id="4534e-146">Click **Designer** to open the format designer.</span></span>
    8. <span data-ttu-id="4534e-147">在格式设计器中，在树中添加在文本文件中出现的新字段。</span><span class="sxs-lookup"><span data-stu-id="4534e-147">In the format designer, add new fields in the tree that are present in text files.</span></span>
    9. <span data-ttu-id="4534e-148">选择新添加的字段，然后单击 **映射** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="4534e-148">Select the newly added field, and click the **Mapping** tab.</span></span>
    10. <span data-ttu-id="4534e-149">在树结构中展开该模型。</span><span class="sxs-lookup"><span data-stu-id="4534e-149">Expand the model in the tree.</span></span>
    11. <span data-ttu-id="4534e-150">选择新添加的模型字段，然后单击 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="4534e-150">Select the newly added model field and then click **Bind**.</span></span>
    12. <span data-ttu-id="4534e-151">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4534e-151">Click **Save**.</span></span>
    13. <span data-ttu-id="4534e-152">单击 **更改状态** &gt; **完成** 以获取新版本。</span><span class="sxs-lookup"><span data-stu-id="4534e-152">Click **Change status** &gt; **Complete** to get a new version.</span></span>



<a name="additional-resources"></a><span data-ttu-id="4534e-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="4534e-153">Additional resources</span></span>
--------

[<span data-ttu-id="4534e-154">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="4534e-154">Configure tax integration for China</span></span>](apac-chn-tax-integration.md)

[<span data-ttu-id="4534e-155">导入中国金税数据实体</span><span class="sxs-lookup"><span data-stu-id="4534e-155">Import the Chinese Golden Tax data entity</span></span>](apac-chn-import-golden-tax-data-entity.md)



