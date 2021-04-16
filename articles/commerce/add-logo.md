---
title: 添加徽标
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797591"
---
# <a name="add-a-logo"></a><span data-ttu-id="834e2-103">添加徽标</span><span class="sxs-lookup"><span data-stu-id="834e2-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="834e2-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。</span><span class="sxs-lookup"><span data-stu-id="834e2-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="834e2-105">建立站点时，您可能要做的第一件事就是将公司或品牌徽标添加到站点页眉中。</span><span class="sxs-lookup"><span data-stu-id="834e2-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="834e2-106">Dynamics 365 Commerce 在线模块库提供了让此任务轻松实现的模块。</span><span class="sxs-lookup"><span data-stu-id="834e2-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="834e2-107">您可以将徽标直接添加到模板、布局或页面中。</span><span class="sxs-lookup"><span data-stu-id="834e2-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="834e2-108">这样，您可以轻松地更改出现在特定页面或页面组上的徽标。</span><span class="sxs-lookup"><span data-stu-id="834e2-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="834e2-109">但本主题介绍最常见的场景：您将徽标添加到可以在站点的所有页面上重复使用的页眉片段中。</span><span class="sxs-lookup"><span data-stu-id="834e2-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="834e2-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="834e2-110">Prerequisites</span></span>

<span data-ttu-id="834e2-111">您必须先完成以下任务，才能将徽标添加到站点的所有页面。</span><span class="sxs-lookup"><span data-stu-id="834e2-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="834e2-112">将徽标上传到媒体库。</span><span class="sxs-lookup"><span data-stu-id="834e2-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="834e2-113">创建页眉片段。</span><span class="sxs-lookup"><span data-stu-id="834e2-113">Create a header fragment.</span></span> <span data-ttu-id="834e2-114">有关如何创建和使用片段的详细信息，请参阅[使用片段](work-with-fragments.md)。</span><span class="sxs-lookup"><span data-stu-id="834e2-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="834e2-115">在站点的页面用来建立布局和模块选项的模板中包含页眉片段。</span><span class="sxs-lookup"><span data-stu-id="834e2-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="834e2-116">有关模板的详细信息，请参阅[使用模板](work-with-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="834e2-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="834e2-117">将徽标添加到页眉片段</span><span class="sxs-lookup"><span data-stu-id="834e2-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="834e2-118">要将徽标添加到您的站点的页眉片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="834e2-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="834e2-119">在左侧的导航窗格中，选择 **片段**。</span><span class="sxs-lookup"><span data-stu-id="834e2-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="834e2-120">选择前面创建的页眉片段，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="834e2-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="834e2-121">展开页眉模块。</span><span class="sxs-lookup"><span data-stu-id="834e2-121">Expand the header module.</span></span>
1. <span data-ttu-id="834e2-122">在页眉模块的属性窗格中，提供徽标的图像和链接。</span><span class="sxs-lookup"><span data-stu-id="834e2-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="834e2-123">保存页眉片段，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="834e2-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="834e2-124">发布更新的页眉片段后，所有使用包含页眉片段的模板的站点页面都将显示您的徽标。</span><span class="sxs-lookup"><span data-stu-id="834e2-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="834e2-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="834e2-125">Additional resources</span></span>

[<span data-ttu-id="834e2-126">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="834e2-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="834e2-127">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="834e2-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="834e2-128">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="834e2-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="834e2-129">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="834e2-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="834e2-130">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="834e2-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="834e2-131">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="834e2-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="834e2-132">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="834e2-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
