---
title: 手风琴模块
description: 本主题介绍手风琴模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 2bb18539f610e5af05f8d9a20a0ba9f34db5c94f
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817126"
---
# <a name="accordion-module"></a><span data-ttu-id="2cfc4-103">手风琴模块</span><span class="sxs-lookup"><span data-stu-id="2cfc4-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2cfc4-104">本主题介绍手风琴模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2cfc4-105">概览</span><span class="sxs-lookup"><span data-stu-id="2cfc4-105">Overview</span></span>

<span data-ttu-id="2cfc4-106">手风琴模块是类似于容器的模块，用于通过提供可折叠的类似于抽屉的功能来组织页面上的信息或模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="2cfc4-107">手风琴模块可以在任何页面上使用。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="2cfc4-108">在每个手风琴模块内，可以添加一个或多个手风琴项模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="2cfc4-109">每个手风琴项模块都代表一个可折叠的抽屉。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="2cfc4-110">在每个手风琴项模块内，可以添加一个或多个模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="2cfc4-111">可添加到手风琴项模块的模块类型没有限制。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="2cfc4-112">下图显示了手风琴模块的示例，该模块用于组织商店的常见问题 (FAQ) 页面的信息。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![手风琴模块的示例](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="2cfc4-114">手风琴模块属性</span><span class="sxs-lookup"><span data-stu-id="2cfc4-114">Accordion module properties</span></span>

| <span data-ttu-id="2cfc4-115">属性名称</span><span class="sxs-lookup"><span data-stu-id="2cfc4-115">Property name</span></span> | <span data-ttu-id="2cfc4-116">值</span><span class="sxs-lookup"><span data-stu-id="2cfc4-116">Values</span></span> | <span data-ttu-id="2cfc4-117">说明</span><span class="sxs-lookup"><span data-stu-id="2cfc4-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2cfc4-118">标题</span><span class="sxs-lookup"><span data-stu-id="2cfc4-118">Heading</span></span> | <span data-ttu-id="2cfc4-119">文本</span><span class="sxs-lookup"><span data-stu-id="2cfc4-119">Text</span></span> | <span data-ttu-id="2cfc4-120">此属性为手风琴模块指定可选的文本标题。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="2cfc4-121">全部展开</span><span class="sxs-lookup"><span data-stu-id="2cfc4-121">Expand All</span></span> | <span data-ttu-id="2cfc4-122">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="2cfc4-122">**True** or **False**</span></span> | <span data-ttu-id="2cfc4-123">如果此值设置为 **True**，表明展开/折叠功能已打开，手风琴模块中的所有项都可以展开和折叠。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="2cfc4-124">交互样式</span><span class="sxs-lookup"><span data-stu-id="2cfc4-124">Interaction Style</span></span> | <span data-ttu-id="2cfc4-125">**独立**或**仅展开一项**</span><span class="sxs-lookup"><span data-stu-id="2cfc4-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="2cfc4-126">此属性定义手风琴项的交互样式。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="2cfc4-127">如果此值设置为**独立**，每个手风琴项都可以独立展开或折叠。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="2cfc4-128">如果此值设置为**仅展开一项**，一次只能展开一项。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="2cfc4-129">项展开时，以前展开的项将折叠。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="2cfc4-130">手风琴项模块属性</span><span class="sxs-lookup"><span data-stu-id="2cfc4-130">Accordion item module properties</span></span>

| <span data-ttu-id="2cfc4-131">属性名称</span><span class="sxs-lookup"><span data-stu-id="2cfc4-131">Property name</span></span> | <span data-ttu-id="2cfc4-132">值</span><span class="sxs-lookup"><span data-stu-id="2cfc4-132">Values</span></span> | <span data-ttu-id="2cfc4-133">说明</span><span class="sxs-lookup"><span data-stu-id="2cfc4-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="2cfc4-134">职称</span><span class="sxs-lookup"><span data-stu-id="2cfc4-134">Title</span></span> | <span data-ttu-id="2cfc4-135">文本</span><span class="sxs-lookup"><span data-stu-id="2cfc4-135">Text</span></span> | <span data-ttu-id="2cfc4-136">此属性为手风琴项模块指定标题文本。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="2cfc4-137">通过选择标题区域，用户可以展开或折叠此部分。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="2cfc4-138">默认展开</span><span class="sxs-lookup"><span data-stu-id="2cfc4-138">Expand by default</span></span> | <span data-ttu-id="2cfc4-139">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="2cfc4-139">**True** or **False**</span></span> | <span data-ttu-id="2cfc4-140">如果此值设置为 **True**，默认情况下，加载页面时会折叠手风琴项。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="2cfc4-141">将手风琴模块添加到常见问题页面</span><span class="sxs-lookup"><span data-stu-id="2cfc4-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="2cfc4-142">若要在站点构建器中将手风琴模块添加到常见问题页面，并设置模块的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2cfc4-143">转到**页面**，使用 Fabrikam 市场营销模板（或任何没有限制的模板）创建一个名为**商店常见问题**的新页面。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="2cfc4-144">在**默认页**的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cfc4-145">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cfc4-146">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cfc4-147">在**添加模块**对话框中，选择**手风琴**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cfc4-148">在手风琴模块的属性窗格中，选择铅笔符号旁边的**标题**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="2cfc4-149">在**标题**对话框中，在**标题文本**下，输入**常见问题**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="2cfc4-150">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-150">Then select **OK**.</span></span>
1. <span data-ttu-id="2cfc4-151">在手风琴模块的属性窗格中，选择**显示全部展开**复选框，然后在**交互样式**字段中，选择**独立**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="2cfc4-152">在**手风琴**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cfc4-153">在**添加模块**对话框中，选择**手风琴项**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cfc4-154">在手风琴项模块的属性窗格中，在**标题**下，输入标题文本（例如，**如何进行退货?**）。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="2cfc4-155">在**手风琴项**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cfc4-156">在**添加模块**对话框中，选择**文本块**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cfc4-157">在文本块模块的属性窗格中，输入一段文本（例如，**退货必须通过呼叫中心处理。退货请联系 1-800-FABRIKAM。产品拥有 30 天退货政策。退货必须在此时间范围内发起。**）。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="2cfc4-158">在**手风琴**插槽中，再添加几个手风琴项模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="2cfc4-159">在每个手风琴项模块中，添加一个有内容的文本块模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="2cfc4-160">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2cfc4-161">页面将显示一个包含您添加的内容的手风琴模块。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="2cfc4-162">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cfc4-163">其他资源</span><span class="sxs-lookup"><span data-stu-id="2cfc4-163">Additional resources</span></span>

[<span data-ttu-id="2cfc4-164">模块库概述</span><span class="sxs-lookup"><span data-stu-id="2cfc4-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2cfc4-165">容器模块</span><span class="sxs-lookup"><span data-stu-id="2cfc4-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2cfc4-166">标签模块</span><span class="sxs-lookup"><span data-stu-id="2cfc4-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="2cfc4-167">文本块模块</span><span class="sxs-lookup"><span data-stu-id="2cfc4-167">Text block module</span></span>](add-content-rich-block.md)
