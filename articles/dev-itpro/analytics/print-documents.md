---
title: 文档打印概览
description: 在 Microsoft Dynamics 365 for Finance and Operations 中，可使用本地打印机或联网设备打印文档。 本文概览如何打印文档。
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 779931a779cdb8fcbc8e85c3d6c2a4e123d8ec47
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864656"
---
# <a name="document-printing-overview"></a><span data-ttu-id="40fd7-104">文档打印概览</span><span class="sxs-lookup"><span data-stu-id="40fd7-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40fd7-105">在 Microsoft Dynamics 365 for Finance and Operations 中，可使用本地打印机或联网设备打印文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-105">In Microsoft Dynamics 365 for Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="40fd7-106">本文概览如何打印文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="40fd7-107">打印概览</span><span class="sxs-lookup"><span data-stu-id="40fd7-107">Printing overview</span></span>

<span data-ttu-id="40fd7-108">Microsoft Dynamics 365 for Finance and Operations 提供集成的设备和客户端应用程序，可用于轻松生成、存储和分发为业务活动提供支持的文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-108">Microsoft Dynamics 365 for Finance and Operations provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="40fd7-109">在 Finance and Operations 中，可使用本地打印机或联网设备打印文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-109">In Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="40fd7-110">此外，还可以将 Finance and Operations 页面和报表作为 PDF 文件或 Microsoft Office 文档直接从客户端导出。</span><span class="sxs-lookup"><span data-stu-id="40fd7-110">In addition, you can export Finance and Operations pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="40fd7-111">最后，可通过分布式工作量使用网络资源直接从移动设备打印业务文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="40fd7-112">尽管打印要求可能各不相同，但是所有行业通常必须使用 Finance and Operations 创建业务文档的硬拷贝。</span><span class="sxs-lookup"><span data-stu-id="40fd7-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using Finance and Operations.</span></span> <span data-ttu-id="40fd7-113">在网络设备上使用托管应用程序打印文档面临一些独有的挑战。</span><span class="sxs-lookup"><span data-stu-id="40fd7-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="40fd7-114">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="40fd7-114">Here are some examples:</span></span>

- <span data-ttu-id="40fd7-115">用户的设备上可能没有打印驱动程序。</span><span class="sxs-lookup"><span data-stu-id="40fd7-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="40fd7-116">用户的设备可能未连接到公司网络。</span><span class="sxs-lookup"><span data-stu-id="40fd7-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="40fd7-117">系统管理员可使用专用主机和执行一些简单的步骤配置部署，以便用户在网络设备上直接从业务应用程序进行打印。</span><span class="sxs-lookup"><span data-stu-id="40fd7-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="printing-scenarios-in-finance-and-operations-applications"></a><span data-ttu-id="40fd7-118">Finance and Operations 应用程序中的打印场景</span><span class="sxs-lookup"><span data-stu-id="40fd7-118">Printing scenarios in Finance and Operations applications</span></span>

<span data-ttu-id="40fd7-119">下表介绍 Finance and Operations applications 中的三种主要的打印场景。</span><span class="sxs-lookup"><span data-stu-id="40fd7-119">The following table describes the three primary printing scenarios in Finance and Operations applications.</span></span>

| <span data-ttu-id="40fd7-120">应用场景</span><span class="sxs-lookup"><span data-stu-id="40fd7-120">Scenario</span></span>                        | <span data-ttu-id="40fd7-121">目标</span><span class="sxs-lookup"><span data-stu-id="40fd7-121">Goal</span></span>                                                      | <span data-ttu-id="40fd7-122">解决方案</span><span class="sxs-lookup"><span data-stu-id="40fd7-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="40fd7-123">1. 打印所见</span><span class="sxs-lookup"><span data-stu-id="40fd7-123">1. Printing what you see</span></span>        | <span data-ttu-id="40fd7-124">打印浏览器中当前显示的内容。</span><span class="sxs-lookup"><span data-stu-id="40fd7-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="40fd7-125">将为浏览器生成“适合打印的”网页版本。</span><span class="sxs-lookup"><span data-stu-id="40fd7-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="40fd7-126">2. 交互式打印</span><span class="sxs-lookup"><span data-stu-id="40fd7-126">2. Interactive printing</span></span>         | <span data-ttu-id="40fd7-127">在本地连接的设备上打印精确文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="40fd7-128">可导出报表的 PDF 版本并下载到浏览器。</span><span class="sxs-lookup"><span data-stu-id="40fd7-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="40fd7-129">3. 在网络设备上打印</span><span class="sxs-lookup"><span data-stu-id="40fd7-129">3. Printing on a network device</span></span> | <span data-ttu-id="40fd7-130">将精确文档发送到域打印机设备。</span><span class="sxs-lookup"><span data-stu-id="40fd7-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="40fd7-131">将把精确文档发送到客户域中托管的服务器上运行的客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="40fd7-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="40fd7-132">由于解决方案因场景而异，所以 Finance and Operations 应用程序提供内置服务和工具，帮助用户达成目标：</span><span class="sxs-lookup"><span data-stu-id="40fd7-132">Because the solution varies, depending on the scenario, Finance and Operations applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="40fd7-133">**场景 1** 受浏览器的 HTML5客户端呈现支持。</span><span class="sxs-lookup"><span data-stu-id="40fd7-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="40fd7-134">**场景 2** 使用客户端应用程序和 Microsoft Office 365 服务。</span><span class="sxs-lookup"><span data-stu-id="40fd7-134">**Scenario 2** uses client applications and Microsoft Office 365 services.</span></span>
- <span data-ttu-id="40fd7-135">**场景 3** 需要客户端应用程序支持和 Microsoft Azure 中托管的服务支持。</span><span class="sxs-lookup"><span data-stu-id="40fd7-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="40fd7-136">除了部署到 Azure 订阅的平台，Finance and Operations 应用程序还为客户提供集成的第一方 Azure 应用程序，帮助客户轻松使用域托管的设备打印文档。</span><span class="sxs-lookup"><span data-stu-id="40fd7-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="40fd7-137">服务概览</span><span class="sxs-lookup"><span data-stu-id="40fd7-137">Service overview</span></span>
<span data-ttu-id="40fd7-138">托管应用程序生成的文档在联网设备上等待打印时，存储在 Azure blob 存储中。</span><span class="sxs-lookup"><span data-stu-id="40fd7-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="40fd7-139">[文档路线选择代理](install-document-routing-agent.md)使用 Azure 身份验证建立通往 Azure 服务的安全通道。</span><span class="sxs-lookup"><span data-stu-id="40fd7-139">The [Document Routing Agent](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="40fd7-140">**执行序列**</span><span class="sxs-lookup"><span data-stu-id="40fd7-140">**Execution sequence**</span></span>

1. <span data-ttu-id="40fd7-141">报表由 Microsoft SQL Server Reporting Services (SSRS) 生成，存储在 Azure blob 存储中。</span><span class="sxs-lookup"><span data-stu-id="40fd7-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="40fd7-142">附加的打印机设置随文档一起存储。</span><span class="sxs-lookup"><span data-stu-id="40fd7-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="40fd7-143">文档路线选择代理查询 Azure 服务总线队列以查找有效作业。</span><span class="sxs-lookup"><span data-stu-id="40fd7-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="40fd7-144">文档由文档路线选择代理下载并假托到网络打印机。</span><span class="sxs-lookup"><span data-stu-id="40fd7-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="40fd7-145">客户可使用基于客户端的解决方案管理打印需求的规模。</span><span class="sxs-lookup"><span data-stu-id="40fd7-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="40fd7-146">打印工作量繁重的客户可安装多个文档路线选择代理来增加并行打印操作的数量。</span><span class="sxs-lookup"><span data-stu-id="40fd7-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="40fd7-147">不过，有些客户只需极少量的文档路线选择代理安装即可处理其预期的打印需求。</span><span class="sxs-lookup"><span data-stu-id="40fd7-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="40fd7-148">网络打印的服务组件</span><span class="sxs-lookup"><span data-stu-id="40fd7-148">Service components for network printing</span></span>

<span data-ttu-id="40fd7-149">下图显示有助于为网络打印操作提供支持的基本组件。</span><span class="sxs-lookup"><span data-stu-id="40fd7-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="40fd7-150">[![网络打印的服务组件\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="40fd7-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="40fd7-151">请注意，可将一台打印机与多个文档路线选择代理关联。</span><span class="sxs-lookup"><span data-stu-id="40fd7-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="40fd7-152">为了解析打印机首选项，托管服务使用用于唯一标识每台网络打印机的网络路径。</span><span class="sxs-lookup"><span data-stu-id="40fd7-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="40fd7-153">因此，即使一台打印机被多个客户端注册，也会在 Finance and Operations 应用程序中的打印机列表内显示为单项选择。</span><span class="sxs-lookup"><span data-stu-id="40fd7-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in Finance and Operations applications.</span></span>
