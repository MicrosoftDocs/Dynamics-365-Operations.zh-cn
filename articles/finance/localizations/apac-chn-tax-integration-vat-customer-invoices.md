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
ms.search.scope: Core, Operations
ms.custom: 264894
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0ece31dff245240dc13452673433f52cd32f47b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183966"
---
# <a name="chinese-tax-integration-modification-for-vat-customer-invoices-faq"></a><span data-ttu-id="157c9-104">增值税客户发票的中国税务集成修改常见问题</span><span class="sxs-lookup"><span data-stu-id="157c9-104">Chinese tax integration modification for VAT customer invoices FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="157c9-105">您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。</span><span class="sxs-lookup"><span data-stu-id="157c9-105">You can generate value-added tax (VAT) customer invoices, and then export them as text files.</span></span> <span data-ttu-id="157c9-106">接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。</span><span class="sxs-lookup"><span data-stu-id="157c9-106">You can then import reference numbers for the VAT customer invoices that can be linked to the original invoices.</span></span>

<span data-ttu-id="157c9-107">在导出增值税客户发票前，您可以拆分增值税客户发票以创建多个发票单据。</span><span class="sxs-lookup"><span data-stu-id="157c9-107">Before you export a VAT customer invoice, you can split the VAT customer invoice to create multiple invoice documents.</span></span> <span data-ttu-id="157c9-108">您还可以合并多个增值税客户发票，以创建一个包含原始发票行明细的发票导出单据。</span><span class="sxs-lookup"><span data-stu-id="157c9-108">You can also combine multiple VAT customer invoices to create one invoice export document that contains the line details of the original invoices.</span></span>

## <a name="what-is-a-vat-customer-invoice"></a><span data-ttu-id="157c9-109">增值税客户发票是什么？</span><span class="sxs-lookup"><span data-stu-id="157c9-109">What is a VAT customer invoice?</span></span>
<span data-ttu-id="157c9-110">当您过帐使用了增值税的销售税组和物料销售税组的客户交易时，则需要生成增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="157c9-110">A VAT customer invoice is generated when you post a customer transaction that uses the sales tax group for VAT and the item sales tax group for VAT.</span></span> <span data-ttu-id="157c9-111">您可以通过销售订单、退货销售订单、普通发票、贷方通知单或项目销售发票创建增值税款客户发票。</span><span class="sxs-lookup"><span data-stu-id="157c9-111">You can generate a VAT customer invoice from a sales order, return sales order, credit note, free text invoice, or project sales invoice.</span></span>

## <a name="can-i-create-one-tax-integration-profile-for-multiple-types-of-documents"></a><span data-ttu-id="157c9-112">我是否可以创建一个用于多种类型单据的纳税集成模板？</span><span class="sxs-lookup"><span data-stu-id="157c9-112">Can I create one tax integration profile for multiple types of documents?</span></span>

<span data-ttu-id="157c9-113">是。</span><span class="sxs-lookup"><span data-stu-id="157c9-113">Yes.</span></span> <span data-ttu-id="157c9-114">您可以创建一个用于多种类型单据的纳税集成模板。</span><span class="sxs-lookup"><span data-stu-id="157c9-114">You can create one tax integration profile for multiple types of documents.</span></span>

## <a name="when-should-i-split-a-vat-customer-invoice"></a><span data-ttu-id="157c9-115">我该何时拆分增值税客户发票？</span><span class="sxs-lookup"><span data-stu-id="157c9-115">When should I split a VAT customer invoice?</span></span>
<span data-ttu-id="157c9-116">如果在**增值税发票集成**页中选中了**超过最大发票金额**复选框，则您应该拆分增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="157c9-116">You should split a VAT customer invoice if the **Over amount limit** check box is selected on the **VAT invoice integration** page.</span></span> <span data-ttu-id="157c9-117">**超过最大发票金额**选项是为了发票总金额超过您在**最大发票金额**字段（位于**税务集成模板**页中）中指定的金额限制的发票选择的。</span><span class="sxs-lookup"><span data-stu-id="157c9-117">The **Over amount limit** option is selected for the invoices that have a total invoice amount that exceeds the amount limit that you specify in the **Maximum invoice amount** field on the **Tax integration profiles** page.</span></span>

## <a name="which-vat-customer-invoices-can-i-combine"></a><span data-ttu-id="157c9-118">我可以合并哪些增值税客户发票？</span><span class="sxs-lookup"><span data-stu-id="157c9-118">Which VAT customer invoices can I combine?</span></span>
<span data-ttu-id="157c9-119">您可以合并使用相同发票帐户和销售税代码的增值税客户发票。</span><span class="sxs-lookup"><span data-stu-id="157c9-119">You can combine VAT customer invoices that use the same invoice account number and sales tax code.</span></span>

## <a name="how-many-times-can-i-export-an-invoice"></a><span data-ttu-id="157c9-120">我可以导出发票多少次？</span><span class="sxs-lookup"><span data-stu-id="157c9-120">How many times can I export an invoice?</span></span>
<span data-ttu-id="157c9-121">一次只能导出一张发票。</span><span class="sxs-lookup"><span data-stu-id="157c9-121">You can only export an invoice one time.</span></span>

## <a name="can-i-export-summarized-invoice-lines-including-miscellaneous-charge-amounts-if-charges-are-applied-for-the-invoice-line"></a><span data-ttu-id="157c9-122">如果对发票行应用费用，我可以导出包含杂项费用金额的汇总发票行吗？</span><span class="sxs-lookup"><span data-stu-id="157c9-122">Can I export summarized invoice lines including miscellaneous charge amounts if charges are applied for the invoice line?</span></span>
<span data-ttu-id="157c9-123">如果在**税务集成模板**页上选中**将行费用添加到发票行**复选框，则您可以导出发票以及汇总发票行金额包含杂项费用的发票行。</span><span class="sxs-lookup"><span data-stu-id="157c9-123">You can export an invoice and its lines with summarized invoice line amounts including miscellaneous charges if **Add line charges into invoice line** check box is selected on the **Tax integration profile** page.</span></span>

## <a name="can-i-customize-or-add-new-information-on-vat-customer-invoices"></a><span data-ttu-id="157c9-124">我是否可以在增值税客户发票中自定义或添加新信息？</span><span class="sxs-lookup"><span data-stu-id="157c9-124">Can I customize or add new information on VAT customer invoices?</span></span>
<span data-ttu-id="157c9-125">是。</span><span class="sxs-lookup"><span data-stu-id="157c9-125">Yes.</span></span> <span data-ttu-id="157c9-126">您可以通过添加其他字段对增值税客户发票自定义，然后将增值税客户发票导出为文本文件。</span><span class="sxs-lookup"><span data-stu-id="157c9-126">You can customize VAT customer invoices by adding other fields, and then you can export the VAT customer invoices as text files.</span></span>

<span data-ttu-id="157c9-127">若要自定义增值税客户发票，使其包括其他详细信息，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="157c9-127">To customize VAT customer invoices to include other details, follow these steps:</span></span>

1. <span data-ttu-id="157c9-128">在**电子申报**页中，选择**申报配置**以打开**配置**。</span><span class="sxs-lookup"><span data-stu-id="157c9-128">On the **Electronic reporting** page, select **Reporting configurations** to open **Configurations**.</span></span>
2. <span data-ttu-id="157c9-129">在树结构中，选择**金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="157c9-129">In the tree, select **Golden Tax(CN)**.</span></span>
3. <span data-ttu-id="157c9-130">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="157c9-130">Click **Designer**.</span></span> <span data-ttu-id="157c9-131">在树结构中的**导出的发票** &gt; **发票**下添加其他字段，然后保存 GER 模型。</span><span class="sxs-lookup"><span data-stu-id="157c9-131">Add other fields on the tree under **Exported Invoices** &gt; **Invoices**, and save the GER model.</span></span>
4. <span data-ttu-id="157c9-132">单击**将模型映射到数据源**，然后选择**金税** &gt; **设计器**。</span><span class="sxs-lookup"><span data-stu-id="157c9-132">Click **Map model to data source** and select **Golden Tax** &gt; **Designer**.</span></span>
5. <span data-ttu-id="157c9-133">单击**保存**并返回到**配置**。</span><span class="sxs-lookup"><span data-stu-id="157c9-133">Click **Save** and return to **Configurations**.</span></span>
6. <span data-ttu-id="157c9-134">将添加的字段映射到表。</span><span class="sxs-lookup"><span data-stu-id="157c9-134">Map the added fields to a table.</span></span> 
    1. <span data-ttu-id="157c9-135">在树结构中，选择**金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="157c9-135">Select **GoldenTax(CN)** in the tree.</span></span>
    2. <span data-ttu-id="157c9-136">单击**更改状态** &gt; **完成**以获取模型的新版本。</span><span class="sxs-lookup"><span data-stu-id="157c9-136">Click **Change status** &gt; **Complete** to get a new version of the model.</span></span>
    3. <span data-ttu-id="157c9-137">在树结构中，展开**金税(CN)**。</span><span class="sxs-lookup"><span data-stu-id="157c9-137">Expand **GoldenTax(CN)** in the tree.</span></span>
    4. <span data-ttu-id="157c9-138">在树结构中，选择**金税(CN)** 格式。</span><span class="sxs-lookup"><span data-stu-id="157c9-138">Select the **GoldenTax(CN)** format in the tree.</span></span>
    5. <span data-ttu-id="157c9-139">单击**重定基本值**。</span><span class="sxs-lookup"><span data-stu-id="157c9-139">Click **Rebase**.</span></span> <span data-ttu-id="157c9-140">确认目标版本是新完成的版本。</span><span class="sxs-lookup"><span data-stu-id="157c9-140">Confirm that the target version is the new completed version.</span></span>
    6. <span data-ttu-id="157c9-141">单击**确定**完成重定基本值过程。</span><span class="sxs-lookup"><span data-stu-id="157c9-141">Click **OK** to finish the rebase process.</span></span>
    7. <span data-ttu-id="157c9-142">单击**设计器**打开格式设计器。</span><span class="sxs-lookup"><span data-stu-id="157c9-142">Click **Designer** to open the format designer.</span></span>
    8. <span data-ttu-id="157c9-143">在格式设计器中，在树中添加在文本文件中出现的新字段。</span><span class="sxs-lookup"><span data-stu-id="157c9-143">In the format designer, add new fields in the tree that are present in text files.</span></span>
    9. <span data-ttu-id="157c9-144">选择新添加的字段，然后单击**映射**选项卡。</span><span class="sxs-lookup"><span data-stu-id="157c9-144">Select the newly added field, and click the **Mapping** tab.</span></span>
    10. <span data-ttu-id="157c9-145">在树结构中展开该模型。</span><span class="sxs-lookup"><span data-stu-id="157c9-145">Expand the model in the tree.</span></span>
    11. <span data-ttu-id="157c9-146">选择新添加的模型字段，然后单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="157c9-146">Select the newly added model field and then click **Bind**.</span></span>
    12. <span data-ttu-id="157c9-147">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="157c9-147">Click **Save**.</span></span>
    13. <span data-ttu-id="157c9-148">单击**更改状态** &gt; **完成**以获取新版本。</span><span class="sxs-lookup"><span data-stu-id="157c9-148">Click **Change status** &gt; **Complete** to get a new version.</span></span>



<a name="additional-resources"></a><span data-ttu-id="157c9-149">其他资源</span><span class="sxs-lookup"><span data-stu-id="157c9-149">Additional resources</span></span>
--------

[<span data-ttu-id="157c9-150">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="157c9-150">Configure tax integration for China</span></span>](apac-chn-tax-integration.md)

[<span data-ttu-id="157c9-151">导入中国金税数据实体</span><span class="sxs-lookup"><span data-stu-id="157c9-151">Import the Chinese Golden Tax data entity</span></span>](apac-chn-import-golden-tax-data-entity.md)



