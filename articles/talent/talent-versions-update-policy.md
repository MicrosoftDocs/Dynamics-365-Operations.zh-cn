---
title: Talent 系统要求
description: 此主题列出了 Dynamics 365 Talent 的要求。
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0bd7d7051dd01834f306e165af55d740192b99e0
ms.sourcegitcommit: caeb24027831efccbc316ff8e7f9e62b42010d65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/19/2019
ms.locfileid: "2818471"
---
# <a name="talent-system-requirements"></a><span data-ttu-id="9076b-103">Talent 系统要求</span><span class="sxs-lookup"><span data-stu-id="9076b-103">Talent system requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9076b-104">本主题介绍 Microsoft Dynamics 365 Talent（包括 Attract、Onboard 和 Core HR）的要求。</span><span class="sxs-lookup"><span data-stu-id="9076b-104">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="9076b-105">还概述支持 Talent 的国家和地区，以及有关 Talent 数据的语言和本地化的信息。</span><span class="sxs-lookup"><span data-stu-id="9076b-105">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="9076b-106">此外，本主题还提供 Talent 的更新策略。</span><span class="sxs-lookup"><span data-stu-id="9076b-106">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="9076b-107">支持的 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="9076b-107">Supported web browsers</span></span>

<span data-ttu-id="9076b-108">Microsoft Dynamics 365 Talent 可在指定操作系统上运行的以下任一 Web 浏览器中运行：</span><span class="sxs-lookup"><span data-stu-id="9076b-108">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="9076b-109">Windows 10 上的 Microsoft Edge（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="9076b-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="9076b-110">Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="9076b-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="9076b-111">Google Chrome（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="9076b-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="9076b-112">Apple Safari（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="9076b-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="9076b-113">要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。</span><span class="sxs-lookup"><span data-stu-id="9076b-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="9076b-114">若要捕获从任务录制器生成的图像并插入到 Microsoft Word 文档中，必须安装 Chrome 扩展。</span><span class="sxs-lookup"><span data-stu-id="9076b-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="9076b-115">Workflow Editor 作为 ClickOnce 应用程序启动。</span><span class="sxs-lookup"><span data-stu-id="9076b-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="9076b-116">只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。</span><span class="sxs-lookup"><span data-stu-id="9076b-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="9076b-117">Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。</span><span class="sxs-lookup"><span data-stu-id="9076b-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="9076b-118">若要预览 PDF 文件，我们建议您使用现代浏览器，如 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）。</span><span class="sxs-lookup"><span data-stu-id="9076b-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="9076b-119">网络要求</span><span class="sxs-lookup"><span data-stu-id="9076b-119">Network requirements</span></span>
> * <span data-ttu-id="9076b-120">Dynamics 365 Talent 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。</span><span class="sxs-lookup"><span data-stu-id="9076b-120">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="9076b-121">该延迟是从浏览器客户端到托管 Talent 的 Microsoft Azure 数据中心的延迟。</span><span class="sxs-lookup"><span data-stu-id="9076b-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="9076b-122">建议在 [www.azurespeed.com](https://www.azurespeed.com "Azure 延迟测试") 测试网络延迟。</span><span class="sxs-lookup"><span data-stu-id="9076b-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="9076b-123">Talent 带宽要求取决于您的方案。</span><span class="sxs-lookup"><span data-stu-id="9076b-123">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="9076b-124">大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。</span><span class="sxs-lookup"><span data-stu-id="9076b-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="9076b-125">请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。</span><span class="sxs-lookup"><span data-stu-id="9076b-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="9076b-126">给定位置的并行使用很难计算。</span><span class="sxs-lookup"><span data-stu-id="9076b-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="9076b-127">对于注重带宽要求的客户，请使用 Talent 的试用版本。</span><span class="sxs-lookup"><span data-stu-id="9076b-127">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="9076b-128">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="9076b-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="9076b-129">若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。</span><span class="sxs-lookup"><span data-stu-id="9076b-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="9076b-130">有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 集成疑难解答")。</span><span class="sxs-lookup"><span data-stu-id="9076b-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="9076b-131">若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="9076b-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="9076b-132">地区可用性、语言和本地化</span><span class="sxs-lookup"><span data-stu-id="9076b-132">Regional availability, languages, and localization</span></span>

<span data-ttu-id="9076b-133">可在 [Microsoft Dynamics 365 全球可用性](https://docs.microsoft.com/dynamics365/get-started/availability)中下载 Talent 支持的国家、地区和语言的 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="9076b-133">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="9076b-134">由于用户界面已本地化为其他语言，所以所有用户数据使用输入语言存储。</span><span class="sxs-lookup"><span data-stu-id="9076b-134">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="9076b-135">可以使用其他语言创建电子邮件和模板，但是目前日程安排信息之类数据仅提供英文版。</span><span class="sxs-lookup"><span data-stu-id="9076b-135">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="9076b-136">如果您是开发人员，并且有效期创建国家或地区特定的自定义项，或者有兴趣为 Microsoft 目前尚未支持的国家或地区创建解决方案，请参阅[全球化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)。</span><span class="sxs-lookup"><span data-stu-id="9076b-136">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

