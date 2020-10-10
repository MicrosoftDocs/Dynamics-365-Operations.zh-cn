---
title: 文本块模块
description: 此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817370"
---
# <a name="text-block-module"></a><span data-ttu-id="f5aa5-103">文本块模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5aa5-104">此主题介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f5aa5-105">概览</span><span class="sxs-lookup"><span data-stu-id="f5aa5-105">Overview</span></span>

<span data-ttu-id="f5aa5-106">文本块模块是用于添加文本内容的模块。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="f5aa5-107">此内容可以是参考内容或促销内容。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="f5aa5-108">文本块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="f5aa5-109">它们是不依赖于页面上下文或其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="f5aa5-110">电子商务中的文本块模块示例</span><span class="sxs-lookup"><span data-stu-id="f5aa5-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="f5aa5-111">可通过以下方式使用文本块模块：</span><span class="sxs-lookup"><span data-stu-id="f5aa5-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="f5aa5-112">在产品详细信息页中展示产品特色。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="f5aa5-113">任何页面中起到参考作用。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-113">For informational purposes on any page.</span></span> <span data-ttu-id="f5aa5-114">例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="f5aa5-115">在产品详细信息页中添加自定义消息。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="f5aa5-116">（例如，“订单金额超过 50 美元免运费”）。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="f5aa5-117">产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="f5aa5-118">下图显示了主页上使用的文本块模块的示例。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![文本块模块示例](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="f5aa5-120">文本块模块属性</span><span class="sxs-lookup"><span data-stu-id="f5aa5-120">Text block module properties</span></span>

| <span data-ttu-id="f5aa5-121">属性名称</span><span class="sxs-lookup"><span data-stu-id="f5aa5-121">Property name</span></span>     | <span data-ttu-id="f5aa5-122">值</span><span class="sxs-lookup"><span data-stu-id="f5aa5-122">Value</span></span>                                            | <span data-ttu-id="f5aa5-123">说明</span><span class="sxs-lookup"><span data-stu-id="f5aa5-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="f5aa5-124">富文本</span><span class="sxs-lookup"><span data-stu-id="f5aa5-124">Rich text</span></span>         | <span data-ttu-id="f5aa5-125">富文本</span><span class="sxs-lookup"><span data-stu-id="f5aa5-125">Rich text</span></span>                                        | <span data-ttu-id="f5aa5-126">段落文本。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-126">Paragraph text.</span></span> <span data-ttu-id="f5aa5-127">支持某些基本的富文本功能，如加粗，加下划线和斜体文本。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="f5aa5-128">自定义类名称</span><span class="sxs-lookup"><span data-stu-id="f5aa5-128">Custom class name</span></span> | <span data-ttu-id="f5aa5-129">级联样式表 (CSS) 类名称</span><span class="sxs-lookup"><span data-stu-id="f5aa5-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="f5aa5-130">开发人员提供的用于格式化此模块的自定义 CSS 类的名称。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="f5aa5-131">类名称应在主题包中定义。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="f5aa5-132">字号</span><span class="sxs-lookup"><span data-stu-id="f5aa5-132">Font size</span></span>         | <span data-ttu-id="f5aa5-133">**小**、**中**、**大**或**特大**</span><span class="sxs-lookup"><span data-stu-id="f5aa5-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="f5aa5-134">内容的字号。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="f5aa5-135">向页面添加文本块模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-135">Add a text block module to a page</span></span>

<span data-ttu-id="f5aa5-136">若要向新页面添加文本块模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f5aa5-137">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f5aa5-138">在**新建模板**对话框的**模板名称**下，输入**内容模板**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="f5aa5-139">在**正文**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5aa5-140">在**添加模块**对话框中，选择**默认页面**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5aa5-141">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f5aa5-142">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f5aa5-143">在**选择模板**对话框中，选择**内容模板**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="f5aa5-144">在**页面名称**下，输入**内容页面**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f5aa5-145">在新页面的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5aa5-146">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5aa5-147">在容器模块的属性窗格中，将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f5aa5-148">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5aa5-149">在**添加模块**对话框中，选择**文本块**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="f5aa5-150">在文本块模块的属性窗格中，将文本添加到**富文本**字段中。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="f5aa5-151">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f5aa5-152">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="f5aa5-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5aa5-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="f5aa5-153">Additional resources</span></span>

[<span data-ttu-id="f5aa5-154">模块库概述</span><span class="sxs-lookup"><span data-stu-id="f5aa5-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f5aa5-155">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f5aa5-156">传送模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f5aa5-157">内容块模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f5aa5-158">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="f5aa5-158">Video player module</span></span>](add-video-player.md)

