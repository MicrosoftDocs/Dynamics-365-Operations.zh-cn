---
title: 文本块模块
description: 此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025589"
---
# <a name="text-block-module"></a><span data-ttu-id="13258-103">文本块模块</span><span class="sxs-lookup"><span data-stu-id="13258-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="13258-104">此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="13258-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="13258-105">概览</span><span class="sxs-lookup"><span data-stu-id="13258-105">Overview</span></span>

<span data-ttu-id="13258-106">文本块模块是用于添加文本内容的模块。</span><span class="sxs-lookup"><span data-stu-id="13258-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="13258-107">此内容可以是参考内容或促销内容。</span><span class="sxs-lookup"><span data-stu-id="13258-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="13258-108">文本块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="13258-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="13258-109">它们是不依赖于页面上下文或其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="13258-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="13258-110">电子商务中的文本块模块示例</span><span class="sxs-lookup"><span data-stu-id="13258-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="13258-111">可通过以下方式使用文本块模块：</span><span class="sxs-lookup"><span data-stu-id="13258-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="13258-112">在产品详细信息页中展示产品特色。</span><span class="sxs-lookup"><span data-stu-id="13258-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="13258-113">任何页面中起到参考作用。</span><span class="sxs-lookup"><span data-stu-id="13258-113">For informational purposes on any page.</span></span> <span data-ttu-id="13258-114">例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。</span><span class="sxs-lookup"><span data-stu-id="13258-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="13258-115">在产品详细信息页中添加自定义消息。</span><span class="sxs-lookup"><span data-stu-id="13258-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="13258-116">（例如，“订单金额超过 50 美元免运费”）。</span><span class="sxs-lookup"><span data-stu-id="13258-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="13258-117">产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。</span><span class="sxs-lookup"><span data-stu-id="13258-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="13258-118">文本块模块属性</span><span class="sxs-lookup"><span data-stu-id="13258-118">Text block module properties</span></span>

| <span data-ttu-id="13258-119">属性名称</span><span class="sxs-lookup"><span data-stu-id="13258-119">Property name</span></span>     | <span data-ttu-id="13258-120">Value</span><span class="sxs-lookup"><span data-stu-id="13258-120">Value</span></span>                                            | <span data-ttu-id="13258-121">说明</span><span class="sxs-lookup"><span data-stu-id="13258-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="13258-122">富文本</span><span class="sxs-lookup"><span data-stu-id="13258-122">Rich text</span></span>         | <span data-ttu-id="13258-123">富文本</span><span class="sxs-lookup"><span data-stu-id="13258-123">Rich text</span></span>                                        | <span data-ttu-id="13258-124">段落文本。</span><span class="sxs-lookup"><span data-stu-id="13258-124">Paragraph text.</span></span> <span data-ttu-id="13258-125">支持某些基本的富文本功能，如加粗，加下划线和斜体文本。</span><span class="sxs-lookup"><span data-stu-id="13258-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="13258-126">自定义类名称</span><span class="sxs-lookup"><span data-stu-id="13258-126">Custom class name</span></span> | <span data-ttu-id="13258-127">级联样式表 (CSS) 类名称</span><span class="sxs-lookup"><span data-stu-id="13258-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="13258-128">开发人员提供的用于格式化此模块的自定义 CSS 类的名称。</span><span class="sxs-lookup"><span data-stu-id="13258-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="13258-129">类名称应在主题包中定义。</span><span class="sxs-lookup"><span data-stu-id="13258-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="13258-130">字号</span><span class="sxs-lookup"><span data-stu-id="13258-130">Font size</span></span>         | <span data-ttu-id="13258-131">**小**、**中**、**大**或**特大**</span><span class="sxs-lookup"><span data-stu-id="13258-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="13258-132">内容的字号。</span><span class="sxs-lookup"><span data-stu-id="13258-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="13258-133">向页面添加文本块模块</span><span class="sxs-lookup"><span data-stu-id="13258-133">Add a text block module to a page</span></span>

<span data-ttu-id="13258-134">若要向新页面添加文本块模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="13258-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="13258-135">创建一个名称为**内容模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="13258-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="13258-136">在**正文**插槽中，添加一个**默认页面**模块。</span><span class="sxs-lookup"><span data-stu-id="13258-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="13258-137">编辑完模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="13258-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="13258-138">使用您刚才创建的内容模板创建一个名称为**内容页**的页面。</span><span class="sxs-lookup"><span data-stu-id="13258-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="13258-139">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="13258-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="13258-140">在容器模块的属性窗格中，将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="13258-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="13258-141">向该容器模块添加一个文本块模块。</span><span class="sxs-lookup"><span data-stu-id="13258-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="13258-142">在文本块模块的属性窗格中，将文本添加到**富文本**字段中。</span><span class="sxs-lookup"><span data-stu-id="13258-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="13258-143">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="13258-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13258-144">其他资源</span><span class="sxs-lookup"><span data-stu-id="13258-144">Additional resources</span></span>

[<span data-ttu-id="13258-145">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="13258-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13258-146">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="13258-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="13258-147">传送模块</span><span class="sxs-lookup"><span data-stu-id="13258-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="13258-148">内容块模块</span><span class="sxs-lookup"><span data-stu-id="13258-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="13258-149">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="13258-149">Video player module</span></span>](add-video-player.md)

