---
title: "POS 硬件外围设备"
description: "Retail Modern 销售点 (POS) 和 Cloud POS 可以使用一系列广泛的 POS 硬件外设，具有多个界面和部署选项以满足零售商的各种业务场景。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 17738e794f18fddc7320b1b40ef55376fba0de24
ms.contentlocale: zh-cn
ms.lasthandoff: 08/30/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="2cc63-103">POS 硬件外围设备</span><span class="sxs-lookup"><span data-stu-id="2cc63-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2cc63-104">Retail Modern 销售点 (POS) 和 Cloud POS 可以使用一系列广泛的 POS 硬件外设，具有多个界面和部署选项以满足零售商的各种业务场景。</span><span class="sxs-lookup"><span data-stu-id="2cc63-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="2cc63-105">为了支持在制造和模型中提供最广泛的设备选择，POS 使用标准界面，例如 OLE for Retail POS (OPOS)、Windows 设备驱动程序和 Windows 服务点应用程序接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="2cc63-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="2cc63-106">通常情况下，如果提供了适当的驱动程序，POS 将在提供的这些设备上工作。</span><span class="sxs-lookup"><span data-stu-id="2cc63-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="2cc63-107">但是，由于每个制造商和软件开发商实施这些标准的方式不一样，因为受支持的功能或行为通常存在差异。</span><span class="sxs-lookup"><span data-stu-id="2cc63-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="2cc63-108">下表列出了 Microsoft 已经内部测试过的每一类设备模型。</span><span class="sxs-lookup"><span data-stu-id="2cc63-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="2cc63-109">**OPOS 设备**</span><span class="sxs-lookup"><span data-stu-id="2cc63-109">**OPOS devices**</span></span>

-   <span data-ttu-id="2cc63-110">条码 – 摩托罗拉 DS9208</span><span class="sxs-lookup"><span data-stu-id="2cc63-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="2cc63-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="2cc63-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="2cc63-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="2cc63-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="2cc63-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="2cc63-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="2cc63-114">Signature pad – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="2cc63-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="2cc63-115">打印机 – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="2cc63-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="2cc63-116">银箱 – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="2cc63-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="2cc63-117">秤 – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="2cc63-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="2cc63-118">**键盘 wedge MSR**</span><span class="sxs-lookup"><span data-stu-id="2cc63-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="2cc63-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="2cc63-119">Magtek USB</span></span>

<span data-ttu-id="2cc63-120">**付款终端**</span><span class="sxs-lookup"><span data-stu-id="2cc63-120">**Payment terminal**</span></span>

-   <span data-ttu-id="2cc63-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="2cc63-121">Equinox L3500</span></span>
-   <span data-ttu-id="2cc63-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="2cc63-122">Verifone MX925</span></span>

<span data-ttu-id="2cc63-123">**网络设备**</span><span class="sxs-lookup"><span data-stu-id="2cc63-123">**Network devices**</span></span>

-   <span data-ttu-id="2cc63-124">打印机 – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="2cc63-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="2cc63-125">银箱 – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="2cc63-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="2cc63-126">付款终端 – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="2cc63-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="2cc63-127">**MPOS 仅直接 IPC**</span><span class="sxs-lookup"><span data-stu-id="2cc63-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="2cc63-128">条码 – 霍尼韦尔 1900，HP LS2208</span><span class="sxs-lookup"><span data-stu-id="2cc63-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="2cc63-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="2cc63-129">MSR – Magtek PN - 21073075</span></span>





