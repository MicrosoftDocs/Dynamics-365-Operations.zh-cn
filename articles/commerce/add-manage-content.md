---
title: 添加内容的方法
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中添加和管理内容。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2232dc7cdd24416b0df0919b96cd5d1f8113299f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914646"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="d4425-103">添加内容的方法</span><span class="sxs-lookup"><span data-stu-id="d4425-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d4425-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中添加和管理内容。</span><span class="sxs-lookup"><span data-stu-id="d4425-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="d4425-105">概览</span><span class="sxs-lookup"><span data-stu-id="d4425-105">Overview</span></span>

<span data-ttu-id="d4425-106">可通过多种方法更改站点的外观和内容。</span><span class="sxs-lookup"><span data-stu-id="d4425-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="d4425-107">非开发人员可以实施这些更改中的许多，具体取决于所需自定义级别。</span><span class="sxs-lookup"><span data-stu-id="d4425-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="d4425-108">例如，不必编写代码即可生成模板，选择主题和选择并配置模板。</span><span class="sxs-lookup"><span data-stu-id="d4425-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="d4425-109">相反，需要开发技能才能新建主题或模块，因为必须使用电子商务软件开发套件 (SDK) 和 Microsoft Dynamics Lifecycle Services (LCS) 部署工作流。</span><span class="sxs-lookup"><span data-stu-id="d4425-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="d4425-110">以下主题提供了有关如何添加和管理站点内容的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d4425-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="d4425-111">重点介绍了无需开发人员的站点区域。</span><span class="sxs-lookup"><span data-stu-id="d4425-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="d4425-112">按照要求，指出了需要 SDK 工作的任务。</span><span class="sxs-lookup"><span data-stu-id="d4425-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="d4425-113">若要更改现有站点页中的文本、图像或视频，请参阅[使用模块](work-with-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="d4425-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="d4425-114">若要帮助确保 Web 内容作者的极简单品牌创作体验，请参阅[使用模板](work-with-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d4425-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="d4425-115">若要重新安排站点页中的分区，请参阅[使用布局](work-with-layouts.md)。</span><span class="sxs-lookup"><span data-stu-id="d4425-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="d4425-116">若要更改站点页的字体、颜色和一般外观，请参阅[选择站点主题](select-site-theme.md)。</span><span class="sxs-lookup"><span data-stu-id="d4425-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4425-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="d4425-117">Additional resources</span></span>

[<span data-ttu-id="d4425-118">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="d4425-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="d4425-119">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="d4425-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="d4425-120">使用发布组</span><span class="sxs-lookup"><span data-stu-id="d4425-120">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="d4425-121">使用模块</span><span class="sxs-lookup"><span data-stu-id="d4425-121">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="d4425-122">使用片段</span><span class="sxs-lookup"><span data-stu-id="d4425-122">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d4425-123">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="d4425-123">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d4425-124">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="d4425-124">Customize site navigation</span></span>](customize-site-navigation.md)
