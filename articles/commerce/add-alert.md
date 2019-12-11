---
title: 预警模块
description: 此主题介绍预警模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785344"
---
# <a name="alert-module"></a><span data-ttu-id="fee27-103">预警模块</span><span class="sxs-lookup"><span data-stu-id="fee27-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fee27-104">此主题介绍预警模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="fee27-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fee27-105">概览</span><span class="sxs-lookup"><span data-stu-id="fee27-105">Overview</span></span>

<span data-ttu-id="fee27-106">预警模块用于在页面中显示内联参考消息。</span><span class="sxs-lookup"><span data-stu-id="fee27-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="fee27-107">预警模块支持文本消息和链接。</span><span class="sxs-lookup"><span data-stu-id="fee27-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="fee27-108">可用于显示电子商务站点所有页面中显示的站点范围促销。</span><span class="sxs-lookup"><span data-stu-id="fee27-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="fee27-109">预警模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="fee27-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="fee27-110">电子商务中的预警模块示例</span><span class="sxs-lookup"><span data-stu-id="fee27-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="fee27-111">可在站点标题中使用预警模块指示站点范围的促销或消息。</span><span class="sxs-lookup"><span data-stu-id="fee27-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="fee27-112">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="fee27-112">Here are some examples:</span></span>

<span data-ttu-id="fee27-113">“年度促销 10 天后结束”</span><span class="sxs-lookup"><span data-stu-id="fee27-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="fee27-114">“返校季大促销。</span><span class="sxs-lookup"><span data-stu-id="fee27-114">"Save big with back to school sale.</span></span> <span data-ttu-id="fee27-115">快来买啦。”</span><span class="sxs-lookup"><span data-stu-id="fee27-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="fee27-116">预警模块属性</span><span class="sxs-lookup"><span data-stu-id="fee27-116">Alert module properties</span></span>

| <span data-ttu-id="fee27-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="fee27-117">Property name</span></span>  | <span data-ttu-id="fee27-118">值</span><span class="sxs-lookup"><span data-stu-id="fee27-118">Value</span></span>                              | <span data-ttu-id="fee27-119">说明</span><span class="sxs-lookup"><span data-stu-id="fee27-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="fee27-120">文本</span><span class="sxs-lookup"><span data-stu-id="fee27-120">Text</span></span>           | <span data-ttu-id="fee27-121">文本</span><span class="sxs-lookup"><span data-stu-id="fee27-121">Text</span></span>                               | <span data-ttu-id="fee27-122">预警模块中显示的文本消息。</span><span class="sxs-lookup"><span data-stu-id="fee27-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="fee27-123">文本对齐</span><span class="sxs-lookup"><span data-stu-id="fee27-123">Text alignment</span></span> | <span data-ttu-id="fee27-124">**向右对齐**、**向左对齐**或**居中对齐**</span><span class="sxs-lookup"><span data-stu-id="fee27-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="fee27-125">用于定义预警模块中的文本如何对齐的值。</span><span class="sxs-lookup"><span data-stu-id="fee27-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="fee27-126">消除预警</span><span class="sxs-lookup"><span data-stu-id="fee27-126">Dismiss alert</span></span>  | <span data-ttu-id="fee27-127">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="fee27-127">**True** or **False**</span></span>              | <span data-ttu-id="fee27-128">如果此值设置为 **True**，则客户可忽略预警。</span><span class="sxs-lookup"><span data-stu-id="fee27-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="fee27-129">链接</span><span class="sxs-lookup"><span data-stu-id="fee27-129">Link</span></span>           | <span data-ttu-id="fee27-130">URL</span><span class="sxs-lookup"><span data-stu-id="fee27-130">URL</span></span>                                | <span data-ttu-id="fee27-131">可选链接的 URL。</span><span class="sxs-lookup"><span data-stu-id="fee27-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="fee27-132">向页面添加预警模块</span><span class="sxs-lookup"><span data-stu-id="fee27-132">Add an alert module to a page</span></span> 

<span data-ttu-id="fee27-133">若要向新页面添加预警模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fee27-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fee27-134">创建一个名称为**预警模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="fee27-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="fee27-135">在默认页的**主**插槽中，添加一个预警模块。</span><span class="sxs-lookup"><span data-stu-id="fee27-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="fee27-136">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="fee27-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="fee27-137">使用您刚才创建的预警模板创建一个名称为**预警页**的页面。</span><span class="sxs-lookup"><span data-stu-id="fee27-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="fee27-138">在新页的**主**插槽中，添加一个预警模块。</span><span class="sxs-lookup"><span data-stu-id="fee27-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="fee27-139">在预警模块的设置中，输入预警文本。</span><span class="sxs-lookup"><span data-stu-id="fee27-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="fee27-140">如果要进一步自定义预警模块，可以编辑其他属性。</span><span class="sxs-lookup"><span data-stu-id="fee27-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="fee27-141">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="fee27-141">Save and preview the page.</span></span> <span data-ttu-id="fee27-142">在页面顶部，应该会看到包含您添加的文本的预警。</span><span class="sxs-lookup"><span data-stu-id="fee27-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="fee27-143">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="fee27-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fee27-144">其他资源</span><span class="sxs-lookup"><span data-stu-id="fee27-144">Additional resources</span></span>

[<span data-ttu-id="fee27-145">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="fee27-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fee27-146">传送模块</span><span class="sxs-lookup"><span data-stu-id="fee27-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fee27-147">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="fee27-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fee27-148">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="fee27-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="fee27-149">特色模块</span><span class="sxs-lookup"><span data-stu-id="fee27-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="fee27-150">主图模块</span><span class="sxs-lookup"><span data-stu-id="fee27-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="fee27-151">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="fee27-151">Video player module</span></span>](add-video-player.md)
