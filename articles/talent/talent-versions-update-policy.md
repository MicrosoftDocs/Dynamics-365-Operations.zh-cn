---
title: Talent 系统要求和更新策略
description: 此主题列出了 Dynamics 365 for Talent 的要求。 另外，还概述了更新策略。
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
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
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741767"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="6354c-104">Talent 系统要求和更新策略</span><span class="sxs-lookup"><span data-stu-id="6354c-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6354c-105">本主题介绍 Microsoft Dynamics 365 for Talent（包括 Attract、Onboard 和 Core HR）的要求。</span><span class="sxs-lookup"><span data-stu-id="6354c-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="6354c-106">还概述支持 Talent 的国家和地区，以及有关 Talent 数据的语言和本地化的信息。</span><span class="sxs-lookup"><span data-stu-id="6354c-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="6354c-107">此外，本主题还提供 Talent 的更新策略。</span><span class="sxs-lookup"><span data-stu-id="6354c-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="6354c-108">支持的 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="6354c-108">Supported web browsers</span></span>

<span data-ttu-id="6354c-109">Microsoft Dynamics 365 for Talent Web 应用程序可在指定操作系统上运行的以下任一 Web 浏览器中运行：</span><span class="sxs-lookup"><span data-stu-id="6354c-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="6354c-110">Windows 10 上的 Microsoft Edge（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="6354c-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="6354c-111">Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="6354c-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="6354c-112">Google Chrome（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="6354c-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="6354c-113">Apple Safari（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="6354c-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="6354c-114">要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。</span><span class="sxs-lookup"><span data-stu-id="6354c-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="6354c-115">若要捕获从任务录制器生成的图像并插入到 Microsoft Word 文档中，必须安装 Chrome 扩展。</span><span class="sxs-lookup"><span data-stu-id="6354c-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="6354c-116">Workflow Editor 作为 ClickOnce 应用程序启动。</span><span class="sxs-lookup"><span data-stu-id="6354c-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="6354c-117">只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。</span><span class="sxs-lookup"><span data-stu-id="6354c-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="6354c-118">Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。</span><span class="sxs-lookup"><span data-stu-id="6354c-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="6354c-119">若要预览 PDF 文件，我们建议您使用现代浏览器，如 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）。</span><span class="sxs-lookup"><span data-stu-id="6354c-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="6354c-120">网络要求</span><span class="sxs-lookup"><span data-stu-id="6354c-120">Network requirements</span></span>
> * <span data-ttu-id="6354c-121">Dynamics 365 for Talent 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。</span><span class="sxs-lookup"><span data-stu-id="6354c-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="6354c-122">该延迟是从浏览器客户端到托管 Dynamics 365 for Talent 的 Microsoft Azure 数据中心的延迟。</span><span class="sxs-lookup"><span data-stu-id="6354c-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="6354c-123">建议在 [www.azurespeed.com](https://www.azurespeed.com "延迟测试") 测试网络延迟。</span><span class="sxs-lookup"><span data-stu-id="6354c-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="6354c-124">Dynamics 365 for Talent 带宽要求取决于您的方案。</span><span class="sxs-lookup"><span data-stu-id="6354c-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="6354c-125">大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。</span><span class="sxs-lookup"><span data-stu-id="6354c-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="6354c-126">请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。</span><span class="sxs-lookup"><span data-stu-id="6354c-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="6354c-127">给定位置的并行使用很难计算。</span><span class="sxs-lookup"><span data-stu-id="6354c-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="6354c-128">对于注重带宽要求的客户，请使用 Dynamics 365 for Talent 的试用版本。</span><span class="sxs-lookup"><span data-stu-id="6354c-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="6354c-129">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="6354c-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="6354c-130">若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。</span><span class="sxs-lookup"><span data-stu-id="6354c-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="6354c-131">有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 集成疑难解答")。</span><span class="sxs-lookup"><span data-stu-id="6354c-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="6354c-132">若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="6354c-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="6354c-133">地区可用性、语言和本地化</span><span class="sxs-lookup"><span data-stu-id="6354c-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="6354c-134">可在 [Microsoft Dynamics 365 全球可用性](https://docs.microsoft.com/dynamics365/get-started/availability)中下载 Talent 支持的国家、地区和语言的 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="6354c-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="6354c-135">由于用户界面已本地化为其他语言，所以所有用户数据使用输入语言存储。</span><span class="sxs-lookup"><span data-stu-id="6354c-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="6354c-136">可以使用其他语言创建电子邮件和模板，但是目前日程安排信息之类数据仅提供英文版。</span><span class="sxs-lookup"><span data-stu-id="6354c-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="6354c-137">如果您是开发人员，并且有效期创建国家或地区特定的自定义项，或者有兴趣为 Microsoft 目前尚未支持的国家或地区创建解决方案，请参阅[全球化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)。</span><span class="sxs-lookup"><span data-stu-id="6354c-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="6354c-138">更新策略</span><span class="sxs-lookup"><span data-stu-id="6354c-138">Update policy</span></span>

<span data-ttu-id="6354c-139">Microsoft Dynamics 365 for Talent 以云产品的形式提供。</span><span class="sxs-lookup"><span data-stu-id="6354c-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="6354c-140">Microsoft 将持续提供并自动应用对 Dynamics 365 for Talent 的更新。</span><span class="sxs-lookup"><span data-stu-id="6354c-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="6354c-141">更新定期针对所有环境发布。</span><span class="sxs-lookup"><span data-stu-id="6354c-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="6354c-142">对 Dynamics 365 for Talent 的支持根据 [Microsoft 支持生命周期策略](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft 支持生命周期")提供，该策略为产品支持可用性提供一致且可预测的指南。</span><span class="sxs-lookup"><span data-stu-id="6354c-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
