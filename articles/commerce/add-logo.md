---
title: 添加徽标
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62b8237fa0c30fa9d901d670de38416cf8615c8d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686638"
---
# <a name="add-a-logo"></a><span data-ttu-id="c1bea-103">添加徽标</span><span class="sxs-lookup"><span data-stu-id="c1bea-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1bea-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。</span><span class="sxs-lookup"><span data-stu-id="c1bea-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c1bea-105">概览</span><span class="sxs-lookup"><span data-stu-id="c1bea-105">Overview</span></span>

<span data-ttu-id="c1bea-106">建立站点时，您可能要做的第一件事就是将公司或品牌徽标添加到站点页眉中。</span><span class="sxs-lookup"><span data-stu-id="c1bea-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="c1bea-107">Dynamics 365 Commerce 在线入门套件提供了让此任务轻松实现的模块。</span><span class="sxs-lookup"><span data-stu-id="c1bea-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="c1bea-108">您可以将徽标直接添加到模板、布局或页面中。</span><span class="sxs-lookup"><span data-stu-id="c1bea-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="c1bea-109">这样，您可以轻松地更改出现在特定页面或页面组上的徽标。</span><span class="sxs-lookup"><span data-stu-id="c1bea-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="c1bea-110">但本主题介绍最常见的场景：您将徽标添加到可以在站点的所有页面上重复使用的页眉片段中。</span><span class="sxs-lookup"><span data-stu-id="c1bea-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1bea-111">先决条件</span><span class="sxs-lookup"><span data-stu-id="c1bea-111">Prerequisites</span></span>

<span data-ttu-id="c1bea-112">您必须先完成以下任务，才能将徽标添加到站点的所有页面。</span><span class="sxs-lookup"><span data-stu-id="c1bea-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="c1bea-113">将徽标上传到媒体库。</span><span class="sxs-lookup"><span data-stu-id="c1bea-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="c1bea-114">创建页眉片段。</span><span class="sxs-lookup"><span data-stu-id="c1bea-114">Create a header fragment.</span></span> <span data-ttu-id="c1bea-115">有关如何创建和使用片段的详细信息，请参阅[使用片段](work-with-fragments.md)。</span><span class="sxs-lookup"><span data-stu-id="c1bea-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="c1bea-116">在站点的页面用来建立布局和模块选项的模板中包含页眉片段。</span><span class="sxs-lookup"><span data-stu-id="c1bea-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="c1bea-117">有关模板的详细信息，请参阅[使用模板](work-with-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="c1bea-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="c1bea-118">将徽标添加到页眉片段</span><span class="sxs-lookup"><span data-stu-id="c1bea-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="c1bea-119">要将徽标添加到您的站点的页眉片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c1bea-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="c1bea-120">在左侧的导航窗格中，选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="c1bea-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c1bea-121">选择前面创建的页眉片段，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="c1bea-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="c1bea-122">展开页眉模块。</span><span class="sxs-lookup"><span data-stu-id="c1bea-122">Expand the header module.</span></span>
1. <span data-ttu-id="c1bea-123">在页眉模块的属性窗格中，提供徽标的图像和链接。</span><span class="sxs-lookup"><span data-stu-id="c1bea-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="c1bea-124">保存页眉片段，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c1bea-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="c1bea-125">发布更新的页眉片段后，所有使用包含页眉片段的模板的站点页面都将显示您的徽标。</span><span class="sxs-lookup"><span data-stu-id="c1bea-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1bea-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="c1bea-126">Additional resources</span></span>

[<span data-ttu-id="c1bea-127">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="c1bea-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c1bea-128">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="c1bea-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c1bea-129">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="c1bea-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c1bea-130">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="c1bea-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c1bea-131">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="c1bea-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c1bea-132">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="c1bea-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c1bea-133">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="c1bea-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

