---
title: 在 Regulatory Configuration Services (RCS) 中配置电子开票
description: 本主题说明如何在 Dynamics 365 Regulatory Configuration Services (RCS) 中配置电子开票。
author: gionoder
ms.date: 05/19/2021
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
ms.openlocfilehash: 6c1d309744c4c8dd0d17f5259551d31c257ede61
ms.sourcegitcommit: 633d51834d7d29b745824924315a3898dc471f1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/19/2021
ms.locfileid: "6075135"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="1b035-103">在 Regulatory Configuration Services (RCS) 中配置电子开票</span><span class="sxs-lookup"><span data-stu-id="1b035-103">Configure Electronic invoicing in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b035-104">本主题提供有关 Dynamics 365 Regulatory Configuration Services (RCS) 中电子开票的配置功能的信息。</span><span class="sxs-lookup"><span data-stu-id="1b035-104">This topic provides information about the configuration capabilities of Electronic invoicing in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="1b035-105">通过配置功能，电子开票可帮助您满足电子发票的业务和法规要求，而无需进行任何编码。</span><span class="sxs-lookup"><span data-stu-id="1b035-105">It is through the configuration capabilities that Electronic invoicing helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="1b035-106">而且，在电子发票必须由 Web 服务以电子方式审核的情况下，配置功能还可以帮助您满足与 Web 服务交换消息的要求，无需编写任何代码。</span><span class="sxs-lookup"><span data-stu-id="1b035-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="1b035-107">电子报告</span><span class="sxs-lookup"><span data-stu-id="1b035-107">Electronic reporting</span></span>

<span data-ttu-id="1b035-108">电子报告 (ER) 支持电子开票。</span><span class="sxs-lookup"><span data-stu-id="1b035-108">Electronic reporting (ER) supports Electronic invoicing.</span></span>

<span data-ttu-id="1b035-109">数据模型映射和格式是可配置的组件，可通过 ER 创建和维护，在电子开票中使用。</span><span class="sxs-lookup"><span data-stu-id="1b035-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in Electronic invoicing.</span></span> <span data-ttu-id="1b035-110">ER 格式设计器是用于创建和维护文件格式的工具。</span><span class="sxs-lookup"><span data-stu-id="1b035-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="1b035-111">用于配置电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="1b035-112">有关详细信息，请参阅[电子报告 (ER) 概述](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="1b035-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="1b035-113">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-113">Electronic invoicing features</span></span>

<span data-ttu-id="1b035-114">电子开票功能负责通过电子开票生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="1b035-114">The electronic invoicing features are responsible for generating electronic invoices through Electronic invoicing.</span></span> <span data-ttu-id="1b035-115">它们封装配置规则，使用它们来处理 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 发送到电子开票和电子发票的数据。</span><span class="sxs-lookup"><span data-stu-id="1b035-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to Electronic invoicing and to electronic invoices.</span></span>

<span data-ttu-id="1b035-116">这些功能还支持需要符合文件格式规范且输出是独立电子文件的场景。</span><span class="sxs-lookup"><span data-stu-id="1b035-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="1b035-117">在大多数情况下，文件格式规范由税务主管机构发布。</span><span class="sxs-lookup"><span data-stu-id="1b035-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="1b035-118">最后，这些功能还支持与税务主管机构或某些认可方托管的外部 Web 服务交换消息，并支持请求授权或在电子发票中增加审核戳记。</span><span class="sxs-lookup"><span data-stu-id="1b035-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="1b035-119">电子开票功能的可用性</span><span class="sxs-lookup"><span data-stu-id="1b035-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="1b035-120">电子开票功能的可用性取决于国家或地区。</span><span class="sxs-lookup"><span data-stu-id="1b035-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="1b035-121">虽然有些功能已正式发布，但其他功能仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="1b035-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="generally-available-features"></a><span data-ttu-id="1b035-122">正式发布的功能</span><span class="sxs-lookup"><span data-stu-id="1b035-122">Generally available features</span></span>

<span data-ttu-id="1b035-123">下表显示了正式发布的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-123">The following table shows the electronic invoicing features that are generally available.</span></span>

| <span data-ttu-id="1b035-124">国家/地区</span><span class="sxs-lookup"><span data-stu-id="1b035-124">Country/region</span></span> | <span data-ttu-id="1b035-125">功能名称</span><span class="sxs-lookup"><span data-stu-id="1b035-125">Feature name</span></span>                         | <span data-ttu-id="1b035-126">业务文档</span><span class="sxs-lookup"><span data-stu-id="1b035-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="1b035-127">埃及</span><span class="sxs-lookup"><span data-stu-id="1b035-127">Egypt</span></span>          | <span data-ttu-id="1b035-128">埃及电子发票 (EG)</span><span class="sxs-lookup"><span data-stu-id="1b035-128">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="1b035-129">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-129">Sales invoices and project invoices</span></span> |

#### <a name="preview-features"></a><span data-ttu-id="1b035-130">预览功能</span><span class="sxs-lookup"><span data-stu-id="1b035-130">Preview features</span></span>

<span data-ttu-id="1b035-131">下表显示了当前处于预览阶段的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-131">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="1b035-132">国家/地区</span><span class="sxs-lookup"><span data-stu-id="1b035-132">Country/region</span></span> | <span data-ttu-id="1b035-133">功能名称</span><span class="sxs-lookup"><span data-stu-id="1b035-133">Feature name</span></span>                         | <span data-ttu-id="1b035-134">业务文档</span><span class="sxs-lookup"><span data-stu-id="1b035-134">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="1b035-135">奥地利</span><span class="sxs-lookup"><span data-stu-id="1b035-135">Austria</span></span>        | <span data-ttu-id="1b035-136">奥地利电子发票 (AT)</span><span class="sxs-lookup"><span data-stu-id="1b035-136">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="1b035-137">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-137">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-138">比利时</span><span class="sxs-lookup"><span data-stu-id="1b035-138">Belgium</span></span>        | <span data-ttu-id="1b035-139">比利时电子发票 (BE)</span><span class="sxs-lookup"><span data-stu-id="1b035-139">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="1b035-140">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-140">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-141">巴西</span><span class="sxs-lookup"><span data-stu-id="1b035-141">Brazil</span></span>         | <span data-ttu-id="1b035-142">巴西 NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-142">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="1b035-143">会计单据模型 55，更正单、取消和弃用</span><span class="sxs-lookup"><span data-stu-id="1b035-143">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="1b035-144">巴西</span><span class="sxs-lookup"><span data-stu-id="1b035-144">Brazil</span></span>         | <span data-ttu-id="1b035-145">巴西 NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-145">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="1b035-146">服务会计单据</span><span class="sxs-lookup"><span data-stu-id="1b035-146">Service fiscal documents</span></span> |
| <span data-ttu-id="1b035-147">丹麦</span><span class="sxs-lookup"><span data-stu-id="1b035-147">Denmark</span></span>        | <span data-ttu-id="1b035-148">丹麦电子发票 (DK)</span><span class="sxs-lookup"><span data-stu-id="1b035-148">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="1b035-149">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-149">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-150">爱沙尼亚</span><span class="sxs-lookup"><span data-stu-id="1b035-150">Estonia</span></span>        | <span data-ttu-id="1b035-151">爱沙尼亚电子发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="1b035-151">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="1b035-152">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-152">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-153">芬兰</span><span class="sxs-lookup"><span data-stu-id="1b035-153">Finland</span></span>        | <span data-ttu-id="1b035-154">芬兰电子发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="1b035-154">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="1b035-155">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-155">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-156">法国</span><span class="sxs-lookup"><span data-stu-id="1b035-156">France</span></span>         | <span data-ttu-id="1b035-157">法国电子发票 (FR)</span><span class="sxs-lookup"><span data-stu-id="1b035-157">French electronic invoice (FR)</span></span>       | <span data-ttu-id="1b035-158">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-158">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-159">德国</span><span class="sxs-lookup"><span data-stu-id="1b035-159">Germany</span></span>        | <span data-ttu-id="1b035-160">德国电子发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="1b035-160">German electronic invoice (DE)</span></span>       | <span data-ttu-id="1b035-161">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-161">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-162">意大利</span><span class="sxs-lookup"><span data-stu-id="1b035-162">Italy</span></span>          | <span data-ttu-id="1b035-163">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="1b035-163">FatturaPA (IT)</span></span>                       | <span data-ttu-id="1b035-164">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-164">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-165">墨西哥</span><span class="sxs-lookup"><span data-stu-id="1b035-165">Mexico</span></span>         | <span data-ttu-id="1b035-166">墨西哥 CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-166">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="1b035-167">销售发票、装箱单、库存转移、付款补充和取消</span><span class="sxs-lookup"><span data-stu-id="1b035-167">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="1b035-168">荷兰</span><span class="sxs-lookup"><span data-stu-id="1b035-168">Netherlands</span></span>    | <span data-ttu-id="1b035-169">荷兰电子发票 (NL)</span><span class="sxs-lookup"><span data-stu-id="1b035-169">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="1b035-170">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-170">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-171">挪威</span><span class="sxs-lookup"><span data-stu-id="1b035-171">Norway</span></span>         | <span data-ttu-id="1b035-172">挪威电子发票 (NO)</span><span class="sxs-lookup"><span data-stu-id="1b035-172">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="1b035-173">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-173">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-174">西班牙</span><span class="sxs-lookup"><span data-stu-id="1b035-174">Spain</span></span>          | <span data-ttu-id="1b035-175">西班牙电子发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="1b035-175">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="1b035-176">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-176">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="1b035-177">欧洲</span><span class="sxs-lookup"><span data-stu-id="1b035-177">Europe</span></span>         | <span data-ttu-id="1b035-178">PEPPOL 电子发票</span><span class="sxs-lookup"><span data-stu-id="1b035-178">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="1b035-179">PEPPOL 销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-179">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="1b035-180">电子开票功能的可配置组件</span><span class="sxs-lookup"><span data-stu-id="1b035-180">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="1b035-181">电子开票功能由以下几组可配置组件组成：</span><span class="sxs-lookup"><span data-stu-id="1b035-181">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="1b035-182">**格式** – 格式让您可以配置当电子单据成为电子发票时电子开票必须生成的内容。</span><span class="sxs-lookup"><span data-stu-id="1b035-182">**Formats** – Formats let you configure what Electronic invoicing must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="1b035-183">格式包括电子发票的格式配置，以及当需要与外部 Web 服务通信时用于提交请求和接收响应的文件和消息的格式配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-183">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="1b035-184">**操作** – 操作让您可以配置电子开票如何将 Finance 和 Supply Chain Management 提交的电子单据转换为电子发票。</span><span class="sxs-lookup"><span data-stu-id="1b035-184">**Actions** – Actions let you configure how Electronic invoicing generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="1b035-185">**适用性规则** – 适用性规则让您可以配置电子开票在处理电子开票功能时必须考虑的上下文。</span><span class="sxs-lookup"><span data-stu-id="1b035-185">**Applicability rules** – Applicability rules let you configure the context that Electronic invoicing must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="1b035-186">**变量** – 变量让您可以配置对构造配置逻辑的支持。</span><span class="sxs-lookup"><span data-stu-id="1b035-186">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="1b035-187">变量可以用作执行特定操作的值的输入。</span><span class="sxs-lookup"><span data-stu-id="1b035-187">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="1b035-188">或者，还可以用作 Finance 和 Supply Chain Management 与电子开票之间的值的交换。</span><span class="sxs-lookup"><span data-stu-id="1b035-188">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and Electronic invoicing.</span></span>
- <span data-ttu-id="1b035-189">**电子单据模型映射** – 电子单据模型映射可让您配置 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="1b035-189">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="1b035-190">此模型映射定义提交电子单据时集成到电子开票中的摘要发票的数据映射。</span><span class="sxs-lookup"><span data-stu-id="1b035-190">The model mapping defines the data mapping of the abstract invoice that is integrated into Electronic invoicing when electronic documents are submitted.</span></span>
- <span data-ttu-id="1b035-191">**发票上下文模型** – 发票上下文模型让您可以配置 ER 发票上下文模型并定义电子开票功能的上下文。</span><span class="sxs-lookup"><span data-stu-id="1b035-191">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="1b035-192">**响应类型** – 响应类型让您可以配置由于进行电子发票处理，电子开票必须在 Finance 和 Supply Chain Management 中更新的内容。</span><span class="sxs-lookup"><span data-stu-id="1b035-192">**Response types** – Response types let you configure what Electronic invoicing must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="1b035-193">格式</span><span class="sxs-lookup"><span data-stu-id="1b035-193">Formats</span></span>

<span data-ttu-id="1b035-194">以下列表显示了可用于电子开票功能的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-194">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="1b035-195">奥地利 (AT) 电子发票：奥地利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-195">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="1b035-196">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="1b035-196">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="1b035-197">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-197">OIOUBL Project invoice</span></span>
- <span data-ttu-id="1b035-198">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-198">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="1b035-199">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-199">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="1b035-200">比利时 (BE) 电子发票：比利时的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-200">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="1b035-201">UBL 销售发票 BE</span><span class="sxs-lookup"><span data-stu-id="1b035-201">UBL Sales invoice BE</span></span>
- <span data-ttu-id="1b035-202">UBL 项目发票 BE</span><span class="sxs-lookup"><span data-stu-id="1b035-202">UBL Project invoice BE</span></span>
- <span data-ttu-id="1b035-203">UBL 项目贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="1b035-203">UBL Project credit note BE</span></span>
- <span data-ttu-id="1b035-204">UBL 销售贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="1b035-204">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="1b035-205">巴西 (BR) NF-e：NF-e 联邦（巴西）</span><span class="sxs-lookup"><span data-stu-id="1b035-205">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="1b035-206">NF-e 提交导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-206">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="1b035-207">NF-e 更正单导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-207">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="1b035-208">NF-e 取消导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-208">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="1b035-209">NF-e 弃用导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-209">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="1b035-210">巴西 NFS-e (BR)：NFS-e ABRASF 库里蒂巴市</span><span class="sxs-lookup"><span data-stu-id="1b035-210">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="1b035-211">NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-211">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="1b035-212">NFS-e ABRASF 查询库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="1b035-212">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="1b035-213">丹麦 (DK) 电子发票：丹麦的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-213">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="1b035-214">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="1b035-214">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="1b035-215">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-215">OIOUBL Project invoice</span></span>
- <span data-ttu-id="1b035-216">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-216">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="1b035-217">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-217">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="1b035-218">荷兰 (NL) 电子发票：荷兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-218">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="1b035-219">UBL 销售发票 NL</span><span class="sxs-lookup"><span data-stu-id="1b035-219">UBL Sales invoice NL</span></span>
- <span data-ttu-id="1b035-220">UBL 项目发票 NL</span><span class="sxs-lookup"><span data-stu-id="1b035-220">UBL Project invoice NL</span></span>
- <span data-ttu-id="1b035-221">UBL 项目贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="1b035-221">UBL Project credit note NL</span></span>
- <span data-ttu-id="1b035-222">UBL 销售贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="1b035-222">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="1b035-223">埃及 (EG) 电子发票：埃及的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-223">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="1b035-224">销售发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="1b035-224">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="1b035-225">项目发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="1b035-225">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="1b035-226">爱沙尼亚 (EE) 电子发票：爱沙尼亚的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-226">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="1b035-227">销售发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="1b035-227">Sales invoice (EE)</span></span>
- <span data-ttu-id="1b035-228">项目发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="1b035-228">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="1b035-229">芬兰 (FI) 电子发票：芬兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-229">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="1b035-230">销售发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="1b035-230">Sales invoice (FI)</span></span>
- <span data-ttu-id="1b035-231">项目发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="1b035-231">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="1b035-232">法国 (FR) 电子发票：法国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-232">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="1b035-233">UBL 销售发票 FR</span><span class="sxs-lookup"><span data-stu-id="1b035-233">UBL Sales invoice FR</span></span>
- <span data-ttu-id="1b035-234">UBL 项目发票 FR</span><span class="sxs-lookup"><span data-stu-id="1b035-234">UBL Project invoice FR</span></span>
- <span data-ttu-id="1b035-235">UBL 项目贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="1b035-235">UBL Project credit note FR</span></span>
- <span data-ttu-id="1b035-236">UBL 销售贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="1b035-236">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="1b035-237">德国 (DE) 电子发票：德国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-237">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="1b035-238">销售发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="1b035-238">Sales invoice (DE)</span></span>
- <span data-ttu-id="1b035-239">项目发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="1b035-239">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="1b035-240">意大利 (IT) 电子发票：意大利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-240">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="1b035-241">销售发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="1b035-241">Sales invoice (IT)</span></span>
- <span data-ttu-id="1b035-242">项目发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="1b035-242">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="1b035-243">墨西哥 (MX) CFDI：墨西哥的 CFDI</span><span class="sxs-lookup"><span data-stu-id="1b035-243">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="1b035-244">CFDI 发票格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-244">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="1b035-245">CFDI 装箱单 (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-245">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="1b035-246">CFDI 库存转移 (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-246">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="1b035-247">CFDI 付款格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-247">CFDI payment format (MX)</span></span>
- <span data-ttu-id="1b035-248">CFDI 发票取消格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="1b035-248">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="1b035-249">挪威 (NO) 电子发票：挪威的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-249">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="1b035-250">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="1b035-250">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="1b035-251">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-251">OIOUBL Project invoice</span></span>
- <span data-ttu-id="1b035-252">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-252">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="1b035-253">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-253">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="1b035-254">PEPPOL 电子发票：PEPPOL 销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-254">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="1b035-255">PEPPOL 销售发票</span><span class="sxs-lookup"><span data-stu-id="1b035-255">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="1b035-256">PEPPOL 项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-256">PEPPOL Project invoice</span></span>
- <span data-ttu-id="1b035-257">PEPPOL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-257">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="1b035-258">PEPPOL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="1b035-258">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="1b035-259">西班牙 (ES) 电子发票：西班牙的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="1b035-259">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="1b035-260">销售发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="1b035-260">Sales invoice (ES)</span></span>
- <span data-ttu-id="1b035-261">项目发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="1b035-261">Project invoice (ES)</span></span>

<span data-ttu-id="1b035-262">除了现成的可用于电子开票服务的电子报告格式配置外，您还可以创建自己的电子报告格式配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-262">In addition to the ER format configurations that are available out of the box to use with the Electronic Invoicing service, you can also create your own ER format configurations.</span></span> <span data-ttu-id="1b035-263">但是，为与电子开票功能一起使用创建的格式配置不支持直接引用 Finance 或 Supply Chain Management 或任何相应的元数据。</span><span class="sxs-lookup"><span data-stu-id="1b035-263">However, the format configurations that are created to use with Electronic Invoicing features don't support direct reference to Finance or Supply Chain Management tables or any of the corresponding metadata.</span></span> <span data-ttu-id="1b035-264">仅支持对电子报告模型映射的引用。</span><span class="sxs-lookup"><span data-stu-id="1b035-264">Only references to the ER model mapping are supported.</span></span>

### <a name="actions"></a><span data-ttu-id="1b035-265">变动</span><span class="sxs-lookup"><span data-stu-id="1b035-265">Actions</span></span>

<span data-ttu-id="1b035-266">下表列出了可用操作，以及这些操作当前是正式发布还是仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="1b035-266">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="1b035-267">行为</span><span class="sxs-lookup"><span data-stu-id="1b035-267">Action</span></span>                                        | <span data-ttu-id="1b035-268">说明</span><span class="sxs-lookup"><span data-stu-id="1b035-268">Description</span></span>                                                                  | <span data-ttu-id="1b035-269">可用性</span><span class="sxs-lookup"><span data-stu-id="1b035-269">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="1b035-270">转换文档</span><span class="sxs-lookup"><span data-stu-id="1b035-270">Transform document</span></span>                            | <span data-ttu-id="1b035-271">运行电子报告格式来转换文档。</span><span class="sxs-lookup"><span data-stu-id="1b035-271">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="1b035-272">正式发布</span><span class="sxs-lookup"><span data-stu-id="1b035-272">Generally available</span></span>  |
| <span data-ttu-id="1b035-273">对 xml 文档签名</span><span class="sxs-lookup"><span data-stu-id="1b035-273">Sign xml document</span></span>                             | <span data-ttu-id="1b035-274">使用数字签名对 xml 文档进行签名。</span><span class="sxs-lookup"><span data-stu-id="1b035-274">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="1b035-275">预览模式</span><span class="sxs-lookup"><span data-stu-id="1b035-275">In preview</span></span>           |
| <span data-ttu-id="1b035-276">对埃及税务主管机构的 json 文档签名</span><span class="sxs-lookup"><span data-stu-id="1b035-276">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="1b035-277">使用数字签名对埃及税务主管机构的 json 文档签名。</span><span class="sxs-lookup"><span data-stu-id="1b035-277">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="1b035-278">正式发布</span><span class="sxs-lookup"><span data-stu-id="1b035-278">Generally available</span></span>  |
| <span data-ttu-id="1b035-279">与埃及 ETA 服务集成</span><span class="sxs-lookup"><span data-stu-id="1b035-279">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="1b035-280">与埃及税务主管机构通信。</span><span class="sxs-lookup"><span data-stu-id="1b035-280">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="1b035-281">正式发布</span><span class="sxs-lookup"><span data-stu-id="1b035-281">Generally available</span></span>  |
| <span data-ttu-id="1b035-282">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="1b035-282">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="1b035-283">与巴西 SEFAZ 服务集成以提交会计单据。</span><span class="sxs-lookup"><span data-stu-id="1b035-283">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="1b035-284">预览模式</span><span class="sxs-lookup"><span data-stu-id="1b035-284">In preview</span></span>           |
| <span data-ttu-id="1b035-285">调用墨西哥 PAC 服务</span><span class="sxs-lookup"><span data-stu-id="1b035-285">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="1b035-286">与墨西哥 PAC 服务集成以提交 CFDI。</span><span class="sxs-lookup"><span data-stu-id="1b035-286">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="1b035-287">预览模式</span><span class="sxs-lookup"><span data-stu-id="1b035-287">In preview</span></span>           |
| <span data-ttu-id="1b035-288">处理响应</span><span class="sxs-lookup"><span data-stu-id="1b035-288">Process response</span></span>                              | <span data-ttu-id="1b035-289">分析从 Web 服务调用收到的响应。</span><span class="sxs-lookup"><span data-stu-id="1b035-289">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="1b035-290">正式发布</span><span class="sxs-lookup"><span data-stu-id="1b035-290">Generally available</span></span>  |
| <span data-ttu-id="1b035-291">使用 MS Power Automate</span><span class="sxs-lookup"><span data-stu-id="1b035-291">Use MS Power Automate</span></span>                         | <span data-ttu-id="1b035-292">与 Microsoft Power Automate 内置流集成。</span><span class="sxs-lookup"><span data-stu-id="1b035-292">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="1b035-293">预览模式</span><span class="sxs-lookup"><span data-stu-id="1b035-293">In preview</span></span>           |

### <a name="applicability-rules"></a><span data-ttu-id="1b035-294">适用性规则</span><span class="sxs-lookup"><span data-stu-id="1b035-294">Applicability rules</span></span>

<span data-ttu-id="1b035-295">适用性规则是在电子开票功能级别定义的可配置子句。</span><span class="sxs-lookup"><span data-stu-id="1b035-295">Applicability rules are configurable clauses that are defined at the Electronic invoicing feature level.</span></span> <span data-ttu-id="1b035-296">规则配置为通过电子开票功能集提供用于执行电子开票功能的上下文。</span><span class="sxs-lookup"><span data-stu-id="1b035-296">The rules are configured to provide a context for execution of electronic invoicing features through the Electronic Invoicing capability set.</span></span>

<span data-ttu-id="1b035-297">当 Finance 或 Supply Chain Management 中的业务文档提交到电子开票时，该业务文档不带有允许电子开票功能集调用特定电子开票功能处理提交的显式引用。</span><span class="sxs-lookup"><span data-stu-id="1b035-297">When a business document from Finance or Supply Chain Management is submitted to electronic invoicing, the business document doesn't carry an explicit reference that allows the Electronic Invoicing capability set to call a particular electronic invoicing feature to process the submission.</span></span>

<span data-ttu-id="1b035-298">但是，如果配置正确，业务文档将包含允许电子开票解决必须选择哪个电子开票功能，然后生成电子发票的必要元素。</span><span class="sxs-lookup"><span data-stu-id="1b035-298">Nevertheless, when properly configured, the business document contains the necessary elements that allow electronic invoicing to resolve which electronic invoicing feature must be selected and then generate the electronic invoice.</span></span>

<span data-ttu-id="1b035-299">适用性规则允许电子开票功能集找到必须用于处理提交的确切电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-299">Applicability rules allow the Electronic Invoicing capability set to find the exact electronic invoicing features that must be used to process the submission.</span></span> <span data-ttu-id="1b035-300">通过将提交的业务文档中的内容与适用性规则中的子句进行匹配来完成此操作。</span><span class="sxs-lookup"><span data-stu-id="1b035-300">This is done by matching the contents from the submitted business document with the clauses from the Applicability rules.</span></span>

<span data-ttu-id="1b035-301">例如，将具有相关适用性规则的两个电子开票功能部署到电子开票功能集中。</span><span class="sxs-lookup"><span data-stu-id="1b035-301">For example, two electronic invoicing features with related Applicability rules are deployed into the Electronic Invoicing capability set.</span></span>

| <span data-ttu-id="1b035-302">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-302">Electronic invoicing feature</span></span> | <span data-ttu-id="1b035-303">适用性规则</span><span class="sxs-lookup"><span data-stu-id="1b035-303">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="1b035-304">A</span><span class="sxs-lookup"><span data-stu-id="1b035-304">A</span></span>                            | <p><span data-ttu-id="1b035-305">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-305">Country = BR</span></span></p><p><span data-ttu-id="1b035-306">与</span><span class="sxs-lookup"><span data-stu-id="1b035-306">and</span></span></p><p><span data-ttu-id="1b035-307">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-307">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="1b035-308">B</span><span class="sxs-lookup"><span data-stu-id="1b035-308">B</span></span>                            | <p><span data-ttu-id="1b035-309">国家/地区 = MX</span><span class="sxs-lookup"><span data-stu-id="1b035-309">Country = MX</span></span></p><p><span data-ttu-id="1b035-310">与</span><span class="sxs-lookup"><span data-stu-id="1b035-310">and</span></span></p><p><span data-ttu-id="1b035-311">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="1b035-311">Legal entity = MXMF</span></span></p>  |

<span data-ttu-id="1b035-312">如果 Finance 或 Supply Chain Management 中的业务文档提交到电子开票功能集，业务文档将包含以下属性，并填充为：</span><span class="sxs-lookup"><span data-stu-id="1b035-312">If a business document from Finance or Supply Chain Management is submitted to the Electronic Invoicing capability set, the business document contains the following attributes filled as:</span></span>

- <span data-ttu-id="1b035-313">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-313">Country = BR</span></span>
- <span data-ttu-id="1b035-314">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-314">Legal entity = BRMF</span></span>

<span data-ttu-id="1b035-315">电子开票功能集将选择电子开票功能 **A** 处理提交并生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="1b035-315">The Electronic Invoicing capability set will select the electronic invoicing feature **A** to process the submission and generate the electronic invoice.</span></span>

<span data-ttu-id="1b035-316">同样，如果业务文档包含：</span><span class="sxs-lookup"><span data-stu-id="1b035-316">In the same way, if the business document contains:</span></span>

- <span data-ttu-id="1b035-317">国家/地区 = MX</span><span class="sxs-lookup"><span data-stu-id="1b035-317">Country = MX</span></span>
- <span data-ttu-id="1b035-318">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="1b035-318">Legal entity = MXMF</span></span>

<span data-ttu-id="1b035-319">选择电子开票功能 **B** 以生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="1b035-319">Electronic invoicing feature **B** is selected to generate the electronic invoice.</span></span>

<span data-ttu-id="1b035-320">适用性规则的配置必须明确。</span><span class="sxs-lookup"><span data-stu-id="1b035-320">The configuration of Applicability rules can't be ambiguous.</span></span> <span data-ttu-id="1b035-321">这意味着两个或多个电子开票功能不能具有相同的子句，否则将导致无法选择。</span><span class="sxs-lookup"><span data-stu-id="1b035-321">This means that two or more electronic invoicing features can't have the same clauses, otherwise it will lead to no selection.</span></span> <span data-ttu-id="1b035-322">如果电子开票功能重复，为避免歧义，请使用其他子句以使电子开票功能集能够区分这两个电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-322">If there is a duplication of electronic invoicing features, to avoid ambiguity, use additional clauses to allow the Electronic Invoicing capability set to distinguish between the two electronic invoicing features.</span></span>

<span data-ttu-id="1b035-323">例如，考虑电子开票功能 **C**。此功能是电子开票功能 **A** 的副本。</span><span class="sxs-lookup"><span data-stu-id="1b035-323">For example, consider electronic invoicing feature **C**. This feature is a copy of electronic invoicing feature **A**.</span></span>

| <span data-ttu-id="1b035-324">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-324">Electronic invoicing feature</span></span> | <span data-ttu-id="1b035-325">适用性规则</span><span class="sxs-lookup"><span data-stu-id="1b035-325">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="1b035-326">A</span><span class="sxs-lookup"><span data-stu-id="1b035-326">A</span></span>                            | <p><span data-ttu-id="1b035-327">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-327">Country = BR</span></span></p><p><span data-ttu-id="1b035-328">与</span><span class="sxs-lookup"><span data-stu-id="1b035-328">and</span></span></p><p><span data-ttu-id="1b035-329">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-329">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="1b035-330">C</span><span class="sxs-lookup"><span data-stu-id="1b035-330">C</span></span>                            | <p><span data-ttu-id="1b035-331">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-331">Country = BR</span></span></p><p><span data-ttu-id="1b035-332">与</span><span class="sxs-lookup"><span data-stu-id="1b035-332">and</span></span></p><p><span data-ttu-id="1b035-333">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-333">Legal entity = BRMF</span></span></p>  |

<span data-ttu-id="1b035-334">在此示例中，功能 **C** 在包含以下内容的业务文档提交之前：</span><span class="sxs-lookup"><span data-stu-id="1b035-334">In this example, feature **C** is in front of a business document submission that contains the following:</span></span>

- <span data-ttu-id="1b035-335">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-335">Country = BR</span></span>
- <span data-ttu-id="1b035-336">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-336">Legal entity = BRMF</span></span>

<span data-ttu-id="1b035-337">电子开票功能无法区分必须用于处理提交的电子开票功能，因为提交包含完全相同的子句。</span><span class="sxs-lookup"><span data-stu-id="1b035-337">The Electronic Invoicing capability can't distinguish which electronic invoicing feature must be used to process the submission because the submissions contain the exact same clauses.</span></span>

<span data-ttu-id="1b035-338">若要通过适用性规则在两个功能之间进行区分，必须在其中一个功能中添加新子句，以允许电子开票功能集选择适当的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-338">To create a distinction between the two features through Applicability rules, a new clause must be added to one of the features to allow the Electronic Invoicing capability set to select the proper electronic invoicing feature.</span></span>

| <span data-ttu-id="1b035-339">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-339">Electronic invoicing feature</span></span> | <span data-ttu-id="1b035-340">适用性规则</span><span class="sxs-lookup"><span data-stu-id="1b035-340">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="1b035-341">A</span><span class="sxs-lookup"><span data-stu-id="1b035-341">A</span></span>                            | <p><span data-ttu-id="1b035-342">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-342">Country = BR</span></span></p><p><span data-ttu-id="1b035-343">与</span><span class="sxs-lookup"><span data-stu-id="1b035-343">and</span></span></p><p><span data-ttu-id="1b035-344">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-344">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="1b035-345">C</span><span class="sxs-lookup"><span data-stu-id="1b035-345">C</span></span>                            | <p><span data-ttu-id="1b035-346">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-346">Country = BR</span></span></p><p><span data-ttu-id="1b035-347">与</span><span class="sxs-lookup"><span data-stu-id="1b035-347">and</span></span></p><p><span data-ttu-id="1b035-348">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-348">Legal entity = BRMF</span></span></p><p><span data-ttu-id="1b035-349">与</span><span class="sxs-lookup"><span data-stu-id="1b035-349">and</span></span></p><p><span data-ttu-id="1b035-350">模型 = 55</span><span class="sxs-lookup"><span data-stu-id="1b035-350">Model=55</span></span></p>  |

<span data-ttu-id="1b035-351">若要支持创建更复杂的子句，可以使用以下资源：</span><span class="sxs-lookup"><span data-stu-id="1b035-351">To support creating more complex clauses, the following resources are available:</span></span>

<span data-ttu-id="1b035-352">逻辑运算符：</span><span class="sxs-lookup"><span data-stu-id="1b035-352">Logic operators:</span></span>
- <span data-ttu-id="1b035-353">并</span><span class="sxs-lookup"><span data-stu-id="1b035-353">And</span></span>
- <span data-ttu-id="1b035-354">或</span><span class="sxs-lookup"><span data-stu-id="1b035-354">Or</span></span>

<span data-ttu-id="1b035-355">运算符类型：</span><span class="sxs-lookup"><span data-stu-id="1b035-355">Operators types:</span></span>
- <span data-ttu-id="1b035-356">Equal</span><span class="sxs-lookup"><span data-stu-id="1b035-356">Equal</span></span>
- <span data-ttu-id="1b035-357">Not equal</span><span class="sxs-lookup"><span data-stu-id="1b035-357">Not equal</span></span>
- <span data-ttu-id="1b035-358">Greater than</span><span class="sxs-lookup"><span data-stu-id="1b035-358">Greater than</span></span>
- <span data-ttu-id="1b035-359">Less than</span><span class="sxs-lookup"><span data-stu-id="1b035-359">Less than</span></span>
- <span data-ttu-id="1b035-360">大于等于</span><span class="sxs-lookup"><span data-stu-id="1b035-360">Greater than or equal to</span></span>
- <span data-ttu-id="1b035-361">小于等于</span><span class="sxs-lookup"><span data-stu-id="1b035-361">Less than or equal to</span></span>
- <span data-ttu-id="1b035-362">Contains</span><span class="sxs-lookup"><span data-stu-id="1b035-362">Contains</span></span>
- <span data-ttu-id="1b035-363">开头是</span><span class="sxs-lookup"><span data-stu-id="1b035-363">Begins with</span></span>

<span data-ttu-id="1b035-364">数据类型：</span><span class="sxs-lookup"><span data-stu-id="1b035-364">Data types:</span></span>
- <span data-ttu-id="1b035-365">字符串</span><span class="sxs-lookup"><span data-stu-id="1b035-365">String</span></span>
- <span data-ttu-id="1b035-366">数值</span><span class="sxs-lookup"><span data-stu-id="1b035-366">Number</span></span>
- <span data-ttu-id="1b035-367">布尔</span><span class="sxs-lookup"><span data-stu-id="1b035-367">Boolean</span></span>
- <span data-ttu-id="1b035-368">日期</span><span class="sxs-lookup"><span data-stu-id="1b035-368">Date</span></span>
- <span data-ttu-id="1b035-369">UUID</span><span class="sxs-lookup"><span data-stu-id="1b035-369">UUID</span></span>

<span data-ttu-id="1b035-370">分组和取消分组子句的功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-370">Capability to group and ungroup clauses.</span></span>
<span data-ttu-id="1b035-371">示例如下所示。</span><span class="sxs-lookup"><span data-stu-id="1b035-371">The example looks like this.</span></span>

| <span data-ttu-id="1b035-372">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-372">Electronic invoicing feature</span></span> | <span data-ttu-id="1b035-373">适用性规则</span><span class="sxs-lookup"><span data-stu-id="1b035-373">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="1b035-374">C</span><span class="sxs-lookup"><span data-stu-id="1b035-374">C</span></span>                            | <p><span data-ttu-id="1b035-375">国家/地区 = BR</span><span class="sxs-lookup"><span data-stu-id="1b035-375">Country = BR</span></span></p><p><span data-ttu-id="1b035-376">与</span><span class="sxs-lookup"><span data-stu-id="1b035-376">and</span></span></p><p><span data-ttu-id="1b035-377">（法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="1b035-377">( Legal entity = BRMF</span></span></p><p><span data-ttu-id="1b035-378">或</span><span class="sxs-lookup"><span data-stu-id="1b035-378">or</span></span></p><p><span data-ttu-id="1b035-379">模型 = 55）</span><span class="sxs-lookup"><span data-stu-id="1b035-379">Model=55)</span></span></p>  |


## <a name="configuration-providers"></a><span data-ttu-id="1b035-380">配置提供方</span><span class="sxs-lookup"><span data-stu-id="1b035-380">Configuration providers</span></span>

<span data-ttu-id="1b035-381">配置提供者提供电子开票功能及其 ER 组件，如模型映射、格式配置和上下文模型。</span><span class="sxs-lookup"><span data-stu-id="1b035-381">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="1b035-382">他们在关联的全局存储库中发布电子开票功能和 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="1b035-382">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="1b035-383">从那里，其他组织可以下载这些功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-383">From there, other organizations can download them.</span></span>

<span data-ttu-id="1b035-384">在通过 RCS 配置电子开票功能之前，您必须在 **电子报告** 模块中将自己的组织配置为配置提供者。</span><span class="sxs-lookup"><span data-stu-id="1b035-384">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="1b035-385">有关如何将配置提供者设置为 **活动** 的信息，请参阅[创建配置提供者并将其标记为活动](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="1b035-385">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="1b035-386">查看全局存储库中的电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-386">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="1b035-387">要浏览特定配置提供者的全局存储库中可用的电子开票功能，请同步组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="1b035-387">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="1b035-388">完成同步后，可用电子开票功能的列表将更新。</span><span class="sxs-lookup"><span data-stu-id="1b035-388">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="1b035-389">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-389">Importing electronic invoicing features</span></span>

<span data-ttu-id="1b035-390">在使用或配置电子开票功能之前，必须将它们导入组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="1b035-390">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="1b035-391">导入操作将创建功能的本地副本，并将功能使用的所有 ER 项目（例如，格式配置和模型配置）复制到组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="1b035-391">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="1b035-392">您可以从任何配置提供者导入电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-392">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="1b035-393">创建电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-393">Creating electronic invoicing features</span></span>

<span data-ttu-id="1b035-394">您可以从头创建电子开票功能，也可以从另一个电子开票功能派生。</span><span class="sxs-lookup"><span data-stu-id="1b035-394">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="1b035-395">从头创建电子开票功能时，必须手动添加 ER 组件（例如，功能版本配置和其他配置，如功能版本设置和应用程序设置）。</span><span class="sxs-lookup"><span data-stu-id="1b035-395">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="1b035-396">通过从另一个功能派生来创建功能时，新功能将继承原始功能的所有配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-396">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="1b035-397">电子开票功能版本</span><span class="sxs-lookup"><span data-stu-id="1b035-397">Electronic invoicing feature version</span></span>

<span data-ttu-id="1b035-398">电子开票功能已版本化。</span><span class="sxs-lookup"><span data-stu-id="1b035-398">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="1b035-399">新版本创建时，版本号会自动递增。</span><span class="sxs-lookup"><span data-stu-id="1b035-399">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="1b035-400">可以为新版本定义“生效开始”日期。</span><span class="sxs-lookup"><span data-stu-id="1b035-400">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="1b035-401">电子开票功能版本采用的生命周期最多包含以下三种状态：</span><span class="sxs-lookup"><span data-stu-id="1b035-401">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="1b035-402">**草稿** – 如果功能版本处于此状态，您可以编辑其配置属性及其任何项目（例如，文件格式配置）。</span><span class="sxs-lookup"><span data-stu-id="1b035-402">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="1b035-403">**完成** – 如果功能版本处于此状态，说明该功能版本已发布到与您的组织关联的全局存储库中。</span><span class="sxs-lookup"><span data-stu-id="1b035-403">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="1b035-404">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="1b035-404">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="1b035-405">**已发布** – 如果功能版本处于此状态，说明该功能版本已发布到电子开票。</span><span class="sxs-lookup"><span data-stu-id="1b035-405">**Published** – If a feature version is in this status, it has been published to Electronic invoicing.</span></span> <span data-ttu-id="1b035-406">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="1b035-406">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="1b035-407">功能配置</span><span class="sxs-lookup"><span data-stu-id="1b035-407">Feature configurations</span></span>

<span data-ttu-id="1b035-408">功能配置保留电子开票功能使用的所有 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-408">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="1b035-409">电子开票功能在处理期间使用的所有电子文件都来自已添加到该功能的功能配置中的格式配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-409">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="1b035-410">从功能配置，您可以访问 ER 格式设计器，这是用于创建格式配置的 ER 工具。</span><span class="sxs-lookup"><span data-stu-id="1b035-410">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="1b035-411">功能设置</span><span class="sxs-lookup"><span data-stu-id="1b035-411">Feature setup</span></span>

<span data-ttu-id="1b035-412">功能设置与功能配置结合使用。</span><span class="sxs-lookup"><span data-stu-id="1b035-412">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="1b035-413">每个功能设置都封装了一组提供预期行为的操作、适用性规则和变量，让电子开票功能可以满足电子发票的特定要求。</span><span class="sxs-lookup"><span data-stu-id="1b035-413">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="1b035-414">应用程序设置</span><span class="sxs-lookup"><span data-stu-id="1b035-414">Application setup</span></span>

<span data-ttu-id="1b035-415">应用程序设置必须与先前创建的已连接应用程序关联。</span><span class="sxs-lookup"><span data-stu-id="1b035-415">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="1b035-416">通过应用程序设置，您可以配置必须在 Finance 和 Supply Chain Management 中进行的电子开票功能的那一部分。</span><span class="sxs-lookup"><span data-stu-id="1b035-416">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="1b035-417">不论是什么电子开票功能，都至少必须有三个可配置组件：</span><span class="sxs-lookup"><span data-stu-id="1b035-417">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="1b035-418">**表名称** – Finance 和 Supply Chain Management 中的实体，保留过帐的发票，电子开票功能基于此实体。</span><span class="sxs-lookup"><span data-stu-id="1b035-418">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="1b035-419">**上下文** – 通过 ER 配置的发票上下文模型的名称。</span><span class="sxs-lookup"><span data-stu-id="1b035-419">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="1b035-420">**业务文档映射** – 通过 ER 配置的发票映射模型的名称。</span><span class="sxs-lookup"><span data-stu-id="1b035-420">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b035-421">可以在 Finance 和 Supply Chain Management 中查看在应用程序设置中输入的配置。</span><span class="sxs-lookup"><span data-stu-id="1b035-421">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="1b035-422">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="1b035-422">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="1b035-423">在 **电子单据** 选项卡上，选择 **部署**，然后选择 **相连应用程序** 选项。</span><span class="sxs-lookup"><span data-stu-id="1b035-423">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="1b035-424">部署功能版本</span><span class="sxs-lookup"><span data-stu-id="1b035-424">Deploying feature versions</span></span>

<span data-ttu-id="1b035-425">在 RCS 中，您使用 **部署** 命令定向发布电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="1b035-425">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="1b035-426">选择 **部署**，然后选择以下选项之一定义部署目标：</span><span class="sxs-lookup"><span data-stu-id="1b035-426">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="1b035-427">**服务环境** – 当部署的目标是服务环境时，电子开票功能版本将发布到服务环境。</span><span class="sxs-lookup"><span data-stu-id="1b035-427">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="1b035-428">然后，电子开票就可以接收和处理 Finance 和 Supply Chain Management 发送的电子单据。</span><span class="sxs-lookup"><span data-stu-id="1b035-428">Electronic invoicing is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="1b035-429">**相连应用程序** – 当部署的目标是相连应用程序时，由应用程序安装程序提供的配置将写入先前与之关联的 Finance 和 Supply Chain Management 实例中。</span><span class="sxs-lookup"><span data-stu-id="1b035-429">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="1b035-430">仅状态为 **已完成** 的电子开票功能版本可以部署到服务环境或连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1b035-430">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="1b035-431">删除功能版本</span><span class="sxs-lookup"><span data-stu-id="1b035-431">Removing feature versions</span></span>

<span data-ttu-id="1b035-432">在 RCS 中，您使用 **取消部署** 命令从电子开票中的服务环境中删除特定的电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="1b035-432">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in Electronic invoicing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b035-433">**取消部署** 命令仅在服务环境中有效。</span><span class="sxs-lookup"><span data-stu-id="1b035-433">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="1b035-434">它不会从连接的应用程序中删除电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="1b035-434">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="1b035-435">重定电子开票功能</span><span class="sxs-lookup"><span data-stu-id="1b035-435">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="1b035-436">当一个电子开票功能是从另一个电子开票功能派生而来时，**重定** 命令使用原始功能中引入的更改来更新派生功能。</span><span class="sxs-lookup"><span data-stu-id="1b035-436">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b035-437">其他资源</span><span class="sxs-lookup"><span data-stu-id="1b035-437">Additional resources</span></span>

- [<span data-ttu-id="1b035-438">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="1b035-438">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
