---
title: 选择站点主题
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中设置或更改站点的主题。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcee3a3f29df316dff04cf22acbda7f968778c93
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914740"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="38b60-103">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="38b60-103">Select a site theme</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="38b60-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中设置或更改站点的主题。</span><span class="sxs-lookup"><span data-stu-id="38b60-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="38b60-105">概览</span><span class="sxs-lookup"><span data-stu-id="38b60-105">Overview</span></span>

<span data-ttu-id="38b60-106">站点的布局和样式（如字体、大小和颜色）由主题定义，并应用于站点。</span><span class="sxs-lookup"><span data-stu-id="38b60-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="38b60-107">主题由公司的开发人员创建和部署。</span><span class="sxs-lookup"><span data-stu-id="38b60-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="38b60-108">有关主题概述，请参阅[主题概述](http://)。</span><span class="sxs-lookup"><span data-stu-id="38b60-108">For an overview of themes, see [Theming overview](http://).</span></span> <span data-ttu-id="38b60-109">有关如何创建和部署主题的详细信息，请参阅[创建新主题](http://)。</span><span class="sxs-lookup"><span data-stu-id="38b60-109">For more information about how to create and deploy themes, see [Create a new theme](http://).</span></span>

<span data-ttu-id="38b60-110">默认情况下，首次创建站点时，使用名称为 **Fabrikam** 的主题。</span><span class="sxs-lookup"><span data-stu-id="38b60-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="38b60-111">入门套件中提供此默认主题。</span><span class="sxs-lookup"><span data-stu-id="38b60-111">This default theme is provided as part of the starter kit.</span></span> <span data-ttu-id="38b60-112">为站点开发了更多主题之后，可以配置站点，使其改用其中之一。</span><span class="sxs-lookup"><span data-stu-id="38b60-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="38b60-113">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="38b60-113">Select the site theme</span></span>

<span data-ttu-id="38b60-114">若要选择应用于站点的主题，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="38b60-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="38b60-115">在站点创作环境中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="38b60-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="38b60-116">转到**站点管理** \> **扩展性**。</span><span class="sxs-lookup"><span data-stu-id="38b60-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="38b60-117">在**主题**下，选择下拉菜单中的一个主题。</span><span class="sxs-lookup"><span data-stu-id="38b60-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="38b60-118">若要将所选主题应用于您的站点，请选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="38b60-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="38b60-119">您在**扩展性**页面中选择**保存并发布**之后，将立即把您选择的主题发布到您的站点。</span><span class="sxs-lookup"><span data-stu-id="38b60-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="38b60-120">若要在应用主题之前在站点中预览该主题，可使用您的开发环境或沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="38b60-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38b60-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="38b60-121">Additional resources</span></span>

[<span data-ttu-id="38b60-122">添加徽标</span><span class="sxs-lookup"><span data-stu-id="38b60-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="38b60-123">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="38b60-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="38b60-124">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="38b60-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="38b60-125">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="38b60-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="38b60-126">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="38b60-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="38b60-127">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="38b60-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="38b60-128">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="38b60-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
