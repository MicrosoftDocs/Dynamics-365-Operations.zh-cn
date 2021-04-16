---
title: 两用商品
description: 本主题说明如何跟踪被识别为两用商品的产品，存储每个相关产品的证书编号和目标国家/地区，以及在相关发票、装箱单和/或销售订单上打印有效的证书编号。
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 15e8696b2bfa9f1df3cecd2d98b9ad2f6c5d6000
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829466"
---
# <a name="dual-use-goods"></a><span data-ttu-id="e170a-103">两用商品</span><span class="sxs-lookup"><span data-stu-id="e170a-103">Dual-use goods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e170a-104">两用商品通常是同时具有民用和军事用途的物料。</span><span class="sxs-lookup"><span data-stu-id="e170a-104">Dual-use goods are typically items that have both civilian and military applications.</span></span> <span data-ttu-id="e170a-105">例如，化学制品可以用作肥料，也可以用作炸药。</span><span class="sxs-lookup"><span data-stu-id="e170a-105">For example, a chemical might be used as either a fertilizer or an explosive.</span></span> <span data-ttu-id="e170a-106">许多国家/地区都有针对两用商品出口、进口和运输的特殊规定。</span><span class="sxs-lookup"><span data-stu-id="e170a-106">Many countries have special regulations that apply to the export, import, and transportation of dual-use goods.</span></span> <span data-ttu-id="e170a-107">因此，掌握各种政策和证书对于涉足两用商品国际贸易的公司很重要。</span><span class="sxs-lookup"><span data-stu-id="e170a-107">Therefore, it's important that companies that are involved in the international trade of dual-use goods keep track of the various policies and certificates.</span></span>

<span data-ttu-id="e170a-108">两用功能帮助公司跟踪被识别为两用商品的产品，存储每个相关产品的证书编号和目标国家/地区，以及在相关发票、装箱单和/或销售订单上打印有效的证书编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-108">The dual-use feature helps companies keep track of products that are identified as dual-use goods, stores certificate numbers for each relevant product and destination country, and print valid certificate numbers on relevant invoices, packing slips, and/or sales orders.</span></span> <span data-ttu-id="e170a-109">它有助于确保产品在装运时始终具有最新认证。</span><span class="sxs-lookup"><span data-stu-id="e170a-109">It helps ensure that, when your products are shipped, they always include up-to-date certifications.</span></span>

<span data-ttu-id="e170a-110">请考虑以下情形：</span><span class="sxs-lookup"><span data-stu-id="e170a-110">Consider the following scenario:</span></span>

1. <span data-ttu-id="e170a-111">系统中的 **两用国家/地区设置** 页面指示目的地为法国的装运需要认证。</span><span class="sxs-lookup"><span data-stu-id="e170a-111">The **Dual use country setup** page in your system indicates that shipments to France require a certification.</span></span>
2. <span data-ttu-id="e170a-112">产品 X-100 的 **已发放产品详细信息** 页面指示它是两用商品。</span><span class="sxs-lookup"><span data-stu-id="e170a-112">The **Released product details** page for product X-100 indicates that it's a dual-use good.</span></span> <span data-ttu-id="e170a-113">代码、类别、组和体系共同表明了产品所属的出口管制分类。</span><span class="sxs-lookup"><span data-stu-id="e170a-113">Together, the code, category, group, and regime indicate the export control classification that the product belongs to.</span></span>
3. <span data-ttu-id="e170a-114">**两用证书** 页面包括产品 X-100 运往法国时的证书。</span><span class="sxs-lookup"><span data-stu-id="e170a-114">The **Dual use certificates** page includes a certificate for product X-100 when it's shipped to France.</span></span> <span data-ttu-id="e170a-115">此证书的有效日期为 2020 年 1 月 1 日。</span><span class="sxs-lookup"><span data-stu-id="e170a-115">This certificate expires January 1, 2020.</span></span>
4. <span data-ttu-id="e170a-116">2020 年 6 月 17 日，您为位于法国的客户公司创建销售订单，该订单包含产品 X-100。</span><span class="sxs-lookup"><span data-stu-id="e170a-116">On June 17, 2020, you create a sales order for a customer company that is based in France, and the order includes product X-100.</span></span>
5. <span data-ttu-id="e170a-117">保存销售订单时，系统确定以下信息：</span><span class="sxs-lookup"><span data-stu-id="e170a-117">When you save the sales order, the system determines the following information:</span></span>

    1. <span data-ttu-id="e170a-118">订单中是否包括任何属于两用商品的产品？</span><span class="sxs-lookup"><span data-stu-id="e170a-118">Does the order include any products that are dual-use goods?</span></span>
    2. <span data-ttu-id="e170a-119">如果订单中包括两用商品，目标国家/地区是否要求提供两用证书？</span><span class="sxs-lookup"><span data-stu-id="e170a-119">If the order includes dual-use goods, does the destination country require dual-use certificates?</span></span>
    3. <span data-ttu-id="e170a-120">如果该国家/地区要求提供两用证书，运往目标国家/地区的每一种两用商品是否都有有效证书？</span><span class="sxs-lookup"><span data-stu-id="e170a-120">If the country requires dual-use certificates, does a valid certificate exist for each dual-use good for the destination country?</span></span>

6. <span data-ttu-id="e170a-121">此订单包括产品 X-100，该产品正在运往法国，并且该产品具有法国证书。</span><span class="sxs-lookup"><span data-stu-id="e170a-121">The order includes product X-100, the product is being shipped to France, and a French certificate exists for the product.</span></span> <span data-ttu-id="e170a-122">但是，证书已过期。</span><span class="sxs-lookup"><span data-stu-id="e170a-122">However, the certificate has expired.</span></span> <span data-ttu-id="e170a-123">因此，您收到以下警告消息：“此销售订单中有一个或多个两用物料的两用证书无效。</span><span class="sxs-lookup"><span data-stu-id="e170a-123">Therefore, you receive the following warning message: "Dual use certificates for one or more dual-use items in this sales order aren't valid.</span></span> <span data-ttu-id="e170a-124">是否要继续确认？”</span><span class="sxs-lookup"><span data-stu-id="e170a-124">Do you want to proceed with the confirmation?"</span></span>

<span data-ttu-id="e170a-125">本主题说明如何配置设置两用商品和支持此情形所需的所有设置。</span><span class="sxs-lookup"><span data-stu-id="e170a-125">This topic explains how to configure all the settings that are required to set up dual-use goods and support this scenario.</span></span>

## <a name="define-dual-use-requirements-for-each-relevant-country"></a><span data-ttu-id="e170a-126">定义每个相关国家/地区的两用要求</span><span class="sxs-lookup"><span data-stu-id="e170a-126">Define dual-use requirements for each relevant country</span></span>

<span data-ttu-id="e170a-127">不同国家/地区对两用商品有不同要求。</span><span class="sxs-lookup"><span data-stu-id="e170a-127">Different countries have different requirements for dual-use goods.</span></span> <span data-ttu-id="e170a-128">您将使用 **两用国家/地区设置** 页面来跟踪需要和不需要证书的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="e170a-128">You use the **Dual use country setup** page to keep track of the countries that do and don't require a certificate.</span></span> <span data-ttu-id="e170a-129">创建销售订单时，系统会检查您在这里指定的信息，并提醒您提供所需的认证。</span><span class="sxs-lookup"><span data-stu-id="e170a-129">The information that you specify here is checked when you create sales orders, and you will be reminded to provide the required certifications.</span></span>

<span data-ttu-id="e170a-130">要设置有关不同国家/地区的两用要求的信息，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e170a-130">To set up the information about dual-use requirements for different countries, follow these steps.</span></span>

1. <span data-ttu-id="e170a-131">转到 **产品信息管理 \> 设置 \> 产品合规性 \> 两用产品 \> 两用国家/地区设置**。</span><span class="sxs-lookup"><span data-stu-id="e170a-131">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use country setup**.</span></span>
2. <span data-ttu-id="e170a-132">选择现有国家/地区设置对其进行编辑，或在“操作窗格”上选择 **新建** 创建新的国家/地区设置。</span><span class="sxs-lookup"><span data-stu-id="e170a-132">Select an existing country setup to edit it, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="e170a-133">为所选或新国家/地区设置设置以下值。</span><span class="sxs-lookup"><span data-stu-id="e170a-133">Set the following values for the selected or new country setup.</span></span>

    | <span data-ttu-id="e170a-134">字段</span><span class="sxs-lookup"><span data-stu-id="e170a-134">Field</span></span> | <span data-ttu-id="e170a-135">说明</span><span class="sxs-lookup"><span data-stu-id="e170a-135">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e170a-136">国家/地区</span><span class="sxs-lookup"><span data-stu-id="e170a-136">Country/region</span></span> | <span data-ttu-id="e170a-137">选择要跟踪要求的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="e170a-137">Select the country that you're tracking requirements for.</span></span> |
    | <span data-ttu-id="e170a-138">需要提供证书</span><span class="sxs-lookup"><span data-stu-id="e170a-138">Certificate Required</span></span> | <span data-ttu-id="e170a-139">对于要求两用商品认证的国家/地区，请选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="e170a-139">Select this check box for countries that require a certification for dual-use goods.</span></span> <span data-ttu-id="e170a-140">对于不需要此认证的国家/地区，将其清除。</span><span class="sxs-lookup"><span data-stu-id="e170a-140">Clear it for countries that don't require this certification.</span></span> |

## <a name="create-dual-use-categories"></a><span data-ttu-id="e170a-141">创建两用类别</span><span class="sxs-lookup"><span data-stu-id="e170a-141">Create dual-use categories</span></span>

<span data-ttu-id="e170a-142">两用商品通常必须根据其出口管制分类编号 (ECCN) 进行分类。</span><span class="sxs-lookup"><span data-stu-id="e170a-142">Dual-use goods must often be categorized according to their export control classification number (ECCN).</span></span> <span data-ttu-id="e170a-143">ECCN 是一种字母数字代码，根据商品和技术等因素对物料进行分类。</span><span class="sxs-lookup"><span data-stu-id="e170a-143">The ECCN is an alphanumeric code that categorizes items based on factors such as the commodity and technology.</span></span> <span data-ttu-id="e170a-144">**两用类别** 页面可帮助您对使用的类别建立一个列表，以进行报告。</span><span class="sxs-lookup"><span data-stu-id="e170a-144">The **Dual use categories** page helps you make a list of the categories that you use, for reporting purposes.</span></span>

<span data-ttu-id="e170a-145">要设置两用类别，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e170a-145">To set up dual-use categories, follow these steps.</span></span>

1. <span data-ttu-id="e170a-146">转到 **产品信息管理 \> 设置 \> 产品合规性 \> 两用产品 \> 两用类别**。</span><span class="sxs-lookup"><span data-stu-id="e170a-146">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use categories**.</span></span>
2. <span data-ttu-id="e170a-147">选择现有类别对其进行编辑，或在“操作窗格”上选择 **新建** 创建新类别。</span><span class="sxs-lookup"><span data-stu-id="e170a-147">Select an existing category to edit it, or select **New** on the Action Pane to create a new category.</span></span>
3. <span data-ttu-id="e170a-148">为所选或新类别设置以下值。</span><span class="sxs-lookup"><span data-stu-id="e170a-148">Set the following values for the selected or new category.</span></span>

    | <span data-ttu-id="e170a-149">字段</span><span class="sxs-lookup"><span data-stu-id="e170a-149">Fields</span></span> | <span data-ttu-id="e170a-150">说明</span><span class="sxs-lookup"><span data-stu-id="e170a-150">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e170a-151">两用代码</span><span class="sxs-lookup"><span data-stu-id="e170a-151">Dual use code</span></span> | <span data-ttu-id="e170a-152">输入完整的 ECCN 代码（例如，*3A001*）。</span><span class="sxs-lookup"><span data-stu-id="e170a-152">Enter the full ECCN code (for example, *3A001*).</span></span>|
    | <span data-ttu-id="e170a-153">两用类别</span><span class="sxs-lookup"><span data-stu-id="e170a-153">Dual use category</span></span> | <span data-ttu-id="e170a-154">输入 ECCN 代码的商业控制列表 (CCL) 类别部分。</span><span class="sxs-lookup"><span data-stu-id="e170a-154">Enter the commerce control list (CCL) category part of the ECCN code.</span></span> <span data-ttu-id="e170a-155">例如，对于 ECCN 代码 *3A001*，此值为 *3*。</span><span class="sxs-lookup"><span data-stu-id="e170a-155">For example, for the ECCN code *3A001*, this value is *3*.</span></span> |
    | <span data-ttu-id="e170a-156">两用组</span><span class="sxs-lookup"><span data-stu-id="e170a-156">Dual use group</span></span> | <span data-ttu-id="e170a-157">输入 ECCN 代码的产品组部分。</span><span class="sxs-lookup"><span data-stu-id="e170a-157">Enter the product group part of the ECCN code.</span></span> <span data-ttu-id="e170a-158">例如，对于 ECCN 代码 *3A001*，此值为 *A*。</span><span class="sxs-lookup"><span data-stu-id="e170a-158">For example, for the ECCN code *3A001*, this value is *A*.</span></span> |
    | <span data-ttu-id="e170a-159">两用体系</span><span class="sxs-lookup"><span data-stu-id="e170a-159">Dual use regime</span></span> | <span data-ttu-id="e170a-160">输入物料的体系代码。</span><span class="sxs-lookup"><span data-stu-id="e170a-160">Enter the regime code for the item.</span></span> <span data-ttu-id="e170a-161">此代码标识将物料归类为两用商品的原因。</span><span class="sxs-lookup"><span data-stu-id="e170a-161">This code identifies the reason why the item is classified as a dual-use good.</span></span> <span data-ttu-id="e170a-162">例如，对于 ECCN 代码 *3A001*，此值为 *001*。</span><span class="sxs-lookup"><span data-stu-id="e170a-162">For example, for the ECCN code *3A001*, this value is *001*.</span></span> |

## <a name="apply-dual-use-categories-to-products"></a><span data-ttu-id="e170a-163">对产品应用两用类别</span><span class="sxs-lookup"><span data-stu-id="e170a-163">Apply dual-use categories to products</span></span>

<span data-ttu-id="e170a-164">要将产品标识为两用商品并对其应用两用类别，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e170a-164">To identify a product as a dual-use good and apply a dual-use category to it, follow these steps.</span></span>

1. <span data-ttu-id="e170a-165">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="e170a-165">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e170a-166">选择或创建一个产品以打开其 **已发放产品详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="e170a-166">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="e170a-167">在 **外贸** 快速选项卡上，将 **两用产品** 选项设置为 **是**，以将当前产品标识为两用商品。</span><span class="sxs-lookup"><span data-stu-id="e170a-167">On the **Foreign trade** FastTab, set the **Dual use products** option to **Yes** to identify the current product as a dual-use good.</span></span>
1. <span data-ttu-id="e170a-168">将 **两用代码** 字段设置为应用于当前产品的代码。</span><span class="sxs-lookup"><span data-stu-id="e170a-168">Set the **Dual use code** field to the code that applies to the current product.</span></span> <span data-ttu-id="e170a-169">（您在 **两用类别** 页定义了此代码。）</span><span class="sxs-lookup"><span data-stu-id="e170a-169">(You defined this code on the **Dual use categories** page.)</span></span>

<span data-ttu-id="e170a-170">创建销售订单时，将检查此设置。</span><span class="sxs-lookup"><span data-stu-id="e170a-170">This setup is checked when you create a sales order.</span></span>

## <a name="set-up-dual-use-certificates"></a><span data-ttu-id="e170a-171">设置两用证书</span><span class="sxs-lookup"><span data-stu-id="e170a-171">Set up dual-use certificates</span></span>

<span data-ttu-id="e170a-172">您将使用 **两用证书** 页设置和管理每个产品和国家/地区所需的两用证书。</span><span class="sxs-lookup"><span data-stu-id="e170a-172">You use the **Dual use certificates** page to set up and manage the required dual-use certificates for each product and country.</span></span> <span data-ttu-id="e170a-173">您可以跟踪每个证书的详细信息，如国家/地区和有效日期。</span><span class="sxs-lookup"><span data-stu-id="e170a-173">You can track each certificate's details, such as the country and the dates of validity.</span></span> <span data-ttu-id="e170a-174">您还可以设置选项来指定应在何处打印此信息。</span><span class="sxs-lookup"><span data-stu-id="e170a-174">You can also set options to specify where this information should be printed.</span></span> <span data-ttu-id="e170a-175">例如，信息可以打印在发票、装箱单和/或销售订单上。</span><span class="sxs-lookup"><span data-stu-id="e170a-175">For example, the information can be printed on the invoice, packing slip, and/or sales order.</span></span> <span data-ttu-id="e170a-176">创建销售订单时，将检查此设置。</span><span class="sxs-lookup"><span data-stu-id="e170a-176">This setup is checked when you create a sales order.</span></span>

1. <span data-ttu-id="e170a-177">转到 **产品信息管理 \> 设置 \> 产品合规性 \> 两用产品 \> 两用证书**。</span><span class="sxs-lookup"><span data-stu-id="e170a-177">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use certificates**.</span></span>
2. <span data-ttu-id="e170a-178">选择现有证书对其进行编辑，或在“操作窗格”上选择 **新建** 创建新证书。</span><span class="sxs-lookup"><span data-stu-id="e170a-178">Select an existing certificate to edit it, or select **New** on the Action Pane to create a new certificate.</span></span>
3. <span data-ttu-id="e170a-179">为所选或新证书设置以下值。</span><span class="sxs-lookup"><span data-stu-id="e170a-179">Set the following values for the selected or new certificate.</span></span>

    | <span data-ttu-id="e170a-180">字段</span><span class="sxs-lookup"><span data-stu-id="e170a-180">Field</span></span> | <span data-ttu-id="e170a-181">说明</span><span class="sxs-lookup"><span data-stu-id="e170a-181">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e170a-182">物料编号</span><span class="sxs-lookup"><span data-stu-id="e170a-182">Item number</span></span> | <span data-ttu-id="e170a-183">选择此证书所应用的两用商品的物料编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-183">Select the item number of the dual-use good that this certificate applies to.</span></span> |
    | <span data-ttu-id="e170a-184">国家/地区</span><span class="sxs-lookup"><span data-stu-id="e170a-184">Country/region</span></span> | <span data-ttu-id="e170a-185">您必须使用此证书的目标国家或地区。</span><span class="sxs-lookup"><span data-stu-id="e170a-185">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="e170a-186">证书编号</span><span class="sxs-lookup"><span data-stu-id="e170a-186">Certificate number</span></span> | <span data-ttu-id="e170a-187">发放给供应商或客户的证书上显示的编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-187">The number that appears on the certificate that is issued to the vendor or customer.</span></span> |
    | <span data-ttu-id="e170a-188">已生效</span><span class="sxs-lookup"><span data-stu-id="e170a-188">Effective</span></span> | <span data-ttu-id="e170a-189">选择当前证书有效的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="e170a-189">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="e170a-190">到期</span><span class="sxs-lookup"><span data-stu-id="e170a-190">Expiration</span></span> | <span data-ttu-id="e170a-191">选择当前证书有效的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="e170a-191">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="e170a-192">打印到发票上</span><span class="sxs-lookup"><span data-stu-id="e170a-192">Print on invoice</span></span> | <span data-ttu-id="e170a-193">选中此复选框可在指定日期范围内在发送到指定国家/地区的发票上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-193">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e170a-194">打印到装箱单上</span><span class="sxs-lookup"><span data-stu-id="e170a-194">Print on packing slip</span></span> | <span data-ttu-id="e170a-195">选中此复选框可在指定日期范围内在发送到指定国家/地区的装箱单上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-195">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e170a-196">打印到销售订单上</span><span class="sxs-lookup"><span data-stu-id="e170a-196">Print on sales order</span></span> | <span data-ttu-id="e170a-197">选中此复选框可在指定日期范围内在发送到指定国家/地区的销售订单上打印证书编号。</span><span class="sxs-lookup"><span data-stu-id="e170a-197">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]