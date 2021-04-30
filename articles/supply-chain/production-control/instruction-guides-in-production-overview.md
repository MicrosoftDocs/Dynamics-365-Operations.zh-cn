---
title: 为生产中的工作人员提供混合现实指南
description: 本主题说明了如何将 Microsoft Dynamics 365 Supply Chain Management 中的生产管理模块与 Dynamics 365 Guides 集成。
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 15595c46f9d6ff91f6fd618859e9f059ae88bd78
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910081"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="77e2d-103">为生产中的工作人员提供混合现实指南</span><span class="sxs-lookup"><span data-stu-id="77e2d-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="77e2d-104">生产流程中的工作人员将从在其工作范围内在适当时间提供的相关说明中受益。</span><span class="sxs-lookup"><span data-stu-id="77e2d-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="77e2d-105">*说明* 适用于多个工作领域，包括：装配、服务、工序、认证和安全。</span><span class="sxs-lookup"><span data-stu-id="77e2d-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="77e2d-106">在所有这些核心业务功能中，持续进行的培训说明可以帮助员工实现更多目标，更好地进行工作。</span><span class="sxs-lookup"><span data-stu-id="77e2d-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="77e2d-107">简介</span><span class="sxs-lookup"><span data-stu-id="77e2d-107">Introduction</span></span>

<span data-ttu-id="77e2d-108">您可以通过不同的方式提供说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="77e2d-109">随附开箱即用的 [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) 的一个有效系统。</span><span class="sxs-lookup"><span data-stu-id="77e2d-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="77e2d-110">Dynamics 365 Guides 可以帮助您的员工通过实践进行学习。</span><span class="sxs-lookup"><span data-stu-id="77e2d-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="77e2d-111">您可以通过分步说明来定义标准化流程，这些分步说明将指导您的员工使用他们所需的工具和零件，并向员工展示如何在实际工作中使用这些工具。</span><span class="sxs-lookup"><span data-stu-id="77e2d-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="77e2d-112">您可以将 Guides 附加到生产控制的各个方面，包括：</span><span class="sxs-lookup"><span data-stu-id="77e2d-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="77e2d-113">资源</span><span class="sxs-lookup"><span data-stu-id="77e2d-113">Resources</span></span>](#resources)
- [<span data-ttu-id="77e2d-114">资源组</span><span class="sxs-lookup"><span data-stu-id="77e2d-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="77e2d-115">已发布产品</span><span class="sxs-lookup"><span data-stu-id="77e2d-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="77e2d-116">配方</span><span class="sxs-lookup"><span data-stu-id="77e2d-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="77e2d-117">配方版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="77e2d-118">物料清单 (BOM)</span><span class="sxs-lookup"><span data-stu-id="77e2d-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="77e2d-119">物料清单版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="77e2d-120">运输路径</span><span class="sxs-lookup"><span data-stu-id="77e2d-120">Routes</span></span>](#routes)
- [<span data-ttu-id="77e2d-121">工艺路线版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="77e2d-122">工艺路线工序关系</span><span class="sxs-lookup"><span data-stu-id="77e2d-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="77e2d-123">您也可以将 Guides 与资产管理附加在一起。</span><span class="sxs-lookup"><span data-stu-id="77e2d-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="77e2d-124">有关该选项的详细信息，请参阅[将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成](../asset-management/asset-management-guides-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="77e2d-125">当一线工作人员通过 Supply Chain Management 在车间中选择作业时，工作人员可以在作业卡上看到[相关指南](#logic)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="77e2d-126">当工作人员选择一个特定指南时，该指南的 QR 码将显示在屏幕上。</span><span class="sxs-lookup"><span data-stu-id="77e2d-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="77e2d-127">然后，工作人员使用他们的 HoloLens 扫描 QR 码，这会启动 Guides 并显示所需的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="77e2d-128">以下小节介绍了一些选定方案，在这些方案中，各个行业的公司都可以看到使用 Guides 显示制造说明时的最大价值。</span><span class="sxs-lookup"><span data-stu-id="77e2d-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="77e2d-129">程序集</span><span class="sxs-lookup"><span data-stu-id="77e2d-129">Assembly</span></span>

<span data-ttu-id="77e2d-130">![在装配任务中使用指南](media/instruction-guides-hero-assembly.png "在服务任务中使用指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="77e2d-131">装配操作说明向工作人员介绍了他们所需的工具和零件，以及如何在实际工作中使用它们。</span><span class="sxs-lookup"><span data-stu-id="77e2d-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="77e2d-132">例如，生产经理可以为[生产工艺路线](routes-operations.md)、[工序关系](routes-operations.md#operation-relations)或[物料清单](bill-of-material-bom.md)创建和分配指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="77e2d-133">工作人员将在车间中找到有关相应操作经验的相关说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="77e2d-134">服务</span><span class="sxs-lookup"><span data-stu-id="77e2d-134">Service</span></span>

<span data-ttu-id="77e2d-135">![在服务任务中使用指南](media/instruction-guides-hero-service.png "在服务任务中使用指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="77e2d-136">在作业现场为技术人员提供指导说明，从而无需计划其他访问。</span><span class="sxs-lookup"><span data-stu-id="77e2d-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="77e2d-137">例如，服务经理可以向完成质量评估例程的特定[产品](../../commerce/product.md)分配指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="77e2d-138">质量</span><span class="sxs-lookup"><span data-stu-id="77e2d-138">Quality</span></span>

<span data-ttu-id="77e2d-139">![在质量保证任务中使用指南](media/instruction-guides-hero-quality.png "在质量保证任务中使用指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="77e2d-140">推出新流程并通过将员工的知识变成可重复的工具来确保提高一致性。</span><span class="sxs-lookup"><span data-stu-id="77e2d-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="77e2d-141">例如，质量保证经理可以向完成质量评估例程的[产品](../../commerce/product.md)分配指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="77e2d-142">认证</span><span class="sxs-lookup"><span data-stu-id="77e2d-142">Certifications</span></span>

<span data-ttu-id="77e2d-143">![在与认证相关的任务中使用指南](media/instruction-guides-hero-certification.png "在与认证相关的任务中使用指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="77e2d-144">通过快速确定谁需要帮助以及哪里需要帮助，确保每个员工都符合高标准。</span><span class="sxs-lookup"><span data-stu-id="77e2d-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="77e2d-145">安全</span><span class="sxs-lookup"><span data-stu-id="77e2d-145">Safety</span></span>

<span data-ttu-id="77e2d-146">![在工作安全说明中使用指南](media/instruction-guides-hero-safety.png "在工作安全说明中使用指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="77e2d-147">提供在尝试进入物理环境之前以虚拟方式完成危险过程的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="77e2d-148">通过混合现实方法，工作人员可以通过虚拟方式体验危险过程。</span><span class="sxs-lookup"><span data-stu-id="77e2d-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="77e2d-149">生产经理可以通过向[产品物料](../../commerce/product.md)、[工艺路线](routes-operations.md)和[工序](routes-operations.md#operation-relations)分配说明来提供有关危险物料处理的专门处理说明或专门处理过程。</span><span class="sxs-lookup"><span data-stu-id="77e2d-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="77e2d-150">开始使用说明和 Guides</span><span class="sxs-lookup"><span data-stu-id="77e2d-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="77e2d-151">为了在生产过程中启用说明，Supply Chain Management 提供了与 Dynamics 365 Guides 的开箱即用集成。</span><span class="sxs-lookup"><span data-stu-id="77e2d-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="77e2d-152">需要 Guides 的许可和安装的应用程序实例，才能为生产资产和工作构建、维护和分配混合现实说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="77e2d-153">先决条件</span><span class="sxs-lookup"><span data-stu-id="77e2d-153">Prerequisites</span></span>

<span data-ttu-id="77e2d-154">若要使用此功能，您的系统必须包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="77e2d-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="77e2d-155">Dynamics 365 Supply Chain Management 版本 10.0.15 或更高版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="77e2d-156">Supply Chain Management 应用的[双写入](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-156">[Dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="77e2d-157">[Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 版本 400.0.1.48 或更高版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-157">[Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="77e2d-158">开启功能</span><span class="sxs-lookup"><span data-stu-id="77e2d-158">Turn on the feature</span></span>

<span data-ttu-id="77e2d-159">若要使该功能在您的系统上可用，必须启用其 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="77e2d-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="77e2d-160">您只需要执行一次。</span><span class="sxs-lookup"><span data-stu-id="77e2d-160">You only need to do this once.</span></span> <span data-ttu-id="77e2d-161">为此，管理员必须执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="77e2d-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="77e2d-162">将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="77e2d-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="77e2d-163">转到 **系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="77e2d-164">展开 **混合现实** 部分，然后选择 **混合现实指南** 复选框。</span><span class="sxs-lookup"><span data-stu-id="77e2d-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="77e2d-165">展开 **生产管理** 部分，然后选择 **生产说明** 复选框。</span><span class="sxs-lookup"><span data-stu-id="77e2d-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="77e2d-166">关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="77e2d-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="77e2d-167">配置指南在车间中的显示方式</span><span class="sxs-lookup"><span data-stu-id="77e2d-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="77e2d-168">若要配置指南在车间中的显示方式，请转到 **混合现实 \> Dynamics 365 Guides \> 配置指南集成**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="77e2d-169">![为制造配置指南集成](media/instruction-guides-configure-integration.png "为制造配置指南集成")</span><span class="sxs-lookup"><span data-stu-id="77e2d-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="77e2d-170">设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="77e2d-170">Set the following fields:</span></span>

- <span data-ttu-id="77e2d-171">**Microsoft Dataverse URL** - 指定在其中创建指南的 Microsoft Dataverse 环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="77e2d-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="77e2d-172">格式为“contoso.crm4.dynamics.com”，其中 URL 的第一部分通常以您的组织（例如“contoso.”）命名，第二部分特定于您环境的数据区域（例如“crm4.”），最后一部分是域（例如“dynamics.com”）。</span><span class="sxs-lookup"><span data-stu-id="77e2d-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="77e2d-173">找到正确 URL 的一种方法是转到 [home.dynamics.com](https://home.dynamics.com/)，然后打开 Guides 应用。</span><span class="sxs-lookup"><span data-stu-id="77e2d-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="77e2d-174">打开 Guides 后，您将在浏览器的地址栏中看到 URL（仅使用基本 URL，它应该类似于前面的示例）。</span><span class="sxs-lookup"><span data-stu-id="77e2d-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="77e2d-175">此值用于构成指南的地址，并将编码为 QR 码。</span><span class="sxs-lookup"><span data-stu-id="77e2d-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="77e2d-176">**QR 码大小** - 设置呈现的 QR 码的大小。</span><span class="sxs-lookup"><span data-stu-id="77e2d-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="77e2d-177">我们建议选择一个将填充大部分显示屏幕而不是超过显示屏幕的大小。</span><span class="sxs-lookup"><span data-stu-id="77e2d-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="77e2d-178">通常，*15* 是一个适合的值。</span><span class="sxs-lookup"><span data-stu-id="77e2d-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="77e2d-179">**QR 码错误纠正级别** - 设置 QR 码的粒度。</span><span class="sxs-lookup"><span data-stu-id="77e2d-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="77e2d-180">更高的粒度可以帮助提高代码的可靠性，但是您的 **QR 码大小** 必须足够大以支持所选纠正级别所需的详细级别。</span><span class="sxs-lookup"><span data-stu-id="77e2d-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="77e2d-181">对于您的显示器过大的 QR 码大小将花费更长时间呈现，将其缩小以适应您的显示器。</span><span class="sxs-lookup"><span data-stu-id="77e2d-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="77e2d-182">这些没有好处。</span><span class="sxs-lookup"><span data-stu-id="77e2d-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="77e2d-183">QR 码太小可能会削弱 HoloLens 在某些环境中正确读取代码的能力。</span><span class="sxs-lookup"><span data-stu-id="77e2d-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="77e2d-184">我们建议您测试为 HoloLens 用户显示 QR 码的每台设备的设置。</span><span class="sxs-lookup"><span data-stu-id="77e2d-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="77e2d-185">选择在车间环境中提供足够的可读性的设置。</span><span class="sxs-lookup"><span data-stu-id="77e2d-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="77e2d-186">获取所有指南分配的概述</span><span class="sxs-lookup"><span data-stu-id="77e2d-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="77e2d-187">使用 **所有指南** 页面以查看组织中所有可用指南的列表以及生产流程和资源的所有分配。</span><span class="sxs-lookup"><span data-stu-id="77e2d-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="77e2d-188">若要打开它，请转到 **混合现实 \> 指南 \> 所有指南**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="77e2d-189">顶部的列表显示了所有可用指南，您可以在此处使用该字段筛选列表。</span><span class="sxs-lookup"><span data-stu-id="77e2d-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="77e2d-190">底部的列表显示了所有指南分配，并提供了用于管理它们的工具栏。</span><span class="sxs-lookup"><span data-stu-id="77e2d-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="77e2d-191">![管理指南](media/instruction-guides-allguides.png "管理指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="77e2d-192">以下部分描述了可以将指南分配到的对象类型。</span><span class="sxs-lookup"><span data-stu-id="77e2d-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="77e2d-193">每个分配的指南都提供了将自动附加到各个生产作业的说明，这些说明将在车间中提供。</span><span class="sxs-lookup"><span data-stu-id="77e2d-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="77e2d-194">将指南关联到资源</span><span class="sxs-lookup"><span data-stu-id="77e2d-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="77e2d-195">将指南添加到[资源](operations-resources.md)以在相关的生产作业中提供指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="77e2d-196">使用资源的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-196">Typical scenario using resources</span></span>

<span data-ttu-id="77e2d-197">例如，您可以将具有常规机器安全性或处理说明的指南附加到机器类型的资源。</span><span class="sxs-lookup"><span data-stu-id="77e2d-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="77e2d-198">然后，该指南将适用于在机器上执行的每个作业。</span><span class="sxs-lookup"><span data-stu-id="77e2d-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="77e2d-199">将指南添加到资源</span><span class="sxs-lookup"><span data-stu-id="77e2d-199">Add a Guide to a resource</span></span>

<span data-ttu-id="77e2d-200">若要将指南添加到资源：</span><span class="sxs-lookup"><span data-stu-id="77e2d-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="77e2d-201">转到 **生产控制 \> 设置 \> 资源 \> 资源**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="77e2d-202">在列表窗格中，选择要为其分配指南的资源。</span><span class="sxs-lookup"><span data-stu-id="77e2d-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-203">展开 **关联的指南** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="77e2d-204">从 **关联的指南** 工具栏中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="77e2d-205">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="77e2d-206">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="77e2d-207">如果您有大量指南，可以筛选列表以查找所需的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="77e2d-208">![管理指南](media/instruction-guides-allguides.png "管理指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="77e2d-209">将指南关联到资源组</span><span class="sxs-lookup"><span data-stu-id="77e2d-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="77e2d-210">如果您使用资源组管理机器、生产线或工作单元的组，您可以向[资源组](tasks/define-discrete-manufacturing-resource-group.md)添加指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="77e2d-211">使用资源组的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="77e2d-212">**示例 1：** 您已经为同一型号的多台机器定义了一个资源组。</span><span class="sxs-lookup"><span data-stu-id="77e2d-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="77e2d-213">不是将机器型号的相关处理说明指南分配给每个相关资源，而是将该指南分配给反映该机器型号的资源组。</span><span class="sxs-lookup"><span data-stu-id="77e2d-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="77e2d-214">**示例 2：** 您已经为包含不同机器的工作单元定义了一个资源组，并且拥有提供有关如何维护工作单元的一般说明的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="77e2d-215">该指南适用于此工作单元中的任何生产活动。</span><span class="sxs-lookup"><span data-stu-id="77e2d-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="77e2d-216">将指南添加到资源组</span><span class="sxs-lookup"><span data-stu-id="77e2d-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="77e2d-217">若要将指南添加到资源组：</span><span class="sxs-lookup"><span data-stu-id="77e2d-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="77e2d-218">转到 **生产控制 \> 设置 \> 资源 \> 资源组**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="77e2d-219">在列表窗格中，选择要为其分配指南的资源组。</span><span class="sxs-lookup"><span data-stu-id="77e2d-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-220">展开 **关联的指南** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="77e2d-221">从 **关联的指南** 工具栏中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="77e2d-222">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="77e2d-223">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="77e2d-224">如果您有大量指南，可以筛选列表以查找所需的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="77e2d-225">![将指南添加到资源组](media/instruction-guides-resourcegroup.png "将指南添加到资源组")</span><span class="sxs-lookup"><span data-stu-id="77e2d-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="77e2d-226">将指南关联到已发布产品</span><span class="sxs-lookup"><span data-stu-id="77e2d-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="77e2d-227">您可以将指南添加到任何[已发布产品](../pim/tasks/create-released-product-single-company.md)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="77e2d-228">使用已发布产品的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-228">Typical scenario using released products</span></span>

<span data-ttu-id="77e2d-229">产品级指南可帮助车间工作人员获得与运营或处理特定分已发布产品或物料相关的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="77e2d-230">将指南添加到已发布产品</span><span class="sxs-lookup"><span data-stu-id="77e2d-230">Add a Guide to a released product</span></span>

<span data-ttu-id="77e2d-231">若要将指南添加到已发布产品：</span><span class="sxs-lookup"><span data-stu-id="77e2d-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="77e2d-232">转到 **生产信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="77e2d-233">打开要为其分配指南的产品。</span><span class="sxs-lookup"><span data-stu-id="77e2d-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-234">在“操作”窗格上，打开 **工程师** 选项卡，然后从 **查看** 组中，选择 **关联的指南**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="77e2d-235">将针对选定产品打开 **关联的指南** 页面。</span><span class="sxs-lookup"><span data-stu-id="77e2d-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="77e2d-236">在“操作”窗格上，选择 **添加** 以向网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="77e2d-237">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-238">![将指南添加到已发布产品](media/instruction-guides-ReleasedProduct-AddGuides.png "将指南添加到已发布产品")</span><span class="sxs-lookup"><span data-stu-id="77e2d-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="77e2d-239">将指南关联到配方</span><span class="sxs-lookup"><span data-stu-id="77e2d-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="77e2d-240">您可以将指南添加到任何[配方](bill-of-material-bom.md#formulas-co-products-and-by-products)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="77e2d-241">使用配方的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="77e2d-242">配方级指南为车间工作人员提供与配方或基本配方相关的指导处理说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="77e2d-243">指南也可以分配到配方的版本。</span><span class="sxs-lookup"><span data-stu-id="77e2d-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="77e2d-244">您可以根据工艺路线、工艺路线版本或工艺路线工序关系的配方分配与生产流程相关的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="77e2d-245">指南当前无法附加到单独的配方行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="77e2d-246">将指南添加到配方</span><span class="sxs-lookup"><span data-stu-id="77e2d-246">Add a Guide to a formula</span></span>

<span data-ttu-id="77e2d-247">若要将指南添加到配方：</span><span class="sxs-lookup"><span data-stu-id="77e2d-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="77e2d-248">转到 **生产信息管理 \> 物料清单和配方 \> 配方**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="77e2d-249">打开要为其分配指南的配方。</span><span class="sxs-lookup"><span data-stu-id="77e2d-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-250">打开顶部快速选项卡上方的 **标题** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="77e2d-251">展开 **关联的指南** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="77e2d-252">从 **关联的指南** 工具栏中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="77e2d-253">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="77e2d-254">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-255">![将指南添加到配方](media/instruction-guides-Formula.png "将指南添加到配方")</span><span class="sxs-lookup"><span data-stu-id="77e2d-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="77e2d-256">将指南关联到配方版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="77e2d-257">您可以将指南添加到任何[配方版本](bill-of-material-bom.md#bom-and-formula-versions)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="77e2d-258">使用配方版本的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="77e2d-259">附加到单独配方版本的指南为车间工作人员提供了演示该版本配方的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="77e2d-260">您可以根据工艺路线、工艺路线版本或工艺路线工序关系的此配方版本分配与生产流程相关的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="77e2d-261">指南当前无法附加到单独的配方行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="77e2d-262">将指南添加到配方版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="77e2d-263">若要将指南添加到配方版本：</span><span class="sxs-lookup"><span data-stu-id="77e2d-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="77e2d-264">转到 **生产信息管理 \> 物料清单和配方 \> 配方**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="77e2d-265">打开包含要为其分配指南的版本的配方。</span><span class="sxs-lookup"><span data-stu-id="77e2d-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-266">打开顶部快速选项卡上方的 **标题** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="77e2d-267">在 **配方版本** 快速选项卡上，选择要为其分配指南的版本。</span><span class="sxs-lookup"><span data-stu-id="77e2d-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-268">在 **配方版本** 工具栏上，选择 **关联的指南**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="77e2d-269">![打开与所选配方版本关联的指南](media/instruction-guides-FormulaVersion.png "打开与所选配方版本关联的指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="77e2d-270">将针对配方版本打开 **关联的指南** 页面。</span><span class="sxs-lookup"><span data-stu-id="77e2d-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="77e2d-271">在“操作”窗格上，选择 **添加** 以向网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="77e2d-272">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-273">![将指南添加到配方版本](media/instruction-guides-FormulaVersionAddGuide.png "将指南添加到配方版本")</span><span class="sxs-lookup"><span data-stu-id="77e2d-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="77e2d-274">将指南关联到物料清单</span><span class="sxs-lookup"><span data-stu-id="77e2d-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="77e2d-275">您可以将指南添加到任何[物料清单](bill-of-material-bom.md) (BOM)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="77e2d-276">使用物料清单的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="77e2d-277">附加到物料清单的指南为车间工作人员提供了解释如何通过物料清单准备和处理物料的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="77e2d-278">指南也可以分配到物料清单的版本。</span><span class="sxs-lookup"><span data-stu-id="77e2d-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="77e2d-279">指南当前无法附加到单独的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="77e2d-280">将指南添加到物料清单</span><span class="sxs-lookup"><span data-stu-id="77e2d-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="77e2d-281">若要将指南添加到物料清单：</span><span class="sxs-lookup"><span data-stu-id="77e2d-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="77e2d-282">转到 **生产信息管理 \> 物料清单和配方 \> 物料清单**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="77e2d-283">打开要为其分配指南的物料清单。</span><span class="sxs-lookup"><span data-stu-id="77e2d-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-284">打开顶部快速选项卡上方的 **标题** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="77e2d-285">展开 **关联的指南** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="77e2d-286">从 **关联的指南** 工具栏中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="77e2d-287">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="77e2d-288">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-289">![将指南添加到物料清单](media/instruction-guides-BOM.png "将指南添加到物料清单")</span><span class="sxs-lookup"><span data-stu-id="77e2d-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="77e2d-290">将指南关联到物料清单版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="77e2d-291">您可以将指南添加到任何[物料清单版本](bill-of-material-bom.md#bom-and-formula-versions)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="77e2d-292">使用物料清单版本的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="77e2d-293">附加到单独物料清单版本的指南为车间工作人员提供解释了如何为不同于通用物料清单或其他版本的物料清单版本准备和处理物料的说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="77e2d-294">指南当前无法附加到单独的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="77e2d-295">将指南添加到物料清单版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="77e2d-296">若要将指南添加到物料清单版本：</span><span class="sxs-lookup"><span data-stu-id="77e2d-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="77e2d-297">转到 **生产信息管理 \> 物料清单和配方 \> 物料清单**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="77e2d-298">打开包含要为其分配指南的版本的物料清单。</span><span class="sxs-lookup"><span data-stu-id="77e2d-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-299">打开顶部快速选项卡上方的 **标题** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="77e2d-300">在 **物料清单版本** 快速选项卡上，选择要为其分配指南的版本。</span><span class="sxs-lookup"><span data-stu-id="77e2d-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-301">在 **物料清单版本** 工具栏上，选择 **关联的指南**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="77e2d-302">![打开与所选物料清单版本关联的指南](media/instruction-guides-BOMVersion.png "打开与所选物料清单版本关联的指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="77e2d-303">将针对物料清单版本打开 **关联的指南** 页面。</span><span class="sxs-lookup"><span data-stu-id="77e2d-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="77e2d-304">在“操作”窗格上，选择 **添加** 以向网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="77e2d-305">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-306">![将指南添加到物料清单版本](media/instruction-guides-BOMVersionAddGuide.png "将指南添加到物料清单版本")</span><span class="sxs-lookup"><span data-stu-id="77e2d-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="77e2d-307">将指南关联到工艺路线</span><span class="sxs-lookup"><span data-stu-id="77e2d-307">Associate a Guide to a route</span></span>

<span data-ttu-id="77e2d-308">您可以将指南添加到任何[工艺路线](routes-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="77e2d-309">使用工艺路线的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-309">Typical scenario using routes</span></span>

<span data-ttu-id="77e2d-310">工艺路线通常用于指定应如何基于物料清单或物料清单版本以及一组资源或资源组来生产特定的已发布产品。</span><span class="sxs-lookup"><span data-stu-id="77e2d-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="77e2d-311">将指南分配到工艺路线，以为各个生产流程提供分步说明。</span><span class="sxs-lookup"><span data-stu-id="77e2d-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="77e2d-312">将指南添加到工艺路线</span><span class="sxs-lookup"><span data-stu-id="77e2d-312">Add a Guide to a route</span></span>

<span data-ttu-id="77e2d-313">若要将指南添加到工艺路线：</span><span class="sxs-lookup"><span data-stu-id="77e2d-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="77e2d-314">转到 **生产控制 \> 所有工艺路线**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="77e2d-315">打开要为其分配指南的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="77e2d-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-316">展开 **关联的指南** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="77e2d-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="77e2d-317">从 **关联的指南** 工具栏中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="77e2d-318">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="77e2d-319">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-320">![将指南添加到工艺路线](media/instruction-guides-Route.png "将指南添加到工艺路线")</span><span class="sxs-lookup"><span data-stu-id="77e2d-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="77e2d-321">将指南关联到工艺路线版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="77e2d-322">您可以将指南添加到任何[工艺路线版本](routes-operations.md#route-versions)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="77e2d-323">使用工艺路线版本的典型方案</span><span class="sxs-lookup"><span data-stu-id="77e2d-323">Typical scenario using route versions</span></span>

<span data-ttu-id="77e2d-324">工艺路线版本通常用于根据现有工艺路线指定生产流程的变体。</span><span class="sxs-lookup"><span data-stu-id="77e2d-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="77e2d-325">您可以为每个工艺路线版本分配不同的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="77e2d-326">将指南添加到工艺路线版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-326">Add a Guide to a route version</span></span>

<span data-ttu-id="77e2d-327">若要将指南添加到工艺路线版本：</span><span class="sxs-lookup"><span data-stu-id="77e2d-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="77e2d-328">转到 **生产控制 \> 所有工艺路线**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="77e2d-329">打开要为其分配指南的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="77e2d-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-330">在 **版本** 快速选项卡上，选择要为其分配指南的版本。</span><span class="sxs-lookup"><span data-stu-id="77e2d-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-331">在 **版本** 工具栏上，选择 **关联的指南**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="77e2d-332">![打开与所选工艺路线版本关联的指南](media/instruction-guides-RouteVersion.png "打开与所选工艺路线版本关联的指南")</span><span class="sxs-lookup"><span data-stu-id="77e2d-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="77e2d-333">将针对物料清单版本打开 **关联的指南** 页面。</span><span class="sxs-lookup"><span data-stu-id="77e2d-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="77e2d-334">在“操作”窗格上，选择 **添加** 以向网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="77e2d-335">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="77e2d-336">![将指南添加到工艺路线版本](media/instruction-guides-RouteVersionAddGuide.png "将指南添加到工艺路线版本")</span><span class="sxs-lookup"><span data-stu-id="77e2d-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="77e2d-337">将指南关联到工艺路线工序关系</span><span class="sxs-lookup"><span data-stu-id="77e2d-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="77e2d-338">您可以将指南添加到任何[工艺路线工序关系](routes-operations.md#operation-relations)。</span><span class="sxs-lookup"><span data-stu-id="77e2d-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="77e2d-339">使用工艺路线工序关系的典型场景</span><span class="sxs-lookup"><span data-stu-id="77e2d-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="77e2d-340">工序关系是向产品流程及其相关工序添加指南的最具体方法。</span><span class="sxs-lookup"><span data-stu-id="77e2d-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="77e2d-341">您可以为工艺路线中的每个工序指定指导，并针对为工艺路线指定的任何类型的关系环境（例如，特定物料、配置等）指定不同的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="77e2d-342">您还可以指定该指南适用于工序中的哪些阶段（例如设置、排队、处理或运输）。</span><span class="sxs-lookup"><span data-stu-id="77e2d-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="77e2d-343">如果为一个工艺路线的多个工序关系指定指南，则在这些指南中，只有最具体的关系中的指南才会显示在生成作业的车间中。</span><span class="sxs-lookup"><span data-stu-id="77e2d-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="77e2d-344">将指南添加到工艺路线工序关系</span><span class="sxs-lookup"><span data-stu-id="77e2d-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="77e2d-345">若要将指南添加到工艺路线工序关系：</span><span class="sxs-lookup"><span data-stu-id="77e2d-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="77e2d-346">转到 **生产控制 \> 所有工艺路线**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="77e2d-347">打开要为其分配指南的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="77e2d-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="77e2d-348">在“操作”窗格上，打开 **工艺路线** 选项卡，然后从 **维护** 组中，选择 **工艺路线详细信息**。</span><span class="sxs-lookup"><span data-stu-id="77e2d-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="77e2d-349">将针对所选工艺路线打开 **工艺路线详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="77e2d-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="77e2d-350">在顶部网格中，选择要为其提供指南的工序。</span><span class="sxs-lookup"><span data-stu-id="77e2d-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="77e2d-351">在底部网格中，选择一个特定的关系（或通用 **所有** 关系）。</span><span class="sxs-lookup"><span data-stu-id="77e2d-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="77e2d-352">![选择一个工序，然后选择一个关系](media/instruction-guides-RouteOperationRelation.png "选择一个工序，然后选择一个关系")</span><span class="sxs-lookup"><span data-stu-id="77e2d-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="77e2d-353">在底部网格的上方，打开 **关联的指南** 选项卡。![关联的指南选项卡](media/instruction-guides-RouteOperationRelation-AddGuide.png "关联的指南选项卡")</span><span class="sxs-lookup"><span data-stu-id="77e2d-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="77e2d-354">在底部网格的顶部，从工具栏中选择 **添加** 以向网格添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="77e2d-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="77e2d-355">对于新行，请使用 **名称** 列中的下拉列表选择要分配的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="77e2d-356">在该行的其余部分，为每个环境选择相应的复选框，其中所选指南应该可用。</span><span class="sxs-lookup"><span data-stu-id="77e2d-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="77e2d-357">您可以为每个工序的每个阶段添加一个或多个指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="77e2d-358">从车间执行界面中选择指南</span><span class="sxs-lookup"><span data-stu-id="77e2d-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="77e2d-359">当工作人员在车间执行界面上打开作业列表时，Supply Chain Management 将为显示的作业找到相关的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="77e2d-360">使用 **指南** 按钮以查看相关的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="77e2d-361">![车间执行界面中的指南按钮](media/instruction-guides-Shopfloor1.png "车间执行界面中的指南按钮")</span><span class="sxs-lookup"><span data-stu-id="77e2d-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="77e2d-362">然后设定 HoloLens，通过浏览 QR 码并激活相应的指南来访问相应的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="77e2d-363">![用于使用 HoloLens 访问指南的 QR 码](media/instruction-guides-Shopfloor2.png "用于使用 HoloLens 访问指南的 QR 码")</span><span class="sxs-lookup"><span data-stu-id="77e2d-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="77e2d-364">解析用于选择指南的逻辑</span><span class="sxs-lookup"><span data-stu-id="77e2d-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="77e2d-365">您可以将指南添加到以下生产数据：</span><span class="sxs-lookup"><span data-stu-id="77e2d-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="77e2d-366">资源</span><span class="sxs-lookup"><span data-stu-id="77e2d-366">Resources</span></span>](#resources)
- [<span data-ttu-id="77e2d-367">资源组</span><span class="sxs-lookup"><span data-stu-id="77e2d-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="77e2d-368">已发布产品</span><span class="sxs-lookup"><span data-stu-id="77e2d-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="77e2d-369">配方</span><span class="sxs-lookup"><span data-stu-id="77e2d-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="77e2d-370">配方版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="77e2d-371">物料清单 (BOM)</span><span class="sxs-lookup"><span data-stu-id="77e2d-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="77e2d-372">物料清单版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="77e2d-373">运输路径</span><span class="sxs-lookup"><span data-stu-id="77e2d-373">Routes</span></span>](#routes)
- [<span data-ttu-id="77e2d-374">工艺路线版本</span><span class="sxs-lookup"><span data-stu-id="77e2d-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="77e2d-375">工艺路线工序关系</span><span class="sxs-lookup"><span data-stu-id="77e2d-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="77e2d-376">当 Supply Chain Management 为车间生成作业时，它将从这些来源收集相关的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="77e2d-377">请注意以下重要的规则。</span><span class="sxs-lookup"><span data-stu-id="77e2d-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="77e2d-378">如果将物料清单版本或配方版本附加到工艺路线或生产订单，则附加到此版本的任何指南以及附加到该版本的父级物料清单或配方的指南都将显示在作业上。</span><span class="sxs-lookup"><span data-stu-id="77e2d-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="77e2d-379">如果将工艺路线版本附加到生产订单，则附加到此版本的任何指南以及附加到该版本的父级工艺路线的指南都将显示在作业上。</span><span class="sxs-lookup"><span data-stu-id="77e2d-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="77e2d-380">如果定义多个包括 *所有* 关系的工艺路线工艺关系并向其分配指南，则仅为该作业显示最具体关系中的指南。</span><span class="sxs-lookup"><span data-stu-id="77e2d-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="77e2d-381">![解析相关指南的图表](media/instruction-guides-Resolve.png "解析相关指南的图表")</span><span class="sxs-lookup"><span data-stu-id="77e2d-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]