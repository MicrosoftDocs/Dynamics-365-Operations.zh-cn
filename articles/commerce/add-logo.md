---
title: 添加徽标
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914608"
---
# <a name="add-a-logo"></a><span data-ttu-id="5f735-103">添加徽标</span><span class="sxs-lookup"><span data-stu-id="5f735-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5f735-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。</span><span class="sxs-lookup"><span data-stu-id="5f735-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f735-105">概览</span><span class="sxs-lookup"><span data-stu-id="5f735-105">Overview</span></span>

<span data-ttu-id="5f735-106">建立站点时，您可能要做的第一件事就是将公司或品牌徽标添加到站点页眉中。</span><span class="sxs-lookup"><span data-stu-id="5f735-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="5f735-107">Dynamics 365 Commerce 在线入门套件提供了让此任务轻松实现的模块。</span><span class="sxs-lookup"><span data-stu-id="5f735-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="5f735-108">您可以将徽标直接添加到模板、布局或页面中。</span><span class="sxs-lookup"><span data-stu-id="5f735-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="5f735-109">这样，您可以轻松地更改出现在特定页面或页面组上的徽标。</span><span class="sxs-lookup"><span data-stu-id="5f735-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="5f735-110">但本主题介绍最常见的场景：您将徽标添加到可以在站点的所有页面上重复使用的页眉片段中。</span><span class="sxs-lookup"><span data-stu-id="5f735-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5f735-111">先决条件</span><span class="sxs-lookup"><span data-stu-id="5f735-111">Prerequisites</span></span>

<span data-ttu-id="5f735-112">您必须先完成以下任务，才能将徽标添加到站点的所有页面。</span><span class="sxs-lookup"><span data-stu-id="5f735-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="5f735-113">将您的徽标上载到数字资产管理器（可以从**资产**页访问）。</span><span class="sxs-lookup"><span data-stu-id="5f735-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="5f735-114">创建页眉片段。</span><span class="sxs-lookup"><span data-stu-id="5f735-114">Create a header fragment.</span></span> <span data-ttu-id="5f735-115">有关如何创建和使用片段的详细信息，请参阅[使用片段](work-with-fragments.md)。</span><span class="sxs-lookup"><span data-stu-id="5f735-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="5f735-116">在站点的页面用来建立布局和模块选项的模板中包含页眉片段。</span><span class="sxs-lookup"><span data-stu-id="5f735-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="5f735-117">有关模板的详细信息，请参阅[使用模板](work-with-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="5f735-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="5f735-118">将徽标添加到页眉片段</span><span class="sxs-lookup"><span data-stu-id="5f735-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="5f735-119">要将徽标添加到您的站点的页眉片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5f735-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="5f735-120">在左侧的导航窗格中，选择**片段**，然后选择您创建的页眉片段。</span><span class="sxs-lookup"><span data-stu-id="5f735-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="5f735-121">选择**签出**。</span><span class="sxs-lookup"><span data-stu-id="5f735-121">Select **Check out**.</span></span>
3. <span data-ttu-id="5f735-122">展开**页眉**插槽和**徽标**插槽。</span><span class="sxs-lookup"><span data-stu-id="5f735-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="5f735-123">选择**徽标**插槽的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="5f735-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="5f735-124">选择徽标模块。</span><span class="sxs-lookup"><span data-stu-id="5f735-124">Select the logo module.</span></span>
6. <span data-ttu-id="5f735-125">在右侧的属性窗格中，配置徽标模块，使其显示您的徽标。</span><span class="sxs-lookup"><span data-stu-id="5f735-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="5f735-126">保存页眉片段，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="5f735-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="5f735-127">发布更新的页眉片段后，所有使用包含页眉片段的模板的站点页面都将显示您的徽标。</span><span class="sxs-lookup"><span data-stu-id="5f735-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f735-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="5f735-128">Additional resources</span></span>

[<span data-ttu-id="5f735-129">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="5f735-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5f735-130">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="5f735-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5f735-131">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="5f735-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5f735-132">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="5f735-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5f735-133">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="5f735-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5f735-134">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="5f735-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5f735-135">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="5f735-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

