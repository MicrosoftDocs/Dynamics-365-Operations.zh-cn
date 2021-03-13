---
title: 在 Regulatory Configuration Services (RCS) 中配置电子开票附加产品
description: 本主题说明如何在 Dynamics 365 Regulatory Configuration Services (RCS) 中配置电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104351"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="002e6-103">在 Regulatory Configuration Services (RCS) 中配置电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="002e6-103">Configure the Electronic invoicing add-on in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

<span data-ttu-id="002e6-104">本主题提供有关 Dynamics 365 Regulatory Configuration Services (RCS) 中电子开票附加产品的配置功能的信息。</span><span class="sxs-lookup"><span data-stu-id="002e6-104">This topic provides information about the configuration capabilities of the Electronic invoicing add-on in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="002e6-105">通过配置功能，电子开票附加产品可帮助您满足电子发票的业务和法规要求，而无需进行任何编码。</span><span class="sxs-lookup"><span data-stu-id="002e6-105">It is through the configuration capabilities that Electronic invoicing add-on helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="002e6-106">而且，在电子发票必须由 Web 服务以电子方式审核的情况下，配置功能还可以帮助您满足与 Web 服务交换消息的要求，无需编写任何代码。</span><span class="sxs-lookup"><span data-stu-id="002e6-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="002e6-107">电子报告</span><span class="sxs-lookup"><span data-stu-id="002e6-107">Electronic reporting</span></span>

<span data-ttu-id="002e6-108">电子报告 (ER) 支持电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="002e6-108">Electronic reporting (ER) supports the Electronic invoicing add-on.</span></span>

<span data-ttu-id="002e6-109">数据模型映射和格式是可配置的组件，可通过 ER 创建和维护，在电子开票附加产品中使用。</span><span class="sxs-lookup"><span data-stu-id="002e6-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in the Electronic invoicing add-on.</span></span> <span data-ttu-id="002e6-110">ER 格式设计器是用于创建和维护文件格式的工具。</span><span class="sxs-lookup"><span data-stu-id="002e6-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="002e6-111">用于配置电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="002e6-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="002e6-112">有关详细信息，请参阅[电子报告 (ER) 概述](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="002e6-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="002e6-113">电子开票功能</span><span class="sxs-lookup"><span data-stu-id="002e6-113">Electronic invoicing features</span></span>

<span data-ttu-id="002e6-114">电子开票功能负责通过电子开票附加产品生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="002e6-114">The electronic invoicing features are responsible for generating electronic invoices through the Electronic invoicing add-on.</span></span> <span data-ttu-id="002e6-115">它们封装了配置规则，使用它们来处理 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 发送到电子开票附加产品和电子发票的数据。</span><span class="sxs-lookup"><span data-stu-id="002e6-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to the Electronic invoicing add-on and to electronic invoices.</span></span>

<span data-ttu-id="002e6-116">这些功能还支持需要符合文件格式规范且输出是独立电子文件的场景。</span><span class="sxs-lookup"><span data-stu-id="002e6-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="002e6-117">在大多数情况下，文件格式规范由税务主管机构发布。</span><span class="sxs-lookup"><span data-stu-id="002e6-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="002e6-118">最后，这些功能还支持与税务主管机构或某些认可方托管的外部 Web 服务交换消息，并支持请求授权或在电子发票中增加审核戳记。</span><span class="sxs-lookup"><span data-stu-id="002e6-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="002e6-119">电子开票功能的可用性</span><span class="sxs-lookup"><span data-stu-id="002e6-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="002e6-120">电子开票功能的可用性取决于国家或地区。</span><span class="sxs-lookup"><span data-stu-id="002e6-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="002e6-121">虽然有些功能已正式发布，但其他功能仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="002e6-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="preview-features"></a><span data-ttu-id="002e6-122">预览功能</span><span class="sxs-lookup"><span data-stu-id="002e6-122">Preview features</span></span>

<span data-ttu-id="002e6-123">下表显示了当前处于预览阶段的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="002e6-123">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="002e6-124">国家/地区</span><span class="sxs-lookup"><span data-stu-id="002e6-124">Country/region</span></span> | <span data-ttu-id="002e6-125">功能名称</span><span class="sxs-lookup"><span data-stu-id="002e6-125">Feature name</span></span>                         | <span data-ttu-id="002e6-126">业务文档</span><span class="sxs-lookup"><span data-stu-id="002e6-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="002e6-127">奥地利</span><span class="sxs-lookup"><span data-stu-id="002e6-127">Austria</span></span>        | <span data-ttu-id="002e6-128">奥地利电子发票 (AT)</span><span class="sxs-lookup"><span data-stu-id="002e6-128">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="002e6-129">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-129">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-130">比利时</span><span class="sxs-lookup"><span data-stu-id="002e6-130">Belgium</span></span>        | <span data-ttu-id="002e6-131">比利时电子发票 (BE)</span><span class="sxs-lookup"><span data-stu-id="002e6-131">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="002e6-132">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-132">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-133">巴西</span><span class="sxs-lookup"><span data-stu-id="002e6-133">Brazil</span></span>         | <span data-ttu-id="002e6-134">巴西 NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-134">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="002e6-135">会计单据模型 55，更正单、取消和弃用</span><span class="sxs-lookup"><span data-stu-id="002e6-135">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="002e6-136">巴西</span><span class="sxs-lookup"><span data-stu-id="002e6-136">Brazil</span></span>         | <span data-ttu-id="002e6-137">巴西 NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-137">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="002e6-138">服务会计单据</span><span class="sxs-lookup"><span data-stu-id="002e6-138">Service fiscal documents</span></span> |
| <span data-ttu-id="002e6-139">巴西</span><span class="sxs-lookup"><span data-stu-id="002e6-139">Brazil</span></span>         | <span data-ttu-id="002e6-140">巴西 NFS-e 圣保罗 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-140">Brazilian NFS-e São Paulo (BR)</span></span>       | <span data-ttu-id="002e6-141">服务会计单据</span><span class="sxs-lookup"><span data-stu-id="002e6-141">Service fiscal documents</span></span> |
| <span data-ttu-id="002e6-142">丹麦</span><span class="sxs-lookup"><span data-stu-id="002e6-142">Denmark</span></span>        | <span data-ttu-id="002e6-143">丹麦电子发票 (DK)</span><span class="sxs-lookup"><span data-stu-id="002e6-143">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="002e6-144">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-144">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-145">埃及</span><span class="sxs-lookup"><span data-stu-id="002e6-145">Egypt</span></span>          | <span data-ttu-id="002e6-146">埃及电子发票 (EG)</span><span class="sxs-lookup"><span data-stu-id="002e6-146">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="002e6-147">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-147">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-148">爱沙尼亚</span><span class="sxs-lookup"><span data-stu-id="002e6-148">Estonia</span></span>        | <span data-ttu-id="002e6-149">爱沙尼亚电子发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="002e6-149">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="002e6-150">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-150">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-151">芬兰</span><span class="sxs-lookup"><span data-stu-id="002e6-151">Finland</span></span>        | <span data-ttu-id="002e6-152">芬兰电子发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="002e6-152">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="002e6-153">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-153">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-154">法国</span><span class="sxs-lookup"><span data-stu-id="002e6-154">France</span></span>         | <span data-ttu-id="002e6-155">法国电子发票 (FR)</span><span class="sxs-lookup"><span data-stu-id="002e6-155">French electronic invoice (FR)</span></span>       | <span data-ttu-id="002e6-156">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-156">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-157">德国</span><span class="sxs-lookup"><span data-stu-id="002e6-157">Germany</span></span>        | <span data-ttu-id="002e6-158">德国电子发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="002e6-158">German electronic invoice (DE)</span></span>       | <span data-ttu-id="002e6-159">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-159">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-160">意大利</span><span class="sxs-lookup"><span data-stu-id="002e6-160">Italy</span></span>          | <span data-ttu-id="002e6-161">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="002e6-161">FatturaPA (IT)</span></span>                       | <span data-ttu-id="002e6-162">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-162">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-163">墨西哥</span><span class="sxs-lookup"><span data-stu-id="002e6-163">Mexico</span></span>         | <span data-ttu-id="002e6-164">墨西哥 CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-164">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="002e6-165">销售发票、装箱单、库存转移、付款补充和取消</span><span class="sxs-lookup"><span data-stu-id="002e6-165">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="002e6-166">荷兰</span><span class="sxs-lookup"><span data-stu-id="002e6-166">Netherlands</span></span>    | <span data-ttu-id="002e6-167">荷兰电子发票 (NL)</span><span class="sxs-lookup"><span data-stu-id="002e6-167">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="002e6-168">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-168">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-169">挪威</span><span class="sxs-lookup"><span data-stu-id="002e6-169">Norway</span></span>         | <span data-ttu-id="002e6-170">挪威电子发票 (NO)</span><span class="sxs-lookup"><span data-stu-id="002e6-170">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="002e6-171">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-171">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-172">西班牙</span><span class="sxs-lookup"><span data-stu-id="002e6-172">Spain</span></span>          | <span data-ttu-id="002e6-173">西班牙电子发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="002e6-173">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="002e6-174">销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-174">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="002e6-175">欧洲</span><span class="sxs-lookup"><span data-stu-id="002e6-175">Europe</span></span>         | <span data-ttu-id="002e6-176">PEPPOL 电子发票</span><span class="sxs-lookup"><span data-stu-id="002e6-176">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="002e6-177">PEPPOL 销售发票和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-177">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="002e6-178">电子开票功能的可配置组件</span><span class="sxs-lookup"><span data-stu-id="002e6-178">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="002e6-179">电子开票功能由以下几组可配置组件组成：</span><span class="sxs-lookup"><span data-stu-id="002e6-179">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="002e6-180">**格式** – 格式让您可以配置当电子单据成为电子发票时电子开票附加产品必须生成的内容。</span><span class="sxs-lookup"><span data-stu-id="002e6-180">**Formats** – Formats let you configure what the Electronic invoicing add-on must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="002e6-181">格式包括电子发票的格式配置，以及当需要与外部 Web 服务通信时用于提交请求和接收响应的文件和消息的格式配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-181">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="002e6-182">**操作** – 操作让您可以配置电子开票附加产品如何将 Finance 和 Supply Chain Management 提交的电子单据转换为电子发票。</span><span class="sxs-lookup"><span data-stu-id="002e6-182">**Actions** – Actions let you configure how the Electronic invoicing add-on generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="002e6-183">**适用性规则** – 适用性规则让您可以配置电子开票附加产品在处理电子开票功能时必须考虑的上下文。</span><span class="sxs-lookup"><span data-stu-id="002e6-183">**Applicability rules** – Applicability rules let you configure the context that the Electronic invoicing add-on must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="002e6-184">**变量** – 变量让您可以配置对构造配置逻辑的支持。</span><span class="sxs-lookup"><span data-stu-id="002e6-184">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="002e6-185">变量可以用作执行特定操作的值的输入。</span><span class="sxs-lookup"><span data-stu-id="002e6-185">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="002e6-186">或者，还可以用作 Finance 和 Supply Chain Management 与电子开票附加产品之间的值的交换。</span><span class="sxs-lookup"><span data-stu-id="002e6-186">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="002e6-187">**电子单据模型映射** – 电子单据模型映射可让您配置 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="002e6-187">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="002e6-188">此模型映射定义提交电子单据时集成到电子开票附加产品中的摘要发票的数据映射。</span><span class="sxs-lookup"><span data-stu-id="002e6-188">The model mapping defines the data mapping of the abstract invoice that is integrated into the Electronic invoicing add-on when electronic documents are submitted.</span></span>
- <span data-ttu-id="002e6-189">**发票上下文模型** – 发票上下文模型让您可以配置 ER 发票上下文模型并定义电子开票功能的上下文。</span><span class="sxs-lookup"><span data-stu-id="002e6-189">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="002e6-190">**响应类型** – 响应类型让您可以配置由于进行电子发票处理，电子开票附加产品必须在 Finance 和 Supply Chain Management 中进行的更新。</span><span class="sxs-lookup"><span data-stu-id="002e6-190">**Response types** – Response types let you configure what the Electronic invoicing add-on must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="002e6-191">格式</span><span class="sxs-lookup"><span data-stu-id="002e6-191">Formats</span></span>

<span data-ttu-id="002e6-192">以下列表显示了可用于电子开票功能的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-192">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="002e6-193">奥地利 (AT) 电子发票：奥地利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-193">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="002e6-194">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="002e6-194">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="002e6-195">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-195">OIOUBL Project invoice</span></span>
- <span data-ttu-id="002e6-196">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-196">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="002e6-197">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-197">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="002e6-198">比利时 (BE) 电子发票：比利时的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-198">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="002e6-199">UBL 销售发票 BE</span><span class="sxs-lookup"><span data-stu-id="002e6-199">UBL Sales invoice BE</span></span>
- <span data-ttu-id="002e6-200">UBL 项目发票 BE</span><span class="sxs-lookup"><span data-stu-id="002e6-200">UBL Project invoice BE</span></span>
- <span data-ttu-id="002e6-201">UBL 项目贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="002e6-201">UBL Project credit note BE</span></span>
- <span data-ttu-id="002e6-202">UBL 销售贷方通知单 BE</span><span class="sxs-lookup"><span data-stu-id="002e6-202">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="002e6-203">巴西 (BR) NF-e：NF-e 联邦（巴西）</span><span class="sxs-lookup"><span data-stu-id="002e6-203">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="002e6-204">NF-e 提交导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-204">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="002e6-205">NF-e 更正单导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-205">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="002e6-206">NF-e 取消导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-206">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="002e6-207">NF-e 弃用导出格式 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-207">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="002e6-208">巴西 NFS-e (BR)：NFS-e ABRASF 库里蒂巴市</span><span class="sxs-lookup"><span data-stu-id="002e6-208">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="002e6-209">NFS-e ABRASF 库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-209">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="002e6-210">NFS-e ABRASF 查询库里蒂巴 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-210">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a><span data-ttu-id="002e6-211">巴西 (BR) NFS-e：NFS-e 圣保罗市</span><span class="sxs-lookup"><span data-stu-id="002e6-211">Brazilian (BR) NFS-e: NFS-e São Paulo city</span></span>

- <span data-ttu-id="002e6-212">NFS-e 圣保罗 (BR)</span><span class="sxs-lookup"><span data-stu-id="002e6-212">NFS-e Sao Paulo (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="002e6-213">丹麦 (DK) 电子发票：丹麦的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-213">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="002e6-214">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="002e6-214">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="002e6-215">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-215">OIOUBL Project invoice</span></span>
- <span data-ttu-id="002e6-216">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-216">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="002e6-217">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-217">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="002e6-218">荷兰 (NL) 电子发票：荷兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-218">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="002e6-219">UBL 销售发票 NL</span><span class="sxs-lookup"><span data-stu-id="002e6-219">UBL Sales invoice NL</span></span>
- <span data-ttu-id="002e6-220">UBL 项目发票 NL</span><span class="sxs-lookup"><span data-stu-id="002e6-220">UBL Project invoice NL</span></span>
- <span data-ttu-id="002e6-221">UBL 项目贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="002e6-221">UBL Project credit note NL</span></span>
- <span data-ttu-id="002e6-222">UBL 销售贷方通知单 NL</span><span class="sxs-lookup"><span data-stu-id="002e6-222">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="002e6-223">埃及 (EG) 电子发票：埃及的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-223">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="002e6-224">销售发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="002e6-224">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="002e6-225">项目发票 (EG)（开票）</span><span class="sxs-lookup"><span data-stu-id="002e6-225">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="002e6-226">爱沙尼亚 (EE) 电子发票：爱沙尼亚的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-226">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="002e6-227">销售发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="002e6-227">Sales invoice (EE)</span></span>
- <span data-ttu-id="002e6-228">项目发票 (EE)</span><span class="sxs-lookup"><span data-stu-id="002e6-228">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="002e6-229">芬兰 (FI) 电子发票：芬兰的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-229">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="002e6-230">销售发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="002e6-230">Sales invoice (FI)</span></span>
- <span data-ttu-id="002e6-231">项目发票 (FI)</span><span class="sxs-lookup"><span data-stu-id="002e6-231">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="002e6-232">法国 (FR) 电子发票：法国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-232">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="002e6-233">UBL 销售发票 FR</span><span class="sxs-lookup"><span data-stu-id="002e6-233">UBL Sales invoice FR</span></span>
- <span data-ttu-id="002e6-234">UBL 项目发票 FR</span><span class="sxs-lookup"><span data-stu-id="002e6-234">UBL Project invoice FR</span></span>
- <span data-ttu-id="002e6-235">UBL 项目贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="002e6-235">UBL Project credit note FR</span></span>
- <span data-ttu-id="002e6-236">UBL 销售贷方通知单 FR</span><span class="sxs-lookup"><span data-stu-id="002e6-236">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="002e6-237">德国 (DE) 电子发票：德国的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-237">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="002e6-238">销售发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="002e6-238">Sales invoice (DE)</span></span>
- <span data-ttu-id="002e6-239">项目发票 (DE)</span><span class="sxs-lookup"><span data-stu-id="002e6-239">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="002e6-240">意大利 (IT) 电子发票：意大利的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-240">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="002e6-241">销售发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="002e6-241">Sales invoice (IT)</span></span>
- <span data-ttu-id="002e6-242">项目发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="002e6-242">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="002e6-243">墨西哥 (MX) CFDI：墨西哥的 CFDI</span><span class="sxs-lookup"><span data-stu-id="002e6-243">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="002e6-244">CFDI 发票格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-244">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="002e6-245">CFDI 装箱单 (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-245">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="002e6-246">CFDI 库存转移 (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-246">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="002e6-247">CFDI 付款格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-247">CFDI payment format (MX)</span></span>
- <span data-ttu-id="002e6-248">CFDI 发票取消格式 (MX)</span><span class="sxs-lookup"><span data-stu-id="002e6-248">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="002e6-249">挪威 (NO) 电子发票：挪威的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-249">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="002e6-250">OIOUBL 销售发票</span><span class="sxs-lookup"><span data-stu-id="002e6-250">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="002e6-251">OIOUBL 项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-251">OIOUBL Project invoice</span></span>
- <span data-ttu-id="002e6-252">OIOUBL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-252">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="002e6-253">OIOUBL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-253">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="002e6-254">PEPPOL 电子发票：PEPPOL 销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-254">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="002e6-255">PEPPOL 销售发票</span><span class="sxs-lookup"><span data-stu-id="002e6-255">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="002e6-256">PEPPOL 项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-256">PEPPOL Project invoice</span></span>
- <span data-ttu-id="002e6-257">PEPPOL 销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-257">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="002e6-258">PEPPOL 项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="002e6-258">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="002e6-259">西班牙 (ES) 电子发票：西班牙的销售和项目发票</span><span class="sxs-lookup"><span data-stu-id="002e6-259">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="002e6-260">销售发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="002e6-260">Sales invoice (ES)</span></span>
- <span data-ttu-id="002e6-261">项目发票 (ES)</span><span class="sxs-lookup"><span data-stu-id="002e6-261">Project invoice (ES)</span></span>

### <a name="actions"></a><span data-ttu-id="002e6-262">操作​​</span><span class="sxs-lookup"><span data-stu-id="002e6-262">Actions</span></span>

<span data-ttu-id="002e6-263">下表列出了可用操作，以及这些操作当前是正式发布还是仍处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="002e6-263">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="002e6-264">行为</span><span class="sxs-lookup"><span data-stu-id="002e6-264">Action</span></span>                                        | <span data-ttu-id="002e6-265">说明</span><span class="sxs-lookup"><span data-stu-id="002e6-265">Description</span></span>                                                                  | <span data-ttu-id="002e6-266">可用性</span><span class="sxs-lookup"><span data-stu-id="002e6-266">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="002e6-267">转换文档</span><span class="sxs-lookup"><span data-stu-id="002e6-267">Transform document</span></span>                            | <span data-ttu-id="002e6-268">运行电子报告格式来转换文档。</span><span class="sxs-lookup"><span data-stu-id="002e6-268">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="002e6-269">正式发布</span><span class="sxs-lookup"><span data-stu-id="002e6-269">Generally available</span></span>  |
| <span data-ttu-id="002e6-270">对 xml 文档签名</span><span class="sxs-lookup"><span data-stu-id="002e6-270">Sign xml document</span></span>                             | <span data-ttu-id="002e6-271">使用数字签名对 xml 文档进行签名。</span><span class="sxs-lookup"><span data-stu-id="002e6-271">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="002e6-272">预览模式</span><span class="sxs-lookup"><span data-stu-id="002e6-272">In preview</span></span>           |
| <span data-ttu-id="002e6-273">对埃及税务主管机构的 json 文档签名</span><span class="sxs-lookup"><span data-stu-id="002e6-273">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="002e6-274">使用数字签名对埃及税务主管机构的 json 文档签名。</span><span class="sxs-lookup"><span data-stu-id="002e6-274">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="002e6-275">正式发布</span><span class="sxs-lookup"><span data-stu-id="002e6-275">Generally available</span></span>  |
| <span data-ttu-id="002e6-276">与埃及 ETA 服务集成</span><span class="sxs-lookup"><span data-stu-id="002e6-276">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="002e6-277">与埃及税务主管机构通信。</span><span class="sxs-lookup"><span data-stu-id="002e6-277">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="002e6-278">正式发布</span><span class="sxs-lookup"><span data-stu-id="002e6-278">Generally available</span></span>  |
| <span data-ttu-id="002e6-279">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="002e6-279">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="002e6-280">与巴西 SEFAZ 服务集成以提交会计单据。</span><span class="sxs-lookup"><span data-stu-id="002e6-280">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="002e6-281">预览模式</span><span class="sxs-lookup"><span data-stu-id="002e6-281">In preview</span></span>           |
| <span data-ttu-id="002e6-282">调用墨西哥 PAC 服务</span><span class="sxs-lookup"><span data-stu-id="002e6-282">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="002e6-283">与墨西哥 PAC 服务集成以提交 CFDI。</span><span class="sxs-lookup"><span data-stu-id="002e6-283">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="002e6-284">预览模式</span><span class="sxs-lookup"><span data-stu-id="002e6-284">In preview</span></span>           |
| <span data-ttu-id="002e6-285">处理响应</span><span class="sxs-lookup"><span data-stu-id="002e6-285">Process response</span></span>                              | <span data-ttu-id="002e6-286">分析从 Web 服务调用收到的响应。</span><span class="sxs-lookup"><span data-stu-id="002e6-286">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="002e6-287">正式发布</span><span class="sxs-lookup"><span data-stu-id="002e6-287">Generally available</span></span>  |
| <span data-ttu-id="002e6-288">使用 MS Power Automate</span><span class="sxs-lookup"><span data-stu-id="002e6-288">Use MS Power Automate</span></span>                         | <span data-ttu-id="002e6-289">与 Microsoft Power Automate 内生成的流集成。</span><span class="sxs-lookup"><span data-stu-id="002e6-289">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="002e6-290">预览模式</span><span class="sxs-lookup"><span data-stu-id="002e6-290">In preview</span></span>           |

## <a name="configuration-providers"></a><span data-ttu-id="002e6-291">配置提供方</span><span class="sxs-lookup"><span data-stu-id="002e6-291">Configuration providers</span></span>

<span data-ttu-id="002e6-292">配置提供者提供电子开票功能及其 ER 组件，如模型映射、格式配置和上下文模型。</span><span class="sxs-lookup"><span data-stu-id="002e6-292">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="002e6-293">他们在关联的全局存储库中发布电子开票功能和 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="002e6-293">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="002e6-294">从那里，其他组织可以下载这些功能。</span><span class="sxs-lookup"><span data-stu-id="002e6-294">From there, other organizations can download them.</span></span>

<span data-ttu-id="002e6-295">在通过 RCS 配置电子开票功能之前，您必须在 **电子报告** 模块中将自己的组织配置为配置提供者。</span><span class="sxs-lookup"><span data-stu-id="002e6-295">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="002e6-296">有关如何将配置提供者设置为 **活动** 的信息，请参阅[创建配置提供者并将其标记为活动](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="002e6-296">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="002e6-297">查看全局存储库中的电子开票功能</span><span class="sxs-lookup"><span data-stu-id="002e6-297">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="002e6-298">要浏览特定配置提供者的全局存储库中可用的电子开票功能，请同步组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="002e6-298">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="002e6-299">完成同步后，可用电子开票功能的列表将更新。</span><span class="sxs-lookup"><span data-stu-id="002e6-299">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="002e6-300">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="002e6-300">Importing electronic invoicing features</span></span>

<span data-ttu-id="002e6-301">在使用或配置电子开票功能之前，必须将它们导入组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="002e6-301">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="002e6-302">导入操作将创建功能的本地副本，并将功能使用的所有 ER 项目（例如，格式配置和模型配置）复制到组织的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="002e6-302">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="002e6-303">您可以从任何配置提供者导入电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="002e6-303">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="002e6-304">创建电子开票功能</span><span class="sxs-lookup"><span data-stu-id="002e6-304">Creating electronic invoicing features</span></span>

<span data-ttu-id="002e6-305">您可以从头创建电子开票功能，也可以从另一个电子开票功能派生。</span><span class="sxs-lookup"><span data-stu-id="002e6-305">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="002e6-306">从头创建电子开票功能时，必须手动添加 ER 组件（例如，功能版本配置和其他配置，如功能版本设置和应用程序设置）。</span><span class="sxs-lookup"><span data-stu-id="002e6-306">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="002e6-307">通过从另一个功能派生来创建功能时，新功能将继承原始功能的所有配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-307">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="002e6-308">电子开票功能版本</span><span class="sxs-lookup"><span data-stu-id="002e6-308">Electronic invoicing feature version</span></span>

<span data-ttu-id="002e6-309">电子开票功能已版本化。</span><span class="sxs-lookup"><span data-stu-id="002e6-309">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="002e6-310">新版本创建时，版本号会自动递增。</span><span class="sxs-lookup"><span data-stu-id="002e6-310">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="002e6-311">可以为新版本定义“生效开始”日期。</span><span class="sxs-lookup"><span data-stu-id="002e6-311">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="002e6-312">电子开票功能版本采用的生命周期最多包含以下三种状态：</span><span class="sxs-lookup"><span data-stu-id="002e6-312">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="002e6-313">**草稿** – 如果功能版本处于此状态，您可以编辑其配置属性及其任何项目（例如，文件格式配置）。</span><span class="sxs-lookup"><span data-stu-id="002e6-313">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="002e6-314">**完成** – 如果功能版本处于此状态，说明该功能版本已发布到与您的组织关联的全局存储库中。</span><span class="sxs-lookup"><span data-stu-id="002e6-314">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="002e6-315">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="002e6-315">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="002e6-316">**已发布** – 如果功能版本处于此状态，说明该功能版本已被发布到电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="002e6-316">**Published** – If a feature version is in this status, it has been published to the Electronic invoicing add-on.</span></span> <span data-ttu-id="002e6-317">您不能再编辑功能版本或任何 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="002e6-317">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="002e6-318">功能配置</span><span class="sxs-lookup"><span data-stu-id="002e6-318">Feature configurations</span></span>

<span data-ttu-id="002e6-319">功能配置保留电子开票功能使用的所有 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-319">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="002e6-320">电子开票功能在处理期间使用的所有电子文件都来自已添加到该功能的功能配置中的格式配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-320">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="002e6-321">从功能配置，您可以访问 ER 格式设计器，这是用于创建格式配置的 ER 工具。</span><span class="sxs-lookup"><span data-stu-id="002e6-321">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="002e6-322">功能设置</span><span class="sxs-lookup"><span data-stu-id="002e6-322">Feature setup</span></span>

<span data-ttu-id="002e6-323">功能设置与功能配置结合使用。</span><span class="sxs-lookup"><span data-stu-id="002e6-323">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="002e6-324">每个功能设置都封装了一组提供预期行为的操作、适用性规则和变量，让电子开票功能可以满足电子发票的特定要求。</span><span class="sxs-lookup"><span data-stu-id="002e6-324">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="002e6-325">应用程序设置</span><span class="sxs-lookup"><span data-stu-id="002e6-325">Application setup</span></span>

<span data-ttu-id="002e6-326">应用程序设置必须与先前创建的已连接应用程序关联。</span><span class="sxs-lookup"><span data-stu-id="002e6-326">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="002e6-327">通过应用程序设置，您可以配置必须在 Finance 和 Supply Chain Management 中进行的电子开票功能的那一部分。</span><span class="sxs-lookup"><span data-stu-id="002e6-327">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="002e6-328">不论是什么电子开票功能，都至少必须有三个可配置组件：</span><span class="sxs-lookup"><span data-stu-id="002e6-328">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="002e6-329">**表名称** – Finance 和 Supply Chain Management 中的实体，保留过帐的发票，电子开票功能基于此实体。</span><span class="sxs-lookup"><span data-stu-id="002e6-329">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="002e6-330">**上下文** – 通过 ER 配置的发票上下文模型的名称。</span><span class="sxs-lookup"><span data-stu-id="002e6-330">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="002e6-331">**业务文档映射** – 通过 ER 配置的发票映射模型的名称。</span><span class="sxs-lookup"><span data-stu-id="002e6-331">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="002e6-332">可以在 Finance 和 Supply Chain Management 中查看在应用程序设置中输入的配置。</span><span class="sxs-lookup"><span data-stu-id="002e6-332">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="002e6-333">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="002e6-333">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="002e6-334">在 **电子单据** 选项卡上，选择 **部署**，然后选择 **相连应用程序** 选项。</span><span class="sxs-lookup"><span data-stu-id="002e6-334">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="002e6-335">部署功能版本</span><span class="sxs-lookup"><span data-stu-id="002e6-335">Deploying feature versions</span></span>

<span data-ttu-id="002e6-336">在 RCS 中，您使用 **部署** 命令定向发布电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="002e6-336">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="002e6-337">选择 **部署**，然后选择以下选项之一定义部署目标：</span><span class="sxs-lookup"><span data-stu-id="002e6-337">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="002e6-338">**服务环境** – 当部署的目标是服务环境时，电子开票功能版本将发布到服务环境。</span><span class="sxs-lookup"><span data-stu-id="002e6-338">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="002e6-339">然后，电子开票附加产品就可以接收和处理 Finance 和 Supply Chain Management 发送的电子单据了。</span><span class="sxs-lookup"><span data-stu-id="002e6-339">The Electronic invoicing add-on is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="002e6-340">**相连应用程序** – 当部署的目标是相连应用程序时，由应用程序安装程序提供的配置将写入先前与之关联的 Finance 和 Supply Chain Management 实例中。</span><span class="sxs-lookup"><span data-stu-id="002e6-340">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="002e6-341">仅状态为 **已完成** 的电子开票功能版本可以部署到服务环境或连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="002e6-341">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="002e6-342">删除功能版本</span><span class="sxs-lookup"><span data-stu-id="002e6-342">Removing feature versions</span></span>

<span data-ttu-id="002e6-343">在 RCS 中，您使用 **取消部署** 命令从电子开票附加产品中的服务环境中删除特定的电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="002e6-343">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in the Electronic invoicing add-on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="002e6-344">**取消部署** 命令仅在服务环境中有效。</span><span class="sxs-lookup"><span data-stu-id="002e6-344">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="002e6-345">它不会从连接的应用程序中删除电子开票功能版本。</span><span class="sxs-lookup"><span data-stu-id="002e6-345">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="002e6-346">重定电子开票功能</span><span class="sxs-lookup"><span data-stu-id="002e6-346">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="002e6-347">当一个电子开票功能是从另一个电子开票功能派生而来时，**重定** 命令使用原始功能中引入的更改来更新派生功能。</span><span class="sxs-lookup"><span data-stu-id="002e6-347">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="002e6-348">其他资源</span><span class="sxs-lookup"><span data-stu-id="002e6-348">Additional resources</span></span>

- [<span data-ttu-id="002e6-349">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="002e6-349">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
