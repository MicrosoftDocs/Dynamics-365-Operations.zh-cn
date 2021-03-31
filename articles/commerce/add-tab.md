---
title: 选项卡模块
description: 本主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209219"
---
# <a name="tab-module"></a><span data-ttu-id="7cfa7-103">标签模块</span><span class="sxs-lookup"><span data-stu-id="7cfa7-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7cfa7-104">本主题介绍选项卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7cfa7-105">选项卡模块是类似于容器的模块，用于组织选项卡的站点页面上的信息。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="7cfa7-106">此类模块可以在必须在选项卡上呈现信息的任何页面上使用。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="7cfa7-107">在每个选项卡模块中，可以添加一个或多个选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="7cfa7-108">每个选项卡项模块代表一个选项卡。在每个选项卡项模块中，可以添加一个或多个模块。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="7cfa7-109">可添加到选项卡项模块的模块类型没有限制。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="7cfa7-110">下图显示了站点页上的选项卡模块的示例。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="7cfa7-111">在此示例中，已选择 **装运** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-111">In this example, the **Shipping** tab selected.</span></span>

![选项卡模块的示例](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="7cfa7-113">选项卡模块属性</span><span class="sxs-lookup"><span data-stu-id="7cfa7-113">Tab module properties</span></span>

| <span data-ttu-id="7cfa7-114">属性名称</span><span class="sxs-lookup"><span data-stu-id="7cfa7-114">Property name</span></span> | <span data-ttu-id="7cfa7-115">值</span><span class="sxs-lookup"><span data-stu-id="7cfa7-115">Values</span></span> | <span data-ttu-id="7cfa7-116">说明</span><span class="sxs-lookup"><span data-stu-id="7cfa7-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="7cfa7-117">标题</span><span class="sxs-lookup"><span data-stu-id="7cfa7-117">Heading</span></span> | <span data-ttu-id="7cfa7-118">文本</span><span class="sxs-lookup"><span data-stu-id="7cfa7-118">Text</span></span> | <span data-ttu-id="7cfa7-119">此属性为选项卡模块指定可选的文本标题。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="7cfa7-120">活动选项卡索引</span><span class="sxs-lookup"><span data-stu-id="7cfa7-120">Active Tab Index</span></span> | <span data-ttu-id="7cfa7-121">数值</span><span class="sxs-lookup"><span data-stu-id="7cfa7-121">Number</span></span> | <span data-ttu-id="7cfa7-122">此属性指定在加载页面时默认应处于活动状态的选项卡。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="7cfa7-123">如果未提供任何值，默认第一个选项卡项处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="7cfa7-124">选项卡项模块属性</span><span class="sxs-lookup"><span data-stu-id="7cfa7-124">Tab item module properties</span></span>

| <span data-ttu-id="7cfa7-125">属性名称</span><span class="sxs-lookup"><span data-stu-id="7cfa7-125">Property name</span></span> | <span data-ttu-id="7cfa7-126">值</span><span class="sxs-lookup"><span data-stu-id="7cfa7-126">Values</span></span> | <span data-ttu-id="7cfa7-127">说明</span><span class="sxs-lookup"><span data-stu-id="7cfa7-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="7cfa7-128">职称</span><span class="sxs-lookup"><span data-stu-id="7cfa7-128">Title</span></span> | <span data-ttu-id="7cfa7-129">文本</span><span class="sxs-lookup"><span data-stu-id="7cfa7-129">Text</span></span> | <span data-ttu-id="7cfa7-130">此属性为选项卡项模块指定标题文本。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="7cfa7-131">向页面添加选项卡模块</span><span class="sxs-lookup"><span data-stu-id="7cfa7-131">Add a tab module to a page</span></span>

<span data-ttu-id="7cfa7-132">若要向页面添加选项卡模块和设置属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="7cfa7-133">使用 Fabrikam 市场营销模板（或任何没有限制的模板）创建一个名为 **商店政策页面** 的新页面。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="7cfa7-134">在 **默认页** 的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7cfa7-135">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7cfa7-136">在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7cfa7-137">在 **添加模块** 对话框中，选择 **选项卡** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7cfa7-138">在选项卡模块的属性窗格中，选择铅笔符号旁边的 **标题**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="7cfa7-139">在 **标题** 对话框中，在 **标题文本** 下，输入标题文本（例如，**政策**）。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="7cfa7-140">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-140">Then select **OK**.</span></span>
1. <span data-ttu-id="7cfa7-141">在 **选项卡** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7cfa7-142">在 **添加模块** 对话框中，选择 **选项卡项** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7cfa7-143">在选项卡项模块的属性窗格中，在 **标题** 下，输入标题文本（例如，**交货**）。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="7cfa7-144">在 **选项卡项** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7cfa7-145">在 **添加模块** 对话框中，选择 **文本块** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7cfa7-146">在文本块模块的属性窗格中，在 **富文本** 下，输入一段文本。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="7cfa7-147">在 **选项卡** 插槽中，再添加几个带有标题的选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="7cfa7-148">在每个选项卡项模块中，添加一个有内容的文本块模块。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="7cfa7-149">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="7cfa7-150">页面将显示一个选项卡模块，其中包含具有您添加的内容的选项卡项模块。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="7cfa7-151">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="7cfa7-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cfa7-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="7cfa7-152">Additional resources</span></span>

[<span data-ttu-id="7cfa7-153">模块库概述</span><span class="sxs-lookup"><span data-stu-id="7cfa7-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7cfa7-154">容器模块</span><span class="sxs-lookup"><span data-stu-id="7cfa7-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7cfa7-155">可折叠模块</span><span class="sxs-lookup"><span data-stu-id="7cfa7-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="7cfa7-156">文本块模块</span><span class="sxs-lookup"><span data-stu-id="7cfa7-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]