---
title: 将脚本代码添加到站点页面以支持遥测
description: 此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901488"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="2613a-103">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="2613a-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2613a-104">此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。</span><span class="sxs-lookup"><span data-stu-id="2613a-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="2613a-105">概览</span><span class="sxs-lookup"><span data-stu-id="2613a-105">Overview</span></span>

<span data-ttu-id="2613a-106">如果要了解客户如何与您的站点交互，并作出有助于优化最大转换体验的决策，Web 分析是至关重要的工具。</span><span class="sxs-lookup"><span data-stu-id="2613a-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="2613a-107">现在有大量 Web 分析包可帮助您实现这些目标，如 Google Analytics、Clicky、Moz Analytics 和 KISSMetrics。</span><span class="sxs-lookup"><span data-stu-id="2613a-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="2613a-108">大多数 Web 分析包都需要您在站点所有页面的 THML 的 **\<head\>** 元素中添加客户端脚本代码。</span><span class="sxs-lookup"><span data-stu-id="2613a-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="2613a-109">此主题中的说明也适用于 Microsoft Dynamics 365 Commerce 本机不提供的其他自定义客户端功能。</span><span class="sxs-lookup"><span data-stu-id="2613a-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="2613a-110">为脚本代码创建可重复使用的片段</span><span class="sxs-lookup"><span data-stu-id="2613a-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="2613a-111">片段使您可以在站点上的所有页面上重复使用内联或外部脚本代码，不管它们使用的模板是什么。</span><span class="sxs-lookup"><span data-stu-id="2613a-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="2613a-112">为内联脚本代码创建可重复使用的片段</span><span class="sxs-lookup"><span data-stu-id="2613a-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="2613a-113">要在站点构建器中为内联脚本代码创建可重复使用的片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2613a-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2613a-114">转到**片段**，然后选择**新建**.</span><span class="sxs-lookup"><span data-stu-id="2613a-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2613a-115">在**新建片段**对话框中，选择**内联脚本**。</span><span class="sxs-lookup"><span data-stu-id="2613a-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2613a-116">在**片段名称**下，输入片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2613a-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2613a-117">在您创建的片段下，选择**默认内联脚本**模块。</span><span class="sxs-lookup"><span data-stu-id="2613a-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="2613a-118">在右侧的属性窗格中，在**内联脚本**下，输入您的客户端脚本。</span><span class="sxs-lookup"><span data-stu-id="2613a-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2613a-119">然后根据需要配置其他选项。</span><span class="sxs-lookup"><span data-stu-id="2613a-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2613a-120">选择**保存**，然后选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2613a-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2613a-121">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2613a-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="2613a-122">为外部脚本代码创建可重复使用的片段</span><span class="sxs-lookup"><span data-stu-id="2613a-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="2613a-123">要在站点构建器中为外部脚本代码创建可重复使用的片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2613a-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2613a-124">转到**片段**，然后选择**新建**.</span><span class="sxs-lookup"><span data-stu-id="2613a-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2613a-125">在**新建片段**对话框中，选择**外部脚本**。</span><span class="sxs-lookup"><span data-stu-id="2613a-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2613a-126">在**片段名称**下，输入片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2613a-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2613a-127">在您创建的片段下，选择**默认外部脚本**模块。</span><span class="sxs-lookup"><span data-stu-id="2613a-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="2613a-128">在右侧的属性窗格中，在**脚本源**下，为外部脚本源添加一个外部或相对 URL。</span><span class="sxs-lookup"><span data-stu-id="2613a-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2613a-129">然后根据需要配置其他选项。</span><span class="sxs-lookup"><span data-stu-id="2613a-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2613a-130">选择**保存**，然后选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2613a-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2613a-131">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2613a-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="2613a-132">如果为您的站点启用了内容安全策略 (CSP)，请确保将所有外部 URL 添加到 Commerce 站点构建器中的 **script-src** CSP 指令。</span><span class="sxs-lookup"><span data-stu-id="2613a-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="2613a-133">有关详细信息，请参阅[管理内容安全策略 (CSP)](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="2613a-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="2613a-134">将包含脚本代码的片段添加到模板</span><span class="sxs-lookup"><span data-stu-id="2613a-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="2613a-135">要将包含脚本代码的片段添加到站点构建器中的模板，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2613a-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2613a-136">转到**模板**，然后打开要将脚本代码添加到的页面的模板。</span><span class="sxs-lookup"><span data-stu-id="2613a-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2613a-137">在左侧窗格中，展开层次结构以打开 **HTML 标头**插槽。</span><span class="sxs-lookup"><span data-stu-id="2613a-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2613a-138">在 **HTML 标头**插槽中，选择省略号按钮 (**...**)，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="2613a-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2613a-139">选择为脚本代码创建的片段。</span><span class="sxs-lookup"><span data-stu-id="2613a-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="2613a-140">选择**保存**，然后选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2613a-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2613a-141">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2613a-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="2613a-142">将外部脚本或内联脚本直接添加到模板</span><span class="sxs-lookup"><span data-stu-id="2613a-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="2613a-143">如果要将内联脚本或外部脚本直接插入由单个模板控制的一组页面中，则不必先创建片段。</span><span class="sxs-lookup"><span data-stu-id="2613a-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="2613a-144">将内联脚本直接添加到模板</span><span class="sxs-lookup"><span data-stu-id="2613a-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="2613a-145">要将内联脚本直接添加到站点构建器中的模板，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2613a-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2613a-146">转到**模板**，然后打开要将脚本代码添加到的页面的模板。</span><span class="sxs-lookup"><span data-stu-id="2613a-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2613a-147">在左侧窗格中，展开层次结构以打开 **HTML 标头**插槽。</span><span class="sxs-lookup"><span data-stu-id="2613a-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2613a-148">在 **HTML 标头**插槽中，选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2613a-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2613a-149">在**添加模块**对话框中，选择**内联脚本**。</span><span class="sxs-lookup"><span data-stu-id="2613a-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2613a-150">在右侧的属性窗格中，在**内联脚本**下，输入您的客户端脚本。</span><span class="sxs-lookup"><span data-stu-id="2613a-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2613a-151">然后根据需要配置其他选项。</span><span class="sxs-lookup"><span data-stu-id="2613a-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2613a-152">选择**保存**，然后选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2613a-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2613a-153">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2613a-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="2613a-154">将外部脚本直接添加到模板</span><span class="sxs-lookup"><span data-stu-id="2613a-154">Add an external script directly to a template</span></span>

<span data-ttu-id="2613a-155">要将外部脚本直接添加到站点构建器中的模板，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2613a-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2613a-156">转到**模板**，然后打开要将脚本代码添加到的页面的模板。</span><span class="sxs-lookup"><span data-stu-id="2613a-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2613a-157">在左侧窗格中，展开层次结构以打开 **HTML 标头**插槽。</span><span class="sxs-lookup"><span data-stu-id="2613a-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2613a-158">在 **HTML 标头**插槽中，选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2613a-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2613a-159">在**添加模块**对话框中，选择**外部脚本**。</span><span class="sxs-lookup"><span data-stu-id="2613a-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2613a-160">在右侧的属性窗格中，在**脚本源**下，为外部脚本源添加一个外部或相对 URL。</span><span class="sxs-lookup"><span data-stu-id="2613a-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2613a-161">然后根据需要配置其他选项。</span><span class="sxs-lookup"><span data-stu-id="2613a-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2613a-162">选择**保存**，然后选择**完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="2613a-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2613a-163">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2613a-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2613a-164">其他资源</span><span class="sxs-lookup"><span data-stu-id="2613a-164">Additional resources</span></span>

[<span data-ttu-id="2613a-165">添加徽标</span><span class="sxs-lookup"><span data-stu-id="2613a-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2613a-166">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="2613a-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2613a-167">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="2613a-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2613a-168">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="2613a-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2613a-169">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="2613a-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2613a-170">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="2613a-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2613a-171">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="2613a-171">Add languages to your site</span></span>](add-languages-to-site.md)
