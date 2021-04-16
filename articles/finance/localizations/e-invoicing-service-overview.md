---
title: 电子开票概览
description: 本主题提供有关 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的电子开票的信息。
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
ms.openlocfilehash: a6a8ea3fcad980dc02f489e07a7b21fe1c1b5a5a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839972"
---
# <a name="electronic-invoicing-overview"></a><span data-ttu-id="1ef41-103">电子开票概览</span><span class="sxs-lookup"><span data-stu-id="1ef41-103">Electronic invoicing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ef41-104">Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的电子开票是一种超级可扩展的多租户服务，可对电子发票单据进行可配置的处理并进行可配置的单据交换。</span><span class="sxs-lookup"><span data-stu-id="1ef41-104">Electronic invoicing for Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management is a hyper-scalable multitenant service that enables configurable processing of electronic invoice documents and configurable document exchange.</span></span> <span data-ttu-id="1ef41-105">处理和集成规则完全可配置，逻辑在 Finance 和 Supply Chain Management 外部运行。</span><span class="sxs-lookup"><span data-stu-id="1ef41-105">The processing and integration rules are fully configurable, and the logic is run outside Finance and Supply Chain Management.</span></span> <span data-ttu-id="1ef41-106">此服务主要针对企业对政府方案中的电子发票处理，但可以自定义配置来用于其他目的。</span><span class="sxs-lookup"><span data-stu-id="1ef41-106">The service is targeted mainly at e-invoice processing in business-to-government scenarios, but it can be custom-configured for other purposes.</span></span>

<span data-ttu-id="1ef41-107">电子开票可以帮助您实现以下目标：</span><span class="sxs-lookup"><span data-stu-id="1ef41-107">Electronic invoicing can help you achieve the following goals:</span></span>

- <span data-ttu-id="1ef41-108">快速轻松地采用国家/地区特定要求</span><span class="sxs-lookup"><span data-stu-id="1ef41-108">Fast and easy adoption of country/region-specific requirements</span></span>
- <span data-ttu-id="1ef41-109">标准化实施电子开解决方案</span><span class="sxs-lookup"><span data-stu-id="1ef41-109">Standardized implementations of an Electronic invoicing solution</span></span>
- <span data-ttu-id="1ef41-110">增强了文档历史记录的可追溯性</span><span class="sxs-lookup"><span data-stu-id="1ef41-110">Enhanced traceability of document history</span></span>
- <span data-ttu-id="1ef41-111">实施周期更短</span><span class="sxs-lookup"><span data-stu-id="1ef41-111">Shorter implementation cycle</span></span>
- <span data-ttu-id="1ef41-112">降低总拥有成本 (TCO)</span><span class="sxs-lookup"><span data-stu-id="1ef41-112">Reduced total cost of ownership (TCO)</span></span>
- <span data-ttu-id="1ef41-113">可轻松调整配置，无需更改代码</span><span class="sxs-lookup"><span data-stu-id="1ef41-113">Easily adjustable configurations that don't required code changes</span></span>
- <span data-ttu-id="1ef41-114">简化配置包装</span><span class="sxs-lookup"><span data-stu-id="1ef41-114">Simplified configuration packaging</span></span>
- <span data-ttu-id="1ef41-115">内置的导出、导入和集成，并可在电子发票单据处理中轻松扩展</span><span class="sxs-lookup"><span data-stu-id="1ef41-115">Built-in export, import, and integration, and easy extensibility in the processing of e-invoice documents</span></span>
- <span data-ttu-id="1ef41-116">在公司之间轻松重复使用相同的导出、导入和集成配置</span><span class="sxs-lookup"><span data-stu-id="1ef41-116">Easy reuse of the same export, import, and integration configurations across companies</span></span>

<span data-ttu-id="1ef41-117">若要使用电子开票，您必须从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目安装它。</span><span class="sxs-lookup"><span data-stu-id="1ef41-117">To use Electronic invoicing, you must install it from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1ef41-118">接下来，按照设置过程打开与 Finance 或 Supply Chain Management 的集成。</span><span class="sxs-lookup"><span data-stu-id="1ef41-118">Next, follow the setup procedure to turn on the integration with Finance or Supply Chain Management.</span></span> <span data-ttu-id="1ef41-119">有关详细信息，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="1ef41-119">For more information, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="service-availability"></a><a name="availability"></a><span data-ttu-id="1ef41-120">服务可用性</span><span class="sxs-lookup"><span data-stu-id="1ef41-120">Service availability</span></span>

<span data-ttu-id="1ef41-121">当前，电子开票通过预览计划向客户提供，在下一阶段，此服务将正式发布。</span><span class="sxs-lookup"><span data-stu-id="1ef41-121">Currently Electronic invoicing is available to customers through the preview program, and in the next phase, the service will become generally available.</span></span> <span data-ttu-id="1ef41-122">由于满足国家/地区特定要求的功能可能会在发行的不同阶段受到限制，因此您应该始终查看最新文档，这些文档重点介绍了受支持的国家/地区特定解决方案的覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="1ef41-122">Because functionality that addresses country/region-specific requirements might be limited at different phases of the release, you should always check the most up-to-date documentation that highlights the coverage and scope of supported country/region-specific solutions.</span></span>

<span data-ttu-id="1ef41-123">电子开票在以下 Azure 地理区域部署：</span><span class="sxs-lookup"><span data-stu-id="1ef41-123">Electronic invoicing is deployed in the following Azure geographies:</span></span>

- <span data-ttu-id="1ef41-124">美国</span><span class="sxs-lookup"><span data-stu-id="1ef41-124">United States</span></span>
- <span data-ttu-id="1ef41-125">欧洲</span><span class="sxs-lookup"><span data-stu-id="1ef41-125">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="1ef41-126">电子开票不支持本地部署。</span><span class="sxs-lookup"><span data-stu-id="1ef41-126">Electronic invoicing doesn't support on-premises deployments.</span></span>

## <a name="extended-configurability"></a><span data-ttu-id="1ef41-127">扩展的可配置性</span><span class="sxs-lookup"><span data-stu-id="1ef41-127">Extended configurability</span></span>

<span data-ttu-id="1ef41-128">电子开票可用于必须创建电子单据并将其发送给指定方的场景。</span><span class="sxs-lookup"><span data-stu-id="1ef41-128">Electronic invoicing can be used in scenarios where you must create and send an electronic document to the designated parties.</span></span> <span data-ttu-id="1ef41-129">它是专为根据接收到的数据运行可配置的处理操作流而设计的。</span><span class="sxs-lookup"><span data-stu-id="1ef41-129">It's specifically designed for running a configurable flow of processing actions, based on received data.</span></span> <span data-ttu-id="1ef41-130">Finance 和 Supply Chain Management 中提供的可配置性选项仅限于文档转换。</span><span class="sxs-lookup"><span data-stu-id="1ef41-130">The configurability options that are available in Finance and Supply Chain Management are limited to document transformation.</span></span> <span data-ttu-id="1ef41-131">此服务通过添加服务中提供的可配置集成来扩展这些选项。</span><span class="sxs-lookup"><span data-stu-id="1ef41-131">The service extends these options by adding the configurable integrations that are available in it.</span></span> <span data-ttu-id="1ef41-132">此外，所有以前提供的电子发票功能，如巴西 Nota fiscal eletrônica (NF-e)、墨西哥 Comprobante Fiscal Digital por Internet (CFDI) 或其他西欧通用商业语言 (UBL)/泛欧洲 Public Procurement OnLine (PEPPOL) 功能，将使用配置导出和导入，以及支持与外部 Web 服务的集成。</span><span class="sxs-lookup"><span data-stu-id="1ef41-132">In addition, all the electronic invoice functionalities that were previously available, such as Brazilian Nota fiscal eletrônica (NF-e), Mexican Comprobante Fiscal Digital por Internet (CFDI), or other Western European Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) functionalities, will use configurations for export and import, and to enable integrations with external web services.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="1ef41-133">功能亮点</span><span class="sxs-lookup"><span data-stu-id="1ef41-133">Feature highlights</span></span>

- <span data-ttu-id="1ef41-134">与 Finance 和 Supply Chain management 的现成集成</span><span class="sxs-lookup"><span data-stu-id="1ef41-134">Out-of-box integration with Finance and Supply Chain management</span></span>
- <span data-ttu-id="1ef41-135">所有国家或地区的电子发票流程的配置和监视具有一致的用户体验</span><span class="sxs-lookup"><span data-stu-id="1ef41-135">Consistent user experience for the configuration and monitoring of the e-invoice process for all countries or regions</span></span>
- <span data-ttu-id="1ef41-136">在新的国家或地区更快、更轻松、更便宜地采用电子开票解决方案</span><span class="sxs-lookup"><span data-stu-id="1ef41-136">Faster, easier, and less expensive adoption of Electronic invoicing solutions in new countries or regions</span></span>
- <span data-ttu-id="1ef41-137">通过 Regulatory Configuration Service (RCS) 和全球化功能设置来配置服务</span><span class="sxs-lookup"><span data-stu-id="1ef41-137">Configuration of the service through the Regulatory Configuration Service (RCS) and Globalization feature setup</span></span>
- <span data-ttu-id="1ef41-138">使用 RCS 中定义的配置将业务数据转换为多种电子发票格式（XML、JavaScript 对象表示法\[JSON\]、TXT 和逗号分隔值\[CSV\]）：</span><span class="sxs-lookup"><span data-stu-id="1ef41-138">Transformation of business data into multiple e-invoice formats (XML, JavaScript Object Notation \[JSON\], TXT, and comma-separated values \[CSV\]) by using configurations that are defined in RCS:</span></span>

    - <span data-ttu-id="1ef41-139">电子报告格式可用于无法配置电子发票转换的国家或地区</span><span class="sxs-lookup"><span data-stu-id="1ef41-139">Electronic reporting formats that are available for countries or regions where configurability for e-invoice transformation isn't available</span></span>

- <span data-ttu-id="1ef41-140">可配置向外部 Web 服务的电子发票提交，包括通过数字签名处理认证：</span><span class="sxs-lookup"><span data-stu-id="1ef41-140">Configurable submission of e-invoices to external web services, including certification handling through digital signatures:</span></span>

    - <span data-ttu-id="1ef41-141">内置、易于扩展且可配置的集成包含适用于多个国家/地区的其他内容</span><span class="sxs-lookup"><span data-stu-id="1ef41-141">Built-in, easily extendable, and configurable integration with additional content for several countries</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ef41-142">当前仅支持有限数量的直接提交。</span><span class="sxs-lookup"><span data-stu-id="1ef41-142">Currently, a limited number of direct submissions are supported.</span></span> <span data-ttu-id="1ef41-143">有关详细信息，请参阅本主题前面的[服务可用性](#availability)一节。</span><span class="sxs-lookup"><span data-stu-id="1ef41-143">For more information, see the [Service availability](#availability) section earlier in this topic.</span></span> <span data-ttu-id="1ef41-144">支持会在将来扩大。</span><span class="sxs-lookup"><span data-stu-id="1ef41-144">Support will be extended in the future.</span></span>

- <span data-ttu-id="1ef41-145">处理 Web 服务的响应，包括可配置的异常消息处理</span><span class="sxs-lookup"><span data-stu-id="1ef41-145">Handling of responses from web services, including configurable exception message handling</span></span>
- <span data-ttu-id="1ef41-146">支持电子签名（例如，使用 XMLDSig 签名算法）</span><span class="sxs-lookup"><span data-stu-id="1ef41-146">Support for electronic signatures (for example, by using the XMLDSig signing algorithm)</span></span>
- <span data-ttu-id="1ef41-147">批量处理电子发票消息</span><span class="sxs-lookup"><span data-stu-id="1ef41-147">Batch processing of e-invoice messages</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="1ef41-148">体系结构和数据流</span><span class="sxs-lookup"><span data-stu-id="1ef41-148">Architecture and data flow</span></span>

<span data-ttu-id="1ef41-149">从 LCS 安装电子开票，并且在所有必需的应用程序中完成必需设置后，安全连接已建立。</span><span class="sxs-lookup"><span data-stu-id="1ef41-149">When Electronic invoicing is installed from LCS, and the required setup is completed in all required applications, a secure connection is established.</span></span> <span data-ttu-id="1ef41-150">此服务当前位于美国和欧洲的数据中心。</span><span class="sxs-lookup"><span data-stu-id="1ef41-150">The service is currently located in data centers in the United States and Europe.</span></span> <span data-ttu-id="1ef41-151">因此，服务位置可能与相关的 Finance 或 Supply Chain Management 实例的位置不同。</span><span class="sxs-lookup"><span data-stu-id="1ef41-151">Therefore, the service location might differ from the location of the related Finance or Supply Chain Management instance.</span></span> <span data-ttu-id="1ef41-152">在完成电子开票的设置并打开集成后，每当发送电子发票时，与特定单据相关的主数据和交易数据就会发送到电子开票。</span><span class="sxs-lookup"><span data-stu-id="1ef41-152">After you complete the setup of Electronic invoicing and turn on the integration, whenever an electronic invoice is sent, master data and transactional data that are related to a specific document are sent to Electronic invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="1ef41-153">如果您的电子发票或任何其他单据包含个人数据，请验证您对此功能的使用符合《一般数据保护条例》(GDPR) 以及与个人数据传输有关的其他法规的要求。</span><span class="sxs-lookup"><span data-stu-id="1ef41-153">If your electronic invoice or any other document contains personal data, verify that your use of this feature meets the General Data Protection Regulation (GDPR) and other regulations that are related to the transfer of personal data.</span></span>

### <a name="high-level-description-of-the-data-flow"></a><span data-ttu-id="1ef41-154">数据流的高级描述</span><span class="sxs-lookup"><span data-stu-id="1ef41-154">High-level description of the data flow</span></span>

1. <span data-ttu-id="1ef41-155">客户端将规范的业务文档发送到服务。</span><span class="sxs-lookup"><span data-stu-id="1ef41-155">The client sends a canonical business document to the service.</span></span>
2. <span data-ttu-id="1ef41-156">基于从客户端接收的上下文信息，服务选择适用的处理流。</span><span class="sxs-lookup"><span data-stu-id="1ef41-156">Based on the context information that is received from the client, the service selects the applicable processing flow.</span></span>
3. <span data-ttu-id="1ef41-157">服务运行处理操作。</span><span class="sxs-lookup"><span data-stu-id="1ef41-157">The service runs the processing actions.</span></span> <span data-ttu-id="1ef41-158">这些操作可能包括将商业文档转换为电子发票、应用电子签名以及将文档提交给外部 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="1ef41-158">These actions might include transforming the business document into an electronic invoice, applying an electronic signature, and submitting the document to an external web service.</span></span>
4. <span data-ttu-id="1ef41-159">所有接收和处理的文档都存储在客户的 Azure Blob 存储中。</span><span class="sxs-lookup"><span data-stu-id="1ef41-159">All the received and processed documents are stored in the customer's Azure Blob storage.</span></span>
5. <span data-ttu-id="1ef41-160">用于处理的所有租户密码和证书都存储在客户的 Azure 密钥保管库中。</span><span class="sxs-lookup"><span data-stu-id="1ef41-160">All the tenant secrets and certificates that were used for processing are stored in the customer's Azure key vault.</span></span>
6. <span data-ttu-id="1ef41-161">服务向客户端提供有关已发送的业务文档的处理状态的按需信息。</span><span class="sxs-lookup"><span data-stu-id="1ef41-161">The service provides on-demand information to the client about the processing status of the business document that was sent.</span></span>
7. <span data-ttu-id="1ef41-162">客户端接收有关完成的处理执行的信息，并使所有日志信息可用。</span><span class="sxs-lookup"><span data-stu-id="1ef41-162">The client receives information about the completed processing execution and makes all the log information available.</span></span> <span data-ttu-id="1ef41-163">同时还使在流处理运行时创建或接收的文档可用。</span><span class="sxs-lookup"><span data-stu-id="1ef41-163">It also makes the document that was created or received during flow processing available.</span></span>

<span data-ttu-id="1ef41-164">下图显示了数据如何流入和流出电子开票。</span><span class="sxs-lookup"><span data-stu-id="1ef41-164">The following illustration shows how data flows to and from Electronic invoicing.</span></span>

![电子开票的数据流](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a><span data-ttu-id="1ef41-166">隐私声明</span><span class="sxs-lookup"><span data-stu-id="1ef41-166">Privacy notice</span></span>
<span data-ttu-id="1ef41-167">启用和使用电子开票可能需要发送有限的数据，其中包括组织税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="1ef41-167">Enabling and using Electronic invoicing may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="1ef41-168">这将被传输到税务机构授权的第三方机构，以便以与这些政府的 Web 服务集成所需的预定义格式发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="1ef41-168">This will be transmitted to third-party agencies authorized by the tax authorities for purposes of sending electronic invoices in the predefined formats required for integration with these government’s web services.</span></span> <span data-ttu-id="1ef41-169">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="1ef41-169">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="1ef41-170">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="1ef41-170">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ef41-171">其他资源</span><span class="sxs-lookup"><span data-stu-id="1ef41-171">Additional resources</span></span>
- [<span data-ttu-id="1ef41-172">服务管理</span><span class="sxs-lookup"><span data-stu-id="1ef41-172">Service administration</span></span>](e-invoicing-service-administration.md)
- [<span data-ttu-id="1ef41-173">在 RCS 中配置电子发票</span><span class="sxs-lookup"><span data-stu-id="1ef41-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="1ef41-174">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="1ef41-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
