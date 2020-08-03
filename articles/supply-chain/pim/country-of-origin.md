---
title: 原产国家/地区
description: 许多组织向其供应商颁发证书，以确保产品符合特定的认证标准。 这些证书通常依赖于原产国家/地区。 本主题提供有关原产国家/地区功能的信息，让您可以将产品链接到其原产国家/地区并跟踪产品认证。
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596206"
---
# <a name="country-of-origin"></a><span data-ttu-id="00500-105">原产国家/地区</span><span class="sxs-lookup"><span data-stu-id="00500-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00500-106">许多组织向其供应商颁发证书，以确保产品符合特定的认证标准。</span><span class="sxs-lookup"><span data-stu-id="00500-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="00500-107">这些证书通常依赖于原产国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="00500-108">原产国家/地区功能让您可以将产品链接到其原产国家/地区并跟踪产品认证。</span><span class="sxs-lookup"><span data-stu-id="00500-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="00500-109">配置来源与目标国家/地区</span><span class="sxs-lookup"><span data-stu-id="00500-109">Configure source and destination countries</span></span>

<span data-ttu-id="00500-110">在发放产品证书之前，必须将产品链接到其目标国家/地区和原产国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="00500-111">转到**产品信息管理 \> 设置 \> 产品合规性 \> 原产国家/地区 \> 原产国家/地区规则**。</span><span class="sxs-lookup"><span data-stu-id="00500-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="00500-112">选择要编辑的现有国家/地区设置，或在“操作窗格”上选择**新建**创建新的国家/地区设置。</span><span class="sxs-lookup"><span data-stu-id="00500-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="00500-113">为所选或新国家/地区设置以下值。</span><span class="sxs-lookup"><span data-stu-id="00500-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="00500-114">字段</span><span class="sxs-lookup"><span data-stu-id="00500-114">Field</span></span> | <span data-ttu-id="00500-115">说明</span><span class="sxs-lookup"><span data-stu-id="00500-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="00500-116">物料编号</span><span class="sxs-lookup"><span data-stu-id="00500-116">Item number</span></span> | <span data-ttu-id="00500-117">选择产品的物料编号。</span><span class="sxs-lookup"><span data-stu-id="00500-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="00500-118">目标国家</span><span class="sxs-lookup"><span data-stu-id="00500-118">Destination country</span></span> | <span data-ttu-id="00500-119">选择要将产品发送到的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="00500-120">原产国家/地区</span><span class="sxs-lookup"><span data-stu-id="00500-120">Origin country</span></span> | <span data-ttu-id="00500-121">选择您装运产品的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="00500-122">此设置的目的是帮助您生成物料清单 (BOM) 报告，报告中可以包括指定了来源和目标国家/地区的每个部件的原产国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="00500-123">此报告将帮助您全面了解部件的来源和去向。</span><span class="sxs-lookup"><span data-stu-id="00500-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="00500-124">跟踪供应商证书</span><span class="sxs-lookup"><span data-stu-id="00500-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="00500-125">您可以使用**原产国家/地区供应商证书**页面跟踪您发放给供应商的证书。</span><span class="sxs-lookup"><span data-stu-id="00500-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="00500-126">您必须确定要发放的证书文件以及如何将其报告给客户。</span><span class="sxs-lookup"><span data-stu-id="00500-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="00500-127">此功能可帮助您跟踪证书。</span><span class="sxs-lookup"><span data-stu-id="00500-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="00500-128">它还让您可以选择是否在发票、装箱单和/或订单确认单上显示相关的证书编号。</span><span class="sxs-lookup"><span data-stu-id="00500-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="00500-129">要设置您的证书信息，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="00500-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="00500-130">转到**产品信息管理 \> 设置 \> 产品合规性 \> 原产国家/地区 \> 原产国家/地区供应商证书**。</span><span class="sxs-lookup"><span data-stu-id="00500-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="00500-131">选择要编辑的现有证书设置，或在“操作窗格”上选择**新建**创建新的证书设置。</span><span class="sxs-lookup"><span data-stu-id="00500-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="00500-132">为所选或新证书设置以下设置。</span><span class="sxs-lookup"><span data-stu-id="00500-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="00500-133">字段</span><span class="sxs-lookup"><span data-stu-id="00500-133">Field</span></span> | <span data-ttu-id="00500-134">说明</span><span class="sxs-lookup"><span data-stu-id="00500-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="00500-135">供应商帐户</span><span class="sxs-lookup"><span data-stu-id="00500-135">Vendor account</span></span> | <span data-ttu-id="00500-136">选择您向其发放证书的供应商。</span><span class="sxs-lookup"><span data-stu-id="00500-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="00500-137">物料编号</span><span class="sxs-lookup"><span data-stu-id="00500-137">Item number</span></span> | <span data-ttu-id="00500-138">选择您为其发放证书的物料。</span><span class="sxs-lookup"><span data-stu-id="00500-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="00500-139">国家/地区</span><span class="sxs-lookup"><span data-stu-id="00500-139">Country/region</span></span> | <span data-ttu-id="00500-140">您必须使用此证书的目标国家或地区。</span><span class="sxs-lookup"><span data-stu-id="00500-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="00500-141">证书编号</span><span class="sxs-lookup"><span data-stu-id="00500-141">Certificate number</span></span> | <span data-ttu-id="00500-142">输入您发放的证书的标识号。</span><span class="sxs-lookup"><span data-stu-id="00500-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="00500-143">已生效</span><span class="sxs-lookup"><span data-stu-id="00500-143">Effective</span></span> | <span data-ttu-id="00500-144">选择当前证书有效的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="00500-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="00500-145">到期</span><span class="sxs-lookup"><span data-stu-id="00500-145">Expiration</span></span> | <span data-ttu-id="00500-146">选择当前证书有效的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="00500-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="00500-147">打印到发票上</span><span class="sxs-lookup"><span data-stu-id="00500-147">Print on invoice</span></span> | <span data-ttu-id="00500-148">选中此复选框可在指定日期范围内在发送到指定国家/地区的发票上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="00500-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="00500-149">打印到装箱单上</span><span class="sxs-lookup"><span data-stu-id="00500-149">Print on packing slip</span></span> | <span data-ttu-id="00500-150">选中此复选框可在指定日期范围内在发送到指定国家/地区的装箱单上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="00500-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="00500-151">打印到销售订单上</span><span class="sxs-lookup"><span data-stu-id="00500-151">Print on sales order</span></span> | <span data-ttu-id="00500-152">选中此复选框可在指定日期范围内在发送到指定国家/地区的销售订单上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="00500-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="00500-153">在 BOM 报告中包括原产国家/地区</span><span class="sxs-lookup"><span data-stu-id="00500-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="00500-154">生成 BOM 报告时，可以为您在**原产国家/地区规则**页面上指定了来源和目标国家/地区的每个部件包含原产国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="00500-155">转到**产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="00500-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="00500-156">选择或创建一个产品以打开其**已发放产品详细信息**页。</span><span class="sxs-lookup"><span data-stu-id="00500-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="00500-157">在“操作窗格”的**设计**选项卡的 **BOM** 组中，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="00500-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="00500-158">在显示的页面上的“操作窗格”上，选择 **BOM \> 打印**。</span><span class="sxs-lookup"><span data-stu-id="00500-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="00500-159">在**物料清单行**对话框中，将**目标国家/地区**字段设置为要在报告中查看的目标国家/地区。</span><span class="sxs-lookup"><span data-stu-id="00500-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="00500-160">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="00500-160">Select **OK**.</span></span>

<span data-ttu-id="00500-161">显示有关每个部件原产国家/地区的信息的报告将生成并显示。</span><span class="sxs-lookup"><span data-stu-id="00500-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="00500-162">以下是一个报告示例。</span><span class="sxs-lookup"><span data-stu-id="00500-162">Here is an example of the report.</span></span>

<span data-ttu-id="00500-163">![原产国家/地区报告](media/country-of-origin-report.png "原产国家/地区报告")</span><span class="sxs-lookup"><span data-stu-id="00500-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
