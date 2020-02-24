---
title: 将脚本代码添加到站点页面以支持遥测
description: 此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001269"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="d39da-103">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="d39da-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d39da-104">此主题介绍如何向站点页添加客户端脚本代码来支持收集客户端遥测。</span><span class="sxs-lookup"><span data-stu-id="d39da-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="d39da-105">概览</span><span class="sxs-lookup"><span data-stu-id="d39da-105">Overview</span></span>

<span data-ttu-id="d39da-106">如果要了解客户如何与您的站点交互，并作出有助于优化最大转换体验的决策，Web 分析是至关重要的工具。</span><span class="sxs-lookup"><span data-stu-id="d39da-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="d39da-107">现在有大量 Web 分析包可帮助您实现这些目标，如 Google Analytics、Clicky、Moz Analytics 和 KISSMetrics。</span><span class="sxs-lookup"><span data-stu-id="d39da-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="d39da-108">大多数 Web 分析包都需要您在站点所有页面的 THML 的 **\<head\>** 元素中添加客户端脚本代码。</span><span class="sxs-lookup"><span data-stu-id="d39da-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="d39da-109">此主题中的说明也适用于 Microsoft Dynamics 365 Commerce 本机不提供的其他自定义客户端功能。</span><span class="sxs-lookup"><span data-stu-id="d39da-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="d39da-110">为脚本代码创建可重复使用的片段</span><span class="sxs-lookup"><span data-stu-id="d39da-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="d39da-111">为脚本代码创建片段之后，可以在站点的所有页面中重复使用该片段。</span><span class="sxs-lookup"><span data-stu-id="d39da-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="d39da-112">转到**片段 \> 新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="d39da-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="d39da-113">选择**外部脚本**，输入片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="d39da-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="d39da-114">在片段层次结构中，选择刚才创建的片段的**脚本注入程序**模块子代。</span><span class="sxs-lookup"><span data-stu-id="d39da-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="d39da-115">在右侧的属性窗格中，添加您的客户端脚本，然后根据需要设置其他配置选项。</span><span class="sxs-lookup"><span data-stu-id="d39da-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="d39da-116">将片段添加到模板</span><span class="sxs-lookup"><span data-stu-id="d39da-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="d39da-117">转到**模板**，然后打开要将脚本代码添加到的页面的模板。</span><span class="sxs-lookup"><span data-stu-id="d39da-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="d39da-118">在左侧窗格中，展开层次结构以打开 **HTML 标头**插槽。</span><span class="sxs-lookup"><span data-stu-id="d39da-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="d39da-119">选择 **HTML 标头**插槽的省略号按钮 (**...**)，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="d39da-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="d39da-120">选择为脚本代码创建的片段。</span><span class="sxs-lookup"><span data-stu-id="d39da-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="d39da-121">保存模板，然后签入。</span><span class="sxs-lookup"><span data-stu-id="d39da-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="d39da-122">完成后，必须发布片段和主模板。</span><span class="sxs-lookup"><span data-stu-id="d39da-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d39da-123">其他资源</span><span class="sxs-lookup"><span data-stu-id="d39da-123">Additional resources</span></span>

[<span data-ttu-id="d39da-124">添加徽标</span><span class="sxs-lookup"><span data-stu-id="d39da-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d39da-125">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="d39da-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d39da-126">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="d39da-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d39da-127">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="d39da-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d39da-128">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="d39da-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d39da-129">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="d39da-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d39da-130">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="d39da-130">Add languages to your site</span></span>](add-languages-to-site.md)

