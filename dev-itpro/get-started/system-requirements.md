---
title: "云部署的系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 云部署的系统要求。"
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: zh-cn
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="7b064-103">云部署的系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b064-104">此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 云部署的系统要求。</span><span class="sxs-lookup"><span data-stu-id="7b064-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="7b064-105">在你安装 Finance and Operations 前，适合执行此步骤时验证你正在使用的系统是否满足或超出最低网络、硬件和软件要求。</span><span class="sxs-lookup"><span data-stu-id="7b064-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="7b064-106">支持的 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="7b064-106">Supported web browsers</span></span>
<span data-ttu-id="7b064-107">Web 应用程序可在指定操作系统上运行的以下任一 Web 浏览器中运行：</span><span class="sxs-lookup"><span data-stu-id="7b064-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="7b064-108">Windows 10 上的 Microsoft Edge（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="7b064-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="7b064-109">Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="7b064-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="7b064-110">Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="7b064-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="7b064-111">Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="7b064-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="7b064-112">要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。</span><span class="sxs-lookup"><span data-stu-id="7b064-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="7b064-113">必须安装预发布 Chrome 扩展以允许任务录制器捕获屏幕截图并包括在生成的 Microsoft Word 文档中。</span><span class="sxs-lookup"><span data-stu-id="7b064-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="7b064-114">Workflow Editor 作为 ClickOnce 应用程序启动。</span><span class="sxs-lookup"><span data-stu-id="7b064-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="7b064-115">只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。</span><span class="sxs-lookup"><span data-stu-id="7b064-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="7b064-116">Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。</span><span class="sxs-lookup"><span data-stu-id="7b064-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="7b064-117">适用于财务申报的报表设计器作为 ClickOnce 应用程序启动。</span><span class="sxs-lookup"><span data-stu-id="7b064-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="7b064-118">它需要 64 位兼容操作系统。</span><span class="sxs-lookup"><span data-stu-id="7b064-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="7b064-119">如果使用的是 Chrome，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。</span><span class="sxs-lookup"><span data-stu-id="7b064-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="7b064-120">如果以匿名模式使用 Chrome，请确保也为匿名模式启用 ClickOnce 扩展。</span><span class="sxs-lookup"><span data-stu-id="7b064-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="7b064-121">若要预览 PDF 文件，我们建议您使用 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）等浏览器。</span><span class="sxs-lookup"><span data-stu-id="7b064-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="7b064-122">Retail Cloud POS 支持的 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="7b064-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="7b064-123">Retail Cloud POS 可在指定操作系统上运行的以下任一 Web 浏览器中运行：</span><span class="sxs-lookup"><span data-stu-id="7b064-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="7b064-124">Windows 10 上的 Microsoft Edge（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="7b064-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="7b064-125">Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="7b064-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="7b064-126">Windows 10、Windows 8.1 或 Windows 7 上的 Chrome（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="7b064-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="7b064-127">网络要求</span><span class="sxs-lookup"><span data-stu-id="7b064-127">Network requirements</span></span>
-   <span data-ttu-id="7b064-128">Finance and Operations 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。</span><span class="sxs-lookup"><span data-stu-id="7b064-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="7b064-129">此延迟是从浏览器客户端到托管 Finance and Operations 的 Microsoft Azure 数据中心的延迟。</span><span class="sxs-lookup"><span data-stu-id="7b064-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="7b064-130">建议在 <http://www.azurespeed.com> 测试网络延迟。</span><span class="sxs-lookup"><span data-stu-id="7b064-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="7b064-131">Finance and Operations 的带宽要求取决于你的方案。</span><span class="sxs-lookup"><span data-stu-id="7b064-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="7b064-132">大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。</span><span class="sxs-lookup"><span data-stu-id="7b064-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="7b064-133">但是，对于需要高负载要求的方案（如涉及工作区或大量自定义的方案），建议提供更高带宽。</span><span class="sxs-lookup"><span data-stu-id="7b064-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="7b064-134">Finance and Operations 通常已针对 Internet 进行了优化。</span><span class="sxs-lookup"><span data-stu-id="7b064-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="7b064-135">从浏览器客户端到 Azure 数据中心的往返次数很小，并且整个负载经过压缩。</span><span class="sxs-lookup"><span data-stu-id="7b064-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="7b064-136">请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。</span><span class="sxs-lookup"><span data-stu-id="7b064-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="7b064-137">给定位置的并行使用很难计算。</span><span class="sxs-lookup"><span data-stu-id="7b064-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="7b064-138">注重带宽要求的客户应使用 Finance and Operations 预览版本。</span><span class="sxs-lookup"><span data-stu-id="7b064-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="7b064-139">.NET Framework 要求</span><span class="sxs-lookup"><span data-stu-id="7b064-139">.NET Framework requirements</span></span>
<span data-ttu-id="7b064-140">Finance and Operations 需要 Microsoft .NET Framework 版本 4.6.2 以满足所有一键式应用程序的要求，如文档路由代理程序。</span><span class="sxs-lookup"><span data-stu-id="7b064-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="7b064-141">有关安装说明，请参阅[安装 .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)。</span><span class="sxs-lookup"><span data-stu-id="7b064-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="7b064-142">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="7b064-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="7b064-143">以下 Microsoft Office 应用程序在 Finance and Operations 的云和本地部署中受支持：</span><span class="sxs-lookup"><span data-stu-id="7b064-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="7b064-144">若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。</span><span class="sxs-lookup"><span data-stu-id="7b064-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="7b064-145">有关版本要求的详细信息，请参阅 [Office 集成疑难解答](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting)。</span><span class="sxs-lookup"><span data-stu-id="7b064-145">For more information about version requirements, see [Office integration troubleshooting](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span></span>
-   <span data-ttu-id="7b064-146">若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="7b064-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="7b064-147">Retail Modern POS 要求</span><span class="sxs-lookup"><span data-stu-id="7b064-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="7b064-148">如果 Retail Modern POS 将使用脱机数据库，计算机必须满足 Microsoft SQL Server 的所有系统要求。</span><span class="sxs-lookup"><span data-stu-id="7b064-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="7b064-149">Retail Modern POS 脱机数据库支持带 Service Pack 3 或更高版本的 Microsoft SQL Server 2012、带 Service Pack 2 或更高版本的 Microsoft SQL Server 2014，以及 Microsoft SQL Server 2016。</span><span class="sxs-lookup"><span data-stu-id="7b064-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="7b064-150">建议始终使用可用的最新版本，并安装所有最新服务包。</span><span class="sxs-lookup"><span data-stu-id="7b064-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="7b064-151">支持的操作系统</span><span class="sxs-lookup"><span data-stu-id="7b064-151">Supported operating systems</span></span>

-   <span data-ttu-id="7b064-152">Retail Modern POS 是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。</span><span class="sxs-lookup"><span data-stu-id="7b064-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="7b064-153">只有 Windows 10 Pro, Enterprise 和 Enterprise Long Term Servicing Branch (LTSB) 版本才支持 Retail Modern POS。</span><span class="sxs-lookup"><span data-stu-id="7b064-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="7b064-154">最低系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-154">Minimum system requirements</span></span>

-   <span data-ttu-id="7b064-155">支持的最低分辨率为 1280 × 1024。</span><span class="sxs-lookup"><span data-stu-id="7b064-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="7b064-156">运行 Retail Modern POS 的计算机必须满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="7b064-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="7b064-157">必须配备以最低不低于 2 千兆赫兹 (GHz) 的速度运行的双核处理器。</span><span class="sxs-lookup"><span data-stu-id="7b064-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="7b064-158">必须配备最低 3 千兆字节 (GB) 的随机存取内存 (RAM)。</span><span class="sxs-lookup"><span data-stu-id="7b064-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="7b064-159">必须可以访问 Internet。</span><span class="sxs-lookup"><span data-stu-id="7b064-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="7b064-160">零售硬件工作站要求</span><span class="sxs-lookup"><span data-stu-id="7b064-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="7b064-161">支持的操作系统</span><span class="sxs-lookup"><span data-stu-id="7b064-161">Supported operating systems</span></span>

-   <span data-ttu-id="7b064-162">零售硬件工作站是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。</span><span class="sxs-lookup"><span data-stu-id="7b064-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="7b064-163">以下操作系统支持零售硬件工作站：</span><span class="sxs-lookup"><span data-stu-id="7b064-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="7b064-164">Windows 7 Professional、Enterprise 和 Ultimate 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="7b064-165">只有当在系统上手动安装 Internet Explorer 11 时，Windows 7 才受支持。</span><span class="sxs-lookup"><span data-stu-id="7b064-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="7b064-166">Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="7b064-167">Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="7b064-168">最低系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-168">Minimum system requirements</span></span>

<span data-ttu-id="7b064-169">计算机必须满足安装和使用以下项的所有系统要求：</span><span class="sxs-lookup"><span data-stu-id="7b064-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="7b064-170">Internet 信息服务 (IIS)</span><span class="sxs-lookup"><span data-stu-id="7b064-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="7b064-171">第三方硬件</span><span class="sxs-lookup"><span data-stu-id="7b064-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="7b064-172">零售商店扩展单位要求</span><span class="sxs-lookup"><span data-stu-id="7b064-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="7b064-173">支持的操作系统</span><span class="sxs-lookup"><span data-stu-id="7b064-173">Supported operating systems</span></span>

-   <span data-ttu-id="7b064-174">零售商店扩展单位是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。</span><span class="sxs-lookup"><span data-stu-id="7b064-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="7b064-175">以下操作系统支持零售商店扩展单位：</span><span class="sxs-lookup"><span data-stu-id="7b064-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="7b064-176">Windows 7 Professional、Enterprise 和 Ultimate 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="7b064-177">Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="7b064-178">Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="7b064-179">最低系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-179">Minimum system requirements</span></span>

-   <span data-ttu-id="7b064-180">4 GB 的 RAM</span><span class="sxs-lookup"><span data-stu-id="7b064-180">4 GB of RAM</span></span>
-   <span data-ttu-id="7b064-181">每个核心 1.6 GHz 的峰值 CPU 速度（至少两个核心。）</span><span class="sxs-lookup"><span data-stu-id="7b064-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="7b064-182">至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）</span><span class="sxs-lookup"><span data-stu-id="7b064-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="7b064-183">建议的系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-183">Recommended system requirements</span></span>

-   <span data-ttu-id="7b064-184">6 GB 的 RAM</span><span class="sxs-lookup"><span data-stu-id="7b064-184">6 GB of RAM</span></span>
-   <span data-ttu-id="7b064-185">每个核心 2.4 GHz i7（或等效）峰值 CPU 速度（建议四个核心。）</span><span class="sxs-lookup"><span data-stu-id="7b064-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="7b064-186">至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）</span><span class="sxs-lookup"><span data-stu-id="7b064-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="7b064-187">连接器需求</span><span class="sxs-lookup"><span data-stu-id="7b064-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="7b064-188">支持的操作系统</span><span class="sxs-lookup"><span data-stu-id="7b064-188">Supported operating systems</span></span>

-   <span data-ttu-id="7b064-189">Connector for Microsoft Dynamics AX 具有两个单独的安装程序，一个针对 Async Server Connector service，一个针对 Real-time service for Dynamics AX 2012 R3。</span><span class="sxs-lookup"><span data-stu-id="7b064-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="7b064-190">两个组件都是 32 位应用程序，但是在 x86 和 x64 架构上都可以运行。</span><span class="sxs-lookup"><span data-stu-id="7b064-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="7b064-191">两个组件都支持以下操作系统：</span><span class="sxs-lookup"><span data-stu-id="7b064-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="7b064-192">Windows 7 Professional、Enterprise 和 Ultimate 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="7b064-193">Windows 8.1 Update 1 Professional、Enterprise 和 Embedded 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="7b064-194">Windows 10 Pro、Enterprise 和 Enterprise LTSB 版本</span><span class="sxs-lookup"><span data-stu-id="7b064-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="7b064-195">Microsoft Windows Server 2012 R2 和 Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b064-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="7b064-196">最低系统要求</span><span class="sxs-lookup"><span data-stu-id="7b064-196">Minimum system requirements</span></span>
-   <span data-ttu-id="7b064-197">2 GB RAM（建议 4 GB RAM）。</span><span class="sxs-lookup"><span data-stu-id="7b064-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="7b064-198">每个核心 1.6 GHz 的峰值 CPU 速度（至少两个核心。）</span><span class="sxs-lookup"><span data-stu-id="7b064-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="7b064-199">至少 10 GB 的可用空间（渠道数据库肯需要大量空间。）</span><span class="sxs-lookup"><span data-stu-id="7b064-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="7b064-200">本地虚拟机上的部署要求</span><span class="sxs-lookup"><span data-stu-id="7b064-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="7b064-201">有关本地虚拟机 (VM) 上的部署要求的信息，请参阅[本地运行虚拟机](../dev-tools/access-instances.md)。</span><span class="sxs-lookup"><span data-stu-id="7b064-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="7b064-202">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b064-202">See also</span></span>

[<span data-ttu-id="7b064-203">获取 Dynamics 365 for Finance and Operations Enterprise Edition 的评估副本</span><span class="sxs-lookup"><span data-stu-id="7b064-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

