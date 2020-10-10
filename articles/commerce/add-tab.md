---
title: 选项卡模块
description: 此主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817026"
---
# <a name="tab-module"></a><span data-ttu-id="58fce-103">选项卡模块</span><span class="sxs-lookup"><span data-stu-id="58fce-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="58fce-104">此主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="58fce-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="58fce-105">概览</span><span class="sxs-lookup"><span data-stu-id="58fce-105">Overview</span></span>

<span data-ttu-id="58fce-106">选项卡模块是类似于容器的模块，用于组织选项卡的站点页面上的信息。</span><span class="sxs-lookup"><span data-stu-id="58fce-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="58fce-107">此类模块可以在必须在选项卡上呈现信息的任何页面上使用。</span><span class="sxs-lookup"><span data-stu-id="58fce-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="58fce-108">在每个选项卡模块中，可以添加一个或多个选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="58fce-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="58fce-109">每个选项卡项模块代表一个选项卡。在每个选项卡项模块中，可以添加一个或多个模块。</span><span class="sxs-lookup"><span data-stu-id="58fce-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="58fce-110">可添加到选项卡项模块的模块类型没有限制。</span><span class="sxs-lookup"><span data-stu-id="58fce-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="58fce-111">下图显示了站点页上的选项卡模块的示例。</span><span class="sxs-lookup"><span data-stu-id="58fce-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="58fce-112">在此示例中，已选择**装运**选项卡。</span><span class="sxs-lookup"><span data-stu-id="58fce-112">In this example, the **Shipping** tab selected.</span></span>

![选项卡模块的示例](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="58fce-114">选项卡模块属性</span><span class="sxs-lookup"><span data-stu-id="58fce-114">Tab module properties</span></span>

| <span data-ttu-id="58fce-115">属性名称</span><span class="sxs-lookup"><span data-stu-id="58fce-115">Property name</span></span> | <span data-ttu-id="58fce-116">值</span><span class="sxs-lookup"><span data-stu-id="58fce-116">Values</span></span> | <span data-ttu-id="58fce-117">说明</span><span class="sxs-lookup"><span data-stu-id="58fce-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="58fce-118">标题</span><span class="sxs-lookup"><span data-stu-id="58fce-118">Heading</span></span> | <span data-ttu-id="58fce-119">文本</span><span class="sxs-lookup"><span data-stu-id="58fce-119">Text</span></span> | <span data-ttu-id="58fce-120">此属性为选项卡模块指定可选的文本标题。</span><span class="sxs-lookup"><span data-stu-id="58fce-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="58fce-121">活动选项卡索引</span><span class="sxs-lookup"><span data-stu-id="58fce-121">Active Tab Index</span></span> | <span data-ttu-id="58fce-122">数值</span><span class="sxs-lookup"><span data-stu-id="58fce-122">Number</span></span> | <span data-ttu-id="58fce-123">此属性指定在加载页面时默认应处于活动状态的选项卡。</span><span class="sxs-lookup"><span data-stu-id="58fce-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="58fce-124">如果未提供任何值，默认第一个选项卡项处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="58fce-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="58fce-125">选项卡项模块属性</span><span class="sxs-lookup"><span data-stu-id="58fce-125">Tab item module properties</span></span>

| <span data-ttu-id="58fce-126">属性名称</span><span class="sxs-lookup"><span data-stu-id="58fce-126">Property name</span></span> | <span data-ttu-id="58fce-127">值</span><span class="sxs-lookup"><span data-stu-id="58fce-127">Values</span></span> | <span data-ttu-id="58fce-128">说明</span><span class="sxs-lookup"><span data-stu-id="58fce-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="58fce-129">职称</span><span class="sxs-lookup"><span data-stu-id="58fce-129">Title</span></span> | <span data-ttu-id="58fce-130">文本</span><span class="sxs-lookup"><span data-stu-id="58fce-130">Text</span></span> | <span data-ttu-id="58fce-131">此属性为选项卡项模块指定标题文本。</span><span class="sxs-lookup"><span data-stu-id="58fce-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="58fce-132">向页面添加选项卡模块</span><span class="sxs-lookup"><span data-stu-id="58fce-132">Add a tab module to a page</span></span>

<span data-ttu-id="58fce-133">若要向页面添加选项卡模块和设置属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="58fce-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="58fce-134">使用 Fabrikam 市场营销模板（或任何没有限制的模板）创建一个名为**商店政策页面**的新页面。</span><span class="sxs-lookup"><span data-stu-id="58fce-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="58fce-135">在**默认页**的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="58fce-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="58fce-136">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="58fce-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="58fce-137">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="58fce-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="58fce-138">在**添加模块**对话框中，选择**选项卡**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="58fce-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="58fce-139">在选项卡模块的属性窗格中，选择铅笔符号旁边的**标题**。</span><span class="sxs-lookup"><span data-stu-id="58fce-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="58fce-140">在**标题**对话框中，在**标题文本**下，输入标题文本（例如，**政策**）。</span><span class="sxs-lookup"><span data-stu-id="58fce-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="58fce-141">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="58fce-141">Then select **OK**.</span></span>
1. <span data-ttu-id="58fce-142">在**选项卡**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="58fce-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="58fce-143">在**添加模块**对话框中，选择**选项卡项**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="58fce-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="58fce-144">在选项卡项模块的属性窗格中，在**标题**下，输入标题文本（例如，**交货**）。</span><span class="sxs-lookup"><span data-stu-id="58fce-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="58fce-145">在**选项卡项**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="58fce-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="58fce-146">在**添加模块**对话框中，选择**文本块**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="58fce-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="58fce-147">在文本块模块的属性窗格中，在**富文本**下，输入一段文本。</span><span class="sxs-lookup"><span data-stu-id="58fce-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="58fce-148">在**选项卡**插槽中，再添加几个带有标题的选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="58fce-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="58fce-149">在每个选项卡项模块中，添加一个有内容的文本块模块。</span><span class="sxs-lookup"><span data-stu-id="58fce-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="58fce-150">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="58fce-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="58fce-151">页面将显示一个选项卡模块，其中包含具有您添加的内容的选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="58fce-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="58fce-152">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="58fce-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58fce-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="58fce-153">Additional resources</span></span>

[<span data-ttu-id="58fce-154">模块库概述</span><span class="sxs-lookup"><span data-stu-id="58fce-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="58fce-155">容器模块</span><span class="sxs-lookup"><span data-stu-id="58fce-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="58fce-156">可折叠模块</span><span class="sxs-lookup"><span data-stu-id="58fce-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="58fce-157">文本块模块</span><span class="sxs-lookup"><span data-stu-id="58fce-157">Text block module</span></span>](add-content-rich-block.md)
