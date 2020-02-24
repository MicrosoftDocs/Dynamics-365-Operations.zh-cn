---
title: 添加欢迎消息
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001246"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="90516-103">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="90516-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="90516-104">此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="90516-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="90516-105">概览</span><span class="sxs-lookup"><span data-stu-id="90516-105">Overview</span></span>

<span data-ttu-id="90516-106">电子商务网站中的欢迎消息可告知访问者正在开展的销售、站点新闻或是否提供应季商品。</span><span class="sxs-lookup"><span data-stu-id="90516-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="90516-107">欢迎消息使用预警模块设置。</span><span class="sxs-lookup"><span data-stu-id="90516-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="90516-108">应该将预警模块添加到页眉片段的**错误/信息消息**插槽中。</span><span class="sxs-lookup"><span data-stu-id="90516-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="90516-109">可使用预警模块指定显示的文本、文本元素和对齐方式。</span><span class="sxs-lookup"><span data-stu-id="90516-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="90516-110">还可以用于指定站点访问者是否可忽略消息。</span><span class="sxs-lookup"><span data-stu-id="90516-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="90516-111">欢迎消息添加到共享页眉片段之后，将在使用以下模板的每个页面中显示：使用这个共享页眉片段的模板。</span><span class="sxs-lookup"><span data-stu-id="90516-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="90516-112">若要向站点添加欢迎消息，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="90516-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="90516-113">在 Dynamics 365 Commerce 中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="90516-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="90516-114">选择**片段**。</span><span class="sxs-lookup"><span data-stu-id="90516-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="90516-115">选择要将消息添加到的页眉片段。</span><span class="sxs-lookup"><span data-stu-id="90516-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="90516-116">在大纲树中，展开**错误/信息消息**。</span><span class="sxs-lookup"><span data-stu-id="90516-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="90516-117">选择预警模块。</span><span class="sxs-lookup"><span data-stu-id="90516-117">Select the alert module.</span></span>

    <span data-ttu-id="90516-118">如果还没有预警模块，请选择 **错误/信息消息**旁边的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="90516-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="90516-119">选择预警模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="90516-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="90516-120">在右侧的属性窗格中**数据**选项卡上，选择**添加数据源**，然后选择**内容**。</span><span class="sxs-lookup"><span data-stu-id="90516-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="90516-121">在**输入文本**字段中，输入欢迎消息的文本。</span><span class="sxs-lookup"><span data-stu-id="90516-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="90516-122">保存页眉片段，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="90516-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="90516-123">现在将在使用所选页眉片段的每个站点页顶部显示欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="90516-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90516-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="90516-124">Additional resources</span></span>

[<span data-ttu-id="90516-125">添加徽标</span><span class="sxs-lookup"><span data-stu-id="90516-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="90516-126">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="90516-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="90516-127">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="90516-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="90516-128">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="90516-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="90516-129">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="90516-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="90516-130">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="90516-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="90516-131">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="90516-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

