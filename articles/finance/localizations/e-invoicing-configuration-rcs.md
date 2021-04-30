---
title: 在 Regulatory Configuration Services (RCS) 中配置电子开票
description: 本主题说明如何在 Dynamics 365 Regulatory Configuration Services (RCS) 中配置电子开票。
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d7945cc899cf161f294dfcc3f6d1a9a79c9453ab
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897712"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="d13e4-103">在 Regulatory Configuration Services (RCS) 中配置电子开票</span><span class="sxs-lookup"><span data-stu-id="d13e4-103">Configure Electronic invoicing in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d13e4-104">本主题提供有关 Dynamics 365 Regulatory Configuration Services (RCS) 中电子开票的配置功能的信息。</span><span class="sxs-lookup"><span data-stu-id="d13e4-104">This topic provides information about the configuration capabilities of Electronic invoicing in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="d13e4-105">通过配置功能，电子开票可帮助您满足电子发票的业务和法规要求，而无需进行任何编码。</span><span class="sxs-lookup"><span data-stu-id="d13e4-105">It is through the configuration capabilities that Electronic invoicing helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="d13e4-106">而且，在电子发票必须由 Web 服务以电子方式审核的情况下，配置功能还可以帮助您满足与 Web 服务交换消息的要求，无需编写任何代码。</span><span class="sxs-lookup"><span data-stu-id="d13e4-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="d13e4-107">电子报告</span><span class="sxs-lookup"><span data-stu-id="d13e4-107">Electronic reporting</span></span>

<span data-ttu-id="d13e4-108">电子报告 (ER) 支持电子开票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-108">Electronic reporting (ER) supports Electronic invoicing.</span></span>

<span data-ttu-id="d13e4-109">数据模型映射和格式是可配置的组件，可通过 ER 创建和维护，在电子开票中使用。</span><span class="sxs-lookup"><span data-stu-id="d13e4-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in Electronic invoicing.</span></span> <span data-ttu-id="d13e4-110">ER 格式设计器是用于创建和维护文件格式的工具。</span><span class="sxs-lookup"><span data-stu-id="d13e4-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="d13e4-111">用于配置电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="d13e4-112">有关详细信息，请参阅[电子报告 (ER) 概述](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="d13e4-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="d13e4-113">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-113">Electronic invoicing features</span></span>

<span data-ttu-id="d13e4-114">电子开票功能负责通过电子开票生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-114">The electronic invoicing features are responsible for generating electronic invoices through Electronic invoicing.</span></span> <span data-ttu-id="d13e4-115">它们封装配置规则，使用它们来处理 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 发送到电子开票和电子发票的数据。</span><span class="sxs-lookup"><span data-stu-id="d13e4-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to Electronic invoicing and to electronic invoices.</span></span>

<span data-ttu-id="d13e4-116">这些功能还支持需要符合文件格式规范且输出是独立电子文件的场景。</span><span class="sxs-lookup"><span data-stu-id="d13e4-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="d13e4-117">在大多数情况下，文件格式规范由税务主管机构发布。</span><span class="sxs-lookup"><span data-stu-id="d13e4-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="d13e4-118">最后，这些功能还支持与税务主管机构或某些认可方托管的外部 Web 服务交换消息，并支持请求授权或在电子发票中增加审核戳记。</span><span class="sxs-lookup"><span data-stu-id="d13e4-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="d13e4-119">电子开票功能的可用性</span><span class="sxs-lookup"><span data-stu-id="d13e4-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="d13e4-120">电子开票功能的可用性取决于国家或地区。</span><span class="sxs-lookup"><span data-stu-id="d13e4-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="d13e4-121">虽然有些功能已正式发布，但其他功能仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="d13e4-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="generally-available-features"></a><span data-ttu-id="d13e4-122">正式发布的功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-122">Generally available features</span></span>

<span data-ttu-id="d13e4-123">下表显示了正式发布的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-123">The following table shows the electronic invoicing features that are generally available.</span></span>

| <span data-ttu-id="d13e4-124">国家/地区</span><span class="sxs-lookup"><span data-stu-id="d13e4-124">Country/region</span></span> | <span data-ttu-id="d13e4-125">功能名称</span><span class="sxs-lookup"><span data-stu-id="d13e4-125">Feature name</span></span>                         | <span data-ttu-id="d13e4-126">业务文档</span><span class="sxs-lookup"><span data-stu-id="d13e4-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="d13e4-127">埃及</span><span class="sxs-lookup"><span data-stu-id="d13e4-127">Egypt</span></span>          | <span data-ttu-id="d13e4-128">埃及电子发票 (EG)</span><span class="sxs-lookup"><span data-stu-id="d13e4-128">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="d13e4-129">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-129">Sales invoices and project invoices</span></span> |

#### <a name="preview-features"></a><span data-ttu-id="d13e4-130">预览功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-130">Preview features</span></span>

<span data-ttu-id="d13e4-131">下表显示了当前处于预览阶段的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-131">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="d13e4-132">国家/地区</span><span class="sxs-lookup"><span data-stu-id="d13e4-132">Country/region</span></span> | <span data-ttu-id="d13e4-133">功能名称</span><span class="sxs-lookup"><span data-stu-id="d13e4-133">Feature name</span></span>                         | <span data-ttu-id="d13e4-134">业务文档</span><span class="sxs-lookup"><span data-stu-id="d13e4-134">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="d13e4-135">奥地利</span><span class="sxs-lookup"><span data-stu-id="d13e4-135">Austria</span></span>        | <span data-ttu-id="d13e4-136">奥地利电子发票 (AT)</span><span class="sxs-lookup"><span data-stu-id="d13e4-136">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="d13e4-137">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-137">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-138">比利时</span><span class="sxs-lookup"><span data-stu-id="d13e4-138">Belgium</span></span>        | <span data-ttu-id="d13e4-139">比利时电子发票 (BE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-139">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="d13e4-140">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-140">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-141">巴西</span><span class="sxs-lookup"><span data-stu-id="d13e4-141">Brazil</span></span>         | <span data-ttu-id="d13e4-142">巴西 NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-142">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="d13e4-143">会计单据模型 55，更正单、取消和弃用</span><span class="sxs-lookup"><span data-stu-id="d13e4-143">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="d13e4-144">巴西</span><span class="sxs-lookup"><span data-stu-id="d13e4-144">Brazil</span></span>         | <span data-ttu-id="d13e4-145">巴西 NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-145">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="d13e4-146">服务会计单据</span><span class="sxs-lookup"><span data-stu-id="d13e4-146">Service fiscal documents</span></span> |
| <span data-ttu-id="d13e4-147">丹麦</span><span class="sxs-lookup"><span data-stu-id="d13e4-147">Denmark</span></span>        | <span data-ttu-id="d13e4-148">丹麦电子发票 (DK)</span><span class="sxs-lookup"><span data-stu-id="d13e4-148">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="d13e4-149">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-149">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-150">爱沙尼亚</span><span class="sxs-lookup"><span data-stu-id="d13e4-150">Estonia</span></span>        | <span data-ttu-id="d13e4-151">爱沙尼亚电子发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-151">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="d13e4-152">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-152">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-153">芬兰</span><span class="sxs-lookup"><span data-stu-id="d13e4-153">Finland</span></span>        | <span data-ttu-id="d13e4-154">芬兰电子发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="d13e4-154">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="d13e4-155">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-155">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-156">法国</span><span class="sxs-lookup"><span data-stu-id="d13e4-156">France</span></span>         | <span data-ttu-id="d13e4-157">法国电子发票 (FR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-157">French electronic invoice (FR)</span></span>       | <span data-ttu-id="d13e4-158">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-158">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-159">德国</span><span class="sxs-lookup"><span data-stu-id="d13e4-159">Germany</span></span>        | <span data-ttu-id="d13e4-160">德国电子发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-160">German electronic invoice (DE)</span></span>       | <span data-ttu-id="d13e4-161">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-161">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-162">意大利</span><span class="sxs-lookup"><span data-stu-id="d13e4-162">Italy</span></span>          | <span data-ttu-id="d13e4-163">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="d13e4-163">FatturaPA (IT)</span></span>                       | <span data-ttu-id="d13e4-164">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-164">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-165">墨西哥</span><span class="sxs-lookup"><span data-stu-id="d13e4-165">Mexico</span></span>         | <span data-ttu-id="d13e4-166">墨西哥 CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-166">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="d13e4-167">销售发票、装箱单、库存转移、付款补充和取消</span><span class="sxs-lookup"><span data-stu-id="d13e4-167">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="d13e4-168">荷兰</span><span class="sxs-lookup"><span data-stu-id="d13e4-168">Netherlands</span></span>    | <span data-ttu-id="d13e4-169">荷兰电子发票 (NL)</span><span class="sxs-lookup"><span data-stu-id="d13e4-169">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="d13e4-170">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-170">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-171">挪威</span><span class="sxs-lookup"><span data-stu-id="d13e4-171">Norway</span></span>         | <span data-ttu-id="d13e4-172">挪威电子发票 (NO)</span><span class="sxs-lookup"><span data-stu-id="d13e4-172">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="d13e4-173">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-173">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-174">西班牙</span><span class="sxs-lookup"><span data-stu-id="d13e4-174">Spain</span></span>          | <span data-ttu-id="d13e4-175">西班牙电子发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="d13e4-175">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="d13e4-176">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-176">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="d13e4-177">欧洲</span><span class="sxs-lookup"><span data-stu-id="d13e4-177">Europe</span></span>         | <span data-ttu-id="d13e4-178">PEPPOL 电子发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-178">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="d13e4-179">PEPPOL 销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-179">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="d13e4-180">电子开票功能的可配置组件</span><span class="sxs-lookup"><span data-stu-id="d13e4-180">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="d13e4-181">电子开票功能由以下几组可配置组件组成：</span><span class="sxs-lookup"><span data-stu-id="d13e4-181">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="d13e4-182">**格式** – 格式让您可以配置当电子单据成为电子发票时电子开票必须生成的内容。</span><span class="sxs-lookup"><span data-stu-id="d13e4-182">**Formats** – Formats let you configure what Electronic invoicing must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="d13e4-183">格式包括电子发票的格式配置，以及当需要与外部 Web 服务通信时用于提交请求和接收响应的文件和消息的格式配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-183">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="d13e4-184">**操作** – 操作让您可以配置电子开票如何将 Finance 和 Supply Chain Management 提交的电子单据转换为电子发票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-184">**Actions** – Actions let you configure how Electronic invoicing generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="d13e4-185">**适用性规则** – 适用性规则让您可以配置电子开票在处理电子开票功能时必须考虑的上下文。</span><span class="sxs-lookup"><span data-stu-id="d13e4-185">**Applicability rules** – Applicability rules let you configure the context that Electronic invoicing must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="d13e4-186">**变量** – 变量让您可以配置对构造配置逻辑的支持。</span><span class="sxs-lookup"><span data-stu-id="d13e4-186">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="d13e4-187">变量可以用作执行特定操作的值的输入。</span><span class="sxs-lookup"><span data-stu-id="d13e4-187">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="d13e4-188">或者，还可以用作 Finance 和 Supply Chain Management 与电子开票之间的值的交换。</span><span class="sxs-lookup"><span data-stu-id="d13e4-188">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and Electronic invoicing.</span></span>
- <span data-ttu-id="d13e4-189">**电子单据模型映射** – 电子单据模型映射可让您配置 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="d13e4-189">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="d13e4-190">此模型映射定义提交电子单据时集成到电子开票中的摘要发票的数据映射。</span><span class="sxs-lookup"><span data-stu-id="d13e4-190">The model mapping defines the data mapping of the abstract invoice that is integrated into Electronic invoicing when electronic documents are submitted.</span></span>
- <span data-ttu-id="d13e4-191">**发票上下文模型** – 发票上下文模型让您可以配置 ER 发票上下文模型并定义电子开票功能的上下文。</span><span class="sxs-lookup"><span data-stu-id="d13e4-191">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="d13e4-192">**响应类型** – 响应类型让您可以配置由于进行电子发票处理，电子开票必须在 Finance 和 Supply Chain Management 中更新的内容。</span><span class="sxs-lookup"><span data-stu-id="d13e4-192">**Response types** – Response types let you configure what Electronic invoicing must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="d13e4-193">格式</span><span class="sxs-lookup"><span data-stu-id="d13e4-193">Formats</span></span>

<span data-ttu-id="d13e4-194">以下列表显示了可用于电子开票功能的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-194">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="d13e4-195">奥地利 (AT) 电子发票：奥地利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-195">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="d13e4-196">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-196">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="d13e4-197">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-197">OIOUBL Project invoice</span></span>
- <span data-ttu-id="d13e4-198">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-198">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="d13e4-199">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-199">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="d13e4-200">比利时 (BE) 电子发票：比利时的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-200">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="d13e4-201">UBL 销售发票 BE</span><span class="sxs-lookup"><span data-stu-id="d13e4-201">UBL Sales invoice BE</span></span>
- <span data-ttu-id="d13e4-202">UBL 项目发票 BE</span><span class="sxs-lookup"><span data-stu-id="d13e4-202">UBL Project invoice BE</span></span>
- <span data-ttu-id="d13e4-203">UBL 项目贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="d13e4-203">UBL Project credit note BE</span></span>
- <span data-ttu-id="d13e4-204">UBL 销售贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="d13e4-204">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="d13e4-205">巴西 (BR) NF-e：NF-e 联邦（巴西）</span><span class="sxs-lookup"><span data-stu-id="d13e4-205">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="d13e4-206">NF-e 提交导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-206">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="d13e4-207">NF-e 更正单导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-207">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="d13e4-208">NF-e 取消导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-208">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="d13e4-209">NF-e 弃用导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-209">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="d13e4-210">巴西 NFS-e (BR)：NFS-e ABRASF 库里蒂巴市</span><span class="sxs-lookup"><span data-stu-id="d13e4-210">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="d13e4-211">NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-211">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="d13e4-212">NFS-e ABRASF 查询库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="d13e4-212">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="d13e4-213">丹麦 (DK) 电子发票：丹麦的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-213">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="d13e4-214">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-214">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="d13e4-215">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-215">OIOUBL Project invoice</span></span>
- <span data-ttu-id="d13e4-216">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-216">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="d13e4-217">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-217">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="d13e4-218">荷兰 (NL) 电子发票：荷兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-218">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="d13e4-219">UBL 销售发票 NL</span><span class="sxs-lookup"><span data-stu-id="d13e4-219">UBL Sales invoice NL</span></span>
- <span data-ttu-id="d13e4-220">UBL 项目发票 NL</span><span class="sxs-lookup"><span data-stu-id="d13e4-220">UBL Project invoice NL</span></span>
- <span data-ttu-id="d13e4-221">UBL 项目贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="d13e4-221">UBL Project credit note NL</span></span>
- <span data-ttu-id="d13e4-222">UBL 销售贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="d13e4-222">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="d13e4-223">埃及 (EG) 电子发票：埃及的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-223">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="d13e4-224">销售发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="d13e4-224">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="d13e4-225">项目发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="d13e4-225">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="d13e4-226">爱沙尼亚 (EE) 电子发票：爱沙尼亚的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-226">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="d13e4-227">销售发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-227">Sales invoice (EE)</span></span>
- <span data-ttu-id="d13e4-228">项目发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-228">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="d13e4-229">芬兰 (FI) 电子发票：芬兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-229">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="d13e4-230">销售发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="d13e4-230">Sales invoice (FI)</span></span>
- <span data-ttu-id="d13e4-231">项目发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="d13e4-231">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="d13e4-232">法国 (FR) 电子发票：法国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-232">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="d13e4-233">UBL 销售发票 FR</span><span class="sxs-lookup"><span data-stu-id="d13e4-233">UBL Sales invoice FR</span></span>
- <span data-ttu-id="d13e4-234">UBL 项目发票 FR</span><span class="sxs-lookup"><span data-stu-id="d13e4-234">UBL Project invoice FR</span></span>
- <span data-ttu-id="d13e4-235">UBL 项目贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="d13e4-235">UBL Project credit note FR</span></span>
- <span data-ttu-id="d13e4-236">UBL 销售贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="d13e4-236">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="d13e4-237">德国 (DE) 电子发票：德国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-237">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="d13e4-238">销售发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-238">Sales invoice (DE)</span></span>
- <span data-ttu-id="d13e4-239">项目发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="d13e4-239">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="d13e4-240">意大利 (IT) 电子发票：意大利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-240">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="d13e4-241">销售发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="d13e4-241">Sales invoice (IT)</span></span>
- <span data-ttu-id="d13e4-242">项目发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="d13e4-242">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="d13e4-243">墨西哥 (MX) CFDI：墨西哥的 CFDI</span><span class="sxs-lookup"><span data-stu-id="d13e4-243">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="d13e4-244">CFDI 发票格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-244">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="d13e4-245">CFDI 装箱单 (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-245">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="d13e4-246">CFDI 库存转移 (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-246">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="d13e4-247">CFDI 付款格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-247">CFDI payment format (MX)</span></span>
- <span data-ttu-id="d13e4-248">CFDI 发票取消格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="d13e4-248">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="d13e4-249">挪威 (NO) 电子发票：挪威的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-249">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="d13e4-250">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-250">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="d13e4-251">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-251">OIOUBL Project invoice</span></span>
- <span data-ttu-id="d13e4-252">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-252">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="d13e4-253">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-253">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="d13e4-254">PEPPOL 电子发票：PEPPOL 销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-254">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="d13e4-255">PEPPOL 销售发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-255">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="d13e4-256">PEPPOL 项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-256">PEPPOL Project invoice</span></span>
- <span data-ttu-id="d13e4-257">PEPPOL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-257">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="d13e4-258">PEPPOL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="d13e4-258">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="d13e4-259">西班牙 (ES) 电子发票：西班牙的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-259">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="d13e4-260">销售发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="d13e4-260">Sales invoice (ES)</span></span>
- <span data-ttu-id="d13e4-261">项目发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="d13e4-261">Project invoice (ES)</span></span>

### <a name="actions"></a><span data-ttu-id="d13e4-262">操作​​</span><span class="sxs-lookup"><span data-stu-id="d13e4-262">Actions</span></span>

<span data-ttu-id="d13e4-263">下表列出了可用操作，以及这些操作当前是正式发布还是仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="d13e4-263">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="d13e4-264">行为</span><span class="sxs-lookup"><span data-stu-id="d13e4-264">Action</span></span>                                        | <span data-ttu-id="d13e4-265">说明</span><span class="sxs-lookup"><span data-stu-id="d13e4-265">Description</span></span>                                                                  | <span data-ttu-id="d13e4-266">可用性</span><span class="sxs-lookup"><span data-stu-id="d13e4-266">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="d13e4-267">转换文档</span><span class="sxs-lookup"><span data-stu-id="d13e4-267">Transform document</span></span>                            | <span data-ttu-id="d13e4-268">运行电子报告格式来转换文档。</span><span class="sxs-lookup"><span data-stu-id="d13e4-268">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="d13e4-269">正式发布</span><span class="sxs-lookup"><span data-stu-id="d13e4-269">Generally available</span></span>  |
| <span data-ttu-id="d13e4-270">对 xml 文档签名</span><span class="sxs-lookup"><span data-stu-id="d13e4-270">Sign xml document</span></span>                             | <span data-ttu-id="d13e4-271">使用数字签名对 xml 文档进行签名。</span><span class="sxs-lookup"><span data-stu-id="d13e4-271">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="d13e4-272">预览模式</span><span class="sxs-lookup"><span data-stu-id="d13e4-272">In preview</span></span>           |
| <span data-ttu-id="d13e4-273">对埃及税务主管机构的 json 文档签名</span><span class="sxs-lookup"><span data-stu-id="d13e4-273">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="d13e4-274">使用数字签名对埃及税务主管机构的 json 文档签名。</span><span class="sxs-lookup"><span data-stu-id="d13e4-274">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="d13e4-275">正式发布</span><span class="sxs-lookup"><span data-stu-id="d13e4-275">Generally available</span></span>  |
| <span data-ttu-id="d13e4-276">与埃及 ETA 服务集成</span><span class="sxs-lookup"><span data-stu-id="d13e4-276">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="d13e4-277">与埃及税务主管机构通信。</span><span class="sxs-lookup"><span data-stu-id="d13e4-277">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="d13e4-278">正式发布</span><span class="sxs-lookup"><span data-stu-id="d13e4-278">Generally available</span></span>  |
| <span data-ttu-id="d13e4-279">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="d13e4-279">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="d13e4-280">与巴西 SEFAZ 服务集成以提交会计单据。</span><span class="sxs-lookup"><span data-stu-id="d13e4-280">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="d13e4-281">预览模式</span><span class="sxs-lookup"><span data-stu-id="d13e4-281">In preview</span></span>           |
| <span data-ttu-id="d13e4-282">调用墨西哥 PAC 服务</span><span class="sxs-lookup"><span data-stu-id="d13e4-282">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="d13e4-283">与墨西哥 PAC 服务集成以提交 CFDI。</span><span class="sxs-lookup"><span data-stu-id="d13e4-283">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="d13e4-284">预览模式</span><span class="sxs-lookup"><span data-stu-id="d13e4-284">In preview</span></span>           |
| <span data-ttu-id="d13e4-285">处理响应</span><span class="sxs-lookup"><span data-stu-id="d13e4-285">Process response</span></span>                              | <span data-ttu-id="d13e4-286">分析从 Web 服务调用收到的响应。</span><span class="sxs-lookup"><span data-stu-id="d13e4-286">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="d13e4-287">正式发布</span><span class="sxs-lookup"><span data-stu-id="d13e4-287">Generally available</span></span>  |
| <span data-ttu-id="d13e4-288">使用 MS Power Automate</span><span class="sxs-lookup"><span data-stu-id="d13e4-288">Use MS Power Automate</span></span>                         | <span data-ttu-id="d13e4-289">与 Microsoft Power Automate 内置流集成。</span><span class="sxs-lookup"><span data-stu-id="d13e4-289">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="d13e4-290">预览模式</span><span class="sxs-lookup"><span data-stu-id="d13e4-290">In preview</span></span>           |

### <a name="applicability-rules"></a><span data-ttu-id="d13e4-291">适用性规则</span><span class="sxs-lookup"><span data-stu-id="d13e4-291">Applicability rules</span></span>

<span data-ttu-id="d13e4-292">适用性规则是在电子开票功能级别定义的可配置子句。</span><span class="sxs-lookup"><span data-stu-id="d13e4-292">Applicability rules are configurable clauses that are defined at the Electronic invoicing feature level.</span></span> <span data-ttu-id="d13e4-293">规则配置为通过电子开票功能集提供用于执行电子开票功能的上下文。</span><span class="sxs-lookup"><span data-stu-id="d13e4-293">The rules are configured to provide a context for execution of electronic invoicing features through the Electronic Invoicing capability set.</span></span>

<span data-ttu-id="d13e4-294">当 Finance 或 Supply Chain Management 中的业务文档提交到电子开票时，该业务文档不带有允许电子开票功能集调用特定电子开票功能处理提交的显式引用。</span><span class="sxs-lookup"><span data-stu-id="d13e4-294">When a business document from Finance or Supply Chain Management is submitted to electronic invoicing, the business document doesn't carry an explicit reference that allows the Electronic Invoicing capability set to call a particular electronic invoicing feature to process the submission.</span></span>

<span data-ttu-id="d13e4-295">但是，如果配置正确，业务文档将包含允许电子开票解决必须选择哪个电子开票功能，然后生成电子发票的必要元素。</span><span class="sxs-lookup"><span data-stu-id="d13e4-295">Nevertheless, when properly configured, the business document contains the necessary elements that allow electronic invoicing to resolve which electronic invoicing feature must be selected and then generate the electronic invoice.</span></span>

<span data-ttu-id="d13e4-296">适用性规则允许电子开票功能集找到必须用于处理提交的确切电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-296">Applicability rules allow the Electronic Invoicing capability set to find the exact electronic invoicing features that must be used to process the submission.</span></span> <span data-ttu-id="d13e4-297">通过将提交的业务文档中的内容与适用性规则中的子句进行匹配来完成此操作。</span><span class="sxs-lookup"><span data-stu-id="d13e4-297">This is done by matching the contents from the submitted business document with the clauses from the Applicability rules.</span></span>

<span data-ttu-id="d13e4-298">例如，将具有相关适用性规则的两个电子开票功能部署到电子开票功能集中。</span><span class="sxs-lookup"><span data-stu-id="d13e4-298">For example, two electronic invoicing features with related Applicability rules are deployed into the Electronic Invoicing capability set.</span></span>

| <span data-ttu-id="d13e4-299">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-299">Electronic invoicing feature</span></span> | <span data-ttu-id="d13e4-300">适用性规则</span><span class="sxs-lookup"><span data-stu-id="d13e4-300">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="d13e4-301">A</span><span class="sxs-lookup"><span data-stu-id="d13e4-301">A</span></span>                            | <p><span data-ttu-id="d13e4-302">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-302">Country = BR</span></span></p><p><span data-ttu-id="d13e4-303">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-303">and</span></span></p><p><span data-ttu-id="d13e4-304">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-304">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="d13e4-305">B</span><span class="sxs-lookup"><span data-stu-id="d13e4-305">B</span></span>                            | <p><span data-ttu-id="d13e4-306">国家/地区 = MX</span><span class="sxs-lookup"><span data-stu-id="d13e4-306">Country = MX</span></span></p><p><span data-ttu-id="d13e4-307">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-307">and</span></span></p><p><span data-ttu-id="d13e4-308">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-308">Legal entity = MXMF</span></span></p>  |

<span data-ttu-id="d13e4-309">如果 Finance 或 Supply Chain Management 中的业务文档提交到电子开票功能集，业务文档将包含以下属性，并填充为：</span><span class="sxs-lookup"><span data-stu-id="d13e4-309">If a business document from Finance or Supply Chain Management is submitted to the Electronic Invoicing capability set, the business document contains the following attributes filled as:</span></span>

- <span data-ttu-id="d13e4-310">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-310">Country = BR</span></span>
- <span data-ttu-id="d13e4-311">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-311">Legal entity = BRMF</span></span>

<span data-ttu-id="d13e4-312">电子开票功能集将选择电子开票功能 **A** 处理提交并生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-312">The Electronic Invoicing capability set will select the electronic invoicing feature **A** to process the submission and generate the electronic invoice.</span></span>

<span data-ttu-id="d13e4-313">同样，如果业务文档包含：</span><span class="sxs-lookup"><span data-stu-id="d13e4-313">In the same way, if the business document contains:</span></span>

- <span data-ttu-id="d13e4-314">国家/地区 = MX</span><span class="sxs-lookup"><span data-stu-id="d13e4-314">Country = MX</span></span>
- <span data-ttu-id="d13e4-315">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-315">Legal entity = MXMF</span></span>

<span data-ttu-id="d13e4-316">选择电子开票功能 **B** 以生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-316">Electronic invoicing feature **B** is selected to generate the electronic invoice.</span></span>

<span data-ttu-id="d13e4-317">适用性规则的配置必须明确。</span><span class="sxs-lookup"><span data-stu-id="d13e4-317">The configuration of Applicability rules can't be ambiguous.</span></span> <span data-ttu-id="d13e4-318">这意味着两个或多个电子开票功能不能具有相同的子句，否则将导致无法选择。</span><span class="sxs-lookup"><span data-stu-id="d13e4-318">This means that two or more electronic invoicing features can't have the same clauses, otherwise it will lead to no selection.</span></span> <span data-ttu-id="d13e4-319">如果电子开票功能重复，为避免歧义，请使用其他子句以使电子开票功能集能够区分这两个电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-319">If there is a duplication of electronic invoicing features, to avoid ambiguity, use additional clauses to allow the Electronic Invoicing capability set to distinguish between the two electronic invoicing features.</span></span>

<span data-ttu-id="d13e4-320">例如，考虑电子开票功能 **C**。此功能是电子开票功能 **A** 的副本。</span><span class="sxs-lookup"><span data-stu-id="d13e4-320">For example, consider electronic invoicing feature **C**. This feature is a copy of electronic invoicing feature **A**.</span></span>

| <span data-ttu-id="d13e4-321">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-321">Electronic invoicing feature</span></span> | <span data-ttu-id="d13e4-322">适用性规则</span><span class="sxs-lookup"><span data-stu-id="d13e4-322">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="d13e4-323">A</span><span class="sxs-lookup"><span data-stu-id="d13e4-323">A</span></span>                            | <p><span data-ttu-id="d13e4-324">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-324">Country = BR</span></span></p><p><span data-ttu-id="d13e4-325">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-325">and</span></span></p><p><span data-ttu-id="d13e4-326">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-326">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="d13e4-327">C</span><span class="sxs-lookup"><span data-stu-id="d13e4-327">C</span></span>                            | <p><span data-ttu-id="d13e4-328">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-328">Country = BR</span></span></p><p><span data-ttu-id="d13e4-329">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-329">and</span></span></p><p><span data-ttu-id="d13e4-330">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-330">Legal entity = BRMF</span></span></p>  |

<span data-ttu-id="d13e4-331">在此示例中，功能 **C** 在包含以下内容的业务文档提交之前：</span><span class="sxs-lookup"><span data-stu-id="d13e4-331">In this example, feature **C** is in front of a business document submission that contains the following:</span></span>

- <span data-ttu-id="d13e4-332">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-332">Country = BR</span></span>
- <span data-ttu-id="d13e4-333">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-333">Legal entity = BRMF</span></span>

<span data-ttu-id="d13e4-334">电子开票功能无法区分必须用于处理提交的电子开票功能，因为提交包含完全相同的子句。</span><span class="sxs-lookup"><span data-stu-id="d13e4-334">The Electronic Invoicing capability can't distinguish which electronic invoicing feature must be used to process the submission because the submissions contain the exact same clauses.</span></span>

<span data-ttu-id="d13e4-335">若要通过适用性规则在两个功能之间进行区分，必须在其中一个功能中添加新子句，以允许电子开票功能集选择适当的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-335">To create a distinction between the two features through Applicability rules, a new clause must be added to one of the features to allow the Electronic Invoicing capability set to select the proper electronic invoicing feature.</span></span>

| <span data-ttu-id="d13e4-336">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-336">Electronic invoicing feature</span></span> | <span data-ttu-id="d13e4-337">适用性规则</span><span class="sxs-lookup"><span data-stu-id="d13e4-337">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="d13e4-338">A</span><span class="sxs-lookup"><span data-stu-id="d13e4-338">A</span></span>                            | <p><span data-ttu-id="d13e4-339">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-339">Country = BR</span></span></p><p><span data-ttu-id="d13e4-340">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-340">and</span></span></p><p><span data-ttu-id="d13e4-341">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-341">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="d13e4-342">C</span><span class="sxs-lookup"><span data-stu-id="d13e4-342">C</span></span>                            | <p><span data-ttu-id="d13e4-343">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-343">Country = BR</span></span></p><p><span data-ttu-id="d13e4-344">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-344">and</span></span></p><p><span data-ttu-id="d13e4-345">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-345">Legal entity = BRMF</span></span></p><p><span data-ttu-id="d13e4-346">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-346">and</span></span></p><p><span data-ttu-id="d13e4-347">模型 = 55</span><span class="sxs-lookup"><span data-stu-id="d13e4-347">Model=55</span></span></p>  |

<span data-ttu-id="d13e4-348">若要支持创建更复杂的子句，可以使用以下资源：</span><span class="sxs-lookup"><span data-stu-id="d13e4-348">To support creating more complex clauses, the following resources are available:</span></span>

<span data-ttu-id="d13e4-349">逻辑运算符：</span><span class="sxs-lookup"><span data-stu-id="d13e4-349">Logic operators:</span></span>
- <span data-ttu-id="d13e4-350">并</span><span class="sxs-lookup"><span data-stu-id="d13e4-350">And</span></span>
- <span data-ttu-id="d13e4-351">或</span><span class="sxs-lookup"><span data-stu-id="d13e4-351">Or</span></span>

<span data-ttu-id="d13e4-352">运算符类型：</span><span class="sxs-lookup"><span data-stu-id="d13e4-352">Operators types:</span></span>
- <span data-ttu-id="d13e4-353">Equal</span><span class="sxs-lookup"><span data-stu-id="d13e4-353">Equal</span></span>
- <span data-ttu-id="d13e4-354">Not equal</span><span class="sxs-lookup"><span data-stu-id="d13e4-354">Not equal</span></span>
- <span data-ttu-id="d13e4-355">Greater than</span><span class="sxs-lookup"><span data-stu-id="d13e4-355">Greater than</span></span>
- <span data-ttu-id="d13e4-356">Less than</span><span class="sxs-lookup"><span data-stu-id="d13e4-356">Less than</span></span>
- <span data-ttu-id="d13e4-357">大于等于</span><span class="sxs-lookup"><span data-stu-id="d13e4-357">Greater than or equal to</span></span>
- <span data-ttu-id="d13e4-358">小于等于</span><span class="sxs-lookup"><span data-stu-id="d13e4-358">Less than or equal to</span></span>
- <span data-ttu-id="d13e4-359">Contains</span><span class="sxs-lookup"><span data-stu-id="d13e4-359">Contains</span></span>
- <span data-ttu-id="d13e4-360">开头是</span><span class="sxs-lookup"><span data-stu-id="d13e4-360">Begins with</span></span>

<span data-ttu-id="d13e4-361">数据类型：</span><span class="sxs-lookup"><span data-stu-id="d13e4-361">Data types:</span></span>
- <span data-ttu-id="d13e4-362">字符串</span><span class="sxs-lookup"><span data-stu-id="d13e4-362">String</span></span>
- <span data-ttu-id="d13e4-363">数值</span><span class="sxs-lookup"><span data-stu-id="d13e4-363">Number</span></span>
- <span data-ttu-id="d13e4-364">布尔</span><span class="sxs-lookup"><span data-stu-id="d13e4-364">Boolean</span></span>
- <span data-ttu-id="d13e4-365">日期</span><span class="sxs-lookup"><span data-stu-id="d13e4-365">Date</span></span>
- <span data-ttu-id="d13e4-366">UUID</span><span class="sxs-lookup"><span data-stu-id="d13e4-366">UUID</span></span>

<span data-ttu-id="d13e4-367">分组和取消分组子句的功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-367">Capability to group and ungroup clauses.</span></span>
<span data-ttu-id="d13e4-368">示例如下所示。</span><span class="sxs-lookup"><span data-stu-id="d13e4-368">The example looks like this.</span></span>

| <span data-ttu-id="d13e4-369">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-369">Electronic invoicing feature</span></span> | <span data-ttu-id="d13e4-370">适用性规则</span><span class="sxs-lookup"><span data-stu-id="d13e4-370">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="d13e4-371">C</span><span class="sxs-lookup"><span data-stu-id="d13e4-371">C</span></span>                            | <p><span data-ttu-id="d13e4-372">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="d13e4-372">Country = BR</span></span></p><p><span data-ttu-id="d13e4-373">与</span><span class="sxs-lookup"><span data-stu-id="d13e4-373">and</span></span></p><p><span data-ttu-id="d13e4-374">（法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="d13e4-374">( Legal entity = BRMF</span></span></p><p><span data-ttu-id="d13e4-375">或</span><span class="sxs-lookup"><span data-stu-id="d13e4-375">or</span></span></p><p><span data-ttu-id="d13e4-376">模型 = 55）</span><span class="sxs-lookup"><span data-stu-id="d13e4-376">Model=55)</span></span></p>  |


## <a name="configuration-providers"></a><span data-ttu-id="d13e4-377">配置提供方</span><span class="sxs-lookup"><span data-stu-id="d13e4-377">Configuration providers</span></span>

<span data-ttu-id="d13e4-378">配置提供者提供电子开票功能及其 ER 组件，如模型映射、格式配置和上下文模型。</span><span class="sxs-lookup"><span data-stu-id="d13e4-378">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="d13e4-379">他们在关联的全局存储库中发布电子开票功能和 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="d13e4-379">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="d13e4-380">从那里，其他组织可以下载这些功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-380">From there, other organizations can download them.</span></span>

<span data-ttu-id="d13e4-381">在通过 RCS 配置电子开票功能之前，您必须在 **电子报告** 模块中将自己的组织配置为配置提供者。</span><span class="sxs-lookup"><span data-stu-id="d13e4-381">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="d13e4-382">有关如何将配置提供者设置为 **活动** 的信息，请参阅[创建配置提供者并将其标记为活动](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="d13e4-382">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="d13e4-383">查看全局存储库中的电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-383">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="d13e4-384">要浏览特定配置提供者的全局存储库中可用的电子开票功能，请同步组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="d13e4-384">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="d13e4-385">完成同步后，可用电子开票功能的列表将更新。</span><span class="sxs-lookup"><span data-stu-id="d13e4-385">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="d13e4-386">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-386">Importing electronic invoicing features</span></span>

<span data-ttu-id="d13e4-387">在使用或配置电子开票功能之前，必须将它们导入组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="d13e4-387">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="d13e4-388">导入操作将创建功能的本地副本，并将功能使用的所有 ER 项目（例如，格式配置和模型配置）复制到组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="d13e4-388">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="d13e4-389">您可以从任何配置提供者导入电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-389">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="d13e4-390">创建电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-390">Creating electronic invoicing features</span></span>

<span data-ttu-id="d13e4-391">您可以从头创建电子开票功能，也可以从另一个电子开票功能派生。</span><span class="sxs-lookup"><span data-stu-id="d13e4-391">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="d13e4-392">从头创建电子开票功能时，必须手动添加 ER 组件（例如，功能版本配置和其他配置，如功能版本设置和应用程序设置）。</span><span class="sxs-lookup"><span data-stu-id="d13e4-392">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="d13e4-393">通过从另一个功能派生来创建功能时，新功能将继承原始功能的所有配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-393">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="d13e4-394">电子开票功能版本</span><span class="sxs-lookup"><span data-stu-id="d13e4-394">Electronic invoicing feature version</span></span>

<span data-ttu-id="d13e4-395">电子开票功能已版本化。</span><span class="sxs-lookup"><span data-stu-id="d13e4-395">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="d13e4-396">新版本创建时，版本号会自动递增。</span><span class="sxs-lookup"><span data-stu-id="d13e4-396">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="d13e4-397">可以为新版本定义“生效开始”日期。</span><span class="sxs-lookup"><span data-stu-id="d13e4-397">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="d13e4-398">电子开票功能版本采用的生命周期最多包含以下三种状态：</span><span class="sxs-lookup"><span data-stu-id="d13e4-398">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="d13e4-399">**草稿** – 如果功能版本处于此状态，您可以编辑其配置属性及其任何项目（例如，文件格式配置）。</span><span class="sxs-lookup"><span data-stu-id="d13e4-399">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="d13e4-400">**完成** – 如果功能版本处于此状态，说明该功能版本已发布到与您的组织关联的全局存储库中。</span><span class="sxs-lookup"><span data-stu-id="d13e4-400">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="d13e4-401">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="d13e4-401">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="d13e4-402">**已发布** – 如果功能版本处于此状态，说明该功能版本已发布到电子开票。</span><span class="sxs-lookup"><span data-stu-id="d13e4-402">**Published** – If a feature version is in this status, it has been published to Electronic invoicing.</span></span> <span data-ttu-id="d13e4-403">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="d13e4-403">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="d13e4-404">功能配置</span><span class="sxs-lookup"><span data-stu-id="d13e4-404">Feature configurations</span></span>

<span data-ttu-id="d13e4-405">功能配置保留电子开票功能使用的所有 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-405">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="d13e4-406">电子开票功能在处理期间使用的所有电子文件都来自已添加到该功能的功能配置中的格式配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-406">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="d13e4-407">从功能配置，您可以访问 ER 格式设计器，这是用于创建格式配置的 ER 工具。</span><span class="sxs-lookup"><span data-stu-id="d13e4-407">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="d13e4-408">功能设置</span><span class="sxs-lookup"><span data-stu-id="d13e4-408">Feature setup</span></span>

<span data-ttu-id="d13e4-409">功能设置与功能配置结合使用。</span><span class="sxs-lookup"><span data-stu-id="d13e4-409">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="d13e4-410">每个功能设置都封装了一组提供预期行为的操作、适用性规则和变量，让电子开票功能可以满足电子发票的特定要求。</span><span class="sxs-lookup"><span data-stu-id="d13e4-410">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="d13e4-411">应用程序设置</span><span class="sxs-lookup"><span data-stu-id="d13e4-411">Application setup</span></span>

<span data-ttu-id="d13e4-412">应用程序设置必须与先前创建的已连接应用程序关联。</span><span class="sxs-lookup"><span data-stu-id="d13e4-412">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="d13e4-413">通过应用程序设置，您可以配置必须在 Finance 和 Supply Chain Management 中进行的电子开票功能的那一部分。</span><span class="sxs-lookup"><span data-stu-id="d13e4-413">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="d13e4-414">不论是什么电子开票功能，都至少必须有三个可配置组件：</span><span class="sxs-lookup"><span data-stu-id="d13e4-414">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="d13e4-415">**表名称** – Finance 和 Supply Chain Management 中的实体，保留过帐的发票，电子开票功能基于此实体。</span><span class="sxs-lookup"><span data-stu-id="d13e4-415">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="d13e4-416">**上下文** – 通过 ER 配置的发票上下文模型的名称。</span><span class="sxs-lookup"><span data-stu-id="d13e4-416">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="d13e4-417">**业务文档映射** – 通过 ER 配置的发票映射模型的名称。</span><span class="sxs-lookup"><span data-stu-id="d13e4-417">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d13e4-418">可以在 Finance 和 Supply Chain Management 中查看在应用程序设置中输入的配置。</span><span class="sxs-lookup"><span data-stu-id="d13e4-418">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="d13e4-419">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="d13e4-419">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="d13e4-420">在 **电子单据** 选项卡上，选择 **部署**，然后选择 **相连应用程序** 选项。</span><span class="sxs-lookup"><span data-stu-id="d13e4-420">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="d13e4-421">部署功能版本</span><span class="sxs-lookup"><span data-stu-id="d13e4-421">Deploying feature versions</span></span>

<span data-ttu-id="d13e4-422">在 RCS 中，您使用 **部署** 命令定向发布电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="d13e4-422">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="d13e4-423">选择 **部署**，然后选择以下选项之一定义部署目标：</span><span class="sxs-lookup"><span data-stu-id="d13e4-423">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="d13e4-424">**服务环境** – 当部署的目标是服务环境时，电子开票功能版本将发布到服务环境。</span><span class="sxs-lookup"><span data-stu-id="d13e4-424">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="d13e4-425">然后，电子开票就可以接收和处理 Finance 和 Supply Chain Management 发送的电子单据。</span><span class="sxs-lookup"><span data-stu-id="d13e4-425">Electronic invoicing is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="d13e4-426">**相连应用程序** – 当部署的目标是相连应用程序时，由应用程序安装程序提供的配置将写入先前与之关联的 Finance 和 Supply Chain Management 实例中。</span><span class="sxs-lookup"><span data-stu-id="d13e4-426">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="d13e4-427">仅状态为 **已完成** 的电子开票功能版本可以部署到服务环境或连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="d13e4-427">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="d13e4-428">删除功能版本</span><span class="sxs-lookup"><span data-stu-id="d13e4-428">Removing feature versions</span></span>

<span data-ttu-id="d13e4-429">在 RCS 中，您使用 **取消部署** 命令从电子开票中的服务环境中删除特定的电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="d13e4-429">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in Electronic invoicing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d13e4-430">**取消部署** 命令仅在服务环境中有效。</span><span class="sxs-lookup"><span data-stu-id="d13e4-430">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="d13e4-431">它不会从连接的应用程序中删除电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="d13e4-431">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="d13e4-432">重定电子开票功能</span><span class="sxs-lookup"><span data-stu-id="d13e4-432">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="d13e4-433">当一个电子开票功能是从另一个电子开票功能派生而来时，**重定** 命令使用原始功能中引入的更改来更新派生功能。</span><span class="sxs-lookup"><span data-stu-id="d13e4-433">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d13e4-434">其他资源</span><span class="sxs-lookup"><span data-stu-id="d13e4-434">Additional resources</span></span>

- [<span data-ttu-id="d13e4-435">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="d13e4-435">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
