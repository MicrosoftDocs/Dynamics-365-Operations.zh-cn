---
title: Attract 的可扩展性
description: 此主题介绍如何使用 Microsoft Power 平台扩展 Microsoft Dynamics 365 for Talent - Attract 应用程序。
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303397"
---
# <a name="extensibility-in-attract"></a><span data-ttu-id="b6df5-103">Attract 的可扩展性</span><span class="sxs-lookup"><span data-stu-id="b6df5-103">Extensibility in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b6df5-104">Microsoft Dynamics 365 for Talent 在 Common Data Service (CDS) for Apps 平台基础上构建，可以使用 Microsoft Power 平台和 Common Data Service for Apps 提供的功能以各种方式扩展。</span><span class="sxs-lookup"><span data-stu-id="b6df5-104">Microsoft Dynamics 365 for Talent is built on top of the Common Data Service (CDS) for Apps platform, and can be extended in various ways by using the Microsoft Power Platform and the capabilities that Common Data Service for Apps offers.</span></span> <span data-ttu-id="b6df5-105">因此，您可以使用 Microsoft PowerApps 和 Microsoft Flow 来配置和个性化系统。</span><span class="sxs-lookup"><span data-stu-id="b6df5-105">Therefore, you can configure and personalize the system by using Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="b6df5-106">还可以使用 Microsoft Power BI 获取有关人员的附加分析。</span><span class="sxs-lookup"><span data-stu-id="b6df5-106">You can also get additional analytics about people by using Microsoft Power BI.</span></span> <span data-ttu-id="b6df5-107">此外，PowerApps 和 Web 内容 (iframe) 活动等新的自定义活动让招聘流程的适应性比以往更强。</span><span class="sxs-lookup"><span data-stu-id="b6df5-107">Furthermore, new custom activities, such as the PowerApps and Web content (iframe) activities, make the hiring process more adaptable than ever.</span></span> <span data-ttu-id="b6df5-108">通过使用这些活动，您可以针对您的业务需要和流程来定制招聘流程，并且可以确保招聘团队和应聘者具有无缝的自定义体验。</span><span class="sxs-lookup"><span data-stu-id="b6df5-108">By using these activities, you can tailor the hiring process to your business needs and processes, and can make sure that both the hiring team and candidates have a seamless, customized experience.</span></span>

## <a name="take-advantage-of-the-microsoft-power-platform"></a><span data-ttu-id="b6df5-109">利用 Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="b6df5-109">Take advantage of the Microsoft Power platform</span></span> 

<span data-ttu-id="b6df5-110">由于 Attract 的所有数据均位于 Common Data Service for Apps 中，您可以使用 Microsoft Power 平台的工具来将您的独特业务需求合并到 Attract 中。</span><span class="sxs-lookup"><span data-stu-id="b6df5-110">Because all the data from Attract resides in Common Data Service for Apps, you can use tools from the Microsoft Power platform to incorporate your unique business needs into Attract.</span></span>

### <a name="powerapps"></a><span data-ttu-id="b6df5-111">PowerApps</span><span class="sxs-lookup"><span data-stu-id="b6df5-111">PowerApps</span></span>

<span data-ttu-id="b6df5-112">您可以使用 PowerApps 轻松构建与您的 Attract 数据连接并且使用如 Microsoft Excel 中的表达式添加逻辑的应用。</span><span class="sxs-lookup"><span data-stu-id="b6df5-112">You can use PowerApps to easily build apps that connect to your Attract data, and that use expressions like the expressions in Microsoft Excel to add logic.</span></span> <span data-ttu-id="b6df5-113">您使用 PowerApps 构建的应用可以在 Web 上以及 Apple iOS 和 Google Android 设备上运行。</span><span class="sxs-lookup"><span data-stu-id="b6df5-113">Apps that you build by using PowerApps can run on the web, and on Apple iOS and Google Android devices.</span></span>

<span data-ttu-id="b6df5-114">例如，您可以构建让其在 Attract 中扫描简历并向应聘者发送职位的轻型应用，从而让招聘人员更加轻松地应对大学招聘会。</span><span class="sxs-lookup"><span data-stu-id="b6df5-114">For example, you can make university career fairs easier for recruiters by building a lightweight app that lets them scan resumes and feed candidates to a position in Attract.</span></span> <span data-ttu-id="b6df5-115">或者，您可以构建帮助您的组织达到合规要求的应用。</span><span class="sxs-lookup"><span data-stu-id="b6df5-115">Alternatively, you can build an app that helps meet your organization's compliance needs.</span></span> <span data-ttu-id="b6df5-116">有关 PowerApps 以及如何用它来构建应用的更多信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps)。</span><span class="sxs-lookup"><span data-stu-id="b6df5-116">For more information about PowerApps and how to use it to build apps, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).</span></span>

### <a name="microsoft-flow"></a><span data-ttu-id="b6df5-117">Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="b6df5-117">Microsoft Flow</span></span> 

<span data-ttu-id="b6df5-118">您可以使用 Microsoft Flow 创建在 Attract 数据基础上运行的自动化工作流。</span><span class="sxs-lookup"><span data-stu-id="b6df5-118">You can use Microsoft Flow to create automated workflows that run on top of Attract data.</span></span> <span data-ttu-id="b6df5-119">您可以轻松连接到成百上千个热闹应用和服务，而不必编写代码。</span><span class="sxs-lookup"><span data-stu-id="b6df5-119">You can easily connect to hundreds of popular apps and services without having to write code.</span></span> <span data-ttu-id="b6df5-120">通过在 Common Data Service for Apps 中构建与 Attract 工作、应聘者和申请实体交互的流，您可以自动执行各种操作。</span><span class="sxs-lookup"><span data-stu-id="b6df5-120">By building flows that interact with the Attract Job, Candidate, and Application entities in Common Data Service for Apps, you can automate various actions.</span></span> <span data-ttu-id="b6df5-121">例如，当应聘者接受聘约时，可以向入职团队发送通知，或可以在 Twitter 上公布新闻。</span><span class="sxs-lookup"><span data-stu-id="b6df5-121">For example, when a candidate accepts an offer, a notification can be sent to an onboarding team, or the news can be announced on Twitter.</span></span> <span data-ttu-id="b6df5-122">有关流的详细信息，请参阅 [Microsoft Flow 文档](https://docs.microsoft.com/en-us/flow/)。</span><span class="sxs-lookup"><span data-stu-id="b6df5-122">For more information about flows, see the [Microsoft Flow documentation](https://docs.microsoft.com/en-us/flow/).</span></span>

### <a name="power-bi"></a><span data-ttu-id="b6df5-123">Power BI</span><span class="sxs-lookup"><span data-stu-id="b6df5-123">Power BI</span></span>

<span data-ttu-id="b6df5-124">Power BI 让您可以建立并查看让您更深入地了解 Attract 数据的自定义报表和仪表板。</span><span class="sxs-lookup"><span data-stu-id="b6df5-124">Power BI lets you build and view custom reports and dashboards that give you deeper insight into your Attract data.</span></span> <span data-ttu-id="b6df5-125">有关 Power BI 以及如何建立交互式报表和仪表板的更多信息，请参阅 [Power BI 文档](https://docs.microsoft.com/en-us/power-bi/)。</span><span class="sxs-lookup"><span data-stu-id="b6df5-125">For more information about Power BI and how to build interactive reports and dashboards, see the [Power BI documentation](https://docs.microsoft.com/en-us/power-bi/).</span></span>

### <a name="custom-activities"></a><span data-ttu-id="b6df5-126">自定义活动</span><span class="sxs-lookup"><span data-stu-id="b6df5-126">Custom activities</span></span> 

<span data-ttu-id="b6df5-127">您可以在工作流程模板或在创建新工作时添加自定义活动，例如 PowerApps 应用和 Web 内容 (iframe) 活动。</span><span class="sxs-lookup"><span data-stu-id="b6df5-127">You can add custom activities, such as the PowerApps apps and Web content (iframe) activities, at the level of the job process template or while you're creating a new job.</span></span> <span data-ttu-id="b6df5-128">这些活动让您可以自定义招聘流程，并将特定于您的组织的业务逻辑带入 Attract。</span><span class="sxs-lookup"><span data-stu-id="b6df5-128">These activities let you customize the hiring process and bring business logic that is unique to your organization into Attract.</span></span>

#### <a name="powerapps-activity"></a><span data-ttu-id="b6df5-129">PowerApps 活动</span><span class="sxs-lookup"><span data-stu-id="b6df5-129">PowerApps activity</span></span> 

<span data-ttu-id="b6df5-130">PowerApps 活动允许工业或工作流程模板的创建者在招聘流程中嵌入 PowerApps 应用。</span><span class="sxs-lookup"><span data-stu-id="b6df5-130">The PowerApps activity lets the creator of a job or job process template embed a PowerApps app in the hiring flow.</span></span> <span data-ttu-id="b6df5-131">在创建和发布应用后，您可以在活动配置中输入其应用 ID。</span><span class="sxs-lookup"><span data-stu-id="b6df5-131">After you create and publish the app, you can enter its app ID in the activity configurations.</span></span> <span data-ttu-id="b6df5-132">通过使用 PowerApps 应用，您可以在 Common Data Service for Apps 中读取和写入数据。</span><span class="sxs-lookup"><span data-stu-id="b6df5-132">By using a PowerApps app, you can read and write data into Common Data Service for Apps.</span></span> <span data-ttu-id="b6df5-133">您甚至可以将应用链接到流。</span><span class="sxs-lookup"><span data-stu-id="b6df5-133">You can even link the app to a flow.</span></span> <span data-ttu-id="b6df5-134">例如，您有一个招聘人员用来在进行电话面试时填写表单的应用。</span><span class="sxs-lookup"><span data-stu-id="b6df5-134">For example, you have an app that recruiters use to fill in a form while they conduct phone interviews.</span></span> <span data-ttu-id="b6df5-135">在这种情况下，您可以将应用链接到评估申请可否在工作申请流程中继续推进的流。</span><span class="sxs-lookup"><span data-stu-id="b6df5-135">In this case, you can link the app to a flow that evaluates whether an applicant can be advanced further in the job application process.</span></span> <span data-ttu-id="b6df5-136">此类活动只能由招聘团队的成员查看。</span><span class="sxs-lookup"><span data-stu-id="b6df5-136">This type of activity can be viewed only by members of the hiring team.</span></span> <span data-ttu-id="b6df5-137">有关如何配置 PowerApps 活动的详细信息，请参阅 [Attract 中的活动](./activities-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="b6df5-137">For more information about how to configure the PowerApps activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b6df5-138">PowerApps 活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="b6df5-138">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

#### <a name="web-content-iframe-activity"></a><span data-ttu-id="b6df5-139">Web 内容 (iframe) 活动</span><span class="sxs-lookup"><span data-stu-id="b6df5-139">Web content (iframe) activity</span></span>

<span data-ttu-id="b6df5-140">Web 内容 (iframe) 活动允许您嵌入在招聘流程或应聘者门户构建的自定义 Web 解决方案。</span><span class="sxs-lookup"><span data-stu-id="b6df5-140">The Web content (iframe) activity lets you embed a custom web solution that you've built in the hiring process or the Candidate portal.</span></span> <span data-ttu-id="b6df5-141">您可以直接从 Common Data Service for Apps 读取和写入数据。</span><span class="sxs-lookup"><span data-stu-id="b6df5-141">You can read and write data directly from Common Data Service for Apps.</span></span> <span data-ttu-id="b6df5-142">还可以自定义解决方案，以使它触发流或利用 Microsoft Azure 功能。</span><span class="sxs-lookup"><span data-stu-id="b6df5-142">You can also customize the solution so that it triggers flows or takes advantage of Microsoft Azure functions.</span></span> <span data-ttu-id="b6df5-143">有关如何配置 Web 内容活动的详细信息，请参阅 [Attract 中的活动](./activities-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="b6df5-143">For more information about how to configure the Web content activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b6df5-144">Web 内容活动仅通过综合招聘附件提供。</span><span class="sxs-lookup"><span data-stu-id="b6df5-144">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>
