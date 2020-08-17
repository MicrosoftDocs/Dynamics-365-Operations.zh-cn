---
title: iframe 模块
description: 此主题介绍 iframe 模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646871"
---
# <a name="iframe-module"></a><span data-ttu-id="4d2f8-103">iframe 模块</span><span class="sxs-lookup"><span data-stu-id="4d2f8-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4d2f8-104">此主题介绍 iframe 模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d2f8-105">概览</span><span class="sxs-lookup"><span data-stu-id="4d2f8-105">Overview</span></span>

<span data-ttu-id="4d2f8-106">iframe 模块提供在站点上托管外部内容的 iframe（内联框架）。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="4d2f8-107">例如，它可以用于在任何站点页面上托管 YouTube 视频或 PDF 文件查看器。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="4d2f8-108">iframe 模块需要目标 URL。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="4d2f8-109">然后，它将目标页面的内容托管在 HTML **iframe** 元素内。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="4d2f8-110">根据站点的内容安全策略 (CSP) 指令，外部 URL 必须在允许列表（也称为“白名单”）上。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="4d2f8-111">对于 iframe 内容，应使用 **frame-ancestor** 指令允许 URL。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="4d2f8-112">有关详细信息，请参阅[管理内容安全策略 (CSP)](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="4d2f8-113">下图显示了 iframe 模块的示例，这些模块在站点页面上展示外部视频。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![展示外部视频的 iframe 模块示例](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="4d2f8-115">iframe 模块属性</span><span class="sxs-lookup"><span data-stu-id="4d2f8-115">Iframe module properties</span></span>

| <span data-ttu-id="4d2f8-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="4d2f8-116">Property name</span></span>             | <span data-ttu-id="4d2f8-117">值</span><span class="sxs-lookup"><span data-stu-id="4d2f8-117">Value</span></span>                 | <span data-ttu-id="4d2f8-118">说明</span><span class="sxs-lookup"><span data-stu-id="4d2f8-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4d2f8-119">标题</span><span class="sxs-lookup"><span data-stu-id="4d2f8-119">Heading</span></span> | <span data-ttu-id="4d2f8-120">文本</span><span class="sxs-lookup"><span data-stu-id="4d2f8-120">Text</span></span> | <span data-ttu-id="4d2f8-121">模块的标题。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-121">The heading for the module.</span></span> |
| <span data-ttu-id="4d2f8-122">目标 URL</span><span class="sxs-lookup"><span data-stu-id="4d2f8-122">Target URL</span></span> | <span data-ttu-id="4d2f8-123">URL</span><span class="sxs-lookup"><span data-stu-id="4d2f8-123">URL</span></span> | <span data-ttu-id="4d2f8-124">在模块中托管的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="4d2f8-125">高度</span><span class="sxs-lookup"><span data-stu-id="4d2f8-125">Height</span></span> | <span data-ttu-id="4d2f8-126">数字或百分比</span><span class="sxs-lookup"><span data-stu-id="4d2f8-126">Number or percentage</span></span> | <span data-ttu-id="4d2f8-127">模块的高度，以像素或百分比表示。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="4d2f8-128">例如，值 **100** 将被视为像素数，值 **100%** 将被视为百分比。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="4d2f8-129">Aria 标签</span><span class="sxs-lookup"><span data-stu-id="4d2f8-129">Aria label</span></span> | <span data-ttu-id="4d2f8-130">文本</span><span class="sxs-lookup"><span data-stu-id="4d2f8-130">Text</span></span> | <span data-ttu-id="4d2f8-131">可以出于可访问性目的定义可访问丰富 Internet 应用程序 (ARIA) 标签。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="4d2f8-132">向页面添加 iframe 模块</span><span class="sxs-lookup"><span data-stu-id="4d2f8-132">Add an iframe module to a page</span></span>

<span data-ttu-id="4d2f8-133">要将 iframe 模块添加到页面上以显示外部视频，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="4d2f8-134">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4d2f8-135">在**新建模板**对话框的**模板名称**下，输入**市场营销模板**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4d2f8-136">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4d2f8-137">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4d2f8-138">在**选择模板**对话框中，选择**市场营销模板**模板。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="4d2f8-139">在**页面名称**下，输入**市场营销页面**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="4d2f8-140">在新页面的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4d2f8-141">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4d2f8-142">在模块的属性窗格中，将**宽度**值设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="4d2f8-143">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4d2f8-144">在**添加模块**对话框中，选择 **iframe** 模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4d2f8-145">在模块的属性窗格中，将**目标 URL** 值设置为视频的外部 URL。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="4d2f8-146">根据您的要求设置其他属性，如**标题**和**高度**。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="4d2f8-147">选择**保存**，选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4d2f8-148">转到您的站点上的市场营销页面。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="4d2f8-149">您应该会看到视频已在 iframe 模块中呈现。</span><span class="sxs-lookup"><span data-stu-id="4d2f8-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="4d2f8-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="4d2f8-150">Additional resources</span></span>

[<span data-ttu-id="4d2f8-151">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="4d2f8-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4d2f8-152">管理内容安全策略 (CSP)</span><span class="sxs-lookup"><span data-stu-id="4d2f8-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
